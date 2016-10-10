# DinamicClass

Class to create attributes dynamically from class object

Installation : pip install DynamicClass

```python
from dynamicclass import DynamicClass

dc = DynamicClass()
dc.foo = 'foo'
dc.sub.nome = 'test1'
dc.subobject2.sub1.teste = 'test2'

assert dc.foo == 'foo'
assert dc.sub.nome == 'test1'
assert dc.subobject2.sub1.teste == 'test2'
```