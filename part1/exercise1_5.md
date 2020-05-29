
$ docker run -d --rm -it --name test_it  ubuntu sh -c 'echo "Input website:";read website;echo "Searching..";sleep 1;curl http://$website
$ container ls -a
CONTAINER ID        IMAGE               COMMAND                   CREATED             STATUS              PORTS               NAMES
ad6d9f13a133        ubuntu              "sh -c 'echo \"Input …"   24 seconds ago      Up 23 seconds                           test_it

$ docker run -d --rm -it test_it sh -c 'echo "Input website:";read website;echo "Searching..";sleep 1;curl http://$website;'
Input website:
helsinki.fi
Searching..
sh: 1: curl: not found
$ docker exec -it test_it bash
root@ad6d9f13a133:/# apt-get update
root@ad6d9f13a133:/# apt-get install curl
done.
root@ad6d9f13a133:/# exit
exit
$ docker exec -it test_it bashsh -c 'echo "Input website:";read website;echo "Searching..";sleep 1;curl http://$website;'
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>

