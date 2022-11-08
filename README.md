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
 
 <h3>1) Euclidean Uzaklığı</h3>
 Öklid uzaklığı, çok boyutlu kartezyen veri uzayında iki nokta arasındaki uzaklığın doğrusal bağlantı yöntemi ile ölçülmesidir. 
KNN algoritmasında en çok kullanılan uzaklık ölçüsüdür.<br/> Genel olarak denklemi aşağıdaki gibidir:
<br/><br/>

![euclidean](https://user-images.githubusercontent.com/73036927/200669135-31650477-3cfb-4878-9f1f-5394497e9671.png)

 <br/>
 <h3>2) Manhattan Uzaklığı</h3>
 Manhattan uzaklığı, n boyutlu iki nokta arasındaki farkların mutlak değerlerinin toplamıdır. <br/>
 Genel olarak denklemi aşağıdaki gibidir:
 <br/><br/>


 ![manhattan](https://user-images.githubusercontent.com/73036927/200669317-d351af22-b27c-43c0-a7d1-ccbe61bc213b.png)
 
<br/>
 <h3>3) Minkowski Uzaklığı</h3>
 <br/>
 Q sayıda bir değişkene bağlı bir uzaklık hesaplamak isteniyorsa Minkowski yöntemi kullanılır.<br/>
 Eğer Q değişkeni iki ise o zaman formül q 2 değişkeni için Öklid uzaklığı ile aynı olur. Genel olarak denklemi aşağıdaki gibidir:
<br/><br/>

![minkowski](https://user-images.githubusercontent.com/73036927/200669446-1658f5cc-158c-4373-8ac9-3adce6d882f1.png)

<br/>
<h1>Euclidean, Manhattan ve Minkowski UZaklık Hesaplamalarına Örnek</h1><br/>
<h3>Veri Seti</h3>
<br/>

![mldataset](https://user-images.githubusercontent.com/73036927/200669939-bb4bf1ba-b5ea-4a8c-98b8-f38d924b31cb.png)

<br/>
<h3>Gözlemlerin birbirine olan uzaklığının Euclidean Uzaklığı ile hesaplanması</h3>
<br/>

![euclideanhesap](https://user-images.githubusercontent.com/73036927/200670027-c1fa239e-d741-4864-a96b-776be85681d7.png)

<br/>
 <h3>Gözlemlerin Euclidean Uzaklıkları bulunduktan sonra tabloya dökülür.</h3>
 
 ![öklittablo](https://user-images.githubusercontent.com/73036927/200671593-2de85b8d-e3be-4db2-8f84-dc2203184d5f.png)

 <p>
İki gözlem arasındaki fark hangisi en küçükse o iki gözlem birbirine en yakındır. Öklit uzaklık hesabına göre en yakın iki gözlem 3 ve 4 gözlemidir.
</p>

<br/>
<h3>Gözlemlerin birbirine olan uzaklığının Manhattan Uzaklığı ile hesaplanması</h3>
<br/>

![manhattanhesap](https://user-images.githubusercontent.com/73036927/200672688-ee17e6ea-f3b6-49f2-a5cf-1e83c539bbff.png)

<br/>
 <h3>Gözlemlerin Manhattan Uzaklıkları bulunduktan sonra tabloya dökülür.</h3>
 <br/>
 
 ![manhattangözlem](https://user-images.githubusercontent.com/73036927/200672953-a7e377c6-8f77-4a2b-99c4-65739f25ece1.png)

<br/>

Gözlemlerin birbirine olan Manhattan uzaklığına bakacak olursak Gözlem 3 ve 4’ün birbirine olan uzaklığı olan 3 en düşük olduğu için bu iki gözlem birbirine en yakın olanlardır.

<br/>

<h3>Gözlemlerin birbirine olan uzaklığının Minkowski Uzaklığı ile hesaplanması</h3>
<br/>

![minkowskihesap](https://user-images.githubusercontent.com/73036927/200673164-d1702cc5-aa2e-4f2c-a3c1-31f9bd22e8dd.png)

<br/>
 <h3>Gözlemlerin Minkowski Uzaklıkları bulunduktan sonra tabloya dökülür.</h3>
 <br/>

![minkowskitablo](https://user-images.githubusercontent.com/73036927/200673409-70896990-a0d9-4e32-866d-dc233ec3e478.png)

<br/>

Gözlemlerin birbirine olan Minkowski uzaklığına bakacak olursak Gözlem 3 ve 4’ün birbirine olan uzaklığı olan 3 en düşük olduğu için bu iki gözlem birbirine en yakın olanlardır.


<h2>KNN Avantaj ve Dezavantajları</h2>

<h4>Avantajları</h4>
<ul>
<li>Basit algoritma olması sebebiyle yorumlaması, uygulaması kolaydır.</li>
<li>Mesafe metriği istenildiği gibi seçilebilir.</li>
<li>Regresyon ve sınıflandırma için kullanışlıdır.
<ul><li>Regresyon ve sınıflandırma için kullanışlıdır.</li></ul>        
</li>
<li>Eğitim (Training) süresi yoktur.
<ul><li>Tüm iş tahmin sırasında gerçekleşir.</li></ul> 
</li>
<li>Sürekli olarak gelişir.
<ul><li>Eğitim adımı olmadığından, veri kümesine her yeni veri eklediğimizde gelişmiş olur.</li></ul> 
</li>
<li>Veriler üzerinde varsayımda bulunmaz (non-parametric).</li>
<li>Yüksek doğruluk (accuracy) ile sonuca varır.</li>
</ul>

<br/><br/>

<h4>Dezavantajları</h4>
<ul>
        <li>Non-parametric olması sebebiyle her tahminde bütün eğitim verilerinin kullanılması gerekir.</li>
        <li>Tembel (lazy) öğrenme algoritmasıdır.
                <ul><li>80% train – 10% validation – 10% test gibi oransal olarak veri seti kullanımı yapmaz.</li></ul>        
        </li>
        <li>Tüm veri seti eğitim seti olarak kullanılır.</li>
        <li>Bu sebeple öğrenmek yerine ezberler (Overfitting).</li>
        <li>Yanlış etiketlenmiş bir veri sınıf sınırlarını değiştirebilir.</li>
</ul>
<br/>
<h2>Kullanım Alanları</h2>
<ul>
        <li>Genetik</li>
        <li>Veri sıkıştırma</li>
        <li>Siyaset bilimi</li>
        <li>Bankacılık sistemleri
                <ul><li>Kredi notu hesaplama</li></ul>
        </li>
        <li>Tavsiye sistemleri</li>
        <li>Metin madenciliği</li>
        <li>Endüstride sınıflandırma problemleri</li>
</ul>

<br/>
<h2>Kaynakça</h2>
<ul>
        <li>https://www.ahmetcevahircinar.com.tr/2017/04/17/</li>
        <li>https://www.youtube.com/watch?v=ZIqGW8mc7gc&ab_channel=HakanCemGer%C3%A7ek</li>
        <li>https://www.ibm.com/topics/knn</li>
        <li>https://serokell.io/blog/knn-algorithm-in-ml</li>
</ul>


