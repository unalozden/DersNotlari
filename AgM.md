*DÖRDÜNCÜ BÖLÜM*

## AĞ MODELLERİ

4.1. GİRİŞ

En iyileme problemlerinin önemli bir bölümünün çözümünde grafik veya ağların
kullanıldığı yöntemler tercih edilmektedir. Bunun başlıca nedeni, çözüm için
kurulan ağ modellerin göze hitap etmesi, böylece sorunun anlaşılması ve çözümün
diğer analitik çözüm yöntemleriyle karşılaştırıldığında daha kolay ve çabuk
olmasıdır. Bu yüzden, ağ modelleri ile çözüm tekniği veya kısaca ağ analizinin
kullanımı giderek yaygınlaşmaktadır. Bu bölümde, her biri kendine has çözüm
yöntemine sahip dört özel grup problem üzerinde durulacaktır. Bunlar sırasıyla;
"en kısa yol problemleri","en yüksek akış problemleri", "en küçük yayılmalı ağaç
problemleri" ile "proje çizelgeleme problemleri" dir.

4.2. TEMEL KAVRAM VE TANIMLAR

Ağ modelleri ile çözüm tekniklerine geçmeden önce konuyla ilgili bazı önemli
kavramları tanımlayalım.

*Grafik*: Grafik kuramı terminolojisine göre, belirli sayıda nokta ve bu
noktaları birbirine birleştiren çizgi ve/veya eğrilerden oluşan kümeye grafik
denir.

*Düğüm*: Grafikte bulunan noktaların her birine düğüm denir.

Düğümler, içlerine kendilerini tanımlayan sembollerin (harf veya rakam)
yazıldığı küçük dairelerle gösterilirler.

*Dal*: Herhangi iki düğümü birbirine birleştiren çizgi veya eğriye dal denir.

Bir dal okla gösterildiğinde yönlendirilmiş olur. Okla birleştirilen iki düğüm i
ve j olmak üzere, bunları birleştiren dal (i, j) ile gösterilir. Bu sembolde i,
(i, j) dalının başlangıç j ise bitiş düğümüdür. Böyle bir dal üzerinde bir akış
söz konusuysa, akışın yönü i’den j’ye olmak üzere tektir. Yönlendirilmemiş bir
(i, j) dalı, biri (i, j) diğeri (j, i) olmak üzere yönlendirilmiş iki dal yerine
geçer. Böyle bir dal üzerinde akış hem i’den j’ye hem de j’den i’ye doğru olmak
üzere çift yönlüdür. Yönlendirilmiş bir dal ileriye veya geriye doğrudur.
Başlangıç düğümü i olan, yani i düğümünü terkeden bütün dallar i düğümüne göre
ileriye doğrudur. Benzer şekilde, bitiş düğümü i olan, yani i düğümüne giren
bütün dallar i düğümüne göre geriye doğrudur. Kısaca, bir düğüm için ileriye
doğru olan bir dal başka bir düğüm için geriye doğru olabilir.

*Ağ*: Grafiğin dalları üzerinde bir akış olması durumunda grafik, akış ağı veya
kısaca ağ (serim, network, şebeke) ismini alır.

Yukarıda açıklandığı gibi ağ, düğüm ve dallardan oluşan bir sistemdir. Her ağın
mutlaka bir başlangıç bir de bitiş düğümü bulunmalı, gerekirse bu düğümler yapay
olarak yaratılmalıdır. Bir ağın bir tek başlangıç ile bir tek bitiş düğümünün
bulunmasının sağladığı yararlar ileride açıklanacaktır. Basit bir ağ örneği
Şekil 4.1’de gösterilmiştir.

# Şekil 4.1

Şekilden görüldüğü gibi ağ, sayılarla gösterilen 5 düğümden oluşmuştur. Ağı
oluşturan dallar; (1, 2), (1, 4), (2, 3), (3, 4), (2, 5), (3, 5), (4, 5) ve (5,
3) olmak üzere sekiz tanedir. Açıklamalarımız için dallardan birini, sözgelimi
(1, 2) dalını ele alalım. Başlangıç düğümü 1, bitiş düğümü 2 ile gösterilen bu
dal üzerinde akışın 1’den 2’ye doğru olmak üzere tek yönlü olduğu görülebilir.
Akışın iki yönlü olduğu tek bir dal (3 ve 5 nolu düğümler arasında) vardır.
İleriye ve geriye doğru dallara örnek olmak üzere 4 nolu düğümü ele alalım.
Şekil 4.1’den görüldüğü gibi (1, 4) dalı 4 nolu düğüme göre geriye doğru iken,
(4, 5) dalı aynı düğüm için ileriye doğrudur. Diğer taraftan (3, 4) dalı 3 nolu
düğüme göre ileriye, 4 nolu düğüme göre geriye doğrudur. Bir dalın incelenen bir
düğüme göre ileriye veya geriye doğru olduğunun belirlenmesi özellikle en yüksek
akış problemlerinde çok önemlidir. Ağ analizinde, dalların oluşturdukları özel
grupların önemi büyüktür. Bu özel gruplardan bazıları aşağıda tanımlanmıştır.

*Yol*: Başlangıç düğümü, kendisinden önce gelen dalın bitiş düğümü ile aynı olan
dallar dizisine yol denir.

Şekil 4.1’deki ağın 1 ve 5 nolu düğümlerini birbirine bağlayan bir yol, Şekil
4.2’de gösterildiği gibi olabilir.

**Şekil 4.2**

Şekil 4.3’de gösterildiği gibi (1, 2), (2, 3), (3, 4), (4, 5) dalları da bir yol
oluşturmaktadır.

**Şekil 4.3**

Başlangıç ve bitiş düğümleri aynı olmak üzere aynı ağ için daha başka yollar
tanımlanabileceği açıktır. (1, 2), (2, 5) veya (1, 4), (4, 5) dizileri gibi.
Kısaca ağ aynı olmak koşuluyla başlangıç ve bitiş düğümleri veya herhangi iki
düğüm arasında bağlantı sağlayan birden fazla yol tanımlanabilir.

*Zincir*: Kendisinden önce gelen dalla tek bir ortak noktası olan dallar
dizisine zincir denir.

Şekil 4.4’deki (1, 2), (2, 3), (5, 3) dallar dizisi bir zincirdir. (1, 4), (3,
4), (4, 5) dallar dizisinin de bir zincir olduğu görülebilir. Daha farklı
zincirler tanımlanabileceği unutulmamalıdır.

**Şekil 4.4**

*Çevrim*: Başlangıç düğümü ile bitiş düğümü aynı olan yola çevrim denir.

(3, 5), (5, 3) dal ikilisi ile tanımlanan çevrim aşağıda gösterilmiştir.

**Şekil 4.5**

Yeri geldiğinde açıklanacak bazı kavram ve kuralların bulunduğunu belirttikten
sonra en yüksek akış problemlerine geçebiliriz.

4.3. EN YÜKSEK AKIŞ PROBLEMLERİ

Bu bölümde, belirli bir zaman aralığında birbirlerine doğrudan değil ara
noktalarla bağlı olan iki nokta arasında taşınan malzeme veya akış miktarının en
büyüklenmesi problemi üzerinde durulacaktır.

Herhangi iki nokta arasında en yüksek trafik akışını sağlayacak trafik planının
programlanması, bir enerji kaynağından aydınlatma noktalarına en yüksek enerji
aktarımının sağlanması vb. işletme problemleri en yüksek akış problemleridir.

İlk bakışta ulaştırma problemi gibi görünen bu tip problemlerin ulaştırma
problemlerinden en önemli farkı, kaynak (başlangıç) ile varış (bitiş) arasındaki
bağlantının doğrudan değil ara noktalar aracılığı ile sağlanmasıdır.
Hatırlanacağı gibi, ulaştırma problemlerinde sunum ile istem merkezleri
arasındaki taşıma işlemi tek bir seferde yapılırken, akış problemlerinde bu
işlem ara noktalar aracılığı ile adım adım gerçekleştirilir. Herhangi bir
malzeme bir ara noktaya geldiğinde hemen diğer bir ara noktaya gider. Bu yönüyle
en yüksek akış problemleri aktarmalı ulaştırma problemlerine benzer. Diğer
taraftan, ulaştırma problemlerinde sunum merkezlerinin her biri bir kaynak ve
istem merkezlerinin her biri bir varış noktası iken, en yüksek akış
problemlerinde bu merkezlerin sayıları bire eşittir.

Şekil 4.6’daki akış ağı, ürünün k ile gösterilen kaynaktan v ile gösterilen
bitişe hangi dallar üzerinden gönderilebileceğini, daha doğru bir ifadeyle
akışın tönünü göstermektedir.

Ara noktalar 1, 2, 3 ile işaretlenmişlerdir. Kaynak ve bitiş dahil ağdaki beş
düğüm birbirlerine (k, 1), (k, 2), (k, 3), (1, 2), (1, v), (2, v), (3, 2) ve (3,
v) olmak üzere 8 dalla bağlıdır.

Yanıtlanmak istenen k’dan v’ye gönderilmek istenen malzemenin, hangi dallar
üzerinden hangi miktarlarda taşınması durumunda, v’ye aktarılan kısmın en büyük
olacağıdır.

**Şekil 4.6**

En yüksek akış problemlerinin çözümünde kullanılan tekniklere geçmeden önce
konuyla ilgili bazı sembolleri açıklayalım.

Her dalın kij ile gösterilen belirli bir taşıma kapasitesi vardır. (i, j) dalı
üzerinden taşınabilecek en yüksek miktarı ifade eden kij aynı zamanda, akışın
i’den j’ye doğru gerçekleştiğini göstermektedir.

Taşınan miktarın en büyük olmasının amaçlandığı bu tip problemlerde, en yüksek
akış miktarı f ile gösterilir.

Diğer taraftan, kapasitesi kij ile gösterilen (i, j) dalı üzerinden taşınan
miktar fij ile açıklanır. Bu sembol de kij’ye benzer şekilde akışın i’den j’ye
doğru olduğunu göstermektedir.

En yüksek akış problemleri doğrusal programlama problemi olarak da formüle
edilip çözülebilir. Bunun için öncelikle ağı oluşturan dalların taşıma
kapasitelerinin belirlenmesi gerekir.

Böyle bir modeli kurmak için Şekil 4.6’daki ağı, fij’ler ile kij’leri ait
oldukları dallar üzerinde göstererek tekrar çizelim.

Açıklamalar doğrultusunda çizilen ağ Şekil 4.7’de gösterilmiştir.

Şeklin ortaya koyduğu gibi ürün akışı kaynaktan 1, 2 ve 3 nolu düğümlere
doğrudur. Buna göre,

fk1 + fk2 + fk3 = f

yazılabilir.

Kaynaktan varışa olan akışlar toplamının kaynaktaki akış miktarına eşitliğini
gösteren bu denkleme "denge denklemi" denir. Kaynak dikkate alınarak yazılan bu
denklem akışın kaynaktaki korunumunu gösterir.

**Şekil 4.7**

Akışın korunumu yalnızca kaynakta değil, diğer bütün düğümlerde sağlanmalıdır.
1, 2 ve 3 nolu ara noktalardaki akışın korunumunu gösteren denge denklemleri
aşağıdaki gibi yazılabilir.

f12 + f1v = fk1

f12 + fk2 + f32 = f2v

f32 + f3v = fk3

Bitişe ulaşan akışın, ara noktalardan bu noktaya olan akışların toplamına
eşitliğini göstermek üzere, "f1v + f2v + f3v = f " yazılmasıyla denge
denklemlerinin belirlediği kısıtlayıcılar tamamlanır. Bir dal üzerindeki akışın
miktarı o dalın kapasitesi ile sınırlıdır ve negatif olamaz. Buna göre negatif
olmama koşulu bütün (i, j)’ler için 0 fij kij olarak yazılır.

Amaç fonksiyonunun Zenb = f şeklinde formüllenmesiyle, yukarıdaki ağın doğrusal
programlama modeli aşağıdaki gibi formüle edilmiş olur.

Zenb = f "Amaç fonksiyonu "

fk1 + fk2 + fk3 = f

Kısıtlayıcılar

f12 + fk2 + f32 = f2v

f32 + f3v = fk3

f1v + f2v + f3v = f

Negatif olmama

koşulu

0 f32 k32, 0 f1v k1v, 0 f2v k2v, 0 f3v k3v

Doğrusal programlama formülasyonunun tamamlanmasından sonra, simpleks yöntem
uygulamasına geçilebilir. Ancak, konu en yüksek akışın belirlenmesi olduğunda,
simpleks yöntemden çok daha etkin çözüm teknikleri vardır. Bunlardan en yaygın
biçimde kullanılanı "en yüksek akış algoritması" dır. Algoritmanın
açıklanmasından önce konuyla ilgili bazı önemli kavramlar üzerinde duralım.
Kaynak ve bitiş dahil ağdaki düğümlerin oluşturduğu küme N olsun. Bu kümeyi,
birinde kaynak diğerinde bitiş düğümünün bulunduğu iki alt kümeye ayıran
bölüştürmeye "kesme" denir. Kaynağı kapsayan alt küme S, bitişi kapsayan alt
küme S0 ile gösterildiğinde kesme (S, S0) olur. Sözgelimi Şekil 4.8’deki
kesmede; S = {k, 1, 2, 3}, S0 = {v} dir.

Şekil 4.8

S S0 = N = {k, 1, 2, 3, v}, S S0 = { }, k S ve v S0 olduğu unutulmamalıdır. k ve
v’yi ayıran diğer bir kesme Şekil 4.9’daki gibi olabilir.

Şekil 4.9

Şekil 4.9’daki kesme için S = {k, 1}, S0 = {2, 3, v} olduğu görülebilir. Aynı ağ
için bir başka kesme; S = {k, 1, 2} ve S0 = {3, v} olmak üzere Şekil 4.10’da
gösterilmiştir. Başka kesmeler de sözgelimi, S = {k}, S0 = {1, 2, 3, v}
tanımlanabileceği unutulmamalıdır.

Şekil 4.10

Her kesmenin K(S, S0) ile gösterilen bir kapasitesi vardır. Bu kapasite, S’deki
düğümleri S0’daki düğümlere doğrudan bağlayan dalların kapasiteleri toplamına
eşittir. Buna göre Şekil 4.8’deki kesmenin kapasitesi k1v + k2v + k3v, Şekil
4.9’dakinin k12 + k1v + kk2 + kk3, Şekil 4.10’daki kesmenin kapasitesi ise k1v +
k2v + kk3 toplamına eşittir. ((3, 2) dalı üzerindeki akış S’den S0’a doğru değil
S0’dan S’ye doğru olduğundan k32 dikkate alınmamıştır.)

Kapasitesi en küçük olan kesmeye "en küçük kesme" denir. Kesme ile ilgili
şekillerden görüleceği gibi, herhangi bir kesmeyi oluşturan dallar ağ dışı
bırakıldıklarında kaynakla bitişi birbirlerine bağlayan bir yol bulunamaz. Bu
durumda uygun bir akış planı belirleme çabaları sonuçsuz kalır. Kısaca kaynak
ile bitiş arasındaki akış kesmedeki dallar üzerinden olur. Buna göre, toplam
akış miktarı f’nin kesmenin kapasitesi ile sınırlı olduğu söylenebilir. Akış ve
kesme arasındaki bu ilişki aşağıda özetlenmiştir.

Yönlendirilmiş bir ağda bitişe aktarılan ürün miktarı f, (S, S0) de kesme ise
f’nin değeri kesmenin kapasitesine eşit veya küçüktür. Bu durum bütün kesmeler
için geçerlidir. Yani, kaynaktan bitişe doğru gerçekleşen bir akışın kabul
edilebilir olması için akış miktarının herhangi bir kesmenin kapasitesini
aşmaması gerekir. Buna göre, en yüksek akış miktarının en küçük kesmenin
kapasitesi ile sınırlı olduğu söylenebilir.

Aşağıdaki önemli teorem herhangi bir ağda k’dan v’ye en küçük kesmenin
kapasitesine eşit uygun bir akış bulunabileceğini belirtmektedir.

*En Yüksek Akış En Küçük Kesme Teoremi*: Herhangi bir ağdaki en yüksek akış
miktarı en küçük kesmenin kapasitesine eşittir. Bu teoremle bağlantılı olarak
bütün kesmelerin ve bunlara ilişkin kapasitelerin listelenmesiyle en küçük
kapasiteli kesme ve buna bağlı olarak en yüksek akış miktarı belirlenebilir.
Ancak bu yolla yalnızca en yüksek akış miktarı belirlenebilmekte, akışın hangi
dallar üzerinden hangi miktarlarda gerçekleştiği sorusu yanıtlanamamaktadır. Bu
soru, geçerliliği bu teoreme dayanan, en yüksek akış algoritması ile
yanıtlanabilir. Söz konusu algoritma aşağıda açıklanmıştır.

**En Yüksek Akış Algoritması**: En yüksek akış algoritmasının esası, kaynaktan
bitişe pozitif akışın söz konusu olduğu bir yol bulmaktır. Böyle bir yol "akış
artırıcı yol" olarak isimlendirilir. Bu yol tüm ağda en yüksek akışı sağlamak
amacıyla kullanılır. Akış artırıcı yol bulma çabalarının sonuçsuz kalması
durumunda en yüksek akış bulunmuş olur. Akış artırıcı bir yol bulunabilmesi için
aşağıda açıklanan rota etiketleme işleminin uygulanması gerekir.

*Rota Etiketleme İşlemi*: Kaynaktan bitişe akış artırıcı yol bulmada kullanılan
etiketleme işlemi kaynağın etiketlenmesiyle başlar. k’dan j’ye pozitif akış söz
konusu ise j düğümü etiketlenir.

Genel olarak, aşağıdaki koşullardan birinin sağlanması durumunda j etiketlenir.

1.  i ve j düğümlerini birleştiren dal ileri doğrudur ve (i, j) üzerindeki akış
    miktarı dalın akış kapasitesinden küçüktür (fij \< kij).

2.  i ve j düğümlerini birleştiren dal (j, i) geriye doğrudur ve (j, i)
    üzerindeki akış miktarı sıfırdan büyüktür (fji \> 0).

Etiketleme işlemi bitiş noktası etiketleninceye değin sürdürülür. Bitiş
etiketlendiğinde akışı artırıcı bir yol belirlenmiş olur.

En yüksek akış algoritması, kapasite kısıtları ile birlikte düğümlerdeki akışın
korunumunu da sağlayan uygun bir akışla başlar. Başlangıç akış planı (doğrusal
programlamanın başlangıç çözümüne benzer) olarak isimlendirilen bu plan, akış
miktarının 0 olduğu duruma karşılık gelir. Bu akışın geliştirilebilmesi için
öncelikle kaynak (başlangıç düğümü) etiketlenir. Etiketlenen düğüm \* ile
işaretlenir. Kaynağın etiketlenmesinden sonra yukarıda açıklanan rota etiketleme
işlemiyle başka bir düğüm etiketlenir. Bitiş etiketlendiğinde pozitif akışın söz
konusu olduğu akış artırıcı bir yol belirlenmiş olur. Belirlenen bu yol
üzerindeki düğümlerin etiketleri yardımıyla yol üzerinden aktarılacak en yüksek
akış (d) hesaplanır. d’nin hesaplanmasından sonra yolun ileri dallarındaki
akışlar d kadar artırılırken, geriye doğru dallardaki akışlar d kadar azaltılır.
Bu işlemler yeni akış artırıcı yolların bulunması için tekrarlanır. Akış
artırıcı yeni yol belirleme çabaları sonuçsuz kaldığında en yüksek akış planı
belirlenmiş olur.

