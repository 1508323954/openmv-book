# HelloWorld例程详解

01Basic——helloworld.py例程详细中文注释如下，

```python
# Hello World Example
#
# Welcome to the OpenMV IDE! Click on the gear button above to run the script!

import sensor, image, time          
#导入依赖的模块，sensor感光元件参数设置模块，image图像处理模块，time计时模块。

sensor.reset()                      
#复位和初始化感光元件

sensor.set_pixformat(sensor.RGB565)
#设置图像输出格式，OV7725可以设置成RGB565或者GRAYSCALE，MT9V034只能设置成GRAYSCALE

sensor.set_framesize(sensor.QVGA)   #设置图像像素大小，
#sensor.QQVGA: 160x120，sensor.QQVGA2: 128x160 (用于LCD扩展板)，sensor.QVGA: 320x240，
#sensor.VGA: 640x480, sensor.QQCIF: 88x72，sensor.QCIF: 176x144，sensor.CIF: 352x288

sensor.skip_frames(time = 2000)     
#跳过前2000ms的图像，等待感光元件变稳定再读取图像的数据

clock = time.clock()                
#初始化时钟

while(True):                        #while循环

    clock.tick()                    #开始计时

    img = sensor.snapshot()         #拍摄一张照片，返回一个Image对象，赋值给img变量。

    print(clock.fps())              #停止计时，返回当前的帧率，并打印当前的帧率。
```