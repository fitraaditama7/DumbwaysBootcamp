# Install GIT and SSH Key

### Step 1 - Setup GIT
- Pertama setting global configuration untuk git di server dengan memasukan username dan email. usahakan email yang didaftarkan sama dengan email yang digunakan untuk akun git
```
    git config --global user.name "John Doe"
    git config --global user.email johndoe@example.com
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/1.%20Install%20GIT%20dan%20SSH%20Key/img/25.png?raw=true)


### Step 2 - Setup SSH 
- Pertama masuk ke server yang akan disetup SSH Key
- Setelah itu buat ssh key baru 
```
    ssh-keygen -t rsa -b 4096 -C “johndoe@example.com”

```
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/1.%20Install%20GIT%20dan%20SSH%20Key/img/26.png?raw=true)

### Step 3 - Setup GITHUB and SSH
- Login ke https://github.com/
- Lalu masuk ke menu **Settings** yang ada pada menu sebelah kanan 

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/1.%20Install%20GIT%20dan%20SSH%20Key/img/11.png?raw=true)


- Setelah itu pilih menu SSH and GPG keys lalu klik **New SSH Key**

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/1.%20Install%20GIT%20dan%20SSH%20Key/img/13.png?raw=true)


- Masukan Title dan SSH yang baru dibuat sebelumnya lalu klik tombol **Add SSH Key**

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/1.%20Install%20GIT%20dan%20SSH%20Key/img/14.png?raw=true)

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/1.%20Install%20GIT%20dan%20SSH%20Key/img/15.png?raw=true)


### Step 4 - Check
- Masuk ke server lalu check dengan menggunakan syntax berikut ini
```
    ssh -T git@github.com
```

 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week2/AWS%20-%20Create%20and%20Setup%20Server/img/24.png?raw=true)



