# begginer-numpy-assignment-2026
Python NumPy practice assignment covering arrays, copy vs view, reshape, iteration, join, split, search, sort and filter.
📌 About This Project

This repository contains a Python NumPy practice assignment based on a student examination marks dataset.

The project focuses on learning and understanding important NumPy concepts through practical examples using a single dataset.

The dataset contains marks of 8 students across 4 subjects: Math, Science, English, and Computer.

🎯 Objectives

The main objectives of this assignment are:

Understand NumPy arrays.
Learn the difference between Copy and View.
Understand array Shape and Dimensions.
Perform array Reshaping.
Learn Array Iteration.
Join multiple arrays.
Split arrays into smaller parts.
Search for specific values.
Sort array elements.
Filter data using conditions.
Perform basic statistical operations.
🛠️ Technologies Used
Python – Programming language.
NumPy – Python library for numerical computing.
📂 Project Structure
text
numpy-practice-assignment/
│
├── numpy_practice_assignment.py
│
└── README.md

File	Description
numpy_practice_assignment.py	Contains all assignment questions and their Python solutions
README.md	Project documentation
📊 Dataset Information

The dataset contains student examination marks.

Total Students: 8
Total Subjects: 4

Dataset Columns:

Column	Subject
Column 1	Math
Column 2	Science
Column 3	English
Column 4	Computer
📚 Topics Covered
1. NumPy Copy vs View
Creating a copy using copy().
Creating a view using view().
Understanding changes in original, copied, and viewed arrays.
2. NumPy Array Shape
Finding array shape using shape.
Counting students and subjects.
Checking dimensions using ndim.
3. NumPy Array Reshape
Converting a 2D array into a 1D array.
Reshaping into 2 rows and 16 columns.
Reshaping into 4 rows and 8 columns.
4. NumPy Array Iterating
Iterating through array elements.
Printing student-wise marks.
Using np.nditer().
5. NumPy Array Join
Joining arrays using np.concatenate().
Joining arrays using np.vstack().
Joining arrays using np.hstack().
6. NumPy Array Split
Splitting arrays into 2 equal parts.
Splitting arrays into 4 parts.
Splitting columns using np.hsplit().
7. NumPy Array Search
Finding positions of marks equal to 90.
Finding marks greater than 90.
Finding students scoring above 85 in Math using np.where().
8. NumPy Array Sort
Sorting all marks in ascending order.
Sorting marks row-wise.
Sorting marks column-wise.
9. NumPy Array Filter
Creating Boolean filters.
Filtering marks greater than 80.
Filtering students with Math marks greater than 85.
⭐ Bonus Challenges

The assignment also includes:

Finding students who scored more than 85 in all subjects.
Finding the highest marks in each subject.
Calculating the average marks of each student.
⚙️ Installation and Setup
Step 1: Install Python

Download Python from https://www.python.org/

Step 2: Install NumPy

Open your terminal and run:

bash
pip install numpy

Step 3: Clone the Repository
bash
git clone https://github.com/LinaChauhan/begginer-numpy-assignment-2026

Step 4: Navigate to the Project Folder
bash
cd numpy-practice-assignment

Step 5: Run the Python File
bash
python numpy_practice_assignment.py

📖 NumPy Functions Used
Function	Purpose
np.array()	Creates a NumPy array
copy()	Creates an independent copy
view()	Creates a view of an array
shape	Returns array shape
ndim	Returns number of dimensions
reshape()	Changes array shape
np.nditer()	Iterates through array elements
np.concatenate()	Joins arrays
np.vstack()	Joins arrays vertically
np.hstack()	Joins arrays horizontally
np.array_split()	Splits an array
np.hsplit()	Splits an array column-wise
np.where()	Finds positions matching a condition
np.sort()	Sorts array elements
np.max()	Finds maximum values
np.mean()	Calculates average
np.all()	Checks whether all elements satisfy a condition
🎓 Learning Outcomes

After completing this assignment, I gained practical knowledge of:

Creating and manipulating NumPy arrays.
Understanding array operations.
Working with multidimensional arrays.
Joining and splitting datasets.
Searching, sorting, and filtering data.
Performing basic statistical calculations.