Açıklamaları bir örnek probleme uygulayalım.

**Örnek 4.1**: Dallarının akış kapasiteleri (fij) oklar üzerinde gösterildiği
gibi olan ağda k’dan v’ye taşınacak en yüksek ürün miktarını ve taşıma planını
belirleyiniz. Problemin akış ağı Şekil 4.11’de gösterilmiştir.

Şekil 4.11

**Çözüm 4.1**: Problemin çözümüne herhangi bir akışın olmadığı durumla
başlayalım. Başlangıç akış planını yansıtan bu durum için aşağıdaki gibi bir
eşitlik yazılabilir.

fk1 = fk2 = fk3 = f12 = f32 = f1v = f2v = f3v = 0

Bu durum orijinal ağ üzerinde aşağıdaki gibi gösterilir. (i, j) dalları
üzerindeki sayılar (fij, kij)’leri göstermektedir.

Şekil 4.12

Birinci Adım: Kaynaktan bitişe akış artırıcı bir yol bulmak için önce başlangıç
düğümü etiketlenir. k’nın etiketlenmesinden sonra 1, 2 veya 3 nolu düğüme
geçilebilir. 1 nolu düğümü seçmiş olalım. (k, 1) dalındaki akış miktarı (0) bu

dalın kapasitesinden az olduğundan, 1 etiketlenir. Buradan 2’ye veya v’ye
geçilebilir. 2’ye geçilmiş olsun. (1, 2) dalı üzerinden 2, (2, v) dalı üzerinden
de v etiketlenerek yalnızca ileriye doğru dalların bulunduğu (k, 1), (1, 2), (2,
v) dallarından oluşan akış arttıcı yol aşağıdaki gibi belirlenmiş olur.

Şekil 4.13

Dallar üzerindeki sayılar, dalların taşıma kapasitelerinin sınırlarını
göstermektedir. Şekil 4.13 ile açıklanan yol üzerindeki en yüksek akış miktarı,
(1, 2)’nin taşıma kapasitesi ile sınırlı olup 5(= enk(20, 5, 15)) birimdir. Bu
durum, anılan yolu oluşturan ileriye doğru dallar üzerindeki akışları 5’er birim
artırır. Sonuçta, halihazırda sıfır birim olan akış miktarı 5 birim artarak; f =
0 + 5 = 5 olur. 5 birim olarak belirlenen miktarın göz önünde bulundurulmasıyla
çizilen düzenlenmiş akış değerli ağ, Şekil 4.14’de gösterilmiştir.

Şekil 4.14

Çözümün izleyen adımlarında (k, 1)’in kapasite sınırının 20 değil 15(= 20 - 5),
(1, 2) dalının taşıma kapasitesinin 5 değil sıfır(= 5 - 5), (2, v) dalının
taşıma kapasitesinin ise 15 değil 10(= 15 - 5) birim olduğu düşünülecektir.
Belirlenen her yeni akış artırıcı yolun ardından bu düzenlemenin yapılması ihmal
edilmemelidir.

İkinci adım: Kaynaktan başlayarak akış arttırıcı yeni bir yol bulmaya çalışalım.
(k, 1) dalı üzerinden taşınan miktar (5 ) ilgili dalın kapasitesinden (20) küçük
olduğundan, 1 nolu düğüm k’dan, aynı gerekçeyle v’de 1’den etiketlenir. Böylece
(k, 1) ve (1, v) dallarından oluşan akış artırıcı yol Şekil 4.15’deki gibi
belirlenmiş olur.

Şekil 4.15

# Görüldüğü gibi; (k, 1), (1, v) yolu üzerindeki en yüksek akış 15(= enk(15, 27)) birimdir. Bu yüklemeyle varışa 15 birim daha gönderilerek, f = 5 + 15 = 20’ye çıkarılmış olur. Yeni duruma göre düzenlenen ağ aşağıda gösterilmiştir.

Şekil 4.16

Üçüncü adım: (k, 1)’deki akış (= 5 + 15) bu dalın kapasitesine eşit olduğundan,
etiketleme için 2 veya 3 nolu düğüme geçilir. Önce 2 nolu düğümü inceleyelim.
(k, 2) dalındaki akış bu dalın kapasitesinden küçük olduğundan 2 nolu düğüm
etiketlenir. Aynı gerekçeyle v, 2’den etiketlenir. Bu yolla belirlenen akış
artırıcı yol aşağıda gösterilmiştir.

**Şekil 4.17**

(k, 2) ve (2, v)’den oluşan yol üzerindeki mümkün akış miktarları incelendiğinde
bu yol üzerindeki en yüksek akış miktarının 10(= enk(30, 10)) birim olduğu
görülecektir. İkinci adımda ağ üzerindeki akışın 20 birim olduğu göz önünde
bulundurulduğunda, f’nin yeni değeri 30 olarak belirlenir. Buna göre düzenlenmiş
akış değerli ağ aşağıda gösterilmiştir.

**Şekil 4.18**

Dördüncü adım: Üçüncü adımda açıklanan gerekçeyle etiketleme için 2 veya 3 nolu
düğüm seçilebilir. 2 nolu düğüm kaynaktan etiketlenebilirse de, (2, v) dalı
üzerindeki akış bu dalın taşıma kapasitesine eşit olduğundan, v etiketlenemez. 3
nolu düğüme geçelim. 3 nolu düğüm k’dan, v’de 3 nolu düğümden etiketlenebilir.
Bu yolla belirlenen akış artırıcı yol aşağıda gösterilmiştir.

Şekil 4.19

Şekil 4.19’daki yolu oluşturan dallardaki mümkün akış miktarları incelendiğinde
(k, 3), (3, v) yolundaki en yüksek akış miktarının 10(= enk(10, 19)) birimle
sınırlı olduğu görülebilir. Bir önceki adımdaki ağ üzerindeki akış miktarının 30
olduğu göz önünde bulundurulduğunda, f’nin yeni değeri 40(= 30 + 10) olarak
belirlenecektir.

Bu belirlemelerin ardından düzenlenen akışı geliştirilmiş ağ Şekil 4.20’de
gösterilmiştir. Şeklin çizilmesinden sonra yeni adıma (beşinci adım)
geçilebilir.

Beşinci adım: (k, 1) ve (k, 3) dallarındaki akış miktarları bu dalların
kapasitelerine eşit olduğundan etiketleme için tek seçenek 2 nolu düğümdür.

**Şekil 4.20**

Şekilden de görüleceği gibi, 2 nolu düğüm k’dan etiketlenir. (1, 2) dalı 2 nolu
düğüme göre geriye doğru olup dal üzerindeki akış miktarı dalın taşıma
kapasitesine eşittir. Bu nedenle 1 nolu düğüm, 2’den etiketlenir. (1, v)
dalındaki akış bu dalın taşıma kapasitesinden küçük olduğundan v’de 1’den
etiketlenir. Bu yol aşağıda gösterilmiştir.

Şekil 4.21

Şekil 4.21’deki yolu oluşturan dalların yönü ve üzerilerindeki akış
miktarlarının dikkate alınmasıyla düzenlenen gelişmiş akışlı ağ aşağıda
gösterilmiştir.

Şekil 4.22’deki gelişmiş akışlı ağ incelendiğinde; (k, 1) ve (k, 3) üzerindeki
akışların ilgili dalların kapasitelerine eşit olduğu görülebilir. Bu durum 1 ve
3 nolu düğümlerin etiketlenemeyeceğini gösterir. 2 nolu düğüm k’dan
etiketlenebilirse de varış 2’den etiketlenemez. Kısaca yeni bir akış artırıcı
yol belirleme çabaları sonuçsuz kaldığından en yüksek akışın gerçekleştiği yol
bulunmuş olur. Bu yol üzerinden gönderilecek en yüksek miktar 45 birimdir. Bu
miktarın (45 birim) en yüksek akış miktarı olduğunun onaylanabilmesi (en yüksek
akış en küçük kesme teoremi) amacıyla son aşamada etiketlenmiş tüm düğümlere
S’de, etiketlenmemiş düğümlere S0’da yer vererek (S, S0) kesmesini tanımlayalım.
Söz konusu kesme de Şekil 4.22’de gösterilmiştir.

Şekil 4.22

Şekilden görüldüğü gibi, S = (k, 2), S0 = (1, 3, v) ve K(S, S0) = 45 olur.
İkilem gereği, f herhangi bir kesmenin kapasitesini aşamayacağından, f = 45’in
en yüksek akış miktarı ve en küçük kesmenin de Şekil 4.22’deki olduğu
belirlenmiş olur.

*Yönlendirilmemiş Dalların Olması Durumu*: En yüksek akış algoritması için ağın
yönlendirilmiş olması gerekmekle birlikte, ağın yönlendirilmemiş olması en
yüksek akışın belirlenmesini engellemez. Söz konusu algoritmanın
yönlendirilmemiş bir ya da birkaç dalın bulunduğu ağlarda uygulanabilmesi için
öncelikle yönlendirilmemiş dalların bulunduğu orijinal ağın yönlendirilmesi,
daha sonra en yüksek akış algoritmasının orijinaline eşdeğer olan bu ağa
uygulanmasına geçilir. i ve j düğümlerini birleştiren K kapasiteli
yönlendirilmemiş bir dal aşağıdaki gibi yorumlanabilir.

fij K

fji K

(fij) (fji) = 0

Yukarıdaki eşitsizlikler (i, j) üzerinden en yüksek K birimlik akışın hem i’den
j’ye hem de j’den i’ye doğru olabileceğini göstermektedir. (fij)(fji) = 0
eşitliğiyle akışın tek yönde olması sağlanmaktadır.

Bir örnek problem ile bu durumu açıklayalım.

**Örnek 4.2**: Aşağıdaki gibi bir yol ağını ele alalım. Dallar üzerindeki
sayılar trafik akış kapasitelerini göstermektedir. Problem, en yüksek trafik
akışını sağlayabilmek için henüz yönlendirilmemiş dallar üzerine tek yön
işaretinin hangi istikamette konulacağının belirlenmesidir.

**Şekil 4.23**

**Çözüm 4.2**: Öncelikle yönlendirilmemiş her bir dalın ters yönlü ve eşit
kapasiteli iki dalla değiştirilmesi gerekir. Bu düzenlemeyle, Şekil 4.24’de
gösterilen yönlendirilmiş ağ elde edilir.

**Şekil 4.24**

En yüksek akış algoritmasının, orijinaline eşdeğer olan bu ağ üzerinde
uygulanmasıyla, k’dan v’ye en yüksek akış miktarı ve en yüksek akışı sağlayan
rota belirlenir.

En iyi çözümün bulunmasından sonra her iki yönde akışın söz konusu olduğu dallar
belirlenir ve aşağıdaki inceleme gerçekleştirilir.

i ve j düğümlerini birleştiren yönlendirilmemiş bir dal üzerinde,

fij \> fji ise, (i, j) dalındaki akış (fij - fji ) olur, yani yönlendirilmemiş
(i, j) dalı i’den j’ye doğru yönlendirilir.

fji \> fij ise, (j, i) dalındaki akış (fji - fij ) olur, yani yönlendirilmemiş
(i, j) dalı j’den i’ye doğru yönlendirilir.

Şekil 4.24’deki ağa en yüksek akış algoritması uygulanmasıyla ulaşılan sonuç
Şekil 4.25’de gösterilmiştir.

Şekil 4.25

*Çok Kaynak-Çok Bitiş Olması*: Ağ üzerinde birden fazla kaynak ve/veya birden
fazla bitiş noktası bulunduğunu düşünelim. Bu durumda en yüksek akışın
belirlenebilmesi için hayali bir kaynak ile hayali bir bitiş noktasının
yaratılması zorunludur. Yaratılan hayali kaynak gerçek kaynaklara, gerçek bitiş
noktaları hayali bitiş noktasına birer dalla bağlanır. Ağa eklenen hayali
dalların tümü ileriye doğrudur. Hayali dalların akış kapasitelerinin
belirlenmesinden sonra problem en yüksek akış problemine dönüşmüş olur.

Konuyu açıklamak için sunum miktarları s1 ve s4 olan iki kaynak ile istem
miktarları d5 ve d8 olan iki bitiş noktasının bulunduğu bir ulaştırma problemi
düşünelim.

Problemin orijinal ağı ve dalların taşıma kapasiteleri aşağıda gösterilmiştir.

**Şekil 4.26**

1 ve 4 nolu düğümler gerçek kaynak, 5 ve 8 nolu düğümler gerçek bitiş
noktalarıdır. Yukarıdaki açıklamalar doğrultusunda düzenlenen hayali kaynak ve
hayali bitiş noktalı ağ aşağıda gösterilmiştir.

Şekil 4.27

Görüldüğü gibi k’yı 1 nolu düğüme bağlayan dalın kapasitesi s1’e, 4 nolu düğüme
bağlayan dalın kapasitesi ise s4’e eşittir. Gerçek bitiş noktalarını hayali
bitiş noktasına bağlayan dalların taşıma kapasiteleri ise çıkış noktalarının
istem miktarlarıyla bağlantılı olarak sırasıyla d5 ve d8’dir.

Bu düzenlemenin ardından hayali kaynaktan bitiş noktasına en yüksek akışın
sağlanmasına geçilebilir. s1 = 40, s4 = 30, d5 = 35, d8 = 35 olarak verilmiş
olsun. Bu durumda en iyi çözüm Şekil 4.28’deki gibi elde edilecektir.

Şekil 4.28

## 4.4. EN KISA YOL PROBLEMLERİ

Başlangıç ve bitiş düğümleri arasındaki en kısa yolun belirlenmesi problemi, en
kısa yol problemi olarak bilinir. Ağ problemlerinin çoğu doğrusal programlama
problemi olarak değerlendirilerek simpleks yöntemle çözülebilir. Bu durum en
kısa yol problemleri için de geçerlidir. Bir en kısa yol problemini doğrusal
programlama olarak inceleyebilmek için dallar üzerindeki akışların 1 birime,
i’den j ’ye malzeme taşıma maliyetinin ise (i, j) dalının uzunluğuna eşit olduğu
düşünülür. En kısa yol problemleri matematik bir modelle formüle edilmeksizin de
çözülebilir. Bunun için başlangıç ve bitiş düğümlerini birbirine bağlayan
alternatif yolların dökümünün yapılması ve listelenen yollara ilişkin toplam
uzunluklarının belirlenmesi yeterlidir. Bu yaklaşım yalnızca küçük boyutlu
problemler için geçerlidir. Problemin boyutu büyüdükçe tüm yolların dökümünü
yapmak yorucu ve zaman alıcı olur. En kısa yol problemleri için geliştirilmiş
çok daha etkin yöntemler vardır. Bunlardan en yaygın biçimde kullanılan Dijkstra
algoritması aşağıda açıklanmıştır.

**Dijkstra Algoritması***:* Dijkstra Algoritması, n düğümlü ağ kapsamındaki tüm
dalların negatif olmayan ve bilinen uzunluklara (dij) sahip olduğu varsayımına
dayanır. dij,, (i, j) dalının uzunluğu, i’den j’ye gitmenin maliyeti veya (i, j)
dalını katetme zamanı olabilir. i ve j düğümleri birbirlerine doğrudan, yani tek
bir dalla bağlı değillerse dij = kabul edilir. dij dji olabilir. Ayrıca, bir
düğümün kendine uzaklığı sıfır olduğundan, dii = 0’dır. Bu varsayımlar altında,
düğümlerin önce geçici, sonra kalıcı olarak etiketlenmesi esasına dayanan
Dijkstra algoritması, en kısa yol belirleninceye kadar aşağıdaki adımların
tekrarlanmasını gerektirir.

Ön adım: Başlangıç düğümüne sıfır (d11 = 0) kalıcı etiketi verilir. Sıfır ile
kalıcı olarak etiketlenen başlangıç düğümü dışındaki bütün düğümlere, birer
geçici etiket verilir. Geçici etiketi hesaplanacak düğüm başlangıç düğümüne tek
bir dalla bağlı ise geçici etiketin değeri o dalın uzunluğuna, değilse +’a
eşittir. Herhangi bir geçici etiketinin değeri, ait olduğu düğümü başka düğüme
bağlayan en kısa yol için bir üst sınırdır. Geçici etiketlerin belirlenmesinden
sonra en küçük olan araştırılır. Araştırma sonucu belirlenen en küçük değer ait
olduğu düğümün kalıcı etiketi olur. En küçük değerli geçici etiket sayısı birden
çok ise seçim, düğümlerden yalnızca birinin seçilmesi kaydıyla, rasgele yapılır.
Kısaca, her seferinde yalnızca bir düğüm kalıcı olarak etiketlenir.

Birinci Adım: Kalıcı etiketi en yeni olan düğüm belirlenir. Bu düğüm K olsun. Ön
adımdaki başlangıç düğümüne karşılık gelen bu düğüme bağlı olarak tüm geçici
etiketlerin yeni değerleri aşağıdaki gibi hesaplanır.

Enk

İkinci adım: Birinci adımda hesaplanan geçici etiketlerden en küçük olanı ait
olduğu düğümün kalıcı etiketi olur ve \* ile işaretlenir. Önceden olduğu gibi,
en küçük değerli etiket birden fazla olduğunda düğüm seçimi, her seferinde
yalnızca bir düğüm olmak üzere, rasgele yapılır. Son düğüm kalıcı olarak
etiketlendiğinde en kısa yol belirlenmiş olur. Son düğümün kalıcı etiketinin
değeri en kısa yolun uzunluğuna eşittir.

En kısa yolu oluşturan dalların belirlenmesi için son düğümden başlanarak geriye
doğru hareket edilir ve düğümlerin kalıcı etiketleri arasındaki farklar
incelenir. Etiketler arasındaki fark iki düğüm arasındaki dalın uzunluğuna
eşitse ilgili dal en kısa yol üzerinde, aksi halde değildir.

En kısa yolu oluşturan dalların belirlenmesinde kullanılabilecek diğer bir
yaklaşım, en son düğümden geriye dönerek hangi düğümün hangi düğümden
etiketlendiğinin belirlenmesidir.

Dijkstra algoritmasını bir örnek problem üzerinde uygulayalım.

**Örnek 4.3**: İzmir’den Ankara’ya gitmek isteyen bir kişi gidebileceği yolları
araştırmış ve iki şehri birbirine bağlayan yolları ve bunların uzaklıklarını
Şekil 4.29’daki gibi belirlemiştir. Sürücünün amacı İzmir’den Ankara’ya en kısa
yoldan gitmektir. İki şehir arasındaki en kısa yolu bulunuz.

Şekil 4.29

**Çözüm 4.3**: Ön adım: Başlangıç düğümünün sıfırla kalıcı olarak
etiketlenmesinden sonra diğer düğümlerin etiketlenmesine geçilir.

Şekil 4.29’dan görüldüğü gibi başlangıç düğümüne doğrudan bağlı iki düğüm (2 ve
3) vardır. Bu düğümlerin başlangıç düğümüne uzaklıkları sırasıyla 5 ve 7
olduğundan bunların geçici etiketleri sırasıyla, 5 ve 7 olarak belirlenir. Bu
iki düğümün dışındaki düğümlerin hepsi başlangıç düğümüne dolaylı olarak bağlı
olduklarından etiketleri +’a eşittir. Bu yolla belirlenen etiket değerleri
aşağıda, ait oldukları düğüm numaraları altında gösterilmiştir.

| Düğüm No:   | 1   | 2 | 3 | 4 |  5 | 6 | 7 |
|-------------|-----|---|---|---|----|---|---|
| Etiket No : | 0\* | 5 | 7 |   |    |   | ] |

