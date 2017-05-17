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

* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog) - An introduction to some of the technologies being used in VocabHunter.
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog) - A detailed look at several important features of JavaFX using VocabHunter as an example.
* [User Interface Testing with TestFX][TestFXBlog] - A guide to automating user interface tests using TestFX.
* [Dependency Injection in JavaFX][DependencyInjection] - How to implement Dependency Injection in a JavaFX application.
* [Building a JavaFX Search Bar] - How the user interface for the search bar works with details of the use of ControlsFX and FontAwesomeFX in giving the bar a distinctive style.

# Acknowledgements and Thanks

Like all good Open Source projects, VocabHunter builds on the software and work of others.  This includes but is not limited to:

* The user interface of VocabHunter is built with the [JavaFX] library that now comes as standard, as part of Java 8.
* The [Apache Tika] project provides the components that make it possible to read a wide variety of document formats.  You can learn more about this in the article [Read (Almost) Any Document in Java].
* [TestFX][TestFXProject] is used for the automated GUI test.  The detailed guide [User Interface Testing with TestFX][TestFXBlog] explains how this works.
* [ControlsFX] is used for some of the GUI components including the status bar.
* The installable bundles are created using the [javafx-gradle-plugin].
* VocabHunter uses [FontAwesomeFX] to generate various icons from the [Font Awesome] set.
* Dependency Injection is handled with [Gluon Ignite] and [Guice].  You can find out all about this in the article [Dependency Injection in JavaFX][DependencyInjection].

Finally, some acknowledgements for this website:

* Output from the [Simple Sharing Buttons Generator] was adapted for the social network sharing buttons on this site.
* The icons for the sharing buttons come from the [Social Flat Rounded Rects] set by [Aha-Soft].

[Adam Carroll]:https://github.com/AdamCarroll/
[download]:/download
[Apache Licence, Version 2.0]:http://www.apache.org/licenses/LICENSE-2.0
[GitHub]:https://github.com/VocabHunter/VocabHunter

[TestFXBlog]:/2016/07/27/TestFX.html
[DependencyInjection]:/2016/11/13/JavaFX-Dependency-Injection.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html

[KingTechBlog1]:https://techblog.king.com/vocabhunter-a-tool-for-learners-of-foreign-languages/
[KingTechBlog2]:https://techblog.king.com/javafx-used-build-desktop-application/

[JavaFX]:http://www.oracle.com/technetwork/java/javase/overview/javafx-overview-2158620.html
[Apache Tika]:https://tika.apache.org/
[TestFXProject]:https://github.com/TestFX/TestFX
[ControlsFX]:http://fxexperience.com/controlsfx/
[javafx-gradle-plugin]:https://github.com/FibreFoX/javafx-gradle-plugin
[Font Awesome]:https://fortawesome.github.io/Font-Awesome/
[FontAwesomeFX]:https://bitbucket.org/Jerady/fontawesomefx
[Gluon Ignite]:http://gluonhq.com/labs/ignite/
[Guice]:https://github.com/google/guice

[Simple Sharing Buttons Generator]:https://simplesharingbuttons.com/
[Social Flat Rounded Rects]:https://www.iconfinder.com/iconsets/social-flat-rounded-rects
[Aha-Soft]:http://www.aha-soft.com/