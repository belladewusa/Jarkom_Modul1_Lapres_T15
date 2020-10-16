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



### NO2
Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

**Jawaban:**

Klik pada File > export object > http > filter Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg > download


**screenshot**

![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%202.png)
![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%202a.png)
![no2](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%202b%20Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg)


### NO3
Cari username dan password ketika login di "ppid.dpr.go.id"!

**Jawaban:**

```
http.host == ppid.dpr.go.id && hhtp.request.method == POST
```

1. Langkah yang harus dilakukan adalah meletakkan filter command ```http.host == ppid.dpr.go.id && hhtp.request.method == POST```
2. Lalu akan terlihat packet yang dicari.
3. Pada bagian HTML Form URL Encoded, terlihat username ```10pemuda```  dan password ```guncangdunia```

**Screenshot:**

![no3](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%203.png)


### NO4
Temukan paket dari web-web yang menggunakan basic authentication method!

**Jawaban:**

Cara yang pertama : 
Ketikan command berikut pada display filter
```
http.authbasic
```
Lalu enter, maka akan muncul web yang menggunakan basic authentication method

Cara lainnya :
Klik edit > find packet > ketik credential > ubah ke string > packet details > lalu find
Maka akan muncul berbagai paket yang mengandung basic authentication method

**Screenshot:**

![no4](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%204.png)
![no4](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%204b.png)


### NO5
Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

**Jawaban:**

```
http.host == aku.pengen.pw
```
Follow http > dapat code basch64 > kemudian di decrypt
Setelah didapatkan hasilnya, segera buka web aku.pengen.pw
Akan diminta username dan password, kemudian di isi dengan code hasil decrypt sebelumnya , yaitu kakakgamtenk:hartatahtabermuda
Setelah berhasil masuk diminta sebutkan urutan konfigurasi pengkabelan T568B , kemudian di SS


**Screenshot:**

![no1](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%205.png)

![no1](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%205a.png)

![no1](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%205b.png)




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



### NO8
Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

**Jawaban:**

Untuk mencari IP Microsoft FTP Service input command berikut ke display filter

```
ftp contains “Microsoft”
```

Setelah didapatkan kita mencari objek apa saja yang didownload dari IP tersebut dengan command berikut
```
ftp.request.command contains "RETR" && ip.dst == 198.246.117.106
```

**Screenshot:**

![no8](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%208.png)
![no8](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%208a.png)



### NO9
Cari username dan password ketika login FTP pada localhost!

**Jawaban:**

```
ftp.request.command == USER || ftp.request.command == PASS
```

Setelah dimasukan commandnya lalu tekan enter , maka langsung terlihat USER dhana PASS dhana123

**Screenshot:**

![no9](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%209.png)


### NO10
Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46"

**Jawaban:**

Langkah-langkahnya
1. Ctrl+F 
2. input clue : 25 50 44 46
3. ubah jadi hex value 
4. klik enter atau find
5. Akan langsung terlihat paketnya lalu klik kanan pada mouse > follow tcp stream > ubah ke raw lalu save as (langsung download) dengan menyimpan format .pdf

**Screenshot:**

![no10](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%2010.png)

![no10](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%2010a.png)






## Capture Filter
### NO11 
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

**Jawaban:**

```
port 21
```

**Screenshot:**

![no10](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%2010.png)

![no10](https://github.com/belladewusa/Jarkom_Modul1_Lapres_T15/blob/main/Display%20Filter/no%2010.png)

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





