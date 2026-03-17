# Remote SSH dari  AWS EC2 Server 

1. Unduh dan Install Putty di https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
![alt text](image.png)

2. Konversi ekstensi Private key dari .pem menjadi .ppk
-Buka Putty Gen
-Load Private Key .pem (file .pem didapat saat membuat instance EC2 yang ada di folder pertemuan 2 yang biasanya di folder download)
![alt text](image-1.png)

-Klik Save Private Key menjadi ekstensi File .ppk
![alt text](image-2.png)

4. Setting-Up Remote SSH dengan PPitty
-Isi Ip4 addres Public

![alt text](image-3.png)
-Port SSH (22)
-Load private key di .ppk di menu COnnection -> SSH ->Auth -> Credential
![alt text](image-4.png)

-User dari instance  masing-masing (ubuntu)
![alt text](image-7.png)

6. Setiap awal Remote kita lakukan Patching OS
-sudo apt-get update && sudo apt-get upgrade
![alt text](image-8.png)

7. Coba lakukan instalasi web server dalam keadaan kosong
![alt text](image-9.png)

Instal salah satu web server
- sudo apt install nginx
![alt text](image-10.png)
