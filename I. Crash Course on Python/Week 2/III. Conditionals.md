# Comparison Operators with Equations

The following examples demonstrate how to use comparison operators with the data types **int** (integers, whole numbers) and **float** (number with a decimal point or fractional value). Comparison operators return Boolean results. As you learned previously, [[Boolean]] is a data type that can hold only one of two values: **True** or **False**.

The comparison operators include:

- ``== (equality)
- ``!= (not equal to)
- ``>  (greater than)
- ``<  (less than)
- ``>= (greater than or equal to)
- ``<= (less than or equal to)

# `PART 1: Equality == and Not Equal To != Operators

In Python, you can use comparison operators to compare values. When a comparison is made, Python returns a Boolean result: **True** or **False**. Note that Boolean data types are not string data types (Boolean **True** is not equal to the string "True").  

- To check if two values are the same, use the **equality operator**: ``== 
- To check if two values are not the same, use the **not equal to operator**: ``!= 

The print() function can be used to display the results of the comparisons.

**Examples:**

```python
print(32 == 30+2)   # The == operator checks if the 2 values are 
True                # equal to each other. If they are equal, 
                    # Python returns a True result.

print(5+10 == 6+7)  # If the two values are not equal, as in the
False               # expression 5+10 == 6+7 (or 15 == 13), Python        
                    # returns a False result.

print(10-4 != 10+4) # The != operator checks if the 2 values are
True                # NOT equal to each other. If true, Python            
                    # returns a True result. 

print(9/3 != 3*1)   # In this last example, 9/3 != 3*1 (or 3 != 3)
False               # is false. So, Python returns a False value.
```

# ``PART 2: Greater Than > and Less Than < Operators

The comparison operators greater than **>** and less than **<** also return a **True** or **False** Boolean result after comparing two values.

- To check if one value is larger than another value, use the greater than operator: ``> 
- To check if one value is smaller than another value, use the less than operator: ``<

**Examples:**

```python
print(11 > 3*3)         # The > operator checks if the left value is
True                    # greater than the right value. If true, it
                        # returns a True result.

print(4/2 > 8-4)        # If the > operator finds that the left value
False                   # is NOT greater than the right value, the
                        # comparison will return a False result.

print(4/2 < 8-4)        # The < operator checks  if the left value is
True                    # less than the right side. If true, the
                        # comparison returns a True result.
print(11 < 3*3)         # If the < operator finds that the left side is False                   
                        # NOT less than the right value, Python returns
False                   # a False result.
```

# ``PART 3: Greater Than or Equal to >= and Less Than or Equal to <= Operators

Like the other comparison operators, the greater than or equal to **>=** and less than or equal to **<=** operators return a **True** or **False** Boolean result when a comparison is made.

- To check if one value is larger than or equal to another value, use the greater than or equal to operator: **>=** 
- To check if one value is smaller than or equal to another value, use the less than or equal to operator: **<=** 

**Examples:**

```python
print(12*2 >= 24)   # The >= operator checks if the left value is
True                # greater than or equal to the right value. 
                    # If one of these conditions is true,  
                    # Python returns a True result. In this case  
                    # the two values are equal. So, the comparison
                    # returns a True result.

print(18/2 >= 15)   # If the >= comparison determines that the left False
False               # value is NOT greater than or equal to the
                    # right, it returns a False result.

print(12*2 <= 30)   # The <= operator checks if the left value is
True                # less than or equal to the right value. In 
                    # this case, the left value is less than the
                    # right value. Again, if one of the two 
                    # conditions is true, Python returns a True
                    # result.

print(15 <= 18/2)   # If the <= comparison determines that the left 
False               # value is NOT less than or equal to the right
                    # value, the comparison returns a False result.
```

For additional Python practice, the following links will take you to several popular online interpreters and codepads:

