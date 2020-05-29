$ nano Dockerfile
$ docker build .
Successfully built 02bce340bece


$ docker build -t curler .
Successfully built 02bce340bece
Successfully tagged curler:latest


$ docker run -it --rm curler
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

