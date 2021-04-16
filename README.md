# README

This repository consits of two shell scripts and a README file.

### 1. extract

Syntax: <code>./extract [-f \<arg\> ] [-l] [-v] <path/to/moodle/installation> [<path/to/pluginfile[.csv]>]</code>

The path to the moodle installation is mandatory.

If no path or name for the plugin file is given it will be created in the current directory using the folder name of the Moodle installation to extract from. If no '.csv.' extension is given it will be created automatically.

Options:<br>
	-f <arg> 	: filter path of plugins to be exported by <arg> <br>
	-l 			: log extraction details. The log is a text file and will be named after the name of the moodle installation location. <br>
	-v 			: verbose - show extraction details on screen <br>

This script will extract information about all installed plugins from GIT information and stores the result in a CSV file.

### 2. build_moodle

Syntax: <code>./build_moodle [-b \<branch\>] [-f] [-c] <path/to/install/moodle> <path/to/pluginfile.csv></code>

The path to install into is mandatory. If it does not exist it will be created. If the path already contains a Moodle installation the initial Moodle installation is skipped and only the plugins will be installed.

The path to the plugin file is mandatory.

Options:<br>
	-b <branch>	: checkout <branch> after cloning core Moodle<br>
	-f 			: force re-isntallation of all plugins from the plugin file<br>
	-c 			: if a commit ID is given for a plugin checkout to that commit ID<br>

----------
version: 210414
