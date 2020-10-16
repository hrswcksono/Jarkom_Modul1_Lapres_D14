# Jarkom_Modul1_Lapres_D14

## no 8

Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

Pertama mencari ip daripada Microsoft FTP itu sendiri dengan FTP contains "Microsoft FTP"
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no8a.png" >

Lalu gabungkan dengan ftp.request.command == RETR and ip.addr == 198.246.117.106
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no8b.png" >

## no 9

Untuk mencari User gunakan ftp.request.command == USER
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no9a.png" >

Sedangkan untuk mencari Password gunakan ftp.request.command == PASS
<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no9b.png" >



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

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no12.png" >

## No 13

Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no13.png" >

## No 14

Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Mencari ip kita dengan command di cmd ipconfig/all

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no14a.png" >

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no14b.png" >

## No 15

Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

<img src="https://github.com/hrswcksono/Jarkom_Modul1_Lapres_D14/blob/main/gambar/no15.png" >