# Matriks
## aritmatika matriks
## aljabar matiks
## matriks invertibel
## determinan
rumus invers= 
$$
A^{-1} = \frac{1}{\det(A)} \cdot \operatorname{adj}(A)
$$
jika:
$$
A =
\begin{bmatrix}
1 & 1 & 1 & 1 \\
2 & -1 & 1 & -1 \\
1 & 2 & -1 & 1 \\
3 & -1 & 2 & 1
\end{bmatrix}
$$

dimana determinan mengekspansi baris pertama:

$
\text{Minor } M_{11}
$

$
M_{11}=
\begin{vmatrix}
-1 & 1 & -1\
2 & -1 & 1\
-1 & 2 & 1
\end{vmatrix}
$

$
-1
\begin{vmatrix}
-1 & 1\
2 & 1
\end{vmatrix}
-1
\begin{vmatrix}
2 & 1\
-1 & 1
\end{vmatrix}
+(-1)
\begin{vmatrix}
2 & -1\
-1 & 2
\end{vmatrix}
$

$
\begin{vmatrix}
-1 & 1\
2 & 1
\end{vmatrix}
=(-1)(1)-(1)(2)=-3
$

$
\begin{vmatrix}
2 & 1\
-1 & 1
\end{vmatrix}
=(2)(1)-(1)(-1)=3
$

$
\begin{vmatrix}
2 & -1\
-1 & 2
\end{vmatrix}
=(2)(2)-(-1)(-1)=3
$

$
M_{11}=(-1)(-3)-1(3)+(-1)(3)=3-3-3=-3
$

$
C_{11}=(+),M_{11}=-3
$

$
\det(A)=1(C_{11})+1(C_{12})+1(C_{13})+1(C_{14})
$

$
\det(A)=-3+9+11-4=13
$

$
\det(A)=13
$

$
A^{-1}=\frac{1}{\det(A)},\operatorname{adj}(A)
$

$
\text{karena } \det(A)=13
$

$
A^{-1}=\frac{1}{13}
\begin{pmatrix}
-3 & 3 & 4 & 2\
9 & 4 & 1 & -6\
11 & 2 & -6 & -3\
-4 & -9 & 1 & 7
\end{pmatrix}
$

$
A^{-1}=
\begin{pmatrix}
-\frac{3}{13} & \frac{3}{13} & \frac{4}{13} & \frac{2}{13}\
\frac{9}{13} & \frac{4}{13} & \frac{1}{13} & -\frac{6}{13}\
\frac{11}{13} & \frac{2}{13} & -\frac{6}{13} & -\frac{3}{13}\
-\frac{4}{13} & -\frac{9}{13} & \frac{1}{13} & \frac{7}{13}
\end{pmatrix}
$

## SOAL
A. Hitunglah determinan matrik berikut dengan menggunakan rumus expansi baris

$
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <munderover>
    <mo data-mjx-texclass="OP">&#x2211;</mo>
    <mrow data-mjx-texclass="ORD">
      <mi>k</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mi>n</mi>
  </munderover>
  <mo stretchy="false">(</mo>
  <mo>&#x2212;</mo>
  <mn>1</mn>
  <msup>
    <mo stretchy="false">)</mo>
    <mrow data-mjx-texclass="ORD">
      <mi>i</mi>
      <mo>+</mo>
      <mi>k</mi>
    </mrow>
  </msup>
  <msub>
    <mi>a</mi>
    <mrow data-mjx-texclass="ORD">
      <mi>i</mi>
      <mi>k</mi>
    </mrow>
  </msub>
  <msub>
    <mi>M</mi>
    <mrow data-mjx-texclass="ORD">
      <mi>i</mi>
      <mi>k</mi>
    </mrow>
  </msub>
</math>
$

dengan M_{ij}
 adalah minior dari matrik A dan

 $
 <math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <msub>
    <mi>M</mi>
    <mrow data-mjx-texclass="ORD">
      <mi>i</mi>
      <mi>j</mi>
    </mrow>
  </msub>
  <mo>=</mo>
  <mo data-mjx-texclass="OP" movablelimits="true">det</mo>
  <msub>
    <mi>A</mi>
    <mrow data-mjx-texclass="ORD">
      <mi>i</mi>
      <mi>j</mi>
    </mrow>
  </msub>
  <mo>.</mo>
</math>
$

A_{ij} adalah submatrik dengan menghapus baris i dan kolom kolom j dari matrix 
A_{mxn} dengan 1 \le i, j \le n

1. 
$
A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}
$

2. 
$
A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}
$

3. 
$
A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}.
$

JAWABAN
1. 
$
A=
\begin{bmatrix}
-7 & -5 \\
1 & 4
\end{bmatrix}
$

Dengan menggunakan rumus ekspansi baris pada baris pertama:

$
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
$

Untuk baris pertama \((i=1)\), maka:

$
\det(A)=(-1)^{1+1}a_{11}M_{11}+(-1)^{1+2}a_{12}M_{12}
$

Cari minor:

$
M_{11}=
\begin{vmatrix}
4
\end{vmatrix}
=4
$

$
M_{12}=
\begin{vmatrix}
1
\end{vmatrix}
=1
$

Substitusikan ke rumus:

$
\det(A)=(-1)^{1+1}(-7)(4)+(-1)^{1+2}(-5)(1)
$

$
=(1)(-28)+(-1)(-5)
$

$
=-28+5
$

$
=-23
$

Jadi,

$
\boxed{\det(A)=-23}
$

2. 
$
A=
\begin{bmatrix}
0 & 2 & -3 \
1 & -2 & -1 \
0 & 0 & 1
\end{bmatrix}
$

Gunakan rumus ekspansi baris pada baris ke-3:

$
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
$

Untuk (i=3), maka:

$
\det(A)=(-1)^{3+1}a_{31}M_{31}+(-1)^{3+2}a_{32}M_{32}+(-1)^{3+3}a_{33}M_{33}
$

Substitusikan elemen-elemen pada baris ke-3:

$
\det(A)=(-1)^4(0)M_{31}+(-1)^5(0)M_{32}+(-1)^6(1)M_{33}
$

$
\det(A)=0+0+(1)(1)M_{33}
$

Cari minor (M_{33}) dengan menghapus baris ke-3 dan kolom ke-3:

$
M_{33}=
\begin{vmatrix}
0 & 2 \
1 & -2
\end{vmatrix}
$

$
M_{33}=(0)(-2)-(2)(1)=-2
$

Substitusikan kembali:

$
\det(A)=1 \cdot (-2)
$

$
\det(A)=-2
$

Jadi,

$
\boxed{\det(A)=-2}
$

## 4. Menentukan Invers Matriks dengan Metode Adjoin

Diketahui:

$$
\begin{split}
A=
\begin{bmatrix}
-7 & -5 \\
1 & 4
\end{bmatrix}
\end{split}
$$

Gunakan rumus:

$$
\begin{split}
A^{-1}=\frac{1}{\det A}\,\text{adj}\,A
\end{split}
$$

---

### Langkah 1: Hitung determinan

$$
\begin{split}
\det(A)
=
(-7)(4)-(-5)(1)
\end{split}
$$

$$
\begin{split}
=
-28+5
\end{split}
$$

$$
\begin{split}
=
-23
\end{split}
$$

---

### Langkah 2: Tentukan adjoin matriks

Untuk matriks orde $2 \times 2$:

$$
\begin{split}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}^{-1}
=
\frac{1}{ad-bc}
\begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}
\end{split}
$$

Maka:

$$
\begin{split}
\text{adj}\,A=
\begin{bmatrix}
4 & 5 \\
-1 & -7
\end{bmatrix}
\end{split}
$$

---

### Langkah 3: Hitung invers

$$
\begin{split}
A^{-1}
=
\frac{1}{-23}
\begin{bmatrix}
4 & 5 \\
-1 & -7
\end{bmatrix}
\end{split}
$$

$$
\begin{split}
A^{-1}
=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{
A^{-1}
=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}}
\end{split}
$$

---

# 5. Menentukan Invers Matriks dengan Metode Adjoin

Diketahui:

$$
\begin{split}
A=
\begin{bmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{bmatrix}
\end{split}
$$

Determinan dari soal sebelumnya:

$$
\begin{split}
\det(A)=-2
\end{split}
$$

Gunakan rumus:

$$
\begin{split}
A^{-1}=\frac{1}{\det A}\,\text{adj}\,A
\end{split}
$$

---

### Hasil perhitungan adjoin

$$
\begin{split}
\text{adj}\,A=
\begin{bmatrix}
-2 & -2 & 8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
\end{split}
$$

---

### Hitung invers

$$
\begin{split}
A^{-1}
=
\frac{1}{-2}
\begin{bmatrix}
-2 & -2 & 8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
\end{split}
$$

$$
\begin{split}
A^{-1}
=
\begin{bmatrix}
1 & 1 & -4 \\
\frac{1}{2} & 0 & \frac{3}{2} \\
0 & 0 & 1
\end{bmatrix}
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{
A^{-1}
=
\begin{bmatrix}
1 & 1 & -4 \\
\frac{1}{2} & 0 & \frac{3}{2} \\
0 & 0 & 1
\end{bmatrix}}
\end{split}
$$

---

# 6. Menentukan Invers Matriks dengan Metode Adjoin

Diketahui:

$$
\begin{split}
A=
\begin{bmatrix}
1 & -3 & 1 & 1 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{bmatrix}
\end{split}
$$

Determinan dari soal sebelumnya:

$$
\begin{split}
\det(A)=-32
\end{split}
$$

Gunakan rumus:

$$
\begin{split}
A^{-1}=\frac{1}{\det A}\,\text{adj}\,A
\end{split}
$$

---

### Hasil invers

$$
\begin{split}
A^{-1}=
\begin{bmatrix}
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
0 & 0 & -\frac{1}{4} & 0 \\
0 & 0 & 0 & -\frac{1}{4}
\end{bmatrix}
\end{split}
$$

---

## Jawaban Akhir

$$
\begin{split}
\boxed{
A^{-1}=
\begin{bmatrix}
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
-\frac{1}{4} & -\frac{1}{4} & 0 & 0 \\
0 & 0 & -\frac{1}{4} & 0 \\
0 & 0 & 0 & -\frac{1}{4}
\end{bmatrix}}
\end{split}
$$