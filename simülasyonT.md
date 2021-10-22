##### ONBEŞİNCİ BÖLÜM

#### *SİMÜLASYON*

15.1. GİRİŞ

Herhangi bir problemle karşılaşıldığında akla öncelikle, problemin analitik
yaklaşımla çözülmesinin mümkün olup olmadığı sorusu gelir ve problemin analitik
yaklaşımla çözülebilecek bir yapıya oturtulmasına çalışılır. Oysa analitik
yaklaşımların hemen hepsi, belirli varsayımların sağlanması durumunda
uygulandıklarından, ulaşılan sonuçların geçerliliği ve güvenilirliği yapılan
varsayımların geçerliliği ile sınırlı kalır. Yapılan varsayımlar geçerli olsalar
bile, sırf analitik çözümü mümkün kılmak için gerçeğin bir bölümünden
vazgeçilmesi sorun yaratabilir. Bu gibi durumlarda daha az sayıda varsayım
gerektiren ve varsayımların gerçekleşmemesi durumuna karşı daha az duyarlı olan
benzetim yolu ile çözümün, yani simülasyonun kullanılması uygun olur.

Karmaşık sistemlerin incelenmesinde yaygın biçimde kullanılan simülasyon, gerçek
bir sürecin veya sistemin zaman boyutundaki davranışını kestirmek amacıyla
oluşturulan modele, araştırıcı tarafından düzenlenen deneme-yanılma deneylerinin
uygulanmasıdır. Deneme-yanılma deney sonuçlarının gözlenmesi ile sürecin nasıl
işlediğinin gözlenmesi arasında büyük benzerlikler vardır. Bu nedenle, belirli
değişiklikler karşısında sürecin göstereceği tepki, aynı değişiklikler
karşısında modelin gösterdiği tepki ile tahminlenmeye çalışılır. Kısaca,
modelden sağlanan bulgular gerçek sistemin tepkisine benzetilir. Sözgelimi bir
uçak tasarımında, uçağın aerodinamik özelliklerinin uçağın üretilmesinden önce
incelenmesi zorunludur. Bu durumda tasarımcı uçağın aerodinamik özelliklerini bu
amaca yönelik olarak tanımladığı eşitliklerin çözümüyle belirlemek ister.
Eşitlikleri çözmek çok zor, hatta imkansız olduğunda, uçağın bir maketini yapmak
ve maket uçağın rüzgar tünelindeki davranışlarını incelemek yeterli olur. Elde
edilen bulgulardan gerçek uçağın rüzgar karşısında göstereceği tepki, yani
aerodinamik özellikleri tahmin edilir. Özetle, simülasyonda genellikle analitik
yaklaşımla çözülemeyen modeller kurulur. Uzay uçuçlarında veya füze gezinti
haritalarının çıkarılmasında olduğu gibi gerçek sistemin veya gerçek sürecin
özelliklerinin gözlenmesinin çok zor hatta imkansız olduğunda simülasyon tek
çaredir.

Diğer tekniklerin çoğu gibi simülasyonun da sayısız avantaj ve dezavantajı
vardır. En önemli avantajı basit oluşudur. Simülasyon yöntemlerinin uygulanması,
daha fazla aritmetik işlem gerektirmesine karşın, analitik yöntemlerin
uygulanmasından çok daha kolaydır. Yalnızca analitik çözümlerin yerine değil,
analitik yaklaşımla belirlenen çözümlerin doğruluğunu gerçeklemek için de
kullanılabilmesi simülasyonun diğer bir avantajıdır. Simülasyon modelleri
analitik modellerden daha az sayıda varsayım gerektirdiklerinden gerçek sistemin
temsili bakımından daha esnektirler. Simülasyon modeli bir kez tasarlandıktan
sonra farklı politikalar, parametreler veya tasarımlar için tekrar tekrar
kullanılabilir. Bu kadar çok avantaja sahip olması, araştırıcıların analitik
yöntemlerin daha uygun olduğu durumlarda da simülasyonu kullanmaları yanılgısına
neden olmaktadır. Bu avantajlarının yanında kesin olmayışlığı simülasyonun
önemli dezavantajlarından biridir. Simülasyon bir en iyileme yöntemi de
değildir. Simülasyon ile en iyileme mümkün olmakla birlikte en iyi çözüme ulaşma
süreci çok yavaş işler. Simülasyon yanıt değil yalnızca sistemin farklı işleyiş
koşullarında göstereceği tepkiyi açıklar. Pek çok durumda bu kesin olmayışlığı
ölçmek oldukça zordur. İyi bir simülasyon modelinin kurulması çok pahalı ve
zaman alıcı olabilir. Sözgelimi, kullanılabilir nitelikte bir planlama modelinin
oluşturulması yıllar sürebilir. Simülasyon çözüm tekniği değil çözüm geliştirme
yolu yaratır. Tüm durumlar simülasyon ile açıklanamaz. Bir durumun simülasyona
uygun olabilmesi için belirsizlik göstermesi ve rasgele bileşen içermesi
gerekir.

15.2. TEMEL KAVRAMLAR ve SİMÜLASYON SÜRECİ

Simülasyon çalışmaları genellikle sistemlerin simülasyonu ile ilgilidir. Bir
sistemin simüle edilmesinin anlamını kavrayabilmek için sistem kavramı
açıklanmalıdır.

*Sistem*: Belirli bir amacı gerçekleştirmek üzere bir arada bulunan ve
birbirlerini karşılıklı olarak etkileyen varlıklardan oluşan bir topluluktur.

Birden fazla parçadan oluşan her bütün bir sistem olarak incelenebilir. Sistemin
kesin tanımı genellikle simülasyon çalışmasının amaçlarına bağlıdır. Belirli bir
çalışma için sistem olarak ele alınan bir topluluk bir başka çalışmada sistem
olarak ele alınan bir topluluğun yalnızca bir alt kümesi hatta bir varlığı
durumunda olabilir.

Sistemler genellikle dinamiktir. Yani, durumları zaman içinde değişiklik
gösterir. Bu eğilimi açıklamak için durum kavramını tanımlayalım.

*Durum*: Zaman boyutunun herhangi bir anında sistemin karakteristiklerinin ve
görünümünün açıklanması bakımından önemli ve gerekli olan değişkenler
topluluğuna sistemin durumu denir.

Bu iki kavramı günlük yaşamdan bir örnekle, sözgelimi bir hastanenin acil
servisiyle açıklayalım. İncelenen sistem acil servistir. Söz konusu sistem, 1.
Doktorlardan, 2. Tedavi edilen hastalardan, 3. Tedavi edilmeyi bekleyen
hastalardan oluşur. Sistemin durumu hastaların servise gelişleri ve tedavisi
tamamlanan hastaların servisten ayrılışlarıyla değişir.

Sistemin durumundaki değişmeler durum değişkenleri ile ifade edilir. Meşgul
doktor sayısı, servisteki hasta sayısı, servise yeni bir gelişin gerçekleşme
zamanı, tedavisi tamamlanan bir hastanın servisten ayrılma zamanı gibi
değişkenler sistemin durumundaki değişmeleri açıklarlar. Bu nedenle bu
değişkenler sistemin durum değişkenleri olarak kullanılabilir.

Herhangi bir sistemde ilgilenilen bir nesneye "varlık", bu varlığın değişik
özelliklerinin her birine "nitelik" denir. Sözgelimi acil servise başvuran
hastalar varlık olarak ele alındıklarında onların yaş, eğitim düzeyi, medeni
durum, aylık gelir, cinsiyet gibi özellikleri nitelikleri olarak ele alınabilir.

Sistemler parçalarının özellikleri, çevresini oluşturan sistemlerle
etkileşimleri, davranışları, durum değişkenlerinin özellikleri, zaman
boyutundaki gelişimi vb. açılardan sınıflandırılmaktadır. Çevresini oluşturan
sistemlerle etkileşimine göre açık ve kapalı sistemler, zaman boyutundaki
gelişimine göre statik ve dinamik sistemler olarak sınıflandırılmaktadır. Durum
değişkenleri esas alındığında ise kesikli veya sürekli sistemler olarak
sınıflandırılırlar. Simülasyon için önemli olan sınıflandırma budur.

*Kesikli Sistem*: Durum değişkenlerinin yalnızca zaman boyutunun sayılabilir
veya kesikli noktalarında değiştiği sistemlere kesikli sistemler denir.

Yukarıdaki acil servis kesikli bir sistemdir. Çünkü sistemin durum değişkenleri
yalnızca servise bir hasta geldiğinde veya servisten bir hasta ayrıldığında
değişir. Bu değişiklikler zamanın belirli noktalarda gerçekleşir.

*Sürekli Sistem*: Durum değişkenleri zaman içinde sürekli değişen sistemlere
sürekli sistemler denir.

Herhangi bir kimyasal süreç sürekli sisteme örnek gösterilebilir. Buradaki
sistem zaman içinde sürekli değişir. Bu tür sistemler genellikle diferansiyel
eşitliklerle açıklanırlar.

Uygulamada tam anlamıyla kesikli veya tam anlamıyla sürekli bir sistemle
karşılaşma olasılığı oldukça düşüktür. Genellikle sistemler bu iki sistemin
özelliklerini taşır niteliktedirler. Bu durumda hangi sistemin özellikleri ağır
basıyorsa sistem o grupta değerlendirilmelidir.

*Model*: Sistemin veya sürecin davranışlarını kontrol etmek, anlaşılabilirliğini
artırmak ve gelecekteki davranışlarını kestirmek amacıyla oluşturulan
basitleştirilmiş temsile model denir.

Simülasyon amacıyla kurulan modele simülasyon modeli denir. Simülasyon modeli
genellikle sistemin işleyişi ile ilgili varsayımlar doğrultusunda sistemin
önemli bileşenleri arasındaki ilişkileri matematiksel veya mantıksal sembollerle
açıklayan bir kümedir.

Simülasyon modelleri esas olarak statik ve dinamik simülasyon modelleri olmak
üzere iki başlık altında incelenir.

*Statik Simülasyon Modeli*: Sistemin zaman boyutunun herhangi bir anındaki
durumunu gösteren simülasyon modeline statik simülasyon modeli denir. Zamanın
sistem üzerinde etkili olmaması durumunda kurulan simülasyon modelleri de
statiktir.

Statik simülasyon modeli ile genellikle Monte Carlo modelleri kastedilmektedir.

*Dinamik Simülasyon Modeli*: Sistemin zaman boyutundaki gelişmesini gösteren
simülasyon modeline dinamik simülasyon modeli denir.

Görüldüğü gibi simülasyon modeli deterministik veya olasılıksal olabilir.

*Deterministik Simülasyon Modeli*: Olasılıksal veya rasgele bileşen içermeyen
simülasyon modeli deterministik simülasyon modelidir.

Bir kimyasal reaksiyonu tanımlayan diferansiyel eşitlikler sistemi deterministik
simülasyon modelidir. Girdinin belirli olması durumunda sistemin çıktısı kesin
çizgilerle belirlenebilir.

*Olasılıksal Simülasyon Modeli*: Bir ya da daha fazla sayıda rasgele değişken
içeren simülasyon modeli olasılıksal simülasyon modelidir.

Stok ve kuyruk sistemlerinin çoğu olasılıksal simülasyon modeli olarak
formüllenir. Olasılıksal simülasyon modelleriyle elde edilen çıktının kendisi de
olasılıksal olduğundan çıktılar, sistemin belirli özelliklerinin gerçek
değerleri değil tahminleridir. Kesikli ve sürekli simülasyon modelleri kesikli
ve sürekli sistemlere benzer. Bu tür modellere "kesikli-olay simülasyon
modelleri" de denir. Kesikli-olay simülasyon modelleri zaman boyutunda değişen
olasılıksal sistemlerin modellenmesiyle ilgilidir.

*Simülasyon Süreci*: Etkin simülasyon çalışmalarının hepsi planlama ve
organizasyon gerektirir. Durumun karmaşıklığına bağlı olarak adımların sırası ve
sayısı değişse de sürecin genel olarak aşağıdaki adımları kapsadığı kabul
edilir. Simülasyon çalışmasının başarılı olabilmesi bakımından her biri son
derecede önemli olan bu aşamalar aşağıda açıklanmıştır.

1\. *Benzetilecek sistemin veya problemin tanımlanması ve amaçların
belirlenmesi*: Modelleme sürecindeki ilk adım problemin en ufak bir yanılgıya
yol açmayacak biçimde açık ve tam olarak belirlenmesidir. Problemin doğru
tanımlanması yalnızca uygun modelin tasarlanmasını kolaylaştırmakla kalmaz,
simülasyon sonuçlarının değerlendirilmesine de esas oluşturur. Genel olarak
simülasyonun hedefi incelenen sistemin belirli koşullarda göstereceği tepkinin
belirlenmesidir. Araştırıcının neyi araştırdığını bilmesi simülasyonun
başarısını artırır. Bu nedenle simülasyonun ayrıntısı ve kapsamı konusunda çok
titiz davranılması gerekir.

2\. *Uygun modelin oluşturulması*: Uygun modelin kurulması simülasyon sürecinin
ikinci aşamasıdır. Geçerli sonuçlara ulaşabilmek için model sistemin simüle
edilmek istenen önemli özelliklerini yansıtmalıdır. Simülasyon modeli fiziksel,
matematiksel, kavramsal veya bunların bir karması durumunda olabilir. Simülasyon
modellerinin büyük bir kısmı fiziksel model olarak belirir. Fiziksel modeller
araştırılacak sistemin gerçek görünümünde olurlar fakat, nicel karar almada
kullanılamazlar. Tahta veya bir başka hammaddeden yapılacak bir gemi veya uçağın
aynı hammaddelerden yapılan maketleri fiziksel simülasyon modellere örnek olarak
verilebilir. Fiziksel model oluşturması genellikle fazla harcamaya yol
açtığından ve nicel karar almada kullanılamadığından mümkünse matematiksel model
kurulması uygun olur. Bilindiği gibi matematiksel modeller sistemin önemli
bileşenlerini ve bileşenler arasındaki etkileşimleri matematik sembol ve
bağıntılarla açıklayan modellerdir.

3\. *Veri derleme*: Veri derleme model kurma aşamasının en önemli kısmıdır. Hangi
verilerin derleneceği ve gerekli veri miktarı üzerlerinde titizlikle durulmaları
gereken konulardır. Bu aşama modelin gerektirdiği verileri tanımlama ve onları
kullanılabilecek ölçülere indirgeme aşamasıdır. Veri, hem model geliştirme hem
de modelin değerlendirilmesi için gereklidir.

