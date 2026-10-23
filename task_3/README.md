# Tugas Individu 3 - Pengembangan Aplikasi Web

## Website Pendaftaran Workshop Informatika ITERA

Nama: Jana Rohman Wasiso

NIM: 123140046

Kelas: PAW RB

## 1. Deskripsi Proyek

Proyek ini adalah website pendaftaran peserta Workshop Informatika ITERA yang dibuat menggunakan HTML5 dan CSS3. Website mempunyai dua halaman, yaitu formulir pendaftaran dan halaman data peserta.

Formulir memakai method `GET`, sehingga data yang diisi muncul sebagai query string pada URL halaman detail. Halaman detail tidak membaca query string tersebut dan tetap menampilkan data dummy yang ditulis langsung di HTML.

## 2. Struktur Folder

```text
Tugas3-PAW/
└── task_3/
    ├── index.html
    ├── detail.html
    ├── style.css
    └── README.md
```

- `index.html` berisi formulir pendaftaran workshop.
- `detail.html` berisi tabel data peserta dummy.
- `style.css` mengatur tampilan kedua halaman.

## 3. Penjelasan Halaman

### Halaman Pendaftaran

Form pada `index.html` menggunakan kode berikut.

```html
<form action="detail.html" method="get">
```

`action` menentukan halaman tujuan, sedangkan `method="get"` mengirimkan data melalui query string. Formulir memiliki lima isian wajib, yaitu nama lengkap, NIM, email, program studi, dan pilihan workshop.

Setiap input memiliki atribut `name` sebagai nama parameter. NIM menggunakan `pattern="[0-9]+"` dan `inputmode="numeric"`, sedangkan email menggunakan `type="email"` agar browser melakukan pemeriksaan format dasar.

### Halaman Data Peserta

`detail.html` menampilkan tabel data peserta dalam enam kolom: nomor, nama, NIM, email, program studi, dan workshop. Tabel berisi tiga data dummy yang dibuat langsung pada HTML.

Halaman ini tetap menampilkan data dummy walaupun URL menerima query string dari formulir. Tidak ada JavaScript atau database yang dipakai untuk memproses data tersebut.

## 4. Penggunaan CSS

File `style.css` dipakai oleh kedua halaman agar tampilan tetap sama. Beberapa selector yang digunakan adalah selector tag seperti `body` dan `table`, selector class seperti `.container` dan `.form-card`, selector atribut `input[type="email"]`, serta pseudo-class seperti `button:hover` dan `tbody tr:nth-child(even)`.

Layout halaman pendaftaran menggunakan CSS Grid. Formulir menggunakan Flexbox dengan `flex-direction: column` supaya label dan input tersusun ke bawah. Padding, margin, border, dan border-radius dipakai untuk membentuk kartu konten dan membuat tampilan lebih rapi.

Tabel menggunakan `border-collapse: collapse`, warna selang-seling pada baris genap, dan efek hover. Pada layar kecil, media query mengatur layout menjadi satu kolom dan tabel dapat digeser secara horizontal.

## 5. Query String GET

Contoh data yang diisi:

- Nama: Jana Rohman Wasiso
- NIM: 123140046
- Email: jana@example.com
- Program Studi: Informatika
- Workshop: Dasar Pemrograman Web

Setelah tombol **Kirim Pendaftaran** ditekan, URL menjadi seperti berikut.

```text
detail.html?nama=Jana+Rohman+Wasiso&nim=123140046&email=jana%40example.com&prodi=Informatika&workshop=Dasar+Pemrograman+Web
```

Tanda `?` memulai query string, `&` memisahkan parameter, dan `=` memisahkan nama parameter dengan nilainya.

## 6. Cara Menjalankan

1. Buka folder `task_3` melalui Visual Studio Code atau file explorer.
2. Jalankan `index.html` di browser atau menggunakan Live Server.
3. Isi formulir dan tekan tombol **Kirim Pendaftaran**.
4. Periksa URL halaman detail untuk melihat query string yang terbentuk.

## 7. Kesimpulan

Website ini menerapkan form HTML, method GET, query string, tabel, CSS selector, layout, dan tampilan responsif. Website dibuat tanpa JavaScript maupun database karena halaman detail hanya digunakan untuk menampilkan data dummy.
