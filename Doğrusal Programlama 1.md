## İKİNCİ BÖLÜM

**DOĞRUSAL PROGRAMLAMA**

# 2.1. GİRİŞ

Günlük yaşantımızın hemen her anında, sahip olduğumuz kısıtlı kaynakların -para,
zaman, güç, yetenek vb.- sınırlayıcı koşulları altında davranmak zorunda
kalırız. Bu durum işletmeler için de geçerlidir. Sınırsız kaynaklara sahip bir
işletmeyle karşılaşmak imkansız gibidir. Bu yüzden, yönetim kararlarının çoğu
makine-techizat, para, emek, zaman, depolama kapasitesi, hammadde gibi
kaynakların ürün (makine-techizat, deterjan, gıda, giyecek, mobilya vb.)
üretiminde veya servis (taşıma ve üretim programlanması, reklam veya yatırım
planlanması vb.) hizmetlerinde etkin kullanımının sağlanmasıyla ilgilidir.
Doğrusal programlama kaynak kullanımıyla ilgili planlama ve karar almada karar
vericiye yol gösteren etkin bir matematiksel programlama tekniğidir. Gerçekte
kökeni çok eskilere, 1920’li yıllara kadar uzanmakla birlikte, doğrusal
programlama bugünkü anlamıyla ilk kez 1947 yılında ABD’nin askeri faaliyetlerini
planlamak amacıyla B. Dantzig tarafından geliştirilmiştir. Doğrusal
programlamanın gelişip önem kazanması "simpleks yöntem" olarak bilinen yöntemin
önerilmesinden sonra gerçekleşmiştir. Bilgisayar teknolojisinin hızlı gelişmesi
sonucunda doğrusal programlama endüstri, çevre, pazarlama, ulaştırma, enerji,
tarım ve sosyal problemlerin çözümünde yaygın olarak kullanılmaya başlanmıştır.

# 2.2. DOĞRUSAL PROGRAMLAMA PROBLEMİ

Herhangi bir problemin doğrusal programlama problemi olabilmesi için bazı
koşulları sağlaması gerekir. Bu koşullar aşağıda açıklanmıştır.

1.  Karar vericinin ulaşmak istediği bir amacı olmalıdır.

2.  İçlerinden en az bir tanesi amacı gerçekleştirecek olan alternatif
    stratejiler bulunmalıdır.

3.  Kaynakların sunumu sınırlı olmalıdır.

4.  Amaç, matematiksel olarak açıklanabilmeli ve kullanılan kaynakların
    sınırları eşitlik ve/veya eşitsizlikler biçiminde gösterilebilmelidir. Bu
    eşitlik veya eşitsizliklerin hepsi doğrusal olmalıdır.

Bu koşullar varsa problem, doğrusal programlama problemidir. Buradaki doğrusal
sözcüğü, iki veya daha fazla değişken arasındaki ilişkinin doğrusal olduğunu,
programlama sözcüğü ise çözüme belirli matematiksel teknikler kullanılarak
ulaşıldığını açıklamaktadır. Doğrusal ve programlama sözcükleri için yapılan
tanımların ve yukarıda açıklanan koşulların dikkate alınmasıyla doğrusal
programlama aşağıdaki gibi tanımlanabilir.

*Doğrusal Programlama*: Belirli doğrusal eşitliklerin veya eşitsizliklerin
kısıtlayıcı koşulları altında, doğrusal bir amaç fonksiyonunu en iyi (optimum)
kılan değişken değerlerinin belirlenmesi amacıyla gerçekleştirilen işlemler
kümesine doğrusal programlama denir.

En iyileme (optimizasyon) iki yolla gerçekleştirilir.

1\. Amaç fonksiyonu değerinin en büyüklenmesi (maksimizasyon)

2\. Amaç fonksiyonu değerinin en küçüklenmesi (minimizasyon)

Genellikle, olanaklar çerçevesinde toplam kârın en büyüklenmesi veya toplam
maliyetin en küçüklenmesi türündeki problemlerle karşılaşılmakla birlikte
değişik nitelikte amaçlar (en kısa süre, en kısa mesafe, en büyük gelir vb.) da
dikkate alınabilir.

# 2.3. DOĞRUSAL PROGRAMLAMA MODELLEMESİ