Geçici etiketlerden en küçük (5) olanı 2 nolu düğüme ait olduğundan, bu düğüm 5
ile kalıcı olarak etiketlenir. Böylece etiketler aşağıdaki gibi belirlenmiş ve
ön adım tamamlanmış olur.

| Düğüm No:   | 1   | 2   | 3 | 4 |  5 | 6 | 7 |
|-------------|-----|-----|---|---|----|---|---|
| Etiket No : | 0\* | 5\* | 7 |   |    |   |   |

Birinci adım: En yeni kalıcı etiket 2 nolu düğüme aittir. Bu düğüme doğrudan
bağlı olan 4 ve 5 nolu düğümlerin yeni geçici etiketlerinin hesaplanması
gerekir. Yeni etiket değerleri aşağıdaki gibi hesaplanmıştır.

Dördüncü düğümün geçici etiketi: Enk{, 5 + 3} = 8

Beşinci düğümün geçici etiketi : Enk{, 5 + 6} = 11

Hesaplanan değerlerin dikkate alınmasıyal düğüm etiketlerinin yeni değerleri
aşağıdaki gibi olur.

| Düğüm No:   | 1   | 2   | 3 | 4 |  5 | 6 | 7 |
|-------------|-----|-----|---|---|----|---|---|
| Etiket No : | 0\* | 5\* | 7 | 8 | 11 |   |   |

İkinci adım: Birinci adımda belirlenen geçici etiketlerden en küçük olanın 7
olduğu ve bunun üçüncü düğüme ait olduğu görülebilir. Buna göre üçüncü düğüm
etiketinin 7 olarak kalıcı kılınmasıyla düğüm etiketleri aşağıdaki gibi
belirlenmiş olacaktır.

| Düğüm No:   | 1   | 2   | 3   | 4 |  5 | 6 | 7 |
|-------------|-----|-----|-----|---|----|---|---|
| Etiket No : | 0\* | 5\* | 7\* | 8 | 11 |   |   |

Henüz tüm etiketler kalıcı olmadığından tekrar birinci adıma dönülür.

Birinci adım: Kalıcı etiketi en yeni olan üçüncü düğüme doğrudan bağlı 4 ve 5
nolu düğümlerin yeni geçici etiketleri,

Dördüncü düğümün geçici etiketi: Enk{ 8, 7 + 4} = 8

Beşinci düğümün geçici etiketi : Enk{11, 7 + 5} = 11

olarak hesaplanacak böylece düğüm etiketleri, aşağıdaki gibi belirlenecektir.

| Düğüm No:   | 1   | 2   | 3   | 4 |  5 | 6 | 7 |
|-------------|-----|-----|-----|---|----|---|---|
| Etiket No : | 0\* | 5\* | 7\* | 8 | 11 |   |   |

İkinci adım: Geçici etiketlerden en küçüğü dördüncü düğüme ait olduğundan,
anılan düğüm 8 ile kalıcı biçimde etiketlenir. Buna göre,

| Düğüm No:   | 1   | 2   | 3   | 4   |  5 | 6 | 7 |
|-------------|-----|-----|-----|-----|----|---|---|
| Etiket No : | 0\* | 5\* | 7\* | 8\* | 11 |   |   |

olur. Henüz tüm etiketler kalıcı olmadığından tekrar birinci adıma dönelim.

Birinci adım: En yeni kalıcı etiket 4 nolu düğüme aittir. Bu düğüme doğrudan
bağlı tek düğüm olan 6 nolu düğümün yeni geçici etiketinin hesaplanması gerekir.
Bu işlem aşağıda gösterilmiştir.

Altıncı düğümün geçici etiketi: Enk{, 8 + 2} = 10

Bu sonucun kullanılmasıyla belirlenen düğüm etiketleri aşağıda gösterilmiştir.

| Düğüm No:   | 1   | 2   | 3   | 4   |  5 |  6 | 7 |
|-------------|-----|-----|-----|-----|----|----|---|
| Etiket No : | 0\* | 5\* | 7\* | 8\* | 11 | 10 |   |

İkinci adım: Geçici etiketlerden en küçüğü altıncı düğüme ait olduğundan anılan
düğümün kalıcı etiketi 10 olur. Buna göre etiketler,

| Düğüm No:   | 1   | 2   | 3   | 4   |  5 |  6   | 7 |
|-------------|-----|-----|-----|-----|----|------|---|
| Etiket No : | 0\* | 5\* | 7\* | 8\* | 11 | 10\* |   |

olur. Etiketleme işlemi henüz tamamlanmadığından birinci adım tekrarlanır.

Birinci adım: Altıncı düğüme bağlı tek düğüm yedinci düğüm olduğundan anılan
düğümün geçici etiketi,

Yedinci düğümün geçici etiketi: Enk{, 10 + 2} = 12

olarak hesaplanır ve düğüm etiketleri aşağıdaki gibi belirlenmiş olur.

| Düğüm No:   | 1   | 2   | 3   | 4   |  5 |  6   |  7 |
|-------------|-----|-----|-----|-----|----|------|----|
| Etiket No : | 0\* | 5\* | 7\* | 8\* | 11 | 10\* | 12 |

İkinci adım: En küçük değerli (11) geçici etiket beşinci düğüme aittir. Bu
nedenle 11, beşinci düğümün kalıcı etiketi olur ve sonuçta düğüm etiketleri
aşağıdaki gibi belirlenmiş olur.

| Düğüm No:   | 1   | 2   | 3   | 4   |  5   |  6   |  7 |
|-------------|-----|-----|-----|-----|------|------|----|
| Etiket No : | 0\* | 5\* | 7\* | 8\* | 11\* | 10\* | 12 |

Bu noktada etiketi geçici olan bir düğüm bulunduğundan birinci adıma dönülür.

Birinci adım: Kalıcı etiketi en yeni olan beşinci düğüme doğrudan bağlı tek
düğüm olan yedinci düğümün geçici etiketinin yeni değeri,

Yedinci düğümün geçici etiketi: Enk{12, 11 + 4} = 12

olarak hesaplanmıştır.

Sonuçta etiketleme işlemi aşağıdaki gibi tamamlanmıştır.

| Düğüm No :  | 1   | 2   | 3   | 4   |  5   |  6   | 7    |
|-------------|-----|-----|-----|-----|------|------|------|
| Etiket No : | 0\* | 5\* | 7\* | 8\* | 11\* | 10\* | 12\* |

Etiketlerin hepsi kalıcı olduğundan en kısa yol bulunmuştur. Şimdi de toplam
uzunluğu 12 birim olan en kısa yol üzerindeki dalları belirleyelim. Bunun için
son düğümden başlayarak geriye doğru düğüm düğüm gidelim. 7 ve 6 nolu düğümlerin
kalıcı etiketleri arasındaki fark (2) anılan düğümleri birbirine birleştiren
dalın uzunluğuna eşit olduğundan (6, 7) dalı en kısa yol üzerindedir. 6 nolu
düğümden 5 nolu düğüme gidilemez. 6 ve 4 nolu düğümlerin kalıcı etiketleri
arasındaki fark (2), (4, 6)’nın uzunluğuna eşit olduğundan, bu dal en kısa yol
üzerindedir. (4, 3) dalının uzunluğu bu düğümlerin etiketleri arasındaki farka
eşit olmadığından, (4, 3) dalı en kısa yol üzerinde değildir. 4 ve 2 nolu
düğümlerin kalıcı etiketleri arasındaki fark (2, 4)’ün uzunluğuna eşit
olduğundan bu dal en kısa yol üzerindedir. Son olarak (2, 1)’in uzunluğu bu dalı
tanımlayan düğümlerin etiketleri arasındaki farka eşittir. Dolayısıyla bu dal en
kısa yol üzerindedir. Buna göre İzmir’den yola çıkan sürücü sırasıyla, 2, 4, 6
nolu düğümlere uğrayarak İzmir’den Ankara’ya en kısa yoldan ulaşmış olur.

En kısa yolu bir de hangi düğümün hangi düğümden etiketlendiğinin belirlenmesi
yaklaşımıyla bulalım. 7 nolu düğüm 6, 6 nolu düğüm 4, 4 nolu düğüm 2, 2 nolu
düğüm de 1 nolu düğümden etiketlendiklerinden sırasıyla, 1, 2, 4, 6 ve 7 nolu
düğümler en kısa yol üzerindedir.

Görünürde en kısa yol problemlerinden oldukça farklı olan pek çok işletme
problemi en kısa yol problemi olarak çözülebilir. Konunun daha iyi
anlaşılabilmesi bakımından farklı işletme problemlerine yer verilmesi uygun
olur.

**Araç Yenileme Problemi**: Gerek işletmelerin gerekse kişilerin kullandıkları
araçların çoğu ilerleyen yaşlarına bağlı olarak sürekli artan bakım-onarım
harcamalarına yol açarlar. Eskiyen araçların belirli aralıklarla yenilenmesi,
araçların her bir yenilenişinde katlanılması gereken yüksek satın alma
maliyetine rağmen toplam maliyeti düşürebilir. Yöneticilerin karşılaştığı en
önemli problemlerden birisi de satın alma ve bakım-onarım harcamalarından oluşan
toplam maliyeti en küçükleyecek araç yenileme politikasını belirlemektir. Bu
problem, en kısa yol problemi olarak formüle edilebilir.

Konuya örnek olması bakımından aşağıdaki problemi çözelim.

**Örnek 4.4**: Tek araca sahip bir işletme gelecek beş yıl için araç yenileme
planını geliştirmek istemektedir. Aracın yıllık bakım-onarım masrafı (TL),
aracın incelenen yılın başındaki yaşına bağlı olup aşağıdaki gibi tahmin
edilmiştir. Aracın yaşına bağlı olarak her yıl biraz daha artan bakım-onarım
masraflarından kurtulmak için eskiyen aracı satıp yerine yenisini almak da
mümkündür. Eskiyen aracın satış fiyatı (TL), satıldığı yıldaki yaşına bağlı olup
aşağıdaki tabloda gösterilmiştir.

Hesaplamalarda basitlik sağlamak için araç satın alma maliyetinin değişmediği ve
15 TL olduğu kabul edilmiştir. Buna göre 5 yıllık planlama dönemi için en iyi
araç yenileme programını oluşturunuz.

# Tablo 4.1

| Aracın Yaşı | Bakım Masrafı | Satış Fiyatı |
|-------------|---------------|--------------|
| 0           | 2             | -            |
| 1           | 3             | 10           |
| 2           | 5             | 9            |
| 3           | 8             | 5            |
| 4           | 12            | 3            |
| 5           | -             | 1            |

**Çözüm 4.4**: Önce, aracın satın alındığı yıl başlangıç, planlama döneminin
sonu bitiş olmak üzere 6 düğümlü ağı oluşturalım. Ara noktalar (j = 1, 2, 3, 4,
5) araç yenilemenin mümkün olduğu yılın başına karşılık gelmektedir.

Şekil 4.30

i \< j için (i, j) dalı, i yılı başında satın alınan aracın j yılı başında
satılarak yerine yenisinin alınmasına karşılık gelir. (i, j) dalının uzunluğu
(dij) ise, i yılı başında satın alınan aracın j yılı başında satılmasına kadar
geçen süre içinde bakım ve onarımını yapmak, j yılının başında aracı satmak ve
yerine yenisini almanın net maliyetine eşittir.

Buna göre i j için dij = ve i \< j için,

dij = (i, i + 1, ..., j - 1 yıllarında araç bakım-onarım harcaması) + (i yılı
başında araç satın

alma maliyeti) - (j yılı başında eski araç satışından elde edilen gelir)

olarak tanımlandığında, her bir (i, j) dalının uzunluğu (net maliyet olarak)
aşağıdaki gibi hesaplanır.

d12 = d23 = d34 = d45 = d56 = 15 + 2 - 10 = 7

d13 = d24 = d35 = d46 = 15 + 2 + 3 - 9 = 11

d14 = d25 = d36 = 15 + 2 + 3 + 5 - 5 = 20

d15 = d26 = 15 + 2 + 3 + 5 + 8 - 3 = 30

d16 = 15 + 2 + 3 + 5 + 8 + 12 - 1 = 44

Hesaplama sonuçları Şekil 4.30’da gösterilmiştir. Artık Dijkstra Algoritmasını
uygulayabiliriz. Algoritmanın uygulanmasıyla elde edilen hesaplama sonuçları
aşağıda arka arkaya verilmiştir.

*Ön adım*:

Düğüm No: [1 2 3 4 5 6]

Ön adım

Düğüm No: [1 2 3 4 5 6]

Etiket : [0\* 7\* 11 20 30 44]

*Birinci adım*:

Düğüm No: [1 2 3 4 5 6]

Birinci tekrar

*İkinci adım*:

Düğüm No: [1 2 3 4 5 6]

Etiket : [0\* 7\* 11\* 18 27 37]

*Birinci adım*:

Düğüm No: [1 2 3 4 5 6]

İkinci tekrar

*İkinci adım*:

Düğüm No: [1 2 3 4 5 6]

Etiket : [0\* 7\* 11\* 18\* 22 31]

*Birinci adım*:

Düğüm No: [1 2 3 4 5 6]

Üçüncü tekrar

*İkinci adım*:

Düğüm No: [1 2 3 4 5 6]

Etiket : [0\* 7\* 11\* 18\* 22\* 29]

*Birinci adım*:

Düğüm No: [1 2 3 4 5 6]

Dördüncü tekrar

*İkinci adım*:

Düğüm No: [1 2 3 4 5 6]

Etiket : [0\* 7\* 11\* 18\* 22\* 29\*]

Etiketlerin hepsi kalıcı olduğundan en kısa yol daha doğrusu, en düşük maliyetli
araç yenileme planı belirlenmiş olur. En düşük net maliyet 29 TL’dir. Şimdi de
işletmenin hangi yıllarda araç yenileyeceğini belirleyelim. 5 ve 6 nolu
düğümlerin etiketleri arasındaki fark (5, 6) dalının uzunluğuna eşit olduğundan
bu dal en kısa yol üzerindedir. 5 ve 4 nolu düğümlerin kalıcı etiketleri
arasındaki fark, bu iki düğümü birleştiren dalın uzunluğuna eşit olmadığından,
bu dal en kısa yol üzerinde değildir. 5 ve 3 nolu düğümlerin etiketleri
arasındaki fark (3, 5) dalının uzunluğuna eşit olduğundan, bu dal en kısa yol
üzerindedir. 3 ve 2 nolu düğümlerin etiketleri arasındaki fark bu düğümleri
birleştiren dalın uzunluğuna eşit değildir. Dolayısıyla, (2, 3) dalı en kısa yol
üzerinde değildir. 3 ve 1 nolu düğümlerin etiketleri arasındaki fark (1, 3)
dalının uzunluğuna eşit olduğundan, bu dal da en kısa yol üzerindedir. Buna göre
çözüm, (1, 3), (3, 5), (5, 6) dallar dizisi olarak belirlenmiş olur. En kısa
yolu oluşturan dalları inceleyelim. Dalların ortaya koyduğu gibi, planlama
dönemi başında satın alınan araç 2 yıl kullanıldıktan sonra satılarak yerine
yenisi alınacaktır. Yeni araç iki yıl kullanıldıktan sonra satılacak, yerine
yenisi alınacak ve yeni araç 1 yıl kullanıldıktan sonra satılacak ve planlama
dönemi tamamlanacaktır.

**Kitap Yerleştirme Problemi**: Kütüphanelerin en önemli sorunlarından bir
tanesi de boyları ve kalınlıkları birbirlerinden farklı çok sayıdaki kitabın
yerleştirileceği raf sisteminin en düşük harcamayla kurulmasını sağlamaktır.
Bütün kitapların boylarının ve kalınlıklarının bilindiğini ve yerleştirmeye kısa
kitaplardan başlanacağını varsayalım. Bu varsayıma göre, yerleştirme Hi kitap
boyu olmak üzere H1, H2, ..., Hn için, H1 \< H2 \< ... \< Hn eşitsizliğini
sağlayacak şekilde gerçekleştirilecektir. Yüksekliği Hi olan bir kitabın
yerleştirileceği rafın yüksekliği en az Hi olmalıdır. Kitapların kalınlıkları
bilindiğinden, boyu Hi olan tüm kitapların yerleştirileceği rafın uzunluğu
hesaplanabilir. Söz konusu rafın uzunluğunu Li ile gösterelim. Kitapların tamamı
tek bir rafa yerleştirilmek istendiğinde kurulacak rafın toplam alanı, rafın
uzunluğu ile en uzun kitap boyunun çarpımına eşittir. Tek bir raf yerine,
kitapları boyları bakımından iki veya daha fazla sayıda gruba ayırarak aynı
sayıda raf kurulması durumunda toplam raf alanı daha az olur.

Farklı yükseklik ve uzunlukta raf kurma maliyeti aşağıda açıklanmıştır.
Yüksekliği Hi olan her bir raf için aşağıdaki tanımları verelim.

Ki = Raf alanından bağımsız sabit maliyet

Ci = Birim alan değişken maliyeti

Kitapların, yükseklikleri Hm ve Hn olan iki rafa dizilmek istendiğini düşünelim.
Hm \< Hn olsun. Yani, boyu Hm veya daha kısa olan kitaplar yüksekliği Hm olan
rafa, diğer bütün kitaplar yüksekliği Hn olan rafa yerleştirilsinler. Buna göre,
toplam maliyet aşağıdaki gibi tanımlanır.

Anlaşılacağı gibi problem, tüm kitapların yerleştirilmesi maliyetini en küçük
yapacak raf sayısı ile bunların uzunluk ve yüksekliklerinin belirlenmesidir.
Şimdi bu problemin bir en kısa yol problemi olarak çözümü üzerinde duralım.
Bunun için, düğümlerin kitap boylarını gösterdiği (n + 1) düğümlü bir ağ
oluşturalım. Ağın başlangıç düğümü sıfır boya, son düğümü en uzun kitap boyuna
karşılık gelsin.

Probleme uygun düşen ağ modelinin gerektirdiği varsayımlar şunlardır:

1\. 0 = Ho \< H1 \< H2 \< ... \< Hn

2\. j \> i ise, i ve j düğümleri birbirlerine doğrudan bağlıdır. Bu varsayım ile
Hi yüksekliğinde bir raftan sonra daha yüksek bir raf kurulması sağlanır. Bu
varsayımın doğal sonucu olarak ağdaki dal sayısı, (n(n + 1))/2) olur.

3\. dij = i ve j arasındaki uzaklık fonksiyonu,

j i için

j i için

olarak tanımlanmıştır.

Bu varsayımların kullanılmasıyla çizilen ağ aşağıda gösterilmiştir.

**Şekil 4.31**

Yapılan varsayımların doğal bir sonucu olarak yukarıdaki ağın başlangıç ve bitiş
düğümleri arasındaki en kısa yol, toplam maliyetin en küçük olmasını sağlayan
raf sayısı ile bunların yükseklik ve uzunluklarını verir. i ve j arasındaki
uzaklık fonksiyonu, sabit maliyet Kj’ye ek olarak boyu Hj olan kitaplar için
yüksekliği Hj olan raf kurma maliyetini gösterir. Önceden açıklandığı gibi +,
iki düğümü birleştiren dal bulunmaması anlamındadır. Bir an için problemin
çözüldüğünü ve en kısa yol üzerindeki düğümlerin (0, 5, 10, n) olarak
belirlendiğini varsayalım. Buna göre, boyu H5 veya daha az olan kitaplar H5
yüksekliğindeki rafa, boyu H10 veya daha kısa (H5’den uzun) olan tüm kitaplar
H10 yüksekliğindeki rafa, diğer bütün kitaplar yüksekliği Hn olan rafa
yerleştirileceklerdir. Bu yolla toplam maliyet, (0, 5), (5, 10) ve (10, n)
dallarının uzunlukları toplamına eşit olur.

