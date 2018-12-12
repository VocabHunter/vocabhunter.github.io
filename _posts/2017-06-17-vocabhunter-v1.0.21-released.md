---
layout: post
title:  "VocabHunter v1.0.21 Released"
date:   2017-06-17
image: /assets/VocabHunter-Release-v1.0.21.png
author: Adam
description: VocabHunter v1.0.21 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v1.0.21 is now available for free download for Mac, Windows and Linux.  Filter file handling is now much faster and the user manual has been improved amongst other enhancements in this release.
---
# New Release
![VocabHunter v1.0.21](/assets/VocabHunter-Release-v1.0.21.png){: .center-image }

VocabHunter is an Open Source tool designed to help you to learn a foreign language.  v1.0.21 of VocabHunter is available now.  Get your free copy from the [download](/download) page.

The main changes in this release are:

* Filter files are now loaded in the background.  Multiple filter files load in parallel.  This makes a big difference to the overall performance of the filtering system.
* Thanks to a new version (v1.15) of [Apache Tika], VocabHunter can now read even more document formats.  The new version includes an important fix to a problem where formatting information appeared as text for certain books in the ePub electronic book format.
* [How to Use VocabHunter], the user manual has been expanded and improved.  Even if you've been using VocabHunter for a while, take a look as you might learn something new about the system:

[![How to Use VocabHunter](/assets/VocabHunter-Help.png){: .center-image }][How to Use VocabHunter]

* As usual, a few software libraries used internally by VocabHunter were updated.

VocabHunter v1.0.21 is available now as a free [download](/download).  The software is all Open Source so if you are technically-minded please feel free to [fork the repository on GitHub][GitHub] and experiment.

# Read (Almost) Any Document in Java
[![Read (Almost) Any Document in Java](/assets/VocabHunter-Read-Any-Document-Title.png){: .center-image }][Read (Almost) Any Document in Java]

If you've ever wondered how VocabHunter is able to read documents in so many varied formats from Microsoft Word through to PDF and much more, all the answers are in the article [Read (Almost) Any Document in Java], published while working on this release.

{% include share.html %}
___

# Related Articles
* [Building a JavaFX Search Bar]
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [Migrating to JUnit 5]
* [Dependency Injection in JavaFX]
* [User Interface Testing with TestFX]
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

[KingTechBlog1]:https://techblog.king.com/vocabhunter-a-tool-for-learners-of-foreign-languages/
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc

[Apache Tika]:https://tika.apache.org/
