---
layout: post
title:  "VocabHunter v1.0.17 Released"
date:   2016-09-08
image: /assets/VocabHunter-Release-v1.0.17.png
author: Adam Carroll
description: VocabHunter v1.0.17 is now available for free download for Mac, Windows and Linux
---
# New Release
![VocabHunter v1.0.17](/assets/VocabHunter-Release-v1.0.17.png)

VocabHunter v1.0.17 is now available.  Get your copy from the [download](/download) page.  The main changes in this release are:

* The status bar now shows a small graph so that you can tell at a glance how far you are through the process of analysing a document.  If you hover the mouse pointer over the graph a pop-up tooltip shows you the percentage value.  As before, you can get more detailed information in the "Progress Report" tab.

![Status Bar Mini Graph](/assets/VocabHunter-StatusBar-MiniGraph.png)

* On the subject of the status bar, this is a component from the [ControlsFX](http://fxexperience.com/controlsfx/) library which has been updated in this release to use v8.40.12.
* VocabHunter now saves the window size and position when you close the application.  The next time you start up VocabHunter, the window will open where you left it previously.
* Some users of previous versions of VocabHunter on Windows had problems when upgrading to v1.0.16.  This was caused by a change in the way that the Jackson library handles Windows paths.  This has been fixed in this release.
* The installable bundle creation is now handled using the [javafx-gradle-plugin](https://github.com/FibreFoX/javafx-gradle-plugin).  This simplifies the build and removes the need to call out to a separate Ant script.  The Gradle plugin also includes workarounds to several known problems with the bundlers.
* The log files used for troubleshooting were far too small.  This has been fixed.
* As usual, a few software libraries used internally by VocabHunter were updated.

# User Interface Testing with TestFX
[![User Interface Testing with TestFX](/assets/VocabHunter-TestFX.png)](/2016/07/27/TestFX.html)

If you're interested in automated user interface testing, take a look at the article I wrote while working on this release: [User Interface Testing with TestFX](/2016/07/27/TestFX.html).