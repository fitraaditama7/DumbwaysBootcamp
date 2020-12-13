# Create and Setup Server

### Step 1 - Create VPC
VPC atau singkatan dari Virtual Private Cloud adalah Tiering Networks tempat Anda dapat memisahkan network A dan network B, dengan maximum Tiers VPC adalah 3. Berikut langkah langkah pembuatan VPC
- Pertama masuk ke Dashboard VPC dengan mengklik Menu **service** -> **VPC**
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/1.png?raw=true)

- Setelah Masuk ke Dashboard VPC Klik Menu VPC Pada Dashboard Sebelah Kanan
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/2.png?raw=true)

- Setelah itu klik tombol Create VPC
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/3.png?raw=true)

- Masukan nama VPC IPv4, CIDR block lalu klik tombol Create VPC
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/5.png?raw=true)


### Step 2 - Create Subnet
Subnet adalah range dari IP yang ada di VPC. Dalam kasus ini subnets kita bagi menjadi 2 yaitu Public Subnet dan Private Subnet. langkah langkah pembuatan subnet public dan private adalah sebagai berikut
- Pada Dashboard VPC klik menu Subnets
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/6.png?raw=true)

- Setelah itu klik tombol Create Subnet
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/7.png?raw=true)

- Pertama saya akan buat Subnet public terlebih dahulu. Pilih VPC yang telah dibuat di step sebelumnya
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/8.png?raw=true)

- Setelah itu akan muncul form baru dibawah form yang sebelumnya. Masukan nama Subnet dan IPv4 CIDR blocknya. disini saya menggunakan 10.0.0.0/24
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/9.png?raw=true)

- Jika sudah sekarang buat Subnet private. Langkahnya sama seperti tadi. dan masukan IPv4 CIDR block dengan IP 10.0.1.0/24
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/10.png?raw=true)


### Step 3 - Create NAT Instance
NAT instace adalah Instance yang digunakan sebagai penyalur koneksi internet pada private server. berikut langkah langkah pembuatan NAT Instance
- Kembali ke Dashboard EC2 lalu klik menu EC2
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/11.png?raw=true)

- Pada menu disebelah kiri klik menu Instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/12.png?raw=true)

- Lalu klik tombol Launch Instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/13.png?raw=true)

- Pilih Menu Community AMIs dan cari instance dengan keyword nat lalu pilih salah satu
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/15.png?raw=true)

-  Pilih type instance yang diinginkan lalu klik tombol Next: Configure Instance Details
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/16.png?raw=true)

- Selanjutnya pada field Network pilih VPC yang telah dibuat sebelumnya. 
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/50.png?raw=true)

- Pada field Subnets Pilih subnet public yang telah dibuat
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/51.png?raw=true)

- Pada Auto-assign Public IP ubah menjadi Enable. setelah selesai klik tombol Next: Add Storage
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/17.png?raw=true)

- Masukan Storage yang diinginkan dan klik tombol Next: Add tags
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/18.png?raw=true)

- Klik tombol Add another tag dan masukan Nama instance yang dibuat. lalu klik tombol Configure Security Group
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/19.png?raw=true)

- Buat security group baru dengan memilih Create anew security group lalu masukan nama dan description. setelah itu klik tombol Add rule dan masuka Type dengan value All traffic, Source dengan value Custom dan tambahkan ip dari subnet Private yang telah dibuat. dan klik tombol Review and launch
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/20.png?raw=true)

- Setelah itu klik tombol Launch
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/21.png?raw=true)

- Buat key pair baru dengan memilih opsi Create a new key pair dan masukan nama key pair yang akan dibuat. setelah itu klik tombol Download Key Pair dan klik tombol Launch Instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/22.png?raw=true)

- Jika sudah maka nat instance berhasil dibuat. tunggu beberapa saat sampai nat instance running dan siap digunakan
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/24.png?raw=true)

- Jika sudah running kita akan mematikan destination check pada NAT instance. caranya klik pada nat instance yang telah dibuat lalu pilih Actions -> Networking -> Change source/destination check
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/83.png?raw=true)

- Pada Source/ destination checking klik centang pada Stop lalu klik tombol save
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/84.png?raw=true)



### Step 4 - Create Internet Gateway
Internet gateway digunakan untuk memberikan akses internet pada kelompok subnet yang telah dibuat. berikut langkah langkah pembuatan Internet Gateway
- Kembali ke Dashboard VPC lalu klik menu Internet gateways yang ada disebelah kiri
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/25.png?raw=true)

- Klik tombol Create Internet Gateway
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/26.png?raw=true)

- Masukan nama internet gateway yang akan dibuat. lalu klik tombol Create Internet Gateway
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/27.png?raw=true)

- Setelah itu daftarkan IGW ke VPC yang telah dibuat sebelumnya. dengan klik field Actions dan pilih Attach to VPC
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/28.png?raw=true)