4\. *Modelin denenmesi*: Modelin düzenlenmesinden sonra sıra çalıştırılmasına
(deneme) gelir. Model deterministic, yani bütün parametreleri biliniyor ve
sabitse bir kez çalıştırılması yeterli olur. Simülasyon olasılıksal, yani sistem
parametreleri rasgele değişim gösteriyorsa modelin geçerliliğinin sınanmasında
ve doğruluğunun kanıtlanmasında birkaç kez çalıştırılması gerekecektir.
Stokastik simülasyon modelinin her bir çalıştırılışında bir gözlem elde edilir.
Bu yönüyle olasılıksal simülasyon, rasgele örnek seçimine benzer. Bu nedenle en
iyi örnek büyüklüğünün, yani simülasyonun kaç kez tekrarlanacağının
belirlenmesinde istatistik kuramına başvurulabilir. Simülasyon sonuçlarının
fazla değişkenlik göstermesi durumunda belirli bir güvenilirlik sağlamak için
modelin pek çok kez çalıştırılması gerekebilir.

5\. *Sonuçların değerlendirilmesi*: Simülasyon sürecinin bu aşamasında modelin
çalıştırılması ile sağlanan sonuçlar yorumlanır ve analiz edilir. Sonuçların
yorumlanması ile simülasyon sonuçlarından çıkarımda bulunulur. Simülasyon
sistemi gerçek sisteme ne kadar yakınsa sonuçların düzeltilmesine duyulan
gereksinim ve sonuçların uygulanmasıyla karşılaşılacak risk de o ölçüde az olur.

6\. *Uygulama*: Simülasyon sürecinin son aşaması modeli ve sonuçlarını uygulamaya
koymaktan ibarettir.

15.3. KESİKLİ-OLAY SİMÜLASYON Örneğİ

Kesikli-olay simülasyonu, durum değişkenleri zamanın ayrı ayrı noktalarında
birdenbire değişen sistemlerin modellenmesiyle ilgilidir. Bu tür simülasyon
modellemesinin ayrıntılarına girmeden önce kesikli-olay simülasyonundaki temel
kavramlar basit bir simülasyon örneği ile açıklanacaktır. Kesikli-olay
simülasyon çalışmalarının çok büyük bir kısmı kuyruk sisteminin simülasyonu ile
ilgili olduğundan burada tek servisli bir kuyruk sistemi üzerinde durulacaktır.
Simüle edilecek tek servisli kuyruk sisteminde müşterilerin kuyruk sistemine
rasgele zamanlarda ve tek tek geldikleri, servis boş ise hizmet almak için
servis sistemine girdikleri, servis meşgulse kuyruğa girerek hizmet sırasının
kendilerine gelmesini bekledikleri varsayılmaktadır. Bilindiği gibi bu model bir
önceki bölümde incelenmiş, sistemin işleyiş özellikleri analitik yaklaşımla
açıklanmıştır. Analitik yaklaşım için sisteme gelişlerin Poisson, sistemden
ayrılışların (servis sürelerinin) üstel dağıldığı varsayımları başta olmak üzere
pek çok varsayım yapılmıştır. Uygulamada bu varsayımlar çoğu zaman gerçekleşmez.
Sözgelimi, gelişlerin tek tek değil gruplar halinde olması durumunda kuyruk
kuramı geçerliliğini yitirir. Bu gibi durumlarda geliş sürecine ilişkin bir
deneysel dağılım yaratılması uygun olur. Simülasyon ile gelişler arası ve servis
sürelerine ilişkin herhangi bir dağılım kullanılabilir. Bu durum, çözüm sürecine
daha fazla esneklik, ulaşılan sonuçlara daha fazla güven duyulmasını sağlar.
Kuyruk sistemini simüle etmek için önce sistemin özelliklerini açıklayalım.
Potansiyel müşteri kaynağı sınırsızdır. Sınırsız sayıdaki müşterinin bekleyeceği
bir yer vardır. Servis, ilk giren ilk çıkar kuralına göre verilmektedir.
Müşterilerin sisteme gelişleri rasgele ve tek tektir. Gelişler arası sürenin
olasılık dağılımı Tablo 15.1’de gösterilmiştir.

Tablo 15.1

| Gelş. Ars. Süre (dak.) | Sıklık | Olasılık |
|------------------------|--------|----------|
| 1                      | 25     | 0.25     |
| 2                      | 20     | 0.20     |
| 3                      | 30     | 0.30     |
| 4                      | 25     | 0.25     |

Servis süreleri de rasgeledir. Hizmet Tablo 15.2’deki olasılık dağılımına göre
verilmektedir.

Tablo 15.2

| Servis Süresi (dak.) | Sıklık | Olasılık |
|----------------------|--------|----------|
| 1                    | 30     | 0.30     |
| 2                    | 40     | 0.40     |
| 3                    | 30     | 0.30     |

Gerçekleşme olasılıkları oldukça yüksek olan varsayımlar sonucu ortaya çıkan bu
kuyruk sistemi aşağıdaki şekilde açıklanmıştır.

Şekil 15.1

Modelin simüle edilmesi ile ilgili açıklamalardan önce, incelenen kuyruk
sisteminin durumunu tanımlayalım ve simülasyondaki saat zamanı ile olay
kavramları üzerinde duralım. Örneklenen sistemin durumu, 1. Sistemdeki müşteri
sayısı, 2. Servis biriminin durumu: servisin meşgul veya aylak olması, 3.
Sisteme yeni bir gelişin gerçekleşme zamanı değişkenleriyle açıklanacaktır.
Olay, sistemin durumu ile çok yakından ilgili bir kavramdır. Sistemin durumunda
değişikliğe yol açan her şey bir olaydır. Buna göre tek-servis kuyruk modelinde
sistemin durumunda değişikliğe neden olan iki mümkün olay vardır. Bunlardan
birisi sisteme bir müşterinin gelmesi, diğeri servisi tamamlanan bir müşterinin
sistemi terketmesidir. Bu olaylar zamanın belirli noktalarında ortaya çıkar.
Simülasyonda sistemin durumunda değişikliğe yol açan olayların ortaya
çıkacakları zaman programlanır. Olayların programlanan zamanları ile ilgili
bilgiler "olay listesi" adı verilen bir listede gösterilir. Programlanan zaman
"saat zamanı" adı verilen bir değişkenle açıklanır. Simülasyon modelini
çalıştırmak için sistemin başlangıç anındaki durumu tanımlanmalıdır.
Simülasyonun kuyruk sistemin boş olduğu durumla başladığını ve ilk olayın sıfır
saat zamanında gerçekleştiğini varsayalım. Buna göre kuyruk probleminin ilk
olayı sıfır saat zamanında gerçekleşen bir müşteri gelişidir. Bu müşteri servis
mekanizmasını boş bulur ve hemen servis sistemine girer. Zamanın başka
noktalarında gelen müşteriler servis sistemini ya meşgul veya aylak bulurlar. Bu
müşteriler servis aylaksa servise, servis meşgulse kuyruğa girerler. Sisteme
müşteri gelişiyle ilgili bu faaliyetler aşağıdaki akış çizelgesinde
özetlenmiştir.

Şekil 15.2

Sisteme gelişlerle ilgili açıklamalardan sonra sistemi ilk terkeden müşterinin
ayrılış zamanı çizelgelenmelidir. Çizelgeleme için servis zamanı dağılımından
rasgele bir servis süresi üretilir. Üretilen sürenin dikkate alınmasıyla ilk
müşterinin sistemden ayrılış zamanı aşağıdaki gibi hesaplanır.

Ayrılış zamanı = Şimdiki saat zamanı + Üretilen servis süresi 15.1

Sisteme yeni gelişin zamanı da ayarlanmalıdır. Bunun için gelişler arası süre
dağılımından rasgele yaklaşımla bir rasgele süre belirlenir ve yeni gelişin
zamanı aşağıdaki gibi ifade edilir.

Geliş zamanı = Şimdiki saat zamanı + Üretilen gelişler arası süre 15.2

Sözgelimi, ilk müşteriye verilecek servisin 1 dakika süreceği belirlenmişse ilk
müşterinin ayrılışı, saat zamanı ile 1’de gerçekleşir. Benzer şekilde, gelişler
arası süre 2 dakika olarak üretilmişse yeni geliş, saat zamanı ile 2’de
gerçekleşir. Bu olaylar ve bunların çizelgelenmiş zamanları olay listesine
aktarılır. Birinci gelişle ilgili tüm bilgilerin listeye aktarılmasından sonra
çizelgelenecek yeni olay ve zamanını belirlemek için olay listesi taranır. Yeni
olayın geliş olduğu belirlenirse saat bu gelişin programlanmış zamanına
ayarlanır. Yeni olay ayrılış ise saat bu ayrılışın programlanan zamanına
ayarlanır. Bu arada kuyruk uzunluğu incelenir. Kuyrukta bekleyen varsa

kuyruğun en önündeki müşteri servise alınır. Bu müşterinin ayrılış zamanı
15.1’den hesaplanır. Müşterinin gelişi ile sistemi terkedişi arasında geçen süre
hesaplanarak belirlenen süre bekleme süresi başlığı altında olay listesine
yazılır. Kuyrukta bekleyen yoksa sistemin aylak olduğu kararlaştırılır. Sistemin
aylak kalma süresi de tıpkı bekleme süresi gibi olay listesinde gösterilmelidir.
Ayrılışla ilgili faaliyetler aşağıdaki akış çizelgesinde açıklanmıştır.

Şekil 15.3

Saat zamanı sürekli güncelleştirildiğinden bu yaklaşıma "yeni-olay
zaman-ilerletme yaklaşımı" denir. Durum değişkenleri yalnızca olay zamanlarında
değişeceklerinden olaylar arasındaki faal olmayan süreler atlanarak olaydan
olaya geçilir. Bu işlem sırasında simülasyon saati, gerçekleşmesi en yakın ve
kesin olan olayın zamanına ilerletilir. Konuyla ilgili sayısal örnekler ileride
verilecektir.

15.4. MONTE CARLO SİMÜLASYONU

Sistemin durumunu değiştiren olayların gerçekleşme zamanlarına ait değerlerin
verilen bir olasılık dağılımından belirlenmesi, "olasılık dağılımından örnek
seçme", "rasgele değer üretimi" veya "Monte Carlo örneklemesi" olarak bilinir.
Bu kesimde kesikli dağılımlardan örnek seçimi ile ilgili değişik yöntemler
açıklanacaktır. İlk olarak rulet kullanımıyla rasgele değer belirleme tekniği ve
rasgele sayıların kullanılmasıyla örnek seçimi üzerinde durulacaktır.

Kesikli dağılımlardan örnek seçiminde olasılığın frekansa bağlı tanımı dikkate
alınır ve uzun dönemde sonuçların olasılık dağılımındaki olasılıkların
belirlediği sıklıklarda gerçekleşmeleri beklenir. Sözgelimi, Tablo 2.2’deki
servis süresi dağılımına göre servis süresinin zamanın %30’unda 1 dakika,
%40’ında 2 dakika, %30’unda ise 3 dakika olarak gerçekleşeceği umulur. Doğru
sıklıklara ulaşmak için örnek seçme yönteminin ürettiği her bir servis
zamanının, kendisinden önce üretilen ve kendisinden sonra üretilecek olan servis
süresinin uzunluğundan bağımsız olmalıdır. Rulet kullanımında bu iki özelliğin
sağlanması için rulet alanı 3 bölüme ayrılır. Her bölümün alanı, karşılık
geldiği servis süresinin olasılığı ile orantılıdır. Buna göre rulet alanının
%30’luk bölümü (S1) 1 dakikalık, %40’lık bölümü (S2) 2 dakikalık, %30’luk kısmı
(S3) ise 3 dakikalık servis süresine ayrılır. Böylece 1 dakikalık servis
süresiyle karşılaşma olasılığının 0.30, 2 dakikalık servis süresiyle karşılaşma
olasılığının %40, 3 dakikalık servis süresiyle karşılaşma olasılığının %30
olması sağlanır.

Şekil 15.4

Bölümlendirme işleminin tamamlanmasından sonra rulet döndürülür ve durması
beklenir. Rulet durduğunda göstergenin işaret ettiği alanın S1 olduğunu
varsayalım. S1, 1 dakikalık servis süresine karşılık geldiğinden servisin 1
dakika süreceği kararlaştırılır. Benzer şekilde, göstergenin S2’yi göstermesi
durumunda servis süresinin 2, S3’ü göstermesi durumunda 3 dakika olduğu
kararlaştırılacaktır. Rulet hilesiz ise uzun dönemde, 1.Türetilen servis
sürelerinin aşağı yukarı olasılık dağılımındaki gibi olmaları, 2. Ruletin her
bir döndürülüşünde ulaşılan sonucun bir önceki ve bir sonraki döndürmelerde
ulaşılan sonuçlardan bağımsız olması sağlanır.

Aynı teknik rulet alanının 3 yerine, her biri 00 ile 99 arasında bulunan bir
tamsayıya karşılık olmak üzere 100 eşit parçaya bölümlendirilmesiyle de
uygulanabilir. Her bir sayının gösterge tarafından gösterilme şansı eşit, yani
0.01’dir. Daireyi bölümlere ayırma yöntemiyle 00’dan 34’e kadar olan 35 sayı 1
dakikalık servis süresine ayrılır. Her sayı ortaya çıkma bakımından eşit şansa
sahip olduğundan, 35 sayı birlikte 0.35 olasılığını verir. Benzer şekilde,
35’den 74’e kadar olan 40 sayı 2 dakikalık servis süresine, 75’den 99’a kadar
olan sayılar 3 dakikalık servis süresine ayrıldığında gerekli olasılıklar
sağlanmış olur. Servis sürelerinin üretilmesi için önceden olduğu gibi rulet
döndürülür ve durması beklenir. Rulet durduğunda gösterge 00 ile 34 arasında bir
sayı gösteriyorsa servis süresinin 1, gösterge 35 ile 74 arasında bir sayı
gösteriyorsa 2, 75 ile 99 arasında bir sayı gösteriyorsa 3 dakika olduğu
kararlaştırılır. Ruletin 100 eşit parçaya bölümlendirilerek göstergenin işaret
ettiği sayıyı belirleme yöntemi, değeri 00 ile 99 arasında bulunan rasgele sayı
üretimine eşdeğerdir. Ruletin, rasgele sayı üreteci olarak kullanılmasıyla iki
rakamlı rasgele sayı belirleme işlemi çok basit olmakla birlikte sayıların
üretilme hızı son derece düşüktür. Bunun yerine bu amaçla hazırlanmış rasgele
sayı tabloları kullanılabilir.

