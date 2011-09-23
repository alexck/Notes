## 安装 JDK 7 ##

下载地址:[[http://www.oracle.com/technetwork/java/javase/downloads/index.html]]

安装 JDK

```java
    # rpm -ivh jdk-7-linux-x64.rpm
    or
    # yum localinstall --nogpgcheck jdk-7-linux-x64.rpm
```

配置 java.sh 系统环境变量

```java
    # vim /etc/profile.d/java.sh

    export JAVA_HOME=/usr/java/latest
    export PATH=$JAVA_HOME/bin:$PATH
    export CLASSPATH=.:$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar

    # source /etc/profile.d/java.sh
```

配置 java.csh 系统环境变量

```java
    # vim /etc/profile.d/java.csh

    setenv JAVA_HOME /usr/java/latest
    set path = ( $JAVA_HOME/bin $PATH )
    setenv CLASSPATH .:$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar

    # csh /etc/profile.d/java.csh
```

配置 java 命令

```java
    # alternatives --config java
    # alternatives --install /usr/bin/java java /usr/java/latest/bin/java * (编号+1)
    # alternatives --config java
```

配置中文字体

```java
    # cd /usr/java/latest/jre/lib/fonts/
    # mkdir fallback
    # cp /home/alex/.fonts/zysong.ttf ./fallback/
    # chmod 644 -R fallback
```

配置 Firefox Plugins

```java
    # cd /usr/lib64/mozilla/plugins
    # ln -s /usr/java/latest/lib/amd64/libnpjp2.so
```
