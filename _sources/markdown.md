## **ELIMINASI GAUSSIAN**
Eliminasi Gaussian adalah algoritma untuk mengubah matriks menjadi bentuk eselon baris (REF). Bagian ini melengkapi pembahasan sistem persamaan linear dengan memberikan metode sistematis untuk menyederhanakan dan menyelesaikannya menggunakan matriks dan operasi baris.

Tujuan utama:

1. Mendefinisikan secara tepat apa yang dimaksud sistem yang “lebih sederhana”.

2. Memberikan algoritma yang jelas untuk mencapainya.

3. Menjelaskan bagaimana membaca solusi dari bentuk tersebut.

### **Eliminasi Gauss**
Serangkaian langkah yang disebut operasi baris yang mempertahankan penyelesaian sistem

$$
\begin{cases}
x_1 - x_2 + x_3 = 3 \\
2x_1 + x_2 + 8x_3 = 18 \\
4x_1 + 2x_2 - 3x_3 = -2
\end{cases}
$$

==

$$
\left[
\begin{array}{ccc|c}
1 & -1 & 1 & 3 \\
2 & 1 & 8 & 18 \\
4 & 2 & -3 & -2
\end{array}
\right]
$$

**Setelah eliminasi Gauss (bentuk tangga)**

$$
\begin{cases}
x_1 - x_2 + x_3 = 3 \\
x_2 + 2x_3 = 4 \\
x_3 = 2
\end{cases}
$$

$$
\left[
\begin{array}{ccc|c}
1 & -1 & 1 & 3 \\
0 & 1 & 2 & 4 \\
0 & 0 & 1 & 2
\end{array}
\right]
$$

### eliminasi gaus dalam bentuk python
```python
import numpy as np

def eliminasi_gauss(A):
    A = A.astype(float)
    n = len(A)

    for i in range(n):

        if A[i][i] == 0:
            for j in range(i+1, n):
                if A[j][i] != 0:
                    A[[i, j]] = A[[j, i]]
                    break

        pivot = A[i][i]
        A[i] = A[i] / pivot

        for j in range(i+1, n):
            faktor = A[j][i]
            A[j] = A[j] - faktor * A[i]

    return A```