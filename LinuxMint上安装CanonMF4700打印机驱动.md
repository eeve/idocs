# LinuxMint上安装CanonMF4700打印机驱动

CannonMF4700这款打印机在Cannon的官方服务支持页面无法找到针对Linux版本的驱动。

Google了一番，在www.ufriidriver.com 上找到了相关的驱动程序。尝试安装确认成功打印

## 下载驱动

找到对应版本的驱动，如无相应版本，可以尝试使用近似的版本驱动。

例如我的打印机型号是`Canon-MF4700`，但是无法找到相应的型号驱动，用的是`Canon-MF4800`的驱动，也能成功。


## 安装驱动

```
tar -zxvf Linux_UFRII_PrinterDriver_V330_uk_EN.tar.gz
cd Linux_UFRII_PrinterDriver_V330_uk_EN
sudo ./install.sh
```

## 驱动下载地址

http://www.ufriidriver.com/canon-mf8400-ufrii-lt-driver-64-bit-32-bit/

http://www.ufriidriver.com/canon-mf4600-series-ufrii-lt-driver-windows-7-8-10/