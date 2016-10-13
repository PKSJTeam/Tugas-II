# Tugas 2

Tugas 2 PKSJ - Ganjil 2016/2017

Pendahuluan

Tugas 2 adalah tugas kedua yang harus di selesaikan sebagai salah satu syarat penilaian pada matakuliah Perancangan Keamanan & Sistem Jaringan (PKSJ) Semester Ganjil 2016/2017, TeknikInformatika ITS, Surabaya

AnggotaKelompok

• Dewi Kartika 5113100008

• M.Sholaudin 5112100075

• FauzanAdim 5113100101

Dasar teori :

    OS yang digunakan


![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Tools/ubuntu1.jpg)


   • Ubuntu Server adalah salah satu varian dari distro linux Ubuntu. Dalam pembahasan kali ini dan pembahasan selanjutnya, saya akan membahas tentang perintah CLI di Linux dan seting server menggunakan ubuntu 12.10. Namun sebelum membahas lebih jauh tentang Ubuntu server akan saya kenalkan dulu apa itu ubuntu server dalam format FAQ sehingga lebih mudah di pahami.

![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Tools/kali.png)

   • Kali Linux adalah distribusi berlandasan distribusi Debian GNU/Linux untuktujuanforensik digital dan di gunakan untuk pengujian penetrasi, yang dipelihara dan didanai oleh Offensive Security. Kali juga dikembangkan oleh Offensive Security sebagai penerus BackTrack Linux. Salah satu distribusi Linux tingkat lanjut untuk Penetration Testingdan audit keamanan. Distroinidulunyaadalahdistro Backtrack, yang kemudian memutuskan mengganti nama distronya tersebut menjadi Kali Linux di versi terbarunya. Kali Linux ini akan dijadikan sebagai standarisasi distro Linux yang digunakan untuk percobaan penetrasi.

    Tools yang digunakan :
    
![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Tools/wordp.png)

   • Wordpress adalah sebuah aplikasi sumber terbuka (open source) yang sangat populer digunakan sebagai mesin blog (blog engine). WordPress dibangun dengan bahasa pemrograman PHP dan basis data (database) MySQL. PHP dan MySQL, keduanya merupakan perangkat lunak sumber terbuka (open source software).

![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Tools/video.jpg)

   • Video player 1.5.16 adalah istilah yang biasa digunakan untuk mendeskripsikan software komputer untuk memainkan file video. Sebagian besar media player dapat menampilkan sejumlah format media, baik file audio ataupun video, sedangkan yang khusus untuk memainkan video disebut dengan video player.

   • League Manager adalah plugin yang digunakan untuk mendesain dan memanajemen sport league dan untuk menampilkan nya pada blog.

![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Tools/xampp.png)

   • XAMPP adalah software yang merupakan software web server apache yang di dalamnya sudah terdapat database seperti mysql, php dan masih banyak lagi. Kelebihan software web server XAMPP ini di banding dengan software web server lain adalah dalam satu kali install software ini telah sekaligus terinstall Apache Web Server, MySQL Database Server, PHP Support.

![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Tools/sqlmap_1.png)

   • SQLMap adalah tool open source yang di jalankan menggunakan command dan support untuk data base MySQL, Oracle, PostgreSQL, Microsoft SQL Server, Microsoft Access, IBM DB2, SQLite, Firebird, Sybase and SAP MaxDB.

    Langkah Instalasi

    3.1 Instalasi Wordpress

    a. Masuk ke user root MySQL

     dengan command mysql -u root -p



    b. Melakukan proses download Wordpress

     dengan command wget http://wordpress.org/latest.tar.gz

    c. Extract Wordprees yang telah didownload

     dengan command tar xzvf latest.tar.gz

    d. Lakukan update pada Ubuntu server

     dengan command sudo apt-get update

    e. Installing PHP

     dengan command sudo apt-get install php5-gd libssh2-php

    f. Konfigurasi wordpress

     dengan command cd ~/wordpress

    g. Lakukan copying

     dengan command cp wp-config-sample.php wp-config.php

    h. Memberika parameter berupa informasi database yang dibuat

     dengan command 

         /** The name of the database for WordPress */

          define('DB_NAME', 'wordpress');


         /** MySQL database username */

          define('DB_USER', 'wordpressuser');


         /** MySQL database password */

          define('DB_PASSWORD', 'password');

    j. Masuk ke /var/www/html/

      dengan command sudo rsync -avP ~/wordpress/ /var/www/html/

    k. Masuk ke document root

      dengan command cd /var/www/html

    l. Quickly assign these ownership values

      dengan command sudo chown -R demo:www-data *

    m. Membuat folder untuk mengisi file upload

      dengan command mkdir /var/www/html/wp-content/uploads

    n. Allow the web server itself to write to this directory

      dengan command sudo chown -R :www-data /var/www/html/wp-content/uploads

    3.2 Instalasi SQLmap
    
    a. Download sqlmap 
        dengan command wget 'https://github.com/sqlmapproject/sqlmap/tarball/master' --output-document=sqlmapproject-sqlmap-0.9-3671-gdcaad75.tar.gz

    3.3 Instalasi League Manager
    Login Admin
    a.![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Image/Plugin/League-Manager/0.jpg)
    
    Halaman Web Admin
    b.![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Image/Plugin/League-Manager/1.jpg)
    
    Install Plugin Baru
    c.![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Image/Plugin/League-Manager/2.jpg)
    
    Upload Plugin
    d.![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Image/Plugin/League-Manager/3.jpg)
    
    Aktifkan Plugin
    e.![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Image/Plugin/League-Manager/4.jpg)
    
    Plugin telah aktif
    f.![alt tag](https://github.com/PKSJTeam/Tugas-II/blob/master/Image/Plugin/League-Manager/5.jpg)
