---
layout: post
title:  "VocabHunter v1.0.18 Released"
date:   2016-11-02
image: /assets/VocabHunter-Release-v1.0.18.png
author: Adam
description: VocabHunter v1.0.18 is now available for free download for Mac, Windows and Linux
excerpt: v1.0.18 of VocabHunter is now available for download for Mac, Windows and Linux.  Read all about it here.
---
# New Release
![VocabHunter v1.0.18](/assets/VocabHunter-Release-v1.0.18.png){: .center-image }

VocabHunter v1.0.18 is now available.  Get your copy from the [download](/download) page.  The main changes in this release are:

* The icons used throughout the user interface are now generated using [FontAwesomeFX] rather than being static images.  This results in a very subtle improvement in the current look and feel of the program but more importantly makes it easier to implement future improvements.  You can see the icons in use here:

![FontAwesomeFX Icons](/assets/VocabHunter-FontAwesomeFX-Icons.png){: .center-image }

* A problem with the Linux installer has now been fixed. The problem related to the installer failing to find Java. Thanks to [Danny Althoff] for providing the fix for this. See [issue #6](https://github.com/VocabHunter/VocabHunter/issues/6) for all the details.
* The Windows installer now lets you choose the install directory rather than forcing the default. Again, thanks to [Danny Althoff] for the tip about fixing this problem.
* Loading and analysing documents now takes place in a background thread to ensure that the user interface remains responsive throughout the process.  The user also gets more feedback while this is taking place. This helps to ensure that the user feels in control and is aware of what is happening at all times.
* While files are loading and being analysed and also when sessions are being loaded, saved and exported, the filename is displayed in the status bar.  Again, this helps to keep the user informed about what is going on at all times.
* The file dialogue for selecting a document to analyse now defaults to offering a much wider range of file formats.  This makes it far more likely that the documents that the user might want to analyse are immediately shown without the need to resort to the "All Files" option.
* The Dependency Injection used in VocabHunter has been completely overhauled.  [Gluon Ignite] with [Guice] are now used throughout to manage the dependencies.  The use of Dependency Injection has been extended across far more of the system.  This change helps to ensure that the code is cleaner, more testable, well decoupled and ultimately more open and welcoming to contribution by others.
* As usual, a few software libraries used internally by VocabHunter were updated.

# How JavaFX was used to build a desktop application
[![How JavaFX was used to build a desktop application](/assets/VocabHunter-JavaFX.png){: .center-image }][KingTechBlog2]

While working on this release, I published this article on the King Tech Blog: [How JavaFX was used to build a desktop application][KingTechBlog2].  The article looks at some of the features of JavaFX used in the VocabHunter user interface and includes examples and links to the relevant code on GitHub.

{% include share.html %}
___

# Related Articles
* [Migrating to JUnit 5]
* [Read (Almost) Any Document in Java]
* [Building a JavaFX Search Bar]
* [Dependency Injection in JavaFX][DependencyInjection]
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)
* [User Interface Testing with TestFX][TestFX]
* [Using the Java Packager with JDK 11] (Medium)

[TestFX]:/2016/07/27/TestFX.html
[DependencyInjection]:/2016/11/13/JavaFX-Dependency-Injection.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Migrating to JUnit 5]:/2017/10/17/migrating-to-junit-5.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[KingTechBlog1]:https://techblog.king.com/vocabhunter-a-tool-for-learners-of-foreign-languages/
[KingTechBlog2]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[Danny Althoff]:https://github.com/FibreFoX
[FontAwesomeFX]:https://bitbucket.org/Jerady/fontawesomefx
[Gluon Ignite]:http://gluonhq.com/labs/ignite/
[Guice]:https://github.com/google/guice