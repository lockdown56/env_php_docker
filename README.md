# 使用说明
开发中还会用到 php 命令行和 composer 工具
1. php-cli
在~/.bashrc 中添加
```
alias php="sudo docker run -it --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp php:7.4.0-cli-alpine php "
```
2. composer 命令行工具
在~/.bashrc 中添加
```
alias composer="sudo docker run --rm -it --user $(id -u):$(id -g) -v $PWD:/app -v /home/composer:/tmp composer:1.9.1 "
```
