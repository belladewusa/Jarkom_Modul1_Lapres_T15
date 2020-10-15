# Jarkom_Modul1_Lapres_T15

Nama Anggota: 
  - Widyantari Febiyanti 05311840000030
  - Nabella Desyawulansari 05311840000039

## Display Filter
### NO1
Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

**Jawaban:**

```
http.host == testing.mekanis.me
```

1. Langkah yang harus dilakukan adalah meletakkan filter command ```http.host == testing.mekanis.me```
2. Lalu akan terlihat packet yang dicari.
3. Lalu klik kanan dan memilih submenu ```Follow``` 
4. Pada submenu ```Follow```, memilih submenu lagi yaitu ```TCP Stream```
5. Akan menampilkan semua info termasuk webserver dari ```testing.mekanis.me```

**Screenshot:**

![no1](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%201.jpg)

### NO6
Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut)

**Jawaban:**

```
ftp-data
```

1. Untuk mencari file ```Answer.zip``` di FTP bisa menggunakan command ```ftp-data``` 
2. Selanjutnya adalah mencari menggunakan ```ctrl+f``` dan mencarinya dengan pilihan ```Reguler Expression``` serta keywordnya berupa ```Answer.zip```. Selanjutnya akan menampilkan packet seperti ini: 
![no6](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%206%20command%20answer.jpg)
3. Selanjutnya melakukan penulusuran dengan submenu ```Follow``` dan ```TCP Stream```
4. Untuk save data tersebut, mengubah ekstensi data pada menu ```Show and Save data as``` menjadi ```Raw```
![no6](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%206%20tcp%20flow%20answer.jpg)
5. Save data tersebut dengan ekstensi ```Answer.zip```
6. File pdf didalam folder ```Answer.zip``` membutuhkan password. Untuk mencarinya, masih menggunakan command yang sama yaitu ```ftp-data```
7. Selanjutnya adalah mencari menggunakan ```ctrl+f``` dan mencarinya dengan pilihan ```Reguler Expression``` serta keywordnya berupa ```Answer.zip```. Selanjutnya akan menampilkan packet seperti ini:
![no6](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%206%20command%20zipkey.jpg)
8. Selanjutnya melakukan penulusuran dengan submenu ```Follow``` dan ```TCP Stream```
9. Untuk save data tersebut, mengubah ekstensi data pada menu ```Show and Save data as``` menjadi ```Raw```
![no6](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%206%20tcp%20follow%20zipkey.jpg)
10. Save data password tadi dengan ekstensi ```zipkey.txt```
11. zipkey.txt akan menunjukkan bahwa password adalah: ```hey997400323051``` dan langsung dimasukkan saja didalam kolom password pdf yang berada didalam folder ```Answer.zip```
![no6](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%206%20insert%20password.jpg)
12. Akan terbuka file pdf yang dicari-cari. 

**Screenshot:**
![no6](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%206%20pdf.jpg)

### NO7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya ```"Yes.pdf"```

**Jawaban:**

```
ftp-data contains Yes.pdf
```

1. Menggunakan Display Filter command ```ftp-data contains Yes.pdf``` untuk mencari data yang diinginkan. 
2. Selanjutnya packet akan terlihat seperti ini: 
![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%207%20(command).jpg)
3. Langkah selanjutnya adalah memilih packet dan melakukan penelusuran lebih lanjut dengan klik kanan dan memilih submenu ```Follow```
4. Pada submenu ```Follow```, memilih submenu lagi yaitu ```TCP Stream```dan akan menampilkan seperti ini: 
![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%207%20(tcp%20follow).jpg)
5. Selanjutnya adalah men-save data. Namun perlu diperhatikan pada saat mens-save, mengubah ekstensi data pada menu ```Show and Save data as``` menjadi ```Raw```
6. Save data tersebut dengan ekstensi ```.zip```
7. Setelah disimpan, ekstrak file zip tersebut dan akan menampilkan file ```Yes.pdf```

**Screenshot:**

![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%207%20(pdf).jpg)

## Capture Filter
### NO11 
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

**Jawaban:**

```
port 21
```

**Screenshot:**

![no1](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Capture%20Filter/no%201.jpg)

### NO12
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

**Jawaban:**

```
src port 80
```

**Screenshot:**

Port 80 tidak muncul disembarang website. Untuk perintah No 2 kami pergi ke halaman website ```ajk.if.its.ac.id```. Command yang digunakan adalah ```src port 80``` yang berfungsi untuk menampilkan semua paket yang berasal dari port 80.

![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Capture%20Filter/no%202.jpg)

### NO13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

**Jawaban:**

```
dst port 443
```

**Screenshot:**

Port 443 banyak muncul di berbagai website. Sebagai contohnya pada nomor ini kami menggunakan halaman website ```google.com```. Command yang digunakan adalah ```dst port 443``` yang berfungsi untuk menangkap semua paket yang menuju port 443. 

![no3](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Capture%20Filter/no%203.jpg)

### NO14
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

**Jawaban:**

1. Mencari alamat IP kita. Buka cmd dan ketik ```ipconfig```
2. Setelah mendapatkan alamat IP, bisa di copy. 
3. Command yang dibutuhkan adalah ```src host <alamat IP>``` yang berfungsi untuk mencari paket yang berasal dari alamat IP kita. 

**Screenshot:**
![no4](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Capture%20Filter/no%204.jpg)

### NO 15
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

**Jawaban:**

```
dst host monta.if.its.ac.id
```

**Screenshot:**

Untuk mencari paket yang menuju alamat ```monta.if.its.ac.id```, dapat menggunakan command ```dst host <alamat tujuan>```

![no5](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Capture%20Filter/no%205.jpg)





