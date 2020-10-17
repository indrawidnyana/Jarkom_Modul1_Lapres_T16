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

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767056880614637588/unknown.png) \
>awalnya dari data dump yang berasa dari soal,  kami mengolahnya menggunakan syntax untuk memfilter file dengan nama **Answer.zip**, dengan menggunakan syntax ```ftp-data contains Answer.zip``` , maka akan muncul beberapa hasil paket seperti pada gambar diatas

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767057198210744401/unknown.png) \
>Selanjutnya kami melakukan **Follow -> TCP Stream** untuk mengecek data didalam paket tersebut. Lalu kami mencari stream baik itu diatas dan ataupun dibawah hingga menemukan paket yang kami curigai berisi file **OpenThis.pdf** yaitu pada stream **ke-12**

![picture](https://cdn.discordapp.com/attachments/691272864644595743/767057401546801222/unknown.png) \
>Setelah itu kami mengubah show and save data as nya menjadi **RAW** dan melakukan save as file dengan nama **nomor6.zip**