İki rakamlı rasgele sayılar tablosunun küçük bir bölümü Tablo 15.3’de
verilmiştir. Rasgele sayılar tablolarının kullanımı kolay ve pek çok durumda
uygundur.

Tablo 15.3

22 17 68 65 84 68 95 23 92 35 61 09 43 95 06 87 02 22 57 51 58 24 82 03 47

19 36 27 59 46 13 79 93 37 55 85 52 05 30 62 39 77 32 77 09 47 83 51 62 74

16 77 23 02 77 09 61 87 25 21 16 71 13 59 78 28 06 24 25 93 23 05 47 47 25

78 43 76 71 61 20 44 90 32 64 46 38 03 93 22 97 67 63 99 61 69 81 21 99 21

03 28 28 26 08 73 37 32 04 05 88 69 58 28 99 69 30 16 09 05 35 07 44 75 47

93 22 53 64 39 07 10 63 76 35 08 13 13 85 51 87 03 04 79 88 55 34 57 72 69

78 76 58 54 74 92 38 70 96 92 82 63 18 27 44 52 06 79 79 45 69 66 92 19 09

23 68 35 26 00 99 53 93 61 28 56 65 05 61 86 52 70 05 48 34 90 92 10 70 80

15 39 25 70 99 93 86 52 77 65 22 87 26 07 47 15 33 59 05 28 86 96 98 29 06

58 71 96 30 24 18 46 23 34 27 49 18 09 79 49 85 13 99 24 44 74 16 32 23 02

57 35 27 33 72 24 53 63 94 09 44 04 95 49 66 41 10 76 47 91 39 60 04 59 81

48 50 86 54 48 22 06 34 72 52 33 29 94 71 11 82 21 15 65 20 15 91 29 12 02

61 96 48 95 03 07 16 39 33 66 77 21 30 27 12 98 56 10 56 79 90 49 22 23 62

36 93 89 41 26 29 70 83 63 51 87 09 41 15 09 99 74 20 52 36 98 60 16 03 03

18 87 00 42 31 57 90 12 02 07 54 08 01 88 63 23 47 37 17 31 39 41 88 92 10

88 56 53 27 59 33 34 72 67 47 08 18 27 38 90 77 34 55 45 70 16 95 86 70 75

09 72 95 84 29 49 41 31 06 70 64 84 73 31 65 42 38 06 45 18 52 53 37 97 15

12 96 88 17 31 65 19 69 02 83 24 64 19 35 51 60 75 86 90 68 56 61 87 39 12

85 94 57 24 16 92 09 84 38 76 29 81 94 78 70 22 00 27 69 85 21 94 47 90 12

38 64 43 59 98 98 77 87 68 07 40 98 05 93 78 91 51 67 62 44 23 32 65 41 18

53 44 09 42 72 00 41 86 79 79 35 55 31 51 51 68 47 22 00 20 00 83 63 22 55

40 76 66 26 84 57 99 99 90 37 37 40 13 68 97 36 63 32 08 58 87 64 81 07 83

02 17 79 18 05 12 59 52 57 02 28 14 11 30 79 22 07 90 47 03 20 69 22 40 98

95 17 82 06 53 31 51 10 96 46 56 11 50 81 69 92 06 88 07 77 40 23 72 51 39

35 76 22 42 92 96 11 83 44 80 33 42 40 90 60 34 68 35 48 77 73 96 53 97 86

26 29 13 56 41 85 47 04 66 08 82 43 80 46 15 34 72 57 59 13 38 26 61 70 04

77 80 20 75 82 72 82 32 99 90 89 73 44 99 05 63 95 73 76 63 48 67 26 43 18

46 40 66 44 52 91 36 74 43 53 78 45 63 98 35 30 82 13 54 00 55 03 36 67 68

37 56 08 18 09 77 53 84 46 47 24 16 74 11 53 31 91 18 95 58 44 10 13 85 57

61 65 61 68 66 37 27 47 39 19 53 21 40 06 71 84 83 70 07 48 95 06 79 88 54

93 43 69 64 07 34 18 04 52 35 61 85 53 83 45 56 27 09 24 86 19 90 70 99 00

21 96 60 12 99 11 20 99 45 18 18 37 79 49 90 48 13 93 55 34 65 97 38 20 46

95 20 47 97 97 27 37 83 28 71 45 89 09 39 84 00 06 41 41 74 51 67 11 52 49

97 86 21 78 73 10 65 81 92 59 04 76 62 16 17 58 76 17 14 97 17 95 70 45 80

69 92 06 34 13 59 71 74 17 32 23 71 82 13 74 27 55 10 24 19 63 52 52 01 41

Bir rasgele sayı (Ri), olasılık yoğunluk fonksiyonu aşağıda gösterilen sürekli
tekdüze dağılımdan rasgele seçimle belirlenen bağımsız bir örnek şeklinde
tanımlanabilir.

f(x) =

Buna göre, her bir rasgele sayı sıfır-1 aralığında tekdüze dağılır. Bu nedenle
bu rasgele sayılara tekdüze rasgele sayılar veya U(0, 1) rasgele sayıları denir.

Rasgele sayı üretiminde kullanılabilecek pek çok yaklaşım vardır. Bu
yaklaşımlardan bazılarında belirli algoritmalar kullanılır. Algoritma kullanımı
sayıların gerçek anlamda rasgele oluşlarını engellediğinden bu yolla üretilen
rasgele sayılara "sözde rasgele sayılar" denir. Sözde rasgele sayı üretiminde
kullanılan belli başlı teknikler aşağıda açıklanmıştır.

Ortakare Tekniği: Tekdüze dağılıma uygun sözde rasgele sayı üretmede kullanılan
ilk aritmetik yöntemlerden biridir. Sayı üretecini çalıştırmak için rasgele
seçimle dört basamaklı bir sayı (R0) belirlenir. Rasgele sayı üretiminde
kullanılacak dört basamaklı bu sayıya başlangıç değeri veya "tohum" denir. İlk
rasgele sayının belirlenmesi için tohumun karesi alınır. Tohumun karesinin, tam
ortada dört basamaklı bir sayı bulundurması için, sekiz basamaklı olması
istenir. Sayı sekiz basamaklı değilse sayının soluna sayının sekiz rakamlı
olmasını sağlayacak kadar sıfır eklenir. Bu yolla belirlenen sayının tam
ortasında bulunan dört basamaklı sayı üretilen ilk rasgele sayı olur. Bu sayı,
ikinci rasgele sayının üretilmesinde kullanılacak olan tohumdur. Aynı işlemler
bu yeni tohumla tekrarlanır ve ikinci rasgele sayı yani, üçüncü rasgele sayının
üretilmesinde kullanılacak tohum belirlenmiş olur. İstenildiği kadar rasgele
sayı elde edilinceye kadar bu adımlar tekrarlanır.

Ortakare tekniği günümüzde kullanılmayan bir sayı üretme tekniğidir. Bunun
nedeni, yöntemi analiz etmenin güçlüğü ve ayrıca ilk rasgele sayı ile rasgele
sayılar dizisinin tekrar uzunluğu arasındaki ilişkiyi kestirmenin zor oluşudur.
Çoğu kez tekrar uzunluğu oldukça kısadır, yani sayılar çok kısa zamanda bozulma
eğilimi gösterir. Sözgelimi ilk sayı, R0 = 6500 olarak seçildiğinde diğer bütün
rasgele sayılar aşağıda gösterildiği gibi 2500 olur.

R0 = 6500 (R0)2 = 42250000

R1 = 2500 (R1)2 = 06250000

R2 = 2500 (R2)2 = 06250000

R3 = 2500 (R3)2 = 06250000

R4 = 2500 vd.

Ortaçarpım Tekniği: Tekdüze dağılıma uygun rasgele sayı üretmede kullanılan bir
başka yöntemdir. Ortakare tekniğinde olduğu gibi sayı üretecini çalıştırmak için
rasgele seçimle dört basamaklı bir sayı belirlenir. Seçilen bu sayı K gibi bir
sabitle çarpılır. Çarpım sonucu belirlenen sayının ortasında bulunan basamaklar
ortaçarpım tekniğiyle belirlenen ilk rasgele sayı olur. İkinci rasgele sayının
belirlenmesi için bir önceki adımda üretilen rasgele sayı yine K ile çarpılarak
ilk rasgele sayının belirlenmesindeki işlemler tekrarlanır. Ortaçarpım tekniği
aşağıdaki eşitlikle ifade edilir.

Rn+1 = K(Rn)

Burada Rn, n’inci rasgele değeri ifade etmektedir. Bu adımlar ne kadar rasgele
sayı isteniyorsa o kadar tekrarlanır. Ortaçarpım tekniği aşağıdaki özelliklere
sahiptir.

1\. Ortakare tekniğinden daha uzun döneme sahiptir.

2\. Ortakare tekniğinden daha tekdüze dağılımlıdır.

3\. Bozulma eğilimi gösterir.

Fibonacci Yöntemi: Fibonacci serisine dayanan bu yöntem aşağıdaki bağıntıyla
açıklanır.

xn+1 = (xn + xn -1) mod m

Burada xn+1, kendisinden önce gelen iki rasgele sayının (xn ve xn-1) toplamının
m ile bölünmesinden artan sayıdır.

Bu yöntem genellikle tekrar uzunluğu m’den büyük olan diziler sağlar. Zayıf yanı
üretilen rasgele sayılar dizisinin rasgelelik testinden geçmemesidir. Bu nedenle
bu yöntem de tatminkar sayılar sağlamaktan uzaktır.

Tekdüze rasgele sayı üretmede kullanılan yöntemlerin bir kısmı eşlik yöntemleri
başlığı altında incelenir. Bu başlık altındaki yöntemlerin her biri bir eşlik
ilişkisine (toplamsal, çarpımsal ve karma) dayanmaktadır. Karma eşlik yöntemi
toplamsal ve çarpımsal eşlik yöntemlerinin özelliklerini bünyesinde taşıdığından
ilk önce bu yöntemin incelenmesi uygun olur. Thomson’un önerdiği karma eşlik
yöntemi aşağıdaki bağıntı ile özetlenir.

xi+1 = (axi + c) mod m (i = 0, 1, 2, ...)

Bu yazılışta, a ve c pozitif sayılardır. x0 üreteci çalıştırmak için rasgele
seçimle belirlenen tohum, m moddur. a, c ve m (a m, c m) sayı üretecinin
parametreleridir. Bu ilişkinin kullanılmasıyla xi+1’in değeri (axi + c)’nin m
ile bölünmesi sonucu beliren artana eşit olur. Böylece değerleri 0, 1, ..., (m -
1) olan rasgele tamsayılar dizisi belirlenmiş olur. Bu tamsayılar istenirse
aşağıdaki bağıntının kullanılmasıyla U(0, 1) sayılarına dönüştürülebilir.

Ri = (i = 0, 1, 2, ...)

Örnek 15.1: x0 = 12, a = 6, c = 3 ve m = 10 olarak verilmiştir. Karma eşlik
yöntemini kullanarak ilk 10 rasgele sayı dizisini belirleyiniz.

Çözüm 15.1: Rasgele sayıların hesaplanması işlemleri aşağıda gösterilmiştir.

x1 = (ax0 + c) mod m x2 = (ax1 + c) mod m

= 6(12) + 3 mod10 = 6(5) + 3 mod 10

= 5 = 3

x3 = (ax2 + c) mod m x4 = (ax3 + c) mod m

= 6(3) + 3 mod 10 = 6(1) + 3 mod 10

= 1 = 9

x5 = (ax4 + 3) mod m x6 = (ax5 + 3) mod m

= 6(9) + 3 mod 10 = 6(7) + 3 mod 10

= 7 = 5

x6 = x1 olarak hesaplandığından daha fazla sayı üretmenin yararı yoktur. Çünkü
bundan sonra üretilecek sayılar sırasıyla; x7 = x2, x8 = x3, .. olacak, yani
aynı sayılar tekrar tekrar üretilecektir. Bu, arzu edilmeyen bir durumdur.
Kuşkusuz arzu edilen, yeterince uzun ve her biri bir diğerinden farklı rasgele
sayılar dizisini oluşturabilmektir. Bu özellik a, c ve m değerlerinin seçiminde
bazı kurallara uyulması ile sağlanabilir. Kurallara uyulduğunda yalnızca tekrar
döneminin uzun olması değil aynı zamanda sözde rasgele sayıların gerçek rasgele
sayılar olması sağlanabilir.

İkili bilgisayarlarda b bit sayısı olmak üzere m = 2b alınır. 32 bitlik
makinelerde m = 232 olur. Bu durumda üretilen rasgele sayılar 0 ile 232 - 1
arasında değişir. Sayıların tekrarını önlemek için a’nın 1, 5, 9, 13, 17, 21,
..., c’nin 1, 3, 5, 7, 9, 11, 13, ... kümesinden seçilmesi uygun olur. Ondalık
bilgisayarlarda m = 10d olur. Bu tip makinelerle çalışırken a’nın 1, 21, 41, 61,
71, ..., c’nin sonu 5’le biten tek sayılar dışındaki sayıların oluşturduğu 1, 3,
7, 9, 11, 13, 17, 21, ... kümesinden seçilmesiyle sayıların tekrar etme sorunu
ortadan kaldırılır. Rasgele sayıların 000, 001, 002, ..., 999 gibi az rakamlı
olması istendiğinde m = 2b veya m = 10d seçilir. Bu yolla dizide tekrarın
başlamasından önce çok sayıda sayı üretilmesi sağlanır. Üretilen sayıların ilk
üç veya son üç basamağı dışında kalanların düşürülmesiyle 000-999 aralığında
rasgele sayılar belirlenmiş olur.

Karma eşlik üretecinde c = 0 olduğunda, üreteç "xi+1 = (axi) mod m" olur. Bu
sayı üretecine "çarpım eşlik üreteci" denir. (axi + c) yazılışında a = 1, c =
xi-1 olarak alındığında karma eşlik toplamsal eşlik yöntemine dönüşür.

En yaygın biçimde kullanılan rasgele sayı üreticilerinden biri de
Lerrmouth-Lewis üretecidir. Çarpım eşlik ilişkisine dayanan üreteç şöyledir:

xn+1 = 75 xn(mod 231 - 1)

Bir rasgele sayı üreticisinin iyi olabilmesi için aşağıdaki özellikleri
sağlaması gerekir.

1\. Üretilen sayılar (0, 1) aralığında olabildiğince tekdüze dağılmalıdır.

2\. Üretilen sayılar birbirlerinden bağımsız olmalı, yani üretilen sayının değeri
kendisinden önce ve sonra üretilen sayılardan etkilenmemelidir.

