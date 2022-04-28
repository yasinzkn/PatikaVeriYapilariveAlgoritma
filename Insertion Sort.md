# Insertion Sort Projesi
[www.patika.dev](https://www.patika.dev) Veri Yapıları ve Algoritmalar Ödevi-1

***
## Soru 1
**[22,27,16,2,18,6]** -> Insertion Sort

* Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.
* Big-O gösterimini yazınız.
* Time Complexity: Average case: Aradığımız sayının ortada olması,Worst case: Aradığımız sayının sonda olması, Best case: Aradığımız sayının dizinin en başında olması.
* Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.


## Çözüm

### Aşamalar
* ***Birinci Aşama:*** 22 ile 27'yi karşılaştırır. 22, 27'den küçük olduğu için bir değişiklik yapmaz.

    [22,**27**,16,2,18,6] **->** [22,**27**,16,2,18,6]

* ***İkinci Aşama:*** 27 ile 16'yı karşılaştırır. 16, 27'den küçük olduğu için 16 ile 27 yer değiştirir. Daha sonra 16 ile 22'yi karşılaştırır. 16, 22'den küçük olduğu için 16 ile 22'nin de yerini değiştirir.

  [22,27,**16**,2,18,6] **->** [22,**16**,27,2,18,6] **->** [**16**,22,27,2,18,6]

* ***Üçüncü Aşama:*** 2 ile 27'yi karşılaştırır. 2, 27'den küçük olduğu için 27 ile 2 yer değiştirir. Daha sonra 2 ile 22'yi karşılaştırır. 2, 22'den küçük olduğu için bu defa 22 ile 2'nin yerinin değiştirir. Son olarak 2 ile 16'yı karşılaştırır 2 yine küçük olduğu için 2 ile 16'nın yeri değişir ve 2 en başa geçmiş olur.

  [16,22,27,**2**18,6] **->** [16,22,**2**,27,18,6] **->** [16,**2**,22,27,18,6] **->** [**2**,16,22,27,18,6]

* ***Dördüncü Aşama:*** 18 ile 27'yi karşılaştırır. 18, 27'den küçük olduğu için yerlerini değiştirir. Daha sonra 18 ile 22 arasında bir karşılaştırma yapar. 18, 22'den küçük olduğu için 18 ile 22'nin yerlerinin değiştirir. 18 ile 16 arasında tekrar bir karşılaştırma işlemi yapar. 18, 16'dan büyük olduğu için herhangi bir değişiklik yapmaz.

  [2,16,22,27,**18**,6] **->** [2,16,22,**18**,27,6] **->** [2,16,**18**,22,27,6]

* ***Beşinci Aşama:*** 6 ile 27'yi karşılaştırır. 6, 27'den küçük olduğu için yerlerini değiştirir. Sonra 6 ile 22 arasında bir karşılaştırma yapar. 6, 22'den küçük olduğu için yerlerini değiştirir. Tekrar bir karşılaştırma yapar. 6 ile 18'i karşılaştırır. 6, 18'den küçük olduğu için yerlerini değiştirir. 6 ile 16 arasında tekrar bir karşılaştırma işlemi gerçekleşir. Bu karşılaştırmanın sonucunda 6, 16'dan küçük olduğu için 6 ile 16'nın yeri değişir. Son olarak 6 ile 2 arasında bir karşılaştırma işlemi yapılır. 6, 2'den büyük olduğu için herhangi bir değişiklik yapılmaz.

  [2,16,18,22,27,**6**] **->** [2,16,18,22,**6**,27] **->** [2,16,18,**6**,22,27] **->** [2,16,**6**,18,22,27] **->** [2,**6**,16,18,22,27]

* **Dizinin son hali ***[2,6,16,18,22,27]*** şeklinde olur.**

### Big-O Gösterimi

* **Best Case:** 

   O(n)

* **Worst Case:**

  O(n<sup>2</sup>)

* **Average Case:**

  O(n<sup>2</sup>)

     18 sayısı ***Average Case*** kapsamına girer.

***

## Soru 2
[7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.


## Çözüm

* **Birinci Adım:**
 7 ile 3'ü karşılaştırır. 7, 3'ten büyük olduğu için yerlerini değiştirir.

  [**7**,3,5,8,2,9,4,15,6] **->** [3,**7**,5,8,2,9,4,15,6]

* **İkinci Adım:**
7 ile 5'i karşılaştırır. 7, 5'ten büyük olduğu için yerlerinin değiştirir.

  [3,7,**5**,8,2,9,4,15,6] **->** [3,**5**,7,8,2,9,4,15,6]

* **Üçüncü Adım:**
7 ile 8'i karşılaştırır. 7, 8'den küçüm olduğu için herhangi bir işlem yapmaz ve sıralamayı değiştirmez.

  [3,5,**7,8**,2,9,4,15,6]

* **Dördüncü Adım:**
8 ile 2'yi karşılaştırır. 8, 2'den büyük olduğu için yerlerini değiştirir.

  [3,5,7,8,**2**,9,4,15,6] **->** [3,5,7,**2**,8,9,4,15,6]
