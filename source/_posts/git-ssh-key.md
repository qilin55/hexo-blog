# 设置git sshkey

- **首先设置git的名字和邮箱**

-   `git config --global user.name "yourname"`
-   `git config --global user.email "your@email.com"`

- **然后如果有.ssh文件夹 先删除文件夹**

- **然后输入git命令**

-   `ssh-keygen -t rsa -C "your@email.com"`
- *然后一直按回车就好*

- **最后在github添加sshkey，把你之前生成的在.ssh文件夹下的id_rsa.pub文件里的文本复制出来就ok了**

- 可以输入`ssh -T git@github.com`测试 输入`yes`就成功了