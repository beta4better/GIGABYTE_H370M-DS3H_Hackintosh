## Sonoma 下启用 Wi-Fi
参考下面几篇文章，目前还没有成功：
* https://elitemacx86.com/threads/how-to-fix-broadcom-wifi-on-macos-sonoma-and-later.1415/
* https://github.com/billabongbruno/macOS-Sonoma-Broadcom-Wifi
* https://www.cnblogs.com/wkvip/p/17787077.html

第三篇算是对第一篇的中文翻译。不知道是不是插件加多了，两台黑苹果都是重启后黑屏，无法进入系统。



### AirportBrcmFixup

https://github.com/acidanthera/AirportBrcmFixup

这个看介绍貌似是Brcm的网卡必须要放的，
https://github.com/acidanthera/AirportBrcmFixup/pull/14
已经有人验证了在 macOS 15 下搭配 OCLP 可以工作。

目前我的网卡在 Sonoma 下蓝牙免驱的，可以直接识别并能够连蓝牙耳机。但是WiFi看不到，甚至在 Hackintosh 软件里都看不到设备。


https://github.com/perez987/Broadcom-wifi-back-on-macOS-Sonoma-with-OCLP?tab=readme-ov-file
这篇文章里提到 amfi=0x80 的参数可以不用了，用 AMFIPass.kext