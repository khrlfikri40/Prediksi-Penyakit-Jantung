# 🫀 Prediksi Risiko Penyakit Jantung (Heart Disease Classification)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0%2B-orange?style=for-the-badge&logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-Latest-150458?style=for-the-badge&logo=pandas)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

Proyek **Machine Learning** berbasis *Supervised Learning* untuk memprediksi apakah seorang pasien berisiko terkena penyakit jantung berdasarkan atribut medis klinis.

---

## 📌 Deskripsi Proyek

Penyakit jantung (*Heart Disease*) merupakan salah satu penyebab kematian utama secara global. Deteksi dini berbasis indikator medis dasar dapat membantu tenaga medis memberikan penanganan yang lebih cepat dan efektif.

Pada proyek ini, dibangun model **Random Forest Classifier** yang mampu mengklasifikasikan diagnosis pasien (Sehat vs. Berisiko Penyakit Jantung) menggunakan data atribut klinis seperti usia, tekanan darah, tingkat kolesterol, dan indikator EKG.

---

## 📊 Dataset Overview

Dataset yang digunakan berasal dari **UCI Heart Disease Repository (Cleveland Dataset)** yang memuat 14 atribut medis:

| Nama Kolom | Deskripsi | Jenis Data |
| :--- | :--- | :--- |
| `age` | Usia pasien (tahun) | Numerik |
| `sex` | Jenis kelamin (1 = Laki-laki, 0 = Perempuan) | Kategorikal |
| `cp` | Tipe nyeri dada / *Chest Pain* (1-4) | Kategorikal |
| `trestbps` | Tekanan darah istirahat (mm Hg) | Numerik |
| `chol` | Kolesterol serum (mg/dl) | Numerik |
| `fbs` | Gula darah puasa > 120 mg/dl (1 = True, 0 = False) | Kategorikal |
| `restecg` | Hasil EKG istirahat (0-2) | Kategorikal |
| `thalach` | Detak jantung maksimum yang dicapai | Numerik |
| `exang` | *Angina* akibat olahraga (1 = Ya, 0 = Tidak) | Kategorikal |
| `oldpeak` | Depresi ST akibat olahraga relatif terhadap istirahat | Numerik |
| `slope` | Kemiringan puncak segmen ST | Kategorikal |
| `ca` | Jumlah pembuluh darah utama (0-3) yang diwarnai fluorosopi | Numerik |
| `thal` | Hasil tes cacat thalassemia (3 = Normal, 6 = Cacat Tetap, 7 = Cacat Reversibel) | Kategorikal |
| **`target`** | **Status Penyakit Jantung (0 = Sehat, 1 = Berisiko)** | **Target Variable** |

---

## 🛠️ Alur Kerja Proyek (Workflow)

```
┌─────────────────────────┐
│  1. Data Loading & EDA  │  --> Memuat dataset UCI dan visualisasi distribusi target
└─────────────────────────┘
             │
             ▼
┌─────────────────────────┐
│  2. Data Preprocessing  │  --> Handling missing values, splitting data, & Feature Scaling
└─────────────────────────┘
             │
             ▼
┌─────────────────────────┐
│  3. Model Training      │  --> Pelatihan model Random Forest Classifier
└─────────────────────────┘
             │
             ▼
┌─────────────────────────┐
│  4. Model Evaluation    │  --> Evaluasi Akurasi, Classification Report, & Confusion Matrix
└─────────────────────────┘
```

---

## 📈 Hasil Evaluasi Model

Model **Random Forest Classifier** diuji menggunakan 20% data *test* dengan hasil sebagai berikut:

* **Akurasi Model:** `~83.61%`
* **Metrik Evaluasi Utama:**
  * **Precision:** Ketepatan model dalam mengidentifikasi pasien berisiko tanpa banyak *False Positive*.
  * **Recall:** Kemampuan model menangkap pasien yang benar-benar berisiko untuk meminimalkan keterlambatan penanganan (*False Negative*).

---

## 🚀 Cara Menjalankan Proyek

### 1. Clone Repositori
```bash
git clone https://github.com/USERNAME/prediksi-penyakit-jantung.git
cd prediksi-penyakit-jantung
```

### 2. Install Dependensi
```bash
pip install -r requirements.txt
```

### 3. Jalankan Jupyter Notebook
```bash
jupyter notebook predict_heart_disease.ipynb
```

---

## 📂 Struktur Repositori

```
.
├── predict_heart_disease.ipynb   # File utama Jupyter Notebook berisi seluruh kodingan ML
├── README.md                     # Dokumentasi proyek
└── requirements.txt              # Daftar library yang dibutuhkan
```

---

## 📝 Lisensi

Proyek ini menggunakan lisensi [MIT License](LICENSE) dan dibuat untuk keperluan portofolio Machine Learning Pemula.