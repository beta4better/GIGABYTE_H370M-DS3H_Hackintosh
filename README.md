# GIGABYTE_H370M-DS3H_Hackintosh

目前是个人在用的黑苹果主机，基于网络上找到的资料修改而来，非原创。

目前的OC版本是0.8.4，之前有两个机型在用（同一台机器上两块硬盘两个系统。

机型一是 macpro5,1，系统是 Mojave，比较老的系统了用它主要是里面的相册有个时刻功能，而且老系统在黑苹果上兼容性相对来说比较好，没有奇奇怪怪的问题。

机型二是 imac19,2，系统是 Ventura，更新到了目前最新的 13.3.1 的版本，用它主要是因为相册里有个重复照片检测功能，而且还增加的共享图库的功能。

新系统在黑苹果下总会有兼容性的小问题，而且本人也不是黑苹果的专家，所以就很头疼。目前在 Ventura 下就一直被 VTDecoderXPCService 服务崩溃导致系统自动重启困扰，也是这个原因才会有机型一存在。但是呢，一个电脑上两个系统用起来总是怪怪的。

## macOS、OC版本

### 机型一：macpro5,1
* macOS： Mojave 10.14.x
* OpenCore： [0.8.4](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.4)

选择 macpro5,1的原因主要是这个机型最高就支持到 Mojave，不会在系统设置里提示有新版本升级。
### 机型二：imac19,2
* macOS： Ventura 13.3.x
* OpenCore： [0.8.4](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.4)

选择 imac19,2的原因是我的CPU是i5-8400，从 OCAT 里看这个机型的默认 CPU 是 i5-8500，最接近了。而且目前来看貌似也是这个机型能解决 VTDecoderXPCService 服务崩溃导致系统自动重启的问题。之前我有用过 macpro7,1 和 imacpro1,1 这两个机型，但是 VTDecoderXPCService 的奔溃问题我没有在这两个机型上验证。



## 硬件配置
* 主板：GA-H370M-DS3H 
* CPU：英特尔 i5 8400
* GPU：核显 UHD 630 + RX460
* 网卡：板载 
* 声卡：板载
* 硬盘：M.2 256GB (macpro5,1) + M.2 960GB (imac19,2)
* 内存：32G
* 机箱：先马

## USB 端口定制
这个稍后补充。

## 已知问题
* 不确定核显是否有正常驱动起来
* USB 端口状态未确认

## 感谢
* https://dortania.github.io/OpenCore-Install-Guide/
* https://github.com/ahuinee/OpenCore-EFI


## 工具
* ProperTree: https://github.com/corpnewt/ProperTree
* GenSMBIOS: https://github.com/corpnewt/GenSMBIOS
* gibMacOS：https://github.com/corpnewt/gibMacOS
* Hackintool：https://github.com/headkaze/Hackintool
* USBMap：https://github.com/corpnewt/USBMap
* OCAT: https://github.com/ic005k/OCAuxiliaryTools/