[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things)
![Project](https://img.shields.io/badge/Project-Internet%20of%20Things-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things
<strong>Tugas Akhir IoT Master Class Indobot 2022</strong><br><br>
Echeveria Peacockii merupakan jenis tanaman yang memiliki kekerabatan dengan kaktus, namun pada tubuh tanaman ini tidak dijumpai adanya duri, sehingga sangat diminati oleh para pecinta tanaman hias. Perawatan Echeveria Peacockii hingga saat ini masih dilakukan secara konvensional, sehingga boros waktu dan tenaga. Oleh karena itu, proyek ini dibuat untuk mendapatkan sistem yang mampu melakukan penyiraman sekaligus mampu memantau perubahan kondisi yang ada di lingkungan sekitar tanaman. Proyek ini telah dilaksanakan dan memakan waktu kurang lebih 1 bulan. Antarmuka sistem menggunakan Bot Telegram. Hasil penelitian menunjukkan bahwa sistem yang dibuat dapat berfungsi dengan baik.

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | DOIT ESP32 DEVKIT V1 |
| Editor Kode | Arduino IDE |
| Dukungan Aplikasi | Bot Telegram |
| Driver | USB-Serial CP210X |
| Platform IoT | • Blynk<br>• ThingsBoard |
| Protokol Komunikasi | • Inter Integrated Circuit (I2C)<br>• Message Queuing Telemetry Transport (MQTT)<br>• Transmission Control Protocol/Internet Protocol (TCP/IP)<br>• MTProto |
| Arsitektur IoT | 4 Lapisan |
| Bahasa Pemrograman | C/C++ |
| Pustaka Arduino | • WiFi (bawaan)<br>• Wire (bawaan)<br>• BlynkSimpleEsp32<br>• ThingsBoard<br>• PubSubClient<br>• CTBot<br>• ArduinoJson<br>• LiquidCrystal_I2C<br>• DHT_sensor_library<br>• FC28 |
| Aktuator | Submersible pump (x2) |
| Sensor | • FC-28: Kelembaban Tanah Resistif (x1)<br>• LDR: Cahaya (x1)<br>• DHT22: Suhu & Kelembaban Udara (x1) |
| Layar | LCD I2C (x1) |
| Komponen Lainnya | • Kabel USB Mikro - USB tipe A (x1)<br>• Kabel jumper (1 set)<br>• Papan ekspansi ESP32 (x1)<br>• Breadboard (x1)<br>• Electrical relay 2 channel (x1)<br>• Adaptor DC 5V (x1)<br>• Resistor<br>• Kotak casing (x1)<br>• Baut plus (1 set)<br>• Mur (1 set) |

<br><br>

## Unduh & Instal
1. Arduino IDE

   <table><tr><td width="810">

   ```
   https://www.arduino.cc/en/software
   ```

   </td></tr></table><br>

2. USB-Serial CP210X

   <table><tr><td width="810">

   ```
   https://bit.ly/CP210X_Driver
   ```

   </td></tr></table>
   
<br><br>

## Rancangan Proyek
<table>
<tr>
<th colspan="2">Desain Perangkat Keras</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/5b54e9a0-2972-46b9-a06b-d8a093266ee9" alt="pictorial-diagram"></td>
<td width="420"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/ab0fb888-ead7-45e3-8ac7-d82bda7de03f" alt="schematic-diagram"></td>
</tr>
</table>
<table>
<tr>
<th colspan="2">Desain Perangkat Lunak</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/3c6af705-8d0b-4291-9825-d633338e1f67" alt="flowchart-blynk"></td>
<td width="420"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/45c85d49-59ff-4f20-98ce-9405e0c07fe5" alt="flowchart-thingsboard"></td>
</tr>
</table>

<br><br>

## Pengaturan Arduino IDE
1. Buka ``` Arduino IDE ``` terlebih dahulu, kemudian buka proyek dengan cara klik ``` File ``` -> ``` Open ``` : 

   <table><tr><td width="810">
      
      ``` SistemPerawatanEcheveriaBlynkIoT.ino ``` atau ``` SistemPerawatanEcheveriaThingsboardIoT.ino ```
         
   </td></tr></table><br>
   
2. Isi ``` Url Pengelola Papan Tambahan ``` di Arduino IDE

   <table><tr><td width="810">

      Klik ``` File ``` -> ``` Preferences ``` -> masukkan ``` Boards Manager Url ``` dengan menyalin tautan berikut :
      
      ```
      https://dl.espressif.com/dl/package_esp32_index.json
      ```
         
   </td></tr></table><br>
   
3. ``` Pengaturan Board ``` di Arduino IDE

   <table>
      <tr><th width="810">

      Cara mengatur board ``` DOIT ESP32 DEVKIT V1 ```
            
      </th></tr>
      <tr><td>
         
      • Cara: klik ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Instal ``` esp32 ```.

      • Kemudian klik: ``` Tools ``` -> ``` Board ``` -> ``` ESP32 Arduino ``` -> ``` DOIT ESP32 DEVKIT V1 ```.

      </td></tr>
   </table><br>
   
4. ``` Ubah Kecepatan Papan ``` di Arduino IDE

   <table><tr><td width="810">

      Klik ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```
         
   </td></tr></table><br>
   
5. ``` Instal Pustaka ``` di Arduino IDE

   <table><tr><td width="810">

      Unduh semua file zip pustaka. Kemudian tempelkan di: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```
         
   </td></tr></table><br>

6. ``` Pengaturan Port ``` di Arduino IDE

   <table><tr><td width="810">

      Klik ``` Port ``` -> Pilih sesuai dengan port perangkat anda ``` (anda dapat melihatnya di Device Manager) ```
         
   </td></tr></table><br>

7. Ubah ``` Nama WiFi ```, ``` Kata Sandi WiFi ```, dan sebagainya sesuai dengan apa yang anda gunakan saat ini.<br><br>

8. Sebelum mengunggah program, silakan klik: ``` Verify ```.<br><br>

9. Jika tidak ada kesalahan dalam kode program, silakan klik: ``` Upload ```.<br><br>
    
10. Beberapa hal yang perlu anda lakukan saat menggunakan ``` board ESP32 ``` :

    <table><tr><td width="810">
       
      • Informasi ``` Arduino IDE ```: ``` Uploading... ``` -> segera tekan dan tahan tombol ``` BOOT ```.

      • Informasi ``` Arduino IDE ```: ``` Writing at .... (%) ``` -> lepaskan tombol ``` BOOT ```.

      • Tunggu sampai muncul pesan: ``` Done Uploading ``` -> ``` Program langsung dioperasikan ```.

      • Tekan tombol ``` EN (RST) ``` lalu ``` Restart ``` untuk menangani board ``` ESP32 ``` yang tidak bisa memproses ``` SC ```.

      • Jangan tekan tombol ``` BOOT ``` dan ``` EN ``` secara bersamaan karena hal ini bisa beralih ke mode ``` Unggah Firmware ```.

    </td></tr></table><br>

11. Jika masih ada masalah saat unggah program, maka coba periksa pada bagian ``` driver ``` / ``` port ``` / ``` yang lainnya ```.

<br><br>

## Pengaturan Blynk
1. Memulai blynk :

   <table><tr><td width="810">
      
      • Buka situs resmi Blynk berikut: <a href="https://blynk.io">blynk.io</a>.
      
      • Klik ``` Start Free ``` untuk mendaftar.
      
      • Masukkan email.
      
      • Buka email untuk konfirmasi.
      
      • Masuk menggunakan akun yang sudah dibuat.

   </td></tr></table><br>   
   
2. Buat template baru :

   <table><tr><td width="810">
      
      • Klik ``` Developer Zone ``` -> lalu pilih opsi ``` My Templates ```.
   
      • Kemudian klik ``` + New Templates ``` untuk membuat Template Baru.
   
      • Bagian ``` NAME ``` diisi dengan ``` Smart Farming ```, ``` HARDWARE ``` pilih ``` ESP32 ```, ``` CONNECTION TYPE ``` pilih ``` WiFi ```, ``` TEMPLATE DESCRIPTION ``` bersifat opsional.
   
      • Klik ``` Done ```.

   </td></tr></table><br>
   
3. Buat datastreams :

   <table><tr><td width="810">
      
      • Masuk ke menu ``` Datastreams ``` -> klik ``` + New Datastreams ``` -> pilih ``` Virtual Pin ```.
      
      • Masukkan data pertama :
   
      - ``` NAME ``` -> ``` suhu_udara ```
      - ``` PIN ``` -> ``` V0 ```
      - ``` DATA TYPE ``` -> ``` Double ```
      - ``` UNITS ``` -> ``` Celcius, °C ```
      - ``` MIN ``` -> ``` 0 ```
      - ``` MAX ``` -> ``` 100 ```
      - ``` DECIMALS ``` -> ``` #.# ```
      - ``` DEFAULT VALUE ``` -> ``` 0 ```<br><br>
            
      • Masukkan data kedua :
   
      - ``` NAME ``` -> ``` kelembapan_udara ```
      - ``` PIN ``` -> ``` V1 ```
      - ``` DATA TYPE ``` -> ``` Integer ```
      - ``` UNITS ``` -> ``` Percentage, % ```
      - ``` MIN ``` -> ``` 0 ```
      - ``` MAX ``` -> ``` 100 ```
      - ``` DEFAULT VALUE ``` -> ``` 0 ```<br><br>
           
      • Masukkan data ketiga :
   
      - ``` NAME ``` -> ``` kelembapan_tanah ```
      - ``` PIN ``` -> ``` V2 ```
      - ``` DATA TYPE ``` -> ``` Integer ```
      - ``` UNITS ``` -> ``` Percentage, % ```
      - ``` MIN ``` -> ``` 0 ```
      - ``` MAX ``` -> ``` 100 ```
      - ``` DEFAULT VALUE ``` -> ``` 0 ```<br><br>
      
      • Masukkan data keempat :
   
      - ``` NAME ``` -> ``` cahaya ```
      - ``` PIN ``` -> ``` V3 ```
      - ``` DATA TYPE ``` -> ``` Integer ```
      - ``` UNITS ``` -> ``` Lux, lx ```
      - ``` MIN ``` -> ``` 0 ```
      - ``` MAX ``` -> ``` 100000 ```
      - ``` DEFAULT VALUE ``` -> ``` 0 ```<br><br>
         
      • Klik ``` Create ```.
      
      • Klik ``` Save ```.

   </td></tr></table><br>
   
4. Buat device baru :

   <table><tr><td width="810">
      
      • Masuk ke menu ``` Devices ```.
      
      • Klik ``` + New Devices ``` untuk menambahkan devices baru.
      
      • Pilih ``` From Templates ``` :
   
      - ``` TEMPLATE ``` -> ``` Smart Farming ```
      - ``` DEVICE NAME ``` -> ``` Smart Farming ```<br><br>
           
      • Klik ``` Create ```.

   </td></tr></table><br>
   
5. Kelola dashboard pada situs Blynk :

   <table><tr><td width="810">
      
      • Klik ``` simbol titik 3 ``` -> kemudian pilih ``` Edit Dashboard ```.
   
      • Pilih ``` widget yang diinginkan ``` lalu ``` drag ``` ke area dashboard.
   
      • Klik ``` setting ``` pada widget yang ditambahkan.
   
      • Pilih datastream yang sudah tersedia, antara lain: ``` suhu_udara ``` / ``` kelembapan_udara ``` / ``` kelembapan_tanah ``` / ``` cahaya ```.
   
      • Klik ``` Save And Apply ```.

   </td></tr></table><br>

6. Kelola dashboard pada Blynk mobile apps :

   <table><tr><td width="810">
      
      • Buka ponsel pintar anda -> lalu di ``` Google Play Store ```, cari aplikasi yang bernama ``` Blynk IoT ``` -> kemudian ``` instal ```.
   
      • Buka aplikasi tersebut -> lalu lakukan konfigurasi seperti yang ada di situs Blynk tadi.
   
      • Selebihnya anda dapat mencari tutorial di ``` Google ``` untuk memperkaya wawasan anda.

   </td></tr></table><br>
   
7. Konfigurasi firmware :

   <table><tr><td width="810">
      
      • Masuk ke menu  ``` Devices ``` -> pilih ``` Smart Farming ``` -> klik ``` Device Info ```.
   
      • Salin ``` ID Template ```, ``` Nama Template ```, dan ``` AuthToken ``` tersebut.
   
      • Kemudian tempelkan pada bagian paling atas kode firmware, contohnya seperti ini :
   
      ```ino
      #define BLYNK_TEMPLATE_ID "TMPL6ZSHxYC-z"
      #define BLYNK_TEMPLATE_NAME "Smart Farming"
      #define BLYNK_AUTH_TOKEN "fw1oXlpe-YfYh7JXQHu4QTS3EqlnM-iw"
      ```

   </td></tr></table>
   
<br><br>

## Pengaturan ThingsBoard
1. Memulai ThingsBoard :

   <table><tr><td width="810">
      
      • Buka situs resmi ThingsBoard berikut: <a href="https://thingsboard.cloud/">thingsboard.cloud</a>.
      
      • Masuk dengan akun google.

   </td></tr></table><br>
   
2. Buat device profile baru :

   <table><tr><td width="810">
      
   • Masuk ke menu ``` Profiles ``` -> lalu pilih ``` Device profiles ```.

   •  Klik ``` + (Add device profile) ```.

   •  Device profile details: ``` Name ``` -> ``` MQTT ```.

   •  Transport configuration: ``` Transport type ``` -> ``` MQTT ```. Lalu isilah data MQTT seperti yang terlihat di bawah ini :

      <table><tr><td width="810">
      
      - Telemetry topic filter: ``` v1/devices/me/telemetry/fpiotdevan ```. Ini nanti harus sama dengan yang ada di kode firmware.
        
      - Attributes publish & subscribe topic filter: ``` v1/devices/me/attributes/fpiotdevan ```. Ini nanti harus sama dengan yang ada di kode firmware.
        
      - MQTT device payload : ``` JSON ```.

      </td></tr></table>

   •  Klik ``` Add ``` untuk menambahkan.

   </td></tr></table><br>
   
3. Buat device baru :

   <table><tr><td width="810">
      
      • Masuk ke menu ``` Entities ``` -> lalu pilih ``` Devices ``` -> ``` Groups ```.
   
      • Ubah akses device groups ``` All ``` menjadi ``` Public ``` agar dapat digunakan secara luas.
   
      • Buka device groups ``` All ```.
   
      • Klik ``` + (Add device) ```.
   
      • Buatlah 1 device dengan ketentuan sebagai berikut :

      <table><tr><td width="810">
      
      - ``` Name ``` -> ``` EcheveriaIoT ```
      - ``` Label ``` -> ``` EcheveriaIoT ```
      - ``` Device profile ``` -> ``` default ```
   
      </td></tr></table>

   </td></tr></table><br>
   
5. Buat dashboard :

   <table><tr><td width="810">
      
      • Masuk ke menu ``` Dashboards ``` -> ``` Groups ``` -> ``` All ```.
   
      • Ubah akses dashboard groups ``` All ``` menjadi ``` Public ``` agar dapat digunakan secara luas.
   
      • Buka dashboard groups ``` All ```.
   
      • Klik ``` + (Add dashboard) ```.
   
      • Lalu beri nama ``` Echeveria Dashboard ``` -> klik ``` Add ``` untuk menambahkan.
   
      • Ubah ``` title ``` menjadi ``` Sistem Perawatan Echeveria ```.
   
      • Pilih ``` widget yang diinginkan ``` -> pengaturan pada widget.

   </td></tr></table><br>
   
6. Konfigurasi firmware :

   <table><tr><td width="810">
      
      • Masuk ke menu ``` Entities ``` -> lalu pilih ``` Devices ``` -> ``` Groups ```.
   
      • Klik ``` EcheveriaIoT ``` -> salin ``` ID Device ``` dan ``` Token ``` tersebut.
   
      • Kemudian tempelkan pada kode firmware, contohnya seperti ini :
   
      ```ino
      #define DEVICE_ID_TB "26001630-a274-11ee-9db5-1fb69bbe078f"
      #define ACCESS_TOKEN_TB "tovosJJOLHzwc42DSfvM"
      ```

   </td></tr></table>

<br><br>

## Pengaturan Bot Telegram
1. Buka <a href="https://t.me/botfather">@BotFather</a>.<br><br>

2. Ketik ``` /newbot ```.<br><br>

3. Ketik nama bot yang diinginkan, contoh: ``` echeveria_bot ```.<br><br>

4. Ketik nama pengguna bot yang diinginkan, contoh: ``` echeveria_bot ```.<br><br>

5. Lakukan juga untuk pengaturan gambar bot, deskripsi bot, dan lain sebagainya menyesuaikan dengan kebutuhan anda.<br><br>

6. Salin ``` API token bot telegram anda ``` -> lalu tempelkan pada bagian ``` #define BOTtoken "YOUR_API_BOT_TOKEN" ```. 

   <table><tr><td width="810">
      
   Contohnya :

   ```ino
   #define BOTtoken "5911801402:AAFEEuBYHPmDxlYQxfPpTCZkRpn5d8hV_3E"
   ```
         
   </td></tr></table>

<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>
   
2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
   
4. Konfigurasikan perangkat anda menurut pengaturan di atas.<br><br>

5. Selamat menikmati [Selesai].

<br><br>

## Sorotan
<table>
<tr>
<th width="840">Produk</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/88b94f07-953e-4cdb-84f8-a4849ff031e8" alt="product"></td>
</tr>
</table>
<table>
<tr>
<th colspan="3">Antarmuka Bot Telegram</th>
<th colspan="1">Pemantauan melalui Blynk Mobile</th>
</tr>
<tr>
<td width="210"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/d57ba0a1-895b-4d49-99b0-22931c8f99bb" alt="interfacebot-1"></td>
<td width="210"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/37cef7d6-f2b2-4e94-8ed6-d696780e13a5" alt="interfacebot-2"></td>
<td width="210"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/ce29156a-5f1b-4231-a1d9-4ba03e28bea5" alt="interfacebot-3"></td>
<td width="210"><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/ef87921c-a8ef-489e-8b66-1a86260e76f9" alt="blynk-mobile"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Pemantauan melalui Thingsboard</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Sistem-Perawatan-Echeveria-Peacockii-Berbasis-Bot-of-Things/assets/54527592/48380dd7-cb7c-4c7d-ae1c-e637bf9adacf" alt="thingsboard"></td>
</tr>
</table>

<br><br>

## Demonstrasi Aplikasi
Via Telegram: <a href="https://t.me/echeveria_bot">@echeveria_bot</a>

<br><br>

## Apresiasi
Jika karya ini bermanfaat bagi anda, maka dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan mengklik tombol ``` ⭐Bintang ``` di bagian atas repositori.

<br><br>

## Penafian
Aplikasi ini dibuat dengan menyertakan sumber-sumber dari pihak ketiga. Pihak ketiga di sini adalah penyedia layanan, yang layanannya berupa pustaka, kerangka kerja, dan lain-lain. Saya ucapkan terima kasih banyak atas layanannya. Telah terbukti sangat membantu dan dapat diimplementasikan.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2023 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
