# vultr搭建ss + Google bbr 加速

- **购买vultr并部署服务器(centOS7)**

-   `https://www.vultr.com/?ref=7892970-4F`

- **登陆到服务器并安装ss，配置信息会在安装好之后返回，要自己保存下来**

-   `ssh root@ip `
-   `wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh`
-    `chmod +x shadowsocks.sh`
-    `./shadowsocks.sh 2>&1 | tee shadowsocks.log`
-    shadowsocks相关操作：启动、停止、重启、状态`/etc/init.d/shadowsocks start stop restart status`
-    卸载shadowsocks`./shadowsocks.sh uninstall`
-    单用户配置{
    "server":"your_server_ip",
    "server_port":8989,
    "local_address":"127.0.0.1",
    "local_port":1080,
    "password":"yourpassword",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}

-    多用户配置{
    "server":"your_server_ip",
    "local_address": "127.0.0.1",
    "local_port":1080,
    "port_password":{
         "8989":"password0",
         "9001":"password1",
         "9002":"password2",
         "9003":"password3",
         "9004":"password4"
    },
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}

- **安装bbr加速**

-   `wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh`

- **输入以下命令，返回值中有bbr则证明安装加速成功**

-   `sysctl net.ipv4.tcp_available_congestion_control`

-   *显示* `net.ipv4.tcp_available_congestion_control = reno cubic bbr`