- [Welcome to Python](https://www.python.org/shell/)
- [Online Python Interpreter](https://www.onlinegdb.com/online_python_interpreter)
- [Create a new Repl](https://repl.it/languages/python3)
- [Online Python-3 Compiler (Interpreter)](https://www.tutorialspoint.com/execute_python3_online.php)
- [Compile Python 3 Online](https://rextester.com/l/python3_online_compiler)
- [Your Python Trinket](https://trinket.io/python3)
# Key takeaways

Python comparison operators return Boolean results: **True** or **False**.
![[Pasted image 20230831101517.png]]
# Resources for more information

For more information about the concepts covered in these practice exercises, please visit:

- [Order of Operations](https://www.mathsisfun.com/operation-order-pemdas.html "Link to a website that reviews the order of operations")
- - A refresher on the mathematical Order of Operations. 
- [Python Comparison Operators with Syntax and Example](https://data-flair.training/blogs/python-comparison-operators/)
- - Provides examples of more complex comparisons.
- [Raise numbers to a power: here’s how to exponentiate in Python](https://kodify.net/python/math/exponents/)
- - Explains multiple methods for calculating exponents in Python.

# Comparison Operators with Strings

In this reading, you will learn more about what comparison operators can and cannot do. If you use the == (equality) and **!=** (not equal to) operators with strings, you can check if two strings contain the same text or not. You can also alphabetize strings using **>** (greater than), **<** (less than)**, >=** (greater than or equal to)**, <=** (less than or equal to) comparison operators. As with numeric data types, comparison operators used with strings will return Boolean (**True**, **False**) results.

## PART 1: Equality == and Not Equal to **!=** Operators with Strings

In Python, you can use comparison operators to compare strings. The equality == and the not equal to **!=** operators are helpful when you need to search for a specific string in a body of text, a log file, a spreadsheet, a database, and more. You can also check user input strings to compare them to another string. Note that Boolean data types are not string data types (Boolean **True** is not equal to the string "True").  

**Examples:**
```python
# The == operator can check if two strings are equal to each other. 
# If they are equal, the Python interpreter returns a True result.
print("a string" == "a string")
True

# In this example, the equality == comparison is between "4 + 5" and
# 4 + 5. Since the left data type is a string and the right data type
# is an integer, the two values cannot be equal. So, the comparison
# returns a False result.
print("4 + 5" == 4 + 5)
False

# The != operator can check if the two strings are NOT equal to each
# other. If they are indeed not equal, then Python returns a True result.
print("rabbit" != "frog")
True

# In this example, the variable event_city has been assigned the string 
# value "Shanghai". This variable is compared to a static string, 
# "Shanghai", using the != operator. As, the strings "Shanghai" and 
# "Shanghai" are the same, the comparison of "Shanghai" != "Shanghai" 
# is false. Accordingly, Python will return a False result.
event_city = "Shanghai"
print(event_city != "Shanghai")
False

# This last example illustrates the result of trying to compare two
# items of different data types using the equality == operator. The
# two items are not equal, so the comparison returns False.
print("three" == 3)
False
```

## PART 2: The Greater Than **>** and Less Than **<** Operators

The comparison operators greater than **>** and less than **<** can be used to alphabetize words in Python. The letters of the alphabet have numeric codes in Unicode (also known as ASCII values). The uppercase letters **A to Z are represented by the Unicode values 65 to 90**. **The lowercase letters a to z are represented by the Unicode values 97 to 122**.

![[bDQ-ePOZTn-CPAUMGiUoRQ_9657c1d2872d485783633c5fe8fa47f1_Unicode_table.png]]

- To check if the first letter(s) of a string have a larger Unicode value (meaning the letter is closer to 122 or lowercase z) than the first letter of another string, use the greater than operator: **>**
- To check if the first letter(s) of a string have a smaller Unicode value (meaning the letter is closer to 65 or uppercase A) than the first letter of another string, use the less than operator: **<** 

Like numeric comparisons with the greater than **>** and less than **<** operators, comparisons between strings also return Boolean **True** or **False** results.

```python
# The greater than > operator checks if the left string has a higher 
# Unicode value than the right string. If true, the Python interpreter
# returns a True result. Since W has a Unicode value of 87, and you can 
# easily calculate that F has a Unicode value of 70, this comparison is
# the same as 87 > 70. As this is true, Python will return a True 
# result.
print("Wednesday" > "Friday")
True
 
# The less than < operator checks if the left string has a lower 
# Unicode value than the right string. If you reference the Unicode 
# chart above, you can see that all lowercase letters have higher 
# Unicode values than uppercase letters. We can see that B has a 
# Unicode value of 66 and b has a Unicode value of 98. This 
# comparison is the same as 66 < 98, which is true. So, Python will 
# return a True result.
print("Brown" < "brown")
True

# If the strings have the same first few letters, the comparison will 
# cycle through each letter of each string, from left to right until it 
# finds two letters that have different Unicode values. In this example, 
# both strings share the initial substring "sun", but then have 
# different letters with different Unicode values in the fourth place 
# in each string. So, the fourth letters 'b' and 't' of the two
# strings are used for the comparison. Since 'b' does not have a higher
# Unicode value than 't', the comparison returns a False result.
print("sunbathe" > "suntan")
False

# If two identical strings are compared using the less than < comparison
# operator, this will produce a False result because they are equal.
print("Lima" < "Lima")
False

# This last example illustrates the result of trying to compare two
# items of different data types using the less than < operator. The 
# greater than > and less than operators < cannot be used to compare
# two different data types. 
print("Five" < 6)
'''
Error on line 1:
    print("Five" < 6)
TypeError: '<' not supported between instances of 'str' and 'int'
```

## `PART 3: The Greater Than or Equal To >= and Less Than or Equal To <= Operators

he greater than or equal to **>=** and less than or equal to **<=** operators can be used with strings as well. Like the other comparison operators, they will return a **True** or **False** Boolean result when a comparison is made between two strings. 
- To check if a string has a larger or equal Unicode value than the first letter(s) of another string, use the greater than or equal to operator: **>=** 
- To check if a string has a smaller or equal Unicode value than the first letter(s) of another string, use the less than or equal to operator: **<=**

At this point, you should be familiar with how comparison operators work in Python. Can you determine what the results will be from the comparisons listed below? When you are ready to check your answers, click Run.
1. "my computer" >= "my chair"
2. "Spring" <= "Winter"
3. "pineapple" >= "pineapple"

```python
# Use the Unicode chart in Part 2 to determine if the Unicode values of 
# the first letters of each string are higher, lower, or equal to one
# another. 

var1 = "my computer" >= "my chair"
var2 = "Spring" <= "Winter"
var3 = "pineapple" >= "pineapple"
 
print("Is \"my computer\" greater than or equal to \"my chair\"? Result: ", var1)
print("Is \"Spring\" less than or equal to \"Winter\"? Result: ", var2)
print("Is \"pineapple\" less than or equal to \"pineapple\"? Result: ", var3)
```
Output:
```
Is "my computer" greater than or equal to "my chair"? Result:  True
Is "Spring" less than or equal to "Winter"? Result:  True
Is "pineapple" less than or equal to "pineapple"? Result:  True
```

For additional Python practice, the following links are for several popular online interpreters and codepads:

- [Welcome to Python](https://www.python.org/shell/)
- [Online Python Interpreter](https://www.onlinegdb.com/online_python_interpreter)
- [Create a new Repl](https://repl.it/languages/python3)
- [Online Python-3 Compiler (Interpreter)](https://www.tutorialspoint.com/execute_python3_online.php)
- [Compile Python 3 Online](https://rextester.com/l/python3_online_compiler)
- [Your Python Trinket](https://trinket.io/python3)

# Key takeaways

Python comparison operators return Boolean results (**True** or **False**) with strings:
![[Pasted image 20230831104245.png]]
# Resources for more information

For more information about the concepts covered in these practice exercises, please visit:

- [Python String Comparison: A Step-by-Step Guide (with Examples)](https://www.codingem.com/python-string-comparison/)
- - A quick reference guide to using comparison operators with strings. Includes part of a Unicode table that displays all of the Unicode values for both uppercase and lowercase letters.
- [Comparing Strings using Python](https://stackabuse.com/comparing-strings-using-python/)
- - Provides more advanced examples of using comparison operators with strings.

# Logical Operators

Logical operators are used to construct more complex expressions. You can make complex comparisons by joining comparison statements together using the logical operators: **and**, **or**, **not**. Complex comparisons return a Boolean (**True** or **False**) result. 

- **and**
    - Both sides of the statement being evaluated must be True for the whole statement to be True.
    - Example: (5 > 1 **and** 5 **<** 10) = **True**
- **or**
    - If either side of the comparison is True, then the whole statement is True.
    - Example: (color = "blue" **or** color = "green") = **True**
- **not**
    - Inverts the Boolean result of the statement immediately following it. So, if a statement evaluates to True, and we put the not operator in front of it, it would become False.
    - Example: (**not** "A" == "A") = **False**

## PART 1: The **and** Logical Operator

In Python, you can use the logical operator **and** to connect more than one comparison. This type of complex comparison is used to check if two comparison statements are both True or not. You might use the **and** operator when you need to execute a block of code, but only if two different conditions are true. For example, you might want to write a script  that automates sending you an emergency alert if a server stops responding _and_ there is an unusual increase in employees opening trouble tickets.  

**Example 1:**

The following model demonstrates the use of the **and** logical operator to join comparisons between two mathematical expressions. The description below the example explains the order in which Python will process the line of code.

```python
# Example 1

print((6*3 >= 18) and (9+9 <= 36/2))
```
Output:
```
True
```

In the example above, the following activities were completed by Python in the following order:  

1. Python solves the numerical expressions using the order of operations. **(6*3 >= 18) and (9+9 <= 36/2) becomes (18 >= 18) and (18 <= 18)**
2. Python compares the results of the numerical expressions using the comparison operators (in this case >= and <=). **(18 >= 18) and (18 <= 18) becomes True and True**
3. Python checks if both sides of the logical operator "and" are true. **True and True become True**
4. Python returns a Boolean value: True or False. **The complex comparison returns a True result.**

**Example 2:**

In this next example, "Nairobi" < "Milan" and "Nairobi" > "Hanoi", the **and** logical operator is connecting two string comparison statements. You learned previously that using the greater than and less than operators on strings will test the alphabetical order (technically Unicode values) of the strings. So, this complex comparison is checking if "Nairobi" is alphabetized before "Milan" (False) AND after "Hanoi" (True). 

This comparison returns a False result because both sides of the logical operator are not True. A comparison statement like this might be used to iterate through a list of names to check if they are alphabetized in the correct order.

```python
# Example 2

print("Nairobi" < "Milan" and "Nairobi" > "Hanoi")
```
Output:
```
False
```

## PART 2: The **or** Logical Operator

The **or** logical operator tests two conditions to determine if at least one side of the **or** logical operator is True. The result of the test can be used to trigger a block of code if at least one condition is present.

**Syntax:**
```
Expression1 or Expression2
```

**Returns Booleans:**
![[Pasted image 20230831110818.png]]

**Examples:**
```python
# True or True returns True
print((15/3 < 2+4) or (0 >= 6-7))
True

# False or True returns True
print(country == "New York City" or city == "New York City")
True

# True or False returns True
print(16 <= 4**2 or 9**(0.5) != 3)
True

# False or False returns False
print("B_name" > "C_name" or "B_name" < "A_name”)
False
```

## PART 3: The **not** Logical Operator

The **not** logical operator inverts the value of the comparison expression. This is a helpful tool when you want to execute a block of code as long as a certain condition is **not** present.

- If the conditional  expression is True, the **not** logical operator can be added to make the expression **not** True (False). 
- If the conditional  expression is False, the **not** logical operator can be added to make the expression **not** False (True).  

**Syntax:**

```
not expression
```

**Example 1:**

```python
# Test Example 1:

x = 2*3 > 6
print("The value of x is:")
print(x)

print("")  # Prints a blank line

print("The inverse value of x is:")
print(not x)
```
Output:
```
The value of x is:
False

The inverse value of x is:
True
```

**Example 2:**

Can you determine the result of the following comparison?

```python
# What happens when you negate a False statement? 
# Click Run when you are ready to check your answer.


today = "Monday"
print(not today == "Tuesday") 


# The "today" variable states today is Monday. This makes the comparison
# "today == Tuesday" False. The logical operator "not" inverts the False
# result to become True. In other words, this expression asks if it is
# false that today is not Tuesday. More succinctly, "not False" means 
# True."
```
Output:
```
True
```

For additional Python practice, the following links are for several popular online interpreters and codepads:

- [Welcome to Python](https://www.python.org/shell/)
- [Online Python Interpreter](https://www.onlinegdb.com/online_python_interpreter)
- [Create a new Repl](https://repl.it/languages/python3)
- [Online Python-3 Compiler (Interpreter)](https://www.tutorialspoint.com/execute_python3_online.php)
- [Compile Python 3 Online](https://rextester.com/l/python3_online_compiler)
- [Your Python Trinket](https://trinket.io/python3)

# Key takeaways

When Python logical operators are used with comparison operators, the interpreter will return Boolean results (**True** or **False**):
![[Pasted image 20230831111228.png]]

# Resources for more information

For more information about the concepts covered in these practice exercises, please visit:
- [Understanding Boolean Logic in Python 3](https://www.digitalocean.com/community/tutorials/understanding-boolean-logic-in-python-3) A handy guide for reviewing both logical and conditional operators.

# if Statements Recap

We can use the concept of **branching** to have our code alter its execution sequence depending on the values of variables. We can use an _if_ statement to evaluate a comparison. We start with the _if_ keyword, followed by our comparison. We end the line with a colon. The body of the _if_ statement is then indented to the right. If the comparison is _**True**_, the code inside the _if_ body is executed. If the comparison evaluates to _**False**__,_ then the code block is skipped and will not be run.

# else Statements and the Modulo Operator

We just covered the _if_ statement, which executes code if an evaluation is true and skips the code if it’s false. But what if we wanted the code to do something different if the evaluation is false? We can do this using the _else_ statement. The _else_ statement follows an _if_ block, and is composed of the keyword _else_ followed by a colon. The body of the _else_ statement is indented to the right, and will be executed if the above _if_ statement doesn’t execute.

We also touched on the modulo operator, which is represented by the percent sign: **%**. This operator performs integer division, but only returns the remainder of this division operation. If we’re dividing 5 by 2, the quotient is 2, and the remainder is 1. Two 2s can go into 5, leaving 1 left over. So 5%2 would return 1. Dividing 10 by 5 would give us a quotient of 2 with no remainder, since 5 can go into 10 twice with nothing left over. In this case, 10%5 would return 0, as there is no remainder.