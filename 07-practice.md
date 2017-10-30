
## 把一个数字的list从小到大排序，然后写入文件，然后从文件中读取出来文件内容，然后反序，在追加到文件的下一行中

```
import codecs
import linecache
import ast


list1 = [234, 4234, 53, 4234, 324, 423, 12, 5, 5]
lst = []

with codecs.open('1.txt', 'w') as ff:
    ff.write(str(sorted(list1)))

print('Finishing writing sorted array to file')

print('About to read array from file')


with codecs.open('1.txt', 'r') as ff:
    lst = ast.literal_eval(ff.read())
    lst.reverse()
    print(lst)

with codecs.open('1.txt', 'a') as ff:
    ff.write('\n')
    ff.write(str(lst))
```



## 分别把 string， list， tuple， dict写入到文件中


```
import codecs

tup1 = ('physics', 'chemistry', 1997, 2000)

with codecs.open('1.txt', 'w') as ff:
    for t in tup1:
        ff.write(str(t) + '\n')
```


```
import codecs
import json

dict = {'Alice': '2341', 'Beth': '9102', 'Cecil': '3258'}

with codecs.open('1.txt', 'w') as ff:
    ff.write(json.dumps(dict))
```