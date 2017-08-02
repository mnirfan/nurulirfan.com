---
layout: post
title:  "Partisi pada Hard Disk Drive"
date:   2017-08-02 00:18
categories: pengetahuan
permalink: /partisi-hdd
---

# Partisi
Partisi adalah pembagian ruang *Hard Disk Drive* (HDD) secara logis. Pembagian ini bertujuan untuk memudahkan manajemen pemnyimpanan di HDD. Misalnya sebuah HDD dibagi menjadi tiga bagian. Bagian pertama untuk meletakkan sistem operasi, bagian kedua untuk menyimpan proyek dan tugas kuliah, dan bagian ketiga untuk menyimpan foto dan video. Dengan membagi-bagi HDD seperti ini kerusakan *filesystem* juga dapat diminimalisir karena kerusakan ini bersifat lokal dalam sebuah partisi, sehingga apabila sebuah partisi rusak (*corrupt*) maka partisi lainnya tidak terkena dampaknya.

Dalam sistem operasi keluarga microsoft (DOS, Windows) setiap partisi HDD dilambangkan dengan sebuah abjad dan diikuti dengan titik dua. misalkan `C:`, `D:`, `E:`, dan seterusnya. Pada Linux dan sistem Unix-like lain sebuah partisi direpresentasikan dengan sebuah file dalam direktori `/dev/`, misalnya `/dev/sda1`, `/dev/sda2`, dan seterusnya.

![]('http://nurulirfan.com/images/post/fs_mount.png')
*mengaitkan partisi*

## Tabel Partisi
Tabel partisi mendeskripsikan partisi-partisi yang ada dalam sebuah HDD.

Ada dua jenis tabel partisi yang sering digunakan:

1. tabel partisi MBR (Master Boot Record)

    Jenis partisi ini banyak digunakan pada PC generasi lama. HDD yang diatur dengan tipe tabel ini hanya mampu menampung empat partisi primer, namun dapat dibuat lebih banyak partisi lagi dengan menggunakan partisi primer bertipe extended.
