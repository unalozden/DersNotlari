SEKİZİNCİ BÖLÜM

##### *KARAR KURAMI*

## 8.1. GİRİŞ

Şimdiye kadar karar ortamının analizi için gerekli tüm bilgilerin bulunduğu,
başka bir deyişle alternatif karar seçeneklerine ilişkin sonuç değerleri ile
olayın yapısı hakkında bilinmesi gereken her şeyin bilindiği varsayılmış ve
karar problemlerinin tamamı bu varsayıma göre modellenmiştir. Bu durum
literatürde, "belirlilik durumunda karar alma" başlığı altında incelenir.
Açıklamalardan anlaşılacağı gibi, belirlilik durumu deterministik yapıya
sahiptir. Oysa, gerçek hayat problemlerinin çoğu olasılıksal yapıdadır.

Karar kuramı, karar vericiye karar alma ve karar sürecini geliştirme konularında
yol gösteren bir yaklaşımdır. Söz konusu yaklaşım, karar verilecek duruma
ilişkin bilgi miktarına göre üç başlık altında incelenir.

-   Belirlilik durumunda karar alma

-   Risk durumunda karar alma

-   Belirsizlik durumunda karar alma

Yukarıda açıklandığı gibi belirlilik durumunda, karar vericinin aralarından
seçim yapacağı karar seçeneklerine ilişkin sonuç değerleri ile olayın yapısı
hakkındaki bilgisinin eksiksiz olduğu varsayılır. Doğal olarak en iyi sonucu
verecek olan alternatif seçilir. Doğrusal programlama belirlilik durumunda karar
alma probleminin bir örneğidir. Konuya açıklık kazandırmak bakımından basit bir
doğrusal programlama problemi tanımlayalım. Bunun için beslenme gereksinmemizi
en düşük maliyetle karşılayacak besin maddeleri miktarlarını belirlemek
istediğimizi düşünelim. Besin maddelerinin birim maliyetleri (Cj) sabit sayılar
olsun. j ürünü tüketim miktarı xj, değeri bilinen bir sabit sayı olarak kabul
edildiğinde, j ürününün maliyete olan katkısı Cjxj de sabit bir sayı olur.

Risk durumunda problemin seçeneklerine ilişkin değerler ve olayın yapısı
olasılıklar ile açıklanırken, belirsizlik durumunda sonuç değerleri bir ölçüde
bilinse de olayın yapısına ilişkin olasılıklar hakkında hiçbir bilgi
edinilememektedir. Özetle, "belirlilik" ve "belirsizlik" verilerle ilgili bilgi
derecesi bakımından iki aşırı ucu temsil ederken, "risk" bu iki uç arasında
bulunur. Risk ve belirsizlik durumlarını açıklamak için beslenme problemi
örneğine dönelim. Risk durumunda maliyet katsayısı Cj sabit sayı olma özelliğini
yitirir ve kesin değeri bilinmeyen ancak, istendiğinde değeri ilgili olasılık
yoğunluk fonksiyonu cinsinden açıklanabilen bir rasgele değişken olur. Buna göre
Cj, olasılık yoğunluk fonksiyonu f(Cj) ile gösterilen bir rasgele değişken
olarak tanımlanabilir. Bu durumda, kendisine ait bir olasılık yoğunluk
fonksiyonu tanımlanmaksızın, Cj hakkında konuşmak fazla anlamlı olmaz. Bunun
sonucunda, xj’nin belirli bir değeri için j’inci değişkenin kra olan katkısı
Cjxj’de kesin değeri bilinmeyen bir rasgele değişken olur.

Belirsizlik durumunda ise, f(Cj) olasılık yoğunluk fonksiyonu bilinmez veya
belirlenemez. Ancak, bu konudaki bilgi eksikliği problem hakkında hiçbir bilgi
yoktur şeklinde yorumlanmamalıdır. Sözgelimi, karar verici Cj’nin değerlerinden
birine eşit olduğunu bilebilir ancak, bu bilgi duruma ilişkin olasılıkların
belirlenmesinde yetersiz kalır. Bu durum belirsizlik ortamında karar alma
durumudur. Karar probleminin nasıl formüle edileceği ve çözüleceği doğrudan
doğruya karar verenin problemin bileşenleri hakkındaki bilgi derecesine
bağlıdır. Bu konuyu açıklamak amacıyla beslenme problemi örneğine dönelim.
Belirlilik varsayımının geçerli olması, yani maliyetlerin (Cj, j = 1, 2, ..., n)
biliniyor olması durumunda, Z = Cjxj şeklinde tanımlanan bağıntının karar ölçütü
olarak kullanılması son derece anlamlıdır. Risk durumunda, Cj’ler sabit değerler
olmadıklarından bunlarla ilgili olasılıklar tanımlanmaksızın Z’nin karar ölçütü
olarak kullanılması fazla anlamlı olmayacaktır. Belirsizlik durumunda ise, ne
Cj’ler ne de bunlara ilişkin olasılıklar belirli olmadıklarından, Z karar ölçütü
olarak kullanılamaz. Bu basit incelemeden anlaşılacağı gibi, yetersiz veri daima
daha karmaşık karar modellerinin kullanılmasını gerektirir. Ayrıca ulaşılan
sonuçlar fazla tatminkar bulunmayabilir. Ancak, gerçek hayat problemlerinin çoğu
veri yetersizliği koşulları altında çözülmek durumunda olduklarından bundan
kaçınmak o kadar kolay değildir.

Belirlilik durumunda evrensel biçimde kabul görmüş karar alma ölçütü, kârın en
büyüklenmesi veya maliyetin en küçüklenmesi iken, belirsizlik ve risk
durumlarında karar almada değişik ölçütler söz konusu olur. Sözgelimi, risk
ortamında karar almada ortalama (beklenen) kârın en büyüklenmesi karar ölçütü
olarak kabul edilebilirse de bu ölçüt bütün durumlar için uygun olmayabilir.

## 8.2. KARAR PROBLEMLERİNİN ORTAK ÖZELLİKLERİ

Birden fazla olay ve birden fazla karar seçeneğinin (eylem biçimi, strateji)
bulunması, sistemin davranış ölçeğinin her bir stratejiye göre farklı değer
alması ve bu değerlerin bilinmemesi durumundaki bir probleme "karar problemi"
denir. Tanımdaki sistemin davranış ölçeği, strateji, olay ve diğer bazı önemli
kavramlar aşağıda açıklanmıştır.

Karar Verici: Sisteme maksadına göre hedefler koyan, bu hedeflere ulaşmak için
amaçlar, stratejiler ve taktikler tanımlayan, bu tanımlar uyarınca sistemin
davranışlarını planlayan, örgütleyen, denetleyen, sapmalar karşısında gerekli
düzenlemeyi yapan birey ya da topluluğa karar verici denir.

Strateji (Eylem Biçimi): Karar vericinin amaç veya amaçlarına ulaşmasını
sağlayacak değişik yollar veya hareket tarzlarının her birine strateji veya
eylem biçimi denir. Stratejilerin belirlenmesi ve tanımlanması karar vericinin
en önemli görevlerindendir. Stratejiler karar vericinin kontrolünde olan
faktörlerdir.

Olay (Doğal Durum): Karar vericinin davranışını etkileyen ve alabileceği
değerlerde karar vericinin hiçbir etkisi olmayan faktörlerdir. Olaylar, karar
vericinin içinde bulunduğu karar ortamını oluştururlar. Sayıları ne olursa olsun
gelecekte yalnızca bir olayın gerçekleşeceği unutulmamalıdır.

Sonuç: Her bir strateji ve olay bileşimi sonucu ortaya çıkan değerdir. Sonuç
değerlerine ödeme, yarar veya kayıp denir ve bunlar genellikle parasal değer
cinsinden açıklanır.

Risk veya belirsizlik ortamındaki bir karar probleminin matris biçiminde
gösterilmesi, problemin değerlendirilmesi ve çözülmesinde büyük kolaylıklar
sağlar. Alternatif stratejiler, olası olaylar ve sonuç değerlerinden oluşan
matrise "karar matrisi" denir. Karar matrisi kavramı son derece genel olup,
bunun yerine sonuç, kazanç, ödeme veya kâr-zarar matrisi deyimleri de
kullanılmaktadır.

**Tablo 8.1**

|          | Olay |     |     |     |     |     |
|----------|------|-----|-----|-----|-----|-----|
| Strateji | O1   | O2  | ... | Oj  | ... | On  |
| S1       | a11  | a12 | ... | a1j | ... | a1n |
| S2       | a21  | a22 | ... | a2j | ... | a2n |
| ..       | ..   | ..  | ... | ..  | ... | ..  |
| Si       | ai1  | ai2 | ... | aij | ... | ain |
| ..       | ..   | ..  | ... | ..  | ... | ..  |
| Sm       | am1  | am2 | ... | amj | ... | amn |

Tablo 8.1’de gösterildiği gibi, matrisinin satırlarını stratejiler, sütunlarını
olaylar oluşturmaktadır. Matrisin aij elemanları ise R(Si, Oj) sonuç
değerleridir. Karar matrisini iyi kavrayabilmek için basit bir örnek verilmesi
uygun olur.

**Örnek 8.1**: Bir spor malzemeleri satış mağazası yaz aylarındaki tenis şortu
istemini karşılamak amacıyla sipariş miktarını araştırmaktadır. Üretici firma,
siparişin bir kerede ve 100’lük kutular halinde verilmesini şart koşmaktadır.
Satın alma fiyatı sipariş miktarına göre değişmektedir. Sipariş miktarına göre
önerilen birim fiyatlar şöyledir.

**Tablo 8.2**

| Sipariş Miktarı  | Birim Fiyat  |
|------------------|--------------|
| 100              | 70           |
| 200              | 60           |
| 300              | 50           |

Yaz aylarında 100 TL’ye satılan şortların, bu aylar dışındaki fiyatı 35 TL’dir.
Sipariş miktarından fazla satış yapılamayacağı açıktır. İstemin
karşılanmamasının işletmeye maliyeti şort başına 5 TL’dir. Mağaza sahibi geçmiş
dönem deneyimlerinden yaz aylarındaki şort isteminin 100, 150, 200 veya 250 adet
olacağını bilmektedir. Sonuç değerlerinin kâra karşılık geldiği durumdaki karar
matrisini düzenleyiniz.

**Çözüm 8.1**: Mağaza sahibinin; 100, 200 veya 300 adet sipariş vermek gibi üç
stratejisi vardır. O1, O2, O3 ve O4 ile simgelenen olaylar sırasıyla, istemin
100, 150, 200 ve 250 adet olduğu karar ortamını açıklar. Karar matrisinin
elemanları farklı sipariş ve istem miktarı birleşimlerinin sonucu elde edilecek
kâr olarak tanımlanmıştır. Sonuç değerlerinin belirlenmesiyle ilgili olarak
sipariş miktarının 100 olduğunu düşünelim. Bu miktarda sipariş için satın alma
maliyeti, 70 TL’dir. Sipariş miktarı 100 iken istem düzeyi de 100 olursa, mağaza
sahibi şort başına 30 (= 100 - 70) TL kazanarak kârının 3000 TL olmasını sağlar.
Sipariş miktarı 100 iken istem 200 olduğunda, 100 birimlik istemin
karşılanmayacağı açıktır. Bunun maliyeti, kaçan fırsat değeri olarak 500 (= 5 x
100) TL’dir. Bu değerin, 100 adet şort satışından elde edilen kârdan
çıkartılmasıyla net kâr 2500 TL olarak hesaplanır. Bu yaklaşımla hesaplanan
değerlerin kullanılmasıyla hazırlanan karar (kâr) matrisi aşağıda gösterilmiştir

**Tablo 8.3**

| Sipariş | İstem Miktarı |       |       |       |
|---------|---------------|-------|-------|-------|
| Miktarı |  100          |  150  |  200  |  250  |
| 100     |  3000         |  2750 |  2500 |  2250 |
| 200     |  1000         |  4750 |  8000 |  7750 |
| 300     |  2000         |  5250 |  8500 | 11750 |

