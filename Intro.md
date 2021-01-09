# Basis

## Importance of Electricity

### Electricity as carrier of Energy

### Electricity as carrier of Information

Information processing  ->  Automatic Control Engineering

Transfer information $\rightarrow$ 	Communication Engineering

## Electric Charge

### Historical Background

#### Ancient world

static electricity(静电) rubes objects.

#### since 18th century

begin of a systematic study of all phenomena related to electricity

lighting, magnetism, muscle contractions, chemical reactions

### The Term "Electric Charge"

经丝绸摩擦过的球可以吸引轻小物体

假设产生这种力的原因是一种“流体”

这种“流体”可以被触摸消除

这种流体就是"Electric charge"（电荷）,用物理量Q来表示

$Q$ 用库伦（C）做单位，也可以用安培秒(Ampere second, As)

$[Q]=C=As$

### Basic Properties of Electric Charge - The Sign 基础电荷属性-符号

同性相斥，异性相吸

对于电荷的正负没有绝对的量化符号，只是一个定义

### Basic Properties of Electric Charge - The Elementary Charge 基本电荷属性-单位点电荷

不可再分的基本单位 **电子** $e$

传统理论是连续理论

当电子数量到一定程度以后就是连续的

微观层面是离散的

### Basic Properties of Electric Charge - Electric Charge Flow 基本电荷属性-电荷流 就是电流

electric current 电流

conductors 导体 charge flow possible

semiconductor 半导体 改变温度光照使之在导体和绝缘体之间来回切换

dielectrics 介电质 insulator 绝缘体

 # Basic Electric Quantities

## Electric Potential / Voltage 电势 / 伏特

### The potential energy of separated charge

reference level 参照线

![image-20210102192127003](image-20210102192127003.png)

$ \varphi = \frac{W_{pot}}{q}$

* 电势被定义成每个电荷的势能

* 电势定义在点上，但是总是有一个参照等势线被定义成0，没有绝对的0电势

* 这是一个将电荷带到一个参考点所需要的能量值

* 如果电荷回到参考线，还是同样的能量

  

### The Potential Difference 电势差

The (Electric) Voltage

两点间的电势差被称作电势差... 电势差是有方向的。

正电势是从高电势指向低电势

### A Conductor under Potential Difference 在电势差下的导体

#### The Current 电流

如果有不同电势差的两个点被导体链接，电流(**current**)就会通过导体

高电势的电荷将会通过穿过导体到低电势能的地方降低它的能量，流动消耗能量（对比水从高重力势能到低重力势能产生动能）

## The (Electric) Current 电流

### The Current Strength 电流强度

用$ i $表示

电流用每极短单位时间内穿过的电荷量表示

$i = lim_{\Delta t \rightarrow 0}\frac{\Delta Q}{\Delta t} = \frac {dQ}{dt}$

$[i] = C/s = A(Ampere)$

如果正电荷移动的方向和电流的方向一样，电流是正电流

电流是标量，但是有方向

### Ohm's Law 欧姆定律

欧姆定律并不总是满足，有些不满足欧姆定律的材料被称作"**non-Ohmic**"

**Electrical Resistance 电阻**

电压和电流的比值在欧姆定律中是一个定值——电阻

电阻取决于材料以及几何形状

## Electric Power 电功率

当能量被电系统提供的时候，电功率是正值

假设电荷$q$从电势能为$\varphi_1$的点$P_{1}$移动到电势能为$\varphi_{2}$的点$P_{2}$,那么消耗的能量是
$$
\Delta W_{pot} = q(\varphi_{1}-\varphi_2)=qu_{12}
$$
传输过程中能量以光或者热的形式消耗

每单位时间电力系统提供的能量被称作功率
$$
p = \frac{\Delta W_{pot}}{t} = \frac{q}{t}(\varphi_1-\varphi_2) = \frac{q}{t} u_{12} = i·u_{12}
$$
功率用**Watt**为单位

# Elements and Components

## General Remarks

电路通常是**集总电路模型(lumped element model)**

|集总参数电路是说电路的几何尺寸远小于工作时候的电磁波波长。

特点是 电路中电磁现象分别集中在各元件上或者是各个空间上，电流的移动不需要时间，同一根导线上的电流处处相等|



电路通常由两个部分组成：

1. 电元件
2. 两个电元件的连接部分，对于不包括一部分电阻(resistance)，电感(inductance)，电容(capacitance)的理想导体

电元件产生(yield)一个关于电压和电流的函数关系，它具有物理上不存在的理想的特性。

|分布参数电路中的电流电压不仅是时间的函数，还是空间坐标的函数|

它构成电器网络的基本组成部分

