BEŞİNCİ BÖLÜM

**TAMSAYILI DOĞRUSAL PROGRAMLAMA**

# 5.1. GİRiŞ

Doğrusal programlamanın bölünebilirlik varsayımı göz ardı edildiğinde, diğer
bütün varsayımlar aynı kalmak koşuluyla, doğrusal programlama tamsayılı doğrusal
programlamaya dönüşür. Kısaca tamsayılı programlama, model değişkenlerinden
bazılarının veya hepsinin tamsayı değerler alması koşulunu içeren bir
programlama türüdür. Problemin farklı fonksiyonları değişkenlerin tamsayı
değerleri için tanımlandıklarından, tamsayılı programlama aslında doğrusal
olmayan bir programlamadır. Bununla birlikte, değişkenlerin tamsayı olma koşulu
ihmal edildiğinde problem doğrusal programlama problemine eşdeğer oluyorsa,
tamsayılı programlama doğrusal programlama olarak ele alınabilir. Aksi halde,
doğrusal olmayan ilişkiler içeren bir problem söz konusu olur ki, çözüm için
doğrusal olmayan programlama çözüm yöntemlerinin uygulanması gerekir. Bu bölümde
tamsayı olma koşulu ihmal edildiğinde doğrusal programlamaya dönüşen tamsayılı
doğrusal programlama açıklanacaktır.

# 5.2. TAMSAYILI DOĞRUSAL PROGRAMLAMAYA GİRİŞ

Bütün değişkenleri tamsayı olan doğrusal programlamaya "tamamen tamsayılı
doğrusal programlama" denir. Tamamen tamsayılı programlamaya örnek olmak üzere
aşağıdaki modeli göz önünde bulunduralım.

Zenb = 3x1 + 6x2

4x1 + 3x2 10

x1, x2 0

x1, x2 tamsayı

Yukarıdaki tamsayılı doğrusal programlama modeli ile buna karşılık gelen
doğrusal programlama modeli arasındaki tek fark, değişken değerlerinin tamsayı
olmasını ifade eden "x1, x2 tamsayı" ek koşuludur.

Değişkenlerden bazılarının tamsayı değerler alması durumunda "karma tamsayılı
doğrusal programlama" söz konusu olur. Sözgelimi, aşağıdaki problemde x2 tamsayı
olmadığından, problem karma tamsayılı doğrusal programlama problemidir.

Zenb = 3x1 + 2x2 + 4x3

x1 + x2 4

x1 + 2x2 + x3 6

x1, x2, x3 0

x1, x3 tamsayı

Tamsayılı programlama problemlerinin çoğunda değişkenlerin bir kısmı veya hepsi
sıfır veya 1 değeri ile sınırlandırılır. Bunun nedeni, tamsayı karar
değişkeninin (xi) genellikle bir faaliyetin yapılması (xi = 1) veya yapılmaması
(xi = 0) ile ilgili olmasıdır. Bu gibi durumlarda "sıfır-1 programlama" söz
konusu olur. Sıfır-1 programlama yalnızca değişkenlerin iki değerli olması
durumlarında değil, orijinal değişkenlerin küçük bir bölümünün ikiden çok değere
sahip olması durumlarında da kullanılır. Karar değişkenleri için ikiden çok
mümkün durum varsa bu değişkenler sıfır-1 sistemi ile tanımlanarak işlemlerde
büyük kolaylıklar sağlanabilir. Özellikle x tamsayı değişkenin değeri,

0 x U, (2N-1 \< U 2N)

şeklinde kısıtlanmış ise x değişkeninin uygun her bir değeri,

xi =

olmak üzere tek bir şekilde gösterilebilir. Bağıntıdaki yi, sıfır veya 1
değerini alan çift değerli değişkendir. Bu nedenle, x değişkeni (N + 1) adet
çift değerli değişken içeren bu toplamla değiştirilebilir.

Tamsayı olma koşulu göz ardı edildiğinde ortaya çıkan programlamaya, tamsayılı
doğrusal programlamanın "doğrusal programlamaya gevşetilmiş biçimi" veya kısaca
"gevşek biçim" denir. Özetle, herhangi bir doğrusal tamsayılı programlama,
kendisine karşılık gelen gevşek biçimin tamsayı ve/veya sıfır veya 1 olma
koşulunu içeren halidir. Gevşek problem kendisine karşılık gelen tamsayılı
programlamadan daha az sayıda kısıt içerdiğinden daha esnektir. Bu nedenle,
gevşek problemin çözüm bölgesi, kendisine karşılık gelen tamsayılı problemin
çözüm bölgesini bütünüyle kapsar. Tamsayılı programlamanın en iyi çözümü ile
buna ilişkin gevşek biçimin en iyi çözümü arasındaki ilişki tamsayı
problemlerinin çözüm sonuçlarının incelenmesi bakımından çok önemlidir. Bu
ilişki, "herhangi bir en büyükleme amaçlı tamsayılı programlamanın amaç
fonksiyonunun en iyi değeri, kendisine karşılık gelen doğrusal programlamanın
amaç fonksiyonunun en iyi değerine eşit veya küçüktür" şeklinde özetlenebilir.
Bir başka deyişle, en büyükleme problemlerinde gevşek problemin en iyi çözümünün
Z değeri, tamsayılı programlama probleminin en iyi çözümü için üst sınırdır.
Problem en küçükleme amaçlı olduğunda bu ilişki, tamsayılı programlama
probleminin en iyi çözüm değeri kendisine karşılık gelen gevşek problemin en iyi
çözüm değerine eşit veya ondan büyük olur şeklinde açıklanır. Yani, en küçükleme
amaçlı tamsayılı programlama problemlerinde gevşek problemin en iyi çözümünün Z
değeri, tamsayılı problemin en iyi çözümü için alt sınırdır.

Tamsayılı programlama problemlerinin diğer özelliklerini açıklayabilmek
bakımından aşağıdaki basit problemi ele alalım. Burada amaç fonksiyonu,

Zenb = 10x1 + 8x2

kısıtlayıcı fonksiyon,

6x1 + 4x2 15

negatif olmama koşulu,

x1, x2 0

tamsayılılık koşulu,

x1, x2 tamsayı olarak verilmiş olsun.

Problemde iki değişken bulunduğundan çözümü grafik yöntemiyle belirleyelim.
Problemin grafik çözümü Şekil 5.1’de gösterilmiştir.

Şekil 5.1

Gevşek biçimin uygun çözüm bölgesi Şekil 5.1’deki gri alan olup, en iyi çözüm;
x1 = 0, x2 = 3.75, Zenb = 30 olarak belirlenmiştir. Buna göre 30, tamsayılı
problemin en iyi çözümü için üst sınırdır. Şekil 5.1’den görüleceği gibi
tamsayılı programlamanın çözüm bölgesi doğrusal programlamanın çözüm bölgesinden
farklıdır. Doğrusal programlamanın çözüm bölgesi konveks iken, tamsayılı
programlamanın çözüm bölgesi bu konveks küme içinde bulunan sınırlı sayıdaki
noktadan oluşan bir alt küme durumundadır. Doğrusal programlamanın en iyi çözümü
konveks bölgenin uç noktalarından birinde belirirken, tamsayılı programlamanın
en iyi çözümü mümkün çözüm noktalarından birinde gerçekleşir. Tamsayılı
programlamanın en iyi çözümünün ortaya çıktığı noktayı bulmak için önce bu
noktaların belirlenmesi gerekir. Tamsayılı problemin çözüm bölgesinin Şekil
5.1’de () ile gösterilen 8 noktadan oluştuğu görülebilir. Bu noktaların
koordinatlarının belirlenmesiyle tamsayılı probleminin uygun çözüm kümesi,

S = {(0, 0), (0, 1), (0, 2), (0, 3), (1, 0), (2, 0), (1, 1), (1, 2)}

olarak düzenlenir. Problemin en iyi çözümüne ulaşmak için her bir noktaya
ilişkin koordinatların amaç fonksiyonuna yerleştirilmesi ve fonksiyonun bu
noktalarda aldığı değerlerin hesaplanması gerekir. Problemin niteliğine göre,
amaç fonksiyonu değerini en büyük veya en küçük yapan nokta en iyi çözüm
noktasıdır. Hesaplanan Z değerleri, aşağıda gösterilmiştir.

Z(0, 0) = 10(0) + 8(0) = 0

Z(0, 1) = 10(0) + 8(1) = 8

Z(0, 2) = 10(0) + 8(2) = 16

Z(0, 3) = 10(0) + 8(3) = 24

**Z(1, 2) = 10(1) + 8(2) = 26**

Z(1, 0) = 10(1) + 8(0) = 10

Z(2, 0) = 10(2) + 8(0) = 20

Z(1, 1) = 10(1) + 8(1) = 18

Yukarıdaki sonuçlar incelendiğinde, tamsayılı programlamanın en iyi çözümüne (1,
2) noktasında ulaşıldığı görülebilir. Burada olduğu gibi, tamamen tamsayılı
programlamanın gevşek biçiminin çözüm bölgesi sınırlı ise, buna karşılık gelen
tamamen tamsayılı programlamanın uygun çözüm bölgesi sınırlı sayıda nokta içeren
bir kümedir. Kuramsal olarak, tamamen tamsayılı doğrusal programlamanın en iyi
çözümü, uygun çözüm noktalarının koordinatlarının amaç fonksiyonuna
yerleştirilmesiyle belirlenebilir. Ancak, gerçek tamsayılı programlamanın pek
çoğunda çok fazla uygun nokta bulunduğundan yerine koyma ile çözümün
uygulanabilir bir yaklaşım olduğu söylenemez.

Tamsayılı doğrusal programlamanın çözümünde kullanılan diğer bir yaklaşım şu
şekilde özetlenebilir. Önce tamsayılı doğrusal programlamayı gevşetmek,
böylelikle normal doğrusal programlama problemi haline gelen problemi çözmek ve
değişkenler için elde edilen ondalık sayıları tamsayı olacak şekilde
yuvarlamaktır. Yuvarlama ile çözüm bulma işlemini doğrusal programlama
gevşeğinin en iyi çözümü olarak belirlenen x1 = 0, x2 = 3.75 çözümüne
uygulayalım. x1 zaten tamsayı olduğundan yuvarlanması gerekmez. 3.75 için en
uygun tamsayı 4’dür. 3.75’in 4’e yuvarlanması durumunda (0, 4) olarak
belirlenecek olan çözümün uygun olmadığı (uygun çözüm bölgesinin dışında)
görüleceğinden, 3.75’in aşağıya doğru, yani 3’e yuvarlanması uygun olur. (0, 3)
uygun bir nokta olduğundan, buna ilişkin çözüm uygun bir çözümdür. Şimdi (0, 3)
çözümünün en iyi olup olmadığı üzerinde duralım. (0, 3) için Z = 24 olarak
hesaplanacaktır. Bu çözümün en iyi olmadığı (24 \< 26) görülebilir. Özetle
gevşek programlamanın tamsayı olmayan en iyi çözüm değerlerini yuvarlayarak
tamsayılı problemin en iyi çözümüne ulaşmak, özellikle küçük değerli
değişkenlerde, her zaman mümkün olmaz. Ayrıca, sıfır-1 programlamada yuvarlama
da söz konusu olamaz. Yuvarlama ile en iyi çözüme ulaşma, değişkenlerin çok
büyük değerli olmaları durumunda uygun olabilir. Yapılan açıklamaların ortaya
koyduğu gibi tamsayılı doğrusal programlamanın çözüm bölgesi, normal doğrusal
programlama çözüm bölgesinin bir alt kümesi olmakla birlikte, tamsayı
programlama problemini çözmek genellikle daha zordur.

# 5.3. TAMSAYILI PROGRAMLAMA İLE MODELLEME

Bu kesimde tamsayılı programlama problemlerinin nasıl formülleneceği örnek
problemlerle açıklanacaktır. Bu amaçla literatürde yaygın biçimde kullanılan ve
uygulamada sıkça ortaya çıkan bazı özel problemler ele alınacaktır. Bu
problemler; sermaye bütçeleme problemleri, sabit harcama problemleri, kapsayan
küme problemleri, sırt çantası problemleri, atama problemleri olarak
gruplandırılabilmektedir.

**Sermaye Bütçeleme Problemleri**: Kuruluşlar veya kişiler çok sık olarak
belirli sayıdaki seçenekler arasından bir veya birkaçının seçilmesi problemiyle
karşılaşırlar. Bu tip problemlerde genellikle, güvenilirlik, risk, gelir, net
bugünkü değer, büyüme vb. faktörler açısından farklılıklar gösteren
seçeneklerden hangilerine ne miktarda yatırım yapılırsa gelir en büyük veya risk
en düşük ya da güvenilirlik en yüksek olur sorularına yanıt aranır. Bu tip
problemlerin tamsayılı programlama problemi olarak değerlendirilmesine örnek
olması bakımından aşağıdaki problemi inceleyelim.

**Örnek 5.1**: Kâryap yatırım kuruluşu yatırım seçeneklerini Tablo 5.1’deki gibi
düzenlemiştir. Yatırımların net bugünkü değerleri (milyar TL) ile her bir
yatırımın gerektirdiği yatırım miktarları (milyar TL) aynı tabloda
gösterilmiştir. Her bir yatırım seçeneği en fazla bir kez değerlendirilmek
istenmektedir. Kuruluşun yatırım için ayırdığı parası 28 milyar TL’dir.
Kuruluşun amacı yatırımlarla ilgili toplam net bugünkü değeri (NBD) en
büyüklemektir. Problemin tamsayılı programlama modelini kurunuz.

