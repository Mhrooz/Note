# 4 The Medium Access Control(MAC) Sublayer

**broadcast channels** are sometimes referred to as **multiaccess channels** or **random access channels**

This chapter mainly told how to allocate the channels.

## 4.1 The Channel Allocation Problem

conference call chaos. Who can talk at same time?

### 4.1.1 Static Channel Allocation

FM band

the amount of senders is small.

传统方法是 FDM 频分多路复用

总共有N个用户就会分成N等分

每个用户会有自己的频段，互不干涉

优点：

简单有效

缺点：

大量宝贵的频谱被浪费

由于数据流量往往是突发性的，所以大多数信道在大多数情况是空闲的

### 4.2.2 Dynamic Channel Allocation 动态信道分配

动态信道分配基于五个基本假设：

1. 站模型(station model)
   一旦一帧被形成，则该站被阻塞

2. 单信道假设(single channel assumption)
   对于所有的通信都只有一个信道可以使用

3. 冲突假设(collision assumption)
   两帧同时被传送则会产生冲突，得到混乱的信号
   所有的站都可以检测到冲突
   冲突的帧之后必须再次发送
   除了冲突，不会有其他错误

4. 连续时间或者分槽时间(Continuous Time)
   任何时间都可以传输帧，不需要通过将一个主时钟时间分散成离散的间隔
   时间被分成离散的间隔，帧的传送总是从一个时槽的起点发送
   一个时槽可能包含0，1，多个帧
   对应空闲时槽，发送时槽，冲突时槽

5. 载波检测或者无载波检测
   发送前可以知道信道有没有被占用
   如果检测到则不能使用，直到空闲为止 通常用于有线网络

   发送前不能检测，传输后判断是否发送成功 通常用于无线网络

   

## 4.2 Multiple Access Protocols 多路访问协议

多路访问信道的算法

### 4.2.1 ALOHA

ALOHA 不同版本的差别在于是否将时间分成离散的时槽

#### 纯ALOHA(Pure ALOHA)

有数据，就传输

冲突帧被损坏，

## 4.4 Wireless Lans (无线LAN)

### 4.4.1 The 802.11 Architecture and Protocol Stack 802.11 协议栈

802.11中，MAC决定下一个改由谁传输数据

MAC子层上面是LLC，隐藏不同标准间的差异

802.11规定物理层上允许的三种技术

分别是红外线，FHSS，DSSS

都是用2.4GHzISM

OFDM，HRDSS被引入

达到更高速度

OFDM被引入

与之前不同的频率

802.11a 5GHz

802.11g 2.4GHz

给到54Mbps

802.11n 

四天线和更宽的信道

给到600Mbps

### 4.4.2 802.11 physical layer 802.11 物理层

#### 802.11b

通常是在11 Mbps

和CDMA系统比较相似

低速使用barker sequence 编码

高速使用 CCK编码

#### 802.11a

在5GHz中使用54Mbps速度

使用OFDM技术：
优点：使频谱更有效率，并且可以抵抗无线信号的劣化

位通过52个子携带者平行的发出，其中48个是携带数据的，4个用来同步
每个信号持续4us，发送1，2，4，6位。实际只有1/2,2/3,3/4的数据没有被毁掉。
802.11a可以传输6-54Mbps的速度

但是802.11b是802.11a的7倍长

#### 802.11g

将802.11a的技术复制到2.4Ghz

也可以提供54Mbps的速度

兼容802.11b的设备

#### 802.11n

可以提供100Mbps以上的速度

使用MIMO技术大大提升速度

### 4.4.3 The 802.11 MAC Sublayer Protocol MAC子层协议

两个问题：暴露站和隐藏站
隐藏站是一个单元中的某一部分正在进行的传输可能不会被同一个单元中的其他地方接收到
暴露站是一个单元的某一部分正在进行的传输的对象可能不是想要传输单元的对象。（糊弄

![image-20210108203446171](The%20Medium%20Access%20Control%20Sublayer.assets/image-20210108203446171.png)

使用dcf和pcf来解决这个问题

dcf是802设备必须实现的，pcf是选择实现的

#### DCF

使用CSMA/CA协议

支持两种操作方法：

1. 当一个站想要传送数据的时候，它首先监听信道。如果信道空闲，它就开始传送，在传送过程中不监听，直接送出所有帧，但这种情况下接收方可能因为干扰数据被毁坏。如果信道正忙，则发送方推迟到信道空闲，在传送。如果冲突发生，则冲突的站等待一段使用二元指数后退算法随机出时间在发送。

2. 以MACAW为基础，使用虚拟信道监听的方法

   有A,B,C,D四个无线站点，A可以覆盖BC，B可以覆盖ACD。现在A想要给B发送数据
   AB视角

   1. A给B发送RTS，请求发送许可
   2. B收到请求，发送准许许可CTS帧
   3. A收到CTS，发送帧，启动ACK定时器
   4. B收到完整数据，向A发送ACK
   5. 如果ACK在A收到之前已经超时，则重复上述步骤

   CD视角，为了全局着想，不占用信道

   1. C收到RTS帧，估算一共需要多久，向内部传输NAV信号
2. D收到CTS帧，也向内部传输NAV信号
   

RTS/CTS被证明没什么用 = =

802.11允许传输的帧分成很小的**碎片(fragments)**，碎片有自己的校验和

若使用停-等协议(stop-and-wait protocol)，分片被单独编号和确认

若分片损坏只需要重传分片，提高吞吐量（因为帧越长越容易出现传输失败的情况）

坏处是收到第一个ACK所有的NAV都会停止，可能会被干扰

#### PCF

PCF 由基站对其他的站进行表决，问是否要发送帧