# **LAPRES MODUL 1** 
-----------------------------------
## **KELOMPOK T16**
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

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767056880614637588/unknown.png)
<br />
>awalnya dari data dump yang berasa dari soal,  kami mengolahnya menggunakan syntax untuk memfilter file dengan nama **Answer.zip**, dengan menggunakan syntax ```ftp-data contains Answer.zip``` , maka akan muncul beberapa hasil paket seperti pada gambar diatas