**Tablo 5.1**

| Yat. Seçeneği | NBD | Yat. Miktarı |
|---------------|-----|--------------|
| 1             | 16  |  5           |
| 2             | 18  |  9           |
| 3             | 20  | 10           |
| 4             | 22  | 11           |

**Çözüm 5.1**: Doğrusal programlama modellemesinde olduğu gibi öncelikle karar
değişkenleri tanımlanmalıdır. Karar değişkenleri, kuruluşun almak zorunda olduğu
her bir karar için bir değişken tanımlayarak belirlenebilir. Bir yatırım
seçeneği seçilir veya seçilmez. Seçime ilişkin başka alternatif olmadığından,

xi = 1 i (i = 1, 2, 3, 4) yatırım seçeneği seçilmişse

xi = 0 i (i = 1, 2, 3, 4) yatırım seçeneği seçilmemişse

yazılabilir. Bu yolla, değeri ya sıfır veya 1 olan karar değişkenleri
tanımlanmış olur. Buna göre, problemin modeli sıfır-1 tamsayılı programlama
modeli olacaktır. Amaç toplam net bugünkü değeri en büyükleyecek yatırım planını
belirlemek olduğundan amaç fonksiyonu,

Z = Toplam Net Bugünkü Değer = 16x1 + 18x2 + 20x3 + 22x4

olmak üzere aşağıdaki gibi olur.

Zenb = 16x1 + 18x2 + 20x3 + 22x4

xj = 1 ise, toplam net bugünkü değer eşitliği i yatırımının net bugünkü değerini
kapsar. Aksi halde, yani xj = 0 ise, kapsamaz. Bu, hangi yatırım veya yatırımlar
seçilmiş olursa olsun eşitliğin yatırım planına ilişkin toplam net bugünkü
değeri vereceği anlamındadır. Sözgelimi, 1 ve 3 nolu yatırım seçeneklerinin
değerlendirilmesi durumunda, x1 = x3 = 1, x2 = x4 = 0 olacağından toplam net
bugünkü değer aşağıdaki gibi hesaplanır.

Toplam Net Bugünkü Değer = 16(1) + 18(0) + 20(1) + 22(0)

= 36 milyar TL

Kuruluşun elindeki nakit miktarı 28 milyar TL’dir. Amaç fonksiyonunun
formüllenmesinde olduğu gibi nakit miktarı aşağıdaki gibi yazılabilir.

Toplam yatırım Miktarı = 5x1 + 9x2 + 10x3 + 11x4

Sözgelimi, x1 = x2 = x3 =1 ve x4 = 0 ise kuruluş ilk üç seçeneği seçer ve

Toplam yatırım Miktarı = 5(1) + 9(1) + 10(1) + 11(0)

= 24 milyar TL

değerinde yatırım yapar.

En fazla 28 milyar TL’lik yatırım yapılabileceğinden, nakit kısıtlayıcısı
aşağıdaki gibi olur.

5x1 + 9x2 +10x3 + 11x4 28

Amaç fonksiyonu, nakit kısıtlayıcısı ve "xi = 0 veya 1" koşulunun
düzenlenmesiyle sıfır-1 programlama modeli, aşağıdaki gibi olur.

Zenb = 16x1 + 18x2 + 20x3 + 22x4

5x1 + 9x2 + 10x3 + 11x4 28

xi = 0 veya 1 (i = 1, 2, 3, 4)

Problemin en iyi çözümü, x1 = 1, x2 = 0, x3 = 1, x4 = 1 ve Zenb = 58 milyar TL
olarak belirlenmiştir. Buna göre, 1, 3 ve 4 nolu yatırım seçenekleri
değerlendirilecek ve 28 milyar TL bu seçenekler arasında sırasıyla, 5, 10 ve 11
olarak paylaştırılacaktır. Bu yolla toplam net bugünkü değerin en büyük olması
sağlanacaktır. En iyi çözüme 26 milyar TL harcayarak (tamsayı olma koşulu
yüzünden 2 milyar TL elde kalmıştır) ulaşıldığı görülebilir. Gevşek problemin en
iyi çözümü, x1 = 28, x2 = x3 = x4 = 0, Zenb = 89.6 milyar olarak belirlenmiştir.
Bu kez eldeki tüm paranın yatırıldığı görülebilir. Tamsayı olma koşulunun
problemi nasıl değiştirdiği, çözüm sonuçlarının karşılaştırılmasıyla belirgin
biçimde ortaya çıkmaktadır.

**Sabit Harcama Problemleri**: Sabit harcama problemleri, herhangi bir faaliyet
için katlanılan maliyetin, faaliyetin düzeyinden bağımsız olduğu durum
problemleridir. Karar vericinin herhangi bir hizmet için yer belirleme durumunda
olması halinde beliren problem de, sabit harcama problemi olarak
değerlendirilebilir. Burada yer belirlemeye konu olan bina, depo, ofis gibi
vasıtaların maliyetleri sabit harcamalar olarak düşünülebilir.

**Örnek 5.2**: Çeliktaş işletmesi üç farklı rulman üretmeyi planlamaktadır.
Rulmanların her birinin üretimi farklı özellikte makine ile
gerçekleştirilmektedir. İşletme rulman tipine uygun makineleri kiralamayı
düşünmektedir. Rulmanların her biri farklı işçilik zamanı ile farklı miktarda
alaşım gerektirmektedir. İşletmenin haftalık işçilik zamanı kapasitesi 40
saattir. Haftada 100 kg çelik alaşımı tedarik edilebilmektedir. Değişken birim
maliyet, kaynak gereksinmeleri, makine kiraları ve rulman satış fiyatları
aşağıdaki tabloda gösterilmiştir. Çözümü, toplam kârın en büyük olmasını
sağlayacak değişken değerlerini verecek olan modeli kurunuz.

**Tablo 5.2**

|  Rulman | Makine Kirası (TL) | Satış Fiyatı (TL) | Değişken Maliyet (TL) | Zaman (saat) | Alaşım (kg) |
|---------|--------------------|-------------------|-----------------------|--------------|-------------|
| A       | 20                 | 30                |  5                    |  2           | 6           |
| B       |  40                |  60               |  8                    |  3           |  9          |
| C       | 55                 |  85               | 10                    |  4           |  15         |

**Çözüm 5.2**: Her zamanki gibi öncelikle karar değişkenlerini tanımlayalım.
Problemin karar değişkenleri aşağıdaki gibi tanımlanabilir.

x1 = A tipi rulman üretim miktarı

x2 = B tipi rulman üretim miktarı

x3 = C tipi rulman üretim miktarı

Kiralama maliyeti üretim miktarına değil, yalnızca üretilecek rulman tipine
bağlı olduğundan sabit maliyet olarak değerlendirilir. Bu nedenle kiralama
maliyetleri aşağıda tanımlanan değişkenlerle açıklanabilir.

y1 = 1 A tipi rulman üretiliyorsa, y1 = 0 A tipi rulman üretilmiyorsa,

y2 = 1 B tipi rulman üretiliyorsa, y2 = 0 B tipi rulman üretilmiyorsa,

y3 = 1 C tipi rulman üretiliyorsa, y3 = 0 C tipi rulman üretilmiyorsa,

Kısaca xi \> 0 ise, yi = 1 ve xi = 0 ise, yi = 0 olur. Bu tanımlamalardan sonra
işletmenin haftalık kârı aşağıdaki gibi açıklanabilir.

Kâr = Satış Geliri - (Değişken Maliyet + Kiralama Maliyeti)

Kârı (hafta bazında )oluşturan elemanlar aşağıdaki gibi formüllenir.

Kiralama Maliyeti = 20y1 + 40y2 + 55y3

Bu denklem, işletmenin ürettiği rulman çeşidinin gerektirdiği makine(lerin)
kirasını yansıtır. Sözgelimi, A tipi rulman üretiliyorsa; x1 \> 0, dolayısıyla
y1 = 1 ve C tipi rulman üretiliyorsa; x3 \> 0, dolayısıyla y3 = 1 olur. Bu
durumda A ve C tipi rulman üretimi sonucu haftalık kiralama maliyeti aşağıdaki
gibi olur.

Haftalık Kiralama Maliyeti = 20(1) + 40(0) + 55(1)

Haftalık Kiralama Maliyeti = 75 TL

Kiralama maliyeti, üretim miktarlarına bağlı olmadığından sabit maliyettir.
Sabit maliyetlerin model kurmayı zorlaştırdıkları unutulmamalıdır.

Haftalık Değişken Maliyet = 5x1 + 8x2 +10x3

Haftalık Satış Geliri = 30x1 + 60x2 + 85x3

saptamalarının ardından haftalık kâr (=Z), aşağıdaki eşitlikle ifade edilir.

Haftalık Kâr = (30x1 + 60x2 + 85x3) - (5x1 + 8x2 +10x3) - (20y1 + 40y2 + 55y3)

Hedef bu toplamın en büyüklenmesi olduğundan, amaç fonksiyonu aşağıdaki gibi
olur.

Zenb = 25x1 + 52x2 + 75x3 - 20y1 - 40y2 - 55y3

Bu toplamın en büyüklenmesi, işletmenin üretim zamanı ve alaşım miktarı
kısıtlayıcı koşulları ile çevrelenmektedir.

Aşağıda gösterildiği gibi, üretim için ayrılan zaman (2x1 + 3x2 + 4x3) işçilik
zamanı kapasitesine (40 saat) eşit veya küçük olabilir.

2x1 + 3x2 + 4x3 40

Üretim miktarlarını kısıtlayan diğer bir faktör alaşım miktarı olup, bu faktör
için düzenlenen kısıtlayıcı fonksiyon aşağıda gösterilmiştir.

6x1 + 9x2 + 15x3 100

x1, x2, x3 değişken değerlerinin tamsayı oldukları ve yi = 0 veya 1 olduğunun
göz önünde bulundurulmasıyla, problemin modeli aşağıdaki gibi yazılır.

Zenb = 25x1 + 52x2 + 75x3 - 25y1 - 50y2 - 65y3

2x1 + 3x2 + 4x3 40

6x1 + 9x2 + 15x3 100

x1, x2, x3 0

x1, x2, x3 tamsayı

y1, y2, y3 = 0 veya 1

Problemin en iyi çözümü, x1 = 0, x2 = 11, x3 = 0, y1 = y2 = y3 = 0 ve Zenb = 572
olarak belirlenmiştir. En iyi olduğu belirlenen bu çözümün uygulanamayacağı
açıktır. Çünkü, y1 = y2 = y3 = 0 belirlemesi işletmenin makinesiz üretim yaptığı
anlamını taşır ki, bu mümkün değildir. Bu durumdan kurtulmak için yukarıdaki
modele, xi \> 0 ise, yi = 1 koşulunun eklenmesi gerekir. Bu koşul basit bir hile
ile gerçekleştirilebilir. Şimdi bunu açıklayalım. M1, M2, M3 çok büyük pozitif
sayılar olsun. Buna göre,

x1 M1y1

x2 M2y2

x3 M3y3

eşitsizlikleri modele eklendiklerinde modelin çözümü xi \> 0 ise, yi = 1
olmasını sağlayacaktır. Bunu açıklamak için ilk eşitsizliği inceleyelim. x1 \> 0
ise, y1 = 0 olamaz. y1 = 0 ise x1 \< 0 veya x1 = 0 olabilir. Buna göre x1 \> 0
ise, y1 = 1 olması, böylece amaç fonksiyonunun kiralama maliyetini içermesi
sağlanır. y1 = 1 olduğunda x1 M1y1 eşitsizliği x1 M1 eşitsizliğine dönüşür. M1
çok büyük olduğundan, bu eşitsizlik x1’in değerini etkilemez. Eklenen
eşitsizliklerin değişkenlerin değerlerini etkilememesi için Mi değerlerinin
xi’nin en büyük değerinden daha büyük seçilmeleri gerekir. Bunun için, gerek
zaman gerekse alaşım kapasitesinin tamamıyla yalnızca A veya yalnızca B ya da
yalnızca C tipi rulman üretildiği kabul edilir. Yalnızca A tipi rulman
üretildiğini düşünelim. Bu durumda, zaman kısıtı dikkate alındığında, A tipi
rulmandan en fazla 20 (= 40/2) adet, alaşım kısıtı dikkate alındığında, en fazla
16 (= 100/6) adet üretilebilir. Kısaca tüm kapasite ile A tipi rulmandan en
fazla 16 adet üretilebilecektir. Bu durumda, M1 = 16 seçilmesi, x1 0 ise y1 = 1
olması için yeterlidir. Benzer şekilde, x2 ve x3’ün en büyük değerleri
sırasıyla, 11 ve 6 olarak belirlenir. M1 = 16, M2 = 11, M3 = 6 belirlemesiyle
yeniden formüllenen problemin en iyi çözümü, x1 = 0, x2 = 11, x3 = 0, y1 = 0, y2
= 1, y3 = 0, Zenb = 532 olarak elde edilmiştir. Görüldüğü gibi, x1 = 0 iken y1 =
0, x3 = 0 iken y3 = 0, x2 \> 0 iken y2 = 1’dir.

**Kapsayan Küme Problemleri**: Kapsayan küme problemlerinde biri diğerini
tamamiyle kapsayan iki küme söz konusudur. Bu tür problemlerde amaç, kapsama
konumunda olan kümenin eleman sayısının en küçük olmasını sağlamaktır. Kapsayan
küme problemleri havayolu uçuş programlaması, bölgelere ayırma, dağıtım
planlaması, yer seçimi gibi uygulama problemlerinin çözümünde kullanılmaktadır.

