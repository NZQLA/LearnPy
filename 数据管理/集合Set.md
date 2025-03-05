# 特性
- 元素是没有顺序的
- 不限制 元素类型
- 不允许 重复元素
- 不允许 修改元素的值，但是允许增删元素

# 创建集合 
## 创建一个空集合
```python
# 创建一个空集合
empty_set = set()
print("空集合:", empty_set)
```
## 创建一个带有初始元素的集合 `name = {itemValue1, itemValue2, ...}`
要使用`{}`创建一个集合，集合中的元素用逗号分隔。
```python
# 创建一个带有初始元素的集合
initial_set = {1, 2, 3, 4, 5}
print("带有初始元素的集合:", initial_set)

```
## 使用随机库生成一个包含随机数的集合
```python
# 使用随机库生成一个包含随机数的集合
import random

random_set = {random.randint(1, 100) for _ in range(10)}
print("包含随机数的集合:", random_set)
```
# 集合的基本操作
## 操作单个元素
- 添加元素 `setTemp.add(vlaue)`
- 删除元素 `setTemp.remove(value)`
- 检查元素是否存在 `value in setTemp`
## 整体操作集合
- 集合的长度 `len(setTemp)`
- 遍历集合 `for item in setTemp:`
- 清空集合 `setTemp.clear()`
- 删除集合 `del setTemp`
## 集合之间的操作
- 集合的交集 `setTemp1 & setTemp2`
- 集合的并集 `setTemp1 | setTemp2`
- 集合的差集 `setTemp1 - setTemp2`
- 集合的对称差集 `setTemp1 ^ setTemp2`
```python
# 集合的基本操作

# 添加元素
initial_set.add(6)
print("添加元素后的集合:", initial_set)

# 删除元素
initial_set.remove(3)
print("删除元素后的集合:", initial_set)

# 检查元素是否存在
element_exists = 2 in initial_set
print("元素2是否在集合中:", element_exists)

# 清空集合
initial_set.clear()
print("清空后的集合:", initial_set)

# 集合的长度
set_length = len(random_set)
print("随机集合的长度:", set_length)

# 集合的并集
another_set = {50, 60, 70}
union_set = random_set.union(another_set)
print("集合的并集:", union_set)

# 集合的交集
intersection_set = random_set.intersection(another_set)
print("集合的交集:", intersection_set)

# 集合的差集
difference_set = random_set.difference(another_set)
print("集合的差集:", difference_set)
```
## 去重
当你创建一个包含重复元素的集合时，Python 会自动去除重复的元素。<br/>
```python
weeks = {1,2,3,4,5,6,7,3,2,6,5}
print(weeks,"长度",weeks.__len__()) # {1, 2, 3, 4, 5, 6, 7} 长度 7
```
使用 set() 方法将集合或者其他可迭代对象（如列表、元组等）转换为集合，并且去除其中的重复元素。
`newSet = set(oldSet)`
```python
weeks = {1,2,3,4,5,6,7,3,2,6,5}
weeksUnique = set(weeks)
print(weeks,"长度",weeks.__len__(),"去重后的集合:", weeksUnique,"长度",weeksUnique.__len__())
```
# 集合的高级操作
展示集合的高级操作，如集合的并集、交集、差集和对称差集。
```python
# 集合的高级操作

# 创建两个集合
set_a = {1, 2, 3, 4, 5}
set_b = {4, 5, 6, 7, 8}

# 并集
union_ab = set_a | set_b
print("集合的并集:", union_ab)
# 集合的并集: {1, 2, 3, 4, 5, 6, 7, 8}

# 交集
intersection_ab = set_a & set_b
print("集合的交集:", intersection_ab)
# 集合的交集: {4, 5}

# 差集(a中有b中没有的元素)
difference_ab = set_a - set_b
print("集合的差集:", difference_ab)
# 集合的差集: {1, 2, 3}

# 对称差集(2个集合中不重复的元素)
symmetric_difference_ab = set_a ^ set_b
print("集合的对称差集:", symmetric_difference_ab)
# 集合的对称差集: {1, 2, 3, 6, 7, 8}
```
# 集合的应用示例
提供一些实际应用集合的示例，如去重、集合运算等。
```python
# 集合的应用示例

# 示例1: 去重
# 创建一个包含重复元素的列表
list_with_duplicates = [1, 2, 2, 3, 4, 4, 5]
# 使用集合去重
unique_elements = set(list_with_duplicates)
print("去重后的元素:", unique_elements)

# 示例2: 集合运算
# 创建两个集合
set_x = {1, 2, 3, 4, 5}
set_y = {4, 5, 6, 7, 8}

# 并集
union_xy = set_x | set_y
print("集合X和集合Y的并集:", union_xy)

# 交集
intersection_xy = set_x & set_y
print("集合X和集合Y的交集:", intersection_xy)

# 差集
difference_xy = set_x - set_y
print("集合X和集合Y的差集:", difference_xy)

# 对称差集
symmetric_difference_xy = set_x ^ set_y
print("集合X和集合Y的对称差集:", symmetric_difference_xy)

# 示例3: 判断子集和超集
# 判断set_x是否是set_y的子集
is_subset = set_x.issubset(set_y)
print("集合X是否是集合Y的子集:", is_subset)

# 判断set_y是否是set_x的超集
is_superset = set_y.issuperset(set_x)
print("集合Y是否是集合X的超集:", is_superset)

# 示例4: 集合的不可变集合
# 创建一个不可变集合
frozenset_example = frozenset([1, 2, 3, 4, 5])
print("不可变集合:", frozenset_example)

# 尝试添加元素到不可变集合会引发错误
try:
    frozenset_example.add(6)
except AttributeError as e:
    print("错误:", e)
```
