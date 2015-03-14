# Installing and Updating #

Before installing or updating make sure you read the [release notes](News.md) and [list of known issues](Issues.md).

### Installing and updating using NetBeans module archives ###

The easiest way to install is to install the plugin from a .nbm file:

  * [List of .nbm files available for download](http://code.google.com/p/nbgit/downloads/list?q=label:Type-Nbm)

After downloading the .nbm file do the following:

  1. Open the _Tools > Plugins_ dialog.
  1. Choose the _Downloaded_ tab.
  1. Press the _Add Plugins..._ button and specify the path to the downloaded .nbm file.
  1. Click _Install_.

### Installing and updating from source ###

To install from source first get the source code either from a git repository or from a source code archive.

  * [List of source code archives available for download](http://code.google.com/p/nbgit/downloads/list?q=label:Type-Source)

  * [List of versioned repositories](http://code.google.com/p/nbgit/wiki/Source)

Then follow these steps:

  1. Clone the repository or unpack the archive, depending on how you choose to get the source.
  1. Open the project using the _File > Open Project_ wizard.
  1. Optionally, but highly recommended, right click on the nbgit project and select _Run_ to test the plugin.
  1. Right click on the nbgit project and select _Install/Reload in Development IDE_.