**Örnek 5.3**: Özel bir sağlık kuruluşu yedi yerleşim merkezinden oluşan bir
bölgeye acil servis istasyonları kurmak istemektedir. Kuruluş en az sayıdaki
servis istasyonuyla, normal koşullarda her bir yerleşim merkezine en fazla 15
dakikada ulaşmayı istemektedir.

Yerleşim merkezleri arasındaki sürüş zamanı aşağıdaki tabloda gösterilmiştir.
Kurulması gereken istasyon sayısı ile bunların hangi merkezlere kurulacağının
belirlenmesinde kullanılacak tamsayılı programlama modelini kurunuz.

**Tablo 5.3**

| Yer. Mer.  | YM 1 | YM 2 | YM 3 | YM 4 | YM 5 | YM 6 | YM 7 |
|------------|------|------|------|------|------|------|------|
| YM 1       |  0   | 18   | 20   |  20  | 10   | 25   | 30   |
| YM 2       | 18   |  0   | 20   | 10   | 20   | 10   | 20   |
| YM 3       | 20   | 20   |  0   | 20   | 15   | 30   | 35   |
| YM 4       | 20   | 10   | 20   |  0   | 20   | 15   | 10   |
| YM 5       | 10   | 20   | 15   | 20   |  0   | 20   | 25   |
| YM 6       |  25  | 10   | 30   | 15   | 20   |  0   | 25   |
| YM 7       |  30  | 20   | 35   | 10   | 25   | 25   |  0   |

**Çözüm 5.3**: Kuruluş, 7 yerleşim merkezinin her biri için o merkeze istasyon
kurulsun mu kurulmasın mı kararı vermek zorundadır. Bu durumu göz önünde
bulundurarak aşağıdaki tanımları yapalım.

xi = 1 i (i = 1, 2, 3, ..., 7) yerleşim merkezine istasyon kurulmuşsa

xi = 0 i (i = 1, 2, 3, ..., 7) yerleşim merkezine istasyon kurulmamışsa

Bu tanıma göre acil servis istasyon sayısı aşağıdaki gibi elde edilecektir.

Z = x1 + x2 + x3 + x4 + x5 + x6 + x7

Amacın Z’yi en küçüklemek olduğu bellidir.

Problemle ilgili kısıtlayıcılar servis istasyonları arasındaki sürüş süresi ile
ilgilidir. Kısıtlayıcılar, bir yerleşim merkezine en fazla 15 dakikalık
uzaklıkta olan en az 1 servis istasyonu bulunmalıdır şeklinde açıklanabilir. 7
yerleşim merkezi bulunduğundan, 7 kısıtlayıcı fonksiyon yazılacaktır.
Kısıtlayıcıların yazılabilmesi için öncelikle, her bir yerleşim merkezine 15
dakikalık sürüş uzaklığında olan merkezleri belirleyelim. Birbirlerine 15
dakikalık sürüş uzaklığında bulunan merkezler Tablo 5.5’de gösterilmiştir.

**Tablo 5.5**

| Merkez | Merkezler  |
|--------|------------|
| 1      | 1, 5       |
| 2      | 2, 4, 6    |
| 3      | 3, 5       |
| 4      | 2, 4, 6, 7 |
| 5      | 1, 3, 5    |
| 6      | 2, 4, 6    |
| 7      | 4, 7       |

Buna göre birinci yerleşim merkezi için,

x1 + x5 1

yazılır. Söz konusu eşitsizliğin x1 = x5 = 0 alternatifini ortadan kaldırdığı,
x1 veya x5’den en az birinin 1’e eşit olmasına imkan verdiği görülebilir. Bu
yolla birinci yerleşim merkezine en fazla 15 dakikalık sürüş uzaklığında olan en
az 1 istasyon bulunması sağlanmış olur.

Benzer şekilde ikinci yerleşim merkezi için,

x2 + x4 + x6 1

yazılmasıyla, ikinci yerleşim merkezine en fazla 15 dakikalık sürüş uzaklığında
en az 1 acil servis istasyonu kurulması sağlanır.

Diğer yerleşim merkezleri için benzer kısıtlayıcıların yazılmasıyla problemin
sıfır-1 programlama modeli aşağıdaki gibi belirlenmiş olur.

Zenk = x1 + x2 + x3 + x4 + x5 + x6 + x7

x1 + x5 1 (YM 1 kısıtlayıcısı)

x2 + x4 + x6 1 (YM 2 kısıtlayıcısı)

x3 + x5 1 (YM 3 kısıtlayıcısı)

x2 + x4 + x6 + x7 1 (YM 4 kısıtlayıcısı)

x1 + x3 + x5 1 (YM 5 kısıtlayıcısı)

x2 + x4 + x6 1 (YM 6 kısıtlayıcısı)

x4 + x7 1 (YM 7 kısıtlayıcısı)

xi = 0 veya 1 (i = 1, 2, ... , 7)

Problemin en iyi çözümü; x4 = x5 = 1, x1 = x2 = x3 = x6 = x7 = 0 ve Zenk = 2
olarak belirlenmiştir. Buna göre biri dördüncü, diğeri beşinci yerleşim
merkezine kurulacak iki servis istasyonu ile tüm yerleşim merkezlerinin servis
istemi karşılanmış olacaktır. Görüldüğü gibi problemde biri yerleşim
merkezlerinden, diğeri acil servis istasyonlarından oluşan iki küme söz
konusudur. İki servis istasyonunun bulunduğu küme kapsayan durumunda olup yedi
merkezin oluşturduğu kümeyi tamamiyle kapsamaktadır.

**Atama Problemleri**: Uygulamada karşılaşılan taşıma, aktarmalı taşıma, atama
ve benzeri dağıtım problemlerinde de karar değişkenlerinin tamsayı değerler
alması zorunludur. 3.8. kesimde açıklanan atama problemleri bu tür problemlerin
en önemlilerindendir. Bir atama probleminin sıfır-1 tamsayılı programlama olarak
modellenmesiyle ilgili basit bir örnek aşağıda verilmiştir.

**Örnek 5.5** : En kısa sürede tamamlanması gereken 4 farklı iş (1, 2, 3, 4) ile
bu işleri yapabilecek dört işçi (A, B, C, D) bulunmaktadır. İşçilerin
yetenekleri birbirlerinden farklı olup her bir işçinin her bir işi tamamlama
süresine ait değerler aşağıda gösterilmiştir. Amaç işlerin en kısa sürede
tamamlanmasını sağlayacak iş-işçi eşleşmesini belirlemektir. Atama modelini
kurunuz.

**Tablo 5.5**

|      | İş  |    |    |    |
|------|-----|----|----|----|
| İşçi | 1   | 2  | 3  | 4  |
| A    |  3  |  8 |  6 |  4 |
| B    |  10 |  6 |  7 |  9 |
| C    |  16 | 10 |  5 |  9 |
| D    |  7  |  8 | 10 |  6 |

**Çözüm 5.5**: Önce karar değişkenlerini tanımlayalım. Bir işçi dört işten
yalnızca birine atanacak, bir iş dört işçiden yalnızca biri tarafından
yapılacaktır. Hangi işçinin hangi işe veya hangi işe hangi işçinin atanmasının
toplam süreyi en kısa yapacağı belirlenmek istendiğinden karar değişkenleri
iş-işçi bire bir eşleşmesini sağlayacak biçimde aşağıdaki gibi tanımlanabilir.

xij = 1 i (i = A, B, C, D) sembollü işçi j (j = 1, 2, 3, 4) nolu işe atanmışsa

xij = 0 i (i = A, B, C, D) sembollü işçi j (j = 1, 2, 3, 4) nolu işe atanmamışsa

A sembollü işçiyi ele alalım. A, 1 nolu işi yaparsa xA1 = 1, xA2 = xA3 = xA4 = 0
olur. A, 2 nolu işe atanırsa; xA2 = 1, xA1 = xA3 = xA4 = 0 olur. A’nın 3 veya 4
nolu işlere atanması durumunda 3 nolu iş için; xA3 = 1 diğer değişkenler sıfır,
4 nolu iş için xA4 = 1, xA1 = xA2 = xA3 = 0 olur. A mutlaka bir işe atanmak
zorundadır. Bu koşul aşağıdaki eşitlikle açıklanır.

xA1 + xA2 + xA3 + xA4 = 1

Benzer şekilde B, dört işten birini yapmak zorundadır. B’nin bir işe atanması
gerektiği koşulu aşağıdaki eşitlikle açıklanır.

xB1 + xB2 + xB3 + xB4 = 1

C ve D’nin de birer işe atanmasıyla ilgili olarak,

xC1 + xC2 + xC3 + xC4 = 1

xD1 + xD2 + xD3 + xD4 = 1

yazılmasıyla işçilerin atanmaları koşulları sağlanmış olur. Diğer taraftan her
iş mutlaka yapılmak zorundadır. 1 nolu işi ele alalım. Bu iş ya A ya B veya C ya
da D tarafından yapılacaktır. Buna göre birinci işin yapılması koşulu aşağıdaki
denklemle ifade edilir.

xA1 + xB1 + xC1 + xD1 = 1

Benzer şekilde diğer üç işin yapılmaları koşulu, her iş için bir eşitlik
yazılmasıyla aşağıdaki gibi elde edilecek, böylece kısıtlayıcıların düzenlenmesi
işlemi tamamlanmış olacaktır.

2 nolu iş için; xA2 + xB2 + xC2 + xD2 = 1

3 nolu iş için; xA3+ xB3 + xC3 + xD3 = 1

4 nolu iş için; xA4 + xB4 + xC4 + xD4 = 1

Amaç, işleri en kısa sürede tamamlamak olduğundan amaç fonksiyonu aşağıdaki gibi
formüllenir.

Zenk = 3xA1 + 10xB1 + 16xC1 + 7xD1 + 8xA2 + 6xB2 + 10xC2 + 8xD2 + 6xA3+ 7xB3

\+ 5xC3 + 10xD3 + 4xA4 + 9xB4 + 9xC4 + 6xD4

Böylece, problemin tüm değişkenleri yalnızca sıfır veya 1 değerini alan 0-1
tamsayılı programlama modeli kurulmuş olur. Problemin en iyi çözümü, xA1 = xB2 =
xC3 = xD4 = 1, Zenk = 20 olarak belirlenmiştir.

**Gezgin Satıcı Problemleri**: Tamsayılı programlama olarak formüllenen
problemlerden bir kısmı gezgin satıcı problemleri başlığı altında incelenir. Bu
tip problemlerde amaç, başlangıç yerleşim merkezine geri dönmek ve her merkeze
yalnızca bir kez uğramak koşuluyla birinci, ikinci, üçüncü, ... olarak hangi
merkezlere gidileceğinin planlanmasıdır. Tüm dikkat, gezi planının katedilen
yolun veya toplam gezi masraflarının ya da harcanan zamanın en küçüklenmesini
sağlaması üzerine yoğunlaştırılır. Gezi planının düzenlenebilmesi için gezi
güzergahı üzerindeki merkezler arasındaki uzaklıkların bilindiği varsayılır. i
ve j (i j) herhangi iki merkez olmak üzere bunlar arasındaki uzaklık Cij ile
gösterilir. Cij = Cji veya Cij Cji olabilir.

Başlangıç noktası 1 nolu yerleşim merkezi olsun. Satıcının i = 1, 2, ..., (n -
1) için seyahatini i’den i + 1’e ve n’den 1’e doğru olmak üzere planladığını
düşünelim. Bu plan "1, 2, ..., n; 1." olarak gösterilir. Plan; 1’den 2’ye, 2’den
3’e, ..., n’den 1’e geçildiğini açıklamaktadır. Görüldüğü gibi her bir merkeze
yalnızca 1 kez girilmekte, her merkez yalnızca bir ama bir kez terkedilmekte ve
tekrar başlangıç noktasına dönülmektedir. Burada olduğu gibi her merkeze bir
kere giren ve her merkezi bir kere terkeden sıralamaya "tur" denir. Tur kavramı
göz önünde bulundurulduğunda başlangıç yerleşim merkezinin önemsiz olduğu
görülecektir. Bununla birlikte anlatımı genelleştirmek amacıyla başlangıç
yerleşim merkezini 1 nolu merkez olarak sabitleyelim. 1 nolu merkezden yola
çıkan bir kişi kalan (n - 1) merkezden herhangi birine gidebilir. Yani, yola
çıkacak birinin gidebileceği (n - 1) sayıda merkez vardır. Bu merkezlerden
birine gelindiğinde kalan (n - 2) sayıda merkezden birine gidilebilir. Bu
durumda n merkezli gezgin satıcı problemlerinde mümkün turların sayısı (n - 1)(n
\- 2)...(2)(1) = (n - 1) dir.

Problem (n - 1)! sayıdaki turun listelenmesi yaklaşımıyla çözülebilirse de bu
yaklaşımın uygulanabilirliği seyahat güzergahı üzerindeki merkez sayısıyla
sınırlıdır. Sözgelimi n = 10 için listelenmesi gerekli tur sayısı 9! yani,
362880’e eşittir. Listelenmesi gereken tur sayısının büyüklüğü problemin
listeleme ile çözümünü imkansız kılmaktadır. Gezgin satıcı problemlerinin
tamsayılı programlama olarak formüllenmesi ve çözülmesi en uygun yaklaşımdır.

Bu tür problemlere sayısal örnek vermeden önce aşağıdaki genel tanımların
incelenmesi doğru olur.

