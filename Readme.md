# Laporan Soal Shift Jaringan Komputer Modul 1

## Kelompok D11

- Afira Rolobessy         5025201006
- Beryl                   5025201029
- Warren Gerald Polandra  5025201233

## Pembagian Tugas:
- Afira: Soal 1-3
- Beryl: Soal 4-7
- Warrren: Soal 8-10

## Soal 1
Web server pada monta.if.its.ac.id
-	Dapat dilihat dengan membuka command prompt
-	Kemudian mengetikkan “Tracert monta.if.its.ac.id”
-	Di sebelah kanan nama web akan ada IP address untuk web server tersebut
-	Web server yang digunakan adalah Nginx
-	Dokumentasi

![hasil 1](https://github.com/AfiraRolobessy03/gambar-modul-1-jarkom/blob/main/image.png)


## Soal 2
Judul TA yang dibuka oleh Ishaq (Halaman 1):  Evaluasi unjuk kerja User Space Filesystem (FUSE)

Cara menemukan judul TA:
-	Dowload File soal dan file *.pcapng dapat di-download di drive.
-	Klik file menggunakan Wireshark
-	Akan muncul index.php/topik/detailTopik/194\
-	Dokumentasi:

![hasil 1](https://github.com/AfiraRolobessy03/gambar-modul-1-jarkom/blob/main/2.png)

-	Jadi judul TA apa yang dibuka oleh ishaq adalah melalui web monta.if.its.ac.id http://monta.if.its.ac.id/index.php/topik/detailTopik/194 Evaluasi unjuk kerja User Space Filesystem (FUSE)

![](https://github.com/AfiraRolobessy03/gambar-modul-1-jarkom/blob/main/3.png)

## Soal 3
3.	Filter wireshark untuk menampilkan paket yang menuju port 80:

-	Download File soal dan file *.pcapng dapat di-download di drive.
-	Buka file soal3-6.pcapng menggunakan Wireshark
-	Masukkan filter tcp.dstport == 80
-	Dokumentasi

![](https://github.com/AfiraRolobessy03/gambar-modul-1-jarkom/blob/main/4.png)

## Soal 4
**Soal:**
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

**Langkah:**
1. Download File soal dan file *.pcapng dapat di-download di drive.
2. Buka file soal3-6.pcapng menggunakan Wireshark
3. Masukkan filter tcp.srcport==21
4. Dokumentasi:

![](https://cdn.discordapp.com/attachments/1023246973551255652/1023247271753695243/unknown.png)

## Soal 5
**Soal:**
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

**Langkah:**
1. Download File soal dan file *.pcapng dapat di-download di drive.
2. Buka file soal3-6.pcapng menggunakan Wireshark
3. Masukkan filter tcp.srcport==443
4. Dokumnetasi:

![](https://cdn.discordapp.com/attachments/1023246973551255652/1023247546983911485/unknown.png)

## Soal 6
**Soal:**
Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !

**Langkah:**
1. Masukkan display filter “ip.dst == lipi.go.id”
2. Maka wireshark akan menampilkan semua paket yang menuju lipi.go.id
3. Dokumentasi:

![](https://cdn.discordapp.com/attachments/1023246973551255652/1023247715913695262/unknown.png)


## Soal 7
**Soal:**
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

**Langkah:**
1. Cari alamat ip di windows settings
2. Buka wireshark dan masukkan capture filter: “ip.src = 192.168.0.166”
3. Maka wireshark hanya akan menangkap paket yang berasal dari alamat ip kami sendiri
4. Dokumentasi:

![](https://cdn.discordapp.com/attachments/1023246973551255652/1023248269868028044/unknown.png)


## Soal 8

**Soal:**
Cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum

**Cara Pengerjaan:**
1. Gunakan display filter: “ip.src == localhost or ip.dst == localhost && tcp.flags.push == 1 && tcp.port == 65432”
2. Filter "ip.src == localhost or ip.dst == localhost" akan semua menangkap paket yang berasal dari atau menuju localhost
3. Filter "tcp.flags.push == 1" digunakan untuk mencari paket yang memiliki flag [PSH]
4. "tcp.port == 65432" digunakan untuk mencari paket yang berasal dari atau menuju port 65432 (ditemukan setelah melihat pola paket)
5. Akan ditemukan semua paket yang berisi data informasi kecurangan tersebut
6. Kita dapat mem-follow TCP stream pada salah satu paket tersebut kemudian akan ditampilkan seluruh percakapan tersebut
7. Dokumentasi:

![Soal 8a](https://cdn.discordapp.com/attachments/856609726225973278/1023269443528298526/unknown.png)

![Soal 8b](https://cdn.discordapp.com/attachments/856609726225973278/1023270138969067651/unknown.png)

## Soal 9

**Soal:**
Carilah pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”

**Cara Pengerjaan:**
1. Dari soal no. 8 didapatkan bahwa pertukaran file dilakukan pada port 9002
2. Dapat dilakukan filtering dengan filter "tcp.port == 9002"
3. Dari filter tersebut, paket yang ada dapat di-follow TCP streamnya hingga terdapat paket yang mengandung data sebesar 56 byte yaitu "Salted__.:....B(......$E...K)..<<......f ......B.G4..+.."
4. File tersebut kemudian dapat diubah ke raw dan disave dengan nama "D11.des3"
5. Dokumentasi:

![Soal 9a](https://cdn.discordapp.com/attachments/856609726225973278/1023272134027522109/unknown.png)

## Soal 10

**Soal:**
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!

**Cara Pengerjaan:**
1. Dari soal no. 8, ditemukan hint bahwa password dari file tersebut adalah sebuah anime kembar lima
2. Dengan mencari informasi di paket lainnya, ditemukan bahwa passwordnya adalah kesamaan dari anime kembar lima tersebut, yaitu nama belakang dari kelima karakter anime tersebut yang bernama "nakano"
3. Sesuai dengan hint dari no. 8, kami memasukkan syntax "openssl des3 -d -salt -in D11.des3 -out flag.txt" untuk mendapatkan flagnya
4. Kemudian kami memasukkan password "nakano"
5. Flag yang kami dapatkan adalah "JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}"
6. Dokumentasi:
![Soal 10a](https://cdn.discordapp.com/attachments/856609726225973278/1023273758871539732/unknown.png)

![Soal 10b](https://cdn.discordapp.com/attachments/856609726225973278/1023274076439052418/unknown.png)
