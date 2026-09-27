# Praktikum Pemrograman Web — Deck Interaktif

Deck presentasi interaktif untuk praktikum Pemrograman Web. Satu folder per pertemuan, dibuka langsung di browser — tanpa build, tanpa dependency.

## Struktur

```
web-perkuliahan/
├── index.html      # Hub — pintu masuk semua pertemuan
├── vercel.json     # Konfigurasi deploy (static, cleanUrls)
├── P01/
│   ├── index.html  # Deck pertemuan 01 (23 slide interaktif)
│   └── img/        # Screenshot modul per step
├── P02/            # Pertemuan berikutnya — copy pola P01
└── ...
```

## Deploy ke Vercel

Situs ini 100% statik — Vercel mendeteksinya otomatis sebagai static project, tanpa build command dan tanpa install dependency.

1. Push repo ini ke GitHub (repo root = folder `web-perkuliahan`):

```bash
git init
git add .
git commit -m "P01 — deck interaktif pengenalan pemrograman web & python"
git branch -M main
git remote add origin https://github.com/USERNAME/web-perkuliahan.git
git push -u origin main
```

2. Di Vercel: **Add New → Project → Import** repo-nya.
   - Framework Preset: **Other** (terdeteksi otomatis)
   - Root Directory: `/` (default — biarkan)
   - Build Command & Output Directory: kosongkan
3. Deploy. URL jadi `https://<nama-proyek>.vercel.app/` → hub → `/P01/`.

Kalau lo push repo yang lebih besar (misal seluruh folder `pemweb` yang ada modulnya), set **Root Directory = `web-perkuliahan`** saat import di Vercel.

## Nambah pertemuan baru

1. Copy folder `P01/` jadi `P02/`, ganti isi slide-nya.
2. Tambah kartu pertemuan baru di `index.html` (copy blok `a.meet`).

## Catatan teknis

- Font (Unbounded, IBM Plex) dan icon (Lucide) dimuat via CDN — butuh internet.
- Semua interaksi (terminal simulator, HTTP simulator, quiz, timer) berjalan client-side, vanilla JS.
- `prefers-reduced-motion` dihormati — animasi mati otomatis untuk yang butuh.
