# 📌 MINI PROJECT

# 🎬 Database Sistem Bioskop (MySQL)

---

Nama Kelompok: 10
Anggota Kelompok:

* Inka Dayu Ningtyas
* Muhammad Wildan Zulfahmi
* Talita Azaria

---

## 👤 Identitas

Nama: Muhammad Wildan Zulfahmi
LinkedIn: [https://www.linkedin.com/in/muhammad-wildan-zulfahmi-195b913a5/](https://www.linkedin.com/in/muhammad-wildan-zulfahmi-195b913a5/)

---

## 📖 Deskripsi Project

Mini project ini bertujuan untuk membuat sistem database bioskop menggunakan MySQL yang berisi:

* 🎬 Data film
* 👤 Data pemesan
* 💳 Data transaksi
* 🏆 Laporan film terlaris
* ⭐ Pelanggan terbanyak

Project ini menerapkan konsep:

* 📘 DDL
* 📙 DML
* 🔗 JOIN
* 👁️ VIEW

---
# 🗂️ Struktur Tabel Database `db_bioskop`

Database **db_bioskop** terdiri dari 3 tabel utama, yaitu:

- 📌 `pemesan` (Data Pelanggan)  
- 📌 `film` (Data Film)  
- 📌 `transaksi` (Data Pemesanan)

---

## 📋 Tabel `pemesan`

Digunakan untuk menyimpan data pelanggan bioskop.

| Field        | Type          | Key | Null | Extra           | Keterangan                  |
|--------------|---------------|-----|------|------------------|------------------------------|
| id_pemesan   | INT           | PK  | NO   | AUTO_INCREMENT   | ID pelanggan                 |
| nama         | VARCHAR(100)  | -   | YES  | -                | Nama pelanggan               |
| no_telepon   | VARCHAR(15)   | -   | YES  | -                | Nomor telepon pelanggan      |

---

## 🎬 Tabel `film`

Digunakan untuk menyimpan data film yang tersedia.

| Field    | Type          | Key | Null | Extra           | Keterangan            |
|----------|---------------|-----|------|------------------|------------------------|
| id_film  | INT           | PK  | NO   | AUTO_INCREMENT   | ID film                |
| judul    | VARCHAR(100)  | -   | YES  | -                | Judul film             |
| genre    | VARCHAR(50)   | -   | YES  | -                | Genre film             |
| harga    | INT           | -   | YES  | -                | Harga tiket            |

---

## 💳 Tabel `transaksi`

Digunakan untuk menyimpan data transaksi pemesanan tiket.

| Field         | Type | Key | Null | Extra         | Keterangan                          |
|---------------|------|-----|------|---------------|--------------------------------------|
| id_transaksi  | INT  | PK  | NO   | AUTO_INCREMENT| ID transaksi                         |
| id_pemesan    | INT  | FK  | YES  | -             | Relasi ke pemesan(id_pemesan)        |
| id_film       | INT  | FK  | YES  | -             | Relasi ke film(id_film)              |
| tanggal       | DATE | -   | YES  | -             | Tanggal transaksi                    |

---

## 🔗 Relasi Antar Tabel

Struktur relasi database:

```text
pemesan (1) ────────< transaksi >──────── (1) film
---

# ✅ Daftar Query dan Penjelasan

---

## 1️⃣ 🗄️ CREATE DATABASE (DDL)

```sql
CREATE DATABASE db_bioskop;
```

Penjelasan: Membuat database baru.

---

## 2️⃣ 📂 USE DATABASE (DDL)

```sql
USE db_bioskop;
```

Penjelasan: Mengaktifkan database.

---

## 3️⃣ 👤 CREATE TABLE PEMESAN (DDL)

```sql
CREATE TABLE pemesan(
 id_pemesan INT AUTO_INCREMENT PRIMARY KEY,
 nama VARCHAR(100),
 no_telepon VARCHAR(15)
);
```

Penjelasan: Membuat tabel pelanggan.

---

## 4️⃣ 🎬 CREATE TABLE FILM (DDL)

```sql
CREATE TABLE film(
 id_film INT AUTO_INCREMENT PRIMARY KEY,
 judul VARCHAR(100),
 genre VARCHAR(50),
 harga INT
);
```

Penjelasan: Membuat tabel film.

---

## 5️⃣ 💳 CREATE TABLE TRANSAKSI (DDL)

```sql
CREATE TABLE transaksi(
 id_transaksi INT AUTO_INCREMENT PRIMARY KEY,
 id_pemesan INT,
 id_film INT,
 tanggal DATE,
 FOREIGN KEY(id_pemesan) REFERENCES pemesan(id_pemesan),
 FOREIGN KEY(id_film) REFERENCES film(id_film)
);
```

Penjelasan: Membuat tabel transaksi.

---

## 6️⃣ ➕ INSERT DATA FILM (DML)

```sql
INSERT INTO film (judul,genre,harga) VALUES
('Avengers','Action',50000),
('Frozen','Action',50000),
('Ejen Ali The Movie','Action',50000),
('Spiderman','Action',10000),
('Iron Man','Action',8000);
```

Penjelasan: Menambahkan data film.

---

## 7️⃣ 👀 SELECT DATA FILM (DML)

```sql
SELECT * FROM film;
```

Penjelasan: Menampilkan data film.

---

## 8️⃣ ➕ INSERT DATA PEMESAN (DML)

```sql
INSERT INTO pemesan (nama,no_telepon) VALUES
('Wildan','081223123'),
('Rahma','01293019212'),
('Jaya','082322312'),
('Nabil','081231239'),
('Rizki','08219391');
```

Penjelasan: Menambahkan data pemesan.

---

## 9️⃣ 💳 INSERT DATA TRANSAKSI (DML)

```sql
INSERT INTO transaksi(id_pemesan,id_film,tanggal) VALUES
(1,2,'2026-02-25'),
(1,1,'2026-02-28'),
(3,1,'2026-02-20'),
(2,5,'2026-02-20'),
(4,4,'2026-02-20');
```

Penjelasan: Menambahkan transaksi.

---

## 🔟 🆕 ADD COLUMN (DDL)

```sql
ALTER TABLE film ADD COLUMN deskripsi TEXT;
```

Penjelasan: Menambah kolom.

---

## 1️⃣1️⃣ 👀 SELECT SETELAH ALTER

```sql
SELECT * FROM film;
```

Penjelasan: Cek perubahan.

---

## 1️⃣2️⃣ 🔄 MODIFY COLUMN

```sql
ALTER TABLE film MODIFY COLUMN deskripsi VARCHAR(100);
```

Penjelasan: Ubah tipe data.

---

## 1️⃣3️⃣ 📋 DESCRIBE TABLE

```sql
DESCRIBE film;
```

Penjelasan: Lihat struktur.

---

## 1️⃣4️⃣ ✏️ RENAME COLUMN

```sql
ALTER TABLE film RENAME COLUMN deskripsi TO info;
```

Penjelasan: Ganti nama kolom.

---

## 1️⃣5️⃣ 📋 DESCRIBE SETELAH RENAME

```sql
DESCRIBE film;
```

Penjelasan: Cek struktur.

---

## 1️⃣6️⃣ ❌ DROP COLUMN

```sql
ALTER TABLE film DROP COLUMN info;
```

Penjelasan: Hapus kolom.

---

## 1️⃣7️⃣ 📋 DESCRIBE AKHIR

```sql
DESCRIBE film;
```

Penjelasan: Struktur akhir.

---

## 1️⃣8️⃣ 🧪 CREATE TABLE TES

```sql
CREATE TABLE table_tes(
 id_pemesan INT AUTO_INCREMENT PRIMARY KEY,
 nama VARCHAR(100),
 no_telepon VARCHAR(15)
);
```

Penjelasan: Tabel percobaan.

---

## 1️⃣9️⃣ 🗑️ DROP TABLE TES

```sql
DROP TABLE table_tes;
```

Penjelasan: Hapus tabel.

---

## 2️⃣0️⃣ 🔁 CREATE TABLE TES ULANG

```sql
CREATE TABLE table_tes(
 id_pemesan INT AUTO_INCREMENT PRIMARY KEY,
 nama VARCHAR(100),
 no_telepon VARCHAR(15)
);
```

Penjelasan: Buat ulang.

---

## 2️⃣1️⃣ ✏️ RENAME TABLE

```sql
RENAME TABLE table_tes TO testing;
```

Penjelasan: Ganti nama.

---

## 2️⃣2️⃣ 🗑️ DROP TABLE TESTING

```sql
DROP TABLE testing;
```

Penjelasan: Hapus tabel.

---

## 2️⃣3️⃣ ⚡ TRUNCATE TABLE

```sql
TRUNCATE TABLE transaksi;
```

Penjelasan: Kosongkan data.

---

## 2️⃣4️⃣ 👀 SELECT SETELAH TRUNCATE

```sql
SELECT * FROM transaksi;
```

Penjelasan: Cek kosong.

---

## 2️⃣5️⃣ 🔁 INSERT TRANSAKSI ULANG

```sql
INSERT INTO transaksi(id_pemesan,id_film,tanggal) VALUES
(1,2,'2026-02-25'),
(1,1,'2026-02-28'),
(3,1,'2026-02-20'),
(2,5,'2026-02-20'),
(4,4,'2026-02-20');
```

Penjelasan: Isi ulang data.

---

## 2️⃣6️⃣ ✏️ UPDATE DATA

```sql
UPDATE transaksi SET id_film=3 WHERE id_transaksi=5;
```

Penjelasan: Update data.

---

## 2️⃣7️⃣ 👀 SELECT TRANSAKSI

```sql
SELECT * FROM transaksi;
```

Penjelasan: Lihat transaksi.

---

## 2️⃣8️⃣ ➕ INSERT TAMBAHAN

```sql
INSERT INTO transaksi(id_pemesan,id_film,tanggal)
VALUES(1,1,'2026-06-25');
```

Penjelasan: Tambah data.

---

## 2️⃣9️⃣ 🗑️ DELETE DATA

```sql
DELETE FROM transaksi WHERE id_transaksi=1;
```

Penjelasan: Hapus data.

---

## 3️⃣0️⃣ 👀 SELECT TERAKHIR

```sql
SELECT * FROM transaksi;
```

Penjelasan: Cek akhir.

---

## 3️⃣1️⃣ 🏆 JOIN FILM TERLARIS

```sql
SELECT f.id_film,f.judul,COUNT(t.id_film) AS total_pemesanan
FROM transaksi t
JOIN film f ON f.id_film=t.id_film
GROUP BY f.id_film,f.judul
ORDER BY total_pemesanan DESC
LIMIT 1;
```

Penjelasan: Cari film terlaris.

---

## 3️⃣2️⃣ ⭐ JOIN PELANGGAN TERBANYAK

```sql
SELECT p.id_pemesan,p.nama,COUNT(t.id_pemesan) AS banyak_memesan
FROM transaksi t
JOIN pemesan p ON p.id_pemesan=t.id_pemesan
GROUP BY p.id_pemesan,p.nama
ORDER BY banyak_memesan DESC
LIMIT 1;
```

Penjelasan: Cari pelanggan terbaik.

---

## 3️⃣3️⃣ 👁️ CREATE VIEW FILM TERLARIS

```sql
CREATE VIEW film_terlaris AS
SELECT f.id_film,f.judul,COUNT(t.id_film) AS total_pemesanan
FROM transaksi t
JOIN film f ON f.id_film=t.id_film
GROUP BY f.id_film,f.judul
ORDER BY total_pemesanan DESC
LIMIT 1;
```

Penjelasan: Buat view.

---

## 3️⃣4️⃣ 👀 SELECT VIEW FILM TERLARIS

```sql
SELECT * FROM film_terlaris;
```

Penjelasan: Tampilkan view.

---

## 3️⃣5️⃣ 👁️ CREATE VIEW PELANGGAN TERBANYAK

```sql
CREATE VIEW pelanggan_terbanyak AS
SELECT p.id_pemesan,p.nama,COUNT(t.id_pemesan) AS banyak_memesan
FROM transaksi t
JOIN pemesan p ON p.id_pemesan=t.id_pemesan
GROUP BY p.id_pemesan,p.nama
ORDER BY banyak_memesan DESC
LIMIT 1;
```

Penjelasan: Buat view pelanggan.

---

## 3️⃣6️⃣ 👀 SELECT VIEW PELANGGAN TERBANYAK

```sql
SELECT * FROM pelanggan_terbanyak;
```

Penjelasan: Tampilkan view.

---

# 📌 Kesimpulan

Project ini telah menerapkan:

* CRUD
* Relasi tabel
* Join
* View
* Aggregate Function

Database ini cocok untuk sistem bioskop sederhana.
