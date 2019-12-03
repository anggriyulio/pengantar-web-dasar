### Where Clause
|Operator|Deskripsi|Contoh|Hasil|
|:---:|---|---|---|
|=|Cek apakah kedua nilai adalah sama, jika ya akan mengembalikan nilai `TRUE` sebaliknya `FALSE`| (1=2) |FALSE|
|!=|Cek apakah kedua nilai tidak sama, jika kedua nilai berbeda maka akan mengembalikan nilai `TRUE` sebaliknya `FALSE`| (1!=2) |TRUE
|>|Cek apakah nilai pertama besar dari nilai kedua|5>2|TRUE|
|<|Cek apakah nilai pertama kecil dari nilai kedua|5>2|FALSE|
|>=|Cek apakah nilai pertama besar atau sama dari nilai kedua|5>=5|TRUE|
|<=|Cek apakah nilai pertama kecil atau sama dari nilai kedua|5<=5|TRUE|

Contoh:
```
SELECT*FROM pengguna where umur = 20;
SELECT*FROM pengguna where umur > 20;
SELECT*FROM pengguna where umur < 20;
SELECT*FROM pengguna where umur >= 20;
SELECT*FROM pengguna where umur <= 20;
```