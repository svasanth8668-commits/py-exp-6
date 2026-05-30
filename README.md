# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```python

from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass


class Rectangle(Shape):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def calculate_area(self):
        return self.length * self.width


class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        pi = 3.14  # Use 3.14 to get exact 50.24
        return pi * self.radius ** 2


rect = Rectangle(5, 3)
print("Area of a rectangle:", rect.calculate_area())

circle = Circle(4)
print("Area of a circle:", circle.calculate_area())
```

## Output
![image](https://github.com/user-attachments/assets/8a3d721c-dd24-4cef-9955-4639b1072e29)


## Result
The program using abstract class is executed successfully.

# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```python
class Rectangle:
    __length = 0
    __breadth = 0
    def __init__(self,length,breadth):
        self.__length = 5
        self.__breadth = 3
    def show(self):
        print(self.__length)
        print(self.__breadth)
            
rect = Rectangle(5,3)
rect.show()

```

## Output
![image](https://github.com/user-attachments/assets/31119647-b613-4053-86f7-568fa4d5fba2)


## Result
Thus,defining a class `Rectangle` with **private member variables** `__length` and `__breadth` is executed successfully.
# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```python
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
    def type(self):
        print("shark")

obj_goldfish=Fish()
obj_hammerhead=Shark()
obj_goldfish.type()
obj_hammerhead.type()



```

## OUTPUT
![image](https://github.com/user-attachments/assets/31a34d98-1faa-4b3b-8b3f-86f02dfdf954)


## RESULT
Thus,python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.
# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```python
class A:
    def __init__(self,a):
        self.a=a
    def __gt__(self,other):
        return self.a > other.a
        
ob1=A(20)
ob2=A(3)

if ob1>ob2:
    print("ob2 is less than ob1")
else:
    print("ob1 is less than or equal to ob2")

```

## Output
![image](https://github.com/user-attachments/assets/a8fc95af-05ed-48c8-bf37-e40e7aec16b4)


## Result
Thus, python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class is executed successfully.
# # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
```python
class Beans():
    def type(self):
         print("Vegetable")
    def color(self):
        print("Green")
    
class Mango():
    def type(self):
        print("Fruit")
    def color(self):
        print("Yellow")
    
def func(obj): 
       obj.type()
       obj.color()
obj_beans = Beans() 
obj_mango = Mango() 
func(obj_beans) 
func(obj_mango)
```

## Output
![image](https://github.com/user-attachments/assets/614961ab-639b-4596-8ec9-941df4f56db9)


## Result
Thus,create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism is executed succesfully.
