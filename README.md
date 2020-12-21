<font color=#66ccff>**opencore 0.6.4 for 华硕ROG STRIX Z370-I GAMING**</font>



#### 根据 Xjn´s Blog [使用 OpenCore 引导黑苹果](https://blog.xjn819.com/post/opencore-guide.html) 制作

#### 主要硬件信息:

- CPU : I3-9300 (PR.PR00)
- 主板 : 华硕Z370i
- 显卡 : RX5500XT (Navi)
- 网卡 : 1820A
- 其他硬件差异无妨

#### 此EFI特性:

- 支持 <font color=red>Big Sur</font> 及 <font color=red>Catalina</font>

- 电源管理完善
- CPU变频定制(CPUFriend) ，睿频积极性为高
- USB定制 ( 无前置USB。后置接口完善，包括 type-c )
- HD630@1.15GHz
- 使用了opencore主题及开机duang声

#### 注意事项:

- ACPI--->SSDT-PLUG.aml 专为 CPU PR.PR00 定制，非此型号自己修改
- 非RX5500XT请移除 DeviceProperties--->Add--->PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)
- 非Navi显卡请移除 boot-args : agdpmod=pikera
- csr-active-config : E70B0000(Big Sur)  E7030000(Catalina)
- PlatformInfo--->Generic 已清空

#### 其他问题请参阅 Xjn博客 [使用 OpenCore 引导黑苹果](https://blog.xjn819.com/post/opencore-guide.html)

![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.39.44.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.48.20.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.48.49.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.49.31.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.50.01.png)
![](https://github.com/WenSong-L/ROG-STRIX-Z370i-Hackintosh/blob/main/Screenshot/截屏2020-12-21%20下午11.53.30.png)
