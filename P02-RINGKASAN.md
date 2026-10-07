# P02 — Setup Lingkungan Pengembangan Web Lanjutan

_Ringkasan seluruh isi deck P02 (27 slide), diekstrak otomatis dari `P02/index.html`._

**Urutan bagian:** Pembuka → Kelas → Dasar teori → Praktik Part 1–6 → Tugas → Penutup.

## Daftar isi

- 1. Rapikan proyek kenalan sama Git *(bagian: Pembuka)*
- 2. Alur pertemuan hari ini *(bagian: Pembuka)*
- 3. Di akhir praktikum, kamu bisa *(bagian: Kelas)*
- 4. Nilai kamu dihitung dari mana *(bagian: Kelas)*
- 5. Debug mode: server yang mengawasi sendiri *(bagian: Dasar teori)*
- 6. Struktur proyek: setiap file punya rumah *(bagian: Dasar teori)*
- 7. Git: mesin waktu untuk kode kamu *(bagian: Dasar teori)*
- 8. Aktifkan debug mode di app.py *(bagian: Praktik · Part 1)*
- 9. Jalankan lagi: python app.py *(bagian: Praktik · Part 1)*
- 10. Buat folder templates dan static *(bagian: Praktik · Part 2)*
- 11. Isi style.css dan index.html *(bagian: Praktik · Part 2)*
- 12. Ganti isi route dengan render_template *(bagian: Praktik · Part 3)*
- 13. Halamannya sekarang dari index.html *(bagian: Praktik · Part 3)*
- 14. Buat akun GitHub *(bagian: Praktik · Part 4)*
- 15. git config: nama & email kamu *(bagian: Praktik · Part 4)*
- 16. Buat kunci SSH ke GitHub *(bagian: Praktik · Part 4)*
- 17. Settings → SSH and GPG keys *(bagian: Praktik · Part 4)*
- 18. ssh -T: uji koneksi ke GitHub *(bagian: Praktik · Part 4)*
- 19. Belum punya Git? Pasang dulu *(bagian: Praktik · Part 5 · Pasang Git)*
- 20. git init & buat .gitignore *(bagian: Praktik · Part 6)*
- 21. Buat repo baru di GitHub *(bagian: Praktik · Part 5)*
- 22. git add & git commit *(bagian: Praktik · Part 6)*
- 23. Branch, remote, dan push *(bagian: Praktik · Part 6)*
- 24. Sekarang giliran kamu *(bagian: Tugas)*
- 25. Ketentuan & pengumpulan *(bagian: Tugas)*
- 26. Kuis kilat — lima soal *(bagian: Penutup)*
- 27. Hari ini, proyek kamu naik kelas *(bagian: Penutup)*
- Lampiran — Kuis (5 soal)


---

# Pembuka

## 1. Rapikan proyek kenalan sama Git

*Praktikum Pemrograman Web — Pertemuan 02*

- $ git push orig
- Setup Lingkungan Pengembangan Web Lanjutan: debug mode & auto-reload, struktur proyek rapi (templates & static), sampai kode kamu tersimpan aman di GitHub.
- Materi: modul praktikum P02 · Deck versi web interaktif

## 2. Alur pertemuan hari ini

*Run of show*

- 100 menit, dari proyek hello world tadi menjadi proyek yang rapi dan punya riwayat versi.
- 01
- Dasar teori
- Debug mode, struktur proyek, dan cara kerja Git
- ±15 menit
- 02
- Praktik: rapikan & simpan
- Debug mode, folder templates/static, SSH, repo, git push
- 45 menit
- 03
- Tugas praktikum
- Struktur folder + index.html + style.css + commit pertama
- 30 menit
- 04
- Kuis & penutup
- Cek pemahaman, lalu recap apa yang sudah kamu kuasai
- ±10 menit


---

# Kelas

## 3. Di akhir praktikum, kamu bisa

*Capaian pembelajaran*

- Debug mode
- Mengatur debug mode dan auto-reload supaya perubahan kode langsung terlihat.
- setup
- Struktur proyek
- Menata proyek web dengan folder templates dan static — tempat HTML, CSS, dan gambar.
- struktur
- Version control
- Memakai Git untuk mencatat riwayat dan menyimpan proyek ke GitHub.
- git

## 4. Nilai kamu dihitung dari mana

*Rubrik penilaian*