Karar matrisinin oluşturulmasından sonra karar alma işlemine geçilebilir. Hangi
miktarda sipariş vermenin uygun olacağı sorusunun yanıtı, karar vericinin
olaylar hakkındaki bilgi düzeyine ve seçim yapmada benimseyeceği ölçütlere
bağlıdır. Hangi olayın gerçekleşeceği kesinlikle bilindiğinde seçim yapmak son
derecede kolaydır. Sözgelimi, mağaza sahibi istemin 250 birim olacağından yüzde
yüz emin olsa, 300 adet sipariş vermeyi kararlaştırır. Çünkü bu istem miktarı
için 100 adetlik siparişle 2250 TL, 200 adet siparişle 7750 TL net kâr
sağlanırken, 300 adetlik siparişle kâr en yüksek değerine ulaşarak 11750 TL
olmaktadır.

Hangi olayın gerçekleşeceği önceden bilinmediğinde, yani belirsizlik durumunda
karar verme oldukça zordur. Belirsizlik durumunda karar alma konusu izleyen
kesimde açıklanmıştır.

## 8.3. BELİRSİZLİK DURUMUNDA KARAR ALMA

Bu kesimde, olayların gerçekleşme olasılıklarının bilinmemesi veya
belirlenememesi koşullarında ortaya çıkan belirsizlik durumunda karar alma
konusu açıklanacaktır. Belirsizlik durumunda karar vericinin değişik stratejiler
arasından seçim yapmasında esas alabileceği belli başlı ölçütler şunlardır:

1.  Laplace

2.  Minimaks (maksimin)

3.  Maksimaks (minimin)

4.  Savage

5.  Hurwicz

Uygun ölçütün seçilmesi karar ortamının yapısına, karar vericinin deneyim ve
eğilimine bağlıdır. Sözgelimi, minimaks ölçütünü seçen karar verici ile
karşılaştırıldığında, Laplace ölçütünü benimseyen karar vericinin daha iyimser
olduğu söylenebilir. Hurwicz ölçütünü benimseyen karar vericinin ise minimaks
ölçütü ile maksimaks ölçütü arasında bir denge bulmaya çalıştığı kabul edilir.
Kısaca bu ölçütler arasında seçim yapmada genel kabul görmüş bir kural yoktur.
Yukarıdaki ölçütlerden birini kullanacak olan karar vericinin zeki bir rakibinin
bulunmadığı, tek rakibinin doğa olduğu kabul edilir. Doğanın karar vericinin
kaybına yol açmayı hedefleyen bir rakip olduğunu söylemek için yeterli bilgi
olmadığı açıktır. Bununla birlikte, akıllı bir rakibin doğanın yerine geçtiği
problemlerle de karşılaşılabilir. Her iki rakibin de akıllı olduğu ve birinin
diğerine üstünlük sağlamak istediği durumlar, ileride rekabet ortamında karar
alma (oyun kuramı) başlığı altında incelenecektir.

Laplace Ölçütü: Laplace ölçütü muhtemel olayların ortaya çıkması ile ilgili
olasılıkların birbirlerine eşit olduğu ilkesine dayanır. Olayların ortaya
çıkması olasılıkları belirlenebildiğinden problem belirsizlik durumunda karar
alma problemi olmaktan çıkarak, risk durumunda karar alma problemine dönüşür.
Laplace ölçütü, olayların gerçekleşmesi olasılıklarının farklı olduğuna ilişkin
bir kanıt olmaması durumunda kullanılabilir. Anılan olasılıkların eşit kabul
edilmesi ilkesine "yetersiz sebep ilkesi" denir.

Problemde iki olay olduğunu düşünelim. Ölçüt gereği her bir olay eşit olasılıkla
gerçekleşeceğinden, her bir olayın ortaya çıkması olasılığı 1/2 olacaktır. Olay
sayısı üç olduğunda, eşit olasılıklar 1/3 olarak belirlenir. Olasılıklarla
ilgili bu açıklama, olay sayısı n olduğunda, olasılıklar (1/n)’ye eşit olur
şeklinde genelleştirilir. Olasılıkların belirlenmesinden sonra, her bir
stratejinin beklenen değerinin hesaplanması gerekir. Beklenen değerlerin
karşılaştırılarak, duruma göre en büyük veya en küçük değerli beklenen değerin
işaret ettiği stratejinin en iyi olduğuna karar verilir.

**Örnek 8.2**: Karar matrisi aşağıda tekrarlanan Örnek 8.1’deki mağaza sahibi
Laplace ölçütüne göre hangi miktarda sipariş verir?

**Tablo 8.4**

| Sipariş  | İstem Miktarı |       |       |       |
|----------|---------------|-------|-------|-------|
| Miktarı  |  100          |  150  |  200  |  250  |
| 100      |  3000         |  2750 |  2500 |  2250 |
| 200      |  1500         |  4750 |  8000 |  7750 |
| 300      |  2000         |  5250 |  8500 | 11750 |
| Olasılık |  1/4          | 1/4   |  1/4  | 1/4   |

**Çözüm 8.2**: Karar matrisinin Laplace ölçütü için düzenlenen biçimi yukarıdaki
tabloda verilmiştir. Görüldüğü gibi gerçekleşme olasılıkları eşit 4 olay vardır.
Bu eşit olasılıkların kullanılmasıyla her bir stratejinin beklenen değeri
aşağıdaki gibi hesaplanır.

E(100) = 1/4(3000) + 1/4(2750) + 1/4(2500) + 1/4(2250) = 2625 TL

E(200) = 1/4(1500) + 1/4(4750) + 1/4(8000) + 1/4(7750) = 5500 TL

E(300) = 1/4(2000) + 1/4(5250) + 1/4(8500) + 1/4(11750) = 6875 TL

Kâr söz konusu olduğundan, beklenen değerlerden en büyük (6875 TL) olanının
işaret ettiği miktarda, yani 300 birimlik sipariş verilmesi uygun olur. Bir de
sonuç değerlerinin kârdan farklı büyüklüklere karşılık gelmesi durumuna örnek
olması bakımından aşağıdaki problemi çözelim.

**Örnek 8.3**: Bir karar probleminin 4 x 4 karar matrisi aşağıdaki tabloda
gösterilmiştir. Laplace ölçütünü kullanarak **i**. Sonuç değerlerinin
kazançları, **ii**. Sonuç değerlerinin kayıpları göstermesi durumundaki en iyi
stratejileri belirleyiniz.

#### Tablo 8.5

|          | Olay |    |    |    |
|----------|------|----|----|----|
| Strateji | O1   | O2 | O3 | O4 |
| S1       | 26   | 26 | 18 | 22 |
| S2       | 22   | 34 | 30 | 18 |
| S3       | 28   | 24 | 34 | 26 |
| S4       | 22   | 30 | 28 | 20 |

**Çözüm 8.3**: Ortaya çıkması olası 4 olay vardır. Eşit olasılık ilkesine göre,
olasılıklar birbirine eşit, yani 1/4 olacaktır. Buna göre, sonuç değerleri ister
kazanç ister kayıp göstersin stratejilere karşılık gelen beklenen değerler
aşağıdaki gibi hesaplanır.

E(S1) = 1/4(26) + 1/4(26) + 1/4(18) + 1/4(22) = 23

E(S2) = 1/4(22) + 1/4(34) + 1/4(30) + 1/4(18) = 26

E(S3) = 1/4(28) + 1/4(24) + 1/4(34) + 1/4(26) = 28

E(S4) = 1/4(22) + 1/4(30) + 1/4(28) + 1/4(20) = 25

**i**. Hesaplanan değerlere göre, sonuç değerlerinin kazançlara karşılık gelmesi
durumunda en yüksek beklenen kazancı sağlayan S3 seçilecektir. **ii**. Sonuç
değerlerinin kayıpları göstermesi durumunda beklenen değerin en küçük olmasını
sağlayan S1’in seçilmesi uygun olur.

Maksimin veya Minimaks Ölçütü: Bu ölçüt yaklaşımlarında tutucu, kötümser karar
vericilerin benimsedikleri karar ölçütüdür. Bu yaklaşım, hangi strateji seçilmiş
olursa olsun daima o eylem için en kötü olan olayın gerçekleşeceği varsayımına
dayanır. Bu nedenle, her bir strateji için öncelikle o eylem için en kötü olan
olayın ortaya çıkması nedeniyle oluşan en kötü sonuç belirlenir. Bu yolla
bulunan en kötü sonuçlar arasından en iyi olanının işaret ettiği stratejinin
seçilmesiyle en iyi hareket tarzı belirlenmiş olur. Karar matrisi elemanları;
gelir, kâr, kazanç gibi büyük olması arzulanan değerlere karşılık geliyorsa
ölçüt en küçüklerin en büyüğü anlamına gelen maksimin; gider, zarar, kayıp gibi
küçük olması arzulanan değerlere karşılık geliyorsa en büyüklerin en küçüğü
anlamını ifade eden minimaks ölçütü adını alır.

**Örnek 8.4**: Maksimin (minimaks) ölçütüyle Örnek 8.3’deki karar matrisini
oluşturan sonuç değerlerinin **i**. Kazançlara, **ii**. Kayıplara karşılık
gelmeleri durumunda en iyi stratejiyi belirleyiniz.

**Çözüm 8.4**: Sonuç değerlerinin kazançlara karşılık gelmesi durumunda, satır
en küçüklerinin belirlenmesi ve bunlardan en büyük olanına karşılık gelen
stratejinin uygulamaya konması gerekir. Satır en küçük değerlerinin satır
sırasıyla; 18, 18, 24 ve 20 olduğu görülebilir. Buna göre bu değerlerden en
büyük olan 24’ün işaret ettiği üçüncü eylem (S3) maksimin ölçütüyle belirlenen
en iyi stratejidir.

Sonuç değerlerinin kayıplara karşılık gelmesi durumunda herhangi bir eylem için
en kötü olay en büyük sonuç değeri sağlayandır. Bu nedenle satır en büyüklerinin
belirlenmesi ve bunlardan en küçük olanına karşılık gelen stratejinin uygulamaya
konması gerekir. Satır en büyük değerlerinin sırasıyla; 26, 34, 34 ve 30 olduğu
görülebilir. Buna göre bu değerlerden en küçük olan 26’nın işaret ettiği S1,
minimaks ölçütüyle belirlenecek en iyi stratejidir.

Maksimaks veya Minimin Ölçütü: Bu ölçüte göre hangi strateji seçilirse seçilsin
o strateji için en iyi olan olayın gerçekleşeceği düşünülür. Bu düşüncenin ürünü
olarak belirlenen en iyi sonuçlardan en iyi olanının işaret ettiği strateji,
karar vericinin en iyi seçimi olur. Karar matrisi elemanlarının büyük olması
arzulanan değerlere karşılık gelmesi durumunda ölçüt maksimaks (en büyüklerin en
büyüğü) ölçütüdür. Matris elemanlarının küçük olması arzulanan değerlere
karşılık gelmesi durumunda ölçüt minimin (en küçüklerin en küçüğü) ölçütü adını
alır. Bu ölçütün kullanılmasıyla en iyi stratejinin belirlenmesini aşağıdaki
örnek yardımıyla açıklayalım.

**Örnek 8.5**: Tablo 8.5’deki karar matrisini kullanarak, maksimaks (minimin)
ölçütüyle sırasıyla, sonuç değerlerinin kazançlara ve sonuç değerlerinin
kayıplara karşılık gelmeleri durumunda en iyi stratejiyi belirleyiniz.

**Çözüm 8.5**: Bu ölçüte göre hangi eylem uygulanırsa uygulansın çeşitli olaylar
arasından en iyi olanı ile karşılaşılacağından; karar matrisi elemanlarının
kazanç değerlerine karşılık gelmesi durumunda satır en büyüklerinin, karar
matrisi elemanlarının kayıp değerlerine karşılık gelmesi durumunda satır en
küçüklerinin bulunması gerekir.

