---
layout: post
title:  "VocabHunter v2.3.0 Released"
date:   2021-06-13
image: /assets/VocabHunter-Release-v2.3.0.png
author: Adam
description: VocabHunter v2.3.0 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v2.3.0 is now available for free download for Mac, Windows and Linux.  This release is built with the new Java 16 "jpackage" tool.
---
# New VocabHunter Release
![VocabHunter v2.3.0](/assets/VocabHunter-Release-v2.3.0.png){: .center-image }

VocabHunter is an Open Source tool designed to help you to learn a foreign language.  v2.3.0 of VocabHunter is available now.  Get your free copy from the [download](/download) page.

The main changes in this release are:

* The installable bundle is now built with the "jpackage" tool that comes with Java 16.  All of these installable bundles are available on the [download](/download) page.  If you'd like to try out building the bundles yourself, you can find instructions [here in the project repository][PACKAGING.md].
* Thanks to a new version (v1.26) of Apache Tika, VocabHunter can now read even more document formats.  You can learn about how Apache Tika is used to read document types ranging from PDF to Microsoft Word in the article [Read (Almost) Any Document in Java].
* A handful of minor bugs were fixed and the versions of the Open Source libraries used in the software were all updated.

VocabHunter v2.3.0 is available now as a free [download](/download).  The software is all Open Source so if you are technically-minded please feel free to [fork the repository on GitHub][GitHub] and experiment.

# Installable Java Apps with jpackage
[![Installable Java Apps with jpackage](/assets/jpackage-installable-java-apps.png){: .center-image }][Installable Java Apps with jpackage]

There is no need to install Java if you want to use VocabHunter.  Everything you need is contained in the installable bundles you'll find on the [download page](/download).  If you'd like to know how this is achieved, have a look at the article [Installable Java Apps with jpackage].

{% include share.html %}
___

# Related Articles
* [Dependency Injection in JavaFX]
* [User Interface Testing with TestFX]
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [Read (Almost) Any Document in Java]
* [Open Source & Secret Santa with Santulator] (King Tech Blog)
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:https://medium.com/@adam_carroll/building-a-javafx-search-bar-6714a27c93d7
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Installable Java Apps with jpackage]:/2021/07/10/installable-java-apps-with-jpackage.html

[GitHub]:https://github.com/VocabHunter/VocabHunter
[PACKAGING.md]:https://github.com/VocabHunter/VocabHunter/blob/master/package/PACKAGING.md

[KingTechBlog1]:https://medium.com/techking/vocabhunter-a-tool-for-learners-of-foreign-languages-55c467a6250c
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[Open Source & Secret Santa with Santulator]:https://medium.com/techking/open-source-secret-santa-with-santulator-9101972359fc
