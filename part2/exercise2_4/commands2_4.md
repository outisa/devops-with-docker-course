$ git clone git@github.com:docker-hy/scaling-exercise.git scaling exercise

$ cd scaling-exercise

// First tried without scaling, computation took around 36 seconds
$ docker-compose up
// It worked already with next command, computation took around 21 seconds.
$ docker-compose up --scale compute=2
// But I wanted to try with bigger scale, computation took around 15 seconds.
$ docker-compose up --scale compute=5
// computation took around 10 seconds.
$ docker-compose up --scale compute=10



