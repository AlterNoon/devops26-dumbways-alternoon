# Day 1 - Introduction to DevOps

## Devops
Devops itu kaya semacam jembatan antara code sama cloud, yang dimana tugasnya mempercepat proses development sampai staging production ke publik. Jadi kita harus mastiin kode kita itu bisa dideploy di production tanpa mengganggu berjalannya sistem.
Why we need DevOps? 
Bayangin di suatu perusahaan itu ada team frontend dan team backend, pada sprint pertama setiap timnya ingin membuat fitur yang berbeda, ketika selesai masing2 dari team mengupload codenya di branch repository, nah beberapa bulan kemudian ketika waktunya dimerge, ternyata masing2 branch itu conflict satu sama lain, entah karena tidak compatible atau buildnya fail, jika sudah terjadi seperti itu maka akan makan banyak waktu lagi untuk fixnya.
Nah disinilah tugas DevOps, yaitu membuat suatu workflow, di mana ketika setiap developer melakukan commit, maka akan trigger an automated workflow pada server. Jadi kalau semisalkan ada error pada code, bisa segera difix oleh developer.
Maka dari itu kunci dari DevOps adalah CI/CD, jadi ya kalo kita gabisa automasi pasti bakalan ribet bgt production itu.


## Install Ubuntu Server 22.04 LTS with VirtualBox

1. Langkah pertama yaitu klik new untuk membuat vm kemudian masukkan ISO Ubuntu 22.04 yang sudah didownload.
tidak perlu centang unattended agar tidak mengisi detail info os.

![1](/week-1/day01/images/1.png)


2. Choose 2 GB of base memory with 2 CPU and 10 GB Storage.

![2](/week-1/day01/images/2.png)

3. Cek kembali untuk configurasinya apakah sudah sesuai, jika sudah klik finish. Sebelum menjalankan vm, klik setting untuk configurasi network, pada adapter pilih bridged adapter dan cocokkan dengan versi yang dipakai pada laptop.
Kenapa pada bridged adapter? karena nanti kita akan config ip manual. Sedangkan kalau pakai Nat ip nya harus dhcp

![3](/week-1/day01/images/3.png)

![3](/week-1/day01/images/3-1.png)

4. Pilih language english

![4](/week-1/day01/images/4.png)

5. Tidak perlu untuk update installer 

![5](/week-1/day01/images/5.png)

6. Pilih default install agar lebih leluasa untuk manage vm

![6](/week-1/day01/images/6.png)

7. Di sini kita akan configurasi manual untuk ipnya, pilih edit IPv4

![7](/week-1/day01/images/7.png)

8. Pada Task 1, diharuskan untuk menentukan "alamat rumah" saya menjadi xxx.xxx.xxx.208. 
Atur subnet menjadi 192.168.1.0/24 addres 192.168.1.208 gateway 192.168.1.1 name server 8.8.8.8, 8.8.4.4 kemudian pilih save.

![8](/week-1/day01/images/8.png)

9. Pada storage configuration, kita akan custom storage sesuai kebutuhan.

![9](/week-1/day01/images/9.png)

10. Pilih free space kemudian pilih gpt partition.

![10](/week-1/day01/images/10.png)

11. Create partition 7gb

![11](/week-1/day01/images/11.png)

12. Create swap partition for 2.8gb

![12](/week-1/day01/images/12.png)

13. Jika sudah sesuai kebutuhan, klik done.

![13](/week-1/day01/images/13.png)

14. Profile configurasi sesuai dengan user.

![14](/week-1/day01/images/14.png)

15. Tidak perlu install SSH untuk saat ini. Jika sudah sesuai semua maka klik continue to install Ubuntu OS, ini akan memakan waktu beberapa menit.

![15](/week-1/day01/images/15.png)

16. Jika instalasi OS berhasil maka akan muncul menu user login.

![16](/week-1/day01/images/16.png)

17. Test ping 8.8.8.8 dan google.com. Jika network unreachable pastikan network configuration sudah diubah menjadi bridged adapter.

![17](/week-1/day01/images/17.png)