(n - 1) sayıdaki mümkün turdan herhangi biri olsun. Bu tur için tamsayı karar
değişkenleri aşağıdaki gibi tanımlanabilir.

xij = 1 i şehrinden j şehrine gidiliyorsa

xij = 0 i şehrinden j şehrine gidilmiyorsa

Her tur bir atamadır. Tur olmayan atamalar da vardır. {(1, 2), (2, 1), (3, 4),
(4,3)}’ün bir atama olmakla birlikte tur olmadığı görülebilir. Tüm merkezleri
tarayan bu atamalar tek bir devre oluşturmamaktadır. Atama planı içinde {(1, 2),
(2, 1)} ve {(3, 4), (4,3)} olmak üzere iki alt tur bulunduğu görülebilir. Bu
açıklamalar çerçevesinde gezgin satıcının problemi aşağıdaki gibi formüllenir.

Zenk =

= 1 j = 1, 2, ..., n

= 1 i = 1, 2, ..., n

xij = 0 veya 1 bütün i, j’ler için

x = (xij) tur ataması

**Örnek 5.5**: Bir satış elemanının sorumlu olduğu dört şehir vardır. Satış
elemanı her ay bu dört şehre giderek satış işlerini kontrol etmek zorundadır.
Satış elemanının yaşadığı şehir (1) dahil 5 şehir arasındaki uzaklıklar
aşağıdaki tabloda gösterilmiştir. Satış elemanının gidiş faaliyetleri sırasında
katedeceği mesafenin en kısa olmasını sağlayacak gezi planını bulunuz.

**Tablo 5.6**

| j i  |  1 |  2 |  3 |  4 |  5 |
|------|----|----|----|----|----|
| 1    |    | 27 | 43 | 16 | 30 |
| 2    | 7  |    | 16 | 1  | 30 |
| 3    | 20 | 13 |    | 35 | 5  |
| 4    | 21 | 16 | 25 |    | 18 |
| 5    | 12 | 46 | 27 | 48 |    |

**Çözüm 5.5**: Önce karar değişkenlerini tanımlayalım. Karar değişkenleri satış
elemanının o anda bulunduğu şehirden sonra hangi şehre gideceği ile ilgili
olarak aşağıdaki gibi tanımlanabilir.

xij = 1 i’den hemen sonra j’ye gidilmişse

xij = 0 i’den hemen sonra j’ye gidilmemişse

xii = 0 olmak zorundadır. xii’lerin sıfır olmasını sağlamak için Cii’ler çok
büyük pozitif sayılar olarak alınır. Büyük Cii değerleri tabloda ile
gösterilmiştir.

Satış elemanının, 1 nolu şehirde bulunduğu herhangi bir turu incelemekte
olduğunu düşünelim. Satıcı 1 nolu şehirdeyse; 2, 3, 4 veya 5 nolu şehirlerden
birine gidebilir. Aynı anda birden fazla şehre gitmek mümkün olmadığından, 1
nolu şehirden ayrılma kısıtı olarak düzenlenen kısıtlayıcı fonksiyon aşağıda
gösterilmiştir.

x12 + x13 + x14 + x15 = 1

Satıcının 1 nolu şehirden ayrıldığını ve başka bir şehre ulaştığını düşünelim.
Bu durumda satıcı 2, 3, 4 veya 5 nolu şehirlerden birinde bulunur. Satıcının 2
nolu şehirde bulunduğunu düşünelim. Bu durumda satıcı 1, 3, 4 veya 5 nolu
şehirlerden birine doğru yola çıkacaktır. Bu koşul, 2 nolu şehirden ayrılma
kısıtı olarak, aşağıdaki eşitlikle açıklanır.

x21 + x23 + x24 + x25 = 1

Benzer şekilde 3, 4 ve 5 nolu şehirlerden yola çıkma kısıtları şöyle olur:

3 nolu şehir için; x31 + x32 + x34 + x35 = 1

4 nolu şehir için; x41 + x42 + x43 + x45 = 1

5 nolu şehir için; x51 + x52 + x53 + x54 = 1

Bu yolla her şehirden yalnızca bir kez ayrılma koşulu sağlanmış olur. Bir
şehirden ayrılmak için önce o şehre gitmiş olmak gerektiği açıktır.

Önce 1 nolu şehre dönüşü planlayalım. 1 nolu şehre 2’den, 3’den, 4’den veya
5’den gelinebilir. Bu koşul aşağıdaki eşitlikle açıklanır.

x21 + x31 + x41 + x51 = 1

Şimdi de 2 nolu şehre geliş üzerinde duralım. Bu şehre, 1, 3, 4 veya 5 nolu
şehirlerden birinden gelinebilir. Bu koşul aşağıdaki eşitlikle ifade edilir.

x12 + x32 + x42 + x52 = 1

Benzer yaklaşımla 3, 4 ve 5 nolu şehirlere gelişlerle ilgili olarak yazılan
eşitlikler aşağıda gösterilmiştir.

3 nolu şehir için; x13 + x23 + x43 + x53 = 1

4 nolu şehir için; x14 + x24 + x34 + x54 = 1

5 nolu şehir için; x15 + x25 + x35 + x45 = 1

Beş tanesi her şehre bir kez gitme, beş tanesi de her şehirden bir kez ayrılma
koşuluyla ilgili olarak toplam 10 (= 2n) kısıtlayıcı fonksiyonun yazılması
tamamlanmış olur. Şimdi de amaç fonksiyonunu yazalım.

Zenk = Mx11 + 27x12 + 43x13 + 16x14 + 30x15 + 7x21 + Mx22 + 16x23 + 1x24 + 30x25
\+ 20x31 + 13x32 + Mx33 + 35x34 + 3x35 + 21x41 + 16x42 + 25x43 + Mx44

\+ 18x45 + 12x51 + 46x52 + 27x53 + 48x54 + Mx55

Amaç fonksiyonunun düzenlenmesiyle gezgin satıcı problemi atama problemi olarak
modellenmiş olur. Modele xij’lerin tur oluşturmaları gerektiği koşulunun
eklenmesiyle modelleme işlemi son bulur. Problem, 5.4. kesimde açıklanacak olan
dal-sınır tekniğiyle çözülmüş ve en iyi çözüm, x14 = x42 = x23 = x35 = x51 = 1,
Zenk = 65 olarak belirlenmiştir.

**Ya-Veya Kısıtlayıcıları**

Matematiksel programlama problemlerinde çok sık olarak değişkenlerin,

f(x1, x2, ..., xn) 0 5.1

g(x1, x2, ..., xn) 0 5.2

kısıtlarından en az birini sağlayacak değerler alması garantilenmek istenir. Bu
durumu sağlamanın yolu problem formülasyonuna, aşağıdaki kısıtları eklemektir.

f(x1, x2, ..., xn) My 5.1

g(x1, x2, ..., xn) M(1 - y) 5.2

5.1 ve 5.2’de bulunan y, sıfır-1 değişken, M ise problemin diğer
kısıtlayıcılarını sağlayan xi’ler için f(x1, x2, ..., xn) M ve g(x1, x2, ...,
xn) M olmasını garanti edecek büyüklüğe sahip bir sayıdır. Eklenen bu iki
kısıtlayıcı f(x1, x2, ..., xn ) 0 ve g(x1, x2, ..., xn) 0 kısıtlayıcılarından en
az birinin gerçekleşmesini sağlayacaktır. 5.1 ve 5.2 ile açıklanan
eşitsizliklerin modele dahil edilmesi 5.1 veya 5.2’den en az birinin
gerçekleşmesini sağlayacaktır. Çünkü, y = 0 veya y = 1’dir. y = 0 ise,

f(x1, x2, ..., xn) 0

g(x1, x2, ..., xn) M

olur. Böylece, 5.1 ile açıklanan kısıtlayıcı gerçeklenir. y = 1 ise,

f(x1, x2, ..., xn) M

g(x1, x2, ..., xn) 0

olur, yani 5.2 eşitsizliği sağlanır. Kısaca y = 0 veya y = 1 olması 5.1 veya 5.2
ile açıklanan kısıtlayıcılardan en az birinin sağlanmasını garanti eder. Aşağıda
ya-veya kısıtlayıcılarının kullanıldığı bir örnek problem verilmiştir.

**Örnek 5.6**: Bir beyaz eşya fabrikası gelecek yıl için üretim planı
yapmaktadır. Fabrikada; buzdolabı, fırın ve çamaşır makinası üretilmektedir. Her
mamülün bir birim üretimi için gerekli olan zaman ve hammadde miktarları ile
birim kârları aşağıdaki tabloda gösterilmiştir. Planlama dönemi için eldeki
hammadde miktarı 22 ton, üretim zamanı ise 9000 saattir. Üretimin ekonomik
olabilmesi için, herhangi bir ürünün üretilmesi durumunda üretim miktarının
350’den az olmaması gerekmektedir. İşletmenin karını en büyükleyecek tamsayılı
programlama modelini kurunuz.

**Tablo 5.7**

|  Ürün            | Hammadde (kg) | Zaman (saat)  | Kâr (milyon TL) |
|------------------|---------------|---------------|-----------------|
| Buzdolabı        | 20            | 6             | 5               |
| Fırın            | 11            |  3            | 3               |
| Çamaşır Makinesi | 16            | 4,5           | 4               |

**Çözüm 5.6**: Her mamulden üretilecek miktarlar belirlenmek istendiğine göre,
karar değişkenleri aşağıdaki gibi tanımlanabilir.

x1: Buzdolabı üretim miktarı

x2: Fırın üretim miktarı

x3 : Çamaşır makinesi üretim miktarı

Amaç üç ürün için toplam kârı, yani 5x1 + 3x2 + 4x3 toplamını en büyüklemek
olduğundan amaç fonksiyonu aşağıdaki gibi tanımlanacaktır.

Zenb = 5x1 + 3x2 + 4x3

Üretimin ekonomik olması, herhangi bir mamulün üretilmesi durumunda, mamul
üretim miktarının en az 350 olmasına bağlıdır. O halde, i = 1, 2, 3 için ya xi 0
veya xi 350 olmalıdır.

Bu koşul her mamul için ayrı ayrı aşağıdaki gibi yazılır.

1\. x1 0 veya x1 350

2\. x2 0 veya x2 350

3\. x3 0 veya x3 350

Hammadde miktarı ve çalışma zamanı kısıtlı olduğundan üretim miktarları
aşağıdaki kısıtlayıcı fonksiyonları sağlamalıdır.

4\. 20x1 + 11x2 + 16x3 22000 (Hammadde kısıtlayıcısı)

5\. 6x1 + 3x2 + 4,5x3 9000 (Zaman kısıtlayıcısı)

Ya-veya türündeki kısıtlarla ilgili açıklamalar çerçevesinde, yukarıda 1, 2 ve 3
ile numaralandırılmış ya-veya kısıtlayıcılarını oluşturalım. x1’den başlayalım.
x1 0 veya x1 350 olmasını sağlamak için aşağıdaki tanımları yapalım.

f(x1, x2, x3) = x1

g(x1, x2, x3) = 350 - x1

Bu tanımları kullanarak 1 nolu kısıtlayıcı fonksiyonu aşağıdaki kısıtlayıcı
fonksiyon çiftiyle değiştirelim. Bu işlemle elde edilen eşitsizlikler aşağıda
gösterilmiştir. y1 = 0 veya 1 olduğu unutulmamalıdır.

x1 M1y1

(350 - x1) M1(1 - y1)

Hem x1, hem de (350 - x1) değerlerinin M1’den küçük olmasını sağlayacak M1
değeri nedir? Bunun için yalnızca buzdolabı üretildiğini düşünelim. Bu durumda
hammadde miktarı 22 ton olduğundan en fazla 1100(= 22000/20) adet buzdolabı
üretileceği açıktır. Zaman kısıtı dikkate alındığında, bu rakam 1500 olur.
Özetle, M1 = 1100 olarak seçilmesi uygun olur. x1 = 1100 ise, x2 = x3 = 0 olur.

Benzer işlemlerin 2 nolu kısıtlayıcı için gerçekleştirilmesiyle elde edilen
eşitsizlikler sistemi aşağıda gösterilmiştir. y1 = 0 veya 1 ve M2 = 2000 olduğu
unutulmamalıdır.

x2 M2y2

(350 - x2) M2(1 - y2)

Benzer şekilde 3 nolu kısıtlayıcı fonksiyon yerine aşağıdaki eşitsizlikler çifti
yazılabilir.

x3 M3y3

(350 - x3) M3(1 - y3), y3 = 0 veya 1, M3 = 1375

Sonuçta, problemin tamsayılı programlama modeli aşağıdaki gibi olur.

Zenb = 5x1 + 3x2 + 4x3

x1 1100y1

(350 - x1) 1100(1 - y1)

x2 2000y2

(350 - x2) 2000(1 - y2)

x3 1375y3

(350 - x3) 1375(1 - y3)

20x1 + 11x2 + 16x3 22000

6x1 + 3x2 + 4.5x3 9000

x1, x2, x3 0

x1, x2, x3 tamsayı

y1, y2, y3 = 0 veya 1

Problemin en iyi çözümü, x2 = 2000, y2 = 1, x1 = x3 = y1 = y3 = 0, Zenb = 6
olarak belirlenmiştir.

İse-Olur Kısıtlayıcıları

