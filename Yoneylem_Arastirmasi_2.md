||
| :- |
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|

|**2 YÖNEYLEM ARAŞTIRMASI**|
| - |
|**Temel Kavramlar**|
|<p>2 </p><p>1  3  5 </p><p>4 </p><p>**Şekil 4.1** </p><p>- *Grafik*: Belirli sayıda nokta ve bu noktaları birbirine birleştiren çizgi ve/veya eğrilerden oluşan kümeye grafik denir. </p><p>- *Düğüm*: Grafikte bulunan noktaların her birine düğüm denir. Düğümler, içlerine kendilerini tanımlayan sembollerin (harf veya rakam) yazıldığı küçük dairelerle gösterilirler. </p><p>- *Dal*: Herhangi iki düğümü birbirine birleştiren çizgi veya eğriye dal denir. Bir dal okla gösterildi- ğinde yönlendirilmiş olur. Okla birleştirilen iki düğüm i ve j olmak üzere, bunları birleştiren dal (i, j) ile gösterilir. Bu sembolde i, (i, j) dalının başlangıç j ise bitiş düğümüdür. Böyle bir dal üzerinde bir akış söz konusuysa, akışın  yönü i’den j’ye olmak  üzere tektir. Yönlendirilmemiş  bir (i, j) dalı, biri (i, j) diğeri (j, i) olmak üzere yönlendirilmiş iki dal yerine geçer. </p><p>- *Ağ*: Grafiğin dalları üzerinde bir akış olması durumunda grafik, akış ağı veya kısaca ağ (serim, network, şebeke) ismini alır. </p><p>- *Yol*: Başlangıç düğümü, kendisinden önce gelen dalın bitiş düğümü ile aynı olan dallar dizisine yol denir.</p><p>- *Zincir*: Kendisinden önce gelen dalla tek bir ortak noktası olan dallar dizisine zincir denir. </p><p>- *Çevrim*: Başlangıç düğümü ile bitiş düğümü aynı olan yola çevrim denir.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**3 YÖNEYLEM ARAŞTIRMASI**|
|**En Yüksek Akış Problemleri**|
|<p>Bu bölümde, belirli bir zaman aralığında birbirlerine </p><p>doğrudan değil ara noktalarla bağlı olan iki nokta arasında taşınan malzeme veya akış miktarının en büyüklenmesi problemi üzerinde durulacaktır. Örneğin en yüksek trafik akışının sağlanmasına ilişkin problemlerin çözümünde EYA algoritması kullanılabilir.</p><p>İlk bakışta ulaştırma problemi gibi görünen bu tip </p><p>problemlerin ulaştırma problemlerinden en önemli farkı, kaynak (başlangıç) ile varış (bitiş) arasındaki bağlantının doğrudan değil ara noktalar aracılığı ile sağlanmasıdır.  </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**4 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>1 </p><p>f  2  v  f </p><p>k </p><p>- Şekil 4.6’daki akış ağı, ürünün k ile gösterilen kaynaktan v ile gösterilen bitişe hangi dallar üzerinden, hangi yöne doğru gönderilebileceğini göstermektedir.</p><p>- Ara noktalar 1, 2, 3 ile işaretlenmişlerdir. Kaynak ve bitiş dahil ağdaki beş düğüm birbirlerine  (k, 1),  (k, 2), (k, 3), (1, 2), (1, v), (2, v), (3, 2) ve (3, v) olmak üzere 8 dalla bağlıdır. </p><p>- Yanıtlanmak istenen k’dan v’ye gönderilmek istenen malzemenin, hangi dallar üzerinden hangi miktarlarda taşınması durumunda, v’ye aktarılan kısmın en büyük olacağıdır.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**5 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- Her dalın kij ile gösterilen belirli bir taşıma kapasitesi vardır. (i, j) dalı üzerinden taşınabilecek en yüksek miktarı ifade eden kij aynı zamanda, akışın i’den j’ye doğru gerçekleştiğini göstermektedir.</p><p>- Taşınan miktarın en büyük olmasının amaçlandığı bu tip problemlerde, en yüksek akış miktarı f ile gösterilir.</p><p>- Diğer taraftan, kapasitesi kij ile gösterilen (i, j) dalı üzerinden taşınan miktar fij ile açıklanır. Bu sembol de kij’ye benzer şekilde akışın i’den j’ye doğru olduğunu göstermektedir.</p><p>- En yüksek akış problemleri doğrusal programlama problemi olarak da formüle edilip çözülebilir. Bunun için öncelikle ağı oluşturan dalların taşıma kapasitelerinin belirlenmesi gerekir.</p><p>1 </p><p>(f1v, k1v) </p><p>(fk1, kk1)  (f , k ) </p><p>12	 12</p><p>f  k  (fk2, kk2)  2  (f2v, k2v)  v  f </p><p>(f , k )  (f32, k32) </p><p>k3 k3 (f3v, k3v) </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**6 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- Açıklamalar doğrultusunda çizilen ağ aşağıdaki şekilde gösterilmiştir.</p><p>- Şeklin ortaya koyduğu gibi ürün akışı kaynaktan 1, 2 ve 3 nolu düğümlere doğrudur. Buna göre,</p><p>fk1 + fk2 + fk3 = f yazılabilir.</p><p>- Kaynaktan varışa olan akışlar toplamının kaynaktaki akış miktarına eşitliğini gösteren bu denkleme "denge denklemi" denir. </p><p>Amaç  fonksiyonunun  Z  =  f  şeklinde  formüllenmesiyle,  yukarıdaki  ağın </p><p>- enb</p><p>doğrusal programlama modeli aşağıdaki gibi formüle edilebilir. </p><p>Zenb = f     "Amaç fonksiyonu " </p><p>f + f + f = f </p><p>k1 k2 k3</p><p>f + f          = f</p><p>12	 1v k1</p><p>f + f + f = f</p><p>12	 k2 32 2v</p><p>f + f          = f</p><p>32	 3v k3</p><p>f1v + f2v + f3v = f </p><p>1 </p><p>(f1v, k1v) </p><p>(fk1, kk1)  (f , k ) </p><p>12	 12</p><p>Kısıtlayıcılar </p><p>f  k  (fk2, kk2)  2  (f2v, k2v)  v  f </p><p>Negatif olmama koşulları  (fk3, kk3)  (f32, k32)  (f , k ) </p><p>3v 3v 0 £ fk1  £ kk1, 0 £ fk2 £ kk2, 0 £ fk3 £ kk3, 0 £ f12 £ k12</p><p>0 £ f32 £ k32, 0 £ f1v £ k1v, 0 £ f2v £ k2v, 0 £ f3v £ k3v</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**7 YÖNEYLEM ARAŞTIRMASI**|
|**En Yüksek Akış Algoritması**|
|<p>- En yüksek akış algoritmasının esası, kaynaktan bitişe pozitif akışın söz konusu olduğu bir yol bulmaktır. Böyle bir yol "akış artırıcı yol" olarak isimlendirilir. Akış artırıcı yol bulma çabalarının sonuçsuz kalması durumunda en yüksek akış bulunmuş olur. </p><p>- *Rota Etiketleme İşlemi*: Kaynaktan bitişe akış artırıcı yol bulmada kullanılan etiketleme işlemi kaynağın etiketlenmesiyle başlar. k’dan j’ye pozitif akış söz konusu ise j düğümü etiketlenir.</p><p>- Genel olarak, aşağıdaki koşullardan birinin sağlanması durumunda j etiketlenir.</p><p>- i ve j düğümlerini birleştiren dal ileri doğrudur ve (i, j) üzerindeki akış miktarı dalın akış kapasitesinden küçüktür (f < k ).</p><p>ij  ij</p><p>- i ve j düğümlerini birleştiren dal (j, i) geriye doğrudur ve (j, i) üzerindeki akış miktarı sıfırdan büyüktür (fji > 0).</p><p>- Etiketleme işlemi bitiş noktası etiketleninceye değin sürdürülür. Bitiş etiketlendiğinde akışı artırıcı bir yol belirlenmiş olur. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**8 YÖNEYLEM ARAŞTIRMASI**|
||
|- En yüksek akış algoritması, kapasite kısıtları ile birlikte düğümlerdeki akışın korunumunu da sağlayan uygun bir akışla başlar. Başlangıç akış planı (doğrusal programlamanın başlangıç çözümüne benzer) olarak isimlendirilen bu plan, akış miktarının 0 olduğu duruma karşılık gelir. Bu akışın geliştirilebilmesi için öncelikle kaynak (başlangıç düğümü) etiketlenir. Etiketlenen düğüm \* ile işaretlenir. Kaynağın etiketlenmesinden sonra yukarıda açıklanan rota etiketleme işlemiyle başka bir düğüm etiketlenir. Bitiş etiketlendiğinde pozitif akışın söz konusu olduğu akış artırıcı bir yol belirlenmiş olur. Belirlenen bu yol üzerindeki düğümlerin etiketleri yardımıyla yol üzerinden aktarılacak en yüksek akış (d) hesaplanır. d’nin hesaplanmasından sonra yolun ileri dallarındaki akışlar d kadar artırılırken, geriye doğru dallardaki akışlar d kadar azaltılır. Bu işlemler yeni akış artırıcı yolların bulunması için tekrarlanır. |
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**9 YÖNEYLEM ARAŞTIRMASI**|
|**Örnek 4.1**|
|<p>**Örnek 4.1**: Dallarının akış kapasiteleri (fij) oklar üzerinde gösterildiği gibi olan ağda  k’dan  v’ye  taşınacak  en  yüksek  ürün  miktarını  ve  taşıma  planını belirleyiniz. Problemin akış ağı  Şekil 4.11’de gösterilmiştir. </p><p>1 </p><p>20  27 </p><p>5 </p><p>f  k  30  2  15  v  f </p><p>10  14  19 </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**10 YÖNEYLEM ARAŞTIRMASI**|
|**Çözüm 4.1**|
|<p>**Çözüm 4.1**: Problemin çözümüne herhangi bir akışın olmadığı durumla başlayalım. </p><p>Başlangıç akış planını yansıtan bu durum için aşağıdaki gibi bir eşitlik yazılabilir.</p><p>f = f =  f =  f = f = f = f = f = 0</p><p>k1 k2 k3 12 32 1v 2v 3v</p><p>Bu durum orijinal ağ üzerinde aşağıdaki gibi gösterilir. (i, j) dalları üzerindeki </p><p>sayılar (fij, kij)’leri göstermektedir.</p><p>1 </p><p>(0, 27) </p><p>(0, 20)  (0, 5) </p><p>f = 0  k  (0, 30)  2  (0, 15)  v  f = 0 </p><p>(0, 14) </p><p>(0, 10)  (0, 19) </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
**11 YÖNEYLEM ARAŞTIRMASI![](hb5een0m.001.png)**

