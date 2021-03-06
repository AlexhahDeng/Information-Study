### 目标

一定范围内用最小数量的中继器满足用户通讯需 求

### 未知量

用户位置、中继器位置和数量

### 约束条件

1.假设用户均匀分布，在区域内用户数量不超过C

2.两个中继器间距离小于2R，则发射机频率必须不低于阈值f=0.6MHz

3.每个用户至少被一个中继器覆盖

### 解决方案

*蜂窝网络*

确定最大的圆可以覆盖多少边长为1的六边形，进而确定中继器的最小数量

*Voronoi算法*

确定中继器的位置，每个中继器代表一个泰森多边形区域，要满足泰森多边形外接圆半径小于用户通信半径

*连续逼近*

考虑用户是移动的，将离散问题转化为连续问题，使用连续均匀分布方法

*极值优化*

通过单独改变最小的适应度来避免局部达到最优，由此剔除符合度最小的种类

*最大生成树和最小生成树*

不改变中继器位置和数量，重新排列中继器的频率和PL数来最大化用户数目

*用户密度波动之伯努利分布*

之前的模型假定用户密度为常数，现实中用户数量在这一领域服从伯努利分布



### 通信领域的理论

*Shannon信息理论*

计算中继器和用户的通信范围以及中继器的容量，估计、一个中继信号在噪声信道信息的能力

*天线理论*

计算信号的接收功率

### 算法

1. 整体设计思路：迭代
2. 知识点：
   - 集合，图论 as 基本模型数学描述
   - 蜂窝网络
   - 泰森多边形
   - 树的搜索算法

​     