3\. Üretilen sayılar istenildiğinde tekrar üretilebilir olmalıdır.

4\. Üretilen bir rasgele sayı uzun bir dönem bir daha ortaya çıkmamalıdır.
Üretilen rasgele sayılar dizisinde aynı rasgele sayıya iki kez rastlanmamalı
kısaca sayılar birbirinden farklı olmalıdır.

5\. Sayılar hızlı üretilmeli ve sayı üretmede kullanılan program bilgisayar
belleğinde fazla yer kaplamamalıdır.

6\. Üreteç sıfır üretmemelidir.

Monte Carlo örneklemesinde bilgisayarda üretilmiş rasgele sayıların kullanımını
açıklayalım. Bu yöntemin ana fikri U(0, 1) rasgele sayılarını 00 ile 99 arasında
bulunan tamsayılara dönüştürmek ve daire bölümlendirme işlemini bu sayılarla
gerçekleştirmektir. U(0, 1) sayılarının tamsayılara dönüştürülmesi işlemi
oldukça basit ve kolaydır. Sıfır ile 1 arasındaki rasgele sayılar (0, 1)
aralığında tekdüze dağıldıklarından bu sayıların 100 ile çarpımları sonucunda
belirlenen sayılar da sıfır ile 100 arasında tekdüze dağılırlar. U(0, 1)
sayıları ondalık sayılar olduklarından bu sayıların 100 ile çarpımları da
ondalık sayılar olurlar. Çarpma işlemiyle belirlenen sayıların ondalık kısımları
atıldığında kalan kısım 00 ile 99 aralığında bir tamsayı olur. Sözgelimi
üretilen sayı 0.64865 ise 0.64865 x 100 = 64.865 olur. Bu sayının ondalık kısmı
atıldığında belirlenen tamsayı 64 olur. Dönüştürme işlemi bilgisayarlarda da bu
şekilde gerçekleştirilir. Yani, önce U(0, 1) sayısı belirlenir sonra sayı 100
ile çarpılır ve elde edilen sayının ondalık kısmı atılarak kalan tamsayı kısmı
rasgele tamsayı olarak kullanılır. Bu yöntemle değeri 00 ile 99 arasında değişen
rasgele tamsayılar üretilir.

Monte Carlo örneklemesi ile kesikli rasgele değişken için rasgele değer üretimi,
1\. Rasgele değişken için birikimli olasılık dağılımının oluşturulması, 2.
Rasgele sayıların değişkenin değişik değerlerine paylaştırılmasında birikimli
olasılık dağılımının kullanılması olmak üzere iki adımdan oluşur.

Yöntemi üçüncü kesimdeki gelişler arası süre olasılık dağılımına uygulayalım.
Tablo 15.1’deki olasılıklarla oluşturulan birikimli olasılık dağılımı Tablo
15.4’ün üçüncü sütununda gösterilmiştir. İlk gelişler arası süre olan 1
dakikanın gerçekleşme olasılığı 0.25’dir. Bu yüzden bu sonuca 25 sayı tahsis
edilmesi gerekir. 00’dan 24’e kadar olan 25 sayı bu amacı gerçekleştirir. Bu
yolla sıfırdan 0.24999’a kadar olan ondalık sayılar kullanılmış olur. Bu
aralığın üst ucu 0.25’lik birikimli olasılığın tam altındadır. 2 dakikalık süre
için 20 rasgele sayı ayrılması gerekir. Bunun için 25’den 44’e kadar olan tam
sayıların kullanılmasıyla tanımlanan aralığın 0.25’den 0.44999’a kadar olan
ondalık sayıları kapsaması sağlanmış olur. Önceden olduğu gibi bu aralığın üst
ucu tam 0.45 birikimli olasılığının altında yer alırken alt ucu bir önceki
birikimli olasılığın üst ucuyla çakışır. 0.45’den 0.749999’a kadar olan ondalık
sayılardan türetilen 30 rasgele sayı 3 dakikalık, 0.75’den 0.99’a kadar olan
ondalık sayılardan türetilen 25 rasgele sayı 4 dakikalık gelişler arası süre
için ayrılır. Bir başka deyişle birikimli olasılık dağılımı rasgele tamsayı
aralıklarının paylaşımını sağlar.

Aralıkların belirlenmesinden sonra rasgele değişken için değer belirleme
konusunda yapılması gereken tek şey bir rasgele bir sayı seçmek, seçilen sayının
rasgele sayı aralıklarından hangisine düştüğünü belirlemekten ibarettir.
Sözgelimi seçilen rasgele sayı 37 olduğunda gelişler arası sürenin 2 dakika, 90
olduğunda 4 dakika olduğu kararlaştırılır.

Tablo 15.4

| Gelişler Arası Süre (dak.) |  Olasılık | Birikimli Olasılık | Ras. Sayı Aralığı |
|----------------------------|-----------|--------------------|-------------------|
| 1                          | 0.25      | 0.25               | 00 - 24           |
| 2                          | 0.20      | 0.45               | 25 - 44           |
| 3                          | 0.30      | 0.75               | 45 - 74           |
| 4                          | 0.25      | 1.00               | 75 - 99           |

15.5. MONTE CARLO SİMÜLASYONU ÖRNEĞİ

Bu bölümde işletmelerde ortaya çıkabilecek değişik problemlerin Monte Carlo
simülasyonu ile çözülmeleri üzerinde durulacaktır. Monte Carlo simülasyonu
statik simülasyon modelidir. Sistemin belirli bir zaman aralığında belirli bir
anındaki durumunu yansıtmak amacıyla kullanılır.

Örnek 15.2: Çok sayıda makinenin bulunduğu bir fabrikada rasgele zamanlarda ve
birbirlerinden bağımsız olarak arızalanan makineler tek bir usta tarafından
onarılmaktadır. Geçmiş dönemin incelenmesi sonucunda arızaların oluşumu ve
giderilmeleri ile ilgili sürelere ait olasılık dağılımları Tablo 15.5’de
verilmiştir. Kuyruk sistemini 2 saatlik bir süre için simüle ederek ortalama
kuyruk uzunluğunu ve kuyrukta bekleme zamanını hesaplayınız.

Tablo 15.5

| Gelişler Arası Süre (Dak.) |  Sıklık |  Olasılık | Servis Süresi (Dak.) |  Sıklık |  Olasılık |
|----------------------------|---------|-----------|----------------------|---------|-----------|
| 1                          | 22      | 0.110     | 2                    | 20      | 0.10      |
| 2                          | 16      | 0.080     | 4                    | 30      | 0.15      |
| 3                          | 30      | 0.150     | 5                    | 50      | 0.25      |
| 4                          | 50      | 0.250     | 6                    | 70      | 0.35      |
| 5                          | 25      | 0.125     | 8                    | 30      | 0.15      |
| 6                          | 28      | 0.140     | Toplam               | 200     | 1.00      |
| 7                          | 19      | 0.095     |                      |         |           |
| 8                          | 10      | 0.050     |                      |         |           |
| Toplam                     | 200     | 1.000     |                      |         |           |

Çözüm 15.2: Kuyruk sisteminin simülasyonu için öncelikle birbirini izleyen iki
geliş arasında geçen her farklı süre için bir rasgele sayı aralığının
belirlenmesi gerekir.

Gelişler arası süreye ilişkin rasgele değerler bu olayla ilgili birikimli
dağılım fonksiyonunun kullanılmasıyla üretilebilir. Her sayının ortaya çıkma
bakımından eşit şansa sahip ve bağımsız olmalarını sağlamak için sıfır ile 1
arasında düzgün dağılımlı rasgele sayılar kullanılır. Gelişler arası sürenin
birikimli olasılıkları ve rasgele sayı aralıkları aşağıda gösterilmiştir.
Olasılıklar virgülden sonra üç basamaklı olduklarından 3 rakamlı rasgele sayılar
kullanılmıştır.

Tablo 15.6’nın üçüncü sütununda gösterildiği gibi 1 dakikalık süre için tahsis
edilen sayı aralığı 000-109’dur. Böylece 110 rasgele sayı bu süre için ayrılmış
olur. Rasgele gelişler arası sürenin belirlenmesi amacıyla çekilen rasgele sayı
bu aralıkta ise en son gelişin gerçekleştiği andan 1 dakika sonra sisteme yeni
bir müşterinin geleceği kabul edilir.

Benzer yaklaşımla servis süresi dağılımına ilişkin rasgele sayı kodlaması Tablo
15.6’nın son sütununda gösterilmiştir. Servis süresine ilişkin olasılıklar
virgülden sonra iki basamaklı olduklarından iki rakamlı rasgele sayılar
kullanılmıştır. Servis süresinin 2 dakika olması olasılığı 0.10’dur. Bu nedenle,
00-09 rasgele sayı aralığı servis süresinin 2 dakika olması durumu için
ayrılmıştır. Rasgele servis süresinin belirlenmesi için çekilen rasgele sayı bu
aralıkta ise servis süresinin 2 dakika olduğu kararlaştırılır.

Rasgele sayı kodlamasının tamamlanmasından sonra kuyruk sisteminin simülasyonuna
geçilir.

Tablo 15.6

| Gelişler Arası Süre | Birikimli Olasılık | Ras. Sayı Aralığı | Servis Süresi | Birikimli Olasılık | Ras. Sayı Aralığı |
|---------------------|--------------------|-------------------|---------------|--------------------|-------------------|
| 1                   | 0.110              | 000 - 109         | 2             | 0.10               | 00 - 09           |
| 2                   | 0.190              | 110 - 189         | 4             | 0.25               | 10 - 24           |
| 3                   | 0.340              | 190 - 339         | 5             | 0.50               | 25 - 49           |
| 4                   | 0.590              | 340 - 589         | 6             | 0.85               | 50 - 84           |
| 5                   | 0.715              | 590 - 714         | 8             | 1.00               | 85 - 99           |
| 6                   | 0.855              | 715 - 854         |               |                    |                   |
| 7                   | 0.950              | 855 - 949         |               |                    |                   |
| 8                   | 1.000              | 950 - 999         |               |                    |                   |

Önce gelişler arası sürenin belirlenmesinde kullanılacak sayıları seçelim.
Gelişler arası süre için Tablo 15.3’ün sol üst köşesinden başlanmış düşey
doğrultudaki sayılar okunmuştur. Bu yolla belirlenen rasgele sayılar Tablo
15.7’nin beşinci sütununda gösterilmiştir. Servis süresinin belirlenmesi için
kullanılan 3 rakamlı rasgele sayıların bir bölümü aşağıda gösterilmiştir.

100 375 084 990 128 660 310 852 635 737

985 118 834 886 995 654 801 743 699 098

914 803 441 125 636 611 154 945 424 235

044 005 359 598 460 321 692 195 451 948

980 331 809 797 186 740 541 116 483 690

765 648 196 093 801 340 455 020 053 035

672 121 099 195 981 783 389 421 125 623

Saati işyerinin işe başlama zamanı olan 8.00’e ayarlayalım. 1 nolu olayın
gerçekleşme zamanı için okunan rasgele sayı 100’dür. Bu sayı 000-109 aralığında
bulunduğundan ilk müşterinin saat 8.01’de ulaşacağı kabul edilir. Bu müşteriye
verilecek hizmetin kaç dakika süreceğinin belirlenmesi için çekilen rasgele sayı
22’dir. Bu sayı 10 - 24 aralığına düştüğünden ilk müşteriye verilecek servisin 4
dakika süreceği kabul edilir. Buna göre saat 8.01’de sisteme giren ilk müşteri
saat 8.05’de sistemden ayrılacaktır. İkinci müşterinin geliş zamanının
belirlenmesi için seçilen rasgele sayı 375, 340 - 589 aralığındadır. Buna göre
ikinci müşteri ilk müşteriden 4 dakika sonra yani, 8.05’de sisteme ulaşacaktır.
İlk müşteri 8.05’de sistemden ayrıldığından ikinci müşteri hemen servise
girecektir. İkinci müşteri için servis süresi 4 dakikadır. Buna göre ikinci
müşterinin saat 8.09’da sistemden ayrılacağı kararlaştırılır. Üçüncü müşterinin
geliş zamanı ikinci müşteriden 1 dakika sonra yani, saat 8.06’da gerçekleşir. Bu
müşteri sisteme geldiğinde ikinci müşteriye hizmet veriliyor olduğundan
halihazırda boş olan kuyruğa girerek kendisinin oluşturduğu tek kişilik kuyrukta
servis sırasının kendisine gelmesini bekler. Üçüncü müşterinin hizmeti 8.13’de
tamamlanır. Dördüncü müşteri saat 8.14’de sisteme geldiğinden servis sistemi
8.13 - 8.14 arasında 1 dakika aylak kalır. Dördüncü müşteri servisi boş
bulduğundan hiç beklemeden servise girer. Bu yaklaşımla 2 saatlik zaman
dönemindeki olaylarla ilgili bilgiler aşağıdaki tabloda gösterilmiştir.

Tablo 15.7

