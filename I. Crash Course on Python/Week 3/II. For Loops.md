# For Loops Recap

_[[for]]_ loops allow you to iterate over a sequence of values. Let's take the example from the beginning of the video:

for x in range(5):

  print(x)

Similar to _if_ statements and _while_ loops, _for_ loops begin with the keyword _**for**_ with a colon at the end of the line. Just like in function definitions, _while_ loops and _if_ statements, the body of the _for_ loop begins on the next line and is indented to the right. But what about the stuff in between the _for_ keyword and the colon? In our example, we’re using the _range()_ function to create a sequence of numbers that our _for_ loop can iterate over. In this case, our variable **x** points to the current element in the sequence as the _for_ loop iterates over the sequence of numbers. Keep in mind that in Python and many programming languages, a range of numbers will start at 0, and the list of numbers generated will be one less than the provided value. So _range(5)_ will generate a sequence of numbers from 0 to 4, for a total of 5 numbers.

Bringing this all together, the range(5) function will create a sequence of numbers from 0 to 4. Our _for_ loop will iterate over this sequence of numbers, one at a time, making the numbers accessible via the variable **x** and the code within our loop body will execute for each iteration through the sequence. So for the first loop, **x** will contain 0, the next loop, 1, and so on until it reaches 4. Once the end of the sequence comes up, the loop will exit and the code will continue.

The power of _for_ loops comes from the fact that it can iterate over a sequence of any kind of data, not just a range of numbers. You can use _for_ loops to iterate over a list of strings, such as usernames or lines in a file.

Not sure whether to use a _for_ loop or a _while_ loop? Remember that a _while_ loop is great for performing an action over and over until a condition has changed. A _for_ loop works well when you want to iterate over a sequence of elements.

# A Closer Look at the Range() Function

The **in** keyword, when used with the **range()** function, generates a sequence of integer numbers, which can be used with a **for** loop to control the start point, the end point, and the incremental values of the loop. 

**Syntax:**

```python
for n in range(x, y, z):
    print(n)
```

The **[[range()]]** function uses a set of indices that point to integer values, which start at the number 0. The numeric values 0, 1, 2, 3, 4 correlate to ordinal index positions 1st, 2nd, 3rd, 4th, 5th. So, when a range call to the 5th index position is made using **range(5)** the index is pointing to the numeric value of 4.

|Index Number|1st index|2nd index|3rd index|4th index|5th index|
|---|---|---|---|---|---|
|Value|0|1|2|3|4|

The **[[range()]]** function can take up to three parameters:  **range(start, stop, step)** 

### **[[Start]]**  
The first item in the **range()** function parameters is the starting position of the range. The default is the first index position, which points to the numeric value 0. This value is included in the range. 

### **[[Stop]]** 
The second item in the **range()** function parameters is the ending position of the range. There is no default index position, so this index number must be given to the **range()** parameters. 

For example, the line **for n in range(4)** will loop 4 times with the **n** variable starting at 0 and looping 4 index positions: 0, 1, 2, 3. As you can see, **range(4)** (meaning index position 4) ends at the numeric value 3. In Python, this structure may be phrased as “the end-of-range value is _excluded_ from the range.” In order to include the value 4 in  **range(4)**, the syntax can be written as **range(4+1)** or **range(5)**. Both of these ranges will produce the numeric values 0, 1, 2, 3, 4.

### **[[Step]]** 
The third item in the **range()** function parameters is the incremental step value. The default increment is +1. The default value can be overridden with any valid increment. However, note that the loop will still end at the end-of-range index position, regardless of the incremental value. 

For example, if you have a loop with the range: **for n in range(1, 5, 6)**, the range will only produce the numeric value 1. This is because the incremental value of 6 exceeded the ending point of the range.

## Practice Exercise

You can use the code block below to test the values of **n** with various **range()** parameters. A few suggestions to test are:

**range(stop)**
- range(3) 
- range(3+1) 

**range(start, stop)**
- range(2, 6)     
- range(5,10+1) 

**range(start, stop, step)**
- range(4, 15+1, 2)         
- range(2*2, 25, 3+2) 
- range(10, 0, -2)

```python
for n in range(1, 5, 6):  
    print(n)
```
Output:
```
1
```

## Examples of the range() function in code:

**Example 1**

```python
# This loop iterates on the value of the "n" variable in a range
# of 0 to 10 (the value of the end-of-range index 11 is excluded).
# The incremental value for the loop is 2. The print() function will 
# output the resulting value of "n" as the loop counts from 0 to 10 
# (end-of-range index 11) in incremental steps of 2. This is one 
# method that can be used in Python to print a list of even numbers.

for n in range(0,11,2):
    print(n)

# The loop should print 0, 2, 4, 6, 8, 10
```
Output:
```
0
2
4
6
8
10
```

**Example 2**

```python
# This loop iterates on the value of the "number" variable in a range
# of 2 to 7+1 (the value of the end-of-range index 7 is excluded, so 
# +1 has been added to the parameter to include the numeric value 7 in 
# the range). The incremental value for the loop is the default of +1.
# The print() function will output the resulting value of "number" 
# multiplied by 3.

for number in range(2,7+1):
    print(number*3)

# The loop should print 6, 9, 12, 15, 18, 21
```
Output:
```
6
9
12
15
18
21
```

