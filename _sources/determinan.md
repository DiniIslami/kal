# TUGAS TANGGAL 23 APRIL 2026

## SOAL

### A. Hitunglah determinan matriks berikut dengan menggunakan rumus ekspansi baris

$$
\sum_{k=1}^{n} (-1)^{i+k} a_{ik} M_{ik}
$$

dengan $M_{ij}$ adalah minor dari matriks $A$ dan

$$
M_{ij}=\det(A_{ij})
$$

$A_{ij}$ adalah submatriks dengan menghapus baris $i$ dan kolom $j$ dari matriks $A_{m\times n}$ dengan

$$
1\le i,j\le n
$$

### 1.

$$
A=
\begin{bmatrix}
-7 & -5\
1 & 4
\end{bmatrix}
$$

### 2.

$$
A=
\begin{bmatrix}
0 & 2 & -3\
1 & -2 & -1\
0 & 0 & 1
\end{bmatrix}
$$

### 3.

$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1\
-3 & 1 & 1 & 1\
1 & 1 & -3 & 1\
1 & 1 & 1 & -3
\end{bmatrix}
$$

---

## JAWABAN

### 1.

$$
A=
\begin{bmatrix}
-7 & -5\
1 & 4
\end{bmatrix}
$$

Dengan menggunakan rumus ekspansi baris pada baris pertama:

$$
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
$$

Untuk baris pertama $(i=1)$, maka

$$
\det(A)=(-1)^{1+1}a_{11}M_{11}+(-1)^{1+2}a_{12}M_{12}
$$

Cari minor:

$$
M_{11}=
\begin{vmatrix}
4
\end{vmatrix}
=4
$$

$$
M_{12}=
\begin{vmatrix}
1
\end{vmatrix}
=1
$$

Substitusikan ke rumus:

$$
\det(A)=(-1)^{1+1}(-7)(4)+(-1)^{1+2}(-5)(1)
$$

$$
=(1)(-28)+(-1)(-5)
$$

$$
=-28+5
$$

$$
=-23
$$

Jadi,

$$
\boxed{\det(A)=-23}
$$

---

### 2.

$$
A=
\begin{bmatrix}
0 & 2 & -3\
1 & -2 & -1\
0 & 0 & 1
\end{bmatrix}
$$

Gunakan rumus ekspansi baris pada baris ke-3:

$$
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
$$

Untuk $(i=3)$:

$$
\det(A)=(-1)^{3+1}a_{31}M_{31}+(-1)^{3+2}a_{32}M_{32}+(-1)^{3+3}a_{33}M_{33}
$$

Substitusikan elemen-elemen pada baris ke-3:

$$
\det(A)=(-1)^4(0)M_{31}+(-1)^5(0)M_{32}+(-1)^6(1)M_{33}
$$

$$
\det(A)=0+0+(1)(1)M_{33}
$$

Cari minor $M_{33}$ dengan menghapus baris ke-3 dan kolom ke-3:

$$
M_{33}=
\begin{vmatrix}
0 & 2\
1 & -2
\end{vmatrix}
$$

$$
M_{33}=(0)(-2)-(2)(1)=-2
$$

Substitusikan kembali:

$$
\det(A)=1\cdot(-2)
$$

$$
\det(A)=-2
$$

Jadi,

$$
\boxed{\det(A)=-2}
$$

---

### 3.

**Diketahui**

$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1\
-3 & 1 & 1 & 1\
1 & 1 & -3 & 1\
1 & 1 & 1 & -3
\end{bmatrix}
$$

Rumus ekspansi baris:

$$
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
$$

dengan

$$
M_{ik}=\det(A_{ik})
$$

### Langkah 1: Operasi baris

Gunakan operasi baris:

$$
R_1\leftarrow R_1+R_2+R_3+R_4
$$

Maka

$$
\begin{aligned}
R_1
&=
(1+(-3)+1+1,;
-3+1+1+1,;
1+1+(-3)+1,;
1+1+1+(-3))
\
&=(0,0,0,0)
\end{aligned}
$$

Sehingga matriks menjadi

$$
A=
\begin{bmatrix}
0 & 0 & 0 & 0\
-3 & 1 & 1 & 1\
1 & 1 & -3 & 1\
1 & 1 & 1 & -3
\end{bmatrix}
$$

Karena operasi penjumlahan baris tidak mengubah determinan, maka nilai determinan tetap sama.

### Langkah 2: Ekspansi baris pertama

Ekspansi pada baris pertama:

$$
\det(A)=\sum_{k=1}^{4}(-1)^{1+k}a_{1k}M_{1k}
$$

Karena semua elemen baris pertama adalah nol:

$$
a_{11}=0,\quad
a_{12}=0,\quad
a_{13}=0,\quad
a_{14}=0
$$

Maka

$$
\begin{aligned}
\det(A)
&=
(-1)^{1+1}(0)M_{11}
+(-1)^{1+2}(0)M_{12}
+(-1)^{1+3}(0)M_{13}
+(-1)^{1+4}(0)M_{14}
\
&=
0+0+0+0
\
&=
0
\end{aligned}
$$

$$
\boxed{\det(A)=0}
$$

# B. Gunakan Rumus Matriks Adjoin untuk Menghitung Invers

Diketahui

$$
(\operatorname{adj}A)*{ij}=(-1)^{i+j}M*{ji}
$$

