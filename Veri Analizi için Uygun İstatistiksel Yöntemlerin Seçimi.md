# **Veri Analizi için Uygun İstatistiksel Yöntemlerin Seçimi**



## **Özet**

Biyoistatistikte, her bir spesifik durum için, verilerin analizi ve yorumlanması için istatistiksel yöntemler mevcuttur. Uygun istatistiksel yöntemi seçmek için, veri analizi için uygun istatistiksel yöntemin seçilebilmesi için istatistiksel yöntemlerin varsayımlarının ve koşullarının bilinmesi gerekir. Veri analizinde iki ana istatistiksel yöntem kullanılır: ortalama ve medyan gibi indeksleri kullanarak verileri özetleyen tanımlayıcı istatistikler ve bir diğeri, öğrencinin t gibi istatistiksel testleri kullanarak verilerden sonuçlar çıkaran çıkarımsal istatistiklerdir.-Ölçek. Uygun istatistiksel yöntemin seçimi şu üç şeye bağlıdır: Çalışmanın amacı ve hedefi, Kullanılan verilerin türü ve dağılımı ve Gözlemlerin doğası (eşli/eşsiz). Ortalamaları karşılaştırmak için kullanılan tüm istatistiksel yöntemler parametrik olarak adlandırılırken, ortalamalar dışında karşılaştırma yapmak için kullanılan istatistiksel yöntemler (eski medyan/ortalama sıralar/oranlar) parametrik olmayan yöntemler olarak adlandırılır. Bu makalede, parametrik ve parametrik olmayan yöntemleri, varsayımlarını ve biyomedikal verilerin analizi ve yorumlanması için uygun istatistiksel yöntemlerin nasıl seçileceğini tartıştık.



## **Giriş**

Uygun istatistiksel yöntemin seçimi, biyomedikal verilerin analizinde çok önemli bir adımdır. İstatistiksel yöntemin yanlış seçilmesi, bulguların yorumlanmasında ciddi problemler yaratmakla kalmaz, aynı zamanda çalışmanın sonucunu da etkiler. İstatistikte, her özel durum için, verilerin analizi ve yorumlanması için istatistiksel yöntemler mevcuttur. Uygun istatistiksel yöntemi seçmek için, istatistiksel yöntemlerin varsayımlarını ve koşullarını bilmek gerekir, böylece veri analizi için uygun istatistiksel yöntem seçilebilir.[1] İstatistiksel yöntemlerin bilinmesi dışında, çok önemli olan diğer bir husus, toplanan verilerin doğası ve türü ve çalışmanın amacıdır çünkü amaca göre, verilen verilere uygun karşılık gelen istatistiksel yöntemler seçilir. Yanlış veya uygun olmayan istatistiksel yöntemin uygulanması, biyomedikal araştırmalarda yayınlanan makalelerde yaygın bir olgudur. Yanlış istatistiksel yöntemler, eşleştirilmemiş t kullanımı gibi birçok durumda görülebilir.-eşleştirilmiş veriler üzerinde test veya normal dağılıma uymayan veriler için parametrik test kullanımı vb., Günümüzde SPSS, R, Stata, SAS gibi birçok istatistiksel yazılım mevcuttur ve bu yazılımlar kullanılarak kolayca işlem yapılabilir. istatistiksel analiz, ancak uygun istatistiksel testin seçimi, özellikle istatistiksel olmayan geçmişi olan biyomedikal araştırmacılar için hala zor bir görevdir.[2] Veri analizinde iki ana istatistiksel yöntem kullanılır: tanımlayıcı istatistikler, ortalama, medyan gibi indeksleri kullanarak verileri özetler. , standart sapma ve bir diğeri, student's t-testi, ANOVA testi, vb. gibi istatistiksel testleri kullanarak verilerden sonuçlar çıkaran çıkarımsal istatistiklerdir.[3]


## **İstatistiksel Yöntemlerin Seçimini Etkileyen Faktörler**

Uygun istatistiksel yöntemin seçimi şu üç şeye bağlıdır: Çalışmanın amacı ve hedefi, Kullanılan verilerin türü ve dağılımı ve Gözlemlerin doğası (eşli/eşsiz).

### Çalışmanın amacı ve hedefi

