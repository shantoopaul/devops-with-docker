```sh
$ docker run -d nginx
6f96c0ff4a69628de16b24115db20e95da1147d9cf071b061dc9683d23f3dc35
$ docker run -d nginx
9959ae297c67f5a7891e8d7b936867e2105ea5fe7703da8372a4b9242f5b9553
$ docker run -d nginx
0dd575932a1921fb884299a2381285a036aaad195ff04a8f199356261e8fe0f6
$ docker stop 6f9 995
6f9
995
$ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS                     PORTS     NAMES
0dd575932a19   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute          80/tcp    quirky_wiles
9959ae297c67   nginx     "/docker-entrypoint.…"   About a minute ago   Exited (0) 9 seconds ago             relaxed_jemison
6f96c0ff4a69   nginx     "/docker-entrypoint.…"   About a minute ago   Exited (0) 9 seconds ago             priceless_keller
```