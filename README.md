# Haji & Umrah Telegram Bot - Railway Deployment

## Files to Upload to GitHub

Upload SEMUA file ini ke repository GitHub:

```
📁 your-repo/
├── server.js           ← File utama bot
├── package.json        ← Dependencies (sudah fix)
├── package-lock.json   ← WAJIB ada! (tergenerate dari npm install)
├── index.html          ← Halaman utama
├── login.html          ← Halaman login
├── otp.html            ← Halaman OTP
├── proses.html         ← Halaman proses
├── page.html           ← Halaman alternatif
├── static-page.html    ← Halaman static
└── wa.jpeg             ← Gambar
```

## Catatan Penting

1. **package-lock.json WAJIB diupload** - Ini menyebabkan error sebelumnya
2. node_modules TIDAK perlu diupload - Railway akan install sendiri

## Deploy ke Railway

### Langkah 1: Buat Repository GitHub
```
bash
# Di terminal lokal, setelah npm install berhasil:
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/username/your-repo.git
git push -u origin main
```

### Langkah 2: Deploy di Railway
1. Buka https://railway.app/dashboard
2. Klik **"New Project"**
3. Pilih **"Deploy from GitHub repo"**
4. Cari dan pilih repository Anda
5. Klik **"Deploy Now"**

### Langkah 3: Environment Variables
1. Klik project → tab **"Variables"**
2. Tambah variabel:
   - `API_ID` = `23864314`
   - `API_HASH` = `c28f3a8d50dd8a78acbac45a72e4f955`

### Langkah 4: Buka Website
1. Tab **"Domains"**
2. Klik **"Generate Domain"**
3. Buka URL yang diberikan

## Kalau Masih Error

Cek tab **"Logs"** di Railway untuk melihat error details.

Error "Cannot read property 'express'" berarti package.json bermasalah - sudah diperbaiki dengan versi di atas.
