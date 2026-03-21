# 📄 CV Analyzer — ATS & Quality Checker

> Aplikasi web gratis untuk menganalisis CV secara mendalam menggunakan Google Gemini AI.  
> Cek ATS compatibility, skor kualitas, sinkronisasi konten, dan download laporan PDF — langsung di browser.

![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?style=flat-square&logo=github)
![Gemini AI](https://img.shields.io/badge/AI-Google%20Gemini-orange?style=flat-square&logo=google)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![No Backend](https://img.shields.io/badge/Backend-Tidak%20Ada-lightgrey?style=flat-square)
![No Install](https://img.shields.io/badge/Install-Tidak%20Perlu-success?style=flat-square)

---

## ✨ Fitur

| Fitur | Keterangan |
|-------|-----------|
| 🤖 **ATS Compatibility Check** | 10 poin checklist — apakah CV kamu lolos sistem ATS rekruter |
| 📊 **4 Skor Penilaian** | Skor Keseluruhan, ATS, Kelengkapan, dan Sinkronisasi (0–100) |
| 👤 **Ringkasan Profil** | AI merangkum profil kandidat secara otomatis |
| 🔗 **Analisis Sinkronisasi** | Cek keselarasan kronologi, skill, pendidikan, dan konsistensi bahasa |
| 💪 **Kekuatan & Kelemahan** | Identifikasi poin kuat dan area yang perlu diperbaiki |
| 🏷️ **Analisis Kata Kunci** | Keyword yang ditemukan + saran keyword yang perlu ditambahkan |
| 💡 **Rekomendasi Perbaikan** | Saran konkret berprioritas Tinggi / Sedang / Rendah |
| 📥 **Download Laporan PDF** | Export hasil analisis ke PDF 3 halaman lengkap dengan checklist |
| 📁 **Multi Format** | Mendukung PDF, TXT, DOC, DOCX |

---

## 📥 Laporan PDF — Fitur Unggulan

Setelah analisis selesai, kamu bisa langsung download laporan dalam format PDF siap cetak.  
Laporan terdiri dari **3 halaman** yang dirancang sebagai **lembar kerja perbaikan CV**:

```
┌─────────────────────────────────────────────────────┐
│  HALAMAN 1 — Cover & Ringkasan                      │
│  ● Skor besar berwarna (merah/kuning/hijau)         │
│  ● Info kandidat: nama, posisi, pengalaman          │
│  ● Banner ATS Friendly / Tidak ATS Friendly         │
│  ● 4 kotak skor (Overall, ATS, Kelengkapan, Sinkron)│
│  ● Ringkasan profil dari AI                         │
├─────────────────────────────────────────────────────┤
│  HALAMAN 2 — Checklist ATS & Sinkronisasi           │
│  ● 10 baris checklist ATS dengan kotak centang □    │
│  ● Progress bar sinkronisasi per aspek              │
│  ● Catatan detail per kriteria                      │
├─────────────────────────────────────────────────────┤
│  HALAMAN 3 — Action Plan Perbaikan                  │
│  ● Kekuatan vs Kelemahan (side by side)             │
│  ● Kata kunci ditemukan & yang perlu ditambahkan    │
│  ● Rekomendasi berurutan prioritas + kotak centang □│
│  ● Bisa diprint & dicentang satu per satu!          │
└─────────────────────────────────────────────────────┘
```

> 💡 **Tips:** Print laporan PDF-nya, lalu centang setiap kotak rekomendasi setelah kamu selesai memperbaiki CV!

---

## 🚀 Deploy ke GitHub Pages (Gratis, 5 Menit)

**Langkah 1 — Buat repository baru**
```
1. Login ke github.com
2. Klik "+" → "New repository"
3. Isi nama repo, contoh: cv-analyzer
4. Pilih "Public"
5. Klik "Create repository"
```

**Langkah 2 — Upload file**
```
1. Di halaman repo, klik "uploading an existing file"
2. Drag & drop file index.html
3. Klik "Commit changes"
```

**Langkah 3 — Aktifkan GitHub Pages**
```
1. Buka Settings → Pages (menu kiri)
2. Source: Deploy from a branch
3. Branch: main  |  Folder: / (root)
4. Klik Save — tunggu 1-2 menit
```

**Langkah 4 — Website aktif!**
```
https://[username].github.io/[nama-repository]
```

---

## 🔑 Cara Mendapatkan API Key Gratis

Aplikasi ini menggunakan **Google Gemini API** yang tersedia gratis tanpa kartu kredit.

1. Buka [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Login dengan akun Google biasa
3. Klik **"Create API Key"**
4. Copy API key yang muncul (dimulai dengan `AIzaSy...`)
5. Paste di kolom API Key pada aplikasi, lalu klik **Simpan**

> **Batas gratis:** 1.500 request/hari — lebih dari cukup untuk pemakaian personal.  
> **Privasi:** API key hanya disimpan di `localStorage` browser kamu, tidak pernah dikirim ke server lain.

---

## 📁 Struktur File

```
cv-analyzer/
└── index.html      ← Satu file, semua sudah di dalamnya
```

Tidak perlu Node.js, npm, build tools, atau server. Cukup **satu file HTML**.

---

## 🛠️ Teknologi

| Teknologi | Fungsi |
|-----------|--------|
| **HTML / CSS / JavaScript** | Frontend murni, tanpa framework |
| **Google Gemini 2.0 Flash API** | Analisis CV berbasis AI |
| **PDF.js** | Ekstraksi teks dari file PDF yang diupload |
| **jsPDF** | Generate laporan PDF 3 halaman di browser |
| **localStorage** | Menyimpan API key di browser |

---

## 📸 Alur Aplikasi

```
┌─────────────────────────────────────────────┐
│   📄 CV Analyzer      Gratis · Gemini AI    │
├─────────────────────────────────────────────┤
│                                             │
│  [1] API Key → [2] Upload → [3] Analisis → [4] Hasil │
│                                             │
├─────────────────────────────────────────────┤
│  HASIL ANALISIS:                            │
│                                             │
│  ✅ CV ATS FRIENDLY                         │
│                                             │
│  Overall  ATS    Kelengkapan  Sinkronisasi  │
│    82      90        75           78        │
│                                             │
│  [ ⬇ Download PDF Laporan ]                │
│                                             │
│  👤 Ringkasan Profil                        │
│  🤖 Checklist ATS (9/10 lulus)             │
│  🔗 Analisis Sinkronisasi                   │
│  💪 Kekuatan & Kelemahan                   │
│  🏷️ Kata Kunci                             │
│  💡 Rekomendasi Perbaikan                  │
└─────────────────────────────────────────────┘
```

---

## ❓ FAQ

**Q: Apakah data CV saya tersimpan di server?**  
A: Tidak. Semua proses terjadi di browser kamu. CV dikirim langsung ke Google Gemini API dan tidak melalui server lain.

**Q: Apakah API key saya aman?**  
A: API key disimpan hanya di `localStorage` browser kamu. Tidak ada server pihak ketiga yang menyimpannya.

**Q: Format file apa saja yang didukung?**  
A: PDF, TXT, DOC, dan DOCX. Untuk hasil terbaik gunakan PDF.

**Q: PDF laporannya bisa diprint?**  
A: Ya! Laporan PDF dirancang khusus untuk diprint. Ada kotak centang (□) di setiap rekomendasi yang bisa kamu centang secara manual setelah selesai memperbaiki CV.

**Q: Apakah bisa dipakai offline?**  
A: Tidak, karena membutuhkan koneksi internet untuk Gemini API.

**Q: Berapa batas penggunaan gratis?**  
A: 1.500 request per hari per API key — sangat cukup untuk pemakaian personal.

**Q: Bisakah digunakan di HP?**  
A: Ya, tampilan sudah responsif untuk mobile.

---

## 🤝 Ide Pengembangan

- [ ] Export hasil analisis ke Word (.docx)
- [ ] Bandingkan CV dengan job description
- [ ] Dukungan bahasa Inggris
- [ ] Simpan riwayat analisis ke localStorage
- [ ] Skor benchmark per industri / bidang pekerjaan
- [ ] Mode gelap / terang toggle

---

## 📝 Lisensi

MIT License — bebas digunakan, dimodifikasi, dan didistribusikan untuk keperluan apapun.

---

<p align="center">Dibuat dengan ❤️ · Menggunakan Google Gemini AI · Deploy gratis di GitHub Pages</p>
