---
layout: post
title:  "VocabHunter v1.0.20 Released"
date:   2017-04-02
image: /assets/VocabHunter-Release-v1.0.20.png
author: Adam
description: VocabHunter v1.0.20 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v1.0.20 is now available for free download for Mac, Windows and Linux.  This release comes with new filtering functionality to make it even easier to focus on just the vocabulary that interests you.
---
# New Release
![VocabHunter v1.0.20](/assets/VocabHunter-Release-v1.0.20.png){: .center-image }

VocabHunter v1.0.20 is now available.  Get your copy from the [download](/download) page.  The main changes in this release are:

* The word filtering functionality has been overhauled to make it even more useful.  First of all you can easily add and edit filters from the main dialogue:

![VocabHunter Filter Dialogue](/assets/VocabHunter-v1.0.20-Filter-Dialogue.png){: .center-image }

* Your saved VocabHunter session files can be used as filters and you can now clearly see the words that will be included in the filter:

![VocabHunter Sesson Filter](/assets/VocabHunter-v1.0.20-Session-Filter.png){: .center-image }

* If you're studying a foreign language and keep track of word lists either in text documents or in spreadsheets, you can use these files as filters:

![VocabHunter Word List Filter](/assets/VocabHunter-v1.0.20-Word-List-Filter.png){: .center-image }

* The VocabHunter test coverage is published on the new [VocabHunter Codecov dashboard] after each commit.
* The automated user interface test now covers even more of the system, including the new filtering functionality.  You can find out more about how the automated GUI test works in the article [User Interface Testing with TestFX].
* As usual, a few software libraries used internally by VocabHunter were updated.  This includes a new version of [FontAwesomeFX] that fixes a problem with the icons on 32-bit Java.

# Building a JavaFX Search Bar
[![Building a JavaFX Search Bar](/assets/VocabHunter-Search-Bar-Title.png){: .center-image }][Building a JavaFX Search Bar]

While working on this release I published the article [Building a JavaFX Search Bar].  This post describes how a search bar was created in JavaFX and how ControlsFX and FontAwesomeFX are used in this attractive and useful new user interface component.

{% include share.html %}
___

# Related Articles
* [Migrating to JUnit 5]
* [Read (Almost) Any Document in Java]
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [Dependency Injection in JavaFX]
* [User Interface Testing with TestFX]
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)
* [Using the Java Packager with JDK 11] (Medium)

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Migrating to JUnit 5]:/2017/10/17/migrating-to-junit-5.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[KingTechBlog1]:https://techblog.king.com/vocabhunter-a-tool-for-learners-of-foreign-languages/
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc

[VocabHunter Codecov dashboard]:https://codecov.io/gh/VocabHunter/VocabHunter

[FontAwesomeFX]:https://bitbucket.org/Jerady/fontawesomefx
