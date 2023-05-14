# WMS-RuoYi

部署文档介绍
提供了docker-compose一键化部署，脚本在该项目RuoYi-WMS\wms-ruoyi\docker目录下，docker目录下的
README.md文档提供了Nginx配置文件以及在linux中的部署文档结构

在linux中文件结构：
[root@localhost ruoyi2]# tree ./
./
├── conf
│   ├── nginx.conf
│   └── redis.conf
├── db
├── docker-compose.yml
├── html
│   └── dist
├── jar
├── mysql-dockerfile
├── nginx-dockerfile
├── redis-dockerfile
└── ruoyi-dockerfile

Nginx.conf配置如下：
worker_processes  1;

events {
    worker_connections  1024;
}

http {
    include       mime.types;
    default_type  application/octet-stream;
    sendfile        on;
    keepalive_timeout  65;

    server {
        listen       80;
        server_name  localhost;

		location / {
            root   /home/ruoyi/projects/ruoyi-ui;
			try_files $uri $uri/ /index.html;
            index  index.html index.htm;
        }

		location /prod-api/{
			proxy_set_header Host $http_host;
			proxy_set_header X-Real-IP $remote_addr;
			proxy_set_header REMOTE-HOST $remote_addr;
			proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
			proxy_pass http://ruoyi-server:8080/;
		}

        error_page   500 502 503 504  /50x.html;
        location = /50x.html {
            root   html;
        }
    }
}

脚本命令：
docker-compose build    构建
docker-compose up -d    运行

在linux部署后访问    IP:80,ip为你的虚拟机ip
登录信息如下：
用户名:  cyl
密码：   cyl_666