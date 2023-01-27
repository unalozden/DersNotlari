# **Sürekli veriler için parametrik olmayan istatistiksel testler: temel kavram ve pratik kullanım**

## **Özet**

Geleneksel istatistiksel testler genellikle parametrik testler olarak adlandırılır. Parametrik testler, birçok tıp makalesinde parametrik olmayan testlerden daha sık kullanılmaktadır çünkü tıp araştırmacılarının çoğu parametrik testlere aşinadır ve istatistiksel yazılım paketleri parametrik testleri güçlü bir şekilde desteklemektedir. Parametrik testler önemli varsayımlar gerektirir; normallik varsayımı, bu, örneklem araçlarının dağılımının normal olarak dağıldığı anlamına gelir. Ancak bu varsayım sağlanmadığında parametrik test yanıltıcı olabilir. Bu durumda, parametrik olmayan testler, normallik varsayımını gerektirmedikleri için mevcut alternatif yöntemlerdir. Parametrik olmayan testler, işaretlere ve sıralara dayalı istatistiksel yöntemlerdir. Bu yazıda, doğru kullanım kılavuzu için parametrik olmayan testlerin temel kavramlarını ve pratik kullanımını tartışacağız.

**Anahtar Kelimeler: **Veri yorumlama, Araştırma tekniği, Parametrik olmayan istatistik, İstatistiksel veri analizi



## **Giriş**

İstatistiksel analiz, bir sonucun geçerliliğini değerlendirmek için kullanılan evrensel bir yöntemdir. Tıbbi bir makalenin en önemli yönlerinden biridir. İstatistiksel analiz, aksi takdirde anlamsız olan sayı dizilerine anlam verir ve araştırmacıların belirsiz gerçeklerden sonuçlar çıkarmasına izin verir. Dolayısıyla veriye hayat veren bir yaratım işidir. Bununla birlikte, istatistiksel tekniklerin uygunsuz kullanımı hatalı sonuçlara yol açar, hatalara yol açar ve makalenin önemini azaltır. Dahası, tıp araştırmacıları, kanıta dayalı tıp bu günlerde tıp sahnesinin merkezinde yer aldığından, istatistiksel geçerlilik elde etmeye daha fazla dikkat etmelidir. Son zamanlarda istatistiksel analiz paketlerindeki hızlı gelişmeler, daha uygun analizlere kapı aralamıştır. Bununla birlikte, istatistiksel analizleri gerçekleştirmenin daha kolay yöntemleri,[1].

