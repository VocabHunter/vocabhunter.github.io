---
layout: page
permalink: /issues/
---

You can help out by reporting or fixing problems you find.

# Using the GitHub Issue Tracker

The VocabHunter project uses the GitHub issue tracker.  First of all you'll need an account with GitHub.  If you don't have an account you can create one [here](https://github.com/join).

Now log onto GitHub and go to the [VocabHunter Issues Page](https://github.com/VocabHunter/VocabHunter/issues).  Here you can see all of the reported issues.  Please first check whether the problem that you've seen has already been reported.  If it hasn't you can press 'New Issue' to report the problem.

# What to Include in the Bug Report

Please include as much relevant information as you can when you report the problem.  The following list is intended to give you an idea of the sort of information to include:

* A list of the steps to reproduce the problem.
* A screenshot illustrating the problem if the issue is a visual one.
* Are you running a Mac, Linux or Windows?
* Details of the text that you are analysing if you think that this is relevant.
* The ``system.log`` file.  See the section below for details of how to obtain this.

Please take care not to upload any copyrighted material.

# Where to Find the Log File

The `system.log` file contains information that can help to find out what VocabHunter was doing when a problem occurred.  The location of this file depends on the system you're using:

| Operating System   | Directory                                 |
|--------------------|-------------------------------------------|
| Apple OSX:         | ``~/Library/VocabHunter/logs/system.log`` |
| Microsoft Windows: | ``%APPDATA%\VocabHunter\logs\system.log`` |
| Linux:             | ``~/.VocabHunter/logs/system.log``        |

# Fixing Problems

VocabHunter is Open Source Software and the project welcomes code contributions.  If you can fix the problem yourself, please send a [GitHub Pull Request](https://help.github.com/articles/using-pull-requests/).