| Sıra No (1) | Rasg. Sayı (2) | Geliş Süresi (3) | Geliş Saati (4) | Rasg. Sayı (5) | Servis Süresi (6) | Bekleme Süresi (7) |  Başl. (8) |  Bitm. (9) | Kuyruk Uzunl. (10) |
|-------------|----------------|------------------|-----------------|----------------|-------------------|--------------------|------------|------------|--------------------|
| 1           | 100            | 1                | 8.01            | 22             | 4                 | 00                 | 8.01       | 8.05       | 0                  |
| 2           | 375            | 4                | 8.05            | 19             | 4                 | 00                 | 8.05       | 8.09       | 1                  |
| 3           | 084            | 1                | 8.06            | 16             | 4                 | 03                 | 8.09       | 8.13       | 0                  |
| 4           | 990            | 8                | 8.14            | 78             | 6                 | 00                 | 8.14       | 8.20       | 1                  |
| 5           | 128            | 2                | 8.16            | 03             | 2                 | 04                 | 8.20       | 8.22       | 1                  |
| 6           | 660            | 5                | 8.21            | 93             | 8                 | 01                 | 8.22       | 8.30       | 1                  |
| 7           | 310            | 3                | 8.24            | 78             | 6                 | 06                 | 8.30       | 8.36       | 2                  |
| 8           | 852            | 6                | 8.30            | 23             | 4                 | 06                 | 8.36       | 8.40       | 1                  |
| 9           | 635            | 5                | 8.35            | 15             | 4                 | 05                 | 8.40       | 8.44       | 1                  |
| 10          | 737            | 6                | 8.41            | 58             | 6                 | 03                 | 8.44       | 8.50       | 1                  |
| 11          | 985            | 8                | 8.49            | 57             | 6                 | 01                 | 8.50       | 8.56       | 1                  |
| 12          | 118            | 2                | 8.51            | 48             | 5                 | 05                 | 8.56       | 9.01       | 1                  |
| 13          | 834            | 6                | 8.57            | 61             | 6                 | 04                 | 9.01       | 9.07       | 1                  |
| 14          | 886            | 7                | 9.04            | 36             | 5                 | 03                 | 9.07       | 9.12       | 0                  |
| 15          | 995            | 8                | 9.12            | 18             | 4                 | 00                 | 9.12       | 9.16       | 0                  |
| 16          | 654            | 5                | 9.17            | 88             | 8                 | 00                 | 9.17       | 9.25       | 1                  |
| 17          | 801            | 6                | 9.23            | 09             | 2                 | 02                 | 9.25       | 9.27       | 0                  |
| 18          | 743            | 6                | 9.29            | 12             | 4                 | 00                 | 9.29       | 9.33       | 0                  |
| 19          | 699            | 5                | 9.34            | 85             | 8                 | 00                 | 9.34       | 9.42       | 1                  |
| 20          | 098            | 1                | 9.35            | 38             | 5                 | 07                 | 9.42       | 9.47       | 1                  |
| 21          | 914            | 7                | 9.42            | 53             | 6                 | 05                 | 9.47       | 9.53       | 2                  |
| 22          | 803            | 6                | 9.48            | 40             | 5                 | 05                 | 9.53       | 9.58       | 2                  |
| 23          | 441            | 4                | 9.52            | 02             | 2                 | 06                 | 9.58       | 10.00      | 2                  |
| 24          | 125            | 2                | 9.54            | 95             | 8                 | 06                 | 10.00      | ...        | ...                |
|  TOPLAM     | 72             | -                | -               | 21             |                   |                    |            |            |                    |

Müşterinin kuyrukta bekleme süresi tablonun yedinci, kuyruk uzunluğu onuncu
sütununda gösterilmiştir. Ortalama bekleme zamanı ile ortalama kuyruk uzunluğu
sırasıyla 3 dakika (= 72/24) ve 0.875 müşteri (= 21/24) olarak hesaplanmıştır.
Bilindiği gibi, olasılıksal sistemlerde simülasyon modelinin bir kaç kez
çalıştırılması gerekir. Kaç kez çalıştırmanın uygun olduğunun belirlenmesi,
örnekleme kuramının örnek büyüklüğünün belirlenmesi konusuyla ilgilidir.

Simülasyon modelinin deneme sonuçlarının karşılaştırılmasıyla servis sisteminin
en iyilenmesi sağlanabilir. Dokuzuncu bölümde açıklandığı gibi, stok
problemlerinin çözümünde hem istem hem de tedarik süresi değişken olduklarında
analitik yaklaşım yerini simülasyona bırakır.

Stok sisteminin simülasyonu aşağıdaki örnek problemle açıklanacaktır.

Örnek 15.3: Üreticiden aldığı zeytinleri 1’er kg’lık paketler haline getirip
satan bir market sahibi en iyi stok politikasını belirlemek istemektedir. Günlük
istem ve tedarik süresi kesin olarak bilinmemekle birlikte istem ve tedarik
süresinin olasılık dağılımları aşağıdaki gibi tahmin edilmiştir.

Günlük istem olasılık dağılımı:

Günlük İstem (kg): 6 7 8 9 10 11 12

Olasılık : 0.05 0.10 0.20 0.30 0.20 0.10 0.05

Tedarik süresi olasılık dağılımı:

Tedarik Süresi (gün): 2 3 4 5

Olasılık : 0.20 0.30 0.35 0.15

Sipariş maliyeti 180 TL, bulundurma maliyeti gün bazında 2 TL/kg’dır.
Bulundurmama maliyeti kaçırılan kâr olarak 20 TL/kg’dır. Market sahibi hem
sipariş miktarı hem de siparişin verileceği stok düzeyinin belirli değerleri
için toplam stok maliyetlerini karşılaştırarak en uygun kararı almak
istemektedir.

Market sahibine yol göstermek için sipariş miktarının 50, sipariş yenileme
düzeyinin 25, başlangıçtaki stok miktarının 30 olduğu duruma ilişkin 40 günlük
simülasyonu gerçekleştiriniz.

Çözüm 15.3: Simülasyon uygulamasının ilk adımı rasgele değişken(ler)
değerlerinin simülasyonunda kullanılacak rasgele sayı aralıklarının belirlenmesi
yani, rasgele sayıların kodlanmasıdır.

Problemin biri günlük istem diğeri tedarik süresi olmak üzere iki rasgele
değişkeni vardır. Önce istem değişkenini ele alalım.

Günlük istemle ilgili olasılıklar virgülden sonra iki rakamlı olduklarından
kodlamada iki rakamlı rasgele sayılar kullanılacaktır. İstem dağılımına ilişkin
rasgele sayı kodlaması aşağıdaki tablonun üçüncü sütununda gösterilmiştir.

Tedarik süresi de değişken olduğundan bu değişkene ait rasgele sayı kodlamasının
yapılması gerekir. Tedarik süresine ait rasgele sayı kodlaması Tablo 15.8’in son
sütununda gösterilmiştir.

Tablo 15.8

| Günlük İstem | Birikimli Olasılık | Ras. Sayı Aralığı | Tedarik Süresi | Birikimli Olasılık  | Ras. Sayı Aralığı |
|--------------|--------------------|-------------------|----------------|---------------------|-------------------|
| 6            | 0.05               | 00 - 04           | 2              | 0.20                | 00 - 19           |
| 7            | 0.15               | 05 - 14           | 3              | 0.50                | 20 - 49           |
| 8            | 0.35               | 15 - 34           | 4              | 0.85                | 50 - 84           |
| 9            | 0.65               | 35 - 64           | 5              | 1.00                | 85 - 99           |
| 10           | 0.85               | 65 - 84           |                |                     |                   |
| 11           | 0.95               | 85 - 94           |                |                     |                   |
| 12           | 1.00               | 95 - 99           |                |                     |                   |

2\. Adım: Rasgele sayı aralıkları belirlendikten sonra rasgele sayılar
tablosundan sayı seçiminde kullanılacak kural saptanır. Rasgele sayılar
tablosunun herhangi bir satır veya sütunu rasgele seçilerek düşey veya yatay ya
da köşegen doğrultusundaki sayılar belirli bir düzen içinde (ardarda veya birer,
ikişer, ... atlayarak) okunur. Günlük istemin simülasyonu için sayıların,
rasgele sayılar tablosunun altıncı sütun, dördüncü satırından başlayarak düşey
doğrultuda ikişer atlayarak okunduğunu varsayalım. Bu kurala göre sayılar, 20,
92, 18, 07, 33, 92, 57, 96, 91, 34, ... olarak belirlenir. Bu yolla simüle
edilecek rasgele değişkenin mümkün değerleri kadar rasgele sayı seçilir. Seçilen
ilk rasgele sayı 20 olup 15 - 34 aralığındadır. Bu aralık günlük istemin 8
olduğu duruma karşılık geldiğinden ilk günün istemi 8 kg olarak simüle edilmiş
olur. İkinci rasgele sayı 92, 85 - 94 aralığındadır. Bu durumda ikinci günün
istemi 11 kg kabul edilir. İlk 15 günlük dönem itibariyle istem aşağıdaki gibi
simüle edilir.

Gün : 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15

Rsg. S.: 20 92 18 07 33 92 57 96 91 34 10 87 79 59 49

Istem : 8 11 8 7 8 11 9 12 11 8 8 11 10 9 9

Tedarik süresinin simülasyonunda kullanılacak rasgele sayıların, rasgele sayılar
tablosunun (Tablo 15.3) sol-üst köşesinden başlayarak düşey doğrultuda ardarda
okunduğunu varsayalım. Bu kurala göre sayılar, 22, 19, 16, 78, 03, ... olarak
belirlenir. Bu yolla simüle edilecek rasgele değişkenin mümkün değerleri kadar
rasgele sayı seçilir. Seçilen ilk rasgele sayı 22 olduğundan ilk sipariş için
tedarik süresi 3 gün, ikinci rasgele sayı 17 olduğundan ikinci siparişin tedarik
süresi 2 gün, ... olur. 40 günlük simülasyon sonuçları Tablo 15.9’da
gösterilmiştir. Tablonun "denge" başlıklı sütununda gösterildiği gibi
başlangıçtaki stok miktarı 30 kg’dır. İlk günün istemi 8 kg olarak
belirlendiğinden bu günün sonunda kalan stok miktarı 22 kg olur. Bu miktar stoğu
bir gün boyunca stoklama maliyeti, tablonun "Bulundurma Maliyeti" başlıklı
sütununda gösterildiği gibi 44 TL’dir. Stok miktarı sipariş yenileme düzeyinin
altına düştüğünden aynı gün 50 kg zeytin sipariş edilir. Bu siparişin tedarik
süresi "Tedarik Süresi" başlıklı sütunda açıklandığı gibi 3 gündür. Buna göre
dördüncü günün başında eldeki stok miktarı bir gün önceden devreden stok miktarı
artı 50 kg olacaktır. Stok tükenmesi söz konusu olmadığından 40 günlük dönemin
ilk gününe ilişkin işlemler tamamlanmış olur. İkinci güne devreden stok miktarı
22 kg’dır. Bu günün istemi olan 11’in stok miktarı 22’den çıkartılmasıyla üçüncü
güne devreden stok miktarı 11 olarak belirlenir. 11 birimi elde tutma maliyeti
22 TL’dir. Stok kontrolünün gerçekleştirileceği 40 günlük zaman diliminin ilk
iki günü için izlenen yaklaşımın sürdürülmesiyle stok sisteminin simülasyonu
tamamlanır. Simülasyon sonuçları Tablo 15.9’da gösterilmiştir.

Tablo 15.9

|  Gün (1) | Rasg. Sayı (2) |  İstem (3) | Rasg.  Sayı (4) | Tedarik Süresi (5) | Sipariş Miktarı  (6) |  Denge  (7) | Sipariş  Maliyeti (8) | Bulundurma Maliyeti (9) | Eksiklik Maliyeti (10) |
|----------|----------------|------------|-----------------|--------------------|----------------------|-------------|-----------------------|-------------------------|------------------------|
| 0        |                |            |                 |                    |                      | 30          |                       |                         |                        |
| 1        | 20             | 8          | 22              | 3                  |                      | 22          | 180                   | 44                      |                        |
| 2        | 92             | 11         |                 |                    |                      | 11          |                       | 22                      |                        |
| 3        | 18             | 8          |                 |                    |                      | 03          |                       | 06                      |                        |
| 4        | 07             | 7          |                 |                    | 50                   | 46          |                       | 92                      |                        |
| 5        | 33             | 8          |                 |                    |                      | 38          |                       | 76                      |                        |
| 6        | 92             | 11         |                 |                    |                      | 27          |                       | 54                      |                        |
| 7        | 57             | 09         | 19              | 2                  |                      | 18          | 180                   | 36                      |                        |
| 8        | 96             | 12         |                 |                    |                      |  06         |                       | 12                      |                        |
| 9        | 91             | 11         |                 |                    | 50                   | 45          |                       | 90                      |                        |
| 10       | 34             | 08         |                 |                    |                      | 37          |                       | 74                      |                        |
| 11       | 10             | 07         |                 |                    |                      | 30          |                       | 60                      |                        |
| 12       | 87             | 11         | 16              | 2                  |                      | 19          |                       | 38                      |                        |
| 13       | 79             | 10         |                 |                    |                      | 09          | 180                   | 18                      |                        |
| 14       | 59             | 09         |                 |                    | 50                   | 50          |                       | 100                     |                        |
| 15       | 49             | 09         |                 |                    |                      | 41          |                       | 82                      |                        |
| 16       | 38             | 09         |                 |                    |                      | 32          |                       | 64                      |                        |
| 17       | 64             | 09         | 78              | 4                  |                      | 23          |                       | 46                      |                        |
| 18       | 16             | 08         |                 |                    |                      | 15          | 180                   | 30                      |                        |
| 19       | 61             | 09         |                 |                    |                      |  6          |                       | 12                      |                        |
| 20       | 10             | 07         |                 |                    |                      | 00          |                       | 00                      | 20                     |
| 21       | 86             | 11         |                 |                    | 50                   | 39          |                       | 78                      | 40                     |
| 22       | 06             | 07         |                 |                    |                      | 32          |                       | 64                      |                        |
| 23       | 90             | 11         | 03              | 2                  |                      | 21          |                       | 42                      |                        |
| 24       | 19             | 08         |                 |                    |                      | 13          | 180                   | 26                      |                        |

Tablo 15.9 (Devam)

|  Gün (1) | Rasg. Sayı (2) |  İstem (3) | Rasg.  Sayı (4) | Tedarik Süresi (5) | Sipariş Miktarı  (6) |  Denge  (7) | Sipariş  Maliyeti (8) | Bulundurma Maliyeti (9) | Eksiklik Maliyeti (10) |
|----------|----------------|------------|-----------------|--------------------|----------------------|-------------|-----------------------|-------------------------|------------------------|
| 25       | 41             | 09         |                 |                    | 50                   | 54          |                       | 108                     |                        |
| 26       | 51             | 09         |                 |                    |                      | 45          |                       | 90                      |                        |
| 27       | 82             | 10         |                 |                    |                      | 35          |                       | 70                      |                        |
| 28       | 27             | 08         |                 |                    |                      | 27          |                       | 54                      |                        |
| 29       | 37             | 09         | 93              | 5                  |                      | 18          |                       | 36                      |                        |
| 30       | 73             | 10         |                 |                    |                      | 08          | 180                   | 16                      |                        |
| 31       | 96             | 12         |                 |                    |                      | 00          |                       | 00                      | 80                     |
| 32       | 43             | 09         |                 |                    |                      | 00          |                       | 00                      | 180                    |
| 33       | 02             | 06         |                 |                    |                      | 00          |                       | 00                      | 120                    |
| 34       | 44             | 09         |                 |                    | 50                   | 41          |                       | 82                      | 180                    |
| 35       | 50             | 09         |                 |                    |                      | 32          |                       | 64                      |                        |
| 36       | 82             | 10         | 78              | 4                  |                      | 22          |                       | 44                      |                        |
| 37       | 93             | 11         |                 |                    |                      | 11          | 180                   | 22                      |                        |
| 38       | 32             | 08         |                 |                    |                      | 03          |                       | 06                      |                        |
| 39       | 93             | 11         |                 |                    |                      | 00          |                       | 00                      | 160                    |
| 40       | 63             | 09         |                 |                    | 50                   | 41          |                       | 82                      |                        |
|  TOPLAM  | 1260           | 1840       | 780             |                    |                      |             |                       |                         |                        |

