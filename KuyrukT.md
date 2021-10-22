*ONÜÇÜNCÜ BÖLÜM*

# *KUYRUK KURAMI*

**13.1. GİRİŞ**

Günlük yaşantımızın en önemli özelliklerinden birisi, değişik yer ve zamanlarda
farklı nedenlerle beklemek zorunda oluşumuzdur. Sinema veya PTT gişeleri önünde,
otobüs veya dolmuş duraklarında, trafik ışıklarında bekleyişlerimiz yaşantımızın
ayrılmaz bir parçası olarak sürüp gitmektedir. Kuşkusuz, beklemek yalnızca
insana özgü bir olay değildir. Merkezi işlem biriminde çalıştırılmayı bekleyen
bilgisayar programları, limana girmek için bekleyen deniz taşıtları, alana inmek
için bekleyen uçaklar, onarılmayı bekleyen makineler, tüketilmek için stokta
bekleyen ürünler, temiz bir hat bekleyen telefon aboneleri beklemenin yalnızca
insana özgü bir olay olmadığını açıklamaktadır. Çeşitli örneklerle açıklanan
beklemelerin oluşum nedeni, hizmet isteyen birimlerin isteklerinin anında
karşılanamamasıdır.

Bekleme hattı kuramı olarak da bilinen kuyruk kuramının temeli, Danimarka’lı A.
K. Erlang tarafından atılmıştır. Erlang’ın 1909 yılında Kopenhag otomatik
telefon sistemindeki telefon konuşmalarının oluşturduğu telefon trafiği
kargaşasını çözümlemek amacıyla başlattığı çalışmalar zamanla, bekleme hattı
oluşturan tüm problemlerin çözümü için geliştirilmiş ve kullanılmıştır.
1950’lere kadar yalnızca telefon problemlerinin çözümünde kullanılan çalışmalar,
1950’lerle birlikte ulaştırmada, stoklamada, bankalarda, hastanelerde kısaca,
her türlü fiziksel akışın oluştuğu mekanlardaki bekleme olaylarına
uygulanmıştır. Ekonomik koşulların giderek zorlaştığı günümüzde, ürün ve/veya
hizmet üreten işletmelerin önemli sorunlarından bir tanesi, müşterilerine en
etkin biçimde hizmet verecek sistemi oluşturabilmektir. Kuyruk kuramı hem hizmet
verme maliyetini, hem de hizmetlerinin anında karşılanmasını bekleyen
müşterilerini dikkate almak zorunda olan yöneticilere olumlu öneri ve sonuçlar
sunmaktadır. İşletme yararları ile müşteri yararlarının dengelenmesi kuyruk
kuramının yarattığı kuyruk modelleri ile gerçekleştirilebilmektedir.

**13.2. KUYRUK SİSTEMİNİN GENEL YAPISI**

Kuyruk sisteminin genel yapısı Şekil 13.1’de gösterilmiştir. Şekilde açıklandığı
gibi bir kuyruk sistemi; 1. Müşteri kaynağı, 2. Kuyruk, 3. Servis sistemi, 4.
Sistemi terkeden müşteriler olmak üzere belli başlı dört elemandan oluşan bir
bütündür.

**Şekil 13.1**

Kuyruk sistemine gelmesi olası birimlerin oluşturduğu topluluğa "müşteri
kaynağı" denir. Servis birimine gelen varlık yani müşteri, servisi bir süre
meşgul eden ve isteği karşılandığı anda sistemden ayrılan herhangi bir şey
olabilir. Müşteri, insan veya madde olmak zorunda değildir. İş, sipariş, mesaj
veya benzeri herhangi bir şey olabilir. Servis birimi, müşterinin isteği
karşılanıncaya değin meşgul ettiği şeydir. İnsan, makine veya başka bir şey
olabilir. Bir kuyruk sisteminin eksiksiz tanımlanabilmesi için bazı özellikleri
belirlenmelidir. Kuyruk sisteminin çeşitli elemanları izleyen kesimde ayrıntılı
biçimde incelenecek ve bazı belirli sistemler için matematiksel sonuçlar
sunulacaktır. Sistemin elemanları aşağıda açıklanmıştır.

**1.** **Geliş Süreci**: Giriş süreci olarak da bilinen bu süreç, müşterilerin
servis almak için sisteme ne tür bir kaynaktan ve nasıl geldiklerini açıklar.
Müşteri kaynağından kuyruk sistemine gelişler farklı esasların dikkate
alınmasıyla aşağıdaki gibi gruplandırılır.

a. *Geliş kaynağına göre*: Müşteri kaynağı, aynı cinsten birimlerin oluşturduğu
bir topluluktur. Örneğin, bir malın potansiyel müşterilerinin oluşturduğu
topluluk o mal için tanımlanan kuyruk sisteminin geliş kaynağıdır. Geliş
kaynağındaki birim sayısı sonlu ya da sonsuz olabilir. Potansiyel müşteri sayısı
yeterince büyükse geliş kaynağı sonsuz kabul edilir. Sonsuz geliş kaynaklı
kuyruk sistemlerinin analizi daha kolaydır.

Az sayıda müşteri varsa geliş kaynağı sonludur. Sonlu geliş kaynaklı kuyruk
sistemlerinin analizi daha zordur. Kuyruk problemlerinin çoğunda geliş kaynağı
sonludur. Geliş kaynağının sonlu veya sonsuz olduğunun belirlenmesinde
kullanılan ölçüt şudur: Potansiyel müşterilerden birinin sistemde olması yeni
bir müşterinin sisteme ulaşma olasılığını çok etkiliyorsa geliş kaynağı
sonludur. Sonlu geliş kaynağından bir tek birimin ayrılması sistem
parametrelerini önemli biçimde etkiler. Bu nedenle bir çok uygulamada geliş
kaynağı sonsuz olmasa da, yeterince büyükse (30 üzeri) yaklaşık çözümlere olanak
sağladığı için sonsuz kabul edilir.

b. *Sayılara göre*: Müşterilerin kuyruk sistemine gelişleri tek tek veya gruplar
halinde olabilir. Arızalanan makinelerin onarım için tamir atölyesine gelişleri,
kitap almak/teslim etmek için öğrencilerin kütüphaneye gelişleri, araçların
benzin almak için benzin istasyonlarına gelişleri tek tek gelişlere, bir
restorana gelen aileler, yük gemilerinin limana gelişleri ile boşaltılmayı
bekleme durumuna geçen yükler gruplar halinde gelişlere örnek verilebilir.

c. *Zamana göre*: Müşteri gelişleri bilinen (belirli veya kontrol edilebilir)
zamanlarda veya rasgele olabilir. Sözgelimi uçakların iniş-kalkış pistine
gelişleri bilinen zamanlarda gerçekleşir. Makinelerin arızalanmaları dolayısıyla
tamir servisine gelişleri ise rasgele gelişlere iyi bir örnektir.

Müşteri gelişlerinin gerçekleşme zamanlarının kesinlikle bilindiği kuyruk
modelleri deterministiktir. Bu modellerle çalışmak oldukça kolay olmakla
birlikte gerçek hayatta deterministik model kullanılmasına uygun kuyruk
sistemleri ile seyrek olarak karşılaşılmakta, daha çok müşteri gelişlerinin
rasgele olduğu problemlerle yüz yüze gelinmektedir. Müşteri geliş zamanlarının
belirsiz olduğu durumlarda, sistemi çözümleyebilmek için müşteri gelişlerine
ilişkin bir olasılık dağılımı tanımlanması zorunludur. Müşteri gelişleri her
zaman aynı özelliği göstermese de gelişlerin Poisson dağılımına uydukları kabul
edilir. Poisson dağılımı, en az düzeyde veri gerektirdiğinden kuyruk
modellerinde en yaygın biçimde kullanılan olasılık dağılımıdır. Poisson dağılımı
ile tüm süreç tek bir parametre (ortalama geliş hızı) ile açıklanabilir.
Kuşkusuz gelişler her zaman Poisson dağılmayabilir. Bu nedenle Poisson
dağılımına karar vermeden önce bu dağılımın uygunluğu araştırılmalıdır. Karar
için, gerçekleşen süreler ile Poisson formülü ile belirlenen sürelerin
karşılaştırılması yeterli olur.

**2.** **Servis Sistemi**: Servis sistemi tanımlanmak istendiğinde öncelikle,
servis sisteminin yapısı ile servis hızı tanımlanmalıdır. Servis süreci
genellikle geliş sürecine benzetilerek irdelenmekle birlikte iki süreç arasında
önemli farklar vardır. En önemli fark müşteri yokken sürecin aylak sürelerle
kesintiye uğraması yüzünden servis sürecinin olasılıksal yapıda olmamasıdır.
Bununla birlikte birbirini izleyen servis sürelerinin bağımsız olduklarının
varsayılması durumunda, geliş süreleri bir olasılık dağılımıyla açıklanabilir.
Bu amaçla kullanılması en kolay dağılım negatif üstel (kısaca üstel) dağılımdır.
Bu dağılım ortalama servis süresi ile eksiksiz tanımlanır.

a. *Servis sisteminin yapısı*: Servis sistemi ile servis veren birimlerin sayısı
ile bunların verdikleri hizmetin durumu anlatılmak istenmektedir. Servis
birimlerinin aynı hizmeti verip vermedikleri son derece önemlidir. Kuyruk
sistemleri servis birimi sayısı ile kuyruk sayısına göre değişik gruplara
ayrılır. Bu gruplama aşağıda açıklanmıştır.

i. *Tek servis-tek kuyruk sistemi*: Müşteri hizmetlerinin tek bir servis birimi
tarafından sağlanması durumunda sistem, tek servisli kuyruk sistemidir. Tek bir
kasiyerin çalıştığı bir market, tek sekreterli bir ofis vb. bu türden sisteme
örnek olarak verilebilir. Aşağıdaki şekil böyle bir sistemin genel yapısını
açıklamaktadır.

**Şekil 13.2**

ii. *Paralel servis-tek kuyruk sistemi*: Birden fazla servis biriminin bulunması
ve tek kuyruk oluşması durumunda sistem, tek kuyruk-paralel servisli kuyruk
sistemidir. Servis birimlerinin paralelliği ile bütün servis birimlerinin aynı
hizmeti verdikleri kastedilmektedir. İstasyona girişin tek bir yerden sağlandığı
üç adet pompalama aygıtının bulunduğu bir benzin istasyonu, iki göz doktorunun
hizmet verdiği bir poliklinik bu sisteme örnek gösterilebilir. Bu sistem Şekil
13.3’de açıklanmıştır.

**Şekil 13.3**

iii. *Paralel servis-çok kuyruk sistemi*: Birden fazla servis biriminin
bulunduğu bu sistemin önceki sistemden tek farkı, her servis biriminin kendisine
ait bir kuyruğa sahip olmasıdır. Paralel servis-çok kuyruk sistemi, birden fazla
paralel servis-tek kuyruk sisteminden oluşan bir bütün olarak düşünülebilir. Bu
sistem Şekil 13.4’de açıklanmıştır.

**Şekil 13.4**

