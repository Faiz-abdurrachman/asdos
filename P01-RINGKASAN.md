# P01 — Pengenalan Pemrograman Web & Python

_Ringkasan seluruh isi deck P01 (27 slide), diekstrak otomatis dari `P01/index.html`._
_Urutan: judul tiap slide, poin isi, simulasi terminal, dan referensi gambar._

**Urutan bagian:** Pembuka → Kelas → Dasar teori → Praktik Part 1–4 → Bantuan → Tugas → Penutup.

## Daftar isi

- 1. Buat web app pertama kamu *(bagian: Pembuka)*
- 2. Alur pertemuan hari ini *(bagian: Pembuka)*
- 3. Di akhir praktikum, kamu bisa *(bagian: Kelas)*
- 4. Nilai kamu dihitung dari mana *(bagian: Kelas)*
- 5. Client-server: dua peran, satu percakapan *(bagian: Dasar teori)*
- 6. HTTP: empat kata kerja *(bagian: Dasar teori)*
- 7. Flask: framework Python yang ringan *(bagian: Dasar teori)*
- 8. Empat alat untuk hari ini *(bagian: Dasar teori)*
- 9. Pasang Python dari situs resminya *(bagian: Praktik · Part 1)*
- 10. Windows: unduh installer dari python.org *(bagian: Praktik · Part 1 · Windows)*
- 11. Pasang: centang “Add python.exe to PATH” *(bagian: Praktik · Part 1 · Windows)*
- 12. Tunggu sampai “Setup was successful” *(bagian: Praktik · Part 1 · Windows)*
- 13. Buka Terminal, lalu buktikan versinya *(bagian: Praktik · Part 1 · Windows)*
- 14. Buat folder, lalu masuk ke dalamnya *(bagian: Praktik · Part 1)*
- 15. Virtual environment: ruang terpisah setiap proyek *(bagian: Praktik · Part 1)*
- 16. Aktifkan venv — sesuai sistem kamu *(bagian: Praktik · Part 1)*
- 17. Satu perintah, tujuh paket *(bagian: Praktik · Part 2)*
- 18. Jangan percaya — verifikasi *(bagian: Praktik · Part 2)*
- 19. app.py — sepuluh baris, klik semua *(bagian: Praktik · Part 3)*
- 20. Jalankan: python app.py *(bagian: Praktik · Part 4)*
- 21. 127.0.0.1:5000 — ketuk pintunya *(bagian: Praktik · Part 4)*
- 22. Apa fungsi debug=True *(bagian: Praktik · Part 4)*
- 23. Jika macet, cek ini dulu *(bagian: Bantuan)*
- 24. Sekarang giliran kamu *(bagian: Tugas)*
- 25. Ketentuan & pengumpulan *(bagian: Tugas)*
- 26. Kuis kilat — lima soal *(bagian: Penutup)*
- 27. Hari ini, dari nol, kamu sudah *(bagian: Penutup)*
- Lampiran A — Rubrik lengkap
- Lampiran B — Empat method HTTP
- Lampiran C — Penjelasan tiap baris `app.py`
- Lampiran D — Pilihan installer Windows
- Lampiran E — Kuis (5 soal)


---

# Pembuka

## 1. Buat web app pertama kamu

*Praktikum Pemrograman Web — Pertemuan 01*

- $ python app.py
- Pengenalan Pemrograman Web & Python: client-server, HTTP, virtual environment, sampai aplikasi Flask pertama kamu berjalan di browser.
- Materi: modul praktikum P01 · Deck versi web interaktif

## 2. Alur pertemuan hari ini

*Run of show*

- 100 menit total, dari nol sampai web app pertama kamu berjalan.
- 01
- Dasar teori
- Client-server, HTTP dan method-nya, kenapa Flask
- ±15 menit
- 02
- Praktik: setup sampai jalan
- Python, folder, venv, pip, app.py, server berjalan
- 45 menit
- 03
- Tugas praktikum
- Route /about dan /profile versi kamu sendiri
- 30 menit
- 04
- Kuis & penutup
- Cek pemahaman, lalu recap apa yang sudah bisa kamu lakukan
- ±10 menit


---

# Kelas

## 3. Di akhir praktikum, kamu bisa

*Capaian pembelajaran*