**Çözüm 4.1**

1 

(20, 20)  (0, 5)  (20, 27) 

f = 45  k**\***   (15, 30)  2  **\***  (15, 15)  f = 45 

v 

(10, 10)  (0, 14) 

(10, 19) 

**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**

|**12 YÖNEYLEM ARAŞTIRMASI**|
| - |
|**Yönlendirilmemiş Dallar**|
|<p>*Yönlendirilmemiş Dalların Olması Durumu*: En yüksek akış algoritması için ağın </p><p>yönlendirilmiş olması gerekmekle birlikte, ağın yönlendirilmemiş olması en yüksek  akışın  belirlenmesini  engellemez.  Söz  konusu  algoritmanın yönlendirilmemiş bir ya da birkaç dalın bulunduğu ağlarda uygulanabilmesi için  öncelikle  yönlendirilmemiş  dalların  bulunduğu  orijinal  ağın yönlendirilmesi, daha sonra en yüksek akış algoritmasının orijinaline eşdeğer olan bu ağa uygulanmasına geçilir. i ve j düğümlerini birleştiren K kapasiteli yönlendirilmemiş bir dal aşağıdaki gibi yorumlanabilir. </p><p>fij £ K </p><p> </p><p>fji £ K </p><p>(f ) (f ) = 0 </p><p>ij ji</p><p>Yukarıdaki eşitsizlikler (i, j) üzerinden en yüksek K birimlik akışın hem i’den j’ye hem de j’den i’ye doğru olabileceğini göstermektedir. (f )(f ) = 0 eşitliğiyle</p><p>ij ji</p><p>akışın tek yönde olması sağlanmaktadır. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**13 YÖNEYLEM ARAŞTIRMASI**|
|**Örnek 4.2**|
|<p>**Örnek 4.2**: Aşağıdaki gibi bir yol ağını ele alalım. Dallar üzerindeki </p><p>sayılar trafik akış kapasitelerini göstermektedir. Problem, en yüksek trafik akışını sağlayabilmek için henüz yönlendirilmemiş dallar üzerine tek yön işaretinin hangi istikamette konulacağının belirlenmesidir.</p><p>30  </p><p>1  3 </p><p>50 30 </p><p>55 </p><p>f </p><p>f </p><p>20 </p><p>30  v </p><p>k  25 </p><p>30 2  4 </p><p>75 </p><p>**Şekil  4.23** </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**14 YÖNEYLEM ARAŞTIRMASI**|
|**Çözüm 4.2**|
|<p>**Çözüm  4.2**:  Öncelikle  yönlendirilmemiş  her  bir  dalın  ters  yönlü  ve  eşit kapasiteli  iki  dalla  değiştirilmesi  gerekir.  Bu  düzenlemeyle,  Şekil  4.24’de gösterilen yönlendirilmiş ağ elde edilir. </p><p>30  </p><p>1  3 </p><p>50 30 </p><p>55 </p><p>f </p><p>30  v  f </p><p>` `25  20 </p><p>k </p><p>30 </p><p>2  4 75 </p><p>**Şekil  4.24** </p><p>En yüksek akış algoritmasının, orijinaline eşdeğer olan bu ağ üzerinde uy- gulanmasıyla, k’dan v’ye en yüksek akış miktarı ve en yüksek akışı sağlayan rota belirlenir. </p><p>En  iyi  çözümün  bulunmasından  sonra  her  iki  yönde  akışın  söz  konusu olduğu dallar belirlenir ve  aşağıdaki inceleme gerçekleştirilir. </p><p>i ve j düğümlerini birleştiren yönlendirilmemiş bir dal üzerinde, </p><p>f > f ise, (i, j) dalındaki akış (f - f ) olur, yani yönlendirilmemiş (i, j) dalı i’den </p><p>ij ji ij ji</p><p>j’ye doğru yönlendirilir. </p><p>fji > fij ise, (j, i) dalındaki akış (fji - fij ) olur, yani yönlendirilmemiş (i, j) dalı j’den i’ye doğru yönlendirilir. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
**15 YÖNEYLEM ARAŞTIRMASI![](hb5een0m.002.png)**

**Çözüm 4.2**

(30, 3 0) 

1  3 

(50, 50)  (50, 55) 

f = 80  k  (20, 25)  (0, 20)  (20, 30)  v  f = 80 (30, 30)  (30, 30) 

2  4 

(50, 75) 

**Şekil  4.25** 

**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**

