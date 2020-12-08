# Instalation Ubuntu Server 18.04 on VirtualBox

### Prerequisites
 - VirtualBox - Download and Install [VirualBox](https://www.virtualbox.org/)
 - Ubuntu Server 18.04 - Download [Ubuntu](https://ubuntu.com/download/server)

 ## Step 1 - Creating Virtual Machine
 - Buka VirtualBox dan Click New untuk membuat Virtual Machine. Isi **Nama** dengan format **nama-nomorInduk**, setelah itu pilih **Type** lalu ubah menjadi **Linux** dan ubah **Version** menjadi **Ubuntu(64-bit)** lalu Klik **Next**
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/1.png?raw=true)

 - Sesuaikan Ukuran RAM yang akan digunakan lalu klik **Next**
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/2.png?raw=true)


 - Setelah Itu Pilih **Create a Virtual Hardisk Now** agar virtual machine yang dibuat memiliki storage. setelah itu pilih **Create**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/3.png?raw=true)

 - Pilih **VDI (Virtualbox Disk Image)** dan klik **Continue**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/4.png?raw=true)

 - Setelah itu pilih **Dynamically Allocated** dan klik **Next**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/5.png?raw=true)

 - Lalu atur alokasi hardisk dan klik **Create**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/6.png?raw=true)

- Setelah selesai maka akan muncul virtual machine yang dibuat

## Step 2 - Setup Virtual Machine
- Setelah virtual machine dibuat, klik pada virtual machine dan klik **setting** pada tab
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/7.png?raw=true)
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/8.png?raw=true)
- Lalu masuk ke tab storage dan klik icon **cd** yang ada disamping kanan **Controller: IDE**
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/9.png?raw=true)
- Klik **Add** untuk menambahkan image ubuntu lalu Klik tombol **Choose** dan klik **OK**
 ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/10.png?raw=true)
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/11.png?raw=true)
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/12.png?raw=true)


## Step 3 - Install Ubuntu & Setup Ubuntu
- Setelah virtual machine selesai di setup klik virtual machine yang telah dibuat dan klik Menu **Start** lalu installasi ubuntu pun dimulai
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/13.png?raw=true)
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/14.png?raw=true)

- Pilih bahasa yang akan digunakan diserver dan tekan **Enter**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/15.png?raw=true)
- Setelah Itu pilih **Update to the new Installer** agar saat installasi menggunakan source terupdate dari ubuntu dan tekan **Enter**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/16.png?raw=true)
- Setelah itu pilih layout dari keyboard yang akan digunakan di server dan tekan **Enter**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/17.png?raw=true)
- Step ini berfungsi untuk mengatur network pada server. namun step ini akan saya atur nanti jadi pilih **Done**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/18.png?raw=true)
- Step ini berfungsi untuk menambahkan proxy pada server namun step ini akan saya skip jadi pilih **Done**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/19.png?raw=true)
- Untuk Step ini berfungsi untuk menambahkan mirror source untuk ubuntu. pada step ini saya akan menggunakan bawaan dari ubuntu jadi klik **Done**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/20.png?raw=true)
- Step Ini berfungsi untuk mengatur storage yang telah ditentukan sebelumnya. Pilih **Custom Storage Layout** agar dapat menambahkan beberapa setting seperti **swap** dll. lalu pilih **Done** dan tekan **Enter**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/21.png?raw=true)
- Pilih Device Storage yang akan diatur lalu tekan **Enter** lalu pilih **Add GPT Partition**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/22.png?raw=true)
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/23.png?raw=true)
- Saat ini saya akan mengatur **Swap** memory maka masukan jumlah Swap Yang diinginkan. lalu ubah **Format** menjadi **swap** dan pilih **Create** Lalu tekan Enter. Swap telah selesai dibuat
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/24.png?raw=true)

- Setelah Swap dibuat langkah selanjutnya adalah membuat storage untuk digunakan pada server
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/25.png?raw=true)
- Pilih Device Storage yang akan diatur lalu tekan **Enter** lalu pilih **Add GPT Partition**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/26.png?raw=true)
- Lalu masukan sisa storage dan Pilih Format **ext4** dan pilih **Create** lalu tekan **Enter**
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/27.png?raw=true)
- Pilih **Done** dan **Continue** untuk melanjutkan setup
  ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/28.png?raw=true)
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/29.png?raw=true)
- Masukan Informasi server seperti **Nama**, **Nama Server**, **Username** dan **Password** lalu pilih **Done** dan tekan **Enter**
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/30.png?raw=true)
- Step Selanjutnya adalah install **OpenSSH**. step ini akan saya skip dan install pada step selanjutnya. maka Pilih **Done** dan tekan **Enter**
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/31.png?raw=true)
- Step ini bertujuan untuk install beberapa software pada ubuntu. berhubung saya belum membutuhkan software maka saya Pilih **Done** dan tekan **Enter**
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/32.png?raw=true)
- Setelah itu ubuntu akan melakukan installasi sesuai dengan setting yang telah dilakukan
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/33.png?raw=true)
- Setelah Melakukan Installasi Ubuntu akan meminta untuk reboot System.
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/34.png?raw=true)
- Setelah Selesai melakukan Reboot. Ubuntu akan Meminta Login. maka masukan username dan password
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/35.png?raw=true)
- Setelah Login ubuntu akan menampilkan informasi system dan server telah selesai di install
    ![alt text](https://github.com/fitraaditama7/DumbwaysBootcamp/blob/master/week1/VIRTUAL%20BOX%20-%20INSTALL%20UBUNTU/img/36.png?raw=true)
