## 关闭 SELinux ##

	vim /etc/selinux/config

```java
SELINUX的状态有 3 种
	1. enforcing - 执行(实行 SELinux 安全政策).
	2. permissive - 宽容(打印 SELinux 信息，而不是强制执行的警告)
	3. disabled - 禁用(关闭 SELinux .)
SELINUX=enforcing (默认)

SELINUXTYPE
	1. targeted - 只是针对网络守护进程得到保护。
	2. strict - 全SELinux的保护
SELINUXTYPE=targeted (默认)
```
关闭方法
```java
	# vim /etc/selinux/config
	SELINUX=disabled
	# reboot
```
