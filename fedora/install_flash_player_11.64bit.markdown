## 安装 Adobe Flash Player 11 64bit ##

下载地址:[[http://labs.adobe.com/downloads/flashplayer11.html]]

$ mkdir flash
$ tar -zxvf flashplayer11_rc1_install_lin_64_090611.tar.gz -C flash
$ sudo mv flash/libflashplayer.so /usr/lib64/mozilla/plugins/
$ sudo mv flash/usr/bin/flash-player-properties /usr/bin/
$ sudo cp -rf flash/usr/share/* /usr/share/
