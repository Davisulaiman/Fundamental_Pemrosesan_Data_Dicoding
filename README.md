Berikut adalah versi rapi dan terstruktur dari file `README.md` Anda:

---

```markdown
# Submission Dicoding Fundamental Pemrosesan Data

Proyek ini merupakan bagian dari submission kelas **Fundamental Pemrosesan Data** di Dicoding. Proyek ini melakukan proses ETL (Extract, Transform, Load) terhadap data produk fashion dari situs [Fashion Studio Dicoding](https://fashion-studio.dicoding.dev/). Data diambil dari halaman 1 hingga 50, kemudian dibersihkan dan disimpan ke berbagai tujuan.

## Struktur Proyek

```

```
.
├── main.py
├── utils/
│   ├── extract.py
│   ├── transform.py
│   └── load.py
├── tests/
│   ├── test_extract.py
│   ├── test_transform.py
│   └── test_load.py
├── products.csv
├── google-sheets-api.json
└── README.md
```

## Fitur

- **Extract**: Mengambil data produk dari situs menggunakan `requests` dan `BeautifulSoup`.
- **Transform**: Membersihkan dan memformat data menggunakan `pandas`.
- **Load**: Menyimpan data hasil scraping ke:
  - File CSV (`products.csv`)
  - Google Sheets ([Link Spreadsheet](https://docs.google.com/spreadsheets/d/1aITkzRRoHxUKjVTMmWys6g-wxJ8Cww5BER4r5NvahgA/edit?hl=id&gid=0))
  - PostgreSQL Database

## Cara Menjalankan

### Jalankan Proses ETL

```bash
python main.py
````

### Jalankan Unit Test

```bash
python -m unittest discover tests
```

### Jalankan Test Coverage

```bash
coverage run -m unittest discover tests
coverage report -m
```

## Konfigurasi Database

Edit bagian `load_to_postgresql()` di `utils/load.py` agar sesuai dengan konfigurasi lokal Anda:

```python
username = 'postgres'
password = 'G1A022001'
host = 'localhost'
port = '5432'
database = 'etl_db'
```

## Autentikasi Google Sheets

Pastikan Anda memiliki file `google-sheets-api.json` di direktori utama sebagai kredensial akses ke Google Sheets API.

## Penulis

* 🧑 Nama: Davi Sulaiman
* 📧 Email: [davisulaiman1@gmail.com](mailto:davisulaiman1@gmail.com)

```

---

