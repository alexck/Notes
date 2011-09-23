## 禁止触摸板 ##

#### 安装 xorg-x11-apps ####

	# yum -y install xorg-x11-apps

#### 设置与测试 ####
```java
    # xinput list	// 查看列表
    # xinput list-props "ETPS/2 Elantech Touchpad"	// 查看触摸板
    # xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 0	// 禁止触摸板 Test 一下.
    # xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 1	// 开启触摸板 Test 一下.
```

#### 制作脚本 ####

建立 ~/.bin 目录在目录下新建以下两个文件跟内容
tips: ~/.bin 目录增加至 PATH 环境变量中.

touchpad-disable

    #!/bin/sh
    xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 0

touchpad-enable

    #!/bin/sh
    xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 1

#### 给予执行权限 ####

	$ chmod u+x touchpad*
