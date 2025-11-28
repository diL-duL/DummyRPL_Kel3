<div align="center">

# 🖥️ Service Display System

**Sistem Manajemen Antrian & Digital Signage Modern Berbasis Web**

[![Laravel](https://img.shields.io/badge/Laravel-12-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)](https://laravel.com)
[![Livewire](https://img.shields.io/badge/Livewire-3-4E56A6?style=for-the-badge&logo=livewire&logoColor=white)](https://livewire.laravel.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![PHP](https://img.shields.io/badge/PHP-8.2-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net)

<p align="center">
  <img src="https://github.com/user-attachments/assets/07f7d579-e5ee-4c1c-8ceb-758dcaf894eb" alt="Service Display Preview" width="100%">
</p>

</div>

---

## 📖 Tentang Aplikasi

Sistem Manajemen Antrian dan Digital Signage (Papan Informasi Digital) modern berbasis web. Dibangun menggunakan Laravel dan Livewire untuk performa real-time yang ringan tanpa memerlukan konfigurasi WebSocket server yang rumit.

Dibangun dengan **Laravel** dan **Livewire**, aplikasi ini menawarkan performa *real-time* yang ringan tanpa memerlukan konfigurasi WebSocket server yang rumit.

---

## ✨ Fitur Utama

### 📺 Public Display (Halaman TV)
| Fitur | Deskripsi |
| :--- | :--- |
| **⚡ Real-time Updates** | Tampilan otomatis berubah setiap 2 detik saat Admin mengupdate data. |
| **📐 Fluid Layout** | Desain responsif memenuhi layar (Full Width & Height) tanpa celah. |
| **🎬 Multimedia Player** | Putar video promosi via **Upload Lokal (MP4)** atau **YouTube Embed**. |
| **🏃 Dynamic Marquee** | *Running text* dengan kecepatan yang dapat diatur via Admin. |
| **📋 Queue List** | Daftar antrian dengan status: `Menunggu`, `Proses`, `Selesai`. |
| **⏳ Countdown Timer** | Hitung mundur estimasi waktu pengerjaan otomatis. |
| **🕒 Clock & Date** | Widget jam digital dan tanggal akurat (*Client-side update*). |

### 🛠️ Admin Dashboard
- **Queue Management**: Tambah, Edit, dan Hapus data antrian dengan mudah.
- **Settings Control**: Ubah Judul, Running Text, Kecepatan Teks, dan Video langsung dari dashboard.
- **Live Preview**: Lihat preview kecepatan teks dan video saat mengedit.
- **Modern UI**: Antarmuka elegan dengan Tailwind CSS.

---

## 🚀 Teknologi

- **Framework**: [Laravel 12](https://laravel.com)
- **Frontend**: [Livewire 3](https://livewire.laravel.com) & [Alpine.js](https://alpinejs.dev)
- **Styling**: [Tailwind CSS](https://tailwindcss.com)
- **Database**: MySQL
- **Build Tool**: Vite

---

## 📦 Instalasi

Ikuti langkah-langkah berikut untuk menjalankan project di komputer lokal Anda:

### 1. Clone Repository
```bash
git clone https://github.com/soleFelidae/DummyRPL_Kel3.git
cd DummyRPL_Kel3
```

### 2. Install Dependencies
Pastikan PHP dan Node.js sudah terinstall.
```bash
composer install
npm install
```

### 3. Konfigurasi Environment
Duplikat file `.env.example` menjadi `.env` dan sesuaikan konfigurasi database.
```bash
cp .env.example .env
php artisan key:generate
```
> **Catatan:** Edit file `.env` dan pastikan `DB_DATABASE`, `DB_USERNAME`, dan `DB_PASSWORD` sesuai dengan database lokal Anda.

### 4. Setup Database & Storage
Jalankan migrasi, seeder, dan link storage (PENTING untuk upload video).
```bash
php artisan migrate --seed
php artisan storage:link
```

### 5. Build Assets & Jalankan Server
Buka dua terminal berbeda:

**Terminal 1 (Build Assets):**
```bash
npm run dev
```

**Terminal 2 (Laravel Server):**
```bash
php artisan serve
```

Akses aplikasi di: `http://127.0.0.1:8000`

---

## 🔑 Akun Default

Gunakan akun berikut untuk masuk ke halaman Admin:

| Role | Email | Password | Login URL |
| :--- | :--- | :--- | :--- |
| **Admin** | `admin@service.com` | `admin` | `/login` |

---

## 📖 Cara Penggunaan

1.  **Login Admin**
    Masuk ke `/login` menggunakan akun default di atas.

2.  **Setup Tampilan**
    -   Buka menu **Pengaturan Tampilan** di dashboard.
    -   Upload video promosi atau masukkan link YouTube.
    -   Isi *Running Text* dan atur kecepatannya.
    -   Klik **Simpan**.

3.  **Kelola Antrian**
    -   Input data pelanggan (ID, Helpdesk, Durasi).
    -   Status awal otomatis `Waiting`.
    -   Ubah status ke `Progress` untuk memunculkan Countdown di layar depan.

4.  **Buka Display**
    -   Buka tab baru atau browser di monitor TV.
    -   Akses URL utama (`/`).
    -   Tekan `F11` untuk mode Fullscreen.

---

<div align="center">
  <small>Project ini merupakan <a href="https://github.com/hndko/app_antrianhelpdesk_laravel12">project orang</a>. repo ini dibuat untuk memenuhi tugas mk RPL</small>
</div>
