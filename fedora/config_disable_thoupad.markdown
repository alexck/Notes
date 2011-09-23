## 禁止触摸板 ##

安装 xorg-x11-apps 

    # yum -y install xorg-x11-apps
    # xinput list
    # xinput list-props "ETPS/2 Elantech Touchpad"
    # xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 0
    # xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 1

建立 ~/.bin 目录在目录下新建以下两个文件

touchpad-disable

    #!/bin/sh
    xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 0

touchpad-enable

    #!/bin/sh
    xinput --set-prop "ETPS/2 Elantech Touchpad" "Device Enabled" 1

$ chmod u+x touchpad*