iv. *Seri servis sistemi*: Her biri farklı hizmet veren birden fazla servis
biriminin bulunduğu bu sistemde müşteri, hizmetinin tamamlanabilmesi için mevcut
servis birimlerinin her birinden belirli bir sırayla hizmet alır. Böyle bir
sistemde her servis biriminin kendisine ait bir kuyruğu olacağından sistem, seri
servis-çok kuyruk sistemi olarak tanımlanır. Çelik çaydanlık üretiminde çeliğin
kesilmesi, kesilen çeliğe biçim verilmesi, parlatılması, kalite kontrolünün
yapılması ve paketlenmesi işlemlerini gerçekleştiren servislerin her biri seri
servis sisteminin bir parçası durumundadır. Bu sistem Şekil 13.5’de
gösterilmiştir.

**Şekil 13.5**

Yukarıda açıklananlardan farklı modeller tanımlanabilirse de açıklananlar en
fazla bilinen ve kullanılanlardır. Çok kuyruklu sistemlerin analizi daha zor
olduğundan, burada çok kuyruklu modeller üzerinde durulmayacaktır.

b. *Servis hızı*: Servis hızı, servis oranı veya servis süresi ile açıklanır.
Servis oranı belirli bir zaman aralığında servis gören müşteri sayısı ile,
servis süresi bir servis için harcanan ortalama zaman uzunluğu ile açıklanır. Bu
süre sabit veya rasgele olabilir. Servis oranı servis süresinin, servis süresi
servis oranının 1’e oranı olduğundan bunlardan birinin biliniyor olması, servis
kapasitesinin belirlenmesi için yeterlidir. Bu durumu açıklamak amacıyla bir
sigorta danışmanının 8 saatlik bir iş gününde ortalama 32 kişiye hizmet
verdiğini düşünelim. Birim zaman saat olarak alındığında, servis oranı 4
müşteri/saat, servis süresi müşteri başına 1/4 saat olur. Analizlerde genellikle
servis süresi dikkate alınır. Servis sürelerinin biliniyor olması durumunda
problem daha kolay biçimde ele alınabilir. Ancak, servis zamanları farklıysa ve
bilinmiyorsa kuyruk sisteminin analizi için servis zamanlarının olasılık
dağılımının dikkate alınması gerekir. Kuyruk modellerinin büyük bir bölümünde
servis sürelerinin ortalama servis süresi etrafında üstel dağılım izlediği kabul
edilir. Geçerli sonuçlara ulaşabilmek için servis sürelerinin gerçekten üstel
dağılıp dağılmadığı kontrol edilmelidir. Bunun için gözlenen servis süresi ile
üstel dağılımla belirlenecek olan servis süresinin karşılaştırılması yeterlidir.

**3. Kuyruk Yapısı**: Kuyruk sisteminin diğer bir elemanı kuyruğun yapısıdır.
Kuyruk sisteminin eksiksiz tanımlanabilmesi için öncelikle kuyruk disiplininin
tanımlanması gerekir. Kuyruk disiplini öncelikle hangi müşterinin hizmet
göreceğini belirleyen veya servise müşteri seçiminde uygulanan politikadır.
Belli başlı kuyruk disiplinleri şunlardır:

a. *İlk Giren İlk Çıkar* (First In First Out = FIFO): En çok bilinen ve en
yaygın biçimde kullanılan kuyruk disiplinidir. Bu standart kurala göre
müşterilere hizmet, müşterilerin sisteme geliş sıraları göz önünde tutularak
verilir. Böylece sisteme ilk giren en önce hizmet görür ve sistemi terkeder.

b. *Son Giren İlk Çıkar* (Last In First Out = LIFO): Bu kuralın uygulandığı
sistemlerde servise, sisteme en son gelen müşteriden başlanır. Buna göre sistemi
en önce terkeden müşteri sisteme en son giren müşteri olur. Sözgelimi,
gelişlerine göre üst üste yığılan mektupların daktilo edilmesine yığının en
üstündeki mektuptan başlanması durumunda ilk yazılacak mektup masaya en son
bırakılan mektup olur.

c. *Rasgele Seçim* (Service In Random Order = SIRO): Bu kuralın uygulandığı
kuyruk sistemlerinde kuyrukta bekleyen müşteriler rasgele seçimle servis
sistemine alınır. Bu disiplinde müşterilerin geliş zamanları önemli değildir.

d. *Öncelikli Seçim*: Bazen kuyrukta bekleyen birimlerden bazılarına, servise ne
zaman geldiklerine bakılmaksızın, servis için öncelik verilir. Sözgelimi, tamir
için çok sayıda makinenin beklediği bir kuyrukta bu makinelere güç sağlayan
makine de tamir için bekliyorsa güç sağlayan makine sisteme en son da gelmiş
olsa öncelik ona verilir. Çünkü diğer makineler, kendilerine güç sağlayan makine
olmazsa çalışamazlar.

Bunlardan başka önce sıra alanlar önce hizmet görür, en kısa servis zamanı
gerektiren işlere öncelik verilir gibi kurallar da kuyruk disiplininde
kullanılmaktadır. İleride inceleyeceğimiz kuyruk modellerinde ilk giren ilk
çıkar kuralının işlediği kabul edilecektir.

Kuyruk sisteminin tanımlanmasında kuyruk disiplininin yanı sıra müşterilerin
kuyruk seçme ve kuyrukta bekleme konusundaki eğilim ve davranışları da çok
önemlidir. Bu kapsamda müşteriler sabırlı-sabırsız olmak üzere iki gruba
ayrılırlar. Kuyruğa katılıp sırası gelene kadar bekleyen ve ancak servis
gördükten sonra sistemden ayrılan müşteriye "sabırlı", kuyrukta beklemenin fazla
zaman alacağını düşünerek kuyruğa girmeyen veya kuyruğa girmesine karşın bir
süre bekledikten sonra, önce kuyruğu sonra sistemi terkeden müşteriye "sabırsız"
müşteri denir. Kuyruk sistemlerinin çoğunda müşterilerin sabırlı oldukları kabul
edilir. Sistemde aynı hizmeti veren servis birimi sayısının birden fazla olması
durumunda müşteri kuyruk seçimini rasgele yapmaz. Bu konudaki genel eğilim, az
sayıda müşterinin bulunduğu kuyruğu seçmek yönündedir. Bir kuyruğa girdikten
sonra diğer bir kuyrukta servisin daha hızlı olduğunu görüp kuyruk değiştiren
müşterilere de rastlanabilir. Ancak burada incelenecek tüm kuyruk modellerinde
müşterilerin sabırlı oldukları ve kuyruk değiştirmedikleri varsayılacaktır.

Kuyruk özellikleri genellikle kuyruğun ulaşabileceği maksimum uzunlukla
tanımlanır. Bu uzunluk sınırlı veya sınırsız olabilir. Sınırlı kuyruk
uzunlukları yer yokluğu veya müşterilerin uzun kuyruklara girmek istemeyişleri
sonucu ortaya çıkar. Burada kuyruğun sınırsız ölçüde uzayabileceği
varsayılacaktır.

**13.3. KUYRUK SİSTEMİNİN İŞLEYİŞ ÖZELLİKLERİ**

Herhangi bir kuyruk sisteminin analizi kuyruk sisteminin işleyişi ile ilgili
özelliklerin incelenmesini gerektirir. Bu inceleme kuyruk modellerinin
kullanılmasıyla gerçekleştirilir. Herhangi bir kuyruk sisteminin nasıl işlediği
ile ilgili bazı önemli özellikleri aşağıda açıklanmıştır. Bu özelliklere kuyruk
sisteminin performans ölçüleri de denir.

1\. *Kuyruk Uzunluğu* (Lq): Kuyrukta bekleyen müşterilerin ortalama sayısına
kuyruk uzunluğu denir. Uzun kuyruklar servis kapasitesinin düşük, kısa kuyruklar
servis kapasitesinin yüksek olduğu izlenimini yaratır.

2\. *Sistem Uzunluğu* (Ls): Kuyrukta bekleyenlerle, servis görenlerin sayıları
toplamıdır. Bu toplamın büyük olması müşteri hoşnutsuzluğuna yol açar. Daha
yüksek servis kapasitesinin gerektiğine işaret eder.

3\. *Kuyrukta Bekleme Süresi* (Wq): Bir müşterinin servis almak için kuyrukta
geçirdiği ortalama bekleme süresidir. Uzun beklemeler hoşnutsuzluğa dolayısıyla
muhtemel müşteri kayıplarına neden olur. Bu durumun önüne geçmek için servis
kapasitesinin arttırılması gerekir.

4\. *Sistemde Bekleme Süresi* (Ws): Bir müşterinin kuyruğa girişinden servis
görüp sistemden ayrılışına kadar geçen ortalama süredir. Bu sürenin uzun oluşu
servis kapasitesinde bazı düzenlemeler yapılması gerektiğine işaret eder.

5\. *Servis Biriminin Aylak Kalması Olasılığı* (Po): Sistem uzunluğunun sıfır
olması olasılığıdır. Bu olasılık yardımıyla sistemin aylak kaldığı süre kolayca
hesaplanabilir. Aylak süre doğrudan doğruya maliyetle ilgilidir. Bu sürenin
kısaltılması çalışmaları, yukarıda açıklanan özelliklerin tümünü olumsuz biçimde
etkiler.

Kuyruk sistemlerinin çoğu çalışmaya sistemin boş olduğu durumla başlar. Sistemin
değişmez durum koşullarına ulaşması için belirli bir süre geçmesi gerekir.
Değişmez durumla sistemdeki müşteri sayısının değil, sistemin işleyişiyle ilgili
bazı ölçülerin (işleyiş özellikleri) değişmeyeceği anlatılmaktadır. Aşağıda
açıklanacak olan kuyruk modellerinin hepsi için, sistemin dengede veya değişmez
durum koşulları altında çalıştığı kabul edilmektedir.

**13.4. KUYRUK MODELLERİ**

Kuyruk modelleri deterministik ve olasılıksal kuyruk modelleri olmak üzere ikiye
ayrılır. Sisteme gelişler bilinen zamanlarda gerçekleşiyor ve ortalama servis
süresi kesinlikle biliniyorsa kuyruk modeli deterministiktir. Üretim akış hattı
üzerindeki birimlerin oluşturduğu kuyruk sistemine ilişkin kuyruk modeli
tartışmasız deterministiktir. Kuyruk modellerinin pek çoğunda bu değerlerin
bilinmediği yalnızca olasılık terimleriyle açıklanabildikleri yani, olasılıksal
oldukları varsayılmaktadır. Uygulamada daha çok olasılıksal kuyruk modelleri
kullanılır.

**13.4.1. Deterministik Kuyruk Modelleri**

İlk olarak kuyruk sistemine gelişlerin belirli ve bilinen zaman aralıklarında
gerçekleştiği ayrıca, servis süresinin bilindiği ve değişmediği durumların
kuyruk modeli üzerinde duralım.

