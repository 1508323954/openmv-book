# OpenMV快速上手教程

## 驱动的下载和安装

### Windows驱动安装

将OpenMV Cam插到电脑上，正常情况Win10系统会自动安装驱动，不需要手动安装，这时在设备管理器中会看到串口：

![串口驱动1](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A81.png?raw=true)

但是Win7系统驱动不会自动安装驱动，这时在设备管理器中会出现一个叹号，表示没有正常安装驱动，这时就需要自己手动安装。

![串口驱动2](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A82.png?raw=true)

**下载驱动**

百度网盘下载链接：https://pan.baidu.com/s/1z_unhOWznVESR32ywlj0EQ

下载完后解压到桌面，然后右键设备管理器中的这个设备，然后选择**更新驱动程序软件**：

![串口驱动3](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A83.png?raw=true)

选择**浏览我的计算机以查找驱动程序软件**

![串口驱动4](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A84.png?raw=true)

点击**浏览**

![串口驱动5](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A85.png?raw=true)

选中桌面上的**openmv_windows驱动**文件夹

![串口驱动6](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A86.png?raw=true)

![串口驱动7](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A87.png?raw=true)

选择**始终安装此驱动程序软件**

![串口驱动8](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A88.png?raw=true)

这时应该会成功的安装好驱动。但是，如果你遇到下面的情况，就比较麻烦了。

![串口驱动9](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/%E4%B8%B2%E5%8F%A3%E9%A9%B1%E5%8A%A89.png?raw=true)

驱动安装失败，大部分的情况都是电脑的问题，精简版操作系统和使用了一些优化软件通常是引起此类问题的原因，这是因为精简版的 window 系统删掉了一些不常用的驱动信息引起的。

解决方法：

1、首先可以参考下面的文章试着解决：
      https://forum.singtown.com/topic/230
2、如果不能解决建议重装系统，最好MSDN的纯净的系统。

##  IDE的下载和安装
官网下载地址：https://openmv.io/pages/download

![IDE下载](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/IDE%E4%B8%8B%E8%BD%BD.png?raw=true)

OpenMV IDE是与OpenMV Cam一起使用的首选集成开发环境。 它具有强大的文本编辑器，调试终端和带有直方图显示的帧缓冲查看器。 OpenMV IDE可以轻松编程OpenMV Cam。OpenMV IDE支持跨平台的，分为Windows，MAC OS，Ubuntu和Rasberry PI的系统，最新的版本为v2.2.0。下面我们用Windows版本和Ubuntu版本为例讲解。
### Windows版本IDE的下载和安装
在官网上下载IDE安装包

![windows IDE下载1](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/win%20IDE%E4%B8%8B%E8%BD%BD1.png?raw=true)

下载的IDE安装包是一个exe文件

![windows IDE安装1](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/win%20IDE%E5%AE%89%E8%A3%851.png?raw=true)

双击exe文件，然后一直点击下一步安装

![windows IDE安装2](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/win%20IDE%E5%AE%89%E8%A3%852.png?raw=true)

正常安装完成后如下图：

![windows IDE界面](https://github.com/1508323954/openmv-book/blob/master/1-%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/pictures/win%20IDE%E7%95%8C%E9%9D%A21.png?raw=true)

### Ubuntu版本IDE的下载和安装

在官网上下载IDE安装包

下载的IDE安装包是一个.run可执行文件

用下面的命令安装：

```
   chmod +x openmv-ide-linux-x86_64-2.2.0.run 
  ./openmv-ide-linux-x86_64-2.2.0.run 

```
这时会出现图形化界面，然后一直点击下一步安装，

### IDE的使用


#### 运行Helloworld例程

用MicroUSB线将OpenMV Cam与电脑连接后，此时电脑上会弹出一个U盘。OpenMV先比较快的闪绿灯，然后亮一下白灯，最后一直慢闪蓝灯。打开IDE，默认打开的是HelloWorld的例程，点击左下角的连接按钮，先闪几下红灯，然后熄灭，还会弹出来三个对话框，提示要注册，都点击No就行，不影响使用，然后按绿色箭头按钮运行，右上角的图像缓冲区就会有图像显示出来。
注：如果不想每次连接弹出这三个对话框，也可以购买官方的license来注册，一个15美金，约合100人民币，捐助支持OpenMV项目。

如果没有右侧的图像缓冲区，窗口最右侧有一个三角按钮，点击一下就可以弹出。

#### 固件的升级
## 脱机运行

在IDE里面执行运行程序的时候， 代码并不会复制到openmv的文件系统中，也就是说，下一次上电运行时还是之前文件系统中的程序。所以如果想脱机运行， 需要将文件复制到SD卡或者Flash的根目录的main.py中。如果要自己定义主文件，需要修改boot.py中的入口文件。

## 注意事项

OpenMV有两个电源输入端：
>- VIN(有时也会标识为VCC)
>- USB输入

VIN输入为3.6V~5V，推荐5V。
USB和VIN可以同时供电。

OpenMV有一个电源**输出端**：

>3.3V，这个电压是OpenMV的稳压器输出的，用于给其他传感器供电。 注意：不要给3.3V直接供电，没有内部芯片的保护，很容易烧毁。

