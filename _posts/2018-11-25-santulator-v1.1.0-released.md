---
layout: post
title:  "Santulator v1.1.0 Released"
date:   2018-11-25
image: /assets/santulator-release-v1.1.0.png
author: Adam
description: Santulator v1.1.0 is now available for free download for Mac, Windows and Linux
excerpt: Santulator v1.1.0 is now available for free download for Mac, Windows and Linux.  You can now import a spreadsheet containing the names of the participants in the Secret Santa draw.
---
# New Santulator Release
[![Santulator](/assets/santulator-release-v1.1.0.png){: .center-image }][Santulator Download]

Santulator is an Open Source application for running Secret Santa draws for your friends or work colleagues.  Get your free copy of v1.1.0 from the [Santulator download page][Santulator Download].

Following feedback from users, the new version includes a facility to import a spreadsheet containing the names of the participants.
[![Santulator in use](/assets/santulator-in-use-1.png){: .center-image }][Santulator Download]
Santulator is available for free and is Open Source software.  All of the source code can be found on [GitHub].  Santulator is written in Java using JDK 11 and has a JavaFX ([OpenJFX 11][OpenJFX]) user interface.  The software is packaged using the [Java Packager] which in turn uses JLink to build a cut-down JDK with just the modules required to run Santulator.  This means you can use the self-contained installer for Mac, Linux or Windows and have everything you need to run the program without the need to install anything else.  Santulator uses the version of JDK 11 provided by [AdoptOpenJDK].

[![Download Santulator](/assets/Santulator-Download-Link.png){: .center-image }][Santulator Download]

{% include share.html %}
___

# Related Articles
* [Using the Java Packager with JDK 11] (Medium)
* [How JavaFX was used to build a desktop application] (King Tech Blog)
* [User Interface Testing with TestFX]
* [Dependency Injection in JavaFX]
* [Building a JavaFX Search Bar]
* [Read (Almost) Any Document in Java]

[How JavaFX was used to build a desktop application]:https://medium.com/techking/how-javafx-was-used-to-build-a-desktop-application-7d4c680d8dc
[User Interface Testing with TestFX]:/2016/07/27/TestFX.html
[Dependency Injection in JavaFX]:/2016/11/13/JavaFX-Dependency-Injection.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html
[Using the Java Packager with JDK 11]:https://medium.com/@adam_carroll/java-packager-with-jdk11-31b3d620f4a8

[GitHub]:https://github.com/Santulator/Santulator
[Santulator]:https://santulator.github.io/
[Santulator Download]:https://santulator.github.io/download/

[OpenJFX]:https://openjfx.io/
[Java Packager]:https://mail.openjdk.java.net/pipermail/openjfx-dev/2018-September/022500.html
[AdoptOpenJDK]:https://adoptopenjdk.net/