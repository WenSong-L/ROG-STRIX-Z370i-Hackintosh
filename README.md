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


#### BIOS设置:

|||
|----|----|
|Fast Boot|禁用|
|CFG Lock|禁用|
|VT-d|禁用|
|CSM|禁用|
|Intel SGX|禁用|
|Secure Boot|禁用|
|VT-x|启用|
|Above 4G decoding|启用|


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

- 非Navi显卡请移除 boot-args : agdpmod=pikera

- csr-active-config : E70B0000(Big Sur)  E7030000(Catalina)

- 4K屏可修改 UIScale 为 02


#### 其他问题请参阅 [使用 OpenCore 引导黑苹果](https://blog.xjn819.com/post/opencore-guide.html) / [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html)

-------------------------------------------------------------------------------------------------------------

#### 2022-01-27
 - 未测试，请反馈。
 - 删除wifi/蓝牙 kext
 - Linux(EXT4)引导
 - 启用Disable RTC wake scheduling(睡眠时被RTC时钟唤醒)
 - boot-args:shikigva=80 尝试使用vege56/64 RX5700/XT等A卡的 DRM.
 - 隐藏引导界面的功能项(需要时请按空格键)

#### 2021-11 更新
 - 未测试，请反馈。
 - 更新 opencore0.7.5
 - 更新 HfsPlus.efi 以支持 macOS12
 - 网卡建议更换白果卡，1820A在12系统下情况未知。


#### 2021-09-07 更新
 - 更新至 opencore0.7.3
 - APFS策略变更，安装Catalina请修改 UEFI-->APFS-->MinDate/MinVersion 请填 -1
 - 删除csr-active-config，开启AllowToggleSip。OC引导界面可选择 开启/关闭 SIP 。
 - 加强对Linux的引导(OpenLinuxBoot.efi)




#### 2021-06-09 更新

 - 更新 opencore0.7.0 和 Kext
 - 更新 主题 Resources 适配 0.7.0
 - 修改引导扫描策略 ScanPolicy ,扫描文件系统:APFS+HFS+NTFS, 扫描设备类型:SATA+NVMe+USB.
   如需引导Linux或其他设备类型，请参考opencore官方文档修改ScanPolicy值，或暂时改为 0 .



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
