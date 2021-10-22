*ONİKİNCİ BÖLÜM*

# DİNAMİK PROGRAMLAMA

### 

### 12.1. GİRİŞ

Karar değişkenlerinin amacı gerçekleyen değerlerinin belirlenmesine yönelik
problemlerin çözümünde, sayıları ne olursa olsun, karar değişkenleri genellikle
topluca veya eşanlı olarak işleme tabi tutulur. Oysa, zaman zaman birbirleriyle
ilişkili bir dizi karar alınmasını gerektiren problemlerle de
karşılaşılabilmekte ve değişkenlerin topluca göz önünde bulundurulması durumunda
problemi çözmek olanaksız veya çok zor olabilmektedir. Bu gibi durumlarda
problemin küçük alt problemlere bölünmesi, bir başka deyişle ayrıştırılmasından
(decomposition) sonra her bir alt problem için çözüm aranması ve alt
problemlerin çözümlerinin birleştirilmesi sonucunda bütün problemin en iyi
çözümünün bulunması daha uygun olabilmektedir. Kısaca açıklanan bu yaklaşım,
"çok aşamalı problem çözüm tekniği" olarak bilinir.

Dinamik programlama, çok aşamalı problemlerin çözümünde etkin biçimde
kullanılabilen uygun bir hesaplama yöntemidir. Amaç fonksiyonunun doğrusal
olmaması durumunda dinamik programlamanın gücü artar. Öyleki, amaç fonksiyonunun
doğrusal olmaması, probleminse çok aşamalı olması durumunda dinamik programlama
etkin bir çözüm yöntemi olarak bazı durumlarda tek, bazı durumlarda alternatif
çözüm yöntemlerinden birisi olarak belirir. Kaba bir yaklaşım olmakla birlikte,
bir problemin dinamik programlama ile çözümündeki işlem sayısının değişken
sayısı ile üstel, alt problem sayısı ile doğrusal olarak arttığı söylenebilir.
Bu sebeple, n değişkenli ayrılabilir bir fonksiyonun, n sayıda tek değişkenli
fonksiyon olarak değerlendirilmesiyle işlem sayısında önemli ölçüde bir azalma
sağlanabilir.

1940’lı yılların sonlarında Richard Bellman tarafından ortaya atılan ve
isimlendirilen dinamik programlama yaygın biçimde kullanılan "yineleme
denklemiyle en iyileme" tekniğidir. Yineleme denklemiyle en iyileme deyimiyle,
çözüme tek bir aşamada değil adım adım veya aşama aşama yaklaşıldığı
anlatılmaktadır. Diğer bazı programlama yöntemlerinde de çözüme adım adım
yaklaşılmakla birlikte, kullanılan yöntem yinelemeli değil iteratiftir.
Sözgelimi, simpleks yöntemi iteratiftir. Dinamik programlamanın doğrusal
programlamada olduğu gibi standart bir matematiksel modeli dolayısıyla,
algoritmik bir çözüm tekniği yoktur. Bir başka deyişle, dinamik programlama bir
kez programlanmış bir algoritma sağlayarak dinamik programlama ile çözümü mümkün
kılan özelliklere sahip bütün problemlerin çözümünde kullanılacak bir
matematiksel model değil, bir hesaplama yöntemidir. Bu nedenle birbirine
benzeyen problemler bir araya toplanarak her özel grup için ortak bir model
dolayısıyla, çözüm yöntemi geliştirilmeye çalışılır. Dinamik programlamayı iyi
anlayabilmek için yöntemin değişik problemlerle açıklanması uygun olur.

### 12.2. DİNAMİK PROGRAMLAMANIN ANLAM ve

### KAPSAMI

## 12.2.1. Matematiksel Betimleme

Doğrusal programlamada olduğu gibi, problemin girdisi olan parametre
değerlerinin bilindiğini ve en iyi çözüme bu değerlerle ulaşılmak istendiğini
düşünelim. Bir başka deyişle, sistemin rasgele değişken içermediğini, yani
deterministik olduğunu varsayalım. Dinamik programlamada karar verme durumunun
ortaya çıktığı her bir noktaya "aşama", sistemin durumunu yansıtan girdi
parametrelerine "durum" denir. Dinamik programlamada kararı etkileyen bir çeşit
kural veya bir çeşit eşitlik tanımlanması zorunludur. Tanımlanan bu kural veya
eşitliğe "dönüştürüm" denir. Dinamik programlamanın bu önemli bileşenleri ve
bunlar arasındaki ilişkiler Şekil 12.1’de gösterilmiştir.

**Şekil 12.1**

Her biri bir karar gerektiren aşamalardan herhangi birinde bulunduğumuzu
düşünelim. Alınan her bir karar iyi veya kötü bir değer yaratır. Alınan karar
sonucu gerçekleşen bu değer, araştırıcının tanımladığı bir eşitlikle açıklanır.
Dinamik programlama için çok önemli olan bu eşitliğe "karar-yarar eşitliği"
denir. Bu eşitlik aynı zamanda, belirli bir durum-karar çiftine bağlı olarak
ortaya çıkan getiri veya sonucu gösterdiğinden, "getiri" veya "sonuç fonksiyonu"
olarak da isimlendirilir. Getiri fonksiyonu genellikle, durum değişkeni ile
alınan kararın bir fonksiyonudur. Herhangi bir n aşamasında, belirli bir durum
değişkeni (Sn) için getiri fonksiyonunu en büyük (veya en küçük) kılan karar,
ait olduğu aşamanın en iyi kararıdır. Bu durum herhangi bir aşama için
fonksiyonel olarak aşağıdaki gibi gösterilebilir.

**Şekil 12.2**

n, kararın alındığı aşamanın numarası olmak üzere Şekil 12.2’deki semboller
aşağıda açıklandıkları gibidir.

Sn = Girdi durumu Šn = Çıktı durumu

xn = Karar değişkeni gn = Getiri fonksiyonu = rn(Sn, xn)

Bu tanımlara açıklık kazandırmak için bir yatırım problemi tanımlayalım. Bir
yatırımcının (karar verici), belirli bir sermaye ile kazançları (getiri
fonksiyonları) bilinen bir dizi (N tane) yatırım faaliyetine girmesi söz konusu
olsun. Burada toplam yatırım kararı, her bir yatırım faaliyeti (aşama) için bir
karar alınması sonucu belirlenecektir. Yatırımcı, yatırım faaliyetlerine
(aşamalar) ne kadarlık yatırım yapacağına karar vermek durumundadır. j’inci
yatırıma ayrılan para miktarını xj (karar) ve bu yatırımdan elde edilen kazancı
rj(xj) ile gösterelim. Buna göre rj(xj), yatırım miktarının bir fonksiyonu
olacaktır. xj’nin değeri doğrudan doğruya yatırımcının sermayesine (durum)
bağlıdır. Bu durumda her bir yatırım faaliyetinden sağlanacak kazanç, durum
değişkeni ile değeri durum değişkeninin değerine bağlı olan karar değişkeninin
bir fonksiyonudur.

Belirli sayıda karar noktası içeren ve kararlar arasındaki ilişkinin Sn+1 = Sn
xn geçiş fonksiyonu ile açıklandığı bir problemle yüz yüze olduğumuzu düşünelim.
Bu yazılışta, Sn+1 = aşama n’nin çıktısı, Sn = aşama n’nin girdisi, xn = aşama
n’nin karar değişkenidir.

Bir aşamadan başka bir aşamaya geçildiğinde karşılaşılabilecek dönüştürümlerle
ilgili seçenekler Tablo 12.1’de gösterilmiştir.

**Tablo 12.1**

|    |  Geçiş Fonksiyonu |
|----|-------------------|
| +  |  Sn+1 = Sn + xn   |
|  - |  Sn+1 = Sn - xn   |
|  x |  Sn+1 = xn x Sn   |
| ±  |  Sn+1 = Sn ±      |

Sn+1, Sn ve xn’lerin birimleri benzeşik olmak zorundadır. Birim; insan, para,
makine, zaman, olasılık, ağırlık veya başka bir ünvan olabilir.

Sistemi biraz daha genişletelim ve sistemin her biri bir karar gerektiren N
aşamadan oluştuğunu varsayalım. Birbirlerine yukarıda açıklanan geçiş
fonksiyonlarından birisi ile bağlı olan aşamalar arasındaki ilişki fonksiyonel
olarak aşağıdaki gibi açıklanabilir.

**Şekil 12.3**

Bir aşamanın çıktısı olan bir durum değişkeni aynı zamanda kendisini izleyen
aşamanın girdisi olduğundan, aşağıda açıklandığı gibi birden fazla sembolle
gösterilmesi uygun olur.

Si+1 = Ši i = (N - 1), (N - 2), ..., 2, 1

Dinamik programlama ile problemler aşama aşama veya bir sıra içinde
çözüldüğünden, bir aşamadan diğer bir aşamaya geçişte o ana kadar birikmiş olan
sonuç değerlerinin izlenmesi gerekir. Belirli bir durum (Sn) için, n aşama
boyunca hesaplanan birikmiş toplam sonucu veya getiriyi fn(Sn, xn) ile
gösterelim. Benzer şekilde (Sn), yine belirli bir Sn girdi durumu için birikmiş
toplam getirinin en iyi değeri olsun. Sn’nin belirli bir değerine karşılık uygun
kararların (xn) sayısı birden fazladır. Bu kararlardan genellikle bir tanesi (x)
en iyi toplam kazancı (Sn) sağlar. (Sn) birikmiş en iyi getirilerden oluştuğu
için aşağıdaki gibi açıklanabilir.

Bu genel gösterimdeki aritmetik işlemci olup probleme bağlı olarak toplama,
çıkarma, çarpma veya bölme olabilir.

Geçişler ile kazançların toplamsal olduğu bir en küçükleme problemiyle yüz yüze
olduğumuzu düşünelim. Bu durumda en iyileme problemi aşağıdaki gibi formüllenir.
Burada en önemli nokta (Sn) değerinin belirlenmesidir.

(Sn) =

### 12.2.2. En İyi Karar Politikasının Geliştirilmesi

Önemli bileşenleri yukarıda açıklanan çok aşamalı bir sistemde,

1.  N sabit bir sayı olmak üzere karar alınacak N nokta (aşama) vardır.

2.  Problemin çözümüne son aşamadan (n = N) başlandığını düşünelim. Bu durumda
    en iyi kararı etkileyen tek şey sistemin bu aşamadaki durumu ve bu aşamada
    alınan karardır. Bu kural basit olmakla birlikte dinamik programlamanın
    esasını oluşturur.

3.  Bir aşama yalnızca kendisini izleyen aşamadaki kararı etkiler. Herhangi bir
    aşamada alınan karar yalnızca sistemin o aşamadaki durumuna ve karar
    değişkeni üzerindeki sınırlara bağlıdır.

Başlamak için sonuncu aşamadaki her mümkün durum için en iyi politikayı (kazanç
fonksiyonu için en iyi değeri sağlayan kararlar kümesi) bildiğimizi varsayalım.
Bu aşamada belirli bir Sn durumu için sonucun en iyi olmasını sağlayacak biçimde
alınan karar, bu aşamadan önce gelen n - 1, n - 2, ..., 1 aşamalarından
etkilenmez. n ve (n + 1) nolu aşamaların aşağıdaki ilişki (geçiş fonksiyonu) ile
bağlı olduklarını düşünelim. Bilgi akışının aşamalarla ters yönde olduklarına
dikkat edilmelidir. Bu gösterimin önemi ve yararı konu ilerledikçe ve problemler
çözüldükçe açığa çıkacaktır.

**Şekil 12.4**

Açıklamaların ortaya koyduğu gibi, tek bir aşamanın (n) kazancı gn = rn(Sn, xn)
ile açıklanır. gn’nin en iyi değeri bu aşamanın karar değişkeninin olası tüm
değerlerinin araştırılması ve sonuç değerlerinin incelenmesiyle bulunur. Bu
nedenle, aşağıdaki gibi yazılır.

xn’nin değer aralığı Sn’ye, Sn’nin değer aralığı bir önceki aşamanın kararına
bağlıdır. Konuyu açıklamak için özel olarak, Sn+1 = Sn - xn tanımını yapalım ve
n aşamasında, (n + 1)’inci aşama kazancı dahil olmak üzere, toplam iki aşama
kazancını tanımlayalım. Bu kazanç,

(Sn) =

veya Sn+1 = Sn - xn şeklinde tanımlandığından aşağıdaki gibi olur.

(Sn) =

Buradan, Sn’nin tüm değerleri için (Sn)’nin, (Sn - xn)’nin değerine bağlı olduğu
görülebilir.

Tek bir aşama için açıklanan bu yaklaşım, N aşamalı genel sistem için
yinelendiğinde, aşağıdaki ifadeye ulaşılır.

(SN) =

Yöntemin özünü açıklayan bu eşitliğin incelenmesinden anlaşılacağı gibi, son
aşamanın girdi durumu verilmişken, (SN)’nin belirlenmesi çok kolaydır. (SN-1)
ancak (SN), f(SN-2) ancak (SN-1), ..., (S1) ancak (S2) biliniyorsa
belirlenebilir. (S1)’e ulaşıldığında problem çözülmüş olur. Buna göre, dinamik
programlama yönteminin S1’in tüm olası değerleri için f1(S1)’in belirlenmesine
yönelik olduğu söylenebilir. (S1) bilindiğinde (S2), S2’nin bütün mümkün
değerleri için aşağıda bir kez daha gösterilen yineleme ilişkisinin
kullanılmasıyla belirlenebilir.

(S2) =

veya S3 = S2 - x2 bağıntısının dikkate alınmasıyla aşağıdaki gibi olur.

(S2) =

Herhangi bir S2 durumu için ikinci aşamanın en iyi politikası belirlendiğinde S3
de belirlenmiş olur. Bu süreç son aşamaya (N) kadar sürdürülür. Genel
açıklamayla yineleme ilişkisi aşağıdaki gibi ifade edilir. Burada, f(SN+1) 0
olduğuna dikkat edilmelidir.

(Sn) =

Dinamik programlamada biri ileriye (baştan sona doğru), diğeri geriye (sondan
başa doğru) olmak üzere iki yaklaşım vardır. Yukarıda geriye doğru hesaplama
yöntemi açıklanmış, yani problemin çözümüne son aşamadan başlanmış ve yineleme
denklemi ilişkisiyle ilk aşamaya ulaşılmaya çalışılmıştır. Matematiksel bakımdan
aynı olmakla birlikte zaman zaman, problemin yapısına bağlı olarak, bu iki
yaklaşımdan biri diğerine tercih edilebilir. Bazı problemler yalnızca geriye
doğru yaklaşımla çözülebilir. Bunlardan uygun olanının seçimi problemin şekline,
daha çok araştırmacının yetenek ve problem çözümündeki ustalığına bağlıdır.
Bundan başka, geçiş fonksiyonu ile getiri fonksiyonunun şekli problemden
probleme değişir. Genel olarak yineleme ilişkisi aşağıdaki eşitlikle
açıklanmaktadır.

(Sn) = , Sn+1 = Sn xn n = N, N - 1, ...,1

Dinamik programlamada en önemli nokta aşamaların belirlenmesidir. Sistemin
durumu, karar değişkenleri ve getiri fonksiyonu problem formülasyonundan elde
edilebilir. Her problemin kendine has bir geçiş fonksiyonu olduğundan ve durumun
belirlenmesi amacıyla yapılan seçim problemden probleme değiştiğinden, dinamik
programlamanın bilimden çok bir sanat olduğu söylenebilir. Bu konuda ustalık
kazanabilmenin tek yolu, çok sayıda dinamik programlama problemi çözmektir.
Dinamik programlamanın ana fikri en iyileme kuralında saklıdır. Bu kural şu
şekilde açıklanabilir. Çok aşamalı bir karar süreci probleminde kararların en
iyi kümesi başlangıç aşaması, durumu ve kararlar ne olursa olsun birinci
aşamanın kararından sonra ortaya çıkan aşama ve durum için geriye kalan kararlar
kalan problem için en iyi kararlar dizisini oluşturur.

## 12.3. AÇIKLAYICI ÖRNEK PROBLEMLER

### 12.3.1. Rota Belirleme Problemleri

Dinamik programlamanın değer ve önemini açıklamanın en iyi yolu onu bir rota
belirleme probleminin çözümünde kullanmaktır. Rota belirleme problemi fiziksel
olarak; elektrik nakli veya gaz, petrol, su gibi sıvıların akışının sağlanacağı
hatların kurulmasıyla ilgilidir.

**Örnek 12.1**: S’deki sıvı yakıt T’ye aktarılmak istenmektedir. Pompalama,
muayene vb. nedenlerden ötürü 3 ara istasyona gerek vardır. Her bir istasyonun
kurulabileceği noktalar, bunları birbirine bağlayan dallar ve maliyetler (oklar
üzerinde) Şekil 12.5’de gösterilmiştir. S ile T’yi en düşük maliyetle bağlayan
rotayı belirleyiniz.

Şekil 12.5

**Çözüm 12.1**: Problemi geriye doğru yaklaşımla çözelim. Bunun için 3 nolu
istasyonun yerini belirleme durumunda olduğumuzu düşünelim. Şekilden görüleceği
gibi bu istasyonun kurulabileceği üç nokta (A3, B3 ve C3) vardır. Bu noktaları
T’ye bağlama maliyetleri bilinmekle birlikte S’den gelen hattın bu noktalardan
hangisinde son bulduğu henüz bilinmediğinden bu aşamada herhangi bir seçim söz
konusu olamaz. A3, B3 ve C3’ün yanlarına kendilerini T’ye bağlama maliyetlerini
yazalım. Problemin bu parçasıyla (son aşama, n = 4) ilgili açıklamalar Şekil
12.6’da gösterilmiştir.

**Şekil 12.6**

Bir adım geriye giderek A2, B2, C2 ve D2 olmak üzere dört farklı yer önerilen
ikinci istasyonun yerini belirlemek istediğimizi düşünelim. Bu noktaların her
birinden T’ye en düşük maliyetle ulaşılmasını sağlayacak rota nedir? A2 den
T’ye; biri A3, diğeri B3 üzerinden iki farklı yolla ulaşılabilmektedir. A2’den
A3 üzerinden T’ye ulaşmanın maliyeti; A2’yi A3’e bağlama maliyeti (7 TL) ile
A3’ü T’ye bağlama maliyeti (8 TL) toplamı olarak 15 TL olur. A2’den T’ye B3
üzerinden ulaşıldığını düşünelim. Bu durumda 10 TL’si A2’yi B3’e, 13 TL’si B3’ü
T’ye bağlama maliyeti olmak üzere toplam 23 TL’lik bir maliyete katlanılması
gerekir. Amaç, A2’den T’ye en az harcayarak ulaşmak olduğundan, A2 noktası için
en düşük maliyetli A2 - A3 - T rotasının seçilmesi uygun olur. A2 için en küçük
olduğu belirlenen 15’i A2’nin yanına yazalım.

İkinci istasyon için B2’de bulunduğumuzu düşünelim. B2, T’ye biri A3 diğeri C3
üzerinden iki yolla bağlıdır.

B2’den A3 üzerinden T’ye ulaşmanın maliyeti; B2’yi A3’e, A3’ü de T’ye bağlama
maliyetlerinin toplamı olarak 16 TL’dir.

B2’den T’ye C3 üzerinden ulaşmanın maliyeti; 16 + 6 = 22 TL’dir. Amaç, B2’den
T’ye en düşük harcamayla ulaşmak olduğundan B2’den T’ye A3 üzerinden gitmek
uygun olur. B2 için en küçük olan 16’yı B2’nin yanına yazalım.

