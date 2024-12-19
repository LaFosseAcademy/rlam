# RLAM - Training Session

## Overview
This course has been designed to give RLAM employees an overview of Python and how it
can be used with Snowflake to sort, analyse, and visualise data. By the end of the session,
trainees should be able to access data using Snowflake and perform queries on that data
which enable them to effectively work with the data set. They should also be able to use the
Charts functionality on Snowflake to visualise that data. Finally, they will be able to use
Matplotlib to refine their visualisations.

1. Introduction
2. Python Basics
3. Loading Data using SQL
4. Analysing Data using Python
5. Data Visualisation

## Introduction

1. Welcome to the session. Explain that, by the end of the session you should be able to:
   - Access data using Snowflake
   - Perform queries on that data
   - Visualise that data
2. **Explain** that we're going to utilise something called a **Notebook** within a piece of software called **Snowflake** that allows users to store, access, and exchange data. It is a cloud-based data platform that provides solutions for data warehousing, data lake management, data engineering, data sharing, and business intelligence. It allows organizations to store and analyze large volumes of structured and semi-structured data using a scalable and secure architecture.
3. **Highlight** that the session is designed to be a code-along - you should be able to type out most commands, but I'll share any long ones in the chat
4. We'll build the Notebook collaboratively over the course of the session and, by the end, will have a set of shareable notes going through everything that we've covered
5. **Insert** visuals that are where we're going to get to **TO COMPLETE**

   **Explain** that, in the session, we're going to look to create three visuals:
   - Analysing the most frequent currency against which base currency is measured
   - Analysing the rate of exchange between GBP and USD across a month
   - Analysis of the performance of the USD against four other currencies between 2022-24 
7. **Open** Snowflake and log-in
8. **Navigate** to `Notebooks` tab > `Go to Notebooks` > `+ Notebook`
9. **Double check** that trainees can see a list of accessible databases on the left-hand panel
10. **Explain** next steps:
   - You should be able to see three **cells** - these are essentially mini-tutorials but this session will cover many of these points so we're not going to use these for now
   - **Delete** `Cells 2 and 3` from the notebook (with the SQL commands and Panda dataframe)
   - **Leave** `Cell 1` - we're going to talk through that now...
11. **Explain** what they can see in `Cell 1`:
      - It is written in **Python**
      - Some **libraries** are `imported` at the top of the cell. A **library** is a collection of code that can make everyday tasks more efficient
      - Explain that, later on, we're going to be using a library called `Matplotlib` to help us do some visualisations
      - Transfer your attention to **line 7** which intoduces **Snowpark**
      - Explain that **Snowpark** is a developer framework provided by Snowflake, enabling users to write data pipelines, data transformations, and other complex operations in Python, Java, or Scala directly within Snowflake
      - So `Cell 1` is setting things up so that we can use **Python** within this session

## Python Basics

1. **Explain** that, in order, to be able to work with the data that we have available to us, we're going to need to learn some Python
2. Get the unsaid question out of the way - yes, it is named after **Monty Python**
3. **Explain** that it's a simple to use programming language that can:
   - be used to create web applications
   - be used to connect to database systems
   - be used to handle big data and perform complex mathematics
4. All in all - it's useful for the sorts of things that we're going to want to do in Snowflake
5. **Create** the following cell:
```
# Zen of Python
import this
```
   - **Explain** that the `#` indicates a note - we'll be using these throughout the session, so that you are able to remember what we are trying to illustrate in each section
   - **Run** the `import this` line
   - **Explain** that the resultant **Zen of Python** is a sort of 'code of conduct' for the way the language should be written
   - **Congratulate people** - they've just written their first line of code!
6. **Demonstrate** that you can 'collapse' cells by clicking **Display Options**
7. **Explain** that an alternative is to simply try all of these bits out in the same cell
8. **Remind** people that we will be sending out a completed **notebook** at the end of this session so if you want to clear this one, that's fine!

### Python Basics - Variables

1. **Explain** that a **variable** is just a named storage location that holds a value
2. **Explain** that you can then access the value by referencing the variable
3. **Create** the following cell:
```
# Variables
age = 5
name = 'Simon'
```
4. **Run** the `cell` - notice that nothing happens - we're going to need a key word:
```
# Variables
age = 5
name = 'Simon'
print(name, age)
```
5. **Ask** trainees to create **two** variables of their own and print them
6. **Ask** a volunteer to walk you through writing and printing two different variables

### Python Basics - Data Types

1. **Point out** that the numbers in the previous exercise did not use quotation marks, but the names did - why?
2. **Answer** these are examples of different data types
3. **Demonstrate** this by showing a new key word:
```
age = 5
name = 'Simon'
type(name)
```
4. **Highlight** that this returns a lot of information - the key piece (for now) is at the top though - `name` is a `string`
5. **Ask** trainees how they would check what data type age is?
6. **Congratulate** the volunteer that says:
```
age = 5
name = 'Simon'
type(age)
```
7. **Highlight** that this is an `integer`
8. **Explain** that we're going to do a few examples, I'll create the variable and you check it
9. **Type** each of the following, in turn and get a volunteer to check the data type:
   - `x = 3.14` should be a `float`
   - `y = True` should be a `bool`
   - `z = ['apple', 'banana', 'pear']` should be a `list`
10. **Ask** what happens if they type:
```
z = ['apple', 'banana', 'pear']
print(z[1])
```
11. **Congratulate** the volunteer that points out that it returns `banana` and explain that this is because, when we code - we start counting from 0
12. **Explain** that we can do all sorts of things with data types - in fact we could just spend two hours right here doing them, but we're going to look at `strings` in particular...

