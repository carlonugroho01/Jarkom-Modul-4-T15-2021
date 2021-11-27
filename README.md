# PRAKTIKUM 4 JARINGAN KOMUNIKASI - T15

Penyelesaian Soal Shift 4 Jaringan Komunikasi 2021\
Kelompok T15
  * Muhammad Yasykur Rafii (05311940000017)
  * Stefanus Lionel Carlo Nugroho (05311940000027)

---

## Topologi pada CPT
![1](https://user-images.githubusercontent.com/34973363/143684269-ed6a0147-0198-490d-9368-5a27b45fa95d.png)

## VLSM-CPT
![2](https://user-images.githubusercontent.com/34973363/143684282-b1c02e48-0546-4cf3-b0df-6deb39e6dbeb.png)

## Topologi pada GNS3
![Untitled (1)](https://user-images.githubusercontent.com/63065991/143442143-168859e0-63b6-496f-9c44-24b562581f21.png)

## CIDR-GNS3
## Pembagian Subnet
### Langkah 1
![Jarkom Modul 4 (1)](https://user-images.githubusercontent.com/63065991/143442166-fdd46806-186d-4cb8-bb96-e88f8ff96e54.png)

### Langkah 2
![Jarkom Modul 4Pembagian Subnet Kelas B (1)](https://user-images.githubusercontent.com/63065991/143442335-a25a4752-db40-47ea-b82b-cd2764549b66.png)

### Langkah 3
![Jarkom Modul 4Pembagian Subnet Kelas C (1)](https://user-images.githubusercontent.com/63065991/143442349-71878db1-0412-4910-9a98-bdd0bd969f3d.png)

### Langkah 4
![Jarkom Modul 4Pembagian Subnet Kelas D (1)](https://user-images.githubusercontent.com/63065991/143442370-f76f8f13-0e32-4feb-9f50-d526749be52d.png)

### Langkah 5
![Jarkom Modul 4Pembagian Kelas E (1)](https://user-images.githubusercontent.com/63065991/143442386-ba275ed5-bd07-4cef-b8f9-b5d01ef9a556.png)

### Langkah 6
![Jarkom Modul 4Pembagian Subnet Kelas F (1)](https://user-images.githubusercontent.com/63065991/143442393-ccedde8c-e2dc-4752-959e-69c4486133f8.png)

### Langkah 7
![Jarkom Modul 4Pembagian Subnet Kelas G (1)](https://user-images.githubusercontent.com/63065991/143442409-f93d7ff8-101f-4b75-ab60-72067fc79ea0.png)

### Langkah 8
![Jarkom Modul 4Pembagian Subnet Kelas H (1)](https://user-images.githubusercontent.com/63065991/143442426-7ae04f39-466c-47bc-b52a-e45c886108ef.png)

### Perhitungan Subnet
![Frame 1Perhitungan Subnet CIDR_T15 (1)](https://user-images.githubusercontent.com/63065991/143442469-d04c7a34-513c-45c0-af8c-bb1943752b3a.png)

### Pembagian IP

| Subnet | Netmask |
|-----------|--------------|
| A1        |  /25         |
| A2        |  /22         |
| A3        |  /30         |
| A4        |  /21         |
| A5        |  /22         |
| A6        |  /30         |
| A7        |  /22         |
| A8        |  /24         |
| A9        |  /22         |
| A10        |  /30         |
| A11        |  /30         |
| A12        |  /23         |
| A13        |  /30         |
| A14        |  /28         |
| A15        |  /30         |

## Setting GNS3
### PUCCI
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.32.2
      netmask 255.255.255.252
      gateway 10.49.32.1

auto eth1
iface eth1 inet static
      address 10.49.67.129
      netmask 255.255.255.128

auto eth2
iface eth2 inet static
      address 10.49.16.1
      netmask 255.255.248.0
```

### PC-PTJIPANGU
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.67.130
      netmask 255.255.255.128
      gateway 10.49.67.129
```

### PC-PTCALMBELT
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.16.2
      netmask 255.255.248.0
      gateway 10.49.16.1
```

### PC-PTCOURTYARD
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.16.3
      netmask 255.255.248.0
      gateway 10.49.16.1
```

### WATER 7
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.32.1
      netmask 255.255.252.0

auto eth1
iface eth1 inet static
      address 10.49.32.1
      netmask 255.255.255.252
      gateway 10.49.32.2

auto eth2
iface eth2 inet static
      address 10.49.67.45
      netmask 255.255.255.252
      gateway 10.49.67.46
```

### PC-PTCIPHER
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
	address 10.49.32.2
	netmask 255.255.252.0
        gateway 10.49.32.1
```

### SEASTONE
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.67.1
      netmask 255.255.255.0
      gateway 10.49.67.2

auto eth1
iface eth0 inet static
      address 10.49.4.1
      netmask 255.255.252.0
```

### PC-PTELENA
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.4.2
      netmask 255.255.252.0
      gateway 10.49.4.1
```

### OIMO
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.67.1
      netmask 255.255.255.252
      gateway 10.49.67.2

auto eth1
iface eth0 inet static
      address 10.49.67.33
      netmask 255.255.255.252

auto eth2
iface eth2 inet static
      address 10.49.66.1
      netmask 255.255.255.0
```

### PC-PTENIESLOBBY
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
	address 10.49.66.2
	netmask 255.255.255.0
            gateway 10.49.66.1

###SERVER-PTFUKUROU
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
	address 10.49.67.34
	netmask 255.255.255.252
            gateway 10.49.67.33
```

### ALABASTA
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.64.1
      netmask 255.255.254.0
      gateway 10.49.64.2

auto eth1
iface eth1 inet static
      address 10.49.67.17
      netmask 255.255.255.240
```

### PC-PTJORGE
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.67.18
      netmask 255.255.255.240
      gateway 10.49.67.17
```

### PC-PTMAINGATE
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.64.1
      netmask 255.255.254.0
      gateway 10.49.64.2
```

### PC-PTJABRA
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
      address 10.49.0.2
      netmask 255.255.252.0
      gateway 10.49.0.1
```

### FOOSHA
```
auto lo
iface lo inet loopback

auto eth2
iface eth2 inet dhcp

auto eth0
iface eth0 inet static
	address 10.49.36.1
	netmask 255.255.252.0

auto eth1
iface eth1 inet static
	address 10.49.67.46
	netmask 255.255.255.252
        gateway 10.49.67.45

auto eth3
iface eth3 inet static
	address 10.49.67.41
	netmask 255.255.255.252
        gateway 10.49.67.42

auto eth4
iface eth4 inet static
	address 10.49.67.38
	netmask 255.255.255.252
        gateway 10.49.67.37
```

### PC-PTBUENO
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
	address 10.49.36.2
	netmask 255.255.252.0
           gateway 10.49.36.1
```

### SERVER-PTDORKI
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
	address 10.49.67.42
	netmask 255.255.255.252
            gateway 10.49.67.41
```

