# bioskop
Link Linkedin: https://www.linkedin.com/in/muhammad-wildan-zulfahmi-195b913a5/

========================================================================
✅ 1️⃣ CREATE DATABASE
Query:
create database db_bioskop;

Penjelasan:
Membuat database baru bernama db_bioskop 🗄️✨ (🅳 DDL)
========================================================================

========================================================================
✅ 2️⃣ USE DATABASE
Query:
use db_bioskop;

Penjelasan:
Memilih database db_bioskop agar bisa digunakan 📂✅ (🅳 DDL)
========================================================================

========================================================================
✅ 3️⃣ CREATE TABLE PEMESAN
Query:
create table pemesan(...);

Penjelasan:
Membuat tabel pemesan untuk menyimpan data pelanggan 👤📋 (🅳 DDL)
========================================================================

========================================================================
✅ 4️⃣ CREATE TABLE FILM
Query:
create table film(...);

Penjelasan:
Membuat tabel film untuk menyimpan data film bioskop 🎬📄 (🅳 DDL)
========================================================================

========================================================================
✅ 5️⃣ CREATE TABLE TRANSAKSI
Query:
create table transaksi(...);

Penjelasan:
Membuat tabel transaksi dan menghubungkan dengan tabel lain 🔗💳 (🅳 DDL)
========================================================================

========================================================================
✅ 6️⃣ INSERT DATA FILM
Query:
insert into film (...);

Penjelasan:
Menambahkan data film ke dalam tabel film 🎬➕🔥 (🅼 DML)
========================================================================

========================================================================
✅ 7️⃣ SELECT DATA FILM
Query:
select * from film;

Penjelasan:
Menampilkan semua data film 👀📊 (🅼 DML)
========================================================================

========================================================================
✅ 8️⃣ INSERT DATA PEMESAN
Query:
insert into pemesan (...);

Penjelasan:
Menambahkan data pelanggan ke tabel pemesan 👤➕📱 (🅼 DML)
========================================================================

========================================================================
✅ 9️⃣ INSERT DATA TRANSAKSI (PERTAMA)
Query:
insert into transaksi (...);

Penjelasan:
Menambahkan data transaksi pertama kali 💳🧾 (🅼 DML)
========================================================================

========================================================================
✅ 🔟 ADD COLUMN
Query:
alter table film add column deskripsi text;

