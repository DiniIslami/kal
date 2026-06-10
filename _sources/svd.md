# SINGULAR VALUE DECOMPOTION (SVD)

Singular Value Decomposition (SVD) adalah teknik faktorisasi matriks untuk menguraikan sebuah matriks menjadi tiga matriks lainnya, mengungkapkan aspek penting dari struktural matriks aslinya. SVD digunakan dalam berbagai aplikasi, termasuk pemrosesan sinyal, kompresi gambar, dan reduksi dimensi dalam machine learning.

Materi ini mengasumsikan kita memiliki pengetahuan dasar aljabar linear. Secara lebih spesifik, dan juga harus familiar dengan konsep-konsep seperti norma vektor dan matriks, rank matriks, dekomposisi eigen (vektor eigen dan nilai eigen), vektor ortonormal, dan proyeksi linear.

## DEFINISI MATEMATIS

Dekomposisi nilai singular dari matriks riil $A$ berukuran $m \times n$ adalah faktorisasi berbentuk:

$$
A = U\Sigma V^T
$$

dengan:

* $U$ adalah matriks ortogonal berukuran $m \times m$ (yaitu, kolom dan barisnya adalah vektor ortonormal). Kolom-kolom $U$ disebut vektor singular kiri dari $A$.

* $\Sigma$ adalah matriks diagonal persegi panjang berukuran $m \times n$ dengan bilangan riil non-negatif pada diagonalnya. Entri diagonal $\Sigma$ dikenal sebagai nilai singular dari $A$ dan biasanya disusun dalam urutan menurun, yaitu

$$
\sigma_1 \ge \sigma_2 \ge \cdots \ge \sigma_r > 0
$$

Jumlah nilai singular yang tidak nol sama dengan rank dari $A$.

* $V$ adalah matriks ortogonal berukuran $n \times n$. Kolom-kolom $V$ disebut vektor singular kanan dari $A$.

## ALGORITMA SVD

### Langkah 1: Menghitung Vektor Singular Kiri

* Hitung matriks $AA^T$ (berukuran $m \times m$)
* Cari nilai-nilai eigen dari $AA^T$
* $\operatorname{Rank}(A)=k$ = banyaknya nilai eigen yang tidak nol
* Nilai eigen ini akan digunakan untuk mendapatkan vektor-vektor kiri

### Langkah 2: Membentuk Matriks $U$

* Tentukan vektor eigen

$$
\mathbf{u}_1,\mathbf{u}_2,\ldots,\mathbf{u}_m
$$

yang berkorespondensi dengan nilai eigen dari $AA^T$.

* Normalisasi setiap vektor eigen:

$$
\mathbf{u}_i=\frac{\mathbf{u}_i}{|\mathbf{u}_i|}
$$

* Susun vektor-vektor ini sebagai kolom matriks $U$ (berukuran $m \times m$).

### Langkah 3: Menghitung Vektor Singular Kanan dan Nilai Singular

* Hitung matriks $A^TA$ (berukuran $n \times n$)
* Cari nilai-nilai eigen dari $A^TA$
* Nilai singular $\sigma_i$ adalah akar dari nilai eigen:

$$
\sigma_i=\sqrt{\lambda_i}
$$

di mana $\lambda_i$ adalah nilai eigen dari $A^TA$.

### Langkah 4: Membentuk Matriks $V$

* Tentukan vektor eigen

$$
\mathbf{v}_1,\mathbf{v}_2,\ldots,\mathbf{v}_n
$$

dari $A^TA$.

* Normalisasi setiap vektor eigen
* Susun sebagai kolom matriks $V$ (berukuran $n \times n$)
* Transpose menjadi $V^T$

### Langkah 5: Membentuk Matriks $\Sigma$

* Buat matriks $\Sigma$ berukuran $m \times n$
* Elemen diagonal berisi nilai singular

$$
\sigma_1,\sigma_2,\ldots,\sigma_k
$$

