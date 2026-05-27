# 🚀 Astro Quest: Penjelajah Antariksa 3D

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Three.js](https://img.shields.io/badge/Three.js-black?logo=three.js&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?logo=vite&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

**Astro Quest** adalah aplikasi simulasi tata surya 3D interaktif yang dibangun menggunakan **Three.js** dan **Vite**. Tidak hanya sekadar melihat planet, aplikasi ini dilengkapi dengan fitur edukasi seperti kuis antariksa interaktif, koleksi planet, pencapaian pemain, hingga fitur **Camera AR** untuk menggabungkan simulasi 3D dengan dunia nyata!

<div align="center">
  <img src="images/solar_system.png" alt="Solar System Overview" width="800"/>
</div>

---

## ✨ Fitur Utama

- 🌍 **Simulasi 3D Realistis**: Jelajahi Matahari, 8 planet, bulan (termasuk satelit seperti Phobos dan Deimos), dan sabuk asteroid dengan rotasi serta orbit yang dihitung secara matematis.
- 📸 **Mode Camera AR (Augmented Reality)**: Gabungkan model tata surya 3D yang interaktif langsung dengan tangkapan kamera perangkat Anda!
- 🎮 **Kuis Antariksa Edukatif**: Uji pengetahuan Anda tentang tata surya. Jawab pertanyaan dengan benar untuk mendapatkan *Poin* dan *Koleksi Planet*!
- 🏆 **Koleksi & Pencapaian**: Simpan koleksi planet 3D yang telah Anda menangkan dari Kuis. Dilengkapi dengan sistem penyimpanan persisten (*LocalStorage* / *Firebase Database*).
- ⚙️ **Kontrol Interaktif**: Atur kecepatan orbit, intensitas rotasi, dan cahaya matahari secara *real-time*.
- 🌌 **Visual Tingkat Lanjut**: Efek pasca-pemrosesan (*Post-Processing*) seperti *Bloom* (Cahaya Matahari), bayangan (*Shadows*), tekstur *bump*, *ShaderMaterial* untuk awan bumi yang bergerak, dan cincin planet.

---

## 🛠️ Teknologi yang Digunakan

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **3D Engine**: [Three.js](https://threejs.org/)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Autentikasi & Database**: Firebase Authentication, Firebase Realtime Database / LocalStorage
- **Deployment**: Vercel / GitHub Pages
- **Fitur Kamera**: WebRTC MediaDevices API

---

## 📁 Struktur Direktori

```text
📦 Astro Quest (Solar-System)
┣ 📂 public/
┃ ┣ 📂 images/            # Tekstur planet, satelit, dan background
┃ ┗ 📂 models/            # Model 3D (jika ada, e.g., asteroid/satelit non-bulat)
┣ 📂 src/
┃ ┣ 📜 index.html         # Halaman utama aplikasi
┃ ┣ 📜 style.css          # Styling utama (Animasi, UI Simulasi AR)
┃ ┣ 📜 misi.css           # Styling untuk Panel Kuis, Koleksi, & Autentikasi
┃ ┣ 📜 script.js          # Logika Three.js, Camera AR, & UI Interaktif
┃ ┗ 📜 misi.js            # Logika Kuis, Algoritma Koleksi, Database & Firebase
┣ 📜 package.json         # Konfigurasi dependensi npm
┣ 📜 vite.config.js       # Konfigurasi bundler Vite
┣ 📜 JALANKAN.bat         # Script otomatis jalankan server lokal (Windows)
┣ 📜 NGROK_JALANKAN.bat   # Script untuk public tunneling
┣ 📜 FORCE_PUSH.bat       # Script sinkronisasi paksa ke GitHub
┗ 📜 readme.md            # Dokumentasi repositori ini
```

---

## 🚀 Cara Menjalankan Aplikasi Secara Lokal

Anda bisa menjalankan game ini di komputer lokal dengan langkah-langkah berikut:

### Prasyarat
- [Node.js](https://nodejs.org/) terinstal di komputer Anda.
- Git untuk melakukan *clone* repository.

### Instalasi & Menjalankan (Windows)
1. **Clone repositori**:
   ```sh
   git clone https://github.com/hasanamirul/Solar-System.git
   cd Solar-System
   ```
2. **Jalankan Aplikasi dengan `JALANKAN.bat`**:
   Cukup klik dua kali (*double click*) file **`JALANKAN.bat`**. Skrip ini akan secara otomatis:
   - Menginstal semua dependensi npm (`npm install`).
   - Menjalankan server lokal Vite.
   - Membuka browser default secara otomatis di `http://localhost:5173`.

> **Alternatif Manual (Mac/Linux)**:
> ```sh
> npm install
> npm run dev
> ```

---

## 🌐 Menjalankan Secara Publik (Ngrok)

Jika Anda ingin membagikan akses sementara atau menguji **Camera AR** di perangkat HP Anda:
1. Daftar dan dapatkan *Authtoken* gratis di [ngrok.com](https://dashboard.ngrok.com).
2. Download file `ngrok.exe` dan letakkan di dalam folder repositori ini.
3. Jalankan konfigurasi token di terminal:
   ```cmd
   ngrok config add-authtoken <TOKEN_ANDA>
   ```
4. Klik dua kali **`NGROK_JALANKAN.bat`**. Link `https://xxxx.ngrok-free.app` akan muncul dan siap digunakan di *smartphone* Anda.

---

## 🕹️ Panduan Penggunaan

- **Navigasi 3D**:
  - `Klik Kiri & Geser (Mouse)` / `Sentuh & Geser (Layar Sentuh)`: Memutar kamera mengelilingi tata surya.
  - `Scroll (Mouse)` / `Cubit (Layar Sentuh)`: Memperbesar (*Zoom In*) atau Memperkecil (*Zoom Out*).
- **Info Planet**: Klik pada planet mana saja untuk melakukan *zoom* otomatis dan melihat panel informasi spesifik planet (Jari-jari, Suhu, Jarak dari Matahari, dll).
- **Camera AR**: Klik tombol **Kamera AR** di dalam simulasi untuk menghidupkan kamera perangkat, seolah tata surya berada di ruangan Anda!
- **Kuis & Koleksi**:
  - Login dengan akun Google (atau akses sebagai Guest).
  - Mulai sesi kuis untuk memenangkan planet 3D.
  - Buka tab "Koleksi Saya" untuk berinteraksi dengan model 3D planet yang sudah Anda kumpulkan.

---

## 🤝 Kontribusi

Aplikasi ini bersifat *Open Source*. Jika Anda ingin menambahkan fitur baru, memperbaiki *bug*, atau meningkatkan kualitas model 3D:
1. Lakukan *Fork* repositori ini.
2. Buat *branch* baru: `git checkout -b fitur-keren-anda`
3. Lakukan *Commit*: `git commit -m 'Menambahkan fitur keren'`
4. Lakukan *Push*: `git push origin fitur-keren-anda`
5. Buat **Pull Request**!

---

## 📄 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE). Anda bebas menggunakan, memodifikasi, dan mendistribusikan proyek ini untuk tujuan pribadi maupun komersial dengan tetap menyertakan atribut *copyright* asli.

---
*Dibuat dengan ❤️ untuk mengeksplorasi luasnya alam semesta dari layar perangkat Anda.*
