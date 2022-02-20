# INSERTION-SORT
>Insertion Sort Bilgisayar bilimlerinde kullanılan bir sıralama algoritmasıdır. Amaç verilen örüntüye ait en küçük elemanı bulup solundaki eleman ile değiştirerek küçükten büyüğe sıralamaktır. Insertion Sortta Time Complexity durumları şunlardır:
  **_Best Case Complexity O(n)_**
  **_Average Case Complexity O(n^2)_**
  **_Worst Case Complexity O(n^2)_**
>>  Best Case Complexity verilen inputun algoritmamızı en hızlı şekilde çalıştırdığı durumdur. Verilen örüntü,dizi ya da öğedeki elemanlar zaten sıralıysa ortaya çıkar.Algoritma n tane elemanı n kere kontrol eder bu sebeple Big O Notation O(n)'dir.
>>  Average Case Complexity genel olarak beklediğim durumdur. Verilen dizi karışık haldedir yani tam olarak azalan ya da artan olarak sıralanmamış haldedir. Burada inputların geldiği dağılımı bilip ona göre analiz etmek gerekiyor. Average case'i analiz etmek diğerlerine göre çok daha zordur ancak algoritmamızın çalışmasını en iyi yansıtan case'dir. Big O Notation ise O(n^2)'dir.
>>  Worst Case Complexity verilen inputun algoritmamızı en yavaş şekilde yani en fazla işlem yapacak şekilde çalıştırdığı durumdur. Her elemanı birbiriyle karşılaştıracağı için her elemanı kontrol edecek bu sebeple Big O Notation O(n^2)'dir.
>>  
*Insertion Sort algoritmasının temel çalışma mantığı şu şekildedir. Verilen dizideki elemanlar 0'dan başlayarak indekslenir. İlk adımda key olarak 1. eleman seçilir ve 1. elemanla başlanır. 1. elemanın solundaki sayı büyükse 1. elemanla yer değiştirir. Eğer solundaki sayı zaten küçükse ya da o sayıya eşitse aynen kalır ve bir dahaki adımda dizinin 2. indeksindeki elemanın solundaki elemanlarla kontrole devam edilir. Küçük olan sola geçerken büyük olan sağa kayar yani bir bakıma yer değiştirirler.*

Örnek: [22,27,16,2,18,6]
Öncelikle Time complexity'nin Average case olduğunu söylememiz gerek. Dizi düzgün sıralı değil bu sebeple Best case değil. Aynı şekilde tersine bir sıralama da yok worst case değil diyebiliriz. Big o Notation O(n^2)'dir.
-1. adım : key = dizi[1] Burada 22<27 olduğu için aynen kalıyor. 
-2. adım : key = dizi[2] -> [16,22,27,2,18,6]
-3. adım : key = dizi[3] -> [2,16,22,27,18,6]
-4. adım: key = dizi[4] -> [2,16,18,22,27,6]
-5. adım : key = dizi[5] -> [2,6,16,18,22,27]

Örnek 2: [7,3,5,8,2,9,4,15,6]
-1. adım : key = dizi[1] -> [3,7,5,8,2,9,4,15,6]
-2. adım : key = dizi[2] -> [3,5,7,8,2,9,4,15,6]
-3. adım : key = dizi[3] -> [3,5,7,8,2,9,4,15,6]
-4. adım : key = dizi[4] -> [2,3,5,7,8,9,4,15,6]
-5. adım : key = dizi[5] -> [2,3,5,7,8,9,4,15,6]
-6. adım : key = dizi[6] -> [2,3,4,5,7,8,9,15,6]
-7. adım : key = dizi[7] -> [2,3,4,5,7,8,9,15,6]
-8. adım : key = dizi[8] -> [2,3,4,5,6,7,8,9,15]
