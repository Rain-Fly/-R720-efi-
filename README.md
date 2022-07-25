# 联想拯救者R720安装黑苹果

### 一、基本参数：

> CPU: I5-7300HQ   
> 
> 核心显卡: HD630 
> 
> 独立显卡 N1050Ti
> 
> MacOS ： macOS Monterey 12.4 
> 
> OpenCore：0.8.0

### 二、安装步骤：

#### a）教程及相关资源：

[新手挑战黑苹果-超详细的OpenCore黑苹果安装教程](https://www.bilibili.com/video/BV18V41187JZ?p=1&share_medium=android&share_medium=android&share_medium=android&share_medium=android&share_plat=android&share_plat=android&share_plat=android&share_plat=android&share_source=COPY&share_source=COPY&share_source=COPY&share_source=COPY&share_tag=s_i%25C3%2597tamp%3D1616727523&share_tag=s_i%25C3%2597tamp%3D1616727523&share_tag=s_i%C3%97tamp%3D1616727523&share_tag=s_i%25C3%2597tamp%3D1616727523&unique_k=uNWbnL&unique_k=uNWbnL&unique_k=uNWbnL&unique_k=uNWbnL&vd_source=2c89c7c11b923bc0c820cde3df8b7a3b%255D%255D%28https%3A%2F%2Fwww.bilibili.com%2Fvideo%2FBV18V41187JZ%3Fp%3D1&vd_source=2c89c7c11b923bc0c820cde3df8b7a3b%255D%29%29%28%5Bhttps%3A%2F%2Fwww.bilibili.com%2Fvideo%2FBV18V41187JZ%3Fp%3D1&vd_source=2c89c7c11b923bc0c820cde3df8b7a3b%5D%28https%3A%2F%2Fwww.bilibili.com%2Fvideo%2FBV18V41187JZ%3Fp%3D1&vd_source=2c89c7c11b923bc0c820cde3df8b7a3b%29%29)

视频下面参考资源地址:

1、macOS镜像下载：[黑果小兵的部落阁](https://blog.daliansky.net/)  
2、启动盘制作工具balenaEtcher下载：https://www.balena.io/etcher/  
3、OpenCore下载：https://github.com/acidanthera/OpenCorePkg/releases  
4、OpenCore驱动下载：[Gathering files | OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/ktext.html)  
5、OpenCore编辑器：[Releases · ic005k/OCAuxiliaryTools · GitHub](https://github.com/ic005k/QtOpenCoreConfig/releases)  
6、OpenCore排错：https://opencore.slowgeek.com/  
7、磁盘精灵：[数据恢复软件,硬盘分区工具,系统备份软件 - DiskGenius官方网站](https://www.diskgenius.cn/)

<mark>黑果小兵的DMG镜像下载要注意使用以下这个版本</mark>

[macOS Monterey 12.4 21F79 Installer for OpenCore 0.8.0 and CLOVER 5142 and FirPE.dmg](https://mp.weixin.qq.com/s?__biz=MjM5OTAzMTI0OA==&mid=2450024949&idx=1&sn=8c03a842cd471d3eae4105a9c8ce91d2&chksm=b13d714a864af85c13a8d547e3ecb8a07e15d612b26ce35e03b362dcc878492035cc4972abd3&scene=127&ascene=78&devicetype=android-31&version=2800183f&nettype=WIFI&abtest_cookie=AAACAA%253D%253D&lang=zh_CN&exportkey=ASr2I%252BCyvCzi6eCyFJUmAqk%253D&pass_ticket=OUiuphDvhoVq7ZSdD1EoaCxiVaDtpjFC7PgLBChRmVikGG8IjbYXM%252BEfaDhTID8f&wx_header=3)

#### b) 参考EFI

1. EFI/1.zip 

2. EFI/2.zip

参考上述两个大佬的EFI， 拿到1 进行引导启动安装都可以正常进入系统，  注意 三个分区选择openCore 启动引导  ， 但是进入系统后 发现 蓝牙 WIFI  HDMI外接  全部无法驱动。

#### c) 解决相关上述缺陷

  WiFi 和蓝牙主要参考 

[关于在macOS 12 Monterey上驱动Intel网卡、蓝牙_华米OV的博客-CSDN博客_黑苹果intel蓝牙驱动](https://blog.csdn.net/qq_24028389/article/details/119961192)

 上述示例中主要注明 12系统中 可以提供多种驱动合集。 主要是引入以下两个驱动

![](/Users/rain/Library/Application%20Support/marktext/images/2022-07-24-17-13-23-image.png)



显卡HDMI 驱动异常主要参考一下：

[i7-9700k,UHD630核显，HDMI接口，usb3.0,成功黑苹果！-远景论坛-微软极客社区](https://bbs.pcbeta.com/viewthread-1839602-1-1.html)





自动更新关闭，并取消红点

[如何取消Mac的小红点和忽略版本升级？](https://zhuanlan.zhihu.com/p/436624540)
