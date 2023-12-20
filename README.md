
# 🖥🖥 Jarkom-Modul-5-D08-2023 🖥🖥

Nama Anggota | NRP
------------------- | --------------		
Timothy Hosia Budianto | 5025211098
Arif Nugraha Santosa | 5025211048

## 🟩🟩 LINK PROJECT 🟩🟩 
Link: 

## 🟩🟩 IP ADDRESS KELOMPOK D08 🟩🟩 
Pembagian Link dan tree : https://docs.google.com/spreadsheets/d/1L_yPff8Ir8eLs_33ec3aH3YuzJUVQYlne1wsLHLZlPs/edit#gid=537274600
```
AURA
auto eth0
iface eth0 inet dhcp
up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.168.0.0/20

auto eth1
iface eth1 inet static
	address 192.195.14.149
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.195.14.145
	netmask 255.255.255.252

HEITER
auto eth0
iface eth0 inet static
	address 192.195.14.150
	netmask 255.255.255.252
	gateway 192.195.14.149

auto eth1
iface eth1 inet static
	address 192.195.0.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 192.195.8.1
	netmask 255.255.252.0

GROBEFOREST
auto eth0
iface eth0 inet static
	address 192.195.8.3
	netmask 255.255.252.0
	gateway 192.195.8.1

SEIN
auto eth0
iface eth0 inet static
	address 192.195.8.2
	netmask 255.255.252.0
	gateway 192.195.8.1

TURKREGION
auto eth0
iface eth0 inet static
	address 192.195.0.2
	netmask 255.255.248.0
	gateway 192.195.0.1

FRIEREN
auto eth0
iface eth0 inet static
	address 192.195.14.146
	netmask 255.255.255.252
	gateway 192.195.14.145

auto eth1
iface eth1 inet static
	address 192.195.14.141
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.195.14.137
	netmask 255.255.255.252

STARK
auto eth0
iface eth0 inet static
	address 192.195.14.142
	netmask 255.255.255.252
	gateway 192.195.14.141

HIMMEL
auto eth0
iface eth0 inet static
	address 192.195.14.138
	netmask 255.255.255.252
	gateway 192.195.14.137

auto eth1
iface eth1 inet static
	address 192.195.12.1
	netmask 255.255.254.0

auto eth2
iface eth2 inet static
	address 192.195.14.1
	netmask 255.255.255.128

LAUBHILLS
auto eth0
iface eth0 inet static
	address 192.195.12.2
	netmask 255.255.254.0
	gateway 192.195.12.1

SCHWERMOUNTAINS
auto eth0
iface eth0 inet static
	address 192.195.14.3
	netmask 255.255.255.128
	gateway 192.195.14.1

FERN
auto eth0
iface eth0 inet static
	address 192.195.14.2
	netmask 255.255.255.128
	gateway 192.195.14.1

auto eth1
iface eth1 inet static
	address 192.195.14.133
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.195.14.129
	netmask 255.255.255.252

RICHTER
auto eth0
iface eth0 inet static
	address 192.195.14.134
	netmask 255.255.255.252
	gateway 192.195.14.133

REVOLTE
auto eth0
iface eth0 inet static
	address 192.195.14.130
	netmask 255.255.255.252
	gateway 192.195.14.129


```

## 🟩🟩 ROUTING KELOMPOK D08 🟩🟩 
```
AURA
route add -net 192.195.0.0 netmask 255.255.248.0 gw 192.195.14.150
route add -net 192.195.8.0 netmask 255.255.252.0 gw 192.195.14.150
route add -net 192.195.14.140 netmask 255.255.255.252 gw 192.195.14.146
route add -net 192.195.14.136 netmask 255.255.255.252 gw 192.195.14.146
route add -net 192.195.12.0 netmask 255.255.254.0 gw 192.195.14.146
route add -net 192.195.14.0 netmask 255.255.255.128 gw 192.195.14.146
route add -net 192.195.14.132 netmask 255.255.255.252 gw 192.195.14.146
route add -net 192.195.14.128 netmask 255.255.255.252 gw 192.195.14.146
FRIEREN
route add -net 192.195.12.0 netmask 255.255.254.0 gw 192.195.14.138
route add -net 192.195.14.0 netmask 255.255.255.128 gw 192.195.14.138
route add -net 192.195.14.132 netmask 255.255.255.252 gw 192.195.14.138
route add -net 192.195.14.128 netmask 255.255.255.252 gw 192.195.14.138

HIMMEL
route add -net 192.195.14.132 netmask 255.255.255.252 gw 192.195.14.2
route add -net 192.195.14.128 netmask 255.255.255.252 gw 192.195.14.2
```

