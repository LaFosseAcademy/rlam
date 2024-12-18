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
3. Introduction to Snowflake and Snowpark
4. Loading Data using SQL
5. Analysing Data using Python
6. Data Visualisation

### Introduction

1. Welcome to the session. Explain that, by the end of the session you should be able to:
   - Access data using Snowflake
   - Perform queries on that data
   - Visualise that data
2. **Explain** that we're going to utilise something called a **Notebook** within a piece of software called **Snowflake** that allows users to store, access, and exchange data. It is a cloud-based data platform that provides solutions for data warehousing, data lake management, data engineering, data sharing, and business intelligence. It allows organizations to store and analyze large volumes of structured and semi-structured data using a scalable and secure architecture.
3. **Highlight** that the session is designed to be a code-along - you should be able to type out most commands, but I'll share any long ones in the chat
4. We'll build the Notebook collaboratively over the course of the session and, by the end, will have a set of shareable notes going through everything that we've covered
5. **Insert** visuals that are where we're going to get to
6. **Open** Snowflake and log-in
7. **Navigate** to `Notebooks` tab > `Go to Notebooks` > `+ Notebook`
8. **Connect** to database on pop-up **CHECK**
9. **Explain** next steps:
   - You should be able to see three **cells** - these are essentially mini-tutorials but this session will cover many of these points so we're not going to use these for now
   - **Delete** `Cells 2 and 3` from the notebook (with the SQL commands and Panda dataframe)
   - **Leave** `Cell 1` - we're going to talk through that now...
10. **Explain** what they can see in `Cell 1`:
      - It is written in **Python**
      - Some **libraries** are `imported` at the top of the cell. A **library** is a collection of code that can make everyday tasks more efficient
      - Explain that, later on, we're going to be using a library called `Matplotlib` to help us do some visualisations
      - Transfer your attention to **line 7** which intoduces **Snowpark**
      - Explain that **Snowpark** is a developer framework provided by Snowflake, enabling users to write data pipelines, data transformations, and other complex operations in Python, Java, or Scala directly within Snowflake
      - So `Cell 1` is setting things up so that we can use **Python** within this session

### Python Basics

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
print(z[1]
```
11. **Congratulate** the volunteer that points out that it returns `banana` and explain that this is because, when we code - we start counting from 0
12. **Explain** that we can do all sorts of things with data types - in fact we could just spend two hours right here doing them, but we're going to look at `strings` in particular...

### Python Basics - Strings

### Python Basics - String Methods

### Python Basics - Functions

