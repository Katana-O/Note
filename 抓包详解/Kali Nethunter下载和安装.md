Kali Nethunter下载和安装

https://bt4g.org/
https://build.nethunter.com/contributors/re4son/
我的手机是Nexus 5 HammerHead

1. 刷 一个全新的ROM
2. adb push Kali Nethunter 到 sdcard，进入 twrp 刷 kali nethunter
3. 在 Linux 中找到 高级网络配置，添加一个 wifi 。
4. SSID：名字岁便器
5. Mode：Hotspot
6. Brand：Automatic
7. Channel：default
8. Device：选择 wlan0(.....)

1. 在 手机的 net hunter 上，点击 Kali Chroot Manager，手机会开始自动安装 Net Hunter
2. 然后选择 KeX Manager

**PC如何连接手机的Nethunter：**
在手机上，选择 Kali Service，开启 ssh -> RunOnRoot
然后在 NetHunter 的 Home 界面，找到 Network Interface Status, 查看 wlan0 inet 的地址
然后在 PC 控制台上, 输入 ssh root@192.168.197(wlan0 inet 的地址)
然后会弹出提示，选择yes。
password 是 toor  和电脑的是一样的。
ifconfig 显示 网卡（此时显示的是手机上的网卡）
