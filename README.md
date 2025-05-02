Berikut adalah file `README.md` yang dirancang berdasarkan struktur dan fungsionalitas yang ada pada proyek Anda:

---

```markdown
# ETL Web Scraping Produk Fashion

Proyek ini melakukan proses ETL (Extract, Transform, Load) terhadap data produk fashion dari situs [Fashion Studio Dicoding](https://fashion-studio.dicoding.dev/). Data produk diambil dari halaman 1 hingga 50, kemudian dibersihkan, dan disimpan ke dalam tiga tujuan: file CSV, Google Sheets, dan database PostgreSQL.

## Struktur Proyek

```

.
├── main.py
├── utils/
│   ├── extract.py
│   ├── transform.py
│   └── load.py
├── tests/
│   ├── test\_extract.py
│   ├── test\_transform.py
│   └── test\_load.py
├── products.csv
├── google-sheets-api.json
└── README.md

````

## Fitur

- **Extract**: Mengambil data produk dari situs web dengan menggunakan `requests` dan `BeautifulSoup`.
- **Transform**: Membersihkan data hasil scraping dan mengubahnya menjadi format yang sesuai menggunakan `pandas`.
- **Load**: Menyimpan data ke:
  - File CSV (`products.csv`)
  - Google Sheets ([Link](https://docs.google.com/spreadsheets/d/1aITkzRRoHxUKjVTMmWys6g-wxJ8Cww5BER4r5NvahgA/edit?hl=id&gid=0))
  - Database PostgreSQL

## Cara Menjalankan

### 1. Jalankan ETL
```bash
python main.py
````

### 2. Jalankan Unit Test

```bash
python -m unittest discover tests
```

### 3. Jalankan Test Coverage

```bash
coverage run -m unittest discover tests
coverage report -m
```

## Konfigurasi Database

Ubah kredensial PostgreSQL di `utils/load.py` bagian `load_to_postgresql()` sesuai dengan konfigurasi lokal Anda:

```python
username = 'postgres'
password = 'G1A022001'
host = 'localhost'
port = '5432'
database = 'etl_db'
```

## Kredensial Google Sheets

File `google-sheets-api.json` dibutuhkan untuk autentikasi API Google Sheets. Pastikan Anda memiliki file ini di direktori utama proyek.

## Ketergantungan

Install semua ketergantungan yang diperlukan:

```bash
pip install -r requirements.txt
```

```

## Penulis

* 🧑 Nama: Davi Sulaiman
* 📧 Email: davisulaiman1@gmail.com

```

