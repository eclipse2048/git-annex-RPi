git-annex-RPi
=============

The git-annex binary including the assistant, compiled for ARM hard float architectute (i.e. Raspberry Pi). 

[git-annex](http://git-annex.branchable.com/) is an awesome piece of software for syncing and keeping track 
of files. It comes with an assistant and webapp to take care of all the command line stuff. Since the pre-compiled 
Debian packages for the Raspberry Pi come without these additional tools, I compiled the binary with the assistant 
myself. 

As of yet, the webapp will not compile on ARM due to the lack of a Haskell compiler with support for 
Template Haskell. The binary also comes without WebDAV and dbus. 

The newest version ist 4.20130815 

