# Laporan Soal Shift Jaringan Komputer Modul 1

## Kelompok D11

- Afira Rolobessy         5025201006
- Beryl                   5025201029
- Warren Gerald Polandra  5025201233

## Soal 1
Web server pada monta.if.its.ac.id
-	Dapat dilihat dengan membuka command prompt
-	Kemudian mengetikkan “Tracert monta.if.its.ac.id”
-	Di sebelah kanan nama web akan ada IP address untuk web server tersebut
-	Web server yang digunakan adalah Nginx
-	Dokumentasi
![](https://github.com/AfiraRolobessy03/gambar-modul-1-jarkom/blob/main/image.png)


## Soal 2
2.	Judul TA yang dibuka oleh Ishaq (Halaman 1):  Evaluasi unjuk kerja User Space Filesystem (FUSE)
Cara menemukan judul TA:
-	Dowload File soal dan file *.pcapng dapat di-download di drive.
-	Klik file menggunakan Wireshark
-	Akan muncul index.php/topik/detailTopik/194\
-	Dokumentasi:

![](https://github.com/AfiraRolobessy03/gambar-modul-1-jarkom/blob/main/2.png)
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
4. Dokumentasi

## Soal 5
**Soal:**
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

**Langkah:**
1. Download File soal dan file *.pcapng dapat di-download di drive.
2. Buka file soal3-6.pcapng menggunakan Wireshark
3. Masukkan filter tcp.srcport==443
4. Dokumnetasi

## Soal 6
**Soal:**
Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !

**Langkah:**
1. Masukkan display filter “ip.dst == lipi.go.id”
2. Maka wireshark akan menampilkan semua paket yang menuju lipi.go.id
3. Dokumentasi:


## Soal 7
**Soal:**
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

**Langkah:**
1. Cari alamat ip di windows settings
2. Buka wireshark dan masukkan capture filter: “ip.src = 192.168.0.166”
3. Maka wireshark hanya akan menangkap paket yang berasal dari alamat ip kami sendiri
4. Dokumentasi:


## Soal 8

## Soal 9

## Soal 10
