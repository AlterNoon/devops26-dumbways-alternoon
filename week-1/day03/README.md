# Manage Server w/ Terminal

## Configure SSH to login only using public key w/o password
1. Generate ssh dengan command ssh-keygen pada windows terminal, simpan pada directory .ssh. Kemudian copy public key yang sudah dibuat

![1](/week-1/day03/images/1.png)

2. Pada vm, masuk ke dalam directory ssh dan paste public key yang sudah dicopy ke dalam file authorized_keys.

![2](/week-1/day03/images/2.png)

3. Cek kembali pada file authorized_keys apakah sudah terdapat public key yang tadi kita masukkan 

![3](/week-1/day03/images/3.png)

4. Kemudian login kembali menggunakan ssh user@ip_address, dan saat ini sudah berhasil login menggunakan public key tanpa menggunakan password

![4](/week-1/day03/images/4.png)

5. Task 2 diminta untuk hanya menerima login ssh menggunakan public key, selain menggunakan key tidak boleh masuk. Maka kita harus ubah configurasi pada file sshd_config.

![5](/week-1/day03/images/5.png)

6. Ubah password authentication menjadi no, kemudian restart ssh jika diperlukan.

![6](/week-1/day03/images/6.png)


## Buat step by step penggunaan text manipulation! (grep, sed, cat, echo)

1. `echo`, command untuk display atau write ke file

![7](/week-1/day03/images/7.png)

2. `cat`, command untuk lihat isi file

![8](/week-1/day03/images/8.png)

3. `sed`, command untuk memanipulasi text secara langsung tanpa harus melihat isi file nya.

![9](/week-1/day03/images/9.png)

4. `grep`, command untuk mencari kata/kalimat tertentu pada file (Ctrl + f di linux).

![10](/week-1/day03/images/10.png)


## Nyalakan ufw dengan memberikan akses untuk port 22, 80, 443, 3000, 5000 dan 6969

1. Enable ufw dengan command `sudo ufw enable`

![11](/week-1/day03/images/11.png)

2. Agar tidak satu per-satu memasukkan portnya, di sini saya menggunakan perulangan for untuk memasukkan portnya.

![12](/week-1/day03/images/12.png)