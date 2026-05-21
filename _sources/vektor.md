### Dekomposisi 

#### Matriks A

$$
A=
\begin{bmatrix}
1 & 2 & 3 & 4\\
4 & 2 & 3 & 1\\
2 & 6 & 4 & 3\\
3 & 1 & 2 & 5
\end{bmatrix}
$$

Kolom-kolom:

$$
a_1=(1,4,2,3)
$$

$$
a_2=(2,2,6,1)
$$

$$
a_3=(3,3,4,2)
$$

$$
a_4=(4,1,3,5)
$$

---

#### 1. Cari q₁

Norm:

$$
\sqrt{1^2+4^2+2^2+3^2}
=
\sqrt{30}
$$

$$
q_1=
\left(
\frac1{\sqrt{30}},
\frac4{\sqrt{30}},
\frac2{\sqrt{30}},
\frac3{\sqrt{30}}
\right)
$$

---

#### 2. Cari q₂

Dot product:

$$
a_2 \cdot q_1
=
\frac{
1(2)+4(2)+2(6)+3(1)
}{\sqrt{30}}
=
\frac{25}{\sqrt{30}}
$$

Proyeksi:

$$
\frac{25}{\sqrt{30}}q_1
=
\left(
\frac56,
\frac{10}3,
\frac53,
\frac52
\right)
$$

Kurangkan:

$$
u_2
=
(2,2,6,1)
-
\left(
\frac56,
\frac{10}3,
\frac53,
\frac52
\right)
$$

$$
=
\left(
\frac76,
-\frac43,
\frac{13}3,
-\frac32
\right)
$$

Norm:

$$
\|u_2\|
=
\sqrt{
\left(\frac76\right)^2+
\left(-\frac43\right)^2+
\left(\frac{13}3\right)^2+
\left(-\frac32\right)^2
}
$$

$$
=
\sqrt{\frac{781}{36}}
=
\frac{\sqrt{781}}6
$$

Maka:

$$
q_2=
\left(
\frac7{\sqrt{781}},
\frac{-8}{\sqrt{781}},
\frac{26}{\sqrt{781}},
\frac{-9}{\sqrt{781}}
\right)
$$

---

#### 3. Cari q₃

Hitung dot pertama:

$$
a_3 \cdot q_1
=
\frac{
1(3)+4(3)+2(4)+3(2)
}{\sqrt{30}}
=
\frac{29}{\sqrt{30}}
$$

Proyeksi ke q₁:

$$
\frac{29}{\sqrt{30}}q_1
=
\left(
\frac{29}{30},
\frac{58}{15},
\frac{29}{15},
\frac{29}{10}
\right)
$$

---

Dot kedua:

$$
a_3 \cdot q_2
=
\frac{
7(3)+(-8)(3)+26(4)+(-9)(2)
}{\sqrt{781}}
$$

$$
=
\frac{83}{\sqrt{781}}
$$

Proyeksi ke q₂:

$$
\frac{83}{\sqrt{781}}q_2
=
\left(
\frac{581}{781},
\frac{-664}{781},
\frac{2158}{781},
\frac{-747}{781}
\right)
$$

---

Kurangkan semuanya:

$$
u_3
=
a_3
-
\text{proj}_{q_1}
-
\text{proj}_{q_2}
$$

Hasil pendekatan:

$$
u_3
\approx
(1.290,0.000,-0.696,0.056)
$$

Norm:

$$
\|u_3\|
\approx 1.467
$$

Maka:

$$
q_3
\approx
(0.879,0,-0.474,0.038)
$$

---

#### 4. Cari q₄

Hitung:

$$
a_4 \cdot q_1
=
\frac{
1(4)+4(1)+2(3)+3(5)
}{\sqrt{30}}
=
\frac{29}{\sqrt{30}}
$$

Proyeksi:

$$
\frac{29}{\sqrt{30}}q_1
=
\left(
\frac{29}{30},
\frac{58}{15},
\frac{29}{15},
\frac{29}{10}
\right)
$$

---

Dot kedua:

$$
a_4 \cdot q_2
=
\frac{
7(4)+(-8)(1)+26(3)+(-9)(5)
}{\sqrt{781}}
$$

$$
=
\frac{53}{\sqrt{781}}
$$

Proyeksi:

$$
\frac{53}{\sqrt{781}}q_2
\approx
(0.475,-0.543,1.764,-0.610)
$$

---

Dot ketiga:

$$
a_4 \cdot q_3
\approx 2.136
$$

Proyeksi:

$$
2.136q_3
\approx
(1.878,0,-1.012,0.081)
$$

---

Kurangkan:

$$
u_4
=
a_4
-
\text{proj}_{q_1}
-
\text{proj}_{q_2}
-
\text{proj}_{q_3}
$$

Hasil pendekatan:

$$
u_4
\approx
(0.680,-2.324,0.315,2.629)
$$

Norm:

$$
\|u_4\|
\approx 3.598
$$

Maka:

$$
q_4
\approx
(0.189,-0.646,0.088,0.731)
$$

---

#### Hasil Akhir Q

$$
Q
\approx
\begin{bmatrix}
0.183 & 0.250 & 0.879 & 0.189\\
0.730 & -0.286 & 0 & -0.646\\
0.365 & 0.931 & -0.474 & 0.088\\
0.548 & -0.322 & 0.038 & 0.731
\end{bmatrix}
$$