Tablo 8.5’in satır en büyükleri ile satır en küçükleri Tablo 8.6’nın enb ve enk
sütun başlıkları altında gösterilmişlerdir. Bu ölçüte göre stratejiler arasından
seçim, en iyilerin en iyisinin seçilmesi biçiminde yapılacağından, kazanç
durumunda en iyi seçenek karar vericiye 34 birim kazanç sağlayan S2 ve S3
seçenekleridir. En küçüklerin dikkate alınması durumunda en iyi seçenekler en
düşük kaybı sağlayacak olan S1 ve S2 seçenekleridir.

**Tablo 8.6**

| Strateji | Enb   | Enk   |
|----------|-------|-------|
| S1       | 26    | 18\*  |
| S2       |  34\* |  18\* |
| S3       |  34\* |  26   |
| S4       | 30    |  22   |

Savage Ölçütü: Bu ölçüt en büyük fırsat kaybının en küçüklenmesi esasına
dayanır. Bu nedenle minimaks fırsat kaybı ölçütü olarak da bilinir. Ölçütün
uygulanması için öncelikle fırsat kaybı veya pişmanlık matrisinin oluşturulması
gerekir. Fırsat kaybı matrisinin oluşturulmasına geçmeden önce fırsat kaybı
kavramı üzerinde duralım.

Fırsat kaybı her bir olay için en iyi sonucu sağlayacak stratejibnin
uygulanmaması sonucu vazgeçilen kazanç veya katlanılan kayıp miktarıdır. Fırsat
kayıpları genellikle pozitif değerler ve rakamlarla açıklanır. Karar tablosu
gelirler cinsinden ifade edildiğinde, ele alınan her bir olaya ilişkin fırsat
kaybı değerleri; en iyi olan eylemin seçilmesi durumunda sağlanacak olan
gelirden diğer seçeneklerin sağlayacağı gelirlerin çıkartılmasıyla
hesaplanırlar. Karar matrisinin maliyetleri göstermesi durumunda fırsat kaybı
değerleri en iyi seçimin maliyet değerinin diğer eylemlerin maliyet
rakamlarından çıkartılması ile belirlenirler. Bu ölçüt ile strateji seçimini
aşağıdaki örnek yardımıyla açıklayalım.

**Örnek 8.6**: Örnek 8.3-8.5’deki 4 x 4 karar matrisi, izleme kolaylığı sağlamak
bakımından, aşağıda tekrarlanmıştır. Savage ölçütüyle sırasıyla; sonuç
değerlerinin kazançlara ve sonuç değerlerinin kayıplara karşılık gelmeleri
durumunda en iyi stratejiyi belirleyiniz.

**Tablo 8.7**

|          | Olay |      |     |     |
|----------|------|------|-----|-----|
| Strateji | O1   | O2   | O3  | O4  |
| S1       | 26   |  26  |  18 |  22 |
| S2       |  22  |  34  |  30 |  18 |
| S3       |  28  |  24  |  34 |  26 |
| S4       |  22  |  30  |  28 |  20 |

**Çözüm 8.6**: Savage ölçütünün kullanılabilmesi için fırsat kaybı matrisi
düzenlenmelidir. Önce, karar matrisi elemanlarının kazançları gösterdiğini
düşünelim. Buna göre, ortaya çıkan olay O1 ise, en yüksek kazancı sağlayan S3
seçilmelidir. Bu durumda karar verici en yüksek kazancı sağlayacağından hiçbir
fırsatı kaçırmayacaktır. Buna göre bu seçimin fırsat kaybı, 28 - 28 = 0 olur.
Aynı olay (O1) için en yüksek kazancı sağlayan S3 yerine S1 seçilirse, 28 yerine
26 TL, yani 2 TL daha az kazanılacak böylece karar verici kaçırdığı 2 TL için
pişmanlık duyacaktır. S2 seçildiğinde, S3’ün seçilmemiş olması yüzünden, kaçan
fırsat 6 TL olacak bu kez karar verici 6 TL daha az kazanmanın pişmanlığını
duyacaktır. Bu işlemin karar matrisinin tüm elemanlarına uygulanması sonucu
belirlenen fırsat kaybı değerleriyle düzenlenen fırsat kaybı matrisi satır en
büyük değerleriyle birlikte aşağıda gösterilmiştir.

**Tablo 8.8**

|          | Olay | Satır |     |    |            |
|----------|------|-------|-----|----|------------|
| Strateji | O1   | O2    | O3  | O4 | En Büyüğü  |
| S1       | 2    |  8    |  16 |  4 |  16        |
| S2       | 6    |  0    |  4  |  8 |  8         |
| S3       | 0    | 10    |  0  |  0 |  10        |
| S4       | 6    |  4    |  6  |  6 |  6\*       |

Fırsat kaybı matrisinin düzenlenmesinden sonra sıra, her bir stratejiye ilişkin
en yüksek fırsat kaybının saptanmasına gelir. En yüksek fırsat kayıpları, fırsat
kaybı matrisinin en sağına eklenen sütunda gösterilmişlerdir. Karar vericinin
amacı fırsat kaybını en düşük düzeyde tutmak olduğundan en büyük pişmanlıklar
arasından en küçük olanının işaret ettiği stratejinin seçilmesiyle en iyi
hareket biçimi belirlenmiş olur. Savage ölçütüne göre en küçük değeri veren S4
seçilmelidir.

Sonuç değerlerinin kayıplara karşılık gelmesi durumunda, her bir olay için en
iyi strateji en düşük kaybı sağlayandır. Bu durumda her bir olay için kaybın en
küçük değeri dikkate alınacak ve fırsat kaybı matrisi elemanları her bir olay
için en iyi olan değerin diğer değerlerden çıkartılmasıyla belirlenecektir. Bunu
karar matrisinin ilk sütununa uygulayalım. O1 gerçekleştiğinde, en iyi strateji
22 TL’lik kayıp gösteren S2 ve S4 seçenekleridir. Bu seçeneklerin fırsat
kayıpları sıfırdır. O1 gerçekleştiğinde S1’in fırsat kaybı 26 - 22 = 4, S3’ün
fırsat kaybı 28 - 22 = 6 TL olur. Bu yaklaşımla oluşturulan fırsat kaybı matrisi
aşağıda gösterilmiştir.

**Tablo 8.9**

|          | Olay | Satır |    |    |           |
|----------|------|-------|----|----|-----------|
| Strateji | O1   | O2    | O3 | O4 | En Küçüğü |
| S1       | 4    |  2    |  0 | 4  |  4\*      |
| S2       | 0    | 10    | 12 | 0  | 12        |
| S3       | 6    |  0    | 16 | 8  | 16        |
| S4       | 0    | 6     | 10 | 2  | 16        |

Pişmanlık matrisinin düzenlenmesinin ardından her bir strateji için en büyük
fırsat kaybı belirlenir. En büyük fırsat kayıpları, önceden olduğu gibi, fırsat
kayıpları matrisinin en sağına eklenen sütunda gösterilmiştir. Savage kuralına
göre en büyük kayıplardan en küçük değerli olanının işaret ettiği S1 stratejisi
en iyi hareket biçimidir. Savage ölçütü maliyet verilerinden oluşan orijinal
matrise minimaks ölçütünün, kazanç verilerinden oluşan orijinal matrise maksimin
ölçütünün uygulanmasına benzer. Bununla birlikte benimsenecek eylemlerin aynı
olmak zorunda olmadıkları unutulmamalıdır.

Hurwicz Ölçütü: Hurwicz’e göre, karar vericinin ne aşırı derecede iyimser, ne de
aşırı derecede kötümser olmasını gerektiren güçlü gerekçeleri yoktur. Bu
nedenle, karar vericinin maksimin ölçütünün aşırı kötümserliği ile maksimaks
ölçütünün aşırı iyimserliği arasında bir denge kurması uygun olur. Bu nedenle bu
ölçüte "ağırlıklı ortalama" veya "gerçekçilik ölçütü" de denir. Hurwicz ölçütü,
seçilen her strateji için iyimserlik koşullarında ortaya çıkan sonuçlar ile
kötümserlik koşullarında ortaya çıkan sonuçların ağırlıklandırılması esasına
dayanır. Bunun için iyimserlik katsayısı olarak bilinen kullanılır. sıfır ile 1
arasında değişir. Çok kötümser bir karar vericinin için seçeceği değer sıfır,
aşırı derecede iyimser bir karar vericinin seçeceği değer 1 olur. ’nın değeri
karar vericinin iyimserlik derecesine göre değişir. Karar verici ’nın değeri
hakkında kararsızsa, = 0.5 seçmesi akılcı olur. Yukarıdaki açıklamaların ortaya
koyduğu gibi, Hurwicz ölçütünün karar verme kuralı olarak kullanılabilmesi için
öncelikle ’nın belirlenmesi gerekir. ’nın belirlenmesinden sonra karar
matrisindeki her bir strateji için en iyi ve en kötü sonuç değerlerinin
sırasıyla ve (1 - ) ile çarpılarak sonuçların toplanması gerekir. Toplama
işlemiyle belirlenen değerler stratejilerin beklenen değerleri olarak yorumlanır
ve beklenen değerler taranarak; karar matrisi kazanç değerlerinden oluşmuşsa en
büyük, maliyet değerlerinden oluşmuşsa en küçük beklenen değere sahip
stratejinin uygulanması önerilir.

Değişik ölçütlerle belirlenmiş olan strateji seçimlerinin kararlaştırılmasını
sağlamak için önceki örneklerde kullanılan karar matrisini ele alalım.

**Örnek 8.7**: Tablo 8.7’deki karar (kazanç) matrisine Hurwicz ölçütünü
uygulayarak sırasıyla ; = 0, = 1 ve = 0.6 için en iyi stratejiyi belirleyiniz*.*

**Çözüm 8.7**: = 0 seçildiğinde her strateji için yalnızca en küçük değerli
sonuçların dikkate alındığı görülebilir. Kural gereği bu en küçük değerlerden en
büyük olanı seçileceğinden, = 0 için Hurwicz ölçütü maksimin ölçütüne
eşdeğerdir. Buna göre, = 0 için S3 (bkz. Örnek 8.4) seçilecektir.

= 1 seçildiğinde, her eylem seçeneği için yalnızca en büyük değerli sonuçların
dikkate alındığı görülebilir. Kural gereği, en büyük değerlerden en büyük
olanının seçilmesi gerektiğinden = 1 için, Hurwicz ölçütü maksimaks ölçütüne
eşdeğerdir (bkz. Örnek 8.5). Buna göre, satır en büyük değerlerinden en büyüğünü
sağlayan S2 ya da S3 seçilecektir.

= 0.6 seçildiğinde, stratejilerin beklenen değerleri satır en büyüklerinin 0.6,
satır en küçüklerinin 0.4 ile çarpımlarının toplamı olarak Tablo 8.10’daki gibi
hesaplanacaklardır.

**Tablo 8.10**

|          | Kazanç İçin | Beklenen |          |
|----------|-------------|----------|----------|
| Strateji | Enb         | Enk      | Kazanç   |
| S1       | 26          | 18       | 22.8     |
| S2       | 34          | 18       | 27.6     |
| S3       | 34          | 24       |  30.0\*  |
| S4       | 30          | 20       | 26.0     |

Karar verici en yüksek beklenen kazancı hedeflediğinden, S3’ü seçecektir. Karar
matrisi elemanlarının kayıplara karşılık gelmesi durumunda stratejilerin
beklenen değerleri satır en küçüklerinin 0.6, satır en büyüklerinin 0.4 ile
çarpımlarının toplamı olarak hesaplanacaklardır.

Hesap sonuçları, Tablo 8.11’de beklenen kayıp başlıklı sütunda gösterilmiştir.
Buna göre beklenen kaybın en küçük olmasını sağlayan S1 benimsenecektir.

**Tablo 8.11**

|          | Kayıp İçin | Beklenen |         |
|----------|------------|----------|---------|
| Strateji | Enb        | Enk      | Kayıp   |
| S1       | 18         | 26       |  21.2\* |
| S2       | 18         | 34       | 24.4    |
| S3       | 24         | 34       | 28.0    |
| S4       | 20         | 30       | 24.0    |

## 8.4. RİSK DURUMUNDA KARAR ALMA

