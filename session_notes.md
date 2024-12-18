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
2. Explain that we're going to utilise something called a **Notebook** within a piece of software called **Snowflake** that allows users to store, access, and exchange data.
   It is a cloud-based data platform that provides solutions for data warehousing, data lake management, data engineering, data sharing, and business intelligence.
   It allows organizations to store and analyze large volumes of structured and semi-structured data using a scalable and secure architecture.
4. We'll build the Notebook collaboratively over the course of the session and, by the end, will have a set of shareable notes going through everything that we've covered.
5. **Insert** visuals that are where we're going to get to
6. **Open** Snowflake and log-in
7. **Navigate** to `Notebooks` tab > `Go to Notebooks` > `+ Notebook`
8. **Connect** to database on pop-up **CHECK**
9. **Explain** next steps:
   - You should be able to see three **cells** - these are essentially mini-tutorials but this session will cover many of these points so we're not going to use these for now
   - **Delete** `Cells 2 and 3` from the notebook (with the SQL commands and Panda dataframe)
   - **Leave** `Cell 1` - we're going to talk through that now...
10. **Explain** what they can see in `Cell 1`
   - It is written in **Python**
   - Some **libraries** are `imported` at the top of the cell. A **library** is a collection of code that can make everyday tasks more efficient
   - Explain that, later on, we're going to be using a library called `Matplotlib` to help us do some visualisations
   - Transfer your attention to **line 7** which intoduces **Snowpark**
   - Explain that **Snowpark** is a developer framework provided by Snowflake, enabling users to write data pipelines, data transformations, and other complex operations in Python, Java, or Scala directly within Snowflake
   - So `Cell 1` is setting things up so that we can use **Python** within this session

### Python Basics