Korean Journal of Anesthesiology dahil olmak üzere birçok dergi, tıp dergilerindeki genel istatistiksel hataları belirlemek ve azaltmak için çaba göstermektedir [ [2], [3], [4], [5]. Sonuç olarak, birçok makalede çok çeşitli istatistiksel hatalar bulundu. Bu, her derginin editörlerini istatistiksel hataları azaltmak için yazarlar ve hakemler [ [6], [7], [8], [9] için kontrol listeleri veya yönergeler geliştirerek dergilerinin kalitesini artırma konusunda daha da motive etmiştir . Dergilerde bulunan en yaygın istatistiksel hatalardan biri, parametrik istatistiksel tekniklerin parametrik olmayan verilere uygulanmasıdır  [4], [5]. Bunun nedeninin, tıbbi araştırmacıların parametrik tekniklere kıyasla parametrik olmayan istatistiksel teknikleri kullanmak için nispeten daha az fırsata sahip olmalarından kaynaklandığı tahmin edilmektedir, çünkü onlar çoğunlukla parametrik istatistik konusunda eğitilmişlerdir ve birçok istatistik yazılım paketi parametrik istatistiksel teknikleri güçlü bir şekilde desteklemektedir. Bu nedenle, bu makale, geçmişte nadiren tanıtılan parametrik olmayan istatistiksel tekniklerin kullanımına ilişkin gerçek vakalar sağlayarak parametrik olmayan istatistiksel analiz anlayışımızı artırmayı amaçlamaktadır.

## **Parametrik Olmayan İstatistiksel Analizin Tarihi**

İskoç bir matematikçi ve doktor olan John Arbuthnott, 1710'da parametrik olmayan analitik yöntemleri tanıtan ilk kişiydi [ [10]. "Her iki cinsiyetin Doğumlarında gözlemlenen sabit düzenlilikten alınan ilahi takdir için bir Argüman" adlı makalesinde bugün kullanılan işaret testine benzer bir istatistiksel analiz yaptı. Bu makaleden sonra bir süre parametrik olmayan analiz kullanılmadı, ta ki Jacob Wolfowitz 1942'de tekrar "parametrik olmayan" terimini kullanana kadar [ [11]. Daha sonra, 1945 yılında Frank Wilcoxon, günümüzde en yaygın kullanılan yöntem olan rank kullanan parametrik olmayan bir analiz yöntemini tanıttı [ [12 ]. 1947'de Henry Mann ve öğrencisi Donald Ransom Whitney, farklı sayıda numuneden oluşan iki grubu karşılaştırmak için bir teknik geliştirmek üzere Wilcoxon'ın tekniğini genişletti [13]. 1951'de William Kruskal ve Allen Wallis, sıralama verilerini kullanarak üç veya daha fazla grubu karşılaştırmak için parametrik olmayan bir test yöntemi geliştirdiler [14]. O zamandan beri, birkaç çalışma parametrik olmayan analizlerin parametrik yöntemler kadar verimli olduğunu bildirdi; parametrik olmayan istatistiksel analizin, özellikle Wilcoxon's Signed Rank testinin ve Mann-Whitney testinin asimptotik bağıl etkinliğinin, veriler normallik varsayımını karşıladığında t-testine karşı 0.955 olduğu bilinmektedir [ [15], [16]. Tukey, parametrik olmayan bir yöntem kullanarak güven aralıklarını hesaplamak için bir yöntem geliştirdiğinden beri, parametrik olmayan analiz, tıp ve doğa bilimleri araştırmalarında yaygın olarak kullanılan bir analitik yöntem olarak kuruldu [17].

## **Parametrik Olmayan İstatistiksel Analizin Temel Prensibi**

Tıbbi araştırmalarda yaygın olarak kullanılan türlerden t-testi ve varyans analizi gibi geleneksel istatistiksel yöntemler, popülasyonun veya örneğin dağılımı hakkında belirli varsayımlar gerektirir. Özellikle, örneklem grubunun ortalamalarının normal dağıldığını belirten normallik varsayımı ve örneklerin ve bunlara karşılık gelen popülasyonun varyanslarının eşit olduğunu belirten eşit varyans varsayımı, en temel önkoşullardır. parametrik istatistiksel analiz. Bu nedenle, parametrik istatistiksel analizler, yukarıdaki varsayımların sağlandığı varsayımıyla yapılır. Ancak bu varsayımlar sağlanmıyorsa, yani örneklemin dağılımı bir tarafa doğru çarpıksa veya örneklem boyutunun küçük olması nedeniyle dağılım bilinmiyorsa, parametrik istatistiksel teknikler kullanılamaz. Bu gibi durumlarda, parametrik olmayan istatistiksel teknikler mükemmel alternatiflerdir.

Parametrik olmayan istatistiksel analiz, verilerin orijinal değerleri yerine yalnızca + veya - işaretlerini veya veri boyutlarının sırasını kullanması bakımından parametrik istatistiksel analizden büyük ölçüde farklıdır. Başka bir deyişle, parametrik olmayan analiz, verinin değerinden ziyade veri boyutunun sırasına odaklanır. Örneğin, bir X değişkeni için aşağıdaki beş veriye sahip olduğumuzu farz edelim.

X1   X2   X3   X4   X5

32   47   32   18   99

Verileri büyüklük sırasına göre sıraladıktan sonra, her bir veri örneği birden beşe kadar sıralanır; en düşük değere sahip veri (18) 1\. sırada, en büyük değere (99) sahip veri ise 5\. sırada yer almaktadır. Değeri 32 olan iki veri örneği vardır ve bunlar buna göre 2.5 olarak sıralanmıştır. Ayrıca, her bir veri örneğine atanan işaretler, referans değerinden büyük değerler için + ve referans değerinden küçük değerler için - şeklindedir. Bu örnekler için 50 referans değeri atarsak, 50'den büyük yalnızca bir değer olur ve bu da bir + ve dört - işaretiyle sonuçlanır. Parametrik analiz karşılaştırılacak grupların ortalamalarındaki farka odaklanırken, parametrik olmayan analiz sıralamaya odaklanarak ortalamadan çok medyan değerlerin farklılıklarına vurgu yapar.

Yukarıda gösterildiği gibi, parametrik olmayan analiz, orijinal verileri boyut sırasına göre dönüştürür ve yalnızca sıralamayı veya işaretleri kullanır. Bu, orijinal verilerin bilgi kaybına yol açabilse de, veriler normal dağılmadığında parametrik olmayan analiz, parametrik analizden daha fazla istatistiksel güce sahiptir. Aslında, yukarıdaki örnekte gösterildiği gibi, parametrik olmayan analizin belirli bir özelliği, uç değerlerden minimum düzeyde etkilenmesidir çünkü maksimum değerin boyutu (99), 99'dan büyük olsa bile sıralamayı veya işareti etkilemez. .

## **Parametrik Olmayan İstatistiksel Analizin Avantajları ve Dezavantajları**

Parametrik olmayan istatistiksel teknikler aşağıdaki avantajlara sahiptir:

- Nüfusla ilgili varsayımlar gereksiz olduğu için yanlış sonuçlara varma olasılığı daha düşüktür. Başka bir deyişle, bu konservatif bir yöntemdir.

- Daha sezgiseldir ve fazla istatistiksel bilgi gerektirmez.

- İstatistikler, işaretlere veya sıralamalara göre hesaplanır ve bu nedenle aykırı değerlerden büyük ölçüde etkilenmez.

- Bu yöntem küçük numuneler için bile kullanılabilir.

Öte yandan, parametrik olmayan istatistiksel teknikler aşağıdaki dezavantajlarla ilişkilidir:

- Bir popülasyondaki gerçek farklılıklar, dağılım fonksiyonu ifade edilemediği için bilinemez.

- Parametrik olmayan yöntemlerden elde edilen bilgiler, parametrik yöntemlere göre daha sınırlıdır ve yorumlanması daha zordur.

- Parametrik yöntemlerle karşılaştırıldığında, yalnızca birkaç analitik yöntem vardır.

- Verilerdeki bilgiler tam olarak kullanılmamıştır.

- Büyük bir örneklem için hesaplama karmaşık hale gelir.

Özetle, parametrik olmayan analiz yöntemlerinin kullanılması, yanlış sonuçlara varma riskini azaltır çünkü bu yöntemler, popülasyon hakkında herhangi bir varsayımda bulunmaz, oysa daha düşük istatistiksel güce sahip olabilir. Başka bir deyişle, parametrik olmayan yöntemler "her zaman geçerlidir, ancak her zaman verimli değildir", parametrik yöntemler ise "her zaman etkilidir, ancak her zaman geçerli değildir". Bu nedenle, aslında kullanılabilir olduklarında parametrik yöntemler önerilir.

## **Parametrik Olmayan İstatistiksel Analiz Türleri**

Bu bölümde, bir örnek için medyan testi, iki eşleştirilmiş örneğin karşılaştırmasını, iki bağımsız örneğin karşılaştırmasını ve üç veya daha fazla örneğin karşılaştırmasını açıklayacağım. Parametrik olmayan analiz tekniklerinin türleri ve karşılık gelen parametrik analiz teknikleri,[tablo 1].

### tablo 1

**Parametik ve Parametrik Olmayan Testlerin Analogları**

<table>

<thead>

<tr>

<th></th>

<th>

**parametrik testler**

</th>

<th>

**parametrik olmayan testler**

</th>

</tr>

</thead>

<tbody>

<tr>

<td rowspan="2">

bir örnek

</td>

<td rowspan="2">

Bir örnek t testi

</td>

<td>

İşaret testi

</td>

</tr>

<tr>

<td>

Wilcoxon imzalı sıralama testi

</td>

</tr>

<tr>

<td rowspan="4">

iki örnek

</td>

<td rowspan="2">

eşleştirilmiş t testi

</td>

<td>

İşaret testi

</td>

</tr>

<tr>

<td>

Wilcoxon imzalı sıralama testi

</td>

</tr>

<tr>

<td rowspan="2">

eşleştirilmemiş t testi

</td>

<td>

Mann-Whitney testi

</td>

</tr>

<tr>

<td>

Kolmorogov-Smirnov testi

</td>

</tr>

<tr>

<td rowspan="3">

K-örnek

</td>

<td rowspan="2">

varyans analizi

</td>

<td>

Kruskal-Wallis testi

</td>

</tr>

<tr>

<td>

Jonckheer testi

</td>

</tr>

<tr>

<td>

2 yollu varyans analizi

</td>

<td>

Friedman testi

</td>

</tr>

</tbody>

</table>

### Bir örnek için medyan testi: işaret testi ve Wilcoxon'un işaretli sıralama testi

İşaret testi ve Wilcoxon'un işaretli sıralama testi, bir numunenin medyan testleri için kullanılır. Bu testler, bir örnek veri örneğinin medyandan (referans değer) daha büyük veya daha küçük olup olmadığını inceler.

### İşaret testi

İşaret testi, bir numunenin konumu ile ilgili tüm parametrik olmayan testler arasında en basit testtir. <sub>Bu test, bir popülasyonun medyanı θ 0</sub> hakkındaki hipotezi inceler ve H <sub>0</sub> : θ = θ <sub>0</sub> sıfır hipotezinin test edilmesini içerir . Gözlenen değer (X <sub>i ) referans değerden (θ 0</sub> ) büyükse + olarak işaretlenir ve gözlenen değer referans değerden küçükse - işareti verilir, bundan sonra + değerlerin sayısı hesaplanır. Numunede referans değerine eşit bir gözlenen değer varsa (θ <sub>0</sub>), söz konusu gözlemlenen değer numuneden elimine edilir. Buna göre, işaret testine devam etmek için numunenin boyutu küçültülür. + İşareti verilen örnek veri örneklerinin sayısı 'B' olarak gösterilir ve işaret istatistiği olarak anılır. Sıfır hipotezi doğruysa, + işaretlerinin sayısı ve - işaretlerin sayısı eşittir. İşaret testi, verilerin gerçek değerlerini yok sayar ve yalnızca + veya - işaretlerini kullanır. Bu nedenle, değerleri ölçmenin zor olduğu durumlarda kullanışlıdır.

### Wilcoxon imzalı sıralama testi

<sub>İşaret testinin bir dezavantajı vardır, çünkü verilen verilerin θ 0</sub> referans değeri ile karşılaştırılmasında sadece + veya - işaretleri kullanıldığından bilgi kaybına yol açabilir . <sub>Buna karşılık, Wilcoxon'un işaretli sıra testi, θ 0</sub> ile karşılaştırmalı olarak sadece gözlemlenen değerleri incelemekle kalmaz, aynı zamanda göreli boyutları da dikkate alır, böylece işaret testinin sınırlamasını hafifletir. Wilcoxon'un imzalı sıralama testi, yalnızca işaretlerin kullanılmasından kaynaklanan bilgi kaybını azaltabileceği için daha fazla istatistiksel güce sahiptir. <sub>İşaret testinde olduğu gibi, θ 0</sub> referans değerine eşit bir gözlenen değer varsa , bu gözlenen değer örneklemden çıkarılır ve buna göre örneklem büyüklüğü ayarlanır. Burada, beş veri noktasına sahip bir örnek verilmiştir (X <sub>i</sub>), da gösterildiği gibi[Tablo 2](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4754273/table/T2/), bu numunenin medyanının (θ <sub>0</sub> ) 50 olup olmadığını test ederiz.

### Tablo 2

**Bir Örnek için İşaret Testi ve Wilcoxon's Singed Rank Test Örnekleri**

<table>

<thead>

<tr>

<th></th>

<th>

**X <sub>1</sub>**

</th>

<th>

**X <sub>2</sub>**

</th>

<th>

**X <sub>3</sub>**

</th>

<th>

**X <sub>4</sub>**

</th>

<th>

**X <sub>5</sub>**

</th>

</tr>

</thead>

<tbody>

<tr>

<td>

Veri

</td>

<td>

47

</td>

<td>

55

</td>

<td>

34

</td>

<td>

26

</td>

<td>

99

</td>

</tr>

<tr>

<td>

50'ye kıyasla +/-

</td>

<td>

-

</td>

<td>

+

</td>

<td>

-

</td>

<td>

-

</td>

<td>

+

</td>

</tr>

<tr>

<td>

R <sub>ben</sub> = X <sub>ben</sub> - 50

</td>

<td>

-3

</td>

<td>

5

</td>

<td>

-16

</td>

<td>

-14

</td>

<td>

49

</td>

</tr>

<tr>

<td>

Rütbe

</td>

<td>

(1)

</td>

<td>

(2)

</td>

<td>

(4)

</td>

<td>

(3)

</td>

<td>

(5)

</td>

</tr>

</tbody>

</table>

Medyan (θ <sub>0</sub> ) 50 olsun. Orijinal veriler sıra ve işaret verilerine dönüştürüldü. +/- sırasıyla X <sub>i</sub> > 50 ve < 50 anlamına gelir. Yuvarlak parantez rütbe anlamına gelir.

Bu durumda, her bir veri noktasından (R <sub>i</sub> = X <sub>i</sub> - θ <sub>0 ) θ 0</sub> çıkarır , mutlak değeri bulur ve değerleri artan sırada sıralarsak, ortaya çıkan sıralama parantez içindeki değere eşittir.[Tablo 2]. Wilcoxon imzalı sıra testi ile aşağıdaki denkleme göre yalnızca pozitif değerlere sahip sıralar toplanır:

W <sup>+</sup> = Σ Ψ <sub>ben</sub> ·|R <sub>ben</sub> |

𝛹𝑖= {1 ( ne zamanR𝑖> 0 )0 ( ne zamanR𝑖< 0 )

## **Eşleştirilmiş bir örneğin karşılaştırılması: işaret testi ve Wilcoxon'un işaretli sıralama testi**

### İşaret testi

Daha önce açıklanan tek örneklem işaret testinde, verilen veriler medyan değerle (θ <sub>0</sub> ) karşılaştırıldı. Eşleştirilmiş bir numune için işaret testi, tedaviden önceki ve sonraki puanları karşılaştırır ve diğer her şey, tek numune işaret testinin nasıl çalıştırıldığıyla aynıdır. İşaret testi, puanların sıralamasını kullanmaz, yalnızca + veya - işaretlerin sayısını dikkate alır. Bu nedenle, aşırı uç değerlerden nadiren etkilenir. Aynı zamanda verilen verilerdeki tüm bilgileri kullanamaz. Bunun yerine, yalnızca iki örnek arasındaki farkın yönü hakkında bilgi sağlayabilir, ancak iki örnek arasındaki farkın boyutu hakkında bilgi sağlayamaz.

### Wilcoxon imzalı sıralama testi

Bu test, eşleştirilmiş bir t testinin parametrik olmayan bir yöntemidir. Bu test ile daha önce açıklanan tek örneklem testi arasındaki tek fark, tek örneklem testinin verilen verileri referans değerle (θ <sub>0</sub> ) karşılaştırması, eşleştirilmiş testin ise tedavi öncesi ve sonrası puanları karşılaştırmasıdır. Beş eşleştirilmiş veri örneğine sahip örnekte (X <sub>ij</sub> ), aşağıda gösterildiği gibi[Tablo 3], eğitim öncesi ve sonrası puanları gösterir, X <sub>1j</sub> j öğrencisinin ön puanını, X <sub>2j</sub> j öğrencisinin son puanını ifade eder. İlk olarak, eğitim öncesi ve sonrası puandaki değişimi hesaplıyoruz (R <sub>j</sub> = X <sub>1j</sub> - X <sub>2j</sub> ). R <sub>j</sub> mutlak değerlerine göre sıralandığında, ortaya çıkan sıra parantez içindeki değerlerle temsil edilir.[Tablo 3]. Wilcoxon'un işaretli sıralama testi daha sonra tek örneklem testinde olduğu gibi + işaretlerinin sayısı eklenerek gerçekleştirilir. Sıfır hipotezi doğruysa, + işaretlerinin sayısı ile - işaretlerin sayısı hemen hemen eşit olmalıdır.

### Tablo 3

**Eşleştirilmiş Numune için Wilcoxon'un Singed Rank Testi Örneği**

<table>

<thead>

<tr>

<th></th>

<th>

**x <sub>ben1</sub>**

</th>

<th>

**ben2 <sub>_</sub>**

</th>

<th>

**ben3 <sub>_</sub>**

</th>

<th>

**ben4 <sub>_</sub>**

</th>

<th>

**ben5 <sub>_</sub>**

</th>

</tr>

</thead>

<tbody>

<tr>

<td>

X <sub>1j</sub> (ön puanlar)

</td>

<td>

33

</td>

<td>

28

</td>

<td>

33

</td>

<td>

33

</td>

<td>

40

</td>

</tr>

<tr>

<td>

X <sub>2j</sub> (sonraki puanlar)

</td>

<td>

34

</td>

<td>

33

</td>

<td>

30

</td>

<td>

39

</td>

<td>

42

</td>

</tr>

<tr>

<td>

R <sub>j</sub> = X <sub>1j</sub> - X <sub>2j</sub>

</td>

<td>

-1

</td>

<td>

-5

</td>

<td>

3

</td>

<td>

-6

</td>

<td>

-2

</td>

</tr>

<tr>

<td>

Rütbe

</td>

<td>

(1)

</td>

<td>

(4)

</td>

<td>

(3)

</td>

<td>

(5)

</td>

<td>

(2)

</td>

</tr>

<tr>

<td>

W <sup>+</sup>

</td>

<td colspan="5">

= 3

</td>

</tr>

<tr>

<td>

K <sup>-</sup>

</td>

<td colspan="5">

= 12 (1 + 4 + 5 + 2 )

</td>

</tr>

</tbody>

</table>

Sıfır hipotezi altında (öncesi/sonrası puanlar arasında fark yok), test istatistikleri (W <sup>+</sup> , pozitif sıranın toplamı) 7,5'a yakın olacaktır (=∑5k= 1k2), ancak alternatif hipotez doğru olduğunda 7.5'ten uzaklaşın. Wilcoxon'un sıra toplamı testi tablosuna göre, test istatistikleri (W <sup>+</sup> ) 3 α = 0.05 (iki kuyruklu test) ve örneklem büyüklüğü = 5 olduğunda P değeri = 0.1363\. Bu nedenle sıfır hipotezi reddedilemez.

İşaret testi, eşleştirilmiş puanlar arasındaki değişimin derecesini yansıtamadığı için sınırlıdır. Wilcoxon'un işaretli sıralama testi, işaret testinden daha fazla istatistiksel güce sahiptir çünkü yalnızca değişimin yönünü dikkate almaz, aynı zamanda eşleştirilmiş puanlar arasındaki değişimin derecesini de sıralayarak analiz için daha fazla bilgi sağlar.

## **İki bağımsız örneklemin karşılaştırılması: Wilcoxon's rank sum testi, Mann-Whitney testi ve Kolmogorov-Smirnov testi**

### Wilcoxon'un sıra toplamı testi ve Mann-Whitney testi

Wilcoxon'ın sıra toplamı testi, tüm veri noktalarını sırayla sıralar, her numunenin sıra toplamını hesaplar ve sıra toplamlarındaki farkı karşılaştırır ([Tablo 4]. İki grubun benzer puanları varsa, sıra toplamları benzer olacaktır; ancak, bir grubun puanı diğer grubunkinden daha yüksek veya daha düşükse, iki grup arasındaki sıralama toplamları daha uzak olacaktır.

### Tablo 4

**Wilcoxon Sıra Toplamı Testinin Örnekleri ve Süreci**

<table>

<tbody>

<tr>

<td>

Grup X

</td>

<td>

18

</td>

<td>

21

</td>

<td>

15

</td>

<td>

30

</td>

<td>

25

</td>

<td></td>

<td></td>

<td></td>

<td></td>

</tr>

<tr>

<td>

Y Grubu

</td>

<td>

20

</td>

<td>

11

</td>

<td>

16

</td>

<td>

14

</td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

</tr>

<tr>

<td>

X ve Y grubundan veriler

</td>

<td>

11

</td>

<td>

14

</td>

<td>

15

</td>

<td>

16

</td>

<td>

18

</td>

<td>

20

</td>

<td>

21

</td>

<td>

25

</td>

<td>

30

</td>

</tr>

<tr>

<td>

Derece (grup)

</td>

<td>

1(Y)

</td>

<td>

2(E)

</td>

<td>

3(X)

</td>

<td>

4(Y)

</td>

<td>

5(X)

</td>

<td>

6(E)

</td>

<td>

7(X)

</td>

<td>

8(X)

</td>

<td>

9(X)

</td>

</tr>

<tr>

<td>

Genişlik <sub>_</sub>

</td>

<td colspan="9">

3 + 5 + 7 + 8 + 9 = 32

</td>

</tr>

<tr>

<td>

W <sub>Y</sub>

</td>

<td colspan="9">

1 + 2 + 4 + 6 = 13

</td>

</tr>

</tbody>

</table>

X (m) grubunun örneklem büyüklüğü 5 ve Y (n) grubunun 4 olduğu iki bağımsız grup vardır. Sıfır hipotezi altında (2 grup arasında fark yok), X grubunun (W <sub>X</sub> ) ve Y grubu (W <sub>Y</sub> ) 22.5'e yakın olacaktır (=∑9k= 1k2, ancak alternatif hipotez doğru olduğunda 22.5'ten uzaklaşın. <sub>Wilcoxon'ın sıra toplamı testi tablosuna göre, m = 5 ve n = 4'te α = 0.05 (iki kuyruklu test) altında test istatistikleri (W Y</sub> ) = 13 olduğunda P değeri = 0.0556 . Bu nedenle, boş hipotez olamaz reddedilmiş.

Öte yandan Mann-Whitney testi , X grubuna ait tüm x <sub>i verilerini ve Y grubuna ait tüm y i</sub> verilerini karşılaştırır ve xi'nin y'den büyük olma olasılığını hesaplar <sub>ben</sub> : P(x <sub>i</sub> > y <sub>i</sub> ) . Sıfır hipotezi P(x <sub>ben</sub> > y <sub>ben</sub> ) = P(x <sub>ben</sub> < y <sub>ben</sub> ) = ½ olduğunu belirtirken, alternatif hipotez P(x <sub>i</sub> > y <sub>ben</sub> ) ≠ ½ olduğunu belirtir. Mann-Whitney testinin süreci şu şekilde gösterilmektedir:[Tablo 5]. Mann-Whitney testi ve Wilcoxon'un sıra toplamı testi hesaplama süreçlerinde biraz farklılık gösterse de, aynı istatistikleri kullandıkları için yaygın olarak eşit yöntemler olarak kabul edilirler.

### Tablo 5

**Mann-Whitney Testi Örneği ve Süreci**

<table>

<tbody>

<tr>

<td>

Grup X

</td>

<td>

18

</td>

<td>

21

</td>

<td>

15

</td>

<td>

30

</td>

<td>

25

</td>

</tr>

<tr>

<td>

Y Grubu

</td>

<td>

20

</td>

<td>

11

</td>

<td>

16

</td>

<td>

14

</td>

<td></td>

</tr>

<tr>

<td>

X > Y sayısı

</td>

<td>

3

</td>

<td>

4

</td>

<td>

2

</td>

<td>

4

</td>

<td>

4

</td>

</tr>

<tr>

<td>

X sayısı < Y

</td>

<td>

2

</td>

<td>

0

</td>

<td>

1

</td>

<td>

0

</td>

<td></td>

</tr>

<tr>

<td>

UX <sub>_</sub>

</td>

<td colspan="5">

3 + 4 + 2 + 4 + 4 = 17

</td>

</tr>

<tr>

<td>

UY <sub>_</sub>

</td>

<td colspan="5">

2 + 0 + 1 + 0 = 3

</td>

</tr>

<tr>

<td>

sen

</td>

<td colspan="5">

Min (U <sub>X</sub> , U <sub>Y</sub> ) = 3

</td>

</tr>

</tbody>

</table>



X grubu (m) 5 ve Y grubu (n) 4 olan iki bağımsız grup vardır. Sıfır hipotezi altında (2 grup arasında fark yok), test istatistikleri (U) 10'a yaklaşır (=m × n2), ancak alternatif hipotez doğru olduğunda daha aşırı (bu örnekte daha küçük) olur. Bu verilerin test istatistiği, m = 5 ve n = 4'te α = 0.05 (iki kuyruklu test) altında 1 referans değerinden büyük olan U = 3'tür. Bu nedenle sıfır hipotezi reddedilemez.

### Kolmogorov-Smirnov testi (KS testi)

KS testi genellikle bir veri setinin normalliğini incelemek için kullanılır. Ancak, orijinal olarak, iki örneğin eşit dağılıma sahip iki popülasyondan mı yoksa aynı popülasyondan mı çıkarıldığını incelemek için iki bağımsız örneğin kümülatif dağılımlarını inceleyen bir yöntemdir. Aynı popülasyondan çıkarılmışlarsa, kümülatif dağılımlarının şekilleri eşit olacaktır. Buna karşılık, iki örnek farklı kümülatif dağılımlar gösteriyorsa, bunların farklı popülasyonlardan çıkarıldığı varsayılabilir. Örneği kullanalım[Tablo 6]Gerçek bir analiz için. İlk olarak, iki bağımsız örneği karşılaştırmak için iki örneğin dağılım modelini belirlememiz gerekir. İçinde[Tablo 6], örneklerin aralığı 43, minimum değeri 50 ve maksimum değeri 93'tür. KS testinin istatistiksel gücü, ayarlanan aralıktan etkilenir. Aralık çok genişse, az sayıda aralık nedeniyle istatistiksel güç azalabilir; benzer şekilde, aralık çok darsa, aşırı aralık sayısı nedeniyle hesaplamalar çok karmaşık hale gelir. gösterilen veriler[Tablo 6] 43 aralığına sahiptir; bu nedenle, 4'lük bir aralık aralığı oluşturacağız ve aralık sayısını 11 olarak ayarlayacağız.[Tablo 6]<sub>, her aralık (S X</sub> , S <sub>Y</sub> ) için kümülatif olasılık dağılım tablosu oluşturulmalı ve iki değişkenin kümülatif dağılımları arasındaki en büyük farka sahip değer (Max(S <sub>X</sub> - S <sub>Y</sub> )) belirlenmelidir. Bu maksimum fark, test istatistiğidir. İki numunenin homojenliğini test etmek için bu farkı referans değerle karşılaştırıyoruz. Gerçek analiz süreci şu bölümde açıklanmaktadır:[Tablo 6].

### Tablo 6

**Kolmogorov-Smirnov Testinin Örneği ve Süreci**

<table>

<thead>

<tr>

<th>

**X**

</th>

<th>

**Y**

</th>

<th>

**Aralık**

</th>

<th>

**X'in frekansı**

</th>

<th>

**S <sub>X</sub>**

</th>

<th>

**Y'nin frekansı**

</th>

<th>

**<sub>SY</sub> _**

</th>

<th>

**S <sub>X</sub> - S <sub>Y</sub>**

</th>

</tr>

</thead>

<tbody>

<tr>

<td>

53

</td>

<td>

88

</td>

<td>

50-53

</td>

<td>

3

</td>

<td>

3/15

</td>

<td>

1

</td>

<td>

1/15

</td>

<td>

2/15

</td>

</tr>

<tr>

<td>

87

</td>

<td>

84

</td>

<td>

54-57

</td>

<td>

2

</td>

<td>

5/15

</td>

<td>

0

</td>

<td>

1/15

</td>

<td>

4/15

</td>

</tr>

<tr>

<td>

71

</td>

<td>

72

</td>

<td>

58-61

</td>

<td>

1

</td>

<td>

6/15

</td>

<td>

0

</td>

<td>

1/15

</td>

<td>

5/15

</td>

</tr>

<tr>

<td>

64

</td>

<td>

91

</td>

<td>

62-65

</td>

<td>

1

</td>

<td>

7/15

</td>

<td>

0

</td>

<td>

1/15

</td>

<td>

6/15

</td>

</tr>

<tr>

<td>

78

</td>

<td>

89

</td>

<td>

66-69

</td>

<td>

3

</td>

<td>

10/15

</td>

<td>

1

</td>

<td>

2/15

</td>

<td>

8/15 (Maksimum fark)

</td>

</tr>

<tr>

<td>

66

</td>

<td>

68

</td>

<td>

70-73

</td>

<td>

1

</td>

<td>

11/15

</td>

<td>

3

</td>

<td>

5/15

</td>

<td>

6/15

</td>

</tr>

<tr>

<td>

52

</td>

<td>

73

</td>

<td>

74-77

</td>

<td>

0

</td>

<td>

11/15

</td>

<td>

1

</td>

<td>

6/15

</td>

<td>

5/15

</td>

</tr>

<tr>

<td>

54

</td>

<td>

52

</td>

<td>

78-81

</td>

<td>

1

</td>

<td>

12/15

</td>

<td>

0

</td>

<td>

6/15

</td>

<td>

6/15

</td>

</tr>

<tr>

<td>

50

</td>

<td>

71

</td>

<td>

82-85

</td>

<td>

1

</td>

<td>

13/15

</td>

<td>

2

</td>

<td>

8/15

</td>

<td>

5/15

</td>

</tr>

<tr>

<td>

91

</td>

<td>

93

</td>

<td>

86-89

</td>

<td>

1

</td>

<td>

14/15

</td>

<td>

4

</td>

<td>

12/15

</td>

<td>

2/15

</td>

</tr>

<tr>

<td>

55

</td>

<td>

87

</td>

<td>

90-93

</td>

<td>

1

</td>

<td>

15/15

</td>

<td>

3

</td>

<td>

15/15

</td>

<td>

0/15

</td>

</tr>

<tr>

<td>

86

</td>

<td>

92

</td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

</tr>

<tr>

<td>

69

</td>

<td>

76

</td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

</tr>

<tr>

<td>

82

</td>

<td>

72

</td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

</tr>

<tr>

<td>

68

</td>

<td>

86

</td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

<td></td>

</tr>

</tbody>

</table>

<sub>Grup X (N X</sub> ) ve grup Y (N <sub>Y</sub> ) 15 olan iki bağımsız grup vardır . X (S <sub>X</sub> ) ve Y (S <sub>Y</sub> ) kümülatif olasılık yoğunluğu arasındaki maksimum fark 8/15'tir. (0.533), NX = N <sub>Y</sub> = 15'te α = 0.05 (iki kuyruklu test) altında 0.467'lik reddetme değerinden daha büyüktür . Bu nedenle, X grubu ile <sub>Y</sub> grubu arasında anlamlı bir fark vardır.

## **k bağımsız örneklemin karşılaştırılması: Kruskal-Wallis testi ve Jonckheere testi**

### Kruskal-Wallis testi

Kruskal-Wallis testi, varyansı analiz etmek için kullanılan parametrik olmayan bir tekniktir. Diğer bir deyişle, üç veya daha fazla bağımsız örneklemin medyan değerlerinde farklılık olup olmadığını analiz eder. Kruskal-Wallis testi, orijinal veri değerlerini sıralaması bakımından Mann-Whitney testine benzer. Yani, örneklerden tüm veri örneklerini toplar ve bunları artan düzende sıralar. İki puan eşitse, verilecek iki sıranın ortalamasını kullanır. Sıra toplamları daha sonra hesaplanır ve Kruskal-Wallis test istatistiği (H) aşağıdaki denklem [14]uyarınca hesaplanır:

H =12N ( N + 1 )∑kj = 1(R2jnj) -3(N+1)(Rj= her numunenin sıra toplamı )

N =∑kj = 1nj(nj= her grup için örnek sayısı ,k = grup sayısı )

### Jonckheere testi

Önceki bilgiler kullanılarak bir sıralama alternatifi hipotezi kurulursa, daha büyük istatistiksel güç elde edilebilir. Bir tedavinin derecesini artırırken, bir tedavinin etkilerinin sırasını tahmin edebileceğimiz bir durumu düşünelim. Örneğin bir ağrı kesicinin etkinliğini değerlendirdiğimizde, grupları kontrol grubu, düşük doz grubu ve yüksek doz grubu olarak ayırarak etkinin doza bağlı olarak artacağını öngörebiliriz. Bu durumda sıfır hipotezi H <sub>2 , sıfır hipotezi H 1'den</sub> daha iyidir .

H <sub>0</sub> : [τ <sub>1</sub> = τ <sub>2</sub> = τ <sub>3</sub> ]

H <sub>1</sub> : [τ <sub>1</sub> , τ <sub>2</sub> , τ <sub>3</sub> hepsi eşit değil]

H <sub>2</sub> : [τ <sub>1</sub> ≤ τ <sub>2</sub> ≤ τ <sub>3</sub> , en azından kesin eşitsizlik ile]

Jonckheere testi, böyle bir sıralı alternatif hipotezi test etmek için kullanılabilen parametrik olmayan bir tekniktir [18].

Gerçek analiz süreci aşağıdaki resimde resimlerle açıklanmıştır:[Tablo 7].

### Tablo 7

**Jonckheere Testi Örneği ve Süreci**

<table>

<tbody>

<tr>

<td>

Grup X

</td>

<td></td>

<td>

9

</td>

<td>

13

</td>

<td>

14

</td>

<td>

18

</td>

<td></td>

</tr>

<tr>

<td>

Y Grubu

</td>

<td></td>

<td>

12

</td>

<td>

16

</td>

<td>

17

</td>

<td>

19

</td>

<td>

20

</td>

</tr>

<tr>

<td>

Grup Z

</td>

<td></td>

<td>

15

</td>

<td>

21

</td>

<td>

23

</td>

<td>

25

</td>

<td>

26

</td>

</tr>

<tr>

<td>

[X < Y] sayısı

</td>

<td>

(U <sub>XY</sub> = 15)

</td>

<td>

5

</td>

<td>

4

</td>

<td>

4

</td>

<td>

2

</td>

<td></td>

</tr>

<tr>

<td>

[Y < Z] sayısı

</td>

<td>

(U <sub>YZ</sub> = 21)

</td>

<td>

5

</td>

<td>

4

</td>

<td>

4

</td>

<td>

4

</td>

<td>

4

</td>

</tr>

<tr>

<td>

[X < Z] sayısı

</td>

<td>

(U <sub>XZ</sub> = 19)

</td>

<td>

5

</td>

<td>

5

</td>

<td>

5

</td>

<td>

4

</td>

<td></td>

</tr>

<tr>

<td colspan="7">

J = U <sub>XY</sub> + U <sub>YZ</sub> + U <sub>XZ</sub> + 15 + 21 + 19 = 55

</td>

</tr>

<tr>

<td colspan="7">

P (J ≥ 55) = 0,037

</td>

</tr>

</tbody>

</table>

Test istatistiği J = 55 ve P (J ≥ 55) = 0,035. Bu nedenle sıfır hipotezi (τ <sub>1</sub> = τ <sub>2</sub> = τ <sub>3</sub> ) reddedilir ve alternatif hipotez (τ <sub>1</sub> ≤ τ <sub>2</sub> ≤ τ <sub>3</sub> , en azından kesin eşitsizlikle) α = 0.05 altında kabul edilir.

## **Çözüm**

Parametrik olmayan testler ve parametrik testler: hangisini kullanmalıyız?

Bir hastalığın birden fazla tedavi yöntemi olduğu gibi istatistiksel analiz yöntemi de birden fazladır. Normallik varsayımı açıkça ihlal edildiğinde, parametrik olmayan analiz yöntemleri açıkça doğru seçimdir; ancak, parametrik tekniklere göre daha az istatistiksel güce sahip oldukları ve okuyucunun anlamasına yardımcı olan "%95 güven aralığını" hesaplamada güçlük çektikleri için küçük örneklemli vakalar için her zaman en iyi seçenek değildirler. Parametrik yöntemler bazı durumlarda anlamlı sonuçlar verirken, parametrik olmayan yöntemler bazı durumlarda daha anlamlı sonuçlar verebilir. Parametrik yöntemler seçildiğinde, araştırmacının argümanlarını en güçlü şekilde desteklemek ve okuyucunun kolay anlamalarına yardımcı olmak için hangi yöntemler seçilebilirse, araştırmacılar, gerekli varsayımların tamamının karşılandığından emin olmalıdır. Eğer durum böyle değilse parametrik olmayan yöntemler "her zaman geçerli ama her zaman verimli değil", parametrik yöntemler ise "her zaman verimli ama her zaman geçerli değil" olduğundan parametrik olmayan yöntemlerin kullanılması daha geçerlidir.

## **Referanslar**

1. Rosenbaum SH. Statistical methods in anesthesia. In: Miller RD, editor. Miller's Anesthesia. 7th ed. Philadelphia: Elsevier Inc; 2010. pp. 3075–3086. [Google Scholar]
2. Ko H, Kwak IY, Kim KW, Ham BM, Choe IH. Statistical methods in the articles of the journal of the Korean society of anesthesiologists from 1981 to 1990. Korean J Anesthesiol. 1993;26:22–27. [Google Scholar]
3. Hwang K, Lee HJ, Kim YJ, Lee SI. Statistical errors in papers in the journal of Korean society of plastic and reconstructive surgeons. J Korean Soc Plast Reconstr Surg. 2001;28:302–309. [Google Scholar]
4. Yim KH, Nahm FS, Han KA, Park SY. Analysis of statistical methods and errors in the articles published in the Korean journal of pain. Korean J Pain. 2010;23:35–41. [PMC free article] [PubMed] [Google Scholar]
5. Ahn W. Statistical methods in the articles in the Korean journal of anesthesiology published from 1994 to 1998. Korean J Anesthesiol. 2000;39:706–711. [Google Scholar]
6. Altman DG, Gore SM, Gardner MJ, Pocock SJ. Statistical guidelines for contributors to medical journals. Br Med J (Clin Res Ed) 1983;286:1489–1493. [PMC free article] [PubMed] [Google Scholar]
7. Gardner MJ, Machin D, Campbell MJ. Use of check lists in assessing the statistical content of medical studies. Br Med J (Clin Res Ed) 1986;292:810–812. [PMC free article] [PubMed] [Google Scholar]
8. Ahn YO, Lee HK. Development of a checklist for assessing the metholological and statistical validity of medical articles. Korean J Med Educ. 1991;3:19–35. [Google Scholar]
9. Lee S, Kang H. Statistical and methodological considerations for reporting RCTs in medical literature. Korean J Anesthesiol. 2015;68:106–115. [PMC free article] [PubMed] [Google Scholar]
10. Arbuthnott J. An argument for divine providence, taken from the constant regularity Observ'd in the births of both sexes. Philos Trans R Soc Lond. 1710;27:186–190. [Google Scholar]
11. Wolfowitz J. Additive partition functions and a class of statistical hypotheses. Ann Math Stat. 1942;13:247–279. [Google Scholar]
12. Wilcoxon F. Individual comparisons by ranking methods. Biom Bull. 1945;1:80–83. [Google Scholar]
13. Mann HB, Whitney DR. On a test of whether one of two random variables is stochastically larger than the other. Ann Math Stat. 1947;18:50–60. [Google Scholar]
14. Kruskal WH, Wallis WA. Use of ranks in one-criterion variance analysis. J Am Stat Assoc. 1952;47:583–621. [Google Scholar]
15. Hodges JL, Jr, Lehmann EL. The efficiency of some nonparametric competitors of the t-test. Ann Math Stat. 1956;27:324–335. [Google Scholar]
16. Chernoff H, Savage IR. Asymptotic normality and efficiency of certain nonparametric test statistics. Ann Math Stat. 1958;29:972–994. [Google Scholar]
17. Tukey JW. Bias and confidence in not-quite large samples. Ann Math Stat. 1958;29:614. [Google Scholar]
18. Jonckheere AR. A distribution-free k-sample test against ordered alternatives. Biometrika. 1954;41:133–145. [Google Scholar]