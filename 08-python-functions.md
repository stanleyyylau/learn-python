## 函数的一般形式

如何定义函数

`def` 是定义函数的关键词

```
def sum(x, y):
    return x+y

m = sum(3, 10)
mm = sum(x=4, y=8)
print(m)
print(mm)
```


## 函数的参数

**可以单独给b变量设定一个默认的值**

```
def funcA(a, b=0):
    print(a)
    print(b)

funcA(1)
funcA(10, 20)
```

**参数为tuple, 3后面全部变成tuple**

def funcD(a, b, *c):
    print(a)
    print(b)
    print(c)
    print(type(c))

funcD(1, 2, 3, 4, 5, 6)

**参数为dict, 要用两个星星号**

def funcF(a, **b):
    print(a)
    for x in b:
        print x + ": " + str(b[x])

funcF(100, x="hello", y="wolrd")


**还有一个传参数的方法，要用到解包**

dict = {'Alice': '2341', 'Beth': '9102', 'Cecil': '3258'}
funcF(100, **dict) 



## 高阶函数

所谓的高阶函数就是把函数当作参数传来传去，和JS传function没有区别

这些函数都是可以接收函数作为参数的

**map**

map的第二个参数为可迭代对象

```
lt = [1, 2, 3, 4, 5]
def f2(x):
    return x*x

ml = map(f2, lt)
print(lm)
```

**reduce**



## 匿名函数

没有名字的函数，快速定义的

m = lamdda x, y: x+y
print(m(4, 5))

sorted高阶函数
[对字典进行排序](https://stackoverflow.com/questions/613183/how-to-sort-a-dictionary-by-value)

```
mm = dict(a=1, c=3, b=10, d=9)
print(mm)
for i in mm:
    print i
for key, value in mm.iteritems():
    print(key, value)

test = sorted(mm)
print(test)

test = sorted(mm.iteritems(), key=lambda d: d[1])
```


## 列表生成式和生成器

**列表生成式子**

用来生成列表的

li = [x*x for x in xrange(1, 101) if x%2==0]



**生成器**

把[]改成()

```
li = (x*x for x in xrange(1, 101) if x%2==0)
```

函数中定义生成器

```
def fib(n):
    sum = 0
    i = 0
    while(i < n):
        sum = sum +i
        i +=    
        yield(sum)

```


## 生成器和迭代器的区别

生成式：
生成器：

可迭代对象：所有可以通过循环调用出来的，都是可迭代对象
迭代器：生成器，要通过next函数调用，迭代器


https://foofish.net/iterators-vs-generators.html
https://github.com/lzjun567/note/blob/master/note/python/iterator_generator.md
