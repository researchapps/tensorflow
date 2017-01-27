Bootstrap: docker
From: tensorflow/tensorflow:0.11.0rc2-gpu 

%runscript
    exec /usr/bin/python "$@"

%post
    apt-get update && apt-get -y upgrade
    apt-get -y install vim python-pip python-dev git

    echo " " >> /environment
    echo "LD_LIBRARY_PATH=/usr/local/cuda/lib64:/usr/local/cuda/lib64/stubs:$LD_LIBRARY_PATH" >> /environment
    echo "PATH=/usr/local/cuda/bin:\$PATH" >> /environment
    echo "export PATH LD_LIBRARY_PATH" >> /environment

    mkdir -p /share/PI
    mkdir -p /scratch
    mkdir -p /local-scratch
