---
layout: post
title:  "VocabHunter v1.0.22 Released"
date:   2017-12-10
image: /assets/VocabHunter-Release-v1.0.22.png
author: Adam
description: VocabHunter v1.0.22 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v1.0.22 is now available for free download for Mac, Windows and Linux.  You can now add notes to words for later study, filters are now even faster and more.
---
# New Release
![VocabHunter v1.0.22](/assets/VocabHunter-Release-v1.0.22.png){: .center-image }

VocabHunter is an Open Source tool designed to help you to learn a foreign language.  v1.0.22 of VocabHunter is available now.  Get your free copy from the [download](/download) page.

The main changes in this release are:

* The performance of word filters was improved.  If you are using multiple filter files you should find that the system starts up much more quickly and that the speed of filtering is generally improved.
* Following a feature request from a user, a new facility to add notes to words was added.  Each word now has a speech bubble icon to activate this functionality.  Press the "n" key or click the icon to add a note to a word.  These notes are saved with the VocabHunter session to make it easier to study the new vocabulary that you have found in a document.  Here you can see the basic flow for adding notes to words:

![VocabHunter Add Note to Word](/assets/VocabHunter-v1.0.22-Add-Word-Note.png){: .center-image }

* The VocabHunter tests were all moved to JUnit 5.  You can read all about how this was done in the article [Migrating to JUnit 5].
* SonarQube software quality analysis is now run on code committed to to the VocabHunter GitHub repository.  Have a look at the latest results on the [VocabHunter SonarCloud Dashboard].  This change helps to ensure that the VocabHunter codebase remains of high quality.
* VocabHunter builds now run [SpotBugs] instead of FindBugs.  Again, this helps to maintain the code quality in the system.
* As usual, a few software libraries used internally by VocabHunter were updated.

VocabHunter v1.0.22 is available now as a free [download](/download).  The software is all Open Source so if you are technically-minded please feel free to [fork the repository on GitHub][GitHub] and experiment.

# Migrating to JUnit 5
[![Migrating to JUnit 5](/assets/VocabHunter-JUnit-5-Title.png){: .center-image }][Migrating to JUnit 5]

Part of the work on this release included a major upgrade of the tests, moving to the new JUnit 5 framework.  I published the details of this in the article [Migrating to JUnit 5].

# The Road to Java 9

VocabHunter is built to work with Java 8.  Work has started to adapt the system to Java 9.  If you're interested, take a look at the experimental [VocabHunter JDK 9 branch] and the associated [VocabHunter JDK 9 milestone].

{% include share.html %}
___

# Related Articles
* [User Interface Testing with TestFX]
* [Read (Almost) Any Document in Java]
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [Building a JavaFX Search Bar]
* [Dependency Injection in JavaFX]
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)
* [Using the Java Packager with JDK 11] (Medium)

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[How to Use VocabHunter]:/help
[Migrating to JUnit 5]:/2017/10/17/migrating-to-junit-5.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[GitHub]:https://github.com/VocabHunter/VocabHunter

[KingTechBlog1]:https://medium.com/techking/vocabhunter-a-tool-for-learners-of-foreign-languages-55c467a6250c
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc

[VocabHunter SonarCloud Dashboard]:https://sonarcloud.io/dashboard?id=io.github.vocabhunter%3Avocabhunter

[VocabHunter JDK 9 branch]:https://github.com/VocabHunter/VocabHunter/tree/jdk9
[VocabHunter JDK 9 milestone]:https://github.com/VocabHunter/VocabHunter/milestone/1

[SpotBugs]:https://github.com/spotbugs/spotbugs