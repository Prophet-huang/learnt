这里只提及局域网连接，外网连接涉及到特殊渗透插件，和安全问题。



服务器端：

- 必备软件`ssh-sever` `ssh-client` `net-tools` 

- 检查是否安装`ssh-sever` `ssh-client` 并启动。

  ```bash
  dpkg -l | grep ssh
  ```

- ```bash
  #如果没有则可以这样启动：
  sudo /etc/init.d/ssh start
  #或
  sudo service ssh start
  ```

- ```bash
  ifconfig # 查看服务器端链接地址
  ```



客户端：

`ssh username@192.168.1.103`
其中，`username为192.168.1.103`机器上的用户，需要输入密码。
断开连接：`exit`