# Matriks
## Aritmatika Matriks
## Aljabar Matriks
## Matriks Invertibel
## Determinan

## TUGAS 9 APRIL

Rumus invers:

$$
A^{-1}=\frac{1}{\det(A)}\cdot \operatorname{adj}(A)
$$

Jika:

$$
A=
\begin{bmatrix}
1 & 1 & 1 & 1 \\
2 & -1 & 1 & -1 \\
1 & 2 & -1 & 1 \\
3 & -1 & 2 & 1
\end{bmatrix}
$$

### Minor \(M_{11}\)

$$
M_{11}=
\begin{vmatrix}
-1 & 1 & -1 \\
2 & -1 & 1 \\
-1 & 2 & 1
\end{vmatrix}
$$

$$
=
(-1)
\begin{vmatrix}
-1 & 1 \\
2 & 1
\end{vmatrix}
-
1
\begin{vmatrix}
2 & 1 \\
-1 & 1
\end{vmatrix}
+
(-1)
\begin{vmatrix}
2 & -1 \\
-1 & 2
\end{vmatrix}
$$

$$
\begin{vmatrix}
-1 & 1 \\
2 & 1
\end{vmatrix}
=
(-1)(1)-(1)(2)=-3
$$

$$
\begin{vmatrix}
2 & 1 \\
-1 & 1
\end{vmatrix}
=
(2)(1)-(1)(-1)=3
$$

$$
\begin{vmatrix}
2 & -1 \\
-1 & 2
\end{vmatrix}
=
(2)(2)-(-1)(-1)=3
$$

$$
M_{11}=(-1)(-3)-1(3)+(-1)(3)=-3
$$

$$
C_{11}=(-1)^{1+1}M_{11}=-3
$$

$$
\det(A)=13
$$

$$
A^{-1}=
\frac{1}{13}
\begin{bmatrix}
-3 & 3 & 4 & 2 \\
9 & 4 & 1 & -6 \\
11 & 2 & -6 & -3 \\
-4 & -9 & 1 & 7
\end{bmatrix}
$$

$$
A^{-1}=
\begin{bmatrix}
-\frac{3}{13} & \frac{3}{13} & \frac{4}{13} & \frac{2}{13} \\
\frac{9}{13} & \frac{4}{13} & \frac{1}{13} & -\frac{6}{13} \\
\frac{11}{13} & \frac{2}{13} & -\frac{6}{13} & -\frac{3}{13} \\
-\frac{4}{13} & -\frac{9}{13} & \frac{1}{13} & \frac{7}{13}
\end{bmatrix}
$$

---

## TUGAS 23 APRIL 2026

### Soal 1

$$
A=
\begin{bmatrix}
-7 & -5 \\
1 & 4
\end{bmatrix}
$$

$$
\det(A)=(-7)(4)-(-5)(1)=-23
$$

---

### Soal 2

$$
A=
\begin{bmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{bmatrix}
$$

$$
\det(A)=
\begin{vmatrix}
0 & 2 \\
1 & -2
\end{vmatrix}
=-2
$$

---

### Soal 3

$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{bmatrix}
$$

Gunakan operasi baris:

$$
R_1 \leftarrow R_1+R_2+R_3+R_4
$$

$$
R_1=(0,0,0,0)
$$

Sehingga:

$$
\det(A)=0
$$

---

## Invers Matriks

### Nomor 4

$$
A=
\begin{bmatrix}
-7 & -5 \\
1 & 4
\end{bmatrix}
$$

$$
A^{-1}=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
$$

---

### Nomor 5

$$
A=
\begin{bmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{bmatrix}
$$

$$
A^{-1}=
\begin{bmatrix}
1 & 1 & 4 \\
\frac{1}{2} & 0 & \frac{3}{2} \\
0 & 0 & 1
\end{bmatrix}
$$
