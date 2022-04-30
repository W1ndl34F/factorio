#### Nullius

##### plan
> 现在的目标不是精准完美的计算，而是protype。细节考虑点到为止。分几个方面：1. 基建 2. workflow的正常运行 

###### 基建
1. 气体类的主要工具是化工厂，固体(铁相关)主要是熔炉/铸造厂。red之后的组装机。破碎机(可手搓，搞沙子用，估计需求不大)
2. 气体回收和废水回收(得搜一下)
3. 管道，需要大量。

###### wf

1. 先到red再看以后的科技树


```mermaid
graph TD;
A[发动机] --> B[red];
C[铁齿轮] --> B;
D[塑料] --> A;
E[铁板] --> A;
E --> AK[铁片];
F[铁丝] --> A;
G[铁棒] --> A;
H[乙烯C2H4] --> D;
I[Cl2] --> D;
H --> J[HCL];
I --> J;
K[甲烷CH4] --> H;
I --> H;
K --> L[水];
I --> L;
M[CO2] --> K;
N[H2] --> K;
M --> L;
N --> L;
O[CO] --> M;
L --> M;
O --> N;
L --> N;
O --> P;
N --> P;
P[石墨] --> O;
L --> O;
P --> N;
L --> N;
Q[空气] --> M[CO2];
Q --> AAJ[N2];
R[海水] --> S[盐水];
R --> T[废水DROP];
S --> I[Cl2];
S --> N[H2];
S --> U[O2];
S --> AAG[氢氧化钠];
AD[铁矿] --> V;
AD --> AE[碎石DROP];
V[铁锭] --> E;
V --> G;
G --> F;
E --> C;
G --> C;
G --> Y[管道];
Y --> Z[地下管道];
AA[沙子] --> Z;
AB[砂岩] --> AA;
AB --> AC[石矿];
AI[绝缘电线] --> AJ[purple];
AF[逻辑电路] --> AJ;
AG[灯] --> AJ;
AH[电容器] --> AJ;
P --> AG;
AK --> AG;
AL[玻璃] --> AG;
AM[SIO2] --> AL;
AN[沙子] --> AM;
S --> AM;
AN --> T;
S --> T;
AO[橡胶] --> AI;
AP[铝线] --> AI;
AQ[铝棒] --> AP;
AR[铝锭] --> AQ;
P --> AR;
AS[AL2O3] --> AR;
AT[氢氧化铝] --> AS;
AU[碎铝土矿] --> AT;
AV[氢氧化钠溶液]  --> AT;
AU --> AW[DROP污泥];
AV --> AW;
AX[铝土矿] --> AU;
AX --> AZ[碎铁矿石];
AX --> AA[沙子];
AAB[丁二烯] --> AO;
AAC[苯乙烯] --> AO;
H --> AAB;
AAD[蒸汽] --> AAB;
N --> AAD;
U --> AAD;
H --> N;
AAD --> N;
H --> AAC;
AAE[苯] --> AAC;
H --> N;
AAE --> N;
O --> AAE;
N --> AAE;
O --> H;
N --> H;
O --> AAF[丙烯];
N --> AAF;
AAG --> AV;
L --> AV;
P --> AF;
D --> AF;
AP --> AF;
AAH[多晶硅] --> AF;
AAI[硅锭] --> AAH;
J --> AAH;
AAJ --> AAH;
AAI --> N;
J --> N;
AAJ --> N;
AAI --> I;
J --> I;
AAJ --> I;
P --> AAH;
AM --> AAH;
P --> AH;
D --> AH;
AS --> AH;
AAK[铝片] --> AH;
AAL[铝板] --> AAK;
AR --> AAL;
```

## 计算和目标

### 目标

1. 现在的目标有3个 --> 
   1. 计算。计算到purple为止需要的red yellow blue，进而从结构上module化remake
   2. red有很多新的产品，产品使用需要熟悉。
   3. 基础建设的增加。
      1. 矿需要很多采矿机(根据planner来计算)
      2. 需要组装机/机械臂/传送带/铁齿轮/铁板/铁棒/管道 --> 估计算是结构上的第二层，设计时，留“自己都无法想象的空隙”
      3. 开地图？

### 计算

- red 317
  - ![hI3skF_w2RMIY](https://cdn.jsdelivr.net/gh/h3x311/upic@main/uPic/2022/hI3skF_w2RMIY.png)
- yellow 265
- blue 247


### TODO
- [ ] 更新mermaid 图，加到purple done
- [ ] planner mod加上，并且计算到purple done

---

purple这步的流体和固体混合自动化很难。为了形成集中的流水线，估计后期得用铁路运矿。
基础建设随着层数的提高变得需要升级基建设备，进而提高效率。

---

目前在开发purple上达到了bottleneck。

比如塑料作为上层产物达到了* 5倍的需求倍增。随着新设备的增加，合成气体(比如乙烯,它在purple主要是橡胶的底层产物，量必然无法通过塑料来分。同样，塑料的wf也需要module化，使得无bottleneck)的方式变得多元。不必在old pattern下remake。

找新的空间按照向外扩展的方向继续设计。

### TODO

1. 铝土矿/塑料生产线扩张。
2. **purple自动化**
   1. 石墨的补给
   2. 四个产物的连接
   3. 计算需要多少purple

---

## TODO
1. 开一条铁片的自动化 --> 灯
2. 石墨自动化
3. 塑料扩展
4. 铝的扩展
5. 红瓶的塑料补给
6. 开地图（有车了！！