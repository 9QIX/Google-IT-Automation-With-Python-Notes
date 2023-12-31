# Study Guide: Module 4 Graded Quiz

It is time to prepare for the Module 4 Graded Quiz. Please review the following items from this module before beginning the quiz. If you would like to refresh your memory on these materials, please also revisit the Study Guides located before each practice quiz in Module 4: [Study Guide: Strings](https://www.coursera.org/learn/python-crash-course/supplement/ydyIo/study-guide-strings), [Study Guide: Lists Operations and Methods](https://www.coursera.org/learn/python-crash-course/supplement/sbRdF/study-guide-lists-operations-and-methods), and [Study Guide: Dictionary Methods](https://www.coursera.org/learn/python-crash-course/supplement/Cc19J/study-guide-dictionary-methods).

# Knowledge

- How to output a list of the keys in a Python dictionary. 
- How to determine the output of a string index range used on a string.
- Determine what a list should contain after the .insert() method is used on the list.
- How to replace a specific word in a sentence with the same word in all uppercase letters.
- How to use a dictionary to count the frequency of letters in a string. 

## Operations, Methods, and Functions

- ### **String Methods, Operations, and Functions**
1. `.upper()`: This method returns a copy of the string with all characters converted to uppercase.
   ```python
   text = "hello world"
   result = text.upper()
   print(result)  # Output: "HELLO WORLD"
   ```

2. `.lower()`: This method returns a copy of the string with all characters converted to lowercase.
   ```python
   text = "Hello World"
   result = text.lower()
   print(result)  # Output: "hello world"
   ```

3. `.split()`: This method splits a string into a list of substrings based on a specified separator. By default, it splits on whitespace.
   ```python
   text = "apple orange banana"
   result = text.split()
   print(result)  # Output: ['apple', 'orange', 'banana']
   ```

4. `.format()`: This method is used for string formatting. You can insert variables or values into a string at specified positions using placeholders.
   ```python
   name = "John"
   age = 30
   message = "My name is {} and I am {} years old.".format(name, age)
   print(message)  # Output: "My name is John and I am 30 years old."
   ```

5. `.isnumeric()`: This method checks if all characters in the string are numeric (0-9).
   ```python
   number = "12345"
   result = number.isnumeric()
   print(result)  # Output: True
   ```

6. `.isalpha()`: This method checks if all characters in the string are alphabetic (letters).
   ```python
   text = "Hello"
   result = text.isalpha()
   print(result)  # Output: True
   ```

7. `.replace()`: This method replaces occurrences of a specified substring with another substring in a string.
   ```python
   text = "I like apples."
   result = text.replace("apples", "bananas")
   print(result)  # Output: "I like bananas."
   ```

8. String index `[ ]`: You can access individual characters in a string by their index, starting from 0 for the first character.
   ```python
   text = "Python"
   char = text[0]  # Access the first character 'P'
   print(char)
   ```

9. `len()`: This function returns the length (number of characters) of a string.
   ```python
   text = "Hello, World!"
   length = len(text)
   print(length)  # Output: 13
   ```


- ### **List Operations and Methods**

1. `.reverse()`: This method reverses the elements of a list in place.
   ```python
   my_list = [1, 2, 3, 4, 5]
   my_list.reverse()
   print(my_list)  # Output: [5, 4, 3, 2, 1]
   ```

2. `.extend()`: This method extends a list by appending elements from another iterable to the end of it.
   ```python
   list1 = [1, 2, 3]
   list2 = [4, 5, 6]
   list1.extend(list2)
   print(list1)  # Output: [1, 2, 3, 4, 5, 6]
   ```

3. `.insert()`: This method inserts an element at a specified position in a list.
   ```python
   my_list = [1, 2, 3, 5]
   my_list.insert(3, 4)
   print(my_list)  # Output: [1, 2, 3, 4, 5]
   ```

4. `.append()`: This method adds an element to the end of a list.
   ```python
   my_list = [1, 2, 3]
   my_list.append(4)
   print(my_list)  # Output: [1, 2, 3, 4]
   ```

5. `.remove()`: This method removes the first occurrence of a specified element from a list.
   ```python
   my_list = [1, 2, 3, 4, 3]
   my_list.remove(3)
   print(my_list)  # Output: [1, 2, 4, 3]
   ```

6. `.sort()`: This method sorts the elements of a list in ascending order in place.
   ```python
   my_list = [4, 1, 3, 2]
   my_list.sort()
   print(my_list)  # Output: [1, 2, 3, 4]
   ```

7. List comprehensions `[ ]`: List comprehensions are a concise way to create lists based on existing iterables.
   ```python
   numbers = [1, 2, 3, 4, 5]
   squares = [x**2 for x in numbers]
   print(squares)  # Output: [1, 4, 9, 16, 25]
   ```

8. List comprehensions `[ ]` with if condition: You can use list comprehensions with conditional statements to filter elements in the list.
   ```python
   numbers = [1, 2, 3, 4, 5]
   even_numbers = [x for x in numbers if x % 2 == 0]
   print(even_numbers)  # Output: [2, 4]
   ```

- ### **Dictionary Operations and Methods**

1. `.items()`: This method returns a view of all key-value pairs in a dictionary as tuples.
   ```python
   my_dict = {'a': 1, 'b': 2, 'c': 3}
   items = my_dict.items()
   print(items)  # Output: dict_items([('a', 1), ('b', 2), ('c', 3)])
   ```

2. `.update()`: This method updates a dictionary with key-value pairs from another dictionary or iterable.
   ```python
   dict1 = {'a': 1, 'b': 2}
   dict2 = {'b': 3, 'c': 4}
   dict1.update(dict2)
   print(dict1)  # Output: {'a': 1, 'b': 3, 'c': 4}
   ```

3. `.keys()`: This method returns a view of all keys in a dictionary.
   ```python
   my_dict = {'a': 1, 'b': 2, 'c': 3}
   keys = my_dict.keys()
   print(keys)  # Output: dict_keys(['a', 'b', 'c'])
   ```

4. `.values()`: This method returns a view of all values in a dictionary.
   ```python
   my_dict = {'a': 1, 'b': 2, 'c': 3}
   values = my_dict.values()
   print(values)  # Output: dict_values([1, 2, 3])
   ```

5. `.copy()`: This method creates a shallow copy of a dictionary.
   ```python
   original_dict = {'a': 1, 'b': 2}
   copied_dict = original_dict.copy()
   ```

6. `dictionary[key]`: You can access the value associated with a specific key in a dictionary using square brackets.
   ```python
   my_dict = {'a': 1, 'b': 2, 'c': 3}
   value = my_dict['b']
   print(value)  # Output: 2
   ```

7. `dictionary[key] = value`: You can assign a value to a specific key in a dictionary or add a new key-value pair.
   ```python
   my_dict = {'a': 1, 'b': 2}
   my_dict['c'] = 3  # Adding a new key-value pair
   my_dict['a'] = 4  # Updating the value of an existing key
   ```

# Coding Skills

## **Skill 1:** Using **string** methods

- Separate numerical values from text values in a string using **.split()**. 
- Iterate over the elements in a string.
- Test if the element contains letters with **.isalpha()**.
- Assign the elements of the split string to new variables.
- Trim any extra white space using **.strip()**.
- Format a string using **.format()** and **{ }** variable placeholders.

```python
def sales_prices(item_and_price):
    # Initialize variables "item" and "price" as strings
    item = ""
    price = ""
    # Create a variable "item_or_price" to hold the result of the split. 
    item_or_price = item_and_price.split()

    # For each element "x" in the split variable "item_or_price" 
    for x in item_or_price:

        # Check if the element is a number
        if x.isalpha():

            # If true, assign the element to the "item" string variable and add a space 
            # for any item names containing multiple words, like "Winter fleece jacket".
            item += x + " "

        # Else, if x is a number (if x.isalpha() is false): 
        else:
            # Assign the element to the "price" string variable. 
            price = x

    # Strip the extra space to the right of the last "item" word
    item = item.strip()

    # Return the item name and price formatted in a sentence 
    return "{} are on sale for ${}".format(item,price)


# Call to the function 
print(sales_prices("Winter fleece jackets 49.99"))
# Should print "Winter fleece jackets are on sale for $49.99"
```
Output:
```
Winter fleece jackets are on sale for $49.99
```

- Use the len() function to measure a string.

```python
# This function accepts a string variable "data_field".  
def count_words(data_field):

    # Splits the string into individual words. 
    split_data = data_field.split()
  
    # Then returns the number of words in the string using the len()
    # function. 
    return len(split_data)
    
    # Note that it is possible to combine the len() function and the 
    # .split() method into the same line of code by inserting the 
    # data_field.split() command into the the len() function parameters.

# Call to the function
count_words("Catalog item 3523: Organic raw pumpkin seeds in shell")
# Output should be 9
```
Output:
```
9
```

## **Skill 2:** Using **list** methods

- Reverse the order of a list using the **.reverse()** method.
- Combine two lists using the **.extend()** method.

```python
# This function accepts two variables, each containing a list of years.
# A current "recent_first" list contains [2022, 2018, 2011, 2006].
# An older "recent_last" list contains [1989, 1992, 1997, 2001].
# The lists need to be combined with the years in chronological order.
def record_profit_years(recent_first, recent_last):

    # Reverse the order of the "recent_first" list so that it is in 
    # chronological order.
    recent_first.reverse()

    # Extend the "recent_last" list by appending the newly reversed 
    # "recent_first" list.
    recent_last.extend(recent_first)

    # Return the "recent_last", which now contains the two lists 
    # combined in chronological order. 
    return recent_last

# Assign the two lists to the two variables to be passed to the 
# record_profit_years() function.
recent_first = [2022, 2018, 2011, 2006]
recent_last = [1989, 1992, 1997, 2001]

# Call the record_profit_years() function and pass the two lists as 
# parameters. 
print(record_profit_years(recent_first, recent_last))
# Should print [1989, 1992, 1997, 2001, 2006, 2011, 2018, 2022]
```
Output:
```
[1989, 1992, 1997, 2001, 2006, 2011, 2018, 2022]
```

## **Skill 3:** Using a **list comprehension** 

- Use a list comprehension [ ] as a shortcut for creating a new list from a range.
- Include a calculation with a **for** loop **in** a **range** with 2 parameters (lower, upper+1).

```python
# The function accepts two parameters: a start year and an end year.
def list_years(start, end):

    # It returns a list comprehension that creates a list of years in a for
    # loop using a range from the start year to the end year (inclusive of 
    # the upper range year, using end+1).
    return [year for year in range(start, end+1)]

# Call the years() function with two parameters.
print(list_years(1972, 1975)) 
# Should print [1972, 1973, 1974, 1975]
```
Output:
```
[1972, 1973, 1974, 1975]
```

- Use a list comprehension [ ] with a **for** loop and an **if** condition.

```python
# The function accepts two variable integers through the parameters and
# returns all odd numbers between x and y-1.
def odd_numbers(x, y):

# This list comprehension uses a for loop to iterate through values 
# of n in a range from x to y, with the value of y excluded (meaning
# keep the default range() function behavior to exclude the
# end-of-range value from the range). Since an incremental value is not 
# specified, the range function uses the default increment of +1.
# The if condition checks n to test if the number is odd using the
# modulo operator. This condition is written to check if n is divided 
# by 2, that the remainder is not 0. 
    return [n for n in range(x, y) if n % 2 != 0]

# Call the years() function with two parameters.
print(odd_numbers(5, 15)) 
# Should print [5, 7, 9, 11, 13]
```
Output:
```
[5, 7, 9, 11, 13]
```

## **Skill 4:** Using **dictionary** methods

- Iterate through the keys and values of a dictionary.
- Return the keys and values in a formatted string using the .format() function.

```python
# The network() function accepts a dictionary "servers" as a parameter.
def network(servers):

    # A string variable is initialized to hold the "result". 
    result = ""

    # For each "hostname" (key) and "IP address" (value) in the "server" dictionary items...
    for hostname, IP_address in servers.items():

        # A string identifying the hostname and IP address for each server is added
        # to the "result" variable. The string .format() function and is used to plug
        # the hostname and IP_address variables into the designated {} placeholders
        # within the string.
        result += "The IP address of the {} server is {}".format(hostname, IP_address) + "\n"
    
    # Return the "result" variable string.
    return result 

# Call the "network" function with the dictionary. 
print(network({"Domain Name Server":"8.8.8.8", "Gateway Server":"192.168.1.1", "Print Server":"192.168.1.33", "Mail Server":"192.168.1.190"}))

# Should print:
# The IP address of the Domain Name Server server is 8.8.8.8
# The IP address of the Gateway Server server is 192.168.1.1
# The IP address of the Print Server server is 192.168.1.33
# The IP address of the Mail Server server is 192.168.1.190
```
Output:
```
The IP address of the Domain Name Server server is 8.8.8.8
The IP address of the Gateway Server server is 192.168.1.1
The IP address of the Print Server server is 192.168.1.33
The IP address of the Mail Server server is 192.168.1.190
```

- Create a copy of a dictionary.
- Iterate through the values of the new dictionary.
- Change each value in the new dictionary, while keeping the same keys.

```python
# The scores() function accepts a dictionary "game_scores" as a parameter.
def reset_scores(game_scores):

    # The .copy() dictionary method is used to create a new copy of the "game_scores".
    new_game_scores = game_scores.copy() 

    # The for loop iterates over new_game_scores items, with the player as the key
    # and the score as the value. 
    for player, score in new_game_scores.items():
    
        # The dictionary operation to assign a new value to a key is used
        # to reset the grade values to 0.
        new_game_scores[player] = 0
  
    return new_game_scores
 
# The dictionary is defined.
game1_scores = {"Arshi": 3, "Catalina": 7, "Diego": 6}
 
# Call the "reset_scores" function with the "game1_scores" dictionary. 
print(reset_scores(game1_scores))
# Should print {'Arshi': 0, 'Catalina': 0, 'Diego': 0}
```
Output:
```
{'Arshi': 0, 'Catalina': 0, 'Diego': 0}
```

# Reminder: Correct syntax is critical

Using precise syntax is critical when writing code in any programming language, including Python. Even a small typo can cause a syntax error and the automated Python-coded quiz grader will mark your code as incorrect. This reflects real life coding errors in the sense that a single error in spelling, case, punctuation, etc. can cause your code to fail. Coding problems caused by imprecise syntax will always be an issue whether you are learning a programming language or you are using programming skills on the job. So, it is critical to start the habit of being precise in your code now. 

No credit will be given if there are any coding errors on the automated graded quizzes - including minor errors. Fortunately, you have 3 optional retake opportunities on the graded quizzes in this course. Additionally, you have unlimited retakes on practice quizzes and can review the videos and readings as many times as you need to master the concepts in this course.  

Now, before starting the graded quiz, please review this list of common syntax errors coders make when writing code.

**Common syntax errors:**

- Misspellings
- Incorrect indentations
- Missing or incorrect key characters:
    - Parenthetical types - ( curved ), [ square ], { curly }
    - Quote types - "straight-double" or 'straight-single', “curly-double” or ‘curly-single’
    - Block introduction characters, like colons - :
- Data type mismatches
- Missing, incorrectly used, or misplaced Python reserved words
- Using the wrong case (uppercase/lowercase) - Python is a case-sensitive language.

# Resources

For additional Python practice, the following links will take you to several popular online interpreters and codepads:

- [Welcome to Python](https://www.python.org/shell/) 
- [Online Python Interpreter](https://www.onlinegdb.com/online_python_interpreter) 
- [Create a new Repl](https://repl.it/languages/python3) 
- [Online Python-3 Compiler (Interpreter)](https://www.tutorialspoint.com/execute_python3_online.php)
- [Compile Python 3 Online](https://rextester.com/l/python3_online_compiler)
- [Your Python Trinket](https://trinket.io/python3)