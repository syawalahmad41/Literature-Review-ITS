# 📚 Literature Review Manager — Disertasi ITS

Aplikasi web untuk manajemen referensi literatur disertasi dengan ekstraksi otomatis metadata PDF menggunakan Claude AI.

---

## ✨ Fitur Utama

- **Login per pengguna** menggunakan nama dan email masing-masing
- **Upload PDF** artikel jurnal dengan ekstraksi metadata otomatis (Claude AI)
- **5 Lembar Kerja** persis sama dengan template Excel asli:
  - Progres 2.1 (Claim 1, 2, 3)
  - Research Gap and Positioning
  - Progres 1
- **Export Excel** (.xlsx) identik dengan format asli, nama file otomatis (nama penulis + tanggal)
- **Penyimpanan lokal** — data tersimpan di browser pengguna

---

## 🚀 Cara Deploy

### Opsi 1: Netlify (Drag & Drop)
1. Buka [netlify.com](https://netlify.com) dan login
2. Pilih **"Add new site" → "Deploy manually"**
3. Drag folder `literature-review-app/` ke area upload
4. Situs langsung aktif! Bagikan link ke semua pengguna

### Opsi 2: Netlify via GitHub
1. Push folder ini ke repository GitHub
2. Di Netlify, pilih **"Import from Git"**
3. Pilih repo, build settings:
   - **Publish directory:** `.` (atau nama folder)
4. Deploy otomatis setiap push

### Opsi 3: Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Di folder `literature-review-app/`, jalankan: `vercel`
3. Ikuti instruksi — situs live dalam hitungan detik

### Opsi 4: GitHub Pages
1. Push ke GitHub repository
2. Settings → Pages → Deploy from branch `main`
3. File `index.html` harus di root atau folder docs

---

## 🔑 API Key Anthropic

Setiap pengguna memasukkan API key Anthropic pribadi mereka saat login:
1. Buat akun di [console.anthropic.com](https://console.anthropic.com)
2. Generate API key di bagian API Keys
3. Masukkan key saat login di aplikasi
4. Key tersimpan hanya di browser lokal (localStorage)

---

## 📊 Struktur Data Excel Output

| Sheet | Kolom |
|-------|-------|
| Progres 2.1 (Claim 1/2/3) | No, Jurnal, Publisher, Quartile, Penulis, Judul, Tahun, Key Result, DOI, Persamaan, Kelebihan, Kekurangan, Research Gap |
| Research Gap & Positioning | No, Aspek, Analisis Gap (×3 claims) |
| Progres 1 | No, Jurnal, Publisher, Quartile, Peneliti, Judul, Tahun, Latar Belakang, Metode, Key Results, DOI |

---

## 🛠 Teknologi

- **Frontend:** HTML5, CSS3, Vanilla JavaScript (tanpa framework)
- **AI Extraction:** Anthropic Claude API (`claude-sonnet-4-20250514`)
- **Excel Export:** SheetJS (xlsx) via CDN
- **Storage:** Browser localStorage (tidak memerlukan server)
- **Font:** Google Fonts (Playfair Display, Source Serif 4, JetBrains Mono)

---

## 📁 File Structure

```
literature-review-app/
├── index.html              # Aplikasi web lengkap
├── netlify.toml            # Konfigurasi Netlify
├── vercel.json             # Konfigurasi Vercel
├── README.md               # Dokumentasi ini
└── Literature_Review_Template.xlsx  # Template Excel referensi
```

---

*Dibuat untuk Institut Teknologi Sepuluh Nopember (ITS) Surabaya · Program Doktor*
