# Setup Network Ubuntu Server 18.04 on VirtualBox

### Step 1 Setting Network On VirtualBox
- Klik Pada VirtualMachine yang telah dibuat lalu klik menu **Setting**
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/1.png?raw=true)
- setelah itu masuk ke tab **Network** Pada Field **Attached to** Pilih **Bridge Adapter**
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/2.png?raw=true)

### Step 2 Setting Static IP On Server
- Masuk ke server lalu Install OpenSSH agar server bisa diakses secara remote
```
    sudo apt-get install openssh-client openssh-server -y
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/3.png?raw=true)

- Buat file didalam folder `/etc/netplan/` dengan nama `01-netcfg.yaml`. Lalu isi dengan settingan seperti berikut ini

```
    network:
        version: 2
        renderer: networkd
        ethernets:
            enp0s3:
            dhcp4: no
            addresses: 
                - 192.168.100.5/24 // Sesuaikan dengan ip yang tersedia di network
            gateway4: 192.168.1.1 // Sesuaikan dengan ip gateway
            nameservers:
                addresses: [8.8.8.8, 8.8.4.4]
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/4.png?raw=true)
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/5.png?raw=true)

- lalu apply changes menggunakan command

```
    sudo netplan apply
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/6.png?raw=true)

- setelah itu cek apakah ip sudah sesuai dengan settingan yang telah dibuat. dengan menggunakan command

```
    ifconfig
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/12.png?raw=true)

- jika sudah sesuai coba untuk masuk ke server dengan menggunakan remote server dengan command
```
    ssh username-anda@ip-address-yang-telah-dibuat
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/8.png?raw=true)

- jika sudah install webserver nginx dengan menggunakan command

```
    sudo apt-get install nginx
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/9.png?raw=true)

- jika sudah selesai installasi cek ke browser dan masukan ip yang telah disetting. didalam kasus saya, saya menggunakan ip 192.169.100.5 hasilnya adalah seperti berikut
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20SETTING%20NETWORK/img/10.png?raw=true)


