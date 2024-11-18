---
title: Analisa graph

---

# Analisa graph

## Pengertian

Graph adalah sekumpulan node yang saling terhubung. 

contoh graph seperti jaringan komputer yang saling terhubung, orang orang dalam sosial media yang saling berhubungan.

contoh graph yang berbobot yaitu jarak antar kota, seperti bangkalan ke sampang 10km, sampang ke sumenep 20km, bangkalan ke sumenep 35km.Bobot menunjukkan jarak jalan, yang dimana akan menghasilkan analisis jarak lintaran terpendek.

## contoh:

![Screenshot 2024-11-11 133536](https://hackmd.io/_uploads/r1-RHQJfJl.png)

analisa node terpenting dalam graph tersebut:

###  Degree Centrality

Degree centrality adalah jumlah edge yang terkoneksi pada suatu node yang mewakili interaksi.

* Pentingnya node ditentukan oleh jumlah node yang berdekatan dengan node tersebut.
- lebih besar derajatnya(degree),maka lebih penting node itu dalam suatu jaringan
- hanya sebagian kecil node yang memiliki derajat tinggi dalam jaringan

![Screenshot 2024-11-11 141049](https://hackmd.io/_uploads/Hyh-RXJfke.png)


### Closeness centrality

Closeness centrality adalah nilai kedekatan antara suatu node dengan node lain dalam jaringan dengan menhitung rata rata dari jarak relasi node-node tersebut. skor closeness centrality mewakili kecepatan dalm penyebaran informasi

![Screenshot 2024-11-11 140458](https://hackmd.io/_uploads/H1xDpQyGkx.png)

### Betweenness Centrality

skor betweeness centrality mewakili seberapa besar informasi yang tersebar dari suatu aktor. semakin besar skor, artinya aktor tersebut semakin berperan dalam penyebaran informasi

Semakin banyak lintasan yang harus melewati persimpangan itu (misal tidak ada jalan alternatif), maka semakin penting arti persimpangan tersebut. hal ini menandakan seberapa besar suatu node diperlukan sebagai penghubung dalam penyebaran informasi di dalam jaringan

Ukuran ini juga dapat digunakan untuk mengidentifikasi boundary spanners, yaitu orang atau node yang berperan sebagai penghubung (jembatan) antara dua komunitas

* Menghitung jumlah lintasan terpendek yang melewati suatu node
* Node dengan  betweenness  tinggi  adalah  penting dalam komunikasi dan penyebaran informasi

* betweenness centrality

![Screenshot 2024-11-11 143618](https://hackmd.io/_uploads/SJzWVNkfkg.png)

![Screenshot 2024-11-11 143859](https://hackmd.io/_uploads/SywoE4kGye.png)

* normalisasi betweenness centrality

![Screenshot 2024-11-11 144636](https://hackmd.io/_uploads/S19PLN1Mke.png)