Daha önce açıklandığı gibi olayların gerçekleşme olasılıklarının bilinmesi
durumundaki karar problemi, risk durumunda karar problemidir. Risk durumunda
karar almada kullanılan başlıca ölçütler şunlardır:

1.  En yüksek olabilirlik

2.  Beklenen değer

3.  Beklenen fırsat kaybı veya beklenen pişmanlık

En Yüksek Olabilirlik Ölçütü: Bu ölçüte göre karar verici tüm dikkatini
olabilirliği en yüksek olan olay üzerinde yoğunlaştırır. Gerçekleşme olasılığı
en büyük olan olayın belirlenmesinden sonra bu olay için en yüksek (en büyükleme
durumunda en büyük, en küçükleme durumunda en küçük) sonucu sağlayan stratejinin
uygulanmasına karar verilir.

**Örnek 8.8**: En yüksek olabilirlik ölçütünü Tablo 8.12’deki kazanç matrisine
uygulayarak en iyi stratejiyi kararlaştırınız. Olayların gerçekleşmesi
olasılıkları aynı tablonun son satırında verilmiştir.

**Tablo 8.12**

|          | Olay |     |      |      |
|----------|------|-----|------|------|
| Strateji | O1   | O2  | O3   | O4   |
| S1       | 26   | 26  | 18   | 22   |
| S2       | 22   | 34  | 30   | 18   |
| S3       | 28   | 24  | 34   | 26   |
| S4       | 22   | 30  | 28   | 20   |
| Olasılık | 0.2  | 0.5 |  0.2 |  0.1 |

**Çözüm 8.8**: Tablo 8.12’nin son satırında görüldüğü gibi olabilirliği en
yüksek olay O2’dir. Karar verici gelecekte O2’nin gerçekleşeceğini düşünerek
kendisine en yüksek kazancı sağlayacak olan S2 stratejisini uygulayacaktır.

Bu kural özellikle mümkün olaylardan birine ilişkin olasılık diğer olaylara
ilişkin olasılıklardan önemli derecede büyükse uygundur. Diğer olayları ve
bunların sonuçlarını göz ardı etmesi ölçütün zayıf tarafıdır.

Beklenen Değer Ölçütü: Beklenen değer ölçütü olayların ortaya çıkması
olasılıklarının bilinmesi durumunda, her bir stratejiye ilişkin beklenen değerin
hesaplanarak bunlar arasından en iyi olanın işaret ettiği stratejinin seçilmesi
esasına dayanır.

Beklenen değer ölçütü kuralını aynı açıklayıcı örnek probleme uygulayalım.

**Örnek 8.9**: Beklenen değer kuralını Tablo 8.12’deki 4 x 4 kazanç matrisine
uygulayınız.

**Çözüm 8.9**: Olayların gerçekleşmesi olasılıkları sırasıyla; 0.2, 0.5, 0.2, ve
0.1 olarak verildiğinden stratejilerin beklenen değerleri aşağıdaki gibi
hesaplanır.

S1 için = 0.2(26) + 0.5(26) + 0.2(18) + 0.1(22) = 24.0

S2 için = 0.2(22) + 0.5(34) + 0.2(30) + 0.1(18) = 29.2

S3 için = 0.2(28) + 0.5(24) + 0.2(34) + 0.1(26) = 27.0

S4 için = 0.2(22) + 0.5(30) + 0.2(28) + 0.1(20) = 27.0

En yüksek beklenen kazancı S2 seçeneği sağladığından, karar vericinin en iyi
kararı S2’yi seçmek olacaktır. Sonuç değerleri kayıp değerlerine karşılık gelse
idi karar verici en küçük beklenen değerli S1’i seçerdi.

Beklenen Fırsat Kaybı veya Beklenen Pişmanlık Ölçütü: Risk durumunda karar
almada kullanılabilecek diğer bir ölçüt beklenen fırsat kaybı veya beklenen
pişmanlık ölçütüdür. Bu ölçütün beklenen değer ölçütünden çok farklı olmadığı
görülebilir. İki ölçüt arasındaki tek fark, dikkate aldıkları sonuç
değerleridir. Fırsat kaybı sonuçlarının dikkate alınması durumunda beklenen
değer ölçütü beklenen fırsat kaybı ölçütü adını alır.

Beklenen fırsat kaybı ile beklenen değer ölçütleri arasındaki benzerliği
görebilmek için beklenen fırsat kaybı ölçütünü aynı örnek probleme uygulayalım.

**Örnek 8.10**: Tablo 8.12’deki karar (kazanç) matrisine beklenen fırsat kaybı
ölçütünü uygulayarak karar vericinin en iyi stratejisini belirleyiniz.

**Çözüm 8.10**: Beklenen fırsat kaybı ölçütünde fırsat kayıpları esas
alındığından önce fırsat kayıpları matrisinin düzenlenmesi gerekir. Daha önce
açıklandığı gibi orijinal karar matrisinin kazanç değerlerinden oluşması
durumunda, fırsat kaybı matrisi, orijinal matrisin sütun değerlerinin her
birinin, sütun en büyük değerinden çıkartılmasıyla aşağıdaki gibi
düzenlenecektir.

**Tablo 8.13**

|          | Olay |     |     |     |
|----------|------|-----|-----|-----|
| Strateji | O1   | O2  | O3  | O4  |
| S1       | 2    |  8  | 16  | 4   |
| S2       | 6    |  0  |  4  | 8   |
| S3       | 0    | 10  | 0   | 0   |
| S4       | 6    |  4  | 6   | 6   |
| Olasılık | 0.2  | 0.5 | 0.2 | 0.1 |

Fırsat kaybı matrisinin oluşturulmasından sonra olayların gerçekleşmesi
olasılıklarından yararlanarak her bir eylem için beklenen fırsat kaybı değerleri
hesaplanmalıdır. Söz konusu değerler aşağıdaki gibi hesaplanacaktır.

S1 için = 0.2(2) + 0.5(8) + 0.2(16) + 0.1(4) = 8.0

S2 için = 0.2(6) + 0.5(0) + 0.2(4) + 0.1(8) = 2.8

S3 için = 0.2(0) + 0.5(14) + 0.2(0) + 0.1(6) = 5.0

S4 için = 0.2(6) + 0.5(4) + 0.2(6) + 0.1(6) = 5.0

Sonuçta, beklenen fırsat kaybı ölçütüne göre en iyi strateji en küçük beklenen
fırsat kaybı değerini veren S2 olacaktır. Bu ölçütle en iyi olduğu
kararlaştırılan S2’nin daha önce beklenen değer ölçütüyle en iyi olduğu
belirlenen strateji olduğuna dikkat edilmelidir.

Tam Bilginin Beklenen Değeri: Karar problemlerinin çoğunda, ön bilgilerle
yetinilip yetinilmemesi konusu kararsızlığa neden olmaktadır. Daha fazla bilgiye
sahip olunduğunda belirsizlik azalacağından, alınan karara duyulan güven
artacaktır. Ancak, daha fazla bilgi sağlamak için yapılan örnekleme, test ve
çeşitli deneylerin bir maliyeti olacağı unutulmamalıdır. Bu nedenle ek bilgi
sağlamak için katlanılması gereken maliyetin katlanmaya değer olup olmadığının
araştırılması gerekir. Bunun için tam bilgiden beklenen gelirle başka bir
deyişle, tam bilginin beklenen değeriyle ek bilgiye ulaşmanın yaratacağı
maliyetin karşılaştırılması uygun olur. Tam bilgi fayda sağlıyor ise tam bilgiye
başvurmak, aksi halde eldeki bilgilerle yetinmek akılcı bir yaklaşım olur. Tam
bilginin beklenen değeri kavramını açıklayıcı örnek problem üzerinde gösterelim.

**Örnek 8.11**: Örnek 8.1’deki mağaza sahibinin tam bilgi durumundaki beklenen
kârını hesaplayarak, tam bilgi altında kârdaki artışı bulunuz.

**Tablo 8.14**

| Sipariş  | İstem Miktarı |      |      |       |
|----------|---------------|------|------|-------|
| Miktarı  | 100           | 150  | 200  | 250   |
| 100      | 3000          | 2750 | 2500 |  2250 |
| 200      | 1500          | 4750 | 8000 |  7750 |
| 300      | 2000          | 5250 | 8500 | 11750 |
| Olasılık | 0.2           | 0.3  | 0.3  | 0.2   |

**Çözüm 8.11**: İstem miktarı kesin olarak bilindiğinde, en iyi sipariş miktarı
da aynı kesinlikle kolayca belirlenebilir. Sözgelimi, istemin 100 adet
olacağından emin olunsa, 100 adet siparişle kazancın en büyük olması sağlanır.
İstemin 100 adet olması olasılığı 0.2 olduğundan, 100 birimlik istem için
beklenen kazanç şöyle olur:

0.2 x 3000 = 600 TL

Benzer şekilde istemin 150 olması durumunda en yüksek kâr 300 adet siparişle
sağlanır. Bu olay-strateji çifti için en yüksek kazanç 5250 TL olduğundan
beklenen kâr bu olayın gerçekleşme olasılığı (0.3) ile 5250’nin çarpılmasıyla
1575 TL olarak hesaplanır. Benzer işlemlerle istemin 200 ve 250 adet olması
durumları için beklenen kârlar sırasıyla aşağıdaki gibi hesaplanır.

0.3 x 8500 = 2550 TL

0.2 x 11750 = 2350 TL

Tam bilgi altında beklenen kâr her bir olay için en iyi stratejinin seçilmesi
sonucu gerçekleşen beklenen kazançların toplamına eşittir. Buna göre tam bilgi
altındaki beklenen kazanç (TBABK) aşağıdaki gibi elde edilir.

TBABK = 0.2(3000) + 0.3(5250) + 0.3(8500) + 0.2(11750)

= 7075 TL

Tam bilgi altında hesaplanan 7075 TL’lik kazanç istemin değeri hakkında kesin
bilgiye sahip olunması durumunda kazanılacak en yüksek miktardır. Bu yolla hangi
stratejinin uygun olacağı konusunda bir öneride bulunulmadığına dikkat
edilmelidir. Burada saptanan yalnızca belirlilik durumunda kârın en fazla 7075
TL olabileceğidir. Kârı bu düzeye çıkarmak için istem miktarlarının olasılıkları
hakkında daha fazla bilgi edinmek istendiğini düşünelim. Bu durumda, ek bilginin
kârda sağlayacağı artış ile gerçekleştirilmesi düşünülen çalışmanın maliyeti
karşılaştırılmalıdır. Ek bilgiyle sağlanacak kâr ek bilgiye ulaşma maliyetinden
fazla ise ek bilgiye başvurulacak aksi halde, eldeki veri ile yetinilerek risk
ortamında beklenen değer ölçütüyle karar verme benimsenecektir. Ek bilginin
beklenen değeri, tam bilgi altındaki beklenen değer ile risk durumundaki
beklenen değer arasındaki farka eşittir.

Risk durumunda en yüksek kâr 6875 TL’dir. Tam bilgi altında en yüksek kâr 7075
TL olduğundan ek bilginin beklenen değeri aşağıdaki gibi hesaplanır.

Ek Bilginin Beklenen Değeri = 7075 - 6875 = 200 TL

Bu değer tam bilgi durumunda kârdaki artışı gösterir. Buna göre ek bilgi
sağlamak için yapılacak çalışmanın maliyeti 200 TL’den fazlaysa mağaza sahibinin
ek bilgi sağlamaktan vazgeçmesi uygun olur. Açıklamalarımız için gerekli
olduğundan problemi bir de beklenen fırsat kaybı ölçütünü kullanarak çözelim.
Problemin fırsat kaybı tablosu aşağıda gösterilmiştir.

**Tablo 8.15**

|          | Olay | Beklenen |      |      |              |
|----------|------|----------|------|------|--------------|
| Strateji | O1   | O2       | O3   | O4   | Fırsat Kaybı |
| S1       | 0    | 2500     | 6000 | 9500 | 4450         |
|  S2      | 1500 | 500      | 500  | 4000 | 1400         |
|  S3      | 1000 | 0        | 0    | 0    |  200         |
| Olasılık | 0.2  | 0.3      | 0.3  | 0.2  | -            |

