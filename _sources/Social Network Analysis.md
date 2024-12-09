---
title: Social Network Analysis

---

# Social Network Analysis

Social Network Analysis merupakan bidang kajian yang mengekplorasitentang hubungan manusia dengan menggunakan teori graf. Implementasi Social Network Analysis dapat menjelaskan relasi atau hubungan antar aktor melalui visualisasi berbentuk graf. Relasi dalam analisis jaringan sosial dapat diproses dalam bentuk perhitungan yang disebut centrality dalam sebuah jaringan sosial sesuai dengan posisi masing-masing aktor di dalam struktur jaringan tersebut

## Graph

Graph adalah sekumpulan node yang saling terhubung. 

contoh graph seperti jaringan komputer yang saling terhubung, orang orang dalam sosial media yang saling berhubungan.

contoh graph yang berbobot yaitu jarak antar kota, seperti bangkalan ke sampang 10km, sampang ke sumenep 20km, bangkalan ke sumenep 35km.Bobot menunjukkan jarak jalan, yang dimana akan menghasilkan analisis jarak lintaran terpendek.

## contoh:

![original image](https://cdn.mathpix.com/snip/images/2XgBue-ahlsabJv_kV0h96Nlm_emFcgFAkteEwcPeaY.original.fullsize.png)

analisa node terpenting dalam graph tersebut:

###  Degree Centrality

Degree centrality adalah jumlah edge yang terkoneksi pada suatu node yang mewakili interaksi.

* Pentingnya node ditentukan oleh jumlah node yang berdekatan dengan node tersebut.
- lebih besar derajatnya(degree),maka lebih penting node itu dalam suatu jaringan
- hanya sebagian kecil node yang memiliki derajat tinggi dalam jaringan


Degree Centrality = 

$$
C_D\left(v_i\right)=d_i=\sum_i A_{i j}
$$

Normalisasi Degree Centrality = 
$$
C_D^{\prime}\left(v_i\right)=d_i /(n-1)
$$


### Closeness centrality

Closeness centrality adalah nilai kedekatan antara suatu node dengan node lain dalam jaringan dengan menhitung rata rata dari jarak relasi node-node tersebut. skor closeness centrality mewakili kecepatan dalm penyebaran informasi


Average Distance : 

$$
D_{\text {avg }}\left(v_i\right)=\frac{1}{n-1} \sum_{j \neq i}^n g\left(v_i, v_j\right)
$$

Closeness Centrality : 

$$
C_C\left(v_i\right)=\left[\frac{1}{n-1} \sum_{j \neq i}^n g\left(v_i, v_j\right)\right]^{-1}=\frac{n-1}{\sum_{j \neq i}^n g\left(v_i, v_j\right)}
$$

### Betweenness Centrality

skor betweeness centrality mewakili seberapa besar informasi yang tersebar dari suatu aktor. semakin besar skor, artinya aktor tersebut semakin berperan dalam penyebaran informasi

Semakin banyak lintasan yang harus melewati persimpangan itu (misal tidak ada jalan alternatif), maka semakin penting arti persimpangan tersebut. hal ini menandakan seberapa besar suatu node diperlukan sebagai penghubung dalam penyebaran informasi di dalam jaringan

Ukuran ini juga dapat digunakan untuk mengidentifikasi boundary spanners, yaitu orang atau node yang berperan sebagai penghubung (jembatan) antara dua komunitas

* Menghitung jumlah lintasan terpendek yang melewati suatu node
* Node dengan  betweenness  tinggi  adalah  penting dalam komunikasi dan penyebaran informasi

* betweenness centrality

$$
C_B\left(v_i\right)=\sum_{v_s \neq v_i \neq v_t \in V, s<t} \frac{\sigma_{s t}\left(v_i\right)}{\sigma_{s t}}
$$

$\sigma_{s t}$ Jumlah lintasan terpendek antara s dan t 
$\sigma_{s t}\left(v_i\right)$ Jumlah lintasan terpendek antara $s$ dan $t$ yang melewati $\mathrm{v}_{\mathrm{i}}$

![](https://cdn.mathpix.com/snip/images/WA7CwKeZ6lES3q-BX6XAuc4XAOiePU3P8EnbY9c3TLk.original.fullsize.png)

* normalisasi betweenness centrality

$$
C_B^{\prime}(i)=\frac{C_B(i)}{(n-1)(n-2) / 2} .
$$






