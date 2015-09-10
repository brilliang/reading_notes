# 凸集

本章介绍了在凸优化这个学科中，用来限定和描述这个数学世界的一些概念。我理解所谓仿射、凸、锥，就是对一些点，扩展成一个空间的方式。

## 点到线的扩展
最基本的从两个点扩展到直线和线段的方式：

$$ \theta x_1 + (1-\theta)x_2 $$

如果不限制 $ \theta $ 就是穿过 $ x_1 $  $ x_2 $ 的直线；如果限制 $ \theta \in  [0, 1] $, 就是从$ x_1 $ 到 $ x_2 $ 的线段

## 概念

介绍了放射、凸、锥这三个概念
<table>
<thead>
    <tr>
        <td>
        </td>
        <td>
            定义
        </td>
        <td>
            组合
        </td>
        <td>
            包
        </td>
    </tr>
</thead>
    
<tbody>
    <tr>
        <td>仿射
        </td>
        <td>
            $ \forall x_1, x_2 \in C, \forall \theta \in R, 都有 \theta x_1 + (1-\theta)x_2 \in C， 则称集合C是仿射的 $
        </td>
        <td>
            $ 如果 \sum\limits_{i=0}^n \theta_i =1, 称 \sum\limits_{i=0}^n \theta_i x_i为x_1, x_2，\cdots， x_n的仿射组合  $
        </td>
        <td>
            $ C中所有点的仿射组合的集合称为C的仿射包 $
        </td>
    </tr>
    
   <tr>
   <td>凸集
   </td>
   <td>
            $ \forall x_1, x_2 \in C, 0 \leq \theta \leq 1, 都有 \theta x_1 + (1-\theta)x_2 \in C， 则称集合C是凸的 $
        </td>
        <td>
            $ 如果 \sum\limits_{i=0}^n \theta_i =1， 且\forall \theta_i > 0, 称 \sum\limits_{i=0}^n \theta_i x_i为x_1, x_2，\cdots， x_n的凸组合  $
        </td>
        <td>
            $ C中所有点的凸组合的集合称为C的凸包 $
        </td>
   </tr>
   
   <tr>
        <td>锥
        </td>
        <td>
            $ \forall x \in C, \theta \geq 0, 都有 \theta x \in C， 则称集合C是锥 $
        </td>
        <td>
            $ 如果 \forall \theta_i \geq 0, 称 \sum\limits_{i=0}^n \theta_i x_i为x_1, x_2，\cdots， x_n的锥组合  $
        </td>
        <td>
            $ C中所有点的锥组合的集合称为C的锥包 $
        </td>
   </tr>
</tbody>    
</table>

锥： 在二维几何上，锥是一个以0为顶点的扇形。


## 一些重要的凸集

## 保凸运算
1. 凸集的交集还是凸集
2. 仿射函数（形如 f(x)=Ax+b，其中$ A \in R^{m \times n}，b \in R^m $）的定义域是凸的，那么值域也是凸的；反之亦然。
3. 透视函数（对向量进行伸缩，时的最后一维分量为1并舍弃之），定义域是凸的，值域也是凸的；反之亦然。
4. 线性分式函数（
$ g(x)=\begin{pmatrix} A \\ C^T \end{pmatrix}  x + \begin{pmatrix} b \\ d \end{pmatrix}$
）

## 广义不等式
根据锥的定义中， $ \theta \ge 0 $，推广出的一个偏序关系。

对一个正常锥K（凸的，闭的，实的，尖的），定义偏序关系如下： $$ x \preceq y \iff y - x \in K $$

#### 最小 & 极小
集合$ S $的最小元x： $ S \in x+K $，其中$ x+K $表示全集中，大于等于x的所有元素

集合$ S $的最小元x： $ S \cap (x-K) =\{x\} $，其中$ x-K $表示全集中，小于等于x的所有元素

## 分离与支撑超平面
用**超平面**或者**仿射函数**将两个凸集划分开。

###超平面分离定理
> 
> 两个不相交的凸集 $ C和D， C \cap D =\emptyset$
> 
> $\exists a \neq 0和b$
> 
> $s.t. \forall x \in C， a^Tx \le b; \forall x \in D, a^Tx \ge b  $

### 严格分离
如果分离平面满足$ \forall x \in C， a^Tx < b; \forall x \in D, a^Tx > b  $，那么称集合$C和D$严格分离。

注意： 不相交的凸集并不一定能被严格分离
### 支撑超平面
> $ x_0 是集合C \subseteq R^n $ 边界**bd** $ C $上的一点。如果 $ a \neq 0，并且\forall x \in C，都满足 a^Tx \le a^Tx_0, 那么称超平面\{x|a^Tx=a^Tx_0\}，为集合C在点x_0处的超平面$

### 支撑超平面定理
> 对于任意非空凸集$ C $ 和任意$ x_0 \in $  **bd** $ C $，在$ x_0 $处都存在$ C $的支撑超平面

### 支撑超平面定理的逆
> 如果一个集合是闭的，有分控内部，并且边界上的每个点都存在支撑超平面，那么它是凸的


## 对偶锥与广义不等式
> 令$ K $为一个锥。集合
> $$ K^* = \{ y| x^Ty \ge 0, \forall x \in K\} $$
> 称为$ K $的对偶锥

对偶锥的性质：

1. $ K^* 是闭凸的 $
2. $ K_1 \subseteq K_2 \Rightarrow K_2^* \subseteq K_1^* $ 
3. 如果K有非空内部，那么$ K^* $是尖的
4. 如果K的闭包是尖的，那么$ K^* $有非空内部
5. $ {K^*}^* $是$ K $的凸包的闭包

由上可知： 如果$ K $是一个正常锥，那么$ {K^*}^* $也是一个正常锥，且$ {K^*}^*  = K$

### 广义不等式的对偶
正常锥$ K $的对偶锥$ K^* $也是正常的，也能导出广义不等式 $ \preceq _{K^*} $。

称$ \preceq _{K^*} $和$ \preceq _{K} $对偶。

1. $ x \preceq _{K} y $  当且仅当  $ \forall \lambda \succeq _{K^*} 0, 都有\lambda ^Tx \le \lambda^Ty$。 
2. $ x \prec _{K} y $  当且仅当  $ \forall \lambda \succeq _{K^*} 0，且\lambda \neq 0, 都有\lambda ^Tx < \lambda^Ty$。 

> 注意：可以将向量内积在几何上等效理解成向量在对方方向上投影的长度（refer：http://www.purplemath.com/modules/mtrxmult.htm）  by zhul

### 利用对偶不等式理解最小元和极小元
最小元
> x是$S$上关于广义不等式 $ \preceq _{K} $ 的最小元（所以S是个正常锥），当且仅当
> $$ \forall \lambda \succ _{k^*} 0, x是z \in S上极小化\lambda ^Tz的唯一最优解$$

> 几何上看，这意味着任意 $ \lambda \succ _{K^*} 0, 超平面 \{ z  |  \lambda ^T(z-x_0)=0 \} 是x_0处对S的一个严格支撑超平面$

极小元
> 如果$\lambda \succ _{K^*} 0，并且z_0是z\in S上极小化\lambda ^Tz的解， 那么z_0是极小的$ 
> 
> 但是其逆并不成立，即$ z_0是极小的，却可能对于任何\lambda \succ _{K^*} 0，z_0都不是z\in S上极小化\lambda ^Tz的解 $
> 
> 但但是，如果S是凸的，那么这个逆命题成立。






