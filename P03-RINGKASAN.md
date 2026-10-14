# P03 — Bangun Portofolio Pribadi Modern (HTML & CSS)

_Ringkasan isi deck P03 (27 slide). Deck self-contained di `P03/index.html` + aset WebP otentik di `P03/img/`._

**Basis Materi:** Codebase portofolio 6 halaman otentik dari `asdos/praktikum` (Flask + HTML5 Semantik + CSS3 Tokens/Flexbox/Grid).  
**Konsep Pembelajaran:** Mahasiswa membedah arsitektur proyek portofolio siap pakai (Home, About, Skills, Projects, Blog, Contact), lalu mempersonalisasi seluruh data diri (nama, bio, foto, keahlian, proyek nyata, medsos, serta variasi tema warna).  
**Deadline tugas:** Rabu, 21 Oktober 2026, 23.59 WIB.

---

## Daftar Isi (27 Slide)

- 1. Bangun Portofolio Pribadi Modern *(Pembuka)*
- 2. Alur pertemuan hari ini *(Pembuka)*
- 3. Di akhir praktikum, kamu bisa *(Kelas)*
- 4. Nilai kamu dihitung dari mana *(Kelas)*
- 5. HTML5 Semantik: Bukan sekadar `<div>` *(Dasar teori)*
- 6. Design Tokens: Kendali warna di `:root` *(Dasar teori)*
- 7. Kapan Flexbox, kapan CSS Grid? *(Dasar teori)*
- 8. Jinja2: Memuat file statis dengan aman *(Dasar teori)*
- 9. Struktur proyek portofolio *(Praktik · Titik awal)*
- 10. Enam rute di `app.py` *(Praktik · Part 1 — backend)*
- 11. Home: Hero section & struktur awal *(Praktik · Part 2 — template)*
- 12. Aset gambar: Foto profil di static/images/ *(Praktik · Part 2 — aset)*
- 13. Pondasi `style.css`: Reset & Tokens *(Praktik · Part 3 — styling)*
- 14. Header melayang & menu aktif *(Praktik · Part 3 — layout)*
- 15. About: Biodata, statistik & riwayat *(Praktik · Part 4 — halaman 2)*
- 16. Skills: Progress bar berbasis CSS variable *(Praktik · Part 4 — halaman 3)*
- 17. Projects: Galeri karya dengan CSS Grid *(Praktik · Part 4 — halaman 4)*
- 18. Blog & Contact: Artikel dan kartu narahubung *(Praktik · Part 4 — halaman 5 & 6)*
- 19. Jalankan server, buka di browser *(Praktik · Part 5 — pengujian)*
- 20. Jelajahi 6 halaman portofolio *(Praktik · Part 5 — navsim)*
- 21. Ubah data Faiz menjadi datamu *(Praktik · Personalisasi — identitas)*
- 22. Eksplorasi tema warna portofolio *(Praktik · Personalisasi — tema)*
- 23. Sekarang giliran kamu *(Tugas)*
- 24. Ketentuan & pengumpulan *(Tugas)*
- 25. Kuis portofolio web modern *(Penutup)*
- 26. Kamu siap punya web portofolio sendiri *(Penutup)*
- 27. Selamat berkreasi! *(Penutup)*

---

## Capaian Pembelajaran

Setelah mengikuti praktikum P03, mahasiswa mampu:
1. Membangun dan menata halaman web multi-halaman dengan struktur **HTML5 Semantik** (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<form>`, `<footer>`).
2. Menerapkan sistem desain modern menggunakan **CSS3 Custom Properties (`:root`)**, efek glassmorphism (`backdrop-filter`), Flexbox, dan CSS Grid responsif.
3. Menghubungkan seluruh template dengan backend Flask menggunakan fungsi **`url_for('static', ...)`** yang bebas dari link patah.
4. Mempersonalisasi identitas, portofolio karya, dan tema warna web secara mandiri.

---

## Rubrik Penilaian

| Kriteria | Bobot | Indikator Utama |
|---|---|---|
| **Struktur HTML5 Semantik** | 25% | Menggunakan elemen semantik yang tepat di seluruh 6 file template, valid, tanpa elemen `<div>` berlebihan. |
| **CSS Styling & Responsif** | 30% | Memanfaatkan design tokens (`:root`), Flexbox, CSS Grid, tipografi bersih, dan responsif di mobile/desktop. |
| **Navigasi & 6 Rute Flask** | 20% | Semua 6 rute (`/`, `/about`, `/skills`, `/projects`, `/blog`, `/contact`) berjalan mulus dengan link aktif. |
| **Personalisasi Konten & Data Diri** | 25% | Seluruh data bawaan (nama Faiz, bio, kontak, foto, proyek) telah diganti dengan identitas otentik mahasiswa. |

---

## Fitur & Interaktivitas Deck

- **Explorer Elemen Semantik** (s5): Klik 6 elemen semantik utama untuk melihat peran arsitekturnya.
- **Explorer Design Tokens** (s6): Klik variabel token CSS (`--bg-primary`, `--accent`, `--glass-bg`, dll.) untuk memahami sistem desain terpusat.
- **Terminal OS-Aware** (s9 & s19): Pilihan tab Windows vs Linux/macOS, badge `venv aktif`, tombol salin command-only, dan output default tersembunyi ("tampilkan output").
- **Code Explorer `app.py`** (s10): Klik tiap baris rute Flask untuk membedah fungsinya satu per satu.
- **Tombol Salin Kode Penuh**: Tersedia di setiap kartu kode (`app.py`, reset CSS, dan seluruh cuplikan template HTML).
- **Galeri Screenshot Otentik & Lightbox Zoom** (s12, s14, s15, s16, s17, s18): Screenshot WebP resolusi tinggi dengan hint **"tekan gambar untuk memperbesar"**.
- **Simulator Navigasi (Navsim)** (s20): Jelajahi langsung 6 halaman portofolio dalam 1 viewport interaktif.
- **Live Theme Switcher** (s22): Uji coba pergantian skema warna (Indigo/Violet, Emerald Green, Sky Blue, Sunset Amber, Coral Rose) secara dinamis sebelum diterapkan ke `style.css`.
- **Kuis Interaktif** (s25): 5 soal evaluasi dengan umpan balik instan dan skor 5/5.
- **Ekspor Cetak PDF**: 1 slide = 1 halaman 16:9 pas (297×167 mm), tepat 27 halaman.

---

## Kunci Jawaban Kuis

1. **Tag semantik pembungkus menu tautan?** → `<nav>`
2. **Cara mendefinisikan CSS custom property global?** → `:root { --nama: nilai; }`
3. **Fungsi Jinja2 untuk memuat file statis secara andal?** → `url_for('static', filename='...')`
4. **Properti CSS untuk efek blur latar belakang kaca?** → `backdrop-filter: blur(...)`
5. **Tata letak terbaik untuk galeri kartu dua arah (baris dan kolom)?** → `CSS Grid (display: grid)`