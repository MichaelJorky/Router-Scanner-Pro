# 📡 Router Scanner Pro v3.8.0.1 (Beta Version)

Router Scanner Pro adalah aplikasi pemindaian router berperforma tinggi yang dirancang untuk melakukan scanning terhadap banyak alamat IP secara paralel menggunakan multi-threading. Aplikasi ini membantu melakukan identifikasi perangkat jaringan, memeriksa port terbuka, mendeteksi otentikasi, serta mengambil informasi jaringan seperti BSSID, ESSID, WiFi Key, WPS Pin, LAN IP Address, LAN Subnet Mask, WAN IP Address, WAN Subnet Mask, WAN Gateway, DNS, Hostname, ASN, ISP Name, Organization Name, Connection Type, Country Name, Country Code, State, Country, City, Postal Code,  Latitude, Longitude, Device MAC Address, Device Serial Number, Software Version dan Hardware Version dari target.

## 🚀 Fitur Utama

### 🔍 1. Pemindaian Daftar IP

* Mendukung **load file IP** eksternal (format `.txt`).
* Setiap IP dipindai secara berurutan atau paralel sesuai jumlah thread.

### ⚙️ 2. Pengaturan Port Scan

* Pengguna dapat mengatur port target untuk pemindaian (contoh: `80`, `8080`, `443`, dll).
* Mendukung single port atau port khusus sesuai kebutuhan.

### 🧵 3. Multi-Threading

* Dilengkapi pengaturan **Max Threads** untuk mengoptimalkan kecepatan.
* Cocok untuk daftar IP besar (ratusan hingga ribuan).

### 🌐 4. Node Relay (Opsional)

* Mode pemindaian melalui relay node eksternal.
* Berguna untuk routing tertentu, bypass pembatasan, atau mode scanning anonim.

## 🖥️ 5. Monitor Informasi Router (Lengkap)

Aplikasi menampilkan informasi router secara detail melalui tabel utama dengan kolom sebagai berikut:

| Kolom                         | Keterangan                                                  |
| ----------------------------- | ----------------------------------------------------------- |
| **No**                        | Nomor urut data                                             |
| **IP Address**                | Alamat IP target yang dipindai                              |
| **Port**                      | Port yang diuji                                             |
| **Time (ms)**                 | Waktu respon dalam milidetik                                |
| **Status**                    | Status koneksi (Success / Failed / Timeout)                 |
| **Device Type / Server Name** | Identifikasi tipe perangkat atau nama server                |
| **Authorization**             | Jenis otentikasi (Basic / Digest / Login Page / etc)        |
| **BSSID**                     | MAC Address Access Point                                    |
| **ESSID**                     | Nama jaringan Wi-Fi                                         |
| **Security**                  | Jenis enkripsi Wi-Fi (WPA2, WPA3, Open, dll)                |
| **WiFi Key**                  | Password Wi-Fi (jika berhasil diambil melalui API tertentu) |
| **WPS Pin**                   | PIN WPS perangkat                                           |
| **LAN IP Address**            | IP lokal router (sisi LAN)                                  |
| **LAN Subnet Mask**           | Subnet mask LAN                                             |
| **WAN IP Address**            | IP publik atau IP WAN router                                |
| **WAN Subnet Mask**           | Subnet mask WAN                                             |
| **WAN Gateway**               | Gateway koneksi WAN                                         |
| **Domain Name Servers**       | DNS yang digunakan router                                   |
| **Hostname**                  | Nama host router                                            |
| **ASN**                       | Autonomous System Number                                    |
| **ISP Name**                  | Nama ISP penyedia layanan                                   |
| **Organization Name**         | Nama organisasi pemilik IP                                  |
| **Connection Type**           | Tipe koneksi (Fiber, Wireless, DSL, dll)                    |
| **Country Name**              | Nama negara pemilik IP                                      |
| **Country Code**              | Kode negara (ISO Code)                                      |
| **State / Province**          | Provinsi / State                                            |
| **District / Country**        | Kabupaten / Distrik                                         |
| **City**                      | Kota                                                        |
| **Postal Code**               | Kode pos lokasi IP                                          |
| **Latitude**                  | Garis lintang lokasi IP                                     |
| **Longitude**                 | Garis bujur lokasi IP                                       |
| **Device MAC Address**        | Alamat MAC perangkat                                        |
| **Device Serial Number**      | Nomor seri perangkat                                        |
| **Software Version**          | Versi firmware / aplikasi router                            |
| **Hardware Version**          | Versi hardware router                                       |

### 🧭 6. Control Panel Lengkap

* **Start Scan** — Memulai pemindaian.
* **Pause Scan** — Menjeda proses.
* **Stop Scan** — Menghentikan pemindaian kapan saja.

### 📊 7. Status Bar Real-Time

Menampilkan informasi berikut:

* Status jaringan (online/offline)
* Progress scanning (%)
* ETA (perkiraan selesai)
* Kecepatan pemindaian (IP/s)
* Jumlah IP berhasil/gagal
* Alamat IP lokal (device info)

---

## 🖥️ Tampilan Antarmuka (UI Overview)

Antarmuka dibuat sederhana dan mudah dipahami, terdiri dari:

* Panel kiri atas: **Load IPs File**
* Panel kanan atas: **Scan Ports**, **Max Threads**, **Node Relay**
* Bagian tengah: **Main Router Table** (tabel hasil scanning)
* Bagian bawah: **Status Bar**

Desain ini memastikan pengguna dapat langsung bekerja tanpa proses konfigurasi rumit.

---

## 📁 Format Input File

File daftar IP yang digunakan harus berupa `.txt`, contoh:

```
192.168.1.1
192.168.0.1
10.0.0.1
172.16.1.5
```

---

## ⚡ Performa

Dengan dukungan multi-thread hingga 50 thread (atau lebih tergantung spesifikasi), pemindaian dapat berjalan sangat cepat dan efisien tanpa membebani sistem operasi.

---

## 🔧 Kompatibilitas

* **OS**: Windows 7 / 8 / 10 / 11
* **Arsitektur**: 32-bit / 64-bit disarankan untuk performa terbaik
* **Library/Framework**:

  * WinSock
  * HTTP/S Client
  * Parsing Header untuk identifikasi perangkat

---

## 🛡️ Catatan Penting (Legal & Etika)

Aplikasi ini **hanya untuk keperluan pembelajaran, pengujian jaringan pribadi, dan administrasi jaringan**.

❗ **Dilarang keras** menggunakan alat ini untuk:

* Pemindaian jaringan tanpa izin
* Akses ilegal
* Aktivitas berbahaya lainnya

Pengembang tidak bertanggung jawab atas penyalahgunaan software.

---

## 📦 Rencana Pengembangan (Roadmap)

* [ ] Penambahan Auto Detect Multiple Ports
* [ ] Export hasil scanning ke HTML, XML atau JSON
* [ ] Integrasi Proxy / VPN
* [ ] UI/UX Modern (WinUI / Fluent)
* [ ] Dark Mode
* [ ] Identifikasi Router berdasarkan Signature Fingerprint

---

## 🤝 Kontribusi

Kontribusi sangat terbuka!
Silakan buat **Issue** atau **Pull Request** melalui GitHub Repository.

---

## 📧 Kontak

Untuk pertanyaan atau saran, hubungi melalui:

**Email:** Wgalxczk3@Mozmail.Com
