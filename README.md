# **LAPRES_MODUL 1_JARKOM** 
-----------------------------------
## **KELOMPOK T_16**
## Bagus Farhan Abdillah (05311840000016)
## I Gede Pradhana Indra Widnyana (05311840000031)

-----------------------------------
## A. Display Filter

### Soal 1 :
### Webserver yang digunakan pada "testing.mekanis.me” adalah sebagai berikut :
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767120694264725523/unknown.png)
<br />
>Data yang awalnya sebelum dilakukan filter adalah seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767121175490199572/unknown.png)
<br />
>Selanjutnya kami melakukan filter dengan syntax ```http.host==”testing.mekanis.me``` seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767121774604976138/unknown.png)
<br /> 
>Selanjutnya kami melakukan follow paket dengan melakukan **Follow -> TCP Stream** seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767122242265939978/unknown.png)
<br />
>Lalu akan muncul window baru setelah metode follow tersebut dan dapat dilihat bahwa server yang digunakan adalah **Nginx/1.14.0 (ubuntu)**.

### Soal 2 :
### Mendownload gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"
## Jawab :

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767120694264725523/unknown.png)
<br />
>Data yang awalnya sebelum dilakukan filter adalah seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767123028152025119/unknown.png)
<br />
>Selanjutnya kami melakukan filter dengan syntax ```http.request.uri contain Tim```. Maka akan muncul seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767123580047327242/unknown.png)
<br /> 
>Pilih paket yang akan di download dengan cara klik **File -> Export Object -> Http** pada menu bar dan akan keluar tab baru seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767124298535665695/unknown.png)
<br />
>Ketik Nama file yang akan diunduh pada kolom text filter lalu klik save.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767124776401502228/Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg)
<br />
>Dan gambar diatas merupakan hasil dari gambar yang telah diunduh.

### Soal 3 :
### Mencari username dan password ketika login di "ppid.dpr.go.id"**
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767120694264725523/unknown.png)
<br />
>Data yang awalnya sebelum dilakukan filter adalah seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767125471573573662/unknown.png)
<br />
>Selanjutnya kami melakukan filter dengan syntax ```http.request.uri contains "login”``` seperti gambar diatas.

![picture](https://media.discordapp.net/attachments/767120480167133215/767125819930837032/unknown.png)
<br />
>Lalu kami menemukan login dan password pada ppid.dpr.go.id pada paket yang kami tandai seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767125471573573662/unknown.png)
<br />
>Selanjutnya dari data paket diatas, lihat pada kolom HTML from URL terdapat item yaitu **username = 10pemuda dan password = guncangdunia**.

### Soal 4 :
### Mencari paket dari web-web yang menggunakan basic authentication method**
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767120694264725523/unknown.png)
<br />
>Data yang awalnya sebelum dilakukan filter adalah seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767126640635412480/unknown.png)
<br />
>Selanjutnya kami melakukan filter dengan syntax ```http.authbasic``` seperti gambar diatas.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767127074510602250/unknown.png)
<br />
>Dan kami menemukan bahwa ```testing.mekanisme.me``` merupakan web pertama yang menggunakan basic authentication.

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767127799457644625/unknown.png)
<br />
>Dan ```aku.pengen.pw``` merupakan web kedua yang kami temukan menggunakan basic authentication.

### Soal 5 :
### Mengikuti perintah di ```aku.pengen.pw```, Username dan password bisa didapatkan dari file .pcapng
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/767120480167133215/767120694264725523/unknown.png)
<br />
>Data yang awalnya sebelum dilakukan filter adalah seperti gambar diatas.





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

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767087800457494628/unknown.png)
<br />
>Awalnya kami melakukan **Capture Filter** dengan menggunakan syntax ```dst port 443``` . menggunakan dst karena dst merupakan kepanjangan dari **destination** yang dimana paket yang ditampilkan adalah paket yang menuju ke port 443

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767088045119766528/unknown.png)
<br />
>Selanjutnya kami membuka website ```https://www.google.com/``` . kami mencoba di google.com karena website tersbut adalah salah satu website yang menggunakan **https** sehingga menggunakan **Port 443** sesuai dengan permintaan soal

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767088162555428874/unknown.png)

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767088269892255795/unknown.png)
<br />
>Setelah kami melakukan akses ke website dengan **https** , maka akan terlihat log paket seperti pada gambar diatas. untuk mengetahui apakah paket tersebut semuanya menuju ke **Port 443** dapat dilihat digambar diatas yang dimana paket menuju ke **Port 443 yang berasal dari Port X**

### Soal 14 :
### Melakukan filter sehingga wireshark hanya mengambil paket yang berasal dari ip kami (dalam hal ini ip kami : 192.168.100.109)
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767093867983667200/unknown.png)
<br />
>Kami melakukan pencarian ip kami dan menemukan ip kami dengan menggunakan ```ipconfig``` pada **cmd** seperti gambar diatas

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767089871990554654/unknown.png)
<br />
>kami melakukan capture filter dengan menggunakan syntax ```src host 192.168.100.109``` yang dimana **src** adalah **source** yang berasal dari **host 192.168.100.109** yang dimana ip tersebut adalah ip kami pada saat melakukan test sebelumnya

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767089912977031198/unknown.png)
<br />
>Setelah melakukan beberapa kegiatan dalam browser, kami mendapatkan hasil capture filter yang sesuai dengan soal seperti gambar diatas.

### Soal 15 :
### Melakukan filter sehingga wireshark hanya mengambil paket yang tujuannya ke **monta.if.its.ac.id**
## Jawab : 

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767091747569795122/unknown.png)
<br />
>Pertama, karena yang diminta adalah paket yang **tujuannya ke monta.if.its.ac.id** maka kami menggunakan syntax ```dst monta.if.its.ac.id``` karena **dst** adalah kepanjangan dari **destination** ke **monta.if.its.ac.id**


![picture](https://cdn.discordapp.com/attachments/691272864644595743/767091857241931806/unknown.png)
<br />
>Gambar diatas adalah hasil capture paket **sebelum** kami mengakses website **monta.if.its.ac.id**

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767091950515257354/unknown.png)
<br />
>Gambar diatas adalah gambar disaat kami mengakses website **monta.if.its.ac.id**

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767092099937468426/unknown.png)
<br />
>Setelah mengakses website **monta.if.its.ac.id**, maka kami menemukan banyak paket yang **Tujuannya** adalah ke **monta.if.its.ac.id**



