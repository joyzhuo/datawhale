# 1. Dict字典

## 1） 定义

Python内置了字典：dict的支持，dict全称dictionary，在其他语言中也称为map，使用键-值（key-value）存储，具有极快的查找速度。

一个key只能对应一个value，所以，多次对一个key放入value，后面的值会把前面的值冲掉

## 2） 创建

```
>>> d = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
>>> d['Michael']
95
```
```
>>> d['Adam'] = 67
>>> d['Adam']
67
```

## 3） 字典的方法

dict提供的get()方法，如果key不存在，可以返回None，或者自己指定的value：

```
>>> d.get('Thomas')
>>> d.get('Thomas', -1)
-1
```

要删除一个key，用pop(key)方法，对应的value也会从dict中删除：

```
>>> d.pop('Bob')
75
>>> d
{'Michael': 95, 'Tracy': 85}
```

# 2. 集合

## 1） 特性

set和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key。

## 2） 创建

要创建一个set，需要提供一个list作为输入集合：

```
>>> s = set([1, 2, 3])
>>> s
{1, 2, 3}
```

## 3） 方法

通过add(key)方法可以添加元素到set中，可以重复添加，但不会有效果：

```
>>> s.add(4)
>>> s
{1, 2, 3, 4}
>>> s.add(4)
>>> s
{1, 2, 3, 4}
```

通过remove(key)方法可以删除元素：

```
>>> s.remove(4)
>>> s
{1, 2, 3}
```

# 3. 判断语句（要求掌握多条件判断）

计算机之所以能做很多自动化的任务，因为它可以自己做条件判断。

```
age = 20
if age >= 18:
    print('your age is', age)
    print('adult')
    
    age = 3
if age >= 18:
    print('your age is', age)
    print('adult')
else:
    print('your age is', age)
    print('teenager')
    
    age = 3
if age >= 18:
    print('adult')
elif age >= 6:
    print('teenager')
else:
    print('kid')
    
    if <条件判断1>:
    <执行1>
elif <条件判断2>:
    <执行2>
elif <条件判断3>:
    <执行3>
else:
    <执行4>
```

a. 判断条件、 else 、elif之后，需要添加 :

b. elif 为 else if 缩写

c. 整数之间比较，不同类型需要进行转换为相同类型
    
# 4. 三目表达式

为真时的结果 if 判定条件 else 为假时的结果

举例：

`100 if  77 > 66 else 99`

如果77大于66，输出100，否则输出99

# 5.循环语句

for..in..

```
for number in [1, 2, 3, 4]:
    print(number)
```

while

```
n = 50
while n>0:
    n = n -10
    print(n)
```

break & continue
与其他语言无异，break 为提前结束循环，continue 为跳过当前循环，开始下一次循环。