Penjelasan:
Menambahkan kolom deskripsi pada tabel film 🆕🛠️ (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣1️⃣ SELECT SETELAH TAMBAH KOLOM
Query:
select * from film;

Penjelasan:
Menampilkan data film setelah kolom baru ditambah 👀📊 (🅼 DML)
========================================================================

========================================================================
✅ 1️⃣2️⃣ MODIFY COLUMN
Query:
alter table film modify column deskripsi varchar(100);

Penjelasan:
Mengubah tipe data kolom deskripsi 🔄📐 (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣3️⃣ DESCRIBE TABLE (PERTAMA)
Query:
describe film;

Penjelasan:
Melihat struktur tabel setelah perubahan 👀🏗️ (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣4️⃣ RENAME COLUMN
Query:
alter table film rename column deskripsi to info;

Penjelasan:
Mengganti nama kolom deskripsi menjadi info ✏️🔁 (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣5️⃣ DESCRIBE TABLE (KEDUA)
Query:
describe film;

Penjelasan:
Mengecek struktur tabel setelah rename kolom 👀🏗️ (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣6️⃣ DROP COLUMN
Query:
alter table film drop column info;

Penjelasan:
Menghapus kolom info dari tabel film ❌📄 (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣7️⃣ DESCRIBE TABLE (KETIGA)
Query:
describe film;

Penjelasan:
Melihat struktur tabel setelah kolom dihapus 👀🏗️ (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣8️⃣ CREATE TABLE TES
Query:
create table table_tes(...);

Penjelasan:
Membuat tabel percobaan untuk percobaan 🧪📋 (🅳 DDL)
========================================================================

========================================================================
✅ 1️⃣9️⃣ DROP TABLE TES
Query:
drop table table_tes;

Penjelasan:
Menghapus tabel percobaan 🗑️❌ (🅳 DDL)
========================================================================

========================================================================
✅ 2️⃣0️⃣ CREATE TABLE TES (ULANG)
Query:
create table table_tes(...);

Penjelasan:
Membuat kembali tabel percobaan 🔁📋 (🅳 DDL)
========================================================================

========================================================================
✅ 2️⃣1️⃣ RENAME TABLE
Query:
rename table table_tes to testing;

Penjelasan:
Mengganti nama tabel menjadi testing ✏️🔁 (🅳 DDL)
========================================================================

========================================================================
✅ 2️⃣2️⃣ DROP TABLE TESTING
Query:
drop table testing;

Penjelasan:
Menghapus tabel testing 🗑️❌ (🅳 DDL)
========================================================================

========================================================================
✅ 2️⃣3️⃣ TRUNCATE TABLE
Query:
truncate table transaksi;

Penjelasan:
Menghapus semua data transaksi tanpa hapus tabel ⚡🗑️ (🅼 DML)
========================================================================

========================================================================
✅ 2️⃣4️⃣ SELECT SETELAH TRUNCATE
Query:
select * from transaksi;

Penjelasan:
Mengecek apakah tabel transaksi kosong 👀📊 (🅼 DML)
========================================================================

========================================================================
✅ 2️⃣5️⃣ INSERT TRANSAKSI (ULANG)
Query:
insert into transaksi(...);

Penjelasan:
Mengisi kembali data transaksi 🔁💳 (🅼 DML)
========================================================================

========================================================================
✅ 2️⃣6️⃣ UPDATE DATA
Query:
update transaksi set id_film=3 where id_transaksi=5;

Penjelasan:
Mengubah data transaksi tertentu ✏️🔄 (🅼 DML)
========================================================================

========================================================================
✅ 2️⃣7️⃣ SELECT TRANSAKSI
Query:
select * from transaksi;

Penjelasan:
Menampilkan data transaksi terbaru 👀📊 (🅼 DML)
========================================================================

========================================================================
✅ 2️⃣8️⃣ INSERT TRANSAKSI TAMBAHAN
Query:
insert into transaksi(...);

Penjelasan:
Menambah satu transaksi baru ➕💳 (🅼 DML)
========================================================================

========================================================================
✅ 2️⃣9️⃣ DELETE TRANSAKSI
Query:
delete from transaksi where id_transaksi=1;

Penjelasan:
Menghapus satu data transaksi 🗑️❌ (🅼 DML)
========================================================================

========================================================================
✅ 3️⃣0️⃣ SELECT TERAKHIR TRANSAKSI
Query:
select * from transaksi;

Penjelasan:
Melihat data transaksi setelah penghapusan 👀📊 (🅼 DML)
========================================================================

========================================================================
✅ 3️⃣1️⃣ JOIN FILM TERLARIS
Query:
select ... join ... count ...

Penjelasan:
Mencari film paling laris berdasarkan transaksi 🏆🎬 (🅹 JOIN + 🅼 DML)
========================================================================

========================================================================
✅ 3️⃣2️⃣ JOIN PELANGGAN TERBANYAK
Query:
select ... join ... count ...

Penjelasan:
Mencari pelanggan yang paling sering memesan 👤⭐ (🅹 JOIN + 🅼 DML)
========================================================================

========================================================================
✅ 3️⃣3️⃣ CREATE VIEW FILM TERLARIS
Query:
create view film_terlaris as ...

Penjelasan:
Membuat view untuk menyimpan query film terlaris 👁️📊 (🆅 VIEW + 🅳 DDL)
========================================================================

========================================================================
✅ 3️⃣4️⃣ SELECT VIEW FILM TERLARIS
Query:
select * from film_terlaris;

Penjelasan:
Menampilkan hasil dari view film terlaris 👀🏆 (🆅 VIEW)
========================================================================

========================================================================
✅ 3️⃣5️⃣ CREATE VIEW PELANGGAN TERBANYAK
Query:
create view pelanggan_terbanyak as ...

Penjelasan:
Membuat view pelanggan terbanyak 👁️⭐ (🆅 VIEW + 🅳 DDL)
========================================================================

========================================================================
✅ 3️⃣6️⃣ SELECT VIEW PELANGGAN TERBANYAK
Query:
select * from pelanggan_terbanyak;

Penjelasan:
Menampilkan hasil view pelanggan terbanyak 👀📊 (🆅 VIEW)
========================================================================
