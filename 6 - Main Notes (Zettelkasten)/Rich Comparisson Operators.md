2025-07-24 14:37

### Status: #baby

### Tags: [[python]]

# RichOperations

In Python, rich comparison operators (<,>,<= and >=) delegate to the reverse method call when the inital method is missing OR returns [[[NotImplemented]]]. IN this example, the interpreter will call `x.__le__(y)`, which prints c and returns NotImplemented, so it then will call `y.__ge__(x)`which will then prints `d` and returns. The same logic will apply for the second statement -  `x.__lt__(y)`will print `a` and will return NotImplemented, so then the interpreter calls `y.__gt__(x)`which will print `b` and returns.

getcracked.io example:
![[Pasted image 20250724144140.png]]







# References









