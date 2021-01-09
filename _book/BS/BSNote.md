# 2 Processes and Threads

## 2.1 Processes

CPU switches from process to process quickly, running each tens or hundreds milliseconds.

at any one instant the CPU is running only one process.

This is **pseudoparallelism**(伪并行)

to the contrast, true hardware parallelism of multiprocessor systems.

### 2.1.1 The Process Model

![image-20201202101120093](image-20201202101120093.png)

only one process will be executed at one time

### 2.1.2 Process Creation

Four principal events cause processes to be created:
1. System initialization.
2. Execution of a process-creation system call by a running process.
3. A user request to create a new process.
4. Initiation of a batch job.

#### UNIX

**fork:**

create a copy of father process
two process have the same state
child process may use **execve()** to change memory image and run another program.

#### Windows

**CreateProcess**

Process creation and loading the correct program into the new process.

***

unix has **copy-on-write** means child or parent wants to modify the memory, the chunk of memory will be copied to prevent

### 2.1.3 Process Termination

Sooner or later the new process will terminate, usually due to one of the following conditions:

1. Normal exit (voluntary).
2. Error exit (voluntary).
3. Fatal error (involuntary).
4. Killed by another process (involuntary).

exit in UNIX

ExitProcess in Windows

### 2.1.4 Process Hierarchies

Unix can





# 3 内存管理

## 3.4 页面置换算法

### 3.4.1 最优页面置换算法

预知后方会有哪些内存支配哪些页面，把当前内存里最后调用的置换出来
算法是最优的但是无法实现

### 3.4.2 最近未使用页面置换算法(Not Recently Used, 最近未使用)

将每个页面标记R/M位，这两位都可以由操作系统设置为0

页面进入时将标记R位，如果要修改则再标记M位。

则会产生如下四种情况

|      | R    | M    |
| ---- | ---- | ---- |
| 0    | 0    | 0    |
| 1    | 0    | 1    |
| 2    | 1    | 0    |
| 3    | 1    | 1    |

操作系统可能会清除R位造成序号为1的情况

在置换页面时置换序号最小的

### 3.4.3 先进先出页面置换算法(FIFO,First-In First-Out Algorithm)

类似队列，先进入的页面最先被置换

易于实现

### 3.4.4 第二次机会置换算法(Second chance Algorithm)

检查最老的页面，如果R位是1则清零并放到队列尾端，否则置换

### 3.4.5 时钟页面置换算法(CLOCK)

防止移动指针消耗时间，在逻辑上使用环形

指针始终指向最老的页面，发生缺页中断则检查当前R位，若为1将R置为0并前移检查次老的页面，否则置换当前页面并前移指针

### 3.4.6 最近最少使用页面置换算法(Least Recently Used, LRU)

置换未使用时间最长的页面。时间复杂度比较高。

或者在每个页后设置计数位，每次执行页面计数器加一，最后检查最小的

### 3.4.7 用软件模拟LRU

#### NFU(Not Frequently Used, 最不常用)

发生时钟中断，就把所有页面的R位加入到页面的计数器中，发生缺页终端则置换计数器值最小的部分

#### 老化

只储存最近x次，最后置换数字最小的





























