# Telkom University Company Profile - Praktikum
Project simulasi HTML, CSS, PHP native, MySQL/MariaDB, dan Git

Perubahan ini dibuat dari simulasi Laptop B

# Simulasi merge conflict
1. Berada pada branch main dengan working tree dalam kondisi bersih
2. Membuat branch baru bernama conflict-navbar
3. Pada branch conflict-navbar, mengubah teks menu navigasi di file includes/header.php dari Profil menjadi Tentang Kami, lalu melakukan commit
4. Kembali ke branch main dengan perintah git switch main
5. Pada branch main, mengubah baris yang sama di includes/header.php dari Profil menjadi Tentang Kampus, lalu melakukan commit
6. Melakukan merge branch conflict-navbar ke main

Saat conflict terjadi, di dalam file akan muncul penanda khusus dari Git. Isi di antara <<<<<<< HEAD dan ======= menunjukkan versi dari branch yang sedang aktif. Sementara isi di antara ======= dan >>>>>>> menunjukkan versi dari branch yang digabungkan.

![conflict](image/conflict.png)
![conflict-2](image/conflict-2.png)
![merge-conflic](image/merge-conflict.png)

# Cara Penyelesaian
1. Memilih dan ganti teks final misalnya "Profil"
2. Menghapus marker conflict (<<<<<<< HEAD, =======, >>>>>>> conflict-navbar)
3. Menyimpan file
4. Jalankan git status. File akan muncul sebagai unmerged sampai di-stage
5. Jalankan git add includes/header.php
6. Jalankan git commit untuk menyelesaikan merge
7. Jalankan project untuk memastikan navbar tetap valid

![penyelesaian-merge-conflict](image/penyelesaian-merge-conflict.png)
![penyelesaian](image/penyelesaian.png)
![penyelesaian-2](image/penyelesaian-2.png)

# Riwayat Praktikum GIT
## Hasil git log -- oneline -- graph -- decorate -- all
PS D:\laragon\www\telkom-company-profile> git log --oneline --graph --decorate --all
* b6056f0 (HEAD -> main, origin/main) docs: perbaiki gambar README
* 04f756d docs: perbaiki screenshot di README
* 344e428 docs: menambahkab dokumentasi praktikum, screenshot conflict, dan git log
* 9512f83 (tag: v1.0.0) docs: perbarui README dari Laptop B
*   4142274 merge: selesaikan conflict navbar
|\  
| * aa1a43a (conflict-navbar) feat: ubah label profil pada branch conflict
* | a09aa51 style: ubah label profil pada main
|/  
* 2817434 feat: tambahkan informasi fokus pembelajaran
* 762a179 feat: tambahkan form admin lokal untuk berita
* d5984df feat: simpan pesan kontak ke database
* 6bd19c3 feat: tambahkan daftar dan detail berita
* 98afaef feat: hubungkan database dan tampilkan program studi
* 91624e6 feat: tambahkan layout dasar dan stylesheet
* 80b4b40 chore: inisialisasi project dan dokumentasi awal

![log](image/log.png)