C2 ve D2 için de aynı işlemleri gerçekleştirelim. C2’den T’ye A3 veya B3 ya da
C3 üzerinden ulaşılabilir.

Uğrak noktası olarak A3’ün seçildiğinde toplam maliyet; 9 + 8 = 17 TL, B3
seçildiğinde, 9 + 13 = 22 TL, C3 seçildiğinde 6 + 6 = 12 TL olur. Yukarıda
gerçekleştirildiği gibi 12 en küçük olduğundan C2’nin yanına yazılır.

D2 için en düşük maliyet,

enk{3 + 13, 14 + 6} = enk{16, 20} = 16

olarak belirlenir. n küçük olduğu belirlenen bu değer D2’nin yanına yazılır.

Şimdiye kadar belirlenen sonuç değerleri (üçüncü aşama, n = 3 hesapları) Şekil
12.5’deki bağlantı ağının ilgili parçası alınarak bu parça üzerinde
gösterilmiştir (bkz. Şekil 12.7).

Şekil 12.7

Şimdi de birinci istasyonun nereye kurulacağını araştıralım. Birinci istasyonun
kurulacağı yerin belirlenmesi için yapılan işlemler aşağıda, işlem sonuçları
Şekil 12.8’de özetlenmiştir.

**Şekil 12.8**

Şekil 12.8’den görüleceği gibi 1 nolu istasyon için A1, B1, C1 ve D1 olmak üzere
dört seçenek vardır. A1 seçildiğinde T’ye, A2 veya B2 ya da D2 üzerinden
ulaşılabilir. A1’den T’ye A2 üzerinden ulaşmanın maliyeti; A1’den A2’ye gitmenin
maliyeti (16 TL) ile A2’den T’ye ulaşmanın en düşük maliyeti olan 15’in toplamı
olarak 31 TL olur. İkinci istasyon B2’ye kurulduğunda maliyet; 10 + 16 = 26 TL,
D2’ye kurulduğunda 13 + 16 = 29 TL olur. Enk{31, 26, 29} = 26 olduğundan 26,
A1’in yanına yazılır. Benzer yaklaşımla B1 için en küçük olduğu saptanan 18 (=
enk{10 + 15, 6 + 12}) B1’in yanına yazılır. C1 için en küçük olan 19’un (= enk{8
\+ 15, 3 + 16, 6 + 16}) C1’in, D1 için en küçük olduğu belirlenen 21’in (= enk{5
\+ 16, 10 + 12, 15 + 16}) D1’in yanına yazılmasıyla bu aşamanın aritmetik
işlemleri tamamlanmış olur

Bir adım geriye giderek başlangıç noktasına gelelim. S ile T arasındaki bağlantı
A1, B1, C1 veya D1 üzerinden sağlanabilir. Bu noktalardan hangisinde bulunmanın
uygun olduğunun kararlaştırılması için dört nokta ayrı ayrı incelenmelidir.
S’den A1’e ulaşmanın maliyeti 13 ile A1’den T’ye ulaşmanın en düşük maliyeti
olarak belirlenen 26’nın toplanmasıyla; S’den A1 yoluyla T’ye ulaşmanın maliyeti
39 TL olarak hesaplanır. S’den B1’e ulaşmanın maliyeti 7 ile yukarıda B1’den
T’ye ulaşma maliyetinin en küçük değeri olarak belirlenmiş olan 18’in
toplanmasıyla; S’den T’ye B1 üzerinden ulaşmanın maliyeti 25 TL olarak
hesaplanır. S’den C1 yoluyla T’ye ulaşmanın maliyeti 6 + 19 = 25 TL; D1 yoluyla
ulaşmanın maliyeti 10 + 21 = 31 TL olur. Bu adımda hesaplanan toplamlardan en
küçüğü olan 25’in (= enk{39, 25, 25, 31}) S’nin yanına yazılmasıyla problem
çözülmüş olur. En küçük olduğu belirlenen 25’e biri B1 diğeri C1 olmak üzere iki
ayrı noktada raslandığı görülebilir. Tüm aşamalar birlikte düşünüldüğünde iki
alternatif çözüm: (S - B1 - C2 - C3 - T), (S - C1 - B2 - A3 - T) olarak
belirlenir. Bu tür dinamik programlama problemleri aşamaları sıralı veya "sıra
izleyen dinamik programlama problemleri" olarak bilinir.

Dinamik programlama problemlerinin çözümünde hata yapma olasılığını azaltmak
için karar tablolarının kullanılması uygun olur. Dinamik programlama
problemlerinin çözümündeki her aşama (n = N, N - 1, ..., 1) için Tablo 12.2’deki
tipte tablolar elde edilir.

**Tablo 12.2**

| xn  | fn(Sn, xn) |     |      |     |   |   |
|-----|------------|-----|------|-----|---|---|
| Sn  | xn1        | xn2 |  ... | xnj | f | x |
| Sn1 |            |     |      |     |   |   |
| Sn2 |            |     |      |     |   |   |
| ... |            |     |      |     |   |   |
| Sni |            |     |      |     |   |   |

f**=** fn(Sn, xn)

Bu karar tablosu son aşama, yani n = 1 için düzenlendiğinde problem çözülmüş
olur. Başlangıç durumu bilindiğinden, başlangıç kararı ile belirtilir. Diğer
aşamalara ilişkin karar değişkenlerinin en iyi değeri sistemin o aşamadaki
durumunun dikkate alınmasıyla belirlenir.

Karar tablolarının kullanılması etkin hesaplama üstünlüğü sağlar. Bu nedenle,
yalnız sıralı dinamik programlama problemlerinde değil, sıralı olmayan
problemlerin çözümünde de karar tablolarının kullanılmasında yarar vardır. Karar
tablosu kullanımıyla çözüme örnek olması bakımından tekrar rota belirleme
problemini inceleyelim. Önce problemin önemli bileşenlerini tanımlayalım.

1.  Her bir istasyon için önerilen belirli sayıdaki merkezden oluşan kümelerin
    her birine aşama denir. Bu durumda aşamaların her biri, fiziksel olarak
    belirli bir pompalama istasyonuna karşılık gelir. Şekil 12.5’de gösterildiği
    gibi S’den T’ye 4 aşamada ulaşılabildiğinden problem dört aşamalıdır.

2.  Herhangi bir aşamada o aşamaya karşılık gelen istasyon için önerilen
    yerlerden birinde olunabilir. Bu, incelenmekte olan aşamanın o anda içinde
    bulunduğu durumudur.

3.  Her aşamada ilgili duruma uygun bir karar alınması gerekir. Her aşamada, bir
    sonraki aşamada hangi noktaya ulaşılmasının uygun olduğu
    kararlaştırılacaktır. Olası kararlar izleyen aşamanın karşılık geldiği
    pompalama istasyonu için önerilen yerlerdir.

4.  Alınan her kararın kazanç adı verilen bir yararı veya maliyeti olmalıdır.
    Kazanç sabit bir değerle, cebirsel bir eşitlikle veya karmaşık bir
    matematiksel modelle açıklanabilir. Örneğimizde kazanç, tek bir değer olup
    pompa istasyonları arasında bağlantı sağlama maliyeti (C(Sn, xn)) olarak
    tanımlanmıştır.

5.  Bir aşamadan diğer bir aşamaya geçişte duruma göre toplam maliyet veya
    toplam kazanç, kısaca problemin kapsamı göz önünde bulundurularak tanımlanan
    toplamın değeri, yineleme fonksiyonu ile hesaplanır. Örneğimizin yineleme
    denklemi noktalar arasında bağlantı sağlayan hatların maliyetleri toplamı
    olarak tanımlanmıştır.

Şu ana kadar yapılan açıklamalardan anlaşılacağı gibi, problemin herhangi bir
aşamasının (n) karar değişkenleri (xn), bu aşamayı izleyen aşamadı (n + 1)
yerleşim merkezlerinin kümesidir. Sn durumunda iken xn’in seçilmesi sonucunda
kalan aşamalar için en iyi karara karşılık gelen toplam maliyeti fn(Sn, xn) ile
gösterelim. fn(Sn, xn)’i en iyileyen (en küçükleyen) xn değerini ile, fn(Sn,
xn)’in en küçük değerini ise (Sn) ile gösterelim.

Yukarıda olduğu gibi problemin çözümüne sondan, yani dördüncü aşamadan
başlayalım. Aşağıdaki karar tablosunun S4 başlıklı sütununda gösterildiği gibi,
n = 4 aşamasında S4 için A3, B3 ve C3 olmak üzere üç değer söz konusudur. Bu
noktalardan sonra varılacak tek bir nokta (T) vardır. T’ye ulaşıldığında
dördüncü alt problem çözülmüş olur. T’ye hangi noktadan hareketle ulaşılmalıdır
şeklinde açıklanabilen bu tek-aşama probleminin karar tablosu aşağıda
gösterilmiştir. (S4) = C(S4, T) olarak belirlenmiştir.

**Tablo 12.3**

|  x4  S4 |  T |  (S4) |   |
|---------|----|-------|---|
|  A3     |  8 |  8    | T |
|  B3     | 13 | 13    | T |
|  C3     |  6 |  6    | T |

Bir aşama geri gidildiğinde varılan üçüncü aşamada; A2, B2, C2 ve D2 olmak üzere
dört durum, A3, B3, C3 olmak üzere gidilecek üç nokta vardır. Bu aşamada bu üç
noktadan hangisine gitmenin uygun olacağı kararlaştırılacaktır. Karar için, her
bir nokta ayrı ayrı değerlendirililmeli ve değerlendirme sonuçları
karşılaştırılmalıdır. A2’de bulunduğumuzu varsayalım. Buradan ya A3 ya da B3’e
ulaşılır. A3’e gitmenin maliyeti 7, B3’e gitmenin maliyeti 10 olarak
verilmiştir. A3’ün seçilmesi durumunda A3’den sonra katlanılan en küçük maliyet
Tablo 12.3’de açıklandığı gibi 8 TL’dir. Buna göre toplam maliyet, 15 (= 7 + 8)
TL olur. Benzer şekilde varış noktası B3 olarak belirlendiğinde, toplam maliyet
23 (= 10 + 13) TL olur. Buna göre A2’de iken en küçük maliyeti ((A2) = 15) veren
= A3’ün seçilmesi gerekir.

B2, C2 ve D2 noktaları için benzer hesaplamaların yapılmasıyla üçüncü istasyon
için yer belirleme probleminin dinamik programlama karar tablosu aşağıdaki gibi
düzenlenir.

**Tablo 12.4**

|  x3  |  f3(S3, x3) = C(S3, x3) + (S4) |              |             |      |     |
|------|--------------------------------|--------------|-------------|------|-----|
| S3   | A3                             |  B3          | C3          | (S3) |     |
|  A2  |  7 + 8 = 15                    | 10 + 13 = 23 | -           | 15   |  A3 |
|  B2  |  8 + 8 = 16                    | -            | 16 + 6 = 22 | 16   |  A3 |
|  C2  |  9 + 8 = 17                    |  9 + 13 = 22 |  6 + 6 = 12 | 12   |  C3 |
|  D2  | -                              |  3 + 13 = 16 | 14 + 6 = 20 | 16   |  B3 |

(S3) = C(S3, x3) + (S4)

Bir aşama geri gidildiğinde ortaya çıkan ikinci aşama probleminin çözümü de
benzer yolla elde edilebilir. İkinci aşama için, f2(S2, x2) = C(S2, x2) +
(S3)’dir. Sözgelimi A1’de iken D2’ye gitmeye karar verildiğinde toplam maliyet
A1’i D2’ye bağlama maliyeti C(A1, D2) ile D2’den sonra katlanılması gereken en
düşük maliyet (D2) = 16’nın toplamına eşit olur. İkinci aşama probleminin çözüm
sonuçları aşağıdaki tabloda gösterilmiştir.

**Tablo 12.5**

| x2 | f2(S2 , x2) = C(S2, x2)+ (S3) |              |              |              |      |    |
|----|-------------------------------|--------------|--------------|--------------|------|----|
| S2 | A2                            | B2           | C2           | D2           | (S2) |    |
| A1 | 16 + 15 = 31                  | 10 + 16 = 26 | -            | 13 + 16 = 29 | 26   | B2 |
| B1 | 10 + 15 = 25                  | -            |  6 + 12 = 18 | -            | 18   | C2 |
| C1 |  8 + 15 = 23                  | 3 + 16 = 19  | -            |  6 + 16 = 22 | 19   | B2 |
| D1 | -                             | 5 + 16 = 21  | 10 + 12 = 22 | 15 + 16 = 31 | 21   | B2 |

(S2) = C(S2, x2) + (S3)

Bir aşama geri gidildiğinde birinci aşamaya, yani başlangıç noktasına ulaşılır.
Bu durumda ortaya çıkan birinci aşama probleminin çözümü aşağıdaki tabloda
gösterilmiştir.

**Tablo 12.6**

| x1 | f1(S1, x1) = C(S1, x1) + (S2) |             |             |              |       |        |
|----|-------------------------------|-------------|-------------|--------------|-------|--------|
| S1 | A1                            | B1          | C1          | D1           |  (S1) |        |
| S  | 13 + 26 = 39                  | 7 + 18 = 25 | 6 + 19 = 25 | 10 + 21 = 31 | 25    | B1, C1 |

f(S1) = C(S1, x1) + (S2)

İlk aşamanın (n = 1) karar tablosunun düzenlenmesiyle problem çözülmüş olur.
Artık tüm problem için en iyi çözüm belirlenebilir.

En iyi çözümün belirlenmesi için son karar tablosundan, yani birinci aşama çözüm
tablosundan başlanır ve geriye doğru giderek sırasıyla diğer tablolardan karar
değişkenlerinin en iyi değerleri okunur.

Son karar tablosunun başlıklı sütunu S’nin ya B1 ya da C1’e bağlanması
gerektiğini gösterir. B1’in seçildiğini varsayalım. Bu durumda, S2 = B1 olur.
İkinci aşama karar tablosunun S2 = B1 satırından = C2 olarak belirlenir. Buna
göre, S3 = C2 olur. Üçüncü aşama çözüm tablosunun S3 = C2 satırından = C3 olduğu
belirlenir. Son olarak dördüncü aşamanın karar tablosundan S4 = C3 için x= T
olduğu saptanır.

Buna göre en küçük toplam maliyetli istasyon yerleştirme planının birincisi
önceden olduğu gibi, **S - B1 - C2 - C3 - T** olarak belirlenir. Yukarıda
açıklandığı gibi ikinci bir yerleştirme planı vardır. İlk yerleştirme planının
belirlenmesinde izlenen adımların tekrarlanmasıyla ikinci yerleştirme planı, **S
\- C1 - B2 - A3 - T** olarak belirlenir.

Her iki planın da, f(S1) = 25 TL’lik harcama gerektirdiği görülebilir.

### 12.3.2. Kaynak Bölüştürme Problemleri

Karar vericilerin sıklıkla karşılaştıkları problemlerden birisi de sınırlı
kaynakların değişik faaliyetler arasında en uygun biçimde bölüştürülmesidir.
Doğrusal programlama, bu amaçla kullanılabilecek uygun bir çözüm tekniği olmakla
birlikte anılan yöntemin bu amaçla kullanılabilmesi için aşağıdaki varsayımların
sağlanması gerekir.

1\. Herhangi bir faaliyete ayrılan kaynak miktarı negatif olmayan bir sayıdır.

2\. Herhangi bir faaliyetten sağlanan kazanç o faaliyet için ayrılan kaynak
miktarıyla orantılıdır.

3\. Değişik faaliyetlerden sağlanan toplam kazanç, faaliyetlerden elde edilen
kazançlar toplamına eşittir.

Dinamik programlama, bu varsayımlardan ilk ikisi geçersiz olsa bile, bölüştürme
planının belirlenmesinde kullanılabilir. Yukarıda açıklandığı gibi, herhangi bir
problemin dinamik programlama ile çözülebilmesi için öncelikle karar aşamaları
(alt problemler) tanımlanmalıdır. Kaynak bölüştürme problemlerinin dinamik
programlama ile çözümünün önemli elemanları aşağıda açıklanmıştır.

Toplam kazanç, faaliyetlerden sağlanan kazançlar toplamına eşit olduğundan N
sayıda yatırım faaliyeti içeren problem N aşamalı olacaktır. Yatırımcı, çeşitli
yatırımlara ne kadarlık yatırım yapacağına karar vermek durumundadır. Toplam
kaynak miktarı (x) bilinen bir tamsayı olmak üzere karar değişkeni xj ile j’inci
yatırıma ayrılan yatırım miktarını, rj(xj) ile de j’inci yatırımdan elde edilen
kazancı gösterelim. Buna göre rj(xj), yatırım miktarının bir fonksiyonu olur.
Bütün yatırımlardan elde edilen toplam kazanç Z ile gösterildiğinde problem
aşağıdaki gibi modellenir.

Amaç fonksiyonu, Zenb =

Kısıtlayıcı fonksiyon, x =

Negatif olmama koşulu, xj 0 j = 1, 2, ..., N

Yatırım kararları her seferinde bir karar olarak belirleneceğinden, x miktarı
geriye doğru yaklaşımla sırasıyla; N, N - 1, N - 2 ve giderek birinci yatırım
faaliyetlerine ayrılacaktır. 0 xn x olmak üzere n’inci yatırım için ayrılan
nakit miktarı xn ile gösterildiğinde, diğer yatırım faaliyetlerine kalan nakit
miktarı (x - xn) olur. (n + 1)’inci yatırım faaliyetten sağlanan kazanç fn+1(x -
xn) ile gösterildiğinde, fn+1(x - xn) aşağıdaki gibi olacaktır.

fn+1(x - xn) =

Buna göre, n’inci faaliyete gelindiğinde biriken kazanç aşağıdaki gibi
açıklanır. Artık problem bu ifadeyi en büyükleyen xn değerinin bulunmasından
ibarettir.

fn(xn) = rn(xn) + (x - xn)

Genel olarak (xn) ifadesi aşağıdaki gibi açıklanmaktadır.

(xn) = {rn(xn) + } n = N, N - 1, ..., 1

Yukarıda açıklandığı gibi, hesaplandığında problem çözülmüş olur. En iyi çözümün
belirlenmesi için ’in hesaplandığı aşamadan başlayıp geriye doğru giderek
değişken (xi) değerlerinin belirlenmesi yeterlidir.

**Örnek 12.2**: Bir yatırımcı elindeki 7 TL ile kazançları bilinen üç değişik
yatırım faaliyetine girmeyi planlamaktadır. j yatırım seçeneğine xj TL ayrılması
durumunda kazanç rj(xj) TL’dir. rj(xj)’ler aşağıdaki gibidir. Yatırım miktarları
tamsayı olmak üzere, yatırımlardan elde edilen kazançlar toplamının en büyük
olmasını sağlayan yatırım planını belirleyiniz.

r1(x1) = 6x1 + 3 (x1 \> 0)

r2(x2) = 3x2 + 9 (x2 \> 0)

r3(x3) = 7x3 + 4 (x3 \> 0)

r1(0) = r2(0) = r3(0) = 0

**Çözüm 12.2**: Yatırım miktarlarına bağlı olarak her bir yatırım faaliyetinden
elde edilen kazançlar kazanç fonksiyonlarından (r1(x1), r2(x2), r3(x3)) tek tek
hesaplanmış ve sonuç değerleri Tablo 12.7’de topluca gösterilmiştir.

**Tablo 12.7**

| xj | A: r1(x1) | B: r2(x2) | C: r3(x3)  |
|----|-----------|-----------|------------|
| 0  | 0         | 0         | 0          |
| 1  | 9         | 12        | 11         |
| 2  | 15        | 15        | 18         |
| 3  | 21        | 18        | 25         |
| 4  | 27        | 21        | 32         |
| 5  | 33        | 24        | 39         |
| 6  | 39        | 27        | 46         |
| 7  | 45        | 30        | 53         |

