## **ELIMINASI GAUSSIAN**
Eliminasi Gaussian adalah algoritma untuk mengubah matriks menjadi bentuk eselon baris (REF). Bagian ini melengkapi pembahasan sistem persamaan linear dengan memberikan metode sistematis untuk menyederhanakan dan menyelesaikannya menggunakan matriks dan operasi baris.

Tujuan utama:

1. Mendefinisikan secara tepat apa yang dimaksud sistem yang “lebih sederhana”.

2. Memberikan algoritma yang jelas untuk mencapainya.

3. Menjelaskan bagaimana membaca solusi dari bentuk tersebut.

### **Contoh operasi baris dan eliminasi tiga variabel**

$$
\begin{cases}
x_1 - x_2 + x_3 = 3 \\
2x_1 + x_2 + 8x_3 = 18 \\
4x_1 + 2x_2 - 3x_3 = -2
\end{cases}
$$

dari persamaan diatas kita menggunakan tiga operasi dasar garis
1. rescale_row(i,a) fungsi: mengalikan baris ke-i dengan skalar a
2. add_multiple_of_row(i, j, a) fungsi: menambahkan a x (baris ke-j) ke baris ke-i
3. swap_rows (i,j) fungsi: menukar baris ke-i dengan baris ke-j

```python
A= matrix([[1, -1, 1, 3], [2, 1, 8, 18], [4, 2, -3, -2]])
#tambahkan -2 kali baris 0 ke baris 1
A.add_multiple_of_row(0,1,-2)
A.add_multiple_of_row(0, 2, -4)
A.add_multiple_of_row(1, 2, -2)
A.with_rescale_row(1, 1, 0/3)
A.with_rescale_row(2, 1, 0/-19)
```

$$
\begin{bmatrix}
1 & -1 & 1 & 3 \\
0 & 3 & 6 & 12 \\
4 & 2 & -3 & -2
\end{bmatrix}
$$

$$
\begin{bmatrix}
1 & -1 & 1 & 3 \\
0 & 3 & 6 & 12 \\
0 & 6 & -7 & -14
\end{bmatrix}
$$

$$
\begin{bmatrix}
1 & -1 & 1 & 3 \\
0 & 3 & 6 & 12 \\
0 & 0 & -19 & -38
\end{bmatrix}
$$

$$
\begin{bmatrix}
1 & -1 & 1 & 3 \\
0 & 1 & 2 & 4 \\
0 & 0 & -19 & -38
\end{bmatrix}
$$

$$
\begin{bmatrix}
1 & -1 & 1 & 3 \\
0 & 1 & 2 & 4 \\
0 & 0 & 1 & 2
\end{bmatrix}
$$

hasil matrix diatas diubah kembali menjadi sistem persamaaan

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <mtable displaystyle="true" columnalign="right" columnspacing="0em" rowspacing="3pt">
    <mtr>
      <mtd>
        <mtable displaystyle="true" columnalign="right center left" columnspacing="0em 0.278em" rowspacing="3pt">
          <mtr>
            <mtd>
              <msub>
                <mi>x</mi>
                <mn>1</mn>
              </msub>
              <mo>&#x2212;</mo>
              <msub>
                <mi>x</mi>
                <mn>2</mn>
              </msub>
              <mo>+</mo>
              <msub>
                <mi>x</mi>
                <mn>3</mn>
              </msub>
            </mtd>
            <mtd>
              <mi></mi>
              <mo>=</mo>
            </mtd>
            <mtd>
              <mn>3</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <msub>
                <mi>x</mi>
                <mn>2</mn>
              </msub>
              <mo>+</mo>
              <mn>2</mn>
              <msub>
                <mi>x</mi>
                <mn>3</mn>
              </msub>
            </mtd>
            <mtd>
              <mi></mi>
              <mo>=</mo>
            </mtd>
            <mtd>
              <mn>4</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <msub>
                <mi>x</mi>
                <mn>3</mn>
              </msub>
            </mtd>
            <mtd>
              <mi></mi>
              <mo>=</mo>
            </mtd>
            <mtd>
              <mn>2</mn>
            </mtd>
          </mtr>
        </mtable>
      </mtd>
    </mtr>
  </mtable>
</math>

dan dapat ditemukan bahwa:

$$
\begin{cases}
x_1 - x_2 + x_3 = 3 \\
x_2 + 2x_3 = 4 \\
x_3 = 2
\end{cases}
$$

 dapat diketahui bahwa X3=2 kita subtitusikan ke persamaan kedua

$$
x_2 + 2(2) = 4
$$

$$
x_2 = 0
$$

lalu  hasil X2 kita subtitusikan ke persamaan pertama

$$
\begin{aligned}
x_1 - 0 + 2 &= 3 \\
x_1 + 2 &= 3 \\
x_1 &= 3 - 2 \\
x_1 &= 1
\end{aligned}
$$

