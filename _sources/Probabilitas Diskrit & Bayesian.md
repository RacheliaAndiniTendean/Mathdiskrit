---
title: Probabilitas Diskrit & Bayesian

---

# Probabilitas Diskrit & Bayesian

## Pengertian

**Probabilitas diskrit** adalah cabang dari teori probabilitas yang berfokus pada variabel acak yang memiliki nilai terhitung dan terbatas. Dalam konteks ini, probabilitas diskrit menggambarkan kemungkinan hasil dari percobaan yang menghasilkan nilai-nilai tertentu. Misalnya, hasil dari lemparan dadu atau jumlah panggilan telepon yang diterima dalam satu jam adalah contoh variabel diskrit.

**Probabilitas Bayesian** adalah pendekatan dalam teori probabilitas yang menggabungkan informasi baru dengan pengetahuan sebelumnya untuk memperbarui kepercayaan terhadap suatu hipotesis. Ini didasarkan pada Teorema Bayes, yang menyatakan bahwa probabilitas suatu hipotesis $H$ setelah melihat data $X$ (dikenal sebagai posterior probability) dapat dihitung dengan rumus:
$P(H \mid X)=\frac{P(X \mid H) \cdot P(H)}{P(X)}$

Di mana:
- $P(H \mid X)$ adalah probabilitas hipotesis setelah data diperoleh (posterior).
- $P(H)$ adalah probabilitas awal hipotesis (prior).
- $P(X \mid H)$ adalah probabilitas data jika hipotesis benar.
- $P(X)$ adalah total probabilitas data 24 .


## Teorema Bayes

### Prior
**Prior probability** adalah distribusi probabilitas yang mencerminkan keyakinan atau pengetahuan awal tentang suatu parameter sebelum data baru diperoleh. Ini menggambarkan asumsi atau informasi yang sudah ada mengenai parameter yang sedang dianalisis. Misalnya, jika kita memperkirakan kemungkinan suatu penyakit, prior dapat didasarkan pada data epidemiologi sebelumnya atau studi populasi.

### Likelihood
**Likelihood** adalah distribusi probabilitas dari data yang diamati diberikan parameter tertentu. Ini menggambarkan seberapa baik model dengan parameter tersebut dapat menjelaskan data yang telah dikumpulkan. Dalam konteks statistik, likelihood dihitung berdasarkan fungsi distribusi dari data yang diperoleh dan parameter yang diasumsikan. Sebagai contoh, jika kita memiliki data tentang hasil tes kesehatan, likelihood akan menunjukkan seberapa besar kemungkinan hasil tersebut terjadi jika parameter kesehatan tertentu benar

### Posterior

**Posterior probability** adalah distribusi probabilitas yang diperoleh setelah menggabungkan informasi dari prior dan likelihood. Ini mencerminkan keyakinan kita tentang parameter setelah mempertimbangkan data yang baru diperoleh.

## Contoh Soal

| No | Usia | Tekanan Darah | Penyakit (H/T) |
| :--- | :--- | :--- | :--- |
| 1 | Muda | Normal | T |
| 2 | Muda | Tinggi | T |
| 3 | Paruh baya | Normal | T |
| 4 | Paruh baya | Tinggi | H |
| 5 | Tua | Normal | H |
| 6 | Tua | Sangat Tinggi | H |
| 7 | Muda | Normal | T |
| 8 | Tua | Tinggi | H |

1. Hitunglah probabilitas Hipertensi terhadapa usia paruh baya tekanan darah sangat tinggi 

2. Hitunglah probabilitas Tidak  Hipertensi terhadap usia paruh baya tekanan darah sangat tinggi 

### Jawaban Menggunakam menggunakan Rumus Naive Bayes
Informasi Awal
1. Total data $(N)=8$.
2. Probabilitas prior:
- $P(H)=4 / 8=0.5$
- $P(T)=4 / 8=0.5$

**Probabilitas Kondisional**

1. Probabilitas $P($ Usia Paruh Baya $\mid H)$ :
- Dari 4 data Hipertensi, Usia Paruh Baya muncul 1 kali (Baris 4).
$$
P($ Usia Paruh Baya $\mid H)=1 / 4=0.25
$$

2. Probabilitas $P($ Sangat Tinggi $\mid H)$ :

- Dari 4 data Hipertensi (H), Tekanan Darah Sangat Tinggi muncul 1 kali.

$$
P(\text { Sangat Tinggi } \mid H)=\frac{1+1}{4+3}=\frac{2}{7} \approx 0.286
$$

3. Probabilitas $P$ (Usia Paruh Baya $\mid T)$ :
- Dari 4 data Tidak Hipertensi (T), Usia Paruh Baya muncul 1 kali.

$$
P(\text { Paruh Baya } \mid T)=\frac{\text { Frekuensi Paruh Baya pada } \mathrm{T}}{\text { Total Frekuensi } \mathrm{T}}=\frac{1}{4}=0.25
$$

4. Probabilitas $P($ Sangat Tinggi $\mid T)$ :
- Dari 4 data Tidak Hipertensi (T), Tekanan Darah Sangat Tinggi muncul 0 kali.

$$
P(\text { Sangat Tinggi } \mid T)=\frac{0+1}{4+3}=\frac{1}{7} \approx 0.143
$$


