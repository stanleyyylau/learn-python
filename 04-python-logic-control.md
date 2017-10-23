## Python的缩进

Python 解析器利用缩进来判断语法执行到哪里和ruby一样

```
a = 1
if a > 10:
    print('aaa')
print('bbb')
```

## if, while 语句

```
a = 0
if a <= -1:
    print('a is nagative')
elif a == 0:
    print('a is 0')
else:
    print('a is positive')
```

while制作死循环

```
while 1:
    print('##'*10)
```


## for 语句

[enumerate() 函数](http://www.runoob.com/python/python-func-enumerate.html)

```
test = dict(a=1, b=2, c=3)
for key, value in enumerate(test):
    print(key)
    print(test[value])
```

range和xrange的区别
range会一次在内存中生成所有的数据
xrange就是当你用的时候再生成，性能更好

```
for i in xrange(1, 101):
    print(i,)
```



## continue, break

continue是退出当前Iteration

```
for i in xrange(1, 11):
    if(i == 3):
        print('i will not output...')
        continue
    print('i = %d' % i)
```

break是退出整个loop循环

```
for i in xrange(1, 11):
    if(i == 3):
        print('i will not output...')
        break     //3后面不用有任何东西输出
    print('i = %d' % i)
```