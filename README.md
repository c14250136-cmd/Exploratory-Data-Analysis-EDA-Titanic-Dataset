# 📊 Exploratory Data Analysis (EDA) Titanic Dataset

## 📝 Pendahuluan

Dataset **Titanic** adalah salah satu dataset klasik yang sering digunakan untuk pembelajaran analisis data. Dataset ini berisi informasi tentang penumpang Titanic, seperti usia, jenis kelamin, kelas tiket, tarif, status selamat atau tidak, dan lain-lain.

Dalam analisis ini, dilakukan **modifikasi kode EDA dasar** dengan menambahkan beberapa variabel baru untuk memperkaya wawasan terhadap faktor-faktor yang mungkin memengaruhi kelangsungan hidup penumpang.

---

## ⚙️ Modifikasi yang Dilakukan

Dari kode EDA sebelumnya, saya menambahkan beberapa variabel baru berikut:

### 1. `family_size`

* **Definisi**: Jumlah anggota keluarga yang ikut berlayar bersama seorang penumpang.

* **Rumus**:

  ```
  family_size = sibsp + parch + 1
  ```

  * `sibsp`: jumlah saudara kandung + pasangan
  * `parch`: jumlah orang tua + anak
  * `+1`: penumpang itu sendiri

* **Tujuan**: Untuk melihat apakah ukuran keluarga memengaruhi kemungkinan selamat.

---

### 2. `is_alone`

* **Definisi**: Indikator apakah penumpang berlayar sendirian atau bersama keluarga.

* **Rumus**:

  ```
  is_alone = 1 jika family_size == 1
  is_alone = 0 jika family_size > 1
  ```

* **Tujuan**: Untuk mengelompokkan penumpang menjadi dua kategori:

  * **Sendirian (is\_alone = 1)**
  * **Tidak sendirian (is\_alone = 0)**

---

## 📈 Visualisasi Tambahan
![At](https://github.com/c14250136-cmd/Exploratory-Data-Analysis-EDA-Titanic-Dataset/blob/main/Screenshot%202025-09-06%20011520.png)
![Alt](https://github.com/c14250136-cmd/Exploratory-Data-Analysis-EDA-Titanic-Dataset/blob/main/Screenshot%202025-09-06%20011542.png)
![Alext](https://github.com/c14250136-cmd/Exploratory-Data-Analysis-EDA-Titanic-Dataset/blob/main/Screenshot%202025-09-06%20011556.png)
## ✅ Kesimpulan Sementara

* Sebagian besar penumpang Titanic memiliki keluarga kecil (ukuran 1–4 orang).
* Penumpang yang **sendirian (is\_alone = 1)** cenderung memiliki tingkat kelangsungan hidup yang berbeda dibanding penumpang yang bersama keluarga.
* Variabel tambahan `family_size` dan `is_alone` memberikan insight lebih dalam mengenai hubungan faktor sosial/keluarga dengan peluang selamat.

---

## 📂 Catatan

* FILE RAW = https://colab.research.google.com/drive/1-8XgpdgzRZ3yL4nKs0G46cTKtPL1TybI#scrollTo=btn0BuO-Fcus
* FILE HASIL IMPROVE DAN MODIFIKASI = https://colab.research.google.com/drive/1tR_G5_v8mrXpNr3sUX-w-JRlUlMT-3Qs?usp=sharing
