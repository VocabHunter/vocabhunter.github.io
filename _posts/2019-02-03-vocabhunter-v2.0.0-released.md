---
layout: post
title:  "VocabHunter v2.0.0 Released"
date:   2019-02-03
image: /assets/VocabHunter-Release-v2.0.0.png
author: Adam
description: VocabHunter v2.0.0 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v2.0.0 is now available for free download for Mac, Windows and Linux.  Java 11 and OpenJFX 11 are now used and the installable bundle contains everything needed to run the program without the need to install Java separately.
---
# New VocabHunter Release
![VocabHunter v2.0.0](/assets/VocabHunter-Release-v2.0.0.png){: .center-image }

VocabHunter is an Open Source tool designed to help you to learn a foreign language.  v2.0.0 of VocabHunter is available now.  Get your free copy from the [download](/download) page.

The main changes in this release are:

* VocabHunter now uses JDK 11 and OpenJFX 11.  This is a big internal change that will benefit users in various ways including bringing all the performance improvements that come with the latest technology.
* The installable bundles provided for Mac, Linux and Windows are now completely self-contained.  There is no longer any need to install Java first before using the system.  The article [Using the Java Packager with JDK 11] explains how this was achieved.
* Thanks to a new version (v1.20) of Apache Tika, VocabHunter can now read even more document formats.  For more information about how Apache Tika is used to read document types ranging from PDF to Microsoft Word, see the article [Read (Almost) Any Document in Java].
* As usual, a few other software libraries used internally by VocabHunter were updated.

VocabHunter v2.0.0 is available now as a free [download](/download).  The software is all Open Source so if you are technically-minded please feel free to [fork the repository on GitHub][GitHub] and experiment.

# Using the Java Packager with JDK 11
[![Using the Java Packager with JDK 11](/assets/java-packager-jdk-11-2.png){: .center-image }][Using the Java Packager with JDK 11]

You don't need to install Java anymore to run VocabHunter.  The installable bundles on the [download](/download) page for Mac, Linux and Windows contain everything you need.  In the article [Using the Java Packager with JDK 11] you can read about how this was done.

{% include share.html %}
___

# Related Articles
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [User Interface Testing with TestFX]
* [Read (Almost) Any Document in Java]
* [Dependency Injection in JavaFX]
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)
* [Open Source & Secret Santa with Santulator] (King Tech Blog)

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:https://medium.com/@adam_carroll/building-a-javafx-search-bar-6714a27c93d7
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[How to Use VocabHunter]:/help
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[GitHub]:https://github.com/VocabHunter/VocabHunter

[KingTechBlog1]:https://medium.com/techking/vocabhunter-a-tool-for-learners-of-foreign-languages-55c467a6250c
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[Open Source & Secret Santa with Santulator]:https://medium.com/techking/open-source-secret-santa-with-santulator-9101972359fc

[VocabHunter JDK 9 branch]:https://github.com/VocabHunter/VocabHunter/tree/jdk9
[VocabHunter JDK 9 milestone]:https://github.com/VocabHunter/VocabHunter/milestone/1
