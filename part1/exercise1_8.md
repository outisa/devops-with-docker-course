
$ docker pull devopsdockeruh/first_volume_exercise
Using default tag: latest
latest: Pulling from devopsdockeruh/first_volume_exercise

Status: Downloaded newer image for devopsdockeruh/first_volume_exercise:latest
docker.io/devopsdockeruh/first_volume_exercise:latest
$ docker images
REPOSITORY                              TAG                 IMAGE ID            CREATED             SIZE
devopsdockeruh/first_volume_exercise    latest              072775acf05a        15 months ago       897MB

$ docker run -d -it -v $(pwd)/logs.txt:/usr/app/logs.txt devopsdockeruh/first_volume_exercise
e00577956eafbbc9099411dc7007d3f558e6dc60bb35716d69b307b4ab2c0e92

$ docker container ls
CONTAINER ID        IMAGE                                  COMMAND             CREATED             STATUS              PORTS               NAMES
e00577956eaf        devopsdockeruh/first_volume_exercise   "node index"        32 seconds ago      Up 30 seconds                           festive_bassi
$ docker stop festive_bassi
festive_bassi

$ nano logs.txt

Sat, 30 May 2020 11:24:03 GMT
4dSat, 30 May 2020 11:24:06 GMT
5dSat, 30 May 2020 11:24:09 GMT
6dSat, 30 May 2020 11:24:12 GMT
dSecret message is:
"Volume bind mount is easy"
Sat, 30 May 2020 11:24:18 GMT
Sat, 30 May 2020 11:24:21 GMT
Sat, 30 May 2020 11:24:24 GMT
Sat, 30 May 2020 11:24:27 GMT
Secret message is:
"Volume bind mount is easy"
Sat, 30 May 2020 11:24:33 GMT
Sat, 30 May 2020 11:24:36 GMT
Sat, 30 May 2020 11:24:39 GMT
Sat, 30 May 2020 11:24:42 GMT
Secret message is:
"Volume bind mount is easy"
Sat, 30 May 2020 11:24:48 GMT

