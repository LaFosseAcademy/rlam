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

- Use Snowflake

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
from snowflake.snowpark.functions import col
```
- This will import the needed packages and functions needed

We'll also need to import other functions to use later on
```python
from snowflake.snowpark.functions import col, avg, date_trunc, round, count
```

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
starter = session.sql()
```
- Here we'll start with SQL, to trim our database
- Why use `session.sql()`?
  - The `session.sql()` method allows you to directly execute raw *SQL* queries in Snowflake
  - In this case, you're bypassing the Snowpark API and using Snowflake SQL to query the data directly
  - Snowflake executes the SQL query and returns the results as a Snowpark DataFrame

<br>

```python
starter = session.sql("SELECT * FROM fxrate")
```
- The first SQL query that we'll use is select
- In this instance we are `selecting` all columns and rows
- This is important to start the trimming

<br>

```python
starter.show()

return starter
```
- This two commands will show the results from the above query

<br>

Now that we now all the columns that we have available, we can improve our SQL query
```python
starter = session.sql("""
  SELECT base_currency, currency_pair, fx_rate_base_currency, quote_currency, rate_date,
  FROM fxrate
""")
```
- In here we are `selecting` only the columns that we will need
- We also need to inform SQL from which table these columns are coming from `FROM fxrate`
- We are using `"""` to have our SQL queries in different lines, so the code looks clean and easy to read
- Run the query again to show the new query

<br>

```python
WHERE currency_pair = 'USDGBP'
```
- After `FROM` we can add `WHERE` to limit our results
- Here we want to see only exchanges between `USD` and `GBP`
- For that we use the keyword `WHERE` followed by the column name `currency_pair` and the currency `USDGBP`

<br>

```python
AND rate_date
BETWEEN '2024-01-01' AND '2024-01-31'
```
- After `WHERE` we use another SQL keywords `AND` & `BETWEEN`
- This keywords combined improve our results
- With those we can check the column `rate_date` and select specific dates for our analysis

<br>

Complete SQL query
```python
starter = session.sql("""
    SELECT base_currency, currency_pair, fx_rate_base_currency, quote_currency, rate_date,
    FROM fxrate
    WHERE currency_pair = 'USDGBP'
    AND rate_date 
    BETWEEN '2024-01-01' AND '2024-01-31'
""")
```
- Run this code again to see the result

<br>

Now that we trimmed our table, let's do some further analysis with Python
- For this first analysis, we need to change our SQL query:
```python
starter = session.sql("""
    SELECT base_currency, currency_pair, fx_rate_base_currency, quote_currency, rate_date,
    FROM fxrate
""")
```

<br>

The first analysis is to see the `most frequent currency against which base currency is measured`
```python
quote_curr = (
    starter
    .group_by('quote_currency')
)
```
- First we create a variable `quote_curr`
- Then we use our SQL variable `starter`
- For Python queries we will use some of the methods that Snowflake has available
- In this case it will be `group_by`, then we pass which column we want to group `quote_currency`

<br>

```python
.agg(count('*').alias('frequency'))
```
- After `group_by`, we use `agg` and `count` 
- `count` is a Snowpark function that was imported in the second line
- `count` will count all `'*'` `quote_currency` and will aggregate all of them
- Then we create an `alias` called `frequency`, that will became a new column with the `agg()` values

<br>

```python
.sort(col('frequency'), ascending=False)
```
- Finally we use the `sort` method
- We want to sort our `col` (another Snowpark function) `frequency`
- And we want it to show from the most `quote_currency` used to the least (`ascending=False`)

<br>

Complete query
```python
quote_curr = (
    starter
    .group_by('quote_currency')
    .agg(count('*').alias('frequency'))
    .sort(col('frequency'), ascending=False)
)
```

<br>

To see the results, use:
```python
quote_curr.show()

return quote_curr
```
- `.show()` must be used when quoting with Python, otherwise you'll get an error about not returning a DataFrame

