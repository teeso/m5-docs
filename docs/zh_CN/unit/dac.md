# DAC - 数模转换Unit {docsify-ignore-all}

<img src="assets/img/product_pics/unit/M5GO_Unit_dac.png" width="30%" height="30%"> <img src="assets/img/product_pics/unit/unit_dac_grove_a.png" width="30%" height="30%">

***

:memo:**[描述](#描述)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:octocat:**[例程](#例程)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🛒**[购买链接](https://item.taobao.com/item.htm?spm=a1z10.3-c.w4002-1172588106.28.312f425eRDFbqp&id=580257615943)**

<!-- :memo:**[描述](#描述)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:octocat:**[例程](#例程)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:electric_plug:**[原理图](#原理图)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🛒**[购买链接](https://item.taobao.com/item.htm?spm=a1z10.3-c.w4002-1172588106.28.312f425eRDFbqp&id=580257615943)** -->

## 描述

**<mark>DAC</mark>** 是一款集成数字信号转模拟信号芯片的Unit，能够实现输出模拟信号，如电压、声音等，内置的DAC芯片型号是**MCP4725**，并且不带EEPROM。

## 特性

-  高达12位的转换精度
-  0~3.3V幅度的电压输出
<!-- -  GROVE接口，支持[UIFlow](http://flow.m5stack.com)编程，[Arduino](http://www.arduino.cc)编程 -->
-  Unit内置两个Lego插件孔，方便与Lego件结合

## 应用

-  MP3播放器
-  mini信号发生器

## 相关链接

- **[官方频道视频](https://i.youku.com/i/UNjE1ODA2MzE0OA==?spm=a2hzp.8253869.0.0)**

- **[官方论坛](http://forum.m5stack.com/)**

-  **数据手册** - [MCP4725](http://pdf1.alldatasheet.com/datasheet-pdf/view/233449/MICROCHIP/MCP4725.html)

## 例程

### 1. Arduino IDE

*以下仅为用法示意，并不完整。如果需要完整例程请点击[这里](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/DAC/Arduino)。*

```arduino
/*
    hardware : m5stack uint dac
    please install adafruit MCP4725 lib
*/
#include <Wire.h>
#include <Adafruit_MCP4725.h>

// new a object
Adafruit_MCP4725 dac;

// initialization
dac.begin(0x60);
dac.setVoltage(2048, false);

// 12bit value , false mean not write EEPROM
dac.setVoltage(1024, false);// input digital value "1024" to unit
delay(1000);
dac.setVoltage(2048, false);// input digital value "2048" to unit
delay(1000);
```

<!-- ### 2. UIFlow -->

<!-- <img src="assets/img/product_pics/unit/unit_example/example_unit_dac_01.png" width="30%" height="30%"> <img src="assets/img/product_pics/unit/unit_example/example_unit_dac_02.png" width="55%" height="55%">

具体例程请点击[这里](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/DAC/UIFlow)。 -->

## 原理图

<img src="assets/img/product_pics/unit/dac_sch.JPG">

### 管脚映射

<table>
 <tr><td>M5Core(GROVE接口A)</td><td>GPIO22</td><td>GPIO21</td><td>5V</td><td>GND</td></tr>
 <tr><td>数模转换Unit</td><td>SCL</td><td>SDA</td><td>5V</td><td>GND</td></tr>
</table>