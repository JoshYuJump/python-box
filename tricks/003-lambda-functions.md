## 003 匿名函数 lambda 函数

---

```python

# 在 python 里面，可以使用 lambda 关键字 
# 声明一个小的匿名函数 :

>>> add = lambda x, y: x + y
>>> add(5, 3)
8

# 你也可以用 def 关键字声明同样的 `add` 函数

>>> def add(x, y):
...     return x + y
>>> add(5, 3)
8

# 所有这样写没有什么好奇怪的?
# Lambda 就是 *函数表达式*:
>>> (lambda x, y: x + y)(5, 3)
8

# • Lambda 函数是单一表达式 
# 不需要函数名的函数（匿名函数）

# • Lambda 函数与普通函数不同
# 永远有一个隐式的 return 

```

> 原文：https://www.getdrip.com/deliveries/bptjmirv1btvobyz6hws?__s=8qjjroyi3vmjjxziqp7v