Çözüme başlamadan önce çözümle ilgili belli başlı elemanları tanımlayalım.

**Aşamalar**: Her bir faaliyete ayrılacak para miktarının kararlaştırılacağı bu
problemde faaliyetlerden birine ayrılan para miktarı diğer faaliyetlere
ayrılacak para miktarını etkileyeceğinden, faaliyetlere göre yatırım miktarları
birbirine bağlı üç karar gerektirir. Bu nedenle, her bir yatırım seçeneği bir
aşama olarak düşünülür. Böylece, n = 1, 2, 3 olur. Burada rota belirleme
probleminden farklı olarak aşamaların sıra izlemediklerine dikkat edilmelidir.
Yani, A’nın, B’nin veya C’nin ele alınış sırası önemli değildir. Önemli olan bir
kez değerlendirilen bir yatırım faaliyetinin tekrar ele alınmamasıdır.

**Durum değişkenleri:** Yatırım faaliyetlerine göre yatırım miktarlarının
değerleri eldeki nakit miktarıyla sınırlıdır. Bu nedenle durum değişkeni eldeki
nakit miktarı olarak tanımlanabilir.

**Karar değişkenleri**: Her bir yatırım faaliyetine yatırılacak nakit
miktarlarına (x1, x2, x3) karar verilecektir.

**Geçiş fonksiyonu**: n’inci aşama ile (n + 1)’inci aşamanın durum değişkeni
arasındaki ilişkiyi yansıtan geçiş fonksiyonu aşağıdaki gibi tanımlanabilir.

Sn+1 = Sn - xn n = 1, 2, 3

Burada, Sn ve Sn+1 sırasıyla, n ve (n + 1)’inci aşamaların durum değişkenleri
(S1 = 7, S4 0), xn: n’inci aşamanın karar değişkeni olarak tanımlanmışlardır.

**Kazanç fonksiyonu**: Herhangi bir aşamada verilen herhangi bir kararın gerçek
değerini yansıtması gereken kazanç fonksiyonu, belirli bir yatırım faaliyetine
yapılan belirli bir yatırımdan elde edilen kazançtır. n’inci faaliyete xn TL
yatırıldığı düşünüldüğünde n’inci aşamanın kazanç fonksiyonu rn(xn) şeklinde
tanımlanabilir.

Bu çerçevede problemin dinamik programlama formülasyonu veya yineleme denklemi
aşağıdaki gibi modellenir.

(Sn) = {rn(xn) + (Sn - xn)} n = 1, 2, 3 (f(S4) = 0 )

Problemin çözümüne sondan, yani yatırım yapılacak tek bir faaliyetin kaldığı
aşamadan (n = 3) başlanır. Tek bir yatırım faaliyetinin (C) kaldığı bu aşamada
eldeki nakit miktarı, A ve B’ye ayrılan miktarlara bağlı olarak; S3 = 0, 1, 2,
3, 4, 5, 6, 7 olabilir. Böylece yatırımcı S3 kadar miktarı C’ye yatırır. C
yatırım seçeneğine yapılan yatırım miktarları üçüncü aşama karar tablosunun
(Tablo 12.8) ilk sütununda gösterilmiştir. Yatırım miktarına bağlı olarak
gerçekleşen kazançlar aynı tablonun ikinci bu aşamanın en iyi kararları üçüncü
sütununda gösterilmiştir. Toplam kazanç (f3(S3, x3)) (S3) = r3(x3) olarak
tanımlanmıştır.

**Tablo 12.8**

| x3 S3 | (S3) |   |
|-------|------|---|
| 0     | 0    | 0 |
| 1     | 11   | 1 |
| 2     | 18   | 2 |
| 3     | 25   | 3 |
| 4     | 32   | 4 |
| 5     | 39   | 5 |
| 6     | 46   | 6 |
| 7     | 53   | 7 |

**B yatırım seçeneği**: n = 2 aşamasında, yatırım yapılacak iki faaliyet (B ve
C) kaldığında nakit miktarı, S2 = 0, 1, 2, 3, 4, 5, 6, 7 olur. Sözgelimi S2 = 2
ise 3 seçenekle karşılaşılır. Birincisi; B’ye yatırım yapmayıp tüm parayı (2 TL)
C’ye yatırmaktır. Böylece B ve C faaliyetlerinden sıfır TL’si B, 18 TL’si C
faaliyetinden olmak üzere toplam 18 TL’lik kazanç sağlanır. İkincisi; eldeki 2
TL’yi B ve C faaliyetleri arasında eşit biçimde paylaştırmak, yani her ikisine
1’er TL ayırmaktır. Bu durumda kazanç 12 TL’si B’den, 11 TL’si C’den olmak üzere
toplam 23 TL olur. Üçüncü alternatif ise C’ye yatırım yapmayıp 2 TL’nin tamamını
B için kullanmaktır. Bu koşulda kazanç 15’i B’den, sıfırı C’den olmak üzere
toplam 15 TL olur. Kısaca, n = 2 aşamasında toplam kazanç; B yatırımına bağlı
olarak B’den sağlanan kazanç ile B’ye yapılan harcamadan sonra kalan paranın
tamamının C’ye yatırılmasıyla sağlanan kazancın toplamına eşittir. Hesaplanan
değerler ile diğer bilgiler Tablo 12.9’da gösterilmiştir.

**Tablo 12.9**

|  x2 | f2(S2, x2) = r2(x2 ) + (S2 - x2) |    |    |    |    |    |    |    |      |   |
|-----|----------------------------------|----|----|----|----|----|----|----|------|---|
| S2  | 0                                | 1  | 2  | 3  | 4  | 5  | 6  | 7  | (S2) |   |
| 0   | 0                                | -  | -  | -  | -  | -  | -  | -  | 0    | 0 |
| 1   | 11                               | 12 | -  | -  | -  | -  | -  | -  | 12   | 1 |
| 2   | 18                               | 23 | 15 | -  | -  | -  | -  | -  | 23   | 1 |
| 3   | 25                               | 30 | 26 | 18 | -  | -  | -  | -  | 30   | 1 |
| 4   | 32                               | 37 | 33 | 29 | 21 | -  | -  | -  | 37   | 1 |
| 5   | 39                               | 44 | 40 | 36 | 32 | 24 | -  | -  | 44   | 1 |
| 6   | 46                               | 51 | 47 | 43 | 39 | 35 | 27 | -  | 51   | 1 |
| 7   | 53                               | 58 | 54 | 50 | 46 | 42 | 38 | 30 | 58   | 1 |

**A yatırım seçeneği**: Başlangıçta 7 TL olduğundan ilk aşamanın (n = 1) durum
değişkeni için tek bir değer (S1 = 7) söz konusudur. Birinci aşamayı oluşturan
A’ya 0, 1, 2, 3, 4, 5, 6, 7 (= x1) TL yatırılabilir. Sözgelimi A’ya 3 TL
yatırıldığında, kalan 4 TL B ve C faaliyetlerine yatırılacak demek olup toplam
kazanç, 21 TL’si A’dan 37 TL’si B ve C faaliyetlerinden olmak üzere 58 TL olarak
hesaplanır. A’ya yatırılan nakit miktarına bağlı olarak hesaplanan toplam
kazançlar ile diğer bilgiler aşağıdaki karar tablosunda topluca gösterilmiştir.

**Tablo 12.10**

| x1 | f1(S1, x1) = r1(x1) + (S1 - x1) |    |    |    |    |    |    |    |      |   |
|----|---------------------------------|----|----|----|----|----|----|----|------|---|
| S1 |  0                              | 1  | 2  | 3  | 4  | 5  | 6  | 7  | (S1) |   |
|  7 | 58                              | 60 | 59 | 58 | 57 | 56 | 51 | 45 | 60   | 1 |

(S1) =

(S1) bulunduğundan, problem çözülmüştür. (S1)’in bulunduğu tablodan başlayarak
en yüksek kazancı sağlayan yatırım politikasını belirleyelim. n = 1 tablosunun
başlıklı sütunundan görüldüğü gibi = 1’dir. Yani, A’ya 1 TL yatırılacaktır. A’ya
1 TL yatırılması sonucu kalan 6 TL’nin dağıtımı için ikinci aşama tablosunun S2
= 6 satırından = 1 okunur. Bu, B’ye 1 TL yatırılacağı anlamındadır. B’ye 1 TL
ayrılmasından sonra kalan 5 TL’nin dağıtımı için üçüncü aşama karar tablosunun
S3 = 5 satırına bakılır. Bu satırdan = 5 olduğu, yani C’ye 5 TL yatırım
yapılması gerektiği görülecektir. Özetle = 1, = 1, = 5 seçimiyle toplam kazancın
en yüksek değeri olan (S1) = 60 TL’ye ulaşılması sağlanacaktır.

Şimdiye kadar çözülen dinamik programlama problemlerinin yineleme
denklemlerindeki aritmetik işlemci () toplama olarak belirmiştir. Dinamik
programlamanın açıklandığı kesimde belirtildiği gibi durum dönüşüm
fonksiyonundaki ve/veya yineleme denklemindeki aritmetik işlemci toplamadan
farklı olabilir. Aşağıdaki örnek problem bu durumla ilgilidir.

**Örnek 12.3**: Dört temel parçadan oluşan bir elektronik sistemin işlevini
yerine getirip getirmemesi sistemi oluşturan parçaların işlevlerini yerine
getirip getirmemelerine bağlıdır. Sistemin güvenilirliği parçaların
güvenilirliklerine bağlı olup parçaların güvenilirlikleri oluştukları paralel
birim sayılarına bağlıdır. Eklenen paralel birim sayılarına bağlı olarak
parçaların işlevlerini yerine getirme olasılıkları ile eklenen birim sayısına
bağlı olarak katlanılması gereken maliyetler Tablo 12.11’de verilmiştir.
Sistemin geliştirilmesi amacıyla ayrılan bütçe 100 TL’dir. Sistemin
güvenilirliğini en yüksek düzeye çıkaracak şekilde her bir temel parçaya
eklenecek paralel birim sayılarını hesaplayınız.

**Tablo 12.11**

| Birim Sayısı | I. Parça | II. Parça | III. Parça | IV. Parça |          |         |          |         |
|--------------|----------|-----------|------------|-----------|----------|---------|----------|---------|
|              | Olasılık | Maliyet   | Olasılık   | Maliyet   | Olasılık | Maliyet | Olasılık | Maliyet |
| 1            | 0.70     | 10        | 0.50       | 20        | 0.70     | 10      | 0.60     | 20      |
| 2            | 0.80     | 20        | 0.70       | 40        | 0.90     | 30      | 0.70     | 30      |
| 3            | 0.90     | 30        | 0.80       | 50        | 0.95     | 40      | 0.90     | 40      |

**Çözüm 12.3**: Bu problemin yatırım problemine benzediği görülebilir. Yatırım
problemindeki sermayenin yerini sistemin güvenilirliğini arttırmak için ayrılan
bütçe, yatırım faaliyetlerinin yerini temel parçalar, yatırım faaliyetlerine
ayrılan nakit miktarlarının yerlerini temel parçalara yapılacak harcamalar
almışlardır. İki problem arasındaki temel fark etkinlik ölçülerinde dolayısıyla,
amaç fonksiyonlarındadır. Yatırım probleminde etkinlik kazanç olarak
tanımlanmışken, bu problemin etkinlik ölçüsü güvenilirlik olasılığıdır.

**Aşamalar**: Yukarıda açıklandığı gibi dört temel parçanın her birine kaçar
adet birim eklenmesinin uygun olacağının belirleneceği problemde dört temel
parça, dinamik programlama formülasyonunun aşamalarını oluşturur.

**Durum değişkenleri**: Eklenecek birim sayılarının alacağı değerler eldeki
nakit miktarına bağlı olduğundan herhangi bir aşamanın durum değişkeni eldeki
nakit miktarıdır.

**Karar değişkenleri**: Her bir temel parçaya eklenecek birim sayılarına (x1,
x2, x3, x4) karar verilecektir.

**Geçiş fonksiyonu**: Geçiş fonksiyonu bir aşamadan diğer bir aşamaya
geçildiğinde karşılaşılan durumu göstermelidir. Problemin durum değişkeni eldeki
nakit miktarı olarak tanımlandığından, geçiş fonksiyonu nakit miktarındaki
değişmeyi göstermelidir. Buna göre geçiş fonksiyonu, n’inci parçaya xn adet
birim eklemenin maliyeti olmak üzere, şöyledir:

Sn+1 = Sn **-**

**Kazanç fonksiyonu**: xn ile n’inci parçaya eklenen birim sayısını ve pn(xn)
ile de xn birim eklenen n’inci parçanın güvenilirlik olasılığını gösterelim.
Buna göre pn(xn) eklenen birim sayısının bir fonksiyonu olur. Sistemin
güvenilirlik olasılığı parçaların güvenilirlik olasılıklarının çarpımına eşit
olduğundan amaç fonksiyonu aşağıdaki gibi tanımlanabilir.

Zenb = = p1(x1) x p2(x2) x p3(x3) x p4(x4)

Problem sınırlı bir bütçe ile çözülmek istendiğinden kısıtlayıcı fonksiyon parça
sayılarına kısıt koyan fonksiyon aşağıdaki gibi modellenir.

100

Sistemin güvenilirliği her bir parçaya eklenen birim sayısına dolayısıyla,
pn(xn) değerine bağlı olduğundan, 100 TL’nin dört temel parçaya paylaştırılması
ile elde edilecek maksimum güvenilirlik aşağıdaki gibi yazılabilir.

fn(Sn, xn) = pn(xn) enb

Harcama kararları her defasında bir karar olarak belirleneceğinden, 100 TL
geriye doğru yaklaşımla sırasıyla, dördüncü, üçüncü, ikinci ve son olarak
birinci parçalara eklenecek birimlere ayrılacaktır. 0 100 olmak üzere, n’inci
parça için harcandığında diğer üç parça için (100 - ) TL kalır. (n + 1)’inci
faaliyetten sağlanan kazancın fn+1(100 - xn) olduğu varsayıldığında , fn+1(x - )
aşağıdaki gibi ifade edilir.

fn+1(x - ) =

Buna göre, n faaliyetten sağlanan toplam güvenilirlik,

(Sn) = pn(xn) f(100 - )

olarak ifade edilir.

Bu durumda problem bu ifadeyi en büyük yapan xn değerinin bulunması olacaktır.

Genel olarak f(Sn) aşağıdaki gibi formüllenir.

(Sn) = {pn(xn) (Sn - )} n = 1, 2, 3, 4

f hesaplandığında çözüm tamamlanmış demektir. En iyi çözümün belirlenebilmesi
için önceden olduğu gibi, f’in hesaplandığı aşamadan başlayıp geriye doğru
giderek xj değerlerinin belirlenmesi yeterlidir.

Kaç birim eklenecek sorusunun yanıtlanacağı tek bir parça (dördüncü parça)
kaldığında, her temel parçaya en az bir birim ekleneceğinden, eldeki nakit
miktarı en az 20 TL en fazla 60 TL olur. Buna göre, S4 = 20, 30, 40, 50, 60
olur.

Eklenen birim sayısına (1, 2, 3) bağlı olarak dördüncü parçanın güvenilirlik
olasılığı olarak tanımlanan; f4(S4, x4) = (S4) = p4(x4) aşağıdaki tablonun
ikinci sütununda gösterilmiştir.

**Tablo 12.12**

|  x4 S4 |  (S4) |   |
|--------|-------|---|
| 20     | 0.60  | 1 |
| 30     | 0.70  | 2 |
| 40     | 0.90  | 3 |
| 50     | 0.90  | 3 |
| 60     | 0.90  | 3 |

**III. Parça**: Üçüncü parçaya gelindiğinde elde en az 30 TL, en fazla 70 TL
vardır. Para miktarı 30 TL ise üçüncü ve dördüncü parçalara birer birim eklenir,
böylece 30 TL’nin 10 TL’si üçüncü, 20 TL’si dördüncü parça için harcanır. Bu iki
parça birlikte düşünüldüğünde sistemin güvenilirlik olasılığı 0.70 x 0.60 = 0.42
olur. Tablo değerlerinin hesaplanmasına başka bir örnek olmak üzere, S3 = 60
olduğunu düşünelim. Bu durumda üç alternatif söz konusudur. Birincisi üçüncü
parçaya tek birim eklemek, böylece 60 TL’nin 10 TL’sini üçüncü parça, kalan 50
TL’sini dördüncü parça için harcamak yani, dördüncü parçaya 3 birim eklemektir.
Bu durumda olasılık; 0.70 x 0.90 = 0.63 olur. İkinci alternatif üçüncü parçaya
iki birim eklenmesidir. Bu parçaya iki birim eklenmesi 30 TL’lik harcama
gerektirdiğinden, dördüncü parçaya 30 TL kalır. Bu dördüncü parçaya iki birim
eklenmesi demektir. Bu durumda sistemin güvenilirlik olasılığı 0.90 x 0.70 =
0.63 olur. Üçüncü alternatif ise üçüncü parçaya üç birim eklemek, yani 60 TL’nin
40 TL’sini bu parça için harcamak, kalan 20 TL ile dördüncü parçaya tek birim
eklemektir. Bu durumda olasılık 0.95 x 0.60 = 0.57 olur. n = 3 karar tablosu
aşağıdadır.

#### Tablo 12.13

| x3 |  f3(S3, x3) = p3(x3) x (S3 - ) |                    |                    |      |      |
|----|--------------------------------|--------------------|--------------------|------|------|
| S3 | 1                              | 2                  | 3                  | (S3) |      |
| 30 | 0.70 x 0.60 = 0.42             | -                  | -                  | 0.42 | 1    |
| 40 | 0.70 x 0.70 = 0.49             | -                  | -                  | 0.49 | 1    |
| 50 | 0.70 x 0.90 = 0.63             | 0.90 x 0.60 = 0.54 | -                  | 0.63 | 1    |
| 60 | 0.70 x 0.90 = 0.63             | 0.90 x 0.70 = 0.63 | 0.95 x 0.60 = 0.57 | 0.63 | 1, 2 |
| 70 | 0.70 x 0.90 = 0.63             | 0.90 x 0.90 = 0.81 | 0.95 x 0.70 = 0.67 | 0.81 | 2    |

(S3) = {p3(x3) x (S3 - )}

**II. Parça**: Problemin çözümüne iki aşama kaldığında eldeki para miktarı; 50,
60, 70, 80, 90 TL olabilir. Buna göre eklenecek birim sayısı 1, 2 veya 3 olur.
Bu aşamanın karar tablosu aşağıda gösterilmiştir.

#### Tablo 12.14

| x2 | f2(S2, x2) = p2(x2) x f |                     |                      |       |   |
|----|-------------------------|---------------------|----------------------|-------|---|
| S2 | 1                       | 2                   | 3                    | (S2)  |   |
| 50 | 0.50 x 0.42 = 0.210     | -                   | -                    | 0.210 | 1 |
| 60 | 0.50 x 0.49 = 0.245     | -                   | -                    | 0.245 | 1 |
| 70 | 0.50 x 0.63 = 0.315     | 0.70 x 0.42 = 0.294 | -                    | 0.315 | 1 |
| 80 | 0.50 x 0.63 = 0.315     | 0.70 x 0.49 = 0.343 | 0.80 x 0.42 = 0.336  | 0.343 | 2 |
| 90 | 0.50 x 0.81 = 0.405     | 0.70 x 0.63 = 0.441 | 0.80 x 0.49 = 0.392  | 0.441 | 2 |

(S2) = {p2(x2) x (S2 - )}

