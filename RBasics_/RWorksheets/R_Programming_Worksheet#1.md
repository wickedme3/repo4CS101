# Worksheet 1: Basic R Functions and Vector Operations

#### **This material is intended for internal use only and should not be shared, copied, or reproduced without authorization.**

---

## Worksheet 1: Basic R Functions and Vector Operations {#worksheet-1}

### Instructions

- Use RStudio or RStudio Cloud to complete this worksheet.
- Create a folder named `RWorksheets` in your `CS101_lastname` directory.
- Save your R script as `RWorksheet_lastname_1.R` in the `RWorksheets` folder.
- Complete this worksheet by answering each question and writing the code manually. DO NOT forget to run the code.

### Functions to Use

`seq()`, `assign()`, `min()`, `max()`, `c()`, `sort()`, `sum()`, `Filter()`

---

### Exercise 1: Creating and Analyzing a Vector

**Question 1.1:** Set up a vector named `age` containing the following 34 data points:
```
34, 28, 22, 36, 27, 18, 52, 39, 42, 29, 35, 31, 27, 22, 37, 34, 19, 20, 57, 49, 50, 37, 46, 25, 17, 37, 42, 53, 41, 51, 35, 24, 33, 41
```

a) How many data points are in this vector? Write the R code to determine this and provide the output.

b) What does the `length()` function tell us about the data structure? How would you use this function to verify that your vector was created correctly?

c) If you needed to find the number of workers younger than 30, what approach would you use? What additional function might be helpful?

---

### Exercise 2: Reciprocal Calculations

**Question 2:** Find the reciprocal of each age value in your `age` vector.

a) Write the R code to calculate the reciprocals and provide the output.

b) Why might reciprocals be useful in statistical analysis? Provide an example scenario where calculating reciprocals would be beneficial.

c) What happens when you try to calculate the reciprocal of zero? How would you modify your code to handle this situation safely?

---

### Exercise 3: Vector Concatenation and Assignment

**Question 3:** Create a new vector using the assignment `new_age <- c(age, 0, age)`.

a) What happens when you create this new vector? Describe the structure and content of `new_age`.

b) How many elements does `new_age` contain? Explain the pattern of how the original `age` vector is being combined with the zero value.

c) What would be the practical use of concatenating data in this manner? When might you want to duplicate data in your analysis?

---

### Exercise 4: Sorting Data

**Question 4:** Sort the values in the `age` vector in ascending order.

a) Write the R code to sort the vector and provide the output.

b) Why is sorting data important in data analysis? What insights become more apparent when data is organized in order?

c) How would you modify the code to sort in descending order? What would be the advantage of viewing data from largest to smallest values?

---

### Exercise 5: Finding Extremes

**Question 5:** Find the minimum and maximum values in the `age` vector.

a) Write the R code to find both values and provide the output.

b) What do the minimum and maximum values tell us about the age distribution in this dataset? How might this information be useful for employers?

c) How would you calculate the range (difference between maximum and minimum)? Why is the range an important summary statistic?

---

### Exercise 6: Working with Decimal Data

**Question 6:** Set up a vector named `data` containing the following 12 values:
```
2.4, 2.8, 2.1, 2.5, 2.4, 2.2, 2.5, 2.3, 2.5, 2.3, 2.4, 2.7
```

a) How many data points are in this vector? Write the R code and provide the output.

b) These values appear to be ratings or measurements on a 1-4 scale. What type of data might produce these values? Can you identify any patterns?

c) What would be the most appropriate measure of central tendency (mean, median, or mode) for this dataset? Why?

---

### Exercise 7: Repeating Vector Elements

**Question 7:** Create a new vector by repeating every value in the `data` vector.

a) Write the R code to create this new vector and describe what happened to the data.

b) How many elements will the new vector contain? Verify your answer with R code.

c) In what practical scenario might you want to repeat data values? Provide an example from a real-world context.

---

### Exercise 8: Generating Sequences

**Question 8:** Generate sequences using the `seq()` function for the following scenarios:

**8.1** Create a sequence of integers from 1 to 100.
- Write the R code and provide the output (showing first and last 10 values).

**8.2** Create a sequence of numbers from 20 to 60.
- Write the R code and provide the output.

**8.3** Calculate the mean of the numbers from 20 to 60.
- Write the R code and provide the result.

