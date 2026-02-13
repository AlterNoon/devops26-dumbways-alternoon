## Reverse Proxy

![1](/week-2/day06/images/proxy.png)

Kalau menggunakan analogi restaurant, forward proxy itu misalkan kita ingin makan di restaurant tapi tidak ingin bertemu dengan pelayan (server), maka kita menyuruh orang lain untuk melakukan reservasi ke restaurant tersebut, jadi bisa dikatakan orang lain itu disebut dengan perantara (proxy).
Sedangkan reverse proxy, semisal ketika client ingin makan di restaurant, kemudian pelayan tersebut sudah tahu kalau si client ini food vlogger, maka si pelayan akan memberi tahu spot meja makan yang bagus untuk shooting video si food vlogger, kemudian jika ada client vip, maka akan diberi tahu spot meja makan yang lebih private. Reverse proxy ada untuk protect server, sedangkan forward proxy ada untuk protect client.

Reverse proxy bekerja sebagai perantara antara server tujuan dan client. Ketika client melakukan request, reverse proxy menerima permintaan tersebut dan meneruskannya ke server tujuan. Kemudian, server tujuan memberikan respons ke reverse proxy (html, json), dan reverse proxy meneruskannya kembali ke client.

## Buatlah Reverse Proxy untuk aplikasi yang sudah kalian deploy kemarin. (wayshub), untuk domain nya sesuaikan nama masing"

1. Edit file host yang terletak pada `Windows/System32/drivers/etc`. Add server ip and domain.

![1](/week-2/day06/images/1.png)

2. Pastikan status nginx sudah running dan cek pada website (firewall port 80 enable)

![2](/week-2/day06/images/2.png)
![2-1](/week-2/day06/images/2-1.png)

3. Masuk ke directory nginx dan buat file baru bernama wayshub.conf pada direktori sites-enabled

![3](/week-2/day06/images/3.png)

4. Set configurasi seperti codingan di bawah dan berjalan pada port 3000

![4](/week-2/day06/images/4.png)

5. Test configurasi apakah sudah berhasil

![5](/week-2/day06/images/5.png)

6. Restart service nginx

![6](/week-2/day06/images/6.png)

3. Web sudah bisa dibuka dengan domain naufal.xyz

![7](/week-2/day06/images/7.png)

