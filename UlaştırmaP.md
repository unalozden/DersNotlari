## 

## Üçüncü BÖLÜM

#### ULAŞTIRMA ve ATAMA PROBLEMLERİ

# 

# 3.1. GİRİŞ

Uygulamada sıkça karşılaşılan ulaştırma problemi, doğrusal programlama
probleminin özel bir biçimidir. Ulaştırma veya dağıtım problemlerinin
formülasyonu ve çözüm önerisi ilk olarak 1941 yılında, Frank L. Hitchcock’un
"Üretimin Belirli Sayıdaki Üretim Kaynağından Çok sayıdaki Merkezlere Dağıtımı"
isimli çalışmasında ortaya atılmıştır. Aynı konu, 1949 yılında Tjalling C.
Koopmans’ın "Ulaştırma Sisteminin Optimum Kullanımı" başlıklı çalışmasında daha
ayrıntılı incelenmiştir. Doğrusal programlama kavramı formüle edilmeden çok daha
önce ele alınan ulaştırma problemi ile ilgili asıl gelişme 1951 yılında G. B.
Dantzig’in "Ulaştırma Problemine Simpleks Yöntemin Uygulanması" isimli
çalışmasının yayınlanmasından sonra olmuştur. 1953 yılında A. Charnes ve W. W.
Cooper, Dantzig tarafından önerilen çözüme sistematik biçimde ulaşmayı sağlayan
göze değiştirme yöntemini geliştirmişlerdir. Konu ile ilgili en önemli gelişme,
R. O. Ferguson tarafından ortaya atılan modi-basitleştirilmiş dağıtım
yönteminden sonra gerçekleşmiştir.

Eserin bu bölümünde ulaştırma probleminin yanı sıra, ulaştırma probleminin özel
bir biçimi olan atama problemi üzerinde de durulacaktır.

# 3.2. ULAŞTIRMA PROBLEMİ

Belirli sayıdaki sunum merkezinden (fabrika, depo, maden yatağı vb.) belirli
sayıdaki istem merkezine (depo, market vb.) ürün ulaştırma sonucu ortaya çıkan
toplam maliyetinin en küçük olmasını sağlayacak bir dağıtım programının
belirlenmesi problemine ulaştırma problemi denir. Esas olarak, bir tür doğrusal
programlama problemi olması nedeniyle, doğrusal programlama için yapılan
varsayımlar ulaştırma problemleri için de geçerlidir.

Ayrıca, herhangi bir sorunun ulaştırma modeli çerçevesinde ele alınabilmesi
için, bu varsayımlara ek olarak yerine getirilmesi gereken daha başka koşullar
ve varsayımlar vardır. Bu koşul ve varsayımlar aşağıdaki gibi altı ana başlık
altında toplanabilir.

1.  Probleme konu olan mal ve hizmetler aynı birimle açıklanabilmeli yani,
    homojen olmalıdır. Başka bir anlatımla, her bir sunum merkezinin sunduğu
    mal, istem merkezlerinin istemini karşılayacak niteliktedir. Sunulan mallar
    arasında farklılık olmadığı için istem merkezlerinin herhangi bir sunum
    merkezini tercih etmesi söz konusu değildir.

2.  Belirli bir dönemde sunum merkezlerinin sunum miktarları ile istem
    merkezlerinin istem miktarlarının bilinmesi gerekir. Sunum miktarları
    toplamı ile istem miktarları toplamı birbirlerine eşit olmalı veya bu
    eşitlik kuramsal olarak sağlanmalıdır. Toplam sunumun toplam isteme
    eşitliğini açıklayan bu koşula "tutarlılık koşulu" denir. Bu koşul
    geçerliyse, problemin denge durumunda olduğu söylenir.

3.  Bir sunum merkezinden istem merkezlerine gönderilen mal miktarı, bu sunum
    merkezinin sunum miktarına eşit olmalıdır.

4.  Bir istem merkezine gönderilen toplam mal miktarı bu merkezin istemine eşit
    olmalıdır. Aksi halde denge durumuna ulaşmak mümkün olmaz.

5.  Sunum merkezlerinden istem merkezlerine mal naklinde aktarma yapılması söz
    konusu değildir. Bazı durumlarda, malın üretim merkezlerinden tüketim
    merkezlerine dolaysız taşınması ekonomik olmayabilir. Bu gibi durumlarda,
    mallar önce bazı transfer noktalarına, daha sonra tüketim merkezlerine
    taşınır. Bu tür ulaştırma problemlerine "aktarmalı ulaştırma problemi"
    denir.

6.  Bir sunum merkezinden herhangi bir istem merkezine bir birim malın taşınması
    maliyeti bilinmelidir. Taşıma maliyetlerinin taşınan miktara bağlı olarak
    değişmemesi gerekir. Bu varsayım, taşınan ürün miktarı ile ulaştırma
    maliyetleri arasındaki ilişkinin doğrusallığını da kapsamaktadır.

Yukarıdaki varsayımların geçerli olması veya geçerliliklerinin sağlanması
durumunda, herhangi bir problem ulaştırma modeli olarak formüle edilebilir.

# 3.3. ULAŞTIRMA MODELİNİN YAPISAL GÖRÜNÜMÜ

Aslında bir tür doğrusal programlama problemi olan ulaştırma problemi, doğrusal
programlama problemi olarak modellenebilir. Ulaştırma probleminin modeli de
doğrusal programlamada olduğu gibi, 1. Amaç fonksiyonu, 2. Kısıtlayıcı
fonksiyonlar, 3. Negatif olmama koşulu olmak üzere üç temel unsurdan oluşur.

m = Sunum merkezi sayısı (i = 1, 2, ..., m)

n = İstem merkezi sayısı (j = 1, 2, ..., n)

Cij = i sunum merkezinden j istem merkezine bir birim mal taşınması maliyeti

xij = i sunum merkezinden j tüketim merkezine taşınan mal miktarı

ai = i sunum merkezinin sunduğu mal miktarı

bj = j istem merkezinin bu mala olan istem miktarı

olmak üzere, modelin genel gösterimi aşağıdaki gibidir.

1\. **Amaç Fonksiyonu**

Tüm doğrusal programlama modellerinde olduğu gibi, ulaştırma modellerinde de
hedeflenen amaç ve bu amacı etkileyen faktörlerin matematiksel bir biçimde ifade
edildiği doğrusal bir amaç fonksiyonu vardır. Taşıma maliyetleri ve taşınan
miktarlar göz önünde bulundurulduğunda toplam ulaştırma maliyeti aşağıdaki gibi
yazılır.

Z =

Amaç, bu maliyetin en küçük olmasını sağlayan ulaştırma planının programlanması
olduğuna göre, amaç fonksiyonu aşağıdaki gibi olur.

Zenk = 3.1

2\. **Kısıtlayıcı Fonksiyonlar**

Doğrusal programlama problemlerinde olduğu gibi ulaştırma problemlerinde de
alternatif stratejilerden amaca en uygun olanının seçimi bazı sınırlayıcı
koşullar altında gerçekleştirilir. Ulaştırma probleminin karar vericiyi
kısıtlayan koşulları iki başlık altında incelenir.

1.  Herhangi bir sunum merkezinden istem merkezlerine gönderilen mal miktarları
    toplamı bu sunum merkezinin sunumuna eşit olmalıdır. Herhangi bir sunum
    merkezinden tüketim merkezlerine gönderilen mal miktarı bu sunum merkezinin
    sunumundan az ise, diğer sunum merkezlerinden gönderilecek mal miktarlarının
    bu merkezlerin sunumlarından fazla olması gerekir. Bu durumun yaratacağı
    tutarsızlıklar "bir sunum merkezinden gönderilen mal miktarı bu sunum
    merkezinin sunumuna eşit olmalıdır" varsayımı ile önlenebilir. Bu koşul
    aşağıdaki gibi ifade edilir.

x11 + x12 + ... + x1n = a1

x21 + x22 + ... + x2n = a2

xm1 + xm2 + ... + xmn = am

Bu kısıtlayıcılar sunum miktarları ile ilgili olduklarından bunlara "sunum
miktarı kısıtlayıcıları" veya kısaca "sunum kısıtlayıcıları" denir. Sunum
kısıtlayıcıları sembolüyle aşağıdaki gibi açıklanır.

i = 1, 2, ..., m ve ai \> 0 3.2

2\. Bir istem merkezine, belirli sunum merkezlerinden gönderilen mallar toplamı o
istem merkezinin istemine eşit olmalıdır. Aksi halde denge durumuna ulaşılamaz.
Bu koşul matematiksel olarak aşağıdaki gibi ifade edilir.

x11 + x21 + xm1 = b1

x12 + x22 + xm2 = b2

x1n + x2n + xmn = bn

İstem miktarlarıyla ilgili olan kısıtlayıcı fonksiyonlara "istem miktarı
kısıtlayıcıları" veya kısaca "istem kısıtlayıcıları" denir. İstem
kısıtlayıcıları sembolüyle aşağıdaki gibi gösterilir.

j = 1, 2, ..., n ve bj \> 0 3.3

Görüldüğü gibi, m sunum merkezi, n istem merkezinin söz konusu olduğu bir
ulaştırma probleminin kısıtlayıcı sayısı (m + n)’ye eşittir. xij’nin biri sunum,
diğeri istem kısıtlayıcısı olmak üzere sadece iki kısıtlayıcıda bulunduğuna
dikkat edilmelidir.

3\. **Negatif Olmama Koşulu**

Doğrusal programlamada olduğu gibi ulaştırma modelinde de karar değişkenleri
negatif olamaz. Taşınan miktarlara karşılık gelen xij değişkenlerinin negatif
değerler almasının bir anlamı yoktur([^1]). Negatif olmama koşulu matematiksel
olarak aşağıdaki gibi açıklanır.

[^1]: Negatif değer, taşımanın sunum merkezinden istem merkezlerine değil, istem
    merkezlerinden sunum merkezine yapıldığını ifade eder.

xij 0 i = 1, 2, ..., m j = 1, 2, ..., n 3.4

Negatif olmama kısıtlayıcısının yazılmasıyla formülasyon tamamlanmış olur.

3.2 ile 3.3’ün uygun olabilmeleri için aşağıdaki bağıntının sağlanması gerekir.

Ulaştırma modelinin kurulması konusundaki açıklamalarımızı basit bir örnek
problem üzerinde uygulayalım.

**Örnek 3.1**: Bir firma değişik yerlerdeki üç fabrikasında (F1, F2, F3)
ürettiği ürünleri, ayrı yerlerde bulunan dört büyük deposuna (D1, D2, D3, D4)
taşımak istemektedir. Fabrikaların haftalık üretim kapasiteleri sırasıyla, 60
(a1) , 60 (a2), 30 (a3) birimdir. Depoların haftalık istemleri ise sırasıyla, 30
(b1), 50 (b2), 50 (b3) ve 20 (b4) birimdir. Firma yönetiminin temel sorunu,
ürünün depolara ulaşımını sağlarken karşılaştığı yüksek tutarlardaki taşıma
giderleridir. Yapılan maliyet çalışmaları sonucunda, fabrikalardan depolara bir
birim ürünün taşınması maliyetleri aşağıdaki gibi belirlenmiştir.

Tablo 3.1

|         | Depo |    |    |    |
|---------|------|----|----|----|
| Fabrika | D1   | D2 | D3 | D4 |
| F1      | 7    | 4  | 2  | 6  |
| F2      | 8    | 5  | 3  | 4  |
| F3      | 10   | 6  | 6  | 1  |

**a**. Problemin denge durumunda olup olmadığını inceleyiniz.

**b**. Problemin matematiksel modelini kurunuz.

**Çözüm 3.1**: **a**. Problemin denge durumunda olması için tutarlılık koşulunun
sağlanması gerekir. Bunun için öncelikle, fabrikaların üretim miktarları toplamı
(toplam sunum) ile depoların istem miktarları toplamını (toplam istem)
hesaplayalım.

Toplam istem = 30 + 50 + 50 + 20 = 150 birim

Toplam sunum = 60 + 60 + 30 = 150 birim

Toplam istemin toplam sunuma eşit olması tutarlılık koşulunun sağlandığını yani,
problemin denge durumunda olduğunu ortaya koymaktadır.

**b**. Amaç, toplam ulaştırma maliyetini en küçükleyen değişken değerlerini
belirlemek olduğuna göre,

x11, x12, x13, x14 birinci fabrikadan sırasıyla, depo 1, depo 2, depo 3 ve depo
4’e taşınan ürün miktarı,

x21, x22, x23, x24 ikinci fabrikadan sırasıyla, depo 1, depo 2, depo 3 ve depo
4’e taşınan ürün miktarı,

x31, x32, x33, x34 üçüncü fabrikadan sırasıyla, depo 1, depo 2, depo 3 ve depo
4’e taşınan ürün miktarı,

olarak tanımlandığında, amaç fonksiyonu aşağıdaki gibi yazılacaktır.

Zenk = 7x11 + 4x12 + 2x13 + 6x14 + 8x21 + 5x22 + 3x23 + 4x24 + 10x31 + 6x32 +
6x33 + 1x34

Her bir fabrikadan gönderilecek ürün miktarı, o fabrikanın üretim miktarına eşit
olacağına göre,

Sunum kısıtlayıcıları

x21 + x22 + x23 + x24 = 60

x31 + x32 + x33 + x34 = 30

yazılabilir.

Diğer taraftan, depo gereksinimlerinin tam olarak karşılanması istendiğinden,

İstem kısıtlayıcıları

x12 + x22 + x32 = 50

x13 + x23 + x33 = 50

x14 + x24 + x34 = 20

yazılmasıyla, sunum ve istem kısıtlayıcılarının yazılması tamamlanmış olur.

Son olarak negatif taşıma olamayacağından,

xij 0 (i = 1, 2, 3; j = 1, 2, 3, 4)

yazılmasıyla model tamamlanmış olur.

# 3.4. ULAŞTIRMA PROBLEMLERİ ÇÖZÜM YÖNTEMLERİ

Esas olarak bir tür doğrusal programlama problemi olan bir ulaştırma problemi
istendiğinde, simpleks yöntemle çözülebilir. Bilindiği gibi, çözüm için simpleks
yönteme karar verildiğinde öncelikle problemin standart biçimde yazılması
gerekmektedir.

Genel gösterimi 3.1-3.4 ile açıklanan ulaştırma problemini standart biçimde
yazmak için, problemin m x n karar değişkenine kısıtlayıcı fonksiyon sayısı
kadar yani, (m + n) tane yapay değişken eklenir. Bunun sonucunda, simpleks çözüm
tablolarında (m + n) satır ve (m x n) + (m + n) sütun bulunacaktır. Satır ve
sütun fazlalığı nedeniyle böyle bir simpleks tablosunun çözümü (küçük boyutlu
problemler de bile) çok zaman ve emek gerektirir. Gerçek uygulama problemlerinde
sunum ve istem merkezleri sayılarının binli rakamlarla ifade edildikleri
düşünüldüğünde, simpleks yöntemin ulaştırma problemleri için etkin bir hesaplama
tekniği olmadığı ortaya çıkar.

Sözgelimi, Örnek 3.1 simpleks yöntemle çözülmek istendiğinde, problemin on iki
karar değişkenine yedi yapay değişken eklenmesi gerekir. Bu durumda, simpleks
çözüm toplam on dokuz değişkenle sürdürülür ki bu, oldukça uzun zaman ve fazla
aritmetik işlem yapılması demektir.

Örnek 3.1’in simpleks başlangıç çözüm tablosu aşağıda gösterilmiştir.

**Tablo 3.2**

| TDV   | x11   | x12   | x13   | x14   | x21   | x22   | x23   | x24   | x31    | x32   | x33   | x34   | A1 | A2 | A3 | A4 | A5 | A6 | A7 | ÇV   |
|-------|-------|-------|-------|-------|-------|-------|-------|-------|--------|-------|-------|-------|----|----|----|----|----|----|----|------|
| A1    | 1     | 1     | 1     | 1     | 0     | 0     | 0     | 0     | 0      | 0     | 0     | 0     | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 60   |
| A2    | 0     | 0     | 0     | 0     | 1     | 1     | 1     | 1     | 0      | 0     | 0     | 0     | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 60   |
| A3    | 0     | 0     | 0     | 0     | 0     | 0     | 0     | 0     | 1      | 1     | 1     | 1     | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 30   |
| A4    | 1     | 0     | 0     | 0     | 1     | 0     | 0     | 0     | 1      | 0     | 0     | 0     | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 30   |
| A5    | 0     | 1     | 0     | 0     | 0     | 1     | 0     | 0     | 0      | 1     | 0     | 0     | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 50   |
| A6    | 0     | 0     | 1     | 0     | 0     | 0     | 1     | 0     | 0      | 0     | 1     | 0     | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 50   |
| A7    | 0     | 0     | 0     | 1     | 0     | 0     | 0     | 1     | 0      | 0     | 0     | 1     | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 20   |
| ZJ    | 2M    | 2M    | 2M    | 2M    | 2M    | 2M    | 2M    | 2M    | 2M     | 2M    | 2M    | 2M    | M  | M  | M  | M  | M  | M  | M  | 300M |
| ZJ-CJ | 2M -7 | 2M -4 | 2M -2 | 2M -6 | 2M -8 | 2M -5 | 2M -3 | 2M -4 | 2M -10 | 2M -6 | 2M -6 | 2M -1 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | -    |

Ulaştırma probleminin çözümü için, içerdiği basitleştirici unsurlar (aij’lerin
sıfır ya da bire eşit olması, kısıtlayıcıların eşitlik şeklinde tanımlanması ve
temel uygun çözümlerin üçgen matris şeklinde olması gibi) göz önünde
bulundurularak çözümlerin en kısa yoldan yani, zaman ve işlem tasarrufu
sağlanarak elde edilmesi amacıyla bazı özel çözüm yöntemleri geliştirilmiştir.
Bu yöntemler aşağıda açıklanacaktır.