dan

$$
A^{-1}=\frac{1}{\det A}\operatorname{adj}A
$$

---

## 4.

**Diketahui**

$$
A=
\begin{bmatrix}
-7 & -5\
1 & 4
\end{bmatrix}
$$

Gunakan rumus:

$$
(\operatorname{adj}A)*{ij}=(-1)^{i+j}M*{ji}
$$

dan

$$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$$

### Langkah 1: Hitung determinan

Untuk matriks

$$
A=
\begin{bmatrix}
a & b\
c & d
\end{bmatrix}
$$

determinan adalah

$$
\det(A)=ad-bc
$$

Substitusi nilai:

$$
\det(A)=(-7)(4)-(-5)(1)
$$

$$
\det(A)=-28+5=-23
$$

### Langkah 2: Hitung minor setiap elemen

$$
M_{11}=4
$$

$$
M_{12}=1
$$

$$
M_{21}=-5
$$

$$
M_{22}=-7
$$

### Langkah 3: Hitung matriks kofaktor

$$
C_{ij}=(-1)^{i+j}M_{ij}
$$

Maka

$$
C_{11}=4
$$

$$
C_{12}=-1
$$

$$
C_{21}=5
$$

$$
C_{22}=-7
$$

Sehingga matriks kofaktor:

$$
C=
\begin{bmatrix}
4 & -1\
5 & -7
\end{bmatrix}
$$

### Langkah 4: Hitung matriks adjoin

Adjoin adalah transpose dari matriks kofaktor:

$$
\operatorname{adj}(A)=C^T
$$

$$
\operatorname{adj}(A)=
\begin{bmatrix}
4 & 5\
-1 & -7
\end{bmatrix}
$$

### Langkah 5: Hitung invers

$$
A^{-1}
======

\frac{1}{-23}
\begin{bmatrix}
4 & 5\
-1 & -7
\end{bmatrix}
$$

$$
A^{-1}
======

\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23}\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
$$

$$
\boxed{
A^{-1}
======

\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23}\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
}
$$

---

## 5.

**Diketahui**

$$
A=
\begin{bmatrix}
0 & 2 & -3\
1 & -2 & -1\
0 & 0 & 1
\end{bmatrix}
$$

Gunakan rumus

$$
A^{-1}
======

\frac{1}{\det(A)}
\operatorname{adj}(A)
$$

dan

$$
(\operatorname{adj}A)_{ij}
==========================

(-1)^{i+j}M_{ji}
$$

### Langkah 1: Hitung determinan

Ekspansi pada baris ketiga:

$$
\det(A)
=======

0\cdot M_{31}
+
0\cdot M_{32}
+
1\cdot M_{33}
$$

Karena hanya elemen terakhir yang tidak nol, maka

$$
\det(A)
=======

\begin{vmatrix}
0 & 2\
1 & -2
\end{vmatrix}
$$

$$
\det(A)
=======

(0)(-2)-(2)(1)
$$

$$
\det(A)=-2
$$

### Langkah 2: Hitung minor dan kofaktor

$$
M_{11}
======

\begin{vmatrix}
-2 & -1\
0 & 1
\end{vmatrix}
=-2
$$

$$
M_{12}
======

\begin{vmatrix}
1 & -1\
0 & 1
\end{vmatrix}
=1
$$

$$
M_{13}
======

\begin{vmatrix}
1 & -2\
0 & 0
\end{vmatrix}
=0
$$

$$
M_{21}
======

\begin{vmatrix}
2 & -3\
0 & 1
\end{vmatrix}
=2
$$

$$
M_{22}
======

\begin{vmatrix}
0 & -3\
0 & 1
\end{vmatrix}
=0
$$

$$
M_{23}
======

\begin{vmatrix}
0 & 2\
0 & 0
\end{vmatrix}
=0
$$

$$
M_{31}
======

\begin{vmatrix}
2 & -3\
-2 & -1
\end{vmatrix}
=============

# (2)(-1)-(-3)(-2)

-8
$$

$$
M_{32}
======

\begin{vmatrix}
0 & -3\
1 & -1
\end{vmatrix}
=3
$$

$$
M_{33}
======

\begin{vmatrix}
0 & 2\
1 & -2
\end{vmatrix}
=-2
$$

### Langkah 3: Matriks kofaktor

$$
C=
\begin{bmatrix}
-2 & -1 & 0\
-2 & 0 & 0\
-8 & -3 & -2
\end{bmatrix}
$$

### Langkah 4: Matriks adjoin

$$
\operatorname{adj}(A)=C^T
$$

$$
\operatorname{adj}(A)=
\begin{bmatrix}
-2 & -2 & -8\
-1 & 0 & -3\
0 & 0 & -2
\end{bmatrix}
$$

### Langkah 5: Invers matriks

$$
A^{-1}
======

\frac{1}{-2}
\begin{bmatrix}
-2 & -2 & -8\
-1 & 0 & -3\
0 & 0 & -2
\end{bmatrix}
$$

$$
A^{-1}
======

\begin{bmatrix}
1 & 1 & 4\
\frac12 & 0 & \frac32\
0 & 0 & 1
\end{bmatrix}
$$

$$
\boxed{
A^{-1}
======

\begin{bmatrix}
1 & 1 & 4\
\frac12 & 0 & \frac32\
0 & 0 & 1
\end{bmatrix}
}
$$
