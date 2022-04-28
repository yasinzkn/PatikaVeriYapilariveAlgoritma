# Binary Search Tree Projesi
[www.patika.dev](https://www.patika.dev) Veri Yapıları ve Algoritmalar Ödevi-3

***
## Soru
**[7,5,1,8,3,6,0,9,4,2]** dizisinin Binary-Search-Tree aşamalarını yazınız.

* Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.


## Çözüm
### Aşamalar
* ***Birinci Aşama:*** Öncelikle diziyi sıralarız.Diziyi sıraladıktan sonra ortanca sayıyı root olarak belirleriz.

  * **[0,1,2,3,4,5,6,7,8,9]**

* ***İkinci Aşama:*** Bu aşamada root ya 4 ya da 5 olacaktır, ikisinden birisi tercih edilebilir.Root 4 olarak seçersek yapı şu şekilde olacaktır;

  * 4'ten küçük olanlar sol tarafa, büyük olanlar sağ tarafa yerleşecek. + root olarak seçildikten sonra sol ve taraf değerler için yine bir ortanca sayı seçilir ve buna göre yapı oluşturulur.

                4
               / \
              2   7

* ***Üçüncü Aşama:*** Daha sonra sol taraf için 2'den büyük değerler sağ tarafa, küçük değerler ise sol tarafa gelecek. Sağ taraf için ise 7'den büyük değerler sağ tarafa küçük değerler sol tarafa yazılacaktır.
  * Bu durumda 3. adım şu şekilde olur;

                4   
              /   \
             2     7
            / \   / \
           1   3 6   8 

* ***Dördüncü Aşama:*** Bu aşamada sol taraf değerlere bakılır 1'den küçük değer olduğu için düğümün altına o değer eklenir. 3 ile ilgili sağ veya sol tarafına herhangi bir yeni düğüm ekleme olmaz. Sağ taraf değerler için 6'nın sol tarafına yeni bir düğüm, 8'in ise sağ tarafına yeni bir düğüm eklenir.
  * Bu durumda şu şekil karşımıza çıkar.

                4  
              /   \
             2     7
            / \   / \
           1   3 6   8
          /     /     \
         0     5       9

* Artık yapı oluştu. Yapının son hali şu şekilde olur;
  * **Root: 4**
  
                4  
              /   \
             2     7
            / \   / \
           1   3 6   8
          /     /     \
         0     5       9