**Örnek 4.5**: Boy (cm), kalınlık (cm) ve sayıları aşağıda verilen toplam 320
kitabın yerleştirileceği uygun raf sistemi belirlenmek istenmektedir.

**Tablo 4.2**

| Boy | Kalınlık | Sayı |
|-----|----------|------|
| 21  | 1        | 120  |
| 23  | 3        | 150  |
| 34  | 6        | 50   |

**Çözüm 4.5**: Yukarıdaki açıklamalar doğrultusunda ilk düğümü sıfır, son düğümü
en uzun kitap boyuna karşılık gelmek üzere dört düğüm ve altı daldan oluşan ağ
aşağıda gösterilmiştir. Ayrıca, dalların uzunluklarının hesaplanması ile ilgili
işlemler aşağıda özetlenmiş, hesaplama sonuçları ait oldukları dallar üzerinde
gösterilmiştir.

d0,1 = 80 + (1 x 21) x (1 x 120) = 2600

d1,2 = 80 + (1 x 23) x (3 x 150) = 10430

d2,3 = 80 + (1 x 34) x (6 x 50) = 10280

d0,2 = 80 + (1 x 23) x ( 1 x 120 + 3 x 150) = 13190

d1,3 = 80 + (1 x 34) x ( 3 x 150 + 6 x 50) = 25580

d0,3 = 80 + 1 x 34 x (1 x 120 + 3 x 150 + 6 x 50) = 29660

# Şekil 4.32

Şimdi de Dijkstra Algoritması ile en düşük maliyetli raf kurma planını
belirleyelim. Algoritmayla ilgili hesaplama sonuçları aşağıda toplu halde
verilmiştir.

**Ön adım:**

**Düğüm No : [0 1  2 3 ]**

**Ön adım**

**İkinci adım:**

**Düğüm No : [0 1  2 3 ]**

**Etiket  : [0\* 2600\* 13190 29660 ]**

**Birinci adım:**

**Düğüm No : [0 1  2 3 ]**

**Birinci tekrar**

**İkinci adım:**

**Düğüm No : [0 1  2 3 ]**

**Etiket  : [0\* 2600\* 13030\* 28180 ]**

**Birinci adım :**

**Düğüm No : [0 1  2 3 ]**

**İkinci tekrar**

**İkinci adım:**

**Düğüm No : [0 1  2 3 ]**

**Etiket  : [0\* 2600\* 13030\* 23310\*]**

**Tüm etiketler kalıcı olduğundan problem çözülmüştür. Şimdi de en kısa yolu,
yani en küçük maliyetli raf planını belirleyelim. Son iki düğüm arasındaki fark,
(2, 3) dalının uzunluğuna eşit olduğundan, (2, 3) en kısa yol üzerindedir. 2 ve
1 nolu düğümlerin etiketleri arasındaki fark (1, 2)’nin uzunluğuna eşit
olduğundan (1, 2), 0 ve 1 nolu düğümlerin etiketleri arasındaki fark (0, 1)
dalının uzunluğuna eşit olduğundan (0, 1) en kısa yol üzerindedir. Kısaca en
kısa yol, (0, 1), (1, 2), (2, 3) dallar dizisi olarak belirlenmiş olur. Bu yolu
oluşturmanın maliyeti 23310 TL olup en küçüktür. Kısaca yükseklik ve uzunlukları
sırasıyla, 21, 120; 23, 450; 34, 300 cm olan üç ayrı raf kurulacaktır.**

## 4.5. EN KÜÇÜK YAYILMALI AĞAÇ PROBLEMLERİ

En küçük yayılmalı ağaç problemleri, en kısa yol problemlerinin özel bir
biçimidir. En kısa yol problemlerinde olduğu gibi, en küçük yayılmalı ağaç
problemlerinde de dal uzunluklarının bilindiği varsayılır. İki problem
arasındaki en önemli fark en küçük yayılmalı ağaç probleminde düğümlerin tümünü,
en kısa yol probleminde düğümlerin bazılarını birleştiren dallar dizisinin
bulunmasıdır. Ayrıca en kısa yol probleminde ağın yönlendirilmiş olması şart
iken, yayılmalı ağaç probleminde ağın yönlendirilmemiş olması gerekir.
Uygulamada çok sık karşılaşılan bu tür problemlere örnek olması bakımından
belirli bir yerdeki bilgisayarlar topluluğunun birbirlerine bağlanmak
istendiklerini düşünelim. Burada, bilgisayarların her biri bir düğüm ve bunları
birbirlerine bağlayan yeraltı kabloları dal olarak ele alınabilir. Bilgisayarlar
arasındaki bağlantıyı sağlayan yeraltı kablolarının toplam uzunluğunun en kısa
olması amaçlanabilir. Bu amaca ulaşmak için belirlenen dallar topluluğunun
herhangi bir çevrim kapsamaması gerekir.

**Yayılan Ağaç: n düğümlü bir ağda tüm düğümler arasında bağlantı kuran ve (n -
1) sayıda daldan oluşan çevrim içermeyen dallar dizisidir.**

Dört düğümlü bir ağ ile bu ağa ait yayılan ağaçların listesi aşağıda
verilmiştir.

Şekil 4.33

**(1, 2), (1, 3), (1, 4) - (1, 2), (1, 4), (2, 3) - (1, 2), (1, 3), (3, 4)**

**(1, 2), (1, 4), (3, 4) - (1, 2), (2, 3), (3, 4) - (1, 3), (1, 4), (2, 3)**

**(1, 3), (2, 3), (3, 4) - (1, 4), (2, 3), (3, 4)**

**En Küçük Yayılmalı Ağaç: Kapsadığı dalların uzunlukları toplamı en küçük olan
yayılan ağaca en küçük yayılmalı ağaç denir.**

**Yukarıda listelenen yayılan ağaçlardan, (1, 4), (2, 3), (3, 4) ve (1, 2), (1,
4), (3,4) olmak üzere ikisinin en küçük uzunluğa (4 birim) sahip olduğu
görülebilir. Anlaşılacağı gibi, bu tip problemler tüm yayılan ağaçların
listelenmesi ve bunların uzunlukların hesaplanmasıyla çözülebilir. Ancak, küçük
ağlar için bile etkin olmayan bu yaklaşım, büyük ağlar için hiç etkin değildir.
En küçük yayılmalı ağaç problemlerinin çözümü için etkin hesaplama teknikleri
geliştirilmiştir. Bunlardan en yaygın biçimde kullanılan "en küçük yayılmalı
ağaç algoritması" aşağıda açıklanmıştır.**

*En Küçük Yayılmalı Ağaç Algoritması***: En küçük yayılmalı ağaç, aşağıda
açıklanan üç adımlık bir algoritmanın tekrarı ile saptanabilir.**

**1. adım: Ağ kapsamındaki düğümlerin oluşturduğu küme N olsun. Bu kümeden
rastgele bir düğüm (i) seçilerek bu düğüme en yakın olan düğüm (j) belirlenir.
Bu iki düğümü birleştiren (i, j) dalı en küçük yayılmalı ağacın bir dalı olur.
Bu yolla ağın düğümleri, birinde birleştirilmiş (i ve j), diğerinde
birleştirilmemiş (i ve j dışındakiler) düğümlerin bulunduğu iki alt kümeye
ayrılmış olur. Birleştirilmiş düğümlerin oluşturduğu küme C, birleştirilmemiş
düğümlerin oluşturduğu küme ile gösterilir. Aloritmanın tüm adımlarında N = C U 
, dolayısıyla C  = { } olduğu unutulmamalıdır.**

**2. adım: ’daki düğümlerden (n), C’deki düğümlerden (m) herhangi birine en
yakın olan düğüm belirlenir. Bu kez, bu iki düğümü birleştiren (m, n) dalı en
küçük yayılmalı ağaca eklenir. Bu durumda C = {i, j, n} olacağından, C’ye
eklenen düğüm (n) kümesinden çıkarılır.**

**3. adım: İkinci adımdaki işlemler tüm düğümler birleştirilinceye değin
tekrarlanır. Birleştirilecek düğüm kalmadığında, yani ={ } olduğunda en küçük
yayılmalı ağaç belirlenmiş olur.**

Örnek 4.6**: Bir işletmenin, çalışanlarının hizmetine sunduğu 7 adet bilgisayarı
vardır. Bilgisayarlar arasındaki uzaklıklar aşağıda gösterilmiştir.**

Şekil 4.34

**Bilgisayarlar yeraltı kabloları ile birbirlerine bağlanmak istenmektedir. Bu
amacı gerçekleştirecek en kısa kablo uzunluğu nedir?**

Çözüm 4.6**: 1. adım: Rastgele seçilen ilk düğüm A olsun. A’ya en yakın düğüm B
olduğundan C = {A, B}, = {C, D, E, F, G} olur. Böylece A’dan sonra B ağaca
eklenir. Eklenen (A, B) dalının dolu çizgiyle gösterilmesiyle ağ aşağıdaki gibi
belirlenmiş olur.**

Şekil 4.35

**2. adım: Birleştirilmemiş düğümlerin (C, D, E, F, G) A ve B’ye olan
uzaklıklarını inceleyelim.**

Uzunlukları karşılaştırılacak dallar şunlardır: (A, C), (A, D), (B, C), (B, E).

**En kısa uzunluk (4) (A, D)’ye ait olduğundan, en küçük yayılmalı ağaca
eklenir. Bu durumda C = {A, B, D}, = {C, E, F, G} olur. Eklenen (A, D) dalının
dolu çizgiyle gösterilmesiyle şimdilik iki daldan oluşan tamamlanmamış ağaç
aşağıdaki gibi belirlenmiş olur.**

Şekil 4.36

**3. adım: Birleştirilen düğümler kümesi C’yi oluşturan A, B ve D’ye uzaklık
bakımından en yakın olan düğümleri belirleyelim. Halihazırda  kapsamında bulunan
C, E ve F düğümlerinin birleştirilmiş A, B ve Ddüğümlerine olan uzaklıkları
incelendiğinde, en kısa mesafenin (C, D)’ye ait olduğu görülecektir. Buna göre,
C = {A, B, C, D} olur ve (C, D) ağaca eklenir. Eklenen (C, D) dalının dolu
çizgiyle gösterilmesiyle, şimdilik üç daldan oluşan tamamlanmamış ağaç aşağıdaki
gibi belirlenmiş olur.**

Şekil 4.37

4\. adım: Ağaca eklenmemiş üç düğüm (E, F, G) vardır. Yani, = {E, F, G}’dir.
içeriğindeki her bir noktanın halihazırda birleştirilmiş olan A, B, C ve D’ye
olan uzaklıkları uzaklıkları incelendiğinde, en kısa mesafenin (C, F)’ye ait
olduğu görülebilir. Bu durumda C = {A, B, C, D, F}, = {E, G} olduğu ve (C,
F)’nin en küçük yayılmalı ağaca ait olduğu kararlaştırılır.

Bu dalın eklenmesiyle, Şekil 4.37’deki ağaçtan daha gelişmiş (üç yerine dört
dalı olan) ancak, henüz tamam olmayan ağaç Şekil 4.38’deki gibi belirlenmiş
olur.

Şekil 4.38

5\. adım: 4. adımda bağlanan 5 noktaya en yakın bilgisayar E’dir. Bu nedenle bu
bilgisayar C’nin yeni elemanı olur.

Bu noktada, C = {A, B, C, D, E, F}, = {G} ve yeni dal Şekil 4.39’da gösterildiği
gibi (E, F) olur.

Şekil 4.39

**6. adım: Ağaca eklenmeyen tek düğüm G’dir. G’yi ağaca bağlayan en kısa dal (E,
G) olduğundan G, E ile birleştirilir.**

**Bu durumda C = {A, B, C, D, E, F, G}, = { } olur. = { } olduğundan problem
çözülmüştür.**

**Şekil 4.40’da koyu renkle çizilmiş ve beklendiği gibi sayıları ağdaki düğüm
sayısının 1 eksiğine (6) eşit olan (A, B), (A, D), (C, D), (C, F), (F, E), (F,
G) dallarından oluşan en küçük yayılmalı ağacın uzunluğu 16 birimdir.**

Şekil 4.40

**Başlangıçta rastgele seçilen düğümün en iyi çözümü değiştirip değiştirmeyeceği
sorulabilir. Soruyu yanıtlamak için ilk düğüm olarak E’yi seçelim. Bu kez
işlemler ayrıntılarıyla değil aşağıdaki gibi küme gösterimiyle açıklanacaktır.**

**Birinci adım: C = {E, F}, = {A, B, C, D, G}; (E, F) ağaçta.**

**İkinci adım: C = {E, F, C}, = {A, B, D, G}; (F, C) ağaçta.**

**Üçüncü adım: C = {E, F, C, D}, = {A, B, G}; (C, D) ağaçta.**

**Dördüncü adım: C = {E, F, C, D, A}, = {B, G}; (D, A) ağaçta.**

**Beşinci adım: C = {E, F, C, D, A, B}, = {G}; (A, B) ağaçta.**

**Altıncı adım: C = {E, F, C, D, A, B, G}, = { }; (E, G) ağaçta.**

Rasgele seçilen ilk düğüm E iken, anılan ağaç {(E, F), (F, C), (C, D), (D, A),
(A, B), (E, G)} olarak belirlenmiştir. E seçimiyle belirlenen en küçük yayılmalı
ağaç ile A seçimiyle belirlenen ağacın aynı olduğuna dikkat edilmelidir.

## 4.6. PROJE ÇİZELGELEME PROBLEMLERİ

Konu ne olursa olsun, eldeki kaynakların etkin biçimde kullanılmasında;
planlama, programlama ve kontrolün önemi büyüktür. Konu proje yönetimi olduğunda
planlama, programlama ve kontrolün önemi daha da belirginleşmektedir. Proje
yönetiminde, planlama tekniklerinden kritik yol yöntemi (CPM[^1]) ile proje
değerlendirme ve gözden geçirme tekniği (PERT[^2]) gelişmiş ülkelerde çok geniş
bir uygulama alanı olan proje çizelgeleme teknikleridir. Anılan yöntemler eldeki
sınırlı kaynaklar ölçüsünde projenin tamamlanma süresinin belirlenmesi, toplam
maliyeti en düşük yapacak proje süresinin saptanması, sürenin kısaltılması
amacıyla kaynak aktarımı yapılması vb. konularda yöneticiler için hayati önem
taşıyan sorunlara etkili çözüm yolları ararlar ve bulurlar. Anılan yöntemler
ülkemizde de birçok büyük projede kullanılmıştır. II. Fatih Sultan Mehmet
Köprüsü ve Güney Doğu Anadolu Projesi CPM, Keban Barajı ve İstanbul Boğaz
Köprüsü PERT’in uygulandığı projelere örnek gösterilebilir.

[^1]: **Critical Path Method kelimelerinin ilk harfleri.**

[^2]: **Program Evaluation and Review Techniques kelimelerinin ilk harfleri.**

CPM ve PERT, birbirine bağlı çok sayıda faaliyetten oluşan büyük ve projelerin
programlanmasında kullanılan yöntemlerdir. Birbirlerinden bağımsız
geliştirilmelerine karşın birbirlerine çok benzeyen bu iki yöntem arasındaki en
önemli fark faaliyet sürelerine ilişkindir. PERT’de faaliyetlere ilişkin süreler
belirsiz olup bir takım olasılık hesaplamaları ile tanımlandığı halde, CPM’de bu
sürelerin kesinlikle bilindiği varsayılmaktadır. Yöntemleri açıklamadan önce
konuyla ilgili temel kavramların açıklanması uygun olur.

**Faaliyet: Bir iş ya da projenin tamamlanması için gerçekleştirilen eylemlerin
her birine faaliyet denir.**

**Her faaliyetin bir süresi vardır ve gerçekleşmesi genellikle belirli
kaynakların kullanılmasını gerektirir. Örneğin, bir ürünün bir yerden başka bir
yere taşınması, temel atılması, duvarın sıvanması, bahçenin sulanması vb. birer
faaliyettir. Projedeki faaliyetler ağ üzerinde oklarla gösterilir. Okların yönü
faaliyetlerin akışını, yeri ise faaliyetlerin proje içindeki sırasını
gösterir.**

**Olay: Bir iş veya projenin zaman akışı içindeki belirli noktalarda varılması
gereken aşamalarına olay denir.**

Süreleri olmamakla birlikte her olayın birer tarih ya da saati vardır. Örneğin
duvarın sıvanmaya başlanması tarihi, kamyonun depoya varış saati gibi. Olaylar
okların birleştikleri yerlerde birer daire ile gösterilirler.

Olay ve faaliyetlerin ağda nasıl gösterildikleri Şekil 4.41’de açıklanmıştır.

Şekil 4.41

**Kukla Faaliyet: Zaman ve kaynak kullanımı gerektirmeyen, yalnızca iki veya
daha fazla sayıdaki gerçek faaliyet arasındaki ilişkileri göstermek amacıyla
kullanılan faaliyetlere kukla faaliyet denir.**

Kukla faaliyetler kesik çizgili oklarla gösterilirler ve paralel (aynı noktada
başlayıp aynı noktada biten) faaliyetlerin ayırt edilmesinde kullanılırlar.

Şekil 4.42

*Süreli Kukla Faaliyet*: Belirli bir süresi olmakla birlikte kaynak kullanımı
gerektirmeyen faaliyete, süreli kukla faaliyet denir.

Örneğin, sulanan veya boyanan bir yerin kuruması için bekletilmesi. Süreli
kuklalar bazan kukla faaliyetler gibi kesik çizgi ile bazan gerçek faaliyetler
gibi dolu çizgi ile gösterilirler.

Konuyla ilgili bu önemli kavramların ardından, önce CPM ardından PERT ile ilgili
açıklamalara geçebiliriz. Ancak daha önce, 1955 yılına kadar proje yönetiminde
en yaygın biçimde kullanılan planlama tekniklerinden Gantt çizelgesi üzerinde
kısaca duralım.

### 4.6.1. Gantt Çizelgesi

Faaliyetler arasındaki zaman ve maliyet faktörlerini de dikkate alarak gösterme
fikri yeni değildir. Özellikle Henry Gantt bu konuda daha 1900’lü yılların
başlarında önemli çalışmalar yapmış, planlama ve kontrol faaliyetleri için kendi
adıyla anılan çizelgeyi (Gantt çizelgesi) geliştirmiştir. 1960’lara kadar,
planlama ve kontrol sorunlarında çözüm aracı olarak yaygın biçimde kullanılan
Gantt çizelgesi günümüzde sanayi mühendisleri tarafından sıkça kullanılmaktadır.
Proje adımlarını sistematik olarak tanımlamaya yarayan Gantt çizelgesi
istatistiksel grafikler içerisinde okunması ve izlenmesi en kolay çizelgelerden
biridir. Faaliyetlerin başlama ve bitiş zamanlarının yatay bir zaman ekseni
üzerinde belirtilmesi esasına dayanan bu çizelgenin bir başka özelliği dinamik
olması yani, programlanan işle belirli bir anda yapılmış olan iş miktarını
karşılaştırma olanağı sağlamasıdır. Gantt çizelgesinde, faaliyetlerin sırası
yukarıdan aşağıya doğru dikey eksen üzerinde, zaman akışı ise yatay eksen
üzerinde gösterilir. Zaman birimi olarak ay, hafta, gün veya saat seçilebilir.
Bu seçim yapılan işin özelliğine göre değişir. Proje planlama yöntemlerinden
olan Gantt çizelgesinde faaliyetler, süreleriyle orantılı olarak şerit halinde
ve yatay çizgi ile gösterilir.