- Klik setiap kriteria untuk melihat level penilaiannya — keempatnya berbobot sama.
- Struktur Folder
- templates, static/css, static/js lengkap
- 25%
- 100%
- Lengkap dan rapi
- 75%
- Cukup lengkap
- 50%
- Kurang lengkap
- 25%
- Tidak ada
- Debug Mode
- Auto-reload & traceback berfungsi
- 25%
- 100%
- Berfungsi dengan baik
- 75%
- Berfungsi
- 50%
- Kurang berfungsi
- 25%
- Tidak ada
- Render Template
- HTML tampil lewat render_template
- 25%
- 100%
- Berhasil merender
- 75%
- Berhasil
- 50%
- Sebagian
- 25%
- Tidak berhasil
- Git
- init, .gitignore, commit, push
- 25%
- 100%
- Git init, .gitignore, commit
- 75%
- Git init
- 50%
- Sebagian
- 25%
- Tidak ada
- Total 100% — diambil dari rubrik resmi modul P02.


---

# Dasar teori

## 5. Debug mode: server yang mengawasi sendiri

*Dasar teori · 1 dari 3*

- Dua hal terjadi saat debug=True: kode berubah → server reload sendiri; ada error → jejaknya muncul di browser. Coba tombolnya.
- Browser · 127.0.0.1:5001
- Hello, World!
- Halaman berjalan normal. Tekan tombol di bawah untuk melihat perilaku debug mode.
- Ubah kode
- Buat error
- Kenapa penting
- Tanpa debug mode, setiap perubahan kode kamu harus restart server manual, dan error hanya tampil sebagai halaman putih atau angka 500.
- auto-reload

## 6. Struktur proyek: setiap file punya rumah

*Dasar teori · 2 dari 3*

- Proyek Flask punya pola folder yang baku. Klik tiap folder untuk tahu isinya.
- app.py
- File utama aplikasi Flask
- templates/
- Folder untuk file HTML
- static/css/
- Folder untuk file CSS
- static/images/
- Folder untuk gambar
- requirements.txt
- Daftar dependencies proyek
- app.py
- File utama aplikasi Flask. Di sinilah route dan tempat menjalankan server ditulis.
- struktur
- Struktur folder di VS Code
- templates, static/css, static/images

**Gambar:**
`img/p2-04-struktur-folder.webp` — VS Code Explorer menampilkan .venv, static/css/style.css, static/images, templates/index.html, dan app.py

## 7. Git: mesin waktu untuk kode kamu

*Dasar teori · 3 dari 3*

- Git mencatat setiap perubahan sebagai "commit" — kamu bisa lihat riwayat, kembali ke versi lama, dan bekerja bareng orang lain.
- 1
- Kerja di komputer
- Kamu mengubah file di folder proyek (working directory).
- 2
- git add — pilih perubahan
- Tandai file mana yang mau ikut disimpan ke dalam commit.
- 3
- git commit — simpan sebagai titik
- Semua perubahan yang ditandai tersimpan jadi satu riwayat dengan pesan.
- 4
- git push — kirim ke GitHub
- Commit kamu diunggah ke repositori online, aman dari kehilangan laptop.
- GitHub itu layanan hosting untuk repo Git — bukan Git itu sendiri. Git = alatnya, GitHub = tempat menyimpannya.


---

# Praktik · Part 1

## 8. Aktifkan debug mode di app.py

*Praktikum · Part 1 — debug mode*

- app.py
- klik barisnya
- 1
- from flask import Flask
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
- 10
- ·
- app.run(debug=True)
- Server development + debug mode: auto-reload dan debugger aktif. Parameter baru pertemuan ini.
- p2 01
- Baris app.run(debug=True)
- parameter yang mengaktifkan mode debug

**Gambar:**
`img/p2-01-debug-code.webp` — VS Code menampilkan app.py baris app.run(debug=True) disorot dengan komentar mode debug auto-reload

## 9. Jalankan lagi: python app.py

*Praktikum · Part 1 — jalankan*

- Dari dalam folder proyek (venv aktif), jalankan server seperti pertemuan lalu. Kali ini perhatikan Debug mode: on dan Debugger is active!.
- Windows
- Linux / macOS
- p2 02
- Server aktif di terminal
- Debug mode on · Running on 127.0.0.1:5001
- p2 03
- Buka di browser
- 127.0.0.1:5001 — Hello, World! tetap tampil

**Terminal — PrakPemWeb — jalankan**

```
```

**Gambar:**
`img/p2-02-run-debug.webp` — Terminal VS Code menjalankan python app.py dengan indikator PrakPemWeb 3.12.3 dan output Debug mode on serta Running on 127.0.0.1:5001
`img/p2-03-browser-hello.webp` — Browser menampilkan 127.0.0.1:5001 dengan halaman Hello, World!


---

# Praktik · Part 2

## 10. Buat folder templates dan static

