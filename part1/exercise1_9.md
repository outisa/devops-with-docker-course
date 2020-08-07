$ docker pull devopsdockeruh/ports_exercise
Status: Downloaded newer image for devopsdockeruh/ports_exercise:latest
docker.io/devopsdockeruh/ports_exercise:latest

$ docker run -d -p 3000:80 devopsdockeruh/ports_exercise

//After this a message about correct ports configuration can be found on http://localhost:3000/.

$ docker container ls 
$ docker port thirsty_brown
80/tcp -> 0.0.0.0:3000
$ docker stop thirsty_brown
 