Hesaplanan beklenen fırsat kayıpları, fırsat kayıpları tablosuna eklenen
"Beklenen Fırsat Kaybı" başlıklı sütunda gösterilmiştir. Görüldüğü gibi en küçük
beklenen fırsat kaybı ek bilginin beklenen değerine eşittir. Bu durum yalnızca
bu problem için değil her zaman böyledir. En küçük beklenen fırsat kaybı
belirsizliğin maliyeti olarak değerlendirilir. Her bir strateji için beklenen kr
ile beklenen pişmanlık değerleri toplamının, tam bilginin beklenen değerine eşit
olduğu gösterilebilir. Bu durumun açıklanmasına örnek olması için S1’i
inceleyelim. S1 için beklenen kr olan 2625 TL ile S1 için beklenen fırsat kaybı
4450 TL’nin toplamı 7075 TL’ye eşittir.

# 8.5. KARAR AĞACI ANALİZİ

Şimdiye kadar, sonuçların matris veya tablo biçiminde gösterilmesinin mümkün
olduğu "bir olaylar kümesi-bir strateji seçimi"olarak özetlenebilecek durumların
karar problemleri incelenmiştir. Oysa karar verme genellikle, birden fazla
olaylar kümesinin bulunduğu, her küme için bir eylem seçiminin söz konusu olduğu
çok aşamalı bir süreçtir. Bu, birden fazla noktada karar verme durumunda olmak
demektir. Bu tip problemlerin matris veya tablo yaklaşımıyla çözülmesi doğru
değildir. Matris yerine karar ağacı oluşturulması uygun olur.

Karar Ağacı: İlk olay veya stratejiyle son sonuçlara ulaşılma aşamasına kadar
ortaya çıkan tüm olay ve eylemlerin tarih sırasına göre düzenlenmesiyle oluşan
bir grafiktir. Grafik ağaca benzediğinden "ağaç grafiği" vaya "karar ağacı"
denir. Özünde bir grafik olduğundan karar ağacı düğümler ve çizgilerden oluşan
bir kümedir.

Karar vericinin karar aldığı her bir nokta karar noktası olup karar noktaları
ağaç üzerinde bir kare ile gösterilir. Bu kareden çıkan dallar karar vericinin
stratejilerine karşılık gelir. Karar vericinin kontrolü dışında olan olaylar
ağaç üzerinde dairelerle gösterilirler. Bu noktalara "olay düğüm noktası" veya
"şans noktası" denir. Daire biçimindeki olay düğüm noktalarından çıkan her dal,
bir olayı simgeler. Olayı simgeleyen sembol ve olayın ortaya çıkma olasılığı ait
olduğu dal üzerinde gösterilir. Şans noktasından çıkan dallar, karar vericiyi
bir başka şans noktasına veya bir karar noktasına götürebilir.

Karar probleminin karar ağacı ile çözümünde, dinamik programlamada[^1] olduğu
gibi, sondan başa doğru hesaplama yaklaşımı uygulanır. Bunun için oluşturulan
karar ağacının en son aşamasındaki uç noktalardan başlanır ve ağaç üzerinde başa
doğru gidilir. Bu ilerleyiş sırasında karşılaşılan karar noktalarının her
birinde o düğümün beklenen değeri hesaplanır. Beklenen değerlerden en iyi olanı
o düğümün üzerine yazılır. Başlangıç noktasına ulaşıldığında çözüm işlemi
tamamlanmış olur.

[^1]: Bkz. Onbirinci Bölüm.

Karar ağacı yaklaşımını sipariş miktarının belirlenmesiyle ilgili örnek probleme
uygulayalım.

**Örnek 8.12**: Örnek 8.1’deki problemin karar ağacını düzenleyerek net krı en
büyükleyen sipariş miktarını bulunuz.

**Çözüm 8.12**: Problemi karar ağacı yaklaşımıyla çözebilmek için öncelikle
karar ağacı oluşturulmalıdır. Karar ağacının düzenlenebilmesi için önce karar
noktası sayısı belirlenir. Bilindiği gibi mağaza sahibinin sipariş miktarını
belirlemek gibi tek bir sorunu, yani almak istediği tek bir karar vardır. Bu
nedenle karar noktası tektir. Bu nokta K ile işaretlenecektir. Sipariş miktarı
için 100, 200 veya 300 olmak üzere 3 seçenek bulunduğundan bu noktadan 3 dal
çıkacaktır. Karar ağacının bu kısmı aşağıda gösterilmiştir.

**Şekil 8.1**

Bir an için sipariş miktarının 100 olarak belirlendiğini düşünelim. İstem düzeyi
100, 150, 200 veya 250 olabilir. İstem düzeyindeki bu belirsizlik olay düğüm
noktası olarak işaretlenir. Olay düğüm noktasından olay sayısı kadar dal çıkacak
ve dalların her biri ayrı bir istem düzeyine karşılık gelecektir. Olaylara
ilişkin olasılıkların ait oldukları dallar üzerinde, olaylara ilişkin kârların
dalların uç noktalarında gösterilmesiyle karar ağacının 100 birimlik sipariş
verilmesi durumunu açıklayan kısmı aşağıdaki gibi belirlenmiş olur.

**Şekil 8.2**

Dallardan geriye doğru giderek 1 nolu düğüm noktasındaki beklenen kârı (BK1)
hesaplayalım.

BK1 = 3000(0.2) + 2750(0.3) + 2500(0.3) + 2250(0.2)

= 2625 TL

Saptanan 2625 TL tutarındaki beklenen kâr 1 nolu olay düğüm noktasının üzerine
yazılır.

Aynı yöntemle 200 ve 300 birimlik sipariş miktarları için 2 ve 3 nolu olay düğüm
noktalarındaki beklenen kârlar aşağıdaki gibi hesaplanır.

BK2 = 1500(0.2) + 4750(0.3) + 8000(0.3) + 7750(0.2) = 5675 TL

BK3 = 2000(0.2) + 5250(0.3) + 8500(0.3) + 11750(0.2) = 6875 TL

Beklenen kârların O2 ve O3 noktalarına yazılmasıyla karar ağacı aşağıdaki gibi
tamamlanmış olur.

**Şekil 8.3**

Her bir olay düğüm noktasının beklenen değerleri hesaplandıktan sonra K ile
simgelenen karar noktasına ulaşırız. Bu nokta; sipariş miktarının 100, 200 veya
300 olması eylemlerinden birinin seçilmesi durumunu gösterir. 300 dalı 100 ve
200 dallarından daha fazla kâr sağladığından mağaza sahibi 100 ve 200 dallarını
değil, 300 dalını seçecektir. Seçilmeyen dallar "//" ile işaretlenir.

Daha önce değindiğimiz gibi karar ağacı yaklaşımı, özellikle birden fazla
noktada karar almanın söz konusu olduğu karar problemlerinin çözümünde etkindir.
Bu nedenle daha karmaşık bir karar problemi çözelim.

**Örnek 8.13**: Piyasaya sürülecek yeni bir ürünün tanıtımı için bir reklam
kampanyası düzenlenecektir. Reklam için ya TV ya da gazete seçilecektir. TV ile
kampanyanın başarılı olması olasılığı 0.6, başarısız olması olasılığı 0.4’dür.
Başarılı bir TV kampanyası sonucunda üreticinin kârı 90 TL olmaktadır. Kampanya
başarısız olduğunda firmanın, ürünün üretim haklarını 10 TL’ye devretmek veya
ürünü yeniden tasarlayarak yeni bir kampanya başlatmak gibi iki stratejisi
vardır.

Yeni tasarımlı ürünün başarılı olması şansı 0.7 olup bu durumda beklenen kâr 70
TL, başarısız olması şansı 0.3 olup beklenen kâr -20 TL’dir. Kampanya gazete ile
yapıldığında başarılı olma olasılığı 0.8, başarısız olma olasılığı 0.2’dir.
Başarılı olunduğunda kâr 60 TL olmaktadır. Başarısız olunması durumunda üretim
haklarının devredilmesi veya reklam ajansının değiştirilmesi mümkündür. Üretim
haklarının devredilmesi durumunda net kâr 25 TL’dir. Ajansın değiştirilmesi
kararlaştırıldığında; yeni kampanyanın başarılı olması olasılığı 0.7, başarısız
olması olasılığı 0.3’dür. Başarılı yeni kampanya 40 TL’lık net kâra, başarısız
yeni kampanya 15 TL net zarara neden olmaktadır. Firmanın en iyi stratejisini
saptayınız.

**Çözüm 8.13**: Önce karar noktası sayısını belirleyelim. İlk karar TV ile
gazete arasından seçim yapılmasına ilişkindir. Bu karar noktası karar ağacında
K1 ile gösterilmiştir. Bir an için reklam için TV’nin seçildiğini düşünelim. Bu
kampanyanın nasıl sonuçlanacağı belirsizlik içindedir. Bu belirsizlik, E1 olay
düğüm noktasında kampanyanın başarılı veya başarısız olması olaylarına karşılık
gelen dallarla açıklanmıştır. Bu olaylardan başarısızlık durumunun
gerçekleştiğini düşünelim. Bu durumda karar verici K2 ile gösterilen karar alma
noktasına gelir.

K2 ikinci aşama karar noktası olup ürünün yeniden tasarlanarak yeni bir kampanya
başlatılması veya üretim haklarının devredilmesi seçenekleri arasından seçim
yapılması durumunu gösterir. Bu aşamada yeni tasarım-yeni kampanya alternatifi
seçilirse E3 olay düğüm noktasından çıkarılan iki dal ile gösterilmiş olan
belirsizlikle karşılaşılır.

Başlangıçta reklam kampanyası için gazetenin seçilmiş olduğunu düşünelim. Bu
seçimin sonucu da belirsizlik içermektedir. Kampanyanın başarısı ile ilgili bu
belirsizlik E2 olay düğüm noktasından çıkan iki dalla açıklanmıştır. Bu
olaylardan başarısızlık durumunun ortaya çıkması halinde firma K3 ile gösterilen
ikinci aşama karar noktasına gelir. Bu karar noktası reklam ajansının
değiştirilmesi veya üretim haklarının satılması seçenekleri arasından bir seçim
yapılması durumunu gösterir.

Ajansın değiştirilmesine karar verildiğini düşünelim. Bu kararın uygulanması
sonucunda kampanya ya başarılı ya da başarısız olacaktır. Bu belirsizlik E4 olay
noktasından çıkarılan iki dalla açıklanmıştır.

Karar ve olay noktaları ile dallarının belirlenmesinden sonra ağacın en
sağındaki uç noktalara karşılık geldikleri kârların yazılmasıyla karar ağacı
aşağıdaki gibi belirlenmiş olur.

70 TL’lik kâr; TV seçimi, başarısızlık, yeni tasarı-yeni kampanya, başarılı olma
eylem-olay bileşenleri sonucu ortaya çıkar. Şimdi de karar ağacının en sağından
başlayıp, ilk karar noktasına doğru dalları izleyerek her bir olay düğüm
noktasındaki beklenen kârları hesaplayalım.

Önce E3 olay düğüm noktasını inceleyelim. Bu noktadaki kârın beklenen değeri,

70(0.7) + (-20)(0.3) = 43 TL

olarak hesaplanmıştır.

Hesaplanan bu değer E3 düğümünün üzerinde gösterilmiştir. 43 TL’lik kâr hakların
satılması durumunun sağladığı 10 TL’lik kârdan yüksek olduğundan hakların
satılması dalı hiçbir zaman seçilmeyecektir. Bu durum bu dal üzerine konulan
"//" işaretiyle açıklanmıştır.

E3’den başa doğru gidildiğinde karşılaşılan E1’deki beklenen kârı
hesaplayabiliriz. E1’deki kâr,

90(0.6) + 43(0.4) = 71.2 TL

olarak hesaplanmıştır.

Hesaplanan bu değer E1 üzerine yazılmıştır.

Şimdi de E4’den başlayıp başlangıç karar noktasına doğru dallar üzerinde
ilerleyerek beklenen kârları hesaplayalım. E4’de beklenen kâr, karar ağacında
gösterildiği gibi,

