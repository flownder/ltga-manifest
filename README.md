layer-repos
===========

Install
----------

Please review the OpenEmbedded/Yocto documentation and make sure your Linux
development machine is supported and you have all the prerequisites installed:

	http://www.yoctoproject.org/docs/current/yocto-project-qs/yocto-project-qs.html

The following steps only need to be performed once, the first time you work
with this repository.

If you've never used "repo" before, or don't have "repo" installed on your
computer, you'll need to perform the following once:

	$ mkdir ~/bin
	$ export PATH=~/bin:$PATH
	$ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
	$ chmod +x ~/bin/repo

To initialize the repositories:

	$ repo init -u git://github.com/flownder/ltga-manifest.git
  
Or, if you want choise a manifestt file:

  $ repo init -u git://github.com/flownder/ltga-manifest.git -m ltga-1.0.0.xml

This will pull down the "master" branch by default. If you want to work on a
branch other than "master" simply specify it with the "-b <branch>" option to
"repo init". For example, to work with the "fido" branch:

	$ repo init -u git://github.com/flownder/ltga-manifest.git -b fido

Now that all the metadata is initialized you need to actually pull the
repositories down:

	$ repo sync