- Lalu pilih VPC yang telah dibuat sebelumnya dan klik tombol Attach Internet Gateway
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/29.png?raw=true)


### Step 5 - Create and Setup Route Table
Route Tables adalah penghubung antara gateway/instance dan Subnet yang telah dibuat. berikut langkah langkah pembuatan Route Table
- Pada Dashboard VPC pilih menu Route Tables disebelah kiri
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/30.png?raw=true)

- Pertama kita akan buat dan setup route table public. Maka klik tombol Create route table
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/31.png?raw=true)

- Masukan Nama Tag dan VPC yang telah dibuat sebelumnya. lalu klik tombol create
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/32.png?raw=true)

- Setelah Route table dibuat saya akan menghubungkan route table dengan subnet public. caranya klik pada route table yang telah dibuat. maka akan muncul menu disebelah bawah. pilih Subnet Associations dan klik tombol Edit subnet Associaitons
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/34.png?raw=true)

- Pilih Subnet Public yang telah dibuat sebelumnya. Lalu klik tombol Save
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/35.png?raw=true)

- Sekarang kita akan menghubungkan route table dengan internet gateway. Agar subnet public dapat mengakses koneksi internet. Pilih menu Routes dan klik Tombol Edit Routes
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/35.png?raw=true)

- Masukan Destination dengan IP 0.0.0.0/0 dan masukan target dengan internet gateway yang telah dibuat sebelumnya. lalu klik tombol save routes
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/37.png?raw=true)
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/38.png?raw=true)

- Sekarang kita akan membuat route table private. Caranya sama seperti pembuatan route table public. Masukan Nama tag dan VPC yang telah dibuat lalu klik tombol Create
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/33.png?raw=true)

- Sekarang kita akan menghungkan route table dengan subnet private. caranya klik pada route table private yang telah dibuat. lalu pilih menu Subnet Associtions dan klik Edit subnet Associations
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/39.png?raw=true)

- Pilih subnet private yang telah dibuat sebelumnya. lalu klik tombol save
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/40.png?raw=true)

- Sekarang kita akan menghubungkan route table private dengan NAT Gateway agar instance yang berada dalam subnet private bisa mengakses internet
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/41.png?raw=true)

- Masukan IP Destination dengan IP 0.0.0.0/0 dan masukan target dengan instance -> lalu nat intance yang telah dibuat sebelumnya. lalu klik tombol save Routes
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/42.png?raw=true)
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/43.png?raw=true)


### Step 6 - Create and Setup Public Instance
Public instance adalah instance yang dibuat sebagai gerbang utama masuknya traffic dari website yang akan buat. berikut adalah langkah langkah pembuatan dan setup Public Instances
- Kembali ke Dashboard EC2 pada menu sebelah kiri klik menu Instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/46.png?raw=true)

- klik tombol launch Instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/47.png?raw=true)

- pada field pencarian masukan keyword "ubuntu server" lalu pilih Ubuntu Server versi 18.04 LTS
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/48.png?raw=true)

- pilih type instance yang diinginkan lalu klik tombol Next: Configure Instance Details
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/16.png?raw=true)

- Selanjutnya pada field Network pilih VPC yang telah dibuat sebelumnya. 
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/50.png?raw=true)

- Pada field Subnets Pilih subnet public yang telah dibuat
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/51.png?raw=true)

- Pada Auto-assign Public IP ubah menjadi Enable. setelah selesai klik tombol Next: Add Storage
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/17.png?raw=true)

- Masukan Storage yang diinginkan dan klik tombol Next: Add tags
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/18.png?raw=true)

- Klik tombol Add another tag dan masukan Nama instance yang dibuat. lalu klik tombol Configure Security Group
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/54.png?raw=true)

- Buat security group baru dengan memilih Create a new security group lalu tambahkan nama dan description. setelah itu tambahkan rule dengan klik tombol Add Rule dan tambahkan value Type SSH dengan Source Custom dan IP 0.0.0.0/0, type HTTP dengan source Custom danIP 0.0.0.0/0, ::/0, type HTTPS dengan source Custom danIP 0.0.0.0/0, ::/0. lalu klik tombol review and Launch
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/55.png?raw=true)

- Setelah itu klik tombol Launch
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/56.png?raw=true)

- Pilih key pair yang telah dibuat sebelumnya lalu klik tombol launch instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/58.png?raw=true)

- Jika sudah maka public instance berhasil dibuat. tunggu beberapa saat sampai public instance running dan siap digunakan
- sekarang saya akan menambahkan Elastic IP untuk public instance. pada menu disebelah kiri pilih menu Elastic IP
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/69.png?raw=true)

- klik tomobl Allocate Elastic IP Address. lalu klik tombol Allocate
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/70.png?raw=true)
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/71.png?raw=true)

- Jika sudah Klik pada tombol Actions dan Pilih Associate Elastic IP Address
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/72.png?raw=true)
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/73.png?raw=true)

