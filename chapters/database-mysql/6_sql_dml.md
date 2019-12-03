
## Data Manipulation Language (DML)
### INSERT INTO (Memasukan Data)
Untuk memasukan record ke dalam sebuah tabel menggunakan perintah `INSERT INTO`. Terdapat dua cara dalam memasukan data, yaitu dengan mendefinisikan nama kolom terlebih dahulu dan tanpa mendefinisikan nama kolom:
- Dengan mendefinisikan nama kolom
  ```
    INSERT INTO table_name (kolom1, kolom2, kolom3, ...)
    VALUES (value1, value2, value3, ...);
    ```
    Contoh:
    ```
    INSERT INTO pengguna (username, password, email)
    VALUES ('anggri', '12346, 'anggriyulio@gmail.com');
    ```
- Tanpa mendefinisikan nama kolom
    ```
     INSERT INTO table_name (value1, value2, value3, ...);
    ```
    Contoh: 
    ```
     INSERT INTO pengguna (5, 'anggri', '123456', 'anggriyulio@gmail.com');
    ```
    > Cara ini mengharuskan kita mengisi nilai `VALUES` sesuai dengan urutan dan jumlah kolom yang ada pada tabel.

### UPDATE (Mengubah Record)
Mengubah record pada sebuah tabel menggunakan perintah `UPDATE` dengan struktur perintah:
```
UPDATE nama_tabel SET nama_kolom=value1, nama_kolom2=value2 [WHERE kondisi];
```
Jika melakukan perubahan pada suatu record maka tambahkan perintah `WHERE`, jika tidak maka seluruh record yang ada di dalam tabel tersebut akan ikut berubah.
Contoh:
```
UPDATE pengguna SET password='password baru';
```
Perintah di atas akan merubah seluruh password tabel pengguna menjadi `'password baru'`. Untuk melakukan perubahan pada record tertentu saja tambahkan perintah `WHERE`.
Contoh:
```
UPDATE pengguna SET password='password baru' WHERE username='budi';
```
Perintah di atas akan mengubah password hanya untuk record dengan username `budi`

### DELETE (Menghapus Record)
Menghapus record menggunakan perintah `DELETE` dengan struktur perintah:
```
DELETE FROM nama_tabel [WHERE];
```
Contoh:
```
DELETE FROM pengguna;
```
Jika ingin menghapus beberapa atau satu record saja maka tambahkan perintah `WHERE`, jika tidak maka seluruh record yang ada di dalam tabel tersebut akan terhapus.
Contoh:
```
DELETE FROM pengguna where id=1;
```
Perintah di atas akan menghapus record yang mempunyai nilai `id` adalah `1`.

### SELECT (Menampilkan Record)

Menampilkan record menggunakan perintah `SELECT` dengan struktur:
```
SELECT [namakolom] FROM namatabel;
```

Untuk ingin menampilkan seluruh kolom, maka gunakan tanda `* (baca: all)`  seperti:
```
SELECT * FROM namatabel;
```

Untuk menampilkan data dengan kondisi tertentu, maka gunakan perintah `WHERE`.

> Untuk melihat daftar operator yang bisa digunakan dalam struktur `WHERE` silahkan merujuk ke halaman [WHERE CLAUSE](7_sql_where.md)