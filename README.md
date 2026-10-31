# 📊 NumPy Student Performance Data Analysis

This project demonstrates **core NumPy operations** using a student marks dataset.
Each problem is structured with a **question followed by its solution**, simulating a real data analysis workflow.

---

## 📁 Dataset

```python
import numpy as np

data = np.array([
 [78, 85, 90, 88],
 [67, 72, 70, 60],
 [90, 92, 94, 96],
 [56, 65, 60, 58],
 [88, 84, 82, 86],
 [73, 75, 78, 72],
 [91, 89, 93, 90],
 [64, 68, 70, 66]
])
```


**Subjects:**

1. Math
2. Science
3. English
4. Computer
<img width="174" height="154" alt="image" src="https://github.com/user-attachments/assets/9504d725-afe1-4992-9ddf-449e523b8739" />

---

# 🧠 Assignment Solutions

---

## 1️⃣ NumPy Copy vs View

### ❓ Question

* Create a copy and a view of the dataset
* Modify original data
* Observe changes

### ✅ Solution

```python
data_copy = data.copy()
data_view = data.view()

data[0, 0] = 100

print("Original:\n", data)
print("Copy:\n", data_copy)
print("View:\n", data_view)
```
<img width="394" height="483" alt="image" src="https://github.com/user-attachments/assets/a32adbf6-b77b-45db-a3aa-5103c0302cb8" />

### 💡 Insight

* Copy → Independent
* View → Reflects original changes

---

## 2️⃣ Array Shape

### ❓ Question

* Find shape, number of students, subjects, and dimensions

### ✅ Solution

```python
print(data.shape)
print("Students:", data.shape[0])
print("Subjects:", data.shape[1])
print("Dimensions:", data.ndim)
```
<img width="197" height="112" alt="image" src="https://github.com/user-attachments/assets/ebbd9da4-56c7-479a-85a2-49c095ddf612" />

---

## 3️⃣ Reshape Array

### ❓ Question

* Convert into different shapes

### ✅ Solution

```python
a = data.reshape(-1)
print(a)

b = data.reshape(2, 16)
print(b)

c = data.reshape(4, 8)
print(c)
```
<img width="522" height="164" alt="image" src="https://github.com/user-attachments/assets/c8c3e9ea-43be-449e-a4a2-edc0b06641e3" />

---

## 4️⃣ Iterating Arrays

### ❓ Question

* Iterate element-wise and row-wise

### ✅ Solution

```python
# Row-wise
for row in data:
    print(row)

# Element-wise
for row in data:
    for val in row:
        print(val)

# Using nditer
for x in np.nditer(data):
    print(x)
```
<img width="547" height="500" alt="image" src="https://github.com/user-attachments/assets/568d89c9-0d43-493c-8200-e865dd4522d2" />

---

## 5️⃣ Join Arrays

### ❓ Question

* Combine datasets using different methods

### ✅ Solution

```python
extra_students = np.array([
 [80, 82, 84, 86],
 [60, 62, 64, 66]
])

print(np.concatenate((data, extra_students), axis=0))
print(np.vstack((data, extra_students)))
print(np.hstack((data, data)))
```
<img width="266" height="494" alt="image" src="https://github.com/user-attachments/assets/756eb623-3b6d-4546-b800-9c5aae6ef9e4" />


---

## 6️⃣ Split Arrays

### ❓ Question

* Split dataset into parts

### ✅ Solution

```python
joined = np.concatenate((data, extra_students), axis=0)

print(np.array_split(joined, 2))
print(np.array_split(joined, 4))
print(np.hsplit(joined, 2))
```
<img width="398" height="621" alt="image" src="https://github.com/user-attachments/assets/57fcf38b-8c0a-4e5a-afec-54fa812bb024" />

---

## 7️⃣ Search Operations

### ❓ Question

* Find values using conditions

### ✅ Solution

```python
print(np.where(data == 90))
print(np.where(data > 90))
print(np.where(data[:, 0] > 85))
```
<img width="421" height="91" alt="image" src="https://github.com/user-attachments/assets/02b4c215-659e-48b0-9824-c60ed3b3ad4d" />

---

## 8️⃣ Sorting

### ❓ Question

* Sort dataset

### ✅ Solution

```python
print(np.sort(data))
print(np.sort(data, axis=1))
print(np.sort(data, axis=0))
```
<img width="207" height="431" alt="image" src="https://github.com/user-attachments/assets/f5f463a4-b37f-49dc-879a-d6500ceb83b3" />

---

## 9️⃣ Filtering (Core Data Analysis)

### ❓ Question

* Filter marks > 80
* Filter students with Math > 85

### ✅ Solution

```python
# Boolean filtering
filter_arr = data > 80
print(data[filter_arr])

# Custom filtering (Math > 85)
filter_math = data[:, 0] > 85
print(data[filter_math])
```
<img width="385" height="109" alt="image" src="https://github.com/user-attachments/assets/b4964546-ca9c-43c5-8c5e-2bbf92d06716" />

---

## 🔥 Custom Filtering (Manual Logic)

```python
filter_arr = []

for row in data:
    for marks in row:
        filter_arr.append(marks > 80)

filter_arr = np.array(filter_arr)
new_arr = np.array_split(filter_arr, 8)
new_arr = np.array(new_arr)

filtered_data = data[new_arr]
print(filtered_data)
```
<img width="355" height="40" alt="image" src="https://github.com/user-attachments/assets/d17487d2-e4fb-4eba-8dff-130cacf5c92c" />

---

## ⭐ Bonus Analysis

### ❓ Question

* Advanced insights

### ✅ Solution

```python
# Students scoring >85 in all subjects
print(data[np.all(data > 85, axis=1)])

# Highest marks per subject
print(np.max(data, axis=0))

# Average marks per student
print(np.mean(data, axis=1))
```
<img width="382" height="98" alt="image" src="https://github.com/user-attachments/assets/b3fd430c-aeae-442f-bb72-03cbfbef1754" />

---

## 🚀 Key Takeaways

* Data structuring using NumPy arrays
* Data transformation and reshaping
* Filtering and conditional selection
* Basic statistical analysis

---

## 📁 Project Structure

```
student-performance-data-analysis/
│── main.py
│── README.md
│── screenshots/
```

---

## 🛠 Requirements

```
pip install numpy
```

---

## 🏁 Run the Project

```
python main.py
```

---

## 📌 Conclusion

This project demonstrates **foundational data analysis techniques** using NumPy, including:

* Data preprocessing
* Data filtering
* Data exploration
* Basic statistical insights

---
