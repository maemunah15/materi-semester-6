# Setting-up Database di AWS Ec2 menggunakan MariaDb

1. Aktifkan instance EC2
2. Remote instance menggunakan ssh Powershell dengan format: ssh -i < path-to-key.pem > @IP
3. Update dan upgrade sistem (sudo apt update && sudo apt upgrade -y)
4. Install MariaDb (sudo apt install mariadb-server -y)
5. Cek status MariaDb (sudo systemctl status mariadb)
![alt text](image.png)

6. Test status database di MariaDb (sudo mysql -u root -p)
Lalu cek database default (show databases;)
![alt text](image-1.png)

7. Hardening Database Server sudo mysql_secure_installation
- Change the password for the root user = Y
- Remove anonymous users = Y
- Disallow root login remotely = Y
- Remove test database and access to it = Y
- Reload privilege tables = Y
8. Create DB untuk Website Company Profile
- Login sebagai root
- Create DB nama dbcompro_NIM => CREATE DATABASE dbcompro_NIM; 
- Create User dengan nama = usrcompro_NIM dan password = [PASSWORD] => CREATE USER 'usrcompro_NIM'@'localhost' IDENTIFIED BY '[PASSWORD]';
- Grant user akses ke DB yang baru dibuat => GRANT ALL PRIVILEGES ON dbcompro_NIM.* TO 'usrcompro_NIM'@'localhost';
- Flush privileges => FLUSH PRIVILEGES;
- exit;
- login sebagai usrcompro_NIM dan cek apakah bisa akses ke DB yang baru dibuat 