2025-07-24 14:49

### Status: #baby

### Tags: [[python]]

# NotImplemented
NotImplemented is a special singleton value (like None) used primarily within *binary special methods* such as `__eq__`, `__add__`, and others. This serves to indicate the the operation is *not implemented* for the given operands.

#### So is it an error?
Not exactly, it is more of a showing that that specific object does not handle what is being passed, but other object in the class might.

```
class MyNumber:
    def __eq__(self, other):
        if isinstance(other, MyNumber):
            return self.value == other.value
        return NotImplemented
```

So, for example, the following code:
```
class A:
    def __eq__(self, other):
        return NotImplemented

class B:
    def __eq__(self, other):
        return True

a = A()
b = B()

print(a == b)  # True
```

So here `a.__eq__(b)` will return `NotImplemented`, so Python will try then `b.__eq__(a)` which will return `True`




# References

http://docs.python.org/3/library/constants.html
https://www.pythonmorsels.com/when-to-use-notimplemented/2025-07-24 15:15

### Status: 

### Tags:

# [NotImplemented









# References

















