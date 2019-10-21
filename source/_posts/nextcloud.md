# 自制云盘 nextcloud

- **登陆到服务器并安装ss，配置信息会在安装好之后返回，要自己保存下来**

-    # 通过yum源安装docker
-    `sudo yum -y install docker`
-    # 启动docker
-    `sudo systemctl start docker`
-    # 开机自启
-    `sudo systemctl enable docker`

- **获取nextcloud镜像, 完成网盘搭建**

-   `docker run -d -p 8080:80 nextcloud`

- **访问自己ip的8080端口**

