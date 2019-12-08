---
layout: post
title:  "Migrating to JUnit 5"
date:   2017-10-17
image: /assets/VocabHunter-JUnit-5-Title.png
author: Adam
description: How an Open Source project was migrated to JUnit 5.
excerpt: VocabHunter was recently updated to use JUnit 5 for testing and this article explains how the change was made, the problems that were encountered and how they were solved.
---
![Migrating to JUnit 5](/assets/VocabHunter-JUnit-5-Title.png){: .center-image }

# Introduction

I recently took the plunge and switched the VocabHunter Open Source project over from JUnit 4 to JUnit 5.  In this article I’ll explain some of the problems I came up against and how I solved them.  I particularly focus on the changes made in the Gradle build to support JUnit 5.  I hope that the description of this experience will be useful to other people considering making the change in their projects. 

# JUnit 5

The focus of this article is on the problems encountered in making the change to JUnit 5 in a real project and how those problems were solved.  I leave the description of the new testing facilities in JUnit 5 to other references such as [A Guide to JUnit 5][BaeldungJUnit5] on the Baeldung site and the [JUnit 5 project page][JUnit5].  This article looks at the practicalities of making the changes, particularly at how to solve problems in the Gradle build script.  Suffice to say here that a lot of what is new in JUnit 5 is related to taking advantage of the new features found in Java 8.

# VocabHunter

I undertook the switch from JUnit 4 to JUnit 5 on the [VocabHunter] Open Source project.  VocabHunter is a free program to help students of foreign languages to learn new vocabulary.  You can see it in action here:

![Screenshot of VocabHunter in use](/assets/VocabHunter-in-use-2.png){: .center-image }

VocabHunter is written in Java and is built using Gradle.  A large part of this article deals with what needed to change in the Gradle build to get everything working correctly for JUnit 5.  I encourage you to fork the [VocabHunter project on GitHub][GitHub] and play around with the code.

I've tried to make the links to the VocabHunter source code as useful as possible.  Each time you see, for example, a reference to "build.gradle" you will find that the link leads you to the precise version of the file being referenced with the lines in question highlighted.

# Changing Gradually

The first thing to note is that you don’t need to change all of your tests at once.  It’s quite possible to leave existing tests in JUnit 4, create new tests in JUnit 5 and if you choose, gradually update the old tests.  To make this happen though you’ll need to update the dependency that you use for JUnit 4.  Before JUnit 5 this would be:

```groovy
dependencies {
  testCompile 'junit:junit:4.12'
  ....
}
```

To get JUnit 4 tests to run under the new engine, change the dependency as follows:

```groovy
dependencies {
  testCompile 'org.junit.vintage:junit-vintage-engine:4.12.0'
  ....
}
```

