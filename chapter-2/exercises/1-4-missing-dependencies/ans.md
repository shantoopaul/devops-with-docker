```fish
$ docker run -it --name terminal-browser ubuntu
root@247cb277ca86:/# sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
Input website:
helsinki.fi
Searching..
sh: 1: curl: not found
Input website:
$ docker exec -it terminal-browser bash
root@247cb277ca86:/# apt-get update
root@247cb277ca86:/# apt-get -y install curl
root@247cb277ca86:/# sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
Input website:
helsinki.fi
Searching..
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.24.0</center>
</body>
</html>
```