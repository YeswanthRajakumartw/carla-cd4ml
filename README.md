**CARLA docker**

 - Ubuntu 18.04
 -  NVIDIA GPU with at least 4GB
  -   NVIDIA drivers > 361.93
   -  Free Disk Space > 30GB (this is the minimum preferred amount so that your system behaves properly)

    $ sudo apt-get update
    $ sudo apt-get install
apt-transport-https
ca-certificates
curl
gnupg-agent
software-properties-common

    $ curl -fsSL  [https://download.docker.com/linux/ubuntu/gpg](https://download.docker.com/linux/ubuntu/gpg)  | sudo apt-key add -
    
    $ sudo add-apt-repository

    "deb [arch=amd64]  [https://download.docker.com/linux/ubuntu](https://download.docker.com/linux/ubuntu)

    $(lsb_release -cs) stable

    $ sudo apt-get update

  

    $ sudo apt-get install docker-ce docker-ce-cli  [containerd.io](http://containerd.io/)

  

    $ sudo docker run hello-world
    
      
    
    $ distribution=$(. /etc/os-release;echo $ID$VERSION_ID) \
    
    && curl -s -L  [https://nvidia.github.io/nvidia-docker/gpgkey](https://nvidia.github.io/nvidia-docker/gpgkey)  | sudo apt-key add - \
    
    && curl -s -L  [https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list](https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list)  | sudo tee /etc/apt/sources.list.d/nvidia-docker.list
    
    $ sudo apt-get update
    
    $ sudo apt-get install -y nvidia-docker2
    
    $ sudo systemctl restart docker
    
    $ docker pull carlasim/carla:0.9.9
    
    $ sudo docker run -d -p 2000-2002:2000-2002 --runtime=nvidia -e NVIDIA_VISIBLE_DEVICES=0 carlasim/carla:0.9.9 /bin/bash CarlaUE4.sh