Bir tanıma göre model, anlaşılması güç ve karmaşık sistemlerin veya problemlerin
bir takım varsayımlarla basitleştirilmiş soyut bir temsilcisidir. Bir modelin
dayandığı varsayımların azlığı ya da çokluğu, o modelin uygulanabilirliği ve
yararlılığı açısından büyük bir önem taşır. Herhangi bir modelden gereği gibi
yararlanabilmek için modelin dayandığı varsayımların iyi bilinmesi gerekir.

### 2.3.1. Doğrusal Programlamanın Varsayımları

Her model gibi, doğrusal programlama modelleri de bir takım varsayımlara
dayanmaktadır. Bu varsayımlar aşağıdaki gibi açıklanabilir.

1.  Doğrusallık: Modeli oluşturan fonksiyonların hepsi doğrusal olmalıdır. Bu
    varsayıma açıklık kazandırmak için amaç fonksiyonunun Z = 3x1 + 8x2 olarak
    düzenlendiğini ve x1 = 10 olarak belirlendiğini düşünelim. Bu durumda amaç
    fonksiyonunun değeri Z = 3(10) + 8x2 olur. x1’in değeri 3 kat arttığında
    x1’in Z’ye katkısı da 3 kat artarak, Z = 3(30) + 8x2 olur. Bu artış x2’den
    bağımsızdır. Aynı durum x2 için de geçerlidir. Yani, x2’nin değeri sözgelimi
    20 kat arttığında x2’nin Z’ye katkısı da 20 kat artar. Bu artış x1’den
    bağımsızdır.

    Doğrusallık varsayımının kısıtlayıcı fonksiyonlardaki sonucu aynı yaklaşımla
    incelenebilir. Kısıtlayıcı fonksiyonun sol tarafı 1.5x1 + 3x2 olsun. x2 = 3
    iken sol taraf 1.5x1 + 3(3) olur. x2 = 30 olduğunda, yani değeri 10 kat
    arttığında kısıtlayıcının sol tarafına katkısı da aynı oranda (10 kat)
    artarak 1.5x1 + 3(30) olur. Bu artış x2’den bağımsızdır. Aynı durum diğer
    değişken için de geçerlidir.

    Değişken değerlerindeki artışın (azalışın) gerek amaç gerekse kısıtlayıcı
    fonksiyonlarda yol açtığı artış (azalış) arasındaki bu ilişki doğrusal
    programlamanın orantılı olma (oransallık) varsayımı olarak bilinir.

2.  Toplanabilirlik: Doğrusallık varsayımı değişkenlerin birbirlerini
    etkilemediğini de ortaya koymaktadır. Değişkenlerin bağımsızlığı doğrusal
    programlamanın toplanabilirlik varsayımı olarak bilinir. Bu varsayımla tüm
    faaliyetlerin tamamlanmasıyla ortaya çıkan değerin tek tek faaliyetlerin
    ortaya çıkardığı sonuç değerleri toplamına eşit olduğu anlatılmak
    istenmektedir. Bu varsayım doğrusal programlamanın doğrusal olmayan
    ilişkilerin bulunduğu problemlere uygulanmasını imkansız kılar.

3.  Deterministik olma (kesinlik-belirlilik): Doğrusal programlama modellerini
    oluşturan parametrelerin (Cj, aij, bi) bilindiği ve öngörülen dönem içinde
    değişmediği kabul edilir. Modelin bu parametrelerdeki değişimlere ne denli
    duyarlı olduğunun saptanmasına ilişkin işlemlerin tümü, duyarlılık
    çözümlemesi kapsamında yer alır. Bu konu ileride incelenecektir.

4.  Negatif olmama: Değişkenlerin negatif değer alamıyacağı, pozitif veya en
    azından sıfıra eşit olacağı düşüncesinin ürünü olan bir varsayımdır.

5.  Süreklilik: Değişkenlerin sürekli oldukları kabul edilir. Yani, karar
    değişkenleri negatif olmamak koşuluyla herhangi bir değer alabilir.
    Süreklilik varsayımına bölünebilirlik varsayımı da denir. Ancak, verilmiş
    durum nedeniyle, değişkenlerden bir ya da birkaçının veya hepsinin tamsayı
    olması uygulamada çok sık olarak ortaya çıkmaktadır. Değişkenlerin tamsayı
    olması istendiğinde, tamsayılı programlama söz konusu olur.

### 2.3.2. Doğrusal Programlama ile Modelleme

Doğrusal programlama modellerinin kurulması ile ilgili örnek problemlere
geçmeden önce, herhangi bir problemin doğrusal programlama modeli olarak ifade
edilmesinde izlenmesi gereken adımları açıklayalım.

