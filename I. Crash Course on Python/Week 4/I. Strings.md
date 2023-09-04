# String Indexing and Slicing

[[String indexing]] allows you to access individual characters in a string. You can do this by using square brackets and the location, or index, of the character you want to access. It's important to remember that Python starts indexes at 0. So to access the first character in a string, you would use the index [0]. If you try to access an index that’s larger than the length of your string, you’ll get an **IndexError**. This is because you’re trying to access something that doesn't exist! You can also access indexes from the end of the string going towards the start of the string by using negative values. The index [-1] would access the last character of the string, and the index [-2] would access the second-to-last character.

You can also access a portion of a string, called a [[slice]] or a substring. This allows you to access multiple characters of a string. You can do this by creating a range, using a colon as a separator between the start and end of the range, like [2:5].

This range is similar to the range() function we saw previously. It includes the first number, but goes to one less than the last number. For example:

```python
>>> fruit = "Mangosteen" 
>>> fruit[1:4] 
>>> 'ang'
```

The slice _includes_ the character at index 1, and _excludes_ the character at index 4. You can also easily reference a substring at the start or end of the string by only specifying one end of the range. For example, only giving the end of the range:

```python
>>> fruit[:5] 
>>> 'Mango'
```

This gave us the characters from the start of the string through index 4, _excluding_ index 5. On the other hand this example gives is the characters _including_ index 5, through the end of the string:

```python
>>> fruit[5:] 
>>> 'steen'
```

You might have noticed that if you put both of those results together, you get the original string back!

```python
>>> fruit[:5] + fruit[5:] 
>>> 'Mangosteen'
```

# Sample code for indexing

```python
def replace_domain(email, old_domain, new_domain):
    # Check if the old domain is present in the email address
    if "@" + old_domain in email:
        # Find the index position of the "@" character followed by the old domain
        index = email.index("@" + old_domain)
        # Create a new email address by replacing the old domain with the new domain
        new_email = email[:index] + "@" + new_domain
        # Return the updated email address
        return new_email
    # If the old domain is not found in the email, return the original email
    return email
```

This function essentially checks if an email address contains a specific old domain and replaces it with a new domain if found. If the old domain is not present, it returns the original email unchanged.

# Basic String Methods

In Python, ***strings are immutable***. This means that they can't be modified. So if we wanted to fix a typo in a string, we can't simply modify the wrong character. We would have to create a new string with the typo corrected. We can also assign a new value to the variable holding our string.

If we aren't sure what the index of our typo is, we can use the string method _index_ to locate it and return the index. Let's imagine we have the string **"lions tigers and bears"** in the variable **animals**. We can locate the index that contains the letter **g** using _animals.index("g")_, which will return the index; in this case 8. We can also use substrings to locate the index where the substring begins. _animals.index("bears")_ would return 17, since that’s the start of the substring. If there’s more than one match for a substring, the index method will return the first match. If we try to locate a substring that doesn't exist in the string, we’ll receive a **ValueError** explaining that the substring was not found.

```python
animals = "lions tigers and bears"
animals.index("g")
```
Output:
```
8
```


```python
animals = "lions tigers and bears"
animals.index("bears")
```
Output:
```
17
```

We can avoid a ValueError by first checking if the substring exists in the string. This can be done using the _**in**_ keyword. We saw this keyword earlier when we covered _for_ loops. In this case, it's a conditional that will be either True or False. If the substring is found in the string, it will be True. If the substring is not found in the string, it will be False. Using our previous variable **animals**, we can do **"horses"** **in animals** to check if the substring "horses" is found in our variable. In this case, it would evaluate to False, since horses aren’t included in our example string. If we did **"tigers" in animals**, we'd get True, since this substring is contained in our string.

```python
animals = "lions tigers and bears"
"horses" in animals
```
Output:
```
False
```


```python
animals = "lions tigers and bears"
"tigers" in animals
```
Output:
```
True
```

# Advanced String Methods

We've covered a bunch of String class methods already, so let's keep building on those and run down some more advanced methods.

The string method **[[lower]]** will return the string with all characters changed to lowercase. The inverse of this is the **[[upper]]** method, which will return the string all in uppercase. Just like with previous methods, we call these on a string using dot notation, like **"this is a string".upper()**. This would return the string **"THIS IS A STRING"**. This can be super handy when checking user input, since someone might type in all lowercase, all uppercase, or even a mixture of cases.

