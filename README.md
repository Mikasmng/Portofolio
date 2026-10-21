# Portofolio Mika: Versi Statis (React + Vite)

Website portofolio publik milik Mika M.F. Simanullang.

**Tidak ada backend PHP, database MySQL, login admin, session, Axios, atau fitur CRUD.** Semua informasi dari `src/data.js`. Tidak ada foto pribadi, galeri dokumentasi, atau PDF yang dipublikasikan.

## Menjalankan di komputer (tanpa Laragon)

Pastikan sudah menginstal Node.js LTS, lalu buka terminal di folder ini.

```bash
npm install
npm run dev
```

Buka tautan `http://localhost:5173/` yang tampil di terminal.

## Mengedit konten

- Nama, biodata, URL media sosial, proyek, pengalaman, publikasi: `src/data.js`
- Desain dan font: `src/App.css`
- Tampilan/komponen: `src/App.jsx`

Konten pendidikan dan pengalaman tetap ditampilkan sebagai teks tanpa lampiran foto atau PDF.

**Catatan:** Karena tidak ada database, untuk mengubah konten website yang sudah online, edit `src/data.js`, commit/push perubahan ke GitHub lalu lakukan deploy ulang (biasanya otomatis jika terhubung ke Vercel).

## Deploy ke Vercel (disarankan)

1. Upload seluruh isi paket ini ke repository GitHub baru.
2. Masuk ke https://vercel.com/, login dengan GitHub, klik **Add New → Project**.
3. Pilih repository tersebut, lalu pengaturan:
   - Framework Preset: **Vite**
   - Root Directory: `/` jika isi folder `frontend` menjadi root repository, atau `frontend` jika upload folder induk.
   - Build Command: `npm run build`
   - Output Directory: `dist`
4. Klik **Deploy**.

Website statis ini tidak memerlukan konfigurasi database atau environment variables.

## Deploy ke GitHub Pages

Untuk deployment di GitHub Pages dengan Vite, gunakan GitHub Actions yang sudah disertakan (`.github/workflows/deploy.yml`).

1. Upload isi folder `frontend` sebagai root repository GitHub.
2. Buka **Settings → Pages** dan pilih **Build and deployment: GitHub Actions**.
3. Buka tab **Actions**, jalankan workflow *Deploy portfolio to GitHub Pages* bila belum berjalan otomatis.
4. Tunggu proses build/deploy selesai, lalu lihat URL di halaman Pages.

## Build lokal

```bash
npm run build
npm run preview
```

Hasil website statis berada di `dist/`.