- Ngejer basisnya
- Memahami arsitektur client-server dan bagaimana HTTP menjadi bahasa percakapan keduanya.
- teori
- Nyiapin dapur
- Menginstal dan mengkonfigurasi lingkungan pengembangan Python yang rapi per proyek.
- setup
- Jalankan aplikasi
- Membuat aplikasi web pertama dengan Flask dan menjalankannya di browser.
- praktik

## 4. Nilai kamu dihitung dari mana

*Rubrik penilaian*

- Klik setiap kriteria untuk melihat level penilaiannya — kode program paling menentukan.
- Instalasi & Setup
- Environment Python + Flask terpasang
- 25%
- 100%
- Environment berhasil, Flask terinstal
- 75%
- Environment berhasil
- 50%
- Instalasi sebagian
- 25%
- Tidak berhasil
- Kode Program
- Route lengkap, kode rapi dan terstruktur
- 35%
- 100%
- 3 route, kode rapi
- 75%
- 2 route, rapi
- 50%
- 1 route
- 25%
- Tidak berfungsi
- Pengujian
- Semua route terbukti berjalan di browser
- 25%
- 100%
- Semua route berfungsi
- 75%
- 2 route berfungsi
- 50%
- 1 route berfungsi
- 25%
- Tidak berfungsi
- Dokumentasi
- File .py + screenshot hasil di browser
- 15%
- 100%
- Lengkap, rapi
- 75%
- Cukup lengkap
- 50%
- Kurang lengkap
- 25%
- Tidak ada
- Total 100% — diambil dari rubrik resmi modul P01.


---

# Dasar teori

## 5. Client-server: dua peran, satu percakapan

*Dasar teori · 1 dari 3*

- Client
- Browser di komputer kamu. Tugasnya: meminta.
- request
- Server
- Komputer lain yang siaga. Tugasnya: layani.
- Kirim request
- Client tidak pernah memberi — server tidak pernah menyerah. Coba kirim.

## 6. HTTP: empat kata kerja

*Dasar teori · 2 dari 3*

- Percakapan client-server punya aturan. Tekan method-nya, lihat percakapannya.
- GET
- mengambil data
- POST
- mengirim data baru
- PUT
- mengupdate data
- DELETE
- menghapus data
- Contoh nyatanya: setiap kali kamu membuka halaman Instagram, browser mengirim GET ratusan kali.

## 7. Flask: framework Python yang ringan

*Dasar teori · 3 dari 3*

- Micro-framework web untuk Python — ringan, fleksibel, tinggal tambah sesuai kebutuhan.
- Flask
- Framework-nya sendiri. Menerima request, memanggil kode kamu, membalas response. Satu file Python cukup untuk memulai.
- pip install flask
- Jinja2
- Template engine bawaan Flask. Membuat HTML yang bisa diisi data dinamis dari Python.
- template engine
- Micro apa maksudnya
- Inti kecil, sisanya pilihan. Tidak dikasih admin panel, ORM, atau aturan struktur folder — kamu yang memutuskan.
- no magic

## 8. Empat alat untuk hari ini

*Perlengkapan*

- Semua gratis. Jika ada yang belum ada, download sebelum praktik dimulai.
- Python 3.10+
- Bahasa pemrograman sekaligus mesin semua yang kita bangun
- Flask
- Framework web — nanti dipasang melalui pip
- VS Code
- Code editor tempat kita menulis app.py
- Browser
- Untuk menguji aplikasi — client kita sejati


---

# Praktik · Part 1

## 9. Pasang Python dari situs resminya

*Praktikum · Part 1 — langkah 1 dari 4*

- Unduh installer dari python.org, ikuti langkahnya sampai selesai — lalu jangan langsung percaya, buktikan melalui terminal.
- python.org/downloads
- step 01
- Halaman download python.org
- klik tombol unduh versi terbaru

**Terminal — cek versi**

```
$ python --version
Python 3.12.3
# versi 3.10 ke atas = siap praktikum
```

**Gambar:**
`img/step-01-download-python.webp` — Halaman python.org dengan tombol Download Python 3.14.7 disorot


---

# Praktik · Part 1 · Windows

## 10. Windows: unduh installer dari python.org

*Jalur Windows — langkah 1 dari 4*

