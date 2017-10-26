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

## file的with用法

好处就是更轻便，有节操的程序员就用这个

```
import codecs
import linecache

with codecs.open('1.txt', 'rb') as f:
    print(f.read())
    print(f.closed)
print(f.closed)

# When you quit the look, file object will be closed automatically

with codecs.open('1.txt', 'rb') as ff:
    for line, value in enumerate(ff):
        #print(line, value)
        # if you want to print a specific line (line3)
        if line == 3 - 1:
            print(value)

count = linecache.getline('1.txt', 2)
print(count)
```