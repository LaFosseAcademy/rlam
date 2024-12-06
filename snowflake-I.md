# Snowflake 1.0

To better understand Python, we will start with something simple...


## The Zen of Python

The Zen of Python is a collection of 19 "guiding principles" for writing computer programs that influence the design of the Python programming language. Python code that aligns with these principles is often referred to as "Pythonic".

```
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

With the 'guiding principles' in mind, let's dive into Python...


## Intro to Python

- Python is a high-level, general-purpose programming language that lets you work quickly and integrate systems more effectively. Its design philosophy emphasizes code readability with the use of significant indentation
- Python's name is derived from the British comedy group Monty Python
- Since 2003, Python has consistently ranked in the top ten most popular programming languages in the TIOBE Programming Community Index
- It was selected Programming Language of the Year in 2007, 2010, 2018, and 2020 (the only language to have done so four times as of 2020)
- Python has made its journey to be the second most demanded programming language in 2023

### What can Python do?

- Python can:
    - be used on a server to create web applications
    - be used alongside software to create workflows
    - connect to database systems. It can also read and modify files
    - be used to handle big data and perform complex mathematics
    - be used for rapid prototyping, or for production-ready software development

### Why Python?

- Python:
    - works on different platforms (Windows, Mac, Linux, Raspberry Pi, etc)
    - has a simple syntax similar to the English language
    - has syntax that allows developers to write programs with fewer lines than some other programming languages
    - runs on an interpreter system, meaning that code can be executed as soon as it is written. This means that prototyping can be very quick
    - can be treated in a procedural way, an object-oriented way or a functional way

<br>

## Coding with Python

### Variables

To declare variables in Python you only need to give it a name and declare it. Python has no command for declaring a variable

```python
age = 5
name = 'Anthony'

x = 3.14
y = 'banana'

print(name, age, x, y)
```

<br>

Variables in Python follow `snake_case` convention. If you want to set a `const` (immutable variable), just use capitalized letter

```python
IMPORTANT_VARIABLE = 'La Fosse Academy'
ANOTHER_IMPORT_VARIABLE = 'The Best Course'
```

<br>

We can also store many values to multiples variables at the same time

```python
x, y, z = 'Banana', 'Orange', 'Pineapple'
```

<br>

---

<br>

Python uses `print` to 'log' values

```python
x = 3.14
print(x)
```

<br>

And `#` is used for comments

```python
# this is a comment
y = 'Hello World' # this as well
```

<br>

---

<br>

### Data Types

In Python we have the following **Data Types**

|  Data Type  |Python Representation|
|-------------|---------------------|
|  Text Type  |        `str`        |
| Numeric Type|    `int`, `float`   |
|Sequence Type|   `list`, `tuple`   |
| Mapping Type|        `dict`       |
|   Set Type  |        `set`        |
| Boolean Type|       `bool`        |


<br>

To see the type of the Data use `type()`
```python
x = 3

print(type(x))
```

<br>

Examples of Data Type usage:

```python
# string
x = 'Hello World'

# integer
x = 20

# float (floating point number)
x = 3.14

# list
x = ['apple', 'banana', 'pear']

# tuple
x = ('London', 'Paris', 'Rome')

# dictionary
x = {'country': 'Brazil', 'capital': 'Brasilia'}

# set
x = {10, 20, 30}

# boolean
x = True
```

<br>

---


### Strings

Strings in Python are surrounded by either single or double quotes `''`/`""`
- `'hello'` is the same as `"hello"`

<br>

You can use `String Concatenation` (concatenate, or combine, two or more strings)

```python
a = 'Hello'
b = 'World'

c = a + b
print(c)
# HelloWorld

c = a + ' ' + b
print(c)
# Hello World
```

<br>

There's also `String Format` that uses `.format()`

```python
name = 'John Snow'
height = 1.93

print('Hello, my name is {}, and I am {}cm tall'.format(name, height))
# Hello, my name is John Snow, and I am 1.93cm tall
```

<br>

And `String Literal` or `f-string`

```python
name = 'Elizabeth'
city = 'London'

print(f'I am {name}, and I live in {city}.')
# I am Elizabeth, and I live in London.
```

This also works with numbers

```python
a = 5
b = 7

print(f'{a} + {b} is {a+b} and not {a*b}.')
# 5 + 7 is 12 and not 35.
```

<br>

String has these `methods`:

|Method|Description|
|------|-----------|
|`capitalize()`| Converts the first character to upper case|
|`count()`| Returns the number of times a specified value occurs in a string|
|`endswith()`| Returns true if the string ends with the specified value|
|`find()`| Searches the string for a specified value and returns the position of where it was found|
|`format()`| Formats specified values in a string|
|`index()`|	Searches the string for a specified value and returns the position of where it was found|
|`islower()`| Returns True if all characters in the string are lower case|
|`isnumeric()`|	Returns True if all characters in the string are numeric|
|`isupper()`| Returns True if all characters in the string are upper case|
|`join()`| Joins the elements of an iterable to the end of the string|
|`lower()`|	Converts a string into lower case|
|`replace()`| Returns a string where a specified value is replaced with a specified value|
|`split()`|	Splits the string at the specified separator, and returns a list|
|`startswith()`| Returns true if the string starts with the specified value|
|`strip()`|	Returns a trimmed version of the string|
|`swapcase()`| Swaps cases, lower case becomes upper case and vice versa|
|`title()`|	Converts the first character of each word to upper case|
|`upper()`|	Converts a string into upper case|

<br>

---

### Boolean

In Python `boolean` values are capitalized

```python
# True or False

print(10 > 9)
# True

print(10 == 9)
# False
```

<br>

---

### Operators

**Arithmetic Operators**

|Operator|	Name	|Example|
|--------|----------|-------|
|`+`|Addition|`x + y`|
|`-`|Subtraction|`x - y`|
|`*`|Multiplication|`x * y`|
|`/`|Division|`x / y`|
|`%`|Modulus|`x % y`|
|`**`|Exponentiation|`x ** y`|
|`//`|Floor division|`x // y`|

<br>

**Assignment Operators**

|Operator|Example |Same As|
|--------|--------|-------|
|`=`|`x = 5`|`x = 5`|
|`+=`|`x += 3`|`x = x + 3`|
|`-=`|`x -= 3`|`x = x - 3`|
|`*=`|`x *= 3`|`x = x * 3`|
|`/=`|`x /= 3`|`x = x / 3`|
|`%=`|`x %= 3`|`x = x % 3`|
|`//=`|`x //= 3`|`x = x // 3`|
|`**=`|`x **= 3`|`x = x ** 3`|

<br>

**Comparison Operators**

|Operator| Name|Example|
|--------|-----|-------|
|`==`|Equal|`x == y`|
|`!=`|Not equal|`x != y`|
|`>`|	Greater than|`x > y`|
|`<`|	Less than|`x < y`|
|`>=`|Greater than or equal to|`x >= y`|
|`<=`|Less than or equal to|`x <= y`|

<br>

**Logical Operators**

|Operator|Description|Example|
|--------|-----------|-------|
|`and`|Returns True if both statements are true|`x < 5 and x < 10`|
|`or`|Returns True if one of the statements is true|`x < 5 or x < 4`|
|`not`|Reverse the result, returns False if the result is true|`not(x < 5 and x < 10)`|

```python
x = 10

print(x < 5 and x > 11)
print(x < 5 or x < 4)
print(not(x < 5 and x < 10))
```

<br>

**Identity Operators**

|Operator|Description|Example|
|--------|-----------|-------|
|`is`|Returns True if both variables are the same object|`x is y`|
|`is not`|Returns True if both variables are not the same object|`x is not y`|

add example

<br>

**Membership Operator**

|Operator|Description|Example|
|--------|-----------|-------|
|`in`|Returns True if a sequence with the specified value is present in the object|`x in y`|
|`not in`|Returns True if a sequence with the specified value is not present in the object|`x not in y`|

add example

<br>

---

### Collections

- There is 4 collections in Python:
    - **List** is a collection which is ordered and changeable. Allows duplicate members
    - **Tuple** is a collection which is ordered and unchangeable. Allows duplicate members
    - **Set** is a collection which is unordered, *unchangeable*, and unindexed. No duplicate members. (Set *items* are unchangeable, but you can remove and/or add items whenever you like.)
    - **Dictionary** is a collection which is ordered and changeable. No duplicate members

<br>

### **Lists**

- **Lists** are used to store multiple items in a single variable
- **List** items are ordered, changeable, and allow duplicate values
- **List** items are indexed, the first item has index `[0]`, the second item has index `[1]`, etc
- You can check the end of your list using `[-1]`


Lists are created using square brackets:
```python
my_list = ['apple', 'banana', 'cherry']
```

<br>


List items can be of any data type:
```python
list1 = ['Ron', 'Hermione', 'Harry']
list2 = [1, 5.5, 7, 9, 3.14]
list3 = [True, False, False]

# OR

another_list = ['abc', 34, True, 40, 'male']
```

<br>

List items are indexed and you can access them by referring to the index number. (Remember index starts at `0`)
```python
my_list = ['audi', 'BMW', 'Mercedes-Benz']

print(my_list[1])
# BMW
```

There’s also Negative indexing, which means start from the end:
```python
my_list = ['audi', 'BMW', 'Mercedes-Benz', 'Aston Martin']

print(my_list[-1])
# Aston Martin
```

You can specify a range of indexes by specifying where to start and where to end the range
- This will start at index 2 and go up to, but not include index 5
```python
my_list = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango']

print(my_list[2:5])
# ['cherry', 'orange', 'kiwi']
```

