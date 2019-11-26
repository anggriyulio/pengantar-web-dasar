## Data Definition Language (DDL)
### Membuat Database
Untuk membuat database menggunakan perintah:
```
CREATE DATABASE [IF NOT EXISTS] belajar;
```
Perintah diatas akan membuat sebuah database dengan nama **belajar**. Jika database sudah ada sebelumnya maka perintah diatas akan menampilkan error `#1007 - Can't create database 'belajar'; database exists`.

Untuk untuk memeriksa terlebih dahulu apakah database `belajar` belum ada gunakan perintah `IF NOT EXIST`
```
CREATE DATABASE IF NOT EXISTS belajar;
```
Artinya jika ternyata database sudah ada sebelumnya maka database tidak akan dibuat lagi.

### Menghapus Database
Untuk menghapus database gunakan perintah:
```
DROP DATABASE belajar
```
Perintah diatas akan menghapus database yang bernama **belajar**. Jika database tidak ada maka perintah tersebut akan menampilkan pesan error `#1008 - Can't drop database 'belajar'; database doesn't exist`.
Untuk untuk memeriksa terlebih dahulu apakah database belajar sudah ada gunakan perintah `IF EXIST`
```
DROP DATABASE IF EXISTS belajar
```

### Menggunakan / Membuka Database
Untuk menggunakan database gunakan perintah:
```
USE DATABASE belajar
```

### Membuat Table
Membuat tabel menggunakan perintah `CREATE TABLE` dengan struktur:
```
CREATE TABLE nama_tabel (
    column1 tipedata [OPTIONS],
    column2 tipedata [OPTIONS],
    column3 tipedata [OPTIONS],
   ....
);
```
Contoh : 
```
CREATE TABLE pengguna(
    id int AUTO_INCREMENT,
    username varchar(20) NOT NULL,
    password varchar(20) NOT NULL,
    email varchar(20) NOT NULL,
    PRIMARY KEY (id)
);
```

- Jenis tipe data yang didukung dapat dilihat di[https://www.w3schools.com/sql/sql_datatypes.asp](https://www.w3schools.com/sql/sql_datatypes.asp). 
- `AUTO_INCREMENT` memungkinkan nilai dari kolom yang berjenis numerik dibuat secara otomatis dan terurut. 
- Parameter `NOT NULL` adalah menandakan bahwa nilai dari kolom tersebut harus diisi (tidak boleh kosong).
- `PRIMARY KEY` untuk menentukan kunci utama dari tabel yang dibuat.

### Menghapus Tabel
Untuk menghapus tabel beserta seluruh record didalamnya gunakan perintah:
```
DROP TABLE nama_tabel;
```
Contoh:
```
DROP TABLE pengguna;
```

### Menghapus Record di dalam suatu tabel
Untuk menghapus seluruh record dalam sebuah tabel menggunakan perintah `TRUNCATE`. Perintah ini juga akan membuat nilai  `AUTO INCREMENT` pada sebuah kolom kembali ke 1.
```
TRUNCATE TABLE nama_tabel;
```
Contoh:
```
TRUNCATE TABLE pengguna;
```

### Mengubah Struktur Tabel
Untuk mengubah struktur tabel menggunakan perintah `ALTER`, mengubah struktur tabel dapat diartikan sebagai operasi untuk menghapus kolom, menambah kolom atau mengubah struktur kolom.
1. Menambah Kolom
   ```
    ALTER TABLE pengguna
    ADD tempatlahir varchar(50);
   ```
   Perintah di atas akan menambah sebuah kolom `tempatlahir` pada akhir tabel `pengguna`.
2. Menghapus Kolom
   ```
    ALTER TABLE pengguna
    DROP COLUMN email;
   ```
   Perintah di atas akan menghapus kolom email pada tabel `pengguna`.
3. Mengubah Struktur Kolom
   ```
    ALTER TABLE pengguna
    MODIFY COLUMN email varchar(100);
   ```
   Perintah diatas akan mengubah tipe data kolom email menjadi varchar dengan panjang 100.

