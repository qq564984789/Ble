## GATT
> 现在低功耗蓝牙（BLE）连接都是建立在GATT（Generic Attribute Profile）协议之上。GATT是一个*在蓝牙连接之上的发送和接收很短的数据段*的通用规范，这些很短的数据段被称为属性（Attribute）。在BLE中所有的协议(Profile)或者服务(Service)都是基于GATT(Generic Attribute Profile)的。

## GAP
> GAP（Generic Access Profile），它在用来控制设备和广播。GAP使你的设备被其他设备可见，并决定了你的设备是否可以或者怎样与合同设备进行交互。例如Beacon设备就只是向外广播，不支持连接，小米手环就等设备就可以与中心设备连接。
1. 设备角色
GAP给设备定义了若干角色，其中主要的两个是：外围设备（Peripheral）和中心设备（Central）。
> 外围设备：这一般就是非常小或者简单的低功耗设备，用来提供数据，并连接到一个更加相对强大的中心设备。例如小米手环。
>  中心设备：中心设备相对比较强大，用来连接其他外围设备。例如手机等。
2. 广播数据
在GAP中外围设备通过两种方式向外广播数据：Advertising Data Payload(广播数据)和Scan Response Data（扫描回复），这里包含一些设备额外的信息，例如设备的名字。
3. 广播流程

![广播流程](http://upload-images.jianshu.io/upload_images/4767316-5496ee806b058916.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## Profile
> Profile,可以理解为一种规范(通信协议)，profile存在于从机中。
SIG规定了一些profile，如心率计，防丢器，HID OVER GATT等等。每个Profile中都包含多个Service。每个Service代表从机的一个能力。

## Service
> Service可以理解为一个服务，在BLE从机中，可以有多个服务，譬如系统电量信息服务，系统信息服务，每个Service又包含多个Characteristic。每个具体的Characteristic值才是BLE通信的主体。比如当前电量是80%，会通过电量的Characteristic特征值存在从机的Profile里面，这样，主机就可以通过这个Characteristic值获得从机的80%电量值。

## Characteristic
> Characteristic :BLE主从机通信均通过Characteristic实现。 可以理解为一个标签，通过这个标签可以获取或写入想要的内容。

## UUID
> UUID :唯一识别码。上述Service 和 Characteristic 均需要通过一个UUID来识别。UUID为128，但是在BLE中，UUID通常用16位，也就是两个字节来替代。16位UUID和128位UUID可以相互转换，具体如何实现需参考SIG文档。


综上，每个从机均由一个或若干个profile构成，不管是simpleprofile还是防丢器Profile等，而每个profile又由一些列Service组成，每个Service包含若干个Characteristic。 主机和从机之间的通信均是由 Characteristic实现。



对于  Proximity Profile，含有如下services:
1. TX Power Service(发射功率服务)
2. Immediate Alert Service (即时报警服务)
3. Link Loss Service (连接丢失服务)
4. Battery Service(电池服务)
5. Immediate Alert Service(定位器服务)

(http://www.cnblogs.com/cb168/articles/4844010.html)
(http://www.2cto.com/kf/201511/450188.html)
(http://blog.csdn.net/xingqingly/article/details/38343405)
(http://www.jianshu.com/p/2b09498b84f2)

