Postern抓包配置

因为偶尔会遇到代理检测，会通过 System.getProperty 来检测是否被代理。
那么就会需要用到 Postern。

1.  apkmirror / apkpure 下载 postern
2.  配置代理 ：
    1.  服务器名称：随便
    2.  服务器地址，PC的局域网IP地址
    3.  服务器端口：charles上面，proxy settings 中 SOCKS proxy 要勾上 Enable SOCKS Proxy 和 Enable HTTP proxying over SOCKS 和 Include default HTTP ports，Enable SOCKS proxy 下要填入的 Port 可以自定义。然后回到 Postern ，在服务器端口填入刚才自定义的 Port，代理类型为 SOCKS5，用户名和密码不填，加密类型是 ases-256-cfb。
    4.  Postern的配置规则，选择其中一个规则。修改匹配类型 -> 匹配所有地址，动作 -> 通过代理连接，代理/代理组 proxy - 192.168.1.101:1112(刚才自定义的端口）
    5.  目标地址全部清空
    6.  回到Postern主菜单。
    7.  打开VPN