# 📰 News Scraper dengan BeautifulSoup

## 📌 Deskripsi Project

Project ini bertujuan untuk melakukan scraping data berita dari RSS Feed Antara News secara otomatis. Data yang diambil meliputi judul, link, tanggal, dan ringkasan berita, kemudian disimpan dalam format terstruktur (CSV & Excel) untuk analisis lebih lanjut.

---

## 🎯 Tujuan

* Mengumpulkan data berita secara otomatis (automation)
* Melakukan data cleaning dari HTML
* Menyimpan data dalam format siap analisis
* Melakukan filtering topik (contoh: teknologi)

---

## ⚙️ Tech Stack

* Python
* requests
* BeautifulSoup
* pandas
* feedparser

---

## 📊 Output Data

Dataset yang dihasilkan memiliki struktur:

| Kolom     | Deskripsi         |
| --------- | ----------------- |
| kategori  | Kategori berita   |
| judul     | Judul berita      |
| link      | URL artikel       |
| ringkasan | Ringkasan berita  |
| tanggal   | Tanggal publikasi |
| scrape_at | Waktu scraping    |

---

## 🔍 Proses Pipeline

1. Mengambil data dari RSS Feed
2. Parsing XML menggunakan feedparser
3. Cleaning HTML menggunakan BeautifulSoup
4. Menyimpan data ke DataFrame
5. Export ke CSV & Excel
6. Filtering berita berdasarkan keyword

---

## 🧠 Contoh Penggunaan BeautifulSoup

```python
from bs4 import BeautifulSoup

html = entry.get('summary', '')
clean_text = BeautifulSoup(html, 'html.parser').get_text()
```

---

## ▶️ Cara Menjalankan

```bash
pip install requests beautifulsoup4 pandas feedparser lxml
```

```python
scraper = NewsScraper(headers=HEADERS)
data = scraper.run_all(RSS_FEEDS)
```

---

## 📁 Output

* `news_data_YYYYMMDD.csv`
* `news_data_YYYYMMDD.xlsx`

---

## 🚧 Pengembangan Selanjutnya

* Menambahkan analisis tren berita
---

## 👩‍💻 Author

Nabella Ayu Giwanti