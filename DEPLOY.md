# 📚 Panduan Deploy Sistem Jadwal Kuliah

## 🚀 Cara 1: GitHub Pages (GRATIS & MUDAH)

### Langkah-langkah:

1. **Buat Akun GitHub** (jika belum punya)
   - Kunjungi: https://github.com
   - Sign up gratis

2. **Buat Repository Baru**
   - Klik tombol "New Repository"
   - Nama: `jadwal-kuliah` (atau nama lain)
   - Centang "Public"
   - Klik "Create Repository"

3. **Upload File via Web (Cara Mudah)**
   - Di halaman repository, klik "Add file" → "Upload files"
   - Drag & drop file `index.html` ke sana
   - Klik "Commit changes"

4. **Aktifkan GitHub Pages**
   - Masuk ke Settings repository
   - Scroll ke bagian "Pages"
   - Di "Source", pilih branch `main`
   - Klik "Save"
   - Tunggu 1-2 menit
   - URL aplikasi akan muncul: `https://username.github.io/jadwal-kuliah/`

✅ **Selesai!** Aplikasi bisa diakses oleh siapa saja via URL tersebut.

---

## 🌐 Cara 2: Netlify Drop (PALING CEPAT - 30 Detik!)

1. Buka: https://app.netlify.com/drop
2. Drag & drop file `index.html` ke halaman tersebut
3. Tunggu upload selesai
4. Netlify akan memberikan URL random seperti: `https://random-name.netlify.app`
5. Bisa diganti nama domain nanti di Settings

✅ **Instant deploy!** Tidak perlu daftar akun.

---

## 📁 Cara 3: Google Drive (Untuk Berbagi File)

**CATATAN:** Google Drive tidak bisa menjalankan HTML dengan baik. Hanya untuk berbagi file yang nanti didownload.

1. Upload `index.html` ke Google Drive
2. Klik kanan → "Get link" → "Anyone with the link"
3. Bagikan link ke orang lain
4. Mereka download dan buka di browser

⚠️ **Kekurangan:** Harus download dulu, tidak langsung buka di browser.

---

## 🖥️ Cara 4: Hosting Sendiri (Untuk yang Punya Server/VPS)

Jika punya hosting atau VPS:

1. Upload `index.html` via FTP/cPanel
2. Letakkan di folder `public_html` atau `www`
3. Akses via: `http://domainanda.com/index.html`

---

## 🔐 PENTING: Keamanan Password

**WAJIB GANTI PASSWORD** sebelum deploy!

Di file `index.html`, cari baris:

```javascript
if (password === "smaracatur") {
```

Ganti `"smaracatur"` dengan password baru:

```javascript
if (password === "passwordBaruAnda") {
```

⚠️ **CATATAN KEAMANAN:**
- Password ini tersimpan di client-side (bisa dilihat di source code)
- Untuk keamanan lebih baik, seharusnya pakai backend authentication
- Untuk internal use saja, ini sudah cukup

---

## 📱 Cara Akses Aplikasi

Setelah deploy, pengguna bisa:
1. Buka URL aplikasi di browser
2. Masukkan password
3. Gunakan sistem jadwal

Aplikasi akan menyimpan data di **localStorage browser** masing-masing pengguna.

⚠️ **PENTING:**
- Data disimpan lokal di browser masing-masing
- Jika beda komputer/browser, data tidak akan sinkron
- Untuk sinkronisasi data antar pengguna, butuh backend/database

---

## 🎯 Rekomendasi Saya

**Untuk pemula:** Gunakan **Netlify Drop** (Cara 2) - paling cepat!
**Untuk jangka panjang:** Gunakan **GitHub Pages** (Cara 1) - gratis selamanya & bisa update mudah

---

## 🔄 Cara Update Aplikasi

### GitHub Pages:
1. Edit file `index.html` di GitHub
2. Atau upload file baru (Replace)
3. Otomatis ter-update

### Netlify:
1. Drag & drop file baru lagi
2. Atau link dengan GitHub untuk auto-deploy

---

## ❓ Troubleshooting

**Q: Data hilang setelah refresh?**
A: Pastikan menggunakan HTTPS (bukan HTTP). LocalStorage tidak bekerja di HTTP.

**Q: Orang lain tidak bisa akses?**
A: Cek apakah repository/site sudah Public.

**Q: Password tidak bekerja?**
A: Pastikan sudah save dan re-upload file setelah ganti password.

---

**Butuh bantuan?** Tanya saya! 😊