A, B, C ve D olmak üzere dört faaliyetten oluşan bir projenin uygulama programı
(Gantt Çizelgesi) Tablo 4.3’de verilmiştır.

**Tablo 4.3**

|          | H A F T A |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
|----------|-----------|---|---|---|---|---|---|---|---|----|----|----|----|----|----|
| Faaliyet | 1         | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 |
| A        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
| B        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
| C        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
| D        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |

Tablo 4.3 incelendiğinde, A’nın 4, B’nin 3, C’nin 6 ve D’nin 2 haftada
tamamlandıkları görülecektir. Buna göre örneğin, 10. haftanın sonunda A ve B
faaliyetlerinin bitmiş, C faaliyetinin yarısının tamamlanmış ve D faaliyetine
hiç başlanmamış olması gerekmektedir. Gantt çizelgesi üzerinde tamamlanan
faaliyetlerin kalın bir şerit ile gösterilmesi sonucunda hangi faaliyetlerin
gerçekleştirildiği belirlenerek programın kontrolü sağlanmış olur. Bu amaçla
oluşturulan Tablo 4.4 incelendiğinde 10. hafta sonunda A ve B faaliyetlerinin
programa uygun olarak tamamlanmış, D faaliyetinin henüz başlamamış olduğu, C
faaliyetinin ise programın 2 hafta gerisinde olduğu görülür.

**Tablo 4.4**

|          | H A F T A |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
|----------|-----------|---|---|---|---|---|---|---|---|----|----|----|----|----|----|
| Faaliyet | 1         | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 |
| A        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
| B        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
| C        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |
| D        |           |   |   |   |   |   |   |   |   |    |    |    |    |    |    |

Basit ve küçük çapta projeler için kullanışlı olmasına karşın, büyük projeler
için kullanışlı olmayan Gantt çizelgesi, faaliyetler arasındaki bağımlılıkları
da tam olarak açıklayamamaktadır. Hangi faaliyetlerin geciktirilebileceği,
hangilerinin geciktirilemeyeceği hakkında bilgi de vermemektedir. Zaman-maliyet
analizi yapabilmek için gerekli bilgi Gantt çizelgesinde yoktur. Söz konusu
çizelgenin bu olumsuz özellikleri ağ yaklaşımını ortaya çıkarmıştır.

### 4.6.2. Ağ Yaklaşımı

Projelerin plan ve programlanması ile ilgili işletme problemleri bir çizelgeyle
gösterilebilir. Bu çizelge şeklindeki gösterim ağ olabilir. Bilindiği gibi ağ
sözcüğü ok şeklinde çizilen ve ağ planlama tekniklerinin esas kısmını oluşturan
birbirlerine bağlı faaliyetlerin şekil ya da çizelge olarak gösterilmesinden
doğmaktadır. Proje söz konusu olduğunda ağ şu şekilde tanımlanmaktadır. "Program
amacına ulaşabilmek için gerçekleşmesi gereken faaliyetlerden ve olaylardan
meydana gelen, faaliyet ve olayların birbirleriyle olan bağlantı ve ilişkilerini
gösteren şemaya ağ" denir. Ağ yaklaşımının sağladığı yararlar aşağıdaki gibi
özetlenebilir.

-   Bir ya da daha fazla sayıda projenin aynı anda ve istenen ayrıntıda planlama
    ve denetiminin yapılmasına olanak sağlar.

-   Faaliyetler arasındaki karmaşık ilişkiler oldukça basit ve açık biçimde
    gösterilir. Böylece proje, planlamayı yapanların dışındaki kimselere de
    kolayca açıklanabilir.

-   İşlemler oldukça basit olup, bilgisayarda kolayca programlanabilir.

-   Kritik faaliyetlerin saptanması sonucunda önemli olan bir grup faalliyete
    dikkat çekilir. Böylece, daha etkin bir planlama ve denetime olanak
    sağlanır.

-   Bazı faaliyetlerin gecikme ve/veya hızlandırılmalarının etkileri ve bunlara
    bağlı olarak oluşacak darboğazların kolayca saptanabileceği bir ortam
    oluşturulur.

-   Değişik proje tarihlerine ilişkin toplam proje maliyetleri hesaplanarak en
    düşük toplam maliyetli proje planı seçilebilir.

-   Çok değişik konu ve kapsamda proje kolayca planlanabilir.

-   Kaynaklar, aynı kaynağı kullanan faaliyetler arasında en düşük toplam
    maliyete neden olacak şekilde bölüştürülebilir. Burada, problemin güçlüğü
    nedeniyle en düşük maliyete neden olacak bölüşüm sağlanamasa da buna yakın
    bir sonuç elde edilebilir.

-   Projenin uygulanması sırasında güncelleştirmeye önem verilerek projenin günü
    gününe izlenmesi sağlanır. Böylece proje yönetiminden sorumlu kimselerin
    aksayan noktaları görebilmeleri ve gerektiğinde süratle müdahale
    edebilmelerini sağlayan bir alet oluşturulmuş olur.

Araştırmalar ağ yaklaşımının kullanıldığı uygun işlerde projenin tamamlanma
süresinin en az %10 azaltılabileceğini, kaynak kullanımındaki faydanın ise en
azından %5 artırılabileceğini göstermiştir.

#### 4.6.2.1. Kritik Yol Yöntemi

Kritik yol yöntemi (CPM), bir projenin gerçekleştirilmesinde insan gücü, makina
ve zamandan en yüksek düzeyde yararlanmayı sağlayan ağ tekniklerini kullanma
bilimidir. CPM formülasyon, planlama, gözlem ve kontrol olmak üzere başlıca üç
bölüm içerir.

a. *Formülasyon*: Bu bölüm aşağıdaki adımları kapsar.

1\. Belirli olay ve faaliyetlere ayırım işleminin yapılması.

2\. Olay ve faaliyetler arasındaki ilişkilerin belirlenmesi.

3\. Proje ağının kurulması.

4\. Tüm faaliyetlerin sürelerinin belirlenmesi.

b. *Planlama*: Bu bölüm esas olarak boşlukları ve kritik yolu bulmayı içerir ve
aşağıdaki adımları kapsar.

1\. Kritik olay ve faaliyetlerin belirlenmesi.

2\. Kritik yolun belirlenmesi.

3\. Tüm olay ve faaliyetlerin boşluklarının hesaplanması.

4\. Tamamlanmış proje planının kurulması.

c. *Gözlem ve Kontrol*: CPM kullanımının bu bölümü aşağıdaki adımları kapsar.

1.  Tüm faaliyetlerin belirlenmiş zamanlarının gözlenerek, hazırlanan planla
    karşılaştırılması.

2.  Esas plandan olan sapmaların belirlenmesi.

3.  Gecikmeler belirlendiğinde, yeniden planlama ile orijinal ağda değişiklik
    yapılması.

4.  Eğer mümkünse boşluklara göre kaynakların faaliyetlere transfer edilmesi.

Yukarıda açıklandığı gibi, formülasyon sürecinde, projenin belirli faaliyet ve
olaylara ayrılmasından sonra bunlar (faaliyetler ve olaylar) arasındaki öncelik
ilişkilerinin belirlenmesi gerekir. Bir faaliyetin kendisinden önce bitirilmesi
gereken faaliyete "önceki faaliyet", kendisinin tamamlanması ile başlayan
faaliyete de "sonraki faaliyet" denir.

Faaliyetlerin öncelik ilişkilerinde istenen önemli bilgiler aşağıdaki üç sorunun
yanıtlanması ile gerçekleştirilebilir.

1\. Herhangi bir faaliyet başlamadan önce hangi faaliyet(ler) tamamlanmalıdır?

2\. Hangi faaliyetler paralel yürütülmelidir?

3\. Bu faaliyetleri hangi faaliyetler izlemelidir?

**A. Proje Ağının Oluşturulması**

Proje ağının çizilmesinde uyulması gereken kurallar şöyledir.

1.  Her ağda tek bir başlama olayı ile tek bir bitiş olayı olmalıdır. Gerekirse
    bu olaylar yapay olarak yaratılırlar.

2.  Bir faaliyet, kendisinden önceki faaliyet(ler) bitmeden başlayamaz.

3.  Bir okun uzunluğu önemli olmayıp oklar yalnızca öncelikleri belirtir.

4.  İki olay en fazla bir faaliyet ile doğrudan bağlanabilir.

5.  Her olayın bir numarası olmalıdır. Olaylar okların küçük numaralı bir
    noktadan daha büyük numaralı bir noktaya gitmesini sağlayacak biçimde
    numaralandırılır. Böylece ağ üzerinde çevrim oluşması engellenmiş olur.

Şekil 4.43’deki faaliyetlerin bir çevrim meydana getirdiği görülmektedir.

Şekil 4.43

Yukarıda açıklanan kurallardan bazılarını inceleyelim. Dördüncü kurala göre iki
olay en fazla bir faaliyetle doğrudan bağlanabilir. Bunun nedeni, faaliyetleri
ayırt edebilme zorunluluğudur. Şekil 4.44’de 1 ve 2 numaralı olaylar birden
fazla faaliyetle doğrudan bağlanmış olup bu yasaktır.

**Şekil 4.44**

Kural 4’e ters düşen bu durumdan kurtulmak için kukla faaliyet kullanılır. Bu
duruma uygun alternatif kukla faaliyetler Şekil 4.45’de gösterilmiştir.

Şekil 4.45

Kukla faaliyetler yalnızca paralel faaliyetlerin ayırt edilmesinde değil,
faaliyetler arasındaki öncelik ilişkilerinin belirtilmesinde de kullanılırlar.
Kukla faaliyet kullanımına örnek olmak üzere Tablo 4.5’deki verileri alalım.

#### Tablo 4.5

| Faaliyet | Önceki Faaliyet |
|----------|-----------------|
| A        | -               |
| B        | -               |
| C        | A, B            |
| D        | B               |

Faaliyetlerin öncelik ilişkilerinin dikkate alınmasıyla çizilen ağ Şekil 4.46’da
gösterilmiştir. Ağın faaliyetler arasındaki öncelik ilişkileri bakımından doğru
olduğu görülebilir. Ancak şekil dikkatle incelendiğinde D faaliyetinin
başlayabilmesi için A ve B faaliyetlerinin tamamlanması gerektiği görülebilir.
Oysa tabloda verildiği gibi D faaliyeti ile A faaliyeti arasında herhangi bir
bağımlılık bulunmamaktadır. Ağın aşağıdaki gibi çizilmesiyle D ve A faaliyetleri
arasında yapay bir bağımlılık yaratılmıştır.

Şekil 4.46

Bu durumdan kurtulabilmek için kukla faaliyetler kullanılır. Tablo 4.5’deki
faaliyetlerin öncelik ilişkilerini yansıtan ve kurallara uygun olarak çizilen ağ
Şekil 4.47’de gösterilmiştir. Buna göre D, B’den sonra, C faaliyeti de A ve B
faaliyetlerinin tamamlanmasından sonra başlayabilmektedir.

Şekil 4.47

Faaliyetlerin öncelik ilişkileri aşağıda bir dizi örnekle açıklanmıştır.

B, A tamamlandıktan sonra başlar veya A, B’den önce gelir (bkz. Şekil 4.48).

Şekil 4.48

C, A ve B tamamlandıktan sonra başlar veya A ve B, C’den önce gelir (bkz. Şekil
4.49).

Şekil 4.49

B ve C, A tamamlandıktan sonra başlar veya A, B ve C’den önce gelir (bkz. Şekil
4.50).

Şekil 4.50

Proje ağı iki farklı yaklaşımla çizilebilir. Yaklaşımlardan birisinde
faaliyetler oklarla, diğerinde noktalarla gösterililir. Her iki yaklaşımın da
olumlu ve olumsuz yönleri vardır. Sözgelimi, faaliyetlerin noktalara atandığı
durumdaki proje ağının çizimi kolay olmakla birlikte faaliyetlere ilişkin
bilgiler net olarak gözükmemektedir. Yüzlerce faaliyetten oluşan büyük
projelerde bu durum karışıklık yaratabilir. Faaliyetlerin oklara atandığı
durumda ağın oluşturulması daha zordur ve kukla faaliyetlere gerek duyulabilir.
Ancak, faaliyetlere ilişkin bilgiler ağdan kolayca izlenebilir. Ayrıca, günümüz
ticari bilgisayar programlarının çoğunda faaliyetlerin oklarla gösterilmesi
yaklaşımı benimsendiğinden, biz de faaliyetlerin oklarla gösterilmesi esasını
benimseyeceğiz. Bu yaklaşım örnek problemlerle açıklanacaktır.

**Örnek 4.7**: Süre ve öncelik ilişkileri aşağıda verilen A, B, ..., G, H
faaliyetlerinden oluşan projenin ağını çiziniz.

#### Tablo 4.6

| Faaliyet | Süre (gün) | Önceki Faaliyet |
|----------|------------|-----------------|
| A        | 4          | -               |
| B        | 8          | -               |
| C        | 2          | A               |
| D        | 3          | A               |
| E        | 8          | B, C            |
| F        | 5          | B, C            |
| G        | 5          | D, E            |
| H        | 10         | D, E, F         |

**Çözüm 4.7**: Tablodaki verilerden hareketle kurulan proje ağı Şekil 4.51’de
gösterilmiştir.

Süreler parantez içerisinde olmak üzere, faaliyet isimleri okların üzerinde
belirtilmiştir. Tabloda belirtildiği gibi D ve E faaliyetleri hem G hem de H’dan
önce gelen faaliyetlerdir. H’dan önce gelen D, E, F faaliyetlerini ağda doğru
olarak gösterebilmek için kukla faaliyete gerek duyulmuştur. Kukla faaliyet
kesikli çizgi ile gösterilmiş ve K ile isimlendirilmiştir. Olaylar projede
ilerleme yönünü belirleyecek sırada numaralanmıştır.

Şekil 4.51

**Örnek 4.8**: Bir işletme A, B ve C parçalarından oluşan yeni bir ürün üretmeyi
planlamaktadır. Ürünün mamul hale gelmesi için öncelikle bu üç parçanın
tasarımının tamamlanması gerekmekte olup bu işlem 5 hafta sürmektedir.
Tasarımdan sonra üretime geçilmektedir. A’nın üretimi 4, B’nin üretimi 5, C’nin
üretimi 3 haftada tamamlanmaktadır. Üretilen parçaların birleştirilmesinden önce
A test edilmekte, bu işlem 2 hafta sürmektedir. Testten sonra montaja
geçilmektedir. Montaj için önce A ile B birleştirilmekte (2 hafta) sonra C
eklenmektedir (1 hafta). C’nin eklenmesiyle tamamlanan ürünün test edilmesi 1
hafta sürmektedir.

Faaliyetleri ve faaliyetler arasındaki ilişkileri belirleyerek üretim projesinin
ağını kurunuz.

**Çözüm 4.8**: Açıklamalar doğrultusunda belirlenen faaliyetler, faaliyetlerin
öncelik ilişkileri ve süreler (gün) aşağıdaki tabloda topluca gösterilmiştir.

# Tablo 4.7

| Faaliyet  Adı |  Faaliyet Tanımı           | Önceki  Faaliyet |  Süre |
|---------------|----------------------------|------------------|-------|
| T             | Tasarım                    | -                | 5     |
| A             | A’nın Üretimi              | T                | 4     |
| B             | B’nin Üretimi              | T                | 5     |
| C             | C’nin Üretimi              | T                | 3     |
| D             | A’nın Testi                | A                | 2     |
| E             | A ve B’nin Birleştirilmesi | B, D             | 2     |
| F             | C’nin Birleştirilmesi      | E, C             | 1     |
| S             | Ürün Testi                 | F                | 1     |

Tablodaki verilerle çizilen proje ağı aşağıda gösterilmiştir.

Şekil 4.52

**Örnek 4.9**: Yeni bir otomobil satın almak için gerekli 15 faaliyet aşağıdaki
tabloda, kısa tanım ve süreleriyle birlikte verilmiştir. Faaliyetler arasındaki
öncelik ilişkileri, aynı tablonun son sütununda gösterildiği gibidir. Proje
ağını çiziniz.

# Tablo 4.8

|  Faaliyet |  Kısa Tanım                                      | Önceki  Faaliyet(ler) |  Süre |
|-----------|--------------------------------------------------|-----------------------|-------|
| A         | Fizibilite Çalışmasını Sonlandırma               | -                     | 3     |
| B         | Şimdiki otomobil için alıcı bulma                | A                     | 14    |
| C         | Olası modelleri listeleme                        | A                     | 1     |
| D         | Olası modelleri araştırma                        | C                     | 3     |
| E         | Servisler hakkında bilgi alma                    | C                     | 1     |
| F         | Bayilerin kampanya broşürlerini toplama          | C                     | 2     |
| G         | Uygun veriyi derleme                             | D, E, F               | 1     |
| H         | En iyi üç modeli seçme                           | G                     | 1     |
| I         | Bu üç modelin test sürüşünü yapma                | H                     | 3     |
| J         | Garanti ve finans verisini toplama               | H                     | 2     |
| K         | Modellerden birini seçme                         | I, J                  | 2     |
| L         | Bayii seçme                                      | K                     | 2     |
| M         | İstenilen renk ve opsiyonları belirleme          | L                     | 4     |
| N         | Seçilen model ile bir kez daha test sürüşü yapma | L                     | 1     |
| O         | Yeni otomobil satın alma                         | B, M, N               | 3     |

**Çözüm 4.9**: A ilk, O son faaliyet olmak üzere tablodaki verilerle çizilen
proje ağı Şekil 4.53’de gösterilmiştir. Ağ çiziminde biri D ve E’nin diğeri E ve
F’nin (dolayısıyla D, E ve F’nin), üçüncüsü I ve J’nin, dördüncüsü M ve N’nin
aynı düğümde tamamlanmasını sağlamak için, 4 kukla faaliyet (K0, K1, K2,K3)
kullanıldığı görülebilir.

Kritik olmayan faaliyetler ise belirli zaman aralıklarında tamamlandıklarında
proje süresini değiştirmeyen esnek faaliyetlerdir. Kritik olmayan faaliyetlerin
esnekliğine ya da geciktirilebilme rahatlığına "boşluk" denir. Boşluk değerleri
kritik yol hesaplamalarında doğrudan kullanılmamakla birlikte, zaman-maliyet
analizinde ve kaynak tahsisinde kullanılmaktadır.

1\. Toplam boşluk, 2. Serbest boşluk, 3. Bağımsız boşluk, 4. Emniyet boşluğu
olmak üzere dört çeşit boşluk hesaplanmaktadır. En çok bilinen boşluklar toplam
boşluk ile serbest boşluktur.

Sözü edilen boşluk çeşitlerini kısaca açıklayalım.

*Toplam Boşluk*: Bir faaliyetin, proje süresini uzatmadan ertelenebileceği en
uzun süreye toplam boşluk (TB) denir.

Toplam boşluk hesaplanırken (i, j) faaliyetinden önce gelen bütün faaliyetlerin
en erken başlama zamanında başladığı kabul edilir. Buna göre toplam boşluk, Lj
ve Ei terimleriyle açıklanabilir. (i, j) faaliyetinin i düğümünde başladığı
dikkate alındığında, i’nin ortaya çıkışı veya (i, j) faaliyetinin tamamlanma
süresi k birim zaman geciktirilirse, (i, j) faaliyeti, Ei + k + Dij zamanında
tamamlanacaktır. Bu durumda,

