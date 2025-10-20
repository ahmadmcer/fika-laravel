# 📚 Book API (Laravel)

Book API adalah backend sederhana berbasis **Laravel** yang menyediakan REST API untuk mengelola data buku.  
Aplikasi ini mendukung fitur **CRUD (Create, Read, Update, Delete)** melalui endpoint `/api/books`.

---

## 🚀 Fitur

- Tambah data buku (Create)
- Lihat semua buku (Read)
- Ubah data buku (Update)
- Hapus buku (Delete)
- API berbasis JSON, siap diintegrasikan dengan Flutter

---

## ⚙️ Persyaratan Sistem

- PHP >= 8.1
- Composer
- MySQL / MariaDB
- Laravel 10+

---

## 🛠️ Cara Instalasi

1. **Clone repository**

   ```bash
   git clone https://github.com/yourusername/book-api.git
   cd book-api

2. **Install dependency**

   ```bash
   composer install
   ```

3. **Salin file environment**

   ```bash
   cp .env.example .env
   ```

4. **Konfigurasi database di `.env`**

    Sesuaikan pengaturan database di file `.env` sesuai dengan konfigurasi lokal Anda.

    ```env
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=book_api
    DB_USERNAME=root
    DB_PASSWORD=
    ```

5. **Generate application key**

    ```bash
    php artisan key:generate
    ```

6. **Jalankan migrasi database**

    ```bash
    php artisan migrate
    ```

7. **Jalankan server lokal**

    ```bash
    php artisan serve
    ```

    Server akan berjalan di `http://127.0.0.1:8000`

---

## 🔗 Endpoint API

---------------------------------------------------------

| Method | Endpoint        | Deskripsi               |
---------------------------------------------------------

| GET    | /api/books     | Mendapatkan semua buku  |
| GET    | /api/books/{id} | Mendapatkan buku by ID  |
| POST   | /api/books     | Menambah buku baru      |
| PUT    | /api/books/{id} | Mengubah data buku by ID|
| DELETE | /api/books/{id} | Menghapus buku by ID    |
---------------------------------------------------------

---

## 📦 Contoh Request

### Dapatkan Semua Buku

**GET** `/api/books`

### Dapatkan Buku by ID

**GET** `/api/books/{id}`

### Tambah Buku

**POST** `/api/books`

```json
{
    "title": "Judul Buku",
    "author": "Nama Penulis",
    "published_year": 2023
}
```

### Update Buku

**PUT** `/api/books/{id}`

```json
{
    "title": "Judul Buku Updated",
    "author": "Nama Penulis Updated",
    "published_year": 2024
}
```

### Hapus Buku

**DELETE** `/api/books/{id}`

---

## 🧩 Struktur Direktori Utama

```
book-api/
├── app/
│   └── Http/Controllers/Api/BookController.php
├── database/
│   └── migrations/
├── routes/
│   └── api.php
├── .env
├── composer.json
└── README.md
```

---
