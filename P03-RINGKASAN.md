# P03 — Komponen Dasar UI (HTML & CSS)

_Ringkasan isi deck P03 (27 slide). Deck self-contained di `P03/index.html` + aset WebP di `P03/img/`._

**Urutan bagian:** Pembuka → Kelas → Dasar teori → Praktik Part 1–4 + Bonus → Tugas → Penutup.
**Deadline tugas:** Rabu, 21 Oktober 2026, 23.59.

## Daftar isi

- 1. Komponen dasar UI — kenalan sama HTML & CSS *(Pembuka)*
- 2. Alur pertemuan hari ini *(Pembuka)*
- 3. Di akhir praktikum, kamu bisa *(Kelas)*
- 4. Nilai kamu dihitung dari mana *(Kelas)*
- 5. HTML: kerangka halaman web *(Dasar teori)*
- 6. CSS: memberi gaya pada struktur *(Dasar teori)*
- 7. Tiga cara memasang CSS *(Dasar teori)*
- 8. Kerangka yang sama di tiap halaman *(Dasar teori)*
- 9. Ingat proyek P02? Sekarang kita isi *(Praktik · Part 1)*
- 10. Buat file `templates/index.html` *(Praktik · Part 1)*
- 11. Menu yang menghubungkan halaman *(Praktik · Part 1)*
- 12. Sambungkan `style.css` ke HTML *(Praktik · Part 1)*
- 13. Buat file `static/css/style.css` *(Praktik · Part 2)*
- 14. Lihat bedanya CSS secara langsung *(Praktik · Part 2)*
- 15. Tambah route di `app.py` *(Praktik · Part 3)*
- 16. Dari URL ke halaman *(Praktik · Part 3)*
- 17. Jalankan server, buka di browser *(Praktik · Part 3)*
- 18. Halaman Home sudah berwarna *(Praktik · Part 3)*
- 19. Tambah halaman `templates/about.html` *(Praktik · Part 4)*
- 20. Tambah halaman `templates/contact.html` *(Praktik · Part 4)*
- 21. Klik menu, pindah halaman *(Praktik · Part 4)*
- 22. Halaman tadi bisa jadi seperti ini *(Praktik · Bonus)*
- 23. Sekarang giliran kamu *(Tugas)*
- 24. Ketentuan & pengumpulan *(Tugas)*
- 25. Kuis kilat — lima soal *(Penutup)*
- 26. Kamu baru saja membangun UI pertamamu *(Penutup)*
- 27. Tampilan web pertamamu sudah jadi *(Penutup)*
- Lampiran — Kuis (5 soal)

---

## Materi & capaian

Setelah mengikuti praktikum, mahasiswa mampu: (1) membangun tampilan antarmuka dengan **HTML5**, (2) memakai **CSS3** untuk styling dasar, (3) menghubungkan **file CSS eksternal** ke HTML.

- **Teori:** elemen HTML dasar (`html`, `head`, `body`, `h1`–`h6`, `p`, `a`, `img`, `div`, `ul`/`ol`), anatomi aturan CSS (selector + property), tiga cara memasang CSS (inline / internal / eksternal), kerangka semantic `header → main → footer`.
- **Praktik:** `templates/index.html`, `static/css/style.css`, tambah 3 route di `app.py`, lalu `templates/about.html` & `templates/contact.html`.
- **Tugas (30 menit):** halaman profil pribadi min. 3 halaman (Home/About/Contact), CSS eksternal, header + nav + main + footer, memakai heading/paragraf/list/link/image. Kumpul zip ke LMS.

## Rubrik (dari modul 003)

| Kriteria | Bobot | Excellent | Good | Fair | Poor |
|---|---|---|---|---|---|
| Struktur HTML | 25% | Lengkap, semantic | Lengkap | Kurang lengkap | Tidak ada |
| CSS Styling | 30% | Rapi, konsisten | Cukup rapi | Kurang rapi | Tidak ada |
| Navigasi | 20% | Semua halaman terhubung | 2 halaman | 1 halaman | Tidak ada |
| Konten | 25% | Lengkap dan informatif | Cukup lengkap | Kurang lengkap | Tidak ada |

## Interaksi / widget

- **Explorer elemen HTML** (s5) — klik 9 elemen → penjelasan.
- **Explorer aturan CSS** (s6) — klik 4 aturan (`body`, `header`, `h2`, `a:hover`) → penjelasan.
- **Tiga cara memasang CSS** (s7) — kartu inline/internal/eksternal.
- **url_for: tulis vs browser** (s12) — toggle menampilkan sintak Jinja ↔ hasil `/static/css/style.css`.
- **CSS playground** (s14) — tombol "dengan CSS / tanpa CSS" + 4 swatch warna header.
- **Code explorer `app.py`** (s15) — klik baris → penjelasan.
- **Peta route → template** (s16) — klik `/`, `/about`, `/contact`.
- **Terminal typewriter OS-aware** (s9 `dir`/`ls`, s17 `python app.py`), badge `venv aktif`/`shell biasa`, output default tersembunyi, tombol **salin perintah** (command-only).
- **Salin isi file** (index.html, style.css, app.py, about.html, contact.html) + **salin baris `<link>`**.
- **Simulator navigasi** (s21) — klik Home/About/Contact → ganti tangkapan hasil render.
- **Checklist tugas + hitung mundur** (s23), **kuis 5 soal** (s25), **lightbox zoom** di tiap `.shotcard` (hint "tekan gambar untuk memperbesar").

## Aset gambar (`P03/img/`)

5 tangkapan modul (VS Code) + hasil render yang dibikin ulang via Playwright:

- `step-01-index-html` … `step-05-contact-html` — tangkapan sumber modul 003.
- `render-home`, `render-about`, `render-contact` — hasil render `127.0.0.1` dari app contoh (kode modul 003).
- `adv-home`, `adv-about`, `adv-contact` — contoh **pengembangan lanjutan** (proyek pribadi asdos, 7 halaman, dark glass) di slide bonus s22.

## Kuis (5 soal)

1. Tag HTML untuk heading/judul paling besar? → **`<h1>`**
2. Atribut pada `<a>` yang berisi alamat tujuan link? → **`href`**
3. Cara paling rapi menghubungkan CSS ke HTML? → **file eksternal via `<link>`**
4. Tag untuk membuat daftar berurutan (bernomor)? → **`<ol>`**
5. Folder Flask tempat menyimpan file HTML? → **`templates/`**

## Catatan penting

- Deck **melanjutkan P02**: P02 sudah membuat `app.py`, `templates/index.html`, dan `static/css/style.css`; P03 **melengkapinya** jadi 3 halaman + UI lengkap (bukan membuat dari nol), sesuai instruksi user.
- Modul 003 memakai CSS dasar (Arial, header `#2c3e50`, body `#f4f4f4`). Semua kode di deck mengikuti modul.
- Jalur lanjutan (s22) bersifat opsional/inspirasi — bukan tuntutan tugas.