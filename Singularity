Bootstrap: docker
From: tensorflow/tensorflow:0.11.0rc2-gpu 

%runscript
    exec /usr/bin/python "$@"

%post
    apt-get update && apt-get -y upgrade
    apt-get -y install vim python-pip python-dev git

    driver_version=367.48
    driver_path=/usr/local/NVIDIA-Linux-x86_64-$driver_version
    echo " " >> /environment
    echo "LD_LIBRARY_PATH=/usr/local/cuda/lib64:/usr/local/cuda/extras/CUPTI/lib64:$driver_path:$LD_LIBRARY_PATH" >> /environment
    echo "PATH=$driver_path:\$PATH" >> /environment
    echo "export PATH LD_LIBRARY_PATH" >> /environment

    mkdir -p /share/PI
    mkdir -p /scratch
    mkdir -p /local-scratch
