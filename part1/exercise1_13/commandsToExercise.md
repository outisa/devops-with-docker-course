commands used:
$ docker build -t myApp .
Failed -> invalid argument "myApp" for "-t, --tag" flag: invalid reference format: repository name must be lowercase

$ docker build  -t myapp .
$ docker run -p 8080:8080 --rm myapp 

At http://localhost:8080 the button did response.
To stop container:
$ docker container ls -a
$ docker stop elegant_mestorf

