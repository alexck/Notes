## 基本安装与配置 ##

### 1.Fedora 更新 ###
```java
    $ su -
    # yum makecache
    # yum update -y
```

### 2.安装第三方源软件库 ###
```java
    # yum localinstall --nogpgcheck http://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-stable.noarch.rpm http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-stable.noarch.rpm
    # yum update -y
```

### 3.Feodra 配置工具 ###
```java
    /* rar 压缩工具 */
    # yum install unrar
    /* 安装 7z压缩工具 */
    # yum install p7zip p7zip-plugins
    /* 安装 Gnome 调节工具 */
    # yum install gnome-tweak-tool
    /* dconf 配置编辑器 */
    # yum install dconf-editor
    /* gconf 管理工具 */
    # yum install gconf-editor
    /* 主菜单编辑器 */
    # yum install alacarte
```

### 4.gnome-shell 扩展程序 ###
```java
    使用 yum install <pagecke_name> 安装
    gnome-shell-extension-cpu-temperature : 在顶部栏显示 CPU 温度
    gnome-shell-extension-gpaste : 剪贴板管理工具
    gnome-shell-extension-icon-manager : 管理顶部工具条
    gnome-shell-extension-mediaplayers : 控制音乐播放器
    gnome-shell-extension-noim : 册除用户名称与IM状态
    gnome-shell-extension-noripple : 禁止热角落产生涟漪效应
    gnome-shell-extension-pidgin : pidgin 扩展(须安装 pidgin)
    gnome-shell-extension-pomodoro : 计时工具
    gnome-shell-extension-presentation-mode : 屏幕保护程序
    gnome-shell-extension-remove-accessibility-icon : 删除辅助功能图标
    gnome-shell-extension-remove-bluetooth-icon : 删除蓝牙图标
    gnome-shell-extension-remove-volume-icon : 删除音量图标
    gnome-shell-extension-righthotcorner : 右边的热角(跟右顶触发一样的行为)
    gnome-shell-extension-theme-selector : 用户主题选择(行为菜单内)
    gnome-shell-extension-workspacesmenu : 快速切换工作空间(右顶部显示工作空间编号)
    gnome-shell-extensions-alternate-tab : 经典 Alt+Tab 键行为
    gnome-shell-extensions-alternative-status-menu : 电源开关
    gnome-shell-extensions-auto-move-windows : 分配到应用程序的具体工作区 
    gnome-shell-extensions-common : 通用的Gnome基本扩展库
    gnome-shell-extensions-dock : 永久显示一个任务式切换工具栏
    gnome-shell-extensions-drive-menu : 磁盘管理
    gnome-shell-extensions-native-window-placement : 一个更自然的方式排列窗口缩略图(win键)
    gnome-shell-extensions-places-menu : 放置在系统状态区的用户目录菜单栏
    gnome-shell-extensions-user-theme : 让用户选择一个自定义主题
    gnome-shell-extensions-windowsNavigator : 键盘选择Windows和叠加模式的工作空间(Alt+编号 每个窗体增加编号)
    ibus-gnome3.x86_64 : IBus输入法与Gnome结合
```

### 5.安装常用工具 ###
```java
    /* 安装 IBus 五笔 */
    # yum install ibus-table ibus-table-chinese ibus-table-chinese-wubi-haifeng ibus-table-chinese-wubi-jidian
    /* 安装 Gvim */
    # yum install gvim
    /* 安装 chm 阅读器 */
    # yum install gnochm
    /* 安装 星际词霸 */
    # yum install stardict stardict-dic-zh_CN stardict-dic-en
    /* 安装 Cairo-Dock 3D 工具栏 */
    # yum install cairo-dock
    /* 安装 音频／视频 解码器 */
    # yum install gstreamer-plugins-bad gstreamer-ffmpeg gstreamer-plugins-bad-free
    /* 安装 exaile 音乐播放器 */
    # yum install exaile
    /* 安装 OSD 桌面歌词 */ 下载地址 http://code.google.com/p/osd-lyrics/
    # yum localinstall --nogpgcheck osdlyrics-0.4.1-1.fc15.x86_64.rpm
    /* 安装 smpalyer */
    # yum install smplayer
```

### gedit markdown 插件安装 ###
```java
	wget http://www.jpfleury.net/site/fichiers/gedit-markdown/gedit-markdown.zip
	unzip gedit-markdown.zip
	gedit-markdown/gedit-markdown.sh install
```