Ei + k + Dij Lj veya k Lj - Ei - Dij

ise projenin en erken tamamlanma süresi gecikmeyecektir.

Buna göre, (i, j) faaliyetinin toplam boşluğu şöyledir:

TBij = Lj - Ei - Dij

Bu açıklamalar çerçevesinde Şekil 4.59’daki D faaliyetine ilişkin toplam boşluğu
hesaplayalım.

# Şekil 4.59

TB24 = TBD = 16 - (4 + 3) = 9 gün olacaktır.

Buna göre D, en erken başlama zamanı olan 4. günde başlatıldığında, izin verilen
en geç zamandan 9 gün önce biter. Faaliyetin 3 gün olan normal süresi (3 + 9)
güne kadar uzatılabilir. Bu gecikmeye karşın programda bir değişiklik olmaz.
Herhangi bir faaliyetin toplam boşluğu kendisine ait süredeki esnekliğin
ölçüsüdür. Kritik faaliyetlerin toplam boşlukları sıfıra eşittir.

Faaliyet süresinin esnekliğiyle ilgili bir başka ölçü serbest boşluktur.

*Serbest Boşluk*: Bir faaliyetin, kendisinden sonra gelen faaliyetlerin
başlamasını etkilemeden ertelenebileceği en uzun süreye serbest boşluk (SB)
denir.

Serbest boşluk bir faaliyetin yalnızca kendisini ilgilendiren bir boşluk
türüdür. Serbest boşluk, toplam boşluğa eşit ya da küçüktür. Serbest boşluk için
de (i, j) faaliyetini etkileyen önceki faaliyetlerin en erken başlama zamanında
başladıkları varsayılır. Olay i’nin ortaya çıkışının veya (i, j)’nin süresinin k
birim uzadığını düşünelim. Bu durumda j’nin en erken ortaya çıkacağı zaman (Ei +
Dij + k)’ya eşit olur. Buna göre,

Ei + Dij + k Eij veya k Ej - Ei - Dij

ise j düğümü gecikmez.

Bu durumda, (i, j) faaliyetinin serbest boşluğu,

SBij = Ej - Ei - Dij

olur.

D faaliyetinin serbest boşluğu aşağıdaki gibi hesaplanmıştır.

SB24 = SBD = 16 - 4 - 3 = 9 gün

D’nin serbest boşluğunun 9 gün olması, bu faaliyetin başlamasının veya
tamamlanmasının 9 gün veya daha fazla uzaması durumunda, bu faaliyeti izleyen E
ve G faaliyetlerinin başlamalarının gecikeceği anlamını taşır.

Toplam boşluk ve serbest boşluk tanımlarında yapılan varsayım, faaliyetlerin
zamanlanmasında sınırlayıcı olabilmektedir. Buna bir çare olarak bağımsız ve
emniyet boşlukları tanımlanmıştır.

*Bağımsız Boşluk*: Bir faaliyetin kendisini izleyen faaliyetlerin başlamalarını
etkilemeden ertelenebileceği en uzun süreye bağımsız boşluk (BB) denir.

Bağımsız boşluk da tıpkı serbest boşluk gibi, yalnızca ait olduğu faaliyeti
ilgilendiren bir boşluk türüdür. (i, j) faaliyetinin bağımsız boşluğu aşağıdaki
bağıntıdan hesaplanır.

BBij = Ej - Li - Dij

Buna göre aynı faaliyetin bağımsız boşluğu aşağıdaki gibi hesaplanır.

BB46 = BBD = 16 - 6 - 3 = 7 gün

*Emniyet Boşluğu*: Bir faaliyetin proje süresini uzatmadan ertelenebileceği en
uzun süreye emniyet boşluğu (EB) denir.

Emniyet boşluğunun toplam boşluktan farkı, (i, j) faaliyetinden önce gelen tüm
faaliyetlerin en geç bitirilme zamanlarında tamamlandıklarının varsayılmasıdır.
Aşağıdaki bağıntının kullanılmasıyla hesaplanır.

EBij = Lj - Li - Dij

Buna göre, diğer boşlukların hesaplanmasında dikkate alınan D faaliyetinin
emniyet boşluğu aşağıdaki gibi hesaplanır.

EB46 = 16 - 6 - 3 = 7 gün

Kritik yol yöntemi kullanımının son aşaması projenin kontrol edilmesidir. Bu
aşamada tüm faaliyetler ve faaliyetlerin belirlenmiş zamanlarının gözlenmesi ve
hazırlanan planla karşılaştırılması gerekir. Projenin programa göre
ilerlemediğinin ve bazı faaliyetlerin geciktiğinin belirlenmesi durumunda yeni
bir program geliştirmeye gerek duyulabilir. Bu durumda projenin o ana kadar
gerçekleştirilmiş faaliyetlerine sıfır süre konularak projenin
güncelleştirilmesi gerekir. Güncelleştirilme yardımıyla faaliyetlerin yeni
süreleri belirlenir. Yalnızca projenin ilerleyişindeki aksamalarda değil,
gelecekte projeye herhangi bir faaliyetin eklenmesi/çıkarılması gerektiğinde de
tüm değişikliklerin ağa yansıtılması gerekir. Proje kontrolü, kaynakların
kullanımı ve transferlerini de içerir. Mümkünse, hesaplanan boşluk değerlerine
göre faaliyetlere gerekli kaynak transferlerinin yapılması sağlanır.

### C. Zaman-Maliyet Analizi

CPM’de faaliyet sürelerinin faaliyetlerde kullanılan kaynak miktarıyla orantılı
olduğu kabul edilir. Genel olarak, herhangi bir faaliyete ayrılan kaynağın
(para, emek, malzeme, makine vb.) artırılması durumunda, faaliyetin süresi
kısaltılabilir. CPM terminolojisinde faaliyet süresinin kısaltılması veya
hızlandırılmasına "hızlandırma" denir. Faaliyetin hızlandırılması için
katlanılan yoğun kaynak kullanımının bir maliyeti vardır. Bu maliyete
"hızlandırma maliyeti" denir.

Bilindiği gibi, projenin tamamlanma süresi kritik yolun uzunluğuna eşittir ve
projenin tamamlanma süresi kritik faaliyetlerle belirlenir. Bu yüzden, projenin
tamamlanma süresi doğrudan doğruya kritik faaliyetlerin süreleri ile ilgilidir.
Bu nedenle, izlenmesi gereken faaliyetler kritik faaliyetlerdir. Kritik
faaliyetlerin hızlandırılması durumunda proje daha erken tamamlanır. Ancak
yukarıda açıklandığı gibi, faaliyetin hızlandırılması yönünde yapılacak
çalışmalar ek bir harcamayla gerçekleştirilir ki, her şeyden önce bu maliyetin
katlanmaya değer olup olmadığı belirlenmelidir. Bunun için, projenin daha kısa
sürede tamamlanmasının sağlayacağı avantajlar ile bu avantajları yakalayabilmek
için yapılan ek harcamalar arasında bir denge oluşturulması gerekir.

Bu denge noktasının bulunması, zaman-maliyet analizi ile gerçekleştirilir.
Zaman-maliyet analizinde amaç, daha yoğun kaynak kullanımının proje süresini
azaltıcı, süre azaltmanın bazı maliyet kalemlerini artırıcı etkilerini
dengeleyerek en düşük maliyete sahip proje planını gerçekleştirmektir.

Proje maliyeti, dolaylı ve dolaysız maliyetlerden oluşur. Dolaysız maliyetler,
faaliyetlerin gerçekleştirilmesindeki işçilik harcamaları, makine kiraları ve
malzeme maliyetlerinden oluşur. Dolaylı maliyetler ise, projenin idaresi ve
kontrolü, danışmanlık hizmetleri, seyahat, mukavele harcamaları gibi dolaylı
maliyetleri kapsar.

Projenin özelliğine göre başka maliyetler de tanımlanabilir. Sözgelimi proje,
belirli bir tip mamul üretmeye yönelik bir fabrikanın kurulması olsun. Fabrika
üretime geçmedikçe bu ürünün pazarlanması söz konusu olmayacaktır. Bu durumda,
her geçen zaman satılmayan birimden kaybedilen kâr cinsinden bir maliyet söz
konusu olacaktır.

Bazı tip projeler belirli protokollere dayalı olabilir. Bu tip projelerde
projenin protokolde belirtilen süreden daha geç bitirilmesi durumunda, geciken
her zaman birimi için bir ceza ödenmesi gerekebilir. Aynı şekilde, projenin
protokolde belirtilen süreden önce tamamlanması durumunda erken bitirme primi
verilebilir. Bu ve benzeri durumlar proje maliyetinin belirlenmesinde mutlaka
dikkate alınmalıdır.

Buna göre, projenin toplam maliyeti, faaliyet süreleri ile orantılı olan
dolaysız maliyetler ile proje süresi ile orantılı olan dolaylı maliyetlerin
toplamına eşittir. CPM esas olarak projenin toplam maliyeti ile onun tamamlanma
süresi arasında denge sağlanmasına yöneliktir. Kısaca, yöntemin esas amacı
projenin en kısa sürede ve en düşük maliyetle tamamlanmasını sağlamaktır.

Bir faaliyetin fazladan kaynak tahsis edilmeksizin tamamlanma süresine "normal
süre" denir. Normal süre aynı zamanda faaliyet için tanınan en uzun süredir.

Faaliyetin maksimum kaynak tahsisiyle tamamlanma süresine "hızlandırılmış süre"
denir. Hızlandırılmış süre, ilgili faaliyet için mümkün olan en kısa süredir.

Tanımlanan bu iki süre ve bunlara karşılık gelen maliyetler arasındaki ilişki
Şekil 4.60’da açıklanmıştır.

Söz konusu şekil incelendiğinde (i, j) faaliyeti için çizilen zaman-maliyet
eğrisinin (dolu çizgi ile çizilmiş), (i, j) faaliyetinin dolaysız maliyeti için
ayrılan bütçe ile bu bütçe sonucu ortaya çıkan faaliyet süresi arasındaki
ilişkiyi yansıttığı görülebilir.

Şekil 4.60

Eğrinin çizimi, biri normal diğeri hızlandırılmış olarak adlandırılan iki
noktaya dayanır. Normal nokta, faaliyetin normal koşullar altında herhangi bir
ek harcama yapılmaksızın tamamlanma süresi ile normal maliyeti verir.
Hızlandırılmış nokta, faaliyetin en fazla kaynak kullanımı ile tamamlanma süresi
ile hızlandırılmış maliyetini verir.

Genel bir yaklaşım olarak, bütün ara noktaların bu doğru parçası üzerinde
bulundukları kabul edilir. Bu nedenle her bir faaliyet için sadece bu iki
noktanın belirlenmesi yeterlidir. Projenin hızlandırılması ile ilgili
çalışmaları gerçekleştirebilmek için, her bir faaliyetin süre-maliyet
ilişkisinin saptanması gerekir.

Faaliyetlerin gerçek süre-maliyet ilişkisini hesaplamak çoğu zaman yorucu ve
zaman alıcı olabilmektedir. Süre maliyet ilişkisi duruma göre değişiklik
gösterir. İlişki, Şekil 4.60’da gösterildiği gibi doğrusal veya Şekil 4.61’de
gösterildiği gibi iç bükey ya da dış bükey olabilir.

İlişkinin iç bükey veya dış bükey olması durumunun açıklandığı Şekil 4.61
incelendiğinde, iç bükey bir ilişkide faaliyet süresindeki bir birimlik azalışın
K’ya kadar maliyette artan oranda artış, K’dan sonra azalan oranda artış
yarattığı görülecektir. Bunun tam tersi durum dış bükey ilişki için geçerlidir.
Dış bükey bir ilişkide faaliyet süresindeki bir birim azalış K noktasına kadar
toplam maliyette küçük bir artış meydana getirirken, K noktasından sonra artan
bir oranda artış gösterir.

Hesaplamalarda basitlik sağlamak için genellikle ilişkinin Şekil 4.60’da
açıklandığı gibi doğrusal ve sürekli olduğu varsayılır.

Şekil 4.61

Hangi faaliyetlerin ne kadar hızlandırılacağının belirlenmesinde, projenin
büyüklüğüne bağlı olarak;

1\. Sayma yöntemi

2\. Matematiksel programlama

olmak üzere iki yaklaşım söz konusu olur.

Projenin bu yaklaşımlarla süre-maliyet ilişkisini hesaplamak için her faaliyetin
zaman-maliyet eğrisinin hesaplanması, yani maliyet birim artışının elde edilmesi
gerekir. Normal ve hızlandırılmış noktalardaki maliyetler arasındaki farkın,
süreler arasındaki farka oranına "maliyet birim artışı" veya "maliyet eğimi"
denir. Maliyet birim artışı aşağıdaki formülle açıklanır.

Formüldeki semboller aşağıdaki gibi tanımlanır.

Dij = (i, j) faaliyetinin normal süresi

= (i, j) faaliyetinin normal (dolaysız) maliyeti

dij = (i, j) faaliyetinin hızlandırılmış süresi

= (i, j) faaliyetini hızlandırma (dolaysız) maliyeti

*Sayma Yöntemi*: Projeyi daha erken sürede tamamlamak için kritik faaliyetlerin
hızlandırılması esasına dayanan sayma yöntemi yalnızca küçük projelere
uygulanabilir. Yöntemin ilk aşamasında faaliyetlerin normal sürelerine göre
kritik yol hesaplanır ve projenin toplam maliyeti kaydedilir. Projenin
tamamlanma süresi kritik faaliyetlerin sürelerine bağlı olduğundan kritik
faaliyetlerin hızlandırılmasına geçilir.

Hızlandırma işlemine, maliyet artışı en küçük olan kritik faaliyetle başlanır.
Seçilen kritik faaliyet hızlandırılabildiği kadar hızlandırılmalı, yani mümkün
olan en kısa sürede tamamlanmalıdır. Kritik faaliyetler hızlandırıldıkça kritik
olmayan faaliyetlerin boşlukları azalır ve sonuçta yok olur. Böylece kritik
olmayan faaliyetler kritik hale gelirler ki bu, paralel kritik yolların
doğmasına neden olur. Bu nedenle, proje en erken tamamlanma süresinden daha kısa
sürede tamamlanmak istendiğinde paralel kritik yollardaki kritik faaliyetlerin
sayısı azalabilir. Herhangi bir kritik faaliyet veya faaliyetlerin
hızlandırılabilmeleri için, hızlandırma sonucu dolaysız maliyetlerde ortaya
çıkan artışın dolaylı maliyetlerdeki azalıştan küçük olması gerekir. Başlangıçta
olduğu gibi her seferinde dolaysız maliyetlerde en düşük artışa sebep olan
kritik faaliyet veya kritik faaliyetler seçilir. Paralel yol üzerindeki kritik
faaliyetler kritik olmadıkça, her adımda en az bir kritik faaliyet en kısa
süresinde tamamlanır.

Bu yöntemin uygulanmasındaki en büyük zorluk, kritik faaliyetlerin
hızlandırılması sonucunda kritik yolun değişmesi veya alternatif kritik yolların
ortaya çıkmasıdır.

Yöntemi bir örnekle açıklayalım.

Örnek 4.10: A, B, C, D, E faaliyetlerinin öncelik ilişkileri, her bir faaliyetin
normal ve hızlandırılmış süreleri ile bunlara karşılık gelen dolaysız maliyetler
aşağıdaki tabloda verilmiştir. Günlük dolaylı maliyet 100 TL’dir. Bu veriler
çerçevesinde zaman-maliyet analizini gerçekleştiriniz.

#### Tablo 4.11

|  Faaliyet | Önce Gelen  Faaliyet | Normal Süre | Hızlandırılmış Süre | Normal  Maliyet | Hızlandırılmış Maliyet | Maliyet Artışı |
|-----------|----------------------|-------------|---------------------|-----------------|------------------------|----------------|
| A         | -                    | 3           | 2                   | 300             | 350                    | 50             |
| B         | A                    | 4           | 2                   | 400             | 520                    | 60             |
| C         | A                    | 5           | 2                   | 500             | 650                    | 50             |
| D         | C                    | 1           | 1                   | 100             | 100                    | 0              |
| E         | B,D                  | 4           | 2                   | 400             | 530                    | 65             |

Çözüm 4.10: Yöntemin ilk aşaması faaliyetlerin normal sürelerinin dikkate
alınmasıyla kritik yolun belirlenmesidir. Kritik yolun belirlenebilmesi için
çizilen ağ ve kritik yol Şekil 4.62’de gösterilmiştir.

Şekil 4.62

Kritik yolun belirlenmesi için yapılan hesaplama sonuçları aşağıdaki tabloda
topluca gösterilmiştir.

#### Tablo 4.12

| Faaliyet | EBij | GBij | ETij | GTij | Fikir        |
|----------|------|------|------|------|--------------|
| A        | 0    | 0    | 3    | 3    | Kritik       |
| B        | 3    | 5    | 7    | 9    | Kritik Değil |
| C        | 3    | 3    | 8    | 8    | Kritik       |
| D        | 8    | 8    | 9    | 9    | Kritik       |
| E        | 9    | 9    | 13   | 13   | Kritik       |

Hesaplamalar projenin 13 günde tamamlanacağını göstermektedir. Tablonun son
sütununda açıklandığı gibi A, C, D ve E kritik faaliyetler olup, bütün
faaliyetler normal süreleri içinde tamamlandıklarında proje, en erken 13 günde
biter. Projeye ilişkin toplam maliyet aşağıdaki bağıntıdan hesaplanır.

Toplam Maliyet = Dolaylı Maliyet + Dolaysız Maliyet

Toplam Maliyet = 13 x 100 + 1700

= 3000 TL

Bütün faaliyetlerin mümkün olan en kısa süreye sıkıştırılmaları durumunda proje
en erken 7 günde tamamlanır. Bu durumun toplam maliyeti aynı bağıntının dikkate
alınmasıyla aşağıdaki gibi hesaplanır.

Toplam Maliyet = 7 x 100 + 2150

= 2850 TL

Proje yönetiminin amacı bu maliyeti en küçük yapacak proje programını
geliştirmektir. Normal süreli kritik yolun belirlenmesinden sonra, en küçük
maliyet eğimli kritik faaliyetin seçimi yapılır. Faaliyetlerin maliyet birim
artışları Tablo 4.11’un son sütununda gösterilmiştir.

Dolaysız maliyette en düşük artış sağlayan kritik faaliyet D olduğundan
hızlandırma işlemine bu faaliyetle başlanır. Ancak, D’nin normal süresi ile en
kısa süresi eşit olduklarından bu faaliyetin hızlandırılması söz konusu olamaz.

A’yı inceleyelim. Bu faaliyet hızlandırılarak 3 yerine 2 günde bitirilmek
istenirse proje 13 değil 12 günde tamamlanır. Projenin 1 gün erken
tamamlanmasıyla dolaylı maliyet 100 TL azalırken, dolaysız maliyet 50 TL artar.
Dolaylı maliyetteki azalış, dolaysız maliyetteki artıştan büyük olduğundan A’nın
sıkıştırılması kararlaştırılır. A’nın 1 gün hızlandırılmasıyla toplam maliyet
2950 TL olur. A’nın daha fazla sıkıştırılması söz konusu olmadığından diğer
faaliyetlere geçilir.