- Halaman python.org menawarkan dua berkas. Untuk praktikum ini kita pilih standalone installer — satu berkas, sekali jalan.
- Standalone installer
- Install manager
- Standalone installer
- Pilihan kita: python-3.14.7-amd64.exe. Satu berkas, langsung menjalankan installer — paling sederhana untuk kelas.
- python.org/downloads
- win 01
- Halaman unduh Windows
- pilih standalone installer 3.14.7
- win 02
- Berkas siap dijalankan
- python-3.14.7-amd64.exe · 31,7 MB

**Gambar:**
`img/win-01-download-page.webp` — Halaman python.org bagian Windows dengan tombol install manager dan tautan standalone installer Python 3.14.7
`img/win-02-download-history.webp` — Riwayat unduhan browser menampilkan python-3.14.7-amd64.exe berukuran 31,7 MB berstatus Done

## 11. Pasang: centang “Add python.exe to PATH”

*Jalur Windows — langkah 2 dari 4*

- Ini langkah yang paling sering terlewat. Sebelum menekan Install Now, pastikan kotak di bagian bawah jendela installer tercentang.
- Add python.exe to PATH
- Membuat perintah python bisa dikenali di terminal.
- Klik kotak di atas untuk melihat apa yang terjadi bila lupa mencentangnya.
- Tanpa centang ini, terminal menjawab: 'python' is not recognized… — dan kamu harus memasang ulang sambil mengaktifkan opsi ini.
- win 03
- Centang PATH, lalu Install Now
- dua hal yang wajib benar di jendela ini

**Gambar:**
`img/win-03-installer-path.webp` — Jendela installer Python 3.14.7 dengan opsi Install Now disorot dan kotak Add python.exe to PATH tercentang

## 12. Tunggu sampai “Setup was successful”

*Jalur Windows — langkah 3 dari 4*

- Installer menyalin interpreter Python, pip, dan IDLE. Jangan tutup jendelanya sebelum selesai.
- jalankan installer
- belum dijalankan
- Setelah selesai, tekan Close. Instalasi hanya sekali — setelah ini python dan pip siap dipakai.
- win 04
- Proses instalasi
- menyalin Core Interpreter (64-bit)
- win 05
- Setup was successful
- Python siap — tekan Close

**Gambar:**
`img/win-04-setup-progress.webp` — Jendela Setup Progress sedang memasang Python 3.14.7 Core Interpreter 64-bit
`img/win-05-setup-success.webp` — Jendela Setup was successful menandakan instalasi Python 3.14.7 selesai

## 13. Buka Terminal, lalu buktikan versinya

*Jalur Windows — langkah 4 dari 4*

- Cari Terminal di menu Start. Di Windows perintahnya python — bukan python3. Jalankan dua perintah ini untuk memastikan semuanya siap.
- win 06
- Buka Terminal dari Start
- cari “terminal”, buka hasil teratas
- win 07
- Verifikasi versi
- python 3.14.7 · pip 26.2.1

**Terminal — Windows PowerShell**

```
PS C:\Users\user> python --version
Python 3.14.7
PS C:\Users\user> pip --version
pip 26.2.1 from C:\Users\user\AppData\Local\Programs\Python\Python314\Lib\site-packages\pip
```

**Gambar:**
`img/win-06-open-terminal.webp` — Menu Start Windows dengan pencarian terminal dan hasil Terminal di urutan teratas
`img/win-07-verify-version.webp` — Windows PowerShell menjalankan python --version dan pip --version menampilkan Python 3.14.7 dan pip 26.2.1


---

# Praktik · Part 1

## 14. Buat folder, lalu masuk ke dalamnya

*Praktikum · Part 1 — langkah 2 dari 4*

- Satu proyek, satu folder — semuanya tinggal di dalamnya: kode, venv, dan file pendukung. Nama foldernya bebas — di contoh ini PrakPemWeb. Setelah dibuat, masuk ke dalamnya supaya perintah berikutnya dijalankan di tempat yang benar.
- Tanpa mengetik: di File Explorer klik kanan folder → Open in Terminal; di VS Code File → Open Folder; di macOS klik kanan folder → New Terminal at Folder.
- step 02
- Buat folder proyek
- lalu masuk ke dalamnya sebelum lanjut

**Terminal — PrakPemWeb — masuk folder proyek**