40(0.7) + (-15)(0.3) = 23.5 TL

olarak hesaplanmıştır.

Ajansın değiştirilmesi durumundaki beklenen kâr, hakların satılması durumunda
sağlanacak olan kârdan az olduğundan ajansın değiştirilmesi düşünülmeyecek yani,
bu dal iptal edilecektir.

E4’den sonra E2’deki beklenen kârı hesaplayalım. E2’deki kâr,

60(0.8) + 25(0.2) = 53 TL

olarak hesaplanmıştır.

Bu değer gazete reklam kampanyasının işletmeye sağlayacağı kârdır. E2’deki kârın
hesaplanmasıyla problem çözülmüş olur.

TV seçiminin sağlayacağı kâr (71.2 TL), gazete seçiminin sağlayacağı kârdan
(53.0 TL) yüksek olduğundan kampanyanın TV ile sürdürülmesine karar verilir.

Böylece belirlenen karar ağacı Şekil 8.4’de gösterilmiştir.

**Şekil 8.4**

# 8.6. BAYESGİL KARAR KURALI: SONRAKİ ANALİZ

Şimdiye kadar muhtemel olaylardan hangisinin gerçekleşeceği konusunda kesin
bilgiye sahip olunmadan ön (önsel) olasılıklarla karar alma üzerinde
durulmuştur. Oysa, kararın olayların önsel olasılıklarının gözden geçirilerek ek
bilgilerle gerekli düzeltmelerin yapılması veya önsel olasılık değerlerinin bir
kez daha onaylanmasından sonra alınması daha uygun olur. Bu yolla, alınacak
karara duyulan güven artacaktır. Çünkü alınan kararın isabetliliği, herşeyden
önce belirsizlik derecesinin azaltılmasına bağlıdır. Belirsizlik derecesinin
azaltılması ek bilgilerle gerçekleştirilir. Ön olasılıklar ek bilgilerle daha az
belirsizlik gösteren sonraki (sonsal) olasılıklara dönüştürülür. Sonsal
olasılıkların elde edilmesi veya önsel olasılıkların güncelleştirilmesi için
Bayes kuralı veya Bayes yaklaşımından yararlanılır. Bayes yaklaşımı, deneyin
mümkün sonuçları ile ilgili olasılıkların gözden geçirilerek gerekli
düzeltmelerin yapılmasına olanak sağlayan son derecede faydalı bir yaklaşımdır.

Beklenen değer yaklaşımının bir uzantısı olan Bayes yaklaşımında da beklenen
değer kavramı kullanılır. Bayesgil yaklaşımının beklenen değer yaklaşımından
farkı olasılıkların sonsal oluşudur. Bayes yaklaşımı aşağıdaki formülle
açıklanır.

Burada; H1, H2, ..., Hn birleşimleri S örneklem uzayını veren ayrık olaylar, E
örneklem uzayının herhangi bir olayıdır. Bayes formülü için daha açık olarak
aşağıdaki gibi yazılır.

i = 1, 2, ..., n

Burada,

P(Hi), i = 1, 2, ..., n ek bilgiye ulaşılmadan önceki (önsel) olasılıklardır.

P(Hj / E), j = 1, 2, ..., n ek bilgiye ulaşıldıktan sonraki (sonsal)
olasılıklardır.

Karar verme problemlerinde Bayes formülü kullanımını sipariş miktarının
belirlenmesiyle ilgili örnek problemle açıklayalım.

**Örnek 8.14**: Mağaza sahibinin istem miktarına ilişkin önsel olasılıklara
güvenmediğini, daha güvenilir olasılıklara ulaşmak için pazar araştırması
kuruluşuyla anlaştığını düşünelim. Araştırma sonucu 4 farklı örnek grubunun
ortaya çıkabileceğini ve bu grupların aşağıdaki raporları sunacaklarını
düşünelim. Bu raporlar çerçevesinde olayların gerçekleşmesi olasılıklarını
gözden geçirerek bunlara ilişkin yeni değerleri elde ediniz

R1: İstem 100 adet olacak.

R2: İstem 150 adet olacak.

R3: İstem 200 adet olacak.

R4: İstem 250 adet olacak.

**Çözüm 8.14**: Pazar araştırmasıyla elde edilen ek bilgiye "gösterge" veya
"örnek bilgi" denir. Buna göre her rapor bir göstergedir. Amaç bu göstergeler
çerçevesinde olayların gerçekleşme olasılıklarını gözden geçirmek; ya onların
değerlerini onaylamak ya da gereken düzeltmeleri yapıp yeni değerlerini elde
etmektir. Araştırma sonucunda ulaşılan bilgiler her zaman yüzde yüz doğru
olmayabilirler. Ulaşılan bilgiden gereğince yararlanabilmek için göstergeler
(R1, R2, R3, R4) ve olaylar (O1, O2, O3, O4) arasındaki olasılık ilişkileri
hakkında bilgi sahibi olunması gerekir. Bunun için pazar araştırması kuruluşunun
daha önce buna benzer bir çalışma yaptığını ve geçmiş dönem kayıtlarından pazar
araştırması raporlarının gerçekleşmesi olasılıklarını Tablo 8.16’daki gibi
belirlediğini varsayalım.

**Tablo 8.16**

|         | Araştırma Raporu |      |      |      |
|---------|------------------|------|------|------|
| Olay    | R1               | R2   | R3   | R4   |
| O1: 100 | 0.70             | 0.10 | 0.05 | 0.15 |
| O2: 150 | 0.05             | 0.85 | 0.05 | 0.05 |
| O3: 200 | 0.10             | 0.05 | 0.75 | 0.10 |
| O4: 250 | 0.05             | 0.05 | 0.10 | 0.80 |

Tabloda verilenler koşullu olasılıklardır. Sözgelimi, tablonun ilk gözesindeki
0.70, istem 100 adet olarak gerçekleşmişken, araştırma kuruluşunun R1 ile
simgelenen raporu sunması olasılığı, yani P(R1/O1)’dir. Aynı şekilde, P(R2/O1) =
0.10, P(R3/O1) = 0.05, P(R4/O1) = 0.15’dir. Diğer olasılıklar; P(R1/O2) = 0.05,
P(R2/O2) = 0.85, ..., P(R2/O3) = 0.05, P(R3/O3) = 0.75, ..., P(R1/O4) = 0.05,
... ve P(R4/O4) = 0.80’dir.

Bu olasılık tahminleri ile sunulan rapora daha fazla güven duyulabilir. Çünkü,
istem 100 adet olarak gerçekleştiğinde gösterge de %70 olasılıkla bu durumu
rapor edecektir. Benzer şekilde istem 150 adet olduğunda, araştırma raporunun
"istem 150 adet olacak" şeklinde olması olasılığı %85’dir. Benzer şekilde istem
200 olduğunda raporun bunu destekler nitelikte olma olasığı %75; istem 250
olduğunda raporun bunu destekler nitelikte olma olasığı %80’dir.

Önsel ve koşullu olasılıklarla sunulan raporun Ri (i = 1, 2, 3, 4) olması
olasılıkları (P(Ri)) hesaplanabilir. Raporun niteliği ne olursa olsun, istem
miktarı mümkün dört değerinden birini alır. Buna göre bu olasılıklar aşağıdaki
gibi hesaplanır.

P(R1) = P(R1 O1) + P(R1 O2) + P(R1 O3) + P(R1 O4)

= P(O1)(R1 /O1) + P(O2)(R1 /O2) + P(O3)(R1 /O3) + P(O4)(R1 /O4)

= 0.2(0.70) + 0.3(0.05) + 0.3(0.10) + 0.2(0.05)

= 0.14 + 0.015 + 0.03 + 0.01 = 0.195

P(R2) = P(R2 O1) + P(R2 O2) + P(R2 O3) + P(R2 O4)

= P(O1)(R2 /O1) + P(O2)(R2 /O2) + P(O3)(R2 /O3) + P(O4)(R2 /O4)

= 0.2(0.10) + 0.3(0.85) + 0.3(0.05) + 0.2(0.05)

= 0.02 + 0.255 + 0.015 + 0.01 = 0.30

P(R3) = P(R3 O1) + P(R3 O2) + P(R3 O3) + P(R3 O4)

= P(O1)(R3 /O1) + P(O2)(R3 /O2) + P(O3)(R3 /O3) + P(O4)(R3 /O4)

= 0.2(0.05) + 0.3(0.05) + 0.3(0.75) + 0.2(0.10)

= 0.01 + 0.015 + 0.03 + 0.16 = 0.27

P(R4) = P(R4 O1) + P(R4 O2) + P(R4 O3) + P(R4 O4)

= P(O1)(R4 /O1) + P(O2)(R4 /O2) + P(O3)(R4 /O3) + P(O4)(R4 /O4)

= 0.2(0.15) + 0.3(0.05) + 0.3(0.10) + 0.2(0.80)

= 0.03 + 0.015 + 0.03 + 0.16 = 0.235

Şimdi de raporun R1 raporu olması durumunda; olayların gerçekleşme
olasılıklarının yeni değerlerini, yani sonsal olasılıkları hesaplayalım.

**a**. R1: "İstem 100 adet olacak." raporu verildiğinde O1, O2, O3, O4
olaylarına ilişkin sonsal olasılıklar Tablo 8.17’deki gibi hesaplanır.

**Tablo 8.17**

|          | Olasılık      |                     |                      |                       |
|----------|---------------|---------------------|----------------------|-----------------------|
|  Olay Oi |  Önsel  P(Oi) | Koşullu   P(R1 /Oi) |  Birleşik   P(R1 Oi) | Sonsal   P(Oi /R1)    |
| O1       | 0.20          | 0.70                | 0.140                | 0.140 / 0.195 = 0.718 |
| O2       | 0.30          | 0.05                | 0.015                | 0.015 / 0.195 = 0.077 |
| O3       | 0.30          | 0.10                | 0.030                | 0.030 / 0.195 = 0.154 |
| O4       | 0.20          | 0.05                | 0.010                | 0.010 / 0.195 = 0.051 |
| Toplam   | 1.00          |                     | 0.195                | -                     |

Tablo 8.17’nin sonsal başlıklı sütun değerleri incelendiğinde; göstergenin R1
olması durumunda; P(O1) için 0.20 yerine 0.718, P(O2) için 0.30 yerine 0.077,
P(O3) için 0.30 yerine 0.154 ve P(O4) için 0.20 yerine 0.051 değerlerinin
hesaplandığı görülebilir.

Sonsal olasılıklara göre beklenen kârın hesaplanması ile ilgili işlemler Tablo
8.18’de gösterilmiştir.

**Tablo 8.18**

|          |          |  Olay    |          |          | Beklenen |
|----------|----------|----------|----------|----------|----------|
| Strateji | O1 (100) | O2 (150) | O3 (200) | O4 (250) | Kâr      |
| 100      | 3000     | 2750     | 2500     |  2250    | 2865.5   |
| 200      | 1500     | 4750     | 8,000    |  7750    | 3070.0   |
| 300      | 2,000    | 5250     | 8500     | 11750    | 3748.5   |
| P(Oi)    | 0.718    | 0.077    | 0.154    | 0.051    | -        |

Sunulan rapor R1 olduğunda; Tablo 8.18’ün son sütununda gösterildiği gibi en
yüksek kârı 300 birimlik sipariş sağladığından bu miktarda sipariş verecektir.

**b**. Şimdi de göstergenin R2 olması durumu üzerinde duralım.

R2: "İstem 150 adet olacak." raporu verildiğinde olayların (O1, O2, O3, O4)
sonsal olasılıkları aşağıdaki gibi hesaplanır.

**Tablo 8.19**

|         | Olasılık    |                   |                     |                        |
|---------|-------------|-------------------|---------------------|------------------------|
| Olay Oi | Önsel P(Oi) | Koşullu P(R2 /Oi) |  Birleşik  P(R2 Oi) |  Sonsal   P(Oi /R2)    |
| O1      | 0.20        | 0.10              | 0.020               | 0.020 / 0.300 = 0.0667 |
| O2      | 0.30        | 0.85              | 0.255               | 0.255 / 0.300 = 0.8500 |
| O3      | 0.30        | 0.05              | 0.015               | 0.015 / 0.300 = 0.0500 |
| O4      | 0.20        | 0.05              | 0.010               | 0.010 / 0.300 = 0.0333 |
| Toplam  | 1.00        | -                 | 0.300               | -                      |