1.  Değeri belirlenecek değişkenlerin tanımlanması ve değişkenlerin uygun
    matematik sembollerle gösterilmesi: Doğrusal programlama karar alma yöntemi
    olduğundan, bu değişkenlere "karar değişkenleri" denir.

2.  Amacın belirlenerek, karar değişkenlerinin doğrusal fonksiyonu olarak
    yazılması: Karar vericinin amacını yansıtan bu fonksiyona "amaç fonksiyonu"
    denir. Değeri çözümün elde edilmesinden sonra belirlenir.

3.  Kısıtlamaların, karar değişkenlerinin doğrusal fonksiyonları olarak eşitlik
    veya eşitsizlik biçiminde ifade edilmesi: Karar değişkenlerinin değerlerini
    sınırlandıran kısıtları yansıtan bu fonksiyonlara "kısıtlayıcı fonksiyonlar"
    veya kısaca "kısıtlayıcılar" denir. Sistemin tanımlanmasında kullanılan
    kısıtlayıcıların değerleri kesin ve önceden belirlenmiştir.

Bu açıklamaların ışığı altında çeşitli işletme problemlerinin doğrusal
programlama modeli olarak formüllenmesine geçebiliriz. Modellenecek problemlerin
doğrusal programlamanın uygulandığı alanlardan olmasına özen gösterdiğimizi
belirtmeliyiz.

Doğrusal programlamanın uygulama alanları sayılamıyacak kadar çok ve çeşitlidir.
Yaygın olarak kullanıldığı alanlar aşağıda açıklandığı gibidir:

1\. Ulaştırma veya dağıtım problemleri: Belirli merkezlerde gerçekleştirilen
üretim işlemi sonrasında ortaya çıkan mal ve hizmetlerin belirli merkezlerin
istemini karşılamak amacıyla dağıtılmasında katlanılacak ulaştırma maliyetleri
toplamını en küçükleyecek dağıtım planının programlanması ulaştırma problemleri
kapsamındadır. Doğrusal programlama problemlerinin özel bir biçimi olarak
nitelendirilen ulaştırma problemlerinin doğrusal programlama problemi olarak
çözülebilmesi için yukarıda benimsenen varsayımlara ek olarak, diğer bazı
varsayımların gerçekleşmesi ve belirli koşulların sağlanması gerekir. Bu konu,
üçüncü bölümde ulaştırma modeli başlığı altında ayrıntılı bir biçimde
inceleneceğinden burada ulaştırma probleminin kısaca açıklanmasıyla
yetinilecektir.

2\. Üretim planlaması: İşletmelerin karşılaştığı problemlerin çoğu para, işgücü,
hammadde, araç-gereç, alan, zaman gibi kısıtlı kaynakların belirli amaçlar
doğrultusunda çeşitli üretim faaliyetleri arasında en uygun biçimde dağıtılması
ve kullanılması yoluyla, kârın en büyüklenmesi veya maliyetlerin en
küçüklenmesidir. Doğrusal programlama bu türden problemlerin çözümlenmesinde
kullanılabilecek etkin bir araçtır.

**Örnek 2.1**: Bir ahşap işleme atölyesinde biri çekmeceli diğeri çekmecesiz iki
tip ahşap sıra üretilmektedir. Üretim ahşabın doğranması, doğranan parçaların
birleştirilmesi ve kalite kontrol aşamalarından oluşmaktadır. Doğrama makinesi
bir günde en fazla 30 m3 ahşap doğrayabilmektedir. Parçaların
birleştirilmesinden sorumlu iki işçinin günlük çalışma kapasitesi toplam 18
saattir. Kalite kontrol bölümü bir günde en fazla 14 saat çalışabilmektedir. Bir
adet çekmeceli sıranın üretiminde 3 m3, bir adet çekmecesiz sıranın üretiminde 2
m3 ahşap kullanılmaktadır. Bir çekmeceli sıra 2 saatte, bir çekmecesiz sıra 1
saatte birleştirilmektedir. Hangi tip olursa olsun bir sıranın kontrol işlemi 1
saat sürmektedir. Bir adet çekmeceli sıranın satışından 40 TL, bir adet
çekmecesiz sıranın satışından 30 TL kâr elde edilmektedir. Problemi, çözümü
firmanın kârının en büyük olmasını sağlayacak sıra sayılarını verecek doğrusal
programlama modeli olarak formülleyiniz.

**Çözüm 2.1**: Yukarıda açıklandığı gibi bir doğrusal programlama probleminin
modellenmesi için,