**I. Parça**: Henüz herhangi bir harcama yapılmadığından, S1 = 100 TL olur. Bu
paranın en az 50 TL’si diğer üç parçaya ayrılacaktır. Birinci parçaya 1, 2 veya
3 birim eklenebilir. Bu parçaya eklenen birim sayısına bağlı olarak hesaplanan
olasılık değerleri ve çözümle ilgili diğer bilgiler Tablo 12.15’de
gösterilmiştir.

#### Tablo 12.15

| x1  |  f1(S1,x1) = p1(x1) x (100 - ) |                       |                      |        |   |
|-----|--------------------------------|-----------------------|----------------------|--------|---|
| S1  | 1                              | 2                     | 3                    | (S1)   |   |
| 100 | 0.70 x 0.441 = 0.3087          | 0.80 x 0.343 = 0.2744 | 0.90 x 0.315 = 0.279 | 0.3087 | 1 |

(S1) = {p1(x1) x (100 - )}

Birinci temel parça için yapılan çözümün yer aldığı tablodan görüldüğü gibi, bu
parçaya 1 birim eklenecek, böylece 100 TL’nin 10 TL’si bu parça için harcanacak
geriye 90 TL kalacaktır. İkinci temel parça için düzenlenen tablonun 90
satırından bu parçaya 2 birim eklenmesi (40 TL harcanması) gerektiği anlaşılır.
Bu harcamayla geriye 50 TL kalır. Üçüncü temel parçanın 50 satırından üçüncü
temel parçaya 1 birim eklenmesi gerektiği okunur. Yani, üçüncü temel parçaya 10
TL harcanması kararlaştırılacaktır. Sonuncu parçaya gelindiğinde elde 40 TL
kalmış olur. Dördüncü parça için gerçekleştirilen çözüm tablosunun 40
satırından, = 3 okunur. Böylece, en yüksek güvenilirlik 100 TL’nin 90 TL’si
harcanarak sağlanmış olur.

Böylece problemin en iyi çözümü şu şekilde belirlenmiş olur: = 1, = 2, = 1, = 3
ve Zenb = 0.3087 = (S1).

**12.3.3. Sırt Çantası Problemi**

Dinamik programlama ile çözülen problemlerin bir kısmı sırt çantası veya yük
taşıma problemleri başlığı altında toplanır. Bu tip problemlerde genellikle,
eldeki kaynağın birim ağırlıkları ile yarar veya zararları bilinen çeşitli
elemanlara en iyi biçimde bölüştürülmesi istenir. Bu başlık altındaki problemler
mevcut kaynağın değişik faaliyetler arasında en iyi biçimde bölüştürülmesinin
sağlanması bakımından yatırım problemlerine benzer. Sırt çantası problemine
örnek olarak aşağıdaki problemi çözelim.

**Örnek 12.4**: Taşıma kapasitesi 20 ton olan bir kamyonla 3 çeşit mal taşınmak
istenmektedir. Malların birim ağırlık (ton) ve sağladıkları kazançlar (TL)
aşağıda gösterilmiştir. Amaç, kamyonun 20 tonluk taşıma kapasitesinin A, B ve C
arasında toplam kazancı en büyük yapacak şekilde paylaştırılmasıdır. Problemi
çözünüz.

# Tablo 12.16

| Ürün - No | Ağırlık | Kazanç |
|-----------|---------|--------|
| A - 1     | 6       | 14     |
| B - 2     | 8       | 17     |
| C - 3     | 7       | 16     |

**Çözüm 12.4**: Diğer problemlerde olduğu gibi önce dinamik programlamanın
önemli elemanlarını tanımlayalım.

**Aşamalar**: Problemin çözümü ile kamyona A’dan, B’den ve C’den kaçar adet
yükleneceği belirleneceğinden A, B ve C’nin her biri bir aşama teşkil eder.
Problem 3 aşamalıdır.

**Durum değişkenleri**: Herhangi bir aşamada alınacak kararı etkileyen kamyonun
incelenen ve gelecekteki aşamaları için kalan taşıma kapasitesidir.

**Geçiş fonksiyonu**: Geçiş fonksiyonu n’inci aşamanın durum değişkeni ile (n +
1)’inci aşamanın durum değişkenini ilişkilendirmelidir. Geçiş fonksiyonu aşağıda
gösterilmiştir.

Sn+1 = Sn - Wn (xn) n = 1, 2, 3

Burada (S4 0, S0 20 olduğu varsayılmaktadır.)

Sn+1 = (n + 1)’inci aşamanın durum değişkeni

Sn = n’inci aşamanın durum değişkeni

xn = n nolu üründen taşınan miktar

Wn = n nolu ürünün birim ağırlığıdır.

**Kazanç fonksiyonu**: Kazanç fonksiyonu her aşamada o aşamada verilen karar
sonrası gerçekleşen toplam kazancı yansıtmalıdır. kn, n nolu üründen sağlanan
kazanç değeri olmak üzere, n’inci aşamanın kazanç fonksiyonu şöyledir:

rn(Sn, xn) = kn (xn) n = 1, 2, 3

Buna göre, yük taşıma probleminin dinamik programlama yineleme denklemi
aşağıdaki gibi olur.

f

Burada, n = 1, 2, 3 için fn(Sn, xn) = rn(Sn, xn) + Sn - xn(Wn) şeklinde
tanımlanmıştır. Bu problemde de ürünlerin ele alınış sırası önemli olmamakla
birlikte son aşama olarak son sıradaki C’yi ele alalım.

**Ürün C (n = 3)**: Sıra C’ye geldiğinde A ve B’den kaçar adet taşındığına bağlı
olarak kamyonda 0 ile 20 ton arasında değişen kapasite bulunur. C’nin 7 ton
ağırlığında olduğu göz önünde bulundurulduğunda durum değişkeninin 0, 1, ...,
19, 20 gibi tek değerlerle değil değer aralıklarıyla açıklanması uygun olur.
Buna göre üçüncü aşama karar tablosu aşağıdaki gibi düzenlenir. = f3(S3, x3) =
16x3 olarak tanımlanmıştır.

# Tablo 12.17

| x3       | 16x3 |   |
|----------|------|---|
| S3       |      |   |
|  0 S3 6  | 0    | 0 |
|  7 S3 13 |  16  | 1 |
| 14 S3 20 |  32  | 2 |

**Ürün B (n = 2)**: Sıra B’ye geldiğinde 0 ile 20 arasında değişen taşıma
kapasitesi kalmış olabilir. B’nin 8 ton, C’nin 7 ton ağırlığında olduklarının
göz önünde bulundurulmasıyla S2 için tıpkı S3’de olduğu gibi uygun aralıklar
belirlenmesi akılcı olur. 20 tonluk taşıma kapasitenin tamamı B için
kullanıldığında bu üründen en fazla 2 adet taşınabileceğinin belirlenmesinin
ardından bu aşamanın karar değişkeninin olası değerleri 0, 1 ve 2 olarak
belirlenir. n = 2 karar tablosu aşağıdaki gibi düzenlenir.

# Tablo 12.18

|  x2      | f2(S2 , x2) = 17x2 + (S2 - 8x2) |              |             |    |   |
|----------|---------------------------------|--------------|-------------|----|---|
|  S2      | 0                               | 1            | 2           |    |   |
| 0 S2 7   | 0 + 16 = 16                     | -            | -           | 16 | 0 |
| 8 S2 13  | 0 + 16 = 16                     |  17 + 0 = 17 | -           | 17 | 1 |
| 14       | 0 + 32 = 32                     |  17 + 0 = 17 | -           | 32 | 0 |
| 15       | 0 + 32 = 32                     | 17 + 16 = 33 | -           | 33 | 1 |
| 16 S2 20 | 0 + 32 = 32                     | 17 + 16 = 33 | 34 + 0 = 34 | 34 | 2 |

= 17x2 + (S2 - 8x2)

**Ürün A (n = 1)**: İlk aşamada kamyon boş olduğundan 20 tonluk taşıma
kapasitesi üç ürün arasında paylaştırılacaktır. A’dan taşınmazsa; x1 = 0, S2 =
20, B ve C’den taşınmaz tüm kapasite A’ya ayrılırsa, x1 = 3, S2 = 2 ( 0) olur.
x1’in olası değerleri sırasıyla 0, 1, 2 ve 3 olarak belirlenir. İlk aşama karar
tablosu aşağıda gösterilmiştir.

# Tablo 12.19

|  x1 | f1(S1, x1) = 14x1 + (20 - 6x1) |              |              |             |      |   |
|-----|--------------------------------|--------------|--------------|-------------|------|---|
|  S1 | 0                              | 1            | 2            | 3           | (S1) |   |
| 20  | 0 + 34 = 34                    | 14 + 32 = 46 | 28 + 17 = 45 | 42 + 0 = 42 | 46   | 1 |

(S1) = 14x1 + (20 - 6x1)

n = 1 karar tablosu düzenlendiğinden en iyi çözüm bulunmuştur. Bu tablodan
başlayarak en iyi çözümü belirleyelim. sütununda görüldüğü gibi = 1’dir. Yani,
A’dan 1 adet taşınacak böylece, 20 tonluk kapasitenin 6 tonu A için
kullanılacaktır. Bu durumda, S2 = 14( = 20 - 6) ton olur. İkinci aşama
tablosunun 14 başlıklı satırından = 0 olduğu, yani B’den taşınmayacağı
belirlenir. C için gerçekleştirilen çözüm tablosunun S3 = 14 satırından = 2
olarak okunur ve C’den 2 adet yüklenir. Sonuçta en iyi çözüm = 1, = 0, = 2, = 46
olarak belirlenmiş olur.

#### 12.3.4. Stok Kontrol Problemi

Dinamik programlama stok kontrol problemlerinin çözümünde de kullanılabilir. Bu
bölümde aşağıdaki özelliklere sahip bir stok kontrol probleminin dinamik
programlama ile çözümü açıklanacaktır.

1.  Stok düzeyinin kontrol edileceği zaman uzunluğu, ilk dönem 1 son dönem N
    olmak üzere, eşit uzunlukta N döneme bölünür.

2.  Dönemlere göre istemin bilindiği varsayılır.

3.  Üretim kapasitesi sınırlıdır. Her dönemin başında o dönemin üretim miktarı
    belirlenmelidir.

4.  Stok tükenmesi söz konusu değildir. Müşteri istemi stoktan veya cari
    üretimden ortaya çıktığı anda karşılanır.

5.  Toplam üretim maliyeti, üretim sabit maliyeti ile değişken maliyetin
    toplamına eşittir.

6.  İşletmenin depolama kapasitesi sınırlıdır.

7.  Bulundurma maliyeti belirlidir. Bulundurma maliyeti her dönemin sonunda elde
    kalan ve izleyen döneme devreden ürün miktarı ile bulundurma maliyetinin
    çarpımına eşittir.

8.  Amaç planlama dönemindeki toplam istemin en düşük maliyetle karşılanmasıdır.

9.  Stok durumu her ayın başında kontrol edilmektedir.

Yukarıdaki varsayımların ortaya koyduğu gibi burada her dönemin başında stok
gözden geçirilmekte, duruma göre üretim/sipariş kararı verilmektedir. Sekizinci
bölümde açıklandığı gibi bu bir periyodik tekrar stok modelidir.

**Örnek 12.5**: Mayo satan bir mağaza sahibi geçmiş deneyimlerinden mayo satış
mevsiminin 5 ay sürdüğünü bilmektedir. Yapılan araştırmalarla gelecek yılın
ilgili 5 ayındaki mayo istemleri aşağıdaki gibi tahminlenmiştir.

# Tablo 12.20

| Ay      | İstem |
|---------|-------|
| Nisan   | 20    |
| Mayıs   | 20    |
| Haziran | 50    |
| Temmuz  | 40    |
| Ağustos | 30    |

Mayoların satın alındığı üretici firma, 10’dan az 50’den fazla olan siparişleri
kabul etmemekte ve siparişlerin 10, 20, 30, 40 veya 50’lik partiler halinde
olmasını istemektedir. Sipariş miktarlarına göre fiyatlar aşağıda
gösterilmiştir. Depolama kapasitesi sınırlı olup en fazla 50 mayo
stoklanabilmektedir.

# Tablo 12.21

| Sip. Mik. | Satış Fiy.  |
|-----------|-------------|
| 10        | 9.5         |
| 20        | 9.0         |
| 30        | 8.5         |
| 40        | 8.2         |
| 50        | 8.0         |

Diğer taraftan sipariş miktarı ne olursa olsun 2 TL’si sipariş verme
hazırlıkları, 8 TL’si siparişin mağazaya ulaşması için olmak üzere toplam 10 TL
harcamak gerekmektedir. Bir mayonun bir ay boyunca stoklanmasının mağazaya
maliyeti 0.5 TL’dir. Mayo satışı mevsimsel olduğundan ve moda değişiminden
etkilendiğinden mevsim sonuna devreden stok miktarının sıfır olması
istenmektedir. Bu bilgilerin ışığı altında mayo satış mevsimi için toplam
maliyetin en küçük olmasını sağlayan sipariş planını belirleyiniz.

**Çözüm 12.5**: Dinamik programlamanın diğer uygulamalarında olduğu gibi
öncelikle ilgili terimleri açıklayalım.

**Aşamalar**: Bilindiği gibi aşama tek bir aşama kaldığında problem çözümünün
çok kolay olmasını sağlayacak biçimde tanımlanmalıdır. Buna göre Ağustos ayı
başında Temmuz ayından devreden mayo stoğu ile Ağustos ayının istemi arasındaki
fark kadar mayo sipariş edilerek dönem sonu stoğunun sıfır olması ve müşteri
isteminin karşılanması sağlanmış olur. Buna göre 5 aylık planlama dönemindeki
her ay bir aşama oluşturur. Dinamik programlama problemlerinin pek çoğunda, eğer
söz konusuysa, belirli zaman dilimleri aşamalar olarak değerlendirilirler.

**Karar değişkenleri**: Aylar itibariyle en iyi sipariş miktarının belirlenmesi
istendiğinden karar değişkeni aylara göre sipariş miktarı (x1, x2, x3, x4, x5)
olarak tanımlanır.

**Durum değişkenleri**: Sipariş miktarının belirlenmesinin amaçlandığı bu
problemde sipariş miktarının değeri stok miktarına bağlıdır. Buna göre n’inci
aşamanın durum değişkeni önceki aydan devreden stok miktarı olarak
tanımlanabilir.

**Geçiş fonksiyonu**: Birbirini izleyen aşamaların durum değişkenleri
arasın-daki ilişkiyi yansıtan geçiş fonksiyonu aşağıdaki gibi açıklanabilir.

Sn+1 = Sn + xn - Dn n = 1, 2, 3, 4, 5

Bu yazılıştaki semboller aşağıda tanımlandıkları gibidir.

So = S1 = Başlangıç stok düzeyi = 0

S6 = Dönem sonu stok düzeyi = 0

Sn = n’inci aşamanın durum değişkeni

xn = n’inci aşamanın karar değişkeni

Dn = n’inci aşamanın istemi

Bu tanımlar çerçevesinde (Sn + xn - Dn ) ifadesi n’inci aşamadan (n + 1)’inci
aşamaya devreden stok miktarını verir.

**Kazanç fonksiyonu**: Her bir aşamanın kazanç fonksiyonu o aşamada verilen
belirli bir karar sonrası ortaya çıkan toplam maliyeti yansıtır. (Sn + xn - Dn )
devreden stok miktarı olmak üzere, n’inci aşamanın kazanç fonksiyonu aşağıda
gösterilmiştir.

rn(Sn, xn) = f(xn) + hn x (Sn + xn - Dn) n = 1, 2, 3, 4, 5

Burada,

f(xn) = n’inci aşamada xn adet ürün sipariş verme maliyeti olup sabit sipariş
maliyeti ile değeri sipariş miktarına bağlı olan satın alma maliyetleri
toplamına eşittir.

hn = Bir birim ürünü bir ay boyunca stokta tutma maliyetidir. hn = 0.5 olarak
verilen bu maliyetin beş ay boyunca değişmediği kabul edilmiştir.

Bu açıklamalar doğrultusunda problemin dinamik programlama formülasyonu, yani
yineleme denklemi aşağıdaki gibi formüllenir. Burada, Sn+1 , So, S6 yukarıda
tanımlandıkları gibi olup, f(S6) = 0 dır.

