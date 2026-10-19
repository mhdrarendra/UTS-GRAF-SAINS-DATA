# UTS Graf Sains Data

Repository ini berisi pengerjaan Ujian Tengah Semester (UTS) mata kuliah **Graf Sains Data** menggunakan dataset e-commerce RetailRocket.

## File Utama

File utama pengerjaan dan analisis terdapat pada notebook berikut:

**[`UTS GRAF.ipynb`](./UTS%20GRAF.ipynb)**

Notebook tersebut berisi tahapan pengolahan data, pembentukan graf, analisis interaksi pengguna dan item, serta sistem rekomendasi berdasarkan interaksi pengguna.

## Struktur Folder

```text
UTS GRAF/
├── UTS GRAF.ipynb
├── data/
│   ├── category_tree.csv
│   ├── events.csv
│   └── filtered/
│       ├── events_P1_training.csv
│       └── events_P2_testing.csv
├── requirements.txt
├── .gitignore
└── README.md
```

*Catatan: Beberapa file dataset berukuran besar tidak disertakan dalam repository.*

## Dataset

Dataset yang digunakan adalah **RetailRocket E-commerce Dataset**, yang berisi informasi interaksi pengguna dengan item pada platform e-commerce.

Data mencakup:
- `events.csv`: data interaksi pengguna, seperti melihat item, menambahkan item ke keranjang, dan transaksi.
- `category_tree.csv`: informasi struktur kategori item.
- `events_P1_training.csv`: data interaksi untuk periode pelatihan.
- `events_P2_testing.csv`: data interaksi untuk periode pengujian.

## Teknologi

- Python
- Jupyter Notebook
- Pandas dan NumPy
- NetworkX
- Scikit-learn
- Neo4j

## Cara Menjalankan

1. Clone repository ini.
2. Install library yang dibutuhkan menggunakan `requirements.txt`.
3. Buka file `UTS GRAF.ipynb` menggunakan Jupyter Notebook atau Visual Studio Code.
4. Pastikan file dataset yang dibutuhkan tersedia di folder `data/`.
5. Jalankan setiap sel notebook secara berurutan.

Instalasi dependensi:

```bash
pip install -r requirements.txt
```

## Catatan

- File utama untuk melihat seluruh proses pengerjaan adalah `UTS GRAF.ipynb`.
- Dataset berukuran besar tertentu tidak disertakan karena keterbatasan ukuran file pada GitHub.
- Jika notebook menggunakan koneksi Neo4j, konfigurasi kredensial disimpan secara lokal pada file `.env` dan tidak disertakan dalam repository.