|**16 YÖNEYLEM ARAŞTIRMASI**|
| - |
||
|<p>*Çok Kaynak-Çok Bitiş Olması*: Ağ üzerinde birden fazla kaynak ve/veya birden fazla bitiş noktası bulunduğunu düşünelim. Bu durumda en yüksek akışın belirlenebilmesi için hayali bir kaynak ile hayali bir bitiş noktasının yaratılması zorunludur. Yaratılan hayali kaynak gerçek kaynaklara, gerçek bitiş noktaları hayali bitiş noktasına birer dalla bağlanır. Ağa eklenen hayali dalların tümü ileriye doğrudur. Hayali dalların akış kapasitelerinin belirlenmesinden sonra problem en yüksek akış problemine dönüşmüş olur. </p><p>•</p><p>- **Örnek 4.3:**</p><p>2  20  5  d5 40  30 </p><p>3  6 </p><p>4  7 </p><p>15 </p><p>10 10 </p><p>d8 </p><p>1  50  20  8 </p><p>s1 </p><p>30 </p><p>20  25  60 s4  35 </p><p>**Şekil 4.26** </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**17 YÖNEYLEM ARAŞTIRMASI**|
|**Çözüm 4.3**|
|<p>20  **d5  f** </p><p>2  5 15 </p><p>3  6 25 </p><p>4  7 </p><p>v </p><p>8 </p><p>40 </p><p>**d 8**</p><p>30 </p><p>10 </p><p>50  10  20 </p><p>1 k </p><p>**s**</p><p>30 </p><p>**1**</p><p>20 </p><p>60 </p><p>**f** </p><p>**s** </p><p>**4** 35 </p><p>**Şekil  4.27** </p><p>Görüldüğü gibi k’yı 1 nolu düğüme bağlayan dalın kapasitesi s1’e, 4 nolu düğüme bağlayan dalın kapasitesi ise s4’e eşittir. Gerçek bitiş noktalarını hayali bitiş noktasına bağlayan dalların taşıma kapasiteleri ise çıkış nokta- larının istem miktarlarıyla bağlantılı olarak sırasıyla d ve d ’dir.</p><p>5 8</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**18 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Bu düzenlemenin ardından hayali kaynaktan bitiş noktasına en yüksek akışın sağlanmasına geçilebilir.  s = 40, s = 30, d = 35, d = 35 olarak verilmiş olsun. </p><p>1 4 5 8</p><p>Bu durumda en iyi çözüm Şekil 4.28’deki gibi elde edilecektir. </p><p>(20, 20)  (35, 35)  **f = 70** </p><p>5 6 7 </p><p>2 3 </p><p>4 </p><p>v </p><p>(10, 10) </p><p>(10, 10) </p><p>(30, 40) </p><p>(35, 35) </p><p>(5, 15) </p><p>(10, 30) (0, 20)</p><p>(5, 20)  8 </p><p>1  (10, 50) k  (30, 30) </p><p>(0, 30) (30, 35) </p><p>(40, 40) **f = 70** </p><p>(0, 25) </p><p>(30, 60) </p><p>**Şekil 4.28**  </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**19 YÖNEYLEM ARAŞTIRMASI**|
|**En Kısa Yol Problemleri**|
|<p>- Başlangıç ve bitiş düğümleri arasındaki en kısa yolun belirlenmesi problemi, en kısa yol problemi olarak bilinir. </p><p>- Ağ problemlerinin çoğu doğrusal programlama problemi olarak değerlendirilerek simpleks yöntemle çözülebilir. Bu durum en kısa yol problemleri için de geçerlidir. Bir en kısa yol problemini doğrusal programlama olarak inceleyebilmek için dallar üzerindeki akışların 1 birime, i’den j ’ye malzeme taşıma maliyetinin ise (i, j) dalının uzunluğuna eşit olduğu düşünülür. </p><p>- Çözüm İçin Kullanılan Yöntemler:</p><p>- Simpleks Yöntemi</p><p>- Listeleme Yöntemi</p><p>- Dijkstra Algoritması</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**20 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- ***Dijkstra Algoritması**:* Dijkstra Algoritması, n düğümlü ağ kapsamındaki tüm dalların negatif olmayan ve bilinen uzunluklara (d ) sahip olduğu varsayımına </p><p>ij</p><p>dayanır. dij,, (i, j) dalının uzunluğu, i’den j’ye gitmenin maliyeti veya (i, j) dalını katetme zamanı olabilir. i ve j düğümleri birbirlerine doğrudan, yani tek bir dalla bağlı değillerse d = ¥kabul edilir. d ¹d olabilir. Ayrıca, bir düğümün </p><p>ij ij ji</p><p>kendine uzaklığı sıfır olduğundan, dii = 0’dır. Bu varsayımlar altında, düğümlerin önce geçici, sonra kalıcı olarak etiketlenmesi esasına dayanan Dijkstra algoritması, en kısa yol belirleninceye kadar aşağıdaki adımların tekrarlanmasını gerektirir.</p><p>- Ön adım: Başlangıç düğümüne sıfır (d = 0) kalıcı etiketi verilir. Sıfır ile kalıcı olarak etiketlenen başlangıç düğümü dışınd11 aki bütün düğümlere, birer geçici </p><p>etiket verilir. Geçici etiketi hesaplanacak düğüm başlangıç düğümüne tek bir dalla bağlı ise geçici etiketin değeri o dalın uzunluğuna, değilse +¥’a eşittir. Geçici etiketlerin belirlenmesinden sonra en küçük olan araştırılır. Araştırma sonucu belirlenen en küçük değer ait olduğu düğümün kalıcı etiketi olur. En küçük değerli geçici etiket sayısı birden çok ise seçim, düğümlerden yalnızca birinin seçilmesi kaydıyla, rasgele yapılır. Kısaca, her seferinde yalnızca bir düğüm kalıcı olarak etiketlenir.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**21 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Birinci Adım: Kalıcı etiketi en yeni olan düğüm belirlenir. Bu düğüm K olsun. Ön adımdaki başlangıç düğümüne karşılık gelen bu düğüme bağlı olarak tüm geçici etiketlerin yeni değerleri aşağıdaki gibi hesaplanır. </p><p>Enk íìi düğümünün halihazırdaki geçici etiketi                   </p><p>îK düğümünün kalıcı etiketi +(j, K) dalının uzunluğu</p><p>İkinci adım: Birinci adımda hesaplanan geçici etiketlerden en küçük olanı ait olduğu düğümün kalıcı etiketi olur ve \* ile işaretlenir. Önceden olduğu gibi, en küçük değerli etiket birden fazla olduğunda düğüm seçimi, her seferinde yalnızca bir düğüm olmak üzere,  rasgele yapılır. Son düğüm kalıcı olarak etiketlendiğinde en kısa yol belirlenmiş olur. Son düğümün kalıcı etiketinin değeri en kısa yolun uzunluğuna eşittir. </p><p>En kısa yolu oluşturan dalların belirlenmesi için son düğümden başlanarak geriye doğru hareket edilir ve düğümlerin kalıcı etiketleri arasındaki farklar incelenir. Etiketler arasındaki fark iki düğüm arasındaki dalın uzunluğuna eşitse ilgili dal en kısa yol üzerinde, aksi halde değildir.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**22 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>**Örnek 4.3**: İzmir’den Ankara’ya gitmek isteyen bir kişi gidebileceği yolları araştırmış ve iki şehri birbirine bağlayan yolları ve bunların uzaklıklarını Şekil 4.29’daki  gibi  belirlemiştir.  Sürücünün  amacı  İzmir’den  Ankara’ya  en  kısa yoldan gitmektir. İki şehir arasındaki en kısa yolu bulunuz. </p><p>2  3  4  2  6 </p><p>5  2 </p><p>1 </p><p>6  7 İzmir  4 </p><p>7  Ankara </p><p>3  5  4 </p><p>5 </p><p>**Şekil  4.29** </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**23 YÖNEYLEM ARAŞTIRMASI**|
|**Çözüm 4.3**|
|<p>**Çözüm  4.3**:  Ön  adım:  Başlangıç  düğümünün  sıfırla  kalıcı  olarak  etiketlen- mesinden sonra diğer düğümlerin etiketlenmesine geçilir. </p><p>Şekil 4.29’dan görüldüğü gibi başlangıç düğümüne doğrudan bağlı iki düğüm (2 ve 3) vardır. Bu düğümlerin başlangıç düğümüne uzaklıkları sırasıyla 5 ve 7 olduğundan bunların geçici etiketleri sırasıyla, 5 ve 7 olarak belirlenir. Bu iki düğümün  dışındaki  düğümlerin  hepsi  başlangıç  düğümüne  dolaylı  olarak bağlı olduklarından etiketleri +¥’a eşittir. Bu yolla belirlenen etiket değerleri aşağıda, ait oldukları düğüm numaraları altında gösterilmiştir.  </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5  7  ¥  ¥  ¥  ¥] </p><p>Geçici  etiketlerden  en  küçük  (5)  olanı  2  nolu  düğüme  ait  olduğundan,  bu düğüm  5  ile  kalıcı  olarak  etiketlenir.  Böylece  etiketler  aşağıdaki  gibi belirlenmiş ve ön adım tamamlanmış olur. </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7  ¥  ¥  ¥   ¥] </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**24 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Birinci adım: En yeni kalıcı etiket 2 nolu düğüme aittir. Bu düğüme doğrudan bağlı  olan  4  ve  5  nolu  düğümlerin  yeni  geçici  etiketlerinin  hesaplanması gerekir. Yeni etiket değerleri aşağıdaki gibi hesaplanmıştır. </p><p>Dördüncü düğümün geçici etiketi: Enk{¥, 5 + 3} =  8 Beşinci düğümün geçici etiketi    : Enk{¥, 5 + 6} = 11 </p><p>Hesaplanan değerlerin dikkate alınmasıyal düğüm etiketlerinin yeni değerleri aşağıdaki gibi olur. </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7  8  11  ¥  ¥] </p><p>İkinci adım: Birinci adımda belirlenen geçici etiketlerden en küçük olanın 7 olduğu ve bunun üçüncü düğüme ait olduğu görülebilir. Buna göre üçüncü düğüm etiketinin 7 olarak kalıcı kılınmasıyla düğüm etiketleri aşağıdaki gibi belirlenmiş olacaktır. </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7\*  8  11  ¥  ¥] </p><p>Henüz tüm etiketler kalıcı olmadığından tekrar birinci adıma dönülür. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**25 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Birinci adım: Kalıcı etiketi en yeni olan üçüncü düğüme doğrudan bağlı 4 ve 5 nolu düğümlerin yeni geçici etiketleri, </p><p>Dördüncü düğümün geçici etiketi: Enk{ 8,  7 + 4} =  8  Beşinci düğümün geçici  etiketi     : Enk{11, 7 + 5} = 11 </p><p>olarak hesaplanacak böylece düğüm etiketleri, aşağıdaki gibi belirlenecektir. </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7\*  8  11  ¥  ¥] </p><p>İkinci adım: Geçici etiketlerden en küçüğü dördüncü düğüme ait olduğundan, anılan düğüm 8 ile kalıcı biçimde etiketlenir. Buna göre, </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7\*  8\*  11  ¥  ¥] </p><p>olur. Henüz tüm etiketler kalıcı olmadığından tekrar birinci adıma dönelim.  </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**26 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Birinci adım: En yeni kalıcı etiket 4 nolu düğüme aittir. Bu düğüme doğrudan bağlı tek düğüm olan 6 nolu düğümün yeni geçici etiketinin hesaplanması gerekir. Bu işlem aşağıda gösterilmiştir. </p><p>Altıncı düğümün geçici etiketi: Enk{¥, 8 + 2} = 10 </p><p>Bu sonucun kullanılmasıyla belirlenen düğüm etiketleri aşağıda gösterilmiştir. </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7\*  8\*  11  10  ¥] </p><p>İkinci adım: Geçici etiketlerden en küçüğü altıncı düğüme ait olduğundan anılan düğümün kalıcı etiketi 10 olur. Buna göre etiketler, </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7\*  8\*  11  10\*  ¥] </p><p>olur. Etiketleme işlemi henüz tamamlanmadığından birinci adım tekrarlanır. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**27 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Birinci adım: Altıncı düğüme bağlı tek düğüm yedinci düğüm olduğundan anılan düğümün geçici etiketi, </p><p>Yedinci düğümün geçici etiketi: Enk{¥, 10 + 2} = 12 </p><p>olarak hesaplanır ve düğüm etiketleri aşağıdaki gibi belirlenmiş olur.  </p><p>Düğüm No:  [1  2  3  4  5   6  7] Etiket No  :  [0\*  5\*  7\*  8\*  11  10\*  12] </p><p>İkinci adım:  En küçük değerli (11) geçici etiket beşinci düğüme aittir. Bu nedenle 11, beşinci düğümün kalıcı etiketi olur ve sonuçta düğüm etiketleri aşağıdaki gibi belirlenmiş olur. </p><p>Düğüm No:  [1  2  3  4  5  6  7] Etiket No  :  [0\*  5\*  7\*  8\*  11\*  10\*  12] </p><p>Bu  noktada  etiketi  geçici  olan  bir  düğüm  bulunduğundan  birinci  adıma dönülür. </p><p>Birinci adım: Kalıcı etiketi en yeni olan beşinci düğüme doğrudan bağlı tek düğüm olan yedinci düğümün geçici etiketinin yeni değeri, </p><p>Yedinci düğümün geçici etiketi: Enk{12, 11 + 4} = 12 olarak hesaplanmıştır.  </p><p>Sonuçta etiketleme işlemi aşağıdaki gibi tamamlanmıştır.  </p><p>Düğüm No :  [1  2  3  4  5  6  7  ] Etiket No    :  [0\*  5\*  7\*  8\*  11\*  10\*  12\*] </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**28 YÖNEYLEM ARAŞTIRMASI**|
||
|Etiketlerin hepsi kalıcı olduğundan en kısa yol bulunmuştur. Şimdi de toplam uzunluğu 12 birim olan en kısa yol üzerindeki dalları belirleyelim. Bunun için son düğümden başlayarak geriye doğru düğüm düğüm gidelim. 7 ve 6 nolu düğümlerin  kalıcı  etiketleri  arasındaki  fark  (2)  anılan  düğümleri  birbirine birleştiren  dalın  uzunluğuna  eşit  olduğundan  (6,  7)  dalı  en  kısa  yol üzerindedir.  6  nolu  düğümden  5  nolu  düğüme  gidilemez.  6  ve  4  nolu düğümlerin  kalıcı  etiketleri  arasındaki  fark  (2),  (4,  6)’nın  uzunluğuna  eşit olduğundan,  bu  dal  en  kısa  yol  üzerindedir.  (4,  3)  dalının  uzunluğu  bu düğümlerin etiketleri arasındaki farka eşit olmadığından, (4, 3) dalı en kısa yol üzerinde değildir. 4 ve 2 nolu düğümlerin kalıcı etiketleri arasındaki fark (2, 4)’ün uzunluğuna eşit olduğundan bu dal en kısa yol üzerindedir. Son olarak (2, 1)’in uzunluğu bu dalı tanımlayan düğümlerin etiketleri arasındaki farka eşittir. Dolayısıyla bu dal en kısa yol üzerindedir. Buna göre İzmir’den yola çıkan sürücü sırasıyla, 2, 4, 6 nolu düğümlere uğrayarak İzmir’den Ankara’ya en kısa yoldan ulaşmış olur. |
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**29 YÖNEYLEM ARAŞTIRMASI**|
||
|Aracın Yaşı |Bakım Masrafı |Satış  Fiyatı |
|0 |2 |- |
|1 |3 |10 |
|2 |5 |9 |
|3 |8 |5 |
|4 |12 |3 |
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**30 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>**Çözüm 4.4**: Önce, aracın satın alındığı yıl başlangıç, planlama döneminin sonu bitiş olmak üzere 6 düğümlü ağı oluşturalım. Ara noktalar (j = 1, 2, 3, 4, 5) araç yenilemenin mümkün olduğu yılın başına karşılık gelmektedir.  </p><p>44 </p><p>30 </p><p>30 </p><p>20 </p><p>20 </p><p>1  7  2  7  3  7  4  7  5  7  6 </p><p>11  11 </p><p>11  11 </p><p>20 </p><p>**Şekil 4.30** </p><p>i < j için (i, j) dalı, i yılı başında satın alınan aracın j yılı başında satılarak yerine yenisinin alınmasına karşılık gelir. (i, j) dalının uzunluğu (d ) ise, i yılı başında </p><p>ij</p><p>satın alınan aracın j yılı başında satılmasına kadar geçen süre içinde bakım ve onarımını yapmak, j yılının başında aracı satmak ve yerine yenisini almanın net maliyetine eşittir. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**31 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Buna göre i ³ j için dij = ¥ ve i < j için, </p><p>dij = (i, i + 1, ..., j - 1 yıllarında araç bakım-onarım harcaması) + (i yılı başında araç satın          alma maliyeti) - (j yılı başında eski araç satışından elde edilen gelir) </p><p>olarak tanımlandığında, her bir (i, j) dalının uzunluğu (net maliyet olarak) aşağıdaki gibi hesaplanır. </p><p>d = d = d = d = d = 15 + 2 - 10 = 7 </p><p>12	 23 34 45 56</p><p>d13 = d24 = d35 = d46 = 15 + 2 + 3 - 9 = 11 d14 = d25 = d36 = 15 + 2 + 3 + 5 - 5 = 20 </p><p>d = d = 15 + 2 + 3 + 5 + 8 - 3 = 30 </p><p>15	 26</p><p>d16 = 15 + 2 + 3 + 5 + 8 + 12 - 1 = 44 </p><p>Hesaplama sonuçları Şekil 4.30’da gösterilmiştir. Artık Dijkstra Algoritmasını uygulayabiliriz.  Algoritmanın  uygulanmasıyla  elde  edilen  hesaplama sonuçları aşağıda arka arkaya verilmiştir.  </p><p>*Ön adım*: </p><p>Düğüm No:  [1  2  3  4  5   6] Etiket        :  [0\*  7  11  20  30  44] Düğüm No:  [1  2  3  4  5   6] Etiket        :  [0\*  7\*  11  20  30  44] </p><p>Ön adım </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|

