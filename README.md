# Jarkom_Modul1_Lapres_D14

### KELOMPOK        : D14
ANGGOTA         :

* Muhammad Haris W.     (05111840000029)
* Vieri Fath Ayuba      (05111840000153)

## Jawaban Soal Praktikum Jarkom Modul 1
#


### 1) Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

* Pertama, kita harus mencari http.host di display capture dengan filter command "http.host == testing.mekanis.me"
* Setelah itu klik kanan -> klik follow --> klik TCP Stream 
* Disitu dapat dilihat webserver yang digunakan pada "testing.mekanis.me" yaitu nginx/1/14/0 (Ubuntu)

### 2) Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

* Pertama, kita memilih file --> Export Object --> HTTP.
* Ketika HTTP Object listt muncul, ketik "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg" pada kolom text filter.
* Setelah itu, pilih file tersebut dan klik save pada direktori yang diinginkan.
* File gambar tersimpan.

### 3) Cari username dan password ketika login di "ppid.dpr.go.id"!

* Pertama, kita harus mencari http.host "ppid.dpr.go.id "dan mencari http request method dengan method "POST". Command display filternya sebagai berikut "http.host == ppid.dpr.go.id and http.request.method == POST.
* Kemudian dilihat detail packetnya di kolom "HTTP Form URL Encode", di kolom tersebut terlihat username dan password untuk login.
* Username : "10pemuda" , Password : "guncangdunia"

### 4) Temukan paket dari web-web yang menggunakan basic authentication method!

* Untuk menemukan paket dari web-web yang menggunakan basic authentication method menggunakan command display filter : http.authbasic

### 5) Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!











## No 8

Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

Pertama mencari ip daripada Microsoft FTP itu sendiri dengan ftp contains "Microsoft FTP"
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no8a.png" >

Lalu gabungkan dengan ftp.request.command == RETR and ip.addr == 198.246.117.106
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no8b.png" >

## no 9

Untuk mencari User gunakan ftp.request.command == USER
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no9a.png" >

Sedangkan untuk mencari Password gunakan ftp.request.command == PASS
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no9b.png" >

## no 10

Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46"

Menggunakan perintah frame contains "application/pdf"
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no10a.png" >

Kemuduan Follow TCP Stream dan arahakan pada RAW lalu simpan dalam bentuk pdf
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no10b.png" >

Ini adalah tampilan dari file pdf tersebut
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no10c.png" >


# Capture Filter

## no 11

Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

Menggunakan filezilla karena port 21 digunakan dalam protokol ftp

Mencoba upload file lewat filezilla
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no11a.png" >

Maka akan ditemukan lalu lintas data pada port 21
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no11b.png" >

## No 12

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

Menggunakan command tcp src port 80

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no12.png" >

## No 13

Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

Menggunakan command tcp dst port 443

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no13.png" >

## No 14

Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Mencari ip kita dengan command di cmd ipconfig/all

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no14a.png" >

Setelah di temukan ipnya, lalu menuliskan ip src 192.168.0.104

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no14b.png" >

## No 15

Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

Menggunakan command dst host monta.if.its.ac.id

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no15.png" >






Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
Cari username dan password ketika login FTP pada localhost!
Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46" 
