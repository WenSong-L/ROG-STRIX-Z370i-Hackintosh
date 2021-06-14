<font color=#66ccff>**opencore for 华硕ROG STRIX Z370-I GAMING**</font>



#### 根据 Xjn´s Blog [使用 OpenCore 引导黑苹果](https://blog.xjn819.com/post/opencore-guide.html) 制作

#### 主要硬件信息:

|硬件|型号|
|----|----|
|CPU|I3-9300|
|主板|ROG Strix Z370-I Gaming|
|显卡|RX5500XT (Navi)|
|核显|UHD630(无输出仅硬解)|
|网卡|1820A|
|硬盘|NVMe+SATA SSD|


#### 此EFI特性:

- 支持 <font color=red>Big Sur</font> 及 <font color=red>Catalina</font>

- 电源管理完善
- ~~CPU变频定制(CPUFriend) ，睿频积极性为高~~
- USB定制 ( **无前置USB**。后置接口完善，包括 type-c )
- HD630@1.15GHz
- 使用了opencore主题及开机duang声

#### 注意事项:

- ACPI--->SSDT-PLUG-DRTNIA.aml 为 Haswell--Comet Lake 的CPU加载原生电源管理，此文件包含过多代码，仅做第一次安装时使用。安装成功后请参考这里[中文](https://blog.xjn819.com/post/opencore-guide.html)3.4章节 或[英文](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-platform.html#desktop)
来定制更符合自己CPU的SSDT。
- ~~非RX5500XT请移除 DeviceProperties--->Add--->PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)~~
- 非Navi显卡请移除 boot-args : agdpmod=pikera
- csr-active-config : E70B0000(Big Sur)  E7030000(Catalina)
- ~~PlatformInfo--->Generic 已清空~~

#### 其他问题请参阅 [使用 OpenCore 引导黑苹果](https://blog.xjn819.com/post/opencore-guide.html) / [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html)

-------------------------------------------------------------------------------------------------------------

#### 2021-06-09 更新

 - 更新 opencore0.7.0 和 Kext
 - 更新 主题 Resources 适配 0.7.0



#### 2021-05-27 更新

 - 更新 opencore0.6.9 和 Kext
 - 更新主题，文件体积减小了
 - 移除不必要的SSDT. 网卡和声卡不再需要注入DeviceProperties





#### 2021-01-05 更新
 - 更新 opencore0.6.5 及部分 Kext
 - 替换CPU电源管理为通用型 SSDT-PLUG-DRTNIA.aml 强烈建议自己定制
 - 移除 CPUFriend.kext 和 CPUFriendDataProvider.kext 避免可能对其他型号CPU的影响,
   可参考博客自己定制变频优化(非必要)。
 - 移除 RX5500XT 显卡的参数，非 Navi 显卡依然要删除 boot-args:agdpmod=pikera
 - 补全随机的 PlatformInfo
 

~~[微云](https://share.weiyun.com/neWqa1eb)
密码：cmtcph~~



![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/kext.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/usb.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/设备.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.39.44.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.48.20.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.48.49.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.49.31.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.50.01.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.53.30.png)
