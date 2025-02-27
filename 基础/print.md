# `print()`

## 打印变量
格式`print("占位符1 占位符2 ... " % 变量1, 变量2, ...)`，其中`%`表示占位符，后面的变量会替换占位符
```python
percentCur = 35
print("当前比例: %d" % percentCur)
```


## 打印时拼接多个数据
```python
percentCur=80
timeUse=0.8
countRefresh=81
print("当前比例: %d, 耗时: %.2fs, 刷新次数: %d" % (percentCur, timeUse, countRefresh))
```

```python
content1 = "今天天气不错"
content2 = "风和日丽呀"
print("%s, %s" % (content1, content2))
```





## 多次打印时，覆盖之前打印的内容
 ```python
print("\r当前比例: %d" % percentCurrent, end="")
```
 > [!summary]  `/r` 表示将光标移动到行首  , `end:""` 表示结尾不用添加换行符
 > 默认情况下，末尾会自动添加换行符，如果不想换行，可以使用 `end=""` 参数
 > [[print.ipynb]]中模拟了一个从0到100的过程，每次仅打印当前的值，之前的会被覆盖
 

