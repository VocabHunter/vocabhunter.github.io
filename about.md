---
layout: page
title: About
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

# Acknowledgements and Thanks

Like all good Open Source projects, VocabHunter builds on the software and work of others.  This includes but is not limited to:

* The user interface of VocabHunter is built with the [JavaFX] library that now comes as standard, as part of Java 8.
* The [Apache Tika] project provides the components that make it possible to read a wide variety of document formats.
* [TestFX][TestFXProject] is used for the automated GUI test.  The detailed guide [User Interface Testing with TestFX][TestFXBlog] explains how this works.
* [ControlsFX] is used for some of the GUI components including the status bar.
* The installable bundles are created using the [javafx-gradle-plugin].
* [Font Awesome] was used for various VocabHunter icons.

[Adam Carroll]:https://github.com/AdamCarroll/
[download]:/download
[Apache Licence, Version 2.0]:http://www.apache.org/licenses/LICENSE-2.0
[GitHub]:https://github.com/VocabHunter/VocabHunter

[TestFXBlog]:/2016/07/27/TestFX.html
[KingTechBlog1]:https://techblog.king.com/vocabhunter-a-tool-for-learners-of-foreign-languages/
[KingTechBlog2]:https://techblog.king.com/javafx-used-build-desktop-application/

[JavaFX]:http://www.oracle.com/technetwork/java/javase/overview/javafx-overview-2158620.html
[Apache Tika]:https://tika.apache.org/
[TestFXProject]:https://github.com/TestFX/TestFX
[ControlsFX]:http://fxexperience.com/controlsfx/
[javafx-gradle-plugin]:https://github.com/FibreFoX/javafx-gradle-plugin
[Font Awesome]:https://fortawesome.github.io/Font-Awesome/