You can check if an item exists in a list
```python
my_list = ['apple', 'banana', 'cherry', 'orange']

if 'cherry' in my_list:
  print('Yes, "cheery" is in the fruits list')
```

You can also change the value of a specific item, like referring to the index number
```python
my_list = ['apple', 'banana', 'cherry']
my_list[1] = 'blackcurrant'

print(my_list)
# apple, blackcurrant, cherry
```

<br>

### List Comprehension

List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list

```python
# Syntax
newlist = [expression for item in iterable if condition == True]
```

The return value is a new list, leaving the old list unchanged:
```python
fruits = ['apple', 'banana', 'cherry', 'kiwi', 'mango']
new_list = [x for x in fruits if 'a' in x]

print(new_list)
# ['apple', 'banana', 'mango']
```

<br>

To join, or concatenate, two or more lists you can use the `+` operator:
```python
list_one = ['cat', 'dog', 'horse']
list_two = [1, 2, 3]

list_three = list_one + list_two
print(list_three)
# ['cat', 'dog', 'horse', 1, 2, 3]
```

<br>

List has these `methods`:

|Method|Description|
|------|-----------|
|`append()`|Adds an element at the end of the list|
|`clear()`|Removes all the elements from the list|
|`copy()`|Returns a copy of the list|
|`count()`|Returns the number of elements with the specified value|
|`extend()`|Add the elements of a list (or any iterable), to the end of the current list|
|`index()`|Returns the index of the first element with the specified value|
|`insert()`|Adds an element at the specified position|
|`pop()`|Removes the element at the specified position|
|`remove()`|Removes the item with the specified value|
|`reverse()`|Reverses the order of the list|
|`sort()`|Sorts the list|

<br>

---

### Tuples

- **Tuples** are used to store multiple items in a single variable
- A **tuple** is a collection which is ordered and **unchangeable**, and allow duplicate values

Tuples are written with round brackets:
```python
my_tuple = ('penne', 'fusilli', 'farfalle')

print(my_tuple)
```

Tuple items can be of any data type:
```python
tuple1 = ('penne', 'fusilli', 'farfalle')
tuple2 = (1, 5.5, 7, 9, 3.14)
tuple3 = (True, False, False)
```

You can access Tuple items by referring to the index number:
```python
my_tuple = ('penne', 'fusilli', 'farfalle')

print(my_tuple[1])
# fusilli
```

Tuples also work with negative index:
```python
my_tuple = ('penne', 'fusilli', 'farfalle')

print(my_tuple[-1])
# farfalle
```

You can also check if the item exists:
```python
my_tuple = ('penne', 'fusilli', 'farfalle')

if 'penne' in my_tuple:
  print('Yes, "penne" is in the pasta tuple')
```

<br>

Tuples are *unchangeable*, meaning that you cannot **change**, **add**, or **remove** items once the tuple is created

You can loop through a Tuple using `for loop`:
```python
my_tuple = ('penne', 'fusilli', 'farfalle')

for x in my_tuple:
  print(x)
# penne
# fusilli
# farfalle
```

You can also join two Tuples
```python
tuple_one = ('spaghetti', 'cannelloni', 'tortelli')
tuple_two = (23, 65, 89)

tuple_three = tuple_one + tuple_two
print(tuple_three)
# ('spaghetti', 'cannelloni', 'tortelli', 23, 65, 89)
```

<br>

Tuple has these `methods`:

|Method|Description|
|------|-----------|
|`count()`|Returns the number of times a specified value occurs in a tuple|
|`index()`|Searches the tuple for a specified value and returns the position of where it was found|

<br>

---

### Sets

- **Sets** are used to store multiple items in a single variable
- A **set** is a collection which is *unordered*, *unchangeable*, and *unindexed, but you can remove and add items*

Sets are written with curly brackets:
```python
this_set = {'lion', 'giraffe', 'zebra'}

print(this_set)
```

Sets cannot have two items with the same value:
```python
my_set = {'lion', 'giraffe', 'zebra', 'lion'}

print(my_set)
# lion, giraffe, zebra
```

The values "`True` and `1`" & "`False` and `0`" are considered the same value in sets, and are treated as duplicates:
```python
my_set = {'lion', 'giraffe', 'zebra', True, 1, 4}

print(my_set)
# {True, 4, 'giraffe', 'zebra', 'lion'}

# AND

my_set = {'lion', 'giraffe', 'zebra', False, 0, 4}

print(my_set)
# {False, 4, 'lion', 'zebra', 'giraffe'}
```

Set items can be of any data type:
```python
set1 = {'lion', 'giraffe', 'zebra'}
set2 = {1, 5.5, 7, 9, 3.14}
set3 = {True, False, False}

# OR

set1 = {'abc', 34, True, 40, 'cat'}
```

<br>

