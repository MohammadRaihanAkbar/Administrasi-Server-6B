### membuat ec2 /instance/vm

1. Pilih menu allservices kemudian pilihh ec2

![1772421174219](https://file+.vscode-resource.vscode-cdn.net/c%3A/Users/raiha/Documents/Semester%206/Administrasi%20Server/Pertemuan-2/image/create-ec2/1772421174219.png)

    

2. Pilih bagian instance didalam ec2

   ![1772421238830](image/create-ec2/1772421238830.png)
3. Pilih menu launch instance

   ![1772421291401](image/create-ec2/1772421291401.png)
4. Beri nama instance dengan NIM_Server

   ![1772421365392](image/create-ec2/1772421365392.png)
5. kita pilih os server untuk instance kita

   ![1772422055108](image/create-ec2/1772422055108.png)
6. pilih resource instance yg t3.micro

   ![1772422147465](image/create-ec2/1772422147465.png)
7. Membuat key pair, pilih new key pair, isi nama key, pake RSA, format file .pem, create key pair

   ![1772422277906](image/create-ec2/1772422277906.png)
8. setting kebijakan keamanan/ security group

   - allow SSH -> artinya membolehkan remote ssh dari luar
   - allow https -> artinya instance bisa di akses di protocol https
   - allow http -> artinya instance bisa di akses di protocol HTTP

     ![1772422600609](image/create-ec2/1772422600609.png)
9. selesai set up klik launch instance

   ![1772422654096](image/create-ec2/1772422654096.png)
10. pastikan launch instance

    ![1772422856818](image/create-ec2/1772422856818.png)