Simülasyon sonuçlarının özetlendiği Tablo 15.9’un altıncı sütununda gösterildiği
gibi yedi kez sipariş verilmiş, sekizinci sütunda gösterildiği gibi sipariş
maliyeti, 1260 TL olarak hesaplanmıştır. Tablonun son satırında gösterildiği
gibi, bulundurma maliyeti 1840 TL, bulundurmama maliyeti 780 TL’dir. Bu üç
maliyetin toplanmasıyla toplam stok maliyeti 3880 TL olarak hesaplanmıştır. Bu
işlemler sipariş miktarı ve sipariş yenileme düzeyinin farklı değerleri için
istenildiği kadar tekrarlanarak uygun stok politikası belirlenebilir.

Örnek 15.4: Bir yatırım şirketi toplam süresi 4 yıl olan bir yatırım projesinin
uygunluğunu incelemektedir. Proje 100000 TL’lik bir yatırım gerektirmektedir.
İskonto oranı %10’dur. Yıllar itibariyle yatırımın sağlayacağı kazançlar
belirsizlik arzetmektedir. Yapılan incelemeler sonucunda mümkün kazançlar ve
bunların gerçekleşme olasılıkları aşağıdaki gibi elde edilmiştir. Tablodaki
dağılımın 4 yıl boyunca değişmediği kabul edilmektedir. Simülasyon ile net
bugünkü değerin ortalama ve varyansını tahmin ediniz.

Tablo 15.10

| Kazanç   | 18000 | 24000 | 36000 | 48000 | 72000 |
|----------|-------|-------|-------|-------|-------|
| Olasılık | 0.10  | 0.25  | 0.35  | 0.25  | 0.05  |

Çözüm 15.4: Kazanç olasılık dağılımı verilerinden hareketle her yıl için
ortalama veya beklenen kazanç aşağıdaki gibi hesaplanır.

E(K) = =

= 18000(0.10) + 24000(0.25) + 36000(0.35) + 48000(0.25) + 72000(0.05)

= 36000 TL

Hiç bir değişikliğin olmadığını ve ortalama kazancın her yıl için 36000 TL
olduğunu düşünelim. Bu durumda, r iskonto oranı, Y yatırım miktarı, t zaman
(burada yıl) olmak üzere net bugünkü değer (NBD),

NBD = - Y

bağıntısından aşağıdaki gibi hesaplanır.

NBD = -100000 + + + +

= 14115.16 TL

NBD’nin ortalama ve varyansının simülasyon ile tahminlenebilmesi için kazanç
dağılımının rasgele sayı kodlaması yapılmalıdır. Kodlama, aşağıdaki tablonun son
sütununda gösterilmiştir.

Tablo 15.11

|  Kazanç |  Olasılık | Birikimli Olasılık | Rasg. Sayı Aralığı |
|---------|-----------|--------------------|--------------------|
| 18000   | 0.10      | 0.10               | 00 - 09            |
| 24000   | 0.25      | 0.35               | 10 - 34            |
| 36000   | 0.35      | 0.70               | 35 - 69            |
| 48000   | 0.25      | 0.95               | 70 - 94            |
| 72000   | 0.05      | 1.00               | 95 - 99            |

18000’e karşılık gelen olasılık 0.10 olduğundan, iki rakamlı rasgele sayıların
%10’u bu olaya tahsis edilir. Tablo 15.11’in son sütununda gösterildiği gibi bu
olasılığa karşılık gelen rasgele sayı aralığı 00-09 dur. Kazancın 24000 olma
olasılığı 0.25 olduğundan, iki rakamlı rasgele sayıların %25’inin bu olaya
tahsis edilmesi gerekir. Bu olaya ayrılan rasgele sayılar 10’dan 34’e kadar olan
sayılardır. Benzer şekilde diğer kazanç değerlerine rasgele sayı aralıklarının
tahsis edilmesiyle rasgele sayı tahsis işlemi tamamlanmış olur. Rasgele sayı
aralıklarının belirlenmesinden sonra rasgele sayılar tablosundan rasgele sayı
seçimine geçilir. Tablo 15.3’ün onaltıncı satır, altıncı sütunundan başlayıp
yatay doğrultuda ardarda okunan rasgele sayılar aşağıda gösterilmiştir.

33 34 72 67 47 08 18 27 38 90 77 34 55 45 70 16 95 86 70 75 09 72 95 84 29 49 41
31 06 70 64 84

İlk rasgele sayı (33), 10 - 34 aralığına düştüğünden birinci yılın kazancı 24000
olur. İkinci rasgele sayı olan 34’de 10 - 34 aralığına düştüğünden ikinci yılın
kazancı da 24000 olur. Aynı yaklaşımla üçüncü ve dördüncü yılların kazançları
sırasıyla 24000 ve 36000 olarak belirlenir. Böylece yıllar itibariyle kazanç
değerlerinin belirlenmesi ile ilgili ilk simülasyon çalışması tamamlanmış ve
yıllar itibariyle nakit akışı aşağıdaki gibi belirlenmiş olur.

t = 0 t = 1 t = 2 t = 3 t = 4

\-100000 24000 24000 48000 36000

Yukarıdaki nakit akışını oluşturan kazanç değerlerinin projenin kabul edilmesi
durumunda yıllar itibariyle gerçekleşmesi beklenen kazanç değerleri olmadıkları
unutulmamalıdır. Bu değerler yalnızca uygun olasılıkların kullanılmasıyla
belirlenen muhtemel kazançlardır. Bu nakit akışına %10 iskonto oranının
uygulanmasıyla yatırımın NBD’si aşağıdaki gibi hesaplanır.

NBD = -100000 + + + +

= 2304.49

Altı kez tekrarlanan simülasyon sonuçları Tablo 15.12’de gösterilmiştir.

Tablo 15.12

|       | Simülasyon Numarası |           |          |          |          |          |
|-------|---------------------|-----------|----------|----------|----------|----------|
| Yıl   | 1                   | 2         | 3        | 4        | 5        | 6        |
| t = 0 | -100000             | -100000   | -100000  | -100000  | -100000  | -100000  |
| t = 1 |  24000              |  18000    |  36000   |  36000   |  72000   |  18000   |
| t = 2 |  24000              |  18000    |  48000   |  36000   |  48000   |  48000   |
| t = 3 |  48000              |  24000    |  48000   |  48000   |  48000   |  72000   |
| t = 4 |  36000              |  24000    |  48000   |  48000   |  48000   |  48000   |
| NBD   | 2304.49             | -17972.82 | 12426.06 | 14934.77 | 73971.72 | 42912.36 |

Simülasyon denemesi ile belirlenen net bugünkü değerlerin ortalaması aşağıdaki
gibi hesaplanır. Bu değer, NBD’nin simülasyonla ulaşılan değeridir.

E\*(NBD) = (141002.64) / 6 = 23500.44

NBD’nin standart sapması,

bağıntısının kullanılmasıyla aşağıdaki gibi hesaplanacaktır.

= 22897.92

Bağıntıdaki değerlerin hesaplanması süreci, Tablo 15.13’de özetlenmiştir.

Tablo 15.13

| NBD       | NBD - NBD\* | (NBD - NBD\*)2 |
|-----------|-------------|----------------|
|  2304.49  | -21195.95   |  44268296      |
| -17972.82 | -41473.26   |  1720031295    |
|  24852.13 |  1251.69    |  1827066       |
|  14934.77 |  -8565.67   |  73370703      |
|  73971.72 |  50471.28   |  2547350105    |
|  42912.36 |  19411.92   |  376821861     |
|           | TOPLAM      |  2621573956    |

Burada olduğu gibi yatırım kararı belirsizlik ortamında alınıyorsa, değişim
katsayısının hesaplanması uygun olur. Bu katsayı, risk göstergesi veya yatırım
çerçevesinin uygunluk ölçüsü olarak değerlendirilir. Risk göstergesi olarak
değişim katsayısının küçük olması arzulanır. Simülasyonun tekrarları ile
ulaşılan sonuçlarla değişim katsayısı aşağıdaki gibi hesaplanacaktır.

C\* =

= = 0.97

15.6. SÜREKLİ RASGELE DEĞİŞKENLERLE

#### SİMÜLASYON

Gerçek sistemlerin olasılıksal davranışlarının çoğu sürekli dağılımlarla daha
iyi açıklanabilir. Bu kesimde, sürekli olasılık dağılımlarından rasgele değişim
üretme konusu üzerinde durulacaktır. Sürekli dağılımlardan rasgele değişim
üretmenin temel kuralı, kesikli dağılımlardan rasgele değer üretmede kullanılan
kuraldan çok farklı değildir. Kesikli yöntemde olduğu gibi, sürekli yöntemde de
önce, dağılımın birikimli olasılık fonksiyonu elde edilir. Sonra sıfır ile 1
arasından bir rasgele sayı üretilir. Daha sonra bu rasgele sayıdan uygun bir
dönüşüm yöntemiyle istenilen dağılıma geçilir. Dönüştürme işlemi kesikli
durumdakinden oldukça farklıdır. Sürekli rasgele değişim üretmede değişik
yöntemler kullanılabilir. Yöntemlerden hangisinin uygun olduğu değer üretmede
kullanılacak olasılık dağılımına olduğu kadar algoritmanın karmaşıklığına,
rasgele değişkenlerin kesinliğine ve hesaplama etkinliğine bağlıdır. Bu kesimde
pek çok durum için uygun olan ters dönüşüm ile kabul-red yöntemleri
açıklanacaktır. Bu iki yöntemin yanı sıra uygulamada çok sık kullanılan normal
dağılımdan rasgele değişim üretme yöntemlerinden ikisi incelenecektir.

15.6.1. Ters Dönüşüm Yöntemi

Ters dönüşüm yöntemi genellikle kapalı birikimli dağılım fonksiyonuna sahip
olasılık dağılımlarında kullanılan bir yöntemdir. Birikimli dağılım
fonksiyonları kapalı formda olan üstel, tekdüze, üçgensel ve Weibull olasılık
dağılımları simülasyonda sıkça karşılaşılan dağılımlarıdır. Dağılım fonksiyonu
kapalı forma uymayan dağılımlardan rasgele değişim üretmede kullanılacak
birikimli dağılım fonksiyonunun belirlenmesinde güç-serileri açılımı gibi
yöntemler kullanılabilir. Ters dönüşüm yöntemi hem açıklanması hem de
uygulanması kolay bir yöntemdir. Belli başlı üç adımda tamamlanır.

Adım 1: X rasgele değişkeninin f(x) olasılık yoğunluk fonksiyonundan birikimli
dağılım fonksiyonu F(x)’in elde edilmesi. F(x) istatistik olarak aşağıdaki
ifadeyle açıklanır.

Adım 2: Sıfır ile 1 arasında değişen bir tekdüze rasgele değer üretilmesi.

Adım 3: F(x) = r bağıntısının x’e göre çözülmesi. Bu durumda X, yoğunluk
fonksiyonu f(x) olan olasılık dağılımından üretilmiş bir rasgele değişim olur.

Ters dönüşüm yöntemini aşağıdaki basit örnek üzerinde açıklayalım.

Örnek 15.5: X rasgele değişkeninin olasılık yoğunluk fonksiyonu aşağıdaki gibi
tanımlanmıştır.

f(x) =

Bu dağılımdan ters dönüşüm yöntemiyle rasgele değişim üretiniz.

Çözüm 15.5: Fonksiyonun grafiği aşağıda gösterilmiştir. f(x) = 2x eğrisi altında
kalan alan rasgele değişkenin gerçekleşme olasılığını gösterir. Dağılımın alt uç
noktası sıfır, üst uç noktası 1’dir. Buna göre X rasgele değişkenin bütün
değerleri bu aralıkta bulunur.

Şekil 15.5

Öncelikle f(x) = 2x’in birikimli dağılım fonksiyonu hesaplanmalıdır. Rasgele
değişken X’in birikimli dağılım fonksiyonunu bulmak için,

olduğu göz önünde bulundurularak,

F(x) =

= x2

elde edilir. Fonksiyonun tanım aralığının (0 x 1) dikkate alınmasıyla,

F(x) =

yazılabilir.

F(x)’in bulunmasından sonra ikinci adıma geçilir. Bu adım bir tekdüze rasgele
sayının bulunmasından ibarettir. Rasgele sayı r olsun.

Üçüncü adımda F(x) = r yazılır ve eşitlik x’e göre çözülür. Buna göre,

x2 = r buradan da x = olur.

0 x 1 olduğundan x = - uygun çözüm değildir.

Uygun çözüm x = + olur.

x = + şeklinde belirlenen bu eşitliğe "süreç" veya "rasgele değişim üreteci"
denir.

Rasgele değişkenin değeri, ikinci adımda belirlenen rasgele sayının üreteçte
yerine konulmasıyla bulunan sayıya eşittir. Sözgelimi, r = 0.74 olduğunda, x = =
0.86 olur. Ters dönüşüm yöntemi grafik olarak aşağıdaki gibi gösterilir.

Şekil 15.6

Rasgele değişkenin değer aralığı (0 x 1) ile birikimli olasılıkların (0 F(x) 1)
uyum içinde oldukları görülebilir. Şekil 15.6’dan görüldüğü gibi, F(x)’in 0, 1
aralığındaki herhangi bir değerine karşılık aynı aralıkta rasgele değişkenin bir
değeri vardır. Rasgele sayı da sıfır-1 aralığında tanımlanmış olduğundan r =
F(x) ilişkisinin kullanılmasıyla r, x’e dönüştürülmüş olur. x’in r cinsinden
çözümü x = F-1(r) bağıntısıyla açıklanır. Yönteme ters dönüşüm yöntemi
denmesinin nedeni x’in r cinsinden çözümünün F(x) fonksiyonunun tersine eşit
olmasıdır. r = 0 ise rasgele değişim 0 olur. Bu rasgele değişkenin alabileceği
en küçük değerdir. r = 1 olduğunda rasgele değişkenin en büyük değeri olan 1
ürer. Ters dönüşüm yöntemi ile üretilen sayıların dağılımı ile X’in dağılımının
aynı oldukları gösterilebilir. x1 x2 olmak üzere x1 ve x2 gibi herhangi iki sayı
için birikimli dağılım fonksiyonu F(x) yardımıyla P(x1 x x2) = F(x2) - F(x1)
yazılabilir. X için üretilen değerin x1 ile x2 arasında olması olasılığının da
F(x2) ile F(x1) arasındaki farka eşit olduğu gösterilebilir. Şekilden görüleceği
gibi, X için üretilen değişim ancak ve ancak seçilen rasgele sayı r1 = F(x1) ile
r2 = F(x2) aralığında ise x1 - x2 aralığında bulunur. Buna göre X için üretilen
değişimin x1 ile x2 arasında bulunması olasılığı F(x2) - F(x1) olur. Bu ters
dönüşüm yönteminin dağılımı X’in dağılımına uyan rasgele sayılar ürettiğinin
kanıtıdır. Açıklamaların ortaya koyduğu gibi, ters dönüşüm yöntemi hem oldukça
basit hem de uygulaması kolay bir yöntemdir. Bununla birlikte, yöntemin etkin
biçimde uygulanabilmesi için F(x)’in kapalı formda olması gerekir. Bir rasgele
değişim için tek bir rasgele sayı yeterlidir. Diğer yöntemlerde, sözgelimi
kabul-red yönteminde, X’in tek bir değeri için birkaç tane rasgele sayı
gerekebilir.

