# 🎬 TikTok Anti-Detection & Lossless Video Modifier (Tiktok Patcher)

Aplikasi otomatisasi untuk memodifikasi video MP4 agar **lolos dari sistem deteksi konten duplikat / re-upload / copyright TikTok, Instagram Reels, dan YouTube Shorts**.

Program ini bekerja secara instan tanpa me-render ulang video sehingga kualitas gambar tetap 100% utuh (*zero quality loss*) dan proses selesai dalam waktu kurang dari 1 detik.

---

## ⬇️ Download Rilis Terbaru

Unduh aplikasi versi standalone siap pakai (tanpa perlu instalasi Python atau software tambahan apa pun):

👉 **[Download Tiktok Patcher v1.0.0 (Windows Standalone)](https://github.com/wahyush04/Tiktok-Patcher/releases/tag/v1.0.0)**

---

## 🌟 Fitur Utama

- ⚡ **Super Cepat & Lossless (Zero Quality Loss)**: Menggunakan teknik *stream copy* langsung tanpa render ulang piksel (*no re-encoding*). Video berdurasi 1 menit beresolusi 1080p atau 4K selesai dalam waktu **0,1 – 0,3 detik**.
- 🔍 **Dukungan Penuh Resolusi 4K & File Besar**: Mendukung video 1080p, 2K, 4K (3840×2160 / 2160×3840 9:16), hingga 8K. Mendukung otomatisasi tabel offset 64-bit (`co64`) untuk file video berukuran besar (> 4 GB).
- 🔄 **Perubahan Sidik Jari File Total**: Mengubah nilai hash kriptografi (MD5 & SHA-256) serta struktur kontainer file secara otomatis sehingga terdeteksi sebagai file video baru.
- 🧹 **Pembersihan Jejak Editor Total**: Menghapus metadata editor (Adobe Premiere Pro XMP, CapCut traces, timecode, dan riwayat file proyek asli).
- 📂 **Manajemen Folder Dinamis**: Cukup masukkan video ke folder `input/`, dan file hasil modifikasi otomatis tersimpan rapi di folder `output/`.
- 🎛️ **Menu Interaktif & Batch Mode**: Tampilan antarmuka terminal yang ramah pengguna, mendukung pemilihan video satuan maupun pemrosesan massal semua video sekaligus.
- 🚀 **Portable & Siap Pakai**: Berupa file executable tunggal (`TiktokPatcher.exe`), langsung berjalan di Windows tanpa perlu instalasi dependency atau setting environment.

---

## 📁 Struktur Direktori

Setelah mengekstrak file rilis ZIP, struktur folder adalah sebagai berikut:

```text
TiktokPatcher/
├── input/                  <--- Tempatkan file video sumber (.mp4, .mov, dll.) di sini
├── output/                 <--- Hasil video termodifikasi otomatis tersimpan di sini
├── TiktokPatcher.exe       <--- Aplikasi utama siap pakai
└── README.md               <--- Panduan penggunaan
```

---

## 💻 Panduan Penggunaan

Aplikasi ini sangat mudah digunakan dan siap pakai tanpa memerlukan software tambahan apa pun di komputer Anda.

### 1. Mode Interaktif (Klik Ganda)
1. Ekstrak file **`TiktokPatcher-v1.0.0-Windows.zip`**.
2. Masukkan file video Anda (`.mp4`, `.mov`, dll.) ke dalam folder **`input`**.
3. Klik 2× file **`TiktokPatcher.exe`** (atau jalankan via terminal/PowerShell).
4. Menu interaktif akan muncul menampilkan daftar video yang ada di folder `input`:
   ```text
   ====================================================================
       TIKTOK ANTI-DETECTION TOOL - EXACT TIKQUICK ENGINE v19
   ====================================================================
   Status Lisensi: AKTIF (Berlaku s/d 17-09-2026 23:59:59)
   Sisa Waktu    : 7 hari 16 jam tersisa
   Folder Input  : C:\...\input
   Folder Output : C:\...\output
   --------------------------------------------------------------------
   Ditemukan 2 video di folder 'input/':

     [1] video1.mp4                     (48.74 MB)
     [2] video2.mp4                     (57.89 MB)
   --------------------------------------------------------------------
     [A] Proses SEMUA video sekaligus (Batch Mode)
     [R] Refresh daftar video
     [0] Keluar
   ====================================================================
   Pilih nomor video yang ingin dimodifikasi (atau A/0): 
   ```
5. Pilih nomor video yang ingin diproses, atau ketik **`A`** untuk memproses seluruh video sekaligus.
6. Pilih mode modifikasi:
   - `[1] TIKQUICK (Default)`: Mode standar modifikasi kontainer TikQuick v19.
   - `[2] CLEAN`: Mode struktur kontainer bersih (*ghost audio track*).
7. Selesai! File hasil modifikasi langsung tersedia di folder **`output`**.

### 2. Mode Otomatis / Batch CLI (Opsional)
Bagi pengguna yang ingin menjalankan aplikasi via skrip otomatisasi atau command line tanpa dialog menu:

```powershell
# Memproses semua video di folder input dengan mode TikQuick
.\TiktokPatcher.exe --all --mode tikquick

# Memproses semua video di folder input dengan mode Clean
.\TiktokPatcher.exe --all --mode clean
```

---

## 📊 Hasil Pengujian & Performa

| Parameter | Sebelum Modifikasi | Setelah Modifikasi | Keterangan |
| :--- | :--- | :--- | :--- |
| **Kualitas Video** | 100% Asli | 100% Asli | Tidak ada kompresi ulang piksel (*bit-for-bit*) |
| **Resolusi** | 1080p / 4K / 8K | 1080p / 4K / 8K | Resolusi dan framerate (60fps) tetap terjaga |
| **Hash MD5 & SHA-256** | Nilai Asli | **Berubah Total** | Terdeteksi sebagai konten baru |
| **Jejak Metadata Editor** | Terekam | **Bersih** | Menghapus jejak Adobe Premiere / editor |
| **Kecepatan Proses** | - | **~0,15 detik / video** | Sangat cepat dan hemat daya |

---

## 💡 Tips Penggunaan untuk Konten TikTok

1. **Resolusi Rekomendasi**: Gunakan resolusi 1080p (1080×1920) atau 4K (2160×3840) pada 60fps untuk ketajaman maksimal.
2. **Akun & Koneksi**: Gunakan akun yang dalam status normal dan pastikan tidak terkena batasan harian upload.

---

## ⚖️ Disclaimer

Aplikasi ini ditujukan untuk tujuan edukasi, manajemen arsip media pribadi, dan optimasi format kontainer multimedia. Pengguna bertanggung jawab penuh atas seluruh materi dan konten yang diunggah ke platform media sosial masing-masing.
