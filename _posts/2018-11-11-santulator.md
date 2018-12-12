---
layout: post
title:  "Santulator"
date:   2018-11-11
image: /assets/Santulator-Summary-Card.png
author: Adam
description: Santulator is now available for free download for Mac, Windows and Linux
excerpt: Santulator is now available for free download for Mac, Windows and Linux.  Using Santulator you can easily run Secret Santa present draws for your friends or work colleagues.
---
# Santulator
[![Santulator](/assets/Santulator-Summary-Card.png){: .center-image }][Santulator Download]

I’m very pleased to announce the release of [Santulator], my new Open Source project.  Using Santulator you can easily run Secret Santa present draws for your friends or work colleagues.  As you run the whole draw on your own computer, there is no need to upload personal data to a random site on the internet.  Santulator creates a personalised PDF file for each person who will be giving a present.  For fun you can add a password to the file and help to keep the secret of the draw.  You can find everything you need to know to get started including instructions for downloading and installing on the [Santulator website][Santulator].
[![Santulator draw results](/assets/Santulator-Draw-Selection-Two-Cards.png){: .center-image }][Santulator Download]
[![Santulator draw title](/assets/Santulator-Draw-Wizard-1.gif){: .center-image }][Santulator Download]
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