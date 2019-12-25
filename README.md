# 使用说明
开发中还会用到 php 命令行和 composer 工具
1. php-cli
在~/.bashrc 中添加别名, 注意 docker 镜像换成自己期望的版本
```
alias php="sudo docker run -it --rm -v \$PWD:/usr/src/myapp -w /usr/src/myapp php:7.4.0-cli-alpine php "
```
2. composer 命令行工具
在~/.bashrc 中添加别名，注意 docker 镜像换成自己期望的版本
```
alias composer="sudo docker run --rm -it --user \$(id -u):\$(id -g) -v \$PWD:/app -v /home/composer:/tmp composer:1.9.1 "
```

# 打包 php 镜像说明
1. 官方 php 镜像只有核心的扩展库，缺少 gd 库等开发生产环境中可能用到的库，需要自己添加所需扩展并打包镜像
2. 官方 composer 镜像同上
