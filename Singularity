Bootstrap: docker
From: ubuntu:16.04

IncludeCmd: yes

%runscript
    exec /bin/bash "$@"

%environment
    export LC_ALL=C
    export PATH=/usr/games:$PATH

%post
    /usr/bin/apt-get update

    # Make folders for CBD HPC cluster
    if [ ! -d /images ]; then mkdir /images; fi
    if [ ! -d /projects ]; then mkdir /projects; fi
    if [ ! -d /containers ]; then mkdir /containers; fi
    if [ ! -d /share ]; then mkdir /share; fi
    if [ ! -d /scratch ]; then mkdir /scratch; fi

%appinstall figlet
    apt-get -y install figlet

%appenv figlet
    BEST_APP=figlet
    export BEST_APP

%apphelp figlet
    For more information visit http://www.figlet.org/

%apprun figlet
figlet "$@"
