---
layout: post
title:  "VocabHunter v1.0.19 Released"
date:   2016-12-11
image: /assets/VocabHunter-Release-v1.0.19.png
author: Adam Carroll
description: VocabHunter v1.0.19 is now available for free download for Mac, Windows and Linux
excerpt: VocabHunter v1.0.19 is now available for free download for Mac, Windows and Linux.  The biggest change in this release is the addition of the search functionality.  You can read all about searching and all the other new features in this post.
---
# New Release
![VocabHunter v1.0.19](/assets/VocabHunter-Release-v1.0.19.png){: .center-image }

VocabHunter v1.0.19 is now available.  Get your copy from the [download](/download) page.  The main changes in this release are:

* To make it even easier to navigate around your VocabHunter session, you can now search through your word list.  Activate the search box from the menu or by using control-F (command-F on a Mac) and start typing.  Your search results will be shown, as you type.  Partial words are allowed and accents on letters are ignored to enable a quick search.  This is what the search box looks like (see if you can spot the [ControlsFX] and [FontAwesomeFX] components):

![VocabHunter Search](/assets/VocabHunter-Search.png){: .center-image }

* [Apache Tika], the library used by VocabHunter to read a wide range of document types from Microsoft Word through to eBook formats, was updated to version 1.14.  This brings with it support for yet more document formats and better handling of existing formats.
* The menus have been switched around a little to accommodate the new search functionality.  You can see the new “Words” menu here:

![VocabHunter Words Menu](/assets/VocabHunter-Words-Menu.png){: .center-image }

* As you might have noticed, the [VocabHunter website] was changed over to use HTTPS by default, redirecting HTTP to HTTPS.  The references to the website in the program itself were updated accordingly.  Thanks to [Robin Schneider] for the pull request!
* The automated GUI test was updated to include the new search functionality and to include some other parts of the system that weren’t being tested before.
* As usual, a few software libraries used internally by VocabHunter were updated.

# Dependency Injection in JavaFX
[![Dependency Injection in JavaFX](/assets/VocabHunter-Dependency-Injection.png){: .center-image }][DependencyInjection]

I published the article [Dependency Injection in JavaFX][DependencyInjection] during my work on this latest release.  If you’re building a JavaFX application you will find that Dependency Injections brings lots of benefits in terms of writing loosely coupled, testable code.  I hope you find my guide useful!

___

# Related Articles
* [Read (Almost) Any Document in Java]
* [Building a JavaFX Search Bar]
* [User Interface Testing with TestFX][TestFXBlog]
* [How JavaFX was used to build a desktop application][KingTechBlog2] (King Tech Blog)
* [VocabHunter – A tool for learners of foreign languages][KingTechBlog1] (King Tech Blog)

[VocabHunter website]:/
[DependencyInjection]:/2016/11/13/JavaFX-Dependency-Injection.html
[TestFXBlog]:/2016/07/27/TestFX.html
[Building a JavaFX Search Bar]:/2017/01/15/Search-Bar.html
[Read (Almost) Any Document in Java]:/2017/04/30/Read-Any-Document-Format.html

[KingTechBlog1]:https://techblog.king.com/vocabhunter-a-tool-for-learners-of-foreign-languages/
[KingTechBlog2]:https://techblog.king.com/javafx-used-build-desktop-application/

[ControlsFX]:http://fxexperience.com/controlsfx/
[FontAwesomeFX]:https://bitbucket.org/Jerady/fontawesomefx
[Apache Tika]:https://tika.apache.org/
[Robin Schneider]:https://github.com/ypid