```
$ cd PrakPemWeb
# masuk — kamu kini berada di dalam folder proyek
# prompt ikut berubah, mis. ~/PrakPemWeb $
# di Windows: C:\Users\user\PrakPemWeb>
```

**Gambar:**
`img/step-02-buat-folder.webp` — File explorer menampilkan folder proyek PrakPemWeb yang baru dibuat

## 15. Virtual environment: ruang terpisah setiap proyek

*Praktikum · Part 1 — langkah 3 dari 4*

- Linux / macOS
- Windows
- Tanpa venv, semua proyek berbagi package Python yang sama — seperti satu rumah bersama untuk semua penghuninya. Dengan venv, setiap proyek punya ruang sendiri. Perintahnya beda tipis: python3 di Linux/macOS, python di Windows.
- step 03
- python3 -m venv .venv
- dijalankan di dalam folder proyek

**Terminal — PrakPemWeb — buat venv**

```
$ python3 -m venv .venv
# tanpa output — dan itu tanda sukses
.venv/ berhasil dibuat
```

**Gambar:**
`img/step-03-venv.webp` — Terminal menjalankan perintah python3 -m venv .venv di dalam folder proyek

## 16. Aktifkan venv — sesuai sistem kamu

*Praktikum · Part 1 — langkah 4 dari 4*

- Linux / macOS
- Windows
- Tanda venv aktif: Warp menampilkan nama environment di indikator Python-nya (di screenshot: PrakPemWeb 3.12.3). Di shell biasa, prompt berubah menjadi (.venv) di depannya. Matikan kapan pun dengan deactivate.
- step 04
- source .venv/bin/activate
- environment PrakPemWeb aktif

**Terminal — PrakPemWeb — aktifkan venv**

```
$ source .venv/bin/activate
(.venv) PrakPemWeb $
```

**Gambar:**
`img/step-04-activate.webp` — Terminal menjalankan source .venv/bin/activate, indikator environment PrakPemWeb 3.12.3


---

# Praktik · Part 2

## 17. Satu perintah, tujuh paket

*Praktikum · Part 2 — pasang Flask*

- Flask kecil, tetapi ia tidak berjalan sendirian — teman-temannya ikut terpasang ke venv kita, bukan ke sistem.
- step 05
- pip install flask
- flask 3.1.3 + 6 dependensi ikut masuk

**Terminal — PrakPemWeb — pasang flask**

```
(.venv) PrakPemWeb $ pip install flask
Collecting flask
Collecting blinker, click, itsdangerous,
jinja2, markupsafe, werkzeug (from flask)
Using cached flask-3.1.3-py3-none-any.whl (103 kB)
Installing collected packages ...
Successfully installed blinker-1.9.0
click-8.5.0 flask-3.1.3 itsdangerous-2.2.0
jinja2-3.1.6 markupsafe-3.0.3 werkzeug-3.1.8
```

**Gambar:**
`img/step-05-pip-install.webp` — Output pip install flask beserta daftar dependensi yang ikut terpasang

## 18. Jangan percaya — verifikasi

*Praktikum · Part 2 — verifikasi*

- step 06
- pip show flask
- kartu identitas Flask: versi, lokasi, dependensi

**Terminal — PrakPemWeb — verifikasi flask**

```
(.venv) PrakPemWeb $ pip show flask
Name: flask
Version: 3.1.3
Summary: A simple framework for
building complex web applications.
Location: .venv/lib/python3.12/site-packages
Requires: blinker, click, itsdangerous,
jinja2, markupsafe, werkzeug
```

**Gambar:**
`img/step-06-pip-show.webp` — Output pip show flask menampilkan versi, ringkasan, lokasi, dan dependensi Flask


---

# Praktik · Part 3

## 19. app.py — sepuluh baris, klik semua

*Praktikum · Part 3 — aplikasi pertama*

- app.py
- klik barisnya
- 1
- from flask import Flask
- 2
- 3
- app = Flask(__name__)
- 5
- @app.route('/')
- 6
- def hello_world():
- 7
- return 'Hello, World!'
- 9
- if __name__ == '__main__':
- 10
- app.run(debug=True)
- Baris
- 1
- ·
- from flask import Flask
- Ambil class Flask dari package yang baru saja kamu pasang. Ini gerbangnya — tanpa baris ini, sisanya hanya teks.
- step 07
- Tulis app.py di VS Code
- satu file di dalam folder proyek

