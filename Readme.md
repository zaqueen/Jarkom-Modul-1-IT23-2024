# Jarkom-Modul-1-IT23-2024

| Nama | NRP |
| ---- | ---- |
| Etha Felisya BR Purba | 5027221017 |
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
<img src="attachment/secret+.jpeg">
<img src="attachment/secret3.jpeg">
<img src="attachment/secret4.jpeg">
<img src="attachment/secret5.jpeg">
<img src="attachment/secret6.jpeg">