İstatistiksel testin seçimi, çalışmanın amacına ve amacına bağlıdır. Hedefimizin sonuç değişkeninin yordayıcılarını bulmak olduğunu varsayalım, ardından regresyon analizi kullanılırken, iki bağımsız örnek arasındaki ortalamaları karşılaştırmak için eşleştirilmemiş örnekler t-testi kullanılır.

### Kullanılan verilerin türü ve dağılımı

Aynı amaç için istatistiksel test seçimi veri tiplerine göre değişmektedir. Nominal, sıralı, ayrık veriler için parametrik olmayan yöntemler kullanılırken, sürekli veriler için parametrik yöntemlerin yanı sıra parametrik olmayan yöntemler de kullanılır.[4] Örneğin regresyon analizinde sonuç değişkenimiz kategorik olduğunda lojistik regresyon, sürekli değişken için ise lineer regresyon modeli kullanılır. Sürekli değişken için en uygun temsili ölçünün seçimi, değerlerin nasıl dağıldığına bağlıdır. Sürekli değişken normal dağılımı izliyorsa, ortalama temsili ölçüdür, normal olmayan veriler için ise medyan veri setinin en uygun temsili ölçüsü olarak kabul edilir. Benzer şekilde kategorik verilerde orantı (yüzde), sıralı/sıralı verilerde ise sıra ortalamaları temsili ölçütümüzdür. Çıkarımsal istatistikte, bu ölçüler kullanılarak hipotez oluşturulur ve ayrıca hipotez testinde bu ölçüler, anlamlılık düzeyini hesaplamak için gruplar arasında/gruplar arasında karşılaştırma yapmak için kullanılır. Diyelim ki diyastolik kan basıncını (DBP) üç yaş grubu (yıl) (<30, 30--50, >50) arasında karşılaştırmak istiyoruz. DBP değişkenimiz normal olarak dağılıyorsa, ortalama değer bizim temsili ölçütümüzdür ve sıfır hipotezi, ortalama DB'yi belirtir.Üç yaş grubunun P değerleri istatistiksel olarak eşittir. Normal olmayan DBP değişkeni durumunda, medyan değer bizim temsili ölçütümüzdür ve sıfır hipotezi, DB P'nin dağılımınınüç yaş grubu arasındaki değerler istatistiksel olarak eşittir. Yukarıdaki örnekte, DBP normal dağılımı izlediğinde ortalamaları karşılaştırmak için tek yönlü ANOVA testi kullanılırken, DBP normal olmayan bir dağılım izlediğinde DBP'nin üç yaş grubu arasındaki dağılımını karşılaştırmak için Kruskal--Wallis H testleri/medyan testleri kullanılır. Benzer şekilde, tedavi ve kontrol grupları arasında ortalama arter basıncını (OAB) karşılaştırmak istediğimizi varsayalım, OAB değişkenimiz normal dağılıma uyuyorsa, bağımsız örnekler t-testi, normal dağılıma uymuyorsa Mann--Whitney U testi kullanılır. tedavi ve kontrol grupları arasındaki OAB'yi karşılaştırmak için.

### Gözlemler eşleştirilmiş veya eşlenmemiş

İstatistiksel testin seçiminde bir diğer önemli nokta, verilerin eşleştirilmiş (aynı denekler farklı zaman noktalarında veya farklı yöntemler kullanılarak ölçümlerdir) veya eşleştirilmemiş (her grubun farklı konusu vardır) olup olmadığını değerlendirmektir. Örneğin, iki grup arasındaki ortalamaları karşılaştırmak için, veriler eşlendiğinde eşleştirilmiş örnekler t testi, eşleştirilmemiş (bağımsız) veriler için bağımsız örnekler t testi kullanılır.


## **Parametrik ve Parametrik Olmayan Yöntemler Kavramı**

Çıkarımsal istatistiksel yöntemler iki olası kategoriye ayrılır: parametrik ve parametrik olmayan. Ortalamaları karşılaştırmak için kullanılan tüm istatistiksel yöntemler parametrik olarak adlandırılırken, ortalamalar dışında karşılaştırma yapmak için kullanılan istatistiksel yöntemler (eski medyan/ortalama sıralar/oranlar) parametrik olmayan yöntemler olarak adlandırılır. Parametrik testler, değişkenin sürekli olduğu ve yaklaşık normal dağılıma uygun olduğu varsayımına dayanır. Veriler, normal dağılıma sahip olmayan veya sürekli değişken dışındaki herhangi bir veri türü ile sürekli olduğunda, parametrik olmayan yöntemler kullanılır. Neyse ki, en sık kullanılan parametrik yöntemlerin parametrik olmayan karşılıkları vardır. Bu, bir parametrik testin varsayımları ihlal edildiğinde ve yedek analiz olarak parametrik olmayan alternatifi seçebileceğimiz zaman yararlı olabilir.[3]


