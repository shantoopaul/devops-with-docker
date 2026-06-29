```sh
$ docker run -d --rm --name secret-msg devopsdockeruh/simple-web-service:ubuntu
7695f4fa26c4e15754bfb6216a98b569c74a5dc0824d861cf0e26a80271ac94a
$ docker exec -it secret-msg bash
root@7695f4fa26c4:/usr/src/app# tail -f ./text.log
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```