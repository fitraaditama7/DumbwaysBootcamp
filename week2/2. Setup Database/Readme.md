# Setup Database Server

### Step 1 - Install and Setup MariaDB
- Pertama update system ubuntu
```
    sudo apt-get update
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/2.%20Setup%20Database/img/102.png?raw=true)


- Install MariaDB. dengan menggunakna mysql_secure_installation kita dapat langsung set password untuk user `root`
```
    sudo apt-get install mariadb-server
    sudo mysql_secure_installation
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/2.%20Setup%20Database/img/103.png?raw=true)


- Setup MariaDB Bind Address. Bind Address digunakan agar mariadb/mysql bisa diakses menggunakan remote server. langkahnya edit my.cnf/mariadb.conf yang didalamnya terdapat `bind-address=127.0.0.1` (dalam kasusku bind-address terdapat dalam file `50-server.cnf`) ubah menjadi `bind-address=0.0.0.0`. bisa juga menggunakan syntax berikut untuk mencari file yang terdapat `bind-address`
```
    sudo grep -R -i "bind-address" /etc/mysql/*
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/2.%20Setup%20Database/img/104.png?raw=true)
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/2.%20Setup%20Database/img/105.png?raw=true)


### Step 2 - Configure User
- Setelah Mariadb terinstall langkah selanjutnya adalah membuat database dan setup user
- Buat database
```
    create database name_database
```
- Masuk ke console mysql menggunakan user root
```
    sudo mysql -u root
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/2.%20Setup%20Database/img/106.png?raw=true)


 - Buat user baru pada mysql.
 ```
    CREATE USER 'username'@'1.2.3.4' IDENTIFIED BY 'password';
 ```
 dalam kasus ini user dapat mengakses server dengan ip `1.2.3.4`. Jika user yang dibuat dapat diakses oleh berbagai server maka ubah ip menjadi `%`
 ```
    CREATE USER 'username'@'%' IDENTIFIED BY 'password';
 ```

 - Beri privilege pada user yang telah dibuat
 ```
    GRANT ALL PRIVILEGES ON nama_database.nama_table TO 'username'@'1.2.3.4' WITH GRANT OPTION;
 ```
 dalam kasus ini user hanya diberikan privilege untuk database `nama_database` dengan table `nama_table` dengan ip `1.2.3.4`. Jika user yang telah dibuat dapat mengakses semua database dan table yang ada didalam server maka nama_database dan table_database dapat diubah menjadi `*`
 ```   
    GRANT ALL PRIVILEGES ON nama_database.nama_table TO 'username'@'1.2.3.4' WITH GRANT OPTION;
 ```

 - Setelah privileges dibuat lalu gunakan syntax ini untuk menerapkan perubahan
 ```
    FLUSH PRIVILEGES;
 ```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/2.%20Setup%20Database/img/100.png?raw=true)

