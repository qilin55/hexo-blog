# 进行下述操作必须先停止mysql服务

- 切换到mysql安装目录
- `cd /usr/local/mysql/bin`
- 获取管理员权限
- `sudo su`
- 开启mysql安全模式，可以跳过密码验证
- `./mysqld_safe --skip-grant-tables &`
- 回车然后输入`./mysql -u root`进入mysql
- 启用mysql数据库
- `use mysql;`
- 修改user表下root用户的登陆密码
- `update user set authentication_string=‘111222’ where User='root';`

## 大功告成

- MAC 允许任何来源安装的app

  `sudo spctl --master-disable`
