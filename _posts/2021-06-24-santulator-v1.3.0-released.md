---
layout: post
title:  "Santulator v1.3.0 Released"
date:   2021-06-24
image: /assets/santulator-release-v1.3.0.png
author: Adam
description: Santulator v1.3.0 is now available for free download for Mac, Windows and Linux
excerpt: Santulator v1.3.0 is now available for free download for Mac, Windows and Linux.  This release is built with the new Java 16 "jpackage" tool.
---
# New Santulator Release
[![Santulator](/assets/santulator-release-v1.3.0.png){: .center-image }][Santulator Download]

Santulator is an Open Source application for running Secret Santa draws for your friends or work colleagues.  Get your free copy of v1.3.0 from the [Santulator download page][Santulator Download].

The main improvements in this new version include:

* The installable bundle is now built with the "jpackage" tool that comes with Java 16.  All of these installable bundles are available on the [download][Santulator Download] page.  If you'd like to try out building the bundles yourself, you can find instructions [here in the project repository][PACKAGING.md].
* Important libraries such as [ControlsFX] and [OpenPDF] were updated.  My thanks to the developers of these Open Source libraries and to those of the many others that Santulator uses.

[![Santulator in use](/assets/santulator-in-use-1.png){: .center-image }][Santulator Download]
If you are interested in the technology behind Santulator, have a look at the article I wrote on the subject, [Open Source & Secret Santa with Santulator].

[![Open Source & Secret Santa with Santulator](/assets/Santulator-Open-Source-And-Secret-Santa.png){: .center-image }][Open Source & Secret Santa with Santulator]

Santulator is available for free and is Open Source software.  All of the source code can be found on [GitHub].  Santulator is written in Java using JDK 16 and has a JavaFX ([OpenJFX]) user interface.  Santulator uses the version of JDK 16 provided by [AdoptOpenJDK].

[![Download Santulator](/assets/Santulator-Download-Link.png){: .center-image }][Santulator Download]

{% include share.html %}
___

# Related Articles
* [Open Source & Secret Santa with Santulator] (King Tech Blog)
* [Building a JavaFX Search Bar]
* [Using the Java Packager with JDK 11] (Medium)
* [Read (Almost) Any Document in Java]
* [How JavaFX was used to build a desktop application] (King Tech Blog)
* [Dependency Injection in JavaFX]
* [User Interface Testing with TestFX]

[How JavaFX was used to build a desktop application]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8
[Open Source & Secret Santa with Santulator]:https://medium.com/techking/open-source-secret-santa-with-santulator-9101972359fc

[GitHub]:https://github.com/Santulator/Santulator
[Santulator]:https://santulator.github.io/
[Santulator Download]:https://santulator.github.io/download/
[PACKAGING.md]:https://github.com/Santulator/Santulator/blob/1.3.0/package/PACKAGING.md

[OpenJFX]:https://openjfx.io/
[AdoptOpenJDK]:https://adoptopenjdk.net/
[OpenPDF]:https://github.com/LibrePDF/OpenPDF
[ControlsFX]:https://github.com/controlsfx/controlsfx