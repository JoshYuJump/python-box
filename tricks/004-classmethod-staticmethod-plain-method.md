### 在操作类时，常用的有以下三种方法
> 类方法 @classmethod
>
> 静态方法 @staticmethod 
>
> 普通方法/实例方法 "plain" methods
>
# 他们的区别是什么呢?

```python
class MyClass:
    def method(self):
        """
        实例方法需要一个类的实例，并通过 self 访问实例本身。
        """
        return 'instance method called', self

    @classmethod
    def classmethod(cls):
        """
        类方法不需要类的实例。
        它不能通过 self 访问实例本身，
        但能通过 cls 访问类本身。
        """
        return 'class method called', cls

    @staticmethod
    def staticmethod():
        """
        静态方法不能访问 cls 和 self 
        它们是绑定在该类的命名空间下的普通函数
        """
        return 'static method called'

# 所有类型的方法都可以通过类实例直接调用：
>>> obj = MyClass()
>>> obj.method()
('instance method called', <MyClass instance at 0x1019381b8>)
>>> obj.classmethod()
('class method called', <class MyClass at 0x101a2f4c8>)
>>> obj.staticmethod()
'static method called'

# 类不能直接调用实例方法，会报 TypeError 的错误:
>>> MyClass.classmethod()
('class method called', <class MyClass at 0x101a2f4c8>)
>>> MyClass.staticmethod()
'static method called'
>>> MyClass.method()
TypeError: 
    "unbound method method() must be called with MyClass "
    "instance as first argument (got nothing instead)"
```    