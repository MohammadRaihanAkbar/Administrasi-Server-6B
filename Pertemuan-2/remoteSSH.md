### Remote instance with putty

1. pastikan putty terinstall di pc

   ![1772423204286](image/remoteSSH/1772423204286.png)
2. konversi file Public key ari .pem menjadi .ppk di putty

   - buka puttygen
   - load
   - save as .ppk

     ![1772423635317](image/remoteSSH/1772423635317.png)
3. set up putty untuk remote SSH

   - buka apps putty
   - isi IP public
   - isi port untuk SSH sesuai security group di instance
   - isi nama session agar saat connect lagi tinggal load saja
   - load file .ppk (di dalam putty)  (klik SSH -> AUTH -> CREDNDTIALS -> load .ppk)

     ![1772424463148](image/remoteSSH/1772424463148.png)
   - ![1772424668373](image/remoteSSH/1772424668373.png)
4. connect ubuntu di aws ke putty

   ![1772425091323](image/remoteSSH/1772425091323.png)
5. sudo apt get-update, sudo apt upgrade

   ![1772425432358](image/remoteSSH/1772425432358.png)
6. pembuktian remote SSH secara visual

   - install webserver sprti apache/nginx

     - sudo apt install apache2 -y

     ![1772425936894](image/remoteSSH/1772425936894.png)
7. Matikan instance agar tidak mengurahi saldo di aws //sudo shutdown now

   ![1772426212390](image/remoteSSH/1772426212390.png)

   ![1772426266146](image/remoteSSH/1772426266146.png)