1.  Karar değişkenlerinin tanımlanması ve bunların uygun matematik sembollerle
    gösterilmesi,

2.  Amaç fonksiyonunun yazılması,

3.  Tüm kısıtlamaların (negatif olmama koşulu dahil), karar değişkenlerinin
    doğrusal fonksiyonları olarak eşitlik veya eşitsizlik biçiminde ifade
    edilmesi gerekmektedir.

Şimdi bu aşamaları izleyerek üretim planlaması probleminin doğrusal programlama
modelini kuralım.

Karar değişkenlerinin tanımlanması ve uygun matematik sembollerle gösterilmesi:
Problemin çözümü ile her bir üründen kaçar adet üretileceğine karar
verilecektir. Buna göre karar değişkenleri aşağıdaki gibi tanımlanabilir.

x1: Çekmeceli sıra üretim miktarı (adet)

x2: Çekmecesiz sıra üretim miktarı (adet)

Amaç fonksiyonunun yazılması: x1 ve x2’nin yukarıda verilen tanımları göz önünde
bulundurulduğunda günlük toplam kâr aşağıdaki gibi yazılır.

Toplam kâr = Z = 40x1 + 30x2

Amaç en büyük kârı sağlamak olduğuna göre amaç fonksiyonu aşağıdaki gibi
yazılacaktır.

Zenb = 40x1 + 30x2

Tüm kısıtlamaların, karar değişkenlerinin doğrusal fonksiyonları olarak eşitlik
veya eşitsizlik biçiminde yazılması: İşletme üretimini, doğrama makinesi ile
birleştirme ve kalite kontrol bölümlerinin günlük çalışma kapasitelerini göz
önünde bulundurarak gerçekleştirmek zorundadır. Bu nedenle bu üç üretim
faktörünün günlük çalışma kapasitelerinin dikkate alınmasıyla her bir üretim
faktörü için bir tane olmak üzere üç kısıtlayıcı yazılması gerekir.

Önce doğrama makinesinin günlük çalışma kapasitesini dikkate alalım. Problemde
verildiği gibi makine bir günde en fazla 30 m3 ahşap doğrayabilmektedir. 1 adet
çekmeceli sıra için 3 m3 ahşap doğranacağına göre, x1 adet çekmeceli sıra için
3x1 m3 ahşap doğranmalıdır. Benzer şekilde, 1 adet çekmecesiz sıra için 2 m3
ahşap doğranması gerektiğine göre, x2 adet çekmeceli sıra için 2x2 m3 ahşap
doğranmalıdır. İki ürün birlikte düşünüldüğünde doğranacak ahşap miktarı, 3x1 +
2x2 olur. En fazla 30 m3 ahşap doğranabildiğinden 3x1 + 2x2 30 yazılır. Böylece
makinenin doğrama kapasitesi formüllenerek ilk kısıtlayıcı fonksiyon yazılmış
olur.

Şimdi de parçaların birleştirilmesinden sorumlu işçilerin çalışma kapasitelerine
ilişkin kısıtlayıcıyı yazalım. 1 adet çekmeceli sıra 2 saatte birleştirildiğine
göre, x1 adet çekmeceli sıranın birleştirilmesi toplam 2x1 saatte tamamlanır.
Benzer şekilde, 1 adet çekmecesiz sıra 1 saatte birleştirildiğine göre, x2 adet
çekmeceli sıra toplam x2 saatte birleştirilir. İki ürün birlikte düşünüldüğünde
toplam birleştirme zamanı 2x1 + x2 olur. Birleştirme bölümü bir günde en fazla
18 saat çalışılabildiğinden 2x1 + x2 18 olmalıdır. Böylece birleştirme bölümünün
günlük çalışma zamanı kapasitesi formüllenerek ikinci kısıtlayıcı fonksiyon
yazılmış olur.

Son olarak kalite kontrol bölümünün günlük çalışma zamanı kapasitesinin sınırını
belirten kısıtlayıcı fonksiyonu yazalım. 1 adet çekmeceli sıra 1 saatte kontrol
edildiğine göre x1 adet çekmeceli sıra x1 saatte kontrol edilir. Benzer şekilde,
1 adet çekmecesiz sıra 1 saatte kontrol edildiğine gore, x2 adet çekmecesiz
sıranın kontrolü x2 saatte tamamlanır. İki ürün birlikte düşünüldüğünde, toplam
birleştirme zamanı, x1 + x2 olur. Kontrol bölümü bir günde en fazla 14 saat
çalışılabildiğinden x1 + x2 14 olması gerekir. Böylece kalite kontrol bölümünün
günlük çalışma zamanı kapasitesi formüllenerek son kısıtlayıcı belirlenmiş olur.