## **Parametrik ve Parametrik Olmayan Yöntemler Arasında Seçim**

Tüm tip t - testi, F testi parametrik test olarak kabul edilir. İki grup arasındaki ortalamaları karşılaştırmak için Student t testi (tek örneklem t testi, bağımsız örneklem t testi, eşleştirilmiş örneklem t testi) kullanılırken, F testi (tek yönlü ANOVA, tekrarlanan ölçümler ANOVA vb.) öğrencinin t uzantısı-test, ortalamaları üç veya daha fazla grup arasında karşılaştırmak için kullanılır. Benzer şekilde, doğrusal regresyon da parametrik yöntemler olarak kabul edilen Pearson korelasyon katsayısı, verilerin ortalama ve standart sapmasını kullanarak hesaplamak için kullanılır. Yukarıdaki parametrik yöntemler için, eşdeğer parametrik olmayan yöntemler de mevcuttur. Örneğin, Student t testi için Mann--Whitney U testi ve Wilcoxon testi kullanılırken, F testinin (ANOVA) alternatif yöntemleri Kruskal--Wallis H testi, medyan testi ve Friedman testidir . Benzer şekilde, Pearson korelasyonunun ve lineer regresyonun parametrik olmayan yöntemi olarak sırasıyla Spearman sıra korelasyon katsayısı ve log lineer regresyon kullanılmaktadır.[ [3], [5], [6], [7],[8] Parametrik ve karşılığı parametrik olmayan yöntemler[tablo 1]

### tablo 1

Parametrik ve Alternatif Parametrik Olmayan Yöntemler

<table>

<thead>

<tr>

<th>

**Açıklama**

</th>

<th>

**Parametrik Yöntemler**

</th>

<th>

**Parametrik Olmayan Yöntemler**

</th>

</tr>

</thead>

<tbody>

<tr>

<td>

Tanımlayıcı istatistikler

</td>

<td>

Ortalama, Standart sapma

</td>

<td>

Medyan, Çeyrekler arası aralık

</td>

</tr>

<tr>

<td>

Nüfus (veya varsayımsal değer) içeren örnek

</td>

<td>

Tek örneklem t testi ( n <30) ve Tek örneklem Z testi ( n ≥30)

</td>

<td>

Bir örnek Wilcoxon imzalı sıralama testi

</td>

</tr>

<tr>

<td>

Eşleştirilmemiş iki grup

</td>

<td>

Bağımsız örnekler t testi (Eşleştirilmemiş örnekler t testi)

</td>

<td>

Mann Whitney U testi/Wilcoxon sıra toplamı testi

</td>

</tr>

<tr>

<td>

İki eşleştirilmiş grup

</td>

<td>

Eşleştirilmiş örnekler t testi

</td>

<td>

İlgili örnekler Wilcoxon işaretli sıralama testi

</td>

</tr>

<tr>

<td>

Üç veya daha fazla eşleştirilmemiş grup

</td>

<td>

Tek yönlü ANOVA

</td>

<td>

Kruskal-Wallis H testi

</td>

</tr>

<tr>

<td>

Üç veya daha fazla eşleştirilmiş grup

</td>

<td>

Tekrarlanan ölçümler ANOVA

</td>

<td>

Friedman Testi

</td>

</tr>

<tr>

<td>

İki değişken arasındaki doğrusal ilişkinin derecesi

</td>

<td>

Pearson korelasyon katsayısı

</td>

<td>

Spearman sıra korelasyon katsayısı

</td>

</tr>

<tr>

<td>

Bir sonuç değişkenini en az bir bağımsız değişkenle tahmin edin

</td>

<td>

Doğrusal regresyon modeli

</td>

<td>

Lineer olmayan regresyon modeli/Log normal verilerinde Log lineer regresyon modeli

</td>

</tr>

</tbody>

</table>



## **Oranları Karşılaştırmak İçin İstatistiksel Yöntemler**

Oranları karşılaştırmak için kullanılan istatistiksel yöntemler parametrik olmayan yöntemler olarak kabul edilir ve bu yöntemlerin alternatif parametrik yöntemleri yoktur. Pearson Ki-kare testi ve Fisher kesin testi, iki veya daha fazla bağımsız grup arasındaki oranları karşılaştırmak için kullanılır. İki eşli grup arasındaki oranların değişimini test etmek için McNemar testi kullanılırken, aynı amaç için üç veya daha fazla eşli grup arasında Cochran Q testi kullanılır. Oranlar için Z testi, bağımsız ve bağımlı gruplar için iki grup arasındaki oranları karşılaştırmak için kullanılır.[6], [7], [8][Tablo 2]

### Tablo 2

Oranları Karşılaştırmak İçin İstatistiksel Yöntemler

<table>

<thead>

<tr>

<th>

**Açıklama**

</th>

<th>

**İstatistiksel Yöntemler**

</th>

<th>

**Veri tipi**

</th>

</tr>

</thead>

<tbody>

<tr>

<td>

İki kategorik değişken arasındaki ilişkiyi test edin (Bağımsız gruplar)

</td>

<td>

Pearson Ki-kare testi/Fisher kesin testi

</td>

<td>

Değişkenin ≥2 kategorisi var

</td>

</tr>

<tr>

<td>

2/3 grup (eşli gruplar) arasındaki oranlardaki değişikliği test edin

</td>

<td>

McNemar testi/Cochrane Q testi

</td>

<td>

Değişkenin 2 kategorisi var

</td>

</tr>

<tr>

<td>

Oranlar arasındaki karşılaştırmalar

</td>

<td>

Oranlar için Z testi

</td>

<td>

Değişkenin 2 kategorisi var

</td>

</tr>

</tbody>

</table>



## **Diğer İstatistiksel Yöntemler**

Sınıf içi korelasyon katsayısı, her iki ön-son veri sürekli ölçekte olduğunda hesaplanır. Ağırlıksız ve ağırlıklı Kappa istatistikleri, sırasıyla nominal ve sıralı veriler için aynı konularda (pre-post) ölçülen iki yöntem arasındaki mutlak uyumu test etmek için kullanılır. Yarı parametrik veya parametrik olmayan bazı yöntemler vardır ve bu yöntemler, karşılığı parametrik yöntemler mevcut değildir. Yöntemler, lojistik regresyon analizi, hayatta kalma analizi ve alıcı işletim özellikleri eğrisidir.[ [9] Lojistik regresyon analizi, bağımsız değişken(ler) kullanılarak kategorik sonuç değişkenini tahmin etmek için kullanılır. Hayatta kalma analizi, hayatta kalma süresini/hayatta kalma olasılığını hesaplamak, gruplar arasında hayatta kalma süresinin karşılaştırılması (Kaplan--Meier yöntemi) ve ayrıca deneklerin/hastaların hayatta kalma süresinin öngörücülerini belirlemek (Cox regresyon analizi) için kullanılır. Alıcı çalışma özellikleri (ROC) eğrisi, kategorik sonuç değişkeni kullanılarak karşılık gelen teşhis doğruluğu ile verilen sürekli değişken için eğri altındaki alanı (AUC) ve kesme değerlerini hesaplamak için kullanılır. Test yönteminin tanısal doğruluğu, başka bir yöntemle (genellikle altın standart yöntemle karşılaştırıldığında) karşılaştırılarak hesaplanır. Duyarlılık (gerçek hastalık vakalarından tespit edilen hastalık vakalarının oranı), özgüllük (hastalık olmayan gerçek deneklerden saptanan hastalık olmayan deneklerin oranı), genel doğruluk (hastalığı ve hastalık olmayan deneklerin doğru bir şekilde saptanması için test ve altın standart yöntemleri arasındaki uyum oranı), test yönteminin teşhis doğruluğu. Yanlış negatif oranı (1-duyarlılık), yanlış-pozitif oranı (1-özgüllük), pozitif olasılık oranı (hassasiyet/yanlış pozitif oranı), negatif olasılık oranı (yanlış negatif oranı/Özgüllük), pozitif tahmin değeri ( test değişkeni tarafından doğru tespit edilen hastalık vakalarının, kendisi tarafından tespit edilen toplam hastalık vakalarına oranı),[3], [6], [10] [[Tablo 3]

### Tablo 3

Yarı parametrik ve parametrik olmayan yöntemler

<table>

<thead>

<tr>

<th>

**Açıklama**

</th>

<th>

**İstatistiksel yöntemler**

</th>

<th>

**Veri tipi**

</th>

</tr>

</thead>

<tbody>

<tr>

<td>

Bağımsız değişkenleri kullanarak sonuç değişkenini tahmin etmek

</td>

<td>

İkili Lojistik regresyon analizi

</td>

<td>

Sonuç değişkeni (iki kategori), Bağımsız değişken(ler): Kategorik (≥2 kategori) veya Sürekli değişkenler veya her ikisi

</td>

</tr>

<tr>

<td>

Bağımsız değişkenleri kullanarak sonuç değişkenini tahmin etmek

</td>

<td>

Çok Terimli Lojistik regresyon analizi

</td>

<td>

Sonuç değişkeni (≥3 kategori), Bağımsız değişken(ler): Kategorik (≥2 kategori) veya sürekli değişkenler veya her ikisi

</td>

</tr>

<tr>

<td>

Sürekli değişkende Eğri altındaki alan ve kesme değerleri

</td>

<td>

Alıcı çalışma özellikleri (ROC) eğrisi

</td>

<td>

Sonuç değişkeni (iki kategori), Test değişkeni : Sürekli

</td>

</tr>

<tr>

<td>

Verilen eşit aralıklar için deneklerin hayatta kalma olasılığını tahmin etmek

</td>

<td>

Yaşam tablosu analizi

</td>

<td>

Sonuç değişkeni (iki kategori), Takip süresi : Sürekli değişken

</td>

</tr>

<tr>

<td>

≥2 gruplarda hayatta kalma süresini P ile karşılaştırmak için

</td>

<td>

Kaplan--Meier eğrisi

</td>

<td>

Sonuç değişkeni (iki kategori), Takip süresi : Sürekli değişken, Bir kategorik grup değişkeni

</td>

</tr>

<tr>

<td>

Hayatta kalma olasılığını etkileyen öngörücüleri değerlendirmek

</td>

<td>

Cox regresyon analizi

</td>

<td>

Sonuç değişkeni (iki kategori), Takip süresi : Sürekli değişken, Bağımsız değişken(ler): Kategorik değişken(ler) (≥2 kategori) veya sürekli değişken(ler) veya her ikisi

</td>

</tr>

<tr>

<td>

Altın standart yönteme kıyasla test değişkeninin tanısal doğruluğunu tahmin etmek

</td>

<td>

Teşhis doğruluğu (Hassasiyet, Spesifiklik vb.)

</td>

<td>

Her iki değişken de (altın standart yöntem ve test yöntemi) kategorik olmalıdır (2 × 2 tablo)

</td>

</tr>

<tr>

<td>

İki teşhis yöntemi arasında Mutlak Uyum

</td>

<td>

Ağırlıksız ve ağırlıklı Kappa istatistikleri/Sınıf içi korelasyon

</td>

<td>

İki Nominal değişken (ağırlıksız Kappa), İki Ordinal değişken (Ağırlıklı kappa), İki Sürekli değişken (Sınıf içi korelasyon) arasında

</td>

</tr>

</tbody>

</table>


## **Parametrik Olmayan Yöntemlerin Parametrik Yöntemlere Göre Avantaj ve Dezavantajları ve Örnek Büyüklüğü Sorunları**

Parametrik yöntemler, parametrik olmayan yöntemlere kıyasla gruplar arasındaki farkı tespit etmek için daha güçlü bir testtir, ancak verilerin normalliği ve örneklem büyüklüğü dahil olmak üzere bazı katı varsayımlar nedeniyle parametrik testi her durumda kullanamayız ve alternatif parametrik olmayan yöntemlerle sonuçlanır. kullanılmış. Ortalama, aykırı değerlerden birkaç kez etkilenen parametrik yöntemi karşılaştırmak için kullanılırken, parametrik olmayan yöntemde, medyan/ortalama sıra, aykırı değerlerden etkilenmeyen temsili ölçümlerimizi ifade eder. [11]

Student t-testi ve ANOVA testi gibi parametrik yöntemlerde, ortalama ve standart sapma kullanılarak anlamlılık düzeyi hesaplanır ve her gruptaki standart sapmayı hesaplamak için en az iki gözlem gerekir. Her grubun en az iki gözlemi yoksa, seçilecek alternatif parametrik olmayan yöntemi, verilerin ortalama sıralarının karşılaştırılmasıyla çalışır.

Küçük örneklem büyüklüğü için (grup başına ortalama ≤15 gözlem), normallik testi yöntemleri normal olmama konusunda daha az hassastır ve normal olmayan verilere sahip olmasına rağmen normalliği tespit etme şansı vardır. Örnek boyutunun küçük olduğu durumlarda, yalnızca oldukça normal dağılan verilerde parametrik yöntemin kullanılması, aksi takdirde karşılık gelen parametrik olmayan yöntemlerin tercih edilmesi önerilir. Benzer şekilde, yeterli veya büyük örneklem büyüklüğünde (grup başına ortalama >15 gözlem), istatistiksel yöntemlerin çoğu normal olmama konusunda oldukça hassastır ve normal verilere sahip olmasına rağmen normal olmamayı yanlış bir şekilde tespit etme şansı vardır. Örneklem büyüklüğünün yeterli olduğu durumlarda sadece yüksek derecede normal olmayan verilerde parametrik olmayan yöntemin kullanılması, aksi takdirde karşılık gelen parametrik yöntemlerin tercih edilmesi önerilir.[12]

### İstatistiksel Yöntemler İçin Gerekli Minimum Örnek Büyüklüğü

Minimum güven düzeyinde (genellikle %95) ve testin gücünde (genellikle %80) ortalamalar/medyanlar/ortalama sıralar/oranlar arasındaki önemli farkı saptamak için, kaç kişi/denek (örnek boyutu) gereklidir? algılanan etki boyutu. Etki büyüklüğü ve buna karşılık gelen gerekli örneklem büyüklüğü birbiriyle ters orantılıdır, yani testin aynı güvenirlik ve güç düzeyinde, etki büyüklüğü arttıkça gerekli örneklem büyüklüğü azalmaktadır. Özet, herhangi bir istatistiksel yöntem için minimum veya maksimum örneklem büyüklüğü sabit değildir ve etki büyüklüğü, güven düzeyi, çalışmanın gücü vb. gibi verilen girdilere dayalı olarak tahmine tabidir. Yalnızca yeterli örneklem büyüklüğü üzerinde, farkı önemli ölçüde tespit edebiliriz. Gerçekte gerekenden daha fazla örneklem büyüklüğünün bulunmaması durumunda,


## **İstatistiksel Yöntemlerin Yanlış Seçiminin Etkisi**

Her duruma özel istatistiksel yöntemler vardır. Uygun istatistiksel yöntemin seçilmemesi, anlamlılık seviyemizi ve sonuçlarını etkiler.[13] Örneğin, bir çalışmada kontrolün sistolik kan basıncı (ortalama ± SS) (126.45 ± 8.85, n <sub>1</sub> =20) ve tedavi (121.85 ± 5.96, n <sub>2</sub> =20) grubu Bağımsız örneklem t - testi (doğru uygulama) kullanılarak karşılaştırıldı. Sonuç, iki grup arasındaki ortalama farkın istatistiksel olarak önemsiz olduğunu gösterdi ( P = 0.061), aynı veriler üzerinde, eşleştirilmiş örnekler t - testi (yanlış uygulama) ortalama farkın istatistiksel olarak anlamlı olduğunu gösterdi ( P = 0.061)= 0.011). Yanlış uygulama nedeniyle, gerçekte fark olmamasına rağmen gruplar arasında istatistiksel olarak anlamlı bir fark tespit ettik.


## **Sonuçlar**

Kaliteli araştırma için uygun istatistiksel yöntemlerin seçimi çok önemlidir. Bir araştırmacının, geçerli ve güvenilir sonuçlar üreten bir araştırma çalışması yürütmek için kullanılan istatistiksel yöntemlerin temel kavramlarını bilmesi önemlidir. Farklı durumlarda kullanılabilecek çeşitli istatistiksel yöntemler vardır. Her test, veriler hakkında belirli varsayımlarda bulunur. En uygun testin hangisi olduğuna karar verilirken bu varsayımlar dikkate alınmalıdır. İstatistiksel yöntemlerin yanlış veya uygunsuz kullanımı hatalı sonuçlara yol açabilir, sonuçta kanıta dayalı uygulamalara zarar verebilir. Bu nedenle, yeterli istatistik bilgisi ve istatistiksel testlerin uygun kullanımı, kaliteli biyomedikal araştırmaları geliştirmek ve üretmek için önemlidir. Yine de, bir biyomedikal araştırmacısının veya akademisyenin istatistiksel yöntemlerin tamamını öğrenmesi son derece zordur. Bu nedenle, yayınlanan araştırmalarda doğru/yanlış uygulamaların fark edilebilmesi ve istatistiksel yöntemlerin uygun seçiminin karar verebilmesi için en azından temel bilgiler çok önemlidir. Verileri analiz etmek için çevrimiçi ve çevrimdışı olarak kullanılabilen birçok yazılım vardır, ancak araştırmacıların anlaması gereken veri ve çalışma hedefi için hangi istatistiksel test setinin uygun olduğu gerçeği hala çok zordur. Bu nedenle çalışmanın planlanmasından veri toplama, analiz ve son olarak inceleme sürecine kadar, İstatistik uzmanlarından uygun konsültasyon alternatif bir seçenek olabilir ve klinisyenlerin çok fazla zaman ve çaba gerektiren ve nihayetinde klinik çalışmalarını etkileyen derinlemesine istatistiklere gitme yükünü azaltabilir. Bu uygulamalar sadece araştırmalarda biyoistatistik yöntemlerin doğru ve uygun kullanımını sağlamakla kalmaz, aynı zamanda araştırmalarda ve dergilerde istatistiksel raporlamanın en yüksek kalitede olmasını sağlar.[14]



## **Referanslar**

1. Nayak BK, Hazra A. How to choose the right statistical test.? Indian J Ophthalmol. 2011;59:85–6. [PMC free article] [PubMed] [Google Scholar]
2. Karan J. How to select appropriate statistical test.? J Pharm Negative Results. 2010;1:61–3. [Google Scholar]
3. Mishra P, Mayilvaganan S, Agarwal A. Statistical methods in endocrine surgery journal club. World J Endoc Surg. 2015;7:21–3. [Google Scholar]
4. Mishra P, Pandey CM, Singh U, Gupta A. Scales of measurement and presentation of statistical data. Ann Card Anaesth. 2018;21:419–22. [PMC free article] [PubMed] [Google Scholar]
5. Campbell MJ, Swinscow TDV. Wiley-Blackwell: BMJ Books; 2009. Statistics at Square One 11th ed. [Google Scholar]
6. Sundaram KR, Dwivedi SN, Sreenivas V. Medical Statistics: Principles And Methods. Anshan: 2010. [Google Scholar]
7. Altman DG. Practical Statistics For Medical Research. CRC Press; 1990. [Google Scholar]
8. Barton B, Peat J. 2nd ed. Wiley Blackwell, BMJ Books; 2014. Medical Statistics: A Guide to SPSS, Data Analysis and Clinical Appraisal. [Google Scholar]
9. Peat J, Barton B. John Wiley & Sons; 2008. Medical Statistics: A Guide to Data Analysis and Critical Appraisal. [Google Scholar]
10. Armitage P, Berry G, Matthews JNS. John Wiley & Sons; 2008. Statistical Methods In Medical Research. [Google Scholar]
11. Kim HY. Statistical notes for clinical researchers: Assessing normal distribution (2) using skewness and kurtosis. Open lecture on statistics. Restor Dent Endod. 2013;38:52–4. [PMC free article] [PubMed] [Google Scholar]
12. Ghasemi A, Zahediasl S. Normality Tests for Statistical Analysis: A Guide for Non-Statisticians. Int J Endocrinol Metab. 2012;10:486–9. [PMC free article] [PubMed] [Google Scholar]
13. Strasak AM, Zaman Q, Pfeiffer KP, Göbel G, Ulmer H. Statistical errors in medical research: A review of common pitfalls. Swiss Med Wkly. 2007;137:44–9. [PubMed] [Google Scholar]
14. Bajwa SJ. Basics, common errors and essentials of statistical tools and techniques in anesthesiology research. J Anesthesiol Clin Pharmacol. 2015;31:547–53. [PMC free article] [PubMed] [Google Scholar]
