$ nano Dockerfile
$ docker build .
$ docker build -t docker-clock .
$ docker run docker-clock

-h,       	--help           	to show this message
-a [age], 	--adult [age]    	to check if you're older than 18
-c [time],	--clock [time]   	to start a clock
-t [size],	--triangle [size]	to draw a triangle, takes second argument as the size
    
$ docker run docker-clock -c
1
2
3
4
   
$ docker run docker-clock -t 12

*
**
* *
*  *
*   *
*    *
*     *
*      *
*       *
*        *
*         *
************

$ nano Dockerfile
$ docker build .    
$ docker build -t docker-clock 
$ docker run docker-clock
13
14
15
16
17
18
19