Sözgelimi, bir güzellik salonuna cilt bakımı için her 10 dakikada bir kişinin
geldiğini ve cilt bakımının 10 dakika sürdüğünü düşünelim. Bu durumda hem
birimlerin sisteme geliş oranı hem de servis oranı saat başına 6 kişidir. Bu
koşullarda kuyruk oluşmayacağı ancak, bakım uzmanının sürekli servis verir
durumda olacağı açıktır. Geliş hızı aynı olmak üzere uzmanın saatte 10 müşteriye
hizmet verebildiğini düşünelim. Bu durumda uzman, zamanının 4/10’unda meşgul,
6/10’unda aylak kalacaktır. Kısaca uzman, toplam 10 dakikanın 4 dakikasını
servise ayırırken, 6 dakikasında aylak kalacaktır. Bu koşullar altında da kuyruk
oluşmayacağı açıktır. Geliş hızı aynı olmak üzere uzmanın saatte 5 kişiye hizmet
verebildiğini düşünelim. Bu durumda görevli hep meşgul olacak, zaman akışı
içinde sistemde sürekli uzayan bir kuyruk oluşacaktır. Servis oranının geliş
oranından küçük olması durumunda sistemde sürekli uzayan bir kuyruk oluşur ve
sonunda sistem çalışmaz hale gelir. Bu durumda sistemde sürekli uzayan
kuyrukların oluşumunu engelleyecek önlemlerin alınması yani, servis
kapasitesinin arttırılması gerekir. Sonuç olarak; müşteri geliş oranı
(müşteri/zaman), servis oranı (müşteri/zaman) olmak üzere,

\> µ ise, sistemde sürekli uzayan bir kuyruk oluşur. Servis birimlerinin sürekli
meşgul olduğu sistem sonunda bozguna uğrar, çalışmaz hale gelir.

µ ise, kuyruk oluşmaz. Bu, bir birimin kuyrukta bekleme süresinin sıfır olması
demektir. Bu koşullarda servis birimi 1 - (/µ) olasılıkla aylaktır. Bu
yazılıştaki /µ (=)’ya "trafik yoğunluğu" veya "sistem etkinliği" denir ve
sistemin meşgul olması olasılığı olarak yorumlanır. Özetle,

\> 1 ise sistem sonunda bozguna uğrar ve çalışmaz hale gelir.

1 ise sistem çalışır.

Düzenli gelişler ve düzenli servis oranlarıyla karşılaşma şansı çok düşüktür.
Özellikle de insan söz konusu olduğunda geliş ve servisle ilgili değerlerin
değişken olması kaçınılmazdır. Kısaca, deterministik kuyruk modellerinin
kullanım alanlarının çok sınırlı olduğunu söylemek yanlış olmaz.

**13.4.2. Olasılıksal Kuyruk Modelleri**

Gelişlerin ve servislerin düzgün olduğu ve değişmediği varsayımı uygulamada pek
seyrek gerçekleşir. Daha sık karşılaşılan durum, hem geliş hem de servis
sürelerinin değişken olmasıdır. Bu nedenle yaygın biçimde kullanılan kuyruk
modelleri olasılıksal olanlardır. Kuyruk sisteminin yapısına bağlı olarak
değişik olasılıksal kuyruk modelleri geliştirilmiştir. Bu kesimde,

1\. Poisson-üstel, tek servis, sonsuz geliş kaynaklı

2\. Poisson-üstel, tek servis, sonlu geliş kaynaklı

3\. Poisson-üstel, çok servis, sonsuz geliş kaynaklı

kuyruk modelleri üzerinde durulacaktır. Model tanımlarındaki Poisson-üstel
kavram ikilisi, müşteri gelişlerinin Poisson (dolayısıyla gelişler arası
sürelerin üstel), ayrılış (veya servis) sürelerinin üstel dağıldığı
anlamındadır. Geliş hızı olmak üzere belirli bir T zaman aralığında sisteme n
birimin ulaşması olasılığı Poisson dağılımına göre aşağıdaki gibi tanımlanır.

Burada, = T, e = 2.7183’dür.

**Örnek 13.1**: Bir güzellik salonuna bir saat içinde ortalama 6 müşteri
gelmektedir. Gelişlerin Poisson dağılımına uyduğu kabul edilmektedir. Buna göre,
salona yarım saatte tam üç müşterinin gelmesi olasılığını hesaplayınız.

**Çözüm 13.1**: = 6 müşt./saat, T = 0.5 saat olarak verildiğinden ve P(n = 3),
aşağıdaki gibi hesaplanır.

= T = 6 x 0.5 = 3

bağıntısından, P(n = 3) = = 0.075

Zaman birimi saat yerine dakika olarak alındığında, dakika cinsinden
açıklanmalıdır. Bu durumda, = 6/60 = 0.1 müşteri/dakika, T = 30 dakika, = T =
30/10 = 3 müşteri olur. Dolayısıyla P(n = 3), önceden olduğu gibi 0.075 olarak
hesaplanır.

Farklı müşterilere verilen servis süreleri birbirlerinden bağımsızsa, bir
servisin tamamlanması için geçen sürenin T zamandan fazla olmaması olasılığı,
ortalama servis oranı olmak üzere, üstel dağılımın kullanılmasıyla, aşağıdaki
olasılık ifadesiyle tanımlanır.

**Örnek 13.2**: Bir süper market yöneticisi kasiyerin 15 dakikada 6 müşteriye
hizmet verebildiğini gözlemiştir. Servis süresinin üstel dağıldığı kabul
edilmektedir. Buna göre bir müşteriye verilen hizmetin, **a**. 3 dakikadan az,
**b**. 9 dakikadan uzun sürmesi olasılıklarını hesaplayınız.

**Çözüm 13.2**: = 24 müş./saat veya = 0.4 (= 24/60) müş/dak., T = 3/60 saat =
0.05 saat veya T = 3 dakika olduğuna göre,

**a**. Zaman dilimi olarak dakika dikkate alındığında, P(t 3) şu şekilde
hesaplanır.

P(t 3) = 1 - (2.7183)-(24)(0.05)

= 1 - (2.7183)-1.2 = 0.6988

Aynı olasılık zaman dilimi olarak saat dikkate alındığında şöyle hesaplanır.

P(t 3) = 1 - (2.7183)-(0.4)(3) = 0.6988

**b**. ve T’nin dakika esasında düzenlenmesiyle, P(t 9) şu şekilde hesaplanır.

P(t 9) = e-T

= (2.7183)-(24)(0.15) = 0.0273

Zaman dilimi olarak saat dikkate alındığında P(t 9),

P(t 9) = (2.7183)-(9)(0.4)

= (2.7183)-3.6 = 0.0273 olarak hesaplanır.

13.4.2.1. Poisson-Üstel, Tek Servis-Sonsuz Geliş Kaynağı

Başlıkta açıklanan duruma uygun modelden tutarlı sonuçların elde edilmesi
aşağıda açıklanan varsayımlara bağlıdır.

1.  Gelişler, ortalama geliş oranı olmak üzere, Poisson dağılımına sahiptir.

2.  Ortalama servis oranı olmak üzere servis süreleri üstel dağılıma sahiptir.

3.  Geliş kaynağı sonsuzdur.

4.  Tek bir servis birimi vardır.

5.  Hizmet ilk giren-ilk çıkar kuralına göre verilir.

6.  Ortalama geliş hızı ortalama servis hızından düşüktür.

7.  Sınırsız sayıdaki müşterinin bekleyeceği yer vardır.

Duruma uygun modelin geliştirilebilmesi için önce müşteri isteğinin servis
birimi tarafından karşılanıp karşılanamayacağı sorusu yanıtlanmalıdır. Yanıt
için ve değerlerinin karşılaştırılması yeterli olur. olması durumunda kuyruk,
sonuçta sistemin bozguna uğramasına yol açacak biçimde uzar. Sisteminin
çalışabilmesi için \< olmalıdır. = olması durumunda da sistemin çalışmayacağı
gösterilebilir.

Daha önce açıklandığı gibi sistemin trafik yoğunluğu, yani servis biriminin
meşgul olması olasılığıdır. Buna göre sistemin aylak kalması olasılığı,yani
sistemde müşteri bulunmaması olasılığı; Po = 1 - olur. Sistemde tek bir müşteri
bulunması olasılığının P1 = Po olduğu gösterilebilir. Benzer şekilde, sistemde
tam iki müşteri bulunması olasılığı; P2 = P1 = ²Po olur. İlişki bu şekilde
sürdürüldüğünde P3 = P2 = (²Po) yazılır. Genelleme yapmak istenirse, sistemde
tam n müşteri bulunması olasılığı Pn = nPo = n (1 - ) olur.

Bu sonuç sistemdeki birimlerin ortalama sayısının bulunmasında kullanılabilir.
Bu amaçla,

=

yazılması ve ifadenin çözülmesi yeterlidir.

Sonuçta, Ls’i hesaplama formülü aşağıdaki gibi elde edilir.

veya

Kuyruktaki birimlerin ortalama sayısı, sistemdeki birimler ile servis görmekte
olan birimlerin ortalama sayıları arasındaki farka eşittir. Servis, zamanın
(/)’sünde meşgul, (1 - /)’sünde aylak olduğuna göre servis görenlerin ortalama
sayısı aşağıdaki gibi olur.

1(/) + 0(1 - /) = /

Bunun sonucunda ortalama kuyruk uzunluğu ya,

veya gerekli aritmetik işlemlerin yapılması ile aşağıdaki gibi türetilir.

Üzerinde önemle durulması gereken konu Lq’nun boş kuyruklar da dahil olmak üzere
sistemdeki tüm kuyrukların ortalama uzunluğu olduğudur. Boş olmayan, yani en az
bir müşterinin beklediği kuyrukların ortalama uzunluğu aşağıda gösterildiği
gibidir.

=

Ortalama geliş oranı iken, gelişler arası ortalama süre 1/’dır. Buna göre bir
müşterinin kuyrukta ortalama bekleme süresi Wq, gelişler arası ortalama süre
(1/) ile ortalama kuyruk uzunluğunun (Lq) çarpımına eşittir. Sembollerle
açıklamak gerekirse, Wq aşağıdaki gibi olur.

Yukarıdaki eşitlikte Lq yerine ²/( - ) yerleştirilmesi ve gerekli işlemlerin
yapılmasıyla Wq aşağıdaki gibi elde edilir.

Benzer şekilde, bir birimin sistemde ortalama kalma süresi (Ws), gelişler arası
ortalama süre ile sistemdeki birimlerin sayıları çarpımına eşit olduğundan, Ws
şöyle yazılır.

Ls yerine /( - )’nın yerleştirilmesiyle, WS aşağıdaki gibi belirlenir.

Özetle, ortalama servis süresi olmak üzere servis için geçen ortalama süre 1/
olur. Bu nedenle, bir müşterinin sistemde kalma süresi kuyrukta geçirdiği süre
ile ortalama servis süresinin toplamına eşittir. Buna göre Ws,

olarak elde edilir.

Son olarak bir müşterinin sistemde t birim zamandan daha uzun kalması
olasılığının,

kuyrukta t birim zamandan daha uzun kalması olasılığının,

olduğunun belirtilmesiyle Poisson-üstel, tek servis-sonsuz geliş kaynaklı kuyruk
modeli ile ilgili tüm açıklamalar tamamlanmış olur. Burada, sistemde harcanan
süre ile servis süresi üstel dağılmakla birlikte bu ikisinin farkı olarak
tanımlanan kuyrukta bekleme süresi Wq(t)’nin üstel dağılmadığı gözden
kaçırılmamalıdır.

