# P05 — Routing Dinamis, HTTP Methods (GET & POST), dan Formulir Interaktif

_Ringkasan isi deck P05 (21 slide interaktif). Deck mandiri (self-contained) di `P05/index.html` + aset gambar hasil render di `P05/img/`._

**Basis Materi:** Codebase portofolio 6 halaman otentik dari `asdos/praktikum-p05` (Flask + Jinja2 + HTML5/CSS modern).  
**Konsep Pembelajaran:** Mengubah website statis P-04 menjadi aplikasi interaktif dinamis dengan menangkap parameter URL menggunakan *Variable Rules* & *Converters* (`<int:post_id>`, `<nama>`), membedakan HTTP Methods (GET vs POST), memproses masukan formulir via `request.form.get()`, mengamankan session dengan `app.secret_key`, menerapkan notifikasi umpan balik *Flash Messages*, dan mengadopsi arsitektur *Post/Redirect/Get (PRG)*.  
**Deadline Tugas:** Rabu, 4 November 2026, 23.59 WIB.

---

## Daftar Isi Slide (21 Slide Terstruktur)

### Babak 1 · Orientasi & Variable Rules (Slide 1–5)
- **Slide 1**: Routing Dinamis & Formulir Interaktif *(Cover Kelas & Meta Praktikum)*
- **Slide 2**: Peta Perjalanan Praktikum Web *(Roadmap P01 s.d. P05)*
- **Slide 3**: Mengapa Butuh Dynamic Routing? *(1 Route untuk 1000 Halaman vs 1000 Route Statis)*
- **Slide 4**: Anatomi Variable Rules & Converter Types *(string, int, float, path, uuid)*
- **Slide 5**: Simulator Converter Interaktif *(Widget uji URL: validasi angka vs huruf real-time)*

### Babak 2 · Backend Dynamic Routing & Template Detail (Slide 6–10)
- **Slide 6**: Langkah 0: Workspace Setup — Opsi A (Tugas Mandiri) vs Opsi B (Clone Starter Kit GitHub)
- **Slide 7**: Langkah 1: Setup Import Flask & `app.secret_key` *(Mengapa butuh secret key?)*
- **Slide 8**: Langkah 2: Rute Dinamis `@app.route('/blog/<int:post_id>')` & `/user/<nama>`
- **Slide 9**: Langkah 3: Menghubungkan Daftar Blog dengan `url_for('blog_detail', post_id=item.id)`
- **Slide 10**: Langkah 4: Template Baru `templates/blog_detail.html` *(Handling Data & 404 Empty State)*

### Babak 3 · HTTP Methods & Form Handling (Slide 11–14)
- **Slide 11**: Teori HTTP Methods: Analogi Kartu Pos (GET) vs Surat Tertutup Amplop (POST)
- **Slide 12**: Simulator HTTP Methods Interaktif *(Bandingkan URL Query String vs Request Body)*
- **Slide 13**: Langkah 5: Mengaktifkan Formulir Kontak (`method="POST"` & pentingnya atribut `name`)
- **Slide 14**: Langkah 6: Backend Form Handling (`request.form.get`) & Pola Post/Redirect/Get (PRG)

### Babak 4 · Notifikasi Flash & Latihan Modul (Slide 15–16)
- **Slide 15**: Langkah 7: Wadah Notifikasi Global di `templates/base.html` *(Alert Sukses & Bahaya)*
- **Slide 16**: Latihan Modul: Sistem Login Sederhana (`/login`, validasi admin/12345 & Flash Message)

### Babak 5 · Evaluasi, Rubrik & Kuis (Slide 17–21)
- **Slide 17**: Freshmen Shield: Panduan Solusi 6 Eror Terpopuler Pemula
- **Slide 18**: Verifikasi Rute Praktikum *(Interactive Route Checker 200 OK)*
- **Slide 19**: Rubrik Penilaian Tugas Modul P05 (Total 100 Poin)
- **Slide 20**: Checklist Tugas & Countdown Timer Pengumpulan
- **Slide 21**: Kuis Interaktif Pemahaman P-05 (5 Soal Pilihan Ganda dengan Skor Otomatis)

---

## Fitur Unggulan Deck P05 untuk Mahasiswa Pemula

1. **Simulator URL Converter Interaktif (Slide 5):**
   Mahasiswa dapat mengetik URL langsung di slide (misal `/blog/1` atau `/blog/halo`) dan melihat secara langsung bagaimana Flask merespons: apakah mengembalikan `200 OK` (karena berupa angka) atau melempar `404 Not Found` (karena ditolak oleh converter `<int:>`).
2. **Simulator HTTP Methods (Slide 11):**
   Mahasiswa dapat mencoba saklar toggle antara metode GET dan POST, melihat visualisasi bagaimana query string ditempel di URL pada GET dan bagaimana data disembunyikan di Request Body pada POST.
3. **Mockup VS Code Asli dengan Sorotan Hijau:**
   Menampilkan potongan kode persis yang perlu ditambahkan di file `app.py`, `templates/blog_detail.html`, `templates/contact.html`, dan `templates/base.html`, lengkap dengan nomor baris dan breadcrumbs folder.
4. **Tombol 1-Klik Salin Kode (`📋 Salin`):**
   Mempermudah mahasiswa menyalin blok kode backend dan template tanpa risiko salah blok atau sintaks terpotong.
5. **Freshmen Shield Anti-Panik (Slide 16):**
   Merangkum 6 eror legendaris mahasiswa baru (`405 Method Not Allowed`, `RuntimeError secret_key`, input `None` akibat lupa atribut `name`, `404 Not Found` pada integer converter, dialog resubmission refresh, dan `NameError request`) lengkap dengan penjelasannya.