||||**32 YÖNEYLEM ARAŞTIRMASI**|
| :- | :- | :- | - |
|||||
|||||
|<p>*Birinci adım*: Düğüm No:  [1 Etiket        :  [0\* *İkinci adım*:   Düğüm No:  [1 Etiket        :  [0\* </p><p>2 7\* </p><p>2 7\* </p>|<p>3 11 </p><p>3 11\* </p>|<p>4 18 </p><p>4 18 </p>|<p>5   6] 27  37] </p><p>Birinci tekrar </p><p>5    6] 27  37] </p>|
|<p>*Birinci adım*: Düğüm No:  [1 Etiket        :  [0\* *İkinci adım*:   Düğüm No:  [1 Etiket        :  [0\* </p><p>2 7\* </p><p>2 7\* </p>|<p>3 11\* </p><p>3 11\* </p>|<p>4 18 </p><p>4 18\* </p>|<p>5   6] 22  31] </p><p>İkinci tekrar </p><p>5    6] 22  31] </p>|
|<p>*Birinci adım*: Düğüm No:  [1 Etiket        :  [0\* *İkinci adım*:   Düğüm No:  [1 Etiket        :  [0\* </p><p>2 7\* </p><p>2 7\* </p>|<p>3 11\* </p><p>3 11\* </p>|<p>4 18\* </p><p>4 18\* </p>|<p>5   6] 22  29] </p><p>Üçüncü tekrar </p><p>5    6] 22\*  29] </p>|
|<p>*Birinci adım*: Düğüm No:  [1 Etiket        :  [0\* *İkinci adım*: Düğüm No:  [1 Etiket        :  [0\* </p><p>2 7\* </p><p>2 7\* </p>|<p>3 11\* </p><p>3 11\* </p>|<p>4 18\* </p><p>4 18\* </p>|<p>5   6] 22\*  29] </p><p>Dördüncü tekrar </p><p>5    6] 22\*  29\*] </p>|
|**İstanbul Ticaret Üniversitesi**|||**Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|

