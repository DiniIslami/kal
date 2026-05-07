# Matriks
## aritmatika matriks
## aljabar matiks
## matriks invertibel
## determinan
### TUGAS 9 APRIL
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
$

dimana determinan mengekspansi baris pertama:

$
\text{Minor } M_{11}
$

$
M_{11}=
\begin{vmatrix}
-1 & 1 & -1 \\
2 & -1 & 1 \\
-1 & 2 & 1
\end{vmatrix}
$

$
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
$

$
\begin{vmatrix}
-1 & 1 \\
2 & 1
\end{vmatrix}
=
(-1)(1)-(1)(2)=-1-2=-3
$

$
\begin{vmatrix}
2 & 1 \\
-1 & 1
\end{vmatrix}
=
(2)(1)-(1)(-1)=2+1=3
$

$
\begin{vmatrix}
2 & -1 \\
-1 & 2
\end{vmatrix}
=
(2)(2)-(-1)(-1)=4-1=3
$

$
M_{11}=(-1)(-3)-1(3)+(-1)(3)
$

$
=3-3-3=-3
$

$
C_{11}=(-1)^{1+1}M_{11}=(+1)(-3)=-3
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

### TUGAS TANGGAL 23 APRIL 2026
### SOAL
A. Hitunglah determinan matrik berikut dengan menggunakan rumus expansi baris

$
\sum_{k=1}^{n} (-1)^{i+k} a_{ik} M_{ik}
$

dengan M_{ij}
 adalah minior dari matrik A dan

$
M_{ij} = \det(A_{ij})
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

## JAWABAN
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

3. 
\textbf{Diketahui}

$
A=
\begin{bmatrix}
1 & -3 & 1 & 1 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{bmatrix}
$

Rumus ekspansi baris:

$
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
$

dengan

$
M_{ik}=\det(A_{ik})
$

\textbf{Langkah 1: Operasi baris}

Gunakan operasi baris:

$
R_1 \leftarrow R_1+R_2+R_3+R_4
$

Maka:

$
\begin{aligned}
R_1 &=
(1+(-3)+1+1,\;
-3+1+1+1,\;
1+1+(-3)+1,\;
1+1+1+(-3)) \\
&=
(0,0,0,0)
\end{aligned}
$

Sehingga matriks menjadi

$
A=
\begin{bmatrix}
0 & 0 & 0 & 0 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{bmatrix}
$

Karena operasi penjumlahan baris tidak mengubah determinan, maka nilai determinan tetap sama.

\textbf{Langkah 2: Ekspansi baris pertama}

Ekspansi pada baris pertama:

$
\det(A)=
\sum_{k=1}^{4}(-1)^{1+k}a_{1k}M_{1k}
$

Karena semua elemen baris pertama adalah nol:

$
a_{11}=0,\quad a_{12}=0,\quad a_{13}=0,\quad a_{14}=0
$

Maka:

$
\begin{aligned}
\det(A)
&=
(-1)^{1+1}(0)M_{11}
+(-1)^{1+2}(0)M_{12}
+(-1)^{1+3}(0)M_{13}
+(-1)^{1+4}(0)M_{14} \\
&=
0+0+0+0 \\
&=
0
\end{aligned}
$

$
\boxed{\det(A)=0}
$

B. Gunakan rumus matriks adjoin untuk menghitung invers dari matriks berikut dengan rumus
(\operatorname{adj} A)_{ij} = (-1)^{i+j} M_{ji}
dan
A^{-1} = \frac{1}{\det A} \operatorname{adj} A.

4. 
$
A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}
$

5. 
$
A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}
$

6.
$
A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}.
$

### jawaban
4. 
\textbf{Diketahui}

$
A=
\begin{bmatrix}
-7 & -5 \\
1 & 4
\end{bmatrix}
$

Gunakan rumus:

$
(\operatorname{adj}A)_{ij}=(-1)^{i+j}M_{ji}
$

dan

$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$

\textbf{Langkah 1: Hitung determinan}

Untuk matriks

$
A=
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$

determinan adalah

$
\det(A)=ad-bc
$

Substitusi nilai:

$
\det(A)=(-7)(4)-(-5)(1)
$

