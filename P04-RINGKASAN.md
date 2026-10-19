# P04 — Layout & Template Engine (Jinja2)

_Ringkasan isi deck P04 (31 slide). Deck self-contained di `P04/index.html` + aset WebP hasil render di `P04/img/`._

**Basis Materi:** Modul `004 — Layout dan Template Engine (Jinja2)` + codebase praktik kelas `~/asdos/praktikum` (6 halaman Flask).  
**Konsep Pembelajaran:** Mahasiswa menutup dua masalah nyata di portofolio P03 — header/footer yang disalin enam kali dan data yang ditulis manual di HTML — memakai enam konsep Jinja2: `extends`, `block`, kirim data, tampilkan data, `for`, dan `if/elif/else`.  
**Deadline tugas:** Rabu, 28 Oktober 2026, 23.59 WIB.

---

## Daftar Isi (31 Slide)

- 1. Layout & Template Engine dengan Jinja2 *(Pembuka)*
- 2. Alur pertemuan hari ini *(Pembuka)*
- 3. Di akhir praktikum, kamu bisa *(Pembuka)*
- 4. Peta enam konsep *(Pembuka)*
- 5. Header dan footer yang sama, enam kali *(Dasar teori)*
- 6. Data ditulis manual di HTML *(Dasar teori)*
- 7. Satu induk, enam anak *(Dasar teori)*
- 8. Dua jenis kurung kurawal *(Dasar teori)*
- 9. Aktifkan venv & siapkan salinan kerja *(Praktik · Titik awal)*
- 10. Baca dulu duplikasinya *(Praktik · Part 1)*
- 11. Langkah 1: head & `{% block title %}` *(Praktik · Part 1)*
- 12. Langkah 2: header, nav, dan menu aktif *(Praktik · Part 1)*
- 13. Langkah 3: `{% block content %}` & footer *(Praktik · Part 1)*
- 14. `index.html` jadi halaman anak *(Praktik · Part 2)*
- 15. `about.html`: bio & timeline tetap *(Praktik · Part 2)*
- 16. `skills.html`: loop + badge level *(Praktik · Part 2)*
- 17. `projects.html`, `blog.html`, `contact.html` *(Praktik · Part 2)*
- 18. Kirim data dari Python ke template *(Praktik · Part 3)*
- 19. Data list: mata kuliah, skills, proyek, artikel *(Praktik · Part 3)*
- 20. Route mengirim data & variabel aktif *(Praktik · Part 3)*
- 21. Tampilkan data dengan `{{ }}` *(Praktik · Part 3)*
- 22. Badge level dengan `{% if / elif / else %}` *(Praktik · Part 3)*
- 23. Kartu profil di `about.html` *(Praktik · Part 3)*
- 24. Jalankan & verifikasi enam route *(Praktik · Part 4)*
- 25. Yang berubah, dan yang sengaja tidak *(Praktik · Part 4)*
- 26. Nilai kamu dihitung dari mana *(Tugas)*
- 27. Sekarang giliran kamu *(Tugas)*
- 28. Ketentuan & pengumpulan *(Tugas)*
- 29. Kuis template engine *(Penutup)*
- 30. Dari enam salinan menjadi satu induk *(Penutup)*
- 31. Selamat, kerangkamu rapi! *(Penutup)*

---

## Widget interaktif

| Slide | Widget | Cara pakai |
|---|---|---|
| 4 | Peta enam konsep | klik kotak → contoh sintaks + slide terkait |
| 5 | Diff duplikasi | panel `about.html` vs `blog.html`, tombol hitung baris identik |
| 6 | Simulator data hard-code | geser slider level Flask → jumlah tempat yang harus diubah |
| 7 | Diagram inheritance | klik halaman anak → blok `base.html` yang terisi menyala |
| 8 | Sintaks switcher | tab `{{ }}` vs `{% %}` + hasil render live |
| 9, 24 | Terminal OS-aware | Windows / Linux-macOS, output default tersembunyi, salin command-only |
| 10 | Pemeriksa duplikasi | klik `head` / `header` / `footer` → penjelasan |
| 12 | Navsim | tombol `aktif=` → link aktif berpindah di mock nav |
| 14–17 | Refactor tracker | chip halaman berubah hijau setelah tiap halaman selesai |
| 18–20, 23 | Code pane `app.py` & template | potongan kode asli + tombol salin |
| 21 | Panel data live | hasil render `profil.nama`, `profil.semester`, loop `matkul` |
| 22 | Simulator badge | klik level → cabang `if/elif/else` yang dipilih |
| 24 | Pemeriksa route | klik tiap route → status terverifikasi |
| 26 | Rubrik interaktif | klik kriteria → detail empat tingkat |
| 27 | Checklist + hitung mundur | centang 5 butir, timer ke deadline 28 Okt 2026 23.59 |
| 29 | Kuis 5 soal | skor + ulangi |
| semua | Lightbox | klik screenshot untuk memperbesar |

---

## Perubahan kode proyek kelas (dipakai di deck)

Salinan kerja: `~/asdos/praktikum-p04/` (repo asli `~/asdos/praktikum` hanya diperbaiki satu `</a>` yang hilang di nav `index.html`).

- **`templates/base.html` (baru)** — head, header + nav dengan `{% if aktif == '…' %}`, `{% block title %}`, `{% block content %}`, footer.
- **6 child template** — `{% extends 'base.html' %}`; header/footer tidak lagi disalin.
- **`app.py`** — data `profil`, `matkul`, `skills`, `proyek`, `artikel`; setiap route mengirim `aktif=` + data yang dibutuhkan.
- **`skills.html`** — `{% for skill in skills %}` + badge `{% if level >= 80 %} Mahir / {% elif >= 60 %} Menengah / {% else %} Dasar`.
- **`about.html`** — kartu profil dari Python, status umur pakai `{% if profil.umur >= 18 %}`.
- **`projects.html`** — loop proyek, ikon dipilih lewat `{% if proyek.icon == … %}`.
- **`blog.html`** — loop artikel.
- **`style.css`** — tambahan `.badge`, `.badge-mahir/-menengah/-dasar`, `.profile-card`, `.profile-head`, `.profile-info`, `.skill-meta`.

Catatan penting (jebakan yang dibahas di deck):

1. Fungsi route **tidak boleh** bernama sama dengan variabel data. `def skills()` menimpa list `skills` → dipakai `def keahlian()` (URL tetap `/skills`).
2. `url_for()` memakai nama fungsi (endpoint), bukan path.
3. Modul 004 asli punya tiga celah yang **tidak** ditiru: `about()` tidak mengirim `data`, tidak ada route `contact`, dan judul block salah.

---

## Hasil verifikasi

- 31 slide; `i[data-lucide]` = 0 sisa; 10 gambar termuat.
- 0 kepotong di 10 viewport (1920×1080 sampai 667×375, termasuk landscape HP).
- Semua widget diklik (peta konsep, diff, slider, diagram, tab sintaks, terminal + OS tab, navsim, badge, route, rubrik, checklist); kuis **5/5**.
- Salin terminal = command-only; output terminal default tersembunyi.
- PDF **31 halaman** 297×167 mm; fullscreen jalan.
- Proyek kelas: 6 route HTTP 200, tanpa `Undefined`, nav aktif benar di 6 halaman.
- Regresi visual: `home`, `projects`, `blog`, `contact` identik (RMSE 0); hanya `skills` (badge) dan `about` (kartu profil) berubah sesuai rencana.
