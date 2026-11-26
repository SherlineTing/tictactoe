# **Tic Tac Toe Game - C++ Ncurses Implementation**

***Tugas Akhir / Final Project Pemrograman C++***

***Game Tic Tac Toe berbasis konsol menggunakan bahasa C++ dan library Ncurses. Permainan ini mendukung dua pemain lokal dengan kontrol keyboard, tampilan papan interaktif, serta sistem penyimpanan skor.***

### **📋 Daftar Isi**

1. [Latar Belakang & Studi Kasus](#latar-belakang--studi-kasus)
2. [Fitur Utama](#fitur-utama)
3. [Struktur Kode & Arsitektur](#struktur-kode--arsitektur)
4. [Prasyarat & Instalasi](#prasyarat--instalasi)
5. [Cara Kompilasi](#cara-kompilasi)
6. [Kontrol Permainan](#kontrol-permainan)
7. [File Eksternal](#file-eksternal)
8. [Credits](#credits)

### **📖 Latar Belakang & Studi Kasus**

Proyek ini dikembangkan sebagai tugas akhir mata kuliah Pemrograman C++. Tujuannya untuk menerapkan konsep dasar pemrograman C++ melalui pembuatan permainan Tic Tac Toe.

**Konsep pemrograman yang diterapkan meliputi:**

- **Array:** Menyimpan kondisi papan permainan berukuran 3 × 3.
- **Function:** Membagi program menjadi beberapa fungsi agar kode lebih terstruktur.
- **Conditional Statement:** Mengatur pergantian pemain, pemeriksaan kemenangan, dan kondisi seri.
- **Looping:** Mengatur perulangan permainan dan proses input keyboard.
- **File Handling (I/O):** Membaca dan menyimpan skor pemain melalui file "skor.txt".
- **External Library:** Menggunakan Ncurses untuk membuat tampilan permainan berbasis terminal dan menerima input keyboard.

### **✨ Fitur Utama**

- **Local Multiplayer:** Mendukung dua pemain dalam satu perangkat.
- **Interactive Game Board:** Menampilkan papan permainan berukuran 3 × 3.
- **Keyboard Navigation:** Menggerakkan kursor menggunakan tombol panah.
- **Player Marker:** Pemain X ditampilkan dengan warna merah dan pemain O dengan warna biru.
- **Win Detection:** Memeriksa kemenangan berdasarkan kombinasi baris, kolom, dan diagonal.
- **Draw Detection:** Mendeteksi kondisi seri ketika seluruh kotak terisi tanpa pemenang.
- **Score System:** Menghitung jumlah kemenangan pemain X, pemain O, dan hasil seri.
- **Persistent Score:** Menyimpan data skor ke dalam file "skor.txt" agar tetap tersedia ketika program dijalankan kembali.
- **Restart Game:** Memulai ulang permainan menggunakan tombol R.

### **🏗 Struktur Kode & Arsitektur**

Proyek ini menggunakan satu file utama untuk menyimpan seluruh kode program.

**Struktur proyek:**

`📦 Tic-Tac-Toe`

`┣ 📜 main.cpp`

`┣ 📜 skor.txt`

`┗ 📜 README.md`

**Penjelasan Komponen Program**

1. **Variabel dan Array** : Menggunakan array dua dimensi "papan[3][3]" untuk menyimpan posisi X dan O pada papan permainan. Variabel tambahan digunakan untuk menyimpan posisi kursor, giliran pemain, dan skor.

2. **Fungsi bacaSkor()** : Membaca data skor pemain dari file "skor.txt" menggunakan "ifstream".

3. **Fungsi simpanSkor()** : Menyimpan skor kemenangan pemain X, pemain O, dan jumlah seri menggunakan "ofstream".

4. **Fungsi resetPapan()** : Mengosongkan seluruh kotak permainan dan mengatur ulang posisi kursor serta giliran pemain.

5. **Fungsi tampilkanPapan()** : Menampilkan papan permainan, posisi kursor, warna simbol pemain, petunjuk kontrol, dan informasi skor menggunakan Ncurses.

6. **Fungsi cekPemenang()** : Memeriksa apakah pemain berhasil membentuk tiga simbol yang sama dalam satu baris, kolom, atau diagonal.

7. **Fungsi cekSeri()** : Memeriksa apakah seluruh kotak sudah terisi. Jika tidak ada pemenang dan papan penuh, permainan dinyatakan seri.

8. **Fungsi gerakKursor()** : Mengatur pergerakan kursor berdasarkan tombol panah pada keyboard.

9. **Fungsi mulaiGame()** : Mengatur jalannya permainan, mulai dari pergantian giliran, pemilihan kotak, pemeriksaan kemenangan, hingga kondisi seri.

10. **Fungsi main()** : Menjadi fungsi utama yang menginisialisasi Ncurses, mengatur warna, membaca skor, menampilkan menu, dan menjalankan permainan.

### **⚙ Prasyarat & Instalasi**

**Pastikan perangkat memiliki:**

- Compiler C++ seperti G++.
- Library Ncurses.
- Terminal yang mendukung Ncurses.
- Sistem operasi atau lingkungan pengembangan yang mendukung library Ncurses.

### **🛠 Cara Kompilasi**

Buka terminal pada direktori proyek, kemudian jalankan perintah:

```g++ main.cpp -o tic_tac_toe -lncurses```

**Jalankan program menggunakan:**

```./tic_tac_toe```

## 🎮 Kontrol Permainan

| Aksi | Tombol Keyboard |
|---|---|
| Bergerak ke atas | ↑ |
| Bergerak ke bawah | ↓ |
| Bergerak ke kiri | ← |
| Bergerak ke kanan | → |
| Memilih kotak | Enter |
| Mengulang permainan | R |
| Keluar dari permainan | ESC |

### **📂 File Eksternal**

**File** ```"skor.txt"```

Digunakan untuk menyimpan data skor permainan.

File akan dibuat atau diperbarui secara otomatis ketika program menyimpan skor.

**Format penyimpanan:**

`Skor_X Skor_O Seri`

**Contoh:**

`3 2 1`

**Artinya:**

- Pemain X menang sebanyak 3 kali.
- Pemain O menang sebanyak 2 kali.
- Permainan seri sebanyak 1 kali.

### **👨‍💻 Credits**

**Universitas Lampung**

| Nama | NPM |
|---|---|
| Bebby Diwa Anzani | 2617051030 |
| Sherline Ting | 2617051046 |

Dibuat dengan C++ menggunakan library Ncurses.
