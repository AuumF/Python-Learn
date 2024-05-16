## 第四天的学习
第三天，我们学习了set的相关内容，知道了set相当于一个只有键(key)的dict(字典),今天将学习有关条件和循环的内容   
****

### 一.条件语句
#### 1.条件语句的定义
Python 条件语句跟其他语言基本一致的，都是通过一条或多条语句的执行结果（ True 或者 False ）来决定执行的代码块。
#### 2.条件语句的基本形式
```python
if 判断条件
    执行语句
else:
    执行语句
```
#### 3.if语句多个判断条件的形式
```python
if 判断语句1:
    执行语句
elif 判断条件2:
    执行语句2
elif 判断条件3:
    执行语句3
else:
    执行语句4
```
实例:
```python
result = 81

if result > 90:
    print("优秀")
elif result > 80:
    print("良好")
elif result > 60:
    print("及格")
else:
    print("不及格")
```
输出结果如下   

![](/picture/屏幕截图%202024-05-16%20150849.png)
#### 4.if语句多个条件同时判断
在实现if语句多个条件同时判断时，需要运用 **and** 和 **or** 字符来实现。and(与)相当于c++中的&&相似，or(或)相当于c++中的||。可以类比使用。
示例代码如下:
```python
a = 90
b = 75

if a > 60 and b > 60:
    print("及格")
else:
    print("不及格")
```
如果在条件的判断过程中需要分优先级，需要用括号来分辨，如下所示:
```python
a = 86
b = 96

if (a > 80 and b < 100) or (b > 80 and a <100):
    print("及格")
```
#### 5.if嵌套
if嵌套即在if语句的执行语句中又出现if语句
```python
a = 95
b = 85

if a > 90:
    if b > 80:
        print("及格")
else:
    print("不及格")
```