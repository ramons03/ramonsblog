title: emacs 25 centos
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-09-22 11:46:20
tags:
---
https://gist.github.com/binarytemple-clients/0a936a9eb81db558da9b

$ sudo yum -y install libXpm-devel libjpeg-turbo-devel openjpeg-devel openjpeg2-devel turbojpeg-devel giflib-devel libtiff-devel gnutls-devel libxml2-devel GConf2-devel dbus-devel wxGTK-devel gtk3-devel
$ wget http://git.savannah.gnu.org/cgit/emacs.git/snapshot/emacs-25.1.tar.gz
$ tar zxvf emacs-25.1.tar.gz
$ cd emacs-25.1
$ ./autogen
$ ./configure --without-makeinfo # incase makeinfo is not available on your system: Example Centos 7 else `./configure` would do
$ sudo make install

## verify installation
$ which emacs
$ emacs --version
GNU Emacs 25.1.1