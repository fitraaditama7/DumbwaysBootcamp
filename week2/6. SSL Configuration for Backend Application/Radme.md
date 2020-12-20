# SSL Configuration for Backend Application

### Step 1 - Install Snapd
- Install Snapd
```
    sudo apt update
    sudo apt install snapd
```

### Step 2 - Install Certbot
- Install Certbot
```
    sudo snap install --classic certbot
```

- Generate SSL, dan masukan informasi yang dibutuhkan
```
    sudo certbot --nginx
```

- Lalu buka domain backend yang telah didaftarkan sebelumnya. maka akan muncul logo gembok disamping kiri
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/6.%20SSL%20Configuration%20for%20Backend%20Application/img/1.png?raw=true)