**Gambar:**
`img/step-07-app-py.webp` — Tampilan VS Code dengan file app.py berisi kode Flask hello world


---

# Praktik · Part 4

## 20. Jalankan: python app.py

*Praktikum · Part 4 — menjalankan*

- step 08
- Server aktif di terminal
- debug mode aktif, debugger aktif, berjalan di port 5001

**Terminal — PrakPemWeb — jalankan**

```
(.venv) PrakPemWeb $ python app.py
* Serving Flask app 'app'
* Debug mode: on
WARNING: This is a development server.
Use a production WSGI server instead.
* Running on http://127.0.0.1:5001
* Press CTRL+C to quit
* Restarting with stat
* Debugger is active!
* Debugger PIN: 142-626-400
```

**Gambar:**
`img/step-08-run.webp` — Terminal menjalankan python app.py dengan output Serving Flask app, Debug mode on, dan Debugger is active

## 21. 127.0.0.1:5000 — ketuk pintunya

*Praktikum · Part 4 — buka di browser*

- 127.0.0.1 itu localhost — komputer kamu sendiri. Secara default Flask berjalan di port 5000, sehingga URL-nya 127.0.0.1:5000. Jika port 5000 sudah terpakai, Flask otomatis pindah — di screenshot ini ia berjalan di 5001, dan terminal selalu memberi tahu melalui baris Running on. Ketik alamat yang muncul di browser, dan:
- 127.0.0.1:5001
- PrakPemWeb
- Hello, World!
- 200 OK — localhost merespon
- step 09
- Hello, World! di browser
- momen pertama kamu menjadi web developer

**Gambar:**
`img/step-09-browser.webp` — Browser menampilkan halaman Hello, World di alamat 127.0.0.1:5001

## 22. Apa fungsi debug=True

*Praktikum · Part 4 — satu parameter penting*

- Satu kata di baris terakhir yang mengubah pengalaman coding kamu selama development.
- Auto-reload
- Kode berubah, server restart sendiri. Tidak perlu Ctrl+C lalu jalankan ulang setiap kali.
- hemat hidup
- Debugger aktif
- Error muncul langsung di browser lengkap dengan jejaknya — bukan hanya angka 500 misterius.
- temukan bug
- Hanya untuk development
- Terminal kamu sendiri mengingatkan: jangan digunakan di production. Gunakan server WSGI saat online.
- jangan production


---

# Bantuan

## 23. Jika macet, cek ini dulu

*Bantuan cepat*

- Empat gangguan paling sering muncul di praktikum hari ini.
- python tidak dikenali
- Coba python3. Di Windows, pasang ulang Python + centang "Add Python to PATH".
- Port 5000 sudah digunakan
- Flask pindah ke port lain (mis. 5001) — buka alamat di baris Running on.
- No module named 'flask'
- Venv belum aktif — jalankan ulang activate, lalu pip install flask.
- Kode diubah, tidak berubah
- Pastikan debug=True supaya auto-reload; jika perlu restart server (Ctrl+C, jalankan lagi).


---

# Tugas

## 24. Sekarang giliran kamu

*Tugas praktikum — 30 menit*

- Route /about
- Halaman "About Me" — tampilkan Nama dan NIM kamu
- Route /profile
- Halaman profile singkat versi kamu sendiri
- Mode debug aktif
- Aplikasi otomatis reload saat kode berubah
- 0/3 selesai
- SISA WAKTU · hari : jam : menit : detik
- 06:17:14:51
- deadline: Rabu, 7 Oktober 2026, 23.59

## 25. Ketentuan & pengumpulan

*Aturan main*

- Ketentuan kode
- Kode rapi dan terstruktur — kebiasaan baik dimulai dari app pertama
- Setiap route punya fungsinya sendiri yang sesuai
- Ekspor file dalam format .py + screenshot hasil di browser
- Pengumpulan
- Upload file .py dan laprak (screenshot di dalam laprak) ke LMS
- Deadline: Rabu, 7 Oktober 2026, 23.59
- Uji dulu semua route di browser sebelum upload — yang dinilai: yang berjalan


---

# Penutup

