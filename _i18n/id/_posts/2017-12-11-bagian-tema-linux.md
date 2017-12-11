---
layout: post
title:  "3 Bagian Tema Di Linux Yang Perlu Diketahui"
date:   2016-03-03 11:22
categories: Linux, Theme, Icon
permalink: /tiga-bagian-tema-di-linux
---

Tema atau Theme, kata ini sudah tak asing tentunya di telinga kita. Sudah banyak sekali di internet yang menyediakan tema untuk Linux, misalnya [GNOME-look](http://gnome-look.org/), [KDE-look](http://kde-look.org/), [Noobslab](http://noobslab.com/) dan [Webupd8](http://webupd8.org/). Disana ada banyak sekali tema-tema yang tersedia.

![mount]({{site.url}}/images/post/tiga-bagian-tema/gnome-look.png)
*Tampilan gnome-look.org*

Mengapa KDE dan GNOME memiliki tema yang berbeda? apa yang membedakan keduanya? Sebelumnya mari kita lihat sekilas gambar berikut

![]({{site.url}}/images/post/tiga-bagian-tema/pembagian-tema.png)

Pada dasarnya tema di Linux dibagi menjadi 3 bagian:

# Window Manager
Window Manager atau biasa disingkat WM adalah komponen yang bertugas mengatur tata letak suatu window, misalnya koordinat di layar, urutan tumpukan window ketika terbuka lebih dari satu, resize ukuran window, dan drag posisi window. Yang termasuk dalam WM pada gambar diatas meliputi title bar beserta seperangkat tombol close, maximize, dan minimize, serta border tipis yang ada pinggiran window.

Di Linux ada beberapa WM yang sering dipakai seperti xfwm, metacity, unity, KWin, openbox, dan mutter (GTK 3). xfwm biasa digunakan oleh Desktop Environment XFCE, metacity digunakan oleh GNOME 2, KWin digunakan oleh KDE, unity digunakan oleh Ubuntu unity. itulah mengapa biasanya ada nama-nama WM ini di tema yang di download.

# Widget
Widget adalah apa saja yang ada di dalam area title bar dan window border. misalnya tombol back, menu bar, teks-teks, dan bahkan background dibalik icon-icon yang ada di gambar. Seperti WM, ada macam-macam juga pembentuk widget ini, ada GTK 2, GTK 3, dan Qt. Khusus GTK 3, pembuatan tema menggunakan CSS. Fantastis. GTK biasanya digunakan oleh software-software buatan GNOME, sedangkan Qt biasanya digunakan oleh software-software buatan KDE

# Icon
Icon juga merupakan aspek yang juga sangat penting di penemaan. Seperti misalnya tombol Home, Back, partisi harddisk, icon-icon di taskbar, semuanya diatur oleh tema icon. Namun ada beberapa aplikasi yang memaksa memakai suatu icon karena biasanya tidak tersedia di tema icon yang sedang digunakan.

-----
Hal ini juga yang membuat kami (Tim Software Riset TeaLinuxOS)  membagi tema dalam software "Theme Switcher Tray" menjadi tiga juga.

![mount]({{site.url}}/images/post/tiga-bagian-tema/theme-tray.png)
*Tampilan pengaturan untuk Theme Switcher Tray*

**Tips**: Jika Tema yang didownload tidak bekerja dengan salah salah satu dari tiga komponen diatas, cek apakah ada di dalam folder `/usr/share/themes/nama_tema` untuk tema WM dan Widget, dan di `/usr/share/icons/nama_icon` untuk tema icon.

Beberapa sumber:

* Wikipedia. Linux. diakses 3 Maret 2016. [https://en.wikipedia.org/wiki/Linux](https://en.wikipedia.org/wiki/Linux)

* Wikipedia. Qt. diakses 3 Maret 2016. [https://en.wikipedia.org/wiki/Qt_(software)](https://en.wikipedia.org/wiki/Qt_(software))

----

Sekian, apabila ada beberapa informasi yang kurang benar dalam artikel ini, saya mohon maaf dan saya sangat menerima kritikan dan saran.

*(Tulisan ini dipindah dari [blog lama](http://blog.nurulirfan.com))*
