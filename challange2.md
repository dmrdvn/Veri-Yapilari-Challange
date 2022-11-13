
# Challange: Merge Sort
 
 **Problem #1:**  

 **[ 16, 21, 11, 8, 12, 22 ]** -> Merge Sort

- Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.

- Big-O gösterimini yazınız.


 
# Problem 1

**[ 16, 21, 11, 8, 12, 22 ]** -> Merge Sort

Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.

-------------------------
[ 16, 21, 11, 8, 12, 22 ]


1- Yukarıdaki diziyi ortadan ikiye ayırıyoruz.

    [ 16, 21, 11 ] - [ 8, 12, 22 ]

2- Tek kalana kadar dizi elemanlarını gruplandırarak birbirinden ayırıyoruz.

    [ 16 ] - [ 21, 11 ] - [ 8 ] - [ 12, 22 ]
    
3- Ayırma işlemi tamamlandığında elimde 9 grup eleman mevcut.

    [ 16 ] - [ 21 ] - [ 11 ] - [ 8 ] - [ 12 ] - [ 22 ]

4- Ayırma tamamlandı. Bundan sonra elemanları sıralayarak birleştiriyoruz.

    [ 16 ] - [ 11, 21 ] - [ 8 ] - [ 12, 22 ]

5- En küçük en başa olacak şekilde tekrar birleştirme yapıyoruz.

    [ 11, 16, 21 ] - [ 8, 12, 22 ]

6- Tüm elemanlar sıralı bir şekilde birleşmiş oldu.

    [ 8, 11, 12, 16, 21, 22 ]

Not: Elemanları sıralı birleştirirken uygulanan proses;

- Önce soldaki grubun ilk elemanını al, sağdaki grubun ilk elemanı ile karşılaştır.
- Sonra soldaki grubun ikinci elemanını al soldaki gruptaki diğer elemanlarla karşılaştır.
- Bu şekide soldaki gruptaki tüm elemanları sağ gruptaki tüm elemanlarla kıyaslayarak en küçüğünü buluyoruz ve tekrardan gruplandırıyoruz.

## Diyagram Üzerinde Gösterim

Ayırma ve Birleştirme adımları diyagram üzerinde tarif edilmiştir.


### Ayırma İşlemleri:

Elemanları sıralayabilmek için önce tek eleman kalana kadar ayırıyoruz.

```mermaid
graph TD;
    A(16, 21, 11, 8, 12, 22) -- 3ünü sola ayırdık -->B;
    A-->C;
    B(16, 21, 11)-->D;
    B-->E;
    D(16)-->H;
    E(21, 11)-->I;
    E-->J;
    C(8, 12, 22)-->F;
    C-->G;
    F(8)-->K;
    G-->L;
    G(12, 22)-->M;
    H((16));
    I((21));
    J((11));
    K((8));
    L((12));
    M((22));
 ```
 
### Birleştirme İşlemleri:

Yukarıda tekli gruplara düşürdüğümüz elemanları sıralayarak tekrar gruplandırıyoruz.

```mermaid
graph TD;
   
    H((16));
    I((21));
    J((11));
    K((8));
    L((12));
    M((22));
    
    H-->N;
    I-->O;
    J-->O;
    K-->P;
    L-->R;
    M-->R;
    
    N(16)-- Sağ kutu ile karşılaştır,en küçüğü aşağıya yaz. -->S;
    O(11, 21)-->S;
    P(8)-->T;
    R(12, 22)-->T;
    
    S(11, 16, 21)-->U;
    T(8,12,22)-->U(8, 11, 12, 16, 21, 22);
 ```

## Big-O Gösterimi

O(nlogn)
