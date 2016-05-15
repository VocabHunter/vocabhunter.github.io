---
layout: default
title: Download
permalink: /download/
weight : 3
description: Download VocabHunter for Mac, Windows or Linux
---

VocabHunter is available for Mac, Windows and Linux.

# Install Java 8

You will need Java 8 installed and configured on your system.  You can find it on the [Java Website](https://java.com/download/).  Make sure you've got Java 8: VocabHunter won't run on earlier versions of Java.

# Apple Mac

Download the latest release here: [VocabHunter-{{site.release_version}}.dmg](https://github.com/VocabHunter/VocabHunter/releases/download/{{site.release_version}}/VocabHunter-{{site.release_version}}.dmg)

Double click the file and in the window that opens, drag the ``VocabHunter.app`` file into the ``Applications`` folder.  You should be able to launch it like any other Mac application.

# Microsoft Windows

The latest release of VocabHunter can be downloaded as a Zip file here: [VocabHunter-{{site.release_version}}.zip](https://github.com/VocabHunter/VocabHunter/releases/download/{{site.release_version}}/VocabHunter-{{site.release_version}}.zip).

First extract the contents of the Zip file into a directory.  Then run the ``VocabHunter.bat`` file found in the ``bin`` directory.  Depending on your Windows version and settings you may see an error preventing you from running the program.  If you do, click the 'More Info' hyperlink and then choose the 'Run Anyway' option.


Alternatively, you can try the experimental new Windows installer: [VocabHunter-{{site.release_version}}.exe](https://github.com/VocabHunter/VocabHunter/releases/download/{{site.release_version}}/VocabHunter-{{site.release_version}}.exe).

Double click on the file and you will be taken through the process of installing VocabHunter on your PC.

# Linux

The latest release of VocabHunter can be downloaded as a Deb file here: [VocabHunter-{{site.release_version}}.deb](https://github.com/VocabHunter/VocabHunter/releases/download/{{site.release_version}}/VocabHunter-{{site.release_version}}.deb).

You can install the package as follows:

~~~
$ sudo dpkg -i vocabhunter-{{site.release_version}}.deb
$ sudo sed -i "s|app.runtime=.*|app.runtime=$JAVA_HOME|g" /opt/VocabHunter/app/VocabHunter.cfg
~~~

VocabHunter will now run like any other Linux desktop application.

# Installing from a Zip File (Any Operating System)

The latest release of VocabHunter can be downloaded as a Zip file here: [VocabHunter-{{site.release_version}}.zip](https://github.com/VocabHunter/VocabHunter/releases/download/{{site.release_version}}/VocabHunter-{{site.release_version}}.zip).

First extract the contents of the Zip file into a directory.  Then run the ``VocabHunter`` file  (``VocabHunter.bat`` on Windows) found in the ``bin`` directory.

# Using the OpenJDK

VocabHunter works well with the OpenJDK 8 as well as the official Oracle Java.  If you choose to use the OpenJDK instead of the Oracle Java, ensure that you also have JavaFX installed.  For example, on Ubuntu 16.04 you can install the OpenJDK 8 and JavaFX as follows:

~~~
$ sudo apt-get install openjdk-8-jre
$ sudo apt-get install openjfx
~~~

# What to Do Now

Once you've installed the system and started it up you can begin hunting for vocab.  See the [help](/help) page for a guide to using VocabHunter.

To get all the latest news about VocabHunter including announcements of new releases, follow [@{{site.twitter_username}}]({{site.twitter_link}}) on Twitter.

# Older Releases

A full list of releases for download can be found on the [project release page](https://github.com/VocabHunter/VocabHunter/releases).

# Information for Techies

If you'd like to build VocabHunter from the source code and even contribute to the project, you can find it on GitHub at: [https://github.com/VocabHunter/VocabHunter](https://github.com/VocabHunter/VocabHunter).

VocabHunter is Open Source Software, published under the [Apache Licence, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).