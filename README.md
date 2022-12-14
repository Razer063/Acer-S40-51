# Acer-S40-51
FIRST of ALL：宏碁的SATA MODE默认不是AHCI模式，请先在WIN10的MSCONFIG中开启“安全引导-最小”，重启先进BIOS，在BIOS设置MAIN栏里按CTRL+S，出现SATA MODE后修改为AHCI，此时进入WIN10为安全模式，再次进入MSCONFIG关闭安全引导后重启即可安装MAC系统，一定要这样否则你会在安装时找不到SSD，直接修改AHCI而不通过WIN10的安全模式会导致无法进入WIN10系统。

## 电脑配置

|   规格   |                         详细信息                          |
| :------: | :-------------------------------------------------------: |
| 电脑型号 |                  宏碁 S40-51 笔记本电脑                   |
| 操作系统 |                  macOS Monterey 12.x                     |
|  处理器  |                   英特尔 Core i5-10210U                   |
|   内存   |                   12 GB ( DDR4 2400MHz )                   |
|   硬盘   | 西数 WDC PC SN520 SDAPNUW-512G-1014 ( 512 GB / 固态硬盘 ) |
|   显卡   |                    英特尔 UHD Graphics 630                   |
|  显示器  |               LG ( 14 英寸 )                |
|   声卡   |                      Realtek ALC256                       |
|   网卡   |                       改装网卡DW1820A DELL                       |


## 安装部分

- #### 安装教程

  - `F2`进入BIOS,
  - 先查看

- 安装之后操作

  - 安装好系统之后，先用制作好的EFI文件进入系统

  - `终端`执行以下代码

  - ```
    sudo spctl --master-disable
    ```

  - 再执行重建缓存：

  - ```
    sudo kextcache -i /
    ```

  - 完整替换EFI

  - 最后重启完成

## 正常工作部分
- 核心显卡
- 电源、电池电量显示
- 屏幕、亮度调整
- 无线网卡、蓝牙
- 声卡、声音调整
- 睡眠
- CPU正常睿频
- 短时间睡眠
- 摄像头
- 键盘映射（睡眠、亮度、触控板、屏幕、声音）
- 风扇似乎可以根据电脑温度、CPU睿频智能调整转速

## 异常部分（已知问题）
- 可能会有长时间睡眠睡死的情况，需要强制重启
- 风扇无法驱动，无法查看转速
