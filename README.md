# Sistem Manajemen Perpustakaan Kampus

Program Java berbasis konsol (menu interaktif dengan `Scanner`) untuk mengelola koleksi buku, lokasi penyimpanan, antrean peminjam, dan riwayat transaksi pada perpustakaan kampus. Program ini mengintegrasikan enam struktur data: Array 1D, Array 2D, Array 3D, ArrayList, Stack, dan Queue.

## Tugas Pemrograman Java
- ***Mata Kuliah:*** Pemrograman Berorientasi Objek
- ***Dosen Pengampu:*** M. Ibadurrahman Arrasyid Supriyanto M.Kom.
- ***Program Studi:*** Sistem Informasi
- ***Angkatan:*** 2025 dan 2024
- ***Kelompok:*** 9

## Anggota Kelompok 9
1. **Marza Hanaya Melodya Goga** - 2409116103 - Kelas C
2. **Ahmad Fajar Novia** - 2509116041 - Kelas B
3. **Harits** - 2509116048 - Kelas B
4. **Farah Hikmatul Maula** - 2509116099 - Kelas C

## Fitur dan Penerapan Struktur Data

| No | Struktur Data | Variabel | Penerapan |
|----|---------------|----------|-----------|
| 1 | Array 1D | `String[] KATEGORI` | Menyimpan daftar kategori buku: Pemrograman, Matematika, Jaringan Komputer, Basis Data |
| 2 | Array 2D | `int[][] peminjaman` | Menyimpan jumlah peminjaman berdasarkan kategori (baris) dan hari dalam seminggu (kolom) |
| 3 | Array 3D | `String[][][] lokasi` | Merepresentasikan lokasi buku berdasarkan lantai, nomor rak, dan posisi (2 lantai, 3 rak, 4 posisi) |
| 4 | ArrayList | `ArrayList<Buku> daftarBuku` | Mengelola daftar buku secara dinamis: tambah, tampilkan, dan hapus buku |
| 5 | Stack (LIFO) | `Stack<Transaksi> riwayat` | Menyimpan riwayat transaksi pinjam/kembali; transaksi terakhir dapat dilihat atau dibatalkan |
| 6 | Queue (FIFO) | `Queue<String> antrean` | Mengelola antrean mahasiswa yang ingin meminjam buku sesuai urutan kedatangan |

### Keterkaitan Antarfitur
- Saat buku ditambahkan, program otomatis menempatkannya pada slot kosong pertama di **Array 3D**.
- Saat mahasiswa terdepan di **Queue** dilayani, buku berstatus dipinjam, hitungan di **Array 2D** bertambah, dan transaksi dicatat ke **Stack**.
- Saat transaksi terakhir di **Stack** dibatalkan, status buku dan hitungan di **Array 2D** dikembalikan seperti semula.
- Saat buku dihapus dari **ArrayList**, slotnya di **Array 3D** dikosongkan kembali.

## Menu Program

```
===== PERPUSTAKAAN KAMPUS =====
1. Kategori buku (Array 1D)
2. Statistik peminjaman (Array 2D)
3. Denah lokasi buku (Array 3D)
4. Kelola buku (ArrayList)
5. Antrean peminjam (Queue)
6. Kembalikan buku
7. Riwayat transaksi (Stack)
0. Keluar
```

## Struktur File Proyek

```
PerpustakaanKampus-Java-Kelompok-9/
├── PerpustakaanKampus.java   
├── model/
│   ├── Buku.java              
│   └── Transaksi.java                         
└── README.md
```



## Data Awal

Program berjalan dengan 4 buku contoh:

| Kode | Judul | Kategori |
|------|-------|----------|
| B001 | Dasar Pemrograman Java | Pemrograman |
| B002 | Kalkulus Dasar | Matematika |
| B003 | Jaringan Komputer | Jaringan Komputer |
| B004 | Sistem Basis Data | Basis Data |

## Alur Contoh Penggunaan
1. Pilih menu **5 → 1** untuk memasukkan nama mahasiswa ke antrean.
2. Pilih menu **5 → 3** untuk melayani mahasiswa terdepan, lalu masukkan kode buku (contoh: `B001`) dan hari peminjaman.
3. Pilih menu **2** untuk melihat statistik peminjaman bertambah.
4. Pilih menu **7 → 1** untuk melihat transaksi terakhir, atau **7 → 3** untuk membatalkannya.
5. Pilih menu **6** untuk mengembalikan buku yang dipinjam.