### Python Basics - Strings

1. **Remind** trainees that a `string` is a data type used to represent a sequence of characters, such as words or sentences
2. **Explain** that `strings` can be surrounded by '' or ""
3. **String Literals** are a fun way to play with strings and insert them into something else - this is a concept called **concatenation**
4. **Create** the following cell:
```
# String Literals
name = 'Elizabeth'
city = 'London'

print(f'I am {name}, and I live in {city}.')
```
5. **Point out** that these principles should start to give us a sense that we can change and alter things using Python

### Python Basics - String Methods

1. **Ask** trainees once again how to check the data type of a variable
2. **Congratulate** the volunteer who says `type(variable)`
3. **Create** the following cell:
```
# String Methods
name = 'indiana jones'
profession = 'archaeologist'
type(name)
```
4. **Highlight** the methods that appear on the screen and explain that these are all essentialy **mini built-in functions** that will give you certain information about the string
5. **Demonstrate** how you would use some of these methods:
```
# String Methods - Capitalize
name = 'indiana jones'
profession = 'archaeologist'
print(name.capitalize())
```
6. **Feign annoyance** that the `j` is not capitalised then demonstrate `Title`:
```
# String Methods - Title
name = 'indiana jones'
profession = 'archaeologist'
print(name.title())
```
7. **What about** if we want to find out how many of a certain letter are in `profession`?
```
# String Methods - Count
name = 'indiana jones'
profession = 'archaeologist'
print(profession.count('a'))
```
8. **Or** if I realised I was actually talking about my friend Matt Jones?
```
# String Methods - Replace
name = 'indiana jones'
profession = 'archaeologist'
print(name.replace('indiana', 'matt'))
```
9. **And** what if I wanted to make sure his name was capitalized in the same code block?
```
# Chaining Methods
name = 'indiana jones'
profession = 'archaeologist'
print(name.replace('indiana', 'matt').title())
```
10. **Challenge** trainees to use the `Index` method to find what position the 'o' is in the word `archaeologist`
11. **Congratulate** the person who comes up with:
```
# String Methods - Index
name = 'indiana jones'
profession = 'archaeologist'
print(profession.index('o'))
```
12. **Ask** what happens when we change the previous cell to use the `split` method?
13. **Congratulate** the volunteer that notices that we're manipulating the string and we've returned a `list`
```
# String Methods - Index
name = 'indiana jones'
profession = 'archaeologist'
print(profession.split('o'))
```
Should return:
`['archae', 'l', 'gist']`

### Python Basics - Functions

1. **Point out** that we've already established that `methods` are mini functions
2. **Of course**, not all functions are built in - sometimes we have to write our own
3. **Explain** that we're not going to spend a long time on functions, but we are going to look at some syntax
4. **Create** the following cell:
```
# Functions
def my_function():
  print('Hello from a function')

# To call this function
my_function()
```
5. **Explain** that `def` is a key word - it **defines** our function
6. **Explain** that we `call` the function at the end so that we can generate the result
7. **Explain** that we've used `print` in the example, but we could also `return` the output too
8. **Explain** that this would return (but not necessarily **display**) the output of the function
9. **Explain** that we can pass information into functions as **arguments**
10. **Create** the following cell:
```
# Functions
def my_function(lotrname):
  print(f'Hello {lotrname}!!')

my_function('Arwen')
my_function('Legolas')
my_function('Elrond')
```
11. **Explain** that we can also use Python's **Operators** to perform, say, maths within functions:
```
# Operators
a = 7
b = 3

def my_function():
   print(a * b)

my_function()
```
12. **Explain** that that's the end of our whistle-stop tour around Python. It's time to start applying some of our core knowledge to manipulate data...

## SQL

1. **Explain** that it's time to start working with some actual data
2. **Explain** that we're going to use some of their previous training first of all and utilise SQL to first connect to, and then check our data set
3. **Explain** that we're going to clear our Python - we don't need it for now
4. **Create** the following **SQL** cell which is going to **connect** our notebook to the database that we want to use - we're going to do this with the `USE SCHEMA` key term:
```
# Connecting the Database
USE SCHEMA TRAINING_ACCOUNT_DATA.DEV_SMNTC_LAYER_IBOR;
```
5. **Demonstrate** the fact that, we can run this command and we get a `Successful Execution` message
6. **Demonstrate** that we can now have a look at our data. **Create** a new **SQL** cell:
```
# Displaying the Data
SELECT * FROM FXRATE
```
7. **Talk** trainees through the data - focusing on the size of the set, the fact that some information appears to be more useful than other information etc.
8. **Explain** that, SQL is really useful to 'trim the fat' off big data sets in particular, so, what we're going to do is use it to get our data set trimmed down to something that we can work with more easily
9. **Remind** trainees that we're going to build 3 visuals:
   - Analysing the most frequent currency against which base currency is measured
   - Analysing the rate of exchange between GBP and USD across a month
   - Analysis of the performance of the USD against four other currencies between 2022-24

### SQL - VISUAL 1 - Analysing the most frequent currency against which base currency is measured
10. **Explain** that we're going to use the same cell that we did the `SELECT *` command in earlier. Walk trainees through the following, line-by-line:
```
# Displaying the Data - Narrowing our Search
SELECT base_currency, currency_pair, fx_rate_base_currency, quote_currency, rate_date,
FROM FXRATE
```