Genel doğrusal programlama problemlerinde olduğu gibi herhangi bir ulaştırma
probleminin bir temel uygun çözümü, standart form kapsamındaki değişkenlerden (m
x n) - (m + n) tanesinin sıfıra eşitlenmesiyle bulunabilir. Ancak, eşitliği
kısıtlayıcılardan birinin gereksiz olduğunu açıklamaktadır. Bu yüzden problemin
çözümü için, (m + n - 1) kısıtlayıcının dikkate alınması yeterlidir. (m + n - 1)
kısıtlayıcının dikkate alınmasıyla belirlenen çözüm, göz ardı edilen
kısıtlayıcıyı da sağlar. Bu nedenle, ulaştırma problemlerinde temel değişken
sayısının (m + n) değil (m + n - 1) olması gerektiği söylenebilir. Pozitif
değerli değişken sayısının (m + n - 1) olduğu çözüme "temel çözüm" denir.

Ulaştırma problemlerinin çözümünde de, doğrusal programlama problemlerinin
çözümünde olduğu gibi, bir başlangıç temel uygun çözümün bulunması zorunludur.
Problemin başlangıç çözümü bulunduktan sonra ardışık yaklaşımla en iyi çözüme
ulaşılmaya çalışılır. Ulaştırma problemlerinin çözüm yöntemlerinin hepsi,
problemin aşağıda gösterilen tablo esasında düzenlenmesini gerektirir. Ulaştırma
tablosu adı verilen bu tablonun satırları sunum merkezlerini, sütunları ise
istem merkezlerini gösterir. Bir satır ve bir sütunun kesişmesiyle ortaya çıkan
her göze belirli bir sunum merkezi-istem merkezi ikilisine karşılık gelir. Birim
taşıma maliyetleri Cij genellikle, gözelerin sağ veya sol üst köşelerinde
gösterilir. Tablo 3.3’den görüldüğü gibi biz sağ üst köşeyi seçtik.

**Tablo 3.3**

Problemin tablo şeklinde düzenlenmesinden sonra çözüme geçilebilir. Çözüm için
önerilen yaklaşımların tümü, genel olarak, üç temel aşama gerektirir.

1.  Başlangıç temel uygun çözümün bulunması: Temel değişkenler aynı anda satır
    veya sütun kısıtlayıcılarından yalnızca birini sağlar. Bununla birlikte, bir
    temel değişkenin bir satır ve bir sütun kısıtlayıcısının her ikisini birden
    aynı anda sağlaması da mümkündür. Bu durumda pozitif değerli değişken sayısı
    (m + n - 1)’den daha az sayıda olur. Bu durumda bozulmadan söz edilir.
    Bozulma durumu 3.6.1. kesimde incelenecektir.

2.  Başlangıç çözümünün en iyi olup olmadığının kontrol edilmesi.

3.  Çözüm en iyi değilse, en iyi çözüme ulaşıncaya kadar ardışık tekrarlara
    devam edilmesi.

Konuyla ilgili yapıtlar incelendiğinde, başlangıç çözümünün belirlenmesinde
kullanılan yöntemlerin belli başlıcalarının, 1. Kuzey-batı köşesi yöntemi, 2. En
küçük maliyetli gözeler yöntemi, 3. VAM veya Vogel Yaklaşım Metodu olduğu
görülebilir. Bu üç yöntem, genel olarak doğrusal programlama konusunda
çalışanlar tarafından en fazla tutulan ve kullanılan yöntemlerdir. Bu yöntemleri
sırasıyla açıklayalım.

# 3.4.1. Kuzey-Batı Köşesi Yöntemi

Dantzig tarafından önerilen ve A. Charnes ve W. W. Cooper tarafından
isimlendirilen bu yöntemle, çözüm işlemine ulaştırma tablosunun
kuzey-batısındaki (sol-üst) ilk gözeden başlanır ve ilk olarak x11 = enk(a1, b1)
olmak üzere x11 belirlenir. a1 ve b1’in karşılaştırılması sonucunda şu üç
durumdan biriyle karşılaşılır.

1.  Birinci istem merkezinin isteminin birinci sunum merkezinin sunumundan küçük
    (b1 \< a1) olması: Bu durumda, birinci istem merkezinin gereksiniminin
    tamamı birinci sunum merkezinden karşılanır ve x11 = enk(a1, b1) = b1 olur.
    Bu dağıtımla birinci istem merkezinin gereksiniminin tamamı karşılandığından
    bundan sonraki dağıtım işlemlerinde bu merkez dikkate alınmaz. Başka bir
    deyişle, j = 2, ...n için bütün x1j’ler sıfıra eşit olur.

2.  Birinci istem merkezinin isteminin birinci sunum merkezinin sunumuna eşit
    (b1 = a1) olması: Bu durumda, birinci istem merkezinin istemi birinci sunum
    merkezinin tüm sunumu ile karşılanır ve x11 = enk(a1, b1) = a1 = b1 olur. Bu
    durumda, birinci sunum merkezinin tüm sunumu birinci istem merkezinin
    gereksinimi için kullanılmış olduğundan, bundan sonraki dağıtım işlemlerinde
    hem birinci satır hem de birinci sütun dikkate alınmaz. Yani, j = 2, 3, ...,
    n için bütün x1j’ler ile i = 2, 3, ..., m için bütün xi1’ler sıfıra eşit
    olur.

3.  Birinci istem merkezinin isteminin birinci sunum merkezinin sunumundan büyük
    (b1 \> a1) olması: Birinci sunum merkezinin sunumunun birinci istem
    merkezinin tüm gereksinimini karşılamada yetersiz kaldığı bu durumda, x11 =
    enk(a1, b1) = a1 olur. Bu dağıtımla birinci sunum merkezinin sunumunun
    tamamı kullanılmış olduğundan bundan sonraki dağıtımlarda birinci sunum
    merkezi dikkate alınmaz. Buna göre, i = 2, 3, ..., m için bütün xi1’ler
    sıfıra eşit olur.

İkinci bir dağıtım nasıl yapılacaktır? Bu sorunun yanıtı ilk dağıtımda
karşılaşılan duruma bağlıdır. Bu nedenle yukarıda karşılaşılan durumları
sırasıyla ele alarak ikinci dağıtımın hangi gözeye hangi miktarda yapılacağını
açıklayalım.

1.  b1 \< a1 ise x11 = enk(a1, b1) = b1 belirlenmesinin ardından (1, 2) gözesine
    geçilir ve b2 ile a1 - b1 karşılaştırılır ve enk(a1 - b1, b2) değeri bu
    gözeye tahsis edilir. Bu durumda x12 = enk(a1 - b1, b2) olur. Birinci satır
    üzerindeki dağıtım işlemi a1 sıfıra indirgeninceye değin sürdürülür.

2.  b1 \> a1 ise a1 (= x11) değerinin (1, 2) gözesine tahsis edilmesinden sonra
    (2, 1) gözesine geçilir ve x21 = enk(b1 - a1, a2) değeri bu gözeye verilir.
    Bu sütun üzerinde aşağıya kayma işlemi b1 sıfıra indirgeninceye kadar
    sürdürülür.

3.  x11 = a1 = b1 ise birinci satır ve birinci sütundan vazgeçilerek güney-doğu
    yönündeki ilk gözeye geçilir ve benzer karşılaştırmalarla sağa veya aşağı
    kayılır.

Bu değerlendirme işlemleri güney-doğudaki son gözeye ulaşılıncaya kadar
sürdürülür. Bütün bu işlemler tamamlandığında kuzey-batı köşesi yöntemiyle
dağıtım planı hazırlanmış ve problemin başlangıç uygun çözümü bulunmuş olur.
Yöntemle ilgili açıklamaların ortaya koyduğu gibi, kuzey-batı köşesi yöntemi ile
dağıtımın planlanmasında maliyetler dikkate alınmamaktadır. Planlanma işleminde
sunum-istem miktarları dikkate alındığından elde edilen başlangıç çözümü
genellikle en iyi çözümden oldukça uzaktır.

Kuzey-batı köşesi yöntemine ilişkin bu basamakları aşağıdaki örnek problem
üzerinde açıklayalım. Yöntemleri açıklarken, pek çok yazarın yaptığı gibi, aynı
kuramsal örnek kullanılacak böylece, yöntemler arasında karşılaştırma yapma
olanağı yaratılmış olacaktır.

**Örnek 3.2**: Örnek 3.1’deki problemin ulaştırma tablosunu düzenleyerek kuzey
batı köşesi yöntemi uygulamasıyla başlangıç çözümünü belirleyiniz.

**Çözüm 3.2**: Problemin kuzey-batı köşesi yöntemi ile ilk dağıtım planının
belirlenmesi için gerekli olan başlangıç tablosu aşağıda gösterilmiştir.

**Tablo 3.4**

Önce a1 ile b1’i karşılaştıralım. b1 \< a1 olduğundan x11 = 30 (= b1), x21 = x31
= 0 olur. Bu dağıtımla depo 1 elimine edilerek, yeni bir dağıtım için (1, 2)
gözesine geçilir. b2 \> (a1 - x11) = 30 (= 60 - 30) olduğundan, x12 = 30 olur.
Bu dağıtımla birinci fabrikanın tüm sunumu dağıtılmış olduğundan (fabrika 1
devre dışı) aşağıya kayılarak (2, 2) gözesine ulaşılır. Depo 2’nin toplam 50
birim olan gereksiniminin 30’u daha önce karşılandığından, istem (b2 - 30) = 20
(= 50 - 30) birime indirgenmiş olur. 20 \< a2 olduğundan x21 = 20 olur. İkinci
sütun devre dışı kalır. Aynı satırda sağa kayıldığında rastlanan ilk göze (2, 3)
gözesidir. b3 ile a2 - x21 farkını karşılaştıralım. b3 \> 40 (= 60 - 20)
olduğundan, x23 = 40 olur.

İkinci sunum merkezinin sunumu tamamen dağıtıldığından aşağıya kayarak (3, 3)
gözesine geçilir. Üçüncü deponun isteminin karşılanmamış kısmı ile fabrika 3’ün
sunumunu karşılaştıralım. b3 - x23 \< a3 olduğundan x33 = b3 - x23 = 10 (= 50 -
40) olur. Bu dağıtımla üçüncü sütun devre dışı bırakılır. Dağıtım yapılacak tek
bir gözenin kaldığı bu aşamada aynı satırda sağa kayılarak (3, 4) gözesine
geçilir. Fabrika 3’ün elinde kalan miktar bu gözenin gereksinimine eşit
olduğundan, x34 = 20 olur.

Böylece problemin tüm kısıtlayıcılarını sağlayan uygun bir başlangıç çözümü
aşağıdaki gibi belirlenmiş olur.

**Tablo 3.5**

Dağıtım işlemlerinde satır ve sütun koşulları dikkate alındığından belirlenen
başlangıç çözümü uygundur. Dağıtım yapılan göze sayısı sayısı (m + n - 1)’e eşit
olduğundan çözüm temeldir, yani bozulma söz konusu değildir. Bu dağıtımın toplam
maliyeti aşağıdaki gibi hesaplanmıştır.

Toplam Ulaştırma Maliyeti = 7x11 + 4x12 + 5x22 + 3x23 + 6x33 + 1x34

= 7(30) + 4(30) + 5(20) + 3(40) + 6(10) + 1(20)

= 630 TL

### 3.4.2. En Düşük Maliyetli Gözeler Yöntemi

Genellikle küçük boyutlu problemlerin çözümünde kullanılan bir yöntemdir. Bu
yöntemin uygulanmasında, 1. Satır yaklaşımı, 2. Sütun yaklaşımı, 3. Genel
yaklaşım olmak üzere üç ayrı yaklaşım söz konusudur.

**1. Satır Yaklaşımı**: Bu yaklaşım, öncelikle her satırın en küçük maliyetli
gözelerine dağıtım yapılması esasına dayanır. En küçük maliyetli gözenin
araştırıldığı satırda aynı en küçük maliyetli birden fazla göze varsa, sütun
indisi küçük olan gözenin seçilmesi önerilir. Seçilen gözeye satır ve sütun
şartlarına bağlı kalarak en yüksek miktardaki yükleme yapılır. Bu dağıtımla
satır şartı yerine gelmişse izleyen satıra geçilir. Aksi halde, dağıtım işlemi
aynı satırın ikinci, üçüncü, ... en küçük maliyetli gözelerine yapılarak
sürdürülür. Bu işlem her seferinde ya bir satır veya bir sütun ya da bir satır
ve bir sütun aynı anda devre dışı bırakılarak tüm satır ve sütun gerekleri
yerine getirilinceye yani, bir başlangıç çözümü elde edilinceye kadar
sürdürülür. Kuzey batı köşesi yöntemiyle çözdüğümüz Örnek 3.2’yi bu yaklaşımla
çözelim.

**Örnek 3.3**: Örnek problem 3.2’nin başlangıç çözümünü en küçük maliyetli
gözeler yönteminin satır yaklaşımıyla bulunuz. Problemin başlangıç tablosu
aşağıda gösterilmiştir.

**Tablo 3.6**

**Çözüm 3.3**: Birinci satırdaki en küçük maliyet (1, 3) gözesine ait
olduğundan, dağıtıma bu göze ile başlanacak, yani ilk olarak x13’ün değeri
belirlenecektir. Bu gözenin ait olduğu deponun istemi (50 birim), bu istemi
karşılamak durumunda olan birinci fabrikanın sunum kapasitesinden (60 birim)
küçük (b1 \< a1) olduğundan, x13 = enk(a1, b1) = 50 olur. Bu göndermeyle depo
3’ün istemi tamamen karşılandığından bu depo devre dışı kalır. a1 - x13 \> 0
olduğundan, aynı satırın ikinci en küçük maliyetli gözesi olan (1, 2) gözesine
geçilir. İkinci deponun istemi ile birinci fabrikanın elinde kalan mal miktarını
karşılaştıralım. b2 \> (a1 - x13) olduğundan x12 = enk(b2, a1 - x13) = 10 olur.
Bu dağıtımla birinci fabrikanın sunumunun tamamı, depo 2 ve 3 için kullanılmış
olur. İkinci satıra geçilir. Bu satırdaki en küçük maliyet (üçüncü sütun devre
dışı olduğu için) (2, 4) gözesine aittir. b4 \< a2 olduğundan, x24 = enk(a2, b4)
= enk(60, 20) = 20 olur ve dördüncü sütun elimine edilir. a2 - x24 \> 0
olduğundan aynı satırdaki ikinci en küçük maliyetli (2, 2) gözesine geçilir.
Depo 2’nin 50 birimlik isteminin 10 birimlik kısmı daha önce karşılandığından,
bu gözeye isteminin karşılanmayan kısmı, yani enk(a2 - 20, b2 - 10) = enk(60 -
20, 50 - 10) = 40 birim yükleme yapılarak ikinci satır şartı yerine getirilir ve
üçüncü satıra geçilir. Üçüncü satırda dağıtım yapılacak bir tek (3, 1) gözesi
vardır. a3 = b1 olduğundan, x31 = 30 olur. Böylece dağıtım işlemleri
tamamlanmış, problemin başlangıç uygun çözümü Tablo 3.7’deki gibi belirlenmiş
olur.

#### Tablo 3.7

Taşıma yapılan gözelere karşılık gelen karar değişkenleri ve bunların değerleri,
x12 = 10, x13 = 50, x22 = 40, x24 = 20, x31 = 30 olarak belirlenmiş, dağıtımın
toplam maliyeti aşağıdaki gibi hesaplanmıştır.

Toplam Ulaştırma Maliyeti = 4(10) + 2(50) + 5(40) + 4(20) + 10(30) = 720 TL

Pozitif değerli değişken sayısı (m + n - 1)’e eşit olmadığından bozulma söz
konusudur. Bu bozuk çözüm kesim 3.6.1’de incelenecek ve bozulmanın giderilmesine
çalışılacaktır.

**2.** **Sütun Yaklaşımı**

En küçük maliyetli gözeler yönteminin sütun yaklaşımında da, en küçük maliyetli
gözeler yönteminin satır yaklaşımındaki gibi hareket edilir. İki yaklaşım
arasındaki tek fark, birinde satırların diğerinde sütunların en küçük maliyetli
gözelerinin dikkate alınmasıdır. Birden fazla en küçük maliyetli göze ile
karşılaşılması durumunda, satır indisi küçük olan gözenin seçilmesi
önerilmektedir.

**Örnek 3.4**: Örnek problem 3.2’nin başlangıç çözümünü en küçük maliyetli
gözeler yönteminin sütun yaklaşımıyla bulunuz.

**Çözüm 3.4**: Birinci sütundaki en küçük maliyet (1, 1) gözesine aittir.
Dağıtıma buradan başlanır. a1 \> b1 olduğundan x11 = enk(a1, b1) = enk(60, 30) =
30 olur. Bu dağıtımla birinci deponun istemi karşılandığından, ikinci sütuna
geçilir. İkinci sütundaki en küçük maliyet (1, 2) gözesine aittir. b2 ile
fabrika 1’in sunumunun dağıtılmayan kısmını karşılaştıralım. b2 \> (a1 - x11)
olduğundan x12 = enk(a1 - x11, b2) = enk(60 - 30, 50) = 30 olur ve birinci
fabrika devre dışı kalır. İkinci deponun istemi tam olarak karşılanmadığından,
bu sütundaki ikinci en küçük maliyet araştırılır. İkinci en küçük maliyet (2,
2)’ye aittir. a2 ile (b2 - x12)’yi karşılaştıralım. a2 \> b2 - x12 olduğundan,
x22 = b2 - x12 = 20 (= 50 - 30) olur. Bu dağıtımla ikinci deponun tüm
gereksinimi karşılandığından üçüncü sütunun en küçük maliyetli gözesi olan (2,
3)’e geçilir. b3 ile (a2 - x22)’yi karşılaştıralım. b3 \> a2 - x22 olduğundan,
x23 = enk(a2 - x22, b3) = enk(40, 50) = 40 olur. Depo 3’ün tüm istemi
karşılanmadığından bu sütunun ikinci en küçük maliyetli gözesi olan (3, 3)’e
geçilir. a3 ile (b3 - x23)’ü karşılaştıralım. a3 \> b3 - x23 olduğundan x33 = b3
\- x23 = 10 olur. Dördüncü sütuna gelindiğinde, ilk iki fabrika devre dışında
bulunduğundan, dağıtım yapılacak tek bir gözenin (3, 4) bulunduğu görülebilir.
b4 ile (a3 - x33)’ü karşılaştıralım. b4 = a3 - x33 olduğundan x34 = a3 - x33 =
30 - 10 = 20 olur. Böylece dağıtım işlemi tamamlanmış, başlangıç uygun çözüm
Tablo 3.8’deki gibi belirlenmiş olur.

Tablo 3.8

Tablo 3.8’den görüldüğü gibi, en düşük maliyetli gözeler yönteminin sütun
yaklaşımıyla, x11 = 30, x12 = 30, x22 = 20, x23 = 40, x33 = 10, x34 = 20 olarak
bulunmuştur. Ulaşılan bu çözüm, temel (temel değişken sayısı = 6 olduğundan)
uygun bir çözümdür. Ayrıca, bu çözüme ilişkin toplam maliyet aşağıdaki gibi
hesaplanmıştır.

Toplam Ulaştırma Maliyeti = 7x11 + 4x12 + 5x22 + 3x23 + 6x33 + 1x34

= 7(30) + 4(30) + 5(20) + 3(40) + 6(10) + 1(20)

= 630 TL

**3. Genel Yaklaşım**

Bu yaklaşım da önceki yaklaşımlar gibi daha çok küçük boyutlu problemlere
uygulanır. Genel yaklaşımda önceki iki yaklaşımdan farklı olarak satır ve sütun
farkına bakılmaksızın başlangıç tablosunun bütünü dikkate alınır. Dağıtım
yapılacak ilk göze, tablonun en küçük maliyetli gözesidir. Bu gözeye satır ve
sütunun kısıtlayıcı koşullarına bağlı kalarak yapılabilecek en yüksek miktarda
dağıtım yapılır. Böylece bir satır veya bir sütun veya her ikisi birden bir
sonraki dağıtımda devre dışı bırakılır. Eğer birden fazla en küçük maliyetli
göze varsa seçim rasgele yapılır. Kesin bir kural olmamakla birlikte, bu
yaklaşımla toplam maliyet, genellikle diğer iki yaklaşımla belirlenen toplam
maliyetlerden küçük olmaktadır.

**Örnek 3.5**: Örnek problem 3.2’nin başlangıç çözümünü en küçük maliyetli
gözeler yönteminin genel yaklaşımıyla bulunuz.

**Çözüm 3.5**: Tablonun bütününde en küçük maliyetli göze (3, 4) olduğundan ilk
dağıtım bu gözeye yapılacaktır. Bu gözeye gönderilecek miktarı belirlemek için
a3 ile b4’ü karşılaştıralım. b4 \< a3 olduğundan x34 = enk(a3, b4) = enk(30, 20)
= 20 olur. Bu dağıtımla depo 4 devre dışı kalır. Üç satır ve üç sütunun kaldığı
bu adımda en küçük maliyet (1, 3)’e aittir. a1 ile b3’ü karşılaştıralım. b3 \<
a1 olduğundan x13 = b3 = 50 olur. Bu dağıtımla üçüncü deponun isteminin tamamı
karşılandığından üçüncü sütun göz ardı edilir. Bu yolla en küçük maliyetin
araştırılacağı tablo (3 x 2) boyutuna indirgenmiş olur. İndirgenmiş tablonun en
küçük maliyeti (1, 2) gözesine aittir. b2 ile (a1 - x13)’ü karşılaştıralım. b2
\> (a1 - x13) = 10 olduğundan x12 = 10 olur. Bu dağıtımla birinci fabrikanın tüm
sunumu dağıtılmış olduğundan bundan sonra birinci satır dikkate alınmaz. Toplam
dört gözenin kaldığı bu aşamada en küçük maliyetli gözenin (2, 2) olduğu
görülebilir. a2 ile (b2 - x12)’yi karşılaştıralım. a2 \> b2 - x12 olduğundan x12
= b2 - x12 = 40 (= 50 - 10) olur. Birisi (2, 1) diğeri (3, 1) olmak üzere sadece
iki gözenin kaldığı bu adımda en küçük maliyet (2, 1) gözesine aittir. b1 \> a2
\- 40 olduğundan x12 = 20 olur. Değerlendirilecek tek bir gözenin kaldığı bu
adımda b1 - 20 = a3 - 20 olduğundan, x31 = enk(b1 -20, a3 - 20) = 10 (= 30 - 20)
olur. Böylece dağıtım işlemi tamamlanmış problemin başlangıç uygun çözümü Tablo
3.9’daki gibi belirlenmiş olur.

Tablo 3.9

Tablo 3.9’dan görüldüğü gibi, başlangıç uygun çözümde (m + n - 1) kuralına uygun
olarak 6 gözeye dağıtım yapıldığından, bozulma söz konusu değildir. Bozuk
olmayan bu temel uygun çözüm; x12 = 10, x13 = 50, x21 = 20, x22 = 40, x31 = 10,
x34 = 20 olarak belirlenmiş, toplam maliyet aşağıdaki gibi hesaplanmıştır.

Toplam Ulaştırma Maliyeti = 4x12 + 2x13 + 8x21 + 5x22 + 10x31 + 1x34

= 4(10) + 2(50) + 8(20) + 5(40) + 10(10) + 1(20)

= 620 TL

Görüldüğü gibi, en küçük maliyetli gözeler yönteminin satır yaklaşımında 720 TL,
sütun yaklaşımında 630 TL olarak hesaplanan maliyet, aynı yöntemin genel
yaklaşımıyla 620 TL olarak hesaplanmıştır.

Yukarıda açıklandığı gibi, kesin bir kural olmamakla birlikte, genel yaklaşımla
belirlenen toplam maliyet, genellikle diğer iki yaklaşımla belirlenen toplam
maliyetlerden küçük olur.

### 3.4.3. Vogel’in Yaklaşım Yöntemi (VAM)

Adını, İngilizce "Vogel's Approximation Method" kelimelerinin ilk harflerinden
alan bu yöntem, William R. Vogel tarafından 1958’de ileri sürülmüştür. Bu
yöntemin en önemli özelliği, genellikle en iyi çözüme en yakın hatta çoğu zaman
en iyi çözümü başlangıçta vermesidir. VAM aşağıdaki aşamaların adım adım
izlenmesi ile uygulanır.

1.  Birim ulaştırma maliyetlerinin oluşturduğu matrisin her bir satır ve her bir
    sütunundaki en küçük iki maliyet değeri belirlenir.

2.  Birinci adımda belirlenen Cij’ler arasındaki farklar hesaplanarak, tabloda
    oluşturulacak bir ek satır ve bir ek sütuna yazılır. Bu farklar en küçük
    maliyetli gözenin kullanılmaması durumunda katlanılacak fazla harcamayı
    yani, bir çeşit cezayı ifade ettiklerinden bunlara birim penaltı değerleri
    de denir. Bu nedenle VAM "birim penaltı yöntemi" olarak da isimlendirilir.

3.  Bütün farklar incelenerek, en büyük değerde olan belirlenir.

4.  En büyük değerli farkın bulunduğu satır veya sütundaki maliyet katsayıları
    incelenerek, en küçük maliyetli göze belirlenir. Bu gözeye satır ve sütun
    koşullarına uygun olarak en yüksek miktardaki dağıtım yapılır. Yapılan bu
    dağıtımın miktarı, ilgili satır ve sütun toplamlarından düşülür. Dağıtım
    yapılan gözeye ilişkin istem merkezinin gereksinimi tamamen karşılanmış ya
    da sunum merkezinin sunumu tamamiyle dağıtılmış ise o üretim merkezi veya
    tüketim merkezi, duruma göre her ikisi birden, bir sonraki dağıtım işleminde
    devre dışı bırakılır.

5.  Dağıtım yapılan satır veya sütunun (veya her ikisinin birden) devre dışı
    bırakılması, sunum ve istem merkezlerinin sunum ve istem miktarlarının
    yeniden ayarlanmasıyla yeni aşama için yeni bir tablo düzenlenir.

6.  Satır veya sütun sayısı bire ininceye değin, 1-5 nolu işlemler yinelenir.

Genellikle büyük boyuttaki problemlerin çözümünde, aynı en büyük fark sayısı
birden fazla olabilir. Hangi en büyük farkın seçileceği konusunda Vogel
tarafından önerilmiş bir kural yoktur. Vogel’e göre en büyük farklardan herhangi
biri rasgele seçilip, işlemlere devam edilir. Ancak, bu durumda en iyi çözüme
ulaşmak için gerekli işlem sayısı artabilir. Roccaferrera tarafından önerilen
aşağıdaki kurallara uyulması durumunda bu tehlike bir dereceye kadar
önlenebilir.

-   En büyük fark iki veya daha fazla satır ya da sütunda ortaya çıkarsa, en
    büyük ai (veya bj) değerli satır veya sütundaki en küçük maliyetli göze
    seçilir.

    -   En büyük fark bir satır ve bir sütunda aynı anda ortaya çıkarsa ve söz
        konusu satır ile sütunun kesiştiği yerdeki gözenin maliyeti en küçük ise
        dağıtım için bu göze seçilir. Eğer söz konusu gözeye ilişkin maliyet en
        küçük değilse, ilgili satır ya da sütunun en küçük maliyetli gözesi
        seçilir.

3.2’deki örnek problemi bu kez VAM’la çözelim.

**Örnek 3.6**: Örnek problem 3.2’nin başlangıç çözümünü VAM’la bulunuz.

**Çözüm 3.6**: VAM’ın ilk aşama hesaplamaları için düzenlenen tablo aşağıda
verilmiştir. Görüldüğü gibi, her satırın en küçük iki maliyeti arasındaki
farklarla oluşturulan sütun tablonun sağına, her sütunun en küçük iki maliyeti
arasındaki farklarla oluşturulan satır tablonun en altına eklenmiştir.

Tablo 3.10

Tablo 3.10’daki farklar incelendiğinde en büyük farkın (5) üçüncü satırda ortaya
çıktığı görülebilir. Yukarıda yapılan açıklamalar çerçevesinde ilk dağıtım, en
büyük değerli farkın bulunduğu üçüncü satırın en küçük maliyetli (3, 4) gözesine
yapılacaktır. x34’ü belirlemek için a3 ile b4’ü karşılaştıralım. b4 \< a3
olduğundan, x34 = b4 = 20 olur. Bu dağıtımla depo 4’ün tüm gereksinimi
karşılanmış, fabrika 3’ün elinde kalan mal miktarı 10 birime indirgenmiş olur.

Yeni dağıtım için, bir önceki aşamada yapılan dağıtım dikkate alınarak yeni bir
tablo düzenlenir. Tablo kapsamındaki indirgenmiş maliyet matrisinin satır ve
sütunları için yeniden farklar hesaplanır. Hesaplanan farklardan oluşan bir
satır ve bir sütun tabloya ilave edilir. Yine en büyük değerli farkın bulunduğu
satır veya sütunun en küçük maliyetli gözesine mümkün olduğu kadar fazla mal
transfer edilir. Birinci dağıtımla depo 4’ün devre dışı kaldığının, üçüncü
fabrikanın sunumunun ise 10 birime düştüğünün göz önünde bulundurulmasıyla
oluşturulan indirgenmiş maliyetli tablo aşağıda gösterilmiştir.

Tablo 3.11’den görüldüğü gibi en büyük fark ilk iki satırda aynı anda ortaya
çıkmıştır. Yukarıda açıklandığı gibi, en büyük fark birden fazla satırda ortaya
çıktığında sağ taraf sabiti en büyük olan satırın en küçük maliyetli gözesi
seçilir. a1 = a2 = 60 olduğundan iki satırdan en küçük maliyetli gözeyi
kapsayanının yani, birinci satırın seçilmesi uygun olur. Bu satırdaki en küçük
maliyet (1, 3)’e ait olduğundan dağıtım işlemi bu gözeyle sürdürülecek yani, x13
temele girecektir.

a1 ile b3 karşılaştırıldığında, b3 \< a1 olduğu görüldüğünden, x13 = enk(a1, b3)
= enk(60, 50) = 50 olur.

Tablo 3.11

Bu dağıtımla depo 3 devre dışı kalırken birinci fabrikanın sunumu 50 birim
azalarak 10 birim olur.

Bu değişiklikler altında düzenlenen indirgenmiş maliyet matrisi Tablo 3.12’de
gösterilmiştir.

Tablo 3.12

Tablo 3.12’den görüldüğü gibi en büyük fark üçüncü satırda ortaya çıktığından
dağıtım bu satırın en küçük maliyetli gözesi olan (3, 2) ile sürdürülecek, yani
x32 temele alınacaktır. b2 ile (a3 - b4)’ü karşılaştırılalım. b2 \> (a3 - b4)
olduğu için x32 = enk(a3 - b4 , b2) = enk(10, 50) = 10 olur. Bu dağıtımla,
üçüncü fabrikanın tüm sunumu dağıtılmış olduğundan izleyen aşamada bu fabrika
dikkate alınmaz. Depo 2’nin isteminin 40 birime indirgendiği ve fabrika 3’ün
devre dışı kaldığının dikkate alınmasıyla hazırlanan, dördüncü aşama dağıtım
tablosu aşağıda gösterilmiştir.

Tablo 3.13

Tablo 3.13’den görüldüğü gibi en büyük fark iki satırda birden ortaya çıkmıştır.
En büyük farka (yan koşula) sahip satırın seçilmesi önerilmekle birlikte biz, en
küçük maliyeti kapsayan birinci satırı seçelim. Bu satırdaki en küçük maliyet
(1, 2)’ye ait olduğundan, dördüncü dağıtım bu gözeye yapılacaktır. (a1 - x13)
ile (b2 - x32) ’yi karşılaştıralım. 10 (= a1 - x13) \< 40 (b2 - x32) olduğundan
x12 = 10 olur. Dördüncü dağıtım sonrasında elde edilen tablo aşağıda
gösterilmiştir.

Tablo 3.14

Dağıtım yapılacak iki gözenin kaldığı bu aşamada, önce (2, 2) gözesine depo
2’nin, sonra (2, 1) gözesine depo 1’in istemi kadar, yani sırasıyla 30 ve 30
birim tahsis edilererek dağıtım işlemi tamamlanır.

Tablo 3.10 - Tablo 3.14 kapsamındaki sonuç değerlerinin bir araya getirilmesiyle
VAM’la ulaşılan başlangıç çözümü Tablo 3.15’deki gibi belirlenmiş olur. Dağıtım
yapılan göze sayısı altıya eşit olduğundan bozulmadan söz edilemez. Temel uygun
bu dağıtımda, x12 = 10, x13 = 50, x21 = 30, x22 = 30, x32 = 10, x34 = 10 olarak
elde edilmiştir.

Tablo 3.15

Dağıtımın toplam maliyeti aşağıdaki gibi hesaplanmıştır.

Toplam Ulaştırma Maliyeti = 4x12 + 2x13 + 8x21 + 5x22 + 6x32 + 1x34

= 4(10) + 2(50) + 8(30) + 5(30) + 6(10) + 1(20)

= 610 TL

VAM’la 610 TL olarak hesaplanan maliyet, kuzey batı köşesi yöntemiyle 630, en
küçük maliyetli gözeler yönteminin satır yaklaşımıyla 720, sütun yaklaşımıyla
630, genel yaklaşımla 620 olarak hesaplanmıştır. Görüldüğü gibi VAM’la
belirlenen dağıtımın maliyeti diğerlerinden daha küçük olduğundan, en iyi çözüme
varışta daha az tekrar gerektirecektir.

# 3.5. EN İYİ ÇÖZÜMÜN ELDE EDİLMESİ

Doğrusal programlama problemlerinde olduğu gibi, ulaştırma problemlerinde de bir
başlangıç temel uygun çözüm bulunduktan sonra, bu çözümün en iyi olup olmadığı,
aynı kısıtlayıcı koşullar altında daha gelişmiş bir çözümün bulunup bulunmadığı
test edilmelidir. Temel olmayan bir değişken temele girdiğinde maliyet
azalıyorsa yürürlükteki çözümün en iyi olmadığı, maliyeti azaltıcı etkisi
bulunan temel olmayan değişken(ler)in temele alınması gerektiği kararlaştırılır.
Temelde bulunmayan değişkenlerin hiçbirisinin maliyet üzerindeki etkisi olumlu
değilse, eldeki çözümün en iyi olduğu kararlaştırılır. Çözümün en iyi olup
olmadığının belirlenmesinde, buna bağlı olarak en iyi çözümün elde edilmesinde
kullanılmak üzere değişik yöntemler geliştirilmiştir. Bu yöntemlerden genel bir
uygulama alanı bulmuş olanlar, "göze değiştirme yöntemi" ile "modi yöntemi"dir.

### 3.5.1. Göze Değiştirme Yöntemi

Bir çözümün en iyi olup olmadığını belirten ve en iyi çözüme adım adım ulaşmayı
sağlayan göze değiştirme yöntemi, A. Charnes ve W. W. Cooper tarafından
geliştirilmiştir. Yöntemin adımları aşağıda açıklanmıştır.

1.  Gizli maliyeti hesaplanacak boş gözenin saptanması.

2.  Belirlenen boş gözeden başlayarak, yalnız yatay ve düşey doğrultularda
    ilerleyip, 90 derecelik dönüşlerle dolu gözelerden geçip tekrar boş gözeye
    dönülmesi: Bu işlemle, kimi yazarların "ilmek" veya "döngü" ismini verdiği
    bir çevrim oluşturulur. Aşağıdaki çevrim örneklerinden görüldüğü gibi
    çevrimin yönü yalnızca dolu gözede değişebilir.

Şekil 3.1’deki çevrimde iki satır, iki sütun ve dört gözeden yararlanılmıştır.

**Şekil 3.1**

Bazı durumlarda, ikiden çok satır ve sütun ile çok sayıda göze kullanılması
gerekebilir. Sözgelimi, Şekil 3.2 ve Şekil 3.3’deki çevrimlerde üç satır, üç
sütun ve altı göze kullanılmıştır.

**Şekil 3.2**

**Şekil 3.3**

1.  Seçilen boş gözeye (+), çevrimdeki her bir dolu gözeye sıra ile (+), (-),
    (+) işaretlerinin konulması: Yukarıdaki çevrimlerin ortaya koyduğu gibi (+)
    ile işaretlenen boş gözenin bulunduğu satır ve sütundaki birer dolu gözeye
    (-) işareti, (-) işaretinin yerleştirildiği dolu gözenin bulunduğu satır ve
    sütundaki birer dolu gözeye (+) işareti konulur. Böylece denge durumu
    korunur. Çevrimdeki tüm gözeler işaretlendiğinde işaretleme işlemine son
    verilir.

2.  Çevrimdeki gözelerin birim taşıma maliyetlerinin gözelere konulan
    işaretlerin dikkate alınmasıyla toplanması: Toplama işlemiyle elde edilen
    maliyete boş gözenin gizli maliyeti denir. dij ile gösterilen gizli
    maliyetler simpleks yöntemindeki (Zj - Cj) katsayılarına benzer.

Gizli maliyet için üç durum (dij \> 0, dij = 0, dij \< 0 ) söz konusu olabilir.

dij \> 0 ise, (i, j) gözesine bir birim aktarılması toplam maliyette dij birim
artışa yol açacağından, hali hazırda boş olan (i, j) gözesinin boş bırakılması
karar laştırılır.

dij = 0 ise, (i, j) gözesine bir birim aktarılması sonucunda maliyette bir
değişiklik olmaz. Bu durumda problemin alternatif bir en iyi çözümü vardır
denir. Alternatif en iyi çözüm (i, j) boş gözesinin dolu göze şekline
dönüştürülmesiyle elde edilir. Bu özel durum, 3.6.3. kesimde açıklanacaktır.

dij \< 0 ise, (i, j) gözesine bir birim aktarılması toplam maliyette dij birim
azalışa yol açacağından, hali hazırda boş olan (i, j) gözesinin doldurulması
karar laştırılır.

Eldeki çözümün en iyi olup olmadığının belirlenebilmesi bakımından tek bir boş
göze için açıklanan bu işlemin, boş gözelerin hepsi için gerçekleştirilmesi
gerekir. Bütün boş gözelerin gizli maliyetleri, sıfır ya da sıfırdan büyükse
ulaşılan çözüm en iyidir. Boş gözelerden bir ya da birkaçının gizli maliyetinin
sıfırdan küçük olması durumunda, çözümün en iyi olmadığına, negatif gizli
maliyete sahip boş gözenin dolu göze durumuna getirilmesine karar verilir.

Bir boş gözenin dolu göze durumuna dönüştürülmesinde çevrimdeki (-) işaretli
gözelerdeki taşıma miktarları dikkate alınarak en küçük olan belirlenir.
Belirlenen bu değer, çevrimdeki (+) işaretli gözelerdeki miktarlara eklenir, (-)
işaretli gözelerdeki miktarlardan çıkartılır. Böylece temel dışı kalan
değişken(ler)in sıfır değerli olması sağlanır. Bu işlemler tüm boş gözelerin
gizli maliyetleri sıfır ya da pozitif oluncaya kadar tekrarlanır.

Göze değiştirme yöntemini, VAM’la belirlenen başlangıç temel uygun çözüm
üzerinde açıklayalım.

**Örnek 3.7**: Örnek 3.2’nin VAM’la elde edilen başlangıç temel uygun çözümünün
en iyi olup olmadığını göze değiştirme yöntemiyle test ediniz.

**Çözüm 3.7**: VAM’la belirlenen başlangıç dağıtım planı Tablo 3.16’da tekrar
gösterilmiştir.

**Tablo 3.16**

Gizli maliyetler yukarıdaki önerilere uygun olarak aşağıdaki gibi hesaplanır.

F1D1: d11 = C11 - C12 + C22 - C21 = 7 - 4 + 5 - 8 = 0

F1D4: d14 = C14 - C34 + C32 - C12 = 6 - 1 + 6 - 4 = 7

F2D3: d23 = C23 - C13 + C12 - C22 = 3 - 2 + 4 - 5 = 0

F2D4: d24 = C24 - C34 + C32 - C22 = 4 - 1 + 6 - 5 = 4

F3D1: d31 = C31 - C32 + C22 - C21 = 10 - 6 + 5 - 8 = 1

F3D3: d33 = C33 - C13 + C12 - C32 = 6 - 2 + 4 - 6 = 2

Görüldüğü gibi gizli maliyetlerin hepsi sıfır veya pozitif olduğundan, VAM’la
ulaşılan çözüm en iyidir.

Buna göre, x12 = 10, x13 = 50, x21 = 30, x22 = 30, x32 = 10, x34 = 20 olur. Zenk
= 610 TL’dir. Ayrıca d11 = d23 = 0 olduğundan problemin alternatif en iyi çözümü
de vardır. Alternatif en iyi çözüm(ler) (1, 1) ve/veya (2, 3) gözelerine taşıma
yapılarak bulunabilir.

### 3.5.2. Modi Yöntemi

En iyi çözümün araştırılmasında kullanılan başka bir yaklaşım R. O. Ferguson
tarafından geliştirilen modi veya U-V yöntemidir. Göze değiştirme yönteminin
gelişmiş biçimi sayılan modi yöntemi ile göze değiştirme yöntemi arasındaki tek
fark, gizli maliyetlerin hesaplanmasında kullandıkları yaklaşımdır. Göze
değiştirme yönteminde gizli maliyetlerin hesaplanması için boş göze sayısı kadar
çevrim oluşturulurken, modi yönteminde gizli maliyetler çevrim yapılmaksızın
hesaplanmakta, çevrim ancak çözümün en iyi olmadığının belirlenmesinden sonra
temele alınacak tek bir boş göze için yapılmaktadır. Bu yolla, en iyi olan
çözüme ulaşmada, göze değiştirme yöntemine oranla, daha az sayıda işlem yeterli
olmaktadır. Modi yöntemi, doğrusal programlamanın primal-dual çözümünden hareket
eden ve ulaştırma problemleri için kullanılan bir yöntemdir.

Önce, ulaştırma probleminin dualini inceleyelim. 3.1-3.4 bağıntılarıyla
açıklanan ve aşağıda bir kez daha gösterilen ulaştırma problemini primal problem
olarak ele alalım.

Zenk =

j = 1, 2, ..., n

i = 1, 2, ..., m

xij 0 i = 1, 2, ..., m j = 1, 2, ..., n

Yukarıdaki primal problemin amaç fonksiyonu en küçükleme tipinde olduğundan,
dual problemin amaç fonksiyonu en büyükleme tipinde olacaktır. Primal problemde
(m + n) kısıtlayıcı fonksiyon olduğundan, dual problemde (m + n) dual değişken
bulunacaktır. Primal problemin her bir değişkenine dual problemde bir
kısıtlayıcı karşılık geleceğinden dual problemde işaretli (m x n) kısıtlayıcı
bulunacaktır. Primal problemin sunum kısıtlayıcılarına karşılık gelen dual
değişkenler Ui (i = 1, 2, ..., m), istem kısıtlayıcılarına karşılık gelen dual
değişkenler Vj (j = 1, 2, .., n) ile gösterildiğinde dual problemin amaç
fonksiyonu aşağıdaki gibi yazılır.

3.6

Dual problemin kısıtlayıcı fonksiyonları aşağıdaki gibi gösterilir.

U i + Vj Cij i = 1, 2, ..., m j = 1, 2, ..., n 3.7

Primal problemin kısıtlayıcıları eşitlik biçiminde olduğundan, bunlara karşılık
gelen dual değişkenler pozitif, sıfır veya negatif istenilen değeri alabilir.
Yani, dual değişkenlerin işaretleri kısıtlanmamıştır.

Modi yönteminde yapılması gereken ilk işlem, Ui ve Vj dual değişkenlerin
değerlerinin hesaplanmasıdır. Ui ve Vj değerlerinin hesaplanmasında, dağıtım
yapılmış olan gözelerden yararlanılır. (Ui + Vj) toplamının dolu gözelerdeki Cij
katsayısına eşit olması gerekir. Ui ve Vj olarak (m + n) bilinmeyene karşılık,
(m + n - 1) temel değişken dolayısıyla, (m + n - 1) denklem vardır. Bilinmeyen
sayısı, denklem sayısından bir fazla olduğu için, Ui veya Vj değişkenlerinden
keyfi olarak seçilen bir tanesine rasgele bir değer (genellikle sıfır) verilerek
diğer bilinmeyenler hesaplanır. Hangi dual değişkene sıfır değeri verileceği
konusunda kesin kurallar olmamakla birlikte, çok sayıda dolu gözenin bulunduğu
satır veya sütuna karşılık gelen dual değişkene sıfır değerinin verilmesi
diğerlerinin hesaplanmasında büyük kolaylık sağlar. Bu amaçla kullanılan diğer
bir yaklaşım ise, durum ne olursa olsun U1’e sıfır değeri vermektir. Hangi dual
değişken için hangi değer verilmiş olursa olsun (Ui + Vj) toplamları değişmez.
Ui ve Vj değerlerinin hesaplanmasından sonra, boş gözelere ilişkin gizli
maliyetler hesaplanır. Gizli maliyetler aşağıdaki formül yardımıyla hesaplanır.

dij = Cij - (Ui + Vj) 3.8

Gizli maliyetlerin hepsi 0 ise ulaşılan çözüm en iyidir. Gizli maliyetlerden en
az biri negatif ise yürürlükteki çözümün en iyi olmadığı kararlaştırılır.
Negatif dij değerli boş gözeye atama yapılarak daha iyi çözüme ulaşılmaya
çalışılır. Boş göze seçildikten sonra göze değiştirme yönteminde olduğu gibi,
boş göze başlangıç noktası olmak üzere, uygun dolu gözeler kullanılarak bir
çevrim oluşturulur ve gözeler arasında mal aktarmaları yapılarak yeni bir
dağıtım planı programlanır. Aktarmalardan sonra ulaşılan çözümün temel olup
olmadığının belirlenmesinden sonra, Ui ve Vj değerleri yeniden hesaplanır. Bu
işlemler en iyi çözüme ulaşılıncaya değin tekrarlanır.

Örnek problemin VAM’la belirlenen başlangıç çözümünün en iyi olup olmadığını bir
de modi yöntemiyle kontrol edelim. Böylece, hem işlemlerin doğruluğunu kontrol
etmiş hem de yöntemler arasındaki farkı incelemiş oluruz.

**Örnek 3.8**: Örnek 3.2’nin VAM’la elde edilen başlangıç temel uygun çözümünün
en iyi olup olmadığını modi yöntemiyle kontrol ediniz.

**Çözüm 3.8**: VAM’la ulaşılan temel uygun çözüm aşağıda gösterilmiştir.

**Tablo 3.17**

Temeldeki değişkenlerin, yani dolu gözelerin kullanılmasıyla yazılan eşitlikler
ve dual değişken değerlerinin hesaplanmasına ilişkin aritmetik işlemler aşağıda
topluca gösterilmiştir.

1\. F1D2: U1 + V2 = C12 U1 + V2 = 4

2\. F1D3: U1 + V3 = C13 U1 + V3 = 2

3\. F2D1: U2 + V1 = C21 U2 + V1 = 8

4\. F2D2: U2 + V2 = C22 U2 + V2 = 5

5\. F3D2: U3 + V2 = C32 U3 + V2 = 6

6\. F3D4: U3 + V4 = C34 U3 + V4 = 1

U1’e sıfır değerini verelim. Buna göre,

1\. U1 = 0 ise U1 + V2 = 4 bağıntısından 0 + V2 = 4 V2 = 4 olur.

2\. U1 = 0 ise U1 + V3 = 2 bağıntısından 0 + V3 = 2 V3 = 2 olur.

3\. V2 = 4 ise U2 + V2 = 5 bağıntısından U2 + 4 = 5 U2 = 1 olur.

4\. V2 = 4 ise U3 + V2 = 6 bağıntısından U3 + 4 = 6 U3 = 2 olur.

5\. U2 = 1 ise U2 + V1 = 8 bağıntısından 1 + V1 = 8 V1 = 7 olur.

6\. U3 = 2 ise U3 + V4 = 1 bağıntısından 2 + V4 = 1 V4 = -1 olur.

Hesaplanan Ui ve Vj değerleri Tablo 3.17’de ait oldukları satır ve sütun
başlarında gösterilmiştir.

Ui ve Vj değerlerinin kullanılmasıyla gizli maliyetler aşağıdaki gibi
hesaplanır.

F1D1: d11 = C11 - (U1 + V1) = 7 - (0 + 7) = 0

F1D4: d14 = C14 - (U1 + V4) = 6 - ( 0 - 1) = 7

F2D3: d23 = C23 - (U2 + V3) = 3 - (1 + 2) = 0

F2D4: d24 = C24 - (U2 + V4) = 4 - (1 - 1) = 4

F3D1: d31 = C31 - (U3 + V1) = 10 - (2 + 7) = 1

F3D3: d33 = C33 - (U3 + V3) = 6 - (2 + 2) = 2

Gizli maliyetlerin hepsi 0 olduğundan çözüm en iyidir.

**Örnek 3.9**: Örnek 3.2’de kuzey-batı köşesi yöntemiyle belirlenen çözümün en
iyi olmadığını göze değiştirme yöntemi ile kanıtlayınız.

**Çözüm 3.9**: Örnek 3.2’nin kuzey-batı köşesi yöntemiyle belirlenen başlangıç
temel uygun çözümü Tablo 3.18’de gösterilmiştir.

**Tablo 3.18**

Boş gözelerin gizli maliyetleri çevrimler yardımıyla aşağıdaki gibi
hesaplanmıştır.

d13 = C13 - C23 + C22 - C12 = 2 - 3 + 5 - 4 = 0

d14 = C14 - C34 + C33 - C23 + C22 - C12 = 6 - 1 + 6 - 3 + 5 - 4 = 9

d21 = C21 - C22 + C12 - C11 = 8 - 5 + 4 - 7 = 0

d24 = C24 - C34 + C33 - C23 = 4 - 1 + 6 - 3 = 6

d31 = C31 - C11 + C12 - C22 + C23 - C33 = 10 - 7 + 4 - 5 + 3 - 6 = -1

d32 = C32 – C33 + C23 – C22 = 6 – 6 + 3 – 5 = -2

d31 = -1 \< 0 ve d32 = -2 \< 0 olduğundan kuzey-batı köşesi yöntemiyle
belirlenen başlangıç temel uygun çözüm en iyi değildir. Bu gözelerden (3, 1)’e
bir birim transfer edilmesi toplam maliyette 1 TL, (3, 2)’ye bir birim
aktarılması toplam maliyette 2 TL azalış sağlayacaktır. En iyi çözüme varışı
daha çabuk sağlayacağı için öncelikle (3, 2) gözesinin doldurulması uygun olur.

Temele girecek değişken (x32) kararlaştırıldıktan sonra temelden ayrılacak
değişkeni belirlemek için (3, 2) gözesinin gizli maliyetinin hesaplanmasında
kullanılan çevrime dönülür. Söz konusu çevrimin işaretleri Tablo 3.18’de
gösterilmiştir. x32’ye ait çevrimdeki (-) işaretli gözelere taşınan miktarlar
incelenir. x22 = 20 ve x33 = 10 olduğunun belirlenmesinden sonra bunlardan en
küçük değerli olan x33’ün temelden ayrılmasına karar verilir. En küçük olduğu
belirlenen değerin (-) işaretli gözelerdeki dağıtım miktarlarından çıkartılması,
(+) işaretli gözelerdeki dağıtım miktarlarına eklenmesiyle çevrimdeki
değişkenlerin değerleri, x32 = 10, x22 = 10, x23 = 50, x33 = 0 olarak bulunur.
Bu belirlemelerle yeni dağıtım planı Tablo 3.19’daki gibi elde edilir.

#### Tablo 3.19

Tablo 3.19’daki dağıtımın toplam maliyeti aşağıdaki gibi hesaplanmıştır.

Toplam Ulaştırma Maliyeti = 7x11 + 4x12 + 5x22 + 3x23 + 6x32 + 1x34

= 7 (30) + 4(30) + 5(10) + 3(50) + 6(10) + 1(20)

= 610 TL

Örnek 3.8’de belirlendiği gibi, VAM’la ulaşılan 610 TL maliyetli dağıtım planı
en iyi olduğundan Tablo 3.19’daki çözüm de en iyidir. Göze değiştirme
yönteminin, kuzey-batı köşesi yöntemiyle ulaşılan başlangıç çözümüne
uygulanmasıyla elde edilen en iyi dağıtım planı ile VAM’la belirlenen dağıtım
planının aynı en küçük toplam maliyeti vermekle birlikte, farklı değişkenler
kümesinden oluştuklarına dikkat edilmelidir. Problemin alternatif en iyi
çözümlerinin bulunması demek olan bu durum 3.6.3. kesimde incelenecektir.

# 3.6. ÖZEL DURUMLAR

Doğrusal programlama problemlerinde olduğu gibi, ulaştırma problemlerinin çözüm
sürecinde de, problemin niteliğine göre bazı özel durumlar ve bunlarla ilgili
sorunlar ortaya çıkmaktadır. Bu kesimde, ulaştırma problemlerinin çözüm
sürecinde ortaya çıkabilecek özel durumlar, sorunlar ve bunların giderilmesi
konuları üzerinde durulacaktır.

### 3.6.1. Bozulma Durumu

Bilindiği gibi, ulaştırma probleminin bir uygun çözümünde temel değişken sayısı
(k), satır ve sütun sayıları toplamının bir eksiğine eşitse çözüm bozuk
değildir. Uygun bir çözümde temel değişken sayısı (m + n - 1)’den farklıysa
"bozulma" söz konusu olur. Bozulma durumuna iki şekilde rastlanır.

1.  Temel değişken sayısının (k), (m + n - 1)’den büyük olması: k \> m + n - 1
    durumuna yalnızca başlangıç çözümünde seyrek olarak rastlanır. Dağıtımda
    yanlışlık yapılması veya problemin yanlış formüle edilmesi sonucunda ortaya
    çıkan bu sorunun üstesinden gelebilmek için modelin ve çözümün kontrol
    edilmesi gerekir.

2.  Temel değişken sayısının (k), (m + n - 1)’den küçük olması: k \< m + n - 1
    durumuna başlangıç çözümünde veya en iyi çözüme ulaşma çabalarının herhangi
    bir aşamasında rastlanabilir. Her iki durum da bozulma durumudur ve
    giderilmesi gerekir.

Bozuk bir dağıtım planında dolu göze sayısı yeterli olmadığından, ne boş
gözelerin hepsi için çevrim oluşturulabilmekte ne de Ui ve Vj değerleri
dolayısıyla, gizli maliyetler hesaplanabilmektedir. Bu nedenle, bazı
değişiklikler yapmadan, bozuk bir çözümden en iyi olan çözüme ulaşmak mümkün
olmamaktadır. Bozulma durumunu gidermek için çok basit bir teknik kullanılır.
Tekniği açıklamak için, k = m + n - 2 olduğunu düşünelim. Bu durumda dağıtımın
uygunluğunu zedelememek için, boş gözelerden birisine geçici bir süre için
miktarında bir taşıma yapılması yeterli olur. Tanım gereği sıfıra son derece
yakın pozitif bir sayıdır. Öyle ki, eklenen bu sayı ne satır ne de sütun
toplamlarını etkilemez. ’nun eklenmesi ve dolu göze sayısının (m + n - 1)’e
eşitlenmesiyle önceden temel olmayan çözüm, temel çözüm haline getirilmiş olur.
Artık, bu temel çözüm üzerinde bilinen işlemleri uygulayarak en iyi çözüme
ulaşmak zor olmaz. ’nun hangi boş gözeye yerleştirileceği önemli bir sorundur.
Kesin bir kural olmamakla birlikte bu konuda, en düşük maliyetli gözenin
seçilmesi biçiminde yaygın bir uygulama vardır. Bu konuda izlenebilecek bir
başka yaklaşım ise, dual değişkenleri hesaplamaya çalışmak, nerede dual
değişkenler hesaplanamıyorsa ’nu o gözeye yerleştirmektir. hangi boş gözeye
yerleştirilirse yerleştirilsin, dikkat edilmesi gereken en önemli nokta, ’nun
yerleştirildiği boş gözenin, dolu gözelerle çevrim oluşturabilmesidir. Yeterli
sayıda ’nun eklenmesinden sonra temel olması sağlanan uygun çözümün en iyi olup
olmadığı bilinen yöntemlerle test edilebilir. Bozulma durumu ve giderilmesine
ilişkin kuralları bir örnekle açıklayalım.

**Örnek 3.10**: Örnek 3.2’nin en düşük maliyetli gözeler yönteminin satır
yaklaşımıyla elde edilen başlangıç uygun çözümünün en iyi olup olmadığını göze
değiştirme yöntemiyle kontrol ediniz.

**Çözüm 3.10**: Örnek 3.2’nin en düşük maliyetli gözeler yönteminin satır
yaklaşımıyla elde edilen başlangıç çözümü Tablo 3.20’de verilmiştir.

**Tablo 3.20**

Başlangıç uygun çözümün pozitif değerli değişken sayısı 5 (3 + 4 - 1)
olduğundan, çözüm bozuktur. Bozulma giderilmeden çözümün en iyi olup olmadığı
incelenemez. Bu nedenle öncelikle bu durumdan kurtulalım. Bozulmayı gidermek
için tablodaki boş gözelerden birine miktarında bir taşıma yapılması yeterli
olur. En düşük maliyet (3, 4) gözesine ait olduğundan ’nun bu gözeye
yerleştirilmesi uygun olur. Bu yolla temel değişken sayısı 6’ya eşit
lendiğinden, çözümün en iyi olup olmadığı incelenebilir. Önce, her boş göze için
uygun çevrimler yardımıyla gizli maliyetleri hesaplayalım. Gizli maliyetler
aşağıdaki gibi hesaplanmıştır.

F1D1: d11 = C11 - C12 + C22 - C24 + C34 - C31 = 7 - 4 + 5 - 4 + 1 - 10 = -5

F1D4: d14 = C14 - C24 + C22 - C12 = 6 - 4 + 5 - 4 = 3

F2D1: d21 = C21 - C24 + C34 - C31 = 8 - 4 + 1 - 10 = -5

F2D3: d23 = C23 - C13 + C12 - C22 = 3 - 2 + 4 - 5 = 0

F3D2: d32 = C32 - C34 + C24 - C22 = 6 - 1 + 4 - 5 = 4

F3D3: d33 = C33 - C13 + C12 - C22 + C24 - C34 = 6 - 2 + 4 - 5 + 4 - 1 = 6

d11 \< 0, d21 \< 0 olduğundan, çözüm en iyi değildir. d11 = d21 (= -5)
olduğundan dağıtım ya (1, 1) veya (2, 1) gözesine yapılmalıdır. (1, 1)’i
seçelim. Bu seçimle oluşturulan çevrim Tablo 3.20’de gösterilmiştir. Enk(x12,
x24, x31) = x12 = 10 olduğundan, (1, 1) gözesine en fazla 10 birim transfer
edilebilir. Aktarmalardan sonra elde edilen gelişmiş çözüm aşağıda
gösterilmiştir.

**Tablo 3.21**

Tablo 3.21’den görüldüğü gibi, temel değişken sayısı (m + n - 1) kuralına uygun
olarak altıya eşit olduğundan bozulma söz konusu değildir. Bu dağıtımın en iyi
olup olmadığı kontrol edilmelidir. Kontrol işlemi modi yöntemiyle
gerçekleştirilecektir. Temeldeki değişkenlerin kullanılmasıyla hesaplanan Ui ve
Vj değerleri Tablo 3.21’de satır ve sütun başlarında gösterilmiştir. Bu
değerlerin kullanılmasıyla dij değerleri aşağıdaki gibi hesaplanmıştır.

d12 = C12 - (U1 + V2) = 4 - (0 - 1) = 5

d14 = C14 - (U1 + V4) = 6 - (0 - 2) = 8

d21 = C21 - (U2 + V1) = 8 - (6 + 7) = -5

d23 = C23 - (U2 + V3) = 3 - (6 + 2) = -5

d32 = C32 - (U3 + V2) = 6 - (3 - 1) = 4

d33 = C33 - (U3 + V3) = 6 - (3 + 2) = 1

d21 (= -5) 0 ve d23 (= -5) 0 olduğu için Tablo 3.21’deki çözüm en iyi değildir.
Daha gelişmiş çözüm için, x21 veya x23 temele alınmalıdır. x23’ü seçelim. x23’ün
çözüme alınması için oluşturulan ve Tablo 3.21’de gösterilen çevrim
incelendiğinde enk(x13, x24, x31) = enk(50, 10, 20) = 10 olduğu görülecektir. Bu
belirlemenin ardından yapılan aktarmalar sonucunda elde edilen yeni dağıtım
planı ile bu daha gelişmiş temel uygun çözümün en iyi olup olmadığının
belirlenmesi için hesaplanan Ui ve Vj değerleri Tablo 3.22’de gösterilmiştir.

**Tablo 3.22**

Tablo 3.22’deki Ui ve Vj değerlerinin kullanılmasıyla hesaplanan dij değerleri
şöyledir: d12 = 0, d14 = 8, d21 = 0, d24 = 5, d32 = -1, d33 = 1

d32 0 olduğu için tablodaki çözüm en iyi değildir. Daha gelişmiş çözüm için x32
temele alınmalıdır. Bu amaçla gerçekleştirilen çevrim Tablo 3.22’de,
aktarmalardan sonra belirlenen çözüm Tablo 3.23’de gösterilmiştir.

**Tablo 3.23**

Tablo 3.23’deki çözümün en iyi olup olmadığının belirlenmesi için hesaplanan Ui
ve Vj değerleri aynı tabloda gösterilmiştir. Bu değerlerin kullanılmasıyla
hesaplanan dij değerleri şöyledir: d21 = 0, d14 = 7, d21 = 0, d24 = 4, d31 = 1,
d33 = 2

Bütün dij 0 olduğu için çözüm en iyi olup, Zenk = 610 olarak hesaplanmıştır.

### 3.6.2. Toplam Sunum ile Toplam İstemin Eşit Olmaması

Ulaştırma modelinde değişiklik yapılmasını gerektiren durumlardan birisi de
toplam sunum ile toplam istemin eşit olmamasıdır. Uygulamada, tutarlılık
koşulunun sağlanmadığı bu tip problemlerle karşılaşmak daha olağandır. Denge
durumunda olmayan ulaştırma problemlerine çözüm bulabilmek için problemin
dengelenmesi yani, sunum-istem eşitliğinin sağlanması gerekir. Denge durumunda
olmayan bir ulaştırma problemini denge durumuna dönüştürmek için öncelikle
toplam sunum ve toplam istem arasındaki fark incelenir. Toplam sunum-toplam
istem farkı iki yönde ortaya çıkar. Ya toplam sunum toplam istemden büyüktür ya
da toplam istem toplam sunumdan büyüktür.

**1. Toplam Sunumun Toplam İstemden Büyük Olması**

Sunum merkezlerinde istem merkezlerinde gerek duyulandan daha fazla mal olması
durumunda, sunum kısıtlayıcıları aşağıdaki gibi yazılır.

i = 1, 2, ..., m

Problemin dengelenmesi için işaretli bu kısıtlayıcıların eşitlik biçimine
dönüştürülmeleri gerekir. Bunun için probleme sunum fazlası kadar mal istediği
varsayılan hayali bir istem merkezi eklenir. Hayali bir istem merkezinin
eklenmesi, sunum kısıtlayıcılarının her birine bir hayali (aylak) değişken
karşılık gelmek üzere, probleme m değişken eklenmesi demektir. Hayali
değişkenler xi,n+1 ile gösterildiğinde yukarıdaki kısıtlayıcılar kümesi
aşağıdaki gibi elde edilir.

i = 1, 2, ..., m

Böylece denge durumuna getirilen problem, bilinen yöntemler yardımıyla
çözülebilir. Gerçekte bulunmayan bir yere gerçek bir taşıma söz konusu
olamayacağından, hayali istem merkezinin bulunduğu sütundaki birim taşıma
maliyetleri (Ci,n+1) sıfır olarak alınır.

**Örnek 3.11**: Bir firma dört fabrikasında ürettiği ürünleri, üç deposuna
taşımaktadır. Fabrikaların aylık üretim kapasiteleri sırasıyla 40, 60, 50 ve 100
birimdir. Depoların aylık depolama kapasiteleri birbirine eşit olup 70 birimdir.
Taşıma maliyetleri, C11 = 3, C12 = 4, C13 = 10, C21 = 5, C22 = 10, C23 = 8, C31
= 7, C32 = 6, C33 = 2, C41 = 9, C42 = 8, C43 = 3 olarak verilmiştir.

Kuzey-batı köşesi yöntemiyle başlangıç temel uygun çözümü bulunuz ve elde
ettiğiniz çözümün en iyiliğini modi yöntemiyle test ediniz.

**Çözüm 3.11**: Önce ulaştırma tablosunu düzenleyelim. İstem ve sunum miktarları
eşit olmadıkları için ulaştırma tablosuna sunum fazlası kadar istekte bulunan
hayali bir depo ekleyelim.

Hayali deponun isteminin,

birim

olduğu görülebilir.

**Tablo 3.24**

Hayali deponun eklenmesiyle dengelenen problemin verileri ve kuzey-batı köşesi
yöntemiyle belirlenen başlangıç çözümü Tablo 3.24’de verilmiştir. Ulaşılan
çözümdeki pozitif değerli değişken sayısı (m + n - 1) kuralına uygun olarak
yediye eşit olduğundan, bozulma söz konusu değildir.

Başlangıç temel uygun bu çözümün en iyiliğini test etmek amacıyla hesaplanan Ui
ve Vj değerleri aynı tabloda ait oldukları satır ve sütun başlarında
gösterilmiştir. Söz konusu Ui ve Vj değerleriyle dij’ler,

d12 = -4, d13 = 6, d14 = -1, d23 = 2, d24 = -3, d31 = 6, d34 = 1, d41 = 7, d42 =
1

olarak hesaplanmıştır.

d12 (= -4) \< 0, d14 (= -1) \< 0, d24 (= -3) \< 0 olduğundan çözüm en iyi
değildir. En büyük negatif değerli gizli maliyet (d12 = -4) (1, 2) gözesinde
ortaya çıktığından x12 temele girer. x12’nin esas alınmasıyla oluşturulan çevrim
Tablo 3.24’de, aktarmalardan sonra ulaşılan ve en iyi olduğu belirlenen çözüm
Tablo 3.25’de verilmiştir. Buna göre en iyi dağıtım planı şöyledir: x11 = 10,
x12 = 30, x21 = 60, x32 = 40, x33 = 10, d43 = 60, x44 = 40.

**Tablo 3.25**

**2. Toplam İstemin Toplam Sunumdan Büyük Olması**

Ulaştırma problemlerinin dengede olmamasına yol açan diğer bir durum sunum
merkezlerinin istem merkezlerinin gereksinimini karşılamada yetersiz kalmasıdır.
Böyle bir durumda, istem kısıtlayıcıları aşağıdaki gibi yazılır.

j = 1, 2, ..., n

Problemin dengelenmesi için işaretli kısıtlayıcıların = işaretli yazılmaları
gerekir. Bunu sağlamanın yolu, probleme istem fazlası kadar mal sunduğu
varsayılan hayali bir sunum merkezinin eklenmesidir. Hayali bir sunum merkezinin
probleme eklenmesi, işaretli kısıtlayıcıların her birine bir hayali değişken
eklenmesi demektir. Hayali değişkenler, xm+1,j ile gösterildiklerinde, istem
kısıtlayıcıları aşağıdaki gibi elde edilir.

j = 1, 2, ..., n

Hayali değişkenlerin eklenmesiyle dengelenen problem bilinen yöntemlerle
çözülebilir. Gerçekte bulunmayan bir sunum kaynağından istem merkezlerine gerçek
bir taşıma söz konusu olamayacağından, bu hayali sunum merkezinin bulunduğu
satırdaki birim taşıma maliyetleri sıfır olarak alınır.

**Örnek 3.12**: Bir firma üç fabrikasında ürettiği ürünleri dört büyük deposuna
taşımaktadır. Fabrikaların haftalık üretim kapasiteleri sırasıyla 100, 60 ve 140
birimdir. Depoların haftalık mal gereksinimleri ise sırasıyla 75, 80, 100 ve 145
birimdir. Taşıma maliyetleri, C11 = 6, C12 = 9, C13 = 10, C14 = 4, C21 = 3, C22
= 5, C23 = 7, C24 = 9, C31 = 3, C32 = 2, C33 = 10, C34 = 4 olarak verilmiştir.
Başlangıç tablosunu düzenleyerek VAM’la bulduğunuz başlangıç çözümünü modi
yöntemiyle test ediniz.

**Çözüm 3.12**: İstem miktarı sunum miktarından fazla olduğundan istem fazlası
kadar mal sunan hayali bir fabrika bulunduğunu düşünelim. Hayali fabrikanın
sunum miktarı, birim olur. Buna göre ulaştırma tablosu aşağıdaki gibi
düzenlenir. Problemin VAM’la elde edilen başlangıç temel uygun çözümü aynı
tabloda gösterilmiştir.

**Tablo 3.26**

VAM’la bulunan başlangıç temel uygun çözümün en iyi olup olmadığının
belirlenmesinde kullanılacak Ui ve Vj değerleri Tablo 3.26’daki gibi
hesaplanmış, gizli maliyetler aşağıdaki gibi elde edilmiştir.

d11 =3, d12 = 7, d13 = 7, d22 = 3, d23 = 3, d24 = 5, d33 = 6, d41 = 3, d42 = 2

Gizli maliyetlerin hepsi pozitif olduğundan çözüm en iyidir.

### 3.6.3. Alternatif En İyi Çözümlerin Bulunması

Doğrusal programlama problemlerinde olduğu gibi, ulaştırma problemlerinin de
alternatif en iyi çözümleri olabilir. Hatırlanacağı gibi, herhangi bir doğrusal
programlama probleminin birden fazla en iyi çözümünün bulunup bulunmadığını
anlamak için, en iyi çözümün temel olmayan değişkenlerinin (Zj - Cj)
değerlerinin incelenmesi yeterli olmaktaydı. Ulaştırma problemlerinin alternatif
en iyi çözümlere sahip olup olmadığı ise, boş gözelerin gizli maliyetlerinin
(dij) incelenmesiyle anlaşılır. Problemin en iyi çözümündeki gizli maliyetlerin
bir ya da birkaçı sıfır ise problemin aynı maliyeti veren birden fazla en iyi
çözümü bulunacaktır. Alternatif en iyi çözümlerin elde edilmesini basit bir
örnek üzerinde gösterelim.

**Örnek 3.13**: Üç fabrika, dört depolu bir ulaştırma probleminin başlangıç
tablosu ve VAM’la elde edilen başlangıç temel uygun çözümü Tablo 3.27’de
gösterilmiştir. Bu çözümün en iyi olup olmadığını inceleyerek varsa diğer en iyi
çözümleri bulunuz.

**Tablo 3.27**

**Çözüm 3.13**: Gizli maliyetlerin hesaplanmasında kullanılan Ui ve Vj değerleri
Tablo 3.27’de, bu değerlerin kullanılmasıyla dij değerlerinin hesaplanması
işlemleri aşağıda gösterilmiştir.

d14 = C14 - (U1 + V4) = 7 - (0 + 3) = 4

d21 = C21 - (U2 + V1) = 10 - (-1 + 3) = 8

d22 = C22 - (U2 + V2) = 4 - (-1 + 5) = 0

d32 = C32 - (U3 + V2) = 7 - (-2 + 6) = 3

d33 = C33 - (U3 + V3) = 8 - (-2 + 6) = 4

d34 = C34 - (U3 + V4) = 12 - (-2 + 3) = 11

Bütün dij’ler 0 olduğundan çözüm en iyidir. Bu çözümde x11 = 75, x12 = 225, x13
= 100, x23 = 250, x24 = 100, x41 = 150, Zenk = 3550’ye eşittir. Ayrıca d22 = 0
olduğu için problemin alternatif en iyi çözümü vardır. Alternatif en iyi çözümü
bulmak için x22 değişkeni temele alınmalıdır. Bunun için (2, 2) gözesinin esas
alınmasıyla bir çevrim oluşturulur. Söz konusu çevrim Tablo 3.27’de
gösterilmiştir.

Enk(225, 250) = 225 olduğunun belirlenmesiyle gerçekleştirilen aktarmalar
sonucunda elde edilen alternatif en iyi çözüm Tablo 3.28’de gösterilmiştir.

**Tablo 3.28**

Tablo 3.28’de verilen çözümde gizli maliyetler, d12 **=** 0, d13 = 4, d21 =
8,d32 = 4, d33 = 4, d34 = 11 olduğundan, bu çözüm de en iyi olup, x11 = 75, x13
= 325, x22 = 225, x23 = 25, x24 = 100, x41 = 150, Zenk = 3550’ye eşittir.

### 3.6.4. En Büyükleme Amaçlı Ulaştırma Modeli

Buraya kadar, en küçükleme amaçlı ulaştırma problemleri üzerinde durulmuş ve
açıklamalar bu konu üzerinde yoğunlaştırılmış olmakla birlikte ulaştırma
gelirlerinin veya kârların en büyüklenmesi durumlarıyla da karşılaşılabilir. Bu
nedenle, en büyükleme amaçlı ulaştırma modeli üzerinde durmak, konuyu tamamlamak
bakımından, yararlı olacaktır.

En büyükleme amaçlı bir ulaştırma probleminin çözümünde iki yaklaşım
izlenebilir. Bu yaklaşımlar aşağıda açıklanmıştır.

1\. En büyükleme amaçlı bir doğrusal programlama problemi en küçükleme problemi
olarak veya bunun karşıtı, en küçükleme amaçlı bir doğrusal programlama problemi
en büyükleme problemi olarak çözülebilir. Bunun için, amaç fonksiyonu
katsayılarının işaretlerinin değiştirilmesi yeterli olur. Esas olarak, bir tür
doğrusal programlama modeli olması nedeniyle bu açıklama, ulaştırma modelleri
için de geçerlidir. Bu nedenle, en büyükleme amaçlı bir ulaştırma problemi en
küçükleme amaçlı bir ulaştırma problemi şekline dönüştürülerek, en küçükleme
amaçlı ulaştırma problemlerinin çözümünde kullanılan yöntemlerle ve aynı süreç
izlenerek çözülebilir. En iyi çözümün elde edilmesinden sonra, amaç fonksiyonu
için belirlenen en iyi değerin (-1) ile çarpılması yeterlidir. Karar
değişkenlerinin en iyi değerlerinin değişmeyeceği unutulmamalıdır.

2\. En büyükleme amaçlı bir ulaştırma problemi, en iyilemenin anlamını
değiştirmeksizin de bilinen yöntemlerle ve aynı süreç izlenerek çözülebilir.
Bunun için öncelikle, kâr katsayılarından oluşan başlangıç tablosunun
düzenlenmesi gerekir. Daha sonra, başlangıç çözümünün belirlenmesi amacıyla
geliştirilen yöntemlerden herhangi birisiyle çözüme başlanır.

En büyükleme amaçlı ulaştırma problemlerinin çözümü ile en küçükleme amaçlı
ulaştırma problemlerinin çözümü arasındaki en önemli fark, dağıtım yapılacak
gözelerin belirlenmesinde ortaya çıkmaktadır. En küçükleme problemlerinde, en
küçük maliyetler esas alınarak çözüme ulaşılırken, en büyükleme problemlerinde
en yüksek kâr katsayıları esas alınır. Sözgelimi, başlangıç çözümü VAM’la elde
edilmek istendiğinde, satır ve sütunlara ilişkin farkların hesaplanmasında en
yüksek iki kâr katsayısı dikkate alınır ve bunlar arasındaki farklar hesaplanır.
Daha sonra, en yüksek farkın bulunduğu satır ya da sütunun en yüksek kar
katsayılı gözesine dağıtım yapılır. Bu işlem, en küçükleme problemlerinde olduğu
gibi, tek bir satır ya da tek bir sütun kalıncaya kadar sürdürülür.

Elde edilen başlangıç çözümünün en iyi olup olmadığının belirlenmesinde ve buna
bağlı olarak en iyi çözümün elde edilmesinde modi veya göze değiştirme yöntemi
kullanılabilir. Ancak, problem en büyükleme olduğundan artık hesaplananlar gizli
maliyetler değil gizli kârlardır. Bu nedenle, en küçükleme problemindeki durumun
tersine, gizli kârların hepsi sıfır ya da negatifse en iyi çözümün elde edildiği
kararlaştırılır. Çözüm en iyi değilse işlemler en küçükleme probleminde olduğu
gibi aynı sırayla tekrarlanır.

## 3.7. ULAŞTIRMA PROBLEMLERİNDE DUYARLILIK

## ÇÖZÜMLEMESİ

Bilindiği gibi model parametrelerinin zaman içinde sürekli değişmesi son derece
olağandır. Herhangi bir ulaştırma probleminin en iyi çözümü bulunduktan sonra
problem verilerinde ortaya çıkan değişimin eldeki en iyi çözüm üzerindeki
etkisinin incelenmesi de karar vericiler için büyük önem taşır.

Bir ulaştırma probleminde ortaya çıkabilecek belli başlı değişiklikler,
aşağıdaki gibi açıklanabilir.

1\. Amaç fonksiyonu katsayılarının değişmesi.

1.  Kısıtlayıcı fonksiyonların sağ taraf sabitlerinin değişmesi.

Bu değişiklikler sonucunda yürürlükteki çözüm en iyi olma özelliğini koruyabilir
veya bunun tersi olarak çözüm, artık en iyi değildir ve en iyi çözümün elde
edilmesi gerekir. Bu iki durumdan hangisinin ortaya çıktığı duyarlılık
çözümlemesi ile belirlenebilmektedir.

Duyarlılık çözümlemesi açıklamalarında kullanılacak en iyi çözüm tablosu aşağıda
gösterilmiştir.

**Tablo 3.29**

### 3.7.1. Amaç Fonksiyonu Katsayılarının Değişmesi

Amaç fonksiyonu katsayılarındaki değişmelerin en iyi çözüme etkisi incelenmek
istendiğinde, doğrusal programlamada olduğu gibi, öncelikle temel değişken
katsayılarının mı temel olmayan değişken katsayılarının mı değiştiğinin
belirlenmesi gerekir. Çünkü, temel değişken katsayılarındaki değişmelerin en iyi
çözüme etkisi ile temel olmayan değişken katsayılarındaki değişmelerin en iyi
çözüme etkisi birbirlerinden farklıdır. Bu nedenle, bu iki durum ayrı ayrı ele
alınacaktır. Önce en iyi çözümün temel olmayan değişken katsayılarındaki
değişime duyarlılığı üzerinde duralım.

**1. Temel olmayan değişken katsayılarının değişmesi**

Bilindiği gibi, dual değişkenlerin değerleri dolu gözelerin maliyet
katsayılarına bağlıdır. Boş gözelerin Cij değerleri ne olursa olsun, hangi yönde
deği-şirse değişsin, dolu gözelerin maliyet katsayıları değişmediği sürece dual
değişkenlerin değerleri aynı kalır. Temel olmayan bir değişkenin katsayısındaki
değişme yalnızca, kendisine ait gizli maliyette değişikliğe neden olur.
Bilindiği gibi, (i, j) boş gözesinin gizli maliyeti aşağıdaki bağıntıdan
hesaplanmaktadır.

dij = Cij - (Ui + Vj)

Bu değer sıfır ya da sıfırdan küçükse, çözümün en iyi olmadığı ve xij’nin temele
alınması kararlaştırılır. Yani Cij (Ui + Vj) ise, xij çözüme girecektir. Kısaca,
temel olmayan değişken katsayılarındaki değişmelerin en iyi çözümü etkileyip
etkilemedikleri, yukarıdaki eşitsizliğin sağlanıp sağlanmadığının incelenmesiyle
anlaşılabilmektedir.

**Örnek 3.14**: En iyi çözümü Tablo 3.29’da verilen problemde C22 ile C24’ün 1
olarak değişmesinin en iyi çözüm üzerindeki etkisini inceleyiniz.

**Çözüm 3.14**: Temel olmayan x22 değişkeninin amaç fonksiyonundaki katsayısı 1
olduğunda d22, aşağıdaki gibi hesaplanır.

d22 = C22 - (U2 + V2) = 1 - (2 - 1) = 0

d22 = 0 olması, yürürlükteki çözümün en iyi olarak kaldığını göstermektedir.
Ayrıca, d22 = 0 olduğundan alternatif en iyi çözüm vardır.

Temel olmayan x24’ün katsayısı C24 = 1 olsun. Bu durumda (2, 4) gözesinin gizli
maliyeti,

d24 = C24 - (U2 + V4) = 1 - (2 + 5) = -6

olarak hesaplanacaktır. Gizli maliyetin negatif olması eldeki çözümün en iyi
olma özelliğini yitirdiğine işaret eder. En iyi çözüme ulaşmak için bilinen
ardışık işlemlerin sürdürülmesi, yani x24 değişkeninin temele alınması gerekir.

Bazen en iyi sonucun, değişkenin hangi değişim aralığında en iyi olarak
kalabileceği bilinmek istenebilir. Yukarıdaki açıklamaların ortaya koyduğu gibi,
Cij (Ui + Vj) olursa yürürlükteki çözüm en iyi özelliğini kaybetmiş demektir.
Örneğin, temel olmayan xij değişkeninin maliyet katsayısı kaç TL’ye düşerse
çözüm en iyi olma özelliğini kaybeder sorusuna yanıt arandığında yapılacak tek
şey, Ui ve Vj değerlerini kullanarak yukarıdaki eşitsizliği yorumlamaktan
ibarettir.

Cij (Ui + Vj) olursa iki durum söz konusu olur. Cij = Ui + Vj olursa
yürürlükteki çözüm hala en iyidir. Ayrıca, aynı en küçük maliyeti sağlayan
farklı bir en iyi çözüm daha bulunabilir. Cij \< (Ui + Vj) olursa eldeki çözüm
artık en iyi değildir. Benzer yorumlamalar bütün boş gözeler için yapılabilir.
Örnek problemimize dönelim ve temel olmayan değişkenlerin katsayılarını tek tek
çözümleyelim.

C11 (U1 + V1) = (0 + 1 ) = 1 1 C11

C12 (U1 + V2) = (0 - 1) = -1 0 C12

C15 (U1 + V5) = (0 + 0) = 0 0 C15

C22 (U2 + V2) = (2 - 1) = 1 1 C22

C24 (U2 + V4) = (2 + 5) = 7 7 C11

C31 (U3 + V1) = (3 + 1) = 4 4 C11

C34 (U3 + V4) = (3 + 5) = 8 8 C11

C35 (U3 + V5) = (3 + 0) = 3 3 C11

Yukarıdaki eşitsizliklerden ilkini yorumlayalım. Bilindiği gibi C11, birinci
üretim merkezinden birinci tüketim merkezine gerçekleştirilen taşımanın birim
maliyetidir. Bu maliyet 1 TL’nin altına düşerse, dij negatif olur ve çözüm en
iyi olma özelliğini yitirir. Kısaca C11, 1’e eşit veya 1’den büyük olursa, çözüm
en iyi olma özelliğini korur. Diğer eşitsizlikler de benzer şekilde
yorumlanabilir.

**2. Temel değişken katsayılarının değişmesi**

Dual değişkenlerin değerleri temel değişkenlerin amaç fonksiyonu katsayılarına
bağlı olduğundan, temel değişken katsayılarındaki değişmeler doğrudan doğruya
dual değişkenlerin değerlerini dolayısıyla, gizli maliyetleri etkiler. Bu
nedenle temel değişken katsayıları değiştiğinde, dual değişken değerleri ile
gizli maliyetlerin yeniden hesaplanması gerekir.

**Örnek 3.15**: En iyi çözümü Tablo 3.29’da verilen problemde C23’ün 5 olarak
değişmesinin en iyi çözüm üzerindeki etkisini inceleyiniz.

**Çözüm 3.15**: x23 temelde bulunduğundan C23’ün değişmesi dual değişken
değerlerini değiştirir. Bu durumda, Ui ve Vj’nin yeni değerleri hesaplanmalıdır.
C23 = 5 için dual değişkenlerin değerleri aşağıdaki gibi hesaplanır.

1\. F1D3: U1 + V3 = 6

2\. F1D4: U1 + V4 = 5

3\. F2D1: U2 + V1 = 3

4\. F2D3: U2 + V3 = 5

5\. F2D5: U2 + V5 = 2

6\. F3D2: U3 + V2 = 2

7\. F3D3: U3 + V3 = 9

U1 = 0 için U2 = -1, U3 = 3 , V1 = 4, V2 = -1, V3 = 6, V4 = 5, V5 = 3 olur. Buna
göre gizli maliyetler aşağıdaki gibi hesaplanır.

F1D1: d11 = C11 - (U1 + V1) = 2 - (0 + 4) = -2

F1D2: d12 = C12 - (U1 + V2) = 4 - (0 - 1) = 5

F1D5: d15 = C15 - (U1 + V5) = 7 - (0 + 3) = 4

F2D2: d22 = C22 - (U2 + V2) = 5 - (-1 - 1) = 7

F2D4: d24 = C24 - (U2 + V4) = 9 - (-1 + 5) = 5

F3D1: d31 = C31 - (U3 + V1) = 10 - (3 + 4) = 3

F3D4: d34 = C34 - (U3 + V4) = 9 - (3 + 5) = 1

F3D5: d35 = C35 - (U3 + V5) = 5 - (3 + 3) = -1

d11 = -2, d35 = -1 olduğundan yürürlükteki çözüm artık en iyi değildir. En iyi
çözüme ulaşmak için öncelikle x11 temele alınmalıdır. Çözümün en iyi olarak
kalması için temel değişkenlerin amaç fonksiyonu katsayıları dikkate alınarak
birer değişim aralığı tanımlanabilir. Değişim aralıklarının belirlenmesinde
Örnek 3.16’da açıklanan yaklaşım kullanılır.

**Örnek 3.16**: En iyi çözümü Tablo 3.29’da verilen problemde, en iyi çözümün
değişmemesi için x23 temel değişkeninin amaç fonksiyonu katsayısına ilişkin
değişim aralığını bulunuz.

**Çözüm 3.16**: x23 değişkeninin yeni katsayısı y olsun. Ui ve Vj
değişkenlerinin yeni değerlerinin hesaplanması amacıyla gerçekleştirilen
işlemler aşağıda gösterilmiştir. U1 = 0 kabul edilmiştir.

1\. F1D3: U1 + V3 = 6 bağıntısından 0 + V3 = 6 V3 = 6 olur.

2\. F1D4: U1 + V4 = 5 bağıntısından 0 + V4 = 5 V4 = 5 olur.

3\. F2D1: U2 + V1 = 3 bağıntısından (y - 6) + V1 = 3 V1 = 9 - y olur.

4\. F2D3: U2 + V3 = y bağıntısından U2 + 6 = y U2 = y - 6 olur.

5\. F2D5: U2 + V5 = 2 bağıntısından (y - 6) + V5 = 2 V5 = 8 - y olur.

6\. F3D2: U3 + V2 = 2 bağıntısından 3 + V2 = 2 V2 = -1 olur.

7\. F3D3: U3 + V3 = 9 bağıntısından U3 + 6 = 9 U3 = 3 olur.

Ui ve Vj değerlerinin kullanılmasıyla gizli maliyetler aşağıdaki gibi
hesaplanır.

F1D1: d11 = C11 - (U1 + V1) = 2 - (0 + 9 - y) = y - 7 0 y 7

F1D2: d12 = C12 - (U1 + V2) = 4 - (0 - 1) = 5

F1D5: d15 = C15 - (U1 + V5) = 7 - (0 + 8 - y) = y - 1 0 y 1

F2D2: d22 = C22 - (U2 + V2) = 5 - (y - 6 - 1) = 12 - y 0 y 12

F2D4: d24 = C24 - (U2 + V4) = 9 - (y - 1) = 10 - y 0 y 10

F3D1: d31 = C31 - (U3 + V1) = 12 - (3 + 9 - y) 0 y 2

F3D4: d34 = C34 - (U3 + V4) = 9 - (3 + 5) = 1

F3D5: d35 = C35 - (U3 + V5) = 5 - (3 + 8 - y) = y - 6 0 y 6

### Eşitsizliklerin oluşturduğu değişim aralığı, 6 y 10 olarak elde edilir. Yani, C23 bu aralık içinde yer alırsa eldeki çözüm en iyi olarak kalır.

### 3.7.2. Kısıtlayıcıların Sağ Taraf Sabitlerinin Değişmesi

Sunum ve istem miktarlarındaki artış veya azalışlar toplam maliyeti etkiler.
Sunum miktarlarındaki değişmeler ile istem miktarlarındaki değişmelerin ayrı
ayrı incelenmesi uygun olur. Çünkü sunum miktarlarındaki değişmelerin toplam
maliyet üzerindeki etkisi Ui’lerle açıklanırken, istem miktarlarındaki
değişmelerin etkisi Vj’ler yardımıyla incelenir.

#### Durum 1. Sunum miktarlarının değişmesi

Sunum miktarlarının değişmesi (artması veya azalması) sonucunda Ui
değişkenlerinin amaç fonksiyonu katsayıları değişir. i sunum kaynağının sunum
miktarının i kadar değiştiğini düşünelim. Bu durumda toplam maliyetin yeni
değeri, aşağıdaki gibi olur.

Zenk/yeni = Zenk/eski + i Ui

**Örnek 3.17**: Tablo 3.29’da verilen en iyi çözüme sahip problemdeki birinci
fabrikanın sunumunun 20 birim artmasının toplam maliyet üzerindeki etkisini
inceleyiniz.

**Çözüm 3.17**: Bu durumda değişecek olan yalnızca U1’in katsayısıdır. Bu
değişiklik altında toplam maliyetin yeni değeri aşağıdaki gibi olur.

Zenk/yeni = Zenk/eski + 20U1

= (40U1 + 60U2 + 50U3 + 25V1 + 40V2 + 40V3 + 20V4 + 25V5) + 20U1

Ui ve Vj değerleri belli olduğuna göre, Zenk/yeni şöyle hesaplanır.

Zenk/yeni = (40 x 0 + 60 x 2 + 50 x 3 + 25 x 1 + 40 x (-1) + 40 x 6 + 20 x 2 +
25 x 0) + 20 x 0

= 595 + 0 = 595

Birden fazla sunum kaynağının sunum kapasitesi de değişebilir. k ve s sırasıyla,
k ve s sunum merkezlerinin sunum miktarlarındaki değişmeleri göstermek üzere
toplam maliyetin yeni değeri aşağıdaki gibi açıklanır.

Zenk/yeni = Zenk/eski + i Uk + sUs

**Durum 2. İstem miktarlarının değişmesi**

İstem miktarlarındaki değişmelerin toplam maliyet üzerindeki etkisi Vj
değişkenleri yardımıyla incelenir. j, j istem merkezinin istem miktarındaki
değişimi göstermek üzere yeni toplam maliyet şöyle olur:

Zenk/yeni = Zenk/eski + j Vj

Birden fazla istem merkezinin istem miktarının değişmesi durumunda değişmeler
aynı anda ve birlikte değerlendirilmelidir. k ve s sırasıyla, k ve s istem
merkezlerinin istemlerindeki değişimleri göstermek üzere yeni toplam maliyet,

Zenk/yeni = Zenk/eski + i Vk + sVs

olur.

**Durum 3. Sunum ve istem miktarlarının aynı anda değişmesi**

Sunum ve istem miktarlarının birlikte değişmesi sonucunda temel değişken
değerleri değişir. Böyle bir değişiklik altında temel değişkenlerin yeni
değerleri hesaplanabilir. Bunun için i sunum merkezinin sunumu ile j istem
merkezinin isteminin aynı miktarda, kadar, arttığını düşünelim. Bu durumda
değişkenlerin yeni değerleri aşağıdaki gibi hesaplanır.

1.  xij temel değişken ise, bu değişkenin temel çözümdeki yeni değeri eski
    değerinden kadar fazla olur.

2.  xij temel olmayan bir değişken ise, temel olmayan değişkenlerin yeni
    değerlerinin hesaplanabilmesi için öncelikle xij değişkeninin ait olduğu boş
    göze esas olmak üzere, bir çevrim oluşturulur ve çevrim üzerindeki gözeler,
    göze değiştirme yönteminde açıklandığı gibi, (+) ve (-) ile işaretlenir.
    Daha sonra çevrimin i’inci satırdaki çizgisi üzerindeki (-) işaretli göze
    belirlenir. Sonra sırasıyla (i, j) gözesi hariç (+) işaretli gözelerden
    kadar eksiltip, (-) işaretli gözelere kadar ekleme yapılarak değişkenlerin
    yeni değerleri hesaplanır.

**Örnek 3.18**: Birinci sunum merkezinin sunum miktarı ile üçüncü istem
merkezinin istem miktarının 10’ar birim artmasının en iyi çözüm üzerindeki
etkisini inceleyiniz.

**Çözüm 3.18**: Birinci sunum merkezi ile üçüncü istem merkezinin işaret ettiği
değişken x13 temelde olduğundan, x13’in yeni değeri, x13 = 20 + 10 = 30 olur. Bu
değişiklik sonucunda toplam maliyet 60 TL (= 6 x 10) artarak 655 TL olur.

**Örnek 3.19**: Birinci sunum merkezinin sunum miktarı ile beşinci istem
merkezinin istem miktarının 10’ar birim artmasının en iyi çözüm üzerindeki
etkisini inceleyiniz.

**Çözüm 3.19**: Birinci sunum merkezi ile üçüncü istem merkezinin işaret ettiği
değişken x15 temelde bulunmadığından, (1, 5) gözesi başlangıç olmak üzere bir
çevrim oluşturulur.

Çevrimdeki gözeler ile gözelere konulan işaretlerin,

(1, 5)(+), (2, 5)(-), (2, 3)(+), (1, 3)(-)

olduğu görülebilir.

İşaretler incelendiğinde, (2, 5) ile (1, 3) gözelerinin her birine onar birim
daha aktarılırken (2, 3)’e taşınan ürün miktarının 10 birim eksiltileceği
görülür. Buna göre çevrim üzerindeki değişkenlerin yeni değerleri,

x13 = 30 (= 20 + 10), x25 = 35 (= 25 + 10), x23 = 0 (= 10 - 10)

olur.

Diğer değişkenler aynı kalır.

Bu değişiklikler sonucunda yeni toplam maliyet, önceden olduğu gibi, 595’e eşit
olur.

### 3.8. Atama Problemİ

Atama problemi, ulaştırma probleminin özel bir şeklidir. Ulaştırma
problemlerinde olduğu gibi, atama problemlerinde de en uygun dağıtım planının
programlanması amaçlanmaktadır. Ancak dağıtımın mal taşınması ile ilişkisi
genellikle yoktur. Atama problemleri işçilerin işlere, işlerin makinelere, satış
elemanlarının satış bölgelerine, uçuşların uçuş hatlarına vb. atanmalarının
programlanmasında yaygın olarak kullanılmaktadır. Programlama bir işçi bir işe,
bir iş bir makineye, bir uçuş bir uçuş hattına, bir satış elemanı bir satış
bölgesine atanacak şekilde yani, bire bir eşleme ile gerçekleştirilir.

Her model gibi atama modeli de bazı varsayımlara dayanır. Esas olarak bir
ulaştırma modeli olduğundan ulaştırma modeli için yapılan varsayımlar atama
modeli için de geçerlidir.

Ulaştırma modelinin varsayımlarına ek olarak, m = n ve ai = 1 (i = 1, 2, ...,
n), bj = 1 (j = 1, 2, ..., n) olduğu varsayılmaktadır.

Bu varsayımın doğal sonucu olarak, i-j bire bir eşlemesini gerçekleştirme veya
i’yi j’ye ulaştırmanın maliyeti Cij olmak üzere, bir atama problemi matematiksel
olarak aşağıdaki gibi modellenir.

Zenk = 3.9

j = 1, 2, ..., n 3.10

i = 1, 2, ..., n 3.11

xij = 0 veya 1 i = 1, 2, ..., n , j = 1, 2, ..., n

3.10 ile 3.11’in uygun olabilmeleri için,

koşulunun sağlanması gerekir.

Ulaştırma problemlerinde olduğu gibi, atama problemlerinin çözümünde kullanılan
yöntem, problemin tablo esasında düzenlenmesini gerektirir. Matematiksel olarak
yukarıdaki gibi modellenen atama probleminin tablo gösterimi aşağıda
verilmiştir. Tablo incelendiğinde Cij’lerin bir kare matris oluşturdukları
görülecektir.

Tablo 3.30

|      | İş  |     |     |     |     |     |       |
|------|-----|-----|-----|-----|-----|-----|-------|
| İşçi | T1  | T2  | ... | Tj  | ... | Tn  | ai    |
| O1   | C11 | C12 | ... | C1j | ... | C1n | 1     |
| O2   | C21 | C22 | ... | C2j | ... | C2n | 1     |
| ...  | ... | ... | ... | ... | ... | ... | ...   |
| Oi   | Ci1 | Ci2 | ... | Cij | ... | Cin | 1     |
| ...  | ... | ... | ... | ... | ... | ... | ...   |
| On   | Cn1 | Cn2 | ... | Cnj | ... | Cnn | 1     |
| bj   | 1   | 1   | ... | 1   | ..  | 1   | n = n |

### 3.8.1. Atama Problemleri Çözüm Yöntemleri

Herhangi bir atama problemi, olanaklı tüm atamaların (bire bir eşlemelerin)
listelenmesiyle çözülebilir. Ancak bu yaklaşım yalnızca küçük boyutlu
problemlerde kullanılabilir. Problemin boyutu büyüdükçe, listeleme çok zor hatta
imkansızdır. n iş, n işçinin olduğu durumda listelenecek bire-bir eşleme sayısı
n’e eşittir. Örneğin 5 iş, 5 işçinin olduğu bir problemde, 5 = 120 farklı atama
yapılabilir. n = 10 için bu sayı 10! = 3628800 olur.

Daha önce açıklandığı gibi esas olarak bir tür ulaştırma problemi olması
nedeniyle, herhangi bir atama problemi, ulaştırma problemlerinin klasik çözüm
yöntemleriyle ve aynı süreç izlenerek çözülebilir. Ancak, bilinen yöntemlerden
hangisi kullanılırsa kullanılsın, başlangıç çözümü dahil, bütün çözümler bozuk
olacaktır. Çünkü, ulaştırma problemlerinde temel bir çözüm için dolu göze
sayısının (m + n - 1 = 2n - 1) olması gerekirken, atama problemlerinde dağıtım
yapılacak göze sayısı her zaman n olmak zorundadır. Atama problemleri,
kendilerine özgü tekniklerle daha az zaman harcayarak ve daha az işlem yapılarak
çözülebilir. Burada Macar yöntemi açıklanacaktır.

Atama problemlerinin çözümünde kullanılan Macar yöntemi Macar matematikçi D.
Konig tarafından formüle edilen sisteme dayanmaktadır. Bu sistem "elemanları
kısmen sıfır kısmen de sıfırdan farklı pozitif sayılar olan her kare matris için
bağlantı doğrularının minimum sayısı, bağımsız noktaların maksimum sayısına
eşittir" ifadesine dayanmaktadır. Macar yönteminin uygulanabilmesi için,
Cij’lerin negatif olmaması gerekir.

Yöntem, atama matrisinin herhangi bir satır veya sütununun tüm elemanlarına
sabit bir sayının eklenmesi veya çıkarılmasının en iyi çözüme etki etmediği
esasına dayanır. Sözgelimi, herhangi bir işi birinci makinede yapmanın maliyeti
k birim azaltıldığında atama probleminin amaç fonksiyonu, aşağıdaki gibi olur.

Z =

=

Burada, i = 1, 2, ..., n için = 1 olduğundan, yukarıda açıklanan amaç fonksiyonu
aşağıdaki gibi açıklanabilir.

Z = (Orijinal amaç fonksiyonu) - k

Amaç fonksiyonunun orijinalinde bulunan bir sabitin (eklenmiş veya çıkartılmış)
göz ardı edilmesinin en iyi çözümü etkilemediği bilinmektedir. Bu durum göz
önünde bulundurularak, negatif eleman kapsayan bir maliyet matrisinin ilgili
eleman veya elemanları negatif olmayan değerlere dönüştürülebilir.

Bu önemli hatırlatmadan sonra Macar yöntemini açıklayabiliriz. Macar yöntemi
esas olarak dört işlemsel adımla uygulanır:

1\. Adım: Maliyet matrisinin her bir satırının en küçük değeri, bulunduğu satırın
tüm elemanlarından çıkartılır. Bu işlemle elde edilen matrise satırları
indirgenmiş matris denir.

2\. Adım: Birinci adımda oluşturulan indirgenmiş matrisin her bir sütununun en
küçük değeri bulunduğu sütunun tüm elemanlarından çıkartılır. Bu yolla
"satırları-sütunları indirgenmiş" bir maliyet (sonuç) matrisi elde edilir.

3\. Adım: İkinci adımda belirlenen matrisin sıfır değerli elemanlarından geçen en
az sayıdaki çizgiler çizilir. Koruma çizgisi adı verilen bu çizgilerin en az
sayıda olması kuraldır. Koruma çizgilerinin çizimi konusunda kararsızlığa
düşmemek için, çizme işlemine sıfırı en çok olan satır veya sütunlardan
başlanması önerilebilir. Koruma çizgisi sayısı matrisin satır/sütun sayısına
eşit ise en iyi çözüm elde edilmiş olur. Sıfır değerine sahip gözelere, bire bir
olmak koşuluyla, yapılacak atamalar sonunda en iyi çözüme ulaşılır. Çizilen en
az sayıdaki çizgilerin sayısı n’ye eşit değilse dördüncü adıma geçilir.

4\. Adım: Üzerinden çizgi geçmeyen elemanların en küçük değerli olanı belirlenir.
Bu elemanın değeri üzerinden çizgi geçmeyen diğer bütün elemanlardan çıkartılır.
Aynı değer çizgilerin kesişme noktalarındaki sayılara eklenir. Üzerinden çizgi
geçen diğer elemanlar değişmeden kalır. Bu işlemlerden sonra üçüncü adıma
dönülür.

En iyi çözüm bulununcaya kadar üçüncü ve dördüncü adımlar tekrarlanır.

**Örnek 3.20**: Beş makinesi bulunan bir firma beş farklı iş siparişi almıştır.
Bu işlerin en kısa sürede tamamlanması istenmektedir. Makinelerin işleri
tamamlama süreleri aşağıdaki tabloda verilmiştir.

İşlerin en kısa toplam sürede tamamlanması istenmektedir. İşlerin en kısa sürede
tamamlanmasını sağlayacak iş-makine eşleşmesini bulunuz.

**Tablo 3.31**

|    | Makine |   |   |       |       |       |
|----|--------|---|---|-------|-------|-------|
| İş | 1      | 2 | 3 | 4     | 5     | ai    |
| A  | **2**  | 4 | 9 | **7** | 10    | 1     |
| B  | 4      | 6 | 8 | **2** | 3     | 1     |
| C  | **5**  | 7 | 9 | 11    | 13    | 1     |
| D  | 10     | 9 | 8 | 7     | **6** | 1     |
| E  | 5      | 5 | 3 | 4     | **2** | 1     |
| bj | 1      | 1 | 1 | 1     | 1     | 5 = 5 |

**Çözüm 3.20**: Öncelikle her bir satırın en küçük değerli elemanının
belirlenmesi gerekmektedir. Satır en küçükleri Tablo 3.31’de koyu
basılmışlardır. Her bir satırdaki en küçük değerin bulunduğu satırın diğer
elemanlarından çıkartılmasıyla satırları indirgenmiş süre matrisi aşağıdaki gibi
elde edilir.

**Tablo 3.32**

|    | Makine |       |       |       |       |       |
|----|--------|-------|-------|-------|-------|-------|
| İş | 1      | 2     | 3     | 4     | 5     | ai    |
| A  | **0**  | **2** | 7     | 5     | 8     | 1     |
| B  | 2      | 4     | 6     | **0** | 1     | 1     |
| C  | **0**  | **2** | 4     | 6     | 8     | 1     |
| D  | 4      | 3     | 2     | 1     | **0** | 1     |
| E  | 3      | 3     | **1** | 2     | **0** | 1     |
| bj | 1      | 1     | 1     | 1     | 1     | 5 = 5 |

İkinci olarak, satırları indirgenmiş matrisin her bir sütunundaki en küçük
değerli eleman belirlenecek ve bunlar bulundukları sütunun tüm elemanlarından
çıkarılacaktır. Sütun en küçükleri satırları indirgenmiş matrisde koyu
basılmışlardır. Çıkartma işleminin tamamlanmasıyla elde edilen, satırları ve
sütunları indirgenmiş matris Tablo 3.33’de gösterilmiştir.

Bundan sonra, en iyi atama planına ulaşılıp ulaşılmadığını araştırmak amacıyla,
satır-sütun indirgenmiş süre tablosundaki bütün sıfır değerlerinden geçen en az
sayıdaki çizgiler çizilecektir.

**Tablo 3.33**

|    | Makine |       |       |       |       |       |
|----|--------|-------|-------|-------|-------|-------|
| İş | 1      | 2     | 3     | 4     | 5     | ai    |
| A  | **0**  | 0     | 6     | 5     | 8     | 1     |
| B  | 2      | 2     | 5     | **0** | 1     | 1     |
| C  | 0      | **0** | 3     | 6     | 8     | 1     |
| D  | 4      | 1     | 1     | 1     | **0** | 1     |
| E  | 3      | 1     | **0** | 2     | 0     | 1     |
| bj | 1      | 1     | 1     | 1     | 1     | 5 = 5 |

Çizilen çizgi sayısı satır/sütun sayısına eşit olduğundan en iyi atama planı
elde edilmiştir. En iyi atama planı, Tablo 3.33’de koyu basılmış sıfırların
bulunduğu gözelerin dikkate alınmasıyla, aşağıdaki gibi elde edilir.

İş A Mak. 1, İş B Mak. 4, İş C Mak. 2, İş D Mak. 5, İş E Mak. 3

En iyi olduğu belirlenen bu plana göre işlerin tamamlanması için gereken en kısa
süre aşağıdaki gibi hesaplanır.

Zenk = CA1 + CB4 + CC2 + CD5 + CE3 = 2 + 2 + 7 + 6 + 3 = 20 saat

Görüldüğü gibi Örnek 3.20’nin en iyi çözümü Macar yönteminin ilk üç adımının
uygulanmasıyla belirlenmiştir.

En iyi atama planı her zaman bu kadar çabuk elde edilmez. Tüm adımların
kullanılmasını gerektiren problemlerle karşılaşmak daha olağandır. Macar
yönteminin tüm adımlarının kullanıldığı bir problem örneği aşağıda verilmiştir.

**Örnek 3.21**: Bir araştırma şirketinin elinde beş proje, bu projelerde
görevlendireceği beş araştırmacısı vardır. Araştırmacıların projelere göre
günlük ücretleri (TL) aşağıdaki tabloda gösterilmiştir. Şirket,
araştırmacılarını günlük ücretler toplamını en küçükleyecek biçimde dağıtmak
istemektedir. Günlük ücret toplamını en küçükleyecek proje-araştırmacı
eşleşmesini bulunuz.

**Tablo 3.34**

|             | Proje |       |    |    |       |
|-------------|-------|-------|----|----|-------|
| Araştırmacı | P1    | P2    | P3 | P4 | P5    |
| A1          | **2** | 4     | 5  | 6  | 8     |
| A2          | **3** | 5     | 6  | 4  | 5     |
| A3          | 6     | **1** | 2  | 3  | 4     |
| A4          | 5     | 7     | 8  | 9  | **1** |
| A5          | **2** | 3     | 5  | 9  | 10    |

**Çözüm 3.21**: Tablo 3.34’de koyu basılmış en küçük değerlerin ait oldukları
satırın tüm elemanlarından çıkartılmasıyla elde edilen satırları indirgenmiş
ücret matrisi aşağıda gösterilmiştir.

**Tablo 3.35**

|             | Proje |       |       |       |       |       |
|-------------|-------|-------|-------|-------|-------|-------|
| Araştırmacı | P1    | P2    | P3    | P4    | P5    | ai    |
| A1          | **0** | 2     | 3     | 4     | 6     | 1     |
| A2          | **0** | 2     | 3     | **1** | 2     | 1     |
| A3          | 5     | **0** | **1** | 2     | 3     | 1     |
| A4          | 4     | 6     | 7     | 8     | **0** | 1     |
| A5          | **0** | 1     | 3     | 7     | 8     | 1     |
| bj          | 1     | 1     | 1     | 1     | 1     | 5 = 5 |

Daha fazla sıfır elde etmek için satırları indirgenmiş matrisin her bir
sütununun en küçük değerli elemanının (Tablo 3.35’de koyu basılmış) bulunduğu
sütununun tüm elemanlarından çıkartılmasıyla elde edilen satırları ve sütunları
indirgenmiş matris Tablo 3.36’da gösterilmiştir.

**Tablo 3.36**

|             | Proje |       |       |       |       |       |
|-------------|-------|-------|-------|-------|-------|-------|
| Araştırmacı | P1    | P2    | P3    | P4    | P5    | ai    |
| A1          | **0** | 2     | 2     | 4     | 6     | 1     |
| A2          | **0** | 2     | 2     | **0** | 2     | 1     |
| A3          | 5     | **0** | **0** | 1     | 3     | 1     |
| A4          | 4     | 6     | 6     | 7     | **0** | 1     |
| A5          | **0** | 1     | 2     | 6     | 8     | 1     |
| bj          | 1     | 1     | 1     | 1     | 1     | 5 = 5 |

Satırları ve sütunları indirgenmiş matrisin sıfırlarını kapatan koruma
çizgileri, yoklama ile Tablo 3.36’daki gibi çizilmiştir. Tablodan görüldüğü
gibi, çizilen çizgi sayısı dörde eşittir. Bu durumda, beş atamadan ancak dördü
gerçekleştirileceğinden daha çok sıfır oluşturmak için dördüncü adıma geçilmesi
gerekir.

Üzerinden çizgi geçmeyen en küçük değerli eleman 1’dir. Bu en küçük değerin
çizgilerin kesişim noktalarındaki elemanlara eklenmesi, üzerinden çizgi geçmeyen
elemanlardan çıkartılmasıyla daha çok sıfır kapsayan yeni matris Tablo 3.37’deki
gibi elde edilir. Tablo 3.37’deki matrisin sıfır değerli elemanlarını kapatan
koruma çizgileri yine yoklama ile Tablo 3.37’deki gibi çizilmiştir.

**Tablo 3.37**

|             | Proje |       |       |       |       |       |
|-------------|-------|-------|-------|-------|-------|-------|
| Araştırmacı | P1    | P2    | P3    | P4    | P5    | ai    |
| A1          | **0** | 1     | 1     | 2     | 5     | 1     |
| A2          | 1     | 2     | 2     | **0** | 2     | 1     |
| A3          | 6     | 0     | **0** | 1     | 3     | 1     |
| A4          | 5     | 6     | 6     | 7     | **0** | 1     |
| A5          | 0     | **0** | 1     | 5     | 7     | 1     |
| bj          | 1     | 1     | 1     | 1     | 1     | 5 = 5 |

Çizilen çizgi sayısı 5’e eşit olduğundan en iyi çözüm elde edilmiştir. Buna
göre, A1 P1, A2 P4, A3 P3, A4 P5, A5 P2 eşlemeleriyle en küçük günlük toplam
ücret aşağıdaki gibi hesaplanacaktır.

Zenk = C11 + C24 + C33 + C45 + C52 = 2 + 4 + 2 + 1 + 3 = 12 TL

Atama probleminde amaç toplam satış gelirinin veya toplam kârın en büyüklenmesi
de olabilir. En büyükleme amaçlı bir atama probleminin çözümü için aşağıdaki
adımların izlenmesi gerekir.

1.  Kazanç matrisindeki en büyük değerin belirlenmesi.

2.  En büyük olduğu belirlenen değerden matris elemanlarının tek tek
    çıkartılarak yeni bir matris oluşturulması. Bu matrise düzeltilmiş matris
    denir. Düzeltilmiş matris elemanları kayıp veya maliyet gösterir.

Düzeltilmiş matrisin oluşturulmasından sonra yapılacak işlemler en küçükleme
problemlerindeki gibidir. Düzeltilmiş matrisli atama problemi için belirlenen en
iyi çözüm orijinal atama probleminin de en iyi çözümü olur.

**Örnek 3.22**: Bir pazarlama şirketinin piyasaya yeni süreceği ürünü için 5
farklı bölgede görevlendireceği beş satış elemanı vardır. Görevlendirilecek
satış elemanına göre, bölgelerden beklenen satış gelirleri Tablo 3.38’de
verilmiştir. Toplam satış gelirini en büyükleyecek dağıtım planını belirleyiniz.

**Tablo 3.38**

| Satış   | Bölge  |    |   |    |    |       |
|---------|--------|----|---|----|----|-------|
| Elemanı | 1      | 2  | 3 | 4  | 5  | ai    |
| A       | 8      | 9  | 8 | 4  | 5  | 1     |
| B       | 5      | 6  | 7 | 10 | 10 | 1     |
| C       | 9      | 4  | 5 | 9  | 7  | 1     |
| D       | 6      | 7  | 5 | 6  | 6  | 1     |
| E       | 10     | 12 | 7 | 10 | 7  | 1     |
| bj      | 1      | 1  | 1 | 1  | 1  | 5 = 5 |

**Çözüm 3.22**: Kazanç matrisinin en büyük elemanı olan 12’den matrisin her bir
elemanının çıkartılmasıyla elde edilen düzeltilmiş matrisli tablo aşağıda
gösterilmiştir.

## Tablo 3.39

| Satış   | Bölge |       |   |       |       |       |
|---------|-------|-------|---|-------|-------|-------|
| Elemanı | 1     | 2     | 3 | 4     | 5     | ai    |
| A       | 4     | **3** | 4 | 8     | 7     | 1     |
| B       | 7     | 6     | 5 | **2** | **2** | 1     |
| C       | **3** | 8     | 7 | **3** | 5     | 1     |
| D       | 6     | **5** | 7 | 6     | 6     | 1     |
| E       | 2     | **0** | 5 | 2     | 5     | 1     |
| bj      | 1     | 1     | 1 | 1     | 1     | 5 = 5 |

Bu aşamadan sonraki işlemler, en küçükleme amaçlı atama problemlerindeki
gibidir. Her bir satırın en küçük değerli elemanının (Tablo 3.39’da koyu
basılmış) belirlenmesi ve bu değerin ait olduğu satırın tüm elemanlarından
çıkartılmasıyla elde edilen satırları indirgenmiş matrisli tablo aşağıda
gösterilmiştir.

Her sütunda en az bir tane sıfır olduğu için sütun indirgeme işleminin yapılması
gerekmez. Kapama çizgilerinin çizilmesi yeterlidir.

**Tablo 3.40**

| Satış   | Bölge |   |   |   |   |       |
|---------|-------|---|---|---|---|-------|
| Elemanı | 1     | 2 | 3 | 4 | 5 | ai    |
| A       | 1     | 0 | 0 | 5 | 4 | 1     |
| B       | 5     | 4 | 2 | 0 | 0 | 1     |
| C       | 0     | 5 | 3 | 0 | 2 | 1     |
| D       | 1     | 0 | 1 | 1 | 1 | 1     |
| E       | 2     | 0 | 4 | 2 | 5 | 1     |
| bj      | 1     | 1 | 1 | 1 | 1 | 5 = 5 |

Tablo 3.40’daki matrisin sıfırlarını kapatan en az sayıdaki çizgilerin sayısı
5’e eşit olmadığından dördüncü adıma geçilir. Üzerinden çizgi geçmeyen
elemanların en küçüğü olan 1’in üzerinden çift çizgi geçen sayılara eklenmesi,
üzerinden çizgi geçmeyen tüm elemanlardan çıkartılmasıyla elde edilen ayarlanmış
matris Tablo 3.41’de gösterilmiştir.

Tablo 3.41’de görüldüğü gibi bütün sıfırların üzerinden geçen en az sayıdaki
çizgilerin sayısı, satır ve sütun sayısına eşit olduğundan bu adımda yapılacak
atamalar sonunda ortaya çıkacak çözüm en iyidir.

**Tablo 3.41**

| Satış   | Bölge |       |       |       |       |       |
|---------|-------|-------|-------|-------|-------|-------|
| Elemanı | 1     | 2     | 3     | 4     | 5     | ai    |
| A       | 1     | 1     | **0** | 5     | 4     | 1     |
| B       | 5     | 5     | 2     | **0** | 0     | 1     |
| C       | **0** | 6     | 3     | 0     | 2     | 1     |
| D       | 0     | 0     | 0     | 0     | **0** | 1     |
| E       | 1     | **0** | 3     | 1     | 4     | 1     |
| bj      | 1     | 1     | 1     | 1     | 1     | 5 = 5 |

Koyu renk basılmış sıfırlara sahip gözelere yapılacak atamalar sonucunda
aşağıdaki en iyi atama planı A 3, B 4, C 1, D 5, E 2 olarak elde edilmiş olur.
Bu atama planına göre günlük satış gelirinin en büyük değeri aşağıdaki gibi
hesaplanır.

Zenb = CA3 + CB4 + CC1 + CD5 + CE2 = 8 + 10 + 9 + 6 + 12 = 45 TL

Bir atama probleminde m n ise öncelikle m = n koşulunun sağlanması gerekir. m \>
n ise atama matrisine (m - n) satır, m \< n ise (n - m) sütun eklenir. Eklenen
satır veya sütunlardaki tüm Cij’ler sıfıra eşittir. Bu düzenlemeden sonra
problem, yukarıda açıklanan adımların aynen izlenmesiyle, kolayca çözülebilir.

# 

# PROBLEMLER

**1**. Tabloları aşağıda verilen ulaştırma problemlerini modelleyerek simpleks
çözüm başlangıç tablolarını düzenleyiniz.

**2**. Tabloları yukarıda verilen problemlerin en iyi çözümlerini,

1.  Kuzey batı köşesi ve göze değiştirme yöntemiyle,

2.  VAM ve göze değiştirme yöntemiyle,

3.  VAM ve modi yöntemiyle,

4.  En düşük maliyetli gözeler yönteminin satır, sütun, genel yaklaşımları ve
    modi yöntemiyle belirleyiniz.

5.  Yöntemlerin etkinliklerini karşılaştırınız.

6.  Problemleri modelleyiniz.

**3.** Aşağıdaki ulaştırma problemini VAM ve modi yöntemiyle çözünüz.

**4**. Aşağıdaki problemi kuzey batı köşesi ve modi yöntemiyle çözünüz.

**5.** Ulaştırma tablosu aşağıda verilen ulaştırma problemini,

1.  Kuzey-batı köşesi ve göze değiştirme yöntemiyle,

2.  VAM ve göze değiştirme yöntemiyle,

3.  En küçük maliyetli gözelerin genel yaklaşımı ve modi yöntemiyle çözünüz.

4.  Ulaştırma modeli olarak formülleyiniz.

5.  Probleme sunum kapasitesi 25 birim olan bir fabrika eklenmesinin en iyi
    çözüme etkisini inceleyiniz.

6.  Probleme istemi 25 birim olan bir deponun eklenmesinin en iyi çözüme
    etkisini inceleyiniz.

7.  En iyi çözümün en iyi olma özelliğini koruması için her temel olmayan
    değişken için en küçük Cij değerini belirleyiniz.

**6**. Ayşe Hanım’ın Mayıs, Haziran, Temmuz, Ağustos aylarını kapsayan dört
aylık bir tatili vardır. Ayşe Hanım tatilinin her bir ayını farklı bir tatil
beldesinde geçirmek istemektedir. Aylara göre farklı beldelerde tatil yapmanın
maliyetleri aşağıdaki tabloda gösterilmiştir. En küçük toplam maliyetli tatil
planını belirleyiniz.

|  Tatil   |  Ay   |         |        |         |
|----------|-------|---------|--------|---------|
|  Beldesi | Mayıs | Haziran | Temmuz | Ağustos |
| Bodrum   | 50    | 45      | 50     | 75      |
| Kemer    | 60    | 90      | 80     | 100     |
| Alanya   | 40    | 100     | 90     | 50      |
| Kuşadası | 30    | 30      | 20     | 50      |

**7**. Bir araba kiralama firmasının elinde markaları farklı beş kiralık arabası
vardır. Araba kiralamak isteyen beş kişinin arabalara ödemeyi kabul ettikleri
kira bedelleri aşağıda gösterilmiştir.

Hangi kişiye hangi arabanın kiralanması durumunda firmanın günlük kira geliri en
büyük olur?

|         |  Marka |       |      |        |       |
|---------|--------|-------|------|--------|-------|
| Müşteri | Uno    | Şahin | Tipo | Kartal | Doğan |
| Deniz   | 150    | 290   | 175  | 200    | 500   |
| Sinan   | 160    | 90    | 400  | 150    | 100   |
| Cihan   | 240    | 100   | 450  | 230    | 250   |
| Ayşe    | 300    | 400   | 250  | 250    | 350   |
| Barış   | 330    | 30    | 300  | 230    | 500   |

**8**. Beş makinesi bulunan bir firma dört farklı iş siparişi almıştır. Bu
işlerin en kısa sürede tamamlanması istenmektedir. Makinelerin işleri tamamlama
süreleri aşağıdaki tabloda verilmiştir. İşlerin en kısa toplam sürede
tamamlanması istenmektedir. Bu amacı gerçekleştirecek iş-makine eşleşmesini
bulunuz.

|    | Makine |    |    |    |    |     |
|----|--------|----|----|----|----|-----|
| İş | 1      | 2  | 3  | 4  | 5  | ai  |
| A  | 12     | 10 | 9  | 7  | 6  | 1   |
| B  | 10     | 9  | 12 | 20 | 21 | 1   |
| C  | 18     | 10 | 9  | 9  | 8  | 1   |
| D  | 10     | 19 | 18 | 20 | 10 | 1   |
| bj | 1      | 1  | 1  | 1  | 1  | 4 5 |
