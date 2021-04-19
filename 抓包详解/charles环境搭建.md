charles环境搭建

**http抓包：**
www.zzzmode.com 找charles破解版
将 破解后的 jar包替换 charles内的jar包
手机上设置wifi，wifi的代理设置为虚拟机的局域网IP,端口自己选
charles就会弹出一个框，connect from ... 

**如果需要手机通过科学上网，并且Buprsuite抓包怎么办：**
最上方，Proxy -> External Proxy Settings -> Use external proxy servers -> SOCKS Proxy
, SOCKS Proxy Server 输入 科学的Server， 然后输入科学的 Port，并且勾上 Select a protocol to configure 内的 SOCKS Proxy,
然后点Proxy -> External DNS Resolver Settings -> Enable External DNS Resolver, 在 External Resolver Address: 输入 8.8.8.8

**如何安装证书开启SSL抓包**
访问 https://chls.pro/ssl 就会提示下载和安装（仅针对安卓8）

**将用户证书移动到系统证书**
安装 Magisk，搜索 Move Certificate 模块，并使用它。然后重启手机。

**开启SSL抓包**
Proxy -> SSL Proxying Settings ->
勾上 Enable SSL Proxying 
在 下面的 Include，点击 Add
Host 和 Port 都填入 *
然后点 Ok

**导出Charles证书**
在  Charles 工具栏里点击 Help --- SSL Proxying --- Save Charles Root Certificate，生成 后缀名是 .cer 的文件