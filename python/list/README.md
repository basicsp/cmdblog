# Summary

##  url 
xxx
## 新增

```
lst.append("ha")  # 最后面添加1个元素
lst.extend(["h", "a"])  # 迭代添加2个元素
lst.extend("ha")  # 把字符串当迭代对象，添加了h和a两个元素，一般不是需要的
```
## 删除元素

```
lst.pop(2)  # 删除第二个元素
lst.remove("ha")  # 删除“ha”这个元素
del lst[1:3]  # 切片删除
lst.clear()  # 清空
```

## 套一个列表


```
a = 'a b c'
lst1 = list(a)  # ['a', ' ', 'b', ' ', 'c']
lst2 = [a]  # ['a b c']
```

# Usage

xxxx