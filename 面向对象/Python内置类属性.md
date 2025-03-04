## `__dict__ `: 类的属性（包含一个字典，由类的数据属性组成）
会列出所有包含的属性，包括私有属性
## `__doc__`:类的文档字符串
class行下方第一个字符串将被视为类的文档
## `__name__`: 类名
## `__module__`: 类定义所在的模块（类的全名是'`__main__.className`'，如果类位于一个导入模块mymod中，那么className.`__module__` 等于 mymod）
## `__bases__` : 类的所有父类构成元素（包含了一个由所有父类组成的元组）
Python内置类属性调用实例如下：
```python
class Student:
	# 类的文档(class行下方第一个字符串将被视为类的文档)
	"""学生类"""
	"""
	构造函数 ， 顺便声明了三个属性
	其中 sex 是私有的
	"""

	def __init__(self, name, age, sex):
		self.name = name
		self.age = age

		# 将 sex 属性设为私有
		self.__sex = sex  

		# 添加获取 sex 属性的方法
	def get_sex(self):
		return self.__sex  

A = Student('Tom', 20, 'M')

print(A.__dict__)
print(A.__doc__)
print(A.__class__.__name__)
print(A.__module__)
print(Student.__bases__)
print(A.get_sex())  # 调用获取 sex 属性的方法
```

```python
{'name': 'Tom', 'age': 20, '_Student__sex': 'M'}
学生类
Student
__main__
(<class 'object'>,)
M
```

