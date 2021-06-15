# Lab11web
Praktikum 11 - Pemrograman Web (PHP Framework

Laporan Praktikum
Persiapan
Persiapan
Mengaktifkan beberapa ekstensi php, diantaranya:

-php-json ekstension untuk bekerja dengan JSON;
-php-mysqlnd native driver untuk MySQL;
-php-xml ekstension untuk bekerja dengan XML;
-php-intl ekstensi untuk membuat aplikasi multibahasa;
libcurl (opsional), jika ingin pakai Curl

![121922151-e2797880-cd63-11eb-89dc-766aa9fcfd33](https://user-images.githubusercontent.com/81457697/121989819-f4d8ce00-cdc6-11eb-915f-e099c189f427.jpg)

Hapus tanda ; (titik koma) pada bagian extension yang akan diaktifkan.

![Screenshot_222](https://user-images.githubusercontent.com/81457697/121989952-2baee400-cdc7-11eb-9d5e-a9db34da2440.png)

#Instalasi CodeIgniter 4
-Codeigniter dapat didownload dari website https://codeigniter.com/download
-Extrak file zip Codeigniter ke direktori htdocs/lab11_php_ci.
-Ubah nama direktory framework-4.x.xx menjadi ci4.
-Buka browser dengan alamat http://localhost/lab11_php_ci/ci4/public/

![unknown](https://user-images.githubusercontent.com/81457697/121990076-63b62700-cdc7-11eb-9fb7-32d39c92b421.png)

#Codeigniter menyediakan CLI, untuk mengaksesnya buka terminal lalu arahkan ke direktori project yang akan dibuat. Kemudian jalankan perintah php spark untuk memanggil CLI codeigniter.

![Screenshot_223](https://user-images.githubusercontent.com/81457697/121990177-8a745d80-cdc7-11eb-8dca-1fb6e14b9ca5.png)

#Codeigniter juga menyediakan mode debugging/development yang dapat menampilkan error/kesalahan dalam kode program. Cara mengaktifkannya dengan mengubah nama file env menjadi .env kemudian buka filenya dan ubah nilai CI_ENVIRONMENT menjadi development.

![121922168-e7d6c300-cd63-11eb-8b2b-bc6027b9f95f](https://user-images.githubusercontent.com/81457697/121990278-b099fd80-cdc7-11eb-9e72-83b904e27e6c.jpg)

#Maka pesan kesalahan akan ditampilkan.

![Screenshot_212](https://user-images.githubusercontent.com/81457697/121990361-d9ba8e00-cdc7-11eb-9269-47b3592ddd3d.png)

#Langkah 1 - Membuat Route
Router terletak pada file app/config/Routes.php

#Untuk mengetahui route yg ada atau telah berjalan dapat menggunakan perintah php spark routes

![Screenshot_224](https://user-images.githubusercontent.com/81457697/121990409-f5259900-cdc7-11eb-8437-fb3ff842aa00.png)

Selanjutnya mencoba akses route yang telah dibuat dengan mengakses http://localhost:8080/about
#Terjadi error file not found dikarenakan tidak ada file/page untuk halaman about.

![Screenshot_215](https://user-images.githubusercontent.com/81457697/121990689-5fd6d480-cdc8-11eb-96ae-140370b95426.png)

#Langkah 2 - Membuat Controller
-Membuat file page.php di dalam direktori Controller (/app/Controllers)

![Screenshot_231](https://user-images.githubusercontent.com/81457697/121993222-46845700-cdcd-11eb-8aa5-202de20c971d.png)

-Kemudian refresh browser maka halaman sudah dapat diakses dan menampilkan hasilnya.

![Screenshot_216](https://user-images.githubusercontent.com/81457697/121990841-ad534180-cdc8-11eb-83ff-2bb7121d2c46.png)

#Menambahkan method baru pada controller page.
-Method ini dapat diakses dengan menggunakan alamat: http://localhost:8080/page/tos

![Screenshot_230](https://user-images.githubusercontent.com/81457697/121993081-0de47d80-cdcd-11eb-9cc3-380370b056d7.png)

#Langkah 3
-Membuat file about.php di dalam direktori View (/app/view/about.php)

![Screenshot_227](https://user-images.githubusercontent.com/81457697/121991305-9a8d3c80-cdc9-11eb-8380-6294beba5c1b.png)


Mengubah method about dalam controller page.
![Screenshot_225](https://user-images.githubusercontent.com/81457697/121992742-6b2bff00-cdcc-11eb-8ead-2579802f7c94.png)











