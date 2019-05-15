---
layout: post
title:  "VocabHunter v2.1.0 Released"
date:   2019-05-15
image: /assets/VocabHunter-Release-v2.1.0.png
author: Adam
description: VocabHunter v2.1.0 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v2.1.0 is now available for free download for Mac, Windows and Linux.  This release includes a new facility to export your list of selected words along with any notes you have attached to them.
---
# New VocabHunter Release
![VocabHunter v2.1.0](/assets/VocabHunter-Release-v2.1.0.png){: .center-image }

VocabHunter is an Open Source tool designed to help you to learn a foreign language.  v2.1.0 of VocabHunter is available now.  Get your free copy from the [download](/download) page.

The main changes in this release are:

* Following user feedback, when you export your list of words, any notes you have added will be exported alongside the words.  If you really just want the words without the notes, use the "Export Selection Without Notes" option in the "Words" menu.
* VocabHunter now runs using version 11.0.3 of Java from [AdoptOpenJDK].  This is bundled with VocabHunter so there is no need to install Java separately.
* A handful of minor bugs were fixed and the versions of the Open Source libraries used in the software were all updated.

VocabHunter v2.1.0 is available now as a free [download](/download).  The software is all Open Source so if you are technically-minded please feel free to [fork the repository on GitHub][GitHub] and experiment.

# Using the Java Packager with JDK 11
[![Using the Java Packager with JDK 11](/assets/java-packager-jdk-11-2.png){: .center-image }][Using the Java Packager with JDK 11]

There is no need to install Java if you want to use VocabHunter.  Everything you need is contained in the installable bundles you'll find on the [download page](/download).  If you'd like to know how this is achieved, have a look at the article [Using the Java Packager with JDK 11].

{% include share.html %}
___

# Related Articles
* [User Interface Testing with TestFX]
* [Open Source & Secret Santa with Santulator] (King Tech Blog)
* [Read (Almost) Any Document in Java]
* [Dependency Injection in JavaFX]
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)

[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:https://medium.com/@adam_carroll/building-a-javafx-search-bar-6714a27c93d7
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[GitHub]:https://github.com/VocabHunter/VocabHunter

[KingTechBlog1]:https://medium.com/techking/vocabhunter-a-tool-for-learners-of-foreign-languages-55c467a6250c
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[Open Source & Secret Santa with Santulator]:https://medium.com/techking/open-source-secret-santa-with-santulator-9101972359fc

[AdoptOpenJDK]:https://adoptopenjdk.net/
