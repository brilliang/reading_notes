# 凸集

本章介绍了在凸优化这个学科中，用来限定和描述这个数学世界的一些概念。我理解所谓仿射、凸、锥，就是对一些点，扩展成一个空间的方式。

### 点到线的扩展
最基本的从两个点扩展到直线和线段的方式：

$$ \theta x_1 + (1-\theta)x_2 $$

如果不限制 $ \theta $ 就是穿过 $ x_1 $  $ x_2 $ 的直线；如果限制 $ \theta \in  [0, 1] $, 就是从$ x_1 $ 到 $ x_2 $ 的线段

### 概念

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

