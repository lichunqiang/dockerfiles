## 本地构建


```
$ docker build -t swoole-cli  .
$ docker run -it --rm --name swoole-http-server -v "$PWD":/usr/src/app -w /usr/src/app -p 9501:9501 swoole-cli php http.php
```


## Repository运行

```
$ docker run -it --rm --name swoole-http-sever -v "$PWD":/usr/src/app -w /usr/src/app -p 9501:9501 light/swoole:1.0.0 php http.php
```