**Probabilitas Posterior (Naive Bayes)**
1. Untuk Hipertensi (H):
$$
P(H \mid \text { Paruh Baya, Sangat Tinggi })=P(\text { Paruh Baya } \mid H) \cdot P(\text { Sangat Tinggi } \mid H) \cdot P(H)
$$

**Substitusi nilai:**
$$
P(H \mid \ldots)=0.25 \cdot 0.286 \cdot 0.5=0.03575
$$

2. Untuk Tidak Hipertensi (T):
$$
P(T \mid \text { Paruh Baya, Sangat Tinggi })=P(\text { Paruh Baya } \mid T) \cdot P(\text { Sangat Tinggi } \mid T) \cdot P(T)
$$

**Substitusi nilai:**
$$
P(T \mid \ldots)=0.25 \cdot 0.143 \cdot 0.5=0.017875
$$

**Normalisasi**
Untuk menghitung probabilitas akhir:
$$
\text { Total }=P(H \mid \ldots)+P(T \mid \ldots)=0.03575+0.017875=0.053625
$$

Probabilitas Hipertensi (H):
$$
P(H \mid \ldots)=\frac{0.03575}{0.053625} \approx 0.666(66.6 \%)
$$

Probabilitas Tidak Hipertensi ( T ):
$$
P(T \mid \ldots)=\frac{0.017875}{0.053625} \approx 0.333(33.3 \%)
$$

**Kesimpulan : **

* Probabilitas seseorang dengan **usia paruh baya** dan **tekanan darah sangat tinggi** mengalami **Hipertensi** adalah 66.6%.
* Probabilitas **Tidak Hipertensi** adalah 33.3%.


### Jawaban Menghitung Menggunakan Rumus Teorema Bayes

Teorema Bayes
Teorema Bayes digunakan untuk menghitung probabilitas posterior $(P(H \mid X))$  berdasarkan probabilitas prior dan probabilitas kondisional.

Rumus umum:

$$
P(H \mid X)=\frac{P(X \mid H) \cdot P(H)}{P(X)}
$$

Di mana:
- $\quad P(H \mid X)$ : Probabilitas seseorang memiliki Hipertensi (H) diberikan data $X$ (fitur yang diamati seperti Usia Paruh Baya dan Tekanan Darah Sangat Tinggi).
- $P(X \mid H)$ : Probabilitas mengamati $X$ jika seseorang memiliki Hipertensi.
- $\quad P(H)$ : Probabilitas prior Hipertensi (H).
- $P(X)$ : Probabilitas mengamati $X$, dihitung sebagai total probabilitas untuk semua kategori (Hipertensi dan Tidak Hipertensi).

Penerapan Teorema Bayes dalam Masalah Ini
Kita ingin menghitung probabilitas posterior untuk:
1. Hipertensi $(P(H \mid$ Paruh Baya, Sangat Tinggi)).
2. Tidak Hipertensi ( $P(T \mid$ Paruh Baya, Sangat Tinggi $)$.

Data:
- $\quad X=$ (Paruh Baya, Sangat Tinggi).
- Probabilitas prior:
- $P(H)=0.5$,
- $P(T)=0.5$.
- Probabilitas kondisional dihitung menggunakan Laplace Smoothing.

**Langkah 1**: Hitung $P(X \mid H)$ dan $P(X \mid T)$

Untuk $P(X \mid H)$ :
$$
\begin{gathered}
P(X \mid H)=P(\text { Paruh Baya } \mid H) \cdot P(\text { Sangat Tinggi } \mid H) \\
P(X \mid H)=0.25 \cdot 0.286=0.0715
\end{gathered}
$$

Untuk $P(X \mid T)$ :
$$
\begin{gathered}
P(X \mid T)=P(\text { Paruh Baya } \mid T) \cdot P(\text { Sangat Tinggi } \mid T) \\
P(X \mid T)=0.25 \cdot 0.143=0.03575
\end{gathered}
$$

**Langkah 2**: Hitung Probabilitas Prior $(P(H)$ dan $P(T)$ )
$$
P(H)=0.5, \quad P(T)=0.5
$$

**Langkah 3**: Hitung $P(X)$ (Normalisasi Total Probabilitas)
$$
\begin{gathered}
P(X)=P(X \mid H) \cdot P(H)+P(X \mid T) \cdot P(T) \\
P(X)=(0.0715 \cdot 0.5)+(0.03575 \cdot 0.5)=0.03575+0.017875=0.053625
\end{gathered}
$$

**Langkah 4**: Hitung Posterior Menggunakan Teorema Bayes

Untuk Hipertensi $(P(H \mid X)$ ):


$$
\begin{gathered}
P(H \mid X)=\frac{P(X \mid H) \cdot P(H)}{P(X)} \\
P(H \mid X)=\frac{0.0715 \cdot 0.5}{0.053625}=\frac{0.03575}{0.053625} \approx 0.666(66.6 \%)
\end{gathered}
$$

Untuk Tidak Hipertensi $(P(T \mid X)$ ):


$$
\begin{gathered}
P(T \mid X)=\frac{P(X \mid T) \cdot P(T)}{P(X)} \\
P(T \mid X)=\frac{0.03575 \cdot 0.5}{0.053625}=\frac{0.017875}{0.053625} \approx 0.333(33.3 \%)
\end{gathered}
$$

**Kesimpulan**
- Probabilitas Hipertensi $(P(H \mid X)$ ): 66.6\%.
- Probabilitas Tidak Hipertensi $(P(T \mid X)$ ): 33.3\%.