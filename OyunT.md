## *dokuzuncu BÖLÜM*

###### Oyun KuramI

## 9.1. GİRİŞ

Şimdiye kadar, tek bir karar vericinin bulunduğu karar problemleri üzerinde
durulmuştur. Problemde tek bir karar vericinin bulunduğundan, amaç fonksiyonu bu
karar vericinin kararına bağlı kalarak değerlendirilmiştir. Uygulamada iki veya
daha çok sayıda karar vericinin bulunduğu karar problemleriyle karşılaşmak daha
olağandır. Esas amacı, birbirlerine rakip olan ve çıkarları çatışan taraflara
akılcı davranış kurallarının belirlenmesinde yardımcı olmak olan oyun kuramı, bu
tür karar ortamlarını açıklayan matematiksel bir yaklaşımdır. Oyun kuramında
karar vericilerin her biri bir oyuncudur. Farklı hedef ve amaçlara sahip olan
oyuncuların kaderleri birbirlerine bağlıdır. Matematiksel olarak bu, "her
oyuncunun kendisine ait bir amaç fonksiyonu vardır ve amaç fonksiyonlarının en
iyi değerleri yalnızca ait olduğu karar vericinin benimseyeceği stratejiye
değil, diğer karar verici(ler)nin strateji(ler)sine de bağlıdır" şeklinde
yorumlanabilir. Bu durum, tam anlamıyla bir çatışma durumudur. Çatışma durumları
daha çok oyunlarda, spor karşılaşmalarında, iktisatta ve askeri hareketlerde
ortaya çıkar. Rakiplerini dikkate almayan bir oyuncunun başarılı olması
beklenmemelidir.

Oyun kuramı ilk kez Fransız matematikçisi Emile Borel tarafından 1921 yılında
ortaya atılmış olmakla birlikte, sistematik olarak matematikçi John von Neumann
ile iktisatçı Oscar Morgenstern tarafından geliştirilmiştir. Oyun kuramının
temel ilkeleri bu iki yazarın 1944 yılında yayınladıkları "The Theory of Games
and Economic Behaviour" isimli çalışmalarında açıklanmıştır. O günden bu yana
oyun kuramı büyük gelişmeler kaydetmiş, John Nas oyun kuramına yaptığı katkılar
için 1994 ekonomi nobel ödülüyle ödüllendirilmiştir. Nash tarafından
geliştirilen "Nash dengesi ve Nash pazarlık problemi" modern oyun kuramının köşe
taşları kabul edilmektedir.

## 9.2. Temel Kavramlar

Bir oyun eksiksiz biçimde tanımlanmış kurallara uygun olarak sürdürülen ve
oyuncuların kendileri için uygun olan stratejileri ve bunlardan herhangi birinin
seçimi ile ilgili mücadele sonuçlarını bildikleri varsayılan bir sistemdir. Daha
basit olarak oyun, birbirleriyle rekabet eden ve her biri kazanmayı isteyen iki
veya daha fazla sayıda karar vericinin (oyuncunun) bulunduğu karar ortamı
şeklinde tanımlanabilir.

Oyunlar çeşitli özelliklerine göre farklı gruplarda sınıflandırılır. Temelde
oyunlar "şans oyunları" ve "strateji oyunları" olmak iki grup altında incelenir.
Oyunlar oyuncu sayısına göre de iki grupta sınıflandırılır. Oyuna katılan iki
oyuncu varsa "iki kişili", ikiden fazla oyuncu varsa genel olarak "n kişili"
oyunlardan söz edilir. Oyunların bir başka sınıflandırılması oyunun sayısal
sonucuna göre yapılır. Oyuncuların kazançlarının toplamı sıfır ise yani,
oyunculardan biri tam diğer tarafın kaybettiği kadar kazanıyorsa oyun, "sıfır
toplamlı" bir oyundur. Sıfır toplamlı oyunlarda oyuncuların çıkarları birbirine
tamamiyle zıttır. Sayısal sonucu sıfırdan farklı oyunlara sabit toplamlı oyunlar
denir. Sabit toplamlı bir oyunda da tarafların çıkarları tamamiyle birbirine
zıttır. Çünkü taraflardan birinin kazancındaki bir birim artış diğer tarafın
kazancında bir birim azalış demektir. Oyuncuların yaptığı ödemeler toplamının
sıfırdan farklı olması durumunda sıfırdan farklı veya sabit toplamlı oyunlardan
söz edilir. Oyuncuların kazançları toplamının sabit bir sayı olmaması durumunda
oyun sabit toplamlı olmayan bir oyundur. Bu tür oyunlarda tarafların çıkarları
tamamiyle zıt değildir. Taraflar birlikte hareket ederek çıkar sağlayabilirler.
Oyunların bir başka sınıflandırılması oyuncuların strateji sayılarının dikkate
alınmasıyla yapılabilir. Herhangi bir oyuncunun stratejilerinin sayısı belirsiz
ise oyun "sonsuz oyun" olur. Her oyuncunun strateji sayısı sonlu ise oyun "sonlu
oyun" dur. Oyunlar her oyuncunun rakibinin hareketleri hakkındaki bilgisinin
derecesi ve cinsine göre de sınıflandırılabilir. Eğer bir oyunda her oyuncu her
hamleyi yaparken daha önce yapılmış olan bütün kişisel veya talih hareketlerinin
sonuçlarını biliyorsa "tam bilgili" oyun söz konusu olur. Sözgelimi satranç ve
dama tam bilgili oyunlardır. Tam bilgili olmayan oyunlarda oyuncular böyle bir
tam bilgiden yoksundurlar. Örneğin pokerde oyuncular rakiplerinin ellerindeki
kağıtları bilmezler. Uygulamada genellikle tam bilgili olmayan oyunlarla
karşılaşılır. Çünkü, çatışma durumunun esas bileşeni tarafların birbirlerinin
hareketlerini bilmemesidir.

Oyun kuramının temel kavramlarından birisi de strateji kavramıdır. Karar kuramı
bölümünde sıkça karşılaştığımız strateji kavramı, oyun söz konusu olduğunda
aşağıdaki gibi tanımlanır.

Strateji: Oyunun devamı sırasında ortaya çıkabilecek bütün durumlar için
oyuncuların seçişlerini belirten kuralları kapsayan kümeye strateji denir.

Oyuncuların amacı en iyi stratejileri, yani kendilerine en fazla kazanç
sağlayacak eylem biçimlerini belirlemektir. Strateji kavramının anlamlı olması
için oyunda kişisel hareketler bulunmalıdır. Bir kişisel hareket, verilen
durumda mümkün olan hareketlerden birinin oyunculardan biri tarafından bilinçli
olarak seçilmesidir. Bir kişisel hareket oyuncuların daha önce yapmış oldukları
hareketlere bağlıdır. Barbut veya rulet gibi salt şans oyunlarında hiçbir
strateji yoktur. Şans oyunları yalnızca şans hareketlerinden oluşur.

## 9.3. İkİ Kİşİlİ SIfIr ToplamlI Oyunlar

Daha önce açıklandığı gibi bir oyunda iki oyuncu varsa oyun iki kişili bir
oyundur. İki kişili bir oyunda oyuncuların kazançları toplamı sıfırsa oyun
iki-kişili sıfır-toplamlıdır. Bu bölümde iki-kişili sıfır-toplamlı sonlu oyunlar
üzerinde durulacaktır. İki-kişili sıfır-toplamlı sonlu bir oyunda,

1.  Biri satır oyuncusu, diğeri sütun oyuncusu olarak isimlendirilen iki oyuncu
    vardır. Satır oyuncusu yerine bizim taraf, sütun oyuncusu yerine de karşı
    taraf deyimlerine rastlanabilir.

2.  Satır oyuncusu için m, sütun oyuncusu için n tane mümkün strateji vardır. Bu
    oyun kısaca mxn oyun olarak isimlendirilir.

3.  Satır oyuncusunun stratejileri R1, R2, ..., Rm ile sütun oyuncusunun
    stratejileri C1, C2, ..., Cn ile gösterilsin. Oyuncuların strateji
    seçimlerinin türlü birleşimlerinden sonuçlanan kazanç veya kayıplarını
    bildiğimizi varsayalım. Satır başlıkları satır oyuncusunun Ri stratejileri,
    sütun başlıkları sütun oyuncusunun Cj stratejileri olmak üzere bu değerler
    bir tablo (matris) şeklinde yazılabilir. Bu tabloya ödül, ödeme, kazanç veya
    kısaca "oyun matrisi" denir. Bir mxn oyunun kazanç matrisi Tablo 9.1’de
    gösterildiği gibidir.

**Tablo 9.1**

| Satır Oyuncusu Stratejisi |  Sütun Oyuncusu Stratejisi |     |     |     |     |     |
|---------------------------|----------------------------|-----|-----|-----|-----|-----|
|                           | C1                         | C2  | ... | Cj  | ... | Cn  |
| R1                        | a11                        | a12 | ... | a1j | ... | a1n |
| R2                        | a21                        | a22 | ... | a2j | ... | a2n |
| ..                        | ..                         | ..  | ... | ..  | ... | ..  |
| Ri                        | ai1                        | ai2 | ... | aij | ... | ain |
| ..                        | ..                         | ..  | ... | ..  | ... | ..  |
| Rm                        | am1                        | am2 | ... | amj | ... | amn |

Sıfır toplamlı bir oyunun matrisi geleneksel olarak yalnızca oyunculardan
birisinin kazancı ile açıklanır. Buna göre oyunculardan birinin kazanç matrisi
diğer oyuncunun kazanç matrisinden belirlenebilir. Bir oyuncunun kazanç
matrisinin tüm elemanlarının ters işaretlilerinden oluşan matris diğer oyuncunun
kazanç matrisidir.

Satır oyuncusunun Ri, sütun oyuncusunun Cj gibi belirli bir stratejiyi kabul
ettiklerini varsayalım. Oyun matrisi satır oyuncusuna göre düzenlenmiş ise aij
satır oyuncusunun kazancını (sütun oyuncusunun kaybını) gösterir.

**Örnek 9.1**: Satır oyuncusunun iki (R1, R2), sütun oyuncusunun dört (C1, C2,
C3, C4) stratejisinin bulunduğu bir oyunun, satır oyuncusunun kazançlarına göre
düzenlenen matrisi aşağıda gösterilmiştir. Oyuncuların stratejilerinin değişik
birleşimlerinden herhangi iki tanesi için oyuncuların kazanç ve kayıplarını
bulunuz.

**Tablo 9.2**

| Satır Oyuncusu Stratejisi | Sütun Oyuncusu  Stratejisi |    |    |    |
|---------------------------|----------------------------|----|----|----|
|                           | C1                         | C2 | C3 | C4 |
| R1                        | 3                          | -2 |  5 | 6  |
| R2                        | 2                          |  1 | -2 | 4  |

**Çözüm 9.1**: Satırdaki oyuncunun R2’yi sütundaki oyuncunun C3’ü seçmesi
durumunda satır oyuncusunun kazancı a23 olur. a23 = -2 olduğundan satır oyuncusu
için negatif kazanç yani kayıp, sütun oyuncusu için negatif kayıp yani, kazanç
söz konusudur. Satır oyuncusunun R1, sütun oyuncusunun C4’ü seçmeleri durumunda
satır oyuncusunun kazancı a14 kadar, yani 6 birim olacaktır. Bu sütun
oyuncusunun 6 birim kaybetmesi demektir.

**9.3.1. İki-Kişili Sıfır-Toplamlı Oyunların Temel Varsayımları**

İki-kişili sıfır-toplamlı oyunların en önemli varsayımı, her oyuncunun rakibinin
kendisinin hangi stratejiyi seçeceği hakkında tam bilgisi olmasına karşın,
kendisi için en iyi olan stratejiyi seçme şansına sahip olduğudur.

İki-kişili sıfır-toplamlı oyunları oynama kuralı bu varsayıma dayanır. Söz
konusu oyunlar ile ilgili kuram John von Neumann ve Oskar Morgenstern tarafından
geliştirilmiştir. Bu varsayımı kullanarak oyuncuların stratejilerini nasıl
belirlediklerini sayısal bir örnek üzerinde açıklayalım.

**Örnek 9.2**: Oyunculardan her birinin üçer stratejisinin bulunduğu bir 3x3
oyunun kazanç matrisi Tablo 9.3’de verildiği gibidir. Söz konusu kazanç
matrisini dikkate alarak, oyuncuların oyunu hangi stratejilerle oynayacağını
belirleyiniz*.*

**Tablo 9.3**

| Satır  Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En  Küçüğü |    |   |
|----------------------------|---------------------------|------------------|----|---|
|                            | C1                        | C2               | C3 |   |
| R1                         | 16                        | 10               | 7  | 7 |
| R2                         | 8                         | 9                | 4  | 4 |
| R3                         | 9                         | 1                | 2  | 1 |
| Sütun  En Büyüğü           | 16                        | 10               | 7  | - |

