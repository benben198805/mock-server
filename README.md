# mock-server

## 拉取镜像，运行镜像
```
docker pull mockserver/mockserver
docker run -d --rm -P mockserver/mockserver
```


## 运行镜像（增加配置）
配置mock server的配置细节，使用mockserver.properties，放置在config目录下。
docker run -v $(pwd):/config -p 1080:1080  mockserver/mockserver -serverPort 1080
其中$(pwd)为当前目录

## 测试
curl --location --request GET 'localhost:1080/simpleFirst'

## UI地址
http://localhost:1080/mockserver/dashboard