|**33 YÖNEYLEM ARAŞTIRMASI**|
| - |
||
|<p>Etiketlerin hepsi kalıcı olduğundan en kısa yol daha doğrusu, en düşük maliyetli </p><p>araç yenileme planı belirlenmiş olur. En düşük net maliyet 29 TL’dir. Şimdi de işletmenin hangi yıllarda araç yenileyeceğini belirleyelim. 5 ve 6 nolu düğümlerin etiketleri arasındaki fark (5, 6) dalının uzunluğuna eşit olduğundan bu dal en kısa yol üzerindedir. 5 ve 4 nolu düğümlerin kalıcı etiketleri arasındaki fark, bu iki düğümü birleştiren dalın uzunluğuna eşit olmadığından, bu dal en kısa yol üzerinde değildir. 5 ve 3 nolu düğümlerin etiketleri arasındaki fark (3, 5) dalının uzunluğuna eşit olduğundan, bu dal en kısa yol üzerindedir. 3 ve 2 nolu düğümlerin etiketleri arasındaki fark bu düğümleri birleştiren dalın uzunluğuna eşit değildir. Dolayısıyla, (2, 3) dalı en kısa yol üzerinde değildir. 3 ve 1 nolu düğümlerin etiketleri arasındaki fark (1, 3) dalının uzunluğuna eşit olduğundan, bu dal da en kısa yol üzerindedir. Buna göre çözüm, (1, 3), (3, 5), (5, 6) dallar dizisi olarak belirlenmiş olur. En kısa yolu oluşturan dalları inceleyelim. Dalların ortaya koyduğu gibi, planlama dönemi başında satın alınan araç 2 yıl kullanıldıktan sonra satılarak yerine yenisi alınacaktır. Yeni araç iki yıl kullanıldıktan sonra satılacak, yerine yenisi alınacak ve yeni araç 1 yıl kullanıldıktan sonra satılacak ve planlama dönemi tamamlanacaktır.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**34 YÖNEYLEM ARAŞTIRMASI**|
|**En Küçük Yayılmalı Ağaç Problemleri** |
|<p>En küçük yayılmalı ağaç problemleri, en kısa yol problemlerinin özel bir biçimidir. </p><p>En küçük yayılmalı ağaç problemlerinde dal uzunluklarının  bilindiği  varsayılır. İki problem arasındaki en önemli fark en küçük yayılmalı ağaç probleminde düğümlerin tümünü, en kısa yol probleminde düğümlerin bazılarını birleştiren dallar dizisinin bulunmasıdır. Ayrıca en kısa yol probleminde ağın yönlendirilmiş olması şart iken, yayılmalı ağaç probleminde ağın yönlendiril- memiş olması gerekir. Uygulamada çok sık karşılaşılan bu tür problemlere örnek olması bakımından belirli bir yerdeki bilgisayarlar topluluğunun birbirlerine bağlanmak istendiklerini düşünelim. Burada, bilgisayarların her biri bir düğüm ve bunları birbirlerine bağlayan yeraltı kabloları dal olarak ele alınabilir. Bilgisayarlar arasındaki bağlantıyı sağlayan yeraltı kablolarının toplam uzunluğunun en kısa olması amaçlanabilir. Bu amaca ulaşmak için belirlenen dallar topluluğunun herhangi bir çevrim kapsamaması gerekir.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**35 YÖNEYLEM ARAŞTIRMASI**|
||
||
|2 |3 |4 |
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**36 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>***En  Küçük  Yayılmalı  Ağaç  Algoritması***:  En  küçük  yayılmalı  ağaç,  aşağıda</p><p>açıklanan üç adımlık bir algoritmanın tekrarı ile saptanabilir.  </p><p>1. adım:  Ağ  kapsamındaki  düğümlerin  oluşturduğu  küme  N  olsun.  Bu kümeden rastgele bir düğüm (i) seçilerek bu düğüme en yakın olan düğüm (j) belirlenir. Bu iki düğümü birleştiren (i, j) dalı en küçük yayılmalı ağacın bir dalı olur. Bu yolla ağın düğümleri, birinde birleştirilmiş (i ve j), diğerinde birleştirilmemiş (i ve j dışındakiler) düğümlerin bulunduğu iki alt kümeye ayrılmış olur. Birleştirilmiş düğümlerin oluşturduğu küme C, birleştirilmemiş</p><p>dNü =ğ üCm Uler C~in ,  odloulşatyuırsıduylğau C k Çü mC~e=  C~ { }i loe ldgöusğtuer uilniru. tAullomramitmaalnıdınır .t ü  m adımlarında </p><p>2. adım:  C~ ’daki düğümlerden (n), C’deki düğümlerden (m) herhangi birine en yakın olan düğüm belirlenir. Bu kez, bu iki düğümü  birleştiren (m, n)  dalı </p><p>en küçük yayılmalı ağaca eklenir. Bu durumda C = {i, j, n} olacağından, C’ye eklenen düğüm (n) C~ kümesinden çıkarılır.  </p><p>t3e. kraadrılman: ırİ. kBinirclie şatidriılmdecekak id üişğlüemml ekra lmtüamd ığdüındğüa, mylearn i bC~irl=eş{ ti}r iolilndcueğyuen  ddae ğeinn küçük yayılmalı ağaç belirlenmiş olur. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**37 YÖNEYLEM ARAŞTIRMASI**|
|**Örnek 4.6**|
|<p>**Örnek 4.6**: Bir işletmenin, çalışanlarının hizmetine sunduğu 7 adet bilgisayarı vardır. Bilgisayarlar arasındaki uzaklıklar aşağıda gösterilmiştir. </p><p>B  7 </p><p>6 </p><p>C </p><p>1 </p><p>D </p><p>E </p><p>` `1 F </p><p>2 </p><p>5 7 </p><p>4 </p><p>5 A </p><p>G </p><p>3 </p><p>4 </p><p>4 </p><p>` `**Şekil  4.34** </p><p>Bilgisayarlar  yeraltı  kabloları  ile  birbirlerine  bağlanmak  istenmektedir.  Bu amacı gerçekleştirecek en kısa kablo uzunluğu nedir? </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**38 YÖNEYLEM ARAŞTIRMASI**|
|**Çözüm 4.6**|
|<p>B  7 </p><p>6 </p><p>C </p><p>1 </p><p>D </p><p>E </p><p>` `1 F </p><p>2 </p><p>5 7 </p><p>4 </p><p>5 </p><p>G </p><p>A </p><p>3 </p><p>4 </p><p>4 </p><p>**Şekil  4.40** </p><p>Başlangıçta  hangi  düğümün  ilk  düğüm  alınmasının  bir  önemi  yoktur.  İlk düğüm olarak E’yi seçelim. Bu kez işlemler ayrıntılarıyla değil aşağıdaki gibi küme gösterimiyle açıklanacaktır. </p><p>Birinci adım: C = {E, F}, C~ = {A, B, C, D, G}; (E, F)  ağaçta.  </p><p>İkinci adım: C = {E, F, C}, C~ = {A, B, D, G}; (F, C) ağaçta. </p><p>Üçüncü adım: C = {E, F, C, D}, C~ = {A, B, G}; (C, D) ağaçta. </p><p>Dördüncü adım: C = {E, F, C, D, A}, C~ = {B, G}; (D, A) ağaçta. </p><p>Beşinci adım: C = {E, F, C, D, A, B}, C~ = {G}; (A, B) ağaçta. </p><p>Altıncı adım: C = {E, F, C, D, A, B, G}, C~ = { }; (E, G) ağaçta.  </p><p>C = {A, B, C, D, E, F, G}, C~ = { } olur. C~ = { } olduğundan problem çözülmüştür. </p><p>Şekil 4.40’da koyu renkle çizilmiş ve beklendiği gibi sayıları ağdaki düğüm sayısının 1 eksiğine (6) eşit olan (A, B), (A, D), (C, D), (C, F), (F, E), (F, G) dallarından oluşan en küçük yayılmalı ağacın uzunluğu 16 birimdir.  </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**39 YÖNEYLEM ARAŞTIRMASI**|
|**Proje Çizelgeleme Problemleri** |
|<p>- Proje yönetiminde, planlama tekniklerinden kritik yol yöntemi (CPM[1]) ile proje değerlendirme ve gözden geçirme tekniği (PERT[2]) gelişmiş ülkelerde çok geniş bir uygulama alanı olan proje çizelgeleme teknikleridir. Anılan yöntemler eldeki sınırlı kaynaklar ölçüsünde projenin tamamlanma süresinin belirlenmesi, toplam maliyeti en düşük yapacak proje süresinin saptanması, sürenin kısaltılması amacıyla kaynak aktarımı yapılması vb. konularda yöneticiler  için hayati önem taşıyan sorunlara  etkili çözüm yolları ararlar ve bulurlar. Anılan yöntemler ülkemizde de birçok büyük projede kullanılmıştır. II. Fatih Sultan Mehmet Köprüsü ve Güney Doğu Anadolu Projesi CPM, Keban Barajı ve İstanbul Boğaz Köprüsü PERT’in uygulandığı projelere örnek gösterilebilir. </p><p>[1] Critical Path Method kelimelerinin ilk harfleri.</p><p>- **[2]** Program Evaluation and Review Techniques kelimelerinin ilk harfleri.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**40 YÖNEYLEM ARAŞTIRMASI**|
||
|- CPM ve PERT, birbirine bağlı çok sayıda faaliyetten oluşan büyük ve projelerin programlanmasında kullanılan yöntemlerdir. Birbirlerinden bağımsız geliştirilmelerine karşın birbirlerine çok benzeyen bu iki yöntem arasındaki en önemli fark faaliyet sürelerine ilişkindir. PERT’de faaliyetlere ilişkin süreler belirsiz olup bir takım olasılık hesaplamaları ile tanımlandığı halde, CPM’de bu sürelerin kesinlikle bilindiği varsayılmaktadır. Yöntemleri açıklamadan önce konuyla ilgili temel kavramların açıklanması uygun olur. |
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**41 YÖNEYLEM ARAŞTIRMASI**|
||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**42 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>ukla  faaliyetler  kesik  çizgili  oklarla  gösterilirler  ve  paralel  (aynı  noktada aşlayıp aynı noktada biten) faaliyetlerin ayırt edilmesinde kullanılırlar. </p><p>Olay  Kukla Faaliyet  Olay </p><p>**Şekil  4.42** </p><p>- *Süreli Kukla Faaliyet*: Belirli bir süresi olmakla birlikte kaynak kullanımı gerektirmeyen faaliyete, süreli kukla faaliyet denir.</p><p>- Örneğin, sulanan veya boyanan bir yerin kuruması için bekletilmesi. Süreli kuklalar bazan kukla faaliyetler gibi kesik çizgi ile bazan gerçek faaliyetler gibi dolu çizgi ile gösterilirler.</p><p>- **Gantt Çizelgesi**</p><p>- Faaliyetler arasındaki zaman ve maliyet faktörlerini de dikkate alarak gösterme fikri yeni değildir. Özellikle Henry Gantt bu konuda daha 1900’lü yılların başlarında önemli çalışmalar yapmış, planlama ve kontrol faaliyetleri için kendi adıyla anılan çizelgeyi (Gantt çizelgesi) geliştirmiştir. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**43 YÖNEYLEM ARAŞTIRMASI**|
||
||**H   A   F   T   A** |
|Faaliyet |1 |2 |3 |4 |5 |6 |7 |8 |9 |10 |11 |12 |13 |14 |15 |
|A ||||||||||||||||
|B ||||||||||||||||
|C ||||||||||||||||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**44 YÖNEYLEM ARAŞTIRMASI**|
||
||**H   A   F   T   A** |
|Faaliyet |1 |2 |3 |4 |5 |6 |7 |8 |9 |10 |11 |12 |13 |14 |15 |
|A ||||||||||||||||
|B ||||||||||||||||
|C ||||||||||||||||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**45 YÖNEYLEM ARAŞTIRMASI**|
|**Ağ Yaklaşımı**|
|<p>Proje söz konusu olduğunda ağ şu şekilde tanımlanmaktadır. "Program amacına ulaşabilmek </p><p>için gerçekleşmesi gereken faaliyetlerden ve olaylardan meydana gelen, faaliyet ve olayların birbirleriyle olan bağlantı ve ilişkilerini gösteren şemaya ağ" denir. Ağ yaklaşımının sağladığı yararlar aşağıdaki gibi özetlenebilir.</p><p>- Bir ya da daha fazla sayıda projenin aynı anda ve istenen ayrıntıda planlama  ve denetiminin yapılmasına olanak sağlar.</p><p>- Faaliyetler arasındaki karmaşık ilişkiler oldukça basit ve açık biçimde gösterilir. </p><p>- İşlemler oldukça basit olup, bilgisayarda kolayca programlanabilir.</p><p>- Kritik faaliyetlerin saptanması sonucunda önemli olan bir grup faalliyete dikkat çekilir. </p><p>- Bazı faaliyetlerin gecikme ve/veya hızlandırılmalarının etkileri ve bunlara bağlı olarak oluşacak darboğazların kolayca saptanabileceği bir ortam oluşturulur.</p><p>- Değişik proje tarihlerine ilişkin toplam proje maliyetleri hesaplanarak en düşük toplam maliyetli proje planı seçilebilir.</p><p>- Kaynaklar, aynı kaynağı kullanan faaliyetler arasında en düşük toplam maliyete neden olacak şekilde bölüştürülebilir. </p><p>- Projenin uygulanması sırasında güncelleştirmeye önem verilerek projenin günü gününe izlenmesi sağlanır. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**46 YÖNEYLEM ARAŞTIRMASI**|
|**Kritik Yol Yöntemi CPM**|
|<p>Kritik yol yöntemi (CPM), bir projenin  erçekleştirilmesinde insan gücü, makina ve </p><p>zamandan en yüksek düzeyde yararlanmayı sağlayan ağ tekniklerini kullanma bilimidir. CPM formülasyon, planlama, gözlem ve kontrol olmak üzere başlıca üç bölüm içerir.</p><p>- Formülasyon sürecinde, projenin belirli faaliyet ve olaylara ayrılmasından sonra bunlar (faaliyetler ve olaylar) arasındaki öncelik ilişkilerinin belirlenmesi gerekir. Bir faaliyetin kendisinden önce bitirilmesi gereken faaliyete "önceki faaliyet", kendisinin tamamlanması ile başlayan faaliyete de "sonraki faaliyet" denir.</p><p>- Faaliyetlerin öncelik ilişkilerinde istenen önemli bilgiler aşağıdaki üç sorunun yanıtlanması ile gerçekleştirilebilir. </p><p>1. Herhangi bir faaliyet başlamadan önce hangi faaliyet(ler) tamamlanmalıdır?</p><p>2. Hangi faaliyetler paralel yürütülmelidir?</p><p>3. Bu faaliyetleri hangi faaliyetler izlemelidir?</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**47 YÖNEYLEM ARAŞTIRMASI**|
|**Proje Ağının Oluşturulması**|
|<p>Proje ağının çizilmesinde uyulması gereken kurallar şöyledir. </p><p>- Her ağda tek bir başlama olayı ile tek bir bitiş olayı olmalıdır. Gerekirse bu olaylar yapay olarak yaratılırlar.</p><p>- Bir faaliyet, kendisinden önceki faaliyet(ler) bitmeden başlayamaz.</p><p>- Bir okun uzunluğu önemli olmayıp oklar yalnızca öncelikleri belirtir.</p><p>- İki olay en fazla bir faaliyet ile doğrudan bağlanabilir.</p><p>- Her olayın bir numarası olmalıdır. Olaylar okların küçük numaralı bir noktadan daha büyük numaralı bir noktaya gitmesini sağlayacak biçimde numaralandırılır. Böylece ağ üzerinde çevrim oluşması engellenmiş olur. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**48 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>Şekil 4.43’deki faaliyetlerin bir çevrim meydana getirdiği görülmektedir. </p><p>2 </p><p>1  3 </p><p>Şekil  4.43 </p><p>Şekil  4.44’de  1  ve  2  numaralı  olaylar  birden  fazla  faaliyetle  doğrudan bağlanmış olup bu yasaktır.  </p><p>1  2 </p><p>**Şekil  4.44** </p><p>Kural 4’e ters düşen bu durumdan kurtulmak için kukla faaliyet kullanılır. Bu duruma uygun alternatif kukla faaliyetler Şekil 4.45’de gösterilmiştir. </p><p>2  2 </p><p>A  K  K  A </p><p>1  B  3  1  B  3 1  A  3  1  A  3 </p><p>B  K  K  B </p><p>2  2 </p><p>Şekil  4.45 </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
**49 YÖNEYLEM ARAŞTIRMASI![](hb5een0m.003.png)**

