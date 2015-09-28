# 对偶

标准的优化问题定义为
$$ minimize\ \ f_0(x) $$
$$ subject\ to\ \ f_i(x) \le 0, i=1, ... ,m,$$
$$\ \ \ \ \ \ \ \ \ h_i(x) = 0, i=1, ..., p,$$

#### Lagrange函数
定义 $L: R^n \times R^n \times R^p \rightarrow R$
$$ L(x, \lambda,\nu ) = f_0(x) + \sum \limits_{i=1}^{m}\lambda_if_i(x) + \sum \limits_{i=1}^{p}\nu_ih_i(x) $$

#### Lagrange乘子
$ \lambda_i和\nu_i$称为对应约束的Lagrange乘子 

#### Lagrange对偶函数
定义 $\lambda \in R^m, \nu \in R^p$，有
$$ g(\lambda, \nu )= \inf \limits_{x \in D} L(x, \lambda, \nu)= \inf \limits_{x \in D}f_0(x) + \sum \limits_{i=1}^{m}\lambda_if_i(x) + \sum \limits_{i=1}^{p}\nu_ih_i(x) $$

Lagrange对偶函数是Lagrange函数关于x取得的最小值。

> 注意：对偶函数是一族关于$(\lambda, \nu)$的仿射函数的逐点下阕街，所以即使原问题不是凸的，对偶函数也是***凹***函数。

## 最优值的下界
对偶函数构成了原问题的最优值$p^*$的下界。
