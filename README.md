# Data Analysis: Hypothesis Testing & Inferential Statistics

[![Status](https://img.shields.io/badge/Status-Completed-success.svg)](https://github.com)
[![Excel](https://img.shields.io/badge/Tools-Microsoft%20Excel%20%7C%20Python-blue.svg)](https://github.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com)

Repositori ini berisi dokumentasi dan implementasi praktis dari konsep **Statistika Inferensial (Inferential Statistics)**, **Uji Hipotesis (Hypothesis Testing)**, **Analisis Varian (ANOVA)**, serta simulasi **Law of Large Numbers (LLN)** dan **Central Limit Theorem (CLT)** menggunakan Microsoft Excel dan perangkat pendukung analisis data.

---

## 📑 Daftar Isi
1. [Deskripsi Singkat](#-deskripsi-singkat)
2. [Ringkasan Materi & Analisis](#-ringkasan-materi--analisis)
   - [Uji T-Test (Two-Sample & Paired T-Test)](#1-uji-t-test-two-sample--paired-t-test)
   - [Uji ANOVA (Analysis of Variance)](#2-uji-anova-analysis-of-variance)
   - [Concept Review: LLN & CLT](#3-concept-review-law-of-large-numbers-lln--central-limit-theorem-clt)
3. [Pertanyaan Refleksi & Jawaban (Reflection Questions)](#-pertanyaan-refleksi--jawaban-reflection-questions)
4. [Metodologi & Tools](#-metodologi--tools-yang-digunakan)
5. [Cara Menggunakan Repositori](#-cara-menjalankan--menggunakan-file-ini)
6. [Kredit & Pemilik Projek](#-kredit--pemilik-projek)

---

## 📌 Deskripsi Singkat
Pengujian hipotesis adalah pilar utama dalam pengambilan keputusan berbasis data (*data-driven decision making*). Repositori ini mengeksplorasi bagaimana cara menguji asumsi statistik, membandingkan rata-rata antar kelompok data (baik dua kelompok maupun multikelompok), serta memahami perilaku distribusi sampling melalui simulasi komputer yang mendalam.

---

## 📊 Ringkasan Materi & Analisis

### 1. Uji T-Test (Two-Sample & Paired T-Test)
Uji t digunakan untuk menentukan apakah ada perbedaan yang signifikan secara statistik antara rata-rata dua kelompok. Berdasarkan sheet `1 A`, tahapan pengujian meliputi:
* **Langkah 1: Penyusunan Hipotesis ($H_0$ & $H_1$)**
  * `$H_0: \mu_1 = \mu_2$` (Tidak ada perbedaan rata-rata antara Stasiun 1 dan Stasiun 2)
  * `$H_1: \mu_1 \neq \mu_2$` (Terdapat perbedaan rata-rata yang signifikan)
* **Langkah 2: Menentukan Tingkat Signifikansi ($\alpha$)**
  * Umumnya menggunakan tingkat signifikansi `$1\%$`, `$5\%$`, atau `$10\%$` (standar umum `$\alpha = 0.05$`).
* **Langkah 3: Uji Kesamaan Variansi ($F$-Test / Levene's Test)**
  * `$H_0: \sigma_1^2 = \sigma_2^2$` (Variansi kedua grup sama)
  * `$H_1: \sigma_1^2 \neq \sigma_2^2$` (Variansi kedua grup tidak sama)
* **Langkah 4: Pemilihan Jenis Uji T**
  * **Paired T-Test:** Digunakan jika data berpasangan (sebelum dan sesudah).
  * **Unpaired T-Test (Equal Variance):** Digunakan jika variansi kedua kelompok homogen.
  * **Welch's T-Test (Unequal Variance):** Digunakan jika variansi kedua kelompok heterogen.

### 2. Uji ANOVA (Analysis_of_Variance)
Berdasarkan studi kasus perbandingan jumlah data yang hilang akibat kasus hacker malware pada tiga perusahaan e-commerce (**Shopee**, **Tokopedia**, dan **TikTok**):
* **Pernyataan Hipotesis:**
  * `$H_0$` (Null Hypothesis): Rataan jumlah data yang hilang pada ketiga perusahaan adalah sama semua (`rataan ketiga perusahaan abc sama semua`).
  * `$H_1$` (Alternative Hypothesis): Minimal ada satu perusahaan yang memiliki rataan jumlah data hilang yang berbeda (`minimal ada satu perusahaan yang rataannya berbeda`).
* **Komponen Kalkulasi ANOVA:**
  * Membandingkan variabilitas antar kelompok (*Between-Group Variability*) dengan variabilitas dalam kelompok (*Within-Group Variability*) untuk menghasilkan nilai `$F$-statistic`.

### 3. Concept Review: Law of Large Numbers (LLN) & Central Limit Theorem (CLT)
Melalui simulasi distribusi (Poisson, Binomial, Uniform, Normal, Right Skew) di dalam Excel:
* **Law of Large Numbers (LLN):** Menyatakan bahwa rata-rata dari hasil sampel yang diperoleh dari banyak percobaan akan mendekati nilai harpan (populasi) yang sebenarnya seiring dengan bertambahnya ukuran sampel.
* **Central Limit Theorem (CLT):** Menyatakan bahwa distribusi dari rata-rata sampel akan mendekati distribusi normal (kurva lonceng) terlepas dari bentuk distribusi populasi asalkan ukuran sampel cukup besar (`$n \ge 30$`).

---

## 💡 Pertanyaan Refleksi & Jawaban (Reflection Questions)

> Berikut adalah rangkapan pertanyaan refleksi beserta jawaban analitis yang mendalam berdasarkan pemahaman materi statistik:

### a. Kapan Uji ANOVA Lebih Relevan Dibandingkan Uji T?
**Pertanyaan:** 
Dalam konteks bisnis, kapan uji ANOVA lebih relevan digunakan dibandingkan uji t, dan apa dampaknya jika salah memilih metode uji? Jelaskan dengan mengaitkan pada perbandingan lebih dari dua kelompok.

**Jawaban:**
Dalam konteks bisnis, uji ANOVA lebih relevan digunakan ketika ingin membandingkan rata-rata dari tiga kelompok atau lebih, sedangkan uji t hanya digunakan untuk membandingkan dua kelompok. Misalnya, perusahaan ingin membandingkan rata-rata penjualan di tiga wilayah, yaitu Jakarta, Bandung, dan Surabaya. Dalam kasus ini, ANOVA lebih tepat karena dapat menguji seluruh kelompok secara bersamaan.

Jika menggunakan beberapa uji t untuk membandingkan lebih dari dua kelompok, risiko terjadinya *Type I Error* (menyimpulkan ada perbedaan padahal sebenarnya tidak ada) akan meningkat secara kumulatif. Akibatnya, perusahaan dapat mengambil keputusan yang kurang tepat, seperti salah menentukan strategi pemasaran atau alokasi anggaran. Oleh karena itu, ANOVA menjadi metode yang lebih akurat dan efisien untuk menganalisis perbedaan rata-rata pada lebih dari dua kelompok.

---

### b. Mengapa Keputusan Perlu Mempertimbangkan P-Value & Tingkat Signifikansi?
**Pertanyaan:** 
Mengapa pengambilan keputusan berbasis uji hipotesis perlu mempertimbangkan p-value dan tingkat signifikansi, bukan hanya melihat perbedaan rata-rata secara kasat mata? Jelaskan risiko yang dapat terjadi jika keputusan diambil tanpa pengujian statistik yang tepat.

**Jawaban:**
Dalam pengambilan keputusan bisnis, `$p\text{-value}$` dan tingkat signifikansi (`$\alpha$`) perlu dipertimbangkan karena membantu menentukan apakah perbedaan yang terlihat pada data benar-benar signifikan secara statistik atau hanya terjadi secara kebetulan akibat variasi acak (*sampling error*). Perbedaan rata-rata yang tampak besar secara kasat mata belum tentu menunjukkan adanya perbedaan yang nyata.

Sebagai contoh, dua strategi pemasaran mungkin memiliki rata-rata penjualan yang berbeda, tetapi tanpa uji hipotesis tidak dapat dipastikan apakah perbedaan tersebut benar-benar disebabkan oleh efektivitas strategi atau hanya karena fluktuasi data sampel. Dengan membandingkan `$p\text{-value}$` terhadap tingkat signifikansi, kita dapat membuat keputusan yang objektif dan berbasis bukti (*evidence-based*).

Jika keputusan diambil tanpa pengujian statistik yang tepat, perusahaan berisiko mengambil keputusan yang salah, seperti menganggap suatu strategi lebih efektif padahal sebenarnya tidak ada perbedaan yang signifikan. Hal ini dapat menyebabkan pemborosan biaya, alokasi sumber daya yang keliru, dan keputusan bisnis yang kurang akurat. Oleh karena itu, uji hipotesis diperlukan untuk memastikan bahwa keputusan yang diambil didukung oleh data yang valid dan dapat dipercaya.

---

## 🛠️ Metodologi & Tools yang Digunakan
Projek ini dikembangkan menggunakan kombinasi alat analisis data profesional:
* **Microsoft Excel:** Pengolahan data, rumus statistik lanjutan (`T.TEST`, `ANOVA`, `Data Analysis Toolpak`), serta simulasi distribusi sampling.
* **Python (Opsional/Pendukung):** Pandas, NumPy, Statsmodels, dan SciPy untuk validasi analisis inferensial lanjutan.

---

## 🚀 Cara Menjalankan / Menggunakan File ini
1. Clone repositori ini ke komputer lokal Anda:
   ```bash
   git clone [https://github.com/username/repository-name.git](https://github.com/username/repository-name.git)
2. Buka file Microsoft Excel utama yang disertakan dalam repositori: Hypothesis Testing Concepts.xlsx.
3. Eksplorasi setiap sheet mulai dari 1 A (T-Test), Anova, hingga sheet simulasi Population, Samples, dan Reflection Questions.
4. Aktifkan Data Analysis Toolpak di Excel jika ingin mereplikasi perhitungan $F$-Test, $t$-Test, atau ANOVA single factor.
