# Laporan Proyek Machine Learning - Muhammad Fadhel Haidar

## Project Overview

Anime Jepang merupakan salah satu budaya populer yang berasal dari Jepang yang dinikmati oleh banyak orang di berbagai negara sebagai program televisi dan/atau konten video di internet [1]. Penggemar anime sangat banyak dan beragam, mulai dari anak-anak hingga dewasa. Anime mencakup berbagai genre, seperti aksi, komedi, romantis, dan lain-lain. Setiap tahun, banyak anime baru yang dirilis, seringkali penggemar anime kesulitan untuk menemukan anime yang sesuai dengan keinginan mereka. Oleh karena itu, diperlukan sebuah sistem rekomendasi yang dapat memberikan rekomendasi anime yang sesuai dengan preferensi pengguna.

Sistem rekomendasi adalah alat yang sangat berguna yang menjamin bahwa informasi yang tepat diberikan kepada pengguna yang tepat pada waktu yang tepat. Sistem rekomendasi ini berguna dalam berbagai bidang, seperti personalisasi web, penyaringan informasi, dan *e-commerce*. Sistem rekomendasi anime dibuat untuk membantu penonton menemukan anime yang sesuai dengan minat mereka. Sistem ini menganalisis data penonton dan menyarankan anime yang sesuai dengan preferensi mereka. Sistem ini dapat menganalisis data penonton seperti anime yang ditonton, rating anime, dan riwayat penonton. Kemudian, sistem akan menyarankan anime yang sesuai dengan preferensi penonton berdasarkan data yang dianalisis. Dengan sistem ini, penonton dapat menemukan anime yang sesuai dengan minat mereka tanpa harus mencari anime satu per satu.

Sistem rekomendasi anime ini menggunakan metode *Neural Collaborative Filtering* (NCF) yang merupakan metode yang digunakan untuk menyelesaikan masalah rekomendasi dengan menggunakan jaringan saraf yang dikenal sebagai *Generalized Matrix Factorization* (GMF) dan *Multi-Layer Perceptron* (MLP) [3]. GMF digunakan untuk mengidentifikasi hubungan antara penonton dan anime, sementara MLP digunakan untuk mengidentifikasi fitur yang terkait dengan anime.

## Business Understanding

Masalah yang diidentifikasi dari latar belakang tersebut adalah kesulitan dalam menemukan anime yang sesuai dengan preferensi pengguna. Penggemar anime sering mengalami kesulitan dalam menemukan anime yang sesuai dengan keinginan mereka karena banyaknya anime yang tersedia. Oleh karena itu, diperlukan sebuah sistem rekomendasi yang dapat memberikan rekomendasi anime yang sesuai dengan preferensi pengguna. Bila dilihat dari latar belakang masalah yang sudah dijelaskan sebelumnya, maka didapati pernyataan masalah sebagai berikut:

### Problem Statements

- Berapa nilai RMSE yang mampu dihasilkan oleh model rekomendasi?
- Berapa nilai *loss* yang mampu dihasilkan oleh model rekomendasi?

### Goals

- Mendapatkan nilai RMSE dari model rekomendasi.
- Mendapatkan nilai *loss* dari model rekomendasi.

### Solution statements

Secara keseluruhan, masalah yang akan diselesaikan dalam project ini adalah menciptakan sebuah sistem rekomendasi anime yang dapat memberikan rekomendasi anime yang sesuai dengan preferensi pengguna dengan menggunakan metode machine learning Neural Collaborative Filter (NCF). Dalam project ini, data yang akan digunakan adalah data rating anime yang diberikan oleh pengguna. Data ini akan digunakan untuk melakukan analisis dan menentukan pola preferensi pengguna. Metode NCF akan digunakan untuk menentukan korelasi antara pengguna dan anime yang mereka rating, NCF menggabungkan teknik  *deep learning* dengan metode *collaborative filtering* untuk meningkatkan akurasi rekomendasi.

## Data Understanding

Dataset terdapat kolom 'anime_id',	'name',	'genre'.	'type',	'episodes',	'rating',	'members',	'user_id',	'user_rating'. Pada kolom 'anime_id' mengenai nomor unik yang mewakilkan dari tiap-tiap judul dar anime. Kemudian kolom 'name' berisi judul dari masing-masing anime. pada kolom 'genre' berisi dari genre atau jenis dari setiap anime yang tedapat pada data. Kolom 'type' merupakan kolom yang berisikan tipe dari anime atau kategori dari setiap anime, kategori anime terbagi menjadi 6 yaitu *TV series*, *Movie*, OVA, ONA, *Special* dan *Music*. kemudian kolom 'episode' berisikan jumlah episode dari setiap anime. kemudian kolom 'rating' berisikan rating dari masing-masing anime. Kolom 'members' berisikan member dari komunitas anime tersebut. kemudian kolom 'user_id' berisikan nomer unik dari *user*. Terakhir merupakan kolom 'user_rating' yang berisi rating terhdap setiap anime dari setiap *user*. 