**Örnek 13.3**: Bir güzellik salonuna saatte ortalama 4 müşteri gelmektedir.
Gelişlerin Poisson dağıldığı, müşterilerin sabırlı olduğu ve FIFO kuralılının
uygulandığı kabul edilmektedir. Güzellik uzmanı saatte ortalama 5 müşteriye
hizmet verebilmektedir. Buna göre,

1.  i. 15 dakikalık zaman dilimi içerisinde, ii. 30 dakikalık zaman dilimi

    içerisinde 0, 1, 2, 3, 4, 5 müşteri gelmesi olasılıklarını hesaplayınız.

2.  Sistemin trafik yoğunluğunu bulunuz.

3.  Sisteminin boş olması olasılığını hesaplayınız.

4.  10 saatlik bir iş gününde uzmanın ortalama kaç saat boş kalacağını
    hesaplayınız.

5.  Salonda 0, 1, 2, 3, 4, 5 müşteri bulunması olasılıklarını hesaplayınız.

6.  Salondaki ortalama müşteri sayısını bulunuz.

7.  Servis için bekleyen ortalama müşteri sayısını bulunuz.

8.  Boş olmayan kuyrukların ortalama uzunluğunu hesaplayınız.

9.  Bir müşterinin kuyrukta harcadığı ortalama süreyi bulunuz.

10. Bir müşterinin salonda harcadığı ortalama süreyi hesaplayınız.

11. Kuyrukta 30 dakikadan daha uzun bekleme olasılığını hesaplayınız.

12. Salonda 50 dakikadan daha uzun kalması olasılığını hesaplayınız.

**Çözüm 13.3**: = 4 müşteri/saat, = 5 müşteri/saat’dir. Buna göre,

**a**. 15 ve 30 dakikalık zaman dilimleri içinde salona 0, 1, 2, 3, 4, 5 müşteri
gelmesi olasılıkları aşağıdaki formülden hesaplanmış, hesaplama sonuçları Tablo
13.1’de sunulmuştur.

**Tablo 13.1**

| Müşteri    | P(n)         |              |
|------------|--------------|--------------|
| Sayısı (n) | T = 1/4 Saat | T = 1/2 Saat |
| 0          | 0.3678       | 0.1353       |
| 1          | 0.3678       | 0.2706       |
| 2          | 0.1839       | 0.2706       |
| 3          | 0.0613       | 0.1804       |
| 4          | 0.0153       | 0.0900       |
| 5          | 0.0031       | 0.0360       |

**b**. = / = 4/5 = 0.8

**c**. Po = 1 - (/) = 1 - 0.8 = 0.2

**d**. 10 saatlik bir iş gününde uzmanın ortalama boş kalma süresi,

10 Saat İçindeki Boş Süre = Po x Süre = (0.2) x 10 = 2 saat

**e**. Sistemde n müşteri bulunması olasılığı = Pn = n(1 - ) olduğuna göre,

P0 = P(n = 0) = 0.200

P1 = P(n = 1) = 0.160

P2 = P(n = 2) = 0.128

P3 = P(n = 3) = 0.102

P4 = P(n = 4) = 0.082

P5 = P(n = 5) = 0.066

**f**. Ls = /(1 - ) = 0.8/(1 - 0.8) = 4 müşteri

**g**. Lq = ²/(1 - ) = (0.8)²/(1 - 0.8) = 0.64/0.20 = 3.2 müşteri

**h**. Lq\* = 1/(1 - ) = 1/(1 - 0.8) = 5 müşteri

**i**. Wq = = = 4/5 saat = 48 dakika

**j**. Ws = = 1/1 = 1 saat = 60 dakika

**k**. Kuyrukta 30 dakikadan fazla bekleme olasılığı aşağıda hesaplanmıştır.

Wq(30) = = (0.8)(e-30/60) = 0.485

**l**. Salonda 50 dakikadan daha uzun kalma olasılığı aşağıdaki gibi hesaplanır.

Ws(50) = = e-50/60 = 0.435

**Örnek 13.4**: Tek bir kasiyerin bulunduğu bir markete saatte ortalama 15
müşteri gelmektedir. Müşteri gelişlerinin Poisson dağılımına uyduğu,
müşterilerin sabırlı oldukları ve FIFO kuralının işlediği kabul edilmektedir.
Kasiyer saatte ortalama 20 müşteriye üstel dağılıma uygun biçimde hizmet
verebilmektedir. Buna göre,

1.  Sistemin trafik yoğunluğunu bulunuz.

2.  Kuyruk sisteminin boş olması olasılığını hesaplayınız.

3.  Sistemdeki ortalama müşteri sayısını bulunuz.

4.  Servis için bekleyen ortalama müşteri sayısını belirleyiniz.

5.  En az bir müşterinin bulunduğu kuyrukların ortalama uzunluğunu hesaplayınız.

6.  Bir müşterinin kuyrukta harcadığı ortalama süreyi bulunuz.

7.  Bir müşterinin markette harcadığı ortalama süreyi hesaplayınız.

    **Çözüm 13.4**: = 15 müşteri/saat, = 20 müşteri/saat olarak verilmiştir.
    Buna göre, istenenler aşağıdaki gibi hesaplanacaktır.

    **a**. = / = 15/20 = 0.75

    **b**. Po = 1 - = (1 - 0.75) = 0.25

    **c**. Ls = /(1 - ) = 0.75/(1 - 0.75) = 3 müşteri

    **d**. Lq = ²/(1 - ) = 0.75²/(1 - 0.75) = 2.25 müşteri

    **e**. Lq\* = 1/(1 - ) = 1/(1 - 0.75) = 4 müşteri

    **f**. Wq = /( - ) = 15/20(20 - 15) = 0.15 saat = 9 dakika

8.  Ws = 1/( - ) = 0.2 saat = 12 dakika

**Örnek 13.5**: Bir dokuma atölyesinde ortalama her 20 dakikada bir arıza
olmakta ve arıza giderilinceye kadar üretim durmaktadır. Bir arızanın
giderilmesi ortalama 12 dakika sürmektedir. Arızaların Poisson, onarım işleminin
üstel dağılımlı olduğu kabul edilmektedir. Buna göre,

1.  Sistemin trafik yoğunluğunu bulunuz.

2.  Atölyenin boş olması olasılığını hesaplayınız.

3.  Atölyedeki ortalama makine sayısını bulunuz.

4.  Onarılmak için bekleyen ortalama makine sayısını belirleyiniz.

5.  En az bir makine bulunan kuyrukların ortalama uzunluğunu hesaplayınız.

6.  Bir makinenin kuyrukta harcadığı ortalama süreyi bulunuz.

7.  Bir makinenin atölyede kaldığı ortalama süreyi hesaplayınız.

**Çözüm 13.5**: = 1/20 arıza/dakika = 3 arıza/saat ve = 5/60 arıza/dakika = 5
arıza/saat olarak verilmiştir. Buna göre,

**a**. = / = 3/5 = 0.6

**b**. Po = (1 - 0.6) = 0.4

**c**. Ls = /(1 - ) = 0.6/(1 - 0.6) = 1.5 müşteri

**d**. Lq = ²/(1 - ) = (0.6)²/(1- 0.6) = 0.9 müşteri

**e**. Lq\* = 1/(1 - ) = 1/(1 - ) = 2.5 müşteri

**f**. Wq = /( - ) = 3/5(5 - 3) = 3/10 saat = 18 dakika

**g**. Ws = 1/( - ) = 1/(5 – 3) = 1/2 saat = 30 dakika

olarak hesaplanır.

*Maliyet Analizi*: Kuyruk modellerinin oluşturulmasındaki en önemli amaç servis
sisteminde optimizasyon sağlayabilmektir.

Servis sisteminin optimizasyonu deneme yanılma yöntemiyle belirlenebilirse de
pek çok durumda sisteme bu şekilde müdahale edilmesi mümkün olmamaktadır. Mümkün
olması durumlarında ise bu yöntem uygulamayı engelleyecek kadar pahalı
olabilmektedir.

Kuyruk modellerinde başlıca iki maliyet unsuru vardır:

-   Birincisi, müşterilerin servis için bekledikleri zaman kaybının maliyetidir.

Buna bekleme zamanı maliyeti denir.

-   İkincisi ise yatırım ve servis sağlama maliyetidir.

Kuyruk analizinin sonuçları genel olarak servis sunma ve bekleme zamanı
maliyetlerinin toplamının en küçüklenmesinde kullanılır. Örneğin servis
olanakları değiştirilerek, tesisin boş kalma maliyeti ile servis bekleme
maliyeti arasında optimal bir denge kurulmaya çalışılmaktadır. Örnek 13.2’deki
güzellik salonunu düşünelim. Salona yeni bir uzman alınması durumunda, müşteri
geliş oranı aynı kalmak koşuluyla, halihazırda 1 saat olarak hesaplanmış olan
ortalama bekleme süresi azalır. Bekleme süresinin azalması bekleme zamanı
maliyetinin azalması sonucunu doğurur.

Maliyet modelleri gerekli maliyet parametrelerinin güvenilir şekilde elde
edilmesi ile olumlu sonuç vermektedir. En iyi servis düzeyi bekleme zamanı
maliyeti ile servis sağlama maliyeti toplamının en küçük olduğu noktada belirir.
İşletme için servis düzeyi artarken servis maliyeti de artmakta, ancak bekleme
zamanı maliyeti azalmaktadır. Maliyet modellerinin uyarlanmasındaki ana problem,
özellikle insan davranışı modeli etkilediğinde birim bekleme maliyetini tahmin
edebilmektir.

Açıklanan maliyet unsurları arasındaki ilişki Şekil 13.6’da gösterilmiştir.

Şekil 13.6

Servis düzeyi artırılırken bekleme zamanı maliyetinin en küçük olması ana
hedeftir. Bu iki maliyet toplamının en küçük olduğu noktadaki servis düzeyi en
iyi servis düzeyidir. Şekil 13.6’daki k, en iyi servis düzeyini göstermektedir.
Maliyetler arasındaki bu en iyi nokta, servis isteyen birimlerin gelişlerini
programlayarak veya en uygun tesislerin kullanılmasıyla elde edilebilir. Bu,
geliş oranı kontrol edilebiliyorsa en küçük toplam maliyeti sağlayacak geliş
oranının sağlanması veya servis düzeyinin bu amaçla ayarlanması demektir. Geliş
zamanları ve olanaklarının her ikisi de kontrol edilebiliyorsa, toplam maliyetin
en küçüklenmesi için hem gelişler programlanabilir hem de servis düzeyi
ayarlanabilir. Tek servisli kuyruk modellerinde denge durumu koşulları
geçerliyse toplam maliyet aşağıdaki ifadeyle tanımlanır. Bu ifadenin geçerli
olması çin bekleme zamanı ve servis maliyeti fonksiyonları doğrusal olmalıdır.

Burada, C1 = Servis verme maliyeti, C2 = Bekleme maliyetidir.

En iyi servis düzeyinin hesabı için, Ls = /( - ) bağıntısının toplam maliyet
fonksiyonunda yerine konulması ile aşağıdaki denkleme ulaşılır.

TM’nin ’ye göre birinci türevinin sıfıra eşitlenerek için çözülmesiyle, en iyi
servis düzeyi aşağıdaki gibi olur:

**Örnek 13.6**: Bir fabrikada 12 dakikada bir makinelerden biri arızalanmakta ve
onarım işlemi 8 dakika sürmektedir. Onarımdan sorumlu ustaya saat başına 40 TL
ödenmektedir. Bir makinenin çalışmamasının işletmeye maliyeti saat başına 25
TL’dir. İşletme, saat ücreti 35 TL olan bir usta daha alıp almama konusunda
ikilem içindedir. Yeni bir usta alınması durumunda, halihazırda 7.5 makine/saat
olan servis hızı 10 makine/saat olarak değişecektir. Makinelerin bir günde 8
saat kullanıldıklarını düşünerek yeni bir eleman alınıp alınmaması konusuna
ilişkin maliyet analizlerini yapınız.

**Çözüm 13.6**: Önce tek bir ustanın çalıştığı durumda günlük toplam maliyeti
hesaplayalım. Günlük servis maliyeti, ustaya saat başına ödenen ücretin 8’le
çarpılmasıyla şöyle hesaplanır: Günlük servis maliyeti = 8 x 40 = 320 TL

Makinelerin arızlanmaları sonucu çalışmamalarından doğan günlük bekleme maliyeti
bir makinenin sistemde kalma süresi ve 1 günde arızalanan makine sayısı ile bir
makinenin çalışmamasının maliyeti çarpımına eşittir.

Önce arızalı bir makinenin sistemde kalma süresini (Ws) hesaplayalım. = 7.5
olduğundan,

Ws = 1/( - ) = 1/(7.5 - 5) = 1/2.5 = 0.4 saat = 24 dakika

olarak hesaplanır. 8 saatlik bir iş gününde onarılmak için sisteme gelen makine
sayısı (saatte 5 olmak üzere) 40’dır. 40 makinenin sistemde kalma süresi 40 x 24
= 960 dakikadır. Buna göre toplam 40 makinenin bir günde 960 dakika (16 saat)
beklemesinin işletmeye maliyeti aşağıdaki gibi hesaplanır.

Bekleme maliyeti = 16 x 25 = 400 TL’dir.

Buna göre toplam maliyet şöyle olur: Toplam Maliyet = 320 + 400 = 720 TL

Yeni usta günlük servis maliyetinin artmasına yol açar. Bu durumda, servis
maliyeti; Servis Maliyeti = 8 x 40 + 8 x 35 = 600 TL olarak hesaplanır.

Yeni ustanın çalışmasıyla = 10 makine/saat olacağından, bir makinenin sistemde
ortalama bekleme süresi azalarak,

Ws = 1/( - ) = 1/(10 - 5) = 1/5 saat = 12 dakika olur.

Makinelerin arızalanma hızları değişmediğinden 8 saat içinde onarılmak için
sisteme gelen makine sayısı önceden olduğu gibi 40’a eşittir. 40 makinenin
sistemde kalma süresi 40 x 12 = 480 dakikadır. Toplam 40 makinenin bir günde 480
dakika (8 saat) beklemesinin işletmeye maliyeti aşağıdaki kadar olur.

Bekleme maliyeti = 8 x 25 = 200 TL

Buradan, Toplam Maliyet = 600 + 200 = 800 TL olarak hesaplanır.

Tek ustanın bulunduğu durum için toplam maliyetin 720 TL olduğunu hatırlayalım.
Usta sayısının artması toplam maliyeti artırdığından, usta sayısının
değiştirilmemesine karar verilecektir.

**13.4.2.2. Poisson-Üstel, Tek Servis-Sonlu Geliş Kaynağı**

Bazı kuyruk problemlerinde servis isteyebilecek birim sayısı sonlu olabilir. Bu
durumda sonlu geliş kaynağı söz konusu olur. Geliş kaynağının sonlu olduğu
kuyruk modelinin dayandığı varsayımlar esasta bir önceki modelin
varsayımlarından çok farklı değildir. Bu yeni model için potansiyel müşteri
sayısı M olmak üzere, müşterinin ya sistemde ya da sisteme ulaşmak üzere olduğu
düşünülür. Sisteme ulaşmak amacıyla harekete geçmiş olan birimin sisteme ulaşma
süresinin 1/ ortalamalı üstel dağılıma sahip bir rasgele değişken olduğu
varsayılır. Bunun sonucunda sistemde n müşteri varsa, sistem dışında ve sisteme
ulaşma durumundaki müşteri sayısı (M - n) olur. Bu durumda sisteme ortalama
varış hızı (M - n) olur. Bilindiği gibi, kuyruk sistemi kendi kendisini
düzenleyen bir yapıya sahiptir. Bu nedenle sistem pek çok müşterinin kuyrukta
beklediği duruma ulaştığında müşteri geliş oranı (ileride izdiham yaşanmasına
yol açmayacak biçimde) düşer. Sistemde M müşteri varsa (M + 1)’inci müşterinin
sisteme gelme olasılığı yaklaşık sıfırdır. Bunu açıklamak için üretimini 5
makine ile sürdüren bir işletme düşünelim. Bu durumda makinelerin bakım ve
onarımından sorumlu servis sisteminde en fazla (birisi onarılmakta dördü
onarılmayı bekleyen) 5 makine olur.

Bir makinenin sisteme geliş olasılığı sisteme girmeye müsait olan müşteri
sayısına bağlı olarak değişir. Bu tip kuyruk modellerinde bir tek gelişle, geliş
kaynağının yapısı değişeceğinden, müşteri geliş kaynağı değişkendir. Varışlar
arasında bağımlılık ilişkilerinin bulunması yüzünden, sonlu geliş kaynaklı
modellerde Poisson olasılık dağılım kuralı tam anlamıyla geçerli değildir. Bu
nedenle ortalama gelişlerden değil gelişler arası ortalama sürelerden söz
ederiz. Gelişler arası süre 1/ ortalama ile üstel dağılır. Böyle bir sistemin
çalışma özellikleri aşağıdaki bağıntılarla açıklanır. Toplam müşterilerin
oluşturduğu geliş kaynağının birey sayısı M, birbirini izleyen gelişler arasında
geçen ortalama süre 1/ ve servis hızı olmak üzere bu kuyruk sisteminin işleyişi
ile ilgili özellikleri aşağıdaki bağıntılarla açıklanmaktadır.

a. Sistemin boş olması olasılığı aşağıdaki bağıntıyla hesaplanır.

b. Sistemde n müşteri bulunması olasılığı hesaplama formülü şöyledir:

P0 =

P0 = 0 n \> M

c. Ortalama kuyruk uzunluğu aşağıdaki formülden hesaplanır.

d. Ls’yi hesaplamak için kullanılan formül aşağıda gösterildiği gibidir.

e. Kuyrukta bekleme süresine ait formül aşağıda gösterilmiştir.

=

f. Sistemde bekleme süresi ile ilgili formül aşağıda verilmiştir.

=

**Örnek 13.7**: Bir işletmenin üretimde kullandığı 4 makinesi vardır. Makineler
ortalama 10 saatte bir arızalanmakta ve üretim sürecinin yavaşlamasına neden
olmaktadır. Makinelerin onarımından sorumlu usta iki saatte ancak bir makine
onarabilmektedir. Buna göre,

1.  Ustanın aylak kalması olasılığını,

2.  Onarım için bekleyen ve onarılmakta olan makine sayısının 0, 1, 2, 3 ve 4
    olması olasılıklarını,

3.  Onarım için bekleyen makinelerin ortalama sayısını,

4.  Onarım için bekleyen ve onarılmakta olan makinelerin ortalama sayısını,

5.  Bir makinenin kuyrukta harcadığı ortalama süreyi,

6.  Bir makinenin sistemde harcadığı ortalama süreyi hesaplayınız.

**Çözüm 13.7**: = 1/2 makine/saat, = 1/10 makine/saat olarak verildiğinden,

=/ = (1/10)/(1/2) = 1/5 = 0.2

olarak hesaplanır.

Bu modelle ilgili formüllerin tümünde Po kullanıldığından Po’ın hesaplanması
uygun olur. Po’ın hesaplanması ile ilgili işlemler Tablo 13.2’de gösterilmiştir.

**Tablo 13.2**

| i | M!/(M-i)! | (/)i   | M!/(M-i)! (/)i |
|---|-----------|--------|----------------|
| 0 | 1         | 1.0000 | 1.0000         |
| 1 | 4         | 0.2000 | 0.8000         |
| 2 | 12        | 0.0400 | 0.4800         |
| 3 | 24        | 0.0080 | 0.1920         |
| 4 | 24        | 0.0016 | 0.0384         |
|   |           | Toplam | 2.5104         |

Buna göre P0 aşağıdaki gibi hesaplanır. P0 bilindiğinde diğer değerlerin
hesaplanması son derece kolaydır.

= (2.5104)-1 = 0.398

**a**. Ustanın aylak kalması olasılığı, Po = 0.398

**b**. Sistemde n’nin olası değerleri kadar makine bulunması olasılıkları
aşağıdaki formülden hesaplanmış ve hesaplama sonuçları Tablo 13.3’de
gösterilmiştir.

**Tablo 13.3**

| n | (/)nM!/(M-n)! | Pn    |
|---|---------------|-------|
| 0 | 1.000         | 0.398 |
| 1 | 0.800         | 0.319 |
| 2 | 0.480         | 0.191 |
| 3 | 0.192         | 0.076 |
| 4 | 0.384         | 0.015 |
|   | Toplam        | 1     |

**c**. Onarım için bekleyen makine sayısı (ortalama kuyruk uzunluğu) şöyledir:

= 4 - 6(0.602) = 0.390 makine

**d**. Sistemde bekleyen ve onarılmakta olan makine sayısı,

= 4 - 5(0.6017) = 0.992 makine

**e**. Kuyrukta bekleme süresi,

= 2(6.648 - 6) = 1.296 saat

**f**. Sistemde bekleme süresi aşağıdaki gibi hesaplanır.

Ws = Wq + (1/) = 1.296 + (1/1/2) = 1.296 + 2 = 3.296 saat

*Maliyet Analizi*: Makinenin 1 saat aylak kalmasının işletmeye 200 TL’ye
malolduğunu düşünelim. Tamirciye saatte 70 TL, makine başında çalışanlara saatte
60 TL ödendiğini düşünelim. Bu bilgileri kullanarak tek bir arızanın beklenen
maliyetini hesaplayınız.

Toplam maliyet, 1. Makinenin aylak kaldığı zamanın maliyeti, 2. Makine başında
çalışanın aylak kaldığı zamanın maliyeti, 3. Tamircinin aylak kaldığı zamanın
maliyeti olmak üzere üç maliyet unsurunun toplamına eşittir. Önce her bir
maliyet unsurunu ayrı ayrı hesaplayalım.

1\. Makine aylak zaman maliyeti = Ws x 200 = 3.295 x 200 = 659 TL

2\. Makineyi çalıştıranın maliyeti = Ws x 60 = 3.295 x 60 = 197.7 TL

3\. Tamirci maliyeti = (Ws - Wq) x 70 = (3.295 - 1.295) x 70 = 140 TL

Buna göre bir arızanın işletmeye maliyeti aşağıdaki gibi hesaplanır.

TM = 659 + 197.7 + 140 = 996.7 TL

