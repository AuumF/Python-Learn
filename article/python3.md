## 第三天的学习
第二天，我们学习了python中的字典(dict)和元组(tuple)，知道了其基本的语法和内置函数，最好能多做几道题目，熟练掌握这两个内容。
****
### 一.set
python 的 set 和其他语言类似, 是一个无序不重复元素集, 基本功能包括关系测试和消除重复元素。   
set和dict相似，set相当于dict只有键(key)而没有值(value)。   
#### 1.set的创建
创建一个set，需要提供一个list作为输入集合
```python
set1 = set([123,456,789])
print(set1)
```
输出结果如下   

![](/picture/屏幕截图%202024-05-05%20233113.png)   

传入的参数 [123,456,789] 是一个 list，而显示的 {456, 123, 789} 只是告诉你这个 set 内部有 456, 123, 789 这 3 个元素，显示的顺序跟你参数中的 list 里的元素的顺序是不一致的，这也说明了 set 是无序的。   

还有一点，我们观察到输出的结果是在大括号中的，经过之前的学习，可以知道，tuple (元组) 使用小括号，list (列表) 使用方括号, dict (字典) 使用的是大括号，dict 也是无序的，只不过 dict 保存的是 key-value 键值对值，而 set 可以理解为只保存 key 值。   

回忆一下，在学习dict(字典)时，键(key)只能出现一次，如果后续出现相同的键(key)，以最后的键值对为准，而在set中将会直接被覆盖，代码如下:   
```python
set2 = set([123,456,789,123,123])
print(set2)
```
输出结果如下   
![](/picture/屏幕截图%202024-05-05%20233731.png)
后续重复的键(key)会被前面的所覆盖   
#### 2.set元素的增加
set中的元素可以通过内置函数add增加，并且可以重复增加，但是后续重复增加的元素会被忽略
```python
set3 = set([123,456,789])
print(set3)
set3.add(100)
print(set3)
set3.add(100)
print(set3)
```
输出结果如下   
![](/picture/屏幕截图%202024-05-05%20234137.png)   
#### 3.set元素的删除
可以使用内置函数remove来对set中的元素进行删除，代码如下:   
```python
set4 = set([123,456,789])
print(set4)
set4.remove(123)
print(set4)
```
输出结果如下   
![](/picture/屏幕截图%202024-05-05%20234431.png)   
#### 4.set的应用
因为 set 是一个无序不重复元素集，因此，两个 set 可以做数学意义上的 union(并集), intersection(交集), difference(差集) 等操作。   

![](/picture/屏幕截图%202024-05-05%20234645.png)
例子:   
```python
set1 = set(['p','y','t','h','o','n','l','d'])
set2 = set('helloWorld')
print(set1)
print(set2)

# 交集(求两个set中相同的元素)
set3 = set1 & set2
print('\n交集 set3:')
print(set3)

# 并集(合并两个set并去除其中的相同元素)
set4 = set1 | set2
print("\n并集 set4:")
print(set4)

# 差集
set5 = set1 - set2
set6 = set2 - set1
print("\n差集 set5:")
print(set5)
print("\n差集 set6:")
print(set6)

# 去除list中的相同的相同元素
list1 = [111,222,333,444,555,111,333,555]
set7 = set(list1)
print("\n去除列表中的重复元素 set7:")
print(set7)
```
结果如下   

![](/picture/屏幕截图%202024-05-06%20000011.png)   
#### 5.set的相关题目(后续补充)
****