# 🍏 FruitStock Inventory & POS

FruitStock adalah sistem manajemen inventaris dan Point of Sale (POS) yang dirancang khusus untuk mempermudah pengelolaan stok buah-buahan dan transaksi penjualan harian. Aplikasi ini dikembangkan untuk memenuhi tugas UAS mata kuliah Pemrograman Web 2.

## 🌟 Fitur Utama
* **Dashboard Interaktif:** Ringkasan informatif yang mencakup total stok, item hampir habis, peringatan stok mendekati busuk, dan total penjualan hari ini.
* **Manajemen Master Data:** Pengelolaan basis data inti yang terstruktur, meliputi Master Buah, Kategori, Gudang, dan Supplier.
* **Manajemen Stok & Peringatan Kritis:** Pemantauan stok secara *real-time* dengan peringatan otomatis untuk stok yang hampir habis atau mendekati masa kadaluarsa.
* **Point of Sale (POS) / Kasir:** Sistem kasir yang intuitif dan terintegrasi langsung dengan pemotongan stok gudang secara otomatis saat transaksi.
* **QC & Retur Barang:** Modul khusus untuk pengecekan kualitas dan pencatatan pengembalian buah yang rusak atau tidak layak jual.
* **Laporan Penjualan:** Rekapitulasi riwayat transaksi harian untuk membantu pengambilan keputusan.
* **Role-Based Access Control & Profil:** Keamanan sistem dengan hak akses terpisah untuk Admin, Petugas Gudang, dan Kasir, serta fitur pengaturan profil pengguna.

## 🛠️ Tech Stack
* **Framework:** Laravel 13
* **Database:** SQLite
* **Frontend:** Blade Templates, Tailwind CSS/Bootstrap
* **Language:** PHP

## 🚀 Panduan Instalasi (Mode Lokal SQLite)
Pastikan kamu sudah menginstal Composer dan PHP 8.2+. Ikuti langkah berikut agar aplikasi bisa berjalan dalam satu kali coba:

**1. Clone Repository & Masuk Folder**
> git clone https://github.com/AdiSingho/FruitStock_UAS
> cd FruitStock_UAS

**2. Install Dependensi**
> composer install
> npm install && npm run build

**3. Setup Environment**
> cp .env.example .env
> php artisan key:generate

*(PENTING: Buka file `.env`, lalu pastikan konfigurasi database diubah menjadi `DB_CONNECTION=sqlite`)*

**4. Migrasi Database**
> php artisan migrate:fresh --seed

**5. Jalankan Aplikasi**
> php artisan serve

*(Buka terminal baru lalu jalankan `npm run dev` untuk merender tampilan. Setelah itu akses http://127.0.0.1:8000 di browser).*

## 👥 Tim Pengembang
* Singgih Adi Nugroho
* Plorentina Fidelis Purba
* Sisilia Irna Lakapu

## 🔐 Default Credentials
Kamu bisa menggunakan akun berikut untuk menguji fitur berdasarkan role yang berbeda:
* **Admin:** `admin@fruitstock.com` | Password: `password123`
* **Petugas Gudang:** `gudang@fruitstock.com` | Password: `password123`
* **Kasir:** `kasir@fruitstock.com` | Password: `password123`