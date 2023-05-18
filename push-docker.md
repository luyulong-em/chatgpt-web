# build 镜像

> 切换到Dockerfile文件所在目录 运行
docker build --platform=linux/x86_64 -t 510248292/chatgpt-web .
# 得到了 名称为510248292/chatgpt-web:latest的镜像 然后
docker push 510248292/chatgpt-web:latest

# 推送到了 dicker hub 用户 510248292

# 接着 到服务器运行
docker pull 510248292/chatgpt-web:latest
# 将该镜像下载到了服务器 之后
# 运行命令
docker run --name chatgpt-web -d -p 3002:3002 --env OPENAI_API_KEY='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' 510248292/chatgpt-web

# 启动了该容器
# 运行
docker ps
# 查看容器是否已经成功启动 查询到该容器chatgpt-web则运行成功

# 需要在服务器开启该端口的访问白名单 且配置协议

```js
<!-- 你把你本地的镜像 打个tag docker tag chatgpt-web 510248292/chatgpt-web:latest,
   docker push 510248292/chatgpt-web:latest,
  然后把你的 docker-compose 的 镜像地址改成 510248292/chatgpt-web:latest ， 再试
	到你的服务器 docker pull

docker run --name chatgpt-web -d -p 3002:3002 --env OPENAI_API_KEY='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' 510248292/chatgpt-web -->
```
