# **LAPRES MODUL 1** 
-----------------------------------
## **KELOMPOK T_16**
## I Gede Pradhana Indra Widnyana (05311840000031)
## Bagus Farhan Abdillah (05311840000016)
-----------------------------------
## A. Display Filter
### Soal 6 :
### Mendownload dan mengextract suatu zip hingga mendapatkan file dengan nama **OpenThis.pdf**
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767056759965614160/unknown.png)

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767056880614637588/unknown.png)
<br />
>awalnya dari data dump yang berasa dari soal,  kami mengolahnya menggunakan syntax untuk memfilter file dengan nama **Answer.zip**, dengan menggunakan syntax ```ftp-data contains Answer.zip``` , maka akan muncul beberapa hasil paket seperti pada gambar diatas

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767057198210744401/unknown.png)
<br />
>Selanjutnya kami melakukan **Follow -> TCP Stream** untuk mengecek data didalam paket tersebut. Lalu kami mencari stream baik itu diatas dan ataupun dibawah hingga menemukan paket yang kami curigai berisi file **OpenThis.pdf** yaitu pada stream **ke-12**

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767057401546801222/unknown.png) 
<br />
>Setelah itu kami mengubah show and save data as nya menjadi **RAW** dan melakukan save as file dengan nama **nomor6.zip**

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767057640970518568/unknown.png) 
<br />
>Untuk mencari password dari file .zip tersebut, kami melakukan filtering lagi dengan menggunakan syntax ```ftp-data contains zipkey.txt``` seperti pada gambar. 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767057640970518568/unknown.png) 
<br />
>Lalu selanjutnya kami melakuka metode yang sama yaitu **Follow -> TCP Stream** hingga menemukan stream password pada gambar diatas. 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767057882020577310/unknown.png) 
<br />
>Setelah itu kami memasukkan password yang kami dapatkan pada stream sebelumnya dan mendapatkan file dengan nama **OpenThis.pdf**

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767058003299401768/unknown.png) 
<br />
>Gambar diatas adalah isi dari file **OpenThis.pdf** yang kami temukan 

### Soal 7 :
### Mendownload dan mengextract suatu zip hingga mendapatkan file dengan isi puisi dengan clue file **Yes.pdf**
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767065517697138719/unknown.png)
<br />
>Awalnya dari data yang di dump, kami melakukan filtering dengan syntax ```ftp-data contains Yes.pdf``` karena **Yes.pdf** merupakan clue utama pada soal. setelah itu kami menemukan beberapa paket sesuai dengan gambar diatas

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767065713118150686/unknown.png)
![picture](https://cdn.discordapp.com/attachments/691272864644595743/767065782689202196/unknown.png)
<br />
>Setelah itu kami melakukan **Follow -> TCP Stream** dan mengecek stream yang kira-kira berisi file **Yes.pdf** dan kebetulan sesuai dengan gambar, kami mencurigai file tersebut ada di dalam stream nomor 442.

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767065924640833536/unknown.png)
<br />
>Lalu kami melakukan save as file dengan mengubah tipe stream menjadi **RAW** terlebih dahulu dan menyimpan file dengan nama **No.7**

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767066077728866354/unknown.png)
![picture](https://cdn.discordapp.com/attachments/691272864644595743/767066201359777822/unknown.png)
<br />
>Setelah itu kami melakukan exctract dalam file dan mendapati file **Yes.pdf** ada di dalam file zip tersebut. Gambar puisi yang berisi di dalam file **Yes.pdf** dapat dilihat pada gambar diatas



-----------------------------------
## B. Capture Filter
### Soal 11 :
### Melakukan filter sehingga wireshark hanya mengambil paket yang mengandung port 21 (lokal)
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767070833817681930/unknown.png)
<br />
>Awalnya kami sudah membuat local user dengan nama **User** yang dimana ini akan kami connect dengan **filezilla dan filezilla** server untuk melakukan pengencekan setiap paket yang lewat ke **Port 21 (lokal)** sesuai dengan gambar diatas

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767071088436969563/unknown.png)
<br />
>Selanjutnya kami melakukan remote login pada filezilla sesuai dengan user yang telah kami buat dan karena pada server lokal, port yang tercantum adalah **Port 21** seperti pada gambar diatas

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767071350187360266/unknown.png)
<br />
>Gambar diatas merupakan gambar sesudah kami melakukan remote login dengan filezilla dalam mode local server

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767071553329954856/unknown.png)
<br />
>Untuk mengetahui paket apa saja yang melalui port 21, maka kami melakukan **Capture filter** dengan menggunakan syntax ```port 21``` sehingga apapun paket ataupun hal yang dilakukan pada port tersebut akan terekan **Log**nya.

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767071735270735872/unknown.png)
<br />
>Setelah melakukan beberapa proses baik pengiriman data dari server ataupun sebaliknya, kami mendapatkan semua log paket yang melalui port 21 seperti gambar diatas.

### Soal 12 :
### Melakukan filter sehingga wireshark hanya mengambil paket yang berasal dari port 80 (Data hanya untuk web http karena port 80 adalah port http)
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767083044477337640/unknown.png)
<br />
>Awalnya kami melakukan **Capture Filter** dengan menggunakan syntax ```src port 80``` . menggunakan src karena src merupakan kepanjangan dari **source** yang dimana paket yang ditampilkan adalah paket yang berasal dari port 80

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767083191294885908/unknown.png)
<br />
>Selanjutnya kami membuka website ```http://elearning.if.its.ac.id/``` . kami mencoba di elearning IF karena website tersbut adalah salah satu website yang menggunakan **http** sehingga menggunakan **Port 80** sesuai dengan permintaan soal

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767083645114122341/unknown.png)

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767083740299264005/unknown.png)
<br />
>Setelah kami melakukan akses ke website dengan **http** , maka akan terlihat log paket seperti pada gambar diatas. untuk mengetahui apakah paket tersebut semuanya berasal dari **Port 80** dapat dilihat digambar diatas yang dimana paket berasal dari **Port 80 menuju ke Port X**

### Soal 13 :
### Melakukan filter sehingga wireshark hanya menampilkan paket yang menuju port 443 (Data hanya untuk web https karena port 443 adalah port https)
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767083044477337640/unknown.png)
<br />
>Awalnya kami melakukan **Capture Filter** dengan menggunakan syntax ```src port 80``` . menggunakan src karena src merupakan kepanjangan dari **source** yang dimana paket yang ditampilkan adalah paket yang berasal dari port 80