(Sn) = {f(xn) + hn x (Sn + xn - Dn) + (Sn+1) n = 1, 2, 3, 4, 5

**Son ay (Ağustos) hesaplamaları**: Dönem sonu stok düzeyi sıfır olacağından,
Temmuz ayından devreden stok miktarı veri olmak üzere, bu ayda en fazla bu ayın
istemi kadar, yani 30 birim mal sipariş edilebilir. Temmuz ayından devreden mal
miktarının en az sıfır, en fazla 30 birim olabileceği göz önünde
bulundurulduğunda, S5 = 0, 10, 20, 30 olur. S5’in olası değerleri dikkate
alındığında x5 karar değişkeninin olası değerleri sırasıyla (D5 - S5)
bağıntısından 30, 20, 10, 0 olarak belirlenir. Bu açıklamaların ışığı altında
hazırlanan karar tablosu aşağıda gösterilmiştir.

# Tablo 12.22

| x5 | (S5) = f(x5) |    |
|----|--------------|----|
| S5 | (S5)         |    |
| 0  | 265          | 30 |
| 10 | 190          | 20 |
| 20 | 105          | 10 |
| 30 | 0            | 0  |

**Temmuz ayı (Aşama 4) hesaplamaları**: Temmuz ayına devreden stok miktarı, S4 =
0, 10, 20, 30, 40, 50 olabilir. Bir önceki aşamada olduğu gibi bir önceki aydan
devreden stok miktarı veri kabul edildiğinde, bu aşamanın karar değişkeni x4’ün
olası değerleri 0, 10, 20, 30, 40, 50 olur.

Haziran ayından stok devretmediğini varsayarsak, müşteri isteminin karşılanması
için, mağaza sahibinin vereceği sipariş miktarı en az 40 veya 50 olur. 40 birim
sipariş verilmesi durumunda toplam maliyet, 328 TL’si satın alma, 10 TL’si
sipariş, 265 TL’si Ağustos ayına stok devredilmemesi sonucu katlanılması gereken
maliyet olmak üzere 603 TL olacaktır. Devreden stok miktarı 40 olduğunda dönem
sonu stok miktarının sıfır olmasını sağlamak için en fazla 30, 50 olduğunda en
fazla 20 adet mal sipariş edilebilir.

Bu yaklaşımla belirlenen değerler aşağıdaki tabloda gösterilmiştir. Tablodaki
değerlerin hesaplanmasına örnek olması bakımından Haziran ayından devreden stok
miktarının 20 birim olduğunu düşünelim. Bu durumda Temmuz ayının isteminin
karşılanması için en az 20 mayo sipariş edilmesi kaçınılmazdır. Buna göre mağaza
sahibi en az 20 adet olmak üzere 30, 40 veya 50 adet mayo sipariş edebilir.
Sözgelimi sipariş miktarı 50 olduğunda Temmuz ayı başı itibariyle eldeki mayo
miktarı 70 adet olur. Bu miktarın 40 adetiyle Temmuz ayı istemi karşılanır, 30
adeti Ağustos ayına devredilir.

Buna göre, Temmuz ayı itibariyle toplam maliyet 400 TL’si satın alma, 10 TL’si
sipariş, 15 TL’si bulundurma sıfır TL’si Ağustos ayına 30 birim stok
devredilmesi maliyeti olmak üzere 425 TL olur. Temmuz ayı dinamik programlama
karar tablosu aşağıda gösterilmiştir.

# Tablo 12.23

|  x4 |  f4(x4, S4) = f(x4) + 0.5 x (S4 + x4 - 40) + (S5) |     |     |     |     |     |      |    |
|-----|---------------------------------------------------|-----|-----|-----|-----|-----|------|----|
| S4  | 0                                                 | 10  | 20  | 30  | 40  | 50  | (S4) |    |
| 0   | -                                                 | -   | -   | -   | 603 | 605 | 603  | 40 |
| 10  | -                                                 | -   | -   | 530 | 533 | 525 | 525  | 50 |
| 20  | -                                                 | -   | 455 | 460 | 453 | 425 | 425  | 50 |
| 30  | -                                                 | 370 | 385 | 380 | 353 | -   | 353  | 40 |
| 40  | 265                                               | 300 | 305 | 280 | -   | -   | 265  | 0  |
| 50  | 195                                               | 220 | 205 | -   | -   | -   | 195  | 0  |

(S4) = {f(x4) + 0.5 x (S4 + x4 - 40) + (S5)}

**Haziran ayı (Aşama 3) hesaplamaları**: Bu aşamanın durum değişkeni S3, Mayıs
ayından devreden stok miktarıdır. S3 = 0, 10, 20, 30, 40, 50 olabilir. Bir
önceki aydan devreden stok miktarı veri kabul edildiğinde bu aşamanın karar
değişkeni x3’ün olası değerleri 0, 10, 20, 30, 40, 50 olur. S3 ve x3’ün olası
değerlerinin göz önünde bulundurulması ve yineleme ilişkisinin kullanılmasıyla
hesaplanan üçüncü aşama değerleri Tablo 12.24’de gösterilmiştir.

# Tablo 12.24

| x3 |  f3(x3, S3) = f(x3) + 0.5 x (S3 + x3 - 50) + (S4) |     |     |     |     |      |      |    |
|----|---------------------------------------------------|-----|-----|-----|-----|------|------|----|
| S3 | 0                                                 | 10  | 20  | 30  | 40  | 50   | (S3) |    |
| 0  | -                                                 | -   | -   | -   | -   | 1013 | 1013 | 50 |
| 10 | -                                                 | -   | -   | -   | 941 |  940 |  940 | 50 |
| 20 | -                                                 | -   | -   | 868 | 868 |  845 |  845 | 50 |
| 30 | -                                                 | -   | 793 | 795 | 773 |  778 |  773 | 40 |
| 40 | -                                                 | 708 | 720 | 700 | 706 |  695 |  695 | 50 |
| 50 | 603                                               | 635 | 625 | 633 | 623 | 630  | 603  | 0  |

(S3) = {f(x3) + 0.5 x (S3 + x3 - 50) + (S4)}

**Mayıs ayı (Aşama 2) hesaplamaları**: Bu aşamanın durum değişkeni S2, Nisan
ayından bu aya devreden stok miktarıdır. S2 = 0, 10, 20, 30, 40, 50 olabilir.
Bir önceki aşamada olduğu gibi bir önceki aydan devreden stok miktarı veri kabul
edildiğinde bu aşamanın karar değişkeni olan x2’nin olası değerleri devreden
stok miktarı, üretim ve depolama kapasitesine bağlı olarak 0, 10, 20, 30, 40, 50
olur. S2 ve x2 değişkenlerinin olası değerlerinin göz önünde bulundurulması ve
yineleme ilişkisinin kullanılmasıyla hesaplanan ikinci aşama değerleri Tablo
12.25’de gösterilmiştir.

# Tablo 12.25

| x2 | f2(x2, S2) = f(x2) + 0.5 x (S2 + x2 - 20) + (S3) |      |      |      |      |      |      |    |
|----|--------------------------------------------------|------|------|------|------|------|------|----|
| S2 | 0                                                | 10   | 20   | 30   | 40   | 50   |      |    |
| 0  | -                                                | -    | 1203 | 1210 | 1193 | 1198 | 1193 | 40 |
| 10 | -                                                | 1118 | 1135 | 1120 | 1126 | 1125 | 1118 | 10 |
| 20 | 1013                                             | 1050 | 1045 | 1053 | 1053 | 1038 | 1013 | 0  |
| 30 |  945                                             |  960 |  978 |  980 |  966 | -    |  945 | 0  |
| 40 |  855                                             |  893 |  905 |  893 | -    | -    |  855 | 0  |
| 50 |  788                                             |  820 |  818 | -    | -    | -    |  788 | 0  |

= {f(x2) + 0.5 x (S2 + x4 - 40) + (S3)}

**Nisan ayı (Aşama 1) hesaplamaları**: Yıl sonuna devredilen stok miktarının
sıfır olması istendiğinden S1 = 0’dır. Bu durumda en az bu ayın istemi kadar (20
adet) mayo sipariş edilir. Buna göre x1 = 20, 30, 40, 50 olur. S1 ve x1
değişkenlerinin olası değerlerinin göz önünde bulundurulması ve yineleme
ilişkisinin kullanılmasıyla hesaplanan birinci aşama değerleri Tablo 12.26’da
gösterilmiştir. Birinci aşama tablosunun düzenlenmesiyle problem çözülmüş olur.

# Tablo 12.26

| x1 | f1(x1, S1) = f(x1) + 0.5 x (S1 + x1 - 20) +  |      |      |      |      |    |
|----|----------------------------------------------|------|------|------|------|----|
| S1 | 20                                           | 30   | 40   | 50   |      |    |
| 0  | 1383                                         | 1388 | 1361 | 1370 | 1361 | 40 |

= {f(x1) + 0.5 x (S1 + x1 - 40) + }

Birinci aşama tablosunun sütunundan görüldüğü gibi en düşük maliyet 1361 TL, =
40’dır. Yani, stok planlama döneminin ilk ayı olan Nisan ayında 40 birimlik mal
sipariş edilecektir. Nisan ayının istemi 20 birimdir. Buna göre, Mayıs ayına
devreden stok miktarı 20 birim olur. İkinci aşama karar tablosunun S2 = 20
satırından, Mayıs ayında sipariş verilmemesi, yani x = 0 olduğu kararlaştırılır.
Haziran ayının durumunu yansıtan S3 = 0’dır. S3 = 0 satırından Haziran ayında 50
birim sipariş verilmesi, yani x= 50 olduğu kararlaştırılır. Bu ayın istemi 50
birim olduğundan, Temmuz ayına devreden stok miktarı sıfır olur. S4 = 0
satırından x= 40 okunur. Bu durum, Ağustos ayına stok devrolmaması demek olup,
Ağustos için bu ayın istemi kadar sipariş verilerek toplam maliyetin en küçük
olması sağlanır.

### 12.3.5. Araç Yenileme Problemi

Araçların çoğu ilerleyen yaşlarına bağlı olarak artan bakım onarım harcamalarına
yol açarlar. Araçların bir süre kullanıldıktan sonra yenilenmeleri durumunda bu
masraflar azalır. Ancak bir aracın yenilenmesi başka bir maliyetin - araç
yenileme maliyeti - doğmasına neden olur. Araç sahibi, bu iki maliyet - bakım
onarım maliyeti ile araç satın alma maliyeti - arasında denge kurmak zorundadır.
En iyi denge, bu iki maliyet toplamının en küçük olduğu noktada ortaya çıkar. Bu
denge noktasını sağlayan plan ve programın geliştirilmesi problemi, araç
yenileme problemi olarak bilinir. Dinamik programlama bu tip problemlerin
çözümünde de kullanılabilir.

**Örnek 12.6**: Üç yaşını doldurduğunda kullanılmaz hale gelen bir aracın
doldurduğu yaşı esas olmak üzere, gerektirdiği bakım onarım masrafı ile hurda
fiyatı aşağıda verilmiştir. Bu araca 5 yıl için ihtiyacı olan araç sahibi 5
yıllık planlama dönemi için araç yenileme planını programlamak istemektedir.

Kolaylık olması bakımından araç yenileme maliyetinin 100 TL olduğu ve planlama
dönemi içinde değişmediği kabul edilmektedir. Aracın yenilenmesi veya
kullanılması kararı her yeni yılın başında verilmek zorundadır. Yenileme planını
belirleyiniz.

| Aracın Yaşı | Bakım Onarım Masrafı | Hurda  Fiyatı |
|-------------|----------------------|---------------|
| 0           | 8                    | -             |
| 1           | 10                   | 60            |
| 2           | 12                   | 50            |
| 3           | -                    | 30            |

**Çözüm 12.6**: Her zaman olduğu gibi önce dinamik programlamanın önemli
bileşenlerini tanımlayalım.

**Aşamalar**: Her yeni yılın başında yeni yaşını doldurmuş aracı yenilemek veya
kullanmaya devam etmek ile ilgili bir karar alınacaktır. Buna göre, 5 yıllık
planlama döneminin her yılı bir aşamayı oluşturur. Kısaca problem 5 aşamalıdır.
Planlama döneminin ilk yılında araç sıfır yaşında olduğundan aşamaların 0, 1, 2,
3, 4 olarak sıralanması uygun olur.

**Durum değişkenleri**: Herhangi bir aşamada alınacak karar doğrudan doğruya
aracın o aşamadaki yaşına bağlıdır. Herhangi bir aşamanın başında araç üç yaşını
doldurmuş ise tek bir karar; aracı hurda fiyatına elden çıkarıp yerine yenisini
almak söz konusudur. Araç üç yaşını doldurmamış ise hurda fiyatına satıp yerine
yenisini alma veya kullanmaya devam etme kararları arasından seçim yapılması
gerekir. O halde, aracın her aşamanın başındaki yaşı o aşamanın durum
değişkenidir.

**Karar değişkenleri**: Beş yıllık planlama döneminin ilk yılının başlangıcı
dışındaki her yeni yılın başında bir önceki yıldan devir alınan aracı yenileme
veya kullanmaya devam etme kararı alınacaktır. Karar değişkeni yenileme kararı
için sıfır, kullanmaya devam etme kararı için 1 olarak tanımlanabilir.

0 Yenile

1 Kullan

n = 0, 1, 2, 3, 4

**Kazanç fonksiyonu**: Kazanç fonksiyonu herhangi bir aşamada verilen karar
sonrası gerçekleşen toplam kazancı (maliyeti) yansıtmalıdır. Buna göre,

ht = t yaşındaki aracın hurda değeri

bt = t yaşındaki aracın bakım-onarım masrafı

olmak üzere, aşama n için toplam maliyet fonksiyonu aşağıdaki gibi olur.

xn = 1 için rn(Sn, xn) = bt n = 0, 1, 2, 3, 4; t = 0, 1, 2

Xn = 0 için rn(Sn, xn) = -ht + 100 + b0 n = 0, 1, 2, 3, 4; t = 0, 1, 2

Buna göre aşama aşama biriken toplam maliyet şöyledir:

fn(Sn, xn) = rn(Sn, xn) + (Sn + xn)

Yineleme denklemi aşağıda gösterilmiştir.

(Sn) = {fn(Sn, xn)}

Araç 5 yıl için gerekli olduğundan, beşinci yılın sonunda yaşı ne olursa olsun
hurda değerine satılacaktır. Aracın beşinci yılın sonundaki yaşı S5 ile
gösterildiğinde S5 için kazanç (negatif maliyet) f(S5) = -holur. S5 için üç
değer (1, 2, 3) söz konusudur. S5 = 1, 2, 3 için f(S5) şöyledir:

f(1) = -60, f(2) = -50, f(3) = -30

Son yıla gelindiğinde aracın yaşı 1, 2 veya 3 olur. Araç 1 veya 2 yaşında ise ya
yenilenmeden ya da yenilendikten sonra 1 yıl kullanıp satılır. Araç 3 yaşında
ise tek seçenek aracı yenilemek ve o yılın sonunda 1 yaşını dolduran aracı elden
çıkarmaktır. Bu açıklamalar her aşama için geçerli olacak biçimde aşağıdaki gibi
genellenebilir.

fn(3) = -h3 + 100 + b0 + f(1) (xn = 0)

\-h2 + 100 + b0 + f(1) (xn = 0)

b2 + f(3) (xn = 1)

fn(2) =

\-h1 + 100 + b0 + f(1) (xn = 0)

b1 + f(2) (xn = 1)

fn(1) =

**Beşinci yıl (n = 4)**: Planlama döneminin sonuna (son yıl) gelindiğinde bir
önceki yıldan teslim alınan araç 1, 2 veya 3 yaşında olabilir. Araç 1 veya 2
yaşındaysa hurda fiyatına satıp yerine yenisini alma veya 1 yıl daha kullanma
kararı alınabilir. Araç 3 yaşındaysa alınacak tek bir karar (yenile) vardır.
Yenileme kararı için sıfır, yenilememe için 1 kullanıldığı dikkate alındığında
x4 = 0 veya 1 olur. Bu kararlara karşılık gelen maliyetlerin hesaplanmasıyla
düzenlenen beşinci yıl karar tablosu aşağıda gösterilmiştir.

# Tablo 12.27

| x4 S4 | f(S4, x4) = r4(S4, x4) + f(S4 + x4) |  f(S4)         |  x  |   |
|-------|-------------------------------------|----------------|-----|---|
|       | 0                                   | 1              |     |   |
| 1     | -60 + 100 + 8 – 60 = -12            | 10 – 50 = -40  | -40 | 1 |
| 2     | -50 + 100 + 8 – 60 = -2             | 12 – 30 = -40  | -18 | 1 |
| 3     | -30 + 100 + 8 – 60 = 18             | -              | 18  | 0 |

f(S4) =

**Dördüncü yıl (n = 3)**: Dördüncü yılın başında araç 1, 2 veya 3 yaşındadır.
Araç 1 veya 2 yaşındaysa yenileme veya 1 yıl daha kullanma, 3 yaşındaysa
yenileme kararı alınacaktır. Yani, x3 = 0 veya 1 olur (bkz. Tablo 12.28).

# Tablo 12.28

| x3 S3 | f(S3, x3) = r3(S3, x3) + f(S3 + x3) |  f(S3)        |  x  |   |
|-------|-------------------------------------|---------------|-----|---|
|       | 0                                   | 1             |     |   |
| 1     | -60 + 100 + 8 – 40 = -12            | 10 – 18 = -8  | -8  | 1 |
| 2     | -50 + 100 + 8 – 40 = -2             | 12 + 18 = 30  |  18 | 0 |
| 3     | -30 + 100 + 8 – 40 = 18             | -             | 38  | 0 |

f(S4) =

**Üçüncü yıl (n = 2)**: Üçüncü yılın başında araç 1 veya 2 yaşındadır. Aracın
yaşına ve alınan karara göre hesaplanan değerler aşağıda gösterilmiştir.

# Tablo 12.29

| x2 S2 | f(S2, x2) = r2(S2, x2) + f(S2 + x2) |  f(S2)        |  x |      |
|-------|-------------------------------------|---------------|----|------|
|       | 0                                   | 1             |    |      |
| 1     | -60 + 100 + 8 – 8 = 40              | 10 + 18 = 28  | 28 | 1    |
| 2     | -50 + 100 + 8 – 8 = 50              | 12 + 38 = 50  | 50 | 0, 1 |

f(S2) =

**İkinci yıl (n = 1)**: İkinci yılın başında araç 1 yaşındadır. Aracın yaşına ve
alınan karar bağlı olarak hesaplanan değerler Tablo 12.30’da gösterilmiştir.

# Tablo 12.30

| x1 S1 | f1(S1, x1) = r1(S1, x1) + f(S1 + x1) |  f(S1)        |  x |   |
|-------|--------------------------------------|---------------|----|---|
|       | 0                                    | 1             |    |   |
| 1     | -60 + 100 + 8 + 28 = 76              | 10 + 50 = 60  | 60 | 1 |

f(S1) =

**Birinci yıl (n = 0)**: Planlama döneminin başında tek bir karar (satın alma)
söz konusu olduğundan, bu yılın karar tablosu aşağıdaki gibi düzenlenecektir.

# Tablo 12.31

| x0 S0 | f0(S0,x0) = r0(S0, x0) |  f(S0) |  x |
|-------|------------------------|--------|----|
|       | 0                      |        |    |
| 0     | 100 + 8 + 60 = 168     | 168    | 0  |

İlk aşama karar tablosunun düzenlenmesiyle problem çözülmüş olur. İlk aşama
karar tablosundan başlayıp geriye doğru gidildiğinde iki tane en iyi çözümün
bulunduğu görülebilir. En iyi çözümler aşağıda gösterilmiştir.

Birinci en iyi çözüm: x = 0, x = 1, x= 1, x= 0, x= 1, (x= 0)

İkinci en iyi çözüm: x = 0, x = 1, x= 0, x= 1, x= 1, (x= 0)

Birinci en iyi çözümün belirlenmesinde izlenen adımları kısaca özetleyelim.
Planlama döneminin başında satın alınan araç 1 yıl sonra (ikinci yılın başında)
1 yaşını tamamlamış olacağından, S1 = 1 olur. n = 1 karar tablosunun S1 = 1
satırından x = 1 olduğu, yani aracın 1 yıl daha kullanılması gerektiği görülür.
Bu durumda üçüncü yılın başında araç 2 yaşını tamamlamış olur. Üçüncü yıl
tablosunun S2 = 2 satırı incelendiğinde iki alternatif kararla karşılaşılır.
Birincisi 2 yaşını dolduran aracı bir yıl daha kullanmak (x= 1) böylece dördüncü
yılın başında 3 yaşında bir araca sahip olmak, ikincisi aracı yenilemek (x= 0)
böylece dördüncü yılın başında 1 yaşında araca sahip olmak. İlk kararın
uygulandığını (x= 1) düşünelim. Bu durumda S3 = 3 olur. Üçüncü aşama tablosunun
S3 = 3 satırından x= 0 okunur. Yani araç yenilenecektir. Bu durumda S4 = 1 olur
ve S4 = 1 satırından x= 1 okunur.

### 12.4. SÜREKLİ DURUM DİNAMİK PROGRAMLAMA

Şimdiye kadar durum ve karar değişkenlerine ait değerlerin kolayca
belirlenebildiği problemler üzerinde durulmuştur. Söz konusu değerlerin kolayca
belirlenebilmelerinin nedeni bunların sadece tamsayı değerler almalarıdır. Pek
çok problemde bu kısıt ortadan kalkar ve hem durum hem de karar değişkeni
herhangi bir değer aralığından değer alabilirler. Bu tip problemler sürekli
durum dinamik programlama problemleri kapsamında değerlendirilir. Değişkenlerin
kesikli oldukları varsayımının ortadan kalkması durumunda uygun değerlerin tek
tek ele alınması imkansız olduğundan matematiğin türev dahil tüm araçlarının
kullanılması gerekir. Bu konu aşağıdaki örnek problemle açıklanacaktır.

**Örnek 12.7([^1])**: Mevsimsel dalgalanmalardan etkilenen bir işte kullanılan
makineleri çalıştıran operatörlerin kiralanmaları zor, eğitimleri pahalıdır. Bu
nedenle yönetici, ölü mevsimlerde operatörlerin işine geçici olarak son vermeyi
düşünmemekle birlikte canlı mevsimlerdeki kadar ödeme yapmayı da göze
alamamaktadır. Yönetici mesai dışı çalışmanın da karşısındadır. Bütün çalışmalar
müşteri siparişine dayandığından ölü mevsimlerde stok oluşturulması da söz
konusu değildir. Mevsimlere göre operatör gereksinimi aşağıdaki gibidir.

[^1]: Frederic S. Hillier, Gerald J. Lieberman, Operations Research, San
    Fransisco, Holden Day Inc., 1974, s.260.

| Mevsim      | : İlkbahar | Yaz | Sonbahar | Kış | İlkbahar | Yaz | … |
|-------------|------------|-----|----------|-----|----------|-----|---|
| Operatör S. | : 255      | 220 |  240     | 200 |  255     | 220 | … |

Operatör sayılarının yukarıdaki sayıların altına düşmemesi istenmektedir.
Fazladan istihdam edilen her bir operatör 2000 TL tutarında ek harcamaya yol
açmaktadır. Kiralama ve işten çıkarma maliyetlerinin toplamı ard arda gelen iki
mevsimdeki istihdam değerleri arasındaki farkın karesinin 200 katına eşittir.
Operataör sayısı tamsayı olmak zorunda değildir. Yöneticinin amacı toplam
maliyetin en küçük olmasını sağlayacak istihdam düzeylerini belirlemektir.
Mevsimlere göre operatör sayılarını bulunuz.

**Çözüm 12.7**: Mevsimlere göre operatör sayıları incelendiğinde, istihdam
düzeyinin 255’in üstüne çıkmasının anlamsız olduğu görülür. Buna göre,
ilkbahardaki operatör sayısı 255 olur. Bu durumda problem, ilkbahar dışındaki
mevsimlerin istihdam düzeylerinin belirlenmesi problemine dönüşür. Öncelikle
problemin önemli bileşenlerini tanımlayalım.

**Aşamalar**: Mevsimlere göre istihdam düzeyinin belirleneceği bu problemde her
mevsim bir aşamayı oluşturur. Belirsiz gelecek söz konusu olduğundan, problemin
sınırsız sayıda aşaması vardır. Bununla birlikte, her yıl aynı mevsimle
başladığından ve ilkbahar istihdamı bilindiğinden ilkbahar son mevsim olmak
üzere 4 mevsimlik tek bir dönemin dikkate alınması yeterli olur. Buna göre
problemin 4 aşamalı olduğu kabul edilebilir.

**Karar değişkenleri**: xn (n = 1, 2, 3, 4) n’inci aşamanın istihdam düzeyi
olarak tanımlanabilir. Son aşamadaki her durum için karar değişkeninin en iyi
değerinin diğer aşamalar dikkate alınmaksızın bilinmesi ve belirlenebilmesi için
ilkbahar son aşamayı oluşturmalıdır. Diğer mevsimlerin istihdam düzeyinin
belirlenebilmesi için izleyen mevsimdeki maliyet dikkate alınmalıdır. Kısaca x1,
x2, x3 ve x4 = 255 sırasıyla yaz, sonbahar, kış ve ilkbaharın istihdam
düzeyleridir.

**Durum değişkeni**: Bir önceki mevsimde istihdam edilen operatör sayısı,
kendisini izleyen mevsimin durumu ile ilgili tüm bilgiyi sağlar. Bu nedenle
herhangi bir aşamanın durum değişkeni (Sn), kendisinden önce gelen aşamanın
istihdam düzeyi ile eksiksiz tanımlanır.

**Geçiş fonksiyonu**: Geçiş fonksiyonu şöyledir:

Sn = xn-1 (x0 = x4 = 255)

**Kazanç fonksiyonu**: Herhangi bir mevsimdeki maliyet, o mevsimde alınan karar
(xn) ile bir önceki mevsimin istihdam düzeyine bağlıdır. n’inci aşamanın en
düşük istihdam düzeyi rn olsun. Buna göre; r1 = 220, r2 = 240, r3 = 200, r4 =
255 olur.

Problemin amacı, ri xi 255, i = 1, 2, 3, 4 kısıtı altında, aşağıdaki bağıntıyı
gerçekleştirecek xi değerlerini belirlemektir

Enk

Buna göre herhangi bir aşama (n = 1, 2, 3, 4) için ri xi 255 olmak üzere fn(Sn,
xn), aşağıdaki gibi yazılır.

fn(Sn, xn) = + enk

Sn = xn-1 olduğu dikkate alındığında toplam maliyetin en küçük değeri f(Sn),
aşağıdaki gibi açıklanır.

f(Sn) = fn(Sn, xn)

Buna göre fn(Sn, xn) aşağıdaki gibi yazılabilir.

fn(Sn, xn) = + f(xn)

İlkbahardan sonra oluşacak maliyetin analizle ilgisi olmadığından, f(S5) = 0
olmalıdır. Problemin temel yapısı Şekil 12.9’da özetlenmiştir.

# Şekil 12.9

f’leri birbirine bağlayan yineleme denklemi aşağıda verilmiştir.

f(Sn) = { + f(xn)}

Özetle dinamik programlama yaklaşımıyla f(S4), f(S3), f(S2), f(255)
fonksiyonları ile bunları sağlayan xn değerleri belirlenecektir.

**İlkbahar (n = 4)**: Halihazırda belirlendiği gibi, x= 255’dir. Buna göre son
aşama karar tablosu aşağıdaki gibi düzenlenir.

# Tablo 12.32

| x4 S4      | f(S4)          | x   |
|------------|----------------|-----|
| 200 S4 255 | 200(255 – S4)2 | 255 |

**Kış (n = 3)**: İlkbaharın istihdamı 255, kışın gerektirdiği operatör sayısı
200 olduğuna göre yineleme denklemi aşağıdaki gibi açıklanır.

f(S3) = f3(S3, x3)

=

f(S3)’ü belirleme problemi aşağıda gösterildiği gibi grafik yaklaşımıyla
çözülebilirse de daha sonra açıklanacağı gibi, çözüme daha hızlı ulaşmayı
sağlayan türev yaklaşımının kullanılması daha uygun olur.

**Şekil 12.10**

f3(S3,x3)’ü en küçükleyen x3 değeri ilgili fonksiyonun x3’e göre alınan
türevinin sıfıra eşitlenmesiyle bulunur. Bu işlem aşağıda gösterilmiştir.

= 400(x3 – S3) + 2000 – 400(255 – x3)

= 400(2x3 – S3 – 250) = 0 x3 =

x3 = olarak belirlenen çözümün en iyi ve uygun olup olmadığının incelenmesinde
f3(S3,x3)’ün ikinci türevinin işareti ile çözümün verilen aralığa (200 x3 255)
düşüp düşmediği araştırılmalıdır. Fonksiyonun ikinci türevi aşağıda
gösterilmiştir.

= 800

İkinci türev pozitif olduğundan, belirlenen çözüm f3(S3, x3)’ü en küçükler.
Ayrıca, 200 255 olduğundan çözüm uygundur. x’ü kullanarak f(S3)’ü hesaplayalım.
Yerine koyma ile f(S3) aşağıdaki gibi elde edilir.

f(S3) = 200+ 200+ 2000

elde edilir. Eşitlik üzerinde gerekli işlemlerin yapılmasından sonra f aşağıdaki
gibi bulunur.

f(S3) = 50+ 50 + 1000(S3 –150)

Üçüncü (n = 3) aşama karar tablosu aşağıda gösterilmiştir.

# Tablo 12.33

| x3 S3      | f(S3)                                          | x |
|------------|------------------------------------------------|---|
| 240 S3 255 | 50(250 – S3)2 + 50(260 – S3)2 + 1000(S3 – 150) |   |

**Sonbahar (n = 2)**: En yüksek istihdam düzeyinin 255, sonbahardaki operatör
sayısının 240 olduğunun dikkate alınması ve kış için gerçekleştirilen işlemlerin
sonbahar için tekrarlanmasıyla f2(S2, x2), 240 x2 255 aşağıdaki gibi elde
edilir.

f2(S2, x2) = 200+ 2000(x2 – r2) + f(x2)

= 200+ 2000(x2 – 240) + 50+ 50+ 1000(x2 – 150)

Bu aşamanın amacı 240 x2 255 olmak koşuluyla f(S2) = f2(S2, x2)

olmasını sağlayacak x2 değerinin bulunmasından ibarettir. f2(S2, x2)’nin x2’ye
göre birinci türevi ile gerçekleştirilen diğer işlemler aşağıda gösterilmiştir.

= 400(x2 – S2) + 2000 – 100(250 – x2) – 100(260 – x2) + 1000

= 200(3x2 – 2S2 –240) = 0 x2 =

Şimdi de ikinci türevin işaretini ve çözümün 240 x2 255 aralığına düşüp
düşmediğini inceleyelim.

= 600 \> 0 olduğundan, S2 \> 240 ise fonksiyon x2 = noktasında en küçük olur.

S2 \< 240 ise çözüm uygun değildir.

240 x2 255 için \> 0 olduğundan x2 = 240, f2(S2, x2)’i en küçük yapar.

Karar tablosunun oluşturulması için S2 240 ve S2 \< 240 aralıkları itibariyle
x2’nin belirlenen değerleri f2(S2, x2)’ye yerleştirilmeli ve f(S2)
hesaplanmalıdır.

Yukarıdaki işlemlerin tamamlanması ve gerekli düzenlemelerin yapılmasıyla
ulaşılan sonuçlarla düzenlenen ikinci aşama (Sonbahar) karar tablosu aşağıda
gösterilmiştir.

Tablo 12.34

| x2 S2      | f(S2)       | x   |
|------------|-------------|-----|
| 220 S2 240 | 200+ 115000 | 240 |
| 240 S2 255 |             |     |

**Yaz (n = 1)**: Yaz mevsiminin yineleme denklemi aşağıda gösterilmiştir.

f1(S1, x1) = 200+ 2000(x1 – r1) + f(x1)

Bilindiği gibi r1 = 220’dir. Buna göre uygun çözüm bölgesi 220 x1 255 olur.
f(x1), 220 x1 240 ve 240 x1 255 aralıklarında farklılık gösterdiğinden, f1(S1,
x1) bu aralıklar için ayrı ayrı tanımlanmalıdır.

f1(S1, x1), 220 x1 240 için aşağıdaki gibi elde edilir.

f1(S1, x1) = 200+ 2000(x1 – 220) + 200+ 115000

240 x1 255 için f1(S1, x1) aşağıda gösterildiği gibidir.

f1(S1, x1) = 200+ 2000(x1 – 220) + [2

\+ + 30(3x1 – 575)]

Önce x1 240 durumunu inceleyelim. x1 240 için tanımlanan f1(S1, x1)’in birinci
türevi aşağıda gösterilmiştir.

= 400(x1 – S1) + 2000 – 400(240 – x1)

= 400(2x1 – S1 –235)

S1 (ilkbahar istihdamı) = 255 olduğu bilindiğinden tüm x1 240 için,

= 800(x1 – 245) \< 0 elde edilir.

Sonuç olarak f1(S1, x1), x1 240 aralığının x1 = 240 noktasında en küçük olur.

240 x1 255 olduğunda, f1(S1, x1)’in birinci türevi şöyle olur.

= 400(x1 – S1) + 2000 -

= (4x1 – 3S1 – 225)

= 0 eşitliğinin x1’e göre çözümünden, x1 = elde edilir. Bütün x1’ler için \> 0
olduğundan, f1(S1, x1) noktasında en küçük olur. S1 = 255 değeri ’e
yerleştirildiğinde x1 = 247.5 olarak hesaplanır. Özetle, f1(S1, x1) fonksiyonu
240 x1 255 aralığındaki en küçük değerine x1 = 247.5 noktasında ulaşmaktadır. Bu
aralık, f1(S1, x1)’i x1 240 aralığında en küçükleyen, x1 = 240’ı da
kapsadığından x1 = 247.5 olarak belirlenen çözüm f1(S1, x1)’i 220 x1 255
aralığında en küçükler. Buna göre, f(S1 = 255) aşağıdaki gibi hesaplanacaktır.

f(S1 = 255) = 200- 2000(247.5 – 220)

\+

= 185000

n = 1 için yapılan tüm işlemler aşağıdaki tabloda özetlenmiştir.

Tablo 12.35

| x1 S1 | f(S1)  | x     |
|-------|--------|-------|
| 255   | 185000 | 247.5 |

Buna göre en iyi çözüm, yani en iyi istihdam politikası x= 247.5, x= 245 (= ),
x= 247.5 (= ), x= 255 olarak belirlenmiş olur. Dört mevsim için toplam maliyet
185000 TL olarak hesaplanmıştır.

### 12.5. OLASILIKSAL DİNAMİK PROGRAMLAMA

Şimdiye kadar herhangi bir aşamanın durum değişkeni ile bu aşamada alınan
kararın, sonraki aşamanın durumunu ve karar sonucu ortaya çıkan toplam kazancını
kesin çizgilerle belirlemeye imkan veren dinamik programlama üzerinde
durulmuştur. Bu nitelikteki dinamik programlama, deterministik dinamik
programlamadır. Uygulamada daha çok, incelenen aşamanın durumunun belirsizlik
göstermesi buna bağlı olarak verilecek kararın kesin çizgilerle belirlenememesi
durumuyla karşılaşılmaktadır. Araştırmacıların sıklıkla karşılaştığı
problemlerin pek çoğunda durum ve karar kesinlikle belirlenebilse bile alınan
karar sonrası ortaya çıkan sonuç veya sonraki aşamanın durumu tam olarak
belirlenememektedir. Sözgelimi, Örnek 12.5’deki stok kontrol probleminde aylara
göre istemin bilindiği varsayılmıştır. Oysa, istemi rasgele değişken olarak
düşünmek daha gerçekçi olur. İncelenen dönemin durumu (başlangıç stok miktarı)
ve karar (incelenen dönemin sipariş miktarı) bilinse bile, izleyen dönemin
durumu ve alınan karar sonucu ortaya çıkan getiri (burada maliyet) rasgele
olabilir. Bu kesimde ilk olarak, incelenen aşama için hesaplanan kazancın
rasgele değişken olması durumunda izlenecek yaklaşım açıklanacak, daha sonra
incelenen aşamanın durumu ve bu aşamada alınan kararın sonraki aşamadaki durumu
tam olarak belirlemede yetersiz kaldığı dinamik programlama problemleri üzerinde
durulacaktır. Bu iki durumdan birinin veya her ikisinin birden söz konusu olduğu
dinamik programlama olasılıksaldır.

Olasılıksal dinamik programlamada karar vericinin amacı, genellikle belirli bir
büyüklükle ilgili beklenen değerin en büyük veya en küçük olmasını sağlayan
değişken değerlerini belirlemektir. İlk olarak sonraki aşamanın durumu ile
ilgili herhangi bir belirsizliğin bulunmadığı, belirsizliğin incelenen aşamanın
sonuç değerlerinde ortaya çıktığı durum üzerinde duralım.

**Örnek** **12**.**8**: Bir yatırımcının yatırım yapıabileceği üç yatırım
faaliyeti ve bunlar için ayırdığı 4 milyon TL’si vardır. Yatırımların net
bugünkü değerleri (I1, I2, I3) ve bunların gerçekleşme olasılıkları aşağıdaki
gibidir. 4 milyon TL’yi yatırım faaliyetleri arasında öyle paylaştırınız ki,
toplam net bugünkü değer en büyük olsun.

Tablo 12.36

| Yatırım Faaliyeti | Yatırım Miktarı (000)  |  Olasılık       |                  |                  |
|-------------------|------------------------|-----------------|------------------|------------------|
|                   | 1                      | P(I1 = 2) = 0.6 | P(I1 = 4) = 0.3  | P(I1 = 5) = 0.1  |
| Proje 1           | 2                      | P(I1 = 4) = 0.5 | P(I1 = 6) = 0.3  |  P(I1 = 8) = 0.2 |
|                   | 3                      | P(I1 = 6) = 0.4 | P(I1 = 7) = 0.5  |  P(I1 =10) = 0.1 |
|                   | 4                      | P(I1 = 7) = 0.2 | P(I1 = 9) = 0.4  |  P(I1 =10) = 0.4 |
|                   | 1                      | P(I2 = 1) = 0.5 | P(I2 = 2) = 0.4  | P(I2 = 4) = 0.1  |
| Proje 2           | 2                      | P(I2 = 3) = 0.4 | P(I2 = 5) = 0.4  | P(I2 = 6) = 0.2  |
|                   | 3                      | P(I2 = 4) = 0.3 | P(I2 = 6) = 0.3  | P(I2 = 8) = 0.4  |
|                   | 4                      | P(I2 = 3) = 0.4 | P(I2 = 8) = 0.3  | P(I2 = 9) = 0.3  |
|                   | 1                      | P(I3 = 0) = 0.2 | P(I3 = 4) = 0.6  | P(I3 = 5) = 0.2  |
| Proje 3           | 2                      | P(I3 = 4) = 0.4 | P(I3 = 6) = 0.4  | P(I3 = 7) = 0.2  |
|                   | 3                      | P(I3 = 5) = 0.3 | P(I3 = 7) = 0.4  | P(I3 = 8) = 0.3  |
|                   | 4                      | P(I3 = 6) = 0.1 | P(I3 = 8) = 0.5  | P(I3 = 9) = 0.4  |

**Çözüm 12.8**: Bu problem, net bugünkü değerlerin (I1, I2, I3) belirsiz oluşu
dışında, Örnek 12.2’deki yatırım problemine çok benzemektedir. Önceden olduğu
gibi ilk olarak problemin önemli bileşenlerini tanımlayalım.

**Aşamalar**: Projelere göre yatırım miktarları belirlenmek istenmektedir. Buna
göre, her bir proje bir aşama olmak üzere problem üç aşamalıdır.

**Durum** **değişkenleri**: Yatırım için ayrılan para miktarı kısıtlıdır. Bu
nedenle yatırım kararını belirleyen eldeki nakit miktarıdır.

Başlangıç değeri 4 milyon olan nakit miktarı her aşamada; 0, 1, 2, 3 veya 4
değerini alır. Deterministik dinamik programlamadaki gibi durum değişkeni
değerleri bilinmektedir.

**Karar değişkenleri**: Alınacak üç karar (x1, x2, x3) vardır. Üç projenin her
birine ne kadarlık yatırım yapılacağına karar verilecektir.

**Kazanç fonksiyonu**: Herhangi bir aşamada, içinde bulunulan duruma bağlı
olarak alınacak kararın değerini yansıtan kazanç fonksiyonu, n’inci projeye
yapılan yatırımın beklenen net bugünkü değeri (bn(Sn, xn))’dir. Deterministik
dinamik programlamadan farklı olarak, sonuç değerleri belirsizdir.

**Geçiş fonksiyonu**: n’inci aşamada alınan karar sonucu (n + 1) aşamasının
durumunu yansıtan geçiş fonksiyonu aşağıda gösterilmiştir. Sn, Sn+1, xn daha
önce tanımlandıkları gibidir.

Sn+1 = Sn - xn

Bu açıklamalar doğrultusunda problemin dinamik programlama formülasyonu, yani
yineleme denklemi şöyledir:

(Sn) = bn(Sn, xn) + (Sn - xn) n = 1, 2, 3

Beklenen net bugünkü değerin en büyüklenmesinin amaçlandığı problemde öncelikle,
yatırım miktarına bağlı olarak her bir projenin sağlayacağı beklenen net bugünkü
değerleri hesaplayalım.

Örnek olması bakımından, 1 nolu yatırım projesine 1 milyon TL yatırıldığını
düşünelim. Bu durumda beklenen net bugünkü değer Tablo 12.36’nın ilk satırının
dikkate alınmasıyla aşağıdaki gibi hesaplanır.

NBD(I1 = 1) = P(I1 = 2) x 2 + P(I1 = 4) x 4 + P(I1 = 5) x 5

= (0.6) x 2 + (0.3) x 4 + (0.1) x 5

= 2.9 milyon TL

Bu yaklaşımla hesaplanan beklenen net bugünkü değerler aşağıdaki tabloda
gösterilmiştir.

#### Tablo 12.37

|  Proje | Yatırım Miktarı |  NBD |  Proje | Yatırım  Miktarı |  NBD |  Proje | Yatırım  Miktarı |  NBD |
|--------|-----------------|------|--------|------------------|------|--------|------------------|------|
|        | 1               | 2.9  |  **2** | 1                | 1.7  |  **3** | 1                | 3.4  |
| **1**  | 2               | 5.4  |        | 2                | 4.4  |        | 2                | 5.4  |
|        | 3               | 6.9  |        | 3                | 6.2  |        | 3                | 6.7  |
|        | 4               | 9.0  |        | 4                | 6.3  |        | 4                | 8.2  |

Çözüme yatırım yapılacak tek bir projenin kaldığı aşamadan başlayalım.

**Proje 1 (n = 3)**: Yatırım miktarının kararlaştırılacağı tek bir projenin
kaldığı bu aşamada eldeki nakit miktarı en az sıfır (paranın tamamı diğer
projelere harcanmışsa) en fazla 4 milyon TL (paranın tamamı bu projeye
ayrılmışsa) olur. Birinci projeye yapılan yatırım miktarına bağlı olarak
hesaplanan net bugünkü değerlerle oluşturulan üçüncü aşama karar tablosu aşağıda
gösterilmiştir. (S3) = b3(S3, x3) olarak tanımlanmıştır.

# Tablo 12.38

| x3 S3 |  (S3) |   |
|-------|-------|---|
| 0     | 0     | 0 |
| 1     | 2.9   | 1 |
| 2     | 5.4   | 2 |
| 3     | 6.9   | 3 |
| 4     | 9.0   | 4 |

**Proje 2**: n = 2 aşamasında yatırım yapılacak iki proje (proje 2 ve proje 3)
kaldığında eldeki nakit miktarı en az sıfır en fazla 4 milyon TL olur. Paranın
bu iki proje arasında paylaştırılmasıyla hesaplanan toplam beklenen net bugünkü
değerler ile diğer bilgiler aşağıdaki karar tablosunda gösterilmiştir.

# Tablo 12.39

| x2 | f2(S2, x2) = b2(S2, x2) + f - x2) |     |     |      |     |      |   |
|----|-----------------------------------|-----|-----|------|-----|------|---|
| S2 | 0                                 | 1   | 2   | 3    | 4   | (S2) |   |
| 0  | 0                                 | -   | -   | -    | -   | 0    | 0 |
| 1  | 2.9                               | 1.7 | -   | -    | -   | 2.9  | 0 |
| 2  | 5.4                               | 4.6 | 4.4 | -    | -   | 5.4  | 0 |
| 3  | 6.9                               | 7.1 | 7.3 | 6.2  | -   | 7.3  | 2 |
| 4  | 9.0                               | 8.6 | 9.8 | 9.1  | 6.3 | 9.8  | 2 |

