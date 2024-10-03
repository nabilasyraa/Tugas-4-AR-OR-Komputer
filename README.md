Nama : Nabila Asyura Chandra Putri

NIM : 09030582327098

Kelas : TK3C

Mata Kuliah : Arsitektur dan Organisasi Komputer 4

# Praktikum 1 Instalasi Sistem Operasi Linux

## 1. Buatlah laporan proses instalasi di computer mahasiswa dan tampilkan screenshotnya.

1. Download system operasi Linux Ubuntu 24.04.01 LTS (https://ubuntu.com/download/desktop)
![Screenshot 2024-10-03 201520](https://github.com/user-attachments/assets/e7166bae-a0a6-4ed1-ba8c-002fa5dc743d)

2. Gunakan aplikasi virtualisasi/emulator system operasi seperti VirtualBox, lalu klik _**New**_
![Screenshot 2024-10-03 212151](https://github.com/user-attachments/assets/e623a2f7-4826-4e6d-9551-1935bf6e1491)

3. Buatlah nama dan masukkan file Ubuntu pada kolom "ISO Image"
![Screenshot 2024-10-03 203017](https://github.com/user-attachments/assets/c0ce93ac-2fc6-4a4c-84d4-784d1e838225)

4. Klik _**Hardware**_, sesuaikanlah "Base Memory" dan "Processors" 
![Screenshot 2024-10-03 203121](https://github.com/user-attachments/assets/89459734-cad4-4721-bad0-632295734788)

5. Klik tombol _**Settings**_ pada menu VirtualBox
![Screenshot 2024-10-03 210405](https://github.com/user-attachments/assets/f2993aab-855e-4ae2-a507-05ddce3eb1ec)

6. Klik _**Network**_ dan pada bagian "Attached to" ganti menjadi _**Internal Network**_, lalu klik _**OK**_
![Screenshot 2024-10-03 203446](https://github.com/user-attachments/assets/3a771059-4b28-439f-b0cb-4f591edc7fb2)

7. Klik tombol _**Start**_ pada menu VirtualBox
![Screenshot 2024-10-03 210342](https://github.com/user-attachments/assets/bfbfac31-a9c4-40e6-978d-8a9d933748ae)

8. Saat keluar tampilan seperti ini, klik _**Enter**_, lalu tunggu
![Screenshot 2024-10-03 213057](https://github.com/user-attachments/assets/1814a15d-6d1c-4ffb-a12a-e6f457160980)

9. Selanjutnya, klik _**Install Ubuntu**_

10. Tunggu sampai proses selesai

11. Setelah selesai, pilih bahasa, lalu klik _**Next**_

12. Klik _**Next**_

13. Pilih "Keyboard Layout", lalu klik _**Next**_

14. Pilih "Use wired connection", lalu klik _**Next**_

15. Pilih "Install Ubuntu", lalu klik _**Next**_

16. Pilih "Interactive installation", lalu klik _**Next**_

17. Pilih "Default selection", lalu klik _**Next**_

18. Pilih "Install third-party software for graphics and Wi-Fi hardware", lalu klik _**Next**_

19. Pilih "Erase disk and install Ubuntu", lalu klik _**Next**_

20. Buatlah nama dan password akun, lalu klik _**Next**_

21. Klik _**Next**_

22. Klik _**Install**_

23. Tunggu sampai proses installasi selesai

24. Setelah proses berhasil, klik _**Restart now**_

25. Masukkan password

26. Selesai, Ubuntu sudah bisa digunakan

## 2. Analisislah pada gambar kenapa saat instalasi perlu dipilih “/” pada opsi Mount Point?
- Root Directory
Mount point “/” merepresentasikan root directory dari sistem file Linux. Ini adalah titik awal dari semua direktori dan file dalam sistem operasi. Semua partisi dan perangkat penyimpanan lainnya akan terhubung ke root directory ini, sehingga tanpa mount point ini, sistem tidak akan dapat mengakses file dan direktori lain yang diperlukan untuk berfungsi dengan baik.
- Struktur File Sistem
Linux memiliki struktur file yang terpusat di bawah satu direktori utama (root). Dengan memilih “/” sebagai mount point, kita mengatur agar semua file sistem, termasuk konfigurasi, aplikasi, dan data pengguna, terorganisir dalam satu hierarki yang jelas. Ini berbeda dengan sistem operasi lain seperti Windows, yang menggunakan beberapa drive letter (C:, D:, dll.) untuk berbagai partisi.
- Manajemen Partisi
Mount point “/” memungkinkan manajemen partisi yang lebih efisien. Misalnya, Anda dapat membuat partisi terpisah untuk /home, /var, atau /tmp, tetapi semua partisi tersebut akan tetap terhubung ke root directory. Ini memudahkan pengelolaan data dan pemisahan antara sistem operasi dan data pengguna.
- Memudahkan Akses dan Penggunaan
Dengan semua data terpusat di bawah root directory, pengguna dapat dengan mudah mengakses file dan folder tanpa perlu berpindah-pindah antar drive atau partisi. Ini meningkatkan kenyamanan dan efisiensi saat bekerja dengan sistem Linux.

## 3. Berikan penjelasan tentang ext4, ext3, swap, ntfs, fat32, btrfs!
1. ext4 (Fourth Extended File System)
  ext4 adalah sistem berkas yang dirancang untuk Linux dan merupakan penerus dari ext3. Ini adalah sistem berkas journaling yang menawarkan peningkatan dalam hal kinerja, kapasitas, dan keandalan.
Fitur Utama:
- Mendukung file hingga 16 TiB dan volume hingga 1 EiB.
- Menggunakan extents, yang memungkinkan pengelolaan ruang disk yang lebih efisien dibandingkan dengan metode pemetaan blok tradisional.
- Memiliki kemampuan untuk menangani jumlah subdirektori yang tidak terbatas dan mendukung fitur seperti subsecond timestamps dan quota journaling124.
2. ext3 (Third Extended File System)
  ext3 adalah sistem berkas journaling yang merupakan versi sebelumnya dari ext4. Ini menjadi standar untuk banyak distribusi Linux sebelum ext4 diperkenalkan.
Fitur Utama:
- Mendukung file hingga 2 TiB dan volume hingga 32 TiB.
- Memiliki tiga mode journaling: journal, ordered, dan writeback, yang memberikan fleksibilitas dalam manajemen data.
- Meskipun lebih tua, ext3 masih banyak digunakan karena kompatibilitasnya dengan ext2 dan kemudahan migrasi ke ext424.
3. Swap
  Swap bukanlah sistem berkas dalam arti tradisional, tetapi lebih merupakan area di disk yang digunakan oleh Linux sebagai memori virtual. Ini membantu mengelola memori ketika RAM penuh.
Fitur Utama:
- Memungkinkan sistem untuk "mengganti" data dari RAM ke disk untuk mengosongkan memori fisik.
- Dapat berupa partisi terpisah atau file swap di dalam sistem berkas.
- Swap membantu meningkatkan stabilitas sistem dengan mencegah kehabisan memori6.
4. ntfs (New Technology File System)
  ntfs adalah sistem berkas yang digunakan oleh Windows NT dan versi selanjutnya (Windows 2000, XP, Vista, 7, 8, 10). Ini dirancang untuk menggantikan FAT32 dengan fitur tambahan.
Fitur Utama:
- Mendukung file hingga 16 TiB dan volume hingga 256 TiB.
- Menawarkan fitur seperti enkripsi file (EFS), kompresi file, dan pemulihan data setelah kerusakan.
- Memiliki sistem izin akses yang lebih canggih dibandingkan FAT325.
5. fat32 (File Allocation Table 32)
  fat32 adalah sistem berkas yang lebih tua dibandingkan NTFS dan sering digunakan pada perangkat penyimpanan yang lebih kecil seperti flash drive dan kartu SD.
Fitur Utama:
- Mendukung file hingga 4 GiB dan volume hingga 8 TiB.
- Sederhana dan kompatibel dengan banyak sistem operasi termasuk Windows, macOS, dan Linux.
- Tidak mendukung fitur keamanan canggih seperti izin akses atau enkripsi5.
6. btrfs (B-tree File System)
  btrfs adalah sistem berkas modern untuk Linux yang dirancang untuk mengatasi kekurangan dari sistem berkas sebelumnya. Ini menawarkan fitur canggih untuk manajemen data.
Fitur Utama:
- Mendukung snapshot dan subvolume, memungkinkan pengguna untuk membuat salinan keadaan sistem secara efisien tanpa menggunakan ruang tambahan secara signifikan.
- Menyediakan integritas data melalui checksum untuk semua data dan metadata.
- Memungkinkan pengelolaan RAID secara langsung di tingkat sistem berkas tanpa memerlukan perangkat keras RAID terpisah12.
