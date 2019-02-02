---
layout: page
title: About VocabHunter
short_title: About
permalink: /about/
weight : 2
description: About VocabHunter, acknowledgements and thanks
image: /assets/VocabHunter-About.png
---

VocabHunter is a system to help learners of foreign languages.  See the [download] page for details on how to download and run the program.  You can follow VocabHunter on Twitter at [@{{site.twitter.username}}]({{site.twitter.link}}).

The system is Open Source Software, published under the [Apache Licence, Version 2.0].  You can find the source code on GitHub [here][GitHub].

[Adam Carroll] is the principal author of VocabHunter.

# Technical Articles

* [Read (Almost) Any Document in Java] - VocabHunter uses Apache Tika to read documents in a wide variety of formats ranging from Microsoft Word through to PDF.  This article explains how it is done.
* [How JavaFX was used to build a desktop application] (King Tech Blog) - A detailed look at several important features of JavaFX using VocabHunter as an example.
* [Migrating to JUnit 5] - How the VocabHunter project was updated to use JUnit 5 for testing.  This article explains the changes that were made, the problems that were encountered and how they were solved.
* [Dependency Injection in JavaFX] - How to Gluon Ignite and Google Guice are used for the  Dependency Injection in VocabHunter.
* [User Interface Testing with TestFX] - A guide to automating user interface tests using TestFX.  VocabHunter includes a complete automated GUI test suite and here you can learn how it works.
* [Building a JavaFX Search Bar] - How the user interface for the VocabHunter search bar works with details of the use of ControlsFX and FontAwesomeFX in giving the bar a distinctive style.
* [VocabHunter – A tool for learners of foreign languages] (King Tech Blog) - An introduction to some of the technologies being used in VocabHunter.

# Acknowledgements and Thanks

Like all good Open Source projects, VocabHunter builds on the software and work of others.  This includes but is not limited to:

* The user interface of VocabHunter is built with the [JavaFX], now developed under the Open Source OpenJFX project.
* [TestFX][TestFXProject] is used for the automated GUI test.  The detailed guide [User Interface Testing with TestFX] explains how this works.
* [ControlsFX] is used for some of the GUI components including the status bar.
* The [Apache Tika] project provides the components that make it possible to read a wide variety of document formats.  You can learn more about this in the article [Read (Almost) Any Document in Java].
* VocabHunter uses [FontAwesomeFX] to generate various icons from the [Font Awesome] set.
* Dependency Injection is handled with [Gluon Ignite] and [Guice].  You can find out all about this in the article [Dependency Injection in JavaFX].
* [JUnit] is used as the principle testing framework.  [Migrating to JUnit 5] explains how the VocabHunter project was migrated to the latest verson of JUnit.
* There is a separate installer for Mac, Linux and Windows, each one tailored to the operating system in question.  These installable bundles are self-contained so that the user doesn't need to have to worry about first installing Java or any other special setup.  The article [Using the Java Packager with JDK 11] explains how this was achieved.

Finally, some acknowledgements for this website:

* Output from the [Simple Sharing Buttons Generator] was adapted for the social network sharing buttons on this site.
* The icons for the sharing buttons come from the [Social Flat Rounded Rects] set by [Aha-Soft].

[Adam Carroll]:https://github.com/AdamCarroll/
[download]:/download
[Apache Licence, Version 2.0]:http://www.apache.org/licenses/LICENSE-2.0
[GitHub]:https://github.com/VocabHunter/VocabHunter

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Migrating to JUnit 5]:/2017/10/17/migrating-to-junit-5.html

[VocabHunter – A tool for learners of foreign languages]:https://medium.com/techking/vocabhunter-a-tool-for-learners-of-foreign-languages-55c467a6250c
[How JavaFX was used to build a desktop application]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[JavaFX]:https://openjfx.io/
[Apache Tika]:https://tika.apache.org/
[TestFXProject]:https://github.com/TestFX/TestFX
[ControlsFX]:http://fxexperience.com/controlsfx/
[Font Awesome]:https://fortawesome.github.io/Font-Awesome/
[FontAwesomeFX]:https://bitbucket.org/Jerady/fontawesomefx
[Gluon Ignite]:http://gluonhq.com/labs/ignite/
[Guice]:https://github.com/google/guice
[JUnit]:http://junit.org/

[Simple Sharing Buttons Generator]:https://simplesharingbuttons.com/
[Social Flat Rounded Rects]:https://www.iconfinder.com/iconsets/social-flat-rounded-rects
[Aha-Soft]:http://www.aha-soft.com/