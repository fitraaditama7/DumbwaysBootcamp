# Instalation Application On Ubuntu Server 18.04

### Step 1 - Install Depedency
- Download Nodejs 10.x
```
    curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/1.png?raw=true)

- Install Nodejs 10.x
```
    sudo apt-get install -y nodejs
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/2.png?raw=true)

- Verifikasi NodeJS telah terinstal dengan melihat versi NodeJS
```
    node -v
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/3.png?raw=true)

- Clone project sample yang telah disediakan
```
    git clone https://github.com/DumbwaysDotId/DW15WDTPH_housy
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/4.png?raw=true)

- Change Directory ke project yang telah di clone
```
    cd DW15WDTPH_housy/
```

- Checkout ke Branch 11.Add-Property
```
    git checkout 11.Add-Property
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/5.png?raw=true)

- Install dependency yang dibutuhkan
```
    npm install
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/7.png?raw=true)

- Setelah depedency yang telah terinstall jalankan aplikasi dengan menggunakan command
```
    npm start
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/8.png?raw=true)

- Buka `192.168.100.5:3000` untuk membuka aplikasi yang berjalan
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20APPLICATION/img/9.png?raw=true)