Ters dönüşüm yönteminin uygulaması aşağıdaki örnek problemlerle
pekiştirilecektir.

Örnek 15.6: Üstel Dağılım: 11. Bölümde açıklandığı gibi kuyruk modellerinin
oluşturulmasında kullanılan varsayımlardan bir tanesi de belirli bir zaman
aralığında kuyruk sistemine gelişlerin Poisson dağıldığıdır. Gelişlerin sayısı
Poisson dağılımına uygun ise birbirini izleyen iki geliş arasında geçen süre
(gelişler arası süre) üstel dağılımla açıklanır. Kısaca olaylar arasında geçen
süre üstel dağılıma uyar. Poisson dağılımı kesikli olmasına rağmen üstel dağılım
süreklidir. Üstel dağılım yalnızca kuyruk kuramında değil kalite kontrolünde,
güvenilirlilik analizinde de kullanılmaktadır. Üstel dağılım olasılık yoğunluk
fonksiyonu aşağıda gösterilmiştir.

f(x) =

Şekil 15.7

Çözüm 15.6: Ters dönüşüm yöntemiyle üstel dağılımdan rasgele değişim üretmek son
derece kolaydır. Önce üstel dağılımın birikimli dağılım fonksiyonunu
hesaplayalım. Üstel rasgele değişken X’in dağılım fonksiyonu aşağıda
gösterilmiştir.

F(x) =

= 1 - -

X’in tanım aralığı dikkate alındığında, F(x) aşağıdaki gibi yazılabilir.

F(x) =

Sayı üretecinde kullanılacak sayı r olsun. Çözüm için, F(x) = r eşitliğinin x’e
göre çözülmesi gerekir. Kısaca, 1 - = r yazılmalı ve x, r cinsinden
belirlenmelidir. Yukarıdaki eşitlik düzenlendiğinde,

= 1 - r

elde edilir. Eşitliğin her iki yanının logaritmasının alınmasıyla ulaşılan
bağıntı aşağıda gösterilmiştir.

x = ln(1 - r)

Sonuçta x’in r cinsinden yazılmasıyla çözüm aşağıdaki gibi belirlenmiş olur.

x = -(1/) ln (1 - r)

Hesaplamaları kolaylaştırmak için (1 - r) yerine r yazılabilir. r rasgele
olduğundan (1 - r)’de rasgele olur. Buna göre, üstel dağılımdan rasgele sayı
üreticisi,

x = -(1/) ln r

olarak belirlenmiş olur. Sözgelimi r = 1/e, x = 1/ ve r = 1 x = 0’ı verir.

Örnek 15.7: Weibull Dağılımı: Weibull dağılımı güvenilirlik analizinde hatalılar
oranı özelliklerini açıklamada kullanılan yoğunluk fonksiyonları grubudur.
Dağılımın olasılık yoğunluk fonksiyonu aşağıdaki gibidir.

f(x) = x 0

x 0, 0, 0 için Weibull yoğunluk fonksiyonu ve ’nın değişen değerlerine bağlı
olarak farklı olasılık eğrisi türetir.

Çözüm 15.7: Weibull rasgele değişim üretmek için ters dönüşüm yöntemi aşağıdaki
gibi uygulanır. Birikimli dağılım fonksiyonu tanımına göre,

F(x) =

yazılır. İntegral alma işlemini kolaylaştırmak için, y = t tanımını yapalım. dy
= t dt olur. Buna göre,

F(x) =

olarak belirlenir. Sonuçta, F(x) aşağıdaki gibi elde edilir.

F(x) = 1 -

F(x) = r bağıntısının yazılmasıyla, 1 - = r buradan da, 1 - r = dolayısıyla, r =
elde edilir. Böylece F-1(r) aşağıdaki gibi belirlenmiş olur.

F-1 = x =

Görüldüğü gibi Weibull dağılımından bir seri değişken üretebilmek için tekdüze
dağılımdan rasgele bir sayı üreterek bunu yukarıdaki bağıntıda yerleştirmek
yeterlidir.

Örnek 15.8: Tekdüze Dağılım: Olasılık yoğunluk fonksiyonu a, b aralığında sabit,
bu aralık dışında sıfır olan olasılık dağılımına tekdüze dağılım denir. Tekdüze
dağılım olasılık yoğunluk fonksiyonu şöyledir:

f(x) =

Çözüm 15.8: Tekdüze dağılımdan ters dönüşüm yöntemiyle değer üretmek için önce
X’in birikimli dağılım fonksiyonu hesaplanır. Birikimli dağılım fonksiyonu
tanımından,

F(x) = =

elde edilir. Özetle F(x) aşağıdaki gibi gösterilir.

F(x) =

Değer üretmek için önce bir rasgele sayı üretilmeli sonra F(x) = r bağıntısı
çözülmelidir. Rasgele sayı r olsun. Buna göre aşağıdaki bağıntı geçerli olur.

= r

Eşitliğin x için çözülmesiyle tekdüze dağılımın sayı üreteci, x = a + (b - a)r
şeklinde elde edilir. Söz konusu üretecin kullanılmasıyla; r = 0 için x = a, r =
1 için x = b, r = 0.5 için x = (a + b)/2 olur.

15.6.2. Kabul-Red Yöntemi

Birikimli dağılım fonksiyonu kapalı formda olmayan çok önemli dağılımlar vardır.
Kuyruk kuramının önemli dağılımlarından Erlang ile PERT’de kullanılan beta
dağılımı birikimli dağılım fonksiyonları kapalı formda oluşmayan önemli
dağılımlardır. Bu dağılımlardan rasgele değişim üretiminde kullanılabilecek
yöntemlerden birisi kabul-red yöntemidir. Kabul-red yöntemi daha çok değer
aralığı sınırlı olan dağılımlara uygulanır. Kısaca, X rasgele değişkeni a, b
aralığında değişiyorsa ve f(x) bu aralıkta sınırlı ise kabul-red yönteminin
kullanılması uygun olur.

Bu yöntem aşağıdaki adımları kapsar.

Adım 1: f(x)’in a, b aralığındaki en büyük değerinin (M) belirlenmesi.

Adım 2: r1 ve r2 gibi iki tekdüze rasgele sayının üretilmesi.

Adım 3: x\* = a + (b - a)r1 bağıntısının hesaplanması. Bu yolla a, b
aralığındaki her bir elemanın x\* olma şansının eşit olması sağlanır.

Adım 4: f(x)’in x\*’daki değerinin hesaplanması. Bu değer f(x\*) olsun.

Adım 5: eşitsizliğinin sağlanıp sağlanmadığının incelenmesi. Eşitsizlik
sağlanıyorsa x\*, X ile aynı dağılıma sahip rasgele değişim olarak kabul
edilecektir. Eşitsizliğin sağlanmaması durumunda x\* reddedilir. x\*’ın
reddedilmesi x\*’ın belirlenen dağılımdan türememiş olduğu anlamına gelir. Bu
durumda değişken değerinin belirlenebilmesi için ikinci adıma dönülür. İşlemler
rasgele değişimin kabul gördüğü noktaya değin tekrarlanır. Kabul edilebilir bir
rasgele değişimin belirlenmesi, algoritmanın pek çok kez tekrarlanmasını
gerektirebilir. Bu yönüyle algoritmanın fazla kullanışlı olmadığı
düşünülmektedir. Algoritmayı daha kullanışlı kılmak için algoritmanın ilk
adımında M gibi bir sabit kullanmak yerine f(x) fonksiyonunun kullanılması
önerilmektedir. Algoritmanın ayrıntılarını iki örnek problem üzerinde
açıklayalım.

Örnek 15.9: X’in olasılık yoğunluk fonksiyonu aşağıda gösterilmiştir. Bu
fonksiyonu ve kabul-red yöntemini kullanarak rasgele bir değer üretiniz.

f(x) =

Çözüm 15.9: X’in tanım aralığında f(x)’in eriştiği en büyük değeri bulmak için
fonksiyonun grafiğinin çizilmesi uygun olur. Grafik aşağıda gösterilmiştir.

Şekil 15. 8

Adım 1: f(x)’in a, b aralığındaki en büyük değerinin (M) belirlenmesi: Şekil
15.8’den görüldüğü gibi f(x)’in en büyük değeri x = 1 için 3’e eşittir. Bir
başka deyişle M = 3’dür.

Adım 2: r1 ve r2 gibi iki rasgele sayının üretilmesi.

Adım 3: x\* = a + (b - a)r1 bağıntısının hesaplanarak r1’in X’e dönüştürülmesi.
Bu adım X için rasgele değer üretme yöntemidir. Bu yöntemle a, b nin her bir
elemanına x\*, yani rasgele değişken değeri olma konusunda eşit şans verilmiş
olur. r1 = 0 ise x\* = a, yani aralığın sol uç noktası, r1 = 1 ise x\* = b yani,
aralığın sağ uç noktası olur. a = 0, b = 1 olduğundan x\* = r1 olur. r1 geçerli
adımın potansiyel rasgele değişken değeridir.

Adım 4: f(x)’in x\*’daki değerinin hesaplanması. x\* = r1 olduğundan f(x\*) =
3r1 olur. Bu değer izleyen adımda x\*’ın kabul veya reddine karar vermede
kullanılacaktır.

Adım 5: eşitsizliğinin sağlanıp sağlanmadığının kontrol edilmesi: f(x\*) = 3r1
ve M = 3 olduğundan = r1 bulunur. r2 r1 ise x\* olasılık yoğunluk fonksiyonu 3x
olan dağılımdan üretilen rasgele değişken olarak kabul edilecektir. Eşitsizliğin
sağlanmaması durumunda x\* reddedilir. Yani x\*’ın belirlenen dağılımdan
türetilmediği kabul edilir ve rasgele değişkenin belirlenebilmesi için ikinci
adıma dönülür.

Örnek 15.10: Olasılık yoğunluk fonksiyonu aşağıda gösterilen dağılımdan
kabul-red yöntemiyle bir rasgele değer üretiniz.

f(x) =

Çözüm 15.10: İlk adım olarak f(x)’in verilen aralıktaki en büyük değerinin
belirlenmesi gerektiğinden Örnek 15.9’daki gibi fonksiyonun grafiğinin çizilmesi
uygun olur. Böylece M değerinin kolayca belirlenmesi sağlanır. f(x) farklı iki
aralık için farklı formda tanımlandığından, basitlik sağlamak için f(x) = 1/2
fonksiyonunu f1(x), f(x) = (3/4) - (x/4) fonksiyonunu f2(x) olarak gösterelim.
Fonksiyonun grafiği aşağıda gösterilmiştir.

Şekil 15.9

Dağılımın iki farklı aralık için farklı formda olduğu göz önünde
bulundurulduğunda yöntemin dördüncü ve beşinci adımlarının duruma uygun biçimde
gözden geçirilmeleri gerekir. İlk üç adımda herhangi bir değişiklik olmaz. Yani,
ilk adımda M, ikinci adımda r1 ve r2 belirlenir, üçüncü adımda r1, x\*’a
dönüştürülür. Şekil 15.9’dan görüldüğü gibi, M = 1/2’dir. Fonksiyon 0, 3
aralığında tanımlandığından, a = 0, b = 3 olur. Bu uç değerler algoritmanın
üçüncü adımında verilen x\* = a + (b - a)r1 bağıntısında yerlerine konulduğunda,
x\* = 3r1 olarak elde edilir. x\*’ın bu değeri halihazırdaki sürecin potansiyel
rasgele değişkenidir. r1, 0 ile 1/3 arasında değişiyorsa, x\* sıfır ile 1
arasında bulunur. r1 1/3 ise, x\* 1, 3 aralığına düşer. Bu durumun dikkate
alınmasını sağlamak için önce dördüncü adımı gözden geçirelim. Eğer x\*, 0, 1
aralığında ise bu adımda f(x\*) değerinin hesaplanmasında kullanılacak fonksiyon
f1(x), aksi halde f2(x)’dir. Dördüncü adım aşağıdaki gibi özetlenir.

0 x\* 1 ise f(x\*) = f1(x\*)

= 1/2

1 x\* 3 ise f(x\* ) = f2(x\* )

= (3/4) - (x\*/4)

= (3/4) - (3r1/4)

Algoritmanın izleyen adımı x\*’ın eldeki değerini kabul veya reddetmektir.
gerçekleşiyorsa x\* kabul, aksi halde reddedilir.

Bu koşul (bkz. 4. adım) 0, 1 ve 1, 3 aralıkları için ayrı ayrı
değerlendirilmelidir. Bir başka deyişle, bu dağılım için 5. adım aşağıdaki gibi
uygulanır.

0 x\* 1 için ,yani r2 = ise x\* kabul.

1 x\* 3 için ,yani r2 = ise x\* kabul.

x\* reddedilirse 2. adıma dönülür.

Adımlar x\*’ın kabul edildiği noktaya gelinceye kadar tekrarlanır.

0 x\* 1 için ,yani r2 = ise, x\* kabul.

1 x\* 3 için ,yani r2 = ise, x\* kabul.

15.6.3. Matematiksel Türetme Yöntemi

Sürekli olasılık dağılımı denildiğinde akla ilk gelen olasılık dağılımı normal
dağılımdır. Bunun en önemli nedeni belirli varsayımların gerçekleşmesi
durumunda, hemen hemen tüm dağılımların normal dağılıma dönüşmesidir. Bu nedenle
normal rasgele değişim üretilmesine özel dikkat sarfedilmesi uygun olur. Normal
dağılım olasılık yoğunluk fonksiyonu aşağıda gösterilmiştir.

f(x) = - x +

