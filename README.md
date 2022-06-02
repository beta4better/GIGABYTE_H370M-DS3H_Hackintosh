# GIGABYTE_H370M-DS3H_Hackintosh

在用的是机型是MacPro5,1，但是找到的能工作的EFI，OC版本只有0.5.6和0.6.6可选。自己配置了几次0.7.8的一直没有引导成功，也还没有找到失败原因，一直在用Mojave。这次用OC_Gen-X工具生成了一个配置文件，简单做了些修改，晚上看能否引导成功。

看起来这次的配置的OC是可以引导的，我拿掉了独立显卡，准备将机型换成Macmini8,1，直接将USB端口定制加进去，待测试确认。

用Mojave的原因是其中的相册有时刻功能，感觉用起来比较方便，尤其是对我这种到目前还有很多重复照片的，新版本就都没有了。


## USB 端口定制
|定制|类型	|名称	    |接口	|连接器	    |备注|
|-|------|--------|--------|-----------|--------------|
|√|XHC	|HS01		|0x01	|USB2	    |后置面板C口旁USB-A口|
|√|XHC	|HS02		|0x02	|TypeC	    |后置面板USB-C口|
|√|XHC	|HS03		|0x03	|USB2	    |板载USB3.0接口1，接前置|
|√|XHC	|HS04		|0x04	|USB2   	|板载USB3.0接口1，接前置|
||XHC	|HS05		|0x05	|USB2	    |后置面板网口旁USB-A口|
||XHC	|HS06		|0x06	|USB2	    |后置面板网口旁USB-A口|
||XHC	|HS07		|0x07	|USB2	    |板载USB3.0接口2?，闲置|
||XHC	|HS08		|0x08	|USB2	    |板载USB3.0接口2?，闲置|
|√|XHC	|HS09		|0x09	|USB2	    |后置面板PS2口旁USB-A口|
|√|XHC	|HS10		|0x0A	|Internel   |后置面板PS2口旁USB-A口，接无线鼠标改内置，靠PS口？|
||XHC	|HS11		|0x0B	|USB2	    |板载USB2.0接口2,接蓝牙后无效|
|√|XHC	|HS12		|0x0C	|Internel	|板载USB2.0接口2,接蓝牙|
|√|XHC	|HS13		|0x0D	|USB2	    |板载USB2.0接口1，接前置|
|√|XHC	|HS14		|0x0E	|USB2   	|板载USB2.0接口1，接前置|
|√|XHC	|SS01		|0x11	|USB3	    |后置面板C口旁USB-A口|
|√|XHC	|SS02		|0x12	|TYPE-C	    |后置面板USB-C口|
|√|XHC	|SS03		|0x13	|USB3	    |板载USB3.0接口，接前置|
|√|XHC	|SS04		|0x14	|USB3   	|板载USB3.0接口，接前置|
|√|XHC	|SS05		|0x15	|USB3	    |后置面板网口旁USB-A口|
|√|XHC	|SS06		|0x16	|USB3	    |后置面板网口旁USB-A口|
||XHC	|SS07		|0x17	|USB3	    |板载USB3.0接口2?，闲置|
||XHC	|SS08		|0x18	|USB3	    |板载USB3.0接口2?，闲置|

其中7和8是猜测的，不想拆线试了。由于有15个口的闲置，对于Big Sur以上的系统最终选择放弃网口旁的两个接口，只保留3.0的属性。

## USB 接口数字定义
|Type	|Info	                            |Comments|
|------|------                            |--------|
|0     |USB 2.0                           |Type-A connector	This is what macOS will default all ports to when no map is present|
|3	    |USB 3.0                           |Type-A connector	3.0, 3.1 and 3.2 ports share the same Type|
|8	    |Type C connector - USB 2.0-only	|Mainly seen in phones|
|9	    |Type C connector - USB 2.0 and USB 3.0 with Switch    |Flipping the device does not change the ACPI port|
|10    |Type C connector - USB 2.0 and USB 3.0 without Switch |Flipping the device does change the ACPI port. generally seen on 3.1/2 motherboard headers|
|255   |Proprietary connector             |For Internal USB ports like Bluetooth|

