This section documents the various options that control how git works. All the options are configurable via either the _Tools > Options_ dialog (referred to as the _options dialog_) or the _Git > Properties_ dialog (referred to as the _properties dialog_). The options dialog is generally where default values can be set, and the properties dialog allows repository-specific values to be configured. Repository-specific values are stored in each repositoriy's configuration file (`.git/config`).



# User Identity #

All users should take the time to tell git what user identity should be used when committing. The user identity consists of:

  * Full Name, e.g. `Random J. Developer`
  * Email Address, e.g. `user@example.org`

From these options the user identity will become `Random J. Developer <user@example.org>`.

The name and email address can be set via both the options and properties dialogs. For repository configuration git options: `user.name` and `user.email` are used.

# Commit Options #

Some open-source projects require that developers sign off on their patches as a way of showing good faith. If you contribute to such a project, the option to automatically append a Signed-off-by line can be of assistance. The line is inserted if there are no previous commit messages. Values configure via the properties dialog are stored using the name `nbgit.signoff`.

One way to ensure that commit messages are clean and have a uniform format is to strip them of spaces at the end of line and removing consecutive empty lines. This can be done automatically if you enable it either in the module options or configure it via the properties dialog, using the `nbgit.stripspace` option.

# Update Options #

When reverting a file to a previous version, you can optionally choose to save the modified file using the prefix `.orig`. The default setting can be set in the options dialog and customized in the revert dialog.

# Custom Actions #

Custom actions are user defined commands that can be configured and run via the Git main menu. The general goal is to provide a temporary solution to some of the missing pieces of nbgit. Custom actions can be created using the wizard available via the _Custom Actions > New Action..._ item in the Git menu.

Each action definition consists of an action name, path to binary or script, arguments (which can contain replaceable tokens) and a handful of options controlling whether to show output or not. For example a use can define a "Gitk All Branches" action to run "gitk --all" in the repository root with no output shown.

Custom actions can be either repository-specific (in which case they are stored in `.git/config`) or global. Below is an example of how a repository-specific actions will appear:
```
[nbgit "action0"]
	name = Publish
	path = /home/fonseca/bin/git
	args = push github
	showOutput = true
	showDirty = true
	workDirRoot = true
```