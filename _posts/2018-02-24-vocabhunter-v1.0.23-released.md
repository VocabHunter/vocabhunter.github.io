---
layout: post
title:  "VocabHunter v1.0.23 Released"
date:   2018-02-24
image: /assets/VocabHunter-Release-v1.0.23.png
author: Adam
description: VocabHunter v1.0.23 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v1.0.23 is now available for free download for Mac, Windows and Linux.  Performance has been improved, new documents can be analysed even faster than before and less memory is used.
---
# New Release
![VocabHunter v1.0.23](/assets/VocabHunter-Release-v1.0.23.png){: .center-image }

VocabHunter is an Open Source tool designed to help you to learn a foreign language.  v1.0.23 of VocabHunter is available now.  Get your free copy from the [download](/download) page.

The main changes in this release are:

* Document analysis speed has been significantly improved.  If you start a new VocabHunter session with, for example, a big novel, you should see that the book is analysed very quickly and that the system is ready for action much sooner than in previous versions.
* As part of the increase in performance, VocabHunter now uses less memory.  This improves the overall experience for the user.
* Thanks to a new version (v1.17) of Apache Tika, VocabHunter can now read even more document formats.  For more information about how Apache Tika is used to read document types ranging from PDF to Microsoft Word, see the article [Read (Almost) Any Document in Java].
* As usual, a few other software libraries used internally by VocabHunter were updated.

VocabHunter v1.0.23 is available now as a free [download](/download).  The software is all Open Source so if you are technically-minded please feel free to [fork the repository on GitHub][GitHub] and experiment.

# Building a JavaFX Search Bar
[![Building a JavaFX Search Bar](/assets/VocabHunter-Search-Bar-Title.png){: .center-image }][Building a JavaFX Search Bar]

While working on this release I republished the article [Building a JavaFX Search Bar] on Medium.  This post describes how a search bar was created in JavaFX and how ControlsFX and FontAwesomeFX are used in this attractive and useful new user interface component.

# Java 9 Support Coming Soon...

VocabHunter is built to work with Java 8.  Work continues to adapt the system to Java 9.  If you're interested, take a look at the experimental [VocabHunter JDK 9 branch] and the associated [VocabHunter JDK 9 milestone].

{% include share.html %}
___

# Related Articles
* [User Interface Testing with TestFX]
* [Migrating to JUnit 5]
* [Read (Almost) Any Document in Java]
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [Dependency Injection in JavaFX]
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)
* [Open Source & Secret Santa with Santulator] (King Tech Blog)
* [Using the Java Packager with JDK 11] (Medium)

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:https://medium.com/@adam_carroll/building-a-javafx-search-bar-6714a27c93d7
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[How to Use VocabHunter]:/help
[Migrating to JUnit 5]:/2017/10/17/migrating-to-junit-5.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[GitHub]:https://github.com/VocabHunter/VocabHunter

[KingTechBlog1]:https://medium.com/techking/vocabhunter-a-tool-for-learners-of-foreign-languages-55c467a6250c
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[Open Source & Secret Santa with Santulator]:https://medium.com/techking/open-source-secret-santa-with-santulator-9101972359fc

[VocabHunter JDK 9 branch]:https://github.com/VocabHunter/VocabHunter/tree/jdk9
[VocabHunter JDK 9 milestone]:https://github.com/VocabHunter/VocabHunter/milestone/1