* Urutkan dari besar ke kecil:

$$
\sigma_1 \ge \sigma_2 \ge \cdots \ge \sigma_k > 0
$$

* Elemen di luar diagonal = 0

### Langkah 6: Hasil Dekomposisi

Matriks $A$ dapat direkonstruksi sebagai:

$$
A = U\Sigma V^T
$$

## Contoh

Matriks:

$$
A=
\begin{bmatrix}
3&1&1\
-1&3&1
\end{bmatrix}
$$

(matriks berukuran $2\times3$)

Carilah SVD dari matriks di atas.

### 1. Menghitung $AA^T$

$$
AA^T=
\begin{bmatrix}
3&1&1\
-1&3&1
\end{bmatrix}
\begin{bmatrix}
3&-1\
1&3\
1&1
\end{bmatrix}
$$

### 2. Mencari Nilai Eigen dari $AA^T$

Persamaan karakteristik:

$$
\det(AA^T-\lambda I)=0
$$

$$
\det
\begin{bmatrix}
11-\lambda&1\
1&11-\lambda
\end{bmatrix}=0
$$

$$
(11-\lambda)^2-1=0
$$

$$
\lambda^2-22\lambda+120=0
$$

$$
(\lambda-12)(\lambda-10)=0
$$

Nilai eigen:

$$
\lambda_1=12,\qquad
\lambda_2=10
$$

Rank$(A)=2$ karena ada dua nilai eigen tidak nol.

### 3. Menentukan Matriks $U$

Untuk mencari vektor eigen, selesaikan:

$$
(\lambda I-AA^T)\mathbf{x}=0
$$

$$
\begin{bmatrix}
\lambda-11&-1\
-1&\lambda-11
\end{bmatrix}
\begin{bmatrix}
x_1\
x_2
\end{bmatrix}
=============

\begin{bmatrix}
0\
0
\end{bmatrix}
$$

#### Untuk $\lambda_1=12$

$$
\begin{bmatrix}
1&-1\
-1&1
\end{bmatrix}
\begin{bmatrix}
x_1\
x_2
\end{bmatrix}
=============

\begin{bmatrix}
0\
0
\end{bmatrix}
$$

$$
x_1-x_2=0
\Rightarrow
x_1=x_2
$$

$$
\mathbf{u}_1=
\begin{bmatrix}
1\
1
\end{bmatrix}
$$

$$
|\mathbf{u}_1|=\sqrt{2}
$$

$$
\mathbf{u}_1=
\begin{bmatrix}
\frac1{\sqrt2}\
\frac1{\sqrt2}
\end{bmatrix}
$$

#### Untuk $\lambda_2=10$

$$
\begin{bmatrix}
-1&-1\
-1&-1
\end{bmatrix}
\begin{bmatrix}
x_1\
x_2
\end{bmatrix}
=============

\begin{bmatrix}
0\
0
\end{bmatrix}
$$

$$
-x_1-x_2=0
\Rightarrow
x_1=-x_2
$$

$$
\mathbf{u}_2=
\begin{bmatrix}
1\
-1
\end{bmatrix}
$$

$$
|\mathbf{u}_2|=\sqrt2
$$

$$
\mathbf{u}_2=
\begin{bmatrix}
\frac1{\sqrt2}\
-\frac1{\sqrt2}
\end{bmatrix}
$$

Matriks $U$:

$$
U=
\begin{bmatrix}
\frac1{\sqrt2}&\frac1{\sqrt2}\
\frac1{\sqrt2}&-\frac1{\sqrt2}
\end{bmatrix}
$$

Nilai singular:

$$
\sigma_1=\sqrt{12}=2\sqrt3
$$

$$
\sigma_2=\sqrt{10}
$$

Perhitungan $A^TA$:

$$
A^TA=
\begin{bmatrix}
3&-1\
1&3\
1&1
\end{bmatrix}
\begin{bmatrix}
3&1&1\
-1&3&1
\end{bmatrix}
$$

