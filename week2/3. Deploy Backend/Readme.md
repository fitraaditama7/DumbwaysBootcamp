# Setup Backend

### Step 1 - Setup Server and Project
- Pertama masuk ke server backend dan clone repository backend
```
    git clone git@github.com:username_github/nama_repo.git
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/1.png?raw=true)


- Masuk ke masuk ke directory backend
```
    cd nama_folder
```

- Install depedency yang tersedia di repository
```
    npm install
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/4.png?raw=true)


- Install Sequelize CLI untuk migrate database
```
    npm install sequelize-cli -g
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/1.png?raw=true)


- Install PM2
```
    npm install pm2 -g
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/5.png?raw=true)


- Hubungkan Backend Server dengan Database Server dengan cara mengedit file `config/config.json`

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/2.png?raw=true)

- Migrate schema database yang ada di backend kedalam database
```
    sequelize db:migrate
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/9.png?raw=true)

- Buat File Ecosystem untuk PM2. lalu ubah isi dari file yang telah dibuat
```
    pm2 ecosystem
    vi ecosystem.config.js
```
```
    module.exports = {
        apps : [{
            name: 'housy',
            script: 'npm start'
        }]
    }
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/7.png?raw=true)

- Jalankan Aplikasi backend di background
```
    pm2 start
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/3.%20Deploy%20Backend/img/8.png?raw=true)
