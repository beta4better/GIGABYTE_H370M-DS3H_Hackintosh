# GIGABYTE_H370M-DS3H_Hackintosh

个人在用的黑苹果主机，基于网络上找到的资料修改而来，非原创。

目前的OC版本是1.0.2，机型用的是 iMac19,2，系统升级到了 Sonoma 14.7.1，

## 硬件配置
* 主板：GA-H370M-DS3H 
* CPU：英特尔 i5-8400
* GPU：核显 UHD 630 + RX460
* 网卡：板载 
* 声卡：板载
* 硬盘：M.2 256GB + 1TB *3 RAID0
* 内存：64G
* 机箱：先马

## USB 端口定制
|类型	|名称	   	|位置ID	    		|接口	 	|连接器	   	|备注					|
|----------|-------------	|---------------		|--------		|  -----------	|----------------------------	|
|XHC	|HS01		|0x14100000		|0x01		|USB2	   	|后置面板C口旁USB-A口|
|XHC	|HS02		|0x14200000		|0x02		|Type-C+SW 	|后置面板C口|
|XHC	|HS05		|0x14300000		|0x05		|USB2		|后置面板网口旁USB-A口（近）|
|XHC	|HS06		|0x14400000		|0x06		|USB2		|后置面板网口旁USB-A口（远）|
|XHC	|HS09		|0x14500000		|0x09		|USB2		|后置面板PS2口旁USB-A口（远）|
|XHC	|HS10		|0x14600000		|0x0A		|USB2		|后置面板PS2口旁USB-A口（近）|
|XHC	|HS12		|0x14700000		|0x0C		|Internal		|板载USB2.0-1|
|XHC	|SS01		|0x14800000		|0x11		|USB3		|后置面板C口旁USB-A口|
|XHC	|SS02		|0x14900000		|0x12		|Type-C+SW	|后置面板C口|
|XHC	|SS05		|0x14A00000		|0x15		|USB3		|后置面板网口旁USB-A口（近）|
|XHC	|SS06		|0x14B00000		|0x16		|USB3		|后置面板网口旁USB-A口（远）|

完整的端口映射信息请参考这里：USB_Map_H370M

## Sonoma 下启用 Wi-Fi
参考下面几篇文章，目前还没有成功：
* https://elitemacx86.com/threads/how-to-fix-broadcom-wifi-on-macos-sonoma-and-later.1415/
* https://github.com/billabongbruno/macOS-Sonoma-Broadcom-Wifi
* https://www.cnblogs.com/wkvip/p/17787077.html
* https://bbs.pcbeta.com/viewthread-1975545-1-1.html
https://github.com/perez987/Broadcom-wifi-back-on-macOS-Sonoma-with-OCLP

第三篇算是对第一篇的中文翻译。不知道是不是插件加多了，两台黑苹果都是重启后黑屏，无法进入系统。
第四篇笔记可能更清楚些。稍晚点我计划整理一下我自己的配置过程和方法。

## 已知问题
* 核显似乎未正确配置，如果拿掉RX460启动会花屏



## 黑苹果工具
* https://dortania.github.io/OpenCore-Install-Guide/
* https://github.com/dortania/OpenCore-Legacy-Patcher
* ProperTree: https://github.com/corpnewt/ProperTree
* GenSMBIOS: https://github.com/corpnewt/GenSMBIOS
* gibMacOS：https://github.com/corpnewt/gibMacOS
* Hackintool：https://github.com/headkaze/Hackintool
* USBMap：https://github.com/corpnewt/USBMap
* OCAT: https://github.com/ic005k/OCAuxiliaryTools/