(S2) = b2(S2, x2) + (S2 - x2)

**Proje 3**: n = 1 aşamasında, yani 4 milyon TL’nin paylaştırılacağı 3 proje
varken, S1 = 4 olur. 4 milyon TL’nin projeler arasında paylaştırılması sonucu
hesaplanan değerlerle oluşturulan n = 1 karar tablosu aşağıda gösterilmiştir.

# Tablo 12.40

| x1 | f1(S1, x1) = b1(S1, x1) + (4 - x1) |      |      |     |     |      |   |
|----|------------------------------------|------|------|-----|-----|------|---|
| S1 | 0                                  | 1    | 2    | 3   | 4   | (S1) |   |
| 4  | 9.8                                | 10.7 | 10.8 | 9.6 | 8.2 | 10.8 | 2 |

(S1) = b1(S1, x1) + (4 - x1)

(S1) bulunduğundan problem çözülmüştür. n = 1 karar tablosundan = 2 olduğu, yani
üçüncü projeye 2 milyon TL yatırılması gerektiği belirlenir. Kalan 2 milyon
TL’nin dağıtımı için n = 2 karar tablosunun S2 = 2 satırından, = 0 okunur.
Böylece ikinci projeye yatırım yapılmaması kararlaştırılır. Kalan 2 milyon
TL’nin dağıtımı için n = 3 aşama tablosunun S3 = 2 satırından x = 2 okunur.
Özetle, en büyük beklenen net bugünkü değere (10.8 milyon) 4 milyon TL’nin 1 ve
3 nolu projelere eşit biçimde paylaştırılmasıyla ulaşılmaktadır.

