# Challange: Insertion Sort
 
 **Problem #1:**   [22,27,16,2,18,6] -> Insertion Sort
Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.

-> Big-O gösterimini yazınız.

-> Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız

	Average case: Aradığımız sayının ortada olması durumu
	Worst case: Aradığımız sayının sonda olması durumu
	Best case: Aradığımız sayının dizinin en başında olması durumu


 **Problem #2:**  [7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.
 
# Problem 1
**[22,27,16,2,18,6]**  -> Verilen dizinin **Insertion sort** türüne göre aşamalarını yazınız.

- "2" dizinin en küçük sayısı olduğundan sıralama için en başa alıyoruz ve 22 ile yer değiştiriyoruz. Yeni sıralama aşağıdaki gibi olmakta. 
	>[ **2,** 27, 16, 22, 18, 6 ]  
- Dizinin "2" den sonra en küçük eleman "6" olduğundan "6" ile "27" elemanlarını yer değiştiriyoruz. Yeni sıralama aşağıdaki gibi olmakta. 
	> [ **2, 6,** 16, 22, 18, 27 ] 
- Dizide "6" dan sonraki en küçük eleman "16" olduğundan üçüncü sıra için işlem yapmamıza gerek kalmadan 4.sıraya bakıyoruz. Burada ise "16" dan sonraki en küçük eleman olan "18" i dördüncü sıraya alabilmek için "22" ile yer değiştiriyoruz. 
	> [ **2, 6, 16, 18,** 22, 27 ]
- Beşinci ve altıncı sıradaki elemanlar zaten sıralı olduğundan dizimiz sıraya alınmış oluyor.
	> [ **2, 6, 16, 18, 22, 27** ]

## Big-O gösteriminin yapılması

- Dizinin eleman sayısına n dersek; diziyi sıralamak için her elemana bakıyoruz ve n kadar işlem yapmış oluyoruz.
- İkinci küçük elemanı bulmak için n-1 işlem yapmış oluyoruz
- Üçüncü adımda önceki iki elemandan sonraki en küçük elemanı bulmak için n-2 tane işlem yapıyoruz.
- Dördüncü adımda üç en küçük elemandan sonraki en küçük elemanı bulmak için n-3 tane işlem yapıyorum
- Beşinci adımda önceki dört elemandan sonraki en küçük elemanı bulmak için n-4 tane işlem yapıyorum
- Sonuç olarak dizi 6 elemanlı olduğu için altıncı adıma gerek kalmadan son elaman altıncı elaman olmuş oluyor.

Yani $n + (n-1) + (n-2) + (n-3) + (n-4) + n$ adet işlem yapıldı.

Dizimiz 6 elemanlı olduğuna göre; 
6 + (6-1) + (6-2) + (6-3) + (6-4) + 6 tanımlaması ile birlikte 21 adet işlemde diziyi sıralamış olduk.

Big-O cinsinden açıklarsak olayı, bu bana birden n'e kadar olan sayıların toplamını veriyor. birden n'e kadar sayıların toplama formülü [n(n+1)]/2 
Bunu da açarsak (n²+n)/2 çıkar. Bunu domine eden fonksiyonu aldığımız için n² değerini alıyoruz. 

Big-O değeri = O(n²)

## Time Complexity

Time Complexity 18 sayısı için sıralarsak, 18 ifadesi ortada kaldığı için **Avarage Case**'e girer.

Average Case:  [ **2, 6, 16, 18, 22, 27** ]

	Average case: Aradığımız sayının ortada olması durumu
	Worst case: Aradığımız sayının sonda olması durumu
	Best case: Aradığımız sayının dizinin en başında olması durumu
	
# Problem 2

[7, 3, 5, 8, 2, 9, 4, 15, 6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.



[**2</span>,** 3, 5, 8, 7, 9, 4, 15, 6]	==> **1. Adım :** 2 en küçük olduğu için başa alınır.

[**2, 3,** 5, 8, 7, 9, 5, 15, 6]	==> **2. Adım :** Sonraki küçük 3 olduğu için aynı yerine kalır.

[**2, 3, 4,** 8, 7, 9, 5, 15, 6]	==> **3. Adım :** 4 daha küçük olduğu için 5 ile yer değişir.

[**2, 3, 4, 5,** 7, 9, 8, 15, 6]	==> **4. Adım :** 5 daha küçük olduğu için 8 ile yer değişir.

