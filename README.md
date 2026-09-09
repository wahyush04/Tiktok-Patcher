# 🎬 TikTok Anti-Detection & Lossless Video Modifier (Tiktok Patcher)

Aplikasi otomatisasi untuk memodifikasi video MP4 agar **lolos dari sistem deteksi konten duplikat / re-upload / copyright TikTok, Instagram Reels, dan YouTube Shorts**.

Program ini bekerja secara instan tanpa me-render ulang video sehingga kualitas gambar tetap 100% utuh (*zero quality loss*) dan proses selesai dalam waktu kurang dari 1 detik.

---

## 🌟 Fitur Utama

- ⚡ **Super Cepat & Lossless (Zero Quality Loss)**: Menggunakan teknik *stream copy* langsung tanpa render ulang piksel (*no re-encoding*). Video berdurasi 1 menit beresolusi 1080p atau 4K selesai dalam waktu **0,1 – 0,3 detik**.
- 🔍 **Dukungan Penuh Resolusi 4K & File Besar**: Mendukung video 1080p, 2K, 4K (3840×2160 / 2160×3840 9:16), hingga 8K. Mendukung otomatisasi tabel offset 64-bit (`co64`) untuk file video berukuran besar (> 4 GB).
- 🔄 **Perubahan Sidik Jari File Total**: Mengubah nilai hash kriptografi (MD5 & SHA-256) serta struktur kontainer file secara otomatis sehingga terdeteksi sebagai file video baru.
- 🧹 **Pembersihan Jejak Editor Total**: Menghapus metadata editor (Adobe Premiere Pro XMP, CapCut traces, timecode, dan riwayat file proyek asli).
- 📂 **Manajemen Folder Dinamis**: Cukup masukkan video ke folder `input/`, dan file hasil modifikasi otomatis tersimpan rapi di folder `output/`.
- 🎛️ **Menu Interaktif & Batch Mode**: Tampilan antarmuka terminal yang ramah pengguna, mendukung pemilihan video satuan maupun pemrosesan massal semua video sekaligus.

---

## 📁 Struktur Direktori

```text
tiktok-video-modifier/
├── input/                  <--- Tempatkan file video sumber (.mp4, .mov, dll.) di sini
├── output/                 <--- Hasil video termodifikasi otomatis tersimpan di sini
├── TiktokPatcher.exe       <--- Aplikasi siap pakai (Windows Standalone, tanpa perlu instal Python)
├── modify_video.py         <--- Skrip Python utama
├── requirements.txt        <--- Daftar dependensi modul Python (jika menggunakan skrip .py)
└── README.md               <--- Panduan penggunaan
```

---

## 💻 Panduan Penggunaan

Terdapat dua cara untuk menjalankan aplikasi ini:

---

### Cara 1: Menggunakan Aplikasi Siap Pakai (`TiktokPatcher.exe`) — Direkomendasikan
*Metode ini tidak memerlukan instalasi Python atau software tambahan apa pun di komputer Anda.*

1. Pastikan folder **`input`** dan **`output`** berada di sebelah file **`TiktokPatcher.exe`**.
2. Masukkan file video Anda (`.mp4`, `.mov`, dll.) ke dalam folder **`input`**.
3. Klik 2× file **`TiktokPatcher.exe`** (atau jalankan via terminal/PowerShell).
4. Menu interaktif akan muncul. Pilih nomor video yang ingin diproses, atau tekan **`A`** untuk memproses semua video sekaligus.
5. Selesai! File hasil modifikasi langsung tersedia di folder **`output`**.

---

### Cara 2: Menggunakan Skrip Python (`modify_video.py`)

#### 1. Persyaratan & Instalasi Dependensi
Pastikan komputer Anda telah terinstal **Python 3.10+**. Jalankan perintah berikut di terminal:

```powershell
pip install -r requirements.txt
```

#### 2. Menjalankan Menu Interaktif
1. Masukkan video ke dalam folder `input/`.
2. Jalankan perintah:
   ```powershell
   python modify_video.py
   ```
3. Pilih nomor video yang ingin dimodifikasi dari daftar menu yang tampil:
   ```text
   ====================================================================
       TIKTOK ANTI-DETECTION TOOL - EXACT TIKQUICK ENGINE v19
   ====================================================================
   Folder Input  : C:\Users\...\input
   Folder Output : C:\Users\...\output
   --------------------------------------------------------------------
   Ditemukan 2 video di folder 'input/':

     [1] video1.mp4                     (48.74 MB)
     [2] video2.mp4                     (57.89 MB)
   --------------------------------------------------------------------
     [A] Proses SEMUA video sekaligus (Batch Mode)
     [R] Refresh daftar video
     [0] Keluar
   ====================================================================
   Pilih nomor video yang ingin dimodifikasi (atau A/0): 1
   ```
4. Pilih mode:
   - `[1] TIKQUICK (Default)`: Mode standar modifikasi kontainer.
   - `[2] CLEAN`: Mode bersih tanpa teks watermark bot.
5. Tekan Enter. File hasil akan langsung tersedia di folder `output/`.

#### 3. Menjalankan Otomatis / Batch Mode (Tanpa Dialog Menu)
Untuk memproses seluruh video di folder `input/` secara otomatis tanpa membuka menu interaktif:

```powershell
# Mode Default
python modify_video.py --all --mode tikquick

# Mode Clean
python modify_video.py --all --mode clean
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
2. **Audio Tambahan**: Disarankan menambahkan atau mengganti musik latar resmi dari aplikasi TikTok saat proses unggah untuk membantu distribusi video.
3. **Akun & Koneksi**: Gunakan akun yang dalam status normal dan pastikan tidak terkena batasan harian upload.

---

## ⚖️ Disclaimer

Aplikasi ini ditujukan untuk tujuan edukasi, manajemen arsip media pribadi, dan optimasi format kontainer multimedia. Pengguna bertanggung jawab penuh atas seluruh materi dan konten yang diunggah ke platform media sosial masing-masing.
