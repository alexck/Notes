##安装 Linux 下载工具 MlDonkey ##

MLDonkey 是一个开源免费的多协议P2P应用程序 [Wiki详情](http://zh.wikipedia.org/wiki/MLDonkey)

### 1.安装MLDonkey ###

    $ sudo yum install mldonkey
    $ mlnet

### 2.安装sancho ###

[sancho官方](http://sancho-gui.sourceforge.net/)
下载 sancho-<version>-linux-gtk-x86_64-java.sh

**安装**
	
    $ sh sancho-0.9.4-59-linux-gtk-x86_64-java.sh

### 配置 sancho ###

**a) 启动器**  

在桌面创建一个启动器连接到安装路径下的 sancho. 双击 sancho 启动器 运行.  

**b) 核心配置**  

一般为: `/usr/bin/mlnet` (你可以用 `which mlnet` 命令查看路径).  
    
**c) 连接配置**  

一般不须要更改参数，直接 connect.  
	
**e) 客户端名称**  

Tools -> preferences -> Main -> client_name 推荐设置成[CHN][VeryCD]yourname的形式,支持中文.  

**d) 配置中文**  

Tools -> preferences -> sancho:Main -> (*) User Locale File: zh_CN (*)<-这样的符号说明要重启 sancho.  
	
**preferences -> Bandwidth**  

设置 max_hard_download_rate 和 max_hard_upload_rate 分别是下载和上传速度，单位是KB.  
    
**preferences -> Networks**  

勾选 enable_kademlia 和 enable_overnet.  
    
**preferences -> Networks -> Donkey**  

ED2K-force_client_high_id  
ED2K-force_high_id  
如果你是公网用户，或者你是内网，且设置了端口映射，则勾选它们，如果你打死都是内网低ID用户，就不要选了，否则会很难连上服务器。  
	
**ED2K-port 设置端口 (我未设置)**  

如果你有windows下的emule，最好把他们的端口(tcp的)设成一样，因为有些路由器有记忆功能，导致windows下的端口在重启后仍然保留。一般emule默认端口为4662,但有些宽带运营商会封掉该端口，建议改掉。  

**ED2K-max_connected_servers**  

设置服务器最大连接数，默认为3，我把它设为6.
	

### 配置 Server 列表 ###
打开 FF 登录 http://localhost:4080/

**a) Options -> Web infos(最下面)**  

删除 URL 状态(State) 为 未知的(unknown) 行.

**b) Servers -> All servers**  

删除 不能连接的 server

**c) Options -> Web infos -> add URL**  

server.met http://eserver.googlecode.com/svn/server.met  
server.met http://ed2k.im/server.met  
server.met http://peerates.net/peerates/trueservers.met 国外

**d) 保存退出**  

Help+ -> save

### 国内服务器 ###
sancho 服务器增加  
IP				端口		域名  
115.239.228.194	8080	no1.eserver.emule.org.cn  
//这个一定要添加上 这可是www.verycd.com的服务器.还有你的用户名要设置成 [CHN][VeryCD]yourname.

### 国外服务器 ###
212.63.206.35:4242		//这个是我见过最多文件的服务器  
94.75.216.6:4666  
178.86.3.184:4184
	
### 可获取服务器的地方 ###
http://www.emule-security.net/serverlist/  
http://emulefans.com/news/plugin/server-list/  