You cannot access items in a set by referring to an index or a key
- But you can loop through the set items using a `for loop`, or ask if a specified value is present in a set, by using the `in` keyword

```python
my_set = {'lion', 'giraffe', 'zebra'}

for x in my_set:
  print(x)

# OR

my_set = {'lion', 'giraffe', 'zebra'}
print('giraffe' in my_set)
# True
```

Once a set is created, you cannot change its items, but you can `add`, `update`, and `remove` new items with the `methods`

<br>

Set has these `methods`:

|Method|Description|
|------|-----------|
|`add()`|	Adds an element to the set|
|`clear()`|Removes all the elements from the set|
|`copy()`|Returns a copy of the set|
|`difference()`|Returns a set containing the difference between two or more sets|
|`difference_update()`|Removes the items in this set that are also included in another, specified set|
|`discard()`|Remove the specified item|
|`pop()`|Removes an element from the set|
|`remove()`|Removes the specified element|
|`update()`|Update the set with the union of this set and others|

<br>

---

### Dictionaries

- **Dictionaries** are used to store data values in `key:value` pairs
- A **dictionary** is a collection which is ordered, changeable and do not allow duplicates
- The values in **dictionary** items can be of any data type

```python
my_dict = {
  'brand': 'Ford',
  'model': 'Mustang',
  'year': 1964,
  'electric': False,
  'colors': ['red', 'white', 'blue']
}
```

You can access the items of a dictionary by referring to its key name, inside square brackets:
```python
my_dict = {
  'brand': 'Ford',
  'model': 'Mustang',
  'year': 1964,
}

x = my_dict['model']
print(x)
```

To determine if a specified key is present in a dictionary use the `in` keyword:
```python
my_dict = {
  'brand': 'Ford',
  'model': 'Mustang',
  'year': 1964,
}

if 'model' in my_dict:
  print('Yes, the "mode" is one of the keys in the dictionary')
```

You can change the value of a specific item by referring to its key name:
```python
my_dict = {
  'brand': 'Ford',
  'model': 'Mustang',
  'year': 1964,
}

my_dict['year'] = 2018
```

Adding an item to the dictionary is done by using a new index key and assigning a value to it:
```python
my_dict = {
  'brand': 'Ford',
  'model': 'Mustang',
  'year': 1964,
}

my_dict['color'] = 'red'
print(my_dict)
```

You can loop through a dictionary by using a `for loop`:
```python
# Print all key names in the dictionary
for x in my_dict:
  print(x)

# Print all values in the dictionary
for x in my_dict:
  print(my_dict[x])
```

A dictionary can also contain dictionaries, this is called nested dictionaries:
```python
my_family = {
  'child_one' : {
    'name': 'James Sirius',
    'age': 10,
  },
  'child_two': {
    'name': 'Albus Severus',
    'age' 8,
  },
  'child_three': {
    'name': 'Lily Luna',
    'age': 5
  }
}
```

<br>

Dictionary has these `methods`:

|Method|Description|
|------|-----------|
|`clear()`|Removes all the elements from the dictionary|
|`copy()`|Returns a copy of the dictionary|
|`get()`|Returns the value of the specified key|
|`items()`|Returns a list containing a tuple for each key value pair|
|`keys()`|Returns a list containing the dictionary's keys|
|`pop()`|Removes the element with the specified key|
|`popitem()`|Removes the last inserted key-value pair|
|`update()`|Updates the dictionary with the specified key-value pairs|
|`values()`|Returns a list of all the values in the dictionary|

<br>

---

### If ... Else

- Python supports the usual **logical conditions** from mathematics
- These conditions can be used in several ways, most commonly in `if statements` and `loops`

```python
a = 33
b = 200

if b > a:
  print('b is greater than a')
```

The `elif` keyword is Python's way of saying "if the previous conditions were not true, then try this condition”:
```python
a = 33
b = 33

if b > a:
  print('b is greater than a')
elif a == b:
  print('a and b are equal')
```

The `else` keyword catches anything which isn't caught by the preceding conditions:
```python
a = 200
b = 33

if b > a:
  print('b is greater than a')
elif a == b:
  print('a and b are equal')
else:
  print('a is greater than b')
```

If you have only one statement to execute, you can put it on the same line as the if statement. These are called `Ternary Operators`, or `Conditional Expressions`:
```python
a = 2
b = 330

if a > b: print('a is greater than b')

# OR

print('A') if a > b else print('B')
```

The `and` & `or` keywords are logical operators, and are used to combine conditional statements:
```python
a = 200
b = 33
c = 500

if a > b and c > a:
  print('Both conditions are True')

# OR

if a > b or a > c:
  print('At least one of the conditions is True')
```

The `not` keyword is a logical operator, and is used to reverse the result of the conditional statement:
```python
a = 33
b = 200

if not a > b:
  print('a is NOT greater than b')
```