Berikut merupakan tabel statiskik dari data anime 

|        |                    name |  genre |  type | episodes |
|-------:|------------------------:|-------:|------:|----------|
|  count |                   12294 |  12232 | 12269 |    12294 |
| unique |                   12292 |   3264 |     6 |      187 |
|    top | Shi Wan Ge Leng Xiaohua | Hentai |    TV |        1 |
|   freq |                       2 |    823 |  3787 |     5677 |

###### Tabel 1,  Statiskik Anime

Berikut merupakan visualisasi dari 10 anime dengan jumlah anggota komunitas terbanyak yang terdapat pada Gambar 1, bisa disimpulkan aime 'Death Note' memiliki jumlah penggemar dengan jumlah lebih dari 1 juta penggemar.

![download (0)](https://user-images.githubusercontent.com/66835763/215034803-09496f4b-85bd-4f86-9571-8897d34d3b70.jpg)
###### Gambar 1,  Top Anime Community

Berikut merupakan visualisasi dari jumlah kategori anime yang terdapat pada gambar 2, Kategori TV merupakan kategori terbanyak dari anime yang ada.

![download (1)](https://user-images.githubusercontent.com/66835763/215035012-2c71f3d7-696c-4b9c-9cef-87e6a04aa7c9.jpg)
###### Gambar 2,  Top Anime Category

Berikut merupakan visualisasi dari anime dengan *rating* tertinggi dengan judul 'Mogura no Motoro' yang terdapat pada Gambar 3, pada anime tersebut memiliki nilai rata-rata *rating* mencapai 9.5. 

![download (2)](https://user-images.githubusercontent.com/66835763/215035602-92b335a6-9a06-43b2-963e-7f3f01b3ecb8.jpg)
###### Gambar 3,  Top Anime Rating

Berikut merupakan visualisasi dari jumlah anime pada genre tertentu yang terdapat pada Gambar 4, genre *comedy* merupakan genre dengan jumlah anim terbanyak.

![download (3)](https://user-images.githubusercontent.com/66835763/215036418-686977a9-acd6-438c-bdf2-fab2204406bd.jpg)
###### Gambar 4,  Top Anime Based On Genre


## Data Preparation
 
Pada bagian data yang sudah dieksplorasi tadi akan kembali dibersihkan, pada data ini masih terdapat beberapa karakter pada kolom nama. 
```
def text_cleaning(text):
    text = re.sub(r'&quot;', '', text)
    text = re.sub(r'.hack//', '', text)
    text = re.sub(r'&#039;', '', text)
    text = re.sub(r'A&#039;s', '', text)
    text = re.sub(r'I&#039;', 'I\'', text)
    text = re.sub(r'&amp;', 'and', text)
    
    return text

data["name"] = data["name"].apply(text_cleaning)
```
Kode di atas digunakan untuk membersihkan teks dari data yang ada di kolom "name" pada dataframe yang disebut "data". Fungsi "text_cleaning" menghapus karakter yang tidak diinginkan menggunakan metode "sub" dari package "re" dan mengganti dengan karakter kosong. Kemudian, metode "apply" digunakan untuk mengaplikasikan fungsi "text_cleaning" pada kolom "name" dari dataframe "data" untuk membersihkan teks dari karakter yang tidak diinginkan.

## Modeling
```
Model: "recommender_net"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
embedding (Embedding)        multiple                  1648350   
_________________________________________________________________
embedding_1 (Embedding)      multiple                  32967     
_________________________________________________________________
embedding_2 (Embedding)      multiple                  493700    
_________________________________________________________________
embedding_3 (Embedding)      multiple                  9874      
_________________________________________________________________
dense (Dense)                multiple                  128       
_________________________________________________________________
dense_1 (Dense)              multiple                  2080      
_________________________________________________________________
dense_2 (Dense)              multiple                  33        
=================================================================
Total params: 2,187,132
Trainable params: 2,187,132
Non-trainable params: 0
```
Model machine learning yang digunakan dalam proyek ini adalah *Neural Collaborative Filter* (NCF). NCF merupakan sebuah metode yang digunakan untuk memberikan rekomendasi item (dalam hal ini anime) berdasarkan interaksi antara pengguna dan item. Model ini terdiri dari beberapa lapisan yang disebut "layer" dan masing-masing lapisan memiliki fungsi yang berbeda.

1. Lapisan "embedding" digunakan untuk mengubah input dari sistem menjadi representasi vektor. Lapisan ini memiliki 1648350 parameter yang dapat di-training.

2. Lapisan "embedding_1" dan "embedding_2" juga digunakan untuk mengubah input menjadi representasi vektor, namun dengan jumlah parameter yang lebih sedikit dibanding lapisan pertama.

3. Lapisan "embedding_3" digunakan untuk mengubah input menjadi representasi vektor, dengan jumlah parameter yang lebih sedikit lagi dibanding lapisan sebelumnya.

4. Lapisan "dense" digunakan untuk mengkombinasikan representasi vektor yang dihasilkan dari lapisan sebelumnya menjadi satu output yang lebih kompak. Lapisan ini memiliki 128 parameter yang dapat dilatih.

5. Lapisan "dense_1" digunakan untuk mengkombinasikan representasi vektor yang dihasilkan dari lapisan sebelumnya menjadi satu *output* yang lebih kompak. Lapisan ini memiliki 2080 parameter yang dapat dilatih.

6. Lapisan "dense_2" digunakan untuk menghasilkan output akhir dari model, yaitu rekomendasi anime yang sesuai dengan preferensi user. Lapisan ini memiliki 33 parameter yang dapat dilatih.

Jumlah total parameter yang dapat dilatih pada model ini adalah 2,187,132.


## Evaluation

Model tersebut berperforma baik dan *loss* serta *root mean squared error*-nya menurun pada setiap 'epoch'. *Loss* validasi dan *root mean squared error* juga menurun, yang menunjukkan bahwa model tidak mengalami *overfitting*. Model mampu mencapai *root mean squared error* validasi sekitar 0,1374 setelah 17-18 'epoch'. Hasil tersebut termasuk ke dalam kondisi yang baik untuk model sistem rekomendasi. Waktu pelatihan untuk setiap 'epoch' sekitar 40 detik, yang merupakan waktu yang wajar untuk dataset dan kompleksitas model seperti ini. Secara keseluruhan, model dapat dianggap sudah dilatih dan siap untuk prediksi pada data baru.Grafik dari pelatihan model dapat dilihat pada Gambar 5.

![download (4)](https://user-images.githubusercontent.com/66835763/215036781-b634e68a-2ee5-4219-a694-c6715e009e6e.jpg)
###### Gambar 5, Grafik Training Loss dan RMSE

Berikut merupakan testing secara acak pada user tertentu, dapat dilihat bahwa hasil rekomendasi dari anime tersebut terbilang baik karena genre dari anime yang direkomendasikan masih serupa.
```
Showing recommendations for user: 58507
====================================
Anime with high ratings from user
--------------------------------
Clannad: After Story : Drama, Fantasy, Romance, Slice of Life, Supernatural
Code Geass: Hangyaku no Lelouch R2 : Action, Drama, Mecha, Military, Sci-Fi, Super Power
Code Geass: Hangyaku no Lelouch : Action, Mecha, Military, School, Sci-Fi, Super Power
Cowboy Bebop : Action, Adventure, Comedy, Drama, Sci-Fi, Space
Mononoke Hime : Action, Adventure, Fantasy
--------------------------------
Top 10 anime recommendations
--------------------------------
Kimi no Na wa. : Drama, Romance, School, Supernatural
Fullmetal Alchemist: Brotherhood : Action, Adventure, Drama, Fantasy, Magic, Military, Shounen
Gintama° : Action, Comedy, Historical, Parody, Samurai, Sci-Fi, Shounen
Steins;Gate : Sci-Fi, Thriller
Gintama&#039; : Action, Comedy, Historical, Parody, Samurai, Sci-Fi, Shounen
Hunter x Hunter (2011) : Action, Adventure, Shounen, Super Power
Ginga Eiyuu Densetsu : Drama, Military, Sci-Fi, Space
Gintama Movie: Kanketsu-hen - Yorozuya yo Eien Nare : Action, Comedy, Historical, Parody, Samurai, Sci-Fi, Shounen
Gintama&#039;: Enchousen : Action, Comedy, Historical, Parody, Samurai, Sci-Fi, Shounen
Gintama : Action, Comedy, Historical, Parody, Samurai, Sci-Fi, Shounen
```

## Kesimpulan

Bisa disimpulkan bahwa Model yang digunakan dalam sistem rekomendasi anime menggunakan *Neural Collaborative Filtering* (NCF) telah dilakukan dengan baik. *Loss* dan *root mean squared error* yang dihasilkan semakin menurun pada setiap 'epoch'. *Loss* dan *root mean squared error* pada data validasi juga semakin menurun, menunjukkan bahwa model tidak terjadi *overfitting*. 

## Daftar Referensi

[1] N. Homma, A. Uemura and T. Kitahara, "Are Theme Songs Usable for Anime Retrieval?," 2021 IEEE 4th International Conference on Multimedia Information Processing and Retrieval (MIPR), Tokyo, Japan, 2021, pp. 227-230, doi: 10.1109/MIPR51284.2021.00042.

[2] A. A. Patel and J. N. Dharwa, "An integrated hybrid recommendation model using graph database," 2016 International Conference on ICT in Business Industry & Government (ICTBIG), Indore, India, 2016, pp. 1-5, doi: 10.1109/ICTBIG.2016.7892680.

[3] X. He, L. Liao, H. Zhang, L. Nie, X. Hu, and T.-S. Chua, “Neural collaborative filtering,” arXiv.org, 26-Aug-2017. [Online]. Available: https://arxiv.org/abs/1708.05031. [Accessed: 27-Jan-2023]. 
