# 🚀 Databricks Certified Associate Developer for Apache Spark™ (Python)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Apache Spark](https://img.shields.io/badge/Apache%20Spark-3.5-orange?style=for-the-badge&logo=apachespark&logoColor=white)](https://spark.apache.org/)
[![Delta Lake](https://img.shields.io/badge/Delta%20Lake-Enabled-blueviolet?style=for-the-badge&logo=deltalake&logoColor=white)](https://delta.io/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

> **Repositori Praktik & Dokumentasi**
>
> Selamat datang di repositori pembelajaran Databricks Certified Associate Developer for Apache Spark. Repositori ini berisi implementasi kode mendalam, eksperimen teknis, dan dokumentasi hasil belajar yang diadaptasi dari materi ahli.

---

## 🌟 Tentang Proyek Ini

Repositori ini adalah **laboratorium eksperimental** di mana dilakukan membedah konsep-konsep inti Apache Spark menggunakan Python (PySpark). Setiap bab mewakili langkah maju dalam memahami bagaimana Spark memproses Big Data, mulai dari manipulasi baris sederhana hingga integrasi **Delta Lake** dan Machine Learning.

### 📚 Kredit & Referensi Utama
Materi dasar dan kurikulum pembelajaran diadaptasi dari buku:
*   **Judul:** *Databricks Certified Associate Developer for Apache Spark Using Python*
*   **Penulis:** Saba Shah
*   **Penerbit:** Packt Publishing (2024)
*   **Repo Asli:** [PacktPublishing/Databricks-Certified-Associate-Developer-for-Apache-Spark-using-Python](https://github.com/PacktPublishing/Databricks-Certified-Associate-Developer-for-Apache-Spark-using-Python)

*Catatan: Repositori ini dikelola secara independen untuk tujuan edukasi dan dokumentasi pribadi.*

---

## 🗂 Struktur & Bedah Kode (Code Deep Dive)

Berikut adalah rincian mendalam tentang apa yang ada di setiap direktori dan konsep teknis yang diterapkan:

| Direktori | Topik Utama | Highlight Teknis & Implementasi |
| :--- | :--- | :--- |
| **`Chapter04/`** | **Spark SQL & DataFrame API** | • **Data Creation:** Membuat DataFrame dari `Row` objects, lists, dan Pandas.<br>• **Schema Definition:** Eksplorasi inferensi skema vs definisi eksplisit.<br>• **Manipulasi Tanggal:** Penggunaan `datetime` dan `date` types dalam Spark.<br>• **Transformasi:** `select`, `filter`, `groupBy`, dan agregasi dasar. |
| **`Chapter05/`** | **Advanced Ops & Delta Lake** | • **Delta Lake Integration:** Konfigurasi `SparkSession` dengan `io.delta` package untuk fitur ACID transactions.<br>• **Complex Types:** Manipulasi tipe data `Struct`, `Array`, dan `Map`.<br>• **UDFs:** Implementasi User Defined Functions Python vs Pandas UDFs untuk performa.<br>• **File Formats:** Perbandingan baca/tulis CSV, ORC, dan Parquet. |
| **`Chapter06/`** | **Architecture & Optimization** | • **Spark Internals:** Memahami DAG, Jobs, Stages, dan Tasks.<br>• **Catalyst Optimizer:** Bagaimana Spark mengoptimalkan query logical plan.<br>• **Caching Strategies:** Penggunaan `cache()` vs `persist()` dan dampaknya pada memori.<br>• **Broadcasting:** Optimasi join menggunakan broadcast variables. |
| **`Chapter07/`** | **Spark Streaming** | • **Structured Streaming:** Konsep micro-batch processing.<br>• **Input Sources:** Membaca data streaming dari file (sebagai simulasi).<br>• **Window Operations:** Event-time windows dan handling late data.<br>• **Output Sinks:** Menulis stream ke console atau memory untuk debugging. |
| **`Chapter08/`** | **Machine Learning (MLlib)** | • **ML Pipeline:** Membangun pipeline `VectorAssembler` ➔ `Model`.<br>• **Feature Engineering:** Transformasi data mentah menjadi vektor fitur.<br>• **Regression:** Studi kasus prediksi harga rumah (`HousePricePrediction.csv`) menggunakan algoritma regresi.<br>• **Evaluasi:** Mengukur performa model dengan metrics standar. |

---

### 💎 Dokumentasi

### 📄 [Databricks Certified Report.pdf](./Databricks%20Certified%20Report.pdf)
Jangan lewatkan file ini. Ini adalah **laporan dokumentasi**. Di dalamnya terdapat:
*   Rangkuman eksekutif dari konsep-konsep tersulit.
*   Analisis pola soal sertifikasi.
*   Catatan kaki tentang "gotchas" dan jebakan umum saat bekerja dengan Spark.

---

## ⚙️ Setup Environment (Windows Optimized)

Salah satu tantangan terbesar menjalankan Spark di Windows adalah konfigurasi `HADOOP_HOME` dan `winutils.exe`. Kode di repositori ini telah dikonfigurasi secara khusus untuk menangani hal tersebut.

### Snippet Konfigurasi (Local Windows)
Anda akan melihat pola konfigurasi ini di setiap notebook untuk memastikan stabilitas di Windows:

```python
import os
import sys
from pyspark.sql import SparkSession

# Konfigurasi Path Windows
os.environ['HADOOP_HOME'] = "C:\\hadoop"
os.environ['PYSPARK_PYTHON'] = sys.executable
os.environ['PYSPARK_DRIVER_PYTHON'] = sys.executable

# JVM Options untuk mengatasi limitasi Java terbaru
jvm_options = (
    "--add-opens=java.base/java.lang=ALL-UNNAMED "
    "--add-opens=java.base/java.nio=ALL-UNNAMED "
    # ... (opsi lainnya)
)
```

### Cara Menjalankan di Lokal

1.  **Clone Repositori**
    ```bash
    git clone https://github.com/username-anda/repo-ini.git
    cd repo-ini
    ```

2.  **Persiapkan Python Environment**
    ```bash
    python -m venv venv
    .\venv\Scripts\Activate
    pip install pyspark pandas jupyter notebook delta-spark
    ```

3.  **Jalankan Jupyter**
    ```bash
    jupyter notebook
    ```
    Buka file `.ipynb` di browser Anda dan jalankan setiap sel.

---

## 🤝 Kontribusi & Lisensi

Repositori ini dilisensikan di bawah **MIT License**.
Anda bebas menggunakan kode ini untuk pembelajaran Anda sendiri. Jika Anda menggunakan materi dari sini, mohon sertakan atribusi ke repositori ini dan penulis aslinya.

---

<div align="center">

**Happy Coding & Good Luck on Your Certification! 🚀**

<sub>Diedit oleh [Muhammad Zaky Farhan]</sub>

</div>