You can have `if` statements inside `if` statements, this is called `nested if` statements:
```python
x = 41

if x > 10:
  print('Above ten,')
  if x > 20:
    print('and also above 20!')
  else:
    print('but not above 20.')
```

<br>

---

### Loops

- Python has two primitive `loop` commands:
  - `while` loops
  - `for` loops

<br>

With the `while loop` we can execute a set of statements as long as a condition is true:
```python
i = 1

while i < 6:
  print(i)
  i += 1

# Always remember to increment i, or else the loop will continue forever
```

<br>

- A `for loop` is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string)
- With the `for loop` we can execute a set of statements, once for each item in a list, tuple, set etc

```python
fruits = ['apple', 'banana', 'orange']

for x in fruits:
  print(x)

# The for loop does not require an indexing variable to set beforehand
```

You can also `loop` through the letters in the word "marshmallow"
```python
for x in 'marshmallow':
  print(x)
```

<br>

- To loop through a set of code a specified number of times, we can use the `range()` function
- The `range()` function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and ends at a specified number

```python
for x in range(6):
  print(x)

# 0
# 1
# 2
# 3
# 4
# 5
```

You can also use `range(2, 6)`, which means values from 2 to 6 (but not including 6):
```python
for x in range(2, 6):
  print(x)

# 2
# 3
# 4
# 5
```

The `range()` function defaults to increment the sequence by 1, however it is possible to specify the increment value by adding a third parameter: `range(2, 20, 3)`:
```python
for x in range(2, 20, 3):
  print(x)

# 2
# 5
# 8
# 11
# 14
# 17
```

The `else` keyword in a `for loop` specifies a block of code to be executed when the loop is finished:
```python
for x in range(6):
  print(x)
else:
  print('Finally finished!')
```

<br>

- We can also have **Nested Loops**, a nested loop is a loop inside a loop
- The "inner loop" will be executed one time for each iteration of the "outer loop”

```python
colors = ['blue', 'white', 'black']
fruits = ['passion fruit', 'dragon fruit', 'kiwi']

for x in colors:
  for y in fruits:
    print(x, y)
```

<br>

---

### Functions

- A function is a block of code which only runs when it is called. You can pass data, known as parameters, into a function. A function can return data as a result
- In Python a function is defined using the `def` keyword

```python
def my_function():
  print('Hello from a function')

# To call this function
my_function()
```

Information can be passed into functions as arguments:
```python
def my_function(fname):
  print(f'Hello {fname}!!')

my_function('Arwen')
my_function('Legolas')
my_function('Elrond')
```

<br>

- **Parameters or Arguments?**
  - A ***parameter*** is the variable listed inside the parentheses in the function definition
  - An ***argument*** is the value that is sent to the function when it is called

To let a function return a value, use the `return` statement:
```python
def my_function(x):
  return 5 * x

print(my_function(3))
print(my_function(5))
print(my_function(9))
```

<br>

### Lambda Function

- A `lambda` function is a small **anonymous** function
- A `lambda` function can take any number of arguments, but can only have one expression

```python
# Syntax
lambda arguments : expression

# Function
x = lambda a : a + 10
```

`Lambda` functions can take any number of arguments:
```python
x = lambda a, b : a * b
print(x(5, 6))
```

<br>

---

## SQL

**SQL**:
- Stands for **Structured Query Language**
- Is a standard language for storing, manipulating and retrieving data in databases
- Lets you access and manipulate databases
- Became a standard of the American National Standards Institute (ANSI) in 1986, and of the International Organization for Standardization (ISO) in 1987

### What Can SQL do?
- execute queries against a database
- retrieve data from a database
- insert records in a database
- update records in a database
- delete records from a database
- create new databases
- create new tables in a database
- create stored procedures in a database
- create views in a database
- set permissions on tables, procedures, and views

<br>

Although **SQL** is an *ANSI/ISO* standard, there are different versions of the SQL language.

However, to be compliant with the *ANSI* standard, they all support at least the major commands (such as `SELECT`, `UPDATE`, `DELETE`, `INSERT`, `WHERE`) in a similar manner.

<br>

Some of The Most Important **SQL Commands**

|Command|Explanation|
|-------|-----------|
|`SELECT`|extracts data from a database|
|`UPDATE`|updates data in a database|
|`DELETE`|deletes data from a database|
|`INSERT INTO`|inserts new data into a database|
|`CREATE DATABASE`|creates a new database|
|`ALTER DATABASE`|modifies a database|
|`CREATE TABLE`|creates a new table|
|`ALTER TABLE`|modifies a table|
|`DROP TABLE`|deletes a table|
|`CREATE INDEX`|creates an index (search key)|
|`DROP INDEX`|deletes an index|

<br>

### How to Use SQL Queries

Image we want to create a dataset like this with **SQL**:

