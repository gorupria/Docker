## Command used to run the container
***docker run -d -it --name looper-it ubuntu:16.04 sh -c 'read website; sleep 3; curl http://$website;'
## Command used to install the curl in sequence
1. docker exec -it looper-it bash
1. apt-get update
1. apt-get install curl 
## Command to run helsinki.fi
docker attach looper-it
input 'helsinki.fi'

OUTPUT

<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>

