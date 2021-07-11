---
layout: post
title:  "Santulator v1.2.0 Released"
date:   2019-12-04
image: /assets/santulator-release-v1.2.0.png
author: Adam
description: Santulator v1.2.0 is now available for free download for Mac, Windows and Linux
excerpt: Santulator v1.2.0 is now available for free download for Mac, Windows and Linux.  This release makes Santulator even better and faster, especially for draws with lots of participants.
---
# New Santulator Release
[![Santulator](/assets/santulator-release-v1.2.0.png){: .center-image }][Santulator Download]

Santulator is an Open Source application for running Secret Santa draws for your friends or work colleagues.  Get your free copy of v1.2.0 from the [Santulator download page][Santulator Download].

The main improvements in this new version include:

* The core Secret Santa draw engine has been optimised so that it runs much faster than before.
* Draws with large numbers of participants are now supported.
* The PDF files containing draw results are  written to disk more quickly than previously.
* The Mac installer now includes the Santulator icon (thanks to user "PurpleAir" [for the help](https://github.com/Santulator/Santulator/issues/16)).
* A handful of minor bugs were fixed.
* Important libraries such as [ControlsFX] and [OpenPDF] were updated.  My thanks to the developers of these Open Source libraries and to those of the many others that Santulator uses.

[![Santulator in use](/assets/santulator-in-use-1.png){: .center-image }][Santulator Download]
If you are interested in the technology behind Santulator, have a look at the article I wrote on the subject, [Open Source & Secret Santa with Santulator].

[![Open Source & Secret Santa with Santulator](/assets/Santulator-Open-Source-And-Secret-Santa.png){: .center-image }][Open Source & Secret Santa with Santulator]

Santulator is available for free and is Open Source software.  All of the source code can be found on [GitHub].  Santulator is written in Java using JDK 11 and has a JavaFX ([OpenJFX 11][OpenJFX]) user interface.  The software is packaged using the [Java Packager][Using the Java Packager with JDK 11] which in turn uses JLink to build a cut-down JDK with just the modules required to run Santulator.  This means you can use the self-contained installer for Mac, Linux or Windows and have everything you need to run the program without the need to install anything else.  Santulator uses the version of JDK 11 provided by [AdoptOpenJDK].

[![Download Santulator](/assets/Santulator-Download-Link.png){: .center-image }][Santulator Download]

{% include share.html %}
___

# Related Articles
* [Installable Java Apps with jpackage]
* [Open Source & Secret Santa with Santulator] (King Tech Blog)
* [Building a JavaFX Search Bar]
* [How JavaFX was used to build a desktop application] (King Tech Blog)
* [Read (Almost) Any Document in Java]
* [User Interface Testing with TestFX]
* [Dependency Injection in JavaFX]

[How JavaFX was used to build a desktop application]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8
[Installable Java Apps with jpackage]:/2021/07/10/installable-java-apps-with-jpackage.html
[Open Source & Secret Santa with Santulator]:https://medium.com/techking/open-source-secret-santa-with-santulator-9101972359fc

[GitHub]:https://github.com/Santulator/Santulator
[Santulator]:https://santulator.github.io/
[Santulator Download]:https://santulator.github.io/download/

[OpenJFX]:https://openjfx.io/
[AdoptOpenJDK]:https://adoptopenjdk.net/
[OpenPDF]:https://github.com/LibrePDF/OpenPDF
[ControlsFX]:https://github.com/controlsfx/controlsfx