**8.4** Calculate the sum of numbers from 51 to 91.
- Write the R code and provide the result.

**8.5** Create a sequence of integers from 1 to 10,000.
- Write the R code to display the first 100 values.

a) How many total data points are generated across exercises 8.1, 8.2, and 8.4 combined? What calculation would you use to find this?

b) What is the difference between using the `:` operator and the `seq()` function? When would you prefer one over the other?

c) How can you efficiently find the 50th element in the sequence from 1 to 10,000 without scrolling through all values?

---

### Exercise 9: Filtering with Conditions

**Question 9:** Use the `Filter()` function to find all integers between 1 and 100 that are **not** divisible by 3, 5, or 7.

```R
Filter(function(i) { all(i %% c(3,5,7) != 0) }, seq(100))
```

a) Write the R code and provide the output.

b) What does the `%%` operator do? Explain how the logical condition works in this filter.

c) How many numbers from 1 to 100 satisfy this condition? What percentage of total numbers is this?

---

### Exercise 10: Reverse Sequences

**Question 10:** Generate a sequence of integers from 1 to 100 in **reverse** (descending) order.

a) Write the R code using at least two different methods and provide the output.

b) What is the most efficient way to reverse a sequence? Are there situations where one method is preferable to another?

c) What would be the practical use of reversing sequences in data analysis?

---

### Exercise 11: Finding Multiples with Conditions

**Question 11:** List all natural numbers below 25 that are multiples of either 3 or 5.

a) Write the R code using the `Filter()` function and provide the output.

b) Find the sum of these multiples. What is the total?

c) Why might we want to find numbers that satisfy multiple conditions (OR logic vs. AND logic)? How would your answer change if you needed numbers divisible by both 3 AND 5?

d) How would you extend this approach to find multiples of 3, 5, or 7 below 100? Write the code and compare the results.

---

### Exercise 12: Understanding Code Blocks and Syntax

**Question 12:** R requires proper syntax for code blocks using curly braces `{}`.

a) Attempt to enter the following code and observe the error:
```R
{x <- 0
x + 5 +}
```

Describe what error message you receive and why it occurred.

b) What is the purpose of curly braces in R? When are they necessary vs. optional?

c) Write the correct code:
```R
{
  x <- 0
  x + 5
}
```

Explain why this version works correctly.

---

### Exercise 13: Vector Indexing

**Question 13:** Set up a vector named `score` with the following 11 values:
```
72, 86, 92, 63, 88, 89, 91, 92, 75, 75, 77
```

a) Access the 2nd and 3rd elements. Write the R code and provide the output.

b) What does the index [1] refer to in R? Is it the first or second element?

c) How would you access elements 2 through 5? Write the code and explain what the colon `:` operator does.

d) How would you find all scores above 85? What function or approach would you use?

---

### Exercise 14: Handling Missing Values (NA)

**Question 14:** Create a vector `a <- c(1, 2, NA, 4, NA, 6, 7)`.

a) Display the vector with missing values represented as "-999" using:
```R
print(a, na.print="-999")
```

b) What does NA mean in R? Why do we need a way to represent missing data?

c) How would you calculate the mean of this vector while accounting for missing values? What function would you use?

d) In a real-world scenario, how would missing data originate? What are best practices for handling it?

---

### Exercise 15: Changing Data Classes

**Question 15:** Create a vector `x <- c(2, 3, 4)`.

a) Check the class of this vector. What is the class type?

b) Change the class to "foo" using:
```R
class(x) <- "foo"
```

c) What does the `class()` function tell us about data in R? Why is it important to know the data type?

d) What happens when you perform calculations on an object of class "foo"? Try adding 1 to x and explain the results.

---

### Exercise 16: User Input and Concatenation

**Question 16:** Enter the following code line by line:

```R
name <- readline(prompt="Enter your name: ")
age <- readline(prompt="Enter your age: ")
print(paste("My name is", name, "and I am", age, "years old."))
print(R.version.string)
```

a) What output do you receive?

b) What does the `paste()` function do? How is it different from `concatenate()` in other programming languages?

c) Why must user input be collected with `readline()` rather than just entering values directly? When would you use user input in real applications?

---

*End of R Programming Worksheets*

*Last Updated: June 19, 2026*
