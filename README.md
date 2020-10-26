# program-in-GeoGebra
一行流

## 前言

突然想通了一些事，切换工具了。

GGB 的函数名称有中英文双版本

### 求数列的 Sn

```
f(x)=2*x+1
```

这步定义函数

```
sum(f(t),t,0,n) 
```

这步计算累和，ggb 会自动识别 n，并询问是否新建变量。

### 拓展：求解黎曼和

```
f(x)=2*x+1
```

定义函数

```
RectangleSum(f, 0, 5, 10, 0)
```

### 求解 fib 的第 n 项

```
迭代(a1 + b1, a1, b1, {1, 1}, n)
```

这里解释一下

在 Python 里，fib 数列是这么写的

```py
def fib():
    a, b = 1, 1
    for _ in range(5):
        a, b = b, a + b
    return a


print(fib())
```

注意对应关系即可

### 求任意带系数的线性递推的 n

以 a<sub>n+2</sub> = 2 a<sub>n+1</sub> + a<sub>n</sub>, a<sub>1</sub> = a<sub>2</sub> =1 为例

结合 fib 数列的思路，容易写出

```
迭代(2*b1 + a1, a1, b1, {1, 1}, n)
```

注意变量顺序

### 求解 taylor 展开

```
TaylorSeries(sin(x), 0, 5)
```

### 表示 n 进制

```
ToBase(99,2)
```

返回值是 Text

### 绘制累和函数

```
sum(abs(x - t), t, 0, 5)
```

### 绘制撞球摆

To Be Continued...

### 只用分支的方阵画法

To Be Continued...
