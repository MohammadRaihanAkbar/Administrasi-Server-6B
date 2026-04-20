# Migration web apps dynamic ke ec2 aws

1. Pastikan web apps dynamic sudah berjalan di local
2. Jika sudah tanpa error kita akan membaut folder build

- npm run build
- pastikan menampilkan folder .next/standalone didalam tersedia   folder static

3. Proses Upload File Folder StandAlone

   - lakukan proses archive pada folder .next/standalone dan folder public.zip
   - running instance -> connect open ssh -> open filezilla
   - upload file hasil archive .zip standalone ke ec2 AWS menggunakan Filezilla

   ![1776657678309](image/migration/1776657678309.png)

   - extract file hasil archive di ec2 aws

   1. install tools unzip di ec2 aws

      - sudo apt install unzip -y
        ![1776658174236](image/migration/1776658174236.png)
   2. extract file hasil archive di ec2 aws

      - unzip standalone.zip
4. export dbCompro dari localhost import ke ec2 AWS

   - login ke SQL  ec2 sudo mysql -u USERCOMPRO -p
   - use dbCompro;
   - copy paste query SQL dari export dbCompro di Localhost
   - cek setiap tabel aoakah sudah terisi
     - select * from berita;
     - select * from users;
5. sesuaikan isi dile .env di ec2 aws

   - DB_HOST=localhost
   - DB_USER=USERCOMPRO
   - DB_PASSWORD=PASSWORD
   - DB_NAME=dbCompro
   - ctrl s
6. di terminal ssh cd ke folder standalone run apps
   -pm2 start server.js
   -pm2 save
   -pm2 startup

   ![1776661054468](image/migration/1776661054468.png);
7. Buka port 3000 di security group ec2 aws

- edit security group
- add rule
- save
  ![1776660384726](image/migration/1776660384726.png)
- Check Perubahan
- ![1776661031978](image/migration/1776661031978.png)
