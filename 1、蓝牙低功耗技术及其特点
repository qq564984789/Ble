## 什么是低功耗蓝牙技术？
- BlueTooth 4.0的一部分
- 应用于无线个人局域网（Wireless Personal Area Network）:一个Master可以同时连接多个Slave(最多8个)。Master可以理解为电脑主机，Slave可以理解为电脑周边的外设。
- 特点：低功耗（Low Power）、低延迟(Low Latency)、低吞吐量(Low throughput)

## TI技术方案,按适用场景分类如下：
### 低功耗传感器：CC2540/1
特点：
1、使用纽扣电池，1年左右寿命
2、无需苹果MFi认证
3、数据传输速率小于100Kbps

### 语音（数据）：CC2560/4 +MSP430
特点：
1、支持传统蓝牙和BLE
2、最大到3Mbps的数据速率

### 音乐：CC2560/4 +MCU(32bit:例如Cortex-M)

## BLE vs WiFi
### 物理信道
3个广播通道、37个连接（数据）通道，每个信道2MHz带宽。BLE的广播通道有效避开了WiFi的通道（1,6,11）.因此BLE和WiFi的互存性较好。
### 最小供电电源
BLE:Coin Cell（最小至2.1V）   BT（传统蓝牙）:AAA   WiFi:Li-ion(锂电池)

### 最大吞吐量（Maximum Throughput）
BLE:1Mbps   BT（传统蓝牙）:3Mbps   WiFi:50Mbps


## 蓝牙Logo
Bluetooth Smart:低功耗蓝牙设备，只能和Bluetooth Smart、Bluetooth Smart Ready通信。例如腕表、可穿戴眼镜、属于单模设备。
Bluetooth Smart Ready：可以和Bluetooth Smart、Bluetooth Smart Ready、Bluetooth通信。例如手机，电脑，属于双模设备。   
Bluetooth:传统蓝牙，可以和Bluetooth Smart Ready、Bluetooth通信。例如耳机、键盘、麦克风。

## Single Mode vs Dual Mode
双模：同时支持Classical Bluetooth 和BLE。和Classical Bluetooth通行时，使用Classical Bluetooth技术。和BLE通信时，使用BLE技术。
典型设备：CC2564
特点：保持传统蓝牙的性质，如:
1、对于class 1设备，有效传输距离达100m
2、发送功率：+10dBm
3、接收灵敏度：-93dBm
4、功耗和传统蓝牙相同
