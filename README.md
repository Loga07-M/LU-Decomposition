# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the program.
2. Import the neccessary libraries(numpy,scipy,linalg).
3. Define the matrix using numpy.
4. Use lu(),lu_solve(),lu_factor() to get the solutions.
5. End of the program.

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

