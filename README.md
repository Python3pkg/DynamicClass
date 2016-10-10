# DinamicClass

Class to create attributes dynamically from class object

Installation : pip install DynamicClass

```python
class DynamicClass():
    def __getattr__(self, item):
        newobj = self.__class__()
        setattr(self, item, newobj)
        return newobj

a = DynamicClass()
a.foo = 'foo'
a.sub.nome = 'test1'
a.subobject2.sub1.teste = 'test2'

assert a.foo == 'foo'
assert a.sub.nome == 'test1'
assert a.subobject2.sub1.teste == 'test2'
```