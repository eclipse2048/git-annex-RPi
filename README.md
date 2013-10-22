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

Install/Upgrade (adjust `$GIT_ANNEX_PATH` and `$GIT_ANNEX_BIN` if necessary):

    GIT_ANNEX_PATH=/opt/git-annex
    GIT_ANNEX_BIN=/usr/local/bin
    mkdir -p $GIT_ANNEX_PATH && cd $GIT_ANNEX_PATH
    curl -Ls  https://raw.github.com/tradloff/git-annex-RPi/master/git-annex-`curl -s https://raw.github.com/tradloff/git-annex-RPi/master/README.md | grep "Latest version" | awk '{ print $NF }'`.tar.gz | tar xvz
    ln -sf $GIT_ANNEX_PATH/git-annex $GIT_ANNEX_BIN/git-annex

