# 李寒的主页nginx配置目录

## 目录介绍

- `conf`：存放nginx配置文件
- `conf.d`：存放nginx:sever配置文件
- `conf`：存放数据文件
- `html`：存放静态资源文件
- `logs`：存放日志文件
- `ssl`：存放ssl证书文件

## 更新

- index.html：根据情况修改网址链接
- ssl：根据情况修改证书文件
- conf.d：根据情况修改配置文件
- conf：根据情况修改配置文件
- html：新增网站放在这里
- - 例如，新增网站 `gameUper`，则在`html`目录下新建`gameUper`目录，然后在`gameUper`目录下放置网站文件 html css 等
- - 然后，在`default.conf`中新增配置:
```nginx
    location /gameUper/ {
        alias /usr/share/nginx/html/gameUper/;
        index index.html;
    }
```