## 🟩🟩 DHCP KELOMPOK D08 🟩🟩 
```
#A1
subnet 192.195.14.128 netmask 255.255.255.252 {
}

#A2
subnet 192.195.14.132 netmask 255.255.255.252 {
}

#A3
subnet 192.195.14.0 netmask 255.255.255.128 {
    range 192.195.14.3 192.195.14.66;
    option routers 192.195.14.1;
    option broadcast-address 192.195.14.127;
    default-lease-time 180;
    max-lease-time 5760;
}

#A4
subnet 192.195.12.0 netmask 255.255.254.0 {
    range 192.195.12.2 192.195.13.0;
    option routers 192.195.12.1;
    option broadcast-address 192.195.13.255;
    default-lease-time 180;
    max-lease-time 5760;
}

#A5
subnet 192.195.14.136 netmask 255.255.255.252 {
}

#A6
subnet 192.195.14.140 netmask 255.255.255.252 {
}

#A7
subnet 192.195.14.144 netmask 255.255.255.252 {
}

#A8
subnet 192.195.14.148 netmask 255.255.255.252 {
}

#A9
subnet 192.195.0.0 netmask 255.255.248.0 {
    range 192.195.0.2 192.195.4.0;
    option routers 192.195.0.1;
    option broadcast-address 192.195.7.255;
    default-lease-time 180;
    max-lease-time 5760;
}

#A10
subnet 192.195.8.0 netmask 255.255.252.0 {
    range 192.195.8.3 192.195.10.3;
    option routers 192.195.8.1;
    option broadcast-address 192.195.11.255;
    default-lease-time 180;
    max-lease-time 5760;
}
```

## 🟩🟩 PENYELESAIAN 🟩🟩

### ⭕ Nomor 1
topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.
### 🟢 Jawaban Nomor 1
### 1️⃣
```
ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')

iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP
```
Berikut adalah penjelasan dari syntax tersebut beserta masing-masing fungsinya:

ip -4 addr show eth0: Menampilkan informasi alamat IP untuk antarmuka jaringan eth0.

grep -oP '(?<=inet\s)\d+(\.\d+){3}': Menggunakan grep untuk mengambil alamat IP dari baris yang mengandung "inet" pada output sebelumnya.`

iptables -t nat -A POSTROUTING: Menambahkan aturan ke chain POSTROUTING pada tabel nat.

-o eth0: Menentukan antarmuka keluar (outgoing) sebagai eth0.

-j SNAT: Menyatakan bahwa rules tersebut adalah Source Network Address Translation.

--to-source $ETH0_IP: Menentukan alamat IP sumber untuk melakukan SNAT, menggunakan alamat IP yang telah diperoleh sebelumnya dari eth0.

### ⭕ Nomor 2
### 🟢 Jawaban Nomor 2
### 2️⃣ 

### ⭕ Nomor 3
### 🟢 Jawaban Nomor 3
### 3️⃣

### ⭕ Nomor 4
### 🟢 Jawaban Nomor 4
### 4️⃣ 

### ⭕ Nomor 5
### 🟢 Jawaban Nomor 5
### 5️⃣ 

### ⭕ Nomor 6
### 🟢 Jawaban Nomor 6
### 6️⃣

### ⭕ Nomor 7
### 🟢 Jawaban Nomor 7
### 7️⃣ 

### ⭕ Nomor 8
### 🟢 Jawaban Nomor 8
### 8️⃣ 

### ⭕ Nomor 9
### 🟢 Jawaban Nomor 9
### 9️⃣ 

### ⭕ Nomor 10
### 🟢 Jawaban Nomor 10
### 🔟
