# Reverse Proxy

### Step 1 - Setup NGINX
- Masuk ke public server
- Install NGINX
```
    sudo apt-get install nginx
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Reverse%20Proxy/img/1.png?raw=true)

- buat folder baru di `/etc/nginx/nama-folder` lalu buat file conf baru didalam folder yang telah dibuat
```
    sudo mkdir /etc/nginx/nama-folder
    sudo vi /etc/nginx/nama-folder/nama-file.conf
```

setelah itu isi file dengan configurasi seperti berikut
``` 
    server {
        listen 80;
        listem [::]:80;

        server_name ip-public;

        location / {
            proxy_pass http://ip-private:3000
        }
    }
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Reverse%20Proxy/img/2.png?raw=true)
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Reverse%20Proxy/img/5.png?raw=true)

 - Daftarkan konfigurasi tadi pada `nginx.conf`
 ```
    sudo vi /etc/nginx/nginx.conf
 ```
 dengan menambahkan syntax
```
    include /etc/nginx/nama-folder/*;
```
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Reverse%20Proxy/img/4.png?raw=true)

- Jika sudah save dan restart nginx
```
    sudo systemctl restart nginx
```

- Buka browser dengan nama ip yang didaftarkan hasilnya adalah seperti berikut
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Reverse%20Proxy/img/6.png?raw=true)





