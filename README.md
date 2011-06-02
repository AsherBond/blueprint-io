# Blueprint I/O

Blueprint I/O pushes and pulls blueprints to and from a remote Blueprint I/O Server.  DevStructure provides the default Blueprint I/O Server at <https://devstructure.com> free of charge, which stores blueprints in Amazon S3.

## Installation

Prerequisites:

* A Debian- or RPM-based Linux distribution such as Debian, Ubuntu, Fedora, CentOS, or RHEL
* Python >= 2.6
* [Blueprint](https://github.com/devstructure/blueprint)

### From source on Debian, Ubuntu, and Fedora

	git clone git://github.com/devstructure/blueprint.git
	(cd blueprint && make && sudo make install)
	git clone git://github.com/devstructure/blueprint-io.git
	(cd blueprint-io && make && sudo make install)

### From source on CentOS and RHEL

	rpm -Uvh http://download.fedora.redhat.com/pub/epel/5/i386/epel-release-5-4.noarch.rpm
	yum install python26
	git clone git://github.com/devstructure/blueprint.git
	(cd blueprint && make && sudo make install PYTHON=/usr/bin/python26)
	git clone git://github.com/devstructure/blueprint-io.git
	(cd blueprint-io && make && sudo make install PYTHON=/usr/bin/python26)

This installs Python 2.6 from EPEL side-by-side with Python 2.4 and so won't break yum.

### From DevStructure's Debian archive

<pre>echo "deb http://packages.devstructure.com/<em>distro</em> <em>release</em> main" \
	| sudo tee /etc/apt/sources.list.d/devstructure.list
wget -O - http://packages.devstructure.com/keyring.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get -y install blueprint-io</pre>

Replace <code><em>distro</em></code> with "`debian`" or "`ubuntu`" and <code><em>release</em></code> with "`lenny`", "`squeeze`", "`lucid`", "`maverick`", or "`natty`" as your situation requires.

### From PyPI

	pip install blueprint_io

Make sure `pip` is using Python >= 2.6, otherwise the installation will succeed but `blueprint` will not run.

## Push your first blueprint

	blueprint push my-first-blueprint

## Documentation

Tutorials will land in the [documentation](https://devstructure.com/docs/) soon.

## Manuals

* [blueprint-push(1)](http://devstructure.github.com/blueprint-io/blueprint-push.1.html)
* [blueprint-pull(1)](http://devstructure.github.com/blueprint-io/blueprint-pull.1.html)

## Contribute

Blueprint I/O is [BSD-licensed](https://github.com/devstructure/blueprint-io/blob/master/LICENSE).

* Source code: <https://github.com/devstructure/blueprint-io>
* Issue tracker: <https://github.com/devstructure/blueprint-io/issues>
* Documentation: <https://devstructure.com/docs/>
* Wiki: <https://github.com/devstructure/blueprint-io/wiki>
* Mailing list: <https://groups.google.com/forum/#!forum/blueprint-users>
* IRC: `#devstructure` on Freenode
