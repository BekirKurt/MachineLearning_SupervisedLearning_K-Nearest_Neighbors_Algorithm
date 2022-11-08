# KNN Algoritması
        K-En Yakın Komşular Algoritması, 1951 yılında Joseph Hodges ve Evelyn Fix tarafından geliştirilmiş daha sonra 1965 yılında N.J. Nilson'un minimum uzaklık sınıflayıcı çalışmaları ile hız kazanmış ve 1967 yılında Thomos M. Cover ve Peter E. Hart tarafından istatiksel analizlere (Regresyon) yönelik kullanılması yönünde genişletilmiştir.
        K-En Yakın Komşular Algoritması, regresyon çalışmaları ve sınıflandırma çalışmaları içerisinde kullanılmasıyla tercih edilen popüler bir algoritmadır.
        
        ![mlimage1](https://user-images.githubusercontent.com/73036927/200666797-af900648-220a-468e-96b6-ef0340174d44.png)

        Sınıflandırma yapmak için "en yakın" k tane noktayı(en yakın komşular) kullanılır. K-En Yakın Komşular Algoritması yapmak için üç şey gerekir :
        <ul>
            <li>Etiketlenmiş kayıtlar kümesi</li>
            <li>Uzaklık metriği(kayıtlar arasında mesafeyi hesaplamak için)</li>
            <li>K değeri(alınacak en yakın komşuların sayısı)</li>
        </ul>
  
  <h4>KNN(K-En Yakın Komşu) Algoritmasının Çalışma Mantığı</h4>
        KNN algoritmasını kullanabilmemiz için öncesinde elimizde bir veri seti bulunmalı ve bu veri seti sınıflandırılmış olmalı. Veri setine yeni bir veri eklendiğinde KNN algoritması, girilen verinin hangi gruba dahil olduğunu bulmaya çalışır. Bunun için veri setine sonradan eklenen veriye en yakın K adet veriye bakar ve ardından bu verilerin çoğunluğu hangi gruptaysa, yeni eklenen veriyi de o gruba dahil eder.
        
<h2>KNN(K-En Yakın Komşular) Uzaklık Hesaplaması</h2>
          <ul>
            <li>Euclidean Uzaklığı</li>
            <li>Manhattan Uzaklığı</li>
            <li>Minkowski Uzaklığı</li>
            <li>Hamming Uzaklığı</li>
            <li>Jacckard İndeksi Uzaklığı</li>
            <li>Mahalonobis Uzaklığı</li>
            <li>Haversiene Uzaklığı</li>
            <li>Sorensen-Dice Uzaklığı</li>
          </ul>
 
 <h5>Euclidean Uzaklığı</h5>
 Öklid uzaklığı, çok boyutlu kartezyen veri uzayında iki nokta arasındaki uzaklığın doğrusal bağlantı yöntemi ile ölçülmesidir. 
KNN algoritmasında en çok kullanılan uzaklık ölçüsüdür. Genel olarak denklemi aşağıdaki gibidir:

![euclidean](https://user-images.githubusercontent.com/73036927/200669135-31650477-3cfb-4878-9f1f-5394497e9671.png)

 
 <h5>Manhattan Uzaklığı</h5>
 Manhattan uzaklığı, n boyutlu iki nokta arasındaki farkların mutlak değerlerinin toplamıdır.
 Genel olarak denklemi aşağıdaki gibidir:


 ![manhattan](https://user-images.githubusercontent.com/73036927/200669317-d351af22-b27c-43c0-a7d1-ccbe61bc213b.png)

 <h5>Minkowski Uzaklığı</h5>
 
 Q sayıda bir değişkene bağlı bir uzaklık hesaplamak isteniyorsa Minkowski yöntemi kullanılır.
 Eğer Q değişkeni iki ise o zaman formül q 2 değişkeni için Öklid uzaklığı ile aynı olur. Genel olarak denklemi aşağıdaki gibidir:

![minkowski](https://user-images.githubusercontent.com/73036927/200669446-1658f5cc-158c-4373-8ac9-3adce6d882f1.png)

<h4>Euclidean, Manhattan ve Minkowski UZaklık Hesaplamalarına Örnek</h4>
<h5>Veri Seti</h5>

![mldataset](https://user-images.githubusercontent.com/73036927/200669939-bb4bf1ba-b5ea-4a8c-98b8-f38d924b31cb.png)

![euclideanhesap](https://user-images.githubusercontent.com/73036927/200670027-c1fa239e-d741-4864-a96b-776be85681d7.png)

 
 
 
 <h1></h1>