**Çözüm 9.2**: Tablo 9.3’den görüleceği gibi her bir oyuncunun üçer stratejisi
bulunduğundan oyun bir 3x3 oyundur. İlk önce satır oyuncusunu ele alalım. Bu
oyuncu R1 stratejisini seçerse, sütun oyuncusu C3 stratejisini seçerek kendi
kaybını, dolayısıyla rakibinin kazancını mümkün olan en düşük düzeyde tutar. Bu
değer yukarıdaki oyun matrisine eklenen "satır en küçüğü" başlıklı sütunda
gösterildiği gibi 7’dir. Satır oyuncusunun ikinci stratejiyi seçmesi durumunda
sütundaki oyuncu yine kendisi için en az (4) kayıp sağlayacak olan stratejiyi
yani, üçüncü stratejiyi seçecektir. Satır oyuncusu üçüncü stratejiyi seçerse
sütun oyuncusu ikinci stratejiyi seçerek yine kendi kaybını dolayısıyla
rakibinin kazancını en düşük kazanç olan 1’de tutmayı başarır. Bu açıklamaların
ortaya koyduğu gibi satır oyuncusu dikkatini satır en küçüklerinin en büyüğüne
karşılık gelen strateji üzerinde yoğunlaştırmak durumundadır. Böylece,
kendisinin her stratejisi için rakibinin seçimi ne olursa olsun rakibinin
kendisine garanti ettiği en düşük kazancı en büyüklemiş olur. Kısaca, enb(7, 4,
1) = 7 olduğundan satır oyuncusu için en iyi strateji R1’dir.

Satır oyuncusunun strateji seçimiyle ilgili bu açıklamalar, satır oyuncusu için
en iyi hareketin satır en küçük değerlerinden en büyük olanının işaret ettiği
stratejiyi seçmek olduğunu ortaya koymaktadır. Yukarıda açıklandığı gibi bu,
sütundaki oyuncu ne yaparsa yapsın satırdaki oyuncunun kazanacağından emin
olduğu miktardır. Bu miktara oyunun "alt değeri" veya "maksimini", ile
gösterilen bu değere karşılık gelen stratejiye de "maksimin strateji" denir.
Maksimin strateji satır oyuncusunun en iyi stratejisidir. Tek bir stratejiye
bağlı kalındığında değeri satır oyuncusunun garantileyeceği en büyük kazançtır.

Problemi bir de sütun oyuncusu açısından ele alalım. Sütundaki oyuncu C1
stratejisini seçerse, satırdaki oyuncu buna kendisine en yüksek kazancı (sütun
en büyüğü) garanti eden birinci strateji ile karşılık verir. Sütun oyuncusunun
ikinci stratejiyi seçmesi durumunda satır oyuncusu yine birinci stratejiyi
seçecek ve kazancının en yüksek olmasını sağlayacaktır. Sütun oyuncusunun üçüncü
stratejiyi seçmesi durumunda satır oyuncusu için en iyi strateji yine kendisine
en yüksek kazancı garanti eden birinci satırdaki strateji olur. Satır
oyuncusunun kazancı sütun oyuncusunun kaybına eşit olduğundan, sütun oyuncusu
kaybını en düşük düzeyde tutmak için sütun en büyüklerinin en küçüğünü sağlayan
stratejiyi seçmek durumundadır. Sütun en büyükleri Tablo 9.3’ün en alt satırında
"sütun en büyüğü" başlığı altında gösterilmiştir. Sütun oyuncusunun strateji
seçimiyle ilgili olarak yapılan bu açıklamalardan sütun oyuncusunun sütun en
büyük değerlerinden en küçük olanının işaret ettiği stratejiyi seçmesi gerektiği
anlaşılır. Bu durumda, satırdaki oyuncu ne yaparsa yapsın sütundaki oyuncunun
kaybı en az olur. Bu miktara oyunun "üst değeri" denir ve ile gösterilir. ’ya
karşılık gelen stratejiye "minimaks strateji" denir. Minimaks strateji sütun
oyuncusunun en iyi stratejisidir.

Stratejilerin kararlı olduğu bazı oyunlar vardır. Bunlar alt ve üst değerleri
eşit olan oyunlardır. Bu tür oyunlara "tepe noktalı oyun"lar denir. Tepe noktası
aynı zamanda bir denge noktası olup hiç bir oyuncu denge durumunu bozmaz. = ise
bunların ortak değerine "oyunun değeri" denir. Oyunun değeri g ile
gösterilecektir. Oyun matrisinin satır oyuncusuna göre düzenlendiğini kabul
edelim. g pozitif ise oyunun sonunda satır oyuncusu ortalama g birim
kazanacağından oyun satır oyuncusu için çekicidir. g negatif ise oyunun sonunda
satır oyuncusu g birim kaybedeceğinden oyun sütun oyuncusu için çekicidir.
Herhangi bir oyunun birden fazla tepe noktası olabileceği gibi hiçbir tepe
noktası bulunmayabilir. Tepe noktasının en önemli özelliği oyuncuların en iyi
stratejilerine sadık kalmaları gerektiğine işaret etmesidir. Bir başka deyişle,
oyunculardan herhangi biri rakibi en iyi stratejisine sadık iken kendisi en iyi
stratejisinden ayrılırsa en iyi koşullarda kazancı aynı kalır genellikle de
azalır. Şu halde, satır oyuncusu en iyi stratejisini oynarken, sütun oyuncusu en
iyi stratejisini oynamaktan vazgeçmekle satır oyuncusunun kazancını azaltamaz.
Rakibinin kazancı en kötü ihtimalle aynı kalır, genellikle de artar. Benzer
şekilde, sütun oyuncusu en iyi stratejisini kullanırken, satır oyuncusu
kendisinin en iyi stratejisinden vazgeçerse sütun oyuncusunun kaybı, dolayısıyla
satır oyuncusunun kazancı asla artmaz genellikle de azalır. Açıklamaların ortaya
koyduğu gibi, tepe noktalı bir oyunda oyuncuların en iyi stratejilerinin bir
kararlılığı vardır. En iyi stratejiler çifti bu anlamda bir "denge konumu" dur.
Bu koşullarda ön bilginin oyunculardan hiçbirine hiçbir yarar sağlamadığını
kaydedelim. Tepe noktalı bir oyunda her iki taraf da kendi en iyi stratejilerine
bağlanırsa, ortalama kazanç oyunun değeri olan ve hem alt hem de üst değere eşit
olan g olacaktır.

Yukarıdaki örnek problem esas alındığında, sözgelimi sütun oyuncusu en iyi
stratejisi olan üçüncü stratejisini oynarken, satır oyuncusu kendisi için en iyi
olan birinci stratejisinden vazgeçerse kazancı ikinci stratejiyi seçmesi
durumunda en fazla 4, üçüncü stratejiyi seçmesi durumunda ise en fazla 2 olur.
Benzer şekilde, satır oyuncusu en iyi stratejisini oynarken sütun oyuncusu
kendisi için en iyi olan üçüncü stratejiden vazgeçerek birinci stratejiyi
oynarsa kaybı 7 yerine 16, ikinci stratejiyi oynarsa 10 birim olur.

Arı (Sade) Strateji: Oyun kaç kez tekrar edilirse edilsin oyunun her bir
tekrarında hep seçilen stratejiye sade strateji denir.

Sade stratejiler tepe noktasının belirlediği stratejilerdir.

Bir oyununun tepe noktasını belirleme sürecini sayısal bir örnek üzerinde
gösterelim.

**Örnek 9.3**: Aşağıdaki kazanç matrisine sahip 4x4 oyunun tepe noktasını
bulunuz.

**Tablo 9.4**

| Satır Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En Küçüğü |       |    |        |
|---------------------------|---------------------------|-----------------|-------|----|--------|
|                           | C1                        | C2              | C3    | C4 |        |
| R1                        | -8                        |  7              |  2    | 3  | -8     |
| R2                        |  1                        | -6              | -2    | 5  | -6     |
| R3                        |  7                        |  5              |  3    | 4  |  **3** |
| R4                        | 4                         | -4              | -8    | 6  | -8     |
| Sütun En Büyüğü           | 7                         | 7               | **3** | 6  | 3 = 3  |

**Çözüm 9.3**: Oyunda tepe noktası bulunup bulunmadığını belirleyebilmek için
önce her satırın en küçük değeriyle satır en küçüğü başlıklı sütunu, daha sonra
her sütunun en büyük değeriyle sütun en büyüğü başlıklı satırı oluşturalım.
Oluşturulan sütunu oyun matrisinin sütunlarına, satırı ise satırlarına
ekleyelim. Şimdi de sırasıyla oyunun alt değeri () ile üst değerini () bulalım.
Oyunun alt ve üst değerleri aşağıda gösterilmiştir.

Oyunun alt değeri = = enb(-8, -6, 3, -8) = 3

Oyunun üst değeri = = enk(7, 6, 3, 6) = 3

3 = 3 olduğundan, oyunun tepe noktası vardır. Bu noktada kesişen iki stratejiden
R3 satır oyuncusunun, C3 sütun oyuncusunun en iyi stratejileridir. Oyunun
ortalama değeri g = 3 olduğundan oyun satır oyuncusu için çekicidir.

Uygulamada tepe noktalı bir oyunla karşılaşma olasılığı, tepe noktası bulunmayan
bir oyunla karşılaşma olasılığından daha küçüktür. Eşit olmayan alt ve üst
sınırlarla, yani tepe noktasız oyunlarla karşılaşmak daha geneldir.

**Örnek 9.4**: Kazanç matrisi aşağıdaki gibi olan oyunun tepe noktasını bulunuz.

**Tablo 9.5**

| Satır Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En Küçüğü |    |    |        |
|---------------------------|---------------------------|-----------------|----|----|--------|
|                           | C1                        | C2              | C3 | C4 |        |
| R1                        | 8                         | -7              | 12 | 13 | -7     |
| R2                        | 1                         | 6               | -2 | 5  | **-2** |
| R3                        | 10                        | 5               | -4 | 4  | -4     |
| Sütun En Büyüğü           | 10                        | **6**           | 12 | 13 | 6 -2   |

**Çözüm 9.4**: Örnek 9.3’deki gibi önce her satırın en küçük değeriyle satır en
küçüğü başlıklı sütunu, daha sonra her sütunun en büyük değeriyle sütun en
büyüğü başlıklı satırı oluşturalım. Oluşturulan sütunu ödemeler matrisinin
sütunlarına, satırı ise ödemeler matrisinin satırlarına ekleyelim. Şimdi de
sırasıyla oyunun alt ve üst değerlerini bulalım. Söz konusu değerler aşağıda
gösterilmiştir.

Oyunun alt değeri = = enb(-7, -2, -4) = -2

Oyunun üst değeri = = enk(10, 6, 12, 13) = 6

\-2 6 olduğundan bu oyunun tepe noktası yoktur. Oyunun tepe noktası
bulunmadığından maksimin ve minimaks stratejilerden dolayısıyla sade
stratejilerden söz edilemez. Tepe noktası bulunmayan oyunlarda strateji
belirleme yöntemi ileride açıklanacaktır.

**Örnek 9.5**: Satır oyuncusu sütun oyuncusuna göstermeden elindeki kağıda 1 ile
20 arasında bir sayı yazar ve sütun oyuncusuna sayıyla ilgili doğru veya yalan
söyler. Sütun oyuncusu ya buna inanır veya rakibinin doğru söylemediğini
düşünerek sayıyı kendisine göstermesini ister. Satır oyuncusunu suçsuz yere
suçlaması durumunda sütun oyuncusu satır oyuncusuna 15 TL öder. Sütun
oyuncusunun satır oyuncusunun kendisine yalan söylediğini doğru tesbit etmesi
durumundaki kazancı 20 TL’dir. Sütun oyuncusu satır oyuncusunun doğru
söylediğini kabul ederse satır oyuncusu sütun oyuncusuna 5 TL öder. Satır
oyuncusu yalan söylediği halde sütun oyuncusu buna inanırsa satır oyuncusu 5 TL
kazanır. Oyun matrisini düzenleyiniz ve oyuncuların sade stratejilerini bulunuz.

**Çözüm 9.5**: Görüldüğü gibi satır oyuncusunun doğru veya yalan söylemek gibi
iki stratejisi vardır. Sütun oyuncusunun da satır oyuncusuna inanmak veya
inanmamak gibi iki stratejisi vardır. Dolayısıyla oyun 2x2 boyutundadır. Bu
belirlemenin ardından düzenlenen ödemeler matrisi Tablo 9.6’da gösterilmiştir.
Sütun en büyükleriyle oluşturulan satır ve satır en küçükleriyle oluşturulan
sütun da tabloda gösterilmiştir.

