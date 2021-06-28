# Praktikum 11 - Pemrograman Web (PHP Framework)

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

-Maka akan tampil seperti ini

![Screenshot_214](https://user-images.githubusercontent.com/81457697/121993470-babefa80-cdcd-11eb-8c98-56a1762e9691.png)

#Langkah 4 - Membuat Layout Web dengan CSS
-Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout).

![Screenshot_232](https://user-images.githubusercontent.com/81457697/121993581-ec37c600-cdcd-11eb-95a9-c06cdf0e0df3.png)

#Kemudian buat folder template pada direktori view, lalu buat file header.php dan footer.php.

![Screenshot_233](https://user-images.githubusercontent.com/81457697/121993705-2b661700-cdce-11eb-83ac-07e61c9dda65.png)
![Screenshot_234](https://user-images.githubusercontent.com/81457697/121993714-2e610780-cdce-11eb-91ac-141bc00e2aba.png)

#Kemudian ubah file about.php (/app/view/about.php) seperti berikut.
<?= $this->include('template/header'); ?>
<h1><?= $title; ?></h1>
<hr>
<p><?= $content; ?></p>
<?= $this->include('template/footer'); ?>

Kemudian refresh browser atau akses alamat http://localhost:8080/about

![Screenshot_217](https://user-images.githubusercontent.com/81457697/121993849-69633b00-cdce-11eb-9ea7-8f87c5bbf163.png)

Pertanyaan dan Tugas
Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.

#Tampilan page about

![Screenshot_218](https://user-images.githubusercontent.com/81457697/121993942-90217180-cdce-11eb-8516-06d83e344509.png)

#tampilan page artikel

![Screenshot_220](https://user-images.githubusercontent.com/81457697/121993973-9e6f8d80-cdce-11eb-9217-22a5baa6e9d8.png)

#tampilan page kontak

![Screenshot_221](https://user-images.githubusercontent.com/81457697/121994017-afb89a00-cdce-11eb-8eed-7b05c668ca4c.png)

# Praktikum 12 Code Igniter Lanjutan Tugas
Nama:Axel Danovan Susanto
Nim:311910405
Kelas:TI.19.A.2

Langkah 1
#Membuat Tabel Database

![Screenshot_250](https://user-images.githubusercontent.com/81457697/122878424-f4f64200-d361-11eb-8944-f6a7fc45f6ce.png)

Langkah 2 
#Konfigurasi koneksi database

![Screenshot_251](https://user-images.githubusercontent.com/81457697/122878796-574f4280-d362-11eb-9da9-c10d2c6df2cc.png)

Langkah 3
#Membuat Model

![Screenshot_252](https://user-images.githubusercontent.com/81457697/122879040-a1d0bf00-d362-11eb-9e39-f3e8fd81e3c8.png)

Langkah 4
#Membuat Controller

![Screenshot_253](https://user-images.githubusercontent.com/81457697/122879142-c5940500-d362-11eb-8881-e692909f0d5a.png)

Langkah 5
#Membuat View

![Screenshot_254](https://user-images.githubusercontent.com/81457697/122879377-0724b000-d363-11eb-9ef8-9743f6800cb4.png)
Kemudian membuka browser kembali, dan akses url : http://localhost:8080/artikel

![2131313211123](https://user-images.githubusercontent.com/81457697/122879830-8914d900-d363-11eb-921f-8120bf9d3368.png)
Belum ada data yang diampilkan. Kemudian coba tambahkan beberapa data pada database agar dapat ditampilkan datanya.

![Screenshot_255](https://user-images.githubusercontent.com/81457697/122880461-38ea4680-d364-11eb-9473-00feb2dd278d.png)
Refresh kembali browser, sehingga akan ditampilkan hasilnya.

![32113232132131132](https://user-images.githubusercontent.com/81457697/122885938-b8c6df80-d369-11eb-97b2-7a4c8117ca3a.png)

Langkah 6
#Membuat Tampilan Detail Artikel

![Screenshot_257](https://user-images.githubusercontent.com/81457697/122881362-494ef100-d365-11eb-9f03-0dfe32f1ead8.png)

Langkah 7 
#Membuat View Detail

![Screenshot_258](https://user-images.githubusercontent.com/81457697/122881560-7dc2ad00-d365-11eb-8f5e-46e743ba0c31.png)

Langkah 8 
#Membuat Routing untuk artikel detail

![Screenshot_259](https://user-images.githubusercontent.com/81457697/122881822-c5493900-d365-11eb-8705-bfeabddb1d1d.png)
Buka Kembali file app/config/Routes.php, kemudian tambahkan routing untuk artikel detail.

![23121213123123213](https://user-images.githubusercontent.com/81457697/122882481-7059f280-d366-11eb-89bb-0f82412274a3.png)

Langkah 9 
#Membuat Menu Admin

![Screenshot_260](https://user-images.githubusercontent.com/81457697/122882989-ee1dfe00-d366-11eb-8f7f-f904a79d1293.png)
Selanjutnya buat view untuk tampilan admin dengan nama admin_index.php

![Screenshot_262](https://user-images.githubusercontent.com/81457697/122883489-743a4480-d367-11eb-9737-fc02ed9869e0.png)
![Screenshot_263](https://user-images.githubusercontent.com/81457697/122883516-7bf9e900-d367-11eb-9461-93050c1d4604.png)

Tambahkan routing untuk menu admin seperti berikut:

![Screenshot_264](https://user-images.githubusercontent.com/81457697/122883801-bbc0d080-d367-11eb-89b4-99bf8e2665cb.png)

Kemudian Akses menu admin dengan url http://localhost:8080/admin/artikel

![321321213312321123](https://user-images.githubusercontent.com/81457697/122884058-f3c81380-d367-11eb-8197-4a9ebb6a6064.png)

Langkah 10
#Menambah Data Artikel

![Screenshot_265](https://user-images.githubusercontent.com/81457697/122884396-4dc8d900-d368-11eb-8e8a-cdaa7dbf8a04.png)

Kemudian buat view untuk form tambah dengan nama form_add.php

![Screenshot_266](https://user-images.githubusercontent.com/81457697/122884629-8bc5fd00-d368-11eb-9966-2af5ef8b198d.png)

Berikut tampilan form untuk menambah data artikel :

![123321312112132223](https://user-images.githubusercontent.com/81457697/122884817-b617ba80-d368-11eb-86a7-09790baf4cb4.png)

Langkah 11
#Mengubah Data

![Screenshot_267](https://user-images.githubusercontent.com/81457697/122885077-efe8c100-d368-11eb-9f1f-704c3396eb83.png)

Kemudian buat view untuk form tambah dengan nama form_edit.php

![Screenshot_268](https://user-images.githubusercontent.com/81457697/122885282-245c7d00-d369-11eb-9c0b-1b4aa2595d69.png)

Berikut tampilan form untuk mengubah data artikel :

![12313221313231123213](https://user-images.githubusercontent.com/81457697/122885443-49e98680-d369-11eb-9515-034c62787fda.png)

Langkah 12 
#Menghapus Data

![Screenshot_269](https://user-images.githubusercontent.com/81457697/122885684-80270600-d369-11eb-943d-076f06495e9a.pn
 
 
 # Praktikum 13 Framework Codeigniter: Lanjutan tugas

#Membuat Tabel Pada Mysql

![Screenshot_279](https://user-images.githubusercontent.com/81457697/123712607-e09fd100-d89c-11eb-9818-795a377670bc.png)

Langkah 1
#Membuat User Model

![Screenshot_280](https://user-images.githubusercontent.com/81457697/123712770-31afc500-d89d-11eb-9f0a-bc6b6ba7e87e.png)

Langkah 2
#Membuat Controller User

![Screenshot_281](https://user-images.githubusercontent.com/81457697/123712824-4ee49380-d89d-11eb-8164-ec4f0b3bc6d9.png)


Langkah 3
#Membuat View Login

![Screenshot_282](https://user-images.githubusercontent.com/81457697/123712940-8a7f5d80-d89d-11eb-9268-75d3fd332fbc.png)

Uji Coba Login
Selanjutnya buka url http://localhost:8080/user/login seperti berikut:

![123633612-9d654400-d843-11eb-924f-4579451ad058](https://user-images.githubusercontent.com/81457697/123713422-93bcfa00-d89e-11eb-9da0-13ff818d7786.png)

Langkah 4
#Menambahkan Auth Filter

![Screenshot_283](https://user-images.githubusercontent.com/81457697/123713560-e3032a80-d89e-11eb-9daf-8e895589a47f.png)

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:

![Screenshot_284](https://user-images.githubusercontent.com/81457697/123713662-15ad2300-d89f-11eb-83f2-565ba37c90de.png)

Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.

![Screenshot_285](https://user-images.githubusercontent.com/81457697/123713813-6b81cb00-d89f-11eb-8c29-9e0ad68a4777.png)
 
 Percobaan Akses Menu Admin
 Buka url dengan alamat http://localhost:8080/admin/artikel 
 
 ![31213313122133](https://user-images.githubusercontent.com/81457697/123713885-910ed480-d89f-11eb-8b62-28f48ff5a05b.png)
 
 Langkah 5
#Membuat Fungsi Logout

![123123213213321231213 ](https://user-images.githubusercontent.com/81457697/123714490-9c163480-d8a0-11eb-86d1-7a6f1c5d9f08.jpg)

 































