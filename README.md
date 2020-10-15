# Jarkom_Modul1_Lapres_T15

Nama Anggota: 
  - Widyantari Febiyanti 05311840000030
  - Nabella Desyawulansari 05311840000039

## Display Filter

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

**Screenshot**

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





