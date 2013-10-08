git-annex-RPi
=============

The git-annex binary including the assistant, compiled for ARMv6 
architecture (namely, the [Raspberry Pi](http://www.raspberrypi.org/)). 

[Git-annex](http://git-annex.branchable.com/) is an awesome piece of 
software for syncing and keeping track of files. It comes with an assistant 
and webapp to set up and sync repositories without the command line. Since the 
pre-compiled Debian packages for the Raspberry Pi and other ARM hardware 
come without these tools, I compiled the binary with the assistant myself. 

As of yet, the webapp will not compile on ARM due to the lack of a Haskell 
compiler that supports Template Haskell. The binary also comes without 
webdav. 

Latest version in this git: 4.20130909

Install dependencies:

    apt-get install libgsasl7

Install/Upgrade (`$GARP_PATH` and `$GARP_BIN` will be overwritten):

    GARP_PATH=/opt/git-annex
    GARP_BIN=/usr/local/bin
    mkdir -p $GARP_PATH && cd $GARP_PATH
    curl -Ls  https://raw.github.com/tradloff/git-annex-RPi/master/git-annex-`curl -s https://raw.github.com/tradloff/git-annex-RPi/master/README.md | grep "Latest version" | awk '{ print $NF }'`.tar.gz | tar xvz
    ln -sf $GARP_PATH/git-annex /usr/local/bin/git-annex

