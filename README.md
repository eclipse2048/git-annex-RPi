git-annex-RPi
=============

The git-annex binary including the assistant, compiled for ARM hard float 
architectute (i.e. Raspberry Pi). 

[Git-annex](http://git-annex.branchable.com/) is an awesome piece of 
software for syncing and keeping track of files. It comes with an assistant 
and webapp to set up and sync annexes without the command line. Since the 
pre-compiled Debian packages for the Raspberry Pi and other ARM Hardware 
come without these tools, I compiled the binary with the assistant myself. 

As of yet, the webapp will not compile on ARM due to the lack of a Haskell 
compiler with support for Template Haskell. The binary also comes without 
webdav and dbus. 

Latest version in this git: 4.20130815 

