# VPN Server

### Step 1 - Create Servers
- Buat Security Group Baru

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/2.png?raw=true)

- Buat Satu Server Baru

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/1.png?raw=true)


- Buat Elastic IP Baru dan hubungkan dengan server baru yang telah dibuat

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/4.png?raw=true)

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/5.png?raw=true)

### Step 2 - Install OpenVPN
- Masuk ke Server VPN dan install OpenVPN
```
    wget https://git.io/vpn -O openvpn-install.sh
    sudo bash openvpn-install.sh
```
Lalu Masukan Settingan seperti Berikut

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/6.png?raw=true)

 Jika sudah maka file ovpn telah berhasil dibuat

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/7.png?raw=true)

- Copy File ovpn ke komputer local
```
    scp user@vpn-address:/path/file.ovpn /path/di/local
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/8.png?raw=true)


- Jika sudah download [tunnelblick](https://tunnelblick.net/) dan install
- buka tunnelblick

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/9.png?raw=true)

- buka file ovpn yang telah di copy dari server dan drag and drop ke tunnelblick lalu klik connect

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/10.png?raw=true)

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/9.png?raw=true)

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/8.%20VPN%20Server/img/11.png?raw=true)





