# Snowflake 2.0

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

- How to use Jupyter Notebook on Codespace

1. Go to GitHub [Codespace](https://github.com/codespaces)
2. Then select `Use this template` under `Jupyter Notebook`
3. On the left hand side, click `notebooks`
4. Create a new file `index.ipynb`
5. On the new file click on `+ Code` (this will open a cell)
6. Write `import this` and use `shift + enter`
7. That will open a `kernel`
8. Select `Python Environments...`
9. Select `Python 3.12.1`
10. Run the cell again (`shift + enter`)

<br>

---

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

---

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

```python
# this is a comment
y = 'Hello World' # this as well
```

<br>

---

### Strings

Strings in Python are surrounded by either single or double quotes `''`/`""`
- `'hello'` is the same as `"hello"`

<br>

You can use `String Literal` or `f-string`, this is a type of `String Concatenation` (concatenate, or combine, two or more strings)


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

--- 

**Logical Operators**

|Operator|Description|Example|
|--------|-----------|-------|
|`and`|Returns True if both statements are true|`x < 5 and x < 10`|
|`or`|Returns True if one of the statements is true|`x < 5 or x < 4`|
|`not`|Reverse the result, returns False if the result is true|`not(x < 5 and x < 10)`|

```python
x = 10

print(x < 15 and x > 9) # True
print(x < 5 or x > 4) # True
print(not(x < 27 and x > 8)) # False
```

<br>

**Identity Operators**

|Operator|Description|Example|
|--------|-----------|-------|
|`is`|Returns True if both variables are the same object|`x is y`|
|`is not`|Returns True if both variables are not the same object|`z is not y`|

```python
x = 9
y = 9
z = 7

print(x is y) # True
print(z is not y) # True
```

<br>

**Membership Operator**

|Operator|Description|Example|
|--------|-----------|-------|
|`in`|Returns True if a sequence with the specified value is present in the object|`x in y`|
|`not in`|Returns True if a sequence with the specified value is not present in the object|`x not in y`|

```python
x = 'my'
y = 'Academy'

print(x in y) # True
print('course' not in y) # True
```

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


Lists are created using square brackets and can be of any data type:

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
my_list = ['apple', 'banana', 'cherry']

print(my_list[1])
# banana
```

You can specify a range of indexes by specifying where to start and where to end the range
- This will start at index 2 and go up to, but not include index 5
```python
my_list = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango']

print(my_list[2:5])
# ['cherry', 'orange', 'kiwi']
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

---

### Using Snowpark on Snowflake Dashboard

- There are some `methods` that are only available for `Python` on **Snowflake**
- To use or `transform` Python code with Snowpark you can use these:

|Method|Explanation|
|------|-----------|
|`col(col_name)`|Returns a reference to a column in the DataFrame|
|`select()`|Returns a new DataFrame with the specified Column expressions as output|
|`filter()`|Filters rows based on the specified conditional expression|
|`sort()`|Sorts a DataFrame by the specified expressions|
|`agg()`|Aggregate the data in the DataFrame|
|`count()`|Executes the query representing this DataFrame and returns the number of rows in the result|
|`group_by()`|Groups rows by the columns specified by expressions|
|`order_by()`|Sorts a DataFrame by the specified expressions|
|`where()`|Filters rows based on the specified conditional expression|
|`describe(*cols)`|Computes basic statistics for numeric columns, which includes count, mean, stddev, min, and max|
|`distinct()`|Returns a new DataFrame that contains only the rows with distinct values from the current DataFrame|
|`explain()`|Prints the list of queries that will be executed to evaluate this DataFrame|
|`show()`|Performing a query and print the results|
|`collect()`|Executes the query representing this DataFrame and returns the result as a list of Row objects|

<br>

---

1. Go to [Snowflake](https://app.snowflake.com/rlam/training/#/homepage) homepage
2. On the left hand side, go to `Home`
3. Then select `Write Python code`
4. Snowflake will create a file with some code in it, specially `Python` using `Snowpark`
5. At the top of the file you'll have to select the `Database` and `Schema` you want to use

```python
# Import the needed packages
import snowflake.snowpark as snowpark
from snowflake.snowpark.functions import col, count

# Define a function just for Python Extracting Data
def python_queries(session: snowpark.Session): 
    tableName = 'FXRATE'
    dataframe = session.table(tableName)

    starter = dataframe.select("base_currency", "rate_date", 'fx_rate_base_currency')
    df = starter.filter(col("base_currency") == 'GBP')
    df2 = starter.order_by('rate_date').limit(10000)
    df3 = starter.group_by('base_currency', 'fx_rate_base_currency').agg(count("*").alias("row_count"))


    # With this queries go on the Chart tab
    # Snowflake cannot generate charts on under 1M rows, also any `limit` above 10k it takes ages to load
    line_chart = df.group_by("rate_date").agg(avg("fx_rate_base_currency").alias("avg_rate")).sort("rate_date").limit(1000)
    bar_chart = df.group_by("quote_currency").agg(count("*").alias("frequency")).sort(col("frequency"), ascending=False).limit(50) # change Y-Axis to `quote_currency`

    # Print the entire dataframe first to show all the rows and columns available
    dataframe.show()

    # Print the other queries to show how to visualize just the columns and rows that you need
    starter.show()

    # Change the return according to what you have on `show()`
    return dataframe


# Define a function just for SQL Extraction Data
def sql_queries(session: snowpark.Session):
    select_all = session.sql("SELECT * FROM fxrate WHERE base_currency = 'GBP' LIMIT 10000")
    select_dist = session.sql("SELECT DISTINCT base_currency FROM fxrate") # Find all unique base currencies
    select_from = session.sql("SELECT base_currency, COUNT(*) AS count FROM fxrate GROUP BY base_currency ORDER BY count DESC") # Find the number of rows for each base currency
    select_where = session.sql("SELECT * FROM fxrate WHERE rate_date BETWEEN '2024-01-01' AND '2024-01-31'") # Retrieve exchange rates for January 2024
    
    
    # With this queries go on the Chart tab
    # Snowflake cannot generate charts on under 1M rows, also any `limit` above 10k it takes ages to load
    scatter_chart = session.sql("SELECT fx_rate_base_currency, fx_rate_quote_currency FROM fxrate WHERE base_currency = 'GBP' AND fx_rate_base_currency > 0.5 AND fx_rate_quote_currency > 0.5 LIMIT 10000")
    heatgrid_chart = session.sql("SELECT base_currency, quote_currency, COUNT(*) AS frequency FROM fxrate GROUP BY base_currency, quote_currency ORDER BY frequency DESC LIMIT 10000")

    # Change show and result according to the query you want to display
    result.show()
    
    return result

# Lastly you need a `main` function to use Snowpark and call the other functions
def main(session: snowpark.Session):
    python_result = python_queries(session)
    sql_result = sql_queries(session)

    return python_result
```

<br>

---

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