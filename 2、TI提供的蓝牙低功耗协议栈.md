Profile:定义了各种不同的应用场景

BLE Stack:包含Control+Host两层。以库的形式提供，提供GAP、GATT、ATT、SM、L2CAP、HCI的各层API接口。
OSAL:提供源码，一个TI自己的简单版任务调度系统
HAL:提供源码，驱动和硬件API。
Application：提供源码，蓝牙SIG定义的Profile+TI自己实现的Profile.

### Host层
所有的数据通信通过ATT实现，ATT规定了Server和Client两端。Server端的数据都以Attribute形式存在。
一个设备可在某一时刻同时保持Server和Client的角色。

GATT是基于ATT的一个Profile,规定了在不同Profile中数据的组织方式，提供给上层Profiel使用。架构也是Server和Client两端，基本和ATT相同。
区别：GATT将ATT规定的Server端数据的attribute细分为service、characteristic。以service封装，以characteristic暴露数据。

GAP规定了4种角色：
1、Peripheral:一个可以被连接的广播者，如心率计。在连接中扮演从角色。
2、Central：扫面广播，并能发起连接，如手机。在连接中扮演主角色。
3、Broadcaster：:一个不可以被连接的广播者，如温度计。
4、Observer：扫面广播，但能发起连接，如温度显示器。
通常来讲：1、2组合在一起使用。3、4组合在一起使用。如果2中设备处于同一个角色，则它们之间也不能相互通信，如只支持外围设备的两方或者只支持中央设备的两方不能互相通信。

### Application层
一个Profile由不同的service组成，但里面至少要有1个service。service由不同的characteristic组成，里面至少要有1个characteristic。