1  A  4  C  5 

K 

2  B  3  D  6 

Şekil  4.47 

1  A  2  B  3 

Şekil  4.48 

1 

A 

C 

3  4 B 

2 

Şekil  4.49 

3 B 

1  A  2 

C 

4 

Şekil  4.50 

**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**

|**50 YÖNEYLEM ARAŞTIRMASI**|
| - |
||
|Faaliyet |Süre (gün) |Önceki Faaliyet |
|A |4 |- |
|B |8 |- |
|C |2 |A |
|D |3 |A |
|E |8 |B, C |
|F |5 |B, C |
|G |5 |D, E |
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**51 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- Herhangi bir proje yönetim problemi doğrusal programlama olarak tanımlanabilir ve simpleks yöntemle çözülebilir. Bu durumu açıklamak için Örnek 4.7’deki problemi ele alalım.</p><p>- di (i = 1, 2, 3, 4, 5, 6) i olayının gerçekleşme zamanı olsun. Buna göre sözgelimi, d6 projenin, d3 ise B ve C faaliyetlerinin tamamlanma zamanlarını gösterir. Bu durumda (d6 - d1), projenin tamamlanması için geçen süreye karşılık gelir. Amaç projenin en kısa süre içinde tamamlanmasıdır. Buna göre amaç fonksiyonu </p><p>- Z = d - d</p><p>enk 6 1 </p><p>- şeklinde  formüle edilebilir. Herhangi bir (i, j) faaliyeti için j’nin ortaya çıkması  i’nin  gerçekleşmesine ve (i, j)’nin tamamlanmış olmasına bağlıdır. Yani, herhangi bir faaliyet belirli bir süreden daha kısa zamanda tamamlanamaz. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**52 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- Buna göre faaliyetlerin tamamlanma süreleri dikkate alınarak aşağıdaki süre kısıtlayıcıları yazılır.</p><p>- Zdenk = d6 - d1  H faaliyeti kısıtlayıcısı    2  D(3)  4 </p><p>- 6 - d5 ³10 G(5) </p><p>- d6 - d4 ³ 5 G faaliyeti kısıtlayıcısı A(4) </p><p>- d5 - d4 ³ 0 Kukla faaliyet kısıtlayıcısı 1  C(2)  E(8)  K(0)  6 </p><p>- d5 - d3 ³ 5 F faaliyeti kısıtlayıcısı</p><p>- d - d ³ 8 E faaliyeti kısıtlayıcısı B(8)  H(10) </p><p>- d - d3 ³ 3 D faaliyeti kısıtlayıcısı 3  F(5)  5 </p><p>4</p><p>4	 2</p><p>- d - d2 ³ 2 C faaliyeti kısıtlayıcısı **Şekil  4.51** </p><p>3</p><p>- d2 - d1 ³ 4 A faaliyeti kısıtlayıcısı</p><p>- d3 - d1 ³ 8 B faaliyeti kısıtlayıcısı</p><p>- Negatif olmama koşulu; di ³0’ın eklenmesiyle kritik yol belirleme probleminin doğrusal programlama formülasyonu tamamlanmış olur.</p><p>- Yukarıdaki gibi formüllenen problem, simpleks yöntemle çözülerek projenin en kısa tamamlanma süresi belirlenebilir. Nitekim, yukarıdaki problem simpleks yöntemle çözülmüş ve projenin en erken 26 günde (Zenk = 26) tamamlanacağı belirlenmiştir. En iyi olduğu belirlenen çözümde d1 = 0, d2 = 4, d3 = 8, d4 = 16, d5 = 16, d6 = 26 olarak elde edilmiştir.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**53 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- Ağ analizi yaklaşımıyla kritik yolun belirlenmesi konusuna geçmeden önce, bundan sonra sıkça kullanılacak olan, bazı sembolleri tanımlayalım.</p><p>- Dij = (i, j) faaliyetinin tamamlanma süresi</p><p>- Ei = i olayının en erken ortaya çıkma zamanı</p><p>- Li = i olayının en geç ortaya çıkma zamanı</p><p>- Ei, i olayından kaynaklanacak faaliyetlerin en erken başlama zamanını, Li ise aynı faaliyetlerin en geç başlama zamanını verir. Kritik yol üzerindeki olayların en erken başlama ile en geç başlama zamanları aynı olmak zorundadır. Ei ¹Li olması durumunda  bu olayları kritik yolu uzatmadan geciktirmek mümkün olur ki bu, kritik yol tanımına aykırıdır.</p><p>- E değerleri aşağıda açıklanan 3 adımlık bir algoritmayla belirlenir.</p><p>i</p><p>- 1. E = 0’dır.</p><p>1</p><p>- 2. Her faaliyet önceki olay meydana gelir gelmez başlatılır.</p><p>- 3. En erken ortaya çıkış veya başlama zamanı, o olayı oluşturan faaliyetlerin en geç tamamlananın bitiş zamanına eşittir. </p><p>- Bu adımlar ağın başlangıç noktasından başlayarak bitiş noktasına kadar olan her olay için uygulanır.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**54 YÖNEYLEM ARAŞTIRMASI**|
||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**55 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- Projenin son olayının en erken ortaya çıkış zamanı hesaplandığında, projenin en erken tamamlanma süresi belirlenmiş olur. En erken tamamlanma süresinin ilk ve son olaylar arasındaki en uzun yolun uzunluğuna eşit olduğu gösterilebilir.</p><p>- L değerleri de E’ler gibi üç adımlık bir algoritma ile hesaplanırlar. i i</p><p>- L = E ’dir</p><p>n n</p><p>- Her faaliyet bir sonraki olay noktasının en geç meydana geliş zamanından faaliyet süresi çıkarıldığında elde edilen zamanda başlatılır.</p><p>- En geç meydana geliş zamanı, o olaydan kaynaklanan faaliyetlerin en küçük başlama zamanı olarak belirlenir.</p><p>- Bu adımlar bitiş noktasından başlayıp geriye doğru giderek başlangıç noktasına kadar olan her olay için uygulanır. </p><p>- Bir olay noktasının en geç meydana geliş zamanının hesaplanabilmesi için o olaydan kaynaklanan faaliyetlerin sona erdiği noktaların tümünün Li değerlerinin hesaplanmış olması gerekir. </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**56 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- En geç meydana geliş zamanı kavramını aşağıdaki şekil üzerinde açıklayalım.</p><p>- Şekil 4.55’den görüldüğü gibi F; L , G; L ve H; L sürelerinde tamamlandıklarında 7 8 9</p><p>projenin tamamlanması ertelenmeyecektir.</p><p>7 </p><p>F(Di7) </p><p>G(D ) </p><p>i  i8 8 </p><p>H(D ) </p><p>i9</p><p>9 </p><p>**Şekil  4.55** </p><p>- Yukarıdaki şeklin ortaya koyduğu gibi, projenin tamamlanma süresinin uzamaması,  </p><p>- olmasına bağlıdır.</p><p>- Bu bağıntı aşağıdaki gibi genellenebilir.</p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**57 YÖNEYLEM ARAŞTIRMASI**|
||
|<p>- Bu açıklamaların ardından örnek 4.7’deki 6 olayın en erken başlama (Ei)  zamanları aşağıdaki gibi hesaplanmıştır. </p><p>- E1 = 0</p><p>- E2 = E1 + D12 = 0 + 4 = 4</p><p>- E3 = enb{E1 + D13, E2 + D23} = enb{0 + 8,  4 + 2} =  8</p><p>- E4 = enb{E2 + D24, E3 + D34} = enb{4 + 3,  8 + 8} = 16</p><p>- E5 = enb{E3 + D35, E4 + D45} = enb{8 + 5, 16 + 0} = 16  </p><p>- E6 = enb{E4 + D46, E5 + D56} = enb{16 + 5, 16 + 10} = 26 2  D(3)  4 </p><p>- En geç tamamlama zamanları (Li) aşağıdaki gibi  A(4)  G(5) hesaplanmıştır.</p><p>1  C(2) </p><p>- L6 = 26 6 </p><p>- L = L - D = 26 - 10 = 16 B(8) </p><p>5	 6 56</p><p>- L4 = enk{L5 - D45, L6 - D46} = enk{16 - 0, 26 - 5} = 16</p><p>- L3 = enk{L4 - D34, L5 - D35} = enk{16 - 8, 16 - 5} =  8</p><p>- L2 = enk{L3 - D23, L4 - D24} = enk{8 - 2, 16 - 30} =  6  </p><p>- L1 = enk{L2 - D12, L3 - D13} = enk{6 - 4, 8 - 8}    =  0</p><p>K(0) </p><p>E(8) </p><p>H(10) </p><p>3  5 F(5) </p><p>**Şekil  4.51** </p>|
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**58 YÖNEYLEM ARAŞTIRMASI**|
||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|