C’ye geçelim. C, 5 gün yerine 4 günde bitirilirse, dolaysız maliyet 50 TL
artarken dolaylı maliyet 100 TL azalır. Bu durumda toplam maliyetten 50 TL
tasarruf edileceğinden C 1 gün hızlandırılır. C’nin biraz daha hızlandırılarak 4
yerine 3 günde bitirilmek istendiğini düşünelim. C, 3 günde bitirildiğinde,
toplam maliyet 50 TL azalacağından C’nin 3 günde bitirilmesi uygun olur. C’nin 1
gün daha hızlandırılmasıyla toplam maliyet 50 TL azalarak 2850 TL olur. C, 3
günde bitirildiğinde orijinal kritik yola paralel başka bir kritik yol (A, B, E)
ortaya çıkar. Bu durumda, paralel kritik faaliyetlerin aynı anda
sıkıştırılmaları gerekir. B ve C aynı anda birer gün hızlandırılacak paralel
kritik faaliyetlerdir. B ve C’nin birer gün hızlandırılmasıyla dolaylı maliyette
sağlanan azalış, dolaysız maliyetteki artıştan büyük (110 \> 100) olduğundan C
ve B’nin sıkıştırılması uygun olmaz.

E’yi sıkıştıralım. E’nin 1 gün önce tamamlanması sonucunda toplam maliyetten 35
(100 - 65) TL tasarruf edileceğinden, E’nin 4 yerine 3 günde bitirilmesine karar
verilir. Projenin iki kritik yolu; A, C, D, E ve A, B, E yollarıdır. Bu durumda
projenin 9 günde toplam 2815 TL maliyetle tamamlanacağı kararlaştırılır. E’nin 1
gün daha hızlandırılıp hızlandırılamayacağını inceleyelim. E’nin 3 yerine 2
günde tamamlanması toplam maliyette 35 TL’lik bir azalış sağlayacağından bu
faaliyetin 1 gün daha sıkıştırılması uygun olur.

Daha fazla hızlandırma mümkün olmadığından, hızlandırma işlemlerine son verilir.
Hızlandırma sonucunda proje 2780 TL toplam maliyetle 8 günde tamamlanacaktır.
Sonuçta, A(2), B(4), C(3), D(1), E(2) olarak uygulanacaktır.

Büyük projelerde kritik yol sayısı genellikle birden fazladır ve kritik
faaliyetler çok sayıdadır. Bu gibi durumlarda paralel kritik yollardaki, kritik
faaliyetlerin sıkıştırılmasıyla ilgili tüm alternatiflerin göz önünde
bulundurulmaları çok zaman alıcı ve zor olabilmektedir. Sözgelimi, her biri 10
kritik faaliyet içeren iki kritik yol bulunduğunda mümkün hızlandırmalar için
100 farklı kombinasyonun dikkate alınması gerekir. Bu sayma yönteminin uygulama
alanını fazlasıyla sınırlandırılan bir durumdur.

*Matematiksel Programlama*: Yukarıda açıklandığı gibi, projenin boyutu büyüdükçe
sayma yönteminin etkinliği azalır. Bu gibi durumlarda matematiksel programlama
yöntemlerinden birinin uygulanması akılcı olur. Bu bölümde, CPM için önerilen
bazı matematiksel programlama yöntemleri açıklanacaktır. Açıklanacak yöntemlerin
hepsi faaliyetlerin her birinin süre-maliyet ilişkisinin bilinmesini gerektiren
yöntemlerdir.

Doğrusal programlama modellemesi için öncelikle karar değişkenleri
tanımlanmalıdır. Amaç, en düşük maliyetli proje süresinin belirlenmesi olduğuna
göre, her bir faaliyet için bir karar değişkeni tanımlanması gerekir. (i, j)
projenin herhangi bir faaliyeti olsun. (i, j)’ye karşılık gelen karar değişkeni,
bu faaliyetin en iyi süresi olmak üzere yij ile gösterilir.

Modelin geliştirilebilmesi için olayların bilinmeyen gerçekleşme zamanları da
tanımlanmalıdır. Projenin ilk olayı 1, son olayı n olmak üzere olayların
gerçekleşme zamanları; ti (i = 1, 2, ..., n) olarak açıklanır. Şimdi modelleri
açıklamaya başlayabiliriz.

*Model I*: T zaman birimi içerisinde tamamlanması gereken bir projede
hızlandırma sonucu ortaya çıkan toplam maliyetin en küçük olmasını sağlayacak
hızlandırma planı belirlenmek istendiğinde, aşağıda gösterilen doğrusal
programlama modeli kullanılabilir. Bu model simpleks yöntemle çözülebilir. Çözüm
sonucu, en büyük hızlandırmayı sağlayan en düşük hızlandırma maliyeti (Z) elde
edilir. yij’lerin en iyi çözüm değerleri en düşük maliyeti sağlayan hızlandırma
planında beliren faaliyet süreleridir.

Zenk =

tj - ti yij bütün (i, j) faaliyetleri için

dij yij Dij bütün (i, j) faaliyetleri için

tn - t1 T

ti 0 i = 1, 2, ..., n için

Bu yaklaşımla belirlenen en iyi çözümün geçerli olması için T’nin, faaliyetlerin
en kısa süreleriyle belirlenecek olan kritik yolun uzunluğuna eşit veya daha
büyük olması gerekir.

*Model II*: Faaliyetlerin hızlandırılmaları için B birim ek bütçe ayrıldığını
düşünelim. Bu ek bütçe ile yaratılan ek kaynakların faaliyetler arasında proje
süresini en küçükleyecek biçimde paylaştırılması istenebilir.

Bu duruma uygun düşen doğrusal programlama modeli aşağıda gösterilmiştir.

Zenk = tn - t1

tj - ti yij bütün (i, j) faaliyetleri için

dij yij Dij bütün (i, j) faaliyetleri için

B

ti 0 i = 1, 2, 3, ..., n

Bu modelin simpleks yöntemle çözülmesi sonucunda, ek bütçe kullanılmasıyla
projenin tamamlanabileceği en kısa süre, bu bütçe ile sıkıştırılan faaliyetler
ve faaliyetlerin en kısa süreleri belirlenir.

Model I ve Model II’nin kullanılmasıyla proje süresi ve toplam hızlandırma
maliyeti arasındaki ilişkinin şekli belirlenebilir. Proje süresi ile dolaysız
maliyetler arasındaki ilişki Şekil 4.63’de gösterilmiştir. Yatay eksendeki Tenk
bütün faaliyetlerin en kısa sürelerinde tamamlanmaları durumunda projenin
tamamlanma süresini, Tenb ise bütün faaliyetlerin normal sürelerinde
bitirilmeleri durumunda projenin tamamlanma süresini göstermektedir.

Şekil 4.63’deki eğri yardımıyla yönetici, 1. Projenin planlanan zamanda
tamamlanması için gerekli ek kaynakların en küçük maliyetini, 2. Kıt
kaynakların, proje süresinde en büyük hızlandırılmayı sağlayacak biçimde
paylaştırılmasını sağlayabilir. Şekil 4.63’de açıklandığı gibi Tenk’de toplam
dolaysız maliyet en büyüktür. Proje süresi uzadıkça bu maliyet önce hızlı sonra
yavaş bir biçimde azalmaktadır.

Şekil 4.63

Daha önce açıklandığı gibi proje süresinin kısalması, dolaylı maliyetlerin
azalması demektir. Bu nedenle, proje süresine bağlı olarak toplam proje
maliyetinin (dolaylı + dolaysız) nasıl değiştiğinin incelenmesi istenebilir.
Değişik proje süreleri için dolaylı ve dolaysız maliyetlerin eklenmesiyle Şekil
4.64’deki gibi bir görüntü elde edilir.

Şekil 4.64

Şekil 4.64’deki U biçimli eğriye "proje maliyet eğrisi" denir. Bu eğri
yardımıyla toplam maliyeti en küçükleyen proje süresinin (T\*) belirlenmesi çok
kolaydır. T’nin en iyi değeriyle bütün faaliyetlerin en iyi süreleri,
hızlandırma maliyeti ve kritik yol belirlenir. Bu bilgilerle en iyi proje
programı düzenlenir.

*Model III*: Dolaylı maliyetler ile proje süresi arasındaki ilişkinin doğrusal
olması durumunda doğrusal programlama ile proje için en iyi süre (T\*) ile en
iyi proje programı belirlenebilir. Proje süresi ile orantılı dolaylı maliyetler,
birim zamanda F olsun. Bu durumda dolaylı maliyet toplamı F(tn - t1 ) olur.
Burada; (tn - t1) projenin bilinmeyen uzunluğudur. (i, j) faaliyetinin
bilinmeyen tamamlanma süresi yij olmak üzere toplam dolaysız maliyet, olarak
açıklanır. Amaç dolaylı ve dolaysız maliyetler toplamı olarak belirlenen toplam
maliyetin en küçüklenmesidir. Bu amaçla kullanılacak doğrusal programlama modeli
aşağıda gösterilmiştir.

Zenk = F(tn - t1) +

tj - ti yij bütün (i, j) faaliyetleri için

dij yij Dij bütün (i, j) faaliyetleri için

ti 0 i = 1, 2, ..., n için

Model III’ü, sayma yöntemiyle çözdüğümüz örnek probleme uygulayalım.

Örnek 4.11: Örnek 4.10’daki problemi doğrusal programlamayla çözünüz.

Çözüm 4.11: (i, j) faaliyetinin tamamlanma süresi yij, i olayının ortaya çıkma
zamanı ti olsun. Bu durumda, 5 olaylı bu projenin tamamlanma süresi (t5 - t1)
olur.

Dolaylı maliyetin 100 TL olduğu göz önünde bulundurulduğunda, toplam dolaylı
maliyet 100(t5 - t1) olarak hesaplanır.

Buna göre yöneticinin problemi aşağıdaki gibi formüllenir.

Zenk = 100(t5 - t1) + 50(3 - y12) + 50(5 - y23) + 60(4 - y24) + 0(1 - y34) +
65(4 - y45)

t2 - t1 y12 t3 - t2 y23 t4 - t2 y24 t4 - t3 y34 t5 - t4 y45

2 y12 3 2 y23 5 2 y24 4 1 y34 1 2 y45 4

t1, t2, t3, t4, t5 0

Problemin simpleks yöntemle belirlenen en iyi çözümü şöyledir:

t1 = 0, t2 = 2, t3 = 5, t4 = 6, t5 = 8; y12 = 2, y23 = 3, y24 = 4, y34 = 1, y45
= 2; Zenk = 2780

Özetle, en iyi süre (t5) 8 gün, projenin en düşük maliyeti 2780 TL’dir. Sayma
yöntemiyle de aynı sonuca ulaşıldığı hatırlanabilir.

### 4.6.2.2. PERT Yöntemi

CPM’de sürelerin kesin olarak bilindiği, ayrıca faaliyetlere ayrılan kaynak
miktarlarının değişmesi durumunda faaliyet sürelerinin de değişebileceği kabul
edilmektedir. Oysa, araştırma ve geliştirme projelerinin her biri özel projeler
olup bu projelerdeki faaliyetlerin pek çoğu yalnızca bir kez
gerçekleştirildiğinden, benzer faaliyetlerden süre ile ilgili önsel bilgiler
elde edilemez. Bu tür projelerin yönetimi faaliyetlerin tamamlanma sürelerindeki
belirsizlikleri dikkate alan PERT tekniği ile gerçekleştirilir.

PERT’de faaliyetlerin tamamlanma süreleri ile değil, bunların beklenen değerleri
(E(Dij)) ile işlem yapılır. Bir başka deyişle, faaliyet sürelerinin rasgele
değişkenler oldukları ve bir olasılık dağılımına göre ortaya çıktıkları
varsayılır. Herhangi bir faaliyetin beklenen tamamlanma süresi, faaliyetin %50
olasılıkla tamamlanacağı süre demektir. Bu sürenin belirlenebilmesi için her bir
faaliyete ilişkin üç ayrı tamamlanma süresinin tahmin edilmesi gerekir. Bu
süreler aşağıda açıklanmışlardır.

1\. *İyimser Süre* (a): Faaliyetin en erken tamamlanacağı süredir. Bu sürenin
tahmininde bütün herşeyin planlandığı gibi gideceği, bütün etmenlerin faaliyeti
iyi yönde etkileyecekleri kabul edilir. İyimser tahminin gerçekleşmesi olasılığı
%1’dir.

2\. *Kötümser Süre* (b): Faaliyetin en geç tamamlanma süresidir. Bu sürenin
tahmininde hiçbir şeyin planlandığı gibi gitmeyeceği, beklenmedik
olayların(mekanik arıza, kaynak temininde aksama, kötü hava koşulları gibi)
faaliyete kötü yönde etki edeceği varsayılır.

3\. *Olabilir Süre* (m): Varsa daha önceki uygulamalardan elde edilen önsel
bilgilerin veya tahmin çalışmaları sonuçlarının kullanılmasıyla normal koşullar
altında faaliyetin tamamlanacağı süreye en yüksek olasılıkla tamamlanma süresi
veya olabilir süre denir. Olabilir süre en gerçekçi süredir.

Faaliyetin tamamlanma süresinin iyimser tahmin ile kötümser tahmin tarafından
belirlenen aralığın dışında olabileceği gözden uzak tutulmamalıdır. Olabilir
süre kesinlikle a ile b aralığında bulunacak olmakla birlikte, (a + b)/2 ile
çakışmak zorunda değildir. m, (a + b)/2 ile belirlenen değerin solunda veya
sağında olabileceği gibi (a + b)/2 ile çakışabilir. Bu özellikten dolayı, (i, j)
faaliyetinin tamamlanma süresi Dij rasgele değişkeninin modu m, alt uç noktası
a, üst uç noktası b olan beta dağılımı gösterdiği varsayılır. a, b ve m
değerlerinin tahmin edilmesinden sonra bu üç sürenin tek bir değer olarak ifade
edilmesi gerekir. (a + b)/2’nin ağırlığı m’nin ağırlığının yarısına eşittir.

#### Şekil 4.65

Bu varsayım altında Dij’nin ortalaması aşağıdaki gibi hesaplanacaktır.

Faaliyetin tamamlanma süresi, ortalama tamamlanma süresinden farklı
olabileceğinden, bu süreye ilişkin varyansın da hesaplanması gerekir. Tek modlu
dağılımların pek çoğunda, uç değerler dağılımın ortalamasından yaklaşık 3
standart sapma uzaklıkta bulunurlar. Bu durumda, 6 = b - a veya = yazılabilir.
Bu bağıntıdan hareketle (i, j) faaliyetinin süresine ilişkin varyans aşağıdaki
gibi elde edilir.

Faaliyet sürelerinin beta dağıldıkları varsayımına ek olarak, anılan sürelerin
birbirinden bağımsız rasgele değişken oldukları kabul edildiğinden, proje
ağındaki herhangi bir yolun tamamlanma süresi de rasgele değişken olur ve bu
değişkenin ortalaması aşağıdaki gibi hesaplanır.

**Herhangi bir yoldaki faaliyetlerin beklenen tamamlanma süresi =**

Benzer yaklaşımla herhangi bir yolun varyansı da şu şekilde hesaplanır:

**Herhangi bir yoldaki faaliyet sürelerinin varyansı =**

Her faaliyetin ortalama süresi ile varyansının hesaplanmasından sonra, CPM
uygulamasına geçilir ve kritik yol belirlenir.

İstenirse projenin herhangi bir zaman süresinden önce veya bu süre içinde
tamamlanma olasılığı hesaplanabilir. Bunun için, kritik yolu oluşturan
faaliyetlerin sayısının kritik yolun normal dağılımlı olmasını sağlayacak
büyüklükte olduğu kabul edilir. Bunun sonucunda; projenin belirli veya öngörülen
zamanda tamamlanma olasılığı ile ilgili sorular kolayca yanıtlanabilir. Bu
amaçla, öngörülen veya dikkate alınan süre T olmak üzere standart normal olarak
adlandırılan bir değişken tanımlanır. Standart normal değişken, genel olarak
aşağıdaki gibi açıklanır.

Z =

Z ile gösterilen bu değişken; ortalaması sıfır, varyansı 1 olan standart normal
değişkendir. Hesaplamaları kolaylaştırmak amacıyla, çeşitli Z değerleri için
normal eğri alanları tablolarından yararlanılmaktadır.

Birden fazla kritik yol olduğunda olasılık hesaplamalarında varyansı büyük olan
kritik yolu dikkate almak gibi bir eğilim vardır. Bu konuda benimsenen diğer bir
yaklaşım ise, projenin beklenenden geç tamamlanması ile ilgili olasılıkların
hesaplanmasında en büyük varyansı, beklenenden daha kısa sürede tamamlanmasıyla
ilgili olasılıklarda en küçük varyansı dikkate almaktır. Böylece ulaşılan
sonuçların daha güvenilir olması sağlanır.

**Örnek 4.12**: Faaliyetlerin öncelik ilişkileri ve tahmini süreleri (a, m, b)
aşağıdaki tabloda verilmiştir. Buna göre,

**a**. Projenin ağını çiziniz.

**b**. Kritik yolu belirleyiniz ve kritik yolun varyansını hesaplayınız.

**c**. Projenin 39 günden önce tamamlanma olasılığını bulunuz.

**d**. Projenin 42 günden önce tamamlanma olasılığını hesaplayınız.

#### Tablo 4.13

|  Faaliyet | Önceki Faaliyet | İyimser   Süre (a) | Olabilir Süre (m) | Kötümser Süre (b) |
|-----------|-----------------|--------------------|-------------------|-------------------|
| A         | -               | 5                  | 6                 | 9                 |
| B         | A               | 8                  | 10                | 14                |
| C         | A               | 4                  | 5                 | 7                 |
| D         | A               | 6                  | 8                 | 10                |
| E         | B, C            | 10                 | 12                | 14                |
| F         | B, C            | 4                  | 6                 | 8                 |
| G         | B               | 3                  | 5                 | 7                 |
| H         | B               | 6                  | 8                 | 10                |
| I         | G, D, E         | 5                  | 7                 | 8                 |
| J         | H, I, F         | 3                  | 5                 | 7                 |

**Çözüm 4.12**: **a**. Verilere göre çizilen proje ağı aşağıda gösterilmiştir.

Şekil 4.66

**b**. Kritik yolun belirlenmesi için her faaliyetin ortalama süresinin
hesaplanması gerekir.

Faaliyetlerin ortalama süreleri,

E(Dij) =

bağıntısından hesaplanmış ve Tablo 4.14’ün beşinci sütununda gösterilmiştir.

Olasılık hesaplamalarında kullanılacak varyans değerleri ise,

bağıntısından hesaplanmış ve aynı tablonun son sütununda verilmiştir.

**Tablo 4.14**

| Faaliyet   | a  | m  | b  | Ortalama | Varyans |
|------------|----|----|----|----------|---------|
| A          | 5  | 6  |  9 |  6.333   | 0.444   |
| B          | 8  | 10 | 14 | 10.333   | 1.000   |
| C          | 4  | 5  |  7 |  5.167   | 0.250   |
| D          | 6  | 8  | 10 |  8.000   | 0.444   |
| E          | 10 | 12 | 14 | 12.000   | 0.444   |
| F          | 4  | 6  |  8 |  6.000   | 0.444   |
| G          | 3  | 5  |  7 |  5.000   | 0.444   |
| H          | 6  | 8  | 10 |  8.000   | 0.444   |
| I          | 5  | 7  |  8 |  6.833   | 0.250   |
| J          | 3  | 5  |  7 | 5.000    | 0.444   |
| K (Kukla)  | 0  | 0  |  0 | 0.000    | 0.000   |

Kritik yolun belirlenmesi için yapılan işlem sonuçları Tablo 4.15’de
gösterilmiştir.

**Tablo 4.15**