Uygulamada sıkça karşılaşılan bir durum da, kısıtlayıcılardan birinin
gerçekleşmesinin başka bir kısıtlayıcının gerçekleşmesini sağlamasıdır. Bu
durum, f(x1, x2, ..., xn) 0 ise g(x1, x2, ..., xn) 0 eşitsizlikleri ile
açıklanır. Bu koşullarda dikkat edilmesi gerekli en önemli nokta, f(x1, x2, ...,
xn) 0 eşitsizliğinin gerçekleşmemesinin, g(x1, x2, ..., xn) 0 koşulunun da
gerçekleşmemesine yol açmayacağıdır. f(x1, x2, ..., xn) 0 eşitsizliği
sağlanmazsa, g(x1, x2, ..., xn) 0 veya g(x1, x2, ..., xn) \< 0 olabilir. Burada
amaç, f(x1, x2, ..., xn) 0 olması durumunda g(x1, x2, ..., xn) 0 olmasını
sağlayacak koşulların yaratılmasıdır.

Bu koşullar, problemin formülasyonuna 0-1 değerli y değişkeninin kullanıldığı ve
aşağıdaki gibi düzenlenen kısıtlayıcıların eklenmesiyle gerçekleştirilir.

\-g(x1, x2, ..., xn) My 5.3

f(x1, x2, ....,xn) M(1 - y) 5.4

Diğer bazı kısıtlayıcılarda olduğu gibi burada da M, problemin diğer
kısıtlayıcılarını gerçekleyen tüm x1, x2, ..., xn değerleri için f M ve -g M
olmasını sağlayacak büyüklükte bir pozitif sayıdır. Modele eklenen
kısıtlayıcıları inceleyelim. f 0 ise 5.4’ün sağlanması için y = 0 olması
gerektiği görülebilir. Bu durumda 5.3, -g 0 veya g 0 olmak üzere arzulanan
sonucu sağlar. O halde f 0 ise, 5.3 ve 5.4, g 0 olmasını sağlar. Diğer taraftan,
f 0 eşitsizliği gerçekleşmiyorsa 5.4, y = 0 veya y = 1 olmasına sebep olur. y =
1 olduğunu düşünelim. Bu durumda, 5.3 kendiliğinden sağlanır. f 0 sağlanmıyorsa,
x1, x2, ..., xn değişkenlerinin değerleri sınırlandırılmamış olduğundan g 0 veya
g 0 durumlarının her ikisi de olabilir.

Bu kısıtlayıcıların uygulamalardaki kullanımını açıklamak için kapsayan küme
problemlerine örnek olarak verdiğimiz probleme dönelim.

**Örnek 5.7**: Örnek 5.4’deki probleme, 3 nolu merkeze istasyon kurulmuşsa 2 ve
5 nolu merkezlere istasyon kurulamaz kısıtını ekleyiniz

**Çözüm 5.7**: 3 nolu merkeze istasyon kurulmuşsa x3 = 1 olur. 2 ve 5 nolu
merkezler için kullanılan değişkenler x2 ve x5 olduğundan, eklenecek kısıtlayıcı
matematiksel olarak aşağıdaki gibi açıklanabilir.

x3 = 1 ise x2 = x5 = 0 olur 5.5

xi sıfır-1 değişken olduğundan 5.5 ile açıklanan kısıt aşağıdaki gibi olur.

x3 0 ise x2 + x5 0 veya -x2 - x5 0 5.5

İse-olur kısıtlayıcıları ile ilgili açıklamalar doğrultusunda,

\-g(x1, x2, x3, x4, x5) = x2 + x5

f(x1, x2, x3, x4, x5) = x3

olarak tanımlandığında, 5.3 ve 5.4 nolu eşitsizliklerin kullanılmasıyla, 5.5
yerine y = 0 veya 1 olmak üzere aşağıdaki eşitsizlikler çifti konulabilir.

x2 + x5 My

x3 M(1 - y)

Hem -g hem de f’nin 2’den büyük olamayacağı dikkate alındığında, M = 2 seçiminin
uygun olduğu anlaşılır. M = 2 için,

x2 + x5 2y

x3 2(1 - y)

olarak belirlenen kısıtlayıcı fonksiyonlar modele yerleştirildiklerinde, 1 nolu
merkezin seçilmesi durumunda 2 ve 5 nolu merkezlerin seçilmemesi sağlanmış olur.

# 5.4. TAMSAYILI PROGRAMLAMA ÇÖZÜM YÖNTEMLERi

Tamsayılı doğrusal programlama problemlerinin çözümünde kullanılan belli başlı
yöntemler; dal-sınır algoritması ile Gomory kesme düzlemi algoritmasıdır.
Yöntemlerin her ikisi de doğrusal programlama için önerilen çözüm yöntemleri
üzerine kurulmuştur. Yöntemleri açıklamadan önce tamsayılı programlama
problemlerinin çözümü ile ilgili basit ama önemli bir konu üzerinde duralım.

Herhangi bir tamsayılı programlamanın gevşek biçiminin en iyi çözümünde tamsayı
olması istenen değişkenlerin hepsi tamsayı ise, bu çözüm tamsayılı
programlamanın da en iyi çözümü olur. Bu durumu aşağıdaki basit problemin çözümü
üzerinde gösterelim.

Zenb = 8x1 + 12x2

x1 + x2 3

x1, x2 0,

x1, x2 tamsayı

Gevşek problemin en iyi çözümü, x1 = 0, x2 = 3, Zenb = 36 şeklinde
belirlenmiştir. Gevşek problemin uygun çözüm bölgesi Şekil 5.2’de OAB üçgen
alanıyla, tamsayılı problemin çözüm noktaları ise () ile gösterilmiştir. Bu
noktaların koordinat değerlerini kullanarak tamsayılı programlamanın en iyi
çözümüne ulaşmaya çalışalım.

Şekil 5.2’den görüldüğü gibi, tamsayılı problemin çözümü olabilecek çözüm
noktaları şunlardır:

(0, 0), (0, 1), (0, 2), (0, 3), (1, 0), (2, 0), (3, 0), (1, 1), (1, 2), (2, 1).

Amaç fonksiyonuna en büyük değeri (Zenb = 36) kazandıran A(x1 = 0, x2 = 3),
tamsayılı problemin en iyi çözümüdür. Böylece, herhangi bir tamsayılı doğrusal
programlamanın gevşek biçiminin en iyi çözümünde tamsayı olması istenen
değişkenler tamsayı iseler, bu çözüm tamsayılı doğrusal programlama probleminin
de en iyi çözümüdür açıklaması kanıtlanmış olur.

**Şekil 5.2**

### 5.4.1. Dal-Sınır Algoritması

Dal-sınır algoritması hem tamamen tamsayılı hem de karma tamsayılı programlama
problemlerinin çözümünde kullanılabilen genel bir yaklaşımdır. Tamsayılı
programlama problemlerinin çözümünde kullanılan bilgisayar paket programlarının
çoğunda bu yaklaşım esas alınmıştır. Dal-sınır yöntemi, tamsayılı uygun
çözümlerin hepsinin sistematik biçimde listelendiği etkin bir yöntemdir.

Bilindiği gibi, tamsayılı problemlerin çözümünde kullanılabilecek pratik bir
yaklaşım, problemin doğrusal programlamaya dönüştürülmüş şeklini çözmek, çözüm
sonucu tamsayı olmayan değerleri yuvarlamak, yani tamsayıya dönüştürmektir. Bir
an için tamsayı olması istenen x1, x2 değişkenleri için, 2.5 ve 5.4 değerlerine
ulaştığımızı düşünelim. Bu durumda tamsayı çözüm için (2, 5), (2, 6), (3, 5),
(3, 6) olmak üzere dört seçenek vardır.

x1’in gerçek en iyi tamsayı çözümü bu aday çözümlerden hiçbirine karşılık
gelmeyebilir. x1 için 2’den küçük veya 3’den büyük olan tamsayı çözüm elde
edilebilir. x1 için tamsayı en iyi çözüm, x1 2 veya x1 3 koşulunu sağlamalıdır.
Benzer şekilde x2’nin gerçek en iyi tamsayı çözümü, x2 5 veya x2 6 olabilir.

Dal-sınır algoritmasının esaslarını sayısal bir örnek üzerinde açıklayalım.

**Örnek 5.8**: Aşağıdaki problemi dal-sınır algoritmasıyla çözünüz .

Zenb = 7x1 + 3x2

3x1 + 2x2 13

x1, x2 0

x1, x2 tamsayı

**Çözüm 5.8**: Dal-sınır algoritmasının ilk adımı tamsayılı problemi gevşetmek
(tamsayı olma koşulunu göz ardı etmek) ve bu problemin en iyi çözümünü
bulmaktır. Problemin normal doğrusal programlamaya dönüştürülmüş biçimi alt
problem 1 (AP-1) olarak isimlendirilir. AP-1’in en iyi çözümünde tamsayı olması
istenen değişkenler tamsayı iseler, bu çözüm tamsayı problemin de en iyi çözümü
olur. AP-1 için en iyi çözüm, x1 = 4.33, x2 = 0, Zenb = 30.333 (bkz. Şekil 5.3)
olarak elde edilmiştir.

**Şekil 5.3**

AP-1’in en iyi çözümü tamsayılı olmadığından dal sınır algoritmasıyla orijinal
problemin en iyi çözümü bulununcaya kadar çözüm bölgesinin düzenlenmesine devam
edilir. Daha önce açıklandığı gibi, en büyükleme amaçlı bir tamsayılı problemin
en iyi Z değeri ile gevşek biçiminin en iyi Z değeri arasında,

**Tamsayılı programlamanın en iyi Z değeri  Gevşek Biçimin en iyi Z değeri**

eşitsizliği ile açıklanan bir ilişki vardır.

Bu ilişki, bu tamsayılı problemin amaç fonksiyonunun en büyük değerinin
30.333’den büyük olamayacağını açıklamaktadır. Bu durumda, 30.333 tamsayılı
programlama probleminin en iyi çözümü için üst sınır kabul edilir. Algoritmanın
ismindeki sınır sözcüğü buradan gelmektedir.

Yöntemin yeni adımı, gevşek problemin çözüm bölgesini parçalara ayırmaktır. Bu
yolla tamsayılı problemin en iyi çözümünün araştırılacağı alan küçültülmüş olur.
Parçalama işleminde, tamsayı olması istenen ama tamsayı olmayan değişkenlerin
seçilmesi esastır. Gevşek biçimin en iyi çözümünde x2 tamsayı olduğundan,
parçalama işlemi için tamsayı olmayan x1’in seçilmesi gerekir. x1’in tamsayı
olmayan (4.333) çözüm değerine en yakın iki tamsayı 4 ve 5’dir. Tamsayılı
programlamanın çözüm bölgesindeki her nokta x1 4 veya x1 5 koşulunu
sağlamalıdır. Bu ikiye ayırma koşulu dallanma kavramının öne çıkmasına neden
olur. x1 4 veya x1 5 şeklindeki parçalama işlemi 4.333 değerine ikinci kez
rastlama şansını ortadan kaldırır. Kısaca, x1 4 veya x1 5 belirlemesiyle, yani
x1’in dallandırılmasıyla gevşek biçimin çözüm bölgesi iki parçaya ayrılmış olur.
Parçalar aşağıda tanımlanmış olan farklı alt problemlere karşılık gelir.

AP-2: AP-1 + x1 4

AP-3: AP-1 + x1 5

Özetle AP-1, biri AP-2 diğeri AP-3 olmak üzere iki problemle yer değiştirmiştir.
Ne AP-2 ne de AP-3 x1 = 4.333 değerini içerir. Şekil 5.4’de gösterildiği gibi
gevşek biçimin en iyi çözümü bir daha ortaya çıkamaz.

**Şekil 5.4**

Orijinal problemin en iyi çözümü ya AP-2’de veya AP-3’dedir. Dolayısıyla bu
problemler çözülmelidir. Önce hangi alt problemin çözülmesi gerektiği konusunda
genel bir kural bulunmamakla birlikte eğilim, en yeni alt problemin seçilmesi
yönündedir. Bu nedenle önce AP-3’ü çözelim. Şekilden görüldüğü gibi, AP-3’ün
çözüm bölgesi ile AP-1’in çözüm bölgesinin hiçbir ortak noktası olmadığından
AP-3’den elde edilecek herhangi bir çözüm uygun olmayacaktır. Bu nedenle,
AP-3’den hareketle belirlenecek bir çözüm en iyi olamaz. Bunu ifade etmek için
uygun çözümü olmayan alt problemler ile işaretlenir (bkz. Şekil 5.5). AP-3’ün
dallandırılması tamsayı çözüm hakkında bilgi sağlamayacağından, bundan sonraki
işlemlerde AP-3’ün dikkate alınmasına gerek yoktur. AP-2’ye geçelim. AP-2’nin en
iyi çözümü; x1 = 4, x2 = 0.5 ve Zenb = 29.5 olarak belirlenmiştir.

Şu ana kadar yapılanlar Şekil 5.5’de özetlenmiştir. Görüldüğü gibi her bir alt
probleme bir düğüm, alt problem yaratmada kullanılan her bir kısıtlayıcıya bir
dal karşılık gelmektedir. Bir alt problemi diğerinden ayıran kısıtlayıcı, ilgili
alt problemler arasındaki dal üzerine yazılmaktadır. Ayrıca alt problemlerin
hangi sırada çözüldükleri düğümlerin yan taraflarına t = sıra no şeklinde
belirtilmektedir.

**Şekil 5.5**

AP-2’nin en iyi çözümünde; x2 tamsayı olmadığından, x2 dallandırma değişkeni
olur. Dallandırma ile AP-2’nin uygun çözüm bölgesi, x2 0 ve x2 1 noktalarını
kapsayan iki bölgeye ayrılır.

Bu yolla yaratılan yeni problemler (AP-4 ve AP-5) aşağıda ve bunların çözüm
bölgeleri Şekil 5.6’da gösterilmiştir.

AP-4: AP-1 + x1 4 + x2 0 = AP-2 + x2 0

AP-5: AP-1 + x1 4 + x2 1 = AP-2 + x2 1

Çözülmemiş problemler AP-4 ile AP-5’dir. Çözüm için en yeni olan AP-5
seçilecektir.

**Şekil 5.6**

AP-5’in en iyi çözümü; x1 = 3.667, x2 = 1 ve Zenb = 28.667’dir.

Alt problemler ve çözüm sonuçları Şekil 5.7’de gösterilmiştir.

**Şekil 5.7**

AP-5’in çözümünde x1 tamsayı olmadığından, (x1 = 3.667) AP-4’ü çözmeden önce x1
dallandırılır. x1 3’le belirlenen AP-6 ve x1 4’le belirlenen AP-7 aşağıda
gösterilmiştir.

AP-6: AP-1 + x1 4 + x2 1 + x1 3 = AP-5 + x1 3

AP-7: AP-1 + x1 4 + x2 1 + x1 4 = AP-5 + x1 4

AP-6 ve AP-7’nin uygun çözüm bölgeleri Şekil 5.8’de gösterildiği gibidir.

**Şekil 5.8**

İkisi yeni (AP-6 ve AP-7), diğeri önceden tanımlanmış ve hala çözülmemiş olan
(AP-4) üç alt problem vardır. Yukarıda açıklandığı gibi alt problemlerin
çözümüne en yeni olandan başlanır. En yeni olanlar arasından seçim rastgele
yapılır. Biz AP-6’yı seçelim. AP-6’nın en iyi çözümü x1 = 3, x2 = 2 ve Zenb = 27
olarak belirlenmiştir (bkz. Şekil 5.9). Çözümde değişkenler tamsayı
olduklarından AP-6’dan sağlanan çözüm tamsayılı problemin en iyi çözümü olmaya
adaydır. Z’nin 27 olarak belirlenen değeri, bundan sonra çözülecek alt
problemlerin Z değerleri için bir alt sınır oluşturur. Yani, bu aşamadan sonra
elde edilecek bir çözümün en iyi olabilmesi için Z değeri en az 27’ye eşit
olmalıdır.

Çözülmemiş iki alt problemin daha bulunduğu bu aşamada, son giren ilk çıkar
kuralı doğrultusunda, AP-7 seçilmelidir. AP-7’nin çözümü uygun olmadığından,
çözülmemiş tek alt problem olan AP-4’e geçilir. AP-4’ün en iyi çözümü x1 = 4, x2
= 0 ve Zenb = 28 olarak belirlenmiştir. Bu çözüm de (değişkenler tamsayı
olduğundan) tamsayılı problemin en iyi çözümü olmaya adaydır. Ayrıca AP-4 için
belirlenen Z = 28 değeri AP-6 için belirlenen çözümün en iyi olmadığına işaret
etmektedir. İki aday çözümün belirlendiği bu problemde en büyük Z değerini veren
çözüm AP-4’ün çözümüdür.

Tüm alt problemler ve çözümleri Şekil 5.9’da özetlenmiştir.

**Şekil 5.9**

Dal sınır algoritmasını bir kez de bir sıfır-1 programlama problemi üzerinde
açıklayalım. Sıfır-1 programlamada her değişken ya sıfır veya 1’e eşit
olduğundan, değişken dallandırılması xi = 1 ve xi = 0 şeklindedir. Bu özellik,
yöntemin uygulanmasında büyük kolaylık sağlar. Öyleki, problemin doğrusal
programlama gevşeği dahil tüm alt problemleri ve bu problemlerin çözümleri basit
bir incelemeyle belirlenebilirler.

Bu açıklamalar doğrultusunda aşağıdaki sırt çantası problemini çözelim.

**Örnek 5.9**: Otostopçu bir genç taşıma kapasitesi 5 kg olan bir sırt çantasına
ağırlıkları farklı 4 eşyayı yerleştirmek istemektedir. Her eşyanın birim
ağırlığı (kg) ve sağladığı kazanç aşağıdaki gibidir. Buna göre 5 kg’lık sırt
çantasına hangi eşyalar yerleştirildiğinde toplam kazanç en büyük olur.

**Tablo 5.8**

| Eşya No | Ağırlık  | Kazanç |
|---------|----------|--------|
| 1       | 3        | 20     |
| 2       | 2        | 16     |
| 3       | 2        | 10     |
| 4       | 1        | 8      |

**Çözüm 5.9**: Çözüme geçmeden önce problemin sıfır-1 programlama modelini
kuralım. Kurulan model aşağıda gösterilmiştir.

Zenb = 20x1 + 16x2 + 10x3 + 8x4

3x1 + 2x2 + 2x3 + x4 5

xi = 0 veya 1 (i = 1, 2, 3, 4)

Ürün kazanç değerleri incelendiğinde akla ilk gelen, çantaya en önce kazanç
değeri en büyük olan 1 nolu eşyayı yerleştirilmektir. Ancak, ağırlıkları göz
ardı edip yalnızca kazançların dikkate alınmasıyla gerçekleştirilecek bir
yerleştirme planı en iyi olmayabilir. Kazanç ile ağırlık arasında bir ilişki
kurmak, yerleştirme planını bu ilişki bazında oluşturmak uygun olur. Amaç
fonksiyonu katsayıları Ci, kısıtlayıcı fonksiyon katsayıları ai olmak üzere i
nolu eşyadan beklenen fayda (Ci / ai) olarak açıklanabilir. Fayda katsayısı en
büyük olan eşya çantaya ilk yerleştirilecek olandır. Çantada kalan boş yer
kapasitesine bağlı olarak sırasıyla fayda katsayısı ikinci, üçüncü, dördüncü
sırada olan eşyalar yerleştirilir. Gevşek problemi bu açıklamaları kullanarak
çözelim. Önce fayda katsayılarını hesaplayalım ve eşyaları fayda katsayılarının
büyüklüğüne göre sıralayalım. Fayda katsayıları ve eşyaların önem dereceleri
Tablo 5.9’da gösterilmiştir. Tablodan görüldüğü gibi 2 ve 4 nolu eşyaların
sıralama dereceleri 1.5’dir. Bunun nedeni, bu eşyaların fayda katsayılarının
eşit olması sonucu, sıralama derecelerinin 1 ile 2’nin ortalaması olarak
alınmasıdır.

**Tablo 5.9**

|  Eşya | Fayda Ci /ai  | Sıralama  (1 = En iyi, 4 = En kötü) |
|-------|---------------|-------------------------------------|
| 1     | 20/3          | 3                                   |
| 2     | 16/2          | 1.5                                 |
| 3     | 10/2          | 4                                   |
| 4     | 8/1           | 1.5                                 |

Sıra değerleri incelendiğinde, yerleştirilecek ilk eşyanın eşit sıralama
katsayılı, yani faydaları aynı olan 2 veya 4 nolu eşya olduğu görülecektir. Eşya
2 seçilmiş olsun. Bu durumda x2 = 1 olur. Bu eşyanın yerleştirilmesiyle çantada
3 kg’lık boş yer kalır. Bu durumda orijinal problem, 3 kg taşıma kapasiteli
çantaya 1, 3 ve 4 nolu eşyaların yerleştirilmesi problemine dönüşmüş olur.
Sıralamada 2 nolu eşya ile aynı yeri paylaşan 4 nolu eşyanın ağırlığı 1 kg
olduğundan çantaya yerleştirilen ikinci eşya 4 nolu olandır. Bu durumda x4 = 1
olur. 2 ve 4 nolu eşyaların yerleştirilmesinden sonra çantada 2 kg’lık boş yer
kalır. Sıralamada 3. sırada bulunan eşya 1’in ağırlığı 3 kg olduğundan x1 = 2/3
olur. 3 nolu eşya için yer kalmamıştır (x3 = 0) . Böylece tamsayı olmayan en iyi
çözüm; x1 = 2/3 , x2 = 1, x3 = 0, x4 = 1 ve Zenb = 37.333 olarak belirlenmiş
olur. Tamsayı olmayan bu çözümün, gevşek formun en iyi çözümü olduğu
unutulmamalıdır. Tamsayılı en iyi çözüme ulaşmak için x1 dallandırılmalıdır. x1
= 0 veya 1 olduğundan, dallandırma x1 = 1 ve x1 = 0 şeklinde yapılır.
Dallandırmayla belirlenen problemler ve çözüm sonuçları Şelil 5.10’da
gösterilmiştir.

**Şekil 5.10**

Şekilden görüldüğü gibi, sıfır-1 tamsayılı problemin en iyi çözümü üçüncü sırada
çözülen AP-3’den elde edilmiştir.

Bilindiği gibi karma tamsayılı programlama problemlerinde değişkenlerden
bazıları tamsayıdır. Bu tip problemler de dal-sınır algoritmasıyla çözülebilir.
Bu kez, dallandırma için yalnızca tamsayı olması istenen değişkenlerin dikkate
alınması yeterli olur. Tamsayı olması gerekmeyen değişkenler hiçbir zaman
dallandırma değişkeni olarak seçilmezler.

Konuyu açıklamak için aşağıdaki karma tamsayılı programlama probleminin çözümünü
araştıralım. Bu kez en küçükleme amaçlı bir problem çözülecektir.

**Örnek 5.10**: Aşağıdaki karma tamsayılı programlama problemini dal-sınır
algoritmasıyla çözünüz.

Zenk = 6x1 + 7x2

6x1 + 3x2 40

3x1 + 2x2 11

x1, x2 0

x1 tamsayı

**Çözüm 5.10**: Tamamen tamsayılı programlama problemlerinin çözümünde olduğu
gibi, öncelikle problem gevşetilmeli ve gevşek problemin en iyi çözümü
bulunmalıdır.

Gevşek biçimin en iyi çözümü; x1 = 6.667, x2 = 0 ve Zenk = 40 olarak
bulunmuştur. 40 olarak belirlenen Z değerinin tamsayılı problemin en iyi çözümü
için bir alt sınır oluşturduğu unutulmamalıdır. Problem en küçükleme amaçlı
olduğundan, orijinal problemin en iyi Z değeri en az 40 olacaktır.

Tamsayı olması istenen değişken x1 olduğundan, dallandırma x1 üzerinde
gerçekleştirilecektir. x1’in tamsayı olmasını sağlayacak dallandırma, x1 6 ve x1
7 şeklindedir.

Bu dallandırma ile,

AP-2: AP-1 + x1 6

AP-3: AP-1 + x1 7

yazılır.

Çözülecek alt problem olarak AP-3’ü seçelim. AP-3’ün çözümünde; x1 = 7, x2 = 0
ve Zenk = 42 olarak belirlenmiştir. Çözümde x1 tamsayı olduğundan AP-3’ün çözümü
tamsayılı problemin en iyi çözümü olmaya adaydır. Ayrıca orijinal problemin en
iyi (en küçük) değeri konusunda Z = 42’nin bir üst sınır olduğu söylenebilir.

Yeni bir dallandırma gerekmediğinden, AP-2’ye geçilir. AP-2’nin en iyi çözümü;
x1 = 6, x2 = 1.333 ve Zenk = 45.333 olarak belirlenmiştir. x1 tamsayı
olduğundan, bu çözüm de en iyi olma şansına sahiptir. Bununla birlikte AP-2’den
hesaplanan Z değeri (45.333), AP-3’ten hesaplanan Z değerinden (42) büyük
olduğundan bir en iyi çözüm olamaz. AP-3 tamsayılı programlamanın en iyi
çözümünü sağlamıştır.

Yaratılan alt problemler ve çözümleri aşağıdaki şekilde gösterilmiştir.

**Şekil 5.11**

**5.4.2. Kesme Düzlemi Algoritması**

Tamsayılı programlama problemlerinin çözümünde kullanılan diğer bir teknik kesme
düzlemi algoritmasıdır. Dal-sınır algoritmasında olduğu gibi, kesme düzlemi
algoritması uygulamasına da tamsayılı problemin gevşetilmiş biçiminin en iyi
çözümüyle başlanır. Bu en iyi çözümde, tamsayı olması istenen değişkenler
tamsayı iseler tamsayılı problem çözülmüş olur. Gevşek problemin en iyi çözümü
tamsayılı programlamanın en iyi çözümü olma özelliğini taşımıyorsa, kesme
düzlemi algoritması uygulamasına geçilebilir. Kesme düzlemi algoritmasında da,
dal-sınır algoritmasında olduğu gibi, tekrarlı bir şekilde özel kısıtlayıcılar
ekleyerek çözüm uzayında gerekli düzeltmeler yapılır. Özel kısıtlayıcı ekleme
işlemi tamsayı olma koşulunu gerçekleyecek bir en iyi çözüme ulaşılıncaya değin
sürdürülür.

Kesme düzlemi algoritmasının nasıl kullanılacağını dal-sınır yöntemi ile çözülen
örnek 5.8’deki problem üzerinde açıklayalım.

**Örnek 5.11**: Aşağıdaki problemi kesme düzlemi algoritmasıyla çözünüz.

Zenb = 7x1 + 3x2

2x1 + x2 9

3x1 + 2x2 13

x1, x2 0

x1, x2 tamsayı

**Çözüm 5.11**: Kesme düzlemi algoritması klasik doğrusal programlama
probleminin simpleks yöntemle elde edilen en iyi çözüm tablosundan işe başlar.
Tamsayı olma koşulunun göz ardı edilmesiyle belirlenen gevşek problemin en iyi
çözümünün yer aldığı simpleks çözüm tablosu aşağıda gösterilmiştir.

**Tablo 5.10**

| TDV     | x1 | x2     | S1 | S2     | ÇV     |
|---------|----|--------|----|--------|--------|
| S1      | 0  | -0.333 | 1  | -0.667 | 0.333  |
| x1      | 1  |  0.667 | 0  |  0.333 | 4.333  |
| Zj      | 7  |  4.669 | 0  |  2.331 | 30.333 |
| Zj - Cj | 0  |  1.669 | 0  |  2.331 | -      |

Elde edilen en iyi çözümde, x2 (= 0) tamsayı olmakla birlikte, x1 (= 4.333)
tamsayı olmadığından bu çözüm aranan en iyi çözüm olamaz. Tamsayılı
programlamanın en iyi çözümü için ek bir kısıtlayıcı koşul yaratılması gerekir.
Bunun için öncelikle tamsayı olması istenen ancak çözüm değeri tamsayı olmayan
değişken(ler) belirlenir. Birden fazla değişken arasından seçim yapılacak olması
durumunda, kesirli kısmı en büyük olan değişkenin seçilmesi uygun olur. Tamsayı
yapılacak değişkenin belirlenmesinden sonra en iyi çözümün bulunduğu simpleks
tablosundan o değişkenin bulunduğu satır elemanları işaretlenir. İşaretlenen bu
elemanlar kısıtlayıcı koşul yaratmada kullanılır. Burada yalnızca x1 değişkeni
temelde bulunduğundan, bu değişkene ilişkin kısıtlayıcı koşul yaratılacağı
açıktır. Tablo 5.10’daki sonuç değerlerinden yaratılan denklem aşağıda
gösterilmiştir.

(1)x1 + (0.667)x2 + (0)S1 + (0.333)S2 = 4.333 5.6

Kısıtlayıcı koşul yaratmada gerçekleştirilen işlemleri genelleştirmek için şu
tanımı yapalım. x, x’e eşit veya daha küçük en büyük tamsayı olsun. Buna göre,
sözgelimi 2.25 = 2, -3.16 = -4 olur. Bu durumda herhangi bir kesirli sayı x + f
olarak açıklanabilir. Buradaki f, x’in tamsayı olmayan, yani kesirli kısmıdır.
Sözgelimi, 2.25 = 2 + 0.25 ve -3.16 = -4 + 0.84 olarak yazılabilir. Kesirli bir
sayının bu biçimde ifade edilmesi kısıtlayıcı koşul yaratmanın esasını
oluşturur. Bu açıklamalar doğrultusunda 5.6’nın tamsayı olmayan değişken
katsayılarını "x + f" formunda yazalım. Buna göre,

(1 + 0)x1 + (0 + 0.667)x2 + (0)S1 + (0 + 0.333)S2 = 4 + 0.333

veya

(1 + 0)x1 + (0)x2 + (0.667)x2 + (0)S1 + (0)S2 + (0.333)S2 = 4 + 0.333

olur.

Katsayıları tamsayı olan bütün terimlerin eşitliğin sol tarafında, diğerlerinin
eşitliğin sağ tarafında gösterilmesiyle ulaşılan eşitlik aşağıda gösterilmiştir.

(1)x1 + (0)x2 + (0)S1 + (0)S2 - 4 = 0.333 - (0.667)x2 - (0.333)S2 5.7

5.7’nin sağ tarafı için,

0.333 - (0.667)x2 - (0.333)S2 0 5.8

yazılabilir.

5.8 ile açıklanan fonksiyona "kesme" denir. Kesme düzlemi algoritmasının esasını
oluşturan kesmenin iki önemli özelliği aşağıda açıklanmıştır.

1\. Tamsayılı programlama için uygun olan bir nokta kesmeyi sağlar

2\. Gevşek biçim için en iyi olduğu belirlenen nokta kesmeyi sağlamaz.

Bu iki özelliğinden dolayı bir kesme, gevşek problemin en iyi çözümünü dışta
bırakırken, tamsayılı programlamanın uygun çözümlerine dokunmaz. Kesme
oluşturmada kullanılan değişkenin tamsayıya ulaştırılabilmesi için kesmenin,
gevşek biçimin en iyi çözümünün bulunduğu simpleks tablosuna yeni bir
kısıtlayıcı olarak eklenmesi gerekir. Bu eklemeden sonra simpleks yöntemin
klasik işlemleriyle tamsayı en iyi çözüm elde edildiğinde, problem çözülmüş
olur. Kesme eklenmesiyle düzenlenen problemin en iyi çözümünde hala tamsayı
olmayan değişken var ise, yeni bir kesme tanımlanır. Bu işlemler istenen çözüme
ulaşıncaya kadar tekrarlanır. Sınırlı sayıda kesme ile tamsayı en iyi çözüme
ulaşılır. Gevşek probleme kesme eklenmesi ve sonrasında yapılan işlemlere
geçmeden önce kesmenin yukarıda açıklanan iki özelliği gerçekleyip
gerçeklemediği konusu üzerinde duralım.

Önce birinci özellik üzerinde duralım. Bu amaçla tamsayılı programlama için
uygun olan bir nokta seçelim. Bu noktada x1 ve x2 tamsayı değerler alacaktır.
Tamsayılı programlama için uygun olan bu nokta gevşek problem için de uygundur.
5.7 nolu denklem, en iyi çözüm tablosunun x1 değişken satırının amaca uygun
olarak düzenlenmiş biçimi olduğundan, tamsayılı programlama için uygun olan
nokta 5.7’yi sağlamak zorundadır. Tamsayılı programlamanın uygun bir çözümünde,
S1 0 ve S2 0 olmak zorundadır. 0.333 \< 1 olduğundan, tamsayılı programlamanın
uygun herhangi bir çözümü için 5.7’nin sağ tarafı 1olur. Ayrıca böyle bir nokta
için 5.7’nin sol tarafı bir tamsayıya eşittir. Sonuç olarak, tamsayılı
programlamanın herhangi bir uygun çözümü için, 5.7’nin sağ tarafı 5.6 ile
belirlenenden küçük bir tamsayıdır.

Şimdi de gevşek problemin en iyi çözümünün kesmeyi sağlamayacağını gösterelim.
Gevşek problemin en iyi çözümünde, x2 = 0, S2 = 0 olarak belirlenen değerleri
5.8 nolu eşitsizlikle açıklanan kesme denklemine yerleştirelim. Bu durumda,

0.333 - (0.667)(0) - (0.333)(0) = 0.333

elde edilir.

0.333 \> 0 olduğundan kesme tatmin edilmemiş, yani gevşek biçimin en iyi çözümü
kesmeyi sağlamamıştır.

İstenirse kesmenin grafiği çizilebilir. Anılan grafiği çizmek için kesme
denkleminin x1, x2 cinsinden yazılması gerekir. İkinci kısıtlayıcıdan S2 için
belirlenen 13 - 3x1 - 2x2 bağıntısı, 5.8’le açıklanan kesme denklemine
yerleştirildiğinde sırasıyla,

0.333 - (0.667)x2 - (0.333)(13 - 3x1 - 2x2) 0

0.333 - (0.667)x2 - 4.329 - (0.999)x1 - (0.666)x2 0

0.333 - (0.667)x2 - 4.329 + (0.999)x1 + (0.666)x2 0

(0.999)x1 4

elde edilir. Buna göre kesme Şekil 5.12’deki gibi çizilir.

**Şekil 5.12**

Kesmenin en iyi çözüm tablosuna yerleştirilmesi için önce sağ tarafında sabit
olacak biçimde, yani (-0.667)x2 - (0.333)S2 -0.333 olarak yazılması, daha sonra
sol tarafına bir aylak değişken (S3) ekleyerek eşitlik biçimine dönüştürülmesi
gerekir. Açıklanan bu işlemlerin tamamlanmasıyla,

(- 0.667)x2 - (0.333)S2 + (1) S3 = - 0.333

elde edilir.

Kesmenin eklenmesiyle elde edilen simpleks çözüm tablosu aşağıda gösterilmiştir.

**Tablo 5.11**

| TDV     | x1 | x2     | S1 | S2     | S3 | ÇV     |
|---------|----|--------|----|--------|----|--------|
| S1      | 0  | -0.333 | 1  | -0.667 | 0  | 0.333  |
| x1      | 1  |  0.667 | 0  |  0.333 | 0  | 4.333  |
| S3      | 0  | -0.667 | 0  | -0.333 | 1  | -0.333 |
| Zj      | 7  | 4.669  | 0  |  2.331 | 0  | 30.333 |
| Zj - Cj | 0  | 1.669  | 0  |  2.331 | 0  | -      |

Tablo 5.11’den görüldüğü gibi eklenen kesme çözümün en iyi olma olma özelliğini
(tüm Zj – Cj 0) etkilememiştir. Ancak, S3’ün negatif olması çözümün uygun
olmamasına yol açmıştır. Uygun çözüm için dual simpleks yöntem([^1])
uygulanmalıdır. Dual simpleks yöntemin değişken seçimi kuralına göre S3 temeli
terkedecek, en küçük oran veren x2 girecektir. Simpleks çözümün ardışık
işlemleriyle oluşturulan tablo aşağıda gösterilmiştir.

[^1]: Uygun olmayan en iyi çözümlü problemlere uygulanan dual simpleks yöntemle
    ilgili ayrıntılı bilgi için bkz: Yılmaz Tulunay, Matematik Programlama ve
    İşletme Uygulamaları, İstanbul, 1991, s.431.; Nalan Cinemre, Doğrusal
    Programlama, Yayınlanmamış Ders Notu, s.162.

Tablo 5.12

| TDV     | x1 | x2 | S1 | S2     | S3     | ÇV     |
|---------|----|----|----|--------|--------|--------|
| S1      | 0  | 0  | 1  | -0.501 | -0.499 | 0.499  |
| x1      | 1  | 0  | 0  | 0      | 0.999  | 4.0    |
| x2      | 0  | 1  | 0  | 0.499  | -1.499 | 0.499  |
| Zj      | 7  | 3  | 0  | 1.497  | 2.496  | 29.497 |
| Zj - Cj | 0  | 0  | 0  | 1.497  | 2.496  | -      |

Tablo 5.12’deki çözüm hem en iyi hem de uygun olmakla birlikte x2 = 0.5
olduğundan, tamsayılı değildir. x2’nin esas alınmasıyla yeni bir kesme
tanımlanması zorunludur.

Kesmenin oluşturulması ve çözüm için uygun şekle dönüştürülmesi ile ilgili
işlemler aşağıda gösterilmiştir.

(0)x1 + (1)x2 + (0)S1 + (0.499)S2 (- 1.499)S3 = 0.499

(0.499)S2 + (0.501)S3 = 0.499

(0.499) - (0.499)S2 - (0.501)S3 0

(-0.499)S2 - (0.501)S3 -0.499

(-0.499)S2 - (0.501)S3 +(1) S4 = -0.499

Bu kısıtlayıcı koşulun en iyi çözüm tablosuna eklenmesiyle yeni çözüm tablosu
aşağıdaki gibi elde edilir.

**Tablo 5.13**

| TDV     | x1 | x2 | S1 | S2     | S3     | S4 | ÇV     |
|---------|----|----|----|--------|--------|----|--------|
| S1      | 0  | 0  | 1  | -0.501 | -0.499 | 0  | 0.499  |
| x1      | 1  | 0  | 0  | 0      | 0.999  | 0  | 4.0    |
| x2      | 0  | 1  | 0  | 0.499  | -1.499 | 0  | 0.499  |
| S4      | 0  | 0  | 0  | -0.499 | -0.501 | 1  | -0.499 |
| Zj      | 7  | 3  | 0  | 1.497  | 2.499  | 0  | 29.497 |
| Zj - Cj | 0  | 0  | 0  | 1.497  | 2.499  | 0  | -      |

Tablo 5.13’den görüldüğü gibi çözüm en iyi olmakla birlikte uygun değildir.
Negatif çözüm değerli S4’ün temelden çıkması, yerine mutlak değerce en küçük
oranı veren S2’nin girmesi gerekir. Gerekli işlemlerden sonra aşağıdaki tabloda
gösterilen yeni çözüme ulaşılır.

**Tablo 5.14**

| TDV     | x1 | x2 | S1 | S2 | S3     | S4    | ÇV    |
|---------|----|----|----|----|--------|-------|-------|
| S1      | 0  | 0  | 1  | 0  | 0      | -1    | 0.999 |
| x1      | 1  | 0  | 0  | 0  | 0.999  | 0     | 4.0   |
| x2      | 0  | 1  | 0  | 0  | -1.998 | 0.998 | 0     |
| S2      | 0  | 0  | 0  | 1  | 1.0    | -2    | 1.0   |
| Zj      | 7  | 3  | 0  | 0  | 0.999  | 2.994 | 28.0  |
| Zj - Cj | 0  | 0  | 0  | 0  | 0.999  | 2.994 | -     |

Tablo 5.14’de sunulan çözümde x1 ve x2 tamsayı bulunmuşlardır. Böylece tamsayı
çözüme ulaşılmıştır. Kesme düzlemi algoritması ile ulaşılan çözümde, x1 = 4, x2
= 0, Zenb = 28 dir. Böylece dal-sınır yöntemi ve kesme düzlemi algoritması çözüm
sonuçları aynı olmaktadır.

Dal-sınır ve kesme düzlemi algoritmalarının hangisinin tercih edileceği
konusunda genel kabul görmüş bir kanı olmadığını belirtmeliyiz. İki yöntemden
hiçbiri, sürekli daha iyi (az işlem, kısa zaman) sonuç vermemektedir. Yine de
deneyimler, dal-sınır algoritmasının daha başarılı olduğunu göstermektedir.

**PROBLEMLER**

**1**. FB basketbol takımı koçu ilk beş oyuncuyu belirlemek istemektedir. Koçun
elinde her biri farklı özellikte yedi oyuncu vardır. Oyuncuların her birinin top
tutma, şut atma, geri sekme ve savunma yetenekleri gözlenmiş ve yetenekleri
derecelendirilmiştir. 1 kötüye, 2 iyiye, 3 mükemmele karşılık gelmek üzere her
bir oyuncu için belirlenen dereceler ile oyuncuların takım içindeki pozisyonları
aşağıdaki tabloda gösterilmiştir.

| Oyuncu | Pozisyon          | Top Tutma | Şut Atma | Geri Sekme | Savunma |
|--------|-------------------|-----------|----------|------------|---------|
| 1      | Pota Altı         | 3         | 3        | 1          | 3       |
| 2      | Orta              | 2         | 1        | 3          | 2       |
| 3      | Pota Altı - İleri | 2         | 3        | 2          | 2       |
| 4      | İleri - Orta      | 1         | 3        | 3          | 1       |
| 5      | Pota Altı - İleri | 1         | 3        | 1          | 2       |
| 6      | İleri - Orta      | 3         | 1        | 2          | 3       |
| 7      | Pota Altı - İleri | 3         | 2        | 2          | 1       |

Oyunu başlatacak ilk 5 oyuncunun aşağıdaki koşulları sağlaması istenmektedir.
Takımın savunma yeteneğini en büyüklemekte kullanılacak modeli düzenleyiniz.

**a**. Pota altı pozisyonuna uygun en az 4 oyuncu olmalıdır. En az 2 oyuncu
ileri oynayabilmeli, en az 1 orta oyuncusu bulunmalıdır.

**b**. Takımın top tutma, şut atma ve geri sekme ortalaması en az 2 olmalıdır.

**c**. 3 nolu oyuncu ilk 5’de ise, 6 nolu oyuncu ilk 5 arasında bulunmamalıdır.

**d**. 1 nolu oyuncu ilk 5 arasındaysa, 4 ve 5 nolu oyuncuların her ikisi ilk 5
arasında bulunmalıdır.

**e**. 2 veya 3 nolu oyuncu ilk 5 arasında bulunmalıdır.

**2.** Yöneylem Araştırması Bölüm mezunu olabilmek için en az iki matematik, iki
yöneylem araştırması, iki de bilgisayar dersi almak gerekmektedir. İsimleri
matematik, yöneylem araştırması, bilgisayar olmamakla birlikte bazı dersler bu
derslerin yerine geçebilmektedir. Analize giriş, matematik yerine; yöneylem
araştırması matematik ve yöneylem araştırması yerine; veri tabanı düzenlemesi,
bilgisayar ve matematik yerine; işletme istatistiği, matematik ve yöneylem
araştırması yerine; simülasyon, yöneylem ve bilgisayar yerine; bilgisayara
giriş, bilgisayar yerine; tahmin yöntemleri, yöneylem araştırması ve matematik
yerine geçmektedir.

Bazı dersler ön koşulludur. İşletme istatistiği için analize giriş; simülasyon
ve veri tabanı düzenlemesi için bilgisayara giriş; tahmin yöntemleri için
işletme istatistiği dersleri önceden alınması gereken derslerdir.

En az sayıda ders alarak mezun olmayı sağlayacak tamsayılı doğrusal programlama
modelini kurunuz

**3.** Çevre halkına içme suyu sağlayan bir baraj gölünde insan sağlığı için
tehlikeli iki madde (A ve B) bulunmaktadır. Gölün bu maddelerden temizlenmesi
için kontrol istasyonları kurulması kararlaştırılmıştır. Kontrol istasyonu için
üç ayrı yer (I, II, III) düşünülmektedir.

Suyun temiz sayılabilmesi için yasa gereği en az 800 ton A, en az 500 ton B’nin
sudan çıkarılması gerekmektedir. Problemle ilgili olarak bilinmesi gerekenler
aşağıdaki tabloda verilmiştir. Yasa gereğini en düşük maliyetle sağlayacak
istasyon yerleşim planını belirleyiniz.

|      |  Maliyetler (TL)        | 1 Ton Sudan Çıkarılan Tehlikeli Madde Miktarı (ton) |      |      |
|------|-------------------------|-----------------------------------------------------|------|------|
|  Yer | İstasyon Kurma Maliyeti | 1 Ton Su İşleme Maliyeti                            |  A   |  B   |
| I    | 100000                  | 20                                                  | 0.40 | 0.30 |
| II   |  60000                  | 30                                                  | 0.25 | 0.20 |
| III  |  40000                  | 40                                                  | 0.20 | 0.25 |

**4.** Bir üretici firma birim kârları sırasıyla 2 ve 5 TL olan iki ürün (I, II)
üretmeyi planlamaktadır. Bir birim I üretimi için 3 birim, bir birim II üretimi
için 6 birim hammadde gerekmektedir. Toplam hammadde miktarı 120 birimdir. I’in
hazırlık maliyeti 10 TL, II’nin hazırlık maliyeti 20 TL’dir. Kârın en
büyüklenmesine yönelik tamsayılı programlama modelini kurunuz.

**5.** Büyük bir kuruluş Ege, Marmara ve Batı Karadeniz bölgelerinin istemlerini
karşılamak için İstanbul, Bursa, Zonguldak ve İzmir’e depo kurmayı
düşünmektedir. Her bir deponun yükleme kapasitesi 100 birimdir. Depo işletme
maliyeti bulunduğu şehre bağlı olup, İstanbul için 400 TL, Bursa için 500 TL,
Zonguldak için 300 TL, İzmir için 150 TL’dir.

Ege bölgesinin haftalık ürün gereksinimi 80 birim, Marmara bölgesinin 70 birim,
Batı Karadeniz bölgesinin 40 birimdir. Taşıma maliyetleri aşağıdaki tabloda
gösterilmiştir.

Aşağıda bir liste halinde verilen kısıtları sağlamak koşuluyla haftalık istemin
en küçük ulaştırma maliyetiyle karşılanması istenmektedir. Problemi tamsayılı
programlama problemi olarak modelleyiniz.

| Depo Yeri | Ege | Marmara | Batı Karadeniz |
|-----------|-----|---------|----------------|
| İstanbul  | 20  | 40      | 50             |
| Bursa     | 48  | 15      | 26             |
| Zonguldak | 26  | 35      | 18             |
| İzmir     | 24  | 50      | 35             |

**a**. İstanbul’a depo kurulması durumunda Bursa’ya da bir depo kurulmalıdır.

**b**. En az iki depo açılmalıdır.

**c**. Ya İzmir ya da Bursa’da bir depo bulunmalıdır.

**6.** Farklı iki üretim hattında üç çeşit (A, B, C) yapıştırıcı üretilmektedir.
Her bir hatta yedi işçi çalışabilmektedir. Birinci üretim hattında çalışanlara
haftada 500 TL, ikinci üretim hattında çalışanlara haftada 900 TL ödenmektedir.
Birinci üretim hattının haftalık maliyeti 1000 TL, ikinci üretim hattının
haftalık maliyeti 2000 TL’dir. Üretim hatlarının haftalık üretim kapasiteleri
aşağıdaki tabloda gösterilmiştir. Her hafta en az 120 adet A, en az 150 adet B
ve en az 200 adet C üretilmektedir. Haftalık üretim maliyetlerini en
küçükleyecek tamsayılı programlama modelini kurunuz.

| Üretim Hattı | A  | B  | C  |
|--------------|----|----|----|
| 1            | 20 | 30 | 40 |
| 2            | 50 | 35 | 45 |

**7.** İki çeşit (A, B) bilgisayar üretilmektedir. Problemle ilgili veriler
aşağıda gösterilmiştir. Üreticinin elinde 3000 adet çip ile 1200 saat çalışma
zamanı vardır. Kârı en büyükleyecek tamsayılı programlama modelini kurunuz.

| Bilgisayar | Zaman  | Çip | Donanım Maliyetleri | Satış Fiyatı |
|------------|--------|-----|---------------------|--------------|
| A          | 1 saat | 2   | 5000                | 400          |
| B          | 2 saat | 5   | 7000                | 900          |

**8.** Müstakil ev ve apartmanlardan oluşan büyük bir site ile ilgili bir proje
üzerinde çalışılmaktadır. Siteye 10000’e kadar ikametgah birimi yerleştirmek
mümkündür. Projede ya havuz ve tenis sahası ya da marina projesi bulunmak
zorundadır. İki proje aynı anda gerçekleştirilememektedir. Marina yapılırsa,
müstakil evlerin sayısı apartman dairelerinin sayısının en az üç katı olmak
zorundadır. Marinanın maliyeti 1.2 milyon TL, yüzme-tenis kompleksinin maliyeti
2.8 milyon TL’dir. Apartman dairelerinin net bugünkü değerleri 46000 TL,
müstakil evlerin ise 48000 TL’dir. Apartman dairesi ve ev inşa etme maliyeti
40000 TL’dir. En büyük kâr amaçlı tamsayılı programlama modelini kurunuz.

**9.** Yatırım için 10 milyon TL’si bulunan bir yatırımcının yatırım
yapabileceği beş seçeneği vardır. Yatırım seçeneklerinin net bugünkü değerleri
ile yatırım miktarları aşağıda verilmiştir. S1 ve S2 aynı anda
değerlendirilemeyen seçeneklerdir. S3 ve S4 yatırımlarını da aynı
değerlendirilmek mümkün değildir. S2’ye yatırım yapabilmek için S4’e yatırım
yapılması zorunludur. Buna göre net bugünkü değerin en büyük olmasını sağlayan
yatırım planını belirleyiniz.

| Yatırım Seçeneği | Yatırım Miktarı | Net Bugünkü Değer |
|------------------|-----------------|-------------------|
| S1               | 2               | 16                |
| S2               | 4               | 22                |
| S3               | 3               | 18                |
| S4               | 2               | 14                |
| S5               | 4               | 25                |

**10.** Tarkan’ın son parçalarından oluşan bir uzun çalar tasarlanmaktadır. Uzun
çaların her yüzündeki parçaların toplam uzunluğu 14 ile 16 dakika arasında
olmalıdır. Tür ve uzunlukları aşağıda gösterilen parçaların uzun çaların A ve B
yüzlerine aşağıdaki koşulları gerçekleyecek biçimde yerleştirilmesini sağlayacak
tamsayılı programlama modelini formülleyiniz.

| Parça | Tür          | Uzunluk  |
|-------|--------------|----------|
| 1     | Yavaş        | 4        |
| 2     | Hızlı        | 5        |
| 3     | Yavaş        | 3        |
| 4     | Hızlı        | 2        |
| 5     | Yavaş        | 4        |
| 6     | Hızlı        | 3        |
| 7     | -            | 5        |
| 8     | Yavaş, Hızlı | 4        |

**a**. Her iki tarafta tam 1’er yavaş parça olmalı.

**b**. A yüzünde en az 3 hızlı parça bulunmalı.

**c**. 5 veya 6 nolu parça A yüzünde bulunmalı.

**d**. 2 ve 4 nolu parçalar A yüzündeyse, 5 nolu parça B yüzünde olmalı

**e.** 8 nolu parça B yüzünde bulunmalıdır.

**11**. Bir gemiye dört çeşit eşya yüklenecektir. Eşyaların birim ağırlık, hacim
ve değerleri aşağıda gösterilmiştir. Yük için maksimum ağırlık 124 ton, hacim
ise 120 m3’dür. Tamsayılı doğrusal programlama modelini kurunuz ve çözümü
gerçekleştiriniz.

|  Eşya | Ağırlık (ton) | Hacim (m3) | Değer (000 TL) |
|-------|---------------|------------|----------------|
| 1     | 5             | 3          | 7              |
| 2     | 8             | 6          | 8              |
| 3     | 4             | 1          | 6              |
| 4     | 5             | 2          | 7              |

**12.** Aşağıdaki tamsayılı programlama problemlerini, dal-sınır yöntemi ve
kesme düzlemi algoritmasıyla çözünüz.

**a**. Zenb = 3x1 + x2

5x1 + 2x2 10

4x1 + x2 7

x1, x2 0

x1, x2 tamsayı

**b**. Zenk = 3x1 + x2

x1 + 5x2 8

x1 + 2x2 4

x1, x2 0

x1, x2 tamsayı

**c**. Zenk = 6x1 + 8x2

3x1 + x2 4

x1 + 2x2 4

x1, x2 0

x1, x2 tamsayı

**d**. Zenk = 3x1 + x2

2x1 - x2 6

4x1 + x2 4

x1, x2 0

x1 tamsayı

**12.** Aşağıdaki problemleri kesme düzlemi algoritmasıyla çözünüz.

**a**. Zenb = 5x1 - 7x2 + 10x3 + 3x4 - x5

\-x1 - 3x2 + 3x3 - x4 - 2x5 0

2x1 - 5x2 + 3x3 -2x4 - 2x5 3

x2 + x3 + x4 - x5 2

x1, x2, x3, x4, x5 = 0 veya 1

**b**. Zenk = 15x1 + 9x2 + 10x3

8x1 + 13x2 + 8x3 10

x1 + 9x2 + x3 7

x1, x2, x3 = 0 veya 1
