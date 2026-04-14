# Linux Learning Notes

Catatan pribadi selama mempelajari dasar-dasar sistem operasi Linux, mencakup perintah-perintah yang sering digunakan dalam pengelolaan server dan infrastruktur.

---

## Navigasi Direktori

| Perintah | Fungsi |
|----------|--------|
| `pwd` | Menampilkan direktori aktif saat ini |
| `ls -la` | Menampilkan semua file termasuk yang tersembunyi beserta detailnya |
| `cd /path/to/dir` | Berpindah ke direktori tertentu |
| `cd ..` | Kembali satu tingkat ke direktori parent |
| `mkdir nama_folder` | Membuat folder baru |
| `mkdir -p a/b/c` | Membuat folder bertingkat sekaligus |

---

## Manajemen File

| Perintah | Fungsi |
|----------|--------|
| `cp file1 file2` | Menyalin file |
| `cp -r folder1 folder2` | Menyalin folder beserta isinya |
| `mv file1 /path/` | Memindahkan atau mengganti nama file |
| `rm file1` | Menghapus file |
| `rm -rf folder` | Menghapus folder beserta seluruh isinya |
| `cat file1` | Menampilkan isi file |
| `head -n 10 file1` | Menampilkan 10 baris pertama file |
| `tail -n 10 file1` | Menampilkan 10 baris terakhir file |
| `tail -f file1` | Memantau file secara real-time (berguna untuk log) |

---

## Manajemen Proses

| Perintah | Fungsi |
|----------|--------|
| `ps aux` | Melihat semua proses yang berjalan |
| `top` | Monitoring proses secara real-time |
| `htop` | Versi interaktif dari top (perlu install terpisah) |
| `kill PID` | Menghentikan proses berdasarkan PID |
| `kill -9 PID` | Memaksa menghentikan proses |
| `systemctl status nama_service` | Mengecek status suatu service |
| `systemctl start nama_service` | Menjalankan service |
| `systemctl stop nama_service` | Menghentikan service |

---

## Permission dan Kepemilikan

| Perintah | Fungsi |
|----------|--------|
| `chmod 755 file` | Mengubah permission file (owner: rwx, group: r-x, others: r-x) |
| `chmod +x file` | Menambahkan permission execute pada file |
| `chown user:group file` | Mengubah kepemilikan file |
| `ls -la` | Melihat permission dan kepemilikan file |

**Tabel referensi permission:**

| Angka | Permission |
|-------|-----------|
| 7 | Read + Write + Execute (rwx) |
| 6 | Read + Write (rw-) |
| 5 | Read + Execute (r-x) |
| 4 | Read only (r--) |
| 0 | Tidak ada akses (---) |

---

## Networking Dasar

| Perintah | Fungsi |
|----------|--------|
| `ip addr` | Melihat IP address pada semua interface |
| `ping google.com` | Mengecek konektivitas ke host tertentu |
| `curl http://example.com` | Mengambil konten dari URL |
| `wget http://example.com/file` | Mendownload file dari URL |
| `ss -tuln` | Melihat port yang terbuka dan service yang listening |
| `netstat -tlnp` | Alternatif dari ss untuk melihat koneksi jaringan |

---

## Disk dan Storage

| Perintah | Fungsi |
|----------|--------|
| `df -h` | Melihat penggunaan disk secara keseluruhan |
| `du -sh folder` | Melihat ukuran folder tertentu |
| `lsblk` | Melihat daftar block device (disk dan partisi) |
| `mount /dev/sdb1 /mnt` | Memasang partisi ke direktori tertentu |

---

## Package Management (Ubuntu/Debian)

| Perintah | Fungsi |
|----------|--------|
| `sudo apt update` | Memperbarui daftar package yang tersedia |
| `sudo apt upgrade` | Menginstall update untuk semua package |
| `sudo apt install nama_package` | Menginstall package baru |
| `sudo apt remove nama_package` | Menghapus package |
| `dpkg -l` | Melihat daftar semua package yang terinstall |

---

## Tentang

Repository ini dibuat sebagai referensi pribadi selama proses belajar administrasi sistem Linux. Catatan ini akan terus diperbarui seiring bertambahnya materi yang dipelajari.