**Example 3**

```python
# This loop iterates on the value of the "x" variable in a range
# of 2 to -1 (the end-of-range index -2 is excluded). The third 
# parameter is also a negative number, making it a decremental value
# of -1. The print() function will output the resulting value of
# "x" as it starts at 2 and counts down to -1 (index -2).

for x in range(2, -2, -1):
    print(x)

# The loop should print 2, 1, 0, -1
```
Output:
```
2
1
0
-1
```

# Key takeaways

The roles of the **range(start, stop, step)** function parameters are:

- **Start** - Beginning of range
    - value included in range
    - default = 0
- **Stop** - End of range
    - value excluded from range (to include, use stop+1)
    - no default
    - must provide the ending index number 
- **Step** - Incremental value 
    - default = 1

# Resources for more information

- [Python range() function](https://www.geeksforgeeks.org/python-range-function/) - This site provides some helpful visualizations for the range index positions. It also offers multiple **for** x **in** **range()** examples and practice exercises. For additional Python practice, the following links will take you to several popular online interpreters and codepads:
- [Welcome to Python](https://www.python.org/shell/)
- [Online Python Interpreter](https://www.onlinegdb.com/online_python_interpreter)
- [Create a new Repl](https://repl.it/languages/python3)
- [Online Python-3 Compiler (Interpreter)](https://www.tutorialspoint.com/execute_python3_online.php)
- [Compile Python 3 Online](https://rextester.com/l/python3_online_compiler)
- [Your Python Trinket](https://trinket.io/python3)

# Study Guide: for Loops

This study guide provides a summary of what you learned in this segment and serves as a guide for the upcoming practice quiz.  

In the **for** Loops segment, you learned about the logical structure and syntax of **for** loops. You took a closer look at the **range()** function. You learned about nested **for** loops and complex nested **for** loops with **if** statements. You also learned how to fix common errors in **for** loops.

# **for** Loops vs. **while** Loops

**for** loops and **while** loops share several characteristics. Both loops can be used with a variety of data types, both can be nested, and both can be used with the keywords **break** and **continue**. However, there are important differences between the two types of loops: 

- **while** loops are used when a segment of code needs to execute repeatedly **while** a condition is true
- **for** loops iterate over a sequence of elements, executing the body of the loop **for** each element in the sequence

### Syntax 

The syntax of a **for** loop with the **in** keyword:

```python
for variable in sequence:
    body of loop
```

# Common **for** Loop Structures 

## **for** Loop with **range()**

The **in** keyword with the **range()** function generates a sequence of integer numbers, which can be used with a **for** loop to configure the iterations of the code. The range of numbers [0, 1, 2] correlates to ordinal index positions (1st, 2nd, 3rd), rather than the cardinal (quantity) values of the numbers 0, 1, and 2. For example, range(5) means the five index positions in the range [0, 1, 2, 3, 4]. 

The **range()** function can take up to three parameters. The roles of the three possible **range(x,y,z)** parameters are:

- **x = Start** - Starting index position of the range 
    - Default index position is 0.
    - The starting index position is included in the range. 
    - Example syntax: range(**2**, y, z) or range(**x+3**, y, z)
- **y = Stop** - Ending index position of range
    - No default index position. Must include the ending index position in the range() parameters.
        - Example syntax: range(**y**)
    - The value of the ending index position is excluded from the range. 
    - To include the ending index number, use the expression: **y+1** (index + 1)
        - Example syntax: range(x, **y+1**, z)
        - Alternatively, if **y** = 10, you can write: range(x, **11**, z)
- **z = Step** - Incremental value
    - Default increment is +1.
    - The default value can be overridden with any valid increment.
    - The incremental value will end the for loop before it reaches the end of range index position (end of range index minus 1).

Example of a **for** loop with the **in** keyword and the **range()** function:

```python
# This loop iterates on the value of the "number" variable in a range
# of 1 to 6+1 (the upper range limit of 6 is excluded, so +1 has
# been added to it to include 6 in the range). The incremental value
# for the loop is 2 (number+2). The print() function will output the
# resulting value of "number" multiplied by 3.

for number in range(1,6+1,2):
    print(number*3)

# The loop should print 3, 9, 15
```
Output:
```
3
9
15
```

### **Common pitfalls when using the range() function:**

- Forgetting that **the upper limit of a range() isn’t included** in the range.
- **Iterating over non-sequences.** For example, strings are iterable letter by letter, but not word by word.

```python
# This loop iterates on the value of the "number" variable in a range
# of 2 to 7 (the upper range limit of 8 is excluded). The print() 
# function will output the resulting value of "number" squared.

for number in range(2,8):
    print(number**2)

# The loop should print 4, 9, 16, 25, 36, 49
```
Output:
```
4
9
16
25
36
49
```

## Nested **for** Loops 

The syntax of nested **for** loops:

```python
for x in sequence:
    # start of the outer loop body
    for y in sequence:
        # start of the inner loop body

        # end of of the inner loop body
    # continue body of the outer loop
    # end of the outer loop body

```

Example of nested **for** loops: