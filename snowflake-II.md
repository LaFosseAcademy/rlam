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

- A **variable** is a named storage location in programming that holds a value, which can be changed during program execution

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

- A data type defines the kind of value a variable can hold, such as integers, strings, or floating-point numbers

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

- A string is a data type used to represent a sequence of characters, such as words or sentences

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

- A logical operator is used to combine or modify boolean expressions, typically including `AND`, `OR`, and `NOT`

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

- Identity operators are used to check if two variables refer to the same object or have the same value, using `is` and `is not`

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

- A membership operator is used to check if a value is present in a sequence, such as a list, tuple, or string, using `in` or n`ot in`

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

- A collection in Python is a data type that holds multiple items, such as `lists`, `tuples`, `sets`, and `dictionaries`

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

- An `if...else` statement executes a block of code based on a condition, running one block if the condition is true and another if it's false
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

- A `loop` iterates over a sequence (such as a `list`, `tuple`, or `range`) and executes a specified block of code for each item in that sequence, one by one

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

- A function is a block of code which only runs when it is called. You can pass data, known as parameters, into a function
- A function can return data as a result
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


To start:
```python
import snowflake.snowpark as snowpark
from snowflake.snowpark.functions import col, count, avg
```
- This will import the needed packages and functions needed

<br>

```python
def python_queries(session: snowpark.Session):
```
- This line will create a function and pass the needed parameter
- Using `session: snowpark.Session` enables *type checking*, which:
  - Prevents Errors: If you accidentally pass an object of the wrong type, it can be flagged by your development environment (like an IDE or linter) before runtime.
  - Improves Debugging: You are explicitly specifying what kind of object the function expects, making errors easier to identify.

If you pass anything other than a `snowpark.Session` object, the code will fail since only `snowpark.Session` provides the methods (table, sql, etc.) used inside the function.

<br>

```python
tableName = 'FXRATE'
dataframe = session.table(tableName)
```
- Here we create two variables to determine:
  - The table name that will be used
  - Make sure that the table is using `session` so queries ca be used with Python

<br>

```python
starter = dataframe.select("base_currency", "rate_date", 'fx_rate_base_currency')
```
- This is the first query that we create
- It will `select` just 3 columns from all the ones available in the Dataframe (table)

<br>

```python
df = starter.filter(col("base_currency") == 'GBP')
```
- In here we are using the first query `starter` and adding a filter
- This filter will only show the rows that have `GBP` in the column `base_currency`

<br>

```python
df2 = starter.order_by('rate_date').limit(10000)
```
- This query is also using the `starter` query and ordering it by the column `rate_date`
- This will show only the first 10k first rows
- And it will be sorted in ascending order

<br>

```python
df3 = starter.group_by('base_currency', 'fx_rate_base_currency').agg(count("*").alias("row_count"))
```
- This query, also using `starter`, groups 2 columns: `base_currency` and `fx_rate_base_currency`
- Then aggregates the data from both columns by counting the number of rows in each group and labels the count as `row_count`
- This query provides the count of rows for each unique combination of `base_currency` and `fx_rate_base_currency`

<br>

Next we will create 2 charts with Python
>Remember: Snowflake cannot generate charts under 1M rows, also any `limit` above 10k it takes ages to load
```python
line_chart = df.group_by("rate_date").agg(avg("fx_rate_base_currency").alias("avg_rate")).sort("rate_date").limit(1000)
```
- This query is using the `df` query (filtering only `GBP` as our `base_currency`)
- Then it groups the `rate_date` column, so the data is organized by date
- It also aggregates the grouped data by calculating the average of `fx_rate_base_currency` for each date and renames the resulting column as `avg_rate`
- It then sorts the result in ascending order and limits the output to the first 1000 rows
- This will display a `Line Chart` after you run your code and change to the `Chart` tab and select `Line` in the Chart type box

<br>

```python
bar_chart = df.group_by("quote_currency").agg(count("*").alias("frequency")).sort(col("frequency"), ascending=False).limit(50)
```
- This query is using the `df` query (filtering only `GBP` as our `base_currency`)
- Then it groups the `quote_currency` column, organizing the data by each unique quote currency
- It will also aggregates the grouped data by counting the number of rows for each `quote_currency`, and labels the result as `frequency`
- And then sorts the result by the `frequency` column in descending order and limits the output to the top 50 rows to show the most frequent quote currencies
- This will display a `Bar Chart` after you run your code and change to the `Chart` tab and select `Bar` in the Chart type box
- Make sure that you change the Y-Axis to `quote_currency` in the `Chart` tab

<br>