<br>

- Move to the `Chart` tab
- Select `Bar` as the Chart type
- Under `Data`
  - First drop down: `FREQUENCY`
  - Second drop down (Y-Axis): `QUOTE_CURRENCY`
- Under `Appearance`
  - Orientation: first option
  - Order bars by: `Bar size`
  - Order direction: `Descending`
  - Series direction: `Descending`


In this `Chart` we can see that the most used currency is `XAU`

<br>

---

<br>

The second analysis is to see the `rate of exchange between GBP and USD across a month`

For this analysis, we'll need the entire SQL query
```python
starter = session.sql("""
    SELECT base_currency, currency_pair, fx_rate_base_currency, quote_currency, rate_date,
    FROM fxrate
    WHERE currency_pair = 'USDGBP'
    AND rate_date 
    BETWEEN '2024-01-01' AND '2024-01-31'
""")
```

<br>

```python
daily_avg = (
    starter
    .select(
        col('base_currency'),
        col('currency_pair'),
        col('fx_rate_base_currency'),
        date_trunc('DAY', col('rate_date')).alias('rate_day')
    )
)
```
- We create a new variable `daily_avg`
- Then we use our SQL query `starter` and use the `select` method
- For this query we are `selecting` three columns: `base_currency`, `currency_pair` and `fx_rate_base_currency`
- Make sure to use the `col` function, so Python (Snowpark) knows that we are referencing columns
- Then we use another Snowpark function called `date_trunc`
- `date_trunc` is commonly used for grouping data by specific date units, in this case we want to group by `DAY`
- We use `DAY` because there is many occurrences throughout the day and we want to make sure it only shows one day at the time
- Then we pass from which column this date is coming from `col('rate_date')`
- Finally we use an `alias` to make it simple to understand: `rate_day`

<br>

```python
.group_by("base_currency", "currency_pair", "rate_day")
```
- Here we are using `group_by`, which organizes the data into groups based on these specified columns

<br>

```python
.agg(round(avg("fx_rate_base_currency"), 3).alias("daily_avg_rate"))
```
- This query performs an aggregation on the grouped data to calculate the average of the `fx_rate_base_currency` column for each group
- The `round()` Snowpark function ensures the average value is rounded to 3 decimal places for precision
- And the resulting column is renamed to `daily_avg_rate` using the alias method

<br>

```python
.sort("rate_day")
```
- Finally we use the `sort` method to show our results in ascending order

<br>

Complete query
```python
daily_avg = (
    starter
    .select(
        col('base_currency'),
        col('currency_pair'),
        col('fx_rate_base_currency'),
        date_trunc('DAY', col('rate_date')).alias('rate_day')
    )
    .group_by("base_currency", "currency_pair", "rate_day")
    .agg(round(avg("fx_rate_base_currency"), 3).alias("daily_avg_rate"))
    .sort("rate_day")
)
```

<br>

To see the results, use:
```python
daily_avg.show()

return daily_avg
```

- Move to the `Chart` tab
- Select `Line` as the Chart type
- Under `Data`
  - First drop down: `DAILY_AVG_RATE` - select average under
  - Second drop down (X-Axis): `RATE_DAY` - select none under
- Under `Appearance`, check:
  - Label X-Axis
  - Label Y-Axis
  - Crop Y Axis
- Increase the size of the chart if needed by dragging the tab up


In this `Chart` we can see how the rate `USDGBP` fluctuate during the month of January

<br>

---

<br>

The third analysis is to see the `performance of the USD against other currencies`

For this analysis, we'll need this SQL query
```python
starter = session.sql("""
    SELECT base_currency, currency_pair, fx_rate_base_currency, quote_currency, rate_date,
    FROM fxrate
""")
```

<br>