Böylece gösterge R2 olduğunda, O1’in önsel olasılığı 0.20 yerine 0.0666, O2’nin
önsel olasılığı 0.30 yerine 0.85, O3’ün önsel olasılığı 0.30 yerine 0.05 ve
O4’ün önsel olasılığı 0.20 yerine 0.033 elde edilmiştir.

Olayların gerçekleşme olasılıklarının yeni değerleriyle hesaplanan beklenen
değerler Tablo 8.20’de gösterilmiştir.

**Tablo 8.20**

|          |  Olay      | Beklenen |         |         |         |
|----------|------------|----------|---------|---------|---------|
| Strateji |  O1 (100)  | O2(150)  | O3(200) | O4(250) | Kâr     |
| 100      | 3000       | 2750     | 2500    | 2250    | 2737.5  |
| 200      | 1500       | 4750     | 8000    | 7750    |  495.5  |
| 300      | 2,000      | 5250     | 8500    | 11750   | 5412.0  |
| P(Oi)    | 0.0667     | 0.850    | 0.0500  | 0.0333  | -       |

İstem 150 adet olacak raporu gerçekleştiğinde en yüksek beklenen kâr 300 adet
siparişle sağlandığından bu miktarda sipariş verilmesi kararlaştıracaktır.

**c**. Şimdi de göstergenin R3 olması durumu üzerinde duralım.

"İstem 200 adet olacak." raporu verildiğinde O1, O2, O3, O4 olaylarına ilişkin
sonsal olasılıklar Tablo 8.21’deki gibi hesaplanır.

Tablo 8.21’in sonsal başlıklı sütunundan görüleceği gibi göstergenin R3 olması
durumunda, olayların gerçekleşme olasılıkları; P(O1) = 0.20 yerine 0.037, P(O2)
= 0.30 yerine 0.555, P(O3) = 0.30 yerine 0.833 ve P(O4) = 0.20 yerine 0.074
olarak elde edilmiştir.

**Tablo 8.21**

|         | Olasılık     |                    |                   |                      |
|---------|--------------|--------------------|-------------------|----------------------|
| Olay Oi | Önsel  P(Oi) | Koşullu  P(R3 /Oi) | Birleşik P(R3 Oi) | Sonsal  P(Oi /R3)    |
| O1      | 0.20         | 0.05               | 0.010             | 0.010 / 0.27 = 0.037 |
| O2      | 0.30         | 0.05               | 0.015             | 0.015 / 0.27 = 0.055 |
| O3      | 0.30         | 0.75               | 0.225             | 0.225 / 0.27 = 0.833 |
| O4      | 0.20         | 0.10               | 0.020             | 0.020 / 0.27 = 0.074 |
| Toplam  | 1.00         | -                  | 0.270             | -                    |

Olasılıkların yeni değerleriyle hesaplanan beklenen kârlar Tablo 8.22’nin son
sütununda gösterilmiştir. Tablonun beklenen kâr sütunu incelendiğinde en yüksek
kârı (8317.93 TL) sağlayan 300 birimlik sipariş verme seçeneği seçilecektir.

**Tablo 8.22**

|          | Olay     | Beklenen |          |          |          |
|----------|----------|----------|----------|----------|----------|
| Strateji | O1 (100) | O2 (150) | O3 (200) | O4 (250) | Kâr      |
| 100      | 3000     | 2750     | 2500     | 2250     | 2512.63  |
| 200      | 1500     | 4750     | 8000     | 7750     | 7556.63  |
| 300      | 2000     | 5250     | 8500     | 11750    | 8317.93  |
| P(Oi)    | 0.037    | 0.055    | 0.833    | 0.074    | -        |

**d**. Son olarak göstergenin R4 olması durumu üzerinde duralım.

R4: "İstem 250 adet olacak." raporu verildiğinde O1, O2, O3, O4 olaylarına
ilişkin sonsal olasılıklar aşağıdaki gibi hesaplanırlar.

**Tablo 8.23**

|         | Olasılık     |                    |                     |                        |
|---------|--------------|--------------------|---------------------|------------------------|
| Olay Oi | Önsel  P(Oi) | Koşullu  P(R4 /Oi) |  Birleşik   P(R4Oi) | Sonsal  P(Oi /R4)      |
| O1      | 0.20         | 0.15               | 0.030               | 0.030 / 0.235 = 0.1276 |
| O2      | 0.30         | 0.05               | 0.015               | 0.015 / 0.235 = 0.0638 |
| O3      | 0.30         | 0.10               | 0.030               | 0.030 / 0.235 = 0.1276 |
| O4      | 0.20         | 0.80               | 0.160               | 0.160 / 0.235 = 0.6808 |
| Toplam  | 1.00         | -                  | 0.235               | -                      |

Olay olasılıklarının yeni değerleriyle hesaplanan beklenen değerler Tablo
8.24’ün son sütununda gösterilmiştir. Söz konusu sütun değerlerinin ortaya
koyduğu gibi gösterge R4 olduğunda mağaza sahibi en yüksek kârı veren 300
birimlik sipariş seçeneğini seçecektir.

**Tablo 8.24**

|          | Olay     | Beklenen |          |          |          |
|----------|----------|----------|----------|----------|----------|
| Strateji | O1 (100) | O2 (150) | O3 (200) | O4 (250) | Kâr      |
| 100      | 3000     | 2750     | 2500     | 2250     |  2425.25 |
| 200      | 1500     | 4750     | 8000     | 7750     |  6791.45 |
| 300      | 2000     | 5250     | 8500     | 11750    | 10088.85 |
| P(Oi)    | 0.1276   | 0.0638   | 0.1276   | 0.6808   | -        |

Özetle araştırma grubu,

R1 ile simgelenen raporu sunduğunda 300 adet,

R2 ile simgelenen raporu sunduğunda 300 adet,

R3 ile simgelenen raporu sunduğunda 300 adet,

R4 ile simgelenen raporu sunduğunda 300 adet,

sipariş verilmesi uygun olacaktır.

Kuşkusuz bu kararların alınabilmesi için raporun türünün biliniyor olması
gerekir. Her bir raporun gerçekleşme olasılıklarının yukarıda önsel olasılıklar
ile koşullu olasılıkların kullanılmasıyla hesaplanan birleşik olasılıklara eşit
yani, P(R1) = 0.195, P(R2) = 0.30, P(R3) = 0.27, P(R4) = 0.235 olsunlar. Buna
göre pazar araştırması raporuna dayanarak alınacak kararın sağlayacağı beklenen
kâr aşağıdaki gibi hesaplanacaktır.

**Tablo 8.25**

|  Rapor |  Olasılık | En İyi Stratejinin Beklenen Kârı | Beklenen Değer |
|--------|-----------|----------------------------------|----------------|
| R1     | 0.195     |  3748.50                         |  730.98        |
| R2     | 0.300     |  5412.00                         | 1623.60        |
| R3     | 0.270     |  8317.93                         |  2245.84       |
| R4     | 0.235     |  10088.85                        |  2370.88       |
| -      | -         | -                                |  6971.28       |

Görüldüğü gibi örnek bilgi altında beklenen kazanç 6971.28 TL olacaktı. Burada
olduğu gibi, örnek bilgi altında beklenen kazanç her zaman tam bilgi altında
beklenen kazançtan küçüktür.

# 

# PROBLEMLER

**1**. Ana bayiden 8 TL’ye alınan bir gazete 10 TL’ye satılmakta, gününde
satılmayan bir gazete ana bayiye 5 TL’ye iade edilmektedir. Günlük satış
miktarını kesin olarak bilmeyen satıcı geçmiş 50 günü gözlemiş, istem miktarının
24 ile 30 arasında değiştiğini belirlemiştir. Bayinin istemle ilgili sahip
olduğu diğer bilgiler aşağıda verilmiştir.

Gazete bayinin her gün kaç gazete satın almasının uygun olacağına karar veriniz.

| Günlük İstem:  | 24 | 25 | 26 | 27 | 28 | 29 | 30 |
|----------------|----|----|----|----|----|----|----|
| Gün Sayısı :   | 5  | 6  | 7  | 7  | 10 | 6  | 4  |

**2**. Geçmiş dönem kayıtlarından günlük ekmek satış miktarları aşağıdaki gibi
belirlenmiştir.

| Günlük Satış (Adet):  | 0  | 50 | 100 | 200 | 250 |
|-----------------------|----|----|-----|-----|-----|
| Gün Sayısı :          | 10 | 20 | 20  | 40  | 10  |

1.  Beklenen satış miktarını belirleyiniz.

2.  Bir adet ekmeğin maliyeti 4 TL, satış fiyatı 6 TL’dir . Üretildiği gün
    satılmayan ekmekler bir süt üretme çiftliğine tanesi 3 TL’den satılmaktadır.
    Beklenen değer ölçütüyle en iyi üretim miktarını belirleyiniz.

**3**. Genç bir çocuk, yaz tatilinde dondurma veya mısır satma arasında seçim
yapmak istemektedir. Dondurma satması durumunda; yaz mevsimi çok sıcak olursa
5000 TL, mevsim ılık geçerse 3000 TL kazanmayı ummaktadır. Mısır satması
durumunda; yaz mevsimi çok sıcak olursa 2500 TL, ılık geçerse 6,000 TL kâr
beklemektedir. Yaz mevsiminin sıcak olması olasılığı %65’dir. Buna göre çocuk
dondurma veya mısırdan hangisini satmalıdır?

**4**. Bir işletme yeni bir ürünün üretimine geçmeyi planlamaktadır. İşletme A
ve B ile gösterilen ürünlerin üretimi için gerekli kaynaklara sahiptir.
Yöneticiler adı geçen ürünlerden yalnızca birinin üretimini benimsemişlerdir.
İki ürünün istemine ilişkin yapılan pazar araştırması sonucu belirlenen
olasılıklar aşağıdaki tabloda gösterilmiştir.

|      | İstem Düzeyi |      |       |
|------|--------------|------|-------|
| Ürün | Yüksek       | Orta | Düşük |
| A    | 0.70         | 0.20 | 0.10  |
| B    | 0.60         | 0.20 | 0.20  |

Ürün çeşidi ve istem düzeyi eşleşmelerine göre hesaplanan kârlarla düzenlenen
karar matrisi aşağıda gösterilmiştir.

|      | İstem Düzeyi  |      |       |
|------|---------------|------|-------|
| Ürün | Yüksek        | Orta | Düşük |
| A    | 30            | 10   |  5    |
| B    | 40            | 15   | -5    |

Problemi beklenen değer yaklaşımıyla çözerek hangi ürünün üretilmesinin uygun
olacağını kararlaştırınız.

**5**. Bir karar verici yatırım seçeneklerini, yatırımlarla ilgili gelirleri ve
olasılıkları aşağıdaki tabloda gösterildiği gibi belirlenmiştir. Beklenen değer
ölçütüyle en uygun yatırım seçeneğini belirleyiniz.

|       | Yatırım Gelirleri Olasılıkları |     |     |
|-------|--------------------------------|-----|-----|
| Gelir | A                              | B   | C   |
| -50   | 0.4                            | 0.2 | 0.2 |
|  0    | 0.0                            | 0.0 | 0.1 |
|  60   | 0.4                            | 0.2 | 0.1 |
| 100   | 0.2                            | 0.4 | 0.6 |
| 150   | 0.0                            | 0.2 | 0.0 |

**6**. Bir alışveriş merkezi için uygun jenaratör büyüklüğüne karar
verilecektir. Merkezde tüketilecek elektrik enerjisi miktarı kesinlikle
bilinmediğinden jenaratör büyüklüğü de belirsizlik arz etmektedir. Enerji
miktarı-jenaratör büyüklüğü eşleşmelerine göre oluşacak masraflar aşağıda
gösterilmiştir.

