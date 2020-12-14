# Custom Domain

### Step 1 - Create Custom Domain
- Masuk ke Cloudflare
- Klik pada tombol DNS lalu klik tombol Add Record
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Custom%20Domain/img/1.png?raw=true)

 - Masukan Nama Domain dan ip public yang telah dibuat

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Custom%20Domain/img/2.png?raw=true)

- Masuk ke server public
- Edit konfigurasi nginx dan arahkan ke custom domain yang telah dibuat
```
    sudo vi /etc/nginx/nama-folder/nama-file.conf
```

lalu ubah `server_name` menjadi nama dari custom domain yang telah dibuat dan save
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Custom%20Domain/img/6.png?raw=true)

 - Restart nginx
 ```
    sudo systemctl restart nginx
 ```

- Jika sudah buka browser dan arahkan ke custom domain yang telah dibuat. hasilnya adalah sebagai berikut
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Custom%20Domain/img/8.png?raw=true)



