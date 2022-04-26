# Merge Sort Projesi
[Yasin Özkan](https://github.com/yasinzkn) Veri Yapıları ve Algoritmalar Ödevi-2

***
## Soru
**[16,21,11,8,12,22]** -> Merge Sort

* Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
* Big-O gösterimini yazınız.


## Çözüm

### Aşamalar
* ***Birinci Aşama:*** Öncelikle dizi **[16,21,11]** ve **[8,12,22]** şeklinde 2'ye ayrılır.

  * **[16,21,11] - [8,12,22]**

* ***İkinci Aşama:*** Daha sonra dizi **[16] - [21,11]** ve **[8,12] - [22]** şeklinde tekrar ayrılır.

  * **[16]** - **[21,11]** | **[8,12]** - **[22]**

* ***Üçüncü Aşama:*** Bir sonraki adımda dizi **[16], [21], [11]** ve **[8], [12], [22]** olacak şekilde tekrar ayrılır.

  * **[16]** - **[21]** - **[11]** | **[8]** - **[12]** - **[22]**

* ***Dördüncü Aşama:*** Dizi tek eleman kalana kadar ayrıldı. Artık birleştirilme aşamasına geçilecek. Dizide bu aşamada küçük sayı en başta olacak şekilde birleştirme işlemi yapılmaya başlar. 16, 21'den küçük olduğu için zaten sıralı durumdadır. 21 ile 11 kıyaslandıktan sonra ise dizinin sol tarafında oluşacak şekil **[16]-[11,21]** olacaktır. Dizinin sağ tarafında ise zaten küçükten büyüğe doğru sıralı olduğu için bir değişiklik olmayacaktır. Bu aşamada son görüntü şöyle olur:

  * **[16]** - **[11,21]** | **[8,12]** - **[22]**

* ***Beşinci Aşama:*** Sıradaki adımda tekrar bir birleştirme işlemine gidilecektir. Bu değişiklik yine dizinin sol tarafında olacaktır. 16 ile 11 kıyaslandıktan sonra 11, 16'dan küçük olduğu için ilk eleman olarak 11 yazılacaktır.

  * **[11,16,21]** - **[8,12,22]**

* ***Altıncı Aşama:*** Bu aşamada dizi artık bir sıraya konularak tekrar bir araya getirilecektir. Dizi sıralanmış biçimdeki son hali şu şekilde olur:

  * **[8,11,12,16,21,22]**

### Big-O Gösterimi
 * O(nlogn)