| Enerji  | Jenaratör Büyüklüğü |      |       |          |
|---------|---------------------|------|-------|----------|
| Miktarı | Küçük               | Orta | Büyük | Olasılık |
| Az      | 50                  | 100  | 150   | 0.2      |
| Orta    | 140                 | 100  | 150   | 0.7      |
| Çok     | 190                 | 190  | 150   | 0.1      |

**a**. Fırsat kaybı tablosunu düzenleyiniz.

**b**. En uygun jenaratör büyüklüğünü kararlaştırınız.

**c**. Tam bilginin beklenen değerini hesaplayınız.

**7**. Saç bakım ürünleri üreticisi bir işletme ürün yelpazesine yeni bir ürün
katmayı planlamaktadır. Yeni ürün üretimi 500000 TL ek harcama gerektirmektedir.
Üretilmesi durumunda satılan her bir yeni ürün işletmenin kârında 1 TL artış
sağlamaktadır. Yeni ürünün istem dağılımı aşağıda gösterildiği gibi tahmin
edilmiştir.

| İstem (000) | Olasılık |
|-------------|----------|
| 30          | 0.05     |
| 40          | 0.10     |
| 50          | 0.20     |
| 60          | 0.30     |
| 70          | 0.35     |

1.  Yeni ürünün üretilmesi uygun mudur? Beklenen kâr nedir?

2.  Tam bilginin beklenen değerini hesaplayınız.

3.  İstemin 30000 olması olasılığı 0.10, 70000 olması olasılığı 0.30 olursa tam
    bilginin değeri ne olur?

**8**. Şampuan üreticisi bir firma, yeni bir şampuan üretmeyi planlamaktadır.
Üretim kapasitesini dikkate alan firma; A, B ve C şampuanlarından birini seçmek
durumundadır. A seçildiğinde üretimin başlama zamanı ile ilgili bir belirsizlik
söz konusu olmaktadır. Üretimin gecikme olasılığı 0.80’dir. Üretim geciksin veya
gecikmesin A’nın fiyatıyla ilgili olarak "yüksek fiyat" ve "düşük fiyat" olmak
üzere iki seçenek vardır. Üretimin gecikmesi ve yüksek fiyata karar verilmesi
durumunda istemin yüksek olma olasılığı 0.30 olup, birim net kâr 6 TL’dir. Aynı
koşulda satışların orta düzeyde gerçekleşme olasılığı 0.70 olarak tahmin
edilmiştir. Bu durumda birim net kâr -0.5 TL olmaktadır. A için düşük fiyata
karar verilmesi durumunda satışların yüksek düzeyde gerçekleşmesi olasılığı,
satışların düşük düzeyde gerçekleşmesi olasılığına eşittir. Yüksek istem
düzeyinde birim net kâr 3 TL, düşük istem düzeyinde birim net kâr 1 TL’dir.

B’nin seçilmesi durumunda üretimin gecikmesi söz konusu değildir. Tıpkı A gibi
B’nin fiyatıyla ilgili olarak "yüksek fiyat" ve "düşük fiyat" olmak üzere iki
seçenek vardır. Yüksek fiyata karar verilmesi durumunda satışların yüksek olması
olasılığı 0.30 olup birim net kâr 16 TL, satışların orta düzeyde gerçekleşme
olasılığı 0.70, birim net kâr -0.5 TL’dir. B için düşük fiyata karar verilmesi
durumunda satışların yüksek düzeyde gerçekleşme olasılığı 0.40, düşük düzeyde
gerçekleşme olasılığı 0.60’dır. İstem fazla olduğunda birim net kâr 8 TL, düşük
olduğunda birim net kâr 6 TL’dir.

C’ye karar verilmesi durumunda üretimin zamanında başlaması söz konusu değildir.
C’nin yüksek fiyatla satışına karar verilmesi durumunda satışların yüksek olması
olasılığı 0.25 olup birim net kâr 16 TL’dir. İstemin orta düzeyde gerçekleşmesi
olasılığı 0.70 olup bu durumda birim net kâr -0.5 TL’dir. C için düşük fiyata
karar verilmesi durumunda satışların yüksek düzeyde gerçekleşme olasılığı,
satışların düşük düzeyde gerçekleşmesi olasılığına eşittir. Yüksek satış
durumunda birim net kâr 13 TL, düşük satış durumunda birim net kâr 8 TL’dir.
Karar ağacını çizerek, beklenen değer yaklaşımıyla hangi şampuanın üretilmesinin
uygun olacağına karar veriniz.

**9**. Fotoğraf makinesi üretiminin gerçekleştirildiği bir işletmede biri
standart diğeri otomatik olmak üzere iki tip fotoğraf makinesi üretilmektedir.
İşletme, yeni yılın ilk haftasında oluşması muhtemel yüksek istemi karşılamak
amacıyla toplam üretim miktarını belirlemek istemektedir. Standart makinenin
değişken maliyeti 10 TL, otomatik makinenin değişken maliyeti 20 TL’dir.
Standart makinenin satış fiyatı 20 TL, otomatik makinenin satış fiyatı 35
TL’dir. Her bir makinenin istem miktarıyla ilgili olasılık dağılımı aşağıdaki
gibi tahminlenmiştir. Yeni yılın ilk haftasında satılmayan fotoğraf makineleri
hurda fiyatına elden çıkarılmaktadır. Standart makinenin hurda fiyatı 5 TL,
otomatik makinenin hurda fiyatı 10 TL’dir. Satış miktarı olasılıklarının
birbirlerinden bağımsız ve üretim miktarının sınırsız olduğu varsayılmaktadır.
Buna göre her bir makineden kaçar adet üretilmesi gerektiğini ve üretim
miktarlarına göre ortalama beklenen değerleri hesaplayınız.

|  Standart | Otomatik |       |          |
|-----------|----------|-------|----------|
| İstem     | Olasılık | İstem | Olasılık |
| 6000      | 0.30     | 2000  | 0.20     |
| 8000      | 0.70     | 4000  | 0.80     |

**10**. Yukarıdaki problemde toplam üretim miktarı 10000 ile
sınırlandırılmıştır. Bu durumu yansıtan karar ağacını çiziniz ve buna göre
üretim miktarlarını hesaplayınız.

**11**. Büyük bir çiftlik sahibi çiftliğinin su ihtiyacını karşılamak için kuyu
açmayı düşünmektedir. Daha önce çiftliğin bulunduğu bölgede açılan kuyuların
%70’inde suya 200 metre derinlikte rastlanmıştır. Bu derinlikte suya
rastlanmaması durumunda iki seçenek söz konusudur: kuyu açmaktan vazgeçmek veya
kuyuyu 50 metre daha derinleştirmek. Kuyunun 50 metre daha derinleştirilmesi
durumunda 250 metre derinlikte suya rastlama olasılığı %20’dir. Kuyu açma
maliyeti 50 TL/m dir. Kuyu açmak yerine suyu komşu çiftlikten satın almak da
mümkündür. Suyun satın alınması durumunda su sahibine 10 yıl için 15000 TL
ödenmesi gerekmektedir. Uygun karar ağacını çizerek beklenen değer yaklaşımıyla
çiftlik sahibi için en uygun kararı belirleyiniz.

**12**. Bilgisayar üreticisi bir şirket bilgisayarların üretiminde kullanılacak
bir parçayı satın almak istemektedir. Parça için; 1. Elle kontrol (EK), 2.
Sayısal kontrol (SK), 3. Otomatik kontrol(OK) olmak üzere üç alternatif vardır.
Parçaların sermaye maliyeti 1’den 3’e doğru artmaktadır.

Alınan karara bağlı olarak sonuçta ulaşılacak olan kâr bilgisayarların
sunulacağı pazarın büyüklüğüne bağlıdır. Pazarın büyüklüğü konusunda üç durum
söz konusudur: küçük, orta, büyük. Pazar büyüklüğü ve parça türüne bağlı olarak
beklenen krlar (negatif değerli olanlar kayıplar olmak üzere) aşağıdaki
gösterilmiştir.

|       | Pazar  |      |       |
|-------|--------|------|-------|
| Parça | Küçük  | Orta | Büyük |
| EK    |  0.5   | 1.0  | 1.5   |
| SK    |  0.0   | 1.5  | 2.5   |
| OK    | -1.5   | 0.5  | 3.5   |

Pazarın büyüklüğüne ilişkin olasılıklar küçük için 0.30, orta için %50, büyük
için %20 olarak belirlenmiştir. Marketin büyüklüğünün araştırılması için bir
araştırma grubuyla anlaşılmıştır. Araştırma grubunun marketin büyüklüğünü doğru
tesbit etmeleriyle ilgili koşullu olasılıklar aşağıdaki tabloda gösterilmiştir.

| Gerçek | Belirlenen Durum |      |       |
|--------|------------------|------|-------|
| Durum  | Küçük            | Orta | Büyük |
| Küçük  | 0.7              | 0.2  | 0.1   |
| Orta   | 0.2              | 0.7  | 0.1   |
| Büyük  | 0.0              | 0.2  | 0.8   |

1.  Koşullu beklenen olasılık tablosunu düzenleyerek tam bilginin beklenen
    değerini hesaplayınız.

2.  Araştırma grubu tarafından sunulan bilgi doğrultusunda koşullu beklenen şans
    tablosunu düzenleyiniz.

3.  Pazar araştırması grubuna araştırma yetkisinin verilebilmesi için araştırma
    grubunun istem edebileceği en yüksek fiyat ne olabilir.

**13**. Bir yatırımcı A ve B seçeneklerinden hangisine yatırım yapmasının uygun
olacağını araştırmaktadır. Yatırımcının alternatif stratejileri yatırım yapmamak
da dahil olmak üzere şöyledir: A’yı seçmek. A’nın seçilmesi ve başarılı olunması
durumunda yatırımcı ya hiçbir şey yapmadan beklemekte ya da elde ettiği kazançla
B’ye yatırım yapmaktadır. Bunun tersi de geçerlidir. A’da başarılı olma
olasılığı 0.70, B’de başarılı olma olasılığı 0.40’dır. Her iki yatırım
seçeneğinin gerektirdiği yatırım miktarı da 2000 TL olup, başarısız olunması
durumunda kazanç –2000 TL olmaktadır. A’nın başarılı olması durumunda 3000 TL
(yatırım miktarı dahil), B’nin başarılı olması durumunda 5000 TL (yatırım
miktarı dahil) elde edilmektedir. Karar ağacını çizerek en uygun stratejiyi
belirleyiniz.

**14**. Bir petrol arama şirketinin petrol haklarını satın almak istediği bir
yer için iki alternatif bölge (X ve Y) vardır. İki bölgeden yalnızca biri
seçilecektir. Aynı bölgede en fazla iki kez arama yapılabilmektedir. X’e karar
verilmiş olsun. İlk aramada X’de petrole rastlama olasılığı 0.40 ve beklenen kr
net 14 milyon TL’dir. İlk aramada petrole rastlanmaması durumunda ya aramadan
vazgeçilmekte veya ikinci kez arama yapılmaktadır. Aramadan vazgeçilmesi
durumunda beklenen zarar 3 milyon TL’dir. X’deki ikinci aramada petrole rastlama
ve rastlamama olasılıkları birbirine eşittir. Bu aramada petrole rastlandığında
net kr 12 milyon, rastlanmadığında net zarar 5 milyon TL olmaktadır. Y’ye karar
verilmiş olsun. İlk aramada Y’de petrole rastlama olasılığı ile rastlamama
olasılığı 0.50’ye eşittir. İlk aramada petrole rastlanması durumunda net kr 10
milyon TL’dir. Aramadan vazgeçildiğinde işletme arama masraflarından oluşan 3
milyon TL’lik zarara katlanmak zorundadır. İkinci bir aramada petrole rastlama
olasılığı 0.70’dir. İkinci aramada petrole rastlanması durumunda işletmenin krı
net 8 milyon TL, rastlanmaması durumunda net zarar 5 milyon TL olmaktadır.
İşletmenin hangi bölgede arama yapmasının uygun olacağını kararlaştırınız.
