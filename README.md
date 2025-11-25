# 📰 Klasifikasi Kategori Berita Detik.com

Repositori ini berisi implementasi lengkap untuk melakukan **klasifikasi kategori judul berita Detik.com** menggunakan tiga pendekatan:

1. **Metode Klasik** – TF-IDF + Naive Bayes
2. **Deep Learning** – LSTM
3. **Pretrained Model** – IndoBERT (Fine-Tuning)

Seluruh proses dituliskan dalam **satu file notebook utama** sehingga mudah dijalankan dari awal sampai akhir.

## 📌 Isi Repository

### 📄 **BERITA_DETIK.ipynb**

Notebook utama yang berisi seluruh tahapan:

1. **Scraping berita**
2. **Preprocessing teks**
3. **Modelling**:

   * TF-IDF + Naive Bayes
   * LSTM
   * IndoBERT
4. **Evaluasi model**
5. **Perbandingan performa 3 pendekatan**

Notebook ini dapat dijalankan dari awal hingga akhir tanpa file tambahan lain.

### 📂 Dataset

#### 📄 **berita_detik_5_kategori.csv**

Dataset hasil scraping dari Detik.com yang berisi:

* Judul berita
* Kategori (5 label)
* Tautan (opsional)

Dataset ini merupakan **data mentah (raw)** sebelum preprocessing.

---

#### 📄 **berita_clean.csv**

Dataset yang sudah melalui tahap preprocessing, termasuk:

* Lowercasing
* Menghapus angka & tanda baca
* Normalisasi teks
* Stopword removal
* Label encoding

Dataset ini digunakan untuk training model TF-IDF, LSTM, dan IndoBERT.

---

## 🚀 Cara Menjalankan

1. Download repository ini atau clone:

```
git clone https://github.com/septindwikurnia/Klasifikasi-Kategori-Berita-Detik.git
```

2. Jalankan notebook:

```
BERITA_DETIK.ipynb
```

3. Ikuti sel dari atas ke bawah.

---

## 📊 Model yang Digunakan

| Pendekatan               | Deskripsi                                      |
| ------------------------ | ---------------------------------------------- |
| **TF-IDF + Naive Bayes** | Model baseline cepat dan ringan                |
| **LSTM**                 | Deep learning berbasis sequence                |
| **IndoBERT**             | Fine-tuning model transformer Bahasa Indonesia |

(*Isi akurasinya dapat ditambahkan setelah training.*)

---

## 🛠 Tools yang Digunakan

* Python
* Pandas, NumPy
* Scikit-Learn
* TensorFlow/Keras
* PyTorch
* Transformers (HuggingFace)
* BeautifulSoup
* Matplotlib

---

## 📄 Lisensi

Proyek ini menggunakan lisensi **MIT License**.

---

Kalau kamu mau, aku bisa tambahkan:

🔥 badge GitHub (Python version, License, Model Accuracy)
🔥 contoh hasil prediksi model
🔥 preview grafik hasil evaluasi

Cukup bilang **“tambah badge”** atau **“tambah contoh prediksi”** ya!
