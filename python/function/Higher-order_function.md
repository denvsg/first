# python 高阶函数

1、一个函数的函数名作为参数传给另外一个函数  
2、一个函数返回值（return）为另外一个函数（返回为自己，则为递归）

## map 映射

map函数接收的是两个参数，一个是函数名，另外一个是序列。  
其功能是 将序列中的数值作为函数的参数依次传入到函数值中执行，然后再返回到列表中。  
返回值是一个迭代器对象

```python
a = [1, 2, 3, 4, 5]
b = list(map(str, a))  # 将数字转换成字符串
```

> 可以看出，只要用map函数，就可以让列表中的每一个数都完成一次对函数参数的调用，并将结果返回到一个可迭代对象中
> 可以通过 list(map()) 将map函数返回的迭代对象转化为列表

#### 高阶函数map一般 和 匿名函数 lambda联合使用

> map 现在可使用推导式替换

## filter 过滤

filter函数也是接收一个函数和一个序列的高阶函数，其主要功能是过滤。  
其返回值也是迭代器对象，

```python
a = [1, 2, 3, 4, 5]
b = list(filter(lambda x: x % 2 == 0, a))  # 过滤偶数
```

> 传入的参数返回的是布尔值， 例如： "Tom".islower()，返回的是一个布尔值False，只有所有的字母小写返回True

## reduce 合并

reduce函数也是一个参数为函数，另一个参数为可迭代对象 Iterable Object。  
其返回值为一个值而不是迭代器对象，故其常用与叠加、叠乘等

```python
from functools import reduce

a = [1, 2, 3, 4, 5]
d = reduce(lambda x, y: x * y, a)  # 连乘
```

> reduce中的函数必须也要接收2个参数，执行时把前一个结果继续和序列的下一个元素做累积计算，其效果就是：
> reduce(f, [x1, x2, x3, x4]) = f(f(f(x1, x2), x3), x4)

## sorted 排序

Python内置的sorted()函数就可以对list进行排序： key指定的函数将作用于list的每一个元素上，并根据key函数返回的结果进行排序。

要进行反向排序，不必改动key函数，可以传入第三个参数reverse=True：

```python
a = [14, 25, 73, 42, 51]

b = sorted(a)
c = sorted(a, reverse=True)
```

<br />
<br />
<br />
<br />
<br />

......     
[回到目录](../contents_page.md)   
......