$
\det(A)=-28+5=-23
$

\textbf{Langkah 2: Hitung minor setiap elemen}

$
M_{11}=4
$

$
M_{12}=1
$

$
M_{21}=-5
$

$
M_{22}=-7
$

\textbf{Langkah 3: Hitung matriks kofaktor}

$
C_{ij}=(-1)^{i+j}M_{ij}
$

Maka:

$
C_{11}=(-1)^{1+1}M_{11}=4
$

$
C_{12}=(-1)^{1+2}M_{12}=-1
$

$
C_{21}=(-1)^{2+1}M_{21}=5
$

$
C_{22}=(-1)^{2+2}M_{22}=-7
$

Sehingga matriks kofaktor:

$
C=
\begin{bmatrix}
4 & -1 \\
5 & -7
\end{bmatrix}
$

\textbf{Langkah 4: Hitung matriks adjoin}

Adjoin adalah transpose dari matriks kofaktor:

$
\operatorname{adj}(A)=C^T
$

$
\operatorname{adj}(A)=
\begin{bmatrix}
4 & 5 \\
-1 & -7
\end{bmatrix}
$

\textbf{Langkah 5: Hitung invers}

$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$

$
A^{-1}=\frac{1}{-23}
\begin{bmatrix}
4 & 5 \\
-1 & -7
\end{bmatrix}
$

$
A^{-1}=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
$

$
\boxed{
A^{-1}=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
}
$

5. 
\textbf{Diketahui}

$
A=
\begin{bmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{bmatrix}
$

Gunakan rumus:

$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$

$
(\operatorname{adj}A)_{ij}=(-1)^{i+j}M_{ji}
$

\textbf{Langkah 1: Hitung determinan}

Ekspansi pada baris ketiga:

$
\det(A)=
0\cdot M_{31}
+
0\cdot M_{32}
+
1\cdot M_{33}
$

Karena hanya elemen terakhir yang tidak nol, maka

$
\det(A)=
\begin{vmatrix}
0 & 2 \\
1 & -2
\end{vmatrix}
$

$
\det(A)=
(0)(-2)-(2)(1)
$

$
\det(A)=-2
$

\textbf{Langkah 2: Hitung minor dan kofaktor}

$
M_{11}=
\begin{vmatrix}
-2 & -1 \\
0 & 1
\end{vmatrix}
=-2
$

$
M_{12}=
\begin{vmatrix}
1 & -1 \\
0 & 1
\end{vmatrix}
=1
$

$
M_{13}=
\begin{vmatrix}
1 & -2 \\
0 & 0
\end{vmatrix}
=0
$

$
M_{21}=
\begin{vmatrix}
2 & -3 \\
0 & 1
\end{vmatrix}
=2
$

$
M_{22}=
\begin{vmatrix}
0 & -3 \\
0 & 1
\end{vmatrix}
=0
$

$
M_{23}=
\begin{vmatrix}
0 & 2 \\
0 & 0
\end{vmatrix}
=0
$

$
M_{31}=
\begin{vmatrix}
2 & -3 \\
-2 & -1
\end{vmatrix}
=(2)(-1)-(-3)(-2)
=-2-6=-8
$

$
M_{32}=
\begin{vmatrix}
0 & -3 \\
1 & -1
\end{vmatrix}
=(0)(-1)-(-3)(1)=3
$

$
M_{33}=
\begin{vmatrix}
0 & 2 \\
1 & -2
\end{vmatrix}
=(0)(-2)-(2)(1)=-2
$

\textbf{Langkah 3: Matriks kofaktor}

$
C_{ij}=(-1)^{i+j}M_{ij}
\]

\[
C=
\begin{bmatrix}
-2 & -1 & 0 \\
-2 & 0 & 0 \\
-8 & -3 & -2
\end{bmatrix}
\]

\textbf{Langkah 4: Matriks adjoin}

Transpose matriks kofaktor:

\[
\operatorname{adj}(A)=C^T
\]

\[
\operatorname{adj}(A)=
\begin{bmatrix}
-2 & -2 & -8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
\]

\textbf{Langkah 5: Invers matriks}

