Bootstrap: docker
From: tensorflow/tensorflow:latest 
IncludeCmd: yes

%runscript
    exec /usr/bin/python "$@"

%post
    apt-get update && apt-get -y upgrade
    apt-get install vim
    apt-get install git
 
    mkdir -p /share/PI
    mkdir -p /scratch
    mkdir -p /local-scratch