#### Tablo 9.6

| Satır Oyuncusu Strateji | Sütun Oyuncusu Stratejisi | Satır En Küçüğü |      |
|-------------------------|---------------------------|-----------------|------|
|                         | İnanmak                   | İnanmamak       |      |
| Doğru Söylemek          | -5                        | 15              | -5   |
| Yalan Söylemek          |  5                        |  -20            |  -20 |
| Sütun En Büyüğü         |  5                        | 15              | -5 5 |

= enb(-5, -20) = -5 = enk(5, 15) = 5 olduğundan oyunun tepe noktası yoktur.
Dolayısıyla oyuncuların sade stratejilerinden söz edilemez.

**Örnek 9.6**: İki oyuncu aynı anda taş, kağıt veya makas demektedirler.
Söylenen kelimeler aynı olduğunda beraberlik söz konusu olmaktadır. Aksi halde,
diğerinden daha güçlü olan nesnenin adını söyleyen oyuncu rakibinden 1 TL
almaktadır. Makas kağıdı kestiğinden makas kağıttan, kağıt taşı sardığından
kağıt taştan, taş makası kırdığından taş makastan güçlüdür. Oyunun kazanç
matrisini düzenleyerek oyuncuların sade stratejilerini belirleyiniz.

**Çözüm 9.6**: Her iki oyuncunun taş, kağıt veya makas demek olmak üzere üçer
stratejisi vardır. Yani oyun 3x3 boyutundadır. Buna göre ödemeler matrisi
aşağıdaki gibi düzenlenecektir.

#### Tablo 9.7

| Satır Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En Küçüğü |       |        |
|---------------------------|---------------------------|-----------------|-------|--------|
|                           | Taş                       | Kağıt           | Makas |        |
| Taş                       | 0                         |  -1             |  1    | **-1** |
| Kağıt                     | 1                         |  0              |  -1   | **-1** |
| Makas                     |  -1                       |  1              |  0    | **-1** |
| Sütun En Büyüğü           | **1**                     | **1**           | **1** | -1 1   |

= enb(-1, -1, -1) = -1 = enk(1, 1, 1) = 1 olduğundan oyunun tepe noktası yoktur.
Dolayısıyla oyuncuların sade stratejilerinden söz edilemez.

**9.3.2. Tepe Noktasız Oyunlar ve Karma Stratejiler**

Bir m x n oyunun tepe noktası yoksa, özellikle m ve n’nin büyük değerleri için
çözüm zor olabilir. Genel olarak bir oyunun tepe noktası yoksa oyunu çözmeden
önce mümkünse m ve n değerlerinin küçültülmesi, yani bazı stratejilerin devre
dışı bırakılmaları uygun olur. Bu işlem ancak bazı özel stratejilerin
belirlenmesiyle gerçekleştirilir. Boyut küçültmede kullanılabilecek iki çeşit
strateji vardır: 1. Eş strateji, 2. Üstünlük stratejisi. İlk olarak eş strateji
kavramını ele alalım. Biri diğerine tercih edilemeyen stratejilere "eş strateji"
ler denir. Genel olarak bir oyun matrisinin bir satır/sütunun tüm elemanları
başka bir satır/sütunun karşılıklı elemanlarına eşit ise bu stratejilere eş
stratejiler denir. Eş stratejilerden rasgele seçilen biri dışındakiler matristen
çıkartılarak oyunun çözümü kolaylaştırılır. Boyut indirgenmesi sonucu ulaşılan
çözüm orijinal problemin de çözümüdür.

Boyut indirgenmesine sayısal bir örnek olması bakımından aşağıdaki 4x4 oyunu göz
önüne alalım.

**Örnek 9.7**: Kazanç matrisi aşağıda verilen oyunun eş stratejilerini
belirleyiniz.

**Tablo 9.8**

| Satır Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi |    |    |    |
|---------------------------|---------------------------|----|----|----|
|                           | C1                        | C2 | C3 | C4 |
| R1                        | 1                         | 2  | 3  | 1  |
| R2                        | 3                         | 6  | 1  | 3  |
| R3                        | 0                         | 5  | 4  | 0  |
| R4                        | 1                         | 2  | 3  | 1  |

**Çözüm 9.7**: C1 ve C4 stratejileri için kazançların, bire bir olmak üzere eşit
oldukları görülebilir. Bunlardan biri diğerine tercih edilemez. Bu yüzden biri,
C4 veya C1, göz ardı edilebilir. Bu yolla oyunun boyutu 4x4’den 4x3’e
indirgenmiş olur. Benzer şekilde, R1 ve R4 stratejileri de eş stratejiler
olduklarından biri dışta bırakılarak oyun 3x3 boyutuna indirgenmiş olur.

Oyunda yeğlenen ve stratejilerden bazılarını devre dışı bırakan stratejilere
"üstün stratejiler", bu yolla devre dışı kalan stratejilere ise "mahkum
stratejiler" denir. Genel olarak bir oyunun tepe noktası yoksa, oyunu çözmeden
önce yapılacak ilk iş varsa bütün eş ve mahkum stratejileri devre dışı
bırakmaktır.

**Örnek 9.8**: Aşağıdaki kazanç matrisine sahip oyunun üstün stratejilerini
bulunuz*.*

**Tablo 9.9**

| Satır Oyuncusu  Stratejisi | Sütun Oyuncusu Stratejisi | Satır  En Küçüğü |    |    |     |
|----------------------------|---------------------------|------------------|----|----|-----|
|                            | C1                        | C2               | C3 | C4 |     |
| R1                         |  1                        |  0               | 3  | 1  | 0   |
| R2                         |  7                        | -1               | 6  | 3  | -1  |
| R3                         | -3                        |  0               | 5  | 1  | -3  |
| R4                         |  2                        |  3               | 4  | 5  |  2  |
| Sütun En Büyüğü            | 7                         | 3                | 6  | 5  | 2 3 |

**Çözüm 9.8**: Yukarıdaki tablonun son gözesinde gösterildiği gibi oyunun alt ve
üst değerleri eşit olmadıklarından oyunun tepe noktası yoktur. Bu açıklamanın
ardından oyunun boyutunun indirgenip indirgenemeyeceğini inceleyelim. R1
satırının her elemanı R4 satırının bire bir karşılık gelen her elemanından
küçüktür. Başka bir deyişle, R1 her zaman R4’den daha az kârlıdır. Bu nedenle
satır oyuncusu R1 stratejisini asla kullanmayacaktır. Bu durumda, R4 stratejisi
R1 stratejisine üstündür veya R1 stratejisi R4 stratejisine mahkumdur. Mahkum
strateji R1 göz ardı edildiğinde oyun 3x4 boyutuna indirgenmiş ve oyun matrisi
aşağıdaki gibi belirlenmiş olur.

**Tablo 9.10**

| Satır Oyuncusu  Stratejisi | Sütun Oyuncusu Stratejisi | Satır  En Küçüğü |    |    |        |
|----------------------------|---------------------------|------------------|----|----|--------|
|                            | C1                        | C2               | C3 | C4 |        |
| R2                         |  7                        | -1               | 6  | 3  | -1     |
| R3                         | -3                        |  0               | 5  | 1  | -3     |
| R4                         |  2                        |  3               | 4  | 5  |  **2** |
| Sütun En Büyüğü            | 7                         | **3**            | 6  | 5  | 2 3    |

Diğer taraftan, indirgenmiş matrisin üçüncü sütunun elemanlarının C2 sütununun
karşılıklı elemanlarından büyük olduğu görülebilir. C3, C2’den daha az kazanç
sağladığından sütun oyuncusu C3 stratejisini asla kullanmayacaktır. Bu nedenle
C2 stratejisine mahkum olan C3 devre dışı bırakılmalıdır. Bu yolla bir önceki
aşamada 3x4 boyutuna indirgenen oyun bu elemeyle 3x3 boyutuna indirgenmiş olur.

**Tablo 9.11**

| Satır  Oyuncusu  | Sütun Oyuncusu Stratejisi | Satır En  |    |        |
|------------------|---------------------------|-----------|----|--------|
| Stratejisi       | C1                        | C2        | C4 | Küçüğü |
| R2               |  7                        | -1        | 3  | -1     |
| R3               | -3                        |  0        | 1  | -3     |
| R4               |  2                        |  3        | 5  |  **2** |
| Sütun  En Büyüğü | 7                         | **3**     | 5  | 2 3    |

3x3 boyutuna indirgenen oyunun daha da indirgenip indirgenemeyeceği üzerinde
duralım. Tablo 9.11 incelendiğinde C4 sütun elemanlarının C2 sütununun
karşılıklı elemanlarından büyük olduğu görülebilir. Bu nedenle C4 devre dışı
bırakılmalıdır. Bu elemeyle oyun en basit durumu olan ve Tablo 9.12’de
gösterilen 3x2 boyutuna indirgenmiş olur.

**Tablo 9.12**

| Satır  Oyuncusu  | Sütun Oyuncusu Stratejisi | Satır En  |        |
|------------------|---------------------------|-----------|--------|
| Stratejisi       | C1                        | C2        | Küçüğü |
| R2               |  7                        | -1        | -1     |
| R3               | -3                        |  0        | -3     |
| R4               |  2                        |  3        |  **2** |
| Sütun  En Büyüğü | 7                         | **3**     | 2 3    |

Bilindiği gibi 4x4 boyutundaki orijinal oyun matrisinden alt değer 2, üst değer
3 olarak belirlenmiş ve tepe noktasının olmadığı kararlaştırılmıştır.
İndirgenmiş matrisin yer aldığı tablonun son gözesinde gösterildiği gibi oyunun
alt değeri tekrar 2, üst değerleri yine 3 olarak belirlenmiştir. Özetle
indirgeme oyunun alt ve üst değerlerinde herhangi bir değişikliğe yol
açmamıştır. Bu bir kuraldır.

Daha önce açıklandığı gibi oyunlar arasında tepe noktasız oyunlarla karşılaşmak
daha olağandır. Tepe noktasız bir oyunda, oyuncuların maksimin ve minimaks
stratejileri bulunamayacağına göre oyuncular stratejilerini nasıl seçeceklerdir?

**Örnek 9.9**: Kazanç matrisi aşağıda gösterilen oyunun tepe noktasını
belirleyerek oyuncuların en iyi stratejilerini bulunuz.

**Tablo 9.13**

| Satır  Oyuncusu  | Sütun Oyuncusu Stratejisi | Satır  En |    |    |         |
|------------------|---------------------------|-----------|----|----|---------|
| Stratejisi       | C1                        | C2        | C3 | C4 | Küçüğü  |
| R1               |  10                       | 10        | 8  | 17 |  8      |
| R2               |  17                       | -13       | 26 | 23 | -13     |
| R3               | -30                       | 30        | 25 | 13 | -30     |
| R4               |  24                       | 32        | 14 | 25 |  **14** |
| Sütun En Büyüğü  | **24**                    | 32        | 26 | 25 | 14 24   |

**Çözüm 9.9**: Tablo 9.13’ün son gözesinde gösterildiği gibi oyunun alt değeri
(14) ile üst değeri (24) eşit olmadıklarından oyunun tepe noktası yoktur. Bu
durumda maksimin ve minimaks stratejilerden dolayısıyla, sade stratejilerden söz
edilemez.

**Örnek 9.10**: Kazanç matrisi aşağıda gösterilen oyunun sade stratejilerini
belirleyiniz.

**Tablo 9.14**

| Satır  Oyuncusu  | Sütun Oyuncusu Stratejisi | Satır En  |        |
|------------------|---------------------------|-----------|--------|
| Stratejisi       | C1                        | C2        | Küçüğü |
| R1               | 3                         | 5         | 3      |
| R2               | 6                         | 4         | **4**  |
| Sütun  En Büyüğü | 6                         | **5**     | 4 5    |

**Çözüm 9.10**: Tablo 9.14’ün son gözesinde gösterildiği gibi oyunun tepe
noktası yoktur. Bu durumda sade stratejilerden söz edilemez. Bu nedenle, karma
strateji kavramının açıklanması gerekir.

Karma Strateji: Belirli bir oranda kullanılmış sade stratejilerin rasgele
sıralanışından ibaret birleşik stratejilere karma strateji denir.

Buna göre bir sade strateji, stratejilerden birinin kullanılma olasılığı 1,
ötekilerin kullanılma olasılığı sıfır olan bir karma stratejinin özel bir durumu
olarak düşünülebilir.

Örnek 9.10’daki oyunu oynayan oyuncuların karma stratejilerini belirleyelim.
Soruna önce satır oyuncusu açısından bakalım. Satır oyuncusunun birinci
stratejiyi seçmesi olasılığına p dersek, ikinci stratejiyi seçmesi olasılığı (1
\- p) olur. Satır oyuncusunun amacı kazancını en büyük yapacak p değerini
belirlemektir. p’nin hesaplanmasında izlenen yaklaşım aşağıda açıklanmıştır.