| **book_id** | **book_title**         | **book_author**     | **book_rating** | **genres**          |
|-------------|------------------------|---------------------|-----------------|---------------------|
| 1           | The Great Gatsby       | F. Scott Fitzgerald | 4.5             | Fiction, Classics   |
| 2           | To Kill a Mockingbird  | Harper Lee          | 4.8             | Fiction, Historical |
| 3           | 1984                   | George Orwell       | 4.7             | Fiction, Dystopian  |
| 4           | Pride and Prejudice    | Jane Austen         | 4.3             | Fiction, Romance    |
| 5           | The Catcher in the Rye | J.D. Salinger       | 3.9             | Fiction, Classics   |


<br>

For this example we will use [Neon](https://console.neon.tech/app/projects/gentle-wildflower-39565190?database=books&branchId=br-aged-meadow-a2pgn22l)

This is the *query* we should use:
```sql
CREATE TABLE books (
    book_id INT PRIMARY KEY,
    book_title VARCHAR(100),
    book_author VARCHAR(100),
    book_rating FLOAT,
    genres VARCHAR(255)
);

INSERT INTO books (book_id, book_title, book_author, book_rating, genres)
VALUES
(1, 'The Great Gatsby', 'F. Scott Fitzgerald', 4.5, 'Fiction, Classics'),
(2, 'To Kill a Mockingbird', 'Harper Lee', 4.8, 'Fiction, Historical'),
(3, '1984', 'George Orwell', 4.7, 'Fiction, Dystopian'),
(4, 'Pride and Prejudice', 'Jane Austen', 4.3, 'Fiction, Romance'),
(5, 'The Catcher in the Rye', 'J.D. Salinger', 3.9, 'Fiction, Classics');
```

After the table is created we can use other *queries*, like:

Retrieve all books:
```sql
SELECT * FROM books;
```

Retrieve specific columns:
```sql
SELECT book_title, book_author 
FROM books;
```

Find books with a rating above 4.5:
```sql
SELECT * 
FROM books 
WHERE book_rating > 4.5;
```

Find books in the "Fiction, Classics" genre:
```sql
SELECT book_title, genres 
FROM books 
WHERE genres = 'Fiction, Classics';
```

Find books whose title starts with 'P':
```sql
SELECT * 
FROM books 
WHERE book_title LIKE 'P%';
```

List all books ordered by rating (highest first):
```sql
SELECT book_title, book_rating 
FROM books 
ORDER BY book_rating DESC;
```

List all books alphabetically by title:
```sql
SELECT book_title, book_author 
FROM books 
ORDER BY book_title ASC;
```

Count the total number of books:
```sql
SELECT COUNT(*) AS total_books 
FROM books;
```

Calculate the average book rating:
```sql
SELECT AVG(book_rating) AS average_rating 
FROM books;
```

Find the highest and lowest ratings:
```sql
SELECT MAX(book_rating) AS highest_rating, MIN(book_rating) AS lowest_rating 
FROM books;
```

Find the number of books in each genre:
```sql
SELECT genres, COUNT(*) AS books_in_genre 
FROM books 
GROUP BY genres;
```

Calculate the average rating per genre:
```sql
SELECT genres, AVG(book_rating) AS average_genre_rating 
FROM books 
GROUP BY genres;
```

Update the rating of a specific book:
```sql
UPDATE books 
SET book_rating = 4.9 
WHERE book_title = 'The Great Gatsby';
```

Delete books with a rating below 4.0:
```sql
DELETE FROM books 
WHERE book_rating < 4.0;
```

Insert new books:
```sql
INSERT INTO books (book_id, book_title, book_author, book_rating, genres)
VALUES
(6, 'Brave New World', 'Aldous Huxley', 4.6, 'Fiction, Dystopian'),
(7, 'Moby-Dick', 'Herman Melville', 4.1, 'Fiction, Classics'),
(8, 'The Hobbit', 'J.R.R. Tolkien', 4.8, 'Fantasy, Adventure'),
(9, 'The Alchemist', 'Paulo Coelho', 4.2, 'Fiction, Philosophy'),
(10, 'War and Peace', 'Leo Tolstoy', 4.3, 'Fiction, Historical');
```

<br>

---

## Snowflake & Python

### What is Snowflake?

**Snowflake** is a cloud-based data platform that provides solutions for data warehousing, data lake management, data engineering, data sharing, and business intelligence. It allows organizations to store and analyze large volumes of structured and semi-structured data using a scalable and secure architecture.

**Key Features**:
- **Cloud-Native Architecture**: Snowflake runs entirely on cloud infrastructure like AWS, Microsoft Azure, and Google Cloud, offering scalability and performance without managing physical hardware.
- **Separation of Storage and Compute**: Users can scale storage and compute independently, optimizing costs and performance.
- **Data Sharing**: It enables seamless sharing of data across organizations without the need for complex integrations or data duplication.
- **Support for Multiple Workloads**: Snowflake supports various use cases, such as data warehousing, data lake management, machine learning, and real-time analytics.
- **SQL-Based Interface**: Snowflake uses standard SQL for querying and managing data, making it accessible to teams familiar with SQL.
- **Security and Compliance**: It includes features like data encryption, role-based access control, and compliance certifications for industries like finance and healthcare.

<br>

### How Python and Snowflake work together

Using Python with Snowflake offers a powerful combination for data analysis, automation, and integration. Python serves as the programming interface to connect, query, and manipulate data stored in Snowflake

### Why Use Python with Snowflake?

**Flexibility and Familiarity**:
- Python is a widely used language for data science, analytics, and automation. Snowflake's Python integration makes it accessible for data professionals already using Python.

**Advanced Data Processing**:
- Combine Snowflake's scalable query engine with Python libraries like Pandas, NumPy, or SciPy for advanced data analysis and transformation.

**Seamless Integration with Other Tools**:
- Python allows you to integrate Snowflake with other services (e.g., machine learning frameworks like TensorFlow or scikit-learn, or visualization tools like Matplotlib and Seaborn).

**Efficient Data Engineering**:
- Using Snowpark, Python scripts can run computations directly in Snowflake, leveraging its powerful cloud infrastructure without moving data out of the platform.

**Cost and Performance Optimization**:
- By processing data in Snowflake and retrieving only the necessary results to Python, you minimize data transfer and local computation costs.

**Workflow Automation**:
- Automate recurring tasks like ETL (Extract/Transform/Load) pipelines, data loading, or report generation.

<br>

### How to Use Python with Snowflake

Install the Snowflake Python Connector:
```python
pip install snowflake-connector-python
```

Connect to Snowflake:
```python
import snowflake.connector

# Establish connection
conn = snowflake.connector.connect(
    user='your_username',
    password='your_password',
    account='your_account_name'
)

# Create a cursor
cursor = conn.cursor()

# Execute a query
cursor.execute("SELECT CURRENT_VERSION()")
print(cursor.fetchone())

# Close the connection
conn.close()
```

<br>

---

### What is Snowpark?

**Snowpark** is a developer framework provided by Snowflake, enabling users to write data pipelines, data transformations, and other complex operations in Python, Java, or Scala directly within Snowflake. It brings the power of DataFrames and server-side programming to Snowflake's cloud-based data platform, allowing data engineers, scientists, and analysts to use their preferred languages for data processing at scale.

<br>

#### How Does Snowpark Work?

**Server-Side Execution**:
- Unlike traditional Python frameworks (like Pandas) that process data on the client machine, Snowpark executes all operations on the Snowflake servers.
- This approach takes advantage of Snowflake's powerful compute engine, eliminating data transfer overhead and improving performance.

**DataFrames**:
- Snowpark's DataFrame API enables users to manipulate data in a way similar to frameworks like Pandas or PySpark.
- Operations such as filtering, grouping, joining, and aggregating data are expressed as transformations on a DataFrame.
- The transformations are lazy, meaning they are compiled into SQL queries and executed when triggered (e.g., when calling `.collect()` or `.show()`).

**Integration with Snowflake**:
- Snowpark is tightly integrated with Snowflake, leveraging:
  - Snowflake’s virtual warehouses for compute.
  - SQL-based transformations, which Snowpark generates under the hood.
  - Secure, scalable, and high-performance storage of Snowflake.

**Extensibility**:
- Snowpark allows running custom Python code on Snowflake using user-defined functions (UDFs) and stored procedures.
- It supports Python libraries for machine learning and analytics, making it suitable for advanced workflows.

<br>

Use Snowpark for Data Engineering on IDE:
```python
# Install Snowpark
pip install snowflake-snowpark-python
```

```python
# Connect the configurations
from snowflake.snowpark import Session

# Connection configuration
connection_params = {
    "account": "your_account_name",
    "user": "your_username",
    "password": "your_password",
    "role": "your_role",
    "warehouse": "your_warehouse",
    "database": "your_database",
    "schema": "your_schema",
}

# Create session
session = Session.builder.configs(connection_params).create()

# Load a table into a DataFrame:
df = session.table("my_table")

# Perform transformations
from snowflake.snowpark.functions import col

filtered_df = df.filter(col("category") == "electronics")
aggregated_df = filtered_df.group_by("brand").agg(count("*").alias("count"))

aggregated_df.show()

# Run SQL directly using Snowpark
result = session.sql("SELECT * FROM my_table WHERE category = 'electronics'").collect()
```

<br>

Use Snowflake with Pandas:
```python
# Install the package
pip install snowflake-connector-python[pandas]
```

```python
import pandas as pd
from snowflake.connector.pandas_tools import write_pandas

# Fetch data into Pandas DataFrame
query = "SELECT * FROM your_table"
df = pd.read_sql(query, conn)

# Modify and upload data back to Snowflake
write_pandas(conn, df, 'your_table_name')
```

<br>

---

### Using Snowpark on Snowflake Dashboard

****** ADD SNOWFLAKE METHODS ******

On the top of the Dashboard you have to select the **Database** you want to work with, and later on the code you should refer just the name of the `table` you want to work with

```python
# Import the needed packages
import snowflake.snowpark as snowpark
from snowflake.snowpark.functions import col, count

# Define a function just for Python Extracting Data
def python_queries(session: snowpark.Session): 
    tableName = 'FXRATE'
    dataframe = session.table(tableName)

    # Snowflake cannot generate charts on under 1M rows, also any `limit` above 10k it takes ages to load
    # df = dataframe.select("base_currency", "rate_date", 'fx_rate_base_currency')
    # df = dataframe.filter(col("base_currency") == 'GBP').limit(15)
    # df = dataframe.order_by('rate_date')
    # df = dataframe.filter(col('base_currency') == 'GBP').order_by('rate_date').limit(10000)
    # df = dataframe.group_by('base_currency', 'fx_rate_base_currency').agg(count("*").alias("row_count"))

    # With this queries go on the Chart tab


    # Print a sample of the dataframe to standard output.
    df.show()

    # Return value will appear in the Results tab.
    return df

# Define a function just for SQL Extraction Data
def sql_queries(session: snowpark.Session):
    
    result = session.sql("SELECT * FROM fxrate WHERE base_currency = 'GBP'")
    # result = session.sql("SELECT * FROM fxrate LIMIT 10")
    # The SELECT DISTINCT statement is used to return only distinct (different) values
    # result = session.sql("SELECT DISTINCT base_currency FROM fxrate") # Find all unique base currencies
    # result = session.sql("SELECT base_currency, COUNT(*) AS count FROM fxrate GROUP BY base_currency ORDER BY count DESC") # Find the number of rows for each base currency
    # result = session.sql("SELECT * FROM fxrate WHERE rate_date BETWEEN '2024-01-01' AND '2024-01-31'") # Retrieve exchange rates for January 2024
    # result = session.sql("SELECT currency_pair, AVG(fx_rate_base_currency) AS avg_rate FROM fxrate GROUP BY currency_pair ORDER BY avg_rate DESC") # Get the average exchange rate (fx_rate_base_currency) for each currency pair
    # result = session.sql("SELECT MAX(fx_rate_base_currency) AS max_rate, MIN(fx_rate_base_currency) AS min_rate FROM fxrate WHERE base_currency = 'GBP'") # Find the highest and lowest exchange rates for a specific base_currency
    
    
    # With this queries go on the Chart tab
    # Line Chart
    # result = session.sql("SELECT rate_date, AVG(fx_rate_base_currency) AS avg_rate FROM fxrate WHERE base_currency = 'GBP' GROUP BY rate_date ORDER BY rate_date LIMIT 500")
    # Bar Chart
    # result = session.sql("SELECT quote_currency, COUNT(*) AS frequency FROM fxrate GROUP BY quote_currency ORDER BY frequency DESC LIMIT 20")
    # Scatter
    # result = session.sql("SELECT fx_rate_base_currency, fx_rate_quote_currency FROM fxrate WHERE base_currency = 'GBP' AND fx_rate_base_currency > 0.5 AND fx_rate_quote_currency > 0.5 LIMIT 10000")
    # Heatgrid
    # result = session.sql("SELECT base_currency, quote_currency, COUNT(*) AS frequency FROM fxrate GROUP BY base_currency, quote_currency ORDER BY frequency DESC LIMIT 10000")

    result.show()
    
    return result

# Lastly you need a `main` function to use Snowpark and call the other functions
def main(session: snowpark.Session):
    python_result = python_queries(session)
    sql_result = sql_queries(session)

    return python_result
```

<br>

#### Why use `session: snowpark.Session`

**Type Checking**
- Using `session: snowpark.Session` enables *type checking*, which:
  - Prevents Errors: If you accidentally pass an object of the wrong type, it can be flagged by your development environment (like an IDE or linter) before runtime.
  - Improves Debugging: You are explicitly specifying what kind of object the function expects, making errors easier to identify.

If you pass anything other than a `snowpark.Session` object, the code will fail since only `snowpark.Session` provides the methods (table, sql, etc.) used inside the function.

<br>

#### Why use `session.sql()`

- The `session.sql()` method allows you to directly execute raw *SQL* queries in Snowflake
- In this case, you're bypassing the Snowpark API and using Snowflake SQL to query the data directly
- Snowflake executes the SQL query and returns the results as a Snowpark DataFrame


- `session.sql()` is for executing raw *SQL* in Snowflake, giving you full SQL capabilities
- `DataFrame methods` allow you to interact with data programmatically using Python, following a logical query-building approach.