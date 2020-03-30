# Dell-5577-hackintosh-sierra/High Sierra/hMojave/Catalina
# 感谢黑果的前辈大佬和网络无名大神，因为他们的辛苦铺路，所以这份5577的引导才会比较完善。 
### 搞黑果，重要的是开心就好。

**系统是10.15.1(19B88)**</p>
Dell5577配置： 

|硬件类型|型号|
|---- | ----- |
|操作系统：|MacOS Ctalina(19B88)|
|处理器：|i5-7300HQ|
|显卡：|HD630 /GTX1050 4G(屏蔽)|
|内存：|12G/2400Mhz/三星|
|声卡：|ALC256|
|网卡：|RTL8111/BCM94360cs2|
|硬盘：|三星860Evo|

|Mojave|Catalina|
|--|--|
|![HD14](https://github.com/Wmyaaa/Dell5577-hackintosh-clover/blob/master/pic/download.jpg)|![HD15](https://github.com/Wmyaaa/Dell5577-hackintosh-clover/blob/master/pic/download-1.jpg)|
</br>
------------------------假把意思分割线-----------------------

### 2020/3/30：
* 因为现在的”网卡“价格略贵，不确定是否刚需的话，可以通过手机的USB共享网络，把手机当做“外置网卡”，hahahah。通过一段的使用后，再确定需要与否。(Catalina 15.1可用)


### 2020/3/6：
* 如果不是大的系统更新(例如10.14跳10.15)导致hac使用过程中出现问题(例如触控板多指触控失效，声卡失效等)，请检查并及时更新lilu.kext核心驱动。
* 此库提供的clover15.1引导最高支持正常使用到10.15.2系统。请各位"玩家"在使用时注意更新驱动提示"游戏体验"。
* 目前hac的体验差不多完善了，后天应该会更新一下吧（候到哪天是哪天😂).

|驱动名称 | 驱动作用|
|---- | ----- |
| lilu | 确保mac系统对各驱动的顺利调用。例如声卡，触控板等驱动的正常使用 | 
| AppleALC | 驱动声卡 功能 | 
| voodooi2C | 驱动触控板 功能(请确定自己的触控板类型) |
|            | voodooi2c配合voodooi2CHID驱动i2c触控板(有些elan设备也有可能是i2c-hid设备)|
|            | voodooi2c配合voodooi2CELAN驱动ELAN触控板 |
|            | voodooi2c配合VoodooI2CFTE驱动FTE触控板 |
|            | voodooi2c配合VoodooI2CSynaptics驱动Synaptics触控板 |
|            | voodooi2c配合VoodooI2CAtmelMXT驱动触控屏方案 |
|VoodooI2CUPDDEngine| UPDD多点触控 |
|ACPIBatteryManager| 电源驱动 |
|AppleBacklightFixup| 亮度驱动 |
|   | 期待下一次闲下来继续补充3.6.2.45|

 

---------------------
### 2019/11/27:  Clover15.1
* 更新了CPU变频的控制，延长了电源的使用时长。平均测试睡眠耗电约为2小时/1%（仅个人测试结果）
* 添加 **releases/发布**版面，提供单独下载。

 |Intel power Gadget|
 | ----- |
 | ![HD1](https://github.com/Wmyaaa/Dell5577-hackintosh/blob/master/pic/IPG.png) |

### 2019/7/21:

* 添加**releases/发布**版面。可根据需要单独下载引导。节约时间和空间。
* 可能下次更新就是15的正式版发布后吧。目前引导没啥问题了。
### (出现问题的大概思路：
* 初期尽量精简驱动。增删驱动时注意有无重复项。
* 移动引导时检查EFI文件夹内的是否齐全。
    * Boot      (必要) 
    * Apple     (必要)
    * Clover    (必要)
    * Microsoft (必要)
    * 以及其他系统的引导文件夹引导  
~~同机型的引导开不了机时，(仅为进系统)~~
 ~~在界面按字母O键。打开Menu Option菜单。
 打开Acpi patching。勾选Debug DSDT或移动到DSDT name(第二个)打开，勾选BIOS.aml~~
  ~~主界面 空格进入引导选项菜单
  开机 -V       第一个   
  (Debug 0x100)  倒数第二个
   Debug kexts    倒数第一个
  然后开机~~
* 排错的话记得-V ~~、Debug 0x100。然后针对错误，再了解修复。
~~* 如有错误，还望指出。不能一直错下去哈。~~
* 装好系统还只是入门，生命在于折腾，没有谁能一口吃成胖子，慢慢来，加油吧。


### 2019/7/15：//Clover14no plug-in<br>
* 添加了无需插件驱动耳机的Efi。睡眠唤醒正常，无爆音。缺点，无耳麦。插入耳机时无法使用麦克风。
* 运行状态：正常(除声卡外，可参照下面mojave运行表的状态)
* **注意事项：此引导仅运行在未安装过相关声卡驱动、插件的设备。反之，在安装过的设备上使用会无法驱动声卡/爆音等现象。建议在新安装的系统使用**

---------------------

### Catalina目前运行状态：<br>
* 日常使用正常，触控板，网卡，显卡，fn，参考下面Mojave运行状态。。。。
* 耳机无法使用
* 开机待优化
* 未知问题待发现
* Catalina的引导支持Mojave，~~但在Mojave下未驱动声能卡~~由于测试版系统但不稳定性，不建议各位玩家盲目跟风。兴趣强烈的话，记得做好安全措施(ps:做好备份，预防隐患。安装出现禁止符号，无法正常引导安装时留言回答。)


|功能|Mojave运行状态|
|--|--|
|触控板|使用万能驱动，支持部分手势。建议关闭触控板静默点按和用力点按功能以防止自动关机、重启的问题|
|睡 眠|唤醒无黑屏、声卡，麦克风正常。有线网络睡眠唤醒后会掉网|
|网 络|支持手机热点USB连接，蓝牙分享连接。更换独立网卡后支持正常网络功能|
|声 卡|声卡、麦克风正常。如果耳机无声等等按驱动文件夹(Kexts)里的声卡文件夹的提示操作，重复开关机会导致概率性无法驱动(没人会像我疯狂开关机测试吧😂)|
|显 卡|正常驱动核显HD630|
|USB|内建相关USB设备，摄像头，USB3.0接口。高清HDMI接口正常。添加SD卡驱动，未测试|
|Fn键|部分按键正常驱动使用|
|电源|正常|



* 目前修改了两款主题，一个是仿原生bootcamp的，另一个就是锤石666.可以根据需要修改themes里的主题。

![hd1](https://github.com/Wmyaaa/Dell5577-hackintosh-clover/blob/master/pic/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-16%20%E4%B8%8B%E5%8D%888.06.56.png)
![hd2](https://github.com/Wmyaaa/Dell5577-hackintosh-clover/blob/master/pic/屏幕快照%202019-04-16%20下午8.07.55.png)
![hd3](https://github.com/Wmyaaa/Dell5577-hackintosh-clover/blob/master/pic/屏幕快照%202019-04-16%20下午8.08.16.png)
![hd4](https://github.com/Wmyaaa/Dell5577-hackintosh-clover/blob/master/pic/screenshot6.png)
![hd5](https://github.com/Wmyaaa/Dell5577-hackintosh-clover/blob/master/pic/screenshot0.png)