Sütun oyuncusu daima birinci stratejiyi (C1) oynarsa, satır oyuncusunun
kazancının beklenen değeri (E1) aşağıdaki gibi olur.

E1 = 3p + 6(1 - p)

= 3p + 6 - 6p

= 6 - 3p

Sütun oyuncusu daima ikinci stratejiyi (C2) oynarsa, satır oyuncusunun
kazancının beklenen değeri (E2) aşağıdaki gibi elde edilir.

E2 = 5p + 4(1 - p)

= 5p + 4 - 4p

= p + 4

Oyunun her bir tekrarında sütun oyuncusu E1 ve E2’yi daha düşük düzeyde tutacak
stratejiyi seçer. Bu durumda satır oyuncusunun amacı bu en küçük değerleri
mümkün olduğunca büyütmektir. Çözüm, E1 ve E2’nin birlikte çözülmesiyle bulunur.
E1 ve E2’nin eşitlenmesi ve çözülmesiyle p aşağıdaki gibi hesaplanacaktır.

E1 = E2

p + 4 = 6 - 3p

p = 1/2 ve 1 - p = 1/2

Buna göre, oyunun n kez tekrarlanması durumunda oyunun değeri (E1 veya E2’den)
4.5 ((E1 = 1/2 + 4 veya E2 = 6 - 3(1/2)) olarak bulunur. Satır oyuncusu ortalama
4.5 birim kazanmayı umar.

Bulgularımızı şekil üzerinde gösterelim. Bunun için yatay eksen p’yi, dikey
eksen beklenen kazancı göstermek üzere bir koordinat sistemi oluşturalım. p’nin
sıfır ile 1 arasında değiştiği göz önünde bulundurulduğunda ilgilenilen alan p =
0 ve p = 1 dikmeleri (I, II) ile belirlenecektir.

**Şekil 9.1**

Şekil 9.1’den görüldüğü gibi satır oyuncusu için en iyi durum, E1 ve E2
doğrularının belirlediği alt zarfın K ile gösterilen en üst noktasıdır. Satır
oyuncusu E1 = E2 olmasını sağlayan olasılıklardan uzaklaşırsa sütun oyuncusu
oyunun değerinin 4.5’den daha düşük olmasını sağlayacak sade bir stratejiye
sahip olur.

Oyuna bir de sütun oyuncusu açısından bakalım. Sütun oyuncusunun birinci
stratejiyi seçmesi olasılığına q dersek, ikinci stratejiyi seçmesi olasılığı (1
\- q) olur. Sütun oyuncusunun amacı kaybını en küçük yapacak q değerini
belirlemektir. q’nun belirlenmesinde izlenen yaklaşım aşağıda açıklanmıştır.

Satır oyuncusu daima birinci stratejiyi (R1) oynarsa, sütun oyuncusunun kaybının
beklenen değeri (F1) aşağıdaki gibi olur.

F1 = 3q + 5(1 - q)

= 3q + 5 - 5q

= -2q + 5

Satır oyuncusu daima ikinci stratejiyi (R2) oynarsa, sütun oyuncusunun kaybının
beklenen değeri aşağıdaki gibi olur.

F2 = 6q + 4(1 - q)

= 6q - 4q + 4

= 2q + 4

Oyunun her bir tekrarında satır oyuncusu F1 ve F2’yi daha yüksek düzeyde tutacak
stratejiyi seçer. Bu nedenle sütun oyuncusunun amacı, bu en büyük değerleri
mümkün olduğunca küçültmektir. Çözüm, F1 ve F2’nin birlikte çözülmesiyle
bulunur. Çözüm aşağıda gösterilmiştir.

F1 = F2

5 - 2q = 2q + 4

q = 1/4, 1 - q = 3/4

Buradan da g, F1 veya F2’den 4.5 (satır oyuncusu için gerçekleştirilen çözümde
olduğu gibi) olarak bulunur. Bulgularımızı şekil üzerinde gösterelim. Bunun için
yatay eksen q’yu, dikey eksen beklenen kazancı göstermek üzere bir koordinat
sistemi oluşturalım. q’nun 0 ile 1 arasında değiştiği dikkate alındığında
ilgilenilen alan q = 0 ve q = 1 dikmeleri (I, II) ile belirlenecektir.

**Şekil 9.2**

Şekil 9.2’den görüldüğü gibi sütun oyuncusu için en iyi durum F1 ve F2
doğrularının belirlediği üst zarfın en alt noktasıdır. Sütun oyuncusu F1 = F2
olmasını sağlayan olasılıklardan uzaklaşırsa satır oyuncusu oyunun değerinin
daha büyük olmasını sağlayacak sade bir stratejiye sahip olur. Özetle, sütun
oyuncusu grafikte M ile işaretlenen noktadan uzaklaşmamalıdır. Sözgelimi, sütun
oyuncusu C1’i 1/4, C2’yi 3/4 yerine eşit olasılıkla oynarsa satır oyuncusu
oyunun her bir tekrarında ikinci stratejiyi oynayarak rakibinin kendisine olan
ödemesinin 4.5 yerine, F2 = 6(1/2) + 4(1/2) = 10/2 = 5 olmasını sağlar. Özetle,
sütun oyuncusunun amacı F1 ve F2’nin en büyüğünün en küçüklenmesi iken, satır
oyuncusunun amacı E1 ve E2’nin en küçüğünün en büyüklenmesidir. Her iki oyuncu
bunu yaparsa oyunda denge kurulmuş olur.

**Örnek 9.11**: Kazanç matrisi Tablo 9.15’de verilen 2x2 oyunu çözerek
oyuncuların en iyi stratejilerini ve oyunun değerini bulunuz.

**Tablo 9.15**

| Satır  Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En  Küçüğü |        |
|----------------------------|---------------------------|------------------|--------|
|                            | C1                        | C2               |        |
| R1                         |  1                        | -1               | **-1** |
| R2                         | -1                        |  1               | **-1** |
| Sütun  En Büyüğü           | **1**                     | **1**            | -1 1   |

**Çözüm 9.11**: Tablonun son gözesinde gösterildiği gibi oyunun tepe noktası
olmadığından, karma stratejilerin belirlenmesi gerekir. Bu amaçla ilk olarak
satır oyuncusunu ele alalım ve satır oyuncusunun kazancının beklenen değerini
hesaplayalım. Örnek 9.10’da olduğu gibi satır oyuncusunun birinci stratejiyi
kullanması olasılığına p, diğerini seçmesi olasılığına (1 - p) diyelim. Buna
göre, sütun oyuncusu daima birinci stratejiyi kullanırsa satır oyuncusu
aşağıdaki kadar (E1) kazanmayı bekler.

E1 = 1(p) + (-1)(1 - p)

= 2p -1

Sütun oyuncusu hep ikinci stratejiyi oynarsa, satır oyuncusunun kazancı
ortalama,

E2 = -(p) + 1(1 - p)

= -2p + 1

kadar olur. p’nin en iyi değeri E1 = E2’nini çözümünden aşağıdaki gibi
hesaplanır.

2p - 1 = -2p + 1 4p = 2 p = 1/2, (1 - p) = 1/2

p = 1/2 değeri E1 veya E2’ye yerleştirildiğinde g = 0 elde edilecektir.

Benzer şekilde sütun oyuncusunun birinci stratejiyi oynaması olasılığına q,
diğerini oynaması olasılığına (1 - q) dersek, satır oyuncusunun birinci
stratejiyi oynaması durumunda sütun oyuncusunun beklenen kaybı aşağıda
gösterildiği gibi 2q - 1 kadar olur.

F1 = q + (-1)(1 - q)

= q - 1 + q

= 2q - 1

Satır oyuncusunun ikinci stratejiyi oynaması durumunda sütun oyuncusunun
beklenen kaybı,

F2 = -q + (1)(1 - q)

= -q + 1 - q

= -2q + 1

olarak elde edilecektir. q’nun en iyi değeri için F1 = F2 bağıntısının, yani

2q - 1 = -2q + 1

eşitliğinin çözülmesiyle,

q = 1/2, (1 - q) = 1/2

elde edilir. Bu değerler F1 veya F2’ye yerleştirildiklerinde g = 0 olarak
hesaplanacaktır. Şu halde her oyuncu için en iyi strateji sade stratejilerden
her ikisini rasgele kullanmaktır. Fakat stratejiler eşit sayıda kullanılmalıdır.
Oyunun değeri sıfırdır. Bilindiği gibi böyle bir oyuna "insaflı oyun" denir.

**9.3.3. mx2 ve 2xn Oyunların Çözümü**

Önceki kesimde herhangi bir 2x2 oyunun basit bir grafik kullanarak nasıl kolayca
çözülebileceğini açıkladık. Aynı yöntem oyunculardan birinin iki, diğerinin
ikiden fazla stratejisinin bulunduğu oyun problemlerinin çözümünde de
kullanılabilir. Grafik yaklaşımı ile herhangi bir 2xn veya mx2 oyunun 2x2 oyuna
indirgenmesi amaçlanmaktadır. Boyutun 2x2’ye indirgenmesinden sonra problem 2x2
durumunda olduğu gibi çözülebilmektedir. Önce satır oyuncusunun R1 ve R2 olmak
üzere iki, sütun oyuncusunun ise C1, C2, ..., Cn olmak üzere n stratejisinin
bulunduğu yani, 2xn boyutundaki bir oyunu çözelim. 2xn durumunda sütun
oyuncusunun n stratejisi n tane doğru tanımlar. 2x2 durumunda olduğu gibi oyunun
çözümü bu doğruların belirlediği alt zarfın en üst noktasında ortaya çıkar.
Oyunun çözümü bu noktanın ordinat ve absisini kullanarak doğrudan bulunabilir.
Çözümün belirlenmesinde kullanılabilecek bir başka yaklaşım şudur: Oyunun
çözümünün ortaya çıktığı noktada kesişen Ci ve Ck gibi bir strateji çifti daima
vardır. Eğer bu noktada ikiden fazla strateji kesişiyorsa, bunlardan herhangi
ikisi rasgele seçilir. Seçilen bu stratejiler sütun oyuncusunun karma
stratejisini oluşturur. Satır oyuncusunun iki stratejisi bulunduğundan ve sütun
oyuncusunun strateji sayısı ikiye indirgendiğinden oyunun boyutu artık 2xn değil
2x2 dir. 2x2 oyunun çözümü aynı zamanda orijinal 2xn oyunun da çözümüdür.

2xn oyunların çözümüne örnek olması bakımından aşağıdaki 2x4 oyunu çözelim.

**Örnek 9.12**: Kazanç matrisi aşağıda verilmiş olan 2x3 oyunu çözünüz.

**Tablo 9.16**

| Satır  Oyuncusu  | Sütun Oyuncusu Stratejisi | Satır  En |    |       |        |
|------------------|---------------------------|-----------|----|-------|--------|
| Stratejisi       | C1                        | C2        | C3 | C4    | Küçüğü |
| R1               | -6                        | 4         | 3  | 5     | -6     |
| R2               | 6                         | 5         | 6  | -5    | **-5** |
| Sütun En Büyüğü  | 6                         | **5**     | 6  | **5** | -5 5   |

**Çözüm 9.12**:  (= -5) (= 5) olduğundan oyunun tepe noktası yoktur. Bu yüzden
çözüm bir karma strateji çifti olacaktır. Şimdi karma strateji çiftini
belirleyelim. Oyunun çözümünü strateji sayısı 2 olan satır oyuncusuyla
başlatalım. Önceden olduğu gibi R1’in seçilmesi olasılığını p, R2’nin seçilmesi
olasılığını (1 - p) ile gösterdiğimizde, sütun oyuncusunun C1 stratejisine
karşılık satır oyuncusunun beklenen kazancı aşağıdaki gibi olur.

C1 için, E1 = -6p + 6(1 - p)

= -6p + 6 - 6p

= -12p + 6

Diğer taraftan sütun oyuncusunun C2’yi seçmesi durumunda satır oyuncusunun
beklenen kazancı aşağıdaki gibi belirlenecektir.

C2 için, E2 = 4p + 5(1 - p)

= 4p + 5 - 5p

= -p + 5

Benzer şekilde, sütun oyuncusunun C3, C4 strateji seçimlerine karşılık satır
oyuncusunun beklenen kazançları aşağıdaki gibi elde edilecektir.

C3 için, E3 = 3p + 6(1 - p) C4 için, E4 = 5p - 5(1 - p)

= 3p + 6 - 6p = 5p -5 + 5p

= -3p + 6 = 10p - 5

Sütun oyuncusunun strateji seçimine bağlı olarak belirlenen kazançların her biri
bir doğru tanımlar. Oyunun çözümü için önce bu doğruların çizilmesi gerekir.
Doğruların çizilmesinin ardından istenen çözüm kolayca belirlenir. Oyunun
grafiği Şekil 9.3’de gösterilmiştir.

**Şekil 9.3**

C1, C2, C3 ve C4 ile gösterilen doğrular sütun oyuncusunun stratejilerine
karşılık gelmektedir. p’nin her bir değeri için doğruların o noktadaki
yüksekliği sütun oyuncusunun ödemesini gösterir.

Herhangi bir Cj stratejisi için en küçük kazancın en büyük olacağı bir karma
strateji bulmak istediğimize göre, C1, C2, C3, C4 stratejileri için bir alt
sınır çizeriz. Şekil 9.3’de bu alt sınır kalın çizilmiş AKB kırık çizgisidir.

Bu durumda sütun oyuncusunun en iyi stratejisi, alt sınırın en üst noktası olan
K’da kesişen C1 ve C4 sade stratejilerinin bir karması olur. K’nın yatay eksene
olan uzaklığının değeri (burada sıfır) oyunun değerine eşittir.

C2, C3 stratejileri devre dışı kaldığından oyun, 2x2 boyutuna indirgenmiş olur.
Şimdi bu 2x2 oyunu çözerek önce satır oyuncusunun karma stratejisini
belirleyelim. Mahkum stratejilerin devre dışı bırakılmasıyla elde edilen
indirgenmiş oyunun kazanç matrisi aşağıda gösterilmiştir.

**Tablo 9.17**

| Satır  Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En  Küçüğü |        |
|----------------------------|---------------------------|------------------|--------|
|                            | C1                        | C4               |        |
| R1                         | -6                        | 5                | -6     |
| R2                         | 6                         | -5               | **-5** |
| Sütun  En Büyüğü           | 6                         | **5**            | -5 5   |

Oyunu satır oyuncusu için çözelim: Satır oyuncusunun R1’i seçme olasılığı p,
R2’yi seçme olasılığı (1 - p) olduğuna göre, sütun oyuncusunun C1 ve C4
stratejilerine karşılık satır oyuncusunun beklenen kazancı sırasıyla şöyle
olacaktır.

C1 için, E1 = -6p + 6(1 - p)

= -6p + 6 - 6p

= -12p + 6

C4 için, E4 = 5p - 5(1 - p)

= 5p - 5 + 5p

= 10p - 5

E1 = E4 bağıntısından, p = 1/2, (1 - p) = 1/2 bulunur. p = 1/2’nin E1 veya E4’e
yerleştirilmesiyle g = 0 olduğu yani, oyunun insaflı olduğu belirlenir.

Oyuncuların karma stratejileri genellikle bir satır vektörle gösterilir. Satır
oyuncusunun karma strateji vektörü **p** = (p1, p2, ..., pm), sütun
oyuncusununki **q** = (q1, q2, ..., qn) şeklindedir. Buna göre, Örnek 9.10’daki
satır oyuncusunun karma strateji vektörü, **p** = (1/2, 1/2) olur.

Şimdi de sütun oyuncusunun C1 ve C4 stratejilerini seçme olasılıklarını bulalım.
C1’in seçilme olasılığına q dersek, C4’ün seçilme olasılığı (1 - q) olur. Buna
göre satır oyuncusunun strateji seçimine bağlı olarak sütun oyuncusunun beklenen
kazancı şöyle olur:

R1 için, F1 = -6q + 5(1 - q) R2 için, F2 = 6q - 5(1 - q)

= -6q + 5 - 5q = 6q - 5 + 5q

= -11q + 5 = 11q - 5

F1 = F2 bağıntısından, -11q + 5 = 11q – 5 elde edilecektir. Eşitliğin
çözülmesiyle q = 5/11, (1 - q) = 6/11 olarak elde edilir. q = 5/11 değerinin F1
veya F2’ye yerleştirilmesiyle, g = 0 bulunur. Buna göre, sütun oyuncusunun karma
strateji vektörü **q** = (5/11, 0, 0, 6/11) olur.

Satır oyuncusunun m, sütun oyuncusunun iki stratejisinin bulunduğu bir mx2 oyun
için problem tamamen 2xn oyuna benzer şekilde çözülebilir. Yalnızca bu kez,
kazançların alt sınırı yerine üst sınırının çizilmesi gerektiği unutulmamalıdır.

Ayrıca oyunun değerini veren nokta üst sınır üzerinde en aşağıdaki noktadır. mx2
oyunların çözümüne örnek olarak matrisi aşağıda gösterilen 4x2 oyunu göz önüne
alalım.

**Örnek 9.13**: Bir 4x3 oyunun kazanç matrisi aşağıda verilmiştir. Oyunu grafik
yöntemiyle çözerek oyuncuların strateji seçimlerini ve oyunun değerini bulunuz.

**Tablo 9.18**

| Satır Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En  Küçüğü |        |
|---------------------------|---------------------------|------------------|--------|
|                           | C1                        | C2               |        |
| R1                        | 3                         | 4                |  **3** |
| R2                        | 2                         | 4                |  2     |
| R3                        | 6                         | 2                |  2     |
| R4                        | 4                         | -2               | -2     |
| Sütun  En Büyüğü          | 6                         | **4**            | 3 4    |

**Çözüm 9.13**: Oyunun alt değeri 3, üst değeri 4 olduğundan, tepe noktası
yoktur. Bu yüzden çözüm bir karma strateji çifti olacaktır. Strateji sayısı iki
olan oyuncu sütun oyuncusu olduğundan çözüm bu oyuncunun stratejileri ile
başlatılır. Sütun oyuncusunun C1’i seçme olasılığına q dersek, C2’yi seçme
olasılığı (1 - q) olur. Buna göre satır oyuncusunun R1, R2, R3 ve R4 strateji
seçimlerine bağlı olarak sütun oyuncusunun beklenen kazancı şöyledir:

R1 için, F1 = 3q + 4(1 - q) R2 için, F2 = 2q + 4(1 - q)

= 3q + 4 - 4q = 2q + 4 - 4q

= -q + 4 = -2q + 4

R3 için, F3 = 6q + 2(1 - q) R4 için, F4 = 4q - 2(1 - q)

= 6q + 2 - 2q = 4q - 2 + 2q

= 4q + 2 = 6q - 2

Yukarıdaki gibi belirlenen beklenen kazançların temsil ettikleri doğrular Şekil
9.4’deki gibi çizilmiştir. Şekil 9.4’de gösterildiği gibi oyunun çözümü
kazançların üst sınırı (kalın çizgiyle çizilmiş) ile belirlenen üst zarfın alt
noktasında ortaya çıkar.

**Şekil 9.4**

K ile gösterilen noktanın yatay eksene olan uzaklığının oyunun değerine eşit
olduğu bilinmektedir. K, R3 ve R1 stratejilerine karşı gelen doğrularla
belirlendiğinden, satır oyuncusu oyunu R2 ve R4 stratejilerini devre dışı
bırakarak oynayacaktır. Bu stratejilerin devre dışı bırakılmasıyla, 4x2oyun 2x2
oyuna dönüştürülmüştür. 2x2 oyunun kazanç matrisi Tablo 9.19’da gösterilmiştir.

**Tablo 9.19**

| Satır  Oyuncusu Stratejisi | Sütun Oyuncusu Stratejisi | Satır En  Küçüğü |       |
|----------------------------|---------------------------|------------------|-------|
|                            | C1                        | C2               |       |
| R1                         | 3                         | 4                | **3** |
| R3                         | 6                         | 2                | 2     |
| Sütun  En Büyüğü           | 6                         | **4**            | 3 4   |

Şimdi bu basit oyunu çözelim. Satır oyuncusunun stratejisine bağlı olarak sütun
oyuncusunun beklenen kazancı aşağıdaki gibi elde edilir.

R1 için, F1 = 3q + 4(1 - q) R3 için, F3 = 6q + 2(1 - q)

= -q + 4 = 4q + 2

F1 = F3 bağıntısından q = 2/5, 1 - q = 3/5 olarak hesaplanır. q = 2/5 olduğu göz
önünde bulundurulduğunda, g = 18/5 olur.

Benzer şekilde, sütun oyuncusunun strateji seçimine bağlı olarak satır
oyuncusunun kazancı aşağıdaki gibi olur.

C1 için, E1 = 3p + 6(1 - p) C2 için, E2 = 4p + 2(1 - p)

= -3p + 6 = 2p + 2

Bu iki kazancın eşit oldukları dikkate alındığında satır oyuncusunun strateji
seçimine ilişkin olasılıklar, p = 4/5, (1 - p) = 1/5, g = 18/5 olarak
belirlenir.

**9.3.4. mxn Oyunların Doğrusal Programlama İle Çözümü**

Şimdiye kadar, oyunculardan en az birinin iki stratejisinin bulunduğu oyunların
çözümü üzerinde durulmuştur. Genel olarak, oyuncuların strateji sayıları
büyüdükçe oyunun çözümü güçleşir. Artan güçlük kesinlikle teoride değil işlem
sayısının hızla artmasındadır. Orjinalinde 2xn veya mx2 olmayan ya da bu
boyutlardan birine indirgenemeyen mxn oyunlar doğrusal programlama ile
çözülürler. Bilindiği gibi bir mxn oyunda satır oyuncusunun R1, R2, ..., Rm gibi
m stratejisi, rakibinin C1, C2, ..., Cn gibi n stratejisi vardır ve oyunun
kazanç matrisi aşağıdaki gibi tablolanır.

**Tablo 9.20**

| Satır   Oyuncusu Stratejisi |  Sütun Oyuncusu Stratejisi |     |     |     |     |     |
|-----------------------------|----------------------------|-----|-----|-----|-----|-----|
|                             | C1                         | C2  | ... | Cj  | ... | Cn  |
| R1                          | a11                        | a12 | ... | a1j | ... | a1n |
| R2                          | a21                        | a22 | ... | a2j | ... | a2n |
| ..                          | ..                         | ..  | ... | ..  | ... | ..  |
| Ri                          | ai1                        | ai2 | ... | aij | ... | ain |
| ..                          | ..                         | ..  | ... | ..  | ... | ..  |
| Rm                          | am1                        | am2 | ... | amj | ... | amn |

Oyunun tepe noktasının bulunmadığı kabul edildiğinden her iki oyuncu oyunu karma
stratejileri ile sürdürecektir. Önce satır oyuncusunu dikkate alalım ve problemi
onun bakış açısıyla çözelim. Satır oyuncusunun stratejilerini p1, p2, ..., pm ()
olasılıkları ile seçtiğini düşünelim. Buna göre sütun oyuncusunun C1, C2, ...,
Cn strateji seçimlerine bağlı olarak satır oyuncusunun beklenen kazancı
aşağıdaki denklem sistemiyle açıklanır.

C1 için: E1 = a11p1 + a21p2 + ... + am1pm

C2 için: E2 = a12p1 + a22p2 + ... + am2pm

... ... ... ... ... ...

Cn için: Em = a1np1 + a2np2 + ... + amnpm

Satır oyuncusunun hedefi, rakibinin strateji seçimi ne olursa olsun, en küçük
kazancını en büyüklemek olduğundan bu oyuncu oyunun en küçük değerini en
büyüklemek ister. Çünkü, satır oyuncusu kazancını en az oyunun değerine eşit
kılmak ister. Buna göre satır oyuncusu açısından problem aşağıdaki gibi
modellenir.

Zenb = g

a11p1 + a21p2 + ... + am1pm g

a12p1 + a22p2 + ... + am2pm g

... ... ... ...

a1np1 + a2np2 + ... + amnpm g

p1 + p2 + ... + pm = 1

pi 0 (i = 1, 2, ..., m)

Oyunun değeri önceden bilinmemekle birlikte pozitif olduğu kabul edilecektir.
Yukarıdaki modelin doğrusal programlama ile çözülebilmesi için kısıtlayıcı
fonksiyonların sağ taraf sabitleri bilinen değerlere dönüştürülmelidir. Bunu
sağlamanın tek yolu, kısıtlayıcı fonksiyonların her birinin g’ye bölünmesidir.
Bölme işlemiyle ortaya çıkan değişkenleri aşağıdaki gibi tanımlayalım.

x1 = p1/g, x2 = p2/g, ..., xm = pm/g

Buradaki xi’ler negatif olmayan sayılardır. p1 + p2 + ... + pm = 1 bağıntısının
dikkate alınmasıyla, x1 + x2 + ... + xm = 1/g elde edilir.

Satır oyuncusunun garanti edilmiş kazancı olan g’nin en büyüklenmesi için,
1/g’nin en küçüklenmesi gerekir.

Buna göre bir m x n oyunun çözümünü bulma problemi, aşağıdaki doğrusal
programlama probleminin çözülmesine indirgenmiş olur.

Zenk = 1/g = x1 + x2 + ... + xm

a11x1 + a21x2 + ... + am1xm 1

a12x1 + a22x2 + ... + am2xm 1

... ... ... ...

a1nx1 + a2nx2 + ... + amnxm 1

x1, x2, ..., xm 0

Problemin doğrusal programlamanın klasik çözüm yöntemi simpleks tekniğiyle
çözümüyle belirlenen xi (i =1, 2, ..., m) değerlerinin xi = pi/g’de yerine
konulmasıyla satır oyuncusunun en iyi karma stratejisi bulunmuş olur.

Simpleks yöntemle belirlenen Z değerinin (1/g)’ye eşit olduğu unutulmamalıdır.
Sütun oyuncusunun problemi, satır oyuncusu için türetilen doğrusal programlama
modelinin duali olarak yorumlanabilir. Yani, problem satır oyuncusu için
çözüldüğünde primal-dual ilişkileri kullanılarak sütun oyuncusunun karma
stratejisi belirlenebilir. Bununla birlikte istenirse, problem sütun oyuncusu
bakımından doğrusal programlama modeli olarak formüllenebilir.

Bir m x n oyunun doğrusal programlama ile çözümünü bir de sütun oyuncusu
bakımından ele alalım. Sütun oyuncusunun stratejilerini sırasıyla, q1, q2, ...,
qn () olasılıkları ile seçtiğini düşünelim.

Buna göre satır oyuncusunun strateji seçimine bağlı olarak sütun oyuncusunun
beklenen kazancı,

R1 için: F1 = a11q1 + a12q2 + ... + a1nqn

R2 için: F2 = a21q1 + a22q2 + ... + a2nqn

... ... ... ... ... ...

Rm için: Fn = am1q1 + am2q2 + ... + amnqn

olarak formüllenir.

Sütun oyuncusunun amacı rakibinin strateji seçimi ne olursa olsun en büyük
kaybını en küçüklemektir. Bunun için sütun oyuncusu kaybının en fazla oyunun
değerine eşit olmasını ister. Buna göre, sütun oyuncusunun problemi aşağıdaki
gibi formüllenir.

Zenk = g

a11q1 + a12q2 + ... + a1nqn g

a21q1 + a22q2 + ... + a2nqn g

... ... ... ...

am1q1 + am2q2 + ... + amnqn g

q1 + q2 + ... + qn = 1

qj 0 j = 1, 2, ..., n

Kısıtlayıcıların sağ taraf sabitlerinin negatif olmamalarını sağlamak için,
önceden olduğu gibi, g’nin pozitif bir sayı olduğunu kabul edeceğiz. Kısıtlayıcı
fonksiyonları uygun şekle dönüştürmek için g ile böler,

y1 = q1/g, y2 = q2/g, ..., yn = qn/g

tanımlarsak, sütun oyuncusu için doğrusal programlama problemi aşağıdaki gibi
olur.

Zenb = 1/g = y1 + y2 + ... + yn

a11y1 + a12y2 + ... + a1nyn 1

a21y1 + a22y2 + ... + a2nyn 1

... ... ... ...

am1y1 + am2y2 + ... + amnyn 1

y1, y2, ..., yn 0

Dönüştürülmüş problemin çözüm sonuçları olan yj değerleri yj = qn/g bağıntısına
yerleştirildiğinde orijinal problem çözülmüş, yani q değerleri belirlenmiş olur.

Problem sütun oyuncusu için çözüldüğünde primal-dual ilişkileri kullanılarak
satır oyuncusunun karma stratejisi belirlenebilir.

Konuyla ilgili sayısal bir örnek vermeden önce, oyunun değerinin pozitif kabul
edilmesinin doğru olup olmadığı üzerinde duralım.

aij’lerden bazılarının negatif olması durumunda oyunun değeri (g) pozitif
olmayabilir. Bu gibi durumlarda oyun matrisinin her elemanına aij’lerin tümünün
pozitif olmasını sağlayacak bir L sabiti eklenebilir. Bu durumda oyunun değeri L
kadar artar, fakat çözüm aynı kalır. L’nin eklenmesiyle belirlenen oyun
değerinden L’nin çıkartılmasıyla da orijinal oyunun değeri belirlenir.

**Örnek 9.14**: Kazanç matrisi aşağıda verilen 3x3 oyunu doğrusal programlama
olarak formülleyerek simpleks yöntemle çözünüz*.*

**Tablo 9.21**

| Satır  Oyuncusu  | Sütun Oyuncusu Stratejisi | Satır En  |    |        |
|------------------|---------------------------|-----------|----|--------|
| Stratejisi       | C1                        | C2        | C3 | Küçüğü |
| R1               | -2                        |  6        | 3  | -2     |
| R2               |  3                        | -4        | 7  | -4     |
| R3               | -1                        |  2        | 4  | **-1** |
| Sütun  En Büyüğü | **3**                     | 6         | 7  | -1 3   |

**Çözüm 9.14**: Doğrusal programlama ile çözüme geçmeden önce matrisin negatif
elemanlarını pozitif değerlere dönüştürmek için kazanç matrisinin her bir
elemanına L = 4 ekleyelim. Tablo 9.21’deki kazanç matrisinin her bir değerine 4
eklenmesiyle problemin orijinal kazanç matrisi, Tablo 9.22’deki gibi olur. Bu
ekleme oyunun değerini 4 artırır ama çözümü değiştirmez.

**Tablo 9.22**

| Sütun  Oyuncusu Stratejisi | Satır Oyuncusu  Stratejisi | Satır En  Küçüğü |    |       |
|----------------------------|----------------------------|------------------|----|-------|
|                            | C1                         | C2               | C3 |       |
| R1                         | 2                          | 10               | 7  | 2     |
| R2                         | 7                          | 0                | 11 | 0     |
| R3                         | 3                          | 6                | 8  | **3** |
| Sütun  En Büyüğü           | **7**                      | 10               | 11 | 3 7   |

Oyunu önce satır oyuncusu için çözelim. Bu oyuncunun doğrusal programlama
formülasyonu aşağıda gösterilmiştir.

Zenk = 1/g = x1 + x2 + x3

2x1 + 7x2 + 3x3 1

10x1 + 0x2 + 6x3 1

7x1 + 11x2 + 8x3 1

x1, x2, x3 0

Burada g oyunun değeri ve xi = pi/g olarak tanımlanmıştır.

Simpleks çözüm için artık ve yapay değişkenlerin modele sokulması ile,

Zenk = x1 + x2 + x3 + 0x4 + 0x5 + 0x6 + MA1 + MA2 + MA3

2x1 + 7x2 + 3x3 - x4 + A1 = 1

10x1 + 0x2 + 6x3 - x5 + A2 = 1

7x1 + 11x2 + 8x3 - x6 + A3 = 1

x1, x2, x3, x4, x5, x6, A1, A2, A3 0

elde edilir.

Problemin başlangıç çözüm tablosu aşağıda gösterilmiştir.

**Tablo 9.23**

| TDV     | x1     | x2    | x3    | x4 | x5 | x6 | A1 | A2 | A3 | ÇV |
|---------|--------|-------|-------|----|----|----|----|----|----|----|
| A1      |  2     |  7    | 3     | -1 |  0 |  0 | 1  | 0  | 0  | 1  |
| A2      | **10** |  0    | 6     |  0 | -1 |  0 | 0  | 1  | 0  | 1  |
| A3      |  7     | 11    | 8     |  0 |  0 | -1 | 0  | 0  | 1  | 1  |
| Zj      | 19M    | 18M   | 17M   | -M | -M | -M | M  | M  | M  | 3M |
| Zj - Cj | 19M-1  | 18M-1 | 17M-1 | -M | -M | -M | 0  | 0  | 0  | -  |

Z1 - C1 = 19M-1 \> Z2 - C2 = 18M - 1, Z3 - C3 = 17M - 1 olduğundan, x1’in temele
alınması, A2 temelden çıkartılması ve bilinen işlemlerin uygulanmasıyla yeni
çözüm tablosu aşağıdaki gibi belirlenmiş olur.

**Tablo 9.24**

| TDV     | x1 | x2     | x3   | x4 | x5    | x6 | A1 | A2    | A3 | ÇV   |
|---------|----|--------|------|----|-------|----|----|-------|----|------|
| A1      | 0  | 7      | 9/5  | -1 | 1/5   | 0  | 1  | -1/5  | 0  | 4/5  |
| x1      | 1  | 0      | 3/5  | 0  | -1/10 | 0  | 0  | 1/10  | 0  | 1/10 |
| A3      | 0  | **11** | 19/5 | 0  | 7/10  | -1 | 0  | -7/10 | 1  | 1/3  |
| Zj      | 1  | 18M    |      | -M |       | -M | M  |       | M  |      |
| Zj - Cj | 0  | 18M-1  |      | -M |       | -M | 0  |       | 0  | -    |

Z2 - C2 = 18M - 1 \> Z3 - C3, Z5 - C5 olduğundan x2’nin temele alınması, A3’ün
temelden çıkartılması ve anahtar işlemlerin uygulanmasıyla, aşağıdaki yeni çözüm
tablosu elde edilir.

**Tablo 9.25**

| TDV     | x1 | x2 | x3     | x4 | x5      | x6       | A1 | A2     | A3    | ÇV     |
|---------|----|----|--------|----|---------|----------|----|--------|-------|--------|
| A1      | 0  | 0  | -34/55 | -1 | -27/110 | **7/11** | 1  | 27/110 | -7/11 | 67/110 |
| x1      | 1  | 0  | 3/5    | 0  | -1/10   | 0        | 0  | 1/10   | 0     | 1/10   |
| x2      | 0  | 1  | 19/55  | 0  | 7/110   | -1/11    | 0  | -7/10  | 1/11  | 3/110  |
| Zj      | 1  | 1  |        | -M |         |          | M  |        |       |        |
| Zj - Cj | 0  | 0  |        | -M |         |          | 0  |        |       | -      |

Z6 - C6 \> 0 olduğundan x6 temele alınır. A1’in temelden çıkartılması ve
simpleks yöntemin bilinen işlemleriyle yeni çözüm aşağıdaki gibi elde edilir.

## Tablo 9.26

| TDV      | x1 | x2 | x3     | x4    | x5     | x6 | A1   | A2    | A3 | ÇV    |
|----------|----|----|--------|-------|--------|----|------|-------|----|-------|
| x6       | 0  | 0  | -34/35 | -11/7 | -27/70 | 1  | 11/7 | 27/70 | -1 | 67/70 |
| x1       | 1  | 0  | 3/5    | 0     | -1/10  | 0  | 0    | 1/10  | 0  | 1/10  |
| x2       | 0  | 1  | 9/35   | -1/7  | 1/35   | 0  | 1/7  | -1/35 | 0  | 4/35  |
| Zj       | 1  | 1  | 6/7    | -1/7  | -1/14  | 0  | 1/7  | 1/14  | 0  | 3/14  |
| Z j - Cj | 0  | 0  | -1/7   | -1/7  | -1/14  | 0  |      |       | -M | -     |

Tüm Zj - Cj 0 olduğundan yürürlükteki çözüm en iyidir. En iyi çözümün yer aldığı
tablodan görüldüğü gibi, x1 = 1/10, x2 = 4/35, x3 = 0’dır.

Bu çözüm kümesi, satır oyuncusunun en iyi stratejisinin belirlenmesinde
kullanılacaktır. Zenk = 3/14 olduğu dikkate alındığında, 1/g = 3/14
bağıntısından, g = 14/3 = 4.666 bulunur. Bu arada, orijinal oyun matrisinin tüm
elemanlarına 4 eklendiği bu yüzden, oyunun asıl değerinin g = 0.666 (= 4.666 -
4) olduğu unutulmamalıdır. Bu çözüm sonuçlarının kullanılmasıyla satır
oyuncusunun strateji seçim olasılıkları aşağıdaki gibi hesaplanır.

p1 = x1 g bağıntısından, p1 = == 0.466

p2 = x2g bağıntısından,

p3 = x3g bağıntısından,

Buna göre satır oyuncusu %46.66 oranında R1 stratejisini, %53.33 oranında R2
stratejisini oynarsa, rakibinin kabul edebileceği düzeyde bir oyun değeri
belirlemiş olacaktır.

Aynı oyunu bir de sütun oyuncusu için çözelim. Yukarıdaki açıklamalar
doğrultusunda sütun oyuncusunun doğrusal programlama formülasyonu aşağıdaki gibi
düzenlenecektir.

Zenb = 1/g = y1 + y2 + y3

2y1 + 10y2 + 7y3 1

7y1 + 0y2 + 11y3 1

3y1 + 6y2 + 8y3 1

y1, y2 ,y3 0

Burada oyunun değeri (g), yi = qi/g olarak tanımlanmıştır.

Problemin simpleks yöntemin gerektirdiği standart biçimi aşağıdadır.

Zenb = y1 + y2 + y3 + 0y4 + 0y5 + 0y6

2y1 + 10y2 + 7y3 + y4 = 1

7y1 + 11y3 + y5 = 1

3y1 + 6y2 + 8y3 + y6 = 1

y1, y2, y3, y4, y5, y6 0

Düzenlenmiş bu modeldeki y4, y5, y6 değişkenleri başlangıç uygun temel çözümdeki
değişkenlerdir. Buna göre düzenlenen simpleks başlangıç çözüm tablosu aşağıda
gösterilmiştir.

**Tablo 9.27**

| TDV     | y1    | y2 | y3 | y4 | y5 | y6 | ÇV |
|---------|-------|----|----|----|----|----|----|
| y4      | 2     | 10 | 7  | 1  | 0  | 0  | 1  |
| y5      | **7** | 0  | 11 | 0  | 1  | 0  | 1  |
| y6      | 3     | 6  | 8  | 0  | 0  | 1  | 1  |
| Zj      | 0     | 0  | 0  | 0  | 0  | 0  | 0  |
| Zj - Cj | -1    | -1 | -1 | 0  | 0  | 0  | -  |

Simpleks yöntemin temel kurallarının uygulanmasıyla elde edilen simpleks çözüm
tabloları aşağıda sırasıyla gösterilmiştir.

**Tablo 9.28**

| TDV     | y1 | y2     | y3   | y4 | y5   | y6 | ÇV  |
|---------|----|--------|------|----|------|----|-----|
| y4      | 0  | **10** | 27/7 | 1  | -2/7 | 0  | 5/7 |
| y1      | 1  | 0      | 11/7 | 0  | 1/7  | 0  | 1/7 |
| y6      | 0  | 6      | 23/7 | 0  | -3/7 | 1  | 4/7 |
| Zj      | 1  | 0      | 11/7 | 0  | 1/7  | 0  | 1/7 |
| Zj - Cj | 0  | -1     | 4/7  | 0  | 1/7  | 0  | -   |

**Tablo 9.29**

| TDV     | y1 | y2 | Y3     | y4   | y5    | y6 | ÇV   |
|---------|----|----|--------|------|-------|----|------|
| y2      | 0  | 1  | 27/70  | 1/10 | -1/35 | 0  | 1/14 |
| y1      | 1  | 0  | 11/7   | 0    | 1/7   | 0  | 1/7  |
| y6      | 0  | 0  | 34/35  | -3/5 | -9/35 | 1  | 1/7  |
| Zj      | 1  | 1  | 137/70 | 1/10 | 4/35  | 0  | 3/14 |
| Zj - Cj | 0  | 0  | 67/70  | 1/10 | 4/35  | 0  | -    |

Tablo 9.29’dan görüldüğü gibi, tüm Zj - Cj 0 olduğundan çözüm en iyidir. Bu
çözümde; y1 = 1/7, y2 = 1/14, y3 = 0’dır. Bu çözüm kümesi sütun oyuncusunun
strateji vektörünün belirlenmesinde kullanılacaktır.

Zenb = 3/14 olduğunun dikkate alınmasıyla, 1/g = 3/14 bağıntısından oyunun
değeri önceki çözüm sürecindeki gibi g = 14/3 = 4.666 bulunur. Oyunun asıl
değerinin 0.666 olduğunu bir kez daha hatırlayalım.

q1 = y1g, q2 = y2g, q3 = y3g bağıntılarından q1, q2, q3 aşağıdaki gibi
hesaplanır.

Buna göre, sütun oyuncusu %66.66 oranında birinci, %33.33 oranında ikinci
stratejisini oynarsa, rakibinin (satır oyuncusunun) ikna olacağı bir düzeyde
oyunun değerini belirlemiş olacaktır. Bu değer g = 0.666 (= 4.666 - 4)’dır.

Görüldüğü gibi problem her iki oyuncu için ayrı ayrı çözülmüştür. Oysa, daha
önce açıklandığı gibi, problem oyunculardan biri için çözüldüğünde diğeri için
de çözülmüş olur. Çünkü satır oyuncusunun problemi primal kabul edildiğinde
sütun oyuncusunun problemi dual olur. Bunun tersi de doğrudur. Primal problemin
çözümünden dual problemin çözümünün veya tersi dual problemin çözümünden primal
problemin çözümünün elde edilebileceği göz önünde bulundurulduğunda problemin
oyunculardan biri için çözülmesinin yeterli olacağı anlaşılır. Buna göre, önce
satır oyuncusu için belirlenen çözümden hareketle sütun oyuncusunun çözümünü
belirleyelim.

Tablo 9.26’nın artık değişkenlerine ait Zj - Cj değerleri dual değişkenlerin
değerlerini (M’nin göz ardı edilmesi koşuluyla) vereceğinden problem sütun
oyuncusu için de çözülmüş olur. Buna göre,

Z7 - C7 = 1/7’den y1 = 1/7

Z8 - C8 = 1/14’den y2 = 1/14

Z9 - C9 = 0’dan y3 = 0

olarak belirlenecektir. Bu durumda yapılacak tek şey y1, y2, y3 için belirlenen
değerleri , q1 = y1g, q2 = y2g, q3 = y3g bağıntılarına yerleştirip gerekli
aritmetik işlemleri gerçekleştirmektir.

Şimdi de sütun oyuncusunun çözümünden hareketle satır oyuncusunun çözümünü elde
edelim. Sütun oyuncusunun en iyi çözümünün bulunduğu Tablo 9.29’un aylak
değişkenlerine ait Zj - Cj değerleri satır oyuncusunun değişken değerlerini
verecektir. Buna göre, x1, x2, x3 aşağıdaki gibi hesaplanır.

Z4 - C4 = 1/10’dan x1 = 1/10

Z5 - C5 = 4/35’den x2 = 4/35

Z6 - C6 = 0’dan x3 = 0

Bu değerlerin p1 = x1g, p2 = x2g, p3 = x3g bağıntılarına yerleştirilip gerekli
işlemlerin yapılmasıyla satırdaki oyuncunun karma stratejisi belirlenmiş olur.

Özetle, problem oyunculardan biri için çözüldüğünde diğer oyuncu için de
çözülmüş olacağından problemin her iki oyuncu için ayrı ayrı çözülmesine gerek
yoktur. Kuşkusuz, kısıtlayıcı fonksiyonları biçiminde olan en büyükleme amaçlı
doğrusal programlama probleminin standartlaştırılmasında daha az değişken
kullanıldığından, sütun oyuncusuna öncelik verilmesi uygun olur.

## 9.4. İKİ KİŞİLİ SABİT TOPLAMLI OYUNLAR

İki-kişili sabit-toplamlı bir oyunda oyuncuların kazançları toplamı c (c 0)
sabitine eşittir. Genel olarak iki-kişili sabit-toplamlı oyunlar iki-kişili
sıfır-toplamlı oyunların çözümünde kullanılan yöntemlerle çözülür.

**Örnek 9.15**: Yörede yayın yapan iki TV kanalı vardır. 20:00-21:00 saatleri
arasında tam 50 milyon kişi bu iki kanalı izlemektedir. Kanallar 20:00-21:00
saatleri arasında yapacakları yayının türünü önceden aynı anda anons etmek
zorundadırlar. Yayın türünün sonradan değiştirilmesi mümkün değildir. Kanalların
mümkün seçimleri ve birinci kanalı seyredeceklerin sayısı Tablo 9.30’da
verilmiştir. Oyunun tepe noktası bulunup bulunmadığını ve birinci kanal için
oyunun değerini bulunuz.

### Tablo 9.30

| Kanal 1 Yayın Türü | Kanal 2 Yayın Türü | Satır En Küçüğü |        |             |
|--------------------|--------------------|-----------------|--------|-------------|
|                    | Yarışma            | Arkası Yarın    | Komedi |             |
| Yarışma            | 25                 | 25              | 40     | **25**      |
| Arkası Yarın       | 25                 | 40              | 18     | 18          |
| Komedi             | 18                 | 24              | 30     | 18          |
| Sütun En Büyüğü    | **25**             | 40              | 40     | **25 = 25** |

**Örnek 9.15**: Tablonun satır en küçükleriyle oluşturulan son sütunu
incelendiğinde enb (25, 18, 18) = 25 olduğu görülecektir. Bu, birinci kanalı en
az 25 milyon kişinin izleyeceği anlamına gelir. Diğer taraftan, sütun en
büyükleriyle oluşturulan son satır incelendiğinde enk(25, 40, 40) =25 olduğu
görülecektir. Bu ise ikinci kanalı en az 25 milyon kişinin izleyeceği anlamına
gelir. Enb(satır en küçükleri) = enk(sütun en büyükleri) olduğundan, oyun tepe
noktalı bir oyundur. Buna göre 25 milyon kişi birinci kanaldaki yarışma
programını, kalan 25 milyon kişi ikinci kanaldaki yarışma programını
izleyecektir. Özetle oyunun satır oyuncusu için değeri 25, sütun oyuncusu için
25 (= 50 – 25) dir.

## 9.5. İKİ KİŞİLİ SABİT OLMAYAN TOPLAMLI OYUNLAR

Uygulamada sabit olmayan toplamlı oyunlarla karşılaşmak daha olağandır. Rakip
işletmelerin tam anlamıyla çatışma durumunda olmaları genellikle beklenmez. Bu
kesimde oyuncuların işbirliği yapmalarının söz konusu olmadığı iki kişili sabit
olmayan toplamlı oyun problemleri üzerinde durulacaktır. Çok bilinen tutuklu
ikilemi problemiyle başlayalım.

# Örnek 9.16: Soygun yapan iki kişi yakalanmış ve tutukevine konmuştur. Suçlu olduklarının bilinmesine karşın yargının elinde suçu kanıtlayacak yeterli delil yoktur. Bu nedenle savcı sanıkları birbirlerine karşı tanıklık etmeleri konusunda ikna etmeye çalışmaktadır. Savcı sanıkların suçlarını itiraf etmelerini sağlamak için her birine ayrı ayrı şunları söyler: Suçu biriniz itiraf eder diğerine karşı tanıklık ederse itiraf eden serbest kalır, itiraf etmeyen 9 yıl ceza alır. Her ikiniz birden suçlu olduğunuzu kabul ederseniz 6’şar yıl ceza alırsınız. Her ikiniz birden suçu reddederseniz 1’er yıl ceza alırsınız. Sizce sanıklar için en uygun davranış ne olur?

**Çözüm 9.16**: Sanıkların birbirleriyle haberleşmelerinin mümkün olmadığını
varsayalım. Buna göre sanıkların kazanç (ceza almak istenmeyen bir durum olduğu
için - değerli) matrisleri aşağıdaki gibi düzenlenir.

Birinci sanık için düzenlenen kazanç (ceza) matrisi aşağıda gösterilmiştir.
İkinci sanığın ceza matrisine geçmeden önce birinci sanık için en iyi davranış
biçiminin ne olacağını araştıralım. Birinci sanığın, ikinci sanığın itiraf
edeceğini umduğunu düşünelim. Bu durumda kendisi için en iyi strateji suçu kabul
etmek olur (-6, -9’dan daha iyidir). Birinci sanığın, ikinci sanığın
reddedeceğini düşündüğünü varsayalım. Bu durumda birinci sanık için en iyi
seçenek suçu kabul etmek olur (0, -1’den iyidir). Özetle ikinci sanığın tavrı ne
olursa olsun birinci sanık için en iyi davranış biçimi suçu kabul etmektir.
Birinci sanığın ceza matrisi Tablo 9.31’de gösterilmiştir.

### Tablo 9.31

| Birinci Sanık | İkinci Sanık |     |
|---------------|--------------|-----|
|               | İtiraf       | Red |
| İtiraf        | -6           |  0  |
| Red           | -9           | -1  |

Şimdi de ikinci sanık için en iyi davranış biçiminin ne olacağını araştıralım.
İkinci sanığın durumunu özetleyen ceza matrisi Tablo 9.32’de gösterilmiştir.

### Tablo 9.32

| Birinci Sanık | İkinci Sanık |     |
|---------------|--------------|-----|
|               | İtiraf       | Red |
| İtiraf        | -6           | -9  |
| Red           |  0           | -1  |

İkinci sanığın, birinci sanığın suçu kabul edeceğini umduğunu düşünelim. Tablo
9.32’den görüleceği gibi, bu durumda kendisi için en iyi strateji suçu kabul
etmek olur (-6, -9’dan iyidir). İkinci sanığın, birinci sanığın reddedeceğini
düşündüğünü varsayalım. Bu durumda kendisi için en iyi seçenek suçu kabul etmek
olur (0, -1’den iyidir). Özetle birinci sanığın tavrı ne olursa olsun ikinci
sanık için en iyi davranış biçimi suçu kabul etmektir.

Sabit olmayan toplamlı oyunlarda oyuncuların oyun matrisleri yukarıdaki gibi
ayrı matrisler olarak değil tek matris halinde gösterilir. Birinci ve ikinci
suçluların ceza matrislerinin göz önünde bulundurulmasıyla oluşturulan ceza
matrisi aşağıda gösterilmiştir.

### Tablo 9.33

| Birinci Suçlu | İkinci Suçlu |          |
|---------------|--------------|----------|
|               | İtiraf       | Red      |
| İtiraf        |  (-6, -6)    | (0, -9)  |
| Red           | (-9, 0)      | (-1, -1) |

Yukarıdaki açıklamaların ortaya koyduğu gibi oyunun tepe noktası (-6, -6)
gözesinde ortaya çıkmaktadır. Bunun anlamı her iki sanığın suçu kabul etmesi ve
6’şar yıl ceza almaları (toplam 12 yıl ceza)’dır.

Tablo 9.33 incelendiğinde (-1, -1) gözesinin işaret ettiği stratejilerin
diğerlerinden daha iyi olduğu düşünülebilir. Çünkü bu sanıkların 6’şar yıl
yerine 1’er yıl ceza almaları demektir. Ancak, (-1, -1) sonucu hiç
gerçekleşmeyebilir. Çünkü sanıklardan biri bu gözenin işaret ettiği stratejiyi
benimsemişken diğeri bundan vazgeçerse cezasının 1 yıl yerine sıfır yıl olmasını
sağlayabilir. Bu yüzden (-1, -1) tepe noktası olamaz. İki-kişili sıfır-toplamlı
oyunlarda olduğu gibi, iki-kişili sabit olmayan-toplamlı oyunların tepe noktası
oyuncuların strateji seçimlerini tek başına değiştirmelerinin oyunculara hiçbir
yarar sağlamadığı noktada ortaya çıkar.

**Örnek 9.17**: Rakip iki marketin (A ve B) satışları toplamı 240 milyon TL’dir.
Rakiplerin bu toplam içindeki payları reklam harcamalarının miktarına bağlıdır.
Rakipler reklama 6 veya 10 milyon TL harcamak durumunda olup reklam harcaması
fazla olan marketin satış geliri 190 milyon TL olmaktadır. Reklam harcamalarının
eşit olması durumunda satış gelirleri de eşit olmaktadır. Bir TL’lik satışdan
elde edilen kâr 0.5 TL’dir. Marketlerin amacı"kâr–reklam harcaması" değerini en
büyüklemektir. Oyun matrisini kurunuz ve oyunun tepe noktası olup olmadığını
belirleyiniz.

**Çözüm 9.17**: Önce market A ve B’nin strateji seçimlerinin sonucunda ortaya
çıkan sonuç değerlerini hesaplayalım. A’nın ve B’nin reklam harcamalarının 10’ar
milyon TL olduğunu düşünelim Buna göre hem A’nın hem de B’nin net kazancı
aşağıdaki gibi hesaplanır.

(120 milyon x 0.5) – (10 milyon) = 50 milyon

Şimdi de hem A’nın hem de B’nin reklam için 6’şar milyon TL harcadıklarını
düşünelim. Buna göre, A ve B’nin birbirine eşit olan kazançları aşağıdaki gibi
hesaplanır.

(120 milyon x 0.5) – (6 milyon) = 54 milyon

A’nın 10, B’nin 6 milyon harcadığını düşünelim. Bu durumda,

A’nın kazancı = (190 milyon x 0.5) – (10 milyon) = 85 milyon

B’nin kazancı = (50 milyon x 0.5) – (6 milyon) = 19 milyon

olur.

Son olarak A’nın 6, B’nin 10 milyon harcadığını düşünelim. Bu durumda kazançlar
aşağıdaki gibi hesaplanır.

A’nın kazancı = (50 milyon x 0.5) – (6 milyon) = 19 milyon

B’nin kazancı = (190 milyon x 0.5) – (10 milyon) = 85 milyon

Hesaplanan bu değerlerin kullanılmasıyla, oyunu özetleyen kazanç matrisi Tablo
9.34’de gösterildiği gibi elde edilir.

### Tablo 9.34

| A’nın Reklam Harcaması | B’nin Reklam Harcaması |           |
|------------------------|------------------------|-----------|
|                        | 6 milyon               | 10 milyon |
| 6 milyon               | (54, 54)               | (19, 85)  |
| 10 milyon              | (85, 19)               | (50, 50)  |

A, B’nin 6 milyon TL harcayacağını düşünüyor olsun. Bu durumda A, 54 milyon
yerine 85 milyon kazanmak için 10 milyon harcar. Rakibinin 10 milyon harcaması
durumunda A, 19 milyon yerine 50 milyon kazanmak için 10 milyon harcar.
Açıklamaların ortaya koyduğu gibi, B’nin tavrı ne olursa olsun A için en iyi
seçim reklam için 10 milyon TL harcamaktır.

Aynı analizi B için gerçekleştirelim. A’nın 6 milyon TL harcaması durumunda B,
10 milyon TL harcayarak kazancının 85 milyon TL olmasını sağlar. Rakibinin 10
milyon harcaması durumunda B, 19 milyon yerine 50 milyon kazanmak için 10 milyon
harcar. Açıklamaların ortaya koyduğu gibi, A’nin tavrı ne olursa olsun B için en
iyi seçim reklam için 10 milyon TL harcamaktır. Özetle, A’nın tavrı ne olursa
olsun, B 10 milyon TL harcamayı kararlaştıracaktır. O halde oyunun tepe noktası
her bir marketin 10 milyon alternatiflerinin kesiştiği gözede gerçekleşir.

(54, 54) gözesinin işaret ettiği stratejilerin daha iyi olduğu düşünülebilir.
Çünkü bu, rakip marketlerin 50’şer milyon yerine 54’er milyon kazanmaları
demektir. Ancak bu sonuç hiç gerçekleşmeyebilir. Çünkü, marketlerden biri bu
gözenin işaret ettiği stratejiyi benimsemişken diğeri bundan vazgeçerse
kazancının 54 yerine 85 milyon olmasını sağlar. Bu yüzden (54, 54) tepe noktası
olamaz.

Oyun problemlerinin çözümünde aşağıdaki akış çizelgesinin göz önünde
bulundurulmasının uygun olur.

**Şekil 9.5**

# PROBLEMLER

1.  İki arkadaştan her biri (A ve B) aynı anda bir kağıt üzerine 1 ile 5
    arasında bir sayı yazar ve diğerinin görmemesi için yazdığı sayıyı eliyle
    kapatır. Yazılan sayılar aynı ise oyuncular arasında ödeme söz konusu
    olmamaktadır. Yazılan sayıların toplamı tek ise A, çift ise B oyunun galibi
    olarak diğerinden sayıların toplamı kadar para almaktadır. Oyunun matrisini
    oluşturunuz.

2.  Aynı pazarda rekabet eden iki firmadan A, pazarın %60’ını; B ise %40’ını
    kontrol etmektedir. Pazar payını artırmak ya da mevcut Pazar payından
    rakibine kaptırmamak için firmalar reklam vermeyi düşünmektedirler.
    Firmaların kullanabilecekleri dört alternatif reklam aracı vardır. Bunlar;

R1 : Fuar ve sergilerde ürün tanıtımı

R2 : TV reklamı

R3 : Gazete reklamı

R4 : Radyo reklamı

dır. Müşteriler halihazırda kullandıkları ürün hakkında yapılan reklamlardan
etkilenmemele birlikterakip firmanın ürünü ile ilgili reklamlardan
etkilenmektedirler. Yapılan araştırmalar R1, R2, R3 ve R4 reklamlarının rakip
firma müşterilerinin sırasıyla %40, %25, %20 ve %10’u üzerinde etkili olduğu ve
bu müşterilerin reklamını gördüğü ürünü almaya başlayacağını göstermektedir.
Oyunun matrisini kurunuz ve firmaların en iyi stratejilerini belirleyiniz.

**3**. Kazanç matrisleri aşağıdaki gibi olan oyunların tepe noktalarını bulunuz.

**4**. Kazanç matrisi aşağıda verilmiş olan 4x4 oyunları 2x2 boyutuna
indirgeyiniz.

**5**. Aynı işi yapan ve aynı bölgede faaliyet gösteren A ve B gibi iki işletme
vardır. Bölgenin potansiyel müşterileri bu iki işletme arasında eşit biçimde
dağılmışlardır. İki işletme müşterilerinin sayısını artırmak amacıyla reklam
vermeyi düşünmektedir. Reklam için gazete, radyo ve televizyon
kullanılabilmektedir. Pazarın eğilimi gözlenmiş ve sonuç değerleri müşteri
sayısına karşılık gelen oyun matrisi aşağıdaki gibi belirlenmiştir. İşletmelerin
en iyi stratejilerini ve oyunun değerini bulunuz.

| A’nın        | B’nin Stratejileri |       |     |
|--------------|--------------------|-------|-----|
| Stratejileri | Gazete             | Radyo | TV  |
| Gazete       | 40                 | -60   | -25 |
| Radyo        | 50                 | 25    | -10 |
| Televizyon   | -100               | 30    |  60 |

**6**. A oyuncusu B oyuncusuna göstermeden bir kağıt parçası üzerine 1 ile 20
arasında bir sayı yazmaktadır. A rakibine şu sayıyı yazdım diyerek ondan
kendisinin doğru mu yanlış mı söylediğini tahmin etmesini istemektedir. B, A’nın
yalan söylediğini doğru tahmin ederse A’dan 10 TL almaktadır. B yanılırsa A’ya 5
TL ödemektedir. B, A’nın doğru söylediğini doğru tahmin ederse 1 TL
kazanmaktadır. A doğru söylediği halde B inanmazsa A’ya 5 TL ödemektedir. Oyunun
değerini ve oyuncuların en iyi stratejilerini bulunuz.

**7**. Sıfır toplamlı oyunların kazanç matrisleri aşağıda gösterilmiştir.
Oyunları ayrı ayrı ele alarak,

1.  Tepe noktalarını belirleyiniz.

2.  Eş ve üstünlük stratejilerini araştırarak matris üzerinde gerekli indirgeme
    işlemini gerçekleştiriniz

3.  Orijinal oyun ile indirgenmiş oyunun maksimin ve minimaks stratejilerini
    bularak elde ettiğiniz sonuçları karşılaştırınız.

4.  Orijinal oyun ile indirgenmiş oyunları ayrı ayrı çözerek çözüm sonuçlarını
    karşılaştırınız.

5.  İnsaflı oyunları belirleyiniz.

**8**. Sıfır toplamlı oyunların kazanç matrisleri aşağıda gösterilmiştir.
Oyunların her biri için,

1.  Maksimin ve minimaks stratejileri bulunuz.

2.  Mümkünse matris boyutunu indirgeyiniz.

3.  Oyunun değerini hesaplayınız.

4.  Oyun insaflı bir oyun mudur açıklayınız.

**9**. Kazanç matrisleri aşağıda gösterilen oyunları grafik tekniğiyle çözerek
oyuncuların en iyi stratejilerini ve oyunların değerlerini bulunuz.

**10**. Bir asker tabancasında tek bir kurşun kalmış bir düşman tarafından
kovalanmaktadır. Kendisine saklanacak yer arayan askerin saklanabileceği 6 delik
(1, 2, 3, 4, 5, 6) vardır. Delikler aşağıda gösterildiği gibi yanyana dizilidir.

Düşman deliklerin arasına (A, B, C, D, E) ateş etmeyi planlamıştır. Asker,
düşmanın ateş ettiği aralığa bitişik delikteyse ölmektedir. Asker ölürse düşman
1 madalya ile ödüllendirilmektedir. Askerin sağ kalması durumunda düşman hiçbir
ödül kazanamamaktadır. Oyunun sıfır toplamlı olduğunu varsayarak ödül matrisini
oluşturunuz ve varsa üstünlük stratejilerini bularak mahkum stratejileri devre
dışı bırakınız. Oyuncuların en iyi stratejilerini ve oyunun değerini bulunuz.

**11**. Aşağıdaki kazanç matrislerine sahip oyunları doğrusal programlama ile
çözünüz.

**12**. İki komşu ülke (A, B) yeni tip bir füze geliştirmek veya eski tip
füzelerle yetinmek konusunda karar vereceklerdir. A ve B’den sadece birinin yeni
tip füze kararı vermesi durumunda yeni tip füze geliştiren ülke diğer ülkenin
topraklarını kazanıyor. Bu kazanımda kazanan ülkenin kazancı 20 birim, yenilen
ülkenin kaybı 100 birim olmaktadır. Yeni tip füze geliştirme maliyeti 10
birimdir. Oyun matrisini düzenleyerek oyunun tepe noktasını bulunuz.

**13**. Aşağıdaki sabit olmayan toplamlı oyunların tepe noktalarını bulunuz.
