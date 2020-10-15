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

### NO7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya ```"Yes.pdf"```

**Jawaban:**

```
ftp-data contains Yes.pdf
```

1. Menggunakan Display Filter command ```ftp-data contains Yes.pdf``` untuk mencari data yang diinginkan. 
2. Selanjutnya packet akan terlihat seperti ini: 
![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%202%20(command).jpg)
3. Langkah selanjutnya adalah memilih packet dan melakukan penelusuran lebih lanjut dengan klik kanan dan memilih submenu ```Follow```
4. Pada submenu ```Follow```, memilih submenu lagi yaitu ```TCP Stream```dan akan menampilkan seperti ini: 
![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%202%20(tcp%20follow).jpg)
5. Selanjutnya adalah men-save data. Namun perlu diperhatikan pada saat mens-save, mengubah ekstensi data pada menu ```Show and Save data as``` menjadi ```Raw```
6. Save data tersebut dengan ekstensi ```.zip```
7. Setelah disimpan, ekstrak file zip tersebut dan akan menampilkan file ```Yes.pdf```

**Screenshot:**

![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%202%20(pdf).jpg)

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





