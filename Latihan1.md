# TugasProyekSistemOperasi
NAMA : ANSAR HALIDI

KELAS : A SI

MATKUL : SISTEM OPERASI

DOSEN : Zulhair Zidan Dj. Tamu


# 1. Buat Struktur Direktori
Gunakan mkdir dan touch untuk membuat folder serta file sample.

#Buat direktori utama proyek
```
mkdir latihan1_SistemOperasi
```
Penjelasan: Perintah mkdir (make directory) digunakan untuk membuat folder baru bernama latihan1_SistemOperasi. Folder ini akan menjadi wadah utama seluruh file proyek.

#Masuk ke direktori tersebut
```
cd proyek_sistem_operasi
```
Penjelasan: Perintah cd (change directory) digunakan untuk berpindah ke direktori proyek_sistem_operasi yang baru saja dibuat.

#Buat subfolder
```
mkdir documents images archives logs
```
Penjelasan: Perintah ini membuat empat folder sekaligus:
documents → tempat file teks atau laporan
images → tempat menyimpan gambar
archives → tempat menyimpan file arsip (.zip, .tar, dll)
logs → tempat menyimpan file log atau catatan aktivitas

#Buat 20 file sample di folder-folder itu
```
cd documents
```
```
touch doc1.txt doc2.txt doc3.txt doc4.txt doc5.txt
```
```
cd ../images
```
```
touch img1.jpg img2.jpg img3.png img4.png img5.jpg
```
```
cd ../archives
```
```
touch file1.zip file2.tar file3.gz file4.zip file5.tar
```
```
cd ../logs
```
```
touch log1.txt log2.txt log3.txt log4.txt log5.txt
```
```
cd ..
```

BERIKUT LINK DESKRIPSI HASIL DOKUMENTASI GAMBAR LANGKAH 1 :
(https://drive.google.com/file/d/1j59SnllwcJMbazUP133wuTZYkgfe9kJT/view?usp=drivesdk)

# 2. Script Organisasi File
Gunakan find, mv, dan cp untuk memindahkan file sesuai ekstensi.

#Buat folder baru untuk hasil pengelompokan
```
mkdir sorted_files
```
#Pindahkan semua file .txt ke folder documents/
```
find . -type f -name "*.txt" -exec mv {} sorted_files/ \;
```
#Salin file gambar ke folder images/
```
find . -type f \( -name "*.jpg" -o -name "*.png" \) -exec cp {} sorted_files/ \;
```

BERIKUT LINK DESKRIPSI HASIL DOKUMENTASI GAMBAR LANGKAH 2 :
(https://drive.google.com/file/d/1iGUKjFQMykxwGci9rcaUNMWQiR0zJ2Rc/view?usp=drivesdk)

# 3. Fungsi Pencarian
Gunakan find dan grep untuk mencari file berdasarkan nama, ukuran, dan isi.

#Cari file berdasarkan nama
```
find . -name "doc1.txt"
```
#Cari file berdasarkan ukuran (contoh: lebih dari 1KB)
```
find . -size +1k
```
#Cari teks di dalam file .txt
```
grep "log" -r documents/
```

BERIKUT LINK DESKRIPSI HASIL DOKUMENTASI GAMBAR LANGKAH 3 :
(https://drive.google.com/file/d/1hMbSNuHsDqcTepH41AJ_loryZKbOgGCv/view?usp=drivesdk)

4. Generate Laporan
Gunakan ls, wc, du, dan | (piping) untuk membuat laporan sistem file.

#Hitung jumlah file dan folder, lalu simpan ke report.txt
```
echo "=== LAPORAN FILE SISTEM ===" > report.txt
```
```
echo "Jumlah file:" >> report.txt
```
```
find . -type f | wc -l >> report.txt
```
```
echo "Jumlah folder:" >> report.txt
```
```
find . -type d | wc -l >> report.txt
```
```
echo "Ukuran total direktori:" >> report.txt
```
```
du -sh >> report.txt
```
```
echo "Daftar file:" >> report.txt
```
```
ls -lhR >> report.txt
```

BERIKUT LINK DESKRIPSI HASIL DOKUMENTASI GAMBAR LANGKAH 4 :
(https://drive.google.com/file/d/1JI-pq6LhxeLXX_ePAG7vVEWk5OQHyC8L/view?usp=drivesdk)

● Hasil Akhir
Setelah semua langkah dijalankan, kamu akan punya struktur seperti ini:
```
proyek_sistem_operasi/
├── archives/
├── documents/
├── images/
├── logs/
├── sorted_files/
└── report.txt
```
BERIKUT LINK DESKRIPSI HASIL DOKUMENTASI GAMBAR HASIL AKHIR :
(https://drive.google.com/file/d/1Epvu0mTfhF24x3TSJ7Ghzww_fBTaj56P/view?usp=drivesdk)

Kesimpulan

Perintah-perintah di atas termasuk dalam dasar administrasi sistem Linux yang umum digunakan untuk:

Manajemen file dan folder (mkdir, touch, mv, cp)

Pencarian file dan teks (find, grep)

Monitoring sistem file (ls, du, wc)

Otomatisasi laporan (echo, piping)

Semua langkah ini membentuk dasar penting dalam pengelolaan sistem operasi berbasis Linux.
