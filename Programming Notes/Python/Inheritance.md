# Inheritance In Python

```python
class Person:  
 def __init__(self, fname, lname):  
 self.firstname = fname  
 self.lastname = lname  
  
 def printname(self):  
 print(self.firstname, self.lastname)  
  
# Use the Person class to create an object, and then execute the printname method:  
  
x = Person("John", "Doe")  
x.printname()
```

```python

class student(Person):
pass

```

**Use the Pass keyword when you don't want to add anymore new methods or properties.**

```python
x = Student("Mike", "Olsen")  
x.printname()
```
Printing this will give the same result cuz this Student class inherites it's property from the Person class.

```python
class Student(Person):  
 def __init__(self, fname, lname):  
 #add properties etc.
```
- **When you are child having a init method you'll no longer inherit from the parent class.**
- **The Child init function overrides the parent's init function**

### We can also add a class to your parent class using super() function or the class name .init() with all the properties.

#### Class name with .init() method

```python
class Student(Person):  
 def __init__(self, fname, lname):  
 Person.__init__(self, fname, lname)
```


#### Super() function.

```python
class Student(Person):  
 def __init__(self, fname, lname):  
 super().__init__(fname, lname)
```

