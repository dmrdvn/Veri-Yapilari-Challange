
# Challange: Binary-Search-Tree
 
 **[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]** dizisinin Binary-Search-Tree aşamalarını yazınız.

Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.


 
# Problem 1

**[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]** dizisinin Binary-Search-Tree aşamalarını yazınız.

Binary Search Tree yönteminde ilk adım bir root eleman seçiyoruz.
Ardından seçtiğimiz root eleman ile dizindeki diğer elemanları sırayla karşılaştırıyoruz.
Sıralamada esas kriter, kıyaslanan eleman önceki elemandan büyükse sağ tarafa, küçük ise sol tarafa yazılır.
Örneğin karşılaştırılan eleman root ile karşılaştırıldıktan sonra root'un altında bulunan diğer elemanla da karşılaştırılır.

## Diyagram Üzerinde Gösterim

Binary Search Tree yöntemine göre sıralama adımları diyagram üzerinde tarif edilmiştir.

Root olarak dizinden bir eleman seçiyoruz. Örnekte root=7 seçilmiştir.

```mermaid
graph TD;

    A((Root = 7));
    B((5));
    C((8));
    D((1));
    E((6));
    F((8));
    G((0));
    H((3));
    I((2));
    J((4));


    A -- '5', '7' den küçük olduğu için sola --> B;
    A -- '8', '7' den küçük olduğu için sağa --> C;
    C -- '9', '8' den büyük olduğu için sağa --> F;
    B -- '1', '5' ten küçük olduğu için sola --> D;
    B -- '6', '5' ten büyük olduğu için sağa --> E;
    D -- '0', '1' den küçük olduğu için sola --> G;
    D -- '3', '1' den büyük olduğu için sağa --> H;
    H -- '2', '3' ten küçük olduğu için sola --> I;
    H -- '4', '3' den büyük olduğu için sağa --> J;
    
 
 ```
 