\[
A^{-1}=
\frac{1}{-2}
\begin{bmatrix}
-2 & -2 & -8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
\]

\[
A^{-1}=
\begin{bmatrix}
1 & 1 & 4 \\
\frac{1}{2} & 0 & \frac{3}{2} \\
0 & 0 & 1
\end{bmatrix}
\]

\[
\boxed{
A^{-1}=
\begin{bmatrix}
1 & 1 & 4 \\
\frac{1}{2} & 0 & \frac{3}{2} \\
0 & 0 & 1
\end{bmatrix}
}
\]

# Tugas
Buat matrik tranformasi dari:
<iframe src="https://www.geogebra.org/calculator/jxrvcyu6?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

Dari gambar, koordinat titik:
- A = (2, 3)
- B = (2, 1)
- C = (4, 1)

---

Diketahui:
A = (2,3)

---

## 1. Transformasi A ke B

Perpindahan:
(2,3) → (2,1)

$$
\begin{bmatrix}
1 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
3
\end{bmatrix}
=
\begin{bmatrix}
(1 \cdot 2 + 0 \cdot 3) \\
(2 \cdot 2 + (-1) \cdot 3)
\end{bmatrix}
=
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$

---

## 2. Transformasi B ke C

Perpindahan:
(2,1) → (4,1)

$$
\begin{bmatrix}
2 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
2 \\
1
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 1) \\
(0 \cdot 2 + 1 \cdot 1)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
1
\end{bmatrix}
$$

---

## 3. Transformasi A ke C

Perpindahan:
(2,3) → (4,1)

$$
\begin{bmatrix}
2 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
3
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 3) \\
(2 \cdot 2 + (-1) \cdot 3)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
1
\end{bmatrix}
$$


Diketahui:
D = (2,4)

---

## 1. Transformasi D ke E

Perpindahan:
(2,4) → (2,0)

$$
\begin{bmatrix}
1 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
4
\end{bmatrix}
=
\begin{bmatrix}
(1 \cdot 2 + 0 \cdot 4) \\
(2 \cdot 2 + (-1) \cdot 4)
\end{bmatrix}
=
\begin{bmatrix}
2 \\
0
\end{bmatrix}
$$

---

## 2. Transformasi E ke F

Perpindahan:
(2,0) → (4,0)

$$
\begin{bmatrix}
2 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
2 \\
0
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 0) \\
(0 \cdot 2 + 1 \cdot 0)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
0
\end{bmatrix}
$$

---

## 3. Transformasi D ke F

Perpindahan:
(2,4) → (4,0)

$$
\begin{bmatrix}
2 & 0 \\
2 & -1
\end{bmatrix}
\begin{bmatrix}
2 \\
4
\end{bmatrix}
=
\begin{bmatrix}
(2 \cdot 2 + 0 \cdot 4) \\
(2 \cdot 2 + (-1) \cdot 4)
\end{bmatrix}
=
\begin{bmatrix}
4 \\
0
\end{bmatrix}
$$


## tugas tanggal 07 mei 2026

https://colab.research.google.com/drive/1A2ccOgG8aB-PJr7eZNsEtjFGKB_yNS-G?usp=sharing

# Penjelasan Program Transformasi Geometri dengan Python

Program ini digunakan untuk membuat animasi transformasi geometri menggunakan Python.

Transformasi yang digunakan:

1. Translasi (pergeseran)
2. Refleksi / pencerminan terhadap sumbu-x

Library yang digunakan:

- NumPy → operasi matriks
- Matplotlib → membuat grafik dan animasi

---

