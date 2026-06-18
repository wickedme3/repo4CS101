# R Programming Exercises

**Author:** Joyce F. Jamile   
**For Educational Use Only** 

---

## Exercises

### Exercise Set 1: Vectors and Basic Operations

**1.1** Create a vector containing the numbers 1 through 100. Find:
   - The length of the vector
   - The sum of all elements
   - The mean of all elements
   - Which elements are greater than 50

**1.2** Create two vectors: `x <- c(2, 4, 6, 8, 10)` and `y <- c(1, 2, 3, 4, 5)`. Calculate:
   - x + y (element-wise addition)
   - x * y (element-wise multiplication)
   - x %% y (element-wise modulus)
   - sqrt(x) (square root of each element)

**1.3** Create a vector of 10 random numbers between 1 and 100 using `runif(10, min=1, max=100)`. Then:
   - Sort the vector in ascending order
   - Sort the vector in descending order
   - Find the rank of each element
   - Find which element is the maximum

**1.4** Create a named vector with the days of the week as names and the number of hours you study each day as values. Calculate:
   - Total hours studied
   - Average hours per day
   - Which day you studied the most
   - Which days you studied more than 2 hours

---

### Exercise Set 2: Matrices

**2.1** Create a 3×4 matrix with numbers 1-12. Then:
   - Access the element in row 2, column 3
   - Extract the entire second row
   - Extract the entire third column
   - Extract rows 1-2, columns 2-3

**2.2** Create two 2×2 matrices:
   ```
   A = [1 2]    B = [5 6]
       [3 4]        [7 8]
   ```
   Calculate:
   - A + B (element-wise addition)
   - A * B (element-wise multiplication)
   - A %*% B (matrix multiplication)
   - t(A) (transpose of A)

**2.3** Create a matrix with row names ("Patient1", "Patient2", "Patient3") and column names ("Age", "Weight", "Height"). Fill it with appropriate sample data.

---

### Exercise Set 3: Data Frames

**3.1** Create a data frame with information about 5 books:
   - Title (character)
   - Author (character)
   - Year Published (numeric)
   - Pages (numeric)
   - Rating (numeric 1-5)

   Then:
   - Display the first 3 rows
   - Extract the "Title" column
   - Find books published after 2015
   - Find books with rating >= 4

**3.2** Create a data frame for 10 students with:
   - Student ID (1001-1010)
   - Name (your choice)
   - Midterm Grade (70-100)
   - Final Grade (70-100)

   Then:
   - Calculate average of midterm and final grades
   - Create a "Passed" column (TRUE if average >= 70)
   - Find students who passed
   - Find the student with the highest average grade

**3.3** Load a built-in dataset: `data(mtcars)`
   - Display basic information about the dataset
   - Find cars with mpg > 25
   - Find cars with hp > 200
   - What are the row names (car models)?

---

### Exercise Set 4: Lists

**4.1** Create a list containing:
   - A vector of 5 numbers
   - A character vector with 3 names
   - A logical vector with 4 elements
   - A single string value

   Then:
   - Access each element using both `[[ ]]` and `$` notation (where applicable)
   - Modify the first numeric element
   - Add a new element to the list

**4.2** Create a list called "person" with:
   - name = "John"
   - age = 25
   - skills = c("R", "Python", "SQL")
   - experience_years = 3

   Then:
   - Access the skills vector
   - Change the age to 26
   - Add a new element "education" = "Bachelor's Degree"

---

### Exercise Set 5: Mixed Data Structures

**5.1** Create a list of 3 data frames, each containing:
   - Student names
   - Three test scores

   Then:
   - Extract the second student's scores from the first data frame
   - Calculate the average score for each data frame
   - Create a summary showing which data frame has the highest average

**5.2** Create a 3D array with dimensions 4×3×2 containing:
   - Quarters (Q1, Q2, Q3, Q4) as rows
   - Regions (East, West, South) as columns
   - Years (2023, 2024) as layers

   Fill with sales data and then:
   - Find the total sales for Q2, 2023
   - Extract all data for the West region
   - Calculate total sales by region

---

**End of Manual**

*This manual was created for educational purposes. For the latest information and updates, visit https://cran.r-project.org/*
