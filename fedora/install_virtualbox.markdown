## 安装 VirtualBox ##

### 配置 Yum.repo ###

	$ wget http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc
	$ sudo rpm --import oracle_vbox.asc
	$ cd /etc/yum.repos.d/
	$ sudo wget http://download.virtualbox.org/virtualbox/rpm/fedora/virtualbox.repo
	
### 安装 dkms 工具 ###

	$ sudo yum install dkms
	
### 安装 ###

	$ sudo yum search VirtualBox
	$ sudo yum install VirtualBox-4.1<最新版本号>
	
### 添加用户至 vboxusers 组 ###

	$ sudo usermod -a -G vboxusers <userName>
	
### USB ###

	$ cat /etc/group | grep vboxusers
    vboxusers:x:501:alex
    $ sudo vim /etc/fstab    //devgid 为你的 vboxusers 组ID
    none                    /proc/bus/usb           usbfs   devgid=501,devmode=664 0 0
	