*Duyarlılık Analizi*: İstenrse parametre değerlerindeki değişmenin en iyi çözümü
nasıl etkilediği incelenebilir. Konuyu açıklamak için yukarıdaki problemde bir
günde onarılan makine sayısındaki değişikliğin en iyi çözüm üzerindeki etkisini
inceleyelim. Aynı inceleme sistemin başka bir parametresinin, sözgelimi geliş
hızının, dikkate alınmasıyla da gerçekleştirilebilir.

Onarılan makine sayısının değişmesi ’nün değişmesi demektir. için sırasıyla,
0.3, 0.8 ve 1.2 değerlerini alalım. ’nın değişmediğini (= 0.1) düşünelim.
Hesaplama sonuçları Tablo 13.4’de gösterilmiştir.

**Tablo 13.4**

|      | Po    |  Ls    |  Lq   |  Ws    | Wq    |
|------|-------|--------|-------|--------|-------|
| 0.3  | 0.206 | 1.618  | 0.824 | 6.795  | 3.462 |
| 0.5  | 0.398 | 0.992  | 0.390 | 3.296  | 1.296 |
| 0.8  | 0.575 | 0.597  | 0.172 | 1.755  | 0.505 |
| 1.2  | 0.699 | 0.382  | 0.080 | 1.055  | 0.221 |

Tablo 13.4’den görüldüğü gibi, servis oranı 0.5’den 0.3’e düştüğünde, yani %40
azaldığında, sistemdeki makine sayısı %63 oranında artarak 0.99’dan 1.62’ye
çıkmaktadır. Kuyruk uzunluğu da bu değişiklikten olumsuz etkilenmekte %220
oranında artarak 0.39’dan 0.82’ye çıkmaktadır. Benzer şekilde ’nün %40 azalması
sistemde bekleme süresinin 2.522’den 6.795’e çıkmasına, yani %170 artmasına yol
açmaktadır. Servis oranındaki %40 oranındaki azalışın kuyrukta bekleme zamanının
%167 oranında artmasına neden olduğu görülebilir. = 0.3 yerine = 0.7 olduğunda,
yani servis hızı %40 arttığında, Ls %30, Lq %44 azalmaktadır. Servis hızındaki
%40’lık artışın Ws ve Wq üzerindeki azalış etkisi sırasıyla %17 ve %49’a
eşittir. Servis oranının %40 azalmasının parametre değerlerinde yol açtığı artış
oranlarının büyüklüğü servis oranındaki artışın parametre değerlerinde yol
açtığı azalış oranlarından çok büyük olduğu görülür. Kısaca sistemin işleyiş
özellikleri servis oranındaki arzu edilmeyen değişiklikten daha fazla
etkilenmektedir.

**13.4.2.3. Poisson-Üstel, Çok Servis, Sonsuz Geliş Kaynağı**

Yukarıdaki modellerde tek bir servis biriminin bulunduğu kabul edilmiştir. Bazı
kuyruk problemlerinde hizmet iki veya daha fazla servis birimince sağlanabilir.
İki veya daha fazla sayıda servis birimi varsa paralel veya seri servisten söz
edilir. Burada servislerin paralel oldukları, yani aynı hizmeti verdikleri kabul
edilecektir. Servis biriminin birden fazla olması durumunda üzerinde önemle
durulması gereken husus her servisin kendisine ait bir kuyruğunun mu bulunduğu
yoksa müşterilerin servise tek bir kuyruktan mı girdiğidir. Sistemde K sayıda
servis birimi olduğunu düşünelim. Her servisin kendisine ait bir kuyruğunun
olması durumunda sistem K tane tek kuyruklu sistemden oluşan bir sistem olarak
analiz edilebilir. Burada müşterilerin tek bir kuyruk oluşturdukları dikkate
alınacaktır. Bu koşullara uygun kuyruk sistemi için türetilecek modelden tutarlı
sonuçların elde edilmesi aşağıda açıklanan varsayımlara bağlıdır.

1.  Müşteri gelişleri, ortalama geliş hızı olmak üzere, Poisson dağılımlıdır.

2.  Servis süresi üstel dağılımlıdır.

3.  Geliş kaynağı sonsuzdur.

4.  Kuyruk disiplini ilk giren-ilk çıkar kuralına uygundur.

5.  Geliş oranı tüm servis birimlerinin birleştirilmiş servis hızından daha
    küçüktür.

6.  Tek bir kuyruk vardır.

7.  Her biri aynı hizmeti veren K sayıda servis birimi vardır.

Bu varsayımlar doğrultusunda,

= Ortalama geliş oranı

= Her bir servis biriminin ortalama servis hızı

K = Servis birimi sayısı

K = Birleştirilmiş ortalama servis hızı

= Sistem kullanım faktörü = /K

olmak üzere sistemin işleyiş özellikleri aşağıdaki gibi açıklanabilir.

**a**. Sistemin boş olması olasılığı:

**b**. Sistemde tam n sayıda müşteri bulunması olasılığı:

n K için

n \> K için

**c**. Kuyrukta bekleyen ortalama müşteri sayısı:

**d**. Sistemdeki ortalama müşteri sayısı:

**e**. Kuyrukta ortalama bekleme süresi:

**f**. Sistemde ortalama bekleme süresi:

ve K’nın değişik değerleri için P0 hesaplanmış ve hesaplama sonuçları Tablo
13.5’de verilmiştir. Sistemin çalışma özellikleri ile ilgili bağıntılardaki
P0’ın bu yolla belirlenmesi hesaplamalarda büyük kolaylıklar sağlayacaktır.

**Örnek 13.8**: Bir göz hastalıkları polikliniğinde her biri, saatte 2 hasta
muayene eden dört göz doktoru bulunmaktadır. Polikliniğe saatte ortalama 6 hasta
gelmektedir. Hastaların tek bir kuyrukta beklediklerini, servise bu kuyruktan
FIFO kuralına göre seçilerek alındıklarını, hasta gelişlerinin Poisson, servis
sürelerinin üstel dağıldığını düşünerek istenenleri hesaplayınız.

**a**. Sistem kullanım faktörünü,

**b**. Sistemin boş olması olasılığını.

**c**. Poliklinikte 3 hasta bulunması olasılığını,

**d**. Poliklinikte 6 hasta bulunması olasılığını,

**e**. Muayene olmak için bekleyen hasta sayısını,

**f**. Muayene edilmekte olan hasta sayısını,

**g**. Kuyrukta bekleme süresini,

**h**. Poliklinikte bulunma süresini.

**Çözüm 13.8**: = 6 hasta/saat , = 8 hasta/saat, K = 4’dür. Buna göre,

**a**. Sistem kullanım faktörü, = /K = 6/8 = 0.75

**b**. Sistemin boş olması olasılığı,

=

şeklinde yazılır.

Burada,

= 13,

ve

olduğundan, P0 aşağıdaki gibi hesaplanmış olur.

P0 = (13 + 13.5)-1 = 1/26.5 = 0.0377

Aynı olasılık değeri Tablo 13.5’in K = 4 sütunundan da bulunabilir. = 0.75
değeri tabloda bulunmadığından 0.75’e en yakın iki değer olan 0.74’e karşılık
gelen 0.401 ile 0.76’ya karşılık gelen 0.0355 değerlerinin ortalaması istenilen
olasılık değerini 0.0378 olarak verecektir.

## Tablo 13.5

| Servis Birimi Sayısı, K |       |       |       |       |       |       |        |        |
|-------------------------|-------|-------|-------|-------|-------|-------|--------|--------|
| K =                     | 2     | 3     | 4     | 5     | 6     | 7     | 8      | 10     |
| 0.02                    | .9608 | .9418 | .9231 | .9048 | .8869 | .8694 | .85214 | .81873 |
| 0.04                    | .9231 | .8869 | .8521 | .8187 | .7866 | .7558 | .72615 | .67032 |
| 0.06                    | .8868 | .8353 | .7866 | .7408 | .6977 | .6570 | .61878 | .54881 |
| 0.08                    | .8519 | .7866 | .7261 | .6703 | .6188 | .5712 | .52729 | .44933 |
| 0.10                    | .8182 | .7407 | .6703 | .6065 | .5488 | .4966 | .44933 | .36788 |
| 0.12                    | .7857 | .6975 | .6188 | .5488 | .4868 | .4317 | .38298 | .30119 |
| 0.14                    | .7544 | .6568 | .5712 | .4966 | .4317 | .3753 | .32628 | .24660 |
| 0.16                    | .7241 | .6184 | .5272 | .4493 | .3829 | .3263 | .27804 | .20190 |
| 0.18                    | .6949 | .5821 | .4866 | .4065 | .3396 | .2837 | .23693 | .16530 |
| 0.20                    | .6667 | .5479 | .4491 | .3678 | .3012 | .2466 | .20189 | .13534 |
| 0.22                    | .6393 | .5157 | .4145 | .3328 | .2671 | .2144 | .17204 | .11080 |
| 0.24                    | .6129 | .4852 | .3824 | .3011 | .2369 | .1864 | .14660 | .09072 |
| 0.26                    | .5873 | .4564 | .3528 | .2723 | .2101 | .1620 | .12492 | .07427 |
| 0.28                    | .5625 | .4292 | .3255 | .2463 | .1863 | .1408 | .10645 | .06081 |
| 0.30                    | .5385 | .4035 | .3002 | .2228 | .1652 | .1224 | .09070 | .04978 |
| 0.32                    | .5152 | .3791 | .2768 | .2014 | .1464 | .1064 | .07728 | .04076 |
| 0.34                    | .4925 | .3561 | .2551 | .1821 | .1298 | .0925 | .06584 | .03337 |
| 0.36                    | .4706 | .3343 | .2351 | .1646 | .1151 | .0804 | .05609 | .02732 |
| 0.38                    | .4493 | .3137 | .2165 | .1487 | .1020 | .0698 | .04778 | .02236 |
| 0.40                    | .4286 | .2941 | .1993 | .1343 | .0903 | .0606 | .04069 | .01830 |
| 0.42                    | .4085 | .2756 | .1834 | .1213 | .0800 | .0527 | .03465 | .01498 |
| 0.44                    | .3889 | .2580 | .1686 | .1094 | .0708 | .0457 | .02950 | .01226 |
| 0.46                    | .3699 | .2414 | .1549 | .0987 | .0626 | .0397 | .02511 | .01003 |
| 0.48                    | .3514 | .2255 | .1422 | .0889 | .0554 | .0344 | .02136 | .00820 |
| 0.50                    | .3333 | .2105 | .1304 | .0801 | .0490 | .0298 | .01816 | .00671 |
| 0.52                    | .3158 | .1963 | .1195 | .0721 | .0432 | .0259 | .01544 | .00548 |
| 0.54                    | .2987 | .1827 | .1094 | .0648 | .0381 | .0224 | .01311 | .00448 |
| 0.56                    | .2821 | .1699 | .0999 | .0581 | .0336 | .0194 | .01113 | .00366 |
| 0.58                    | .2658 | .1576 | .0912 | .0521 | .0296 | .0167 | .00943 | .00298 |
| 0.60                    | .2500 | .1460 | .0831 | .0466 | .0260 | .0144 | .00799 | .00243 |
| 0.62                    | .2346 | .1349 | .0755 | .0417 | .0228 | .0124 | .00675 | .00198 |
| 0.64                    | .2195 | .1244 | .0685 | .0372 | .0200 | .0107 | .00570 | .00161 |
| 0.66                    | .2048 | .1143 | .0619 | .0330 | .0175 | .0092 | .00480 | .00131 |
| 0.68                    | .1905 | .1048 | .0559 | .0293 | .0152 | .0079 | .00404 | .00106 |
| 0.70                    | .1765 | .0957 | .0502 | .0259 | .0132 | .0067 | .00338 | .00085 |
| 0.72                    | .1628 | .0870 | .0450 | .0228 | .0114 | .0057 | .00283 | .00069 |
| 0.74                    | .1494 | .0788 | .0401 | .0200 | .0099 | .0048 | .00235 | .00055 |
| 0.76                    | .1364 | .0709 | .0355 | .0174 | .0085 | .0041 | .00195 | .00044 |
| 0.78                    | .1236 | .0634 | .0313 | .0151 | .0072 | .0034 | .00160 | .00035 |
| 0.80                    | .1111 | .0562 | .0273 | .0130 | .0061 | .0028 | .00131 | .00028 |
|                         |       |       |       |       |       |       |        |        |

