# 凸函数
> 1. $dom$ $f$是凸的
> 
> 2. $\forall x, y \in dom$  $f$， $\forall 0 \le  \theta \le 1$，有 
> $$ f(\theta x + (1-\theta)y) \le  \theta f(x) + (1-\theta)f(y) $$
> 则称 $f: R^n \rightarrow R$是凸函数

如果$-f$是凸的，那么$f$是凹的。

定义凸函数在定义域外的值为 $ \infty $，从而可以将凸函数的定义域扩展到全空间。这样就不需要增加定义域的描述了——反正这样也不影响最优化的效果。

## 一阶条件
函数$ f $是凸函数的充要条件是：
> $dom$ $f$是凸的，$\forall x, y \in dom f$，下式成立
> $$ f(y) \ge f(x) + \nabla f(x)^T(y-x) $$

证明：

1. 先证明$f: R \rightarrow R$
2. 再将$f: R^n \rightarrow R$ 映射到一维情况

## 二阶条件

函数$ f $是凸函数的充要条件是：
> 其Hessian举证是半正定的，即 $$ \forall x \in dom f, 有 \nabla ^ 2 f(x) \succeq 0 $$

## 常见凸函数
仿射函数的一般形式为 $f(x)=Ax+b$，其中$A \subseteq R^{m*n}, x \subseteq R^n, b \subseteq R^m $。一个函数是仿射函数，当且仅当它是即凸又凹。

$R$上的一些函数
> $e^{ax}$
> 
> $x^a, a \ge 0或者a \le 1$
> 
> $ |x|^a , a\ge 1$
> 
> $logx$
> 
> 负熵： $xlogx$

$R^n$上的一些函数
> $R^n$上任意的范数
> 
> $f(x)=max\{x_1,..., x_n\}$
> 
> $ dom f =R \times R_{++}, f(x_1, x_2) = x_1^2 / x_2$
> 
> 指数和的对数: $f(x) = log(e^{x_1} + ... + e^{x_n})$
> 
> 几何平均： $f(x) = (\prod_{i=1}^{n}x_i)^{1/n}$
> 
> 对数-行列式
> 

#上境图
函数$f：R^n \rightarrow R$的图像定义为 $\{(x, f(x)) | x \in dom f\}$，它是$R^{n+1}$的一个子集。

将这个函数的上境图定义为 $epi f=\{ (x, t) | x \in dom f, t \ge f(x)   \}$。几何上理解，就是所有函数图像上方的空间。
> 函数是凸函数，当且仅当其上境图是凸集

## Jensen不等式
最初有Jensen提出的不等式 $$ f\left( \frac{x+y}{2} \right) \le \frac{f(x) + f(y)}{2} $$

$f$是凸函数，$ \theta _1, ... , \theta _k \ge 0， 且 \theta_1+...+\theta_k=1$ ，上式可扩展为 
$$f(\theta_1 x_1+... + \theta_k x_k) \le \theta_1 f(x_1) + ... + \theta_k f(x_k)$$

如果相应的积分存在，那么下式成立：
$$ f\left( \int_s p(x)x dx \right) \le \int_sf(x)p(x)dx $$

如果$x$是随机变量，且事件$x \in dom f$发生的概率为1，$f$是凸函数，相应的期望存在时，有 
$$ f(Ex) \le Ef(x) $$

### 不等式
> 凸性和Jesen不等式可以作为不等式理论的基础
例如 $-logx$是凸的， 所以 $ -log \left( \frac{a+b}{2}  \right) \le \frac{-loga-logb}{2}$，从而得到 $ \frac{a+b}{2} \ge \sqrt{ab}$

# 保凸运算
保持函数凸性的运算，可以用来构造新的凸函数。

- 非负加权求和
 
> $f_i是凸函数，w_i \ge 0，那么f=w_if_i + ... w_mf_m是凸函数$

- 复合仿射映射

> $ g(x) = f(Ax+b)$，如果f是凸函数，那么g也是凸函数

- 逐点最大

> $ f(x) = max\{  f_1(x), f_2(x)\}$ 如果 $f_1，f_2  $是凸函数，那么f是凸函数

- 几乎所有的凸函数都可以表示成一簇仿射函数的逐点上确界。

### 复合函数
考虑函数 $f(x) = h(g(x))$的保凸条件。
