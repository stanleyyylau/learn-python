## 实现1-100的所有的和

```
sum = 0

for i in xrange(1, 101):
    sum += i
print(sum)
```


## 实现1-500所有奇数的和

```
sum = 0

for i in xrange(1, 501):
    if (i % 2) != 0:
        sum += i
print(sum)

```

## 求1+ 2! + 3! + 4! + ……20！的和

```
def getFactorial (num):
    total = 1
    for j in xrange(1, num + 1):
        total *= j
    return total

totalSum = 0
for i in xrange(1, 21):
    theFactorialOfCurrentNum = getFactorial(i)
    totalSum += theFactorialOfCurrentNum

print(totalSum)
```

## 对指定一个list进行排序[2,32,43,453,54,6,576,5,7,6,8,78,7,89]

```
list1 = [2,32,43,453,54,6,576,5,7,6,8,78,7,89]
list1.sort()
print(list1)
```

## 复习字典排序，字符串， list， tuple常用方法