```python
usd_against = (
    starter
    .select(
        col('base_currency'),
        col('quote_currency'),
        col('fx_rate_base_currency'),
        date_trunc('DAY', col('rate_date')).alias('rate_day')
    )
)
```
- As before we create a variable `usd_against`, use our SQL query `starter` and then `select()` the columns we want to use
- Here we use `date_trunc` again for grouping the data by `DAY`
- We use `DAY` because there is many occurrences throughout the day and we want to make sure it only shows one day at the time

<br>

```python
.where(
    (col('base_currency') == 'USD') 
    & ((col('quote_currency') == 'EUR') 
    | (col('quote_currency') == 'GBP')
    | (col('quote_currency') == 'IEP')
    | (col('quote_currency') == 'CHF'))
) 
```
- This `where` condition filters rows in the DataFrame based on these criteria:
  - It selects the `base_currency` column and the base is `USD`
  - The condition uses the `&` operator for logical "AND" between `base_currency` and the combined conditions for `quote_currency`
    - This means that we want the `base_currency` AND something else (in this case `quote_currency`)
  - The `|` operator is used for logical "OR" to allow any of the three specified `quote_currency` values
- Mainly this query is used to extract data for `USD` currency conversions specifically to `EUR` (Euro), `GBP` (Pounds), `IEP` (Irish Pounds), and `CHF` (Swiss Franc)

<br>

```python
.group_by('base_currency', 'quote_currency', 'rate_day')
```
- This is grouping the columns that we want to be displayed

<br>

```python
agg(round(avg('fx_rate_base_currency'), 3).alias('avg_rate'))
```
- Here the `agg()` function is used to perform aggregation on the specified column `fx_rate_base_currency`
- Then it calculates the average (`avg()`) of the `fx_rate_base_currency` values
- The result is rounded to 3 decimal places using `round()` and is given an alias of `avg_rate`

<br>

```python
.sort("rate_day")
```
- Finally we use the `sort` method to show our results in ascending order

<br>

Complete query
```python
usd_against = (
    starter
    .select(
        col('base_currency'),
        col('quote_currency'),
        col('fx_rate_base_currency'),
        date_trunc('DAY', col('rate_date')).alias('rate_day')
    )
    .where(
        (col('base_currency') == 'USD') 
        & ((col('quote_currency') == 'EUR') 
        | (col('quote_currency') == 'GBP')
        | (col('quote_currency') == 'IEP')
        | (col('quote_currency') == 'CHF'))
    ) 
    .group_by('base_currency', 'quote_currency', 'rate_day')
    .agg(round(avg('fx_rate_base_currency'), 3).alias('avg_rate'))
    .sort("rate_day")
)
```

<br>

To see the results, use:
```python
usd_against.show()

return usd_against
```

- Move to the `Chart` tab
- Select `Line` as the Chart type
- Under `Data`
  - First drop down: `AVG_RATE` - select average
  - Second drop down (Series): `QUOTE_CURRENCY` (if you cannot see it, just add a new column)
  - Third drop down (X-axis): `RATE_DAY` - none
- Under `Appearance`, check:
  - Show Legend
  - Label X-Axis
  - Label Y-Axis
  - Crop Y Axis
- Increase the size of the chart if needed by dragging the tab up

In this `Chart` we can see the quote values of USD against EUR, GBP, IEP, and CHF from 2022 to 2024.

<br>

---

<br>

In case Matplotlib is required, here are some notes