Şimdi de incelenen aşamada alınan karar sonrası, yeni aşamadaki durumun
belirsizlik gösterdiği problemler üzerinde duralım. Bu koşullarda yeni aşamanın
durum değişkeninin mümkün değerleri olasılıklar yardımıyla belirlenir.

Olasılık dağılımının belirlenmesinde incelenmekte olan aşamanın durumu ve bu
aşamada alınan karar kullanılır. İncelenen aşamayı (n) izleyen aşamanın (n + 1)
durum değişkeninin alması muhtemel değerlerinin sayısı N olsun. Bu muhtelif
değerlerin gerçekleşme olasılıklarını, p1, p2, ..., pN ile gösterelim. n
aşamasında alınan karara bağlı olarak bundan sonraki aşamada i ile gösterilen
duruma dönüşümün amaç fonksiyonuna katkısı Ci (i = 1, 2, ..., N) olsun. Sonuçta
ortaya çıkan temel yapı Şekil 12.11’deki gibi açıklanabilir. Söz konusu şeklin,
her bir aşamanın bütün mümkün durumları ve kararları için çizilmesi sonucunda
ortaya çıkan grafiğe karar ağacı denir. Karar ağacı problemin çözülmesinde büyük
kolaylıklar sağlar. Bu nedenle problem çok kapsamlı değilse karşılık gelen karar
ağacının çizilmesi uygun olur.

Olasılıksal yapı gereği fn(Sn, xn) ile (Sn+1) arasındaki ilişkinin belirlenmesi
deterministik dinamik programlamadakinden daha karmaşıktır. fn(Sn, xn) ile
(Sn+1) arasındaki ilişkinin kesin şekli amaç fonksiyonunun şekline bağlıdır.

Şekil 12.11

Yukarıdaki açıklamalar çerçevesinde, amacın aşamaların katkıları toplamının
beklenen değerinin en küçüklenmesi olduğunu düşünelim. Bu durumda fn(Sn, xn),
n’inci aşamadaki durum ve karar sonrası ortaya çıkan en küçük değerli beklenen
toplamdır. Bu toplam aşağıdaki gibi açıklanabilir.

fn(Sn, xn) =

Burada, aşağıda tanımlandığı gibidir.

fn+1(Sn+1, xn+1)

Örnek 12.9 bu durumla ilgilidir.

**Örnek 12.9**: Bir firma gelecek üç ay için üretimini planlamak istemektedir.
Ocak, Şubat ve Mart ayları için istem düzeyleri 1/3 olasılıkla 1, 2/3 olasılıkla
2 adet olarak tahminlenmiştir. Üretim maliyeti üretim miktarına bağlı olup, x \>
0 için C(x) = 8 + 2x bağıntısıyla hesaplanmaktadır. Firma aylara göre üretim
kapasitesi 4 birimdir. Depolama olanakları sınırlı olup her ay en fazla 3 birim
stoklanabilmektedir. Bulundurma maliyeti birim başına 1 TL’dir. Stok tükenmesi
söz konusu değildir. Mart ayı sonunda elde kalan ürün tanesi 6 TL’den
satılmaktadır. Ocak ayı başındaki stok miktarı 1 adettir. Üç aylık dönem
itibariyle beklenen net maliyetin en küçük olmasını gerçekleştirecek üretim
politikasını belirleyiniz.

**Çözüm 12.9**: Şimdiye kadar çözülen problemlerde olduğu gibi, önce problemin
önemli bileşenlerini tanımlayalım.

**Aşamalar**: Üç aylık dönemin her ayı bir aşamayı oluşturur.

**Karar değişkenleri**: Aylar itibariyle üretim miktarının belirlenmesi
istendiğinden karar değişkeni (xn) üretim miktarı olarak tanımlanır. İstem
miktarı kesin olmadığından xn’de kesin değildir.

**Durum değişkenleri**: Üretim miktarı devreden stok miktarına bağlı olduğundan
n’inci aşamanın durum değişkeni bir önceki aydan devreden stok miktarı olarak
tanımlanabilir. İstem ve üretim miktarları rasgele olduklarından stok miktarı da
rasgeledir.

**Geçiş fonksiyonu**: Durum değişkenleri arasındaki ilişkiyi yansıtan geçiş
fonksiyonu aşağıdaki gibi açıklanabilir.

Sn+1 = 1/3 (Sn + xn - 1) + 2/3 (Sn + xn - 2) n = 1, 2, 3

Burada, So = S1 = Başlangıç stok düzeyi = 1, S4 = Dönem sonu stok düzeyi = 0,
Sn, Sn+1, xn daha önce tanımlandıkları gibidir.

**Kazanç fonksiyonu**: Herhangi bir aşamada (n) alınan belirli bir karar sonrası
ortaya çıkan toplam maliyeti (üretim + bulundurma) yansıtan kazanç fonksiyonu
aşağıda gösterilmiştir.

fn(Sn, xn) = C(xn) + (1/3) x (1) x (Sn + xn - 1) + (2/3) x (1) x (Sn + xn - 2)

Bu açıklamalar doğrultusunda yineleme denklemi n, n+1, ..., 3 dönemlerinin en
küçük beklenen net maliyeti olmak üzere aşağıdaki gibi yazılabilir.

**=**

Ocak ve Şubat aylarında ıskarta değerine satış söz konusu olmadığından, bu iki
ayın her biri için maliyet aşağıdaki gibidir.

= 0 n = 1, 2 için

Bu açıklamalardan sonra son aydan (Mart) başlayarak problemi çözelim.

**Mart ayı (n = 3)**: Mart ayı net maliyeti, beklenen üretim maliyeti ile
beklenen bulundurma maliyetleri toplamının beklenen ıskarta değerinden farkına
eşittir. Şubat ayından devreden stok miktarı S3 olsun. Mart ayı üretim miktarı
x3 olmak üzere beklenen üretim maliyeti C(x3) = 8 + 2x3 olur. Mart ayı istem
miktarı 1 olduğunda (S3 + x3 - 1) adet, 2 olduğunda (S3 + x3 - 2) adet ürün
stoklanacaktır. İstemin 1 olması olasılığı 1/3, 2 olması olasılığı 2/3
olduğundan, bulundurma maliyetinin beklenen değeri aşağıdaki gibi olur.

Bu ayın sonunda elde kalan mal ıskarta değerine elden çıkarılacağından, bu
satıştan umulan kazanç (negatif maliyet), aşağıdaki gibi açıklanır.

6S3 + 6x3 - 10

Stok tükenmesine izin verilmediğinden, S3 + x3 2 veya x3 2 - S3 olmalıdır.
Benzer şekilde, Mart sonundaki stok miktarı en fazla 3 adet olacağından, istemin
1 olarak gerçekleşmesi durumuyla bağlantılı olarak, S3 + x3 -1 3 veya x3 4 - S3
sağlanmalıdır. n = 1, 2 için yineleme denklemi , xn (üretim miktarı) olmak
üzere, aşağıdaki gibi düzenlenir.

Burada xn {0, 1, 2, 3, 4} ve (2 - Sn) xn (4 - Sn) olarak tanımlanmıştır.

Olasılıksal dinamik programlamadaki aritmetik işlemlerin sayısı fazla
olduğundan, tüm işlemlerin karar tablosunda gösterilmesi, deterministik dinamik
programlamadaki kadar kolay değildir. n = 3 için gerçekleştirilen işlemler Tablo
12.41’de gösterilmiştir.

# Tablo 12.41

|     |     |           | Beklenen Maliyet             | )                          |                        |             |
|-----|-----|-----------|------------------------------|----------------------------|------------------------|-------------|
|  S3 |  x3 | C(x3) (i) | Bulundurma  (ii) (S3+x3-5/3) | Iskarta (iii) (6S3+6x3-10) | Toplam  (i + ii - iii) | )           |
| 3   | 0   | 0         | 3+0-5/3 = 4/3                |  18+0-10 = 8               |  0+4/3-8 = -20/3\*     | (3) = -20/3 |
| 3   | 1   | 10        | 3+1-5/3 = 7/3                |  18+ 6-10 = 14             |  10+7/3-14 = -5/3      |  (3) = 0    |
| 2   | 0   | 0         | 2+0-5/3 = 1/3                |  12+ 0-10 = 2              |  0+1/3-2 = -5/3\*      | (2) = -5/3  |
| 2   | 1   | 10        | 2+1-5/3 = 4/3                |  12+ 6-10 = 8              |  10+4/3-2 = 10/3       |  (2) = 0    |
| 2   | 2   | 12        | 2+2-5/3 = 7/3                |  12+12-10 = 14             |  12+7/3-14 = 1/3       |             |
| 1   | 1   | 10        | 1+1-5/3 = 1/3                |  6+ 6-10 = 2               |  10+1/3-2 = 25/3       | (1) = 7/3   |
| 1   | 2   | 12        | 1+2-5/3 = 4/3                |  6+12-10 = 8               |  12+4/3-8 = 16/3       |  (1) = 3    |
| 1   | 3   | 14        | 1+3-5/3 = 7/3                |  6+18-10 = 14              |  14+7/3-14 = 7/3\*     |             |
| 0   | 2   | 12        | 0+2-5/3 = 1/3                |  0+12-10 = 2               |  12+1/3-2 = 31/3       | (0) = 13/3  |
| 0   | 3   | 14        | 0+3-5/3 = 4/3                |  0+18-10 = 8               |  14+4/3-8 = 22/3       |  (0) = 4    |
| 0   | 4   | 16        | 0+4-5/3 = 7/3                |  0+24-10 = 14              |  16+7/3-14 = 13/3\*    |             |

Hata yapma riskini ortadan kaldırmak için Tablo 12.41’i deterministik dinamik
programlama karar tablosu olarak düzenleyelim. Söz konusu düzenlemeyle elde
edilen karar tablosu aşağıda gösterilmiştir.

# Tablo 12.42

| x3 S3 |  (S3) |   |
|-------|-------|---|
| 0     | 13/3  | 4 |
| 1     |  7/3  | 3 |
| 2     |  -5/3 | 0 |
| 3     | -20/3 | 0 |

Şubat (n = 2) ve Ocak (n = 1) ayları için Mart ayının yineleme denklemine benzer
bir denklem oluşturulabilir.

xn, n aşamasının üretim miktarı olmak üzere toplam maliyetin beklenen değeri
aşağıdaki eşitlikle açıklanır.

C(xn) + (1/3)(1)(Sn + xn - 1) + (2/3)(1)(Sn + xn - 2)

Ocak ve Şubat ayları için ıskarta değerine satışın söz konusu olmadığı
unutulmamalıdır. Zamanın 1/3’ünde istem 1 birim olacağından izleyen aya devreden
stok miktarı 1/3 olasılıkla (Sn + xn - 1)’e eşittir. Bu durumda, n + 1, n + 2,
..., 3 aylarının beklenen maliyeti "(Sn + xn - 1) " olur. Benzer şekilde, n + 1
dönemine devreden stok miktarının (Sn + xn - 2)’ye eşit olması olasılığı
2/3’dür. Buna göre; n + 1, n + 2, ..., 3 ayları için beklenen maliyet şöyle
olur:

(Sn + xn - 2) = (1/3)(Sn + xn - 1) + (2/3)(Sn + xn - 2)

Sonuç olarak n = 1, 2 için yineleme denklemi,

olarak elde edilir.

xn {0, 1, 2, 3, 4} için (2 - Sn) xn (4 - Sn) koşulunun geçerli olması
gerektiğini akılda tutarak n = 2 aşamasına, yani Şubat ayına geçelim. Şubat
ayının en iyi üretim politikasını belirlemek amacıyla gerçekleştirilen işlemler
Tablo 12.43’de gösterilmiştir.

# Tablo 12.43

|     |     |            | Beklenen Maliyet            |                                                |                    |           |
|-----|-----|------------|-----------------------------|------------------------------------------------|--------------------|-----------|
|  S2 |  x2 |  C(x2) (i) | Bulundurma (S2+x2-5/3) (ii) | Gelecekteki (iii) (S2 + x2 - 1) +(S2 + x2 - 2) |  Toplam (i+ii+iii) | (S2) (S2) |
| 3   | 0   |  0         | 4/3                         |  1/3(-5/3) + 2/3(7/3) = 1                      | 7/3\*              | (3)=7/3   |
| 3   | 1   | 10         | 7/3                         |  1/3(-20/3) + 2/3(-5/3) = -30/9                | 9                  |  (3)=0    |
| 2   | 0   |  0         | 1/3                         |  1/3(7/3) + 2/3(13/3) = 33/9                   | 36/9=4\*           |  (2)=4    |
| 2   | 1   | 10         | 4/3                         |  1/3(-5/3) + 2/3(7/3) = 1                      | 7/312.3            |  (2)=0    |
| 2   | 2   | 12         | 7/3                         |  1/3(-20/3) + 2/3(-5/3) = -30/9                | 99/9=1             |           |
| 1   | 1   | 10         | 1/3                         |  1/3(7/3) + 2/3(13/3) = 33/9                   | 126/9=14           |  (1)=13   |
| 1   | 2   | 12         | 4/3                         |  1/3(-5/3) + 2/3(7/3) = 1                      | 43/3=14.3          |  (1)=3    |
| 1   | 3   | 14         | 7/3                         |  1/3(-20/3) + 2/3(-5/3) = -30/9                | 17/9=13\*          |           |
| 0   | 2   | 12         | 1/3                         |  1/3(7/3) + 2/3(13/3) = 33/9                   | 144/9=16           |  (0)=15   |
| 0   | 3   | 14         | 4/3                         |  1/3(-5/3) + 2/3(7/3) = 1                      | 9/3=16.3           |  (0)=4    |
| 0   | 4   | 16         | 7/3                         |  1/3(-20/3) + 2/3(-5/3) = -30/9                | 35/9=15\*          |           |

Tablo 12.43’ün son sütun değerleriyle oluşturulan karar tablosu aşağıda
gösterilmiştir.

# Tablo 12.44

| x2 S2 |  (S2) |   |
|-------|-------|---|
| 0     | 15    | 4 |
| 1     | 13    | 3 |
| 2     | 4     | 0 |
| 3     | 7/3   | 0 |

Planlama döneminin ilk ayına devreden stok miktarının 1 olduğu bilindiğinden
Ocak ayı (n = 1) karar tablosu aşağıdaki gibi düzenlenir.

# Tablo 12.45

|      |      |            | Beklenen Maliyet                 |                                               |                         |           |
|------|------|------------|----------------------------------|-----------------------------------------------|-------------------------|-----------|
|   S1 |   x1 |  C(x1) (i) | Bulundurma  (S1 + x1 - 5/3) (ii) | Gelecekte (iii) (f(1+ x1 -1)) +(f(1+ x1 -2))  |  Toplam  (i + ii + iii) | (S1) (S1) |
| 1    | 1    | 10         | 1/3                              |  1/3(13) + 2/3(15) = 43/3                     |  74/3= 24.66            | (1) =19.7 |
| 1    | 2    | 12         | 4/3                              |  1/3(4) + 2/3(13) = 28/3                      |  68/3= 22.67            | (1)=3     |
| 1    | 3    | 14         | 7/3                              |  1/3(7/3) + 2/3(4) = 31/9                     |  178/9=19.7\*           |           |

Diğer aylarda olduğu gibi Ocak ayının olasılıksal dinamik programlama karar
tablosunu, deterministik dinamik programlama karar tablosu olarak düzenleyelim.

# Tablo 12.46

|  x1 |  f1(S1, x1) |       |       |       |    |
|-----|-------------|-------|-------|-------|----|
| S1  | 1           |  2    | 3     | f(S1) |  x |
| 1   | 24.66       | 22.67 | 19.77 | 19.77 | 3  |