```python
text = "This is a String"
lower_text = text.lower()
upper_text = text.upper()

print(lower_text)  # Output: "this is a string"
print(upper_text)  # Output: "THIS IS A STRING"
```

You can use the **[[strip]]** method to remove surrounding whitespace from a string. Whitespace includes spaces, tabs, and newline characters. You can also use the methods  **lstrip** and **rstrip** to remove whitespace only from the left or the right side of the string, respectively.

```python
text = "   Some whitespace   "
stripped_text = text.strip()
left_stripped_text = text.lstrip()
right_stripped_text = text.rstrip()

print(stripped_text)        # Output: "Some whitespace"
print(left_stripped_text)   # Output: "Some whitespace   "
print(right_stripped_text)  # Output: "   Some whitespace"
```

The method **[[count]]** can be used to return the number of times a substring appears in a string. This can be handy for finding out how many characters appear in a string, or counting the number of times a certain word appears in a sentence or paragraph.

```python
text = "This is a test sentence. This sentence is a test."
word = "is"
count = text.count(word)

print(f"The word '{word}' appears {count} times in the text.")
# Output: "The word 'is' appears 2 times in the text."
```

If you wanted to check if a string ends with a given substring, you can use the method **[[endswith]]**. This will return True if the substring is found at the end of the string, and False if not.

```python
text = "Hello, World!"
check1 = text.endswith("World!")
check2 = text.endswith("Hello")

print(check1)  # Output: True
print(check2)  # Output: False
```

The **[[isnumeric]]** method can check if a string is composed of only numbers. If the string contains only numbers, this method will return True. We can use this to check if a string contains numbers before passing the string to the **int()** function to convert it to an integer, avoiding an error. Useful!

```python
numeric_str = "12345"
non_numeric_str = "abc123"

check1 = numeric_str.isnumeric()
check2 = non_numeric_str.isnumeric()

print(check1)  # Output: True
print(check2)  # Output: False
```

We took a look at string concatenation using the plus sign, earlier. We can also use the **[[join]]** method to concatenate strings. This method is called on a string that will be used to join a list of strings. The method takes a list of strings to be joined as a parameter, and returns a new string composed of each of the strings from our list joined using the initial string. For example, **" ".join(["This","is","a","sentence"])** would return the string **"This is a sentence"**.

```python
words = ["This", "is", "a", "sentence"]
joined_text = " ".join(words)

print(joined_text)  # Output: "This is a sentence"
```

The inverse of the join method is the **[[split]]** method. This allows us to split a string into a list of strings. By default, it splits by any whitespace characters. You can also split by any other characters by passing a parameter.

```python
text = "This is a sentence"
split_text = text.split()  # By default, splits by whitespace

print(split_text)  # Output: ['This', 'is', 'a', 'sentence']
```

# String Formatting

You can use the **[[format]]** method on strings to concatenate and format strings in all kinds of powerful ways. To do this, create a string containing curly brackets, **{}**, as a placeholder, to be replaced. Then call the format method on the string using _.format()_ and pass variables as parameters. The variables passed to the method will then be used to replace the curly bracket placeholders. This method automatically handles any conversion between data types for us. 

If the curly brackets are empty, they’ll be populated with the variables passed in the order in which they're passed. However, you can put certain expressions inside the curly brackets to do even more powerful string formatting operations. You can put the name of a variable into the curly brackets, then use the names in the parameters. This allows for more easily readable code, and for more flexibility with the order of variables.

```python
name = "Alice"
age = 30
message = "Hello, {}! You are {} years old.".format(name, age)
print(message)  # Output: Hello, Alice! You are 30 years old.
```

```python
name = "Bob"
age = 25
message = "Hello, {name}! You are {age} years old.".format(name=name, age=age)
print(message)  # Output: Hello, Bob! You are 25 years old.
```

You can also put a formatting expression inside the curly brackets, which lets you alter the way the string is formatted. For example, the formatting expression **{:.2f}** means that you’d format this as a float number, with two digits after the decimal dot. The colon acts as a separator from the field name, if you had specified one. You can also specify text alignment using the greater than operator: **>**. For example, the expression **{:>3.2f}** would align the text three spaces to the right, as well as specify a float number with two decimal places. String formatting can be very handy for outputting easy-to-read textual output.

```python
price = 19.99
formatted_price = "The price is {:.2f} dollars.".format(price)
print(formatted_price)  # Output: The price is 19.99 dollars.
```