- Use GitHub [Codespace](https://github.com/codespaces)
- Create a new Jupyter Notebook
- In the codespace:
  - Create a new file with the extension `ipynb` inside the `notebooks` folder
- Select `+ Code` to create a new cell to code

<br>


```python
import matplotlib.pyplot as plt
```
- Import Matplotlib
- Run the cell with `shift + enter`
- This will open a tab to select an environment
  - Select `Python 3.12.1`
- Run the cell again

<br>

```python
days = [1, 2, 3, 4, 5, 8, 9, 10, 11, 12]
avg_rate = [0.783, 0.791, 0.79, 0.786, 0.783, 0.783, 0.786, 0.784, 0.786, 0.783]
```
- Create dummy data from the original database
- This is 2 weeks (excluding weekends) of average rate between USD & GBP

<br>

```python
plt.figure(figsize=(8, 5))
```
- Using `plt` (Matplotlib alias) we can start creating a graph
- This creates a figure with a size of 8 inches wide and 5 inches tall

<br>

```python
plt.plot(days, avg_rate, marker='o', color='darkorange')
```
- This line plots a line graph of `avg_rate` against days with orange circles marking each data point
- In Matplotlib, the `plt.plot()` function creates a line chart by default because it is designed to connect the data points sequentially with straight lines unless specified otherwise
- If type of chart are needed, it would be necessary to specify it explicitly, such as using `plt.scatter()` for a scatter plot or `plt.bar()` for a bar chart

<br>

```python
plt.title('Daily Avg Rate USDGBP')
plt.xlabel('Day')
plt.ylabel('Daily Avg Rate')
```
- Here we are giving the graph a title and labels for each axis

<br>

```python
plt.grid()
```
- This line adds a grid to the plot for better visualization of data points

<br>

```python
plt.show()
```
- Finally, to display the plot we use `.show()`


Complete code:
```python
import matplotlib.pyplot as plt

days = [1, 2, 3, 4, 5, 8, 9, 10, 11, 12]
avg_rate = [0.783, 0.791, 0.79, 0.786, 0.783, 0.783, 0.786, 0.784, 0.786, 0.783]

plt.figure(figsize=(8, 5))
plt.plot(days, avg_rate, marker='o', color='darkorange')
plt.title('Daily Avg Rate USDGBP')
plt.xlabel('Day')
plt.ylabel('Daily Avg Rate')

plt.grid()
plt.show()
```

<br>

---

<br>

Another graph that we can create is:

```python
quote_curr = ['XAU', 'FRF', 'MTL', 'FIM', 'EUR', 'DEM', 'IEP', 'SKK', 'NLG', 'LVL']
frequency = [33842, 33148, 33146, 33146, 33146, 33146, 33142, 33134, 33132, 33130]
```
- Using the quote currency and it's frequency (top 10)

<br>

```python
plt.figure(figsize=(10, 5))
```
- This line creates a figure with a size of 10 inches wide and 5 inches tall

<br>

```python
plt.bar(quote_curr, frequency, color='seagreen', edgecolor='black', linewidth=0.5, width=0.7)
```
- Here it is draw a bar chart with green bars (`color='seagreen'`), black borders (`edgecolor='black'`), thin border lines (`linewidth=0.5`), and a width of 0.7 (`width=0.7`)
- You can play around it with to show the changes

<br>

```python
plt.title('10 Top Quote Currency Frequency', fontsize=14, fontweight='bold')
```
- This line sets the chart title with bold text and font size 14

<br>

```python
plt.xlabel('Quote Currency', fontsize=12)
plt.ylabel('Frequency', fontsize=12)
```
- Here we set the labels the `x-axis` as "Quote Currency" and the `y-axis` as "Frequency" with a font size of 12

<br>

```python
plt.grid(axis='y', linestyle='-', alpha=0.1)
```
- This line adds a light grid with solid lines along the `y-axis` for better readability
- You can also change the `linestyle` and the `alpha` to show the differences

<br>

```python
plt.xticks(rotation=45)
```
- `xticks` is a Matplotlib function used to customize the placement, labels, and rotation of the ticks on the `x-axis`
- And here it rotates the `x-axis` labels by 45 degrees to improve visibility

<br>

```python
plt.show()
```
- Finally, to display the plot we use `.show()`


Complete code:
```python
quote_curr = ['XAU', 'FRF', 'MTL', 'FIM', 'EUR', 'DEM', 'IEP', 'SKK', 'NLG', 'LVL']
frequency = [33842, 33148, 33146, 33146, 33146, 33146, 33142, 33134, 33132, 33130]

plt.figure(figsize=(10, 5))
plt.bar(quote_curr, frequency, color='seagreen', edgecolor='black', linewidth=0.5, width=0.7)
plt.title('10 Top Quote Currency Frequency', fontsize=14, fontweight='bold')
plt.xlabel('Quote Currency', fontsize=12)
plt.ylabel('Frequency', fontsize=12)

plt.grid(axis='y', linestyle='-', alpha=0.1)
plt.xticks(rotation=45)

plt.show()
```

<br>

---

<br>

And finally we can create this other graph:

```python
months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
EUR = [0.98, 0.912, 0.902, 0.912, 0.896, 0.929]
GBP = [0.964, 0.901, 0.876, 0.861, 0.824, 0.89]
IEP = [0.837, 0.811, 0.799, 0.788, 0.783, 0.802]
CHF = [0.772, 0.719, 0.71, 0.716, 0.706, 0.731]
```
- For this graph we'll compare `USD` aginst other 4 currencies over the period of 6 months
- The currency value is the average for each month

<br>

```python
plt.figure(figsize=(12, 6))
```
- We start by creating a figure with dimensions of 12 inches wide and 6 inches tall

<br>

```python
plt.plot(months, EUR, marker='o', label='Euro', color='royalblue')
plt.plot(months, GBP, marker='s', label='British Pound', color='mediumseagreen')
plt.plot(months, IEP, marker='d', label='Irish Pound', color='darkred')
plt.plot(months, CHF, marker='^', label='Swiss Franc', color='mediumpurple')
```
- In this 4 lines we are ploting lines:
  - For the Euro with circular markers and a blue color
  - For the British Pound with square markers and a green color
  - For the Irish Pound with diamond markers and a dark red color
  - For the Swiss Franc with triangle markers and a purple color

<br>

```python
plt.title('Average Monetary Rates Against USD (Half Year)', fontsize=16, fontweight='bold')
```
- Here it's adding a bold title to the chart with font size 16

<br>

```python
plt.xlabel('Month', fontsize=12)
plt.ylabel('Average Rate', fontsize=12)
```
- These lines are setting the labels for the `x-axis` as "Month" and the `y-axis` as "Average Rate" with a font size of 12

<br>

```python
plt.legend(title='Currencies', fontsize=10)
```
- Here adds a legend with the title "Currencies" and a font size of 10
- The `.legend()` function in Matplotlib adds a legend to the plot, displaying labels for each plotted data series to improve interpretability

<br>

```python
plt.grid(axis='y', linestyle='--', alpha=0.7)
```
- These adds a dashed grid along the y-axis with 70% opacity for better readability

<br>

```python
plt.show()
```
- Finally, to display the plot we use `.show()`


Complete code:
```python
months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
EUR = [0.98, 0.912, 0.902, 0.912, 0.896, 0.929]
GBP = [0.964, 0.901, 0.876, 0.861, 0.824, 0.89]
IEP = [0.837, 0.811, 0.799, 0.788, 0.783, 0.802]
CHF = [0.772, 0.719, 0.71, 0.716, 0.706, 0.731]

plt.figure(figsize=(12, 6))

plt.plot(months, EUR, marker='o', label='Euro', color='royalblue')
plt.plot(months, GBP, marker='s', label='Gritish Pound', color='mediumseagreen')
plt.plot(months, IEP, marker='d', label='Irish Pound', color='darkred')
plt.plot(months, CHF, marker='^', label='Swiss Franc', color='mediumpurple')

plt.title('Average Monetary Rates Against USD (Half Year)', fontsize=16, fontweight='bold')
plt.xlabel('Month', fontsize=12)
plt.ylabel('Average Rate', fontsize=12)
plt.legend(title='Currencies', fontsize=10)
plt.grid(axis='y', linestyle='--', alpha=0.7)

plt.show()
```