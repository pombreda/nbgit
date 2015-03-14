NbGit is a module for the [NetBeans IDE](http://netbeans.org/) that adds support for working with the [Git version control system](http://www.git-scm.com/). It uses the [JGit](http://repo.or.cz/w/jgit.git) library created as part of [EGit](http://egit.googlecode.com/) to interact with Git repositories. Because the module is Java code all the way, it should work better cross-platform modulo platform specific differences, such as file system behavior. It is based on the NetBeans [Mercurial module](http://wiki.netbeans.org/wiki/view/MercurialVersionControl). [More...](About.md)

## Project Mission ##

The goal of this project is to provide a cross-platform Git module for NetBeans that enables developers to perform the basic and common workflows associated with version control: status, diff, commit, and history browsing. For now, more advanced and Git-specific workflows and  features, such as [rebasing branches](http://www.kernel.org/pub/software/scm/git/docs/git-rebase.html), have lower priority.

## Licensing ##

The source code is licensed under several different open source licenses; the header of each file states its terms of licensing. Most of the code is derived from the NetBeans repository and is dual licensed under the Common Development and Distribution License and the GNU General Public License Version 2 only with the "Classpath" exception. The source code and the installable NetBeans module (the ".nbm" file) is distributed with several [third-party components](Credits.md), which have different licensing than the NbGit code.

## Status and Features ##

This module is still **experimental** and may randomly crash, eat all your memory, or otherwise mess up your NetBeans IDE. Be sure to check the [known issues](Issues.md) and the [release notes](News.md) before installing and upgrading.

The module currently has the following set of features:

  * Initialize local and clone remote (only via git://) repositories.
  * IDE diff annotations and Status UI honoring .gitignore.
  * File diff and commit UI.
  * Minimal history UI and graph visualization.

## Screenshots ##

Everybody likes [screenshots](http://nbgit.googlecode.com/svn/images/) ...

![http://nbgit.googlecode.com/svn/images/early-prototype-small.png](http://nbgit.googlecode.com/svn/images/early-prototype-small.png)