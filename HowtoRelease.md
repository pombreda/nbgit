# Howto Release #

A mostly sequential recipe of the actions involved in forging a new release for version X.Y.

## Before releasing ##

  * Run the test suite and test general use cases: initialization, status, commit, etc.

  * Update the [News](News.md) page to mention noteworthy changes. It should list the fixed issues, labeled with [Milestone-ReleaseX.Y](http://code.google.com/p/nbgit/issues/list?q=label:Milestone-ReleaseX.Y).

  * Synchronize javahelp files with wiki pages, i.e. [News](News.md) and [Manual](http://code.google.com/p/nbgit/w/list?q=label:Manual) pages. Commit.

  * Go through [the issues](http://code.google.com/p/nbgit/issues/list?q=label:Milestone-ReleaseX.Y) assigned to the release. Retarget [any issues](http://code.google.com/p/nbgit/issues/list?can=2&q=label:Milestone-ReleaseX.Y+-status:FixPending) which will not be fixed in this released.

## The release ##

  * Update the version number and commit. The list of files include:
    * `manifest.mf`
    * `src/org/nbgit/resources/settings.xml`

  * Tag the commit:
```
git tag -s nbgit-X.Y
```
> The message title should read something like `nbgit X.Y`. Optionally, include the list of noteworthy changes in the message body.

  * Create a zip file:
```
git archive --format=zip --prefix=nbgit-X.Y/ HEAD > nbgit-X.Y.zip
```

  * Build a .nbm file with reduced dependencies:
    * Update and checkout the [release](http://github.com/jonas/nbgit/tree/release) branch
    * Merge in `master`.
    * Fix any problems: Usually missing code from the versioning.util module.
    * Commit.
    * In NetBeans build the .nbm.
    * Rename build/org-nbgit.nbm to nbgit-X.Y.nbm.

  * Push the nbgit-X.Y tag and associated commit.

  * Upload the zip and nbm files to the [download page](http://code.google.com/p/nbgit/downloads/entry). Apply labels about Type, NetBeans version, etc., as well as the **Featured** label.

## After the release ##

  * Remove Feature label from downloads related to the previous release.

  * The status of issues marked with [FixPending](http://code.google.com/p/nbgit/issues/list?q=label:FixPending) are changed to **Fixed**.

  * If they do not already exist, create the labels NbGit-X.Y and Milestone-ReleaseX.(Y+1) in [the issue tracker](http://code.google.com/p/nbgit/adminIssues).

  * Post a release announcement to the Google Group.

  * Upload the nbm to the NetBeans [Plugin Portal](http://plugins.netbeans.org/PluginPortal/faces/PluginDetailPage.jsp?pluginid=13221).

  * Announce the release on other sites: [Freshmeat](http://freshmeat.net/projects/nbgit/).