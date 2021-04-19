遇到VPN检测怎么办？

App可以通过
java.net.NetworkInterface.getName() 是否等于 "tun0" / "ppp0" 来判断是否存在 VPN。
Bypass方法：hook这个api并让他返回 "rmnet_data1".

还能通过 
android.net.ConnectivityManager.getNetworkCapabilities 来判断