f(S1) bulunduğundan problem çözülmüştür. Artık en iyi çözümü belirleyebiliriz.

Tablo 12.46’nın x başlıklı sütunundan görüldüğü gibi Ocak ayı üretim miktarı 3
birimdir. Bu ayın istemi 1 veya 2 adettir. İstem miktarının 1 adet olması
durumunu inceleyelim. Ocak ayında gerçekleşen istem 1 adet olursa Şubat ayına
devreden stok miktarı 3 (= 1 + 3 - 1) birim olur.

Şubat ayına devreden stok miktarı 3 birim olduğunda Şubat ayına ait karar
tablosunun S2 = 3 satırından x= 0 okunur. Böylece Şubat ayında üretim
yapılmaması kararlaştırılır.

Üretimin söz konusu olmadığı Şubat ayında istem 1 veya 2 olur. Şubat ayındaki
istemin 1 birim olarak gerçekleştiğini düşünelim. Bu istemin Ocak ayından
devreden stoktan karşılanmasıyla, Mart ayına devreden stok miktarı 2 (= 3 - 1)
birim olur.

Mart ayına devreden stok miktarı 2 olduğunda Mart ayı için düzenlenen karar
tablosunun S3 = 2 satırı incelenmelidir. Bu tablonun S3 = 2 satırının
incelenmesinden = 0 olarak belirlenir. Bu açıklamalar Ocak, Şubat ve Mart
aylarındaki istem miktarlarının 1 birim olması durumuna aittir. İstem miktarları
değiştiğinde üretim miktarlarının da değişeceği açıktır.

Aşağıdaki karar ağacı istem miktarına bağlı olarak gerçekleştirilmesi gereken
üretim politikalarını gözler önüne sermektedir. Aylara göre istem miktarları
ağacın dalları üzerinde, o ay için izlenen üretim politikası düğüm içlerinde
gösterilmiştir. Mart ayı sonunda elde kalan ürün miktarı S4 ile gösterilmiştir.
Ağacın dalları dikkatle izlendiğinde sekiz farklı üretim politikasının söz
konusu olduğu görülecektir. Bu politikalardan bazıları aşağıda listelenmiştir.

S1 = 1, x1 = 3 (D1 = 1); S2 = 3, x2 = 0 (D2 = 1); S3 = 2, x3 = 0 (D3 = 1); S4 =
1

S1 = 1, x1 = 3 (D1 = 1); S2 = 3, x2 = 0 (D2 = 1); S3 = 2, x3 = 0 (D3 = 2); S4 =
0

S1 = 1, x1 = 3 (D1 = 1); S2 = 3, x2 = 0 (D2 = 2); S3 = 1, x3 = 3 (D3 = 1); S4 =
3

S1 = 1, x1 = 3 (D1 = 1); S2 = 3, x2 = 0 (D2 = 2); S3 = 1, x3 = 3 (D3 = 2); S4 =
2

S1 = 1, x1 = 3 (D1 = 2); S2 = 2, x2 = 0 (D2 = 1); S3 = 1, x3 = 3 (D3 = 1); S4 =
3

S1 = 1, x1 = 3 (D1 = 2); S2 = 2, x2 = 0 (D2 = 1); S3 = 1, x3 = 3 (D3 = 1); S4 =
3

S1 = 1, x1 = 3 (D1 = 2); S2 = 2, x2 = 0 (D2 = 1); S3 = 1, x3 = 3 (D3 = 1); S4 =
3

S1 = 1, x1 = 3 (D1 = 2); S2 = 2, x2 = 0 (D2 = 1); S3 = 1, x3 = 3 (D3 = 1); S4 =
3

S1 = 1, x1 = 3 (D1 = 2); S2 = 2, x2 = 0 (D2 = 1); S3 = 1, x3 = 3 (D3 = 1); S4 =
3

**Şekil**

# PROBLEMLER

**1**. Ortaköy’ü Emirgan’a bağlayan yollar ve bunların uzaklıkları aşağıdaki
gibidir. Ortaköy-Emirgan arasındaki en kısa yolu belirleyiniz.

**2**. Hakkari’den yurtdışına çıkmak isteyen bir kişinin önce Ankara veya
İstanbul’a gitmesi gerekmektedir. Hakkari’yi Ankara ve İstanbul’a bağlayan
yollar ve bu yolların uzunlukları aşağıda gösterilmiştir. Hakkari’den Ankara
veya İstanbul’dan hangisine gidilirse katedilen mesafe en kısa olur?

**3**. Yatırım yapılabilecek 3 yatırım seçeneği ve toplam 12 milyon TL vardır.
Yatırım miktarına bağlı olarak seçeneklerin sağladıkları kazançlar aşağıdaki
kazanç fonksiyonlarından hesaplanmaktadır. Yatırım miktarları tamsayı olmak
üzere yatırım politikasını belirleyiniz.

r1(x1) = 6 + 2x1 (x1 \> 0) r1(0) = 0

r2(x2) = 3 + 3x2 (x2 \> 0) r2(0) = 0

r3(x3) = 8 + 4x3 (x3 \> 0) r3(0) = 0

**4**. 3 nolu problemdeki yatırımcı parasını xi 0 olmak üzere yatırmak isterse
nasıl bir yatırım politikası izlemelidir?

**5**. 10 tonluk bir kamyonla üç farklı mal taşınmak istenmektedir. Aşağıda
gösterildiği gibi malların birim ağırlıkları (ton) ve sağladıkları kârlar (TL)
birbirinden farklıdır. Kârı en büyüklemek için 10 tonluk taşıma kapasitesinin üç
mal arasında nasıl paylaştırması gerektiğini bulunuz.

| Mal | Ağırlık | Kâr |
|-----|---------|-----|
| A   | 3       | 45  |
| B   | 5       | 65  |
| C   | 4       | 50  |

**6**. Aylık üretimi 6 ton olan bir fabrika ürettiği ürünleri 4 ayrı kuruluş
aracılığıyla satmaktadır. Fabrika ürettiğini satmakta yani, stok
bulundurmamaktadır. Kuruluş yerinin büyüklüğü, fabrikaya uzaklığı, reklam, vb.
nedenlerden ötürü farklı kuruluşlardan farklı kazançlar elde edilmektedir.
Fabrika 6 tonluk üretimini kuruluşlar arasında nasıl paylaştırırsa kârı en
yüksek olur? Gönderilen miktara (ton) göre her kuruluştan sağlanan kazançlar
(TL) aşağıda gösterilmiştir.

| Kazanç |    |    |    |    |
|--------|----|----|----|----|
| Miktar | K1 | K2 | K3 | K4 |
| 0      | 0  | 0  | 0  | 0  |
| 1      | 2  | 3  | 4  | 4  |
| 2      | 3  | 5  | 7  | 6  |
| 3      | 6  | 10 | 8  | 8  |
| 4      | 7  | 8  | 7  | 7  |
| 5      | 8  | 6  | 5  | 5  |
| 6      | 10 | 12 | 10 | 6  |

**7**. Bir firma Ocak, Şubat, Mart ve Nisan aylarındaki üretimini planlamak
istemektedir. Firma, Ocak ve Şubat aylarında en fazla 5, Mart ve Nisan aylarında
en fazla 6 birim üretebilmektedir. Üretim maliyeti üretim miktarına bağlı olup,
C(x) = 6 + 2x olarak tahmin edilmiştir. Aylar itibariyle istem miktarı 4 birim
olarak öngörülmüştür. Firmanın stoklama olanakları sınırlı olup her ay en fazla
5 birim stoklayabilmektedir. Stok bulundurma maliyeti birim başına 0.5 TL’dir.
Nisan ayı bitiminde elde ürün kalmaması arzu edilmektedir. Toplam maliyetin en
küçük olmasını sağlayacak üretim planını oluşturunuz.

**8**. Halihazırdaki marketler zincirine yeni marketler eklemeyi düşünen
yönetici bu iş için 3 bölge belirlemiştir. Market büyüklüğü olarak 3 seçenek
vardır. Kuruluş yeri ve market büyüklüğüne bağlı olarak kuruluş maliyeti ve
beklenen gelirler aşağıda gösterilmiştir. Sermaye miktarı 30 TL olduğuna göre
market kurulacak bölgeler ile market büyüklüklerini belirleyiniz.

|       | Büyük   | Orta  | Küçük   |       |         |       |
|-------|---------|-------|---------|-------|---------|-------|
| Bölge | Maliyet | Gelir | Maliyet | Gelir | Maliyet | Gelir |
| 1     | 15      | 3.6   | 8       | 1.8   | 6       | 1.6   |
| 2     | 18      | 4.2   | 6       | 2.0   | 5       | 1.4   |
| 3     | 10      | 5.0   | 8       | 2.6   | 4       | 1.2   |

**9**. Üç temel parçadan oluşan bir elektronik aygıt tasarlanmaktadır. Üç parça
birbirine seri bağlanacaktır. Bağlama seri olacağından parçalardan herhangi
birinin bozulması aygıtın bozulmasına sebep olmaktadır. Aygıtın güvenilirliği
parçalara paralel olarak bağlanacak ek parçalarla artırılabilmektedir. Her
parçaya 1, 2 veya 3 adet paralel parça eklenebilmektedir. Tasarım için ayrılan
sermaye 8 TL’dir. Eklenen paralel parça sayısına bağlı olarak yapılan harcama ve
temel parça güvenilirlikleri aşağıda gösterilmiştir. Her temel parçaya eklenecek
parça sayısını bulunuz.

| Parça  | I. Temel Parça | II. Temel Parça | III. Temel Parça |        |         |        |
|--------|----------------|-----------------|------------------|--------|---------|--------|
| Sayısı | Maliyet        | Güven.          | Maliyet          | Güven. | Maliyet | Güven. |
| 0      | 0              | 0               | 0                | 0      | 0       | 0      |
| 1      | 1              | 0.5             | 2                | 0.4    | 3       | 0.6    |
| 2      | 3              | 0.7             | 3                | 0.6    | 5       | 0.8    |
| 3      | 5              | 0.8             | 4                | 0.8    | 6       | 0.9    |

**10**. Dört farklı alanda bilgi sahibi olmak isteyen bir üniversite öğrencisi
dört farklı bölümden 10 seçmeli ders belirlemek istemektedir. Bunun için her
bölümden en az bir ders almak zorunda olduğunu ayrıca, bir bölümden belirli bir
sayının üstünde ders seçmesi durumunda o derslerin kendisine fazla katkısının
olmayacağını düşünmektedir. Öğrenci öğrenme kapasitesini, her bölümden aldığı
ders sayısının bir fonksiyonu olarak ölçmüş ve aşağıdaki tabloyu oluşturmuştur.
Öğrencinin her bölümden alacağı ders sayısını bulunuz.

|       | Ders Sayısı |    |    |    |    |    |    |    |     |     |
|-------|-------------|----|----|----|----|----|----|----|-----|-----|
| Bölüm | 1           | 2  | 3  | 4  | 5  | 6  | 7  | 8  | 9   | 10  |
| I     | 25          | 50 | 60 | 80 | 20 | 50 | 50 | 10 | 90  | 30  |
| II    | 30          | 50 | 70 | 90 | 45 | 80 | 10 | 20 | 100 | 40  |
| III   | 30          | 40 | 50 | 80 | 60 | 90 | 20 | 40 | 70  | 50  |
| IV    | 10          | 20 | 30 | 40 | 50 | 60 | 70 | 80 | 90  | 100 |

**11**. Üç ayrı yerde marketi olan bir kişi marketlerin süt gereksinimini büyük
bir çiftlikten karşılamaktadır. Marketlerin günlük toplam süt istemi 60
litredir. Çiftlikten litresi 1 TL’ye alınan süt, marketlerde litresi 2 TL’den
satılmaktadır. Gününde satılmayan süt çiftliğe 0.5 TL’ye iade edilmektedir.
Günlük süt isteminin ne olacağını kesin olarak bilinmemekle birlikte geçmiş
dönem deneyimlerinden aşağıdaki bilgiler elde edilmiştir.

Satın alınan 60 litre sütü marketler arasında günlük net kazancı en büyükleyecek
şekilde paylaştırınız.

| Market   | İstem | Olasılık |
|----------|-------|----------|
|          | 10    | 0.50     |
| Market1  | 20    | 0.20     |
|          | 30    | 0.30     |
|          | 10    | 0.40     |
| Market 2 | 20    | 0.50     |
|          | 30    | 0.10     |
|          | 10    | 0.30     |
| Market 3 | 20    | 0.40     |
|          | 30    | 0.40     |

**12**. Bir firma Mart, Nisan Mayıs ayları için üretim politikasını planlamak
istemektedir. Firma her ayın başında üretim karar vermek durumundadır. Üretim
maliyeti üretim miktarına bağlı olup, x \> 0 için C(x) = 10 + 2x olarak tahmin
edilmiştir. İşletmenin üretim kapasitesi sınırlı olup her ay en fazla 5 birim
mal üretebilmektedir. Firmanın depolama olanakları sınırlı olup her ay en fazla
4 birim mal stoklayabilmektedir. Stok bulundurma maliyeti birim başına 1 TL’dir.
Dönem başı ve dönem sonu stok düzeyi sıfır olmalıdır. Aylar itibariyle ürün
istemi eşit olasılıkla 1, 2, veya 3 olarak tahminlenmiştir.

Firmanın amacı istemleri zamanında karşılamak ve toplam maliyeti en
küçüklemektir. En uygun üretim planını tasarlayınız.

**13**. AC üretim işletmesi dönem başı ve dönem sonu stok miktarı sıfır olmak
koşuluyla 4 dönem için üretimini planlamak istemektedir. Firma her dönem en
fazla 5 birim üretebilmekte ve her dönem en fazla 4 birim stoklayabilmektedir.
Üretim maliyeti üretim miktarına bağlı olup, C(x) = 5 + 3x (x \> 0) olarak
tahmin edilmiştir.

Dönemlere göre istem miktarı ve bulundurma maliyeti aşağıdaki tabloda
gösterilmiştir. Buna göre en düşük maliyeti üretim planını saptayınız.

|  Dönem |  İstem | Bulundurma  Maliyeti |
|--------|--------|----------------------|
| 1      | 2      | 1                    |
|  2     | 3      | 2                    |
| 3      | 3      | 1                    |
| 4      | 2      | 2                    |

**14**. Üç ayrı atölyede üretilen bir ürünün kusurlu olma olasılıkları atölye
sırasıyla, 0.40, 0.70 ve 0.50’dir. Her atölyeye 1 veya 2 yeni eleman alındığında
söz konusu ürünün kusurlu olma olasılığı azalmaktadır. Aşağıdaki verilere göre
alınacak 2 yeni elemanı atölyeler arasında, toplam kusurlu olma oranının en
küçük olmasını sağlayacak biçimde dağıtınız.

| Yeni          | Atölye |      |      |
|---------------|--------|------|------|
| Eleman Sayısı | A      | B    | C    |
| 0             | 0.40   | 0.70 | 0.50 |
| 1             | 0.30   | 0.40 | 0.30 |
| 2             | 0.20   | 0.10 | 0.20 |

**15**. 20 kg taşıma hakkına sahip olan bir kişi değer ve ağırlıkları aşağıdaki
gibi olan 4 çeşit eşya arasından toplam değeri en büyük yapacak seçimi
gerçekleştirmek istemektedir. 20 kg taşıma kapasitesi kısıtına göre hangi
eşyalardan kaçar tane alınmasının uygun olacağını belirleyiniz.

| Eşya     | Değer | Ağırlık |
|----------|-------|---------|
| Kazak    | 13    | 2       |
| Pantalon | 12    | 2       |
| Kitap    | 23    | 3       |
| Radyo    | 24    | 4       |

**16**. Üretimini mevsimlik planlayan bir işletmenin üretim kapasitesi sınırlı
olup her mevsim en fazla 8 birim üretilebilmektedir. Depolama olanakları sınırlı
olup en fazla 5 birim stoklanabilmektedir. Bulundurma maliyeti birim başına 2
TL’dir. Üretim maliyeti aşağıda gösterildiği gibidir.

C(x) = 2x + 10, x 4

= 0 x \< 4

Mevsimlere göre istemler sırasıyla 4, 3, 7, 7’dir. Üretim miktarı 4’den az
olduğunda üretim kendiliğinden durmaktadır. Dönem sonu ve dönem başı stok
düzeyinin en az 1, en fazla 2 birim olması istenmektedir. En düşük maliyetli
üretim planını saptayınız.

**17**. Bir yatırımcı elindeki 10 milyon TL’yi yıllık getirileri belirli 4
yatırım seçeneği arasında paylaştırmak istemektedir. Rasyonel davranmak isteyen
yatırımcı her seçeneği değerlendirmek istemektedir. Bunun için her seçeneğe en
az 1 milyon TL yatırım yapılması gerekmektedir. Yatırım miktarları milyonun
tamsayı katları olmak üzere 10 milyon TL yatırım seçenekleri arasında nasıl
dağıtılsın ki yatırımcının toplam kazancı en büyük olsun. Her seçenekten
sağlanabilecek kazançlar yatırım miktarının fonksiyonu olarak aşağıda
tanımlanmıştır.

r1(x1) = 8 + 2x1 x1 \> 0

r2(x2) = 3 + 4x2 x2 \> 0

r3(x3) = 6 + 3x3 x3 \> 0

r4(x4) = 10 + x4 x4 \> 0

r1(0) = r2(0) = r3(0) = r4(0) = 0

**18**. Elinde 1 milyon TL’si bulunan bir yatırımcı parasını iki ayrı yatırım
seçeneğinden birine yatırmak durumundadır. Yatırımların getirisi belirsizlik
göstermektedir. Her bir yatırım seçeneğinin sağlayacağı kazanç ve bunlara
ilişkin olasılıklar aşağıdaki gibi belirlenmiştir. Her yıl tutarı 1 milyon TL
olan tek bir yatırım yapılacaktır. Biriken para başka bir şekilde
değerlendirilmektedir. 3 yılın sonunda eldeki paranın en büyük olmasını
sağlayacak yatırım planını saptayınız.

| Yatırım  | Kazanç | Olasılık |
|----------|--------|----------|
| A        | 0      | 0.4      |
|          | 2      | 0.6      |
| B        | 1      | 0.9      |
|          | 2      | 0.1      |

**19**. Şu anda 2 yaşında olan bir makinenin gelecek dört yıl içindeki yenilenme
politikası geliştirilmek istemektedir. 5 yaşını dolduran makine kesinlikle
yenilenecektir. Makine yenileme maliyeti 200 TL’dir. Makinenin bitirdiği yaş
esas olmak üzere bakım onarım masrafı ve hurda fiyatı aşağıdaki tabloda
gösterilmiştir. Yenileme programını belirleyiniz.

| Yaş | Bakım-Onarım | Hurda Değeri |
|-----|--------------|--------------|
| 0   | 15           | -            |
| 1   | 20           | 150          |
| 2   | 28           | 100          |
| 3   | 35           | 90           |
| 4   | 40           | 75           |
| 5   | 45           | 50           |

**20**. Halihazırda 100 koyunu olan bir çiftçi her yılın sonunda koyunlardan
kaçını satıp kaçını besleyeceğine karar vermek zorundadır. Çiftçi izleyen üç
yılı programlamak istemektedir. i yılında satılan bir koyun çiftçiye 10 TL kâr
sağlamaktadır. i yılında satılmayıp beslemeye alınan bir koyunun i + 1 yılında
satılması durumunda kâr 20 TL olmaktadır. Üç yılın sonunda tüm koyunlar
satılacaktır. Yıllar itibariyle kaç koyun satılması gerektiğini bulunuz.