*Praktikum · Part 2 — struktur folder*

- Buat dua folder di root proyek: templates/ untuk HTML, dan static/ (isi css/ dan images/) untuk file pendukung. Flask otomatis mencari kedua nama ini — jangan diganti.
- Struktur akhir
- PrakPemWeb/
- ├── app.py
- ├── templates/
- │ └── index.html
- └── static/
- ├── css/
- │ └── style.css
- └── images/
- p2 03
- Folder sudah dibuat
- templates, static/css, static/images

**Gambar:**
`img/p2-04-struktur-folder.webp` — VS Code Explorer menampilkan folder static/css, static/images, templates/index.html, dan app.py di dalam PrakPemWeb

## 11. Isi style.css dan index.html

*Praktikum · Part 2 — isi file*

- static/css/style.css
- * { margin: 0; padding: 0; box-sizing: border-box; }
- body {
- font-family: Arial, sans-serif;
- line-height: 1.6;
- background-color: #f4f4f4;
- }
- header {
- background-color: #35424a;
- color: white;
- padding: 20px;
- text-align: center;
- }
- main {
- max-width: 800px;
- margin: 20px auto;
- padding: 20px;
- background: white;
- border-radius: 5px;
- }
- footer {
- text-align: center;
- padding: 10px;
- background-color: #35424a;
- color: white;
- }
- templates/index.html
- <!DOCTYPE html>
- <html lang="id">
- <head>
- <meta charset="UTF-8">
- <title>PrakPemWeb - Pertemuan 2</title>
- <link rel="stylesheet"
- href="{{ url_for('static',
- filename='css/style.css') }}">
- </head>
- <body>
- <header>
- <h1>Struktur Project Flask</h1>
- </header>
- <main>
- <h2>Struktur Folder:</h2>
- <ul>
- <li><strong>app.py</strong> - utama</li>
- <li><strong>templates/</strong> - HTML</li>
- <li><strong>static/css/</strong> - CSS</li>
- <li><strong>static/images/</strong> - gambar</li>
- </ul>
- </main>
- <footer><p>Praktikum Pemrograman Web - P2</p></footer>
- </body>
- </html>
- Perhatikan url_for('static', filename='css/style.css') — jalur relatif ke folder static, bukan jalur biasa.


---

# Praktik · Part 3

## 12. Ganti isi route dengan render_template

*Praktikum · Part 3 — render template*

- app.py
- klik barisnya
- 1
- from flask import Flask, render_template
- 3
- app = Flask(__name__)
- 5
- @app.route('/')
- 6
- def index():
- 7
- return render_template('index.html')
- 9
- if __name__ == '__main__':
- 10
- app.run(debug=True)
- Baris
- 7
- ·
- return render_template('index.html')
- Flask mengambil templates/index.html dan mengirimkannya sebagai halaman jadi — inilah cara kerja template.
- p2 04
- render_template dipakai
- HTML dikirim lewat template, bukan string

**Gambar:**
`img/p2-05-render-template.webp` — VS Code menampilkan app.py dengan from flask import Flask, render_template dan return render_template index.html disorot

## 13. Halamannya sekarang dari index.html

*Praktikum · Part 3 — lihat hasilnya*

- Buka 127.0.0.1:5001 (atau port yang muncul di baris Running on). Kali ini yang tampil bukan lagi teks polos, tapi halaman HTML yang sudah diberi CSS. Coba ubah teks di index.html, simpan, dan karena debug mode — halamannya berubah tanpa restart.
- 127.0.0.1:5001
- PrakPemWeb
- Struktur Project Flask
- halaman dari templates/index.html
- p2 05
- Hasil render di browser
- HTML + CSS tampil rapi di 127.0.0.1:5001

**Gambar:**
`img/p2-06-browser-render.webp` — Browser menampilkan halaman Struktur Project Flask di alamat 127.0.0.1:5001 hasil render template


---

# Praktik · Part 4

## 14. Buat akun GitHub

*Praktikum · Part 4 — akun GitHub*

- Buka github.com/signup, isi email, password, dan username. Verifikasi email, lalu kamu langsung masuk ke Dashboard — halaman utama berisi daftar repo.
- github.com/signup
- Belum punya akun? Selesaikan dulu sebelum lanjut — langkah SSH di slide berikutnya butuh akun ini.
- p2 06
- Dashboard GitHub
- halaman utama setelah login

**Gambar:**
`img/p2-07-github-dashboard.webp` — Dashboard GitHub dengan daftar top repositories NetMedix, catat-keuangan, dan tombol New

## 15. git config: nama & email kamu

*Praktikum · Part 4 — kenalkan diri ke Git*

