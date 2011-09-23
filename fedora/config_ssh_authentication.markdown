### 1.生成密钥

    $ ssh-keygen -t rsa

### 2.配置

    # vim /etc/ssh/sshd_config

```java
#端口
Port 22

#ssh 协议版本
Protocol 2

#是否允许 Root 登录 否
PermitRootLogin no

#严格的模式
StrictModes yes

#是否RSA 认证 是
RSAAuthentication yes

#是否公钥认证
PubkeyAuthentication yes

#是否密码认证
PasswordAuthentication no

#是否允许空密码
PermitEmptyPasswords no

```

$ mv ~/.ssh/id_rsa.pub ~/.ssh/authorized_keys
$ chmod 600 ~/.ssh/authorized_keys
