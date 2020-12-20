# Setup Reverse Proxy Backend

### Step 1 - Installation
- Jika kalian dirasa sudah install nginx bisa lanjut ke step selanjutnya. jika belum install nginx di server public
```
    sudo apt-get install nginx
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/4.%20Reverse%20Proxy%20Backend/img/1.png?raw=true)

### Step 2 - Setup Reverse Proxy Backend
- Buat folder didalam  `/etc/nginx`
```
    sudo mkdir /etc/nginx/backend
```

- buat file configurasi
```
    sudo vi /etc/nginx/backend/backend.conf
```

- Tulis file dengan syntax seperti berikut ini
```
    server {
        listen 80;
        listen [::]:80;

        server_name 54.144.231.196;

        location / {
        proxy_pass      ip-yang-akan-digunakan:5000;
        }
    }
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/4.%20Reverse%20Proxy%20Backend/img/2.png?raw=true)

- Daftarkan configurasi yang baru dibuat ke konfigurasi utama nginx
```
    sudo vi /etc/nginx/nginx.conf
```

tambahkan folder yang tadi dibuat didalam file konfigurasi utama nginx
```
    include /etc/nginx/backend/*;
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/4.%20Reverse%20Proxy%20Backend/img/3.png?raw=true)
