# SSL Configuration

### Step 1 - Setup SSL
- Install Certbot
```
    sudo apt install snapd
    sudo snap install core; sudo snap refresh core
    sudo snap install --classic certbot
    sudo ln -s /snap/bin/certbot /usr/bin/certbot
```

- Setup Certbot untuk NGINX
```
    sudo certbot --nginx
```
Lalu masukan informasi yang dibutuhkan
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20SSL%20Configuration/img/7.png?raw=true)

 - Jika sudah buka browser lalu arahkan ke custom domain yang telah dibuat. lalu cek icon gembok yang ada disebelah kiri

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20SSL%20Configuration/img/13.png?raw=true)