Bu yazılışta , x değerlerinin aritmetik ortalaması, ise standart sapmasıdır.
Genel olarak normal değişken, XN(, 2) ile gösterilir. Her (, 2) çifti için
farklı bir normal dağılım söz konusu olur. Bunun yerine uygun geçiş formülleri
ile normal dağılım standartlaştırılabilir. Bunun için,

bağıntısının f(x)’de yerine konması gerekir. Yerine koyma işlemiyle standart
normal dağılım olasılık yoğunluk fonksiyonu aşağıdaki gibi elde edilecektir.

\- z +

Görüldüğü gibi fonksiyon sınırsız aralık üzerinde tanımlanmıştır. Normal
dağılımlı X’in birikimli dağılım fonksiyonu şu şekilde belirtilir.

F(x) =

Bu fonksiyonu analitik olarak değerlendirmek çok zordur.

Ters dönüşüm yöntemi ile kabul-red yönteminin her ikisi de normal dağılım için
uygun değillerdir. Çünkü, 1. Birikimli yoğunluk fonksiyonu kapalı formda
değildir, 2. Dağılım sınırlı bir aralık üzerinde tanımlanmamıştır. Ters dönüşüm
yöntemi için sayısal yöntemler uygulamak veya kabul-red yöntemi için normal
dağılım aralığının uçlarını keserek tanım aralığını sınırlı hale getirmek
mümkünse de bu yaklaşımlar yöntemlerin etkinliklerini olumsuz yönde etkilerler.
Bu durumda standart normal değişim üretmek amacıyla önerilmiş özel yaklaşımlar
kullanılabilir. Burada bu yöntemlerden ikisi açıklanacaktır.

\- Konvülüsyon tekniklerine dayanan konvülüsyon algoritması

\- Dolaysız dönüştürüm algoritması

Konvülüsyon algoritması merkezi limit teoremine dayanır. Bu teorem normal
dağılımın yaygın biçimde kullanılmasının en önemli nedenlerinden biridir. Y1,
Y2, ..., Yn, ortalama, 2 varyansla aynı dağılıma sahip bağımsız rasgele
değişkenler olsunlar. Bu durumda, Y = Y1 + Y2 + ... + Yn olarak tanımlanan
rasgele değişken n ortalama, 2 varyans ile normal dağılır. Bunu, U(0, 1)
değişkenlerine uygulayalım. R1, R2, ..., Rn, = 0.5, 2 = 1/12 varyans ile tekdüze
dağılan rasgele değişkenler olsunlar. Bu durumda Ri’lerin toplamı olarak
tanımlanan R, 0.5n ortalama, n/12 varyans ile normal dağılır. Standart normal
dağılım tanımına göre,

Z =

olarak tanımlanan Z, sıfır ortalama, 1 varyansla yaklaşık normal dağılımlıdır. n
olduğunda dağılımın normale yaklaşması daha hızlı olur. Simülasyon ile ilgili
kaynaklarda n = 12 değerinin kullanılmasının uygun olduğu ileri sürülmektedir. n
= 12 değerinin kullanılması hesaplamada büyük kolaylık sağlar. Yukarıdaki
bağıntıda, n = 12 yerine konulduğunda normal değişim üretme üreteci aşağıdaki
gibi olur. Bu eşitlik karekök alma ve bölme işlemlerinden kurtulmayı sağlar.

Z =

Ortalaması , varyansı 2 olan normal değer üretmek istediğimizi düşünelim. Bu
durumda önce süreç üretecini kullanarak Z’nin üretilmesi gerekir. Z’nin
üretilmesinden sonra X = + Z bağıntısıyla Z’nin X’e dönüştürülmesi işlemi
gerçekleştirilir. Bu dönüştürme, normal dağılım için geçerli olup diğer
dağılımlara uygulanamaz.

Normal rasgele değişim üretmede kullanılan diğer bir yöntem Box ve Muller
tarafından geliştirilmiş yöntemdir. "Box ve Muller dolaysız dönüştürüm tekniği"
uygulaması kolay, hızlı çalışan yöntemlerin başında gelir. Bu yöntem (0, 1)
aralığında bulunan r1 ve r2 gibi iki tekdüze rasgele sayının ortalaması sıfır,
varyansı 1 olan iki standart normal sayıya dönüştürülmesinden ibarettir. Normal
rasgele sayılara dönüşüm aşağıda verilmiş olan dolaysız dönüştürüm
bağıntılarının kullanılmasıyla gerçekleştirilir.

Z1 =

Z2 =

Konvülüsyon yönteminde olduğu gibi bu standart normal değerlerin ortalama, 2
varyanslı normal dağılımdan türeyen X1 ve X2 ile gösterilen normal değerlere
dönüştürülmesi çok kolaydır. Söz konusu dönüştürme, aşağıda gösterilen
eşitliklerin kullanımıyla gerçekleştirilir.

X1 = + Z1

X2 = + Z2

Konvülüsyon yöntemi yaklaşık normal değer üretirken dolaysız dönüştürüm
yöntemiyle üretilen normal değerler tam normal rasgele değerlerdir. Bu nedenle
dolaysız yöntem daha yaygın kullanılır.

# **PROBLEMLER**

1\. Orta büyüklükte bir fırın sahibi her günün başlangıcında, üreteceği ekmek
miktarına karar vermek durumundadır. Üretim maliyeti 25 TL olan ekmeğin satış
fiyatı 40 TL’dir. Daha önceki 200 günlük gözlem ve kayıtlardan günlük ekmek
talebinin 5’in katları olarak 20 ile 45 arasında değiştiği belirlenmiştir. İstem
miktarı dikkete alındığında, günlük üretim miktarının da 5’in katları olması
öngörülmektedir. Üretildiği gün satılmayan ekmekler o günün akşamında bir tavuk
üretim çiftliğine, tanesi 10 TL’den satılmaktadır. Bulundurmama maliyeti,
kaçırılan kâr olarak 15 TL’dir. İstem, yüksek, orta ve düşük olmak üzere üç
farklı düzeyde gerçekleşmektedir. Herhangi bir günde talebin yüksek düzeyde
gerçekleşmesi olasılığı 0.30, orta düzeyde gerçekleşmesi olasılığı 0.45, düşük
düzeyde gerçekleşmesi olasılığı 0.25’dir. Üretim miktarı ve istem düzeyinin
değişik grupları itibariyle istem dağılımı aşağıda verilmiştir. Günlük kârı en
büyükleyen üretim miktarını bulunuz.

| Üretim  | İstem Düzeyi |      |       |
|---------|--------------|------|-------|
| Miktarı | Yüksek       | Orta | Düşük |
| 20      | 0.05         | 0.10 | 0.15  |
| 25      | 0.10         | 0.20 | 0.25  |
| 30      | 0.25         | 0.30 | 0.35  |
| 35      | 0.30         | 0.25 | 0.15  |
| 40      | 0.20         | 0.10 | 0.05  |
| 45      | 0.10         | 0.05 | 0.05  |

2\. A ve B kendi aralarında çok basit bir oyun oynamaktadırlar. Oyunda bir çift
zar yere atılmakta ve oyunun galibi üste gelen sayıların toplamına göre
belirlenmektedir. Sayıların toplamı 7 veya 11 olduğunda A; 2, 3 veya 12
olduğunda B kazanan taraf olmaktadır. Bunların dışındaki her durum için A’ya
yeni bir şans verilmektedir. Oyunun bu bölümünde zar atışı 7 veya ilk atıştaki
toplama eşit oluncaya kadar tekrarlanmaktadır. Toplam 7 olduğunda A oyunun
yenileni, toplam ilk atıştaki toplama eşit olduğunda oyunun yeneni olmaktadır.
Zarların hilesiz olduğunu düşünerek A’nın kazanan taraf olması olasılığını
bulunuz.

3\. Bir sıvı yakıt dolum tesisine tanker gelişleri arasında geçen sürenin
olasılık dağılımı aşağıda gösterilmiştir. Tesisin doldurma işlemini
gerçekleştirdiği iki kapısı (A ve B) vardır. B kapısı A kapısından daha yeni
olduğundan B’de gerçekleştirilen dolum işlemi A’da gerçekleştirilen dolum
işleminden daha kısa sürmektedir.

| Gelişler Arası Süre (gün) |  Olasılık |
|---------------------------|-----------|
| 1                         | 0.20      |
| 2                         | 0.25      |
| 3                         | 0.35      |
| 4                         | 0.15      |
| 5                         | 0.05      |

Doldurma işleminin uzunluğu doldurulan tankerin tipine bağlıdır. Bir süpertanker
A kapısında 4 günde, B kapısında 3 günde doldurulmaktadır. Orta büyüklükteki bir
tankerin doldurulması A kapısında 3 günde, B kapısında 2 günde tamamlanmaktadır.
Tanker küçük ise doldurulması A kapısında 2 günde, B kapısında 1 günde
tamamlanmaktadır. Dolum tesisine ulaşan tankerler tesisin ana giriş kapısında
tek bir kuyruk oluşturarak dolum sırasının kendilerine gelmesini
beklemektedirler. Servis ilk gelen ilk çıkar kuralına göre verilmektedir. Tanker
tipleri ve bunların tesise gelme sıklıkları aşağıda gösterilmiştir.

| Tanker Tipi  | Olasılık |
|--------------|----------|
|  Süper       | 0.40     |
|  Orta        | 0.35     |
|  Küçük       | 0.25     |

Simülasyon modelini geliştirerek ortalama kuyruk uzunluğunu, ortalama bekleme
zamanını ve kapıların aylak kalma sürelerini hesaplayınız.

4\. Mönüsünde pizadan başka hamburger ve salata bulunan bir piza salonu
müşterilerinin, özellikle gündüz 11.00-13.00 saatleri arasında, çok fazla vakit
kaybettikleri yolundaki şikayetlerine maruz kalmaktadır. Müşteri gelişleri
arasında geçen sürenin olasılık dağılımı aşağıda gösterilmiştir.

| Gelişler Arası Süre (dak.) |  Olasılık |
|----------------------------|-----------|
|  3                         | 0.30      |
|  5                         | 0.20      |
|  6                         | 0.15      |
|  8                         | 0.30      |
| 10                         | 0.15      |

Hamburger müşterileri, genellikle, gruplar halinde gelmektedirler. Müşterilerin
sipariş ettikleri hamburger sayısı 0, 1 veya 2’dir Grup büyüklükleri ile kişi
başına sipariş edilen hamburger sayısının olasılık dağılımları aşağıda
gösterilmiştir.

| Grup Büyüklüğü |  Olasılık | Hamburger Sayısı |  Olasılık |
|----------------|-----------|------------------|-----------|
| 1              | 0.40      | 0                | 0.20      |
| 2              | 0.30      | 1                | 0.65      |
| 3              | 0.20      | 2                | 0.15      |
| 4              | 0.10      |                  |           |

Müşterilerin salonda kalma süreleri olasılık dağılımı aşağıdaki gibidir. Salona
bir grup geldiğinde grubun sistemde kalış süresi salonu en son terkeden grup
elemanının sistemde kalma süresine eşittir. Sistemin durumunu 6 saatlik süre
için simüle ederek aşağıdaki soruları yanıtlayınız.

| Süre (dak.) | Olasılık |
|-------------|----------|
| 10          | 0.10     |
| 15          | 0.40     |
| 20          | 0.30     |
| 25          | 0.20     |

a. Bir saat için ortalama kaç adet hamburger hazırlanması uygun olur?

**b**. Bir grup salonda ortalama kaç saat kalır?

**5**. Bir fabrikada makineler rasgele zamanlarda ve birbirlerinden bağımsız
olarak arızalanmakta ve onarılıncaya kadar üretim dışı kalmaktadırlar.
Arızaların giderilmesi için harcanan süre tıpkı arızaların ortaya çıkış zamanı
gibi birbirlerinden bağımsız ve rasgeledir. Bir saat içinde arızalanan makine
sayısı ile onarım süresi (saat) olasılık dağılımları aşağıda gösterilmiştir.

| Arıza Sayısı |  Olasılık | Onarım Süresi |  Olasılık |
|--------------|-----------|---------------|-----------|
| 0            | 0.900     | 1             | 0.100     |
| 1            | 0.085     | 2             | 0.240     |
| 2            | 0.012     | 3             | 0.450     |
| 3            | 0.003     | 4             | 0.165     |
|              |           | 5             | 0.040     |
|              |           | 6             | 0.005     |

Bir makinenin bir saat boyunca (onarıma alınması ve onarılması için geçen süre)
üretim dışı kalmasının işletmeye maliyeti 80 TL’dir. Onarım işlerinden sorumlu
bir ustaya saatte 8 TL ödendiğine göre kaç usta çalıştırılmasının uygun
olacağını hesaplayınız. Sistemi aşağıdaki rasgele sayıları (sol üst köşeden
başlayıp sağa doğru okuyarak) kullanarak 50 saat uzunluğundaki dönem için simüle
ediniz.

Arızalanan makine sayısı için:

985 118 834 886 995 654 801 743 699 098

914 803 441 125 636 611 154 945 424 235

044 005 359 598 460 321 692 195 451 948

100 375 084 990 128 660 310 852 635 737

980 331 809 797 186 740 541 116 483 690

Onarım süresi için:

765 648 196 093 801 340 455 020 053 035

672 121 099 195 981 783 389 421 125 623

6\. Bir kitabevi yöneticisi "Katma Değer Vergisi" isimli kitaptan kaç adet
sipariş etmesi gerektiğini araştırmaktadır. Yayınevinden 60 TL’ye satın alınan
kitabın satış fiyatı 80 TL’dir. Vergi yasalarının bir kısmı yıldan yıla
değiştiğinden basıldığı yıl içinde satılmayan bir kitabın sonraki yıllardaki
satış fiyatı 30 TL’dir. Geçmiş dönem deneyimlerinden kitabın yıllık istem
miktarı olasılık dağılımı aşağıdaki gibi belirlenmiştir.

İstem Miktarı: 15 16 17 18 19 20 21 22

Olasılık: 0.05 0.08 0.20 0.45 0.10 0.07 0.03 0.02

Tablo 15.3’ün sol üst köşesinden başlayıp düşey doğrultuda 3’er atlayarak
belirlediğiniz rasgele sayıları kullanarak 20 yıllık zaman döneminin istem
miktarını oluşturunuz. Yöneticinin olası eylem biçimlerini dikkate alarak
ortalama kârını hesaplayınız. En iyi eylem biçimini belirleyiniz.

7\. Aşağıda gösterilen dağılımlardan birer rasgele değişim üretiniz.

a. f(x) = b. f(x) = c. f(x) = d. f(x) = e. f(x) =
