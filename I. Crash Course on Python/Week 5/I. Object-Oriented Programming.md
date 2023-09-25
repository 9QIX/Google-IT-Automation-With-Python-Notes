# Object-Oriented Programming Defined

In object-oriented programming, concepts are modeled as **[[classes]]** and **[[objects]]**. An idea is defined using a class, and an instance of this class is called an object. Almost everything in Python is an object, including strings, lists, dictionaries, and numbers. When we create a list in Python, we’re creating an object which is an instance of the list class, which represents the concept of a list. Classes also have attributes and methods associated with them. **[[Attributes]]** are the characteristics of the class, while methods are functions that are part of the class.

1. **[[Class]]:** A class is a blueprint or template that defines the structure and behavior of an object. It serves as a model for creating objects of that class. In Python, classes are defined using the `class` keyword and can contain attributes and methods.
2. **[[Object]]:** An object is an instance of a class, created based on the class's blueprint. Objects represent specific instances or occurrences of a concept. For example, if you have a `Car` class, an object of that class could represent a specific car with its unique properties and behaviors.
3. **[[Attributes]]:** Attributes are the characteristics or properties associated with a class or object. These attributes store data that describes the object's state. In Python, attributes are defined within a class and can have different data types like strings, numbers, or other objects. For example, a `Car` class might have attributes like `color`, `make`, and `model`.
4. **[[Methods]]:** Methods are functions defined within a class that can perform actions or operations related to that class. They define the behaviors or actions that objects of the class can undertake. Methods can access and manipulate the attributes of the class. For instance, a `Car` class might have methods like `start_engine()` and `accelerate()`.

In Python, OOP is an integral part of the language, and most data types and operations are implemented using classes and objects. This makes Python highly extensible and allows you to create custom classes to model specific concepts or entities in your programs.

Here's a Pythonic example to illustrate these concepts:

```python
# Define a class called Car
class Car:
    # Constructor method to initialize attributes
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.is_running = False  # A boolean attribute

    # Method to start the car's engine
    def start_engine(self):
        self.is_running = True
        print(f"The {self.year} {self.make} {self.model}'s engine is now running.")

    # Method to accelerate the car
    def accelerate(self):
        if self.is_running:
            print(f"The {self.year} {self.make} {self.model} is accelerating.")
        else:
            print(f"You need to start the engine first.")

# Create an instance (object) of the Car class
my_car = Car("Toyota", "Camry", 2022)

# Access attributes and call methods
print(f"My car is a {my_car.year} {my_car.make} {my_car.model}.")
my_car.start_engine()
my_car.accelerate()
```

In this example, `Car` is a class, `my_car` is an object, and `make`, `model`, `year`, and `is_running` are attributes. The `start_engine()` and `accelerate()` methods define behaviors associated with the `Car` class.

# Classes and Objects in Detail

We can use the **type()** function to figure out what class a variable or value belongs to. For example, **type(" ")** tells us that this is a string class. The only attribute in this case is the string value, but there are a bunch of methods associated with the class. We've seen the **upper()** method, which returns the string in all uppercase, as well as **isnumeric()** which returns a boolean telling us whether or not the string is a number. You can use the **dir()** function to print all the attributes and methods of an object. Each string is an instance of the string class, having the same methods of the parent class. Since the content of the string is different, the methods will return different values. You can also use the **help()** function on an object, which will return the documentation for the corresponding class. This will show all the methods for the class, along with parameters the methods receive, types of return values, and a description of the methods.

# Defining Classes (Optional)

We can create and define our classes in Python similar to how we define functions. We start with the **class** keyword, followed by the name of our class and a colon. Python style guidelines recommend class names to start with a capital letter. After the class definition line is the class body, indented to the right. Inside the class body, we can define attributes for the class.

Let's take our Apple class example:

```python
>>> class Apple:
...     color = ""
...     flavor = ""
... 
```

We can create a new instance of our new class by assigning it to a variable. This is done by calling the class name as if it were a function. We can set the attributes of our class instance by accessing them using dot notation. Dot notation can be used to set or retrieve object attributes, as well as call methods associated with the class.

```python
>>> jonagold = Apple()
>>> jonagold.color = "red"
>>> jonagold.flavor = "sweet"
```

We created an Apple instance called jonagold, and set the color and flavor attributes for this Apple object. We can create another instance of an Apple and set different attributes to differentiate between two different varieties of apples.

```python
>>> golden = Apple()
>>> golden.color = "Yellow"
>>> golden.flavor = "Soft"
```

We now have another Apple object called golden that also has color and flavor attributes. But these attributes have different values.