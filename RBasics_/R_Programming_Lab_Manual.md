# R Programming Basics

**Author:** Joyce F. Jamile   
**For Educational Use Only** 

---

## Table of Contents

1. [Introduction](#introduction)
2. [Chapter 1: Getting Started with R](#chapter-1-getting-started-with-r)
3. [Chapter 2: R Fundamentals and Data Types](#chapter-2-r-fundamentals-and-data-types)
4. [Chapter 3: Working with Vectors](#chapter-3-working-with-vectors)
5. [Chapter 4: Matrices and Matrix Operations](#chapter-4-matrices-and-matrix-operations)
6. [Chapter 5: Arrays and Multi-Dimensional Data](#chapter-5-arrays-and-multi-dimensional-data)
7. [Chapter 6: Lists](#chapter-6-lists)
8. [Chapter 7: Data Frames](#chapter-7-data-frames)
9. [Comprehensive Exercises](#comprehensive-exercises)
10. [Solutions to Exercises](#solutions-to-exercises)
11. [References](#references)

---

## Introduction

### What is R?

R is a free, open-source programming language and software environment for statistical computing and graphics. Created in 1995 by Ross Ihaka and Robert Gentleman at the University of Auckland, R has become the de facto standard for statistical analysis, data science, and academic research (Chambers, 2020). The language is highly extensible through its package system, with 23973 contributed packages available on CRAN (Comprehensive R Archive Network) as of June 2026.

---

## Chapter 1: Getting Started with R

### 1.1 Understanding Objects and the Assignment Operator

In R, **everything is an object**. An object is a container that holds data, functions, or other information that R can work with. To create an object and give it a name, we use the **assignment operator** `<-`.

The assignment operator `<-` points from right to left:
- The value on the right is stored in the name on the left
- Read it as "gets" or "is assigned"

Another assignment operator which is `=`, however `=` operator is commonly used to specify  function arguments.
```r
  mean(x = c(1,2,3))
```
Here `x` is the argument name of the `mean()` function

#### Example 1.1

```r
# Create some objects
num1 <- 10
num2 <- 20
name <- "Alice"
result <- num1 + num2

# Display the objects
num1
```

**Expected Output:**
```
[1] 10
```

```r
name
```

**Expected Output:**
```
[1] "Alice"
```

```r
result
```

**Expected Output:**
```
[1] 30
```

**Key Observations:**
- `<-` creates an object and assigns a value
- Variable names are case-sensitive `(num1 ≠ Num1)`
- The `#` symbol creates comments (ignored by R)
- `[1]` indicates the first element of output
- `=` is used to specify function arguments

---

### 1.2 The R Console and Basic Interaction

The **R Console** is your primary interface with R. It processes commands immediately and displays results.

#### Example 1.2: Console Basics

```r
# Simple arithmetic
7 * 9
```

**Expected Output:**
```
[1] 63
```

```r
# Incomplete command - R waits for input
5 *
# You would then type: 
# 4
# Result:
[1] 20
```

```r
# Multiple commands
x <- 15
y <- 3
x / y
```

**Expected Output:**
```
[1] 5
```

---

### 1.3 Basic Arithmetic Operations

R supports all standard arithmetic operations. The order of operations (PEMDAS/BODMAS) applies.

| Operation | Operator | Example | Result |
|-----------|----------|---------|--------|
| Addition | `+` | `5 + 3` | `8` |
| Subtraction | `-` | `5 - 3` | `2` |
| Multiplication | `*` | `5 * 3` | `15` |
| Division | `/` | `15 / 3` | `5` |
| Exponentiation | `^` or `**` | `2 ^ 3` | `8` |
| Integer Division | `%/%` | `7 %/% 3` | `2` |
| Modulus (Remainder) | `%%` | `7 %% 3` | `1` |

#### Example 1.3: Arithmetic Operations

```r
# Basic operations
5 + 3        # Addition
10 - 4       # Subtraction
6 * 7        # Multiplication
20 / 4       # Division
2 ^ 5        # Exponentiation
```

**Expected Output:**
```
[1] 8
[1] 6
[1] 42
[1] 5
[1] 32
```

```r
# Order of operations
2 + 3 * 4
```

**Expected Output:**
```
[1] 14
```

(Not 20, because multiplication happens before addition)

```r
# Modulus - returns the remainder
17 %% 5      # 17 divided by 5 is 3 remainder 2
```

**Expected Output:**
```
[1] 2
```

```r
# Storing results
area_of_circle <- pi * 5^2
area_of_circle
```

**Expected Output:**
```
[1] 78.53982
```

---

### 1.4 Working with Text and Strings

Text values, called **strings** or **character data**, must be enclosed in quotes (single or double).

#### Interactive Example 1.4: Text and Strings

```r
# Creating text objects
first_name <- "Robert"
last_name <- "Smith"
greeting <- "Welcome to R programming!"

# Display
first_name
```

**Expected Output:**
```
[1] "Robert"
```

```r
# Concatenating strings with paste()
# paste() adds a space between elements
full_name <- paste(first_name, last_name)
full_name
```

**Expected Output:**
```
[1] "Robert Smith"
```

```r
# paste0() concatenates without spaces
password <- paste0("user_", 2024)
password
```

**Expected Output:**
```
[1] "user_2024"
```

```r
# Creating more complex messages
message <- paste("Hello,", first_name, "! Welcome to", "R", "programming.")
message
```

**Expected Output:**
```
[1] "Hello, Robert ! Welcome to R programming."
```

---

### 1.5 Pre-defined Constants and Functions

R provides built-in constants and functions that are always available.

#### Interactive Example 1.5: Constants and Functions

```r
# Mathematical constant
pi
```

**Expected Output:**
```
[1] 3.141593
```

```r
# Logical values
TRUE
FALSE
T        # Shortcut for TRUE
F        # Shortcut for FALSE
```

**Expected Output:**
```
[1] TRUE
[1] FALSE
[1] TRUE
[1] FALSE
```

```r
# Built-in sequences
LETTERS    # Uppercase alphabet
```

**Expected Output:**
```
 [1] "A" "B" "C" "D" "E" "F" "G" "H" "I" "J" "K" "L" "M" "N" "O" "P" "Q" "R" "S"
[20] "T" "U" "V" "W" "X" "Y" "Z"
```

```r
letters    # Lowercase alphabet
```

**Expected Output:**
```
 [1] "a" "b" "c" "d" "e" "f" "g" "h" "i" "j" "k" "l" "m" "n" "o" "p" "q" "r" "s"
[20] "t" "u" "v" "w" "x" "y" "z"
```

```r
# Integer sequence
1:10
```

**Expected Output:**
```
 [1]  1  2  3  4  5  6  7  8  9 10
```

---

### 1.6 Getting Help in R

One of R's greatest strengths is its comprehensive help system.

```r
# Get help on a specific function
?seq
help(seq)          # Alternative syntax

# Get help on operators (use quotes)
?"+"
?"%in%"

# Search for functions related to a topic
??matrix           # Search documentation

# List all available functions in a package
library(help = base)

# Get examples
example(plot)
```

---

## Chapter 2: R Fundamentals and Data Types

### 2.1 Understanding Data Types

Every value in R has a **type**. Understanding data types is essential for writing correct programs.

R has five main data types:

| Data Type | Description | Example | R Output |
|-----------|-------------|---------|----------|
| Numeric | Real numbers (decimals) | `3.14`, `5.0`, `-2.5` | `[1] 3.14` |
| Integer | Whole numbers | `5L`, `10L`, `-3L` | `[1] 5` |
| Character | Text strings | `"hello"`, `'world'` | `[1] "hello"` |
| Logical | Boolean (TRUE/FALSE) | `TRUE`, `FALSE`, `T`, `F` | `[1] TRUE` |
| Complex | Complex numbers | `3+4i`, `5+2i` | `[1] 3+4i` |

#### Interactive Example 2.1: Data Types

```r
# Creating variables of different types
numeric_var <- 3.14159
integer_var <- 42L
character_var <- "Data Science"
logical_var <- TRUE
complex_var <- 3 + 4i

# Checking types
class(numeric_var)
```

**Expected Output:**
```
[1] "numeric"
```

```r
class(integer_var)
```

**Expected Output:**
```
[1] "integer"
```

```r
class(character_var)
```

**Expected Output:**
```
[1] "character"
```

```r
class(logical_var)
```

**Expected Output:**
```
[1] "logical"
```

```r
class(complex_var)
```

**Expected Output:**
```
[1] "complex"
```

```r
# Alternative: using typeof()
typeof(numeric_var)
```

**Expected Output:**
```
[1] "double"
```

---

### 2.2 Type Conversion

Sometimes you need to convert data from one type to another. R provides conversion functions.

#### IExample 2.2: Type Conversion

```r
# Convert numeric to character
num <- 2024
class(num)
```

**Expected Output:**
```
[1] "numeric"
```

```r
num_as_char <- as.character(num)
num_as_char
class(num_as_char)
```

**Expected Output:**
```
[1] "2024"
[1] "character"
```

```r
# Convert character to numeric
text_number <- "42"
class(text_number)
```

**Expected Output:**
```
[1] "character"
```

```r
converted <- as.numeric(text_number)
converted
class(converted)
```

**Expected Output:**
```
[1] 42
[1] "numeric"
```

```r
# Convert to logical
as.logical(1)        # Non-zero is TRUE
as.logical(0)        # Zero is FALSE
as.logical(NA)       # NA stays NA
```

**Expected Output:**
```
[1] TRUE
[1] FALSE
[1] NA
```

```r
# Convert to integer
as.integer(3.7)      # Truncates (removes decimal)
as.integer(3.2)
```

**Expected Output:**
```
[1] 3
[1] 3
```

---

### 2.3 Mathematical Functions

R provides many built-in mathematical functions for data analysis.

#### Interactive Example 2.3: Mathematical Functions

```r
# Basic statistics
data <- c(10, 20, 15, 30, 25)

min(data)            # Minimum value
```

**Expected Output:**
```
[1] 10
```

```r
max(data)            # Maximum value
```

**Expected Output:**
```
[1] 30
```

```r
mean(data)           # Average
```

**Expected Output:**
```
[1] 20
```

```r
median(data)         # Middle value
```

**Expected Output:**
```
[1] 20
```

```r
sum(data)            # Total
```

**Expected Output:**
```
[1] 100
```

```r
prod(data)           # Product (multiplication)
```

**Expected Output:**
```
[1] 112500000
```

```r
# More mathematical functions
sqrt(16)             # Square root
```

**Expected Output:**
```
[1] 4
```

```r
abs(-5)              # Absolute value
```

**Expected Output:**
```
[1] 5
```

```r
round(3.7)           # Round to nearest integer
floor(3.7)           # Round down
ceiling(3.2)         # Round up
```

**Expected Output:**
```
[1] 4
[1] 3
[1] 4
```

```r
# Logarithmic and exponential
log(10)              # Natural logarithm
log10(100)           # Base-10 logarithm
exp(1)               # e^1
```

**Expected Output:**
```
[1] 2.302585
[1] 2
[1] 2.718282
```

---

### 2.4 Logical Operations and Comparisons

Logical operations compare values and return TRUE or FALSE (Chambers, 2020).

#### Example 2.4: Comparisons and Logical Operations

```r
# Comparison operators
5 > 3                # Greater than
5 < 3                # Less than
5 == 5               # Equal to
5 != 3               # Not equal to
5 >= 5               # Greater than or equal
5 <= 5               # Less than or equal
```

**Expected Output:**
```
[1] TRUE
[1] FALSE
[1] TRUE
[1] TRUE
[1] TRUE
[1] TRUE
```

```r
# Logical operators
# & (AND) - both must be TRUE
(5 > 3) & (3 > 1)    # TRUE AND TRUE
```

**Expected Output:**
```
[1] TRUE
```

```r
(5 > 10) & (3 > 1)   # FALSE AND TRUE
```

**Expected Output:**
```
[1] FALSE
```

```r
# | (OR) - at least one must be TRUE
(5 > 10) | (3 > 1)   # FALSE OR TRUE
```

**Expected Output:**
```
[1] TRUE
```

```r
# ! (NOT) - negates the value
!(5 > 10)            # NOT FALSE = TRUE
```

**Expected Output:**
```
[1] TRUE
```

```r
# Complex expressions
x <- 15
(x > 10) & (x < 20)  # Is x between 10 and 20?
```

**Expected Output:**
```
[1] TRUE
```

```r
(x < 10) | (x > 20)  # Is x outside the 10-20 range?
```

**Expected Output:**
```
[1] FALSE
```

---

## Chapter 3: Working with Vectors

### 3.1 Creating Vectors

A **vector** is R's most basic data structure—a sequence of values of the same type. Even single numbers are vectors of length 1.

#### Example 3.1: Creating Vectors

```r
# Method 1: Using c() (combine or concatenate)
numbers <- c(2, 6, 8, 4, 2, 9, 4, 0)
numbers
```

**Expected Output:**
```
[1] 2 6 8 4 2 9 4 0
```

```r
# Character vector
cars <- c("volvo", "honda", "mazda", "lexus")
cars
```

**Expected Output:**
```
[1] "volvo" "honda" "mazda" "lexus"
```

```r
# Logical vector
flags <- c(TRUE, FALSE, TRUE, TRUE, FALSE)
flags
```

**Expected Output:**
```
[1]  TRUE FALSE  TRUE  TRUE FALSE
```

```r
# Method 2: Using the colon operator (:) for sequences
seq1 <- 1:10
seq1
```

**Expected Output:**
```
 [1]  1  2  3  4  5  6  7  8  9 10
```

```r
# Descending sequence
seq2 <- 10:1
seq2
```

**Expected Output:**
```
 [1] 10  9  8  7  6  5  4  3  2  1
```

```r
# With negative numbers
seq3 <- -3:3
seq3
```

**Expected Output:**
```
[1] -3 -2 -1  0  1  2  3
```

```r
# Method 3: Using seq() for custom sequences
seq(1, 10)           # Same as 1:10
```

**Expected Output:**
```
 [1]  1  2  3  4  5  6  7  8  9 10
```

```r
seq(1, 10, by = 2)   # Jump by 2
```

**Expected Output:**
```
[1] 1 3 5 7 9
```

```r
seq(0, 1, length = 5)  # 5 equally spaced values from 0 to 1
```

**Expected Output:**
```
[1] 0.00 0.25 0.50 0.75 1.00
```

```r
# Method 4: Using rep() to repeat values
rep(5, 4)            # Repeat 5 four times
```

**Expected Output:**
```
[1] 5 5 5 5
```

```r
rep(c("A", "B"), 3)  # Repeat a vector
```

**Expected Output:**
```
[1] "A" "B" "A" "B" "A" "B"
```

```r
rep(c("A", "B"), each = 2)  # Repeat each element
```

**Expected Output:**
```
[1] "A" "A" "B" "B"
```

---

### 3.2 Vector Properties

Every vector has properties we can inspect.

#### Example 3.2: Vector Properties

```r
# Create a sample vector
my_vector <- c(10, 20, 30, 40, 50)

# Length - number of elements
length(my_vector)
```

**Expected Output:**
```
[1] 5
```

```r
# Class - data type
class(my_vector)
```

**Expected Output:**
```
[1] "numeric"
```

```r
# Mode - storage mode
mode(my_vector)
```

**Expected Output:**
```
[1] "numeric"
```

```r
# Structure - detailed info
str(my_vector)
```

**Expected Output:**
```
 num [1:5] 10 20 30 40 50
```

---

### 3.3 Accessing Vector Elements

R uses **1-based indexing** (first element is 1, not 0). Access elements using square brackets `[]`.

#### Interactive Example 3.3: Indexing Vectors

```r
# Create a sample vector
scores <- c(85, 90, 78, 92, 88)

# Access single elements
scores[1]            # First element
```

**Expected Output:**
```
[1] 85
```

```r
scores[3]            # Third element
```

**Expected Output:**
```
[1] 78
```

```r
scores[5]            # Last element
```

**Expected Output:**
```
[1] 88
```

```r
# Access multiple elements
scores[c(1, 3, 5)]   # Elements at positions 1, 3, 5
```

**Expected Output:**
```
[1] 85 78 88
```

```r
# Access a range
scores[2:4]          # Elements 2 through 4
```

**Expected Output:**
```
[1] 90 78 92
```

```r
# Negative indexing - exclude elements
scores[-2]           # All except element 2
```

**Expected Output:**
```
[1] 85 78 92 88
```

```r
scores[-c(2, 4)]     # Exclude elements 2 and 4
```

**Expected Output:**
```
[1] 85 78 88
```

---

### 3.4 Logical Indexing

Filter vectors using logical conditions.

#### Example 3.4: Logical Indexing

```r
# Create a data vector
ages <- c(25, 18, 30, 22, 35, 28)

# Create a logical vector
ages > 25            # Which are greater than 25?
```

**Expected Output:**
```
[1] FALSE FALSE  TRUE FALSE  TRUE FALSE
```

```r
# Use the logical vector to filter
ages[ages > 25]      # Extract ages greater than 25
```

**Expected Output:**
```
[1] 30 35
```

```r
# Multiple conditions
ages[(ages > 20) & (ages < 30)]  # Between 20 and 30
```

**Expected Output:**
```
[1] 25 22 28
```

```r
# OR condition
ages[(ages < 20) | (ages > 30)]  # Less than 20 OR greater than 30
```

**Expected Output:**
```
[1] 35
```

---

### 3.5 Vector Operations

Operations on vectors are applied element-wise.

#### Interactive Example 3.5: Vector Operations

```r
# Element-wise operations
v1 <- c(1, 2, 3, 4)
v2 <- c(10, 20, 30, 40)

v1 + v2              # Addition
```

**Expected Output:**
```
[1] 11 22 33 44
```

```r
v1 * v2              # Multiplication
```

**Expected Output:**
```
[1] 10 40 90 160
```

```r
# Recycling - shorter vector is repeated
v3 <- c(1, 2)
v1 + v3              # v3 is recycled: (1+1, 2+2, 3+1, 4+2)
```

**Expected Output:**
```
[1] 2 4 4 6
```

```r
# Operations with scalars
v1 * 2               # Multiply each element by 2
```

**Expected Output:**
```
[1] 2 4 6 8
```

```r
# Vectorized functions
sqrt(c(1, 4, 9, 16))  # Apply sqrt to each element
```

**Expected Output:**
```
[1] 1 2 3 4
```

---

### 3.6 Named Vectors

Give elements meaningful names for clarity.

#### Example 3.6: Named Vectors

```r
# Method 1: Create with names
temperatures <- c(Monday = 72, Tuesday = 75, Wednesday = 70)
temperatures
```

**Expected Output:**
```
  Monday  Tuesday Wednesday 
      72       75       70 
```

```r
# Method 2: Assign names afterward
days_of_week <- 1:7
names(days_of_week) <- c("Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun")
days_of_week
```

**Expected Output:**
```
Mon Tue Wed Thu Fri Sat Sun 
  1   2   3   4   5   6   7 
```

```r
# Access by name
temperatures["Monday"]
```

**Expected Output:**
```
Monday 
    72 
```

```r
# Get just the names
names(temperatures)
```

**Expected Output:**
```
[1] "Monday"    "Tuesday"   "Wednesday"
```

---

### 3.7 Sorting and Ranking

Organize vectors in different ways.

#### Example 3.7: Sorting Vectors

```r
# Create sample data
scores <- c(85, 92, 78, 92, 88, 76)

# Sort in ascending order
sort(scores)
```

**Expected Output:**
```
[1] 76 78 85 88 92 92
```

```r
# Sort in descending order
sort(scores, decreasing = TRUE)
```

**Expected Output:**
```
[1] 92 92 88 85 78 76
```

```r
# Order - returns indices that would sort
order(scores)        # Positions that sort the vector
```

**Expected Output:**
```
[1] 5 3 1 4 2 6
```

```r
# Use order to reorder a vector
names <- c("Alice", "Bob", "Charlie", "Diana", "Eve", "Frank")
names[order(scores)]  # Names in order of scores
```

**Expected Output:**
```
[1] "Frank"   "Charlie" "Alice"   "Diana"   "Bob"     "Diana"  
```

```r
# Rank - gives rank of each element
rank(scores)         # What rank is each score?
```

**Expected Output:**
```
[1] 3 5.5 1 5.5 4 2
```

(Note: 92 appears twice, so both get the average rank 5.5)

---

## Chapter 4: Matrices and Matrix Operations

### 4.1 What is a Matrix?

A **matrix** is a two-dimensional collection of elements arranged in rows and columns. All elements must be the same data type (Venables & Smith, 2024).

#### Example 4.1: Creating Matrices

```r
# Method 1: Using matrix() function
m1 <- matrix(1:12, nrow = 3, ncol = 4)
m1
```

**Expected Output:**
```
     [,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12
```

```r
# By default, fills column-by-column (column-major order)

# Fill row-by-row with byrow = TRUE
m2 <- matrix(1:12, nrow = 3, byrow = TRUE)
m2
```

**Expected Output:**
```
     [,1] [,2] [,3] [,4]
[1,]    1    2    3    4
[2,]    5    6    7    8
[3,]    9   10   11   12
```

```r
# Method 2: Combine vectors with cbind() and rbind()
# cbind - combine as columns
cbind(c(1, 2, 3), c(4, 5, 6))
```

**Expected Output:**
```
     [,1] [,2]
[1,]    1    4
[2,]    2    5
[3,]    3    6
```

```r
# rbind - combine as rows
rbind(c(1, 2, 3, 4), c(5, 6, 7, 8))
```

**Expected Output:**
```
     [,1] [,2] [,3] [,4]
[1,]    1    2    3    4
[2,]    5    6    7    8
```

---

### 4.2 Accessing Matrix Elements

Access matrix elements using `[row, column]` notation.

#### Example 4.2: Matrix Indexing

```r
# Create sample matrix
m <- matrix(1:15, nrow = 3)
m
```

**Expected Output:**
```
     [,1] [,2] [,3] [,4] [,5]
[1,]    1    4    7   10   13
[2,]    2    5    8   11   14
[3,]    3    6    9   12   15
```

```r
# Single element
m[2, 3]              # Row 2, Column 3
```

**Expected Output:**
```
[1] 8
```

```r
# Entire row
m[1, ]               # All of row 1
```

**Expected Output:**
```
[1]  1  4  7 10 13
```

```r
# Entire column
m[, 2]               # All of column 2
```

**Expected Output:**
```
[1] 4 5 6
```

```r
# Multiple rows/columns
m[1:2, 2:4]          # Rows 1-2, Columns 2-4
```

**Expected Output:**
```
     [,1] [,2] [,3]
[1,]    4    7   10
[2,]    5    8   11
```

---

### 4.3 Matrix Properties

Inspect and modify matrix dimensions.

#### Example 4.3: Matrix Properties

```r
m <- matrix(1:20, nrow = 4)

# Dimensions
dim(m)               # Returns c(rows, columns)
```

**Expected Output:**
```
[1] 4 5
```

```r
nrow(m)              # Number of rows
ncol(m)              # Number of columns
length(m)            # Total elements
```

**Expected Output:**
```
[1] 4
[1] 5
[1] 20
```

```r
# Add row and column names
rownames(m) <- c("A", "B", "C", "D")
colnames(m) <- c("Col1", "Col2", "Col3", "Col4", "Col5")
m
```

**Expected Output:**
```
  Col1 Col2 Col3 Col4 Col5
A    1    5    9   13   17
B    2    6   10   14   18
C    3    7   11   15   19
D    4    8   12   16   20
```

```r
# Transpose a matrix
t(m)                 # Switch rows and columns
```

**Expected Output:**
```
     A B C D
Col1 1 2 3 4
Col2 5 6 7 8
Col3 9 10 11 12
Col4 13 14 15 16
Col5 17 18 19 20
```

---

### 4.4 Matrix Operations

Perform calculations on matrices.

#### Example 4.4: Matrix Calculations

```r
# Create matrices
A <- matrix(c(1, 2, 3, 4), nrow = 2)
B <- matrix(c(5, 6, 7, 8), nrow = 2)

A
B
```

**Expected Output:**
```
     [,1] [,2]
[1,]    1    3
[2,]    2    4

     [,1] [,2]
[1,]    5    7
[2,]    6    8
```

```r
# Element-wise operations
A + B                # Addition
```

**Expected Output:**
```
     [,1] [,2]
[1,]    6   10
[2,]    8   12
```

```r
A * B                # Element-wise multiplication (not matrix multiply)
```

**Expected Output:**
```
     [,1] [,2]
[1,]    5   21
[2,]   12   32
```

```r
# Matrix multiplication
A %*% B              # True matrix multiplication
```

**Expected Output:**
```
     [,1] [,2]
[1,]   17   31
[2,]   22   40
```

```r
# Other operations
rowSums(A)           # Sum each row
colSums(A)           # Sum each column
```

**Expected Output:**
```
[1] 4 6
[1] 3 7
```

```r
rowMeans(A)          # Mean of each row
colMeans(A)          # Mean of each column
```

**Expected Output:**
```
[1] 2 3
[1] 1.5 3.5
```

---

## Chapter 5: Arrays and Multi-Dimensional Data

### 5.1 Understanding Arrays

An **array** is a multi-dimensional generalization of a vector. While matrices are 2D, arrays can have 3D, 4D, or more dimensions.

#### Example 5.1: Creating Arrays

```r
# Create a 3D array
arr <- array(1:24, dim = c(3, 4, 2))    
arr
```

`dim = c(3, 4, 2)` indicates the dimensions:
- 3 rows
- 4 columns
- 2 matrices (layers)

**Expected Output:**
```
, , 1

     [,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12

, , 2

     [,1] [,2] [,3] [,4]
[1,]   13   16   19   22
[2,]   14   17   20   23
[3,]   15   18   21   24
```

(This creates a 3×4×2 array: 3 rows, 4 columns, 2 "layers")

```r
# With dimension names
arr_named <- array(1:24,
                   dim = c(3, 4, 2),
                   dimnames = list(
                     c("Row1", "Row2", "Row3"),
                     c("A", "B", "C", "D"),
                     c("Layer1", "Layer2")
                   ))

arr_named[, , "Layer1"]  # Access Layer1
```

**Expected Output:**
```
      A B  C  D
Row1  1 4  7 10
Row2  2 5  8 11
Row3  3 6  9 12
```

---

### 5.2 Accessing Array Elements

Access array elements using multi-dimensional indexing.

#### Example 5.2: Array Indexing

```r
arr <- array(1:24, dim = c(3, 4, 2))

# Single element: [row, col, layer]
arr[2, 3, 1]         # Row 2, Column 3, Layer 1
```

**Expected Output:**
```
[1] 8
```

```r
# Entire row from a layer
arr[1, , 1]
```

**Expected Output:**
```
[1]  1  4  7 10
```

```r
# Entire layer
arr[, , 2]
```

**Expected Output:**
```
     [,1] [,2] [,3] [,4]
[1,]   13   16   19   22
[2,]   14   17   20   23
[3,]   15   18   21   24
```

---

### 5.3 Converting Between Data Structures

R allows flexible conversion between vectors, matrices, and arrays by modifying dimensions.

#### Example 5.3: Dimension Conversion

```r
# Start with a vector
vec <- 1:12
length(vec)
```

**Expected Output:**
```
[1] 12
```

```r
# Convert to matrix by assigning dimensions
dim(vec) <- c(3, 4)
vec
```

**Expected Output:**
```
     [,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12
```

```r
# Now it's a matrix! But the underlying data is the same
class(vec)
```

**Expected Output:**
```
[1] "matrix" "array"
```

```r
# Convert same object to 3D array
dim(vec) <- c(2, 3, 2)
vec
```

**Expected Output:**
```
, , 1

     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6

, , 2

     [,1] [,2] [,3]
[1,]    7    9   11
[2,]    8   10   12
```

```r
# Check dimensions
dim(vec)
```

**Expected Output:**
```
[1] 2 3 2
```

---

## Chapter 6: Lists

### 6.1 Understanding Lists

A **list** is R's most flexible data structure. Unlike vectors and matrices, lists can contain elements of different types and different lengths. Lists are often used to return multiple results from functions.

#### Example 6.1: Creating Lists

```r
# Simple list
my_list <- list("apple", "banana", "orange")
my_list
```

**Expected Output:**
```
[[1]]
[1] "apple"

[[2]]
[1] "banana"

[[3]]
[1] "orange"
```

```r
# List with mixed types
student <- list(
  name = "Alice",
  age = 20,
  grades = c(85, 90, 88),
  enrolled = TRUE
)
student
```

**Expected Output:**
```
$name
[1] "Alice"

$age
[1] 20

$grades
[1] 85 90 88

$enrolled
[1] TRUE
```

---

### 6.2 Accessing List Elements

Lists can be accessed by position or by name.

#### Example 6.2: List Access

```r
student <- list(name = "Bob", age = 22, grades = c(92, 88, 95))

# Single bracket - returns a list
student[1]
```

**Expected Output:**
```
$name
[1] "Bob"
```

```r
class(student[1])   # Still a list
```

**Expected Output:**
```
[1] "list"
```

```r
# Double bracket - returns the element itself
student[[1]]
```

**Expected Output:**
```
[1] "Bob"
```

```r
class(student[[1]])  # Now it's a character
```

**Expected Output:**
```
[1] "character"
```

```r
# Dollar sign - access by name
student$name        # Same as student[["name"]]
```

**Expected Output:**
```
[1] "Bob"
```

```r
student$grades      # Access the grades vector
```

**Expected Output:**
```
[1] 92 88 95
```

```r
student$grades[2]   # Second grade
```

**Expected Output:**
```
[1] 88
```

---

### 6.3 Modifying Lists

Add, remove, or change list elements.

#### Example 6.3: List Modification

```r
my_list <- list("volvo", "honda", "toyota")

# Add an element
my_list[[4]] <- "bmw"
my_list
```

**Expected Output:**
```
[[1]]
[1] "volvo"

[[2]]
[1] "honda"

[[3]]
[1] "toyota"

[[4]]
[1] "bmw"
```

```r
# Change an element
my_list[[2]] <- "ford"
my_list
```

**Expected Output:**
```
[[1]]
[1] "volvo"

[[2]]
[1] "ford"

[[3]]
[1] "toyota"

[[4]]
[1] "bmw"
```

```r
# Use append() to add elements
fruits <- list("apple", "banana", "cherry")
fruits <- append(fruits, "date")       # Add at end
fruits
```

**Expected Output:**
```
[[1]]
[1] "apple"

[[2]]
[1] "banana"

[[3]]
[1] "cherry"

[[4]]
[1] "date"
```

```r
# Add at specific position
fruits <- append(fruits, "blueberry", after = 1)
fruits
```

**Expected Output:**
```
[[1]]
[1] "apple"

[[2]]
[1] "blueberry"

[[3]]
[1] "banana"

[[4]]
[1] "cherry"

[[5]]
[1] "date"
```

---

### 6.4 Removing List Elements

Remove elements using negative indexing.

#### Example 6.4: Removing List Elements

```r
my_list <- list("A", "B", "C", "D", "E")

# Remove element 2
new_list <- my_list[-2]
new_list
```

**Expected Output:**
```
[[1]]
[1] "A"

[[2]]
[1] "C"

[[3]]
[1] "D"

[[4]]
[1] "E"
```

```r
# Remove multiple elements
my_list[-c(2, 4)]
```

**Expected Output:**
```
[[1]]
[1] "A"

[[2]]
[1] "C"

[[3]]
[1] "E"
```

---

### 6.5 Checking List Membership

Check if values exist in lists.

#### Interactive Example 6.5: List Membership

```r
cars <- list("volvo", "honda", "toyota")

# Check membership
"honda" %in% cars    # Is "honda" in the list?
```

**Expected Output:**
```
[1] TRUE
```

```r
"ford" %in% cars     # Is "ford" in the list?
```

**Expected Output:**
```
[1] FALSE
```

```r
# Case-sensitive
"Honda" %in% cars    # Capital H
```

**Expected Output:**
```
[1] FALSE
```

---

## Chapter 7: Data Frames

### 7.1 Understanding Data Frames

A **data frame** is R's most important data structure for statistical analysis. It's like a spreadsheet or SQL table: rows represent observations, columns represent variables. Each column can be a different data type, but within a column, all elements must be the same type (R Core Team, 2024).

#### Example 7.1: Creating Data Frames

```r
# Create a data frame
students <- data.frame(
  student_id = c(1001, 1002, 1003, 1004),
  name = c("Alice", "Bob", "Charlie", "Diana"),
  age = c(20, 19, 21, 20),
  gpa = c(3.8, 3.5, 3.9, 3.7)
)

students
```

**Expected Output:**
```
  student_id     name age gpa
1        1001    Alice  20 3.8
2        1002      Bob  19 3.5
3        1003  Charlie  21 3.9
4        1004    Diana  20 3.7
```

---

### 7.2 Data Frame Properties

Inspect data frame structure and dimensions.

#### Example 7.2: Data Frame Properties

```r
students <- data.frame(
  name = c("Alice", "Bob", "Charlie"),
  age = c(20, 19, 21),
  gpa = c(3.8, 3.5, 3.9)
)

# Dimensions
nrow(students)       # Number of rows
ncol(students)       # Number of columns
dim(students)        # Both dimensions
```

**Expected Output:**
```
[1] 3
[1] 3
[1] 3 3
```

```r
# Column names
names(students)
colnames(students)
```

**Expected Output:**
```
[1] "name" "age"  "gpa" 
[1] "name" "age"  "gpa"
```

```r
# Row names
rownames(students)
```

**Expected Output:**
```
[1] "1" "2" "3"
```

```r
# Class
class(students)
```

**Expected Output:**
```
[1] "data.frame"
```

```r
# Structure - detailed view
str(students)
```

**Expected Output:**
```
'data.frame':       3 obs. of  3 variables:
 $ name: chr  "Alice" "Bob" "Charlie"
 $ age : num  20 19 21
 $ gpa : num  3.8 3.5 3.9
```

---

### 7.3 Accessing Data Frame Elements

Access data frames like matrices or by column name.

#### Example 7.3: Data Frame Indexing

```r
students <- data.frame(
  name = c("Alice", "Bob", "Charlie", "Diana"),
  age = c(20, 19, 21, 20),
  gpa = c(3.8, 3.5, 3.9, 3.7)
)

# Access by row and column
students[1, 2]       # Row 1, Column 2
```

**Expected Output:**
```
[1] 20
```

```r
# Access entire row
students[2, ]        # Row 2 (all columns)
```

**Expected Output:**
```
  name age gpa
2  Bob  19 3.5
```

```r
# Access entire column
students[, 1]        # Column 1 (all rows)
```

**Expected Output:**
```
[1] "Alice"   "Bob"     "Charlie" "Diana"  
```

```r
# Access column by name - recommended!
students$name
```

**Expected Output:**
```
[1] "Alice"   "Bob"     "Charlie" "Diana"  
```

```r
students$gpa
```

**Expected Output:**
```
[1] 3.8 3.5 3.9 3.7
```

```r
# Access first few rows
head(students)       # First 6 rows (or fewer)
head(students, n = 2)  # First 2 rows
```

**Expected Output:**
```
  name age gpa
1 Alice  20 3.8
2   Bob  19 3.5

  name age gpa
1 Alice  20 3.8
2   Bob  19 3.5
```

```r
# Access last few rows
tail(students, n = 2)
```

**Expected Output:**
```
    name age gpa
3 Charlie  21 3.9
4   Diana  20 3.7
```

---

### 7.4 Subsetting Data Frames

Filter data frames based on conditions.

#### Example 7.4: Subsetting

```r
students <- data.frame(
  name = c("Alice", "Bob", "Charlie", "Diana", "Eve"),
  age = c(20, 19, 21, 20, 18),
  gpa = c(3.8, 3.5, 3.9, 3.7, 3.6)
)

# Find students with age > 19
students[students$age > 19, ]
```

**Expected Output:**
```
    name age gpa
1  Alice  20 3.8
3 Charlie  21 3.9
4  Diana  20 3.7
```

```r
# Find students with GPA >= 3.7
students[students$gpa >= 3.7, ]
```

**Expected Output:**
```
    name age gpa
1  Alice  20 3.8
3 Charlie  21 3.9
4  Diana  20 3.7
```

```r
# Combine conditions
students[(students$age >= 20) & (students$gpa >= 3.7), ]
```

**Expected Output:**
```
    name age gpa
1  Alice  20 3.8
3 Charlie  21 3.9
4  Diana  20 3.7
```

---

### 7.5 Adding Columns to Data Frames

Add new variables to existing data frames.

#### Example 7.5: Adding Columns

```r
students <- data.frame(
  name = c("Alice", "Bob", "Charlie"),
  midterm = c(85, 78, 92),
  final = c(88, 82, 95)
)

students
```

**Expected Output:**
```
    name midterm final
1  Alice      85    88
2    Bob      78    82
3 Charlie      92    95
```

```r
# Add a new column
students$average <- (students$midterm + students$final) / 2
students
```

**Expected Output:**
```
    name midterm final average
1  Alice      85    88    86.5
2    Bob      78    82    80.0
3 Charlie      92    95    93.5
```

```r
# Add a column with a condition
students$passed <- students$average >= 80
students
```

**Expected Output:**
```
    name midterm final average passed
1  Alice      85    88    86.5   TRUE
2    Bob      78    82    80.0   TRUE
3 Charlie      92    95    93.5   TRUE
```

---

### 7.6 Importing Data from Files

Load data from external sources.

```r
# Read CSV file
data <- read.csv("data.csv", header = TRUE)

# Arguments explained:
# - file: path to the file
# - header: TRUE if first row contains column names
# - sep: field separator ("," for CSV, "\t" for TSV)
# - stringsAsFactors: FALSE keeps strings as character (not factors)

# Example with options
data <- read.csv("mydata.csv", 
                 header = TRUE,
                 sep = ",",
                 stringsAsFactors = FALSE)

# Quick inspection
head(data)        # First 6 rows
tail(data)        # Last 6 rows
str(data)         # Structure
summary(data)     # Summary statistics
```

---

### 7.7 Saving Data

Export data frames to files.

```r
# Save as R data format (preserves all R info)
save(students, file = "students.RData")

# Load R data format
load("students.RData")
```

```r
# Save as CSV
write.csv(students, "students.csv", row.names = FALSE)

#Read/Load as CSV
read.csv(students, header = TRUE, sep = ",")
```
---

## References

Chambers, J. M. (2020). *Statistical computing with R* (2nd ed.). Chapman and Hall/CRC.

Grolemund, G., & Wickham, H. (2017). *R for data science: Import, tidy, transform, visualize, and model data*. O'Reilly Media.

Kabacoff, R. I. (2022). *R in action: Data analysis and graphics with R* (3rd ed.). Manning Publications.

Matloff, N. (2011). *The art of R programming: A tour of statistical software design*. No Starch Press.

Peng, R. D., Kross, S., & Anderson, B. (2024). *The art of data science*. Leanpub. Retrieved from https://leanpub.com/artofdatascience

R Core Team. (2024). *R: A language and environment for statistical computing*. R Foundation for Statistical Computing. https://www.R-project.org/

Wickham, H., Çetinkaya-Rundel, M., & Grolemund, G. (2024). *R for data science* (2nd ed.). O'Reilly Media. Retrieved from https://r4ds.hadley.nz/

Venables, W. N., & Smith, D. M. (2024). *An introduction to R*. Retrieved from https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf

---

### Academic Papers

Ihaka, R., & Gentleman, R. (1996). R: A language for data analysis and graphics. *Journal of Computational and Graphical Statistics*, 5(3), 299-314.

Becker, R. A., Chambers, J. M., & Wilks, A. R. (1988). *The new S language: A programming environment for data analysis and graphics*. Chapman and Hall.

---

### Online Resources

- **CRAN (Comprehensive R Archive Network)**: https://cran.r-project.org/
- **R Documentation**: https://www.rdocumentation.org/
- **RStudio Community**: https://community.rstudio.com/
- **Stack Overflow R Tag**: https://stackoverflow.com/questions/tagged/r

---

## Appendix: Quick Reference

### Common Functions by Category

**Vector Creation**
- `c()` - Combine values
- `seq()` - Generate sequences
- `rep()` - Repeat values
- `:` - Create integer sequences
- `runif()` - Random uniform numbers
- `rnorm()` - Random normal numbers

**Vector Information**
- `length()` - Number of elements
- `class()` - Data type
- `str()` - Structure
- `head()`, `tail()` - First/last elements

**Vector Operations**
- `sort()` - Sort values
- `order()` - Sorting indices
- `rank()` - Ranks
- `unique()` - Remove duplicates
- `sum()`, `mean()`, `median()` - Statistics

**Matrix/Array Functions**
- `matrix()` - Create matrix
- `array()` - Create array
- `dim()` - Dimensions
- `nrow()`, `ncol()` - Number of rows/columns
- `rbind()`, `cbind()` - Combine by rows/columns
- `t()` - Transpose
- `%*%` - Matrix multiplication

**Data Frame Functions**
- `data.frame()` - Create data frame
- `str()` - Structure
- `head()`, `tail()` - Sample rows
- `summary()` - Summary statistics
- `read.csv()` - Read CSV file
- `write.csv()` - Write CSV file

**List Functions**
- `list()` - Create list
- `names()` - Element names
- `append()` - Add elements
- `$` operator - Access by name

---

## Glossary of Terms

**Array**: Multi-dimensional data structure (2D, 3D, etc.)

**Assignment Operator**: `<-` symbol used to create objects

**Atomic Vector**: Basic vector containing single data type

**Class**: Data type in R (numeric, character, logical, etc.)

**Concatenate**: Combine multiple elements using `c()`

**Data Frame**: Table-like structure with rows and columns

**Element**: Individual value in a vector, matrix, or list

**Function**: Reusable block of code that performs a task

**Index/Indexing**: Selecting elements using `[ ]` notation

**List**: Collection of objects of different types

**Matrix**: Two-dimensional rectangular array

**Mode**: Storage type of an object

**Object**: Any value, data structure, or function in R

**Recycling**: R repeats shorter vectors to match longer ones

**Vector**: One-dimensional sequence of values

---

**End of Manual**

*This manual was created for educational purposes. For the latest information and updates, visit https://cran.r-project.org/*
