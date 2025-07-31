2025-07-31 09:19

### Status: #baby

### Tags: [[python]]

# What is  _ _ name_ _  == `__main__``?

 _ _ name_ _  == `__main__` is a way of letting Python know which file to run.

Whenever you run a file, there the [[dunder]] function `__name__` will check if the file running is either a script or a module.

If script:
- the name will **always** be `__main__`

If module:
- `__name__` takes the name of the imported file

## Descriptions





# References









