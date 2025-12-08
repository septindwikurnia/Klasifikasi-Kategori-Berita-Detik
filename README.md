# **Klasifikasi Berita Detik 5 Kategori**

Repository ini berisi implementasi sistem klasifikasi teks untuk berita Detik ke dalam 5 kategori menggunakan pendekatan:

* **Metode Klasik** (TF-IDF + SVM)
* **Deep Learning** (LSTM)
* **Pretrained Model** (IndoBERT)
* **Fine-Tuning Efisien** (LoRA pada IndoBERT)

Seluruh proses pengolahan data, pelatihan model, dan evaluasi dilakukan melalui Google Colab.

---

## **1. Struktur Folder**

```
data/
  raw/                        # Dataset mentah
    - berita_detik_5_kategori.csv
  processed/                  # Dataset hasil preprocessing
    - berita_clean.csv

models/
  classic/                    # Artefak TF-IDF + SVM
  indobert/                   # Tokenizer + config IndoBERT
  lora/                       # Adapter LoRA + tokenizer
  lstm/                       # Model dan artefak LSTM

notebooks/
  BERITA_DETIK_5_KATEGORI.ipynb   # Notebook utama

README.md
```

---

## **2. Alur Penelitian**

1. **Data Preparation**

   * Pembersihan teks (lowercase, stopword removal, stemming).
   * Penyimpanan hasil di `data/processed/`.

2. **Modeling**

   * **TF-IDF + SVM** → baseline klasik.
   * **LSTM** → pemodelan berbasis deep learning.
   * **IndoBERT** → fine-tuning model pretrained.
   * **LoRA** → fine-tuning parameter-efficient untuk IndoBERT.

3. **Evaluation**

   * Menggunakan accuracy, precision, recall, F1-score, dan confusion matrix.

---

## **3. Artefak Model**

Model dan artefak disimpan pada folder `models/`:

* Folder *classic* → TF-IDF + SVM
* Folder *lstm* → tokenizer + label encoder + model `.h5`
* Folder *indobert* → tokenizer & config (model besar tidak disertakan)
* Folder *lora* → adapter LoRA dan tokenizer

*Catatan:* File model besar (>100MB) tidak diunggah ke GitHub untuk memenuhi batas ukuran repository.

---

## **4. Notebook Utama**

Seluruh tahapan mulai dari pemrosesan data hingga pelatihan dan evaluasi model terdapat pada:

```
notebooks/BERITA_DETIK_5_KATEGORI.ipynb
```

Notebook ini dapat dijalankan langsung pada Google Colab.

---

## **5. Menjalankan Proyek**

1. Clone repository:

```bash
git clone https://github.com/USERNAME/NAMA-REPO.git
```

2. Buka notebook dalam folder `notebooks/`.

3. Sesuaikan path dataset dan model jika diperlukan.

---

## **6. Catatan Tambahan**

* Model pretrained penuh (IndoBERT) perlu diunduh ulang melalui kode di notebook.
* LoRA digunakan untuk memperkecil ukuran fine-tuning dan mempermudah penyimpanan artefak di GitHub.
