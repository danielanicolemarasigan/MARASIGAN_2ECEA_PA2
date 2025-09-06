# MARASIGAN_2ECEA_PA2

This repository contains python scripts/codes solving the 2 different given problems in my programming assignment on Numerical Python (Numpy).

---

## Files
* 'MARSIGAN_2ECEA_PA2.ipynb': This Jupyter Notebook file contains the codes for each problem.
* 'README.md': This file contains the summary of the assignment.

---

## Solutions Overview
### 1. Normalization Problem

**Problem:** Create a random 5 x 5 ndarray and store it to variable X. Normalize X.

**Approach:**
1. To initialize the program, we import the Numpy library to the program/file.
2. We then generate a random 5x5 ndarray, then store it in variable X.
3. The mean and standard deviation is stored in variables x & o respectively.
4. Then the Z value (or the normalized value) is computed with its formula, then storing it in variable Z.
5. The normalized array is then saved as an npy file.
6. To load the npy file, it will be stored in variable Norm.
7. Then Norm is printed in order to display the normalized array.

<pre>import numpy as np #Gives the program/file access to the Numpy library
X = np.random.random((5,5)) #Generates a random 5x5 ndarray, then stores it in variable X.
x = np.mean(X) #Computes for the mean of array X, then stores it in variable variable x.
o = np.std(X) #Computes for the standard deviation of array X, then stores it in variable o.

Z = (X-x)/o #Computes for the normalized value, Z, by normalizing X. It is then stored in variable Z.
Z #Prints Z, being the normalized array.

np.save('X_normalized.npy', Z) #Saves the normalized array as an npy file.</pre>
<pre>
  Norm = np.load('X_normalized.npy') #Stored in variable Norm, it loads the saved npy file containing the normalized array.
  Norm #Prints Norm
</pre>

---

## 2. Divisible by 3 Problem
**Problem:** Create a 10x10 array containing the squares of the first 100 positive integers. From this array, determine all elements that are divisible by 3.

**Approach:**
1.

<pre>import numpy as np #Gives access to the Numpy library
A = np.arange(1,101)**2 ##Generates an array containing numbers 1-100 (101 being the excluded terminal value), then stored to variable A
Ten = A.reshape(10,10) #Reformats/reshapes array A into a 10x10 array

DivBy3 = A[A%3 == 0] #Prints all numbers in the array that are divisible by 3 (or when divided by 3 its remainder (modulo) is zero (0))

np.save('div_by_3.npy', DivBy3) #Saves the newly made array as an npy file.</pre>
<pre>
  Div3 = np.load('div_by_3.npy') #Stored in variable Div3, it loads the saved npy file containing the array with perfect squares that are multiples of 3.
  Div3 #Prints Div3
</pre>
---
## How to View:

The Notebook file may be previewed via Github, or may be imported as an .ipynb file to Jupyter Notebook in order to see the full code with its input & output.

