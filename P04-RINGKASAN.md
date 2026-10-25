# P04 — Layout & Template Engine (Jinja2)

_Ringkasan isi deck P04 (24 slide). Deck self-contained di `P04/index.html` + aset WebP hasil render di `P04/img/`._

**Basis Materi:** Codebase portofolio 6 halaman otentik dari `asdos/praktikum` (Flask + HTML5 + CSS Tokens/Flexbox/Grid).  
**Konsep Pembelajaran:** Mahasiswa membedah dan merefaktor portofolio P03 — menghilangkan repetisi layout 6 halaman menjadi 1 template induk (`base.html`), serta memindahkan data statis ke controller Python (`app.py`) menggunakan Jinja2 (`extends`, `block`, `url_for`, variables `{{ }}`, loop `{% for %}`, dan conditional `{% if %}`).  
**Deadline tugas:** Rabu, 28 Oktober 2026, 23.59 WIB.

---

## Daftar Isi (24 Slide Terstruktur)

### Babak 1 · Orientasi & Analogi (Slide 1–4)
- 1. Layout & Template Engine (Jinja2) *(Cover Kelas)*
- 2. Header & Footer Dicopy-Paste 6 Kali! *(Refleksi P-03 & Diff Widget)*
- 3. Solusi: Prinsip "Kop Surat" (DRY) *(Konsep 1 Induk 6 Anak)*
- 4. 3 Misi Utama Praktikum Hari Ini *(Peta Jalan 3 Babak)*

### Babak 2 · Membuat Template Induk (Slide 5–8)
- 5. Dua Simbol Keramat Jinja2 *(Cheat Sheet {{ }} vs {% %})*
- 6. Langkah 1: Buat File templates/base.html *(Tombol Salin Kode Lengkap)*
- 7. 3 Zona Penting di base.html *(title, content, nav)*
- 8. Simulasi Menu Aktif 6 Rute *(Widget NavSim)*

### Babak 3 · Merefaktor Halaman Anak (Slide 9–13)
- 9. Rumus Emas Halaman Anak *(extends, title, content)*
- 10. Langkah 2: Refaktor templates/index.html *(Live Bersama & Tombol Salin)*
- 11. Langkah 3: Refaktor about.html & skills.html *(Tab Explorer)*
- 12. Langkah 4: Refaktor projects.html, blog.html, & contact.html *(Tab Explorer)*
- 13. Selamat! 6 Halaman Sukses Dimodularisasi *(Progres & Hasil Browser)*

### Babak 4 · Data Dinamis dari Python (Slide 14–18)
- 14. Kenapa Data Tidak Boleh Diketik Mati di HTML? *(Statis vs Dinamis)*
- 15. Langkah 5: Menyiapkan Data Backend di app.py *(Tombol Salin app.py)*
- 16. Langkah 6: Menampilkan Variabel {{ profil.nama }} *(Data Passing)*
- 17. Langkah 7: Perulangan Otomatis {% for s in skills %} *(Skills Loop)*
- 18. Langkah 8: Percabangan Logika {% if level >= 80 %} *(Slider Simulator Badge)*

### Babak 5 · Verifikasi & Evaluasi (Slide 19–24)
- 19. Verifikasi 6 Route di Terminal *(Route Checker 200 OK)*
- 20. Mengalami Error? Cek 4 Hal Ini Dulu! *(Troubleshooting Cheat Sheet)*
- 21. Penilaian Tugas P04 (Total 100 Poin) *(Accordion Rubrik 4x25%)*
- 22. Checklist Pengerjaan Sebelum Dikumpulkan *(Countdown & Checklist)*
- 23. Kuis Pemahaman Jinja2 (5 Soal) *(Interactive Quiz)*
- 24. Pertemuan 04 Berhasil! *(Penutup & Teaser P-05)*

---

## Fitur Ramah Pemula di Deck Ini

1. **Screenshot Visual VS Code Nyata:** Menampilkan jendela VS Code lengkap dengan folder explorer sidebar (`praktikum-p04 > templates`), breadcrumbs, dan nomor baris code. Mahasiswa tidak akan bingung file mana yang harus dibuka atau di folder mana file baru harus dibuat.
2. **Kotak Sorot Merah & Hijau (Visual Patching):**
   - **Merah (Hapus):** Menyorot persis nomor baris yang harus dihapus (misal: baris 1 s/d 20 di `index.html`).
   - **Hijau (Tempel):** Menyorot persis nomor baris tempat menempelkan kode baru (misal: baris 1 di `index.html` atau baris 5 di `app.py`).
   - Dilengkapi tab interaktif: Mahasiswa bisa beralih antara "🔴 1. Yang Dihapus" dan "🟢 2. Yang Ditempel".
3. **Tombol 1-Klik Salin Kode (`📋 Salin`):** Mahasiswa tidak perlu blok mouse yang rawan terpotong. Cukup klik tombol kuning, kode langsung tersalin ke clipboard.
4. **Side-by-Side Guide:** Sisi kiri berisi instruksi langkah demi langkah dan tombol salin, sisi kanan berisi mockup VS Code beresolusi tinggi (bisa diklik untuk zoom fullscreen via modal Lightbox).
5. **Cheat Sheet Error Asdos:** Slide 20 khusus merangkum 4 error yang paling sering dialami mahasiswa semester 1 (TemplateNotFound, extends di luar baris 1, block lupa ditutup, dictionary key typo) dan cara memperbaikinya dalam 5 detik.
