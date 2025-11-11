# TugasProyekSistemOperasi

1. Buat Struktur Direktori
Gunakan mkdir dan touch untuk membuat folder serta file sample.

#Buat direktori utama proyek
```
mkdir proyek_sistem_operasi
```
#Masuk ke direktori tersebut
```
cd proyek_sistem_operasi
```
#Buat subfolder
```
mkdir documents images archives logs
```
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

2. Script Organisasi File
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

3. Fungsi Pencarian
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

Kesimpulan

Perintah-perintah di atas termasuk dalam dasar administrasi sistem Linux yang umum digunakan untuk:

Manajemen file dan folder (mkdir, touch, mv, cp)

Pencarian file dan teks (find, grep)

Monitoring sistem file (ls, du, wc)

Otomatisasi laporan (echo, piping)

Semua langkah ini membentuk dasar penting dalam pengelolaan sistem operasi berbasis Linux.