$$
A^TA=
\begin{bmatrix}
10&0&2\
0&10&4\
2&4&2
\end{bmatrix}
$$

Nilai singular:

$$
\sigma_1=\sqrt{12}=2\sqrt3\approx3.464
$$

$$
\sigma_2=\sqrt{10}\approx3.162
$$

### 4. Vektor-vektor Eigen $\mathbf{v}_1,\mathbf{v}_2,\mathbf{v}_3$

Untuk mencari vektor eigen:

$$
(A^TA-\lambda I)\mathbf{v}=\mathbf0
$$

dengan

$$
A^TA=
\begin{bmatrix}
10&0&2\
0&10&4\
2&4&2
\end{bmatrix}
$$

#### a. Mencari $\mathbf{v}_1$ untuk $\lambda_1=12$

$$
(A^TA-12I)\mathbf{v}_1=\mathbf0
$$

$$
\mathbf{v}_1=
\begin{bmatrix}
1\
2\
1
\end{bmatrix}
$$

#### b. Mencari $\mathbf{v}_2$ untuk $\lambda_2=10$

$$
(A^TA-10I)\mathbf{v}_2=\mathbf0
$$

$$
\mathbf{v}_2=
\begin{bmatrix}
2\
-1\
0
\end{bmatrix}
$$

#### c. Mencari $\mathbf{v}_3$ untuk $\lambda_3=0$

$$
(A^TA)\mathbf{v}_3=\mathbf0
$$

$$
\mathbf{v}_3=
\begin{bmatrix}
1\
2\
-5
\end{bmatrix}
$$

## PROSES NORMALISASI DAN PEMBENTUKAN MATRIKS $V$

### 1. Normalisasi $\mathbf{v}_1=[1,2,1]^T$

$$
|\mathbf{v}_1|=\sqrt6
$$

$$
\hat{\mathbf{v}}_1=
\frac1{\sqrt6}
\begin{bmatrix}
1\
2\
1
\end{bmatrix}
$$

### 2. Normalisasi $\mathbf{v}_2=[2,-1,0]^T$

$$
|\mathbf{v}_2|=\sqrt5
$$

$$
\hat{\mathbf{v}}_2=
\frac1{\sqrt5}
\begin{bmatrix}
2\
-1\
0
\end{bmatrix}
$$

### 3. Normalisasi $\mathbf{v}_3=[1,2,-5]^T$

$$
|\mathbf{v}_3|=\sqrt{30}
$$

$$
\hat{\mathbf{v}}_3=
\frac1{\sqrt{30}}
\begin{bmatrix}
1\
2\
-5
\end{bmatrix}
$$

Membentuk matriks $V$:

$$
V=
\begin{bmatrix}
\frac1{\sqrt6}&\frac2{\sqrt5}&\frac1{\sqrt{30}}\
\frac2{\sqrt6}&-\frac1{\sqrt5}&\frac2{\sqrt{30}}\
\frac1{\sqrt6}&0&-\frac5{\sqrt{30}}
\end{bmatrix}
$$

Matriks $V^T$:

$$
V^T=
\begin{bmatrix}
\frac1{\sqrt6}&\frac2{\sqrt6}&\frac1{\sqrt6}\
\frac2{\sqrt5}&-\frac1{\sqrt5}&0\
\frac1{\sqrt{30}}&\frac2{\sqrt{30}}&-\frac5{\sqrt{30}}
\end{bmatrix}
$$


## Perhitungan dengan SageMath

<div id="sagecell">
<script type="text/x-sage">
A = matrix([
[-7,-5],
[1,4]
])

show(A.det())
show(A.inverse())
</script>
</div>

<script src="https://sagecell.sagemath.org/static/embedded_sagecell.js"></script>

<script>
sagecell.makeSagecell({
    inputLocation: '#sagecell',
    evalButtonText: 'Hitung'
});
</script>