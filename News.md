#summary Information about releases.
#labels Manual,Featured
#sidebar TableOfContents

# Release Notes #

News about features and issues that have been resolved.

### nbgit v0.3 (2009-08-30) ###

New features:

  * Initial support for cloning; Only git:// protocol is supported for now. ([issue 48](https://code.google.com/p/nbgit/issues/detail?id=48))
  * Graph visualization of repository history. ([issue 1](https://code.google.com/p/nbgit/issues/detail?id=1))
  * Check email addresses entered though the properties UI. ([issue 4](https://code.google.com/p/nbgit/issues/detail?id=4))

Bug fixes:

  * Track changes to and refresh internally cached .gitignore files. ([issue 3](https://code.google.com/p/nbgit/issues/detail?id=3))
  * Gracefully handle repositories containing submodules. ([issue 23](https://code.google.com/p/nbgit/issues/detail?id=23), [issue 33](https://code.google.com/p/nbgit/issues/detail?id=33), [issue 34](https://code.google.com/p/nbgit/issues/detail?id=34))
  * Fix revert when using folder/project selection. ([issue 51](https://code.google.com/p/nbgit/issues/detail?id=51))

### nbgit v0.2 (2009-08-07) ###

New features:

  * Optionally strip spaces from commit messages. ([issue 8](https://code.google.com/p/nbgit/issues/detail?id=8))
  * Support for .gitignore files. ([issue 3](https://code.google.com/p/nbgit/issues/detail?id=3))

Bug fixes:

  * Make code compatible with Java 1.5. ([issue 22](https://code.google.com/p/nbgit/issues/detail?id=22) and [issue 21](https://code.google.com/p/nbgit/issues/detail?id=21))
  * Update the status cache after creating a repository. ([issue 24](https://code.google.com/p/nbgit/issues/detail?id=24))
  * Bundle version utilities with the nbm file. ([issue 19](https://code.google.com/p/nbgit/issues/detail?id=19))

### nbgit v0.1 (2008-09-10) ###

New features:

  * init: Create a new git repository.
  * status: List the status of changed files.
  * diff: View changes to files (side-by-side).
  * commit: Commit a selected range of files.
  * log: Search and view revisions.
  * update: Revert individual file changes.
  * properties: Change repository specific options (i.e. user.name and user.email).
  * custom: User defined commands (e.g. to open gitk). ([issue 16](https://code.google.com/p/nbgit/issues/detail?id=16))

Resolved issues:

  * Prefill the history summary view when opened. ([issue 5](https://code.google.com/p/nbgit/issues/detail?id=5))
  * Optionally insert Signed-off-by line in commit messages. ([issue 7](https://code.google.com/p/nbgit/issues/detail?id=7))
  * Reorder class path extensions to allow nbgit to be opened in NetBeans 6.5beta. ([issue 14](https://code.google.com/p/nbgit/issues/detail?id=14))