- Pilih Public Instance Yang telah dibuat Sebelumnya lalu klik Associate. dengan ini public instance telah memiliki static IP
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/74.png?raw=true)
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/75.png?raw=true)

- Sekarang kita akan setup user pada server public. masuk terminal dan masuk ke folder dimana key pair disimpan. lalu ubah privilege keypair menjadi 400. dengan cara
```
    chmod 400 nama-key-pair.pem
```
lalu ssh ke public server menggunakan key-pair yang telah didownload dan dengan user default yaitu ubuntu dengan cara
```
    ssh -i nama-key-pair.pem ubuntu@ip-publib 
```
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/76.png?raw=true)

- jika sudah masuk buat user baru dengan cara
```
    sudo adduser username
```
lalu masukan informasi yang dibutuhkan seperti password, full name dll.
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/77.png?raw=true)

- Setelah itu daftarkan user pada group sudo. dengan cara
```
    sudo usermod -aG sudo username
```
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/78.png?raw=true)

- agar saat akses server hanya perlu memasukan username, ip dan password maka kita harus edit file sshd `/etc/ssh/sshd_config`. lalu Ganti `PasswordAuthentication` dari no menjadi yes.
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/79.png?raw=true)

- setelah itu restart sshd agar configurasi yang kita buat bisa langsung diimplementasi
```
    sudo service restart sshd
```

- jika sudah keluar dari server dan coba masuk ke server dengan menggunakan format username@ip-address. jika bisa masuk maka configurasi berhasil
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/81.png?raw=true)


### Step 7 - Create and Setup Private Instance
Private Instance adalah instance yang terisolasi digunakan untuk menyimpan source code, database ataupun setup lain yang tidak terhubung langsung pada dunia luar. berikut langkah langkah pembuatan dan setup private instances
- klik tombol launch Instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/47.png?raw=true)

- pada field pencarian masukan keyword "ubuntu server" lalu pilih Ubuntu Server versi 18.04 LTS
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/48.png?raw=true)

- pilih type instance yang diinginkan lalu klik tombol Next: Configure Instance Details
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/16.png?raw=true)

- Selanjutnya pada field Network pilih VPC yang telah dibuat sebelumnya. 
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/50.png?raw=true)

- Pada field Subnets Pilih subnet private yang telah dibuat
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/51.png?raw=true)

- Pada Auto-assign Public IP ubah menjadi disable. setelah selesai klik tombol Next: Add Storage
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/17.png?raw=true)

- Masukan Storage yang diinginkan dan klik tombol Next: Add tags
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/18.png?raw=true)

- Klik tombol Add another tag dan masukan Nama instance yang dibuat. lalu klik tombol Configure Security Group
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/65.png?raw=true)

- Pilih security group yang telah dibuat sebelumnya. lalu klik review and launch
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/66.png?raw=true)

- Setelah itu klik tombol Launch
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/56.png?raw=true)

- Pilih key pair yang telah dibuat sebelumnya lalu klik tombol launch instances
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/58.png?raw=true)

- Jika sudah maka private instance berhasil dibuat. tunggu beberapa saat sampai private instance running dan siap digunakan

- Jika Server Private sudah running maka kita bisa setup server private.

- copy key-pair-pem yang telah dibuat sebelumnya ke server public. masuk ke folder tempat key-pair.pem berada lalu copy ke server dengan cara
```
    scp key-pair.pem username@ip-address:~/
```

- setelah di copy ubah privilege menjadi 400 lalu akses private instance dari server public dengan menggunakan key pair dan username default yaitu ubuntu
```
    chmod 400 key-pair.pem
```
```
    ssh -i key-pair.pem ubuntu@ip-address
```
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/82.png?raw=true)

- jika sudah masuk kita buat user pada private instances. dengan cara
```
    sudo adduser username
```
lalu masukan password dan informasi lainnya
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/85.png?raw=true)

- setelah itu daftarkan user ke group sudo. dengan cara
```
    sudo usermod -aG sudo maman
```
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/86.png?raw=true)

- agar saat akses server hanya perlu memasukan username, ip dan password maka kita harus edit file sshd `/etc/ssh/sshd_config`. lalu Ganti `PasswordAuthentication` dari no menjadi yes.
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/87.png?raw=true)

- setelah itu restart sshd agar configurasi yang kita buat bisa langsung diimplementasi
```
    sudo service restart sshd
```

- jika sudah keluar dari server private dan coba masuk ke server dengan menggunakan format username@ip-address. jika bisa masuk maka configurasi berhasil

- sekarang kita akan setup nodejs caranya
```
    sudo apt-get update
    curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
    sudo apt-get install -y nodejs
```
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/90.png?raw=true)
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/91.png?raw=true)

- verifikasi versi nodejs yang telah kita install
 
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/AWS%20-%20Create%20and%20Setup%20Server/img/92.png?raw=true)

- jika versi nodejs sudah sesuai dengan keinginan maka configurasi nodejs telah selesai