```python
value = 42
aligned_value = "Value: {:>5}".format(value)
print(aligned_value)  # Output: Value:    42
```

More complex example:
```python
# Define a function to convert Fahrenheit to Celsius
def to_celsius(x):
    return (x - 32) * 5 / 9

# Loop through Fahrenheit temperatures from 0 to 100 in steps of 10
for x in range(0, 101, 10):
    # Format and print the temperature in both Fahrenheit and Celsius
    print("{:>3} F | {:>6.2f} C".format(x, to_celsius(x)))

# Expected Output:
#  0 F | -17.78 C
# 10 F | -12.22 C
# 20 F |  -6.67 C
# 30 F |  -1.11 C
# 40 F |   4.44 C
# 50 F |  10.00 C
# 60 F |  15.56 C
# 70 F |  21.11 C
# 80 F |  26.67 C
# 90 F |  32.22 C
#100 F |  37.78 C
```

This code defines a function `to_celsius` to convert Fahrenheit to Celsius and then uses a loop to print a table of Fahrenheit and Celsius values in a well-formatted manner.

# String Reference Guide

In Python, there are a lot of things you can do with strings. In this guide, you’ll find the most common string operations and string methods.

### String operations

1. **[[len(string)]]** - Returns the length of the string.
   ```python
   text = "Hello, World!"
   length = len(text)
   print(length)  # Output: 13
   ```

2. **[[for character in string]]** - Iterates over each character in the string.
   ```python
   text = "Python"
   for char in text:
       print(char)  # Output: P y t h o n
   ```

3. **[[if substring in string]]** - Checks whether the substring is part of the string.
   ```python
   text = "Hello, World!"
   if "World" in text:
       print("Found")  # Output: Found
   ```

4. ``string[i]`` - Accesses the character at index i of the string, starting at zero.
   ```python
   text = "Python"
   char = text[2]
   print(char)  # Output: t
   ```

5. ``string[i:j]`` - Accesses the substring starting at index i, ending at index j minus 1. If i is omitted, its value defaults to 0. If j is omitted, the value will default to len(string).
   ```python
   text = "Python"
   substring = text[1:4]
   print(substring)  # Output: yth
   ```

### String methods

6. **[[string.lower()]]** - Returns a copy of the string with all lowercase characters.
   ```python
   text = "Hello, World!"
   lowercase = text.lower()
   print(lowercase)  # Output: hello, world!
   ```

7. **[[string.upper()]]** - Returns a copy of the string with all uppercase characters.
   ```python
   text = "Hello, World!"
   uppercase = text.upper()
   print(uppercase)  # Output: HELLO, WORLD!
   ```

8. **[[string.lstrip()]]** - Returns a copy of the string with the left-side whitespace removed.
   ```python
   text = "   Python"
   stripped = text.lstrip()
   print(stripped)  # Output: "Python" (with no leading spaces)
   ```

9. **[[string.rstrip()]]** - Returns a copy of the string with the right-side whitespace removed.
   ```python
   text = "Python   "
   stripped = text.rstrip()
   print(stripped)  # Output: "Python" (with no trailing spaces)
   ```

10. **[[string.strip()]]** - Returns a copy of the string with both the left and right-side whitespace removed.
    ```python
    text = "   Python   "
    stripped = text.strip()
    print(stripped)  # Output: "Python" (with no leading or trailing spaces)
    ```

11. **[[string.count(substring)]]** - Returns the number of times substring is present in the string.
    ```python
    text = "She sells seashells by the seashore."
    count = text.count("se")
    print(count)  # Output: 3
    ```

12. **[[string.isnumeric()]]** - Returns True if there are only numeric characters in the string. If not, returns False.
    ```python
    num_str = "12345"
    is_numeric = num_str.isnumeric()
    print(is_numeric)  # Output: True
    ```

13. **[[string.isalpha()]]** - Returns True if there are only alphabetic characters in the string. If not, returns False.
    ```python
    alpha_str = "Python"
    is_alpha = alpha_str.isalpha()
    print(is_alpha)  # Output: True
    ```

14. **[[string.split()]]** - Returns a list of substrings that were separated by whitespace (whitespace can be a space, tab, or new line).
    ```python
    text = "Split this sentence into words"
    words = text.split()
    print(words)  # Output: ['Split', 'this', 'sentence', 'into', 'words']
    ```

