**

**After ssh into AWS ubuntu**

**
List all the Conda env

     $ conda env list

Choose py37

     $ conda activate py37

List all the docker images

    $ docker image ls

For running Carla

```
$ sudo docker run -d -p 2000-2002:2000-2002 --runtime=nvidia -e NVIDIA_VISIBLE_DEVICES=0 carlasim/carla:0.9.9 /bin/bash CarlaUE4.sh

```

For running Mlflow dashboard

```
$ mlflow ui --backend-store-uri ‘mysql://root:password@localhost:3306/mlflow’ --host=0.0.0.0
```
