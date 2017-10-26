## file读文件

```
import codecs

f = codecs.open('1.txt')
print(f.read())
f.close()
```

* `f.read()` 还可以加正则，这个超级好用！！！要记着


## file写文件

```
# codecs solve file encoding issue
# open(filename, mode)
# mode -- arguments you need to know

# r read
# w write
# b binary
# a append

import codecs

f = codecs.open('2.txt', 'ab')

f.write('hello world\n')

f.write('hello stanley\n')

f.write('you are very cool\n')

f.close()
```


## file常用方法

```
readlines()
readline()  # To read line by line
next()
writelines()
write()
```

这部分内容用的比较少，可以用的时候再查

```
tell()
seek()
flush()
name
enclosed
mode
```

## 