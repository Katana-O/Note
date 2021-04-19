burpsuite环境搭建

**http抓包：**
下载 burpsuite 破解版
java -jar burploader.jar
激活好了后，到burpsuite的 proxy -> Options，找到 interface，选择 all interface, 端口号要两边的一样
把 interceptor 改成 off

**如果需要手机通过科学上网，并且Buprsuite抓包怎么办：**
User options -> SOCKS Proxy
在 SOCKS Proxy 中 填入 SOCKS proxy host(科学的host) 和 SOCKS proxy port(科学的port). 

**如何安装证书开启SSL抓包**
到达用户界面，Proxy -> Options -> Import / export CA certificate -> Export -> Certificate in DER format -> Next -> 选择一个地方保存。

然后执行下面的命令，der 就会 转化成 pem
openssl x509 -inform DER -in burp.der -out burpder1545.pem

然后 push 到 /sdcard/Download

然后在手机 ： 从存储设备安装

然后激活 Magisk 的 move certificate 模块，并且重启手机

**将用户证书移动到系统证书**
安装 Magisk，搜索 Move Certificate 模块，并使用它。