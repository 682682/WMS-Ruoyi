文件结构如下：
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