# Analisis Sentimen Pelanggan Menggunakan Apache Spark dan Logistic Regression

## Deskripsi Proyek

Proyek ini merupakan implementasi analisis sentimen pelanggan menggunakan dataset ulasan Yelp berskala besar. Tujuan utama proyek adalah mengklasifikasikan sentimen pelanggan menjadi **positif**, **netral**, dan **negatif** berdasarkan teks ulasan yang diberikan pelanggan.

Seluruh proses pengolahan data dan pelatihan model dilakukan menggunakan **Apache Spark (PySpark)** untuk menangani data berskala besar.

---

## Tujuan Proyek

1. Menganalisis sentimen pelanggan berdasarkan ulasan teks.
2. Mengidentifikasi pola perilaku pelanggan melalui data ulasan.
3. Menerapkan teknologi Big Data untuk memproses jutaan data ulasan.
4. Mengevaluasi performa model klasifikasi sentimen.

---

## Dataset

Dataset yang digunakan adalah **Yelp Open Dataset**.

Informasi dataset:

* Jumlah review: 6.990.280 ulasan
* Ukuran dataset: ±4.2 GB
* Format: JSON
* Sumber: Yelp Open Dataset

File utama yang digunakan:

* `yelp_academic_dataset_review.json`

---

## Teknologi yang Digunakan

### Big Data Tools

* Apache Spark
* PySpark

### Machine Learning

* Logistic Regression
* HashingTF
* Tokenizer
* StopWordsRemover

### Visualisasi

* Matplotlib
* Seaborn

### Environment

* Google Colab

---

## Arsitektur Sistem

Dataset Yelp
↓
Data Cleaning
↓
Labeling Sentimen
↓
Train-Test Split
↓
Tokenizer
↓
StopWords Removal
↓
HashingTF
↓
Logistic Regression
↓
Evaluasi Model
↓
Visualisasi Hasil

---

## Label Sentimen

Label sentimen dibentuk berdasarkan rating yang diberikan pengguna.

| Rating | Sentimen |
| ------ | -------- |
| 1 - 2  | Negative |
| 3      | Neutral  |
| 4 - 5  | Positive |

Encoding label:

| Sentimen | Label |
| -------- | ----- |
| Negative | 0     |
| Neutral  | 1     |
| Positive | 2     |

---

## Tahapan Pemrosesan Data

### 1. Data Cleaning

Meliputi:

* Mengubah teks menjadi huruf kecil (lowercase)
* Menghapus URL
* Menghapus karakter khusus
* Menghapus angka yang tidak diperlukan
* Menghapus spasi berlebih

### 2. Tokenisasi

Memecah kalimat menjadi kumpulan kata.

### 3. Stopword Removal

Menghapus kata umum yang tidak memberikan informasi penting.

### 4. Feature Extraction

Menggunakan HashingTF untuk mengubah teks menjadi representasi numerik yang dapat diproses oleh algoritma Machine Learning.

### 5. Model Training

Menggunakan Logistic Regression sebagai model klasifikasi sentimen.

---

## Cara Menjalankan Proyek

### 1. Clone Repository

```bash
git clone https://github.com/arsyadfillah/bigdata-project.git
cd bigdata-project
```

### 2. Upload Dataset Yelp

Unduh Yelp Open Dataset dari sumber resmi dan upload file:

```text
yelp_academic_dataset_review.json
```

ke Google Drive.

### 3. Buka Notebook

Buka file:

```text
Final_project_bigdata.ipynb
```

menggunakan Google Colab.

### 4. Mount Google Drive

```python
from google.colab import drive
drive.mount('/content/drive')
```

### 5. Jalankan Notebook

Jalankan seluruh cell secara berurutan:

1. Setup Spark
2. Load Dataset
3. Data Cleaning
4. Labeling Sentimen
5. Train-Test Split
6. Model Training
7. Evaluation
8. Visualization

---

## Hasil Evaluasi Model

Model Logistic Regression menghasilkan performa sebagai berikut:

| Metric    | Score  |
| --------- | ------ |
| Precision | 0.8428 |
| Recall    | 0.8622 |
| F1 Score  | 0.8466 |

Hasil menunjukkan bahwa model memiliki kemampuan yang baik dalam mengklasifikasikan sentimen pelanggan pada dataset berskala besar.

---

## Visualisasi

Visualisasi yang dihasilkan meliputi:

* Distribusi Sentimen
* Distribusi Rating
* Confusion Matrix
* Performa Model

---

## Struktur Repository

```text
bigdata-project/
│
├── Final_project_bigdata.ipynb
├── README.md
│

```

---

