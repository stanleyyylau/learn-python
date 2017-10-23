# Python数据类型

## 整型

```
age = input("Please input your age")
name = raw_input("Please input your name")
print(type(age))
print(type(name))

input只能接收整型
raw_input是接收任何类型然后转换成字符串类型
```

```
a = 100

print(a.__abs__())

print(dir(a))

print(abs(a))
```


## 浮点型

```
print('##' * 20)
c = 2.556
print(round(c,2))
```

### round函数的两种用法情况

**round()**

1. 默认保留一位小数
2. 采用四舍五入的方法进行计算

**round(floor, 精确)**

先进行四舍五入的运算，如果小数点精度的最后一位是偶数，符合条件，如果小数点精度的最后一位四舍五入之后为奇数，则舍弃原小数点精度以后的所有数字，小数点精度的最后一位必须为偶数。


## 布尔类型

不单独出现，一般和逻辑运算符一起出现

```
a = 10
b = 20
c = 100
print(not True)
print(not(a>b and c>a))
```


## 字符串

这个类型要重点掌握

### 常用的方法

str1 = "stirwejfi"
用``print(dir(str1))`` 来查看字符串的方法

```
find 
replace 
split 
join 
strip 
format
```

format字符串的几种方法

* print("hello %s) % name          --- %s 字符串  %d 整型  %f 浮点型
* print("hello {0}, my age is {1}".format(name, age))
* print('{name}:{age}'.format(name="ajing", age=20))

在python文件开头用```this is comment```可以作为解释

## 列表

常用方法
append
index
insert
pop
remove
reverse


## 元组

其实就是list，但是是不重复的list，这个东西叫做tuple，也是很重要的数据类型

列表是 list = {'q23', 'fwef'}
Tuple 是 tuple1 = ('1', '2')
tuple 只要一个的时候要 tuple2 = ('1':)


## 字典

这部分也是重点内容，很多key-value的数据库，包括redis都是用这种数据结构，另外这种结构的另一个好处的读取速度快，类似数据库里面加了index，要掌握好。

定义字典类型变量
k1 = dict(a=1, b=2, c=3)

字典常用的方法

get
setdefault
keys
iteritems
pop
fromkeys 获得keys

对字典进行排序


## 帮助

dir()  打印属性
help()  
type()
str(INT) 强制类型转换