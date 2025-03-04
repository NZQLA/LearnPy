# 构造函数
```python
class person:
	def __init__(self, name, age):
		self.name = name
		self.age = age
```
## 名字必须是`__init__`
## 第一个参数代表实例，其它名字也可以，即使是没有真正的参数，也必须包含这个实例参数
它就相当于`C#`中的`this` , 是一个指向实例本身的引用 。

# ![[Python内置类属性]]


# 继承
python[[../1 代码规范/允许多继承|允许多继承]]
继承语法是：`class 派生类名(基类名):`
```python
class person:
	def __init__(self, name, age):
		self.name = name
		self.age = age
	def display(self):
		print('name:',self.name)
		print('age:',self.age)
```
## 重写父类方法
```python
class student(person):
	def __init__(self, name, age, grade):
		person.__init__(self, name, age)
		self.grade = grade
	def display(self):
		# 调用父类方法
		person.display(self)
		print('grade:',self.grade)
```



