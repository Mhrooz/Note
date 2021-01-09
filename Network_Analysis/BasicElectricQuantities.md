 # Basic Electric Quantities

## Electric Potential / Voltage 电势 / 伏特

### The potential energy of separated charge

reference level 参照线

![image-20210102192127003](BasicElectricQuantities.assets/image-20210102192127003.png)

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