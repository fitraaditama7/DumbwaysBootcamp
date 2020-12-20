# Setup Custom Domain Backend

### Step 1 - Register Domain
- Masuk ke cloudflare dan daftarkan domain dengan ip public yang telah dibuat

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/5.%20Custom%20Domain%20Backend/img/1.png?raw=true)

### Step 2 - Edit Server Name
- Setelah domain dibuat masuk ke server public dan edit `/etc/nginx/backend/backend.conf`. ubah `server_name` menjadi nama domain yang telah didaftarkan

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/5.%20Custom%20Domain%20Backend/img/2.png?raw=true)

- Restart Nginx
```
    sudo service nginx restart
```