### PhpMyAdmin dan Mengelola Database
**PhpMyAdmin** adalah perangkat lunak bebas yang ditulis dalam bahasa pemrograman PHP yang digunakan untuk menangani administrasi MySQL melalui. Dengan kata lain PhpMyAdmin merupakan antarmuka yang mempermudah kita dalam melakukan mengelola MySQL dan MariaDB.

PhpMyAdmin dapat diakses melalui tautan [http://localhost/phpmyadmin](http://localhost/phpmyadmin) dengan terlebih dahulu menjalankan service Apache dan MySQL pada control panel XAMPP.

![Antarmuka PhpMyAdmin](figures/3_1.png)
*Antarmuka PhpMyadmin*

#### Mengelola Database
##### Membuat Database dan Tabel
Pada tab menu phpmyadmin pilih **Databases**, masukan nama database yang akan dibuat lalu klik **Create** ![Membuat Database](figures/3_2.png)

Selanjutnya kita diarahkan kehalaman pembuatan tabel. Disini saya membuat table `pengguna` yang di dalamnya terdapat 4 kolom.
![Membuat Tabel](figures/3_3.png)

Selanjutnya definisikan kolom yang akan dibuat pada tabel `pengguna`, struktur tabel yang saya buat adalah:
|Kolom|Tipe Data|Panjang|Keterangan|
|-----|---------|:-------:|----------|
|id|Integer|11|Primary Key, Auto Increments|
|username|Varchar|50||
|password|Varchar|255||
|email|Varchar|50||
![Membuat Kolom](figures/3_4.png)

##### Memanipulasi Data
1. Menambah Data (Insert)
Untuk memasukan data baru, pilih melalui menu ***Insert*** lalu isikan borang yang tersedia dan klik **Go** ![Menambah Data](figures/3_5.png)
> Cobalah untuk masukan beberapa tambahan data

2. Melihat Data (Select)
Untuk melihat daftar record yang sudah dimasukan sebelumnya, dengan memilih menu **Browse** ![Melihat Data](figures/3_6.png)

3. Mengubah Data (Update)
Untuk mengubah data yang telah dimasukan sebelumnya, dengan mengklik tombol edit. ![Mengubah Data](figures/3_7.png) 
Kemudian ubah data yang diinginkan lalu klik Go ![Mengubah Data](figures/3_8.png)

4. Menghapus Data (Delete)
Untuk menghapus data yang telah dimasukan sebelumnya, dengan mengklik tombol delete. ![Menghapus Data](figures/3_9.png)