**Tablo 13.5 (Devam)**

| Servis Birimi Sayısı, K |       |       |       |       |       |       |        |        |
|-------------------------|-------|-------|-------|-------|-------|-------|--------|--------|
| K =                     | 2     | 3     | 4     | 5     | 6     | 7     | 8      | 10     |
| 0.82                    | .0898 | .0493 | .0236 | .0111 | .0051 | .0023 | .00106 | .00022 |
| 0.84                    | .0870 | .0428 | .0202 | .0093 | .0042 | .0019 | .00085 | .00017 |
| 0.86                    | .0753 | .0366 | .0170 | .0077 | .0035 | .0015 | .00067 | .00013 |
| 0.88                    | .0638 | .0306 | .0140 | .0063 | .0028 | .0012 | .00052 | .00010 |
| 0.90                    | .0526 | .0249 | .0113 | .0050 | .0021 | .0009 | .00039 | .00007 |
|                         |       |       |       |       |       |       |        |        |
| 0.92                    | .0417 | .0195 | .0087 | .0038 | .0016 | .0007 | .00028 | .00005 |
| 0.94                    | .0309 | .0143 | .0063 | .0027 | .0011 | .0005 | .00019 | .00003 |
| 0.96                    | .0204 | .0093 | .0040 | .0017 | .0007 | .0003 | .00012 | .00002 |
| 0.98                    | .0101 | .0045 | .0019 | .0008 | .0003 | .0001 | .00005 | .00001 |

**c**. Sistemde 3 müşteri bulunması olasılığı,

n K

**d**. Sistemde 6 müşteri bulunması olasılığı,

n \> K için

**e**. Kuyrukta bekleyenlerin ortalama sayısı:

hasta

**f**. Sistemde bekleyenlerin ortalama sayısı,

= 1.53 + 3 = 4.53 hasta

olarak hesaplandığından ve Lq = 1.53 olarak bilindiğinden,

Lmuayene = Ls - Lq = 4.53 - 1.53 = 3 hasta

**g**. Kuyrukta bekleme süresi,

= 1.53/6 = 0.255 saat = 15.3 dakika

**h**. Poliklinikte bekleme süresi,

= 0.255 + 1/2 = 0.755 saat = 45.3 dakika

*Maliyet Analizi*: Poliklinikteki doktor sayısının artırılarak beşe çıkarılmak
istendiğini düşünelim. Hastaların bekleme süresi maliyeti saat başına 20 TL,
doktorların ücreti ise 50 TL/saat olsun. Doktor sayısını artırmanın uygun olup
olmadığını kararlaştırınız.

Ortalama maliyet saat bakımından hesaplanabilir. Önce, dört doktorun olması
durumundaki toplam maliyeti hesaplayalım.

4 doktorun bir saat çalışmasının maliyeti = 4 x 50 = 200 TL’dir.

Polikliniğe saatte 6 hasta geldiğine ve her hasta ortalama 0.755 saat
beklediğine göre bekleme maliyeti, 6 hastanın poliklinikte toplam bekleme süresi
ile bekleme süresi maliyetinin çarpımına eşittir. Buna göre,

Bekleme Maliyeti = (6 x 0.755) x 20 = 4.53 x 20 = 90.6 TL/saat

Olduğundan toplam maliyet aşağıdaki gibi hesaplanır.

Toplam Maliyet = 200 + 90.6 = 290.6 TL/saat

Doktor sayısı 5olduğunda bir saatlik servis maliyeti aşağıdaki gibi hesaplanır.

Servis Maliyeti = 5 x 50 = 250 TL

Poliklinikte 5 doktor bulunduğunda değişeceğinden Ws yeniden hesaplanmalıdır. =
10, K = 5 için Tablo 13.5’den P0 = 0.0466 belirlemesiyle,

hasta, Wq = Lq/ = 0.353/6 = 0.059 dakika, Ws = 0.059 + 1/2 = 0.559 dakika olarak
hesaplandığından,

Bekleme maliyeti = (6 x 0.559) x 20 = 67.08 TL olur.

Servis maliyeti 250 TL olarak hesaplandığından toplam maliyet,

TM = 250 + 67.08 = 317.08 TL olarak elde edilir.

Buna göre, dört doktorun bulunması durumunda toplam maliyet daha düşük
olduğundan doktor sayısının 5’e çıkarılmasının uygun olmadığı kararlaştırılır.

# PROBLEMLER

**1.** Bir adet yükleme havuzlu bir ambarda yüklemeden sorumlu üç tayfa vardır.
Havuza saatte ortalama 4 kamyon gelmektedir. Bir kamyonun yüklenmesi ortalama 4
dakikada tamamlanmaktadır. Bir kamyonun çalışmamasının maliyeti 20 TL/saat dir.
Tayfalara saat başına 10 TL ödenmektedir. Yeni bir tayfanın alınmasıyla bir
kamyonun yüklenmesi 3 dakikada tamamlanacaktır.Yeni bir tayfanın alınması sizce
uygun mudur?

**2.** Bir kafeteryada ödeme yapmak için saatte ortalama 10 kişi kasaya
gelmektedir. Ödeme kişi başına ortalama 5 dakikada tamamlanmaktadır. Gelişlerin
Poisson, çıkışların üstel dağılım gösterdiği kabul edildiğine göre,

**a.** Trafik yoğunluğunu,

**b.** Kasiyerin aylak kalması olasılığını,

**c.** Ödeme yapmak için bekleyenler ile ödeme yapanların sayısını,

**d.** Kafeteryada bulunanların sayısını,

**e.** Müşterilerin ödeme kuyruğunda bekleme süresini hesaplayınız.

**3.** Bir TV tamircisi bir TV’yi ortalama 40 dakikada tamir etmektedir. Bu süre
değişkendir ve üstel dağılıma uyduğu kabul edilmektedir. Tamir atölyesine 8
saatlik bir iş gününde ortalama 6 TV gelmektedir. TV’lerin atölyeye gelişleri
Poisson dağılımına uygundur. Buna göre,

**a.** Tamir edilecek TV bulunmaması olasılığını,

**b.** Onarım için bekleyen TV sayısını,

**c.** Belirli bir t zamanında tamircinin aylak kalması olasılığını,

**d.** Bir TV’nin atölyedeki ortalama bekleme süresini,

**e.** TV’lerin bozulma oranı %20 arttığında onarım için bekleyen TV sayısını
hesaplayınız.

**4.** Bir markette saatte ortalama 10 kişi ödeme için kasaya gelmektedir.
Müşteriler kasa önünde çok uzun beklediklerinden yakınmaktadırlar. Kasiyer
saatte ortalama 12 kişiye hizmet verebilmektedir.

**a.** Müşterilerin ödeme kuyruğunda harcadığı ortalama süreyi,

**b.** Kasiyerin aylak kalması olasılığını,

**c.** Müşterilerinin kuyrukta 12 dakikadan daha uzun kalma olasılığını
hesaplayınız.

**5.** Bir fabrika günde 8 saat olmak üzere yılda 240 gün çalışmaktadır. Fabrika
çok sayıda küçük makine satın almıştır. Bu makinelerin bakım ve onarımı ücreti 4
TL/saat olan bir makine mühendisi tarafından yapılmaktadır. Bir makinenin bir
saat çalışmamasının işletmeye maliyeti 8 TL’dir. Makinelerin satın alındığı
işletme makinelerin bakım ve onarımını da üstlenebileceklerini söylemiştir.
Satıcı herhangi bir arıza durumunda fabrikaya bir tamirci göndermeyi kabul
etmektedir. Satıcı bu iş için fabrika yönetiminden yıllık 20000 TL talep
etmektedir. Bir makinenin bakım ve onarımını fabrika mühendisi 1.7 günde,
satıcının tamircisi 1.5 günde tamamlamaktadır. Makinelerin arızaya geçmesi
rasgele olup ortalama 5 günde 2 makine olmak üzere Poisson dağılım
göstermektedir. Fabrika yöneticisine makinelerin bakım ve onarımı için satıcının
önerisini tavsiye eder misiniz?

**6.** Bir banka para yatırmak veya para çekmek isteyen müşterilerine birer
görevli tahsis etmiştir. Para çekme ve para yatırma işlemlerinin her ikisi 3’er
dakikada tamamlanmaktadır. Servis sürelerinin üstel dağıldığı kabul
edilmektedir. Bankaya para çekmek için gelenlerin sayısı saatte ortalama 16,
para yatırmak için gelenlerin sayısı saatte ortalama 14’dür. Bu iki görevlinin
her birinin her iki hizmeti yerine getirmesi durumunda müşterilerin kuyrukta
bekleme süreleri ne yönde değişir hesaplayınız. Servis süresi 3.5 dakika olursa
ortalama kuyruk uzunluğu ne olur?

**7.** Günün 24 saati hizmet veren bir poliklinik acil servisine günde ortalama
96 hasta gelmektedir. Her hastaya ortalama 10 dakika zaman ayrılmaktadır. Bir
hastaya 10 dakikalık zaman ayırmanın kliniğe maliyeti 100 TL’dir. Ortalama
servis zamanındaki 1 TL’lik azalış kliniğin hasta başına harcamasını 10 TL
azaltmaktadır. Acil serviste uzun kuyrukların oluştuğunu gören klinik yöneticisi
kuyrukta bekleyenlerin sayısını %60 oranında azaltmayı istemektedir. Bunu
sağlamak için yönetici kaç liralık bir bütçe ayırmalıdır?

**8.** Günde 8 saat çalışan bir işyerine müşterilerin geliş hızı saatte ortalama
20’dir. Halihazırdaki servis mekanizması ile saatte ortalama 30 müşteriye servis
sağlanabilmektedir. Buna göre,

**a.** Bir müşterinin işyerinde harcadığı ortalama süreyi hesaplayınız.

**b.** İşyeri yöneticisi servis hızını saatte 40 müşteriye hizmet verecek
şekilde düzenleyip düzenlememe konusunda karar vermek istemektedir. Bekleme
zamanı maliyeti en fazla ne olursa servis hızlandırılmalıdır.

