# Load Balancing Frontend

### Step 1 - Create Servers
- Pada AWS buat 2 Server Frontend dengan subnet private dan security group yang sama

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/7.%20Load%20Balancing%20Frontend/img/1.png?raw=true)
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/7.%20Load%20Balancing%20Frontend/img/2.png?raw=true)

### Step 2 - Setup Project
- Masuk ke private server Frontend-1 dan Frontend-2
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
