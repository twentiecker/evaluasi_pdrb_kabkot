# SISTEM EVALUASI PDRB KABUPATEN/KOTA

## 1. Pendahuluan

Sistem Evaluasi PDRB Kabupaten/Kota merupakan aplikasi berbasis Python yang dirancang untuk mendukung proses evaluasi data Produk Domestik Regional Bruto (PDRB) pada tingkat kabupaten/kota.

Aplikasi ini bertujuan untuk:

- Membantu proses evaluasi data secara sistematis dan terstandarisasi
- Mengidentifikasi nilai yang melewati batas evaluasi (threshold)
- Menghasilkan output evaluasi yang terstruktur per provinsi
- Mendukung proses monitoring dan pengendalian kualitas data PDRB

Aplikasi dikembangkan menggunakan Python 3.10.11 dan dijalankan melalui Jupyter Notebook.

---

## 2. Ruang Lingkup

Sistem ini digunakan untuk:

1. Evaluasi PDRB Tahunan
2. Evaluasi PDRB Triwulanan

Evaluasi dilakukan berdasarkan aturan (rule) dan batas nilai (threshold) yang dapat disesuaikan sesuai kebutuhan analisis.

---

## 3. Struktur Direktori

Struktur direktori proyek adalah sebagai berikut:

```bash
evaluasi_pdrb_kabkot/
│
├── main_2025.ipynb
├── main_2023_2024.ipynb
├── input/
│   └── Evaluasi.xlsx
├── output/
│   └── (hasil evaluasi per provinsi)
├── requirements.txt
└── README.md
```

Penjelasan:

- `main_2025.ipynb`  
  Digunakan untuk evaluasi tahun 2025, baik tahunan maupun triwulanan.

- `main_2023_2024.ipynb`  
  Digunakan khusus untuk evaluasi tahunan tahun 2023 dan 2024.

- Folder `input/`  
  Digunakan untuk menyimpan file sumber dengan nama wajib:

- Folder `output/`  
  Digunakan untuk menyimpan hasil evaluasi yang dihasilkan sistem.  
  Output akan berupa beberapa file yang dikelompokkan berdasarkan provinsi.

---

## 4. Mekanisme Evaluasi

### 4.1 Evaluasi Tahunan

Untuk evaluasi tahunan:

- Tahun 2025 → gunakan `main_2025.ipynb`
- Tahun 2023 dan 2024 → gunakan `main_2023_2024.ipynb`

Pada masing-masing notebook tersedia parameter threshold yang dapat disesuaikan sesuai kebijakan evaluasi.

---

### 4.2 Evaluasi Triwulanan

Untuk evaluasi triwulanan:

- Gunakan `main_2025.ipynb`

Parameter threshold dapat diubah pada bagian konfigurasi awal notebook.

---

## 5. Spesifikasi Teknis

### 5.1 Versi Python

Aplikasi ini menggunakan: Python 3.10.11

Disarankan menggunakan versi yang sama untuk menghindari ketidaksesuaian dependency.

---

### 5.2 Library yang Digunakan

Library utama:

- pandas
- openpyxl

Library bawaan Python:

- os
- re

---

## 6. Instalasi dan Persiapan Lingkungan

### 6.1 Membuat Virtual Environment (Direkomendasikan)

```bash
python -m venv venv
```

Aktivasi environment:
Windows:

```bash
venv\Scripts\activate
```

Mac/Linux:

```bash
source venv/bin/activate
```

### 6.2 Instalasi Dependency

Install seluruh dependency yang dibutuhkan:

```bash
pip install -r requirements.txt
```

---

## 7. Prosedur Penggunaan

1. Pastikan folder input/ dan output/ tersedia.

2. Letakkan file sumber dengan nama: "Evaluasi.xlsx"

3. Buka notebook sesuai kebutuhan: "main_2025.ipynb" atau "main_2023_2024.ipynb"
4. Jalankan seluruh sel (Run All Cells).
5. Hasil evaluasi akan tersimpan secara otomatis pada folder: "output/"

---

## 8. Kustomisasi Parameter Evaluasi

Nilai threshold dan parameter evaluasi dapat disesuaikan pada bagian awal notebook.

Perubahan parameter harus dilakukan dengan memperhatikan:

- Konsistensi metodologi evaluasi

- Standar yang berlaku

- Dokumentasi perubahan (jika digunakan dalam konteks institusi)

---

## 9. Ketentuan dan Catatan Penting

- Nama file input wajib: Evaluasi.xlsx

- Struktur dan format Excel harus sesuai template yang digunakan sistem

- Folder input/ dan output/ harus tersedia sebelum proses dijalankan

- Disarankan tidak mengubah struktur logika utama tanpa pemahaman teknis yang memadai

---

## 10. Penutup

Sistem ini dikembangkan untuk meningkatkan efisiensi, konsistensi, dan akuntabilitas dalam proses evaluasi data PDRB Kabupaten/Kota.

Pengembangan lanjutan dapat mencakup:

- Otomatisasi validasi data

- Integrasi dengan sistem basis data

- Pengembangan antarmuka pengguna (GUI/Web Interface)
