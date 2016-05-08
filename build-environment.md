
HOWTO setup a build environment to build a freetz image for FRITZ!Box home routers based on Ubuntu 16.04 (should work with earlier version too). Short codelisting for further reference. Useful to spin up an instance on vultr / digitalocean etc

    apt-get update
    apt-get upgrade
    adduser freetz --disabled-password

    # http://freetz.org/wiki/help/howtos/common/install
    # realtime priority: "no"
    # nevermind missing packages
    apt-get install imagemagick subversion git gcc g++ binutils autoconf automake autopoint libtool-bin make bzip2 libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config ecj fastjar realpath perl libstring-crc32-perl ruby ruby1.8 gawk python libusb-dev unzip intltool libacl1-dev libcap-dev libc6-dev-i386 lib32ncurses5-dev gcc-multilib lib32stdc++6 libglib2.0-dev build-essential composite ncurses-dev zlib1g-dev libacl1-dev libcap-dev
    # http://freetz.org/wiki/common/source_code
    cd /home/freetz
    su freetz
    umask 0022
    svn co http://svn.freetz.org/trunk
    cd trunk
    make menuconfig

