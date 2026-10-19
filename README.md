# UTS Graf Sains Data

Repository ini berisi pengerjaan Ujian Tengah Semester (UTS) mata kuliah **Graf Sains Data** menggunakan Retailrocket Recommender System Dataset. Proyek ini mencakup pengolahan data, pembentukan graf, representasi interaksi pengguna dan item menggunakan Vector Space Model (VSM), serta sistem rekomendasi berbasis interaksi pengguna.

## File Utama

File utama pengerjaan terdapat pada notebook berikut:

**[`UTS GRAF.ipynb`](./UTS%20GRAF.ipynb)**

Notebook ini berisi tahapan pengolahan data, analisis graf, pembentukan VSM User dan VSM Item, serta rekomendasi dan evaluasi menggunakan data pelatihan dan pengujian.

## Struktur Folder

```text
UTS GRAF/
├── UTS GRAF.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── data/
    ├── category_tree.csv
    ├── events.csv
    ├── item_properties_part1.csv
    ├── item_properties_part2.csv
    └── filtered/
        ├── events_P1_training.csv
        └── events_P2_testing.csv
```

**Catatan:** Struktur di atas menunjukkan seluruh file dataset yang digunakan atau disiapkan dalam proyek. Tidak semua file ditampilkan di repository GitHub karena terdapat file berukuran besar yang dikecualikan.

## Dataset

Dataset yang digunakan adalah **Retailrocket Recommender System Dataset**, yang berisi data interaksi pengguna, kategori, dan properti item pada platform e-commerce.

### 1. Daftar Dataset

| Nama file | Deskripsi | Status di GitHub |
|---|---|---|
| `category_tree.csv` | Struktur hierarki kategori item, termasuk relasi kategori induk dan kategori anak. | **Diunggah** |
| `events.csv` | Data interaksi pengguna dengan item, termasuk waktu interaksi, ID pengguna, jenis event, ID item, dan ID transaksi jika tersedia. | **Diunggah** |
| `item_properties_part1.csv` | Bagian pertama data properti item, berisi informasi atribut item berdasarkan waktu dan identitas item. | **Tidak diunggah** |
| `item_properties_part2.csv` | Bagian kedua data properti item yang melengkapi data properti item pada bagian pertama. | **Tidak diunggah** |
| `events_P1_training.csv` | Data interaksi yang telah difilter untuk periode P1 dan digunakan sebagai data pelatihan. | **Diunggah** |
| `events_P2_testing.csv` | Data interaksi yang telah difilter untuk periode P2 dan digunakan sebagai data pengujian. | **Diunggah** |
| `ecommerce-dataset.zip` | Arsip dataset asli dalam format ZIP. | **Tidak diunggah** |

### 2. Alasan Dataset Tidak Diunggah

Beberapa file tidak disertakan dalam repository karena ukurannya besar dan melewati batas ukuran file GitHub.

| Nama file | Ukuran lokal | Alasan |
|---|---:|---|
| `item_properties_part1.csv` | Sekitar 461,88 MB | Melebihi batas maksimum 100 MB per file pada GitHub. |
| `item_properties_part2.csv` | Sekitar 389,99 MB | Melebihi batas maksimum 100 MB per file pada GitHub. |
| `ecommerce-dataset.zip` | Lebih dari 100 MB | Tidak diunggah untuk menghindari pengunggahan arsip besar yang tidak diperlukan jika file CSV sudah tersedia secara terpisah. |

Kedua file `item_properties` tetap menjadi bagian dari dataset yang digunakan atau tersedia secara lokal, tetapi tidak disertakan dalam repository karena batas ukuran file GitHub. File `ecommerce-dataset.zip` juga dikecualikan untuk menghindari duplikasi data berukuran besar.

### 3. Pembagian Data Training dan Testing

Data interaksi pada `events.csv` dibagi berdasarkan rentang waktu menjadi periode P1 sebagai data pelatihan dan periode P2 sebagai data pengujian.

#### P1 — Training Data

- **Nama file:** `events_P1_training.csv`
- **Jumlah data:** 1.201.045 baris
- **Rentang waktu:** 3 Mei 2015 pukul 03:00:04.384 hingga 30 Juni 2015 pukul 23:59:59.292
- **Kegunaan:** Membentuk representasi interaksi pengguna dan item, membangun graf, serta menghasilkan rekomendasi.

#### P2 — Testing Data

- **Nama file:** `events_P2_testing.csv`
- **Jumlah data:** 1.251.346 baris
- **Rentang waktu:** 1 Juli 2015 pukul 00:00:06.967 hingga 31 Agustus 2015 pukul 23:59:58.647
- **Kegunaan:** Menguji dan mengevaluasi hasil rekomendasi menggunakan interaksi pengguna pada periode setelah data pelatihan.

Pembagian berdasarkan waktu ini memungkinkan evaluasi rekomendasi menggunakan data periode berikutnya, sehingga data pengujian tidak digunakan untuk membangun rekomendasi pada periode pelatihan.

## Tools yang Digunakan

- Python
- Jupyter Notebook
- Pandas
- NumPy
- NetworkX
- Scikit-learn
- Neo4j

## Cara Menjalankan

1. Clone repository ini.
2. Siapkan Python dan dependensi yang tercantum di `requirements.txt`.
3. Pastikan file dataset yang dibutuhkan tersedia di folder `data/`.
4. Buka `UTS GRAF.ipynb` menggunakan Jupyter Notebook atau Visual Studio Code.
5. Jalankan setiap sel notebook secara berurutan.

Instalasi dependensi:

```bash
pip install -r requirements.txt
```

## CATATAN
- File utama pengerjaan adalah `UTS GRAF.ipynb`.
- File `.env` yang berisi konfigurasi kredensial Neo4j disimpan secara lokal dan tidak diunggah ke GitHub.
- Dataset yang dikecualikan harus tersedia secara lokal jika ada bagian notebook yang membutuhkannya.
- Beberapa file CSV memiliki ukuran besar, tetapi masih di bawah batas keras GitHub sebesar 100 MB per file sehingga tetap dapat diunggah meskipun muncul peringatan ukuran.

NAMA: Muhammad Rarendra Satiya

NIM: 23031554117