|  Faaliyet  |  EBij  |  GBij  |  ETij  |  GTij  | Boşluk GBij - EBij |
|------------|--------|--------|--------|--------|--------------------|
| A          | 0      | 0      | 6.333  | 6.333  | Kritik             |
| B          | 6.333  | 6.333  | 16.667 | 16.667 | **Kritik**         |
| C          | 6.333  | 11.500 | 11.500 | 16.667 | 5.167              |
| D          | 6.333  | 20.667 | 14.333 | 28.667 | 14.333             |
| E          | 16.667 | 16.667 | 28.667 | 28.667 | Kritik             |
| F          | 16.667 | 29.500 | 22.667 | 35.500 | 12.833             |
| G          | 16.667 | 23.667 | 21.667 | 28.667 | 7.000              |
| H          | 16.667 | 27.500 | 24.667 | 35.500 | 10.833             |
| I          | 28.667 | 28.667 | 35.500 | 35.500 | Kritik             |
| J          | 35.500 | 35.500 | 40.500 | 40.500 | **Kritik**         |
| K (Kukla)  | 16.667 | 16.667 | 16.667 | 16.667 | Kritik             |

Hesaplamalar kritik yolun; A, B, E, I, J ve K faaliyetlerinden oluştuğunu ve
projenin 40.5 günde tamamlanacağını göstermektedir. Kritik yolun varyansı kritik
faaliyetlerin varyanslarının dikkate alınmasıyla,

V(KY) = 0.444 + 1.000 + 0.444 + 0.250 + 0.444 + 0.000 = 2.582

olarak hesaplanmıştır.

**c**. Kritik yolun uzunluğunun standartlaştırılmasıyla istenilen olasılık
değeri aşağıdaki gibi hesaplanacaktır.

P(KY 39) =

Şekil 4.67’de gösterildiği gibi Z = - 0.933, normal eğri altında ortalamanın sol
tarafındadır. Normal dağılım tablosundan aranılan olasılık değeri 0.1762 olarak
saptanır. Buna göre projenin 39 gün içerisinde tamamlanma olasılığı yaklaşık %18
olarak belirlenmiş olur.

P(Z -0.933)

\-0.933

Z

0

#### Şekil 4.67

**d**. Şekil 4.68’de gösterildiği gibi Z = 0.933’ün solundaki alan
sorulmaktadır.

P(Z 0.933)

Z

0.933

0

#### Şekil 4.68

Buna göre, aranılan olasılık değeri aşağıdaki gibi elde edilir.

P(KY 42) =

= 0.8238

Buna göre, projenin en geç 42 günde tamamlanma olasılığı yaklaşık %82’dir.

#### 

#### PROBLEMLER

1\. k ile v’yi birbirine bağlayan yolların taşıma kapasiteleri (otomobil/saat)
aşağıda gösterilmiştir.

1.  k ve v’yi birleştiren alternatif yolları listeleyiniz.

2.  Alternatif kesmeleri ve kapasitelerini bulunuz.

3.  Etiketleme yöntemiyle en yüksek akış planını belirleyiniz.

2\. k ile v’yi birleştiren yollar ve yolların trafik kapasiteleri aşağıda
gösterilmiştir. Şekilden görüldüğü gibi yönü belirsiz üç yol vardır. Bu
yollardaki trafik akış yönünü, en yüksek akışı sağlayacak biçimde belirleyiniz.

3\. Bir işletme üç fabrikasında üretim yapmakta ve üretimini 4 ayrı deposuna
göndermektedir. Fabrikaların üretimi ile depoların istem miktarları aşağıdaki
tabloda verilmiştir. Bu problemin aynı zamanda bir en yüksek akış problemi
olduğunu gösteriniz ve en yüksek akışı bularak sonucu yorumlayınız.

|         | Depo |      |      |     |        |
|---------|------|------|------|-----|--------|
| Fabrika | D1   | D2   | D3   | D4  | Toplam |
| F1      |  130 |  110 |  0   | 140 | 120    |
| F2      |  0   |  0   |  110 |  50 | 120    |
| F3      |  120 |  110 |  140 |  5  | 200    |
| Toplam  | 120  | 120  | 160  |  40 | -      |

4\. 5 kadın, 5 erkek bir dansta buluşmuşlardır. Dansı düzenleyenlerin amacı bu
kadın ve erkeklerden en fazla sayıda alternatif uygun çift yaratmaktır. Uygun
çiftler tabloda U ile gösterilmiştir. Tabloya uyan ağı çizerek uygun çift
sayısını ve uygun çiftleri belirleyiniz.

|        | Tarkan | Ozan | Cihan | Emre | Ali |
|--------|--------|------|-------|------|-----|
| Deniz  | -      | U    | -     | -    | -   |
| Demet  | U      | -    | -     | U    | -   |
| Yıldız | U      | U    | -     | -    | -   |
| Esin   | U      | U    | -     | -    | U   |
| Zeynep | -      | -    | U     | -    | U   |

5\. Küçük bir tamirhane sahibi işi için gerekli yontma makinesinin gelecek beş
yıl içindeki yenileme planını çıkarmak istemektedir. Makinenin yıllık
bakım-onarım masrafı makinenin incelenen yılın başındaki yaşına bağlı olup
aşağıdaki gibidir. Yaşa bağlı olarak her yıl biraz daha artan bakım-onarım
masraflarından kurtulmak için eskiyen makinenin satılarak yerine yenisinin
alınması mümkündür. Eskimiş makinenin satış fiyatı satıldığı yılın başındaki
yaşına bağlı olup aşağıda gösterildiği gibidir. Hesaplamalarda basitlik sağlamak
için makine yenileme maliyetinin planlama dönemi boyunca sabit kaldığı ve 25 TL
olduğu kabul edilmiştir. Buna göre 5 yıllık planlama dönemi için en iyi araç
yenileme programını oluşturunuz.

| Makinenin  Yaşı | Bakım  Masrafı | Satış Fiyatı |
|-----------------|----------------|--------------|
| 0               | 3              | -            |
| 1               | 4              | 20           |
| 2               | 6              | 15           |
| 3               | 8              | 10           |
| 4               | 12             |  7           |
| 5               | -              | 2            |

6\. Bir makine atölyesinde gelecek yedi yıl için bir araca gereksinim vardır.
Araç satın alma maliyeti 28 TL’dir. Bu maliyetin yedi yıllık planlama dönemi
boyunca değişmediği kabul edilmektedir. Aracın ömrü 3 yıl olup üçüncü yılın
sonunda kullanılmaz hale gelmektedir. Aracın yıllık bakım-onarım masrafı aracın
incelenen yılın başındaki yaşına bağlı olup aşağıdaki tabloda gösterildiği
gibidir. Makinenin yaşına bağlı olarak her yıl biraz daha artan bakım-onarım
masraflarından kurtulmak için eskiyen aracın satılarak yerine yenisinin alınması
da mümkündür. Eskiyen aracın hurda fiyatı satıldığı yıldaki yaşına bağlı olup
aşağıda gösterildiği gibidir. Buna göre 7 yıllık planlama dönemi için en iyi
araç yenileme programını oluşturunuz.

| Makinenin  Yaşı | Bakım  Masrafı | Hurda Fiyatı |
|-----------------|----------------|--------------|
| 0               | 3              | -            |
| 1               | 4              | 20           |
| 2               | 6              | 15           |
| 3               | 8              | 10           |

7\. Boy, kalınlık ve sayıları aşağıdaki tabloda verilen 450 kitabın
yerleştirileceği raf sistemi planlanmaktadır. Tek bir kitabın yerleştirilmesi
için gerekli raf alanı, kitabın boyu ile kalınlığının çarpımına eşittir. Raf
yapımında kullanılacak olan çelik levhanın 1 cm2’sinin maliyeti 3 TL’dir. Sabit
maliyet 46 TL’dir. En düşük maliyetli raf planını belirleyiniz.

| Boy | Kalınlık | Sayı |
|-----|----------|------|
| 20  | 1        | 100  |
| 23  | 3        | 150  |
| 30  | 6        | 125  |
| 34  | 5        | 75   |

8\. Aşağıdaki ağın 1 ve 5 nolu düğümler arasındaki en kısa yolu bulunuz.

9\. Dallarının uzunlukları; d12 = 5, d13 = 3, d14 = 7, d23 = 4, d34 = 2, d35 =
10, d36 = 9, d46 = 3, d56 = 3, d57 = 4, d67 = 9, d68 = 8 ve d78 = 6 olan bir
ağda 1 ve 8 nolu düğümler arasındaki en kısa yolu bulunuz.

10\. 5 ayrı yerleşim merkezi arasındaki uzaklıklar aşağıdaki tabloda
gösterilmiştir. Tüm merkezleri birbirine bağlayan otoyol planını oluşturunuz.

| Y. M. | 1   | 2   | 3   | 4   | 5   |
|-------|-----|-----|-----|-----|-----|
| 1     | -   | 232 | 150 | 46  | 155 |
| 2     | 232 | -   | 310 | 290 | 201 |
| 3     | 150 | 310 | -   | 101 | 213 |
| 4     |  46 | 290 | 101 | -   |  79 |
| 5     | 155 | 201 | 213 |  79 | -   |

11\. Aşağıdaki ağı göz önünde bulundurarak en küçük yayılmalı ağacı önce 2 sonra
4 nolu düğümden başlayarak belirleyiniz.

12\. Aşağıdaki faaliyetlerden oluşan projenin ağını çiziniz.

| Faaliyet | Önceki Faaliyet |
|----------|-----------------|
| A        | -               |
| B        | A               |
| C        | A               |
| D        | B, C            |
| E        | C               |
| F        | D               |
| G        | E, F            |

Öncelik ilişkileri tabloda verilen faaliyetlerin süreleri A(8), B(10), C(10),
D(5), E(7), F(13), G(2) olarak verilmiştir. Kritik yolu bulunuz ve tüm
boşlukları hesaplayınız.

13\. Aşağıdaki öncelik kurallarını sağlayan faaliyetlerin oluşturduğu projeye
ilişkin ağı çiziniz.

-   A projenin ilk faaliyetidir.

-   B ve C, A’dan sonra gelir.

-   D, B’yi izler.

-   E ve F, C’den sonra gelirler.

-   G, D ve E faaliyetlerinden sonra gelir.

-   H, F’yi izler.

-   I, G ve H’dan sonra gelir.

-   J, G ve H’ı izler.

-   K, I’dan sonra gelir.

-   L, J’den sonra gelir. K ve L projenin son faaliyetleridir.

14\. Verileri aşağıdaki tabloda verilen projeye ilişkin ağı çiziniz.

| Faaliyet | Önceki Faaliyet |
|----------|-----------------|
| A        | -               |
| B        | A               |
| C        | A               |
| D        | B               |
| E        | B               |
| F        | B               |
| G        | E               |
| H        | D, E            |
| I        | G               |
| J        | G               |
| K        | F, J            |
| L        | H, I            |
| M        | L, K            |
| N        | M, C            |

15\. Aşağıdaki 11 faaliyetten oluşan proje ağını çiziniz.

| Faaliyet Tanımı                                            | Önc. Faaliyet |
|------------------------------------------------------------|---------------|
| A: Reklam planının geliştirilmesi                          | -             |
| B: Promosyon ve eğitim malzemelerinin geliştirilmesi       | -             |
| C: Eğitim planının geliştirlmesi                           | -             |
| D: Radyo, TV, gazete reklamlarının programlanması          | A             |
| E: Reklam kampanyasının geliştirilmesi                     | A             |
| F: Promosyon materyallerinin hazırlanması                  | B             |
| G: Eğitim materyallerinin hazırlanması                     | B             |
| H: Reklam koordinatörleriyle ön görüşme                    | D, K          |
| I: Eğitime katılacak yöneticilerin araştırılması ve seçimi | C             |
| K: Eğitim programını harekete geçirme                      | G, I          |
| L: 1000 kişi üzerinde görüşme                              | F, H          |

16\. Projeyi oluşturan 8 faaliyetin öncelik ilişkileri, tanımları ve tamamlanma
süreleri aşağıda gösterilmiştir.

Buna göre,

1.  Proje ağını çiziniz.

2.  Kritik yolu bulunuz.

3.  Boşlukları hesaplayınız

4.  Boşluk değerlerini yorumlayınız.

| Faaliyet | Kısa Tanım              | Önceki Faaliyet | Süre |
|----------|-------------------------|-----------------|------|
| A        | Ürün Tasarımı           | -               | 6    |
| B        | Pazar Araştırması       | -               | 5    |
| C        | Hammade Siparişi        | A               | 3    |
| D        | Hammadde Tedariki       | C               | 2    |
| E        | Örnek Ürün Üretimi      | A, D            | 3    |
| F        | Reklam Kampanyası       | B               | 2    |
| G        | Üretimin Başlaması      | E               | 4    |
| H        | Ürünün Satışa Sunulması | G, F            | 2    |

17\. Aşağıdaki ağın hatalarını bularak nedenleriyle açıklayınız.

18\. Bir projenin faaliyetleri ve bunlar arasındaki öncelik ilişkileri ile
faaliyet süreleri aşağıda gösterilmiştir. Kritik yolu bulunuz.

| Faaliyet | Önceki Faaliyet | Süre |
|----------|-----------------|------|
| A        | -               | 8    |
| B        | -               | 2    |
| C        | A               | 1    |
| D        | B               | 9    |
| E        | B               | 4    |
| F        | C, D            | 5    |
| G        | E               | 6    |
| H        | E               | 3    |
| I        | G               | 3    |
| J        | H               | 5    |
| K        | I, J            | 2    |

19\. Projeyi oluşturan faaliyetler arasındaki öncelik kuralları ve faaliyet
süresi tahminleri aşağıdaki tabloda verilmiştir.

|  Faaliyet | Önceki  Faaliyet | İyimser Süre (a) | Olabilir Süre (m) | Kötümser Süre (b) |
|-----------|------------------|------------------|-------------------|-------------------|
| A         | -                | 2                | 4                 | 6                 |
| B         | A                | 2                | 5                 | 8                 |
| C         | A                | 2                | 4                 | 6                 |
| D         | B                | 12               | 13                | 16                |
| E         | B                | 10               | 13                | 17                |
| F         | C                | 4                | 6                 | 8                 |
| G         | E                | 10               | 15                | 20                |
| H         | D, F             | 3                | 5                 | 10                |
| I         | G, H             | 2                | 4                 | 7                 |

1.  Kritik yolu bulunuz ve standart sapmasını hesaplayınız.

2.  Projenin 20 günde tamamlanma olasılığını hesaplayınız.

    1.  Kritik olmayan herhangi bir yol tanımlayarak bu yolun standart sapmasını
        hesaplayınız.

    2.  Standart sapmasını hesapladığınız kritik olmayan yolun 13 günde
        tamamlanması olasılığını bulunuz.

20\. Faaliyetlerin öncelik ilişkileri ve tahmini süreler aşağıda verilmiştir.
Projenin en geç 30 gün içerisinde tamamlanması olasılığını bulunuz.

| Faaliyet | Önceki Faaliyet | a   | m | b  |
|----------|-----------------|-----|---|----|
| A        | -               | 0.5 | 1 | 2  |
| B        | A               | 1   | 2 | 3  |
| C        | A               | 1   | 3 | 5  |
| D        | B               | 3   | 4 | 5  |
| E        | C               | 2   | 3 | 4  |
| F        | C               | 3   | 5 | 7  |
| G        | D, E            | 4   | 5 | 6  |
| H        | F               | 6   | 7 | 8  |
| I        | G, H            | 2   | 4 | 6  |
| J        | G, H            | 5   | 6 | 8  |
| K        | I               | 1   | 2 | 3  |
| L        | J               | 3   | 5 | 7  |
| M        | I, J            | 7   | 9 | 10 |
| N        | I, J            | 2   | 3 | 4  |

21\. Projeyi oluşturan 11 faaliyet arasındaki öncelik kuralları ve faaliyet
süresi tahminleri aşağıdaki tabloda verilmiştir.

|  Faaliyet | Önce Gelen  Faaliyet | İyimser Süre (a) | Olabilir Süre (m) | Kötümser Süre (b) |
|-----------|----------------------|------------------|-------------------|-------------------|
|  A        | -                    | 3                | 6                 | 9                 |
| B         | -                    | 2                | 5                 | 8                 |
| C         | A                    | 2                | 4                 | 6                 |
| D         | B                    | 2                | 3                 | 10                |
| E         | B                    | 1                | 3                 | 11                |
| F         | C, D                 | 4                | 6                 | 8                 |
| G         | E, C                 | 1                | 5                 | 15                |
| H         | E                    | 3                | 5                 | 7                 |
| I         | G                    | 2                | 6                 | 10                |
| J         | I, H                 | 4                | 5                 | 6                 |
| L         | J                    | 5                | 7                 | 9                 |

1.  Kritik yolu bulunuz ve boşlukları hesaplayınız.

2.  Projenin 18 günde tamamlanması olasılığını hesaplayınız.

3.  B-E-H-J-L yolunun 18 günde tamamlanması olasılığını bulunuz.

22\. 14 faaliyetin normal ve sıkıştırılmış süreleri ile bu sürelere ilişkin
dolaysız maliyetler aşağıda gösterilmiştir. Haftalık dolaylı maliyet 40 TL
olduğuna göre en düşük maliyetli proje programını oluşturunuz.

|  Faaliyet | Önceki  Faaliyet | Normal  Süre | Hızlandırılmış Süre | Normal  Maliyet | Hızlandırılmış  Maliyet |
|-----------|------------------|--------------|---------------------|-----------------|-------------------------|
| A         | -                | 10           |  8                  | 120             | 180                     |
| B         | A                |  5           |  3                  |  50             |  80                     |
| C         | A                |  8           |  7                  | 110             | 135                     |
| D         | B                | 14           | 12                  | 120             | 140                     |
| E         | D                |  8           |  5                  |  70             | 110                     |
| F         | D                | 10           | 2                   | 100             | 180                     |
| G         | D                | 9            | 6                   | 120             | 180                     |
| H         | B                | 4            | 1                   | 100             | 400                     |
| I         | C, E             | 7            | 3                   | 40              | 60                      |
| J         | G, H             | 8            | 1                   | 400             | 640                     |
| K         | F, I, J          | 3            | 2                   | 75              | 100                     |
| L         | K                | 9            | 7                   | 900             | 960                     |
| M         | H, G             | 5            | 2                   | 60              | 120                     |
| N         | M                | 12           | 8                   | 500             | 1800                    |

23\. Faaliyetlerin normal ve hızlandırılmış süreleri ile dolaysız maliyetleri
aşağıda gösterilmiştir. Günlük dolaylı maliyet 4 TL olduğuna göre en düşük
maliyetli proje programını oluşturunuz.

|  Faaliyet | Önceki  Faaliyet | Normal Süre | Hızlandırılmış Süre | Normal Maliyet | Hızlandırılmış Maliyet |
|-----------|------------------|-------------|---------------------|----------------|------------------------|
| A         | -                | 3           | 1                   | 11             | 17                     |
| B         | -                | 6           | 3                   | 6              | 9                      |
| C         | -                | 5           | 4                   | 3              | 5                      |
| D         | A, B             | 11          | 3                   | 13             | 17                     |
| E         | B                | 10          | 7                   | 9              | 12                     |
| F         | B                | 5           | 1                   | 4              | 14                     |
| G         | F, C             | 3           | 2                   | 5              | 8                      |
| H         | B                | 9           | 4                   | 3              | 5                      |
| I         | E, H             | 4           | 2                   | 8              | 17                     |
| J         | E, H             | 3           | 3                   | 9              | 16                     |
| K         |  I, J            | 8           | 4                   | 15             | 23                     |
| L         | K,G              | 11          | 7                   | 20             | 28                     |