- Sebelum membuat commit, Git harus tahu siapa yang menulisnya. Sekali saja, berlaku untuk semua proyek (--global).
- Windows
- Linux / macOS
- Kenapa wajib
- Setiap commit menempelkan nama & email ini. Kalau kosong, Git akan menolak atau commit-mu tidak terhubung ke akun GitHub.
- sekali saja

**Terminal — PrakPemWeb — konfigurasi Git**

```
PS C:\Users\user\PrakPemWeb> git
```

## 16. Buat kunci SSH ke GitHub

*Praktikum · Part 4 — kunci SSH*

- Windows
- Linux / macOS
- p2 07
- Kunci publik SSH
- id_ed25519.pub — yang disalin ke GitHub

**Terminal — buat kunci SSH**

```
PS C:\Users\user\PrakPemWeb> ssh
```

**Gambar:**
`img/p2-08-ssh-keygen.webp` — Terminal Linux menampilkan isi folder .ssh dan perintah cat id_ed25519.pub

## 17. Settings → SSH and GPG keys

*Praktikum · Part 4 — tempel kunci di GitHub*

- Di GitHub, buka menu profil (kanan atas) → Settings → SSH and GPG keys. Dari sini kita menambahkan kunci publik yang tadi disalin.
- p2 08
- Buka Settings
- menu profil kanan atas
- p2 09
- SSH and GPG keys
- menu kiri, bagian Access
- p2 10
- Klik New SSH key
- default masih kosong (no keys)
- p2 11
- Isi Title & Key
- tempel isi id_ed25519.pub

**Gambar:**
`img/p2-09-github-settings.webp` — Menu profil GitHub terbuka dengan pilihan Settings disorot
`img/p2-10-ssh-gpg-menu.webp` — Menu Settings GitHub dengan pilihan SSH and GPG keys disorot
`img/p2-11-new-ssh-key.webp` — Halaman SSH keys dengan tombol New SSH key disorot
`img/p2-12-add-ssh-form.webp` — Form Add new SSH Key dengan Title SSH Github - Ubuntu dan isi Key ssh-ed25519

## 18. ssh -T: uji koneksi ke GitHub

*Praktikum · Part 4 — buktikan tersambung*

- p2 12
- Kunci tersimpan
- muncul di Authentication keys
- Windows
- Linux / macOS
- p2 13
- Berhasil terhubung
- “successfully authenticated”

**Terminal — uji koneksi SSH**

```
PS C:\Users\user\PrakPemWeb> ssh
```

**Gambar:**
`img/p2-13-ssh-added.webp` — Daftar SSH keys menampilkan SSH Github - Ubuntu yang baru ditambahkan
`img/p2-14-ssh-verify.webp` — Terminal menjalankan ssh -T git@github.com dan menampilkan pesan Hi XsafiD You've successfully authenticated


---

# Praktik · Part 5 · Pasang Git

## 19. Belum punya Git? Pasang dulu

*Praktikum · Part 5 — pasang Git*

- Jika perintah git belum dikenali di terminal, unduh dan pasang Git dari situs resminya. Setelah terpasang, cek dengan git --version.
- git-scm.com/install
- Windows
- Linux / macOS
- Windows
- Unduh installer Git for Windows, jalankan, dan biarkan semua opsi default. Setelah selesai, buka Terminal baru supaya perintah git dikenali.
- default sudah cukup

**Terminal — cek Git**

```
PS C:\Users\user\PrakPemWeb> git
```


---

# Praktik · Part 6

## 20. git init & buat .gitignore

*Praktikum · Part 6 — mulai repo lokal*

- Windows
- Linux / macOS
- git init membuat folder tersembunyi .git — di sanalah seluruh riwayat proyek disimpan.
- p2 14
- git init
- repo lokal dimulai
- p2 15
- .gitignore
- kecualikan .venv dan cache
- Konvensi umum: .venv/, __pycache__/, *.pyc, .env — file yang tidak perlu masuk repo.

**Terminal — PrakPemWeb — mulai repo**

```
PS C:\Users\user\PrakPemWeb> git
```

**Gambar:**
`img/p2-19-git-init.webp` — Terminal menjalankan git init dengan hint menggunakan nama branch master
`img/p2-20-gitignore.webp` — VS Code menampilkan file .gitignore berisi .venv, __pycache__, dan *.pyc


---

# Praktik · Part 5

## 21. Buat repo baru di GitHub

*Praktikum · Part 5 — repositori baru*

