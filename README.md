# HeartRate
> 调研报告：基于光电传感器技术的心率/脉率检测方法研究
一个Arduino为微处理器的心率检测仪，传感器为光电传感器，实时显示心率。
# 基于光电传感器的心率/脉率检测方法研究
## 基本原理
### [光电转化原理]("https://zh.wikipedia.org/wiki/%E5%85%89%E7%94%B5%E4%BA%8C%E6%9E%81%E7%AE%A1 "光电二极管")
一个光电二极管的基础结构通常是一个PN结或者PIN结。当一个具有充足能量的光子冲击到二极管上，它将激发一个电子，从而产生自由电子（同时有一个带正电的空穴）。这样的机制也被称作是内光电效应。如果光子的吸收发生在结的耗尽层，则该区域的内电场将会消除其间的屏障，使得空穴能够向着阳极的方向运动，电子向着阴极的方向运动，于是光电流就产生了。实际的光电流是暗电流和光照产生电流的综合，因此暗电流必须被最小化来提高器件对光的灵敏度。<br>
**光电导模式** <br>
当工作在这一模式时，光电二极管常常被反向偏置，急剧的降低了其响应时间，但是噪声不得不增加作为代价。同时，耗尽层的宽度增加，从而降低了结电容，同样使得响应时间减少。反向偏置会造成微量的电流（饱和电流），这一电流与光电流同向。对于指定的光谱分布，光电流与入射光照度之间呈线性比例关系。<br>
尽管这一模式响应速度快，但是它会引发更大的信号噪声。一个良好PIN二极管的泄漏电流很小（小于1纳安），因此负载电阻的约翰逊·奈奎斯特噪声（Johnson–Nyquist noise）会造成较大的影响。<br>
### 光电容积法

## 项目设计方案
基于光电传感器，小型便携家用心率测量，使用三个七段数码管显示。（戒指/指套？太小可能实现不了）<br>
肤色不同、手指粗细不同，绿光与红光的区别，光电容积法PPG<br>

## 系统结构设计

# 基于光电传感器的心率/脉率检测系统具体器件选型
发光二极管LED：AM2520(绿)<br>
光接收器：APDS-9008 //光敏电阻or光电二极管<br>
运放：MCP6001<br>
差分放大：<br>
滤波：<br>
微处理器：arduino uno<br>
显示：LCD 16X2<br>
电源：<br>

# 参考
1. [Pulse serson](https://pulsesensor.com/ "光电传感器模块")<br>
2. [TINKERCAD](https://www.tinkercad.com/ "Arduino仿真")<br>

# 测量仪器设计拓展
## 一般结构
* **传感器：** 实现生理信号从非电量到电量的变换；<br>
* **传感器接口电路：** 将传感器输出信号转换成低输出电阻的电压信号；<br>
* **放大滤波器：** 获得纯净可识别信号；<br>
* **ADC：** 模拟/数字变换，得到数字信号；<br>
* **微处理器/微控制器：** 实现信号输出显示、存储、控制，以及改变电路参数。<br>

## 设计原则
确定目标，总体框架，功能模块，具体技术，具体型号，参数选择<br>
先从整体考虑，逐步精细化，直至达成目标。(自上而下)<br>
1. 被测量的量是什么？信号的大小与频率是多少？（心率，很小，60~100次/min）<br>
2. 输出是什么？如何与使用者传达信息？（通过显示屏输出）<br>
3. 仪器的测量的精度、性能<br>
4. 仪器的使用条件<br>
5. 仪器的功能（测量心率）<br>
6. ~~成本、工艺条件~~<br>