# BE-PBF-KRS

BE-PBF-KRS adalah aplikasi backend web untuk sistem Kartu Rencana Studi (KRS) yang dibangun menggunakan CodeIgniter4. Proyek ini bertujuan untuk memudahkan mahasiswa dalam menyusun KRS secara online, memberikan admin kemudahan dalam mengelola data mahasiswa juga mata kuliah, menyajikan data dengan rapi serta terstruktur pada frontend.

## Fitur

-   Autentikasi pengguna (login & registrasi)
-   Manajemen data mahasiswa
-   Manajemen data mata kuliah
-   Penyusunan KRS online
-   API Catching yang mudah
-   Strukturisasi API yang jelas, termasuk query dalam mengambil data dari database

## Teknologi yang Digunakan

-   CodeIgniter4
-   PHP
-   MySQL
-   JSON Web Token

```bash
https://jwt.io/
```

## Instalasi

### 1. Clone repositori

Clone repositori Back-End ke dalam direktori lokal:

```bash
git clone https://github.com/ndan47/BE-PBF-KRS.git
cd BE-PBF-KRS
```

### 2. Instal dependensi PHP

Install semua dependensi yang dibutuhkan menggunakan Composer:

```bash
composer install
```

### 4. Konfigurasi Environment

## Salin file .env.example menjadi .env

### 5. Nyalakan Web Server dengan Laragon atau XAMPP

### 6. Jalankan server lokal

```bash
php spark serve
```

### Aplikasi akan berjalan di http://localhost:8080.

## Struktur Direktori

-   app/ - Berisi logika utama aplikasi: Controller, Model, Entity, Filter, dan konfigurasi khusus aplikasi (Config/)

-   public/ - Entry point aplikasi (seperti index.php) dan tempat menyimpan file yang bisa diakses publik, seperti gambar, CSS, dan JavaScript

-   writable/ - Folder untuk file yang ditulis oleh aplikasi, seperti cache, logs, session, dan upload file

-   system/ - Berisi inti (core) framework

-   tests/ - Folder untuk unit testing, termasuk file PHPUnit

-   vendor/ - Berisi dependensi pihak ketiga yang dikelola oleh Composer

-   .env - File konfigurasi environment (database, baseURL, dsb.) yang dapat diaktifkan dan diedit sesuai kebutuhan

###
## 📚 Endpoint untuk Mahasiswa, Mata Kuliah, Prodi, dan KRS

### Mahasiswa

* **Daftar Mahasiswa**

  * **Endpoint**: `GET http://localhost:8080/api/mahasiswa`
  * **Header**:

```
Authorization: Bearer <jwt_token_here>
```

* **Tambah Mahasiswa**

  * **Endpoint**: `POST http://localhost:8080/api/mahasiswa`
  * **Body JSON**:

```json
{
    "nama_mahasiswa": "Hendra Satria",
    "alamat_mahasiswa": "Jalan Katik",
    "id_prodi": "900"
}
```

### Mata Kuliah

* **Daftar Dosen**

  * **Endpoint**: `GET http://localhost:8080/api/matkul`
  * **Header**:

```
Authorization: Bearer <jwt_token_here>
```

* **Tambah Mata Kuliah**

  * **Endpoint**: `POST http://localhost:8080/api/matkul`
  * **Body JSON**:

```json
{
    "semester": 4,
    "nama_matkul": "Ilmu Membelah Diri",
    "banyak_sks": 2,
    "banyak_jam_matkul": 6,
    "keterangan": ""
}
```

### Mata Kuliah

* **Daftar Mata Kuliah**

  * **Endpoint**: `GET http://localhost:8080/matkul`
  * **Header**:

```
Authorization: Bearer <jwt_token_here>
```

* **Tambah Mata Kuliah**

  * **Endpoint**: `POST http://localhost:8080/matkul`
  * **Body JSON**:

```json
{
    "kode": "IF101",
    "nama": "Pemrograman Web",
    "sks": 3
}
```

### Prodi

* **Daftar Prodi**

  * **Endpoint**: `GET http://localhost:8080/api/prodi`
  * **Header**:

```
Authorization: Bearer <jwt_token_here>
```

* **Tambah Prodi**

  * **Endpoint**: `POST http://localhost:8080/api/prodi`
  * **Body JSON**:

```json
{
    "nama_prodi": "Sastra Mesin"
}
```
