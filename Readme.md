# Jarkom-Modul-1-IT23-2024

| Nama | NRP |
| ---- | ---- |
| Etha Felisya Br Purba | 5027221017 |
| Rahmad Aji Wicaksono | 5027221034 |

## Challenges
  - [Creds] 
  - [ATM or ATP or FTP ? 🤔] 
  - [whoami] 
  - [malwleowleo] 
  - [How Many packets?] 
  - [trace him] 
  - [evidence] 
  - [fuzz] 
  - [secret] 
  - [malwaew] 

## Challenges Completion

### ! creds
> Attacker menyadari jika dia bisa membuat clone ftp server dari target, temukan kredensial dari server ftp yang dibuat oleh attacker.

Langkah:
  1. Masukkan nc 10.15.40.20 10007
  2. Apa username ftp yang digunakan oleh attacker?
     hal pertama yang terpikirkan adalah memfilter dengan filter **tcp.len>0** yang langsung menampilkan hanya paket yang ada isinya.
     pada beberapa paket sudah ketemu username ftp yang digunakan oleh attacker.
     <img src="attachment/creds1.jpeg">
  3. Apa password ftp yang digunakan oleh attacker?
     hal pertama yang saya lakukan yaitu melakukan **follow TCP Stream** pada paket yang berisi kredensial username.
     melihat isi stream ke 2 langsung ketemu password ftp yang digunakan oleh attacker.
     <img src="attachment/creds2.jpeg">
  4. Setelah menjawab beberapa pertanyaan tersebut flag berhasil didapatkan.
     <img src="attachment/creds3.jpeg">

### ! ATM or ATP or FTP ? 🤔
> Pradityo mencoba mengembangkan server ftp, tetapi seseorang mencoba melakukan bruteforce login, bisakah anda menganalisis apa yang terjadi?

Langkah:
  1. Masukkan nc 10.15.40.20 10004
  2. Apa password yang berhasil didapatkan oleh hacker setelah melakukan bruteforce login ftp?
     filter yang saya gunakan pertama yaitu **tcp.len>0** kemudian mencari dengan filter **frame contains "Login"**.
     setelah itu scroll kebawah hingga menemukan login successful.
     <img src="attachment/atm-or-atp-or-ftp1.jpeg">
  3. Setelah menjawab pertanyaan tersebut flag akan didapatkan.
     <img src="attachment/atm-or-atp-or-ftp2.jpeg">

### whoami
Dapatkah kamu menemukan siapa identitas attacker?
1. Buka cmd dan input command **ncat 10.15.40.20 10009** maka soalnya akan muncul seperti dibawah
<img src="attachment/whoami1.jpeg">
2. Buka attachment yang sama dengan yang ada pada soal creds, dan follow TCP Stream
<img src="attachment/whoami2.jpeg">
3. Saya menemukan string seperti berikut
<img src="attachment/whoami3.jpeg">
4. Setelah string tersebut didecode ditemukan pesan seperti dibawah
<img src="attachment/whoami4.jpeg">
5. Masukkan nama attacker sesuai dengan format yang diminta dan flag dapat diperoleh
<img src="attachment/whoami5.jpeg">

### secret
Temukan pesan rahasia dari attacker
1. Buka cmd dan input command **ncat 10.15.40.20 10010** maka soalnya akan muncul seperti dibawah
<img src="attachment/secret1.jpeg">
2. Gunakan filter STOR untuk memfokuskan pada aktivitas pengiriman file dalam koneksi FTP.
<img src="attachment/filter2.jpeg">
Selain malicious file pada pertanyaan sebelumnya, ditemukan juga mirza.jpg
<img src="attachment/secret+.jpeg">
3. Download file tersebut dengan cara klik file dan export objects dan pilih FTP DATA
<img src="attachment/secret3.jpeg">
kemudian klik file mirza.jpg dan save
<img src="attachment/secret4.jpeg">
4. Buka file yang telah di download dan pesan ditemukan
<img src="attachment/secret5.jpeg">
5. Masukkan pesan ke cmd dan flag diperoleh
<img src="attachment/secret6.jpeg">

