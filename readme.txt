
欢迎使用 GFW.Press 新一代军用级高强度加密抗干扰网络数据高速传输软件


一、客户端

请(翻墙)下载客户端安装包

Windows 版: 
http://gfw.press/GFW.Press.msi

Android 版: 
http://gfw.press/GFW.Press.apk

或者使用 eMule 下载

Windows 版: 

ed2k://|file|[GFW.Press][%E7%BF%BB%E5%A2%99][%E5%A4%A7%E6%9D%80%E5%99%A8][Windows%E7%89%88][MD5][3ac2d799280bd88156844dab9b6dd9ae].msi|51766272|4B3126EBF941F8D448678F3F54C3244F|h=STP3OBYXXH2PGKQVHA3VMM2MWFGNLHCA|/

Android 版: 

ed2k://|file|[GFW.Press][%E7%BF%BB%E5%A2%99][%E5%A4%A7%E6%9D%80%E5%99%A8][Android%E7%89%88][MD5][9d65698139f2167aafd31c0dd754bd2f].apk|1329970|669ECE2ADA9430DAFE6A9A92B465868B|h=QD4OYU34QLLHYNWIY7EXSDVPB35YK2Q6|/

请(翻墙)访问 http://gfw.press 获取连接配置信息

配置填写完成，点击“确定”按钮

设置浏览器代理，地址： 127.0.0.1  端口： 3128


二、服务器

以 CentOS 为例:

一键安装：wget -N --no-check-certificate https://raw.githubusercontent.com/bysight/gfw.press/master/install_server_centos.sh && install_server_centos.sh && install_server_centos.sh

第一步：下载 gfw.press

cd / && git clone https://github.com/chinashiyu/gfw.press.git ;

第二步：安装 JDK

yum install java-1.8.0-openjdk-devel -y ;

第三步：安装代理软件
3.1
yum install squid -y ; 
3.2
squid性能快速优化
squid是常用的http代理服务器，默认情况下，通常会使用部分内存作为缓存，并且会记录访问日志；
但是，在大多数实际应用中，缓存并不能提高访问速度，而记录日志也会占用系统资源；
所以，除非有特别需求，可以禁止缓存和日志，将减少资源使用，明显提高squid的性能；

具体设置，以 CentOS 下的 squid 3.5 为例，只需把下面的配置加入 /etc/squid/squid.conf 文件并重启squid即可

dns_nameservers 8.8.4.4 8.8.8.8
shutdown_lifetime 3 seconds
access_log none
cache_log /dev/null
logfile_rotate 0
cache deny all

3.3启动 squid软件
chkconfig squid on && service squid start
第四步：修改连接帐号文件user.txt

每行表示一个帐号，由 端口号+空格+密码 组成，密码长度至少8位，必需包含大小写字母和数字

第五步：修改脚本可执行属性

chmod u+x /gfw.press/server.sh ;
chmod u+x /gfw.press/stop.sh ;

第六步：运行

bash /gfw.press/server.sh ;

第七步：停止

bash /gfw.press/stop.sh ;


赞助捐款帐号(PayPal 或 Skrill)： donate@gfw.press

Bitcoin： 1GC4jSScEALNnqVq1zzE5RwDMEFfY34Gf8

每捐赠一美元，可能会帮助到十个人翻墙一个月


请访问 https://gfw.press/ 获取免费翻墙服务

请访问 http://twitter.com/chinashiyu 发表意见及建议

祝您好运

chinashiyu 

2016-04-16 23:49:00
2016-12-05 11:44:00
2016-12-05 22:00:00
2016-12-29 09:00:00
2017-02-17 10:00:00


