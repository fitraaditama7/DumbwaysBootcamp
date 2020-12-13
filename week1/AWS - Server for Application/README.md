# Server for Application

### Step 1 - Setup Port
- Masuk ke Dashboard EC2 lalu pilih menu Security Group

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Server%20for%20Application/img/8.png?raw=true)

- Pilih User group yang digunakan untuk instance public dan private. Lalu Klik pada Security group ID

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Server%20for%20Application/img/9.png?raw=true)

- Pada Inbound Rule klik tombol Edit Inbound rules

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Server%20for%20Application/img/9.png?raw=true)

- Klik Add Rules dan tambahkan Rules Seperti berikut

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Server%20for%20Application/img/10.png?raw=true)


### Step 2 - Setup Project
- Masuk ke private server
- Clone repository github yang telah disediakan
```
    git clone https://github.com/DumbwaysDotId/DW15WDTPH_housy
    cd DW15WDTPH_housy
    npm install
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Server%20for%20Application/img/1.png?raw=true)


### Step 3 - Setup PM2
- Install PM2 secara global
```
    sudo npm install pm2 -g
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Server%20for%20Application/img/2.png?raw=true)

- Buat Ecosystem file pada folder project. dengan cara
```
    pm2 ecosystem
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Server%20for%20Application/img/3.png?raw=true)

- Ubah isi dari ecosystem.config.js menjadi seperti ini
```
    module.exports = {
        apps : [{
            name: 'housy',
            script: 'npm start
        }]
    };
```

- running application dengan cara
```
    pm2 start
```