Once you start writing JUnit 5 tests you’ll need the JUnit 5 dependencies.  Here are the ones I added to the VocabHunter [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/build.gradle#L52-L58):

```groovy
testCompile 'org.junit.jupiter:junit-jupiter-api:5.0.0'
testCompile 'org.junit.jupiter:junit-jupiter-params:5.0.0'
testRuntime 'org.junit.jupiter:junit-jupiter-engine:5.0.0'
```

# Gradle Plugin

Launching the Gradle build for VocabHunter automatically runs the tests.  Once I started to convert tests from JUnit 4 to 5, I needed to add the Gradle plugin for running the tests.  Without this, the new tests didn’t get included in the build.  To define the plugin version, the following is used in [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/build.gradle#L15-L29):

```groovy
buildscript {
  ....
  dependencies {
    ....
    classpath 'org.junit.platform:junit-platform-gradle-plugin:1.0.0'
  }
}
```

The plugin is then applied in [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/build.gradle#L43) to each of the sub-projects that contain the actual Java code:

```groovy
subprojects {
  ....
  apply plugin: 'org.junit.platform.gradle.plugin'
  ....
}
```

# Mockito

VocabHunter tests make use of the excellent [Mockito] framework to create mocks.  Mockito needs to be initialised before the test begins so that the mocks can be created.  Before the change to JUnit 4, this was achieved in VocabHunter using the annotation `@RunWith(MockitoJUnitRunner.class)`.  JUnit 5 has an extension mechanism and in the future it will be possible to achieve the same effect using something such as `@ExtendWith(MockitoExtension.class)`.  However, at the time of writing, this is just a proof of concept and the supported way to do this is by explicitly calling the `initMocks()` method.  To make it easier to replace this at a later date when the annotation becomes available, wherever this initialisation is required I’ve isolated the call in a separate method:

```java
@BeforeEach
public void initMocks() {
  MockitoAnnotations.initMocks(this);
}
```

The updated version of [`TextGridManagerTest`](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/core/src/test/java/io/github/vocabhunter/analysis/grid/TextGridManagerTest.java#L42-L45) shows an example of the change in context.

# Code Coverage with Jacoco

You can find the latest test coverage information for VocabHunter [online in Codecov][Codecov].  This is automatically updated for each push of the project to GitHub as part of the Continuous Integration process.  The coverage information itself is generated using [Jacoco].  Prior to the change to JUnit 5, the Jacoco plugin was configured as follows in [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/1.0.21/build.gradle#L81-L90):

```groovy
subprojects {
  ....
  jacoco {
    toolVersion = '0.7.9'
  }

  jacocoTestReport {
    reports {
      xml.enabled true
      xml.destination "${buildDir}/reports/jacoco/report.xml"
    }
  }
  ....
}
```

After the move to JUnit 5, I needed to update the build script [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/build.gradle#L87-L105) to get Jacoco working again:

```groovy
subprojects {
  ....
  jacoco {
    toolVersion = '0.7.9'
    applyTo junitPlatformTest
  }

  if (it.name in ['core', 'gui']) {
    jacocoTestReport {
      reports {
        xml.enabled true
        xml.destination file("${buildDir}/reports/jacoco/report.xml")
      }
    }
  }

  junitPlatformTest {
    jacoco {
      destinationFile = file("$buildDir/jacoco/test.exec")
    }
  }
  ....
}
```

# JVM Arguments

The VocabHunter test suite includes an automated GUI test.  You can find more details in the article [User Interface Testing with TestFX].  If you run the test from your IDE you can watch as the robot clicks away on each of the buttons and menus as the test progresses.  However when launched from the Gradle script the GUI test will run by default in a "headless" mode so as not to bother the user and to make it easy to run the build in a continuous integration environment.  This behaviour is controlled by a Java system property that is read in the [`GuiTest`](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/gui/src/test/java/io/github/vocabhunter/gui/main/GuiTest.java#L80-L90) class:

```java
@BeforeAll
public static void setupSpec() throws Exception {
  if (Boolean.getBoolean("headless")) {
    ....
  }
  ....
}
```

The Gradle script sets the property by default, unless the build is launched with the parameter `-PnoHeadless`.  Before the change to JUnit 5, this was setup as follows in [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/1.0.21/gui/build.gradle#L53-L55):

```groovy
test {
  ....
  if (!project.hasProperty("noHeadless")) {
    jvmArgs "-Dheadless=true"
  }
}
```

With the JUnit 5 plugin I made the following change in [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/gui/build.gradle#L57-L61) to make sure that this continued to work:

```groovy
junitPlatformTest {
  if (!project.hasProperty("noHeadless")) {
    jvmArgs "-Dheadless=true"
  }
}
```

# Excluding Tests

The VocabHunter automated GUI test is an important part of the overall test suite.  However, sometimes we want to run the build quickly, skipping this test.  To make this easier I included the build parameter `-PskipGuiTests`.  If you launch the Gradle build with this parameter, everything will run as normal except the GUI test.  Before migrating to JUnit 5, this was implemented in [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/1.0.21/gui/build.gradle#L50-L52) as follows:

```groovy
test {
  if (project.hasProperty("skipGuiTests")) {
    exclude 'io/github/vocabhunter/gui/main/GuiTest*'
  }
  ....
}
```

For JUnit 5, this now changes in [build.gradle](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/gui/build.gradle#L49-L55) to:

```groovy
junitPlatform {
  if (project.hasProperty("skipGuiTests")) {
    filters {
      excludeClassNamePattern 'io.github.vocabhunter.gui.main.GuiTest'
    }
  }
}
```

# PMD Problems

The build process for VocabHunter includes static analysis of the source code to check for errors.  If problems are found then the build fails.  This helps to catch problems early on before they become bugs to be found and fixed.  Part of this static analysis is provided by the PMD plugin.  [PMD] makes use of rule sets and one of these, the "migrating" rule set, includes rules to catch problems with the use of annotations in JUnit tests.  These rules are based on the old JUnit 4 annotations and when I made the change to JUnit 5, PMD started to produce false positives.  To fix this I explicitly excluded the problematic rules from the PMD configuration file [ruleset.xml](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/config/pmd/ruleset.xml#L69-L73):

```xml
<rule ref="rulesets/java/migrating.xml">
  <exclude name="JUnit4TestShouldUseBeforeAnnotation"/>
  <exclude name="JUnit4TestShouldUseAfterAnnotation"/>
  <exclude name="JUnit4TestShouldUseTestAnnotation"/>
</rule>
```

# Tricks for Updating Tests

The first changes were easy to make and some classes were updated with a simple search and replace of the old annotations with the new.  I had several tests based on the old `@Test(expected = VocabHunterException.class)` style of exception testing that needed to be updated to the new `assertThrows()` style.  So my first job was to get all of the tests switched over to JUnit 5 so that I could remove the `org.junit.vintage:junit-vintage-engine` Gradle dependency.  After that, the more interesting work began.

One unexpected change was in the order of the parameters passed to any `assertXXX()` methods that include a message.  For example in the JUnit 4 version of [`AnalysisSystemTest`](https://github.com/VocabHunter/VocabHunter/blob/fef331140b68be9664e38bdedc216876f9e2b1e9/core/src/test/java/io/github/vocabhunter/analysis/file/AnalysisSystemTest.java#L65) you will see:

```java
assertEquals("Line number count", lineCount, lines.size());
```

Whereas in the JUnit 5 version of [`AnalysisSystemTest`](https://github.com/VocabHunter/VocabHunter/blob/a9c396e5796da72a6aeb2ce691bf034e4f8e06a2/core/src/test/java/io/github/vocabhunter/analysis/file/AnalysisSystemTest.java#L72) this changes to:

```java
assertEquals(lineCount, lines.size(), "Line number count");
```

I use IntelliJ IDEA as an IDE and this includes a feature to swap around method arguments.  I found the trick in this [Stack Overflow answer].  If you use a different IDE, you may well find you have access to a similar feature to make your task easier.

JUnit 5 includes the new `assertAll()` method for situations where you want to perform multiple assertions in a test.  The advantage of doing things the new way is that you will get information about all of the assertions that fail instead of just the first one.  This can help you to quickly track down a problem.  One way to find some of the tests that might benefit from this is to find the classes with more `assertXXX()` calls than `@Test` annotations.  The quick and dirty approach to this I took was to run the following two commands and then combine the output using [LibreOffice]:

```shell
find * -name '*Test.java' -print0 \
  | xargs -0 grep -c '^[^i].*assert' >asserts.csv
```

```shell
find * -name '*Test.java' -print0 \
  | xargs -0 grep -c '@Test' >tests.csv
```

If you open the resulting two CSV files as spreadsheets, splitting on the `:` character then you can make the comparison by copying and pasting the counts from one spreadsheet into the other.  It’s then nice and easy to see which classes have more asserts than tests.  Once you have this list you can look at the tests individually.

# Final Words

JUnit 5 is a welcome update to an already very valuable framework.   Hopefully my experience described here will save you some time if you choose to update your project to the new version.  Please feel free to [fork the VocabHunter project][GitHub] and experiment with it to see how the change to JUnit 5 works for this particular Open Source code base.  I hope you find it useful.

{% include share.html %}
___

# Related Articles
* [Using the Java Packager with JDK 11] (Medium)
* [User Interface Testing with TestFX]
* [Read (Almost) Any Document in Java]
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [Building a JavaFX Search Bar]
* [Dependency Injection in JavaFX]
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)
* [Open Source & Secret Santa with Santulator] (King Tech Blog)

[VocabHunter]:/
[GitHub]:https://github.com/VocabHunter/VocabHunter
[Codecov]:https://codecov.io/gh/VocabHunter/VocabHunter

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[KingTechBlog1]:https://medium.com/techking/vocabhunter-a-tool-for-learners-of-foreign-languages-55c467a6250c
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[Open Source & Secret Santa with Santulator]:https://medium.com/techking/open-source-secret-santa-with-santulator-9101972359fc

[JUnit5]:http://junit.org/junit5/
[BaeldungJUnit5]:http://www.baeldung.com/junit-5

[Mockito]:http://mockito.org/
[Jacoco]:http://www.eclemma.org/jacoco/
[PMD]:https://pmd.github.io/
[LibreOffice]:https://www.libreoffice.org/

[Stack Overflow answer]:https://stackoverflow.com/a/35359629