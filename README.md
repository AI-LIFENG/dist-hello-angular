#安装虚拟机
```sh
docker run --name ANGULAR -p8288:8288\
  -v /bigdata/SITES/:/www/ \
  -it -d node:18.15.0-bullseye
```

#进入容器
```sh
docker exec -it ANGULAR bash
```

- 安装vi
```sh
  echo 'deb https://mirrors.tencent.com/debian/ bullseye main'                    > /etc/apt/sources.list   &&\
  echo 'deb https://mirrors.tencent.com/debian-security/ bullseye-security main' >> /etc/apt/sources.list   &&\
  echo 'deb https://mirrors.tencent.com/debian/ bullseye-updates main'           >> /etc/apt/sources.list   &&\
apt update && apt install -y vim
```

- 0到1初始化项目
```sh
npm install -g @angular/cli &&\
cd /www/ && ng new hello-angular
#...N Policy
#...y routing
#...Sass
```

- 启动应用（开发模式）
```sh
ng serve --port 8288 --host 0.0.0.0
```

- 打包应用