## 26. Kuis kilat — lima soal

*Cek pemahaman*

- Soal 1/5
- Method HTTP yang digunakan untuk MENGAMBIL data dari server?

## 27. Hari ini, dari nol, kamu sudah

*Recap — pertemuan 01 selesai*

- Memahami percakapan client ↔ server dan empat method HTTP
- Membuat virtual environment yang rapi dan memasang Flask di dalamnya
- Menjalankan app.py — web app pertama kamu, live di 127.0.0.1:5000
- $ ex
- Tugasnya jangan lupa: /about dan /profile, upload ke LMS paling lambat Rabu, 7 Oktober 2026 pukul 23.59. Sampai ketemu di P02.

---

# Lampiran B — Empat method HTTP

### GET

- Contoh nyatanya: setiap kali kamu membuka halaman Instagram, browser mengirim GET ratusan kali.
- `GET /halaman HTTP/1.1`
- `-> server: mencari halamannya`
- `<- 200 OK — halaman dikirim ke browser`

### POST

- Submit formulir pendaftaran? Itu POST — mengirim data baru ke server.
- `POST /daftar HTTP/1.1`
- `-> server: terima data (nama, email)`
- `<- 201 Created — akun baru tersimpan`

### PUT

- Edit profil di media sosial — perubahan kamu dikirim melalui PUT.
- `PUT /profil/123 HTTP/1.1`
- `-> server: update data profil #123`
- `<- 200 OK — profil ter-update`

### DEL

- Hapus postingan — browser mengirim DELETE, data dihapus di server.
- `DELETE /post/456 HTTP/1.1`
- `-> server: hapus post #456`
- `<- 204 No Content — post hilang`

---

# Lampiran C — Penjelasan tiap baris `app.py`

### Baris 1 — `from flask import Flask`

Ambil class Flask dari package yang baru saja kamu pasang. Ini gerbangnya — tanpa baris ini, sisanya hanya teks.

### Baris 3 — `app = Flask(__name__)`

Membuat instance aplikasi Flask. __name__ memberi tahu Flask nama modul ini — Flask menggunakannya untuk mencari file template & static nanti.

### Baris 5 — `@app.route('/')`

Decorator: daftarin path / ke fungsi di bawahnya. Path / = halaman depan. Ini inti routing Flask.

### Baris 6 — `def hello_world():`

Fungsi yang dijalankan saat / dikunjungi. Nama fungsinya bebas — hello_world hanya konvensi.

### Baris 7 — `return 'Hello, World!'`

Nilai yang dibalas ke browser. Teks ini yang muncul di layar — coba ganti, refresh, lihat berubah.

### Baris 9 — `if __name__ == '__main__':`

Server berjalan hanya jika file ini dieksekusi langsung — jika di-import dari file lain, blok ini dilewati.

### Baris 10 — `app.run(debug=True)`

Jalankan server development bawaan Flask + debug mode: auto-reload & debugger aktif — lihat dua slide berikutnya.

---

# Lampiran D — Pilihan installer Windows

1. **Standalone installer** — Pilihan kita: python-3.14.7-amd64.exe. Satu berkas, langsung menjalankan installer — paling sederhana untuk kelas.

2. **Install manager** — Pengelola beberapa versi Python sekaligus. Berguna kalau kamu sering berpindah versi — untuk hari ini cukup yang standalone.

---

# Lampiran E — Kuis (5 soal)

**1. Method HTTP yang digunakan untuk MENGAMBIL data dari server?**

- A. GET  ✅
- B. POST
- C. PUT
- D. DELETE

**2. Kamu ingin mengirim data formulir pendaftaran ke server. Method yang tepat?**

- A. GET
- B. POST  ✅
- C. PUT
- D. DELETE

**3. Perintah untuk membuat virtual environment baru bernama .venv?**

- A. pip install .venv
- B. python venv --new
- C. python -m venv .venv  ✅
- D. source .venv

**4. Flask berjalan di port berapa secara default?**

- A. 80
- B. 3000
- C. 8080
- D. 5000  ✅

**5. Template engine yang digunakan Flask?**

- A. Jinja2  ✅
- B. Django
- C. Tailwind
- D. Laravel

_Jawaban benar ditandai centang._

---

_Selesai — 27 slide, 5 soal kuis._