# 1. Import Library

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
from IPython.display import HTML
```

Penjelasan:

- `numpy` digunakan untuk operasi matriks dan koordinat.
- `matplotlib.pyplot` digunakan untuk membuat grafik.
- `FuncAnimation` digunakan untuk membuat animasi.
- `HTML` digunakan agar animasi tampil di notebook `.ipynb`.

---

# 2. Membuat Objek Awal

```python
objek = np.array([
    [2, 3],
    [2, 4],
    [3, 4],
    [3, 3],
    [2, 3]
])
```

Objek berbentuk persegi dengan titik:

- A(2,3)
- B(2,4)
- C(3,4)
- D(3,3)

Titik pertama diulang agar garis kembali ke titik awal sehingga bangun tertutup.

---

# 3. Matriks Refleksi

```python
R = np.array([
    [1,  0],
    [0, -1]
])
```

Matriks refleksi terhadap sumbu-x:

$$
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$$

Rumus refleksi:

$$
(x,y) \rightarrow (x,-y)
$$

Artinya:

- koordinat x tetap
- koordinat y berubah tanda

Contoh:

$$
(2,3) \rightarrow (2,-3)
$$

---

# 4. Fungsi Translasi

```python
def T(tx, ty):
```

Fungsi ini membuat matriks translasi:

$$
\begin{bmatrix}
1 & 0 & t_x \\
0 & 1 & t_y \\
0 & 0 & 1
\end{bmatrix}
$$

Rumus translasi:

$$
(x,y) \rightarrow (x+t_x,\ y+t_y)
$$

Keterangan:

- `tx` = pergeseran horizontal
- `ty` = pergeseran vertikal

---

# 5. Koordinat Homogen

```python
def ke_homogen(obj):
```

Digunakan untuk mengubah koordinat biasa:

$$
(x,y)
$$

menjadi koordinat homogen:

$$
(x,y,1)
$$

Tujuannya agar translasi dapat dilakukan menggunakan perkalian matriks.

---

# 6. Fungsi update(frame)

```python
def update(frame):
```

Fungsi ini merupakan inti animasi.

Fungsi akan dijalankan terus-menerus untuk setiap frame animasi.

---

# 7. Gerakan Translasi

```python
ty = (frame / (total_frames - 1)) * max_translation
```

Nilai `ty` berubah setiap frame sehingga objek bergerak perlahan.

Karena:

```python
max_translation = -2.0
```

maka objek bergerak turun sejauh 2 satuan.

Transformasi:

$$
(x,y) \rightarrow (x,y-2)
$$

---

# 8. Translasi Objek Asli

```python
asli = (T(0, ty) @ obj_h.T).T
```

Objek asli bergerak turun secara vertikal.

Contoh:

$$
(2,3) \rightarrow (2,1)
$$

---

# 9. Refleksi terhadap Sumbu-x

```python
refleksi_awal = (R @ objek.T).T
```

Objek dicerminkan terhadap sumbu-x.

Contoh:

$$
(2,3) \rightarrow (2,-3)
$$

---

# 10. Gerakan Bayangan Refleksi

```python
refleksi = (T(0, -ty) @ refleksi_h.T).T
```

Bayangan refleksi bergerak berlawanan arah dengan objek asli.

Jika objek asli turun, maka bayangan bergerak naik.

Hal ini membuat animasi tetap simetris terhadap sumbu-x.

---

# 11. Menggambar Objek

```python
ax.plot(...)
```

Digunakan untuk menggambar:

- objek asli (warna biru)
- bayangan refleksi (warna merah)

---

# 12. Label Koordinat

```python
gambar_label(...)
```

Digunakan untuk menampilkan koordinat setiap titik pada grafik.

Contoh:

$$
(2,3)
$$

---

# 13. Membuat Animasi

```python
anim = FuncAnimation(...)
```

Keterangan:

- `frames=15` → jumlah frame animasi
- `interval=300` → jeda antar frame (300 ms)
- `repeat=True` → animasi diulang terus-menerus

---

# 14. Menampilkan Animasi

```python
HTML(anim.to_jshtml())
```

Digunakan agar animasi tampil langsung pada notebook `.ipynb`.

---

# Kesimpulan

Program ini menerapkan konsep transformasi geometri berupa:

## Refleksi terhadap sumbu-x

$$
(x,y) \rightarrow (x,-y)
$$

## Translasi

$$
(x,y) \rightarrow (x+t_x,\ y+t_y)
$$

## Matriks Refleksi

$$
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$$

## Matriks Translasi Homogen

$$
\begin{bmatrix}
1 & 0 & t_x \\
0 & 1 & t_y \\
0 & 0 & 1
\end{bmatrix}
$$

Dengan menggunakan transformasi tersebut, objek dapat bergerak dan dicerminkan secara animasi pada bidang koordinat.