bentuk himpunan penyelesaiannya (1,0, 2)

### **contoh penyelesaian sistem persamaan empat variabel**

$$
\begin{cases}
x + y + z + w = 10 \\
2x + y + z + w = 13 \\
x + 2y + z + w = 14 \\
x + y + 2z + w = 15
\end{cases}
$$

**Penyelesaian:**
### 1. Ubah ke Matriks Augmented
1. Kode:
    ```python
    A = matrix([[1, 1, 1, 1, 10], [2, 1, 1, 1, 13], [1, 2, 1, 1, 14], [1, 1, 2, 1, 15]])
    A
2. Output:
    $$
    \begin{cases}
    x + y + z + w = 10 \\
    2x + y + z + w = 13 \\
    x + 2y + z + w = 14 \\
    x + y + 2z + w = 15
    \end{cases}
    $$

### 2. Eliminasi Gaussian (Operasi Baris Elementer)
1. Hilangkan elemen di bawah pivot pertama
    B2 → B2 − 2B1,
    B3 → B3 − B1,
    B4 → B4 − B1

    *Artinya:* Menghilangkan angka pertama agar jadi 0 dengan menggunakan **A.add_multiple_of_row** untuk melakukan perkalian kemudian penjumlahan.
    -  A.add_multiple_of_row(1, 0, -2) *Artinya:* Tambahkan -2* (baris 0) ke baris 1
    -  A.add_multiple_of_row(2, 0, -1) *Artinya:* Tambahkan -1* (baris 0) ke baris 2
    -  A.add_multiple_of_row(3, 0, -1) *Artinya:* Tambahkan -1* (baris 0) ke baris 3

        1. Kode:

            ```python
            A.add_multiple_of_row(1, 0, -2)
            A.add_multiple_of_row(2, 0, -1)
            A.add_multiple_of_row(3, 0, -1)
            A

        2. Output:

            $$
            \left[
            \begin{array}{cccc|c}
            1 & 1 & 1 & 1 & 10 \\
            0 & -1 & -1 & -1 & -7 \\
            0 & 1 & 0 & 0 & 4 \\
            0 & 0 & 1 & 0 & 5
            \end{array}
            \right]
            $$

2. Tukar B2 (baris 1) dan B3 (baris 2) (agar pivot positif)
    1. Kode:

        ```python
        A.swap_rows(1, 2)
        A

    - A.swap_rows(1, 2) *Artnya:* Tukar baris 1 dan 2

    2. Output:

        $$
        \left[
        \begin{array}{cccc|c}
        1 & 1 & 1 & 1 & 10 \\
        0 & 1 & 0 & 0 & 4 \\
        0 & -1 & -1 & -1 & -7 \\
        0 & 0 & 1 & 0 & 5
        \end{array}
        \right]
        $$

3. Hilangkan elemen di bawah pivot kedua
    B3 → B3 + B2

    1. Kode:

        ```python
        A.add_multiple_of_row(2, 1, 1)
        A

    2. Output:

        $$
        \left[
        \begin{array}{cccc|c}
        1 & 1 & 1 & 1 & 10 \\
        0 & 1 & 0 & 0 & 4 \\
        0 & 0 & -1 & -1 & -3 \\
        0 & 0 & 1 & 0 & 5
        \end{array}
        \right]
        $$

4. Hilangkan elemen di bawah pivot ketiga
    B4 → B4 + B3

    1. Kode:

        ```python
        A.add_multiple_of_row(3, 2, 1)
        A
    
    2. Output:

        $$
        \left[
        \begin{array}{cccc|c}
        1 & 1 & 1 & 1 & 10 \\
        0 & 1 & 0 & 0 & 4 \\
        0 & 0 & -1 & -1 & -3 \\
        0 & 0 & 0 & -1 & 2
        \end{array}
        \right]
        $$

5. Substitusi Balik
    1. Dari baris 4:

        $$−w = \Rightarrow 2 w = −2$$
    
    2. Baris 3

        $$−z −w = −3
        −z + 2 = −3
        z = 5$$
    
    3. Baris 2

        $$y = 4$$
    
    4. Baris 1

        $$x + y + z + w = 10
        x + 4 + 5 − 2 = 10
        x = 3$$

        **ATAU**

6. Jadikan pivot ketiga dan keempat = 1
    1. Kode:

        ```python
        A.rescale_row(2, -1)
        A.rescale_row(3, -1)
        A

    2. Output:

        $$
        \begin{bmatrix}
        1 & 1 & 1 & 1 & 10 \\
        0 & 1 & 0 & 0 & 4 \\
        0 & 0 & -1 & -1 & -3 \\
        0 & 0 & 0 & -1 & 2
        \end{bmatrix}
        $$

    3. Substitusi Balik (Manual)

        $$w = −2
        z = 5
        y = 4
        x = 3$$

7. Solusi (Hasil)

    $$(x,y,z,w) = (3,4,5,−2)$$