||
| :- |
||
|`  `0  |`   `0  |`   `0 |
||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|

|**60 YÖNEYLEM ARAŞTIRMASI**|
| - |
||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|
|**61 YÖNEYLEM ARAŞTIRMASI**|
||
||
|`  `0  |`   `0  |`   `0 |
||||` `26 |`    `0 |`   `2|
||
|A |4 |0 |4 |2 |6 |2 |Kritik Değil ||
|B |8 |0 |8 |0 |8 |0 |**Kritik** ||
|||||||||`  `8  |`   `0  |`   `8 |` `16 |`   `0   |` `16 ||
|C |2 |4 |6 |6 |8 |2 |Kritik Değil |`  `8  |`   `0  |`   `8 |` `16 |`   `0   |` `16 ||
|D |3 |4 |7 |13 |16 |9 |Kritik Değil ||
|E |8 |8 |16 |8 |16 |0 |**Kritik** ||
|F |5 |8 |13 |11 |16 |3 |Kritik Değil ||
|K |0 |16 |16 |16 |16 |0 |**Kritik** ||
|G |5 |16 |21 |21 |26 |5 |Kritik Değil ||
||
|**İstanbul Ticaret Üniversitesi Prof. Dr. Ünal H. ÖZDEN** ©**15 Mart 2021 Pazartesi**|

