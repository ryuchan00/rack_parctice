# rack_parctice
Perfect Ruby

## Rackとは

> Rackとは、WEBrickやThin、Unicornと言ったWebアプリケーションサーバとRoRなどのWebアプリケーションフレームワークのインターフェースとなるライブラリです。

## installation

```
bundle install
bundle exec rackup -v
Rack 1.3 (Release: 2.0.7)
```

## 最も小さなRackアプリケーション

```
$ be rackup config_1.ru
[2019-09-08 18:11:42] INFO  WEBrick 1.4.2
[2019-09-08 18:11:42] INFO  ruby 2.5.0 (2017-12-25) [x86_64-darwin16]
[2019-09-08 18:11:42] INFO  WEBrick::HTTPServer#start: pid=9851 port=9292
::1 - - [08/Sep/2019:18:12:07 +0900] "GET / HTTP/1.1" 200 - 0.0003

```

```
$ curl -i http://localhost:9292
HTTP/1.1 200 OK
Content-Type: text/plain
Transfer-Encoding: chunked
Server: WEBrick/1.4.2 (Ruby/2.5.0/2017-12-25)
Date: Sun, 08 Sep 2019 09:12:07 GMT
Connection: Keep-Alive

Hello!% 

```

```
$ be rackup config_2.ru
[2019-09-08 18:54:37] INFO  WEBrick 1.4.2
[2019-09-08 18:54:37] INFO  ruby 2.5.0 (2017-12-25) [x86_64-darwin16]
[2019-09-08 18:54:37] INFO  WEBrick::HTTPServer#start: pid=35528 port=9292
{"GATEWAY_INTERFACE"=>"CGI/1.1",
 "PATH_INFO"=>"/",
 "QUERY_STRING"=>"",
 "REMOTE_ADDR"=>"::1",
 "REMOTE_HOST"=>"::1",
 "REQUEST_METHOD"=>"GET",
 "REQUEST_URI"=>"http://localhost:9292/",
 "SCRIPT_NAME"=>"",
 "SERVER_NAME"=>"localhost",
 "SERVER_PORT"=>"9292",
 "SERVER_PROTOCOL"=>"HTTP/1.1",
 "SERVER_SOFTWARE"=>"WEBrick/1.4.2 (Ruby/2.5.0/2017-12-25)",
# 省略
 "rack.hijack_io"=>nil,
 "HTTP_VERSION"=>"HTTP/1.1",
 "REQUEST_PATH"=>"/",
 "rack.tempfiles"=>[]}
::1 - - [08/Sep/2019:18:55:34 +0900] "GET / HTTP/1.1" 200 - 0.0018

```
