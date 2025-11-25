# 📰 Klasifikasi Kategori Berita Detik.com

Repositori ini berisi implementasi lengkap untuk melakukan **klasifikasi kategori judul berita Detik.com** menggunakan tiga pendekatan berbeda:

1. **Metode Klasik** – TF-IDF + Naive Bayes
2. **Deep Learning** – LSTM
3. **Pretrained Model** – IndoBERT (Fine-Tuning)

Semua proses mulai dari **scraping → preprocessing → training → evaluasi** ditulis dalam **1 file notebook utama**.

---

## 📌 Isi Repository

### 📄 **BERITA_DETIK.ipynb**

Notebook utama yang berisi seluruh pipeline:

1. **Scraping berita Detik.com**
2. **Preprocessing teks** (cleaning, normalisasi, stopword, tokenizing)
3. **Training model**:

   * TF-IDF + Naive Bayes
   * LSTM
   * IndoBERT
4. **Evaluasi dan perbandingan hasil**
5. **Visualisasi metrik model**

Notebook bisa dijalankan langsung dari awal sampai akhir.

---

## 📂 Dataset

### 📄 **berita_detik_5_kategori.csv**

Dataset **mentah hasil scraping**, berisi:

* Judul berita
* 5 kategori (label dari Detik.com)
* URL berita (opsional)

### 📄 **berita_clean.csv**

Dataset **setelah preprocessing**, meliputi:

* Lowercase
* Hapus angka & tanda baca
* Normalisasi teks
* Stopword removal
* Label encoding

Dataset ini digunakan untuk ketiga model.

---

## 🏷️ Kategori Berita yang Digunakan

Dataset terdiri dari **5 kategori utama**:

1. **News**
2. **Finance**
3. **Sport**
4. **Tech**
5. **Entertainment**

---

## 📊 Hasil Evaluasi Model

Berikut performa singkat ketiga pendekatan:

| Pendekatan                      | Akurasi |
| ------------------------------- | ------- |
| **TF-IDF + Naive Bayes**        | **88%** |
| **Deep Learning – LSTM**        | **42%** |
| **Pretrained Model – IndoBERT** | **88%** |

> Catatan: Nilai akurasi dapat sedikit berbeda tergantung preprocessing dan random seed, tetapi hasil di atas mewakili performa yang diperoleh dari notebook.

---

## 🛠 Tools & Library yang Digunakan

* Python
* Pandas, NumPy
* Scikit-Learn
* TensorFlow / Keras
* PyTorch
* HuggingFace Transformers
* BeautifulSoup (scraping)
* Matplotlib / Seaborn

---

## 🚀 Cara Menjalankan

1. Clone repository:

   ```bash
   git clone https://github.com/septindwikurnia/Klasifikasi-Kategori-Berita-Detik.git
   ```

2. Buka dan jalankan:

   ```
   BERITA_DETIK.ipynb
   ```

3. Eksekusi sel secara berurutan dari atas ke bawah.

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan pembelajaran dan penelitian akademik.

---