15. **[[string.split(delimiter)]]** - Returns a list of substrings that were separated by whitespace or a delimiter.
    ```python
    csv_data = "Alice,Bob,Charlie,David"
    values = csv_data.split(',')
    print(values)  # Output: ['Alice', 'Bob', 'Charlie', 'David']
    ```

16. **[[string.replace(old, new)]]** - Returns a new string where all occurrences of old have been replaced by new.
    ```python
    text = "Hello, World!"
    new_text = text.replace("World", "Python")
    print(new_text)  # Output: Hello, Python
	```

17. **[[delimiter.join(list of strings)]]** - Returns a new string with all the strings joined by the delimiter.

    ```python
    words = ["This", "is", "a", "sentence"]
    sentence = " ".join(words)
    print(sentence)  # Output: "This is a sentence"
    ```

Check out the official documentation for [all available String methods](https://docs.python.org/3/library/stdtypes.html#string-methods)

# Formatting Strings Guide

Python offers different ways to format strings. In the video, we explained the format() method. In this reading, we'll highlight three different ways of formatting strings. For this course you only need to know the format() method. But on the internet, you might find any of the three, so it's a good idea to know that the others exist.

### Using the format() method

The format method returns a copy of the string where the {} placeholders have been replaced with the values of the variables. These variables are converted to strings if they weren't strings already. Empty placeholders are replaced by the variables passed to format in the same order.

```python
# "base string with {} placeholders".format(variables)

example = "format() method"

formatted_string = "this is an example of using the {} on a string".format(example)

print(formatted_string)

"""Outputs:
this is an example of using the format() method on a string
"""
```

If the placeholders indicate a number, they’re replaced by the variable corresponding to that order (starting at zero).

```python
# "{0} {1}".format(first, second)

first = "apple"
second = "banana"
third = "carrot"

formatted_string = "{0} {2} {1}".format(first, second, third)

print(formatted_string)

"""Outputs:
apple carrot banana
"""
```

If the placeholders indicate a field name, they’re replaced by the variable corresponding to that field name. This means that parameters to format need to be passed indicating the field name.

```python
# "{var1} {var2}".format(var1=value1, var2=value2)

"{:exp1} {:exp2}".format(value1, value2)
```

If the placeholders include a colon, what comes after the colon is a formatting expression. See below for the expression reference.

Official documentation for [the format string syntax](https://docs.python.org/3/library/string.html#formatstrings)

### Formatting expressions

|Expr|Meaning|Example|
|---|---|---|
|{:d}|integer value|'{:d}'.format(10.5) → '10'|
|{:.2f}|floating point with that many decimals|'{:.2f}'.format(0.5) → '0.50'|
|{:.2s}|string with that many characters|'{:.2s}'.format('Python') → 'Py'|
|{:<6s}|string aligned to the left that many spaces|'{:<6s}'.format('Py') → 'Py    '|
|{:>6s}|string aligned to the right that many spaces|'{:>6s}'.format('Py') → '    Py'|
|{:^6s}|string centered in that many spaces|'{:^6s}'.format('Py') → '  Py '|

Check out the official documentation for [all available expressions](https://docs.python.org/3/library/string.html#format-specification-mini-language).

### Old string formatting (Optional)

The format() method was introduced in Python 2.6. Before that, the % (modulo) operator could be used to get a similar result. While this method is **no longer recommended** for new code, you might come across it in someone else's code. This is what it looks like:

```
"base string with %s placeholder" % variable
```

The % (modulo) operator returns a copy of the string where the placeholders indicated by %  followed by a formatting expression are replaced by the variables after the operator.

```
"base string with %d and %d placeholders" % (value1, value2)
```

To replace more than one value, the values need to be written between parentheses. The formatting expression needs to match the value type.

```
"%(var1) %(var2)" % {var1:value1, var2:value2}
```

Variables can be replaced by name using a dictionary syntax (we’ll learn about dictionaries in an upcoming video).

```
"Item: %s - Amount: %d - Price: %.2f" % (item, amount, price)
```

The formatting expressions are mostly the same as those of the format() method. 

Check out the official documentation for [old string formatting](https://docs.python.org/3/library/stdtypes.html#old-string-formatting).

### Formatted string literals (Optional)

This feature was added in Python 3.6 and isn’t used a lot yet. Again, it's included here in case you run into it in the future, but it's not needed for this or any upcoming courses.

A formatted string literal or f-string is a string that starts with 'f' or 'F' before the quotes. These strings might contain {} placeholders using expressions like the ones used for format method strings.

The important difference with the format method is that it takes the value of the variables from the current context, instead of taking the values from parameters.

Examples:
```
>>> name = "Micah"

>>> print(f'Hello {name}')

Hello Micah
```

```
>>> item = "Purple Cup"

>>> amount = 5

>>> price = amount * 3.25

>>> print(f'Item: {item} - Amount: {amount} - Price: {price:.2f}')

Item: Purple Cup - Amount: 5 - Price: 16.25
```


Check out the official documentation for [f-strings](https://docs.python.org/3/reference/lexical_analysis.html#f-strings)

# Study Guide: Strings

This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz. The string readings in this section are great syntax guides to help you on the Strings Practice Quiz.

In the Strings segment, you learned about the parts of a string, string indexing and slicing, creating new strings, string methods and operations, and formatting strings. 

# Knowledge

### String Operations and Methods

- **.format()** - String method that can be used to concatenate and format strings. 
    - **{:.2f}** - Within the .format() method, limits a floating point variable to 2 decimal places. The number of decimal places can be customized.
- **len(string)** - String operation that returns the length of the string.
- **string[x]** - String operation that accesses the character at index [x] of the string, where indexing starts at zero.
- **string[x:y]** - String operation that accesses a substring starting at index [x] and ending at index [y-1]. If x is omitted, its value defaults to 0. If y is omitted, the value will default to len(string).
- **string.replace(old, new)** - String method that returns a new string where all occurrences of an old substring have been replaced by a new substring.
- **string.lower()** - String method that returns a copy of the string with all lowercase characters.

# Coding skills

### **Skill Group 1**

- Use a **for** loop to iterate through each letter of a string.
- Add a character to the front of a string.
- Add a character to the end of a string.
- Use the **.lower()** string method to convert the case (uppercase/lowercase) of the letters within a string variable. _This method is often used to eliminate cases as a factor when comparing two strings. For example, all lowercase “cat” is not equal to “Cat” because “Cat” contains an uppercase letter. To be able to compare the two strings to see if they are the same word, you can use the .lower() string method to remove capitalization as a factor in the string comparison._

# Coding skills

### **Skill Group 1**

- Use a **for** loop to iterate through each letter of a string.
- Add a character to the front of a string.
- Add a character to the end of a string.
- Use the **.lower()** string method to convert the case (uppercase/lowercase) of the letters within a string variable. _This method is often used to eliminate cases as a factor when comparing two strings. For example, all lowercase “cat” is not equal to “Cat” because “Cat” contains an uppercase letter. To be able to compare the two strings to see if they are the same word, you can use the .lower() string method to remove capitalization as a factor in the string comparison._

```python
# This function accepts a given string and checks each character of 
# the string to see if it is a letter or not. If the character is a
# letter, that letter is added to the end of the string variable
# "forwards" and to the beginning of the string variable "backwards".
def mirrored_string(my_string):

    # Two variables are initialized as string data types using empty 
    # quotes. The variable "forwards" will hold the "my_string"
    # minus any character that is not a letter. The "backwards" 
    # variable will hold the same letters as "forwards", but in  
    # in reverse order.
    forwards = ""
    backwards = ""

    # The for loop iterates through each character of the "my_string"
    for character in my_string:

        # The if-statement checks if the character is not a space.
        if character.isalpha():

            # If True, the body of the loop adds the character to the
            # to the end of "forwards" and to the front of
            # "backwards". 
            forwards += character
            backwards = character + backwards

        # If False (meaning the character is not a letter), no action
        # is needed. This coding approach results prevents any 
        # non-alphabetical characters from being written to the
        # "forwards" and "backwards" variables. The for loop will 
        # restart until all characters in "my_string" have been
        # processed.
        
    # The final if-statement compares the "forwards" and "backwards"
    # strings to see if the letters are the same both forwards and
    # backwards. Since Python is case sensitive, the two strings will 
    # need to be converted to use the same case for this comparison. 
    if forwards.lower() == backwards.lower():
        return True
    return False
 
print(mirrored_string("12 Noon")) # Should be True
print(mirrored_string("Was it a car or cat I saw")) # Should be False
print(mirrored_string("'eve, Madam Eve")) # Should be True

```

