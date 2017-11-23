---
layout: post
title:  "Partisi pada Hard Disk Drive"
date:   2017-08-02 00:18
categories: pengetahuan
permalink: /partisi-hdd
---

# Partisi
Partisi adalah pembagian ruang *Hard Disk Drive* (HDD) secara logis. Pembagian ini bertujuan untuk memudahkan manajemen pemnyimpanan di HDD. Misalnya sebuah HDD dibagi menjadi tiga bagian. Bagian pertama untuk meletakkan sistem operasi, bagian kedua untuk menyimpan proyek dan tugas kuliah, dan bagian ketiga untuk menyimpan foto dan video. Dengan membagi-bagi HDD seperti ini kerusakan *filesystem* juga dapat diminimalisir karena kerusakan ini bersifat lokal dalam sebuah partisi, sehingga apabila sebuah partisi rusak (*corrupt*) maka partisi lainnya tidak terkena dampaknya.

Dalam sistem operasi keluarga microsoft (DOS, Windows) setiap partisi HDD dilambangkan dengan sebuah abjad dan diikuti dengan titik dua. misalkan `C:`, `D:`, `E:`, dan seterusnya. Pada Linux dan sistem Unix-like lain sebuah partisi direpresentasikan dengan sebuah file dalam direktori `/dev/`, misalnya `/dev/sda1`, `/dev/sda2`, dan seterusnya. Untuk dapat mengakses partisi-partisi yang ada maka perlu dikaitkan ke sistem operasi terlebih dahulu. misalkan `sda2` dikaitkan kedalam direktori `/mnt/videos` maka seluruh berkas yang ada di `sda2` akan muncul dan dapat diakses di `/mnt/videos`. lihat ilustrasi berikut.

![mount]({{site.url}}/images/post/fs_mount.png)
*mengaitkan partisi*



## Tabel Partisi
Tabel partisi mendeskripsikan partisi-partisi yang ada dalam sebuah HDD. Tipe tabel partisi dapat diubah sesuai keinginan namun **berakibat pada hilangnya seluruh data dalam HDD dan seluruh susunan partisinya**. Jika ingin melakukan pengubahan tipe tabel sebaiknya backup data-data yang penting ke penyimpanan lain.

Ada dua jenis tabel partisi yang sering digunakan:

### 1. Master Boot Record (MBR)

Tabel partisi MBR memiliki [boot sector](https://en.wikipedia.org/wiki/Master_boot_record) yang terletak di bagian paling awal dari sebuah HDD, yang disebut sebagai MBR. MBR ini menampung informasi tentang bagaimana partisi-partisi yang ada diorganisir. Selain itu MBR juga berisi tentang dimana lokasi sistem operasi yang harus di-boot. Jenis tabel partisi ini banyak digunakan pada PC generasi lama. HDD yang diatur dengan tipe tabel ini hanya mampu menampung empat partisi primer, namun dapat dibuat lebih banyak partisi lagi dengan menggunakan partisi primer bertipe extended. Karena merupakan generasi lama, MBR hanya dapat diterapkan pada HDD dengan kapasitas maksimal 2[TiB](https://en.wikipedia.org/wiki/Tebibyte).

![]({{site.url}}/images/post/pembagian_partisi_mbr.png)
*ilustrasi pengalokasian HDD dengan tabel MBR*

Ketika bootloader sebuah sistem operasi dipasang maka akan secara otomatis mengubah informasi lokasi dimana bootloader tersebut dipasang. Misalkan sebuah PC dipasang sistem operasi linux di `sda1`, maka MBR akan berisi informasi bahwa bootloader berada di `sda1`. Ketika dipasang lagi sistem operasi windows di `sda2` maka MBR juga akan berubah untuk menunjukkan lokasi bootloader berada di `sda2`. Itulah mengapa sebaiknya untuk dual boot sistem operasi windows dengan Linux sangat disarankan untuk mengakhirkan Linux karena bootloader Linux mau mendeteksi bootloader windows, namun tidak sebaliknya.

### 2. GUID Partition Table (GPT)

GUID Partition Table atau GPT adalah tipe tabel partisi yang lebih modern dari MBR. GPT ini sering digunakan di PC generasi sekitar kemunculan windows 8 hingga sekarang. Berbeda dengan MBR, GPT mendukung HDD dengan kapasitas 8[ZiB](https://en.wikipedia.org/wiki/Zebibyte). Selain itu GPT juga
