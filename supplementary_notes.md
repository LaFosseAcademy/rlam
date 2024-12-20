# RLAM - Supplementary Notes

These notes have been designed to compliment the core training and expand on the tools and technologies covered.

## Variables

In computer programming, **variables** are used to store data or objects referred to as a value. In the example below we have defined two variables; **age** and **name** which hold the values `5` and `'Simon'` respectively. 

```py
age = 5
name = 'Simon'
```

## Data Types

Our variables can be assigned to represent a number of different **data type's**. Although there are many different data types, the one's most commonly seen are:

1. Numeric Types - Assigned with no special rules
  - `int` - Integer values (e.g. `5`, `-10`)
  - `float` - Floating-point values (e.g. `3.14`, `-2.71`)

2. Text Type - Enclosed in either single (`'`) or double (`"`)
  - `str` - String values used for text data (e.g. `'foobar'`)

3. Boolean Type - Assigned with values (`True` or `False` - case-sesitive)
  - `bool` - Representing `True` or `False`
    - This can often be viewed like a condition (Yes/No or On/Off)

4. Sequence Types - Enclosed in square brackets `[]`.
  - `list` - Ordered collections(e.g. `[True, 'Hello World', 5]`)


```py
age = 5
name = 'Simon'
type(name)
```

## String Literals

String Literals or concatenation refers to combining two or more strings in a single string. 

As is often the case in computer programming there's multiple ways to achieve a specific outcome. Below you'll find an example using the `+` operator and also another example using **formatted strings**.

```py
name = 'Elizabeth'
city = 'London'

print('I am ' + name + ', and I live in ' + city) # Output: 'I am Elizabeth, and I live in London'
print(f'I am {name}, and I live in {city}') # Output: 'I am Elizabeth, and I live in London'
```

## String Methods

Python provides built **methods** specifically designed for working with its various data types. 

Below you'll find several examples of different **string methods**. 

A complete list can be accessed [here](https://docs.python.org/3/library/stdtypes.html#string-methods)

```py
# Capitalize
name = 'indiana jones'
profession = 'archaeologist'
name.capitalize() # Output: 'Indiana jones'

# Title 
name = 'indiana jones'
profession = 'archaeologist'
print(name.title()) # Output: 'Indiana Jones'

# Count
name = 'indiana jones'
profession = 'archaeologist'
print(profession.count('a')) # Output: 2

# Replace
name = 'indiana jones'
profession = 'archaeologist'
print(name.replace('indiana', 'matt')) # Output: 'matt jones'

# Chaining Methods
name = 'indiana jones'
profession = 'archaeologist'
print(name.replace('indiana', 'matt').title()) # Output: 'Matt Jones'
```

## Functions

Software engineers aim to minimise repeating similar code snippets to enhance maintainability and efficiency. When a built-in method isn't available, **functions** enable frequently used logic to be encapsulated into reusable blocks of code.

```py
def my_function(lotr_name): # Function defined with name 'my_function'
  print(f'Hello {lotr_name}!!') # Function code block

# my_function being called with three seperate 'arguments' 
my_function('Arwen') # Output: 'Hello Arwen!!'
my_function('Legolas') # Output: 'Hello Legolas!!'
my_function('Elrond') # Output: 'Hello Elrond!!'
```

## Packages 

Programming languages often come with built-in functionality, and we can define our own when needed. However, there are times when implementing certain functionality ourselves would be too resource-intensive or overly complex. In such cases, we can rely on pre-built packages of functionality, such as frameworks and libraries. These are collections of code developed and shared by other professionals, providing ready-to-use solutions for commonly required features.

```py
import pandas as pd
import matplotlib.pyplot as plt
```

Using the `import` syntax in the session you accessed and renamed two packages **pandas** and **matplotlib**.

- **pandas** renamed to **pd** is primariliy used as a powerful data manipulation and analysis tool, providing data atructures like DataFrames for handling structured data efficiently.
- **matplotlib** renamed to **plt** is a widely-used library for creating static and interactive visualisations in Python. 

## Snowflake 

**Snowflake** is designed to warehouse an organisations data. Within this ecosystem, users have access to **snowpark** which is a library developed to enable data processing and transformations using Python. 

The functionality specifically accessed from **snowpark** performs actions as defined below:
- **col**: allows referencing to a specific column in a DaraFrame.
- **avg**: computes the average of a column's values.
- **data_trunc()**: truncates a data with a specified precision (e.g. day, month, year).
- **round**: rounds numberical values to a specified number of decimal places.
- **count**: counts the number of rows or occurrences in a column.


```py
from snowflake.snowpark.context import get_active_session # Retrieves Snowflake session allowing users to connect to their database.
from snowflake.snowpark.functions import col, avg, date_trunc, round, count
session = get_active_session()
```