Üretim miktarları negatif olamayacağından, x1, x2 0 yazılmasıyla problem
aşağıdaki gibi modellenmiş olur.

Zenb = 40x1 + 30x2

3x1 + 2x2 30 Makine zamanı kısıtlayıcısı

2x1 + x2 18 Birleştirme zamanı kısıtlayıcısı

x1 + x2 14 Kalite kontrol zamanı kısıtlayıcısı

x1, x2 0

3\. Beslenme (diyet) veya yem karışım problemleri: Beslenme sorununun hem
kişilerin yaşamında hem de ekonomilerde önemli bir yeri vardır. Doğrusal
programlama hayvanların dengeli beslenmelerini sağlayacak en küçük maliyetli yem
karışımının araştırılmasında, düşük maliyetli yemek listesinin oluşturulmasında,
benzin veya bazı tekstil ürünleri ile ilgili karışımların belirli ölçütleri
sağlayacak biçimde hazırlanmasında yaygın biçimde kullanılmaktadır. Bu tür
problemlerde amaç genellikle, maliyetin en küçüklenmesidir.

**Örnek 2.2**: Dengeli beslenmek için bir günde en az 60 birim A, 40 birim B, 32
birim C vitamini alınması gerektiği bilinmektedir. Bu vitaminlerin bulunduğu iki
çeşit sebze (havuç ve ıspanak) vardır. 1 kg havuç 15 birim A, 10 birim B, 4
birim C; 1 kg ıspanak 4 birim A, 15 birim B, 16 birim C içermektedir. Havucun
fiyatı 3 TL, ıspanağın fiyatı 2 TL’dir. Günlük vitamin gereksinmesini en düşük
harcamayla karşılayacak sebze miktarlarını belirleyiniz.

**Çözüm 2.2**: Örnek 2.1’deki gibi önce karar değişkenlerini tanımlayalım.

Karar değişkenleri: Her bir sebzeden kaçar kg tüketileceğinin kararlaştırılacağı
bu problemde karar değişkenleri aşağıdaki gibi tanımlanabilir.

x1: Günlük havuç tüketim miktarı (kg)

x2: Günlük ıspanak tüketim miktarı (kg)

1 kg havuç 3 TL olduğuna göre x1 kg havucun maliyeti 3x1 TL, 1 kg ıspanak 2 TL
olduğuna göre x2 kg ıspanağın maliyeti 2x2 olur. Bu durumda x1 kg havuç, x2 kg
ıspanak satın almanın maliyeti,

Toplam maliyet = Z = 3x1 + 2x2

olur.

Amaç, bu toplamın en küçük olmasını sağlamak olduğuna göre, amaç fonksiyonu
aşağıdaki gibi yazılır.

Zenk = 3x1 + 2x2

Bir kg havuçta 15 birim A bulunduğuna göre, x1 kg havuçta 15x1 birim A bulunur.
Benzer şekilde 1 kg ıspanak 4 birim A içerdiğine göre, x2 kg ıspanak 4x2 birim A
içerir. Bu durumda x1 kg havuç, x2 kg ıspanak tüketildiğinde toplam 15x1 + 4x2
birim A alınmış olur. En az 60 birim A vitamini alınması gerektiğinden 15x1 +
4x2 60 olur. Bu eşitsizlik A vitamini kısıtlayıcısıdır. Benzer şekilde B
vitamini kısıtlayıcısı,

10x1 + 15x2 40

C vitamini kısıtlayıcısı,

4x1 + 16x2 32

olur.

Negatif tüketim söz konusu olamayacağına göre, x1, x2 0 yazılmasıyla model
tamamlanmış, problem aşağıdaki gibi formüle edilmiş olur.

Zenk = 3x1 + 2x2

15x1 + 4x2 60 A vitamini kısıtlayıcısı

10x1 + 15x2 40 B vitamini kısıtlayıcısı

4x1 + 16x2 32 C vitamini kısıtlayıcısı

x1, x2 0

Kısıtlayıcılardaki işareti alınması gereken vitamin miktarlarının belirtilen
değerlerin altına düşmeyeceğini fakat, bu miktarlardan fazla olabileceğini
belirtmektedir.

4\. Yatırım planlaması: Bilindiği gibi yatırım seçenekleri risk, büyüme oranı,
geri dönüş hızı gibi faktörler açısından birbirlerinden farklıdır. Yatırım
yapmak isteyen kişi veya kuruluşların bu faktörleri dikkate alması gerekir.
Doğrusal programlama hangi yatırım seçeneklerine hangi miktarlarda yatırım
yapılırsa yatırım planının riski en düşük veya getirisi en büyük olur gibi
soruların yanıtlanmasında yaygın biçimde kullanılır.

**Örnek 2.3**: Bir yatırımcının yatırım yapabileceği dört yatırım seçeneği ve
80000 TL birikimi vardır. Yatırım seçenekleri ve bunların getiri oranları
(yıllık yüzde olarak) Tablo 2.1’de verilmiştir. Yatırımlarla ilgili gelirlerin
gerçekleşmesi için gereken ortalama yatırım süreleri (yıl) aynı tablonun son
sütununda gösterilmiştir. Yatırımcı karşılaşabileceği risklere önlem olarak
yatırımların risk katsayılarını araştırmış ve bunları Tablo 2.1’deki gibi
belirlemiştir.

**Tablo 2.1**

| Yatırım Seçeneği | Getiri Oranı (%) | Risk Katsayısı | Yatırım Süresi  |
|------------------|------------------|----------------|-----------------|
| Hisse Senedi     | 80               | 8              | 3               |
| Banka Mevduatı   | 50               | 5              | 1               |
| Altın            | 30               | 2              | 5               |
| Tahvil           | 60               | 3              | 5               |

Yatırımcı aşağıdaki kısıtları sağlayacak en yüksek getirili yatırım planını
araştırmaktadır. Problemi doğrusal programlama olarak modelleyiniz.

1.  Hisse senedi yatırımı toplam yatırımın en az %20’si kadar olmalıdır.

2.  Altına yapılan yatırım, tahvile ayrılan paranın %10’undan fazla olmamalıdır.

3.  Yatırım planının ortalama riski 5’den fazla olmamalıdır.

4.  Toplam yatırım süresi en fazla 6 yıl olmalıdır.

**Çözüm 2.3**: Her bir yatırım seçeneğine yapılacak yatırım miktarı belirlenmek
istendiğine göre karar değişkenleri aşağıdaki gibi tanımlanabilir.

x1: Hisse senedine ayrılan para miktarı

x2: Banka mevduatı için ayrılan para miktarı

x3: Altına yapılan yatırım miktarı

x4: Tahvil için ayrılan para miktarı

Yatırımcının amacı toplam getirinin en büyük olmasını sağlamak olduğuna göre,
amaç fonksiyonu aşağıdaki gibi olur.

Zenb = 0.80x1 + 0.50x2 + 0.30x3 + 0.60x4

Çeşitli yatırım seçeneklerine ayrılan paralar toplamının eldeki para miktarına
eşit olması gerektiği aşağıdaki gibi formüllenir.

x1 + x2 + x3 + x4 = 80000

1.  Hisse senedi yatırım miktarının x1, toplam yatırım miktarının 80000 TL
    olduğu düşünüldüğünde, hisse senedi yatırım miktarına ilişkin kısıt
    aşağıdaki gibi formüllenir.

x1 0.20(80000) veya x1 16000

1.  Altına yapılan yatırımın tahvile ayrılan paranın %10’undan fazla olmaması
    istenmektedir. Buna göre altın için ayrılan paranın x3, tahvile ayrılan
    paranın x4 olduğu dikkate alındığında, x3 0.10x4 yazılır.

    Kısıtlayıcının sağ tarafında bir sabit olacak şekilde yazılması
    gerektiğinden,

x3 - 0.10x4 0

olur.

1.  Ortalama riskin 5’den fazla olmaması kısıtı aşağıda açıklanmıştır.

8x1 + 5x2 + 2x3 + 3x4 5

1.  Toplam yatırım süresi ile ilgili sınırlama aşağıdaki gibi formüle edilir.

3x1 + 1x2 + 5x3 + 5x4 6

Negatif yatırım söz konusu olamayacağına göre, x1, x2, x3, x4 0 yazılmasıyla
model tamamlanmış olur.

Doğrusal programlamanın uygulama alanlarından olan görev dağıtımının
planlanması, kuruluş yerinin seçimi, en kısa yolun veya en yüksek akışı
sağlayacak rotanın belirlenmesi ve oyun problemleri özel ön bilgi
gerektirdiklerinden şimdilik bu tür problemlerin doğrusal programlama
modellerinin kurulması üzerinde durulmayacaktır.