```python
dataframe.show()
```
- To see all the above, firstly you should use this code and show the entire table (you will see all columns and how many rows it has)

<br>

```python
starter.show()
```
- Then you can change it for each query (e.g. `df.show()`, `bar_chart.show()`)

<br>

```python
return dataframe
```
- Because we are using Python, we must return something
- The something is which query name you are using with the `show()` method (e.g. `return df3`, `return line_chart.show()`)

<br>

Now we'll do exactly the same but with **SQL** inside a Python function

```python
def sql_queries(session: snowpark.Session):
```
- First we create a function for our SQL queries and pass the needed parameters

<br>

```python
select_all = session.sql("SELECT * FROM fxrate WHERE base_currency = 'GBP' LIMIT 10000")
```
- To use SQL queries, we don't need to create variables with the table name
- This query selects all columns from the `fxrate` table where `base_currency` is `GBP` and limits the result to the first 10k rows

- Why use `session.sql()`?
  - The `session.sql()` method allows you to directly execute raw *SQL* queries in Snowflake
  - In this case, you're bypassing the Snowpark API and using Snowflake SQL to query the data directly
  - Snowflake executes the SQL query and returns the results as a Snowpark DataFrame

<br>

```python
select_dist = session.sql("SELECT DISTINCT base_currency FROM fxrate")
```
- This query will select only the unique values from the `base_currency` column, eliminating any duplicates
- The `DISTINCT` keyword is used to return only unique values

<br>

```python
select_from = session.sql("SELECT base_currency, COUNT(*) AS count FROM fxrate GROUP BY base_currency ORDER BY count DESC")
```
- This query selects the `base_currency` column and calculates the count of rows for each unique `base_currency`, labeling the result as `count`
- The results are grouped by `base_currency` and then sorted by the `count` in descending order to show the most frequent base currencies first
- Mainly this query finds the number of rows for each base currency

<br>

```python
select_where = session.sql("SELECT * FROM fxrate WHERE rate_date BETWEEN '2024-01-01' AND '2024-01-31'")
```
- This query is selecting all columns from the `fxrate` table
- Then filters the rows where the `rate_date` fall within the date range from 1 Jan 2024 to 31 Jan 2024

<br>

Now we will create 2 charts with SQL queries
>Remember: Snowflake cannot generate charts under 1M rows, also any `limit` above 10k it takes ages to load
```python
scatter_chart = session.sql("SELECT fx_rate_base_currency, fx_rate_quote_currency FROM fxrate WHERE base_currency = 'GBP' AND fx_rate_base_currency > 0.5 AND fx_rate_quote_currency > 0.5 LIMIT 10000")
```
- This query selects the `fx_rate_base_currency` and `fx_rate_quote_currency` columns from `fxrate` table
- Then filters the rows where `base_currency` is `GBP`, and both `fx_rate_base_currency` and `fx_rate_quote_currency` are greater than 0.5, limiting the result to the first 10k rows
- This will display a `Scatter Plot Chart` after you run your code and change to the `Chart` tab and select `Scatter` in the Chart type box

<br>

```python
heatgrid_chart = session.sql("SELECT base_currency, quote_currency, COUNT(*) AS frequency FROM fxrate GROUP BY base_currency, quote_currency ORDER BY frequency DESC LIMIT 10000")
```
- This query selects the `base_currency`, `quote_currency`, and counts the occurrences of each unique combination, labeling the count as `frequency`
- Then groups the results by `base_currency` and `quote_currency`, ordering them by the `frequency` in descending order, and limits the result to the first 10k rows
- This will display a `Heatgrid Chart` after you run your code and change to the `Chart` tab and select `Heatgrid` in the Chart type box

<br>

As before, to see all the above displayed you must use:
```python
result.show()

return result
```
- You can change the variable according to the query you want to display (e.g. `select_where.show()`, `return select_where`)

<br>

Lastly you need a `main` function to use Snowpark and call the other functions

```python
def main(session: snowpark.Session):
```
- Here we create the `main` function passing the needed parameter
- If we don't have a main function, snowflake will raise an error

<br>

```python
python_result = python_queries(session)
```
- Here create a variable called `python_result`
- Then we assign the Python queries function to it and pass the `session` argument
- We need to pass `session` as an argument because it establishes the connection to Snowflake, allowing the function to interact with the database

<br>

```python
sql_result = sql_queries(session)
```
- Here we do the same for our SQL function
- Also passing `session` as an argument

<br>

```python
return python_result
```
- Finally we need to return one of the variables that we create above
- You can keep change between `python_result` and `sql_result` to visualise the queries from both

<br>

---