# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner


## ALGORITHM 1: To Find L and U Matrices Using LU Decomposition

1. Start the program.
2. Import the required libraries: `numpy` and `lu` from `scipy.linalg`.
3. Read the input matrix and convert it into a NumPy array.
4. Apply the `lu()` function to the matrix.
5. Obtain the permutation matrix **P**, lower triangular matrix **L**, and upper triangular matrix **U**.
6. Display the lower triangular matrix **L**.
7. Display the upper triangular matrix **U**.
8. End the program.


## ALGORITHM 2: To Solve a System of Equations Using LU Decomposition

1. Start the program.
2. Import the required libraries: `numpy`, `lu_factor`, and `lu_solve` from `scipy.linalg`.
3. Read the coefficient matrix **A** and convert it into a NumPy array.
4. Read the constant matrix/vector **B** and convert it into a NumPy array.
5. Perform LU factorization of matrix **A** using `lu_factor()`.
6. Store the LU matrix and pivot indices obtained from the factorization.
7. Use `lu_solve()` with the LU matrix, pivot indices, and matrix/vector **B** to compute the solution.
8. Store the resulting solution vector **X**.
9. Display the solution vector **X**.
10. End the program.


## Program:
(i) To find the L and U matrix
```
'''Program to find L and U matrix using LU decomposition.
Developed by:LOGA SRI M
RegisterNumber: 212225230153
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np 
from scipy.linalg import lu
matrix = np.array(eval(input()))
P,L,U=lu(matrix)
print(L)
print(U)
```
(ii) To find the LU Decomposition of a matrix
```
'''Program to solve a matrix using LU decomposition.
Developed by: LOGA SRI M
RegisterNumber: 212225230153
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu_factor,lu_solve
A=np.array(eval(input()))
B=np.array(eval(input()))
lu,pivot=lu_factor(A)
x=lu_solve((lu,pivot),B)
print(x)

```

## Output:
<img width="1240" height="466" alt="Screenshot 2026-05-21 140646" src="https://github.com/user-attachments/assets/cdd512a7-4b2f-433b-bc58-89859f7ca88e" />

<img width="1216" height="202" alt="Screenshot 2026-05-21 140709" src="https://github.com/user-attachments/assets/cbcdf545-b5bf-42ea-8794-c858445170bc" />




## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