有五个基础的电元件：

1. 电阻（理想电阻器，即符合欧姆定律的电阻器） |耗能集中|
2. 电容（理想电容器）|电能集中|
3. 电感（理想电感）|磁能集中|
4. （理想）电流源
5. （理想）电势源

其它的元件也可以被定义，但应该由这五个元件组成

**电气组件(An electric component (device))**是电器件的物理实现。它拥有一些非理想特性。它的特性可以通过用理想电器件组成的等效电路实现

***

一个实际电路可能有多个电路模型

不同的器件可以有相同的模型

电路处理的是信号，信号会有频率，频率会有宽频不同调制信号



### Classification of Elements 电器件的分类

**有源元件(An active element)** 为电路提供电能

注意： 有源元件经常被叫做起源(sources),但是，并没有给起源的能量，能量只能被转换。

**无源元件(A Passive element)** 从电路中消耗能量。

注意：如果有器件暂时存放能量，稍后也会把能量用在电路中，该器件也被视作无源元件

#### Linear and Non-Linear Elements 线性和非线性元件

线性元件符合叠加原理(The principle of superposition) 即 $i_1 = f(u_1)$,$i_2 = f(u_2)$,那么就有$f(u_1+u_2) = f(u_1)+f(u_2)$

非线性元件不考虑^

|

#### Linear and Non-Linear Circuit 线性和非线性电路*

描述电路特性的所有方程都是线性代数或者是微积分就是线性电路。

线性电路是完全由线性元件、独立元、线性受控源构成的电路。



### Proportion of electric components 电器件的组成

为了满足集总电路模型的假设，场量应该是常数

电磁激励？？？

实际电路的几何储存远小于其工作电磁波的波长$\lambda$时，可以认为传送的电路各处的电磁能量同时到达，整个电路为电磁空间的一个点
$$
\lambda = \frac{c}{f} \\
c是光速，f是频率
$$
电磁激励使得频率有了上限，集总电路模型是可行的

![image-20210103165432935](image-20210103165432935.png)

## Electric Connections

### Ideal Connection

理想链接由实线表示，可以有弯折

junctions (交叉)

理想导线没有电阻，并且可以没有电压降的携带电流

### Real Connection

大多数导线由金属制成

highly doped semiconductor

所有线缆都会产生电阻，以电流承载有上限，会以热的形式损失能量

### Ideal Sources 理想电源

#### (1) 理想电压源

符号

<img src="image-20210103190300426.png" alt="image-20210103190300426" style="zoom: 67%;" />

#### (2) 理想电流源

<img src="image-20210103190329659.png" alt="image-20210103190329659" style="zoom:67%;" />

注意电流和电压的方向在电源内和电源外的方向相反

### (Ideal) Dependent (or Controlled) Sources （理想）独立（或控制）源

![image-20210103191034374](image-20210103191034374.png)

### Real Voltage Sources 真实电压源

电源来自于其他的转换为电的能量

真正的电压依赖很多或者一部分电流（和理想电压源相反）

来源：

* 化学能——电池
* 机械能——发电机
* 电能——转换
* 其它——太阳能，生物能，潮汐发电

#### battery 电池

电池使用发生在电极(electrodes)和电解质(electrolyte)之间的化学反应来生成能量

#### Types of battery 电池的种类

* 一次性电池(Primary (disposable) batteries)

  化学反应不可逆
  只能使用一次
  类型：
  锌碳电池(Zinc-carbonbattery)
  碱性电池(Alkaline battery)

* 可充电电池(Secondary(rechargeable)batteries)

  化学反应可逆
  反复使用

  类型：NiCd Batteries, Ni-metal hybride (NiMH) batteries, Li-ion-batteries, Lead-acid
  batteries

#### Generators 发电机

电磁铁生成静电场

通过电磁感应在磁场中旋转产生电压

#### Power Plant 动力设备

初级能源 $\rightarrow$ 创造热或者辐射衰弱
风能、水能$\rightarrow$通过涡轮机

<img src="image-20210103193624832.png" alt="image-20210103193624832" style="zoom:67%;" />

### Real Current Sources 真实电流源

电流源通常由半导体设备实现，并且被特殊电源设计。每一个真实电流源或多或少的显示出强烈的电流对施加电压的依赖

### Ideal Resistors (The Element Resistance) 理想电阻（电阻元件）

<img src="image-20210103194042353.png" alt="image-20210103194042353" style="zoom:67%;" />

规定电阻的倒数叫做**电导**(Electric Conductance)，单位是**西蒙(Siemens)**~~西门子~~

### Current-Voltage-Characteristics 电流电压特征

电阻和电导分别是**特性(slope)**的斜率