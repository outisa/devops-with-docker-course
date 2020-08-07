$ docker build -t  backend .
Sending build context to Docker daemon    235kB
Step 1/9 : FROM ubuntu:16.04
 ---> fab5e942c505
Step 2/9 : WORKDIR /dist
 ---> Using cache
 ---> 642dbeb7e459
Step 3/9 : RUN apt update && apt install -y curl
 ---> Using cache
 ---> c65f859ae727
Step 4/9 : RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs
 ---> Using cache
 ---> 91bd4ec49a5b
Step 5/9 : COPY ./backend-example-docker .
 ---> Using cache
 ---> 35a9227a6921
Step 6/9 : RUN npm install
 ---> Using cache
 ---> 764a0e405b4b
Step 7/9 : COPY logs.txt .
 ---> 526e790281db
Step 8/9 : EXPOSE 8000
 ---> Running in a74d29438638
Removing intermediate container a74d29438638
 ---> 2779ba4e01a2
Step 9/9 : ENTRYPOINT npm start
 ---> Running in f9e40000db6f
Removing intermediate container f9e40000db6f
 ---> 567dcbc7fd24
Successfully built 567dcbc7fd24
Successfully tagged backend:latest

$ docker run -p 8000:8000 -v  $(pwd)/logs.txt:/dist/logs.txt backend

> backend-example-docker@1.0.0 start /dist
...
Started on port 8000

//Going to localhost:8000
// Check container name:
$ docker container ls -a
$ docker stop exciting_gauss

$ cat logs.txt
8/7/2020, 5:43:35 PM: Connection received in root
$docker start exciting_gauss
// Refresh localhost:8000 two times
$ docker stop exciting_gauss

$ cat logs.txt
8/7/2020, 5:43:35 PM: Connection received in root
8/7/2020, 5:43:39 PM: Connection received in root
8/7/2020, 5:46:19 PM: Connection received in root