**9.** 5 dakikada ortalama 3 araç paralı otoyol girişindeki gişeye gelmektedir.
Araçların gelişi Poisson dağılımına uygundur. Her bir ödeme yaklaşık 1 dakikada
tamamlanmaktadır. Ödemenin tamamlanması zamanı üstel dağılımlıdır. Buna göre,

**a.** 10 dakikalık zaman aralığında gişeye, 0, 1, 2, 3, 4, 5 müşteri gelmesi
olasılıklarını,

**b.** 8 saatlik bir iş gününde gişe memurunun boş olduğu süreyi,

**c**. Ortalama kuyruk uzunluğunu,

**d.** Sistemdeki müşteri sayısını,

**e.** Ödeme yapmak için kuyrukta bekleyen müşteri sayısını hesaplayınız.

**10. B**üyük bir otelin çamaşırhanesinde 6 adet çamaşır makinesi vardır.
Makineler rasgele zamanlarda arızalanmaktadır. Birbirini izleyen iki arıza
arasında ortalama 4 saat geçmektedir. Arızalanan bir makinenin onarımı yaklaşık
45 dakikada tamamlanmaktadır. Makinelerin onarımı üstel dağılım izlemektedir. Bu
bilgileri kullanarak istenenleri hesaplayınız.

**a.** Trafik yoğunluğu.

**b.** Onarım atölyesinde 1, 2, 3, 4, 5 ve 6 adet çamaşır makinesi bulunması
olasılığı.

**c.** Bir makinenin kuyrukta bekleme süresi.

**d.** Bir makinenin onarım atölyesinde bulunduğu süre.

**e.** Onarım atölyesinde bulunan makine sayısı.

**f.** Kuyrukta bekleyen makine sayısı.

**11.** Büyük bir alış veriş merkezine elektrik sağlayan 4 büyük jenaratör
vardır. Jenaratörler zaman zaman arızalanarak elektrik dağıtımının aksamasına
sebep olmaktadırlar. Geçmiş dönem deneyimlerinden bir jenaratörün ortalama her
12 ayda bir arızalandığı bilinmektedir. Jenaratörlerin bakım ve onarımlarının
gerçekleştirildiği atölyenin sahibi bir arızanın yaklaşık 2 ayda giderildiğini
açıklamıştır. Buna göre,

**a.** Atölyenin boş olması olasılığını,

**b.** Atölyedeki arızalı jenaratör sayısının 1, 2, 3 ve 4 olması
olasılıklarını,

**c.** Atölyedeki jenaratör sayısını,

**d.** Bir jenaratörün kuyrukta bekleme süresini hesaplayınız.

**12.** Bir hastanede kontrol için gelenlerin kayıtları tek bir memur tarafından
yapılmaktadır. Ortalama 1.5 dakikalık zaman aralıklarında gelmekte olan
hastaların kontrolünden sorumlu 5 doktor vardır. Her bir hastanın kontrolü üstel
dağılıma uygun olarak 6 dakikada tamamlanmaktadır. Buna göre,

**a.** Trafik yoğunluğunu,

**b.** Her üç doktorun aylak kalması olasılığını,

**c.** Hastanede tam üç hasta bulunması olasılığını,

**d.** Kontrol için bekleyen hastalardan oluşan kuyruğun uzunluğunu,

**e.** Hastanede bulunan hastaların beklenen sayısını,

**f.** Hastanede tam 8 hasta bulunması olasılığını,

**g.** Bir hastanın kuyrukta ortalama bekleme süresini,

**h.** Bir hastanın hastanede ortalama bekleme süresini hesaplayınız.

**13.** Bir büroda mektupların daktilo edilmesinden sorumlu iki sekreter vardır.
Her bir sekretere saaatte ortalama 3 mektup gelmekte ve her bir sekreter bir
saatte ortalama 3 mektup daktilo etmektedir.

**a.** Her bir sekreterin kendi işini yapması durumunda bir mektubun daktilo
edilmek için beklediği süreyi hesaplayınız.

**b.** İki sekreterin ortaklaşa çalışmaları durumunda bir mektubun daktilo
edilmek için beklediği süreyi bulunuz.

**14.**Küçük bir postanede müşteri hizmetinden sorumlu iki memur vardır. Hizmet
tamamlama hızları aynı olan memurların her biri bir hizmeti ortalama 1.5
dakikada tamamlamaktadır. Postaneye her bir dakikada bir müşteri gelmektedir.
Buna göre,

**a.** Postanede hiç müşteri bulunmaması olasılığını,

**b.** Postanede 1 müşteri bulunması olasılığını,

**c.** Postanede 5 müşteri bulunması olasılığını,

**d.** Kuyrukta bekleyen ortalama müşteri sayısını,

**e.** Postanede bulunan ortalama müşteri sayısını,

**f.** Bir müşterinin postanede ortalama bekleme süresini hesaplayınız.

**15.** Randevusuz müşterinin kabul edilmediği bir işyerinde randevular müşteri
gelişlerinin tam 10 dakikada bir olmasını sağlayacak biçimde ayarlanmaktadır.
Gerekli evrakların düzenlenmesi, muayene ve dağıtım işlemleri tam 15 dakikada
tamamlanmaktadır. Bu işlerden sorumlu çalışana saat başına 8 TL ödenmektedir.
İlk müşteri, işyeri açılır açılmaz gelmekte ve işyerinde kendisiyle ilgilenecek
bir sorumluyu kendisini bekler bulmaktadır. İşyerinin herhangi bir işgününün ilk
üç saati içindeki (180. dakikada gelen müşteri dahil) durumu için,

**a.** Sekizinci ve dokuzuncu müşterinin işyerinden ne zaman ayrılacaklarını
hesaplayınız.

**b.** 19. müşterinin servisinin tamamlanmasından sonraki aylak zamanı göz ardı
ederek müşterinin bekleme zamanı maliyeti ile memurun aylak zaman maliyeti
toplamını bulunuz.

**c.** Servisin iki memur tarafından sağlanması durumunda (a) ve (b)’nin
yanıtları nasıl olur?

**d.** İki memurlu durumda, 8 saatlik bir iş gününde kaç kişiye randevu
verilmesi gerektiği bulunuz.

**e.** Randevu verilmesi gereken müşteri sayısı (d)’deki gibi olduğunda, toplam
maliyetin en küçük olmasını sağlayacak memur sayısı ne olur?

**16.** Müşterilerle muhatap olan tek bir memurun bulunduğu bir bankada
müşterilerin oturmaları için iki sandalye vardır. Müşterilerin bankaya gelişleri
rasgele olup 10 dakikada bir müşteri gelmektedir. Her müşteriye verilen hizmet 5
dakikada tamamlanmaktadır. Uygun varsayımları yaparak,

**a.** Gelen bir müşterinin sandalyeye oturması olasılığını,

**b.** Gelen müşterinin ayakta beklemesi olasılığını,

**c.** Müşterinin ortalama bekleme zamanını hesaplayınız.

**17.** Her 15 dakikada bir müşteri çek tahsili için bankaya gelmektedir. Çekin
ödenmesi ile ilgili işlemler tek bir görevli tarafından 10 dakikada
gerçekleştirilmektedir. Uygun varsayımları yaparak,

**a.** Ortalama kuyruk uzunluğunu,

**b.** İkinci bir görevlinin tahsis edilmesini gerektiren müşteri geliş
hızındaki artışı hesaplayınız.

**18.** Bir ekmek fabrikasına müşterilerin gelişleri Poisson dağılımına
uygundur. Fabrikadaki satış sorumlusu bir saatte ortalama 12 müşteriye hizmet
verebilmektedir. Servis zamanı üstel dağılımlıdır. Müşterilerin ortalama geliş
hızı saatte 20 kişidir. Sizce bu sistem çalışır mı? Gerekçesiyle yanıtlayınız.

**19.** Bir önceki problemdeki ekmek fabrikasında servis hızı aynı kalmış,
müşteri geliş hızı saatte 10 kişiye düşmüştür. Fabrika yöneticisi müşteri geliş
hızındaki düşüşe müşterilerin fazla bekletilmelerinin yol açtığına inanmaktadır.
Fabrika günde 10 saat çalışmakta ve satış sorumlusuna saatte 80 TL ödenmektedir.
Yönetici satışların daha hızlı gerçekleştirilmesi için bir kişi daha istihdam
ederek bir saatlik servis oranını saatte 20 kişiye çıkartmak istemektedir.
Müşterilerin beklemekten ötürü maliyetlerinin saatte 500 TL olduğu kabul
edilmektedir. Buna göre satıştan sorumlu ikinci kişinin alınmasının uygun olup
olmadığına karar veriniz.

**20.** Bir havaalanına turizm sezonunda saatte ortalama 20 uçak inmektedir. İyi
havalarda havaalanının kapasitesi saatte 60 uçak iken kötü havalarda bu sayı 30
uçağa inmektedir. Havaalanında karmaşa olduğunda uçaklara alana inme izni
verilmemekte ve uçaklar havaalanı yakınlarında uçmaya zorlanmaktadır.

**a.** İyi havalarda alana inmek için izin bekleyen uçak sayısını bulunuz.

**b.** Kötü havalarda alana inmek için izin bekleyen uçak sayısını bulunuz.

**c.** İyi hava koşullarında bir uçağın havaalanına inmek için ne kadar süreyle
uçacağını hesaplayınız.

**21.**Bir araba yıkama servisine saatte ortalama 10 araba gelmektedir. Bir
araba 5 dakikada yıkanmaktadır. Servis süresi üstel dağılımlıdır. Arabaların
yıkamaya alınmadan önce park edebilecekleri yere en fazla üç araba sığmaktadır.
Park yeri yoksa müşteriler arabalarını bir başka yere almakta ve orada
beklemektedirler. Sistemin durağan durumda olduğunu varsayarak,

**a.** Servise gelen bir arabanın park yerinde yer bulması olasılığını
hesaplayınız.

**b.** Servise gelen bir arabanın park yeri dışında bir yerde beklemesi
olasılığını bulunuz.

**c.** Sistemde ortalama kaç araba bulunduğunu hesaplayınız.

**d.** Sistemde beklenen ortalama bekleme süresini bulunuz.

**e.** Kuyrukta beklenen ortalama bekleme süresini bulunuz.

**f.** Servise gelen tüm müşterilerin i. zamanın en az %20’sinde, ii. zamanın en
az %50’sinde park etmelerini sağlamak için kaç arabalık park yeri düzenlenmesi
gerektiğini bulunuz.

**22.**Evlere su servisi yapan bir su dağıtım istasyonunun 4 hatlı bir telefonu
vardır. Hatlardan biri meşgulken arayan olursa arayan kişi boş hatlardan birinde
bekletilmeye alınmaktadır. Hatların hepsi meşgul olduğunda arayan biri meşgul
sinyali almakta ve başka bir su dağıtım istasyonunu armaktadır (müşteri kaybı).
Saatte ortalama 30 müşteri telefon ettiğine ve her konuşma ortalama 1.5 dakika
sürdüğüne göre,

**a.** Arayan bir müşterinin hemen konuşması olasılığını,

**b.** Arayan müşterinin beklemeye alınması olasılığını,

**c.** Arayan müşterinin beklerken geçirdiği süreyi,

**d.** 8 saatlik bir iş gününde kaybedilen müşteri sayısını hesaplayınız.
