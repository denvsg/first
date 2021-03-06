### 浮点型

浮点型，就是数字的小数形式 定义浮点型可直接 `i = 5.2`  
当然，也可以通过字符串强制转化为整型，如 `i = float("123.4")`

`float(x)` 将x转换到一个浮点数

浮点型数据也可直接进行数学运算：

##### 1. 加法

```python
a = 3.2
b = 5.5
print(a + b)
```

##### 2. 减法

```python
a = 13.7
b = 5.6
print(a + b)
```

##### 3. 乘法

```python
a = 3.3
b = 5.5
print(a * b)
```

##### 4. 除法

> 注意： python除法 `/` 默认是带有小数位的，如需整除，可使用 `//`

```python
a = 35.5
b = 5
print(a / b)  # 7.1
print(a // b)  # 7
```

##### 5. 乘方

> python 中，`**` 表示幂运算 `3**2` 便是3 的 平方

```python
a = 3.5
b = 5
print(a ** b)  # 525.21875
```

##### 6. 数值比较

数字还可以进行比较大小，一般用作条件判断

```python
a = 5.3
print(a > 5.5)  # False
```

[数字还可直接转换成 bool 类型](bool.md)

```python
a = 5
print(bool(a))
```



<br />
<br />
<br />
<br />
<br />

......     
[上一篇：整型](int.md)    
[回到目录](../contents_page.md)    
[下一篇：布尔型](bool.md)    
......    