- Klik tombol New di Dashboard → beri nama Project-PrakPemWeb → pilih Public → Create repository. Setelah jadi, pilih tab SSH dan catat URL repo-nya.
- p2 16
- Tombol New
- buat repo baru
- p2 17
- Klik New
- mulai buat repo
- p2 19
- URL SSH repo
- git@github.com:XsafiD/Project-PrakPemWeb.git
- p2 18
- Beri nama repo
- Project-PrakPemWeb · Public

**Gambar:**
`img/p2-15-github-home.webp` — Dashboard GitHub dengan tombol New di bagian Top repositories
`img/p2-16-new-repo-btn.webp` — Tombol New disorot merah di dashboard GitHub
`img/p2-18-repo-ssh-url.webp` — Halaman repo baru menampilkan tab SSH dengan URL git@github.com XsafiD Project-PrakPemWeb.git
`img/p2-17-create-repo.webp` — Halaman Create a new repository dengan nama Project-PrakPemWeb dan owner XsafiD


---

# Praktik · Part 6

## 22. git add & git commit

*Praktikum · Part 6 — commit pertama*

- Windows
- Linux / macOS
- p2 20
- git add .
- tandai semua file
- p2 21
- git commit
- 4 files changed · commit pertama

**Terminal — PrakPemWeb — commit**

```
PS C:\Users\user\PrakPemWeb> git
```

**Gambar:**
`img/p2-21-git-add.webp` — Terminal VS Code menjalankan git add . pada branch master
`img/p2-22-git-commit.webp` — Terminal menjalankan git commit dengan pesan 2026-09-13 Update Pertemuan 2 dan hasil 4 files changed

## 23. Branch, remote, dan push

*Praktikum · Part 6 — kirim ke GitHub*

- Windows
- Linux / macOS
- A
- git branch -M main
- Ganti nama branch jadi main. Cukup sekali di awal.
- B
- git remote add origin …
- Hubungkan repo lokal dengan repo GitHub (pakai URL SSH).
- C
- git push -u origin main
- Unggah commit pertama ke GitHub. Cek repo-nya di browser.

**Terminal — PrakPemWeb — push ke GitHub**

```
PS C:\Users\user\PrakPemWeb> git
```


---

# Tugas

## 24. Sekarang giliran kamu

*Tugas praktikum — 30 menit*

- Struktur folder lengkap
- templates, static/css, static/js dibuat
- index.html + style.css
- Halaman HTML sederhana yang terhubung ke CSS
- Git init + commit pertama
- Repo diinisialisasi dan di-commit, siap di-push
- 0/3 selesai
- SISA WAKTU · hari : jam : menit : detik
- 07:04:57:02
- deadline: Rabu, 14 Oktober 2026, 23.59

## 25. Ketentuan & pengumpulan

*Aturan main*

- Ketentuan kode
- Proyek dikumpulkan dalam bentuk zip — seluruh folder proyek
- Folder .venv/ tidak perlu ikut (kecualikan lewat .gitignore)
- Struktur folder harus sesuai pola: templates & static
- Pengumpulan
- Upload seluruh file proyek (zip) ke LMS
- Deadline: Rabu, 14 Oktober 2026, 23.59
- Pastikan python app.py berjalan sebelum mengumpulkan — yang dinilai: yang berjalan


---

# Penutup

## 26. Kuis kilat — lima soal

*Cek pemahaman*

- Soal 1/5
- Parameter yang mengaktifkan debug mode di Flask?

## 27. Hari ini, proyek kamu naik kelas

*Recap — pertemuan 02 selesai*

- Menyalakan debug=True — auto-reload dan debugger siap menolong
- Menata proyek dengan folder templates/ dan static/
- Menyambungkan SSH dan mengirim kode ke GitHub lewat git push
- $ ex
- Tugasnya jangan lupa: struktur folder + commit pertama, upload zip ke LMS. Sampai ketemu di P03.

---

# Lampiran — Kuis (5 soal)

**1. Parameter yang mengaktifkan debug mode di Flask?**

- A. debug=True  ✅
- B. mode=debug
- C. run(debug)
- D. Flask(debug)

**2. Folder tempat Flask mencari file HTML (template)?**

- A. static/
- B. templates/  ✅
- C. html/
- D. views/

**3. Fungsi Flask untuk mengirim file HTML sebagai halaman?**

- A. render_template()  ✅
- B. send_html()
- C. load_template()
- D. html()

**4. Perintah untuk menyimpan perubahan ke riwayat Git?**

- A. git save
- B. git commit  ✅
- C. git push
- D. git store

**5. Perintah untuk mengirim commit lokal ke GitHub?**

- A. git pull
- B. git clone
- C. git push  ✅
- D. git add

_Jawaban benar ditandai centang._