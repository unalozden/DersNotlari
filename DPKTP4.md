PAGE  97

***DOĞRUSAL PROGRAMLAMA***














## ***4.1 GİRİŞ***
`	`Doğrusal programlama problemlerinin çözümünü kavrayabilmek bakımından önemli olan grafik yöntemi, çok değişkenli doğrusal programlama problemlerinin çözümünde son derece yetersiz kalmaktadır. Grafikle çözümün uygulanamadığı çok değişkenli doğrusal programlama problemlerinin çözümünde yaygın biçimde kullanılan yöntem *simpleks yöntemidir*. George B. Dantzig tarafından geliştirilen bu yöntem tekrarlı bir yöntem olduğundan *simpleks algoritma* olarak da adlandırıl-maktadır. Simpleks adı uygun çözüm bölgesinin şeklinden türetilmiştir. n boyutlu uzayda (n + 1) uç noktaya sahip konveks çoklu düzleme *simpleks* denir. Örneğin, iki boyutlu uzayda simpleks bir üçgen, üç boyutlu uzayda bir dörtgendir. Simpleks yöntemin tekrarları simpleksin bir uç noktasından daha büyük (en büyükleme problemlerinde) veya daha küçük (en küçükleme problemlerinde) bir Z değeri sağlayacak komşu uç noktalarına yapılan hareketlerden oluşur. Sonlu sayıda uç noktası olan simpleks üzerinde belirli sayıda tekrardan sonra en iyi çözüme ulaşılır. Yöntemin en belirgin özelliği çok sayıda değişken içeren doğrusal programlama problemlerine kolayca uygulanabilmesidir. Yöntemle ilgili açıklamalara geçmeden önce yöntemin kuramsal açıklamaları üzerinde durmayacağımızı, simpleks yöntemini matematiksel olmayan bir yaklaşımla açıklayacağımızı belirtmeliyiz.
## `	`***4.2 KANONİK VE STANDART BİÇİMLER***
`	`Daha önce açıklandığı gibi problemin belirlenmesinden sonra yapılması gerekli en önemli iş, problemi en iyi biçimde temsil eden ve çözümü kolay olan bir modelin kurulmasıdır. Bilindiği gibi, doğrusal programlama problemleri farklı biçimlerde gösterilmektedir. Amaç fonksiyonu Zenb veya Zenk, kısıtlayıcı fonksiyonları eşitsizlik (³ veya £) ya da eşitlik biçiminde tanımlanabilir. Bu kesimde, doğrusal programlamanın kanonik ve standart biçimleri üzerinde durulacaktır.

***1**. **Kanonik Biçim***

Zenb = C1x1 + C2x2 + ... + Cnxn

`          `a11x1 + a12x2  	+  ... + a1nxn £ b1

`          `a21x1 + a22x2  	+  ... + a2nxn £ b2

`              `.           .         ...        .        .

`          `am1x1 + am2x2 	+ ...  + amnxn £ bm

`                     `x1 ³ 0, x2 ³ 0, ..., xn ³ 0

olarak formüle edilen doğrusal programlama aşağıdaki özelliklere sahipse, *kanonik* biçimde olduğu söylenir.

*1*. Tüm karar değişkenleri negatif değildir.

*2*. Amaç fonksiyonu en büyükleme tipindedir.     

*3*. Tüm kısıtlayıcı fonksiyonlar (£) işaretlidir.

***2**. **Standart Biçim***

Zenk/enb = C1x1 + C2x2 + ... + Cnxn

`               `a11x1 + a12x2  +  ... + a1nxn = b1

`               `a21x1 + a22x2  +  ... + a2nxn = b2

`                  `.           .         ...        .         .              

`               `am1x1 + am2x2 + ... + amnxn = bm

`                         `x1 ³ 0, x2 ³ 0, ..., xn ³ 0

olarak formüle edilen doğrusal programlama modeli aşağıdaki özelliklere sahipse, *standart* biçimde olduğu söylenir. 

*1*. Tüm karar değişkenleri negatif değildir.

*2*. Amaç fonksiyonu en büyükleme veya en küçükleme tipindedir. 

*3*. Tüm kısıtlayıcı fonksiyonlar (negatif olmama koşulu dışında) = işaretlidir.

*4*. Kısıtlayıcı fonksiyonların sağ taraf sabitleri negatif değildir. 

Herhangi bir doğrusal programlama modeli bazı basit dönüştürme işlemleriyle her iki biçimde de yazılabilir. Dönüştürme işlemlerinin yaygın biçimde kullanılanları aşağıda açıklanmıştır.

***1**.**En iyilemenin anlamını değiştirme***: Bilindiği gibi, bir fonksiyonun en büyük değeri ile ters işaretlisinin en küçük değeri birbirine eşittir. Bu nedenle, en büyükleme amaçlı bir doğrusal programlama problemi en küçükleme problemi olarak çözülebilir. Bunun tersi de doğrudur. Her iki durumda da amaç fonksiyonunun (-1) ile çarpılması yeterlidir. Örneğin,

Zenb = C1x1 + C2x2 + ... + Cnxn

olarak tanımlanmışken,

= (-Zenb ) = -C1x1 - C2x2 - ... - Cnxn	 

veya 

Zenk = C1x1 + C2x2 + ... + Cnxn

olarak verilmişken,

= (-Zenk) = -C1x1 - C2x2 - ... - Cnxn

yazılabilir.

Bu dönüşümü mümkün kılan, her iki amacın aynı uygun çözüm bölgesinde en iyilenmesidir. 

Örnek olması bakımından amaç fonksiyonunun aşağıdaki gibi formüle edildiğini düşünelim.

Zenk = 3x1 - 4x2 + 2x3 - 5x4

Amaç fonksiyonundaki tüm terimlerin işaretlerinin değiştirilmesiyle amaç fonksi- yonu aşağıdaki gibi yazılabilir.

= (-Zenk) = -3x1 + 4x2 - 2x3 + 5x4

Dönüştürme işlemi, karar değişkenlerinin en iyi değerlerini değiştirmez. Problemi çözdükten sonra amaç fonksiyonunun en iyi değeri (-1) ile çarpılırsa orijinal problemin Zenk (Zenb) değeri bulunur.

***2**.**Eşitsizliklerin yönünü değiştirme***: Herhangi bir eşitsizliğin her iki tarafı (-1) ile çarpıldığında  eşitsizlik  yön değiştirir. Sözgelimi, a1x1 + a2x2 ³ b ile her iki tarafının  (-1) ile çarpılmasıyla elde edilen -a1x1 - a2x2 £ -b birbirlerine eşittir. Benzer biçimde, a1x1 + a2x2 £ b yerine -a1x1 - a2x2 ³ -b yazılabilir.

***3**.**Eşitliği eşitsizliğe dönüştürme***: Eşitlik biçimindeki bir kısıtlayıcı fonksiyon iki eşitsizlikle açıklanabilir. Örneğin, a1x1 + a2x2 = b biçimindeki bir fonksiyon yerine, a1x1 + a2x2 ³ b  ve  a1x1 + a2x2 £ b veya a1x1 + a2x2 £ b  ve  -a1x1 - a2x2 £ -b yazılabilir.

***4**.**İşareti sınırlandırılmamış değişkenler***: İşareti sınırlandırılmamış bir değişken (pozitif, negatif veya sıfır) negatif olmayan iki değişken arasındaki fark olarak açıklanabilir. Sözgelimi, x işareti sınırlandırılmamış bir değişken ise, x yerine kullanılabilir. Burada, ³ 0 ve ³ 0’dır. Negatif olmayan ve  değişkenlerinden en fazla biri en iyi çözümde pozitif değerli olur.

***5**.**Eşitsizlik biçimindeki kısıtlayıcı fonksiyonların eşitlik biçimine dönüştürülmesi***:

Simpleks yöntem bir eşitlikler sistemine, standart işlemlerin tekrar tekrar uygulanmasıyla çözüm arayan bir süreçtir. Bu nedenle yöntemin en önemli adımı kısıtlayıcı fonksiyonların eşitlik biçiminde yazılmasıdır. Eşitsizlik biçimindeki bir kısıtlayıcının eşitsizliğin yönü bakımından iki türlü olduğu bilinmektedir. Eşitsizlikler £ bi veya ³ bi biçimindedir.

(£) işaretli eşitsizlikleri eşitlik biçimine dönüştürmek için bunların sol taraflarına negatif olmayan birer değişken eklenir. *Aylak değişken* adı verilen bu değişkenler xn+1, xn+2, ..., xn+m ile gösterilir. (³) işaretli eşitsizlikler ise, sol taraflarından negatif olmayan birer değişken çıkartılmasıyla eşitlik biçimine dönüştürülür. Eşitsizliğin iki tarafı arasındaki farkı gösteren bu değişkene *artık değişken* denir. Bu değişkenler de aylak değişkenler gibi xn+1, xn+2 , ..., xn+m sembolleriyle gösterilirler. Yukarıda açıklandığı gibi, negatif olmama koşulu karar değişkenlerinin yanı sıra aylak ve artık değişkenlere de uygulanmaktadır. Bunun nedeni, kısıtlayıcı fonksiyonlardaki (³) ve (£) şartlarının gerçekleşmesini sağlamaktır.

***6**. **Mutlak değerli kısıtlayıcı fonksiyonların eşitsizlik biçiminde yazılması***: Çok sık olmasa da mutlak değer içeren kısıtlayıcı fonksiyonlara rastlanabilir. Hangi yöntem uygulanırsa uygulansın bu tür kısıtlayıcılarla çözüme ulaşılamaz. Bu yüzden mutlak değerden kurtulmak gerekir. Örnek olması bakımından, kısıtlayıcı fonksiyonun £ b şeklinde formüllendiğini düşünelim. Bu durumda yapılması gereken £ b yerine a1x1 + a2x2 ³ -b ve a1x1 + a2x2 £ b ikilisini yerleştirmektir. Kısıtlayıcı  ³ b ise  ³ b yerine geçecek eşitsizlikler a1x1 + a2x2 ³ b ve a1x1 + a2x2 £ -b biçimindedir.

Herhangi bir doğrusal programlama modelinin standart veya kanonik biçimde yazılmasını bir örnek üzerinde açıklayalım.

***Örnek 4.1***: Aşağıdaki gibi verilmiş olan doğrusal  programlama  problemini, ***a***. Kanonik biçimde,  ***b***. Standart biçimde yazınız.

Zenk = -6x1 + 7x2 + 7x3 - x4

`              `x1 +  2x2  - 4x3         ³ 30

`            `2x1  + 9x2 + 6x3 + x4 £ 60

`            `6x1            +   x3 + x4 = 15

`           `|3x1 + 4x2|                  £ 80

`                              `x1, x2,  x4 ³ 0,  x3 sınırlandırılmamış

***Çözüm 4.1***: ***a***. Kanonik biçimde amaç fonksiyonunun Zenb olması gerektiğinden Zenk olarak verilen amaç fonksiyonu her iki tarafının (-1) ile çarpılmasıyla Zenb biçimine dönüştürülür. x3’ün işareti bakımından sınırlandırılmamış olduğu göz önünde bulundurulduğunda amaç fonksiyonu aşağıdaki gibi elde edilir. 

= 6x1 - 7x2 - 7() + x4

Kanonik biçimin kısıtlayıcı fonksiyonlarının (£) işaretli olması gerektiğinden, bu özelliği taşımayan kısıtlayıcıların uygun dönüştürme işlemleriyle (£) biçiminde yazılması zorunludur. Bu amaçla, kısıtlayıcı fonksiyonları sırasıyla ele alalım. İlk kısıtlayıcı (³) işaretli olduğundan, her iki yanı (-1) ile çarpılır. x3’ün işareti sınırlandırılmamış olduğundan, x3 yerine () yazılmasıyla birinci kısıtlayıcı fonksiyon aşağıdaki gibi düzenlenir. 

-x1 - 2x2 + 4() £ -30

İkinci kısıtlayıcı fonksiyonun yönü doğrudur. x3 yerine () yazılmasıyla fonksiyon aşağıdaki gibi düzeltilmiş olur.

2x1 + 9x2 + 6() + x4 £ 60

Üçüncü kısıtlayıcı eşitlik biçiminde olduğundan aşağıdaki eşitsizlikler çiftiyle açıklanmalıdır.

6x1 + x3 + x4 £  15

6x1 + x3 + x4  ³ 15

Bu eşitsizlik çiftine x3 =  yerleştirilmesi ve (³) işaretli kısıtlayıcının her iki tarafının (-1) ile çarpılması sonucunda bu kısıtlayıcı fonksiyon,

` `6x1 + () + x4 £  15

-6x1 -  () - x4  £ -15

olarak kanonik biçime uygun hale dönüştürülmüş olur.

Dördüncü kısıtlayıcı fonksiyonun sol tarafındaki mutlak değer bu kısıtlayıcının,

3x1 + 4x2 £  80

3x1 + 4x2 ³ -80

biçiminde yazılmasını gerektirir. (³) işaretli kısıtlayıcının her iki tarafının (-1) ile çarpılmasıyla mutlak değerli kısıtlayıcının yerine kullanılacak fonksiyonlar:  3x1 + 4x2 £  80 ve -3x1 - 4x2 £  80 olarak elde edilmiş olur. Kanonik biçim tümüyle aşağıdaki gibi yazılabilir.

= 6x1 - 7x2 - 7() + x4

`            `-x1 -  2x2 + 4()         £ -30                 

`           `2x1 + 9x2 + 6() + x4 	£  60                 

`           `6x1           +   () + x4 	£  15  

`          `-6x1           -    () - x4  	£ -15

`           `3x1 + 4x2                                 £  80

`          `-3x1 - 4x2                                  £  80

`                             `x1, x2, , , x4 ³ 0

***b***. *S*tandart modelin amaç fonksiyonu Zenb veya Zenk türünde olabilir. Bu yüzden orijinal amaç fonksiyonu standart biçim için de geçerli olur. Burada, dikkat edilmesi gereken en önemli nokta, x3’ün işaretçe sınırlandırılmamış olduğudur. O halde, standart biçimin amaç fonksiyonu aşağıdaki gibi olur.

Zenk = -6x1 + 7x2 + 7() - x4

Standart biçimde tüm kısıtlayıcı fonksiyonların eşitlik biçiminde olması gerektiğinden, bu biçime uymayan kısıtlayıcılar eşitlik biçiminde düzenlenmelidir. Kısıtlayıcı fonksiyonları sırasıyla ele alalım. 

Birinci kısıtlayıcının yönü (³) olduğundan, eşitsizliğin sol tarafından negatif olmayan bir değişkenin (x5) çıkartılması gerekir. x3’ün sınırlandırılmamış olduğunun dikkate alınmasıyla, standart biçimin ilk kısıtlayıcı fonksiyonu aşağıdaki gibi elde edilir. 

x1 + 2x2 - 4() - x5 = 30

İkinci kısıtlayıcıya bir aylak değişken (x6) eklenmesi ve x3 =  yazılmasıyla kısıtlayıcı fonksiyon aşağıdaki gibi olur.

2x1 + 9x2 + 6() + x4 + x6 = 60

Üçüncü kısıtlayıcı eşitlik biçiminde olduğundan değişmez. x3 yerine () yazılmasıyla elde edilen kısıtlayıcı kısıtlayıcı fonksiyon şöyledir: 

6x1 + () + x4 = 15

Modelin son kısıtlayıcı fonksiyonu yerine -3x1 - 4x2 £ 80 ve 3x1 + 4x2 £ 80 yazılması bunlara sırasıyla x7 ve x8 aylak değişkenlerinin eklenmesiyle,

-3x1 - 4x2 + x7 = 80

3x1 + 4x2 + x8 = 80

elde edilir.

Tüm kısıtlayıcı fonksiyonlar uygun biçimde düzenlendiğinden, negatif olmama koşulunun yazılmasıyla standart biçim, 

Zenk = -6x1 + 7x2 + 7() - x4

`              `x1 + 2x2 -  4()         - x5                     	= 30

`            `2x1 + 9x2 + 6() + x4        + x6              	= 60

`            `6x1           +  () + x4                             	= 15

`          `-3x1 -  4x2                                              + x7       	= 80

`           `3x1 + 4x2                                                                                         + x8	= 80

`                                      `x1, x2, , x4, , , x5, x6, x7, x8 ³ 0

olarak düzenlenmiş olur.
## `	`***4.3 SİMPLEKS YÖNTEMİN AÇIKLANMASI***
`	`Yukarıda belirtildiği gibi, simpleks yöntem herhangi bir doğrusal programlama problemine, eğer varsa, sınırlı sayıda tekrar sonucunda bir en iyi çözüm bulan veya sınırsız çözüm olduğunu belirten bir tekrarlar sürecidir. Yani, en iyi çözüm standart işlemlerin sınırlı tekrarı ile elde edilir. Her bir tekrarda uygun çözümlerden bir tanesi incelenir. Ardışık çözümlerin her biri kendisinden önceki çözümden daha gelişmiş, başka bir deyişle en iyi çözüme biraz daha yakın (en kötü ihtimalle önceki çözüme eşit) bir çözümdür. Ardışık tekrarların sayısı değişebilir. Deneyimler m kısıtlayıcı, n karar değişkeninden oluşan bir doğrusal programlama probleminin en iyi çözümüne ulaşılıncaya kadarki tekrar sayısının m ile 3m arasında değiştiğini, ortalama 2m olduğunu, göstermiştir. 

Yöntemi açıklamak için problemin aşağıdaki gibi formüllendiğini düşünelim. 

Zenb = C1x1 + C2x2 + ... + Cnxn

`          `a11x1 + a12x2  +  ... + a1nxn £ b1

`          `a21x1 + a22x2  +  ... + a2nxn £ b2

`              `.          .         ...        .        .  

`          `am1x1 + am2x2 + ... + amnxn £ bm

`                    `x1 ³ 0, x2 ³ 0, ..., xn ³ 0

Simpleks yöntemin ilk adımı tüm eşitsizliklerin (negatif olmama koşulu hariç) eşitlik biçimine dönüştürülmesidir. Kesim 4.2’de açıklandığı gibi (£) işaretli bir eşitsizliği eşitliğe dönüştürmek için eşitsizliğin sol tarafına negatif olmayan bir aylak değişken eklenir. Her bir eşitsizlik için bir aylak değişken kullanılmasıyla yukarıdaki kısıtlayıcı fonksiyonlar aşağıdaki gibi olur.

a11x1 + a12x2 +  ... + a1nxn + 1xn+1 + 0xn+2 + ... + 0xn+m = b1

a21x1 + a22x2 +  ... + a2nxn + 0xn+1 + 1xn+2 + ... + 0xn+m = b2	 

`   `.           .         ...        .            .           .       ...        .         .

am1x1 + am2x2 + ... + amnxn + 0xn+1 + 0xn+2 + ... + 1xn+m = bm	 

Aylak değişkenlerin eklendikleri kısıtlayıcı fonksiyonlardaki katsayılarının +1, diğerlerinde sıfıra eşit olduğu görülebilir. 

Karar değişkenleri ile aylak değişkenler negatif olmadığından, standart biçimin negatif olmama koşulu aşağıdaki gibi olur.

x1, x2, ..., xn, xn+1, xn+2, ..., xn+m ³ 0

Aylak değişkenlerin amaç fonksiyonu katsayıları, bir başka deyişle bu değişkenlerin amaç fonksiyonuna birim katkıları (birim kârları) sıfırdır([^1]).

Bu durumda amaç fonksiyonu aşağıdaki gibi olur.

Zenb = C1x1 + C2x2 + ... + Cnxn + 0xn+1 + 0xn+2 + ... + 0xn+m

Standart biçimdeki doğrusal programlama modelinin kısıtlayıcı fonksiyonları matrislerle şöyle gösterilir.

Kısıtlayıcıların eşitlik biçimine dönüştürülmesiyle, modelin yürürlükteki n karar değişkenine m değişken eklenmiş, yani bilinmeyen sayısı n’den (n + m)’ye çıkar- tılmıştır. (n + m) bilinmeyene karşılık denklem sayısı m olduğundan, herhangi n bilinmeyen sıfıra eşitlenip diğer m bilinmeyen eşitlikler sisteminin birlikte çözülmesiyle elde edilir. Bu yolla ulaşılan çözüme *temel çözüm*, temel çözümde değerleri sıfırdan farklı olan değişkenlere ise *temel değişken* denir. Çözüm değerleri sıfır olan değişkenler *temel olmayan değişkenlerdir*.

Temel çözüm sayısı sonlu bir sayıdır ve herhangi m sayıdaki değişkeni göz önünde tutarak elde edilir. m kısıtlayıcı, n değişkenin bulunduğu standart biçimdeki problemin  temel çözümlerinin sayısının hesaplama formülü şöyledir. 

\= 

İçeriğindeki değişkenlerin tümü pozitif (> 0) olan temel çözüme *temel uygun çözüm* denir. Temel değişkenlerden bir ya da bir kaçının sıfıra eşit olması durumundaki çözüme bozuk (dejenere) çözüm denir. Temel uygun çözümlerin sayısı da yukarıdaki bağıntıyla hesaplanan sayı ile sınırlıdır. Standart biçimin oluşturulmasından sonra en iyi çözümün araştırılması işlemine geçilebilir. Simpleks yöntemin ardışık tekrarları *başlangıç çözüm tablosu* adı verilen bir tablonun düzenlenmesinden sonra başlar. Başlangıç çözüm tablosu, aşağıdaki tablo esasına göre düzenlenir. Özü, daha doğrusu kapsadıkları bilgi aynı olmakla birlikte bazı kaynaklarda simpleks çözüm tablolarının değişik düzenlemelerine rastlanabilir.

***Tablo 4.1***
##### ***Simpleks Başlangıç Çözüm Tablosu***



|TDV|x1|x2|…|xn|xn+1|xn+2|…|xn+m|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0    xn+1|A11|a12|…|a1n|1|0|…|0|b1|
|0       xn+2|A21|a22|…|a2n|0|1|…|0|b2|
|.|.|.|…|.|.|.|…|.|.|
|.|.|.|…|.|.|.|…|.|.|
|0    xn+m|am1|am2.|…|amn|0|0|…|1|bm|
|Zj|0|0|…||0|0|…|0|0|
|Zj - Cj|-C1|-C2|…|-Cn|0|0|…|0|-|
Tablo 4.1 kapsamındaki bölümler aşağıda açıklanmıştır.

***1**. **Değişkenler satırı**:* Tablonun ilk satırıdır. Standart biçimin tüm değişkenleri önce karar değişkenleri, sonra diğer değişkenler olmak üzere bu satırda gösterilir. 

***2***. ***Temel değişkenler sütunu***: Tablonun ilk sütunudur. Tablodaki çözüme karşılık gelen temel çözümün değişkenleri ile bu değişkenlerin amaç fonksiyonu katsayılarını gösterir. Başlangıçta sadece aylak değişkenler temelde bulunduklarından, Cj’ler sıfıra eşittir. Bu sütunun önemli özelliği başlangıç çözümünün sıfır olduğunu göstermesidir. Yani, başlangıç simpleks tablosunda aylak değişkenler temel değişkenler, karar değişkenleri ise temel olmayan değişkenlerdir. Yukarıda açıklandığı gibi, temelde bulunmayan değişkenlerin çözüm değerleri sıfırdır. Temel olmayan değişkenler için sıfır konulmasıyla temel değişkenler ve değerleri, 

x1, x2, ... , xn = 0  ve xn+1 = b1, xn+2 = b2, ... , xn+m = bm

olur.

Matematik olarak mümkün olan ve *başlangıç* *temel uygun çözüm* olarak isimlendirilen bu çözümün pratik bir anlamı olmamakla birlikte, uygun çözümlerin ve giderek en iyi çözümün bulunmasında bir başlangıç olması bakımından önemlidir. Bu çözüm koordinat sisteminin orijin noktasına karşılık gelir.

***3***. ***Gövde***: Problemin orijinal karar değişkenlerinin kısıtlayıcı fonksiyonlardaki  katsa- yılarından (aij, i = 1, 2, ..., m;  j = 1, 2, ..., n) oluşan m x n matristir. 

***4**. **Birim matris***: Aylak değişkenlerin kısıtlayıcı fonksiyon katsayılarının oluşturduğu m x m birim matristir. 

***5**. **Çözüm vektörü***: Temeldeki değişkenlerin çözüm değerlerini gösteren m x 1 sütun vektördür. Başlangıçta, kısıtlayıcı fonksiyonların sağ taraf sabitlerinden oluşur. 

***6***. ***Zj satırı***: Yürülükteki temelde bulunan değişkenlerin amaç fonksiyonu katsayıları ile xj sütunundaki katsayıların karşılıklı çarpımlarının toplamından oluşur. Buna göre örneğin, Z1 = 0(a11) + 0(a21) + ... + 0(am1) = 0 olur.

Başlangıçtaki temelde yalnızca aylak değişkenlerin bulunmasının doğal sonucu olarak tüm Zj değerleri sıfıra eşittir. İzleyen tablolarda Zj’lerin sıfırdan farklı olabilecekleri unutulmamalıdır.

Temel değişkenlerde ortaya çıkan değişiklikler nedeniyle, amaç fonksiyonu değerinin değişimi Zj sembolünde toplanır. Ayrıca, bu satırın son elemanı amaç fonksiyonunun o simpleks tablo için aldığı değeri gösterir. Başlangıç tablosunda bu değer genellikle sıfıra (0(xn+1) + 0(xn+2) + ... + 0(xn+m) = 0) eşittir.       

***7***. ***Zj - Cj satırı***: Tablonun son satırıdır. Elemanları, Zj ile o sütunla ilgili değişkenin amaç fonksiyonu katsayısı arasındaki farka eşittir. Zj - Cj farkları xj değişkeninin temele alınmasının amaç fonksiyonunda yol açacağı değişikliği ters işaretle gösterir. 

Başlangıç çözümünün bulunmasından sonra sıra amaç fonksiyonunun değerini artıracak diğer temel değişkenlerin araştırılmasına gelir. Bunun için, temelde bulunan değişkenlerden bir tanesinin temelden çıkartılması, yerine bu adımda temelde bulunmayan değişkenlerden bir tanesinin alınması gerekir.

Çıkan ve giren değişkenlerin seçimi nasıl yapılacaktır? Çıkan ve giren değişkenlerin seçiminde hangi ölçüt esas alınmalıdır? Kuşkusuz, amaç fonksiyonuna marjinal katkısı en büyük olan değişken çözüme giren ilk değişken olacaktır. Marjinal katkının büyüklüğü değişkenlerin amaç fonksiyonundaki katsayılarının incelenmesiyle belirlenir.

O halde, simpleks çözüm tablosu göz önüne alındığında giren değişkeni belirleyen ölçüt şudur: Zj - Cj satırındaki negatif değerler arasında  mutlak  değerce  en  büyük Zj - Cj değerli değişken çözüme girmelidir. Bu kural en büyükleme problemleri için geçerlidir.

En küçükleme problemlerinde kullanılan kural, yeri geldiğinde açıklanacaktır.

Giren değişkenin seçiminde kullanılan bu kurala *Dantzig kuralı* denir. Mutlak değerce aynı en büyük negatif değerli birden fazla Zj - Cj varsa, temele giren değişkenler arasında bağ vardır denir. Bu durumda izlenmesi gereken yöntem 4.4. kesimde açıklanacaktır.

Yeni bir değişken temele girdiğine göre, yürürlükteki temelde bulunan değişkenlerden bir tanesinin temeli terketmesi gerekir. Bu yolla temeldeki değişken sayısının aynı kalması sağlanır.

Temeli terkedecek değişken ölçütü, çözüm vektörü elemanlarının çözüme girmesine karar verilen değişkene ait sütunun karşılıklı elemanlarının oranına dayanır.

Bu oranlar arasından (negatif ve sıfır olanlar dışında([^2])) en küçük olana sahip değişken temelden ayrılır([^3]).

Simpleks yöntemle çözümde, temele giren değişkenin bulunduğu sütuna *anahtar sütun*, temeli terkeden değişkenin bulunduğu satıra *anahtar satır* denir. 

Temele giren ve temelden çıkan değişkenlerin belirlenmesinden sonra yeni çözüm tablosu hazırlanır. Yeni çözüm tablosunun temel değişkenler sütunu, çıkan değişken yerine giren değişkenin yazılmasıyla oluşturulacaktır. 

Temele girmesine karar verilen değişkenin temele girmesi ancak ve ancak bu anahtar sütunun çözümü terkedecek değişkenle ilgili sütun vektöre benzemesiyle, yani bir birim vektör olmasıyla olanaklıdır. Anahtar sütun, birim sütun vektöre dönüştü- rülmek istendiğinde bu sütunun hangi elemanı 1 olmalıdır? *Anahtar sayı*, anahtar sütunla anahtar satırın kesiştiği gözedeki sayıya eşittir.

Bu sayının belirlenmesinden sonra anahtar sütun birim sütun vektöre dönüştürülebilir. Bunu sağlamak için *Gauss- Jordan*** *eleme* yöntemindeki eleme işlemine denk olan anahtar işlemlerden yararlanılır. Bu yönteme göre yapılacak ilk iş anahtar satır elemanlarını anahtar sayıya bölerek anahtar satırın yeni elemanlarının hesaplanmasıdır. Bu yolla anahtar sayının bulunduğu gözedeki sayı 1 yapılır.

Diğer bütün satır elemanlarının (Zj ve Zj - Cj satırları dışında) yeni değerleri aşağıdaki formülle bulunur.

-x 

Yöntemin uygulanışını aşağıdaki örnek problem üzerinde gösterelim.

***Örnek 4.2***: Bir sanayii işletmesi bakır, alüminyum ve çinko metallerinin farklı alaşımlarını kullanarak A ve B gibi iki çeşit ürün üretmektedir. İşletmenin elinde 20 ton bakır, 30 ton alüminyum ve 40 ton çinko vardır. Bir birim A ve bir birim B’nin üretiminde kullanılan bakır, alüminyum ve çinko miktarları (ton) ile A ve B’nin bir biriminden elde edilen kârlar (TL) aşağıdaki tabloda gösterilmiştir.

Bu bilgileri ve tablodaki verileri kullanarak problemin doğrusal programlama modelini kurunuz ve işletmenin kârını en büyükleyen üretim miktarlarını simpleks yöntemle bulunuz. 

||Hammadde ||
| - | :-: | :-: |
|Ürün|Bakır|Alüminyum|Çinko|Kâr|
|A|6|3|1|2|
|B|4|1|1|3|
***Çözüm 4.2***: Problemin doğrusal programlama modeli aşağıda gösterilmiştir.

Zenb = 2x1 + 3x2                  

`          `6x1 + 4x2 £ 20   (Bakır kısıtı)

`          `3x1 +   x2 £ 30   (Alüminyum kısıtı)

`            `x1 +   x2 £ 40   (Çinko kısıtı)

`                 `x1, x2 ³ 0

Simpleks yöntemle çözüm için öncelikle problem standart biçimde yazılmalıdır. Eşitsizliklerin tümü (£) işaretli olduğundan, her bir eşitsizliğin sol tarafına bir aylak değişken eklenmesiyle standart biçim aşağıdaki gibi olur.

Zenb = 2x1 + 3x2 + 0x3 + 0x4 + 0x5

`          `6x1 + 4x2 +   x3  + 0x4 + 0x5 = 20

`          `3x1 +   x2 + 0x3  +   x4 + 0x5 = 30

`            `x1 +   x2 + 0x3  + 0x4 +   x5 = 40

`                              `x1, x2, x3, x4, x5 ³ 0

Görüldüğü gibi, başlangıç tablosunun gerektirdiği bütün bilgiler elde edilmiştir. Standart biçim kapsamındaki tüm bilgilerin simpleks tablosuna yerleştirilmesiyle başlangıç tablosu aşağıdaki gibi oluşurulur.

`                                                      `***Tablo 4.2***

`                               `***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|ÇV|Oran|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0    x3|` `6|` `**4**|1|0|0|20|20/4|
|0    x4|` `3|` `1|0|1|0|30|30/1|
|0    x5|` `1|` `1|0|0|1|40|40/1|
|Zj|` `0|` `0|0|0|0|0||
|Zj - Cj|-2|-3|0|0|0|-||

Zj satır elemanları, bulundukları sütundaki katsayılarla temel değişkenlerin amaç fonksiyonu katsayılarının karşılıklı çarpımlarının toplamı olarak aşağıdaki gibi hesaplanmıştır.

Z1 =   0(6) +   0(3) +   0(1) = 0

Z2 =   0(4) +   0(1) +   0(1) = 0

Z3 =   0(1) +   0(0) +   0(0) = 0 

Z4 =   0(0) +   0(1) +   0(0) = 0

Z5 =   0(0) +   0(0) +   0(1) = 0

Z6 = 0(20) + 0(30) + 0(40) = 0

Yukarıdaki Zj değerlerinin kullanılmasıyla Zj - Cj değerleri aşağıdaki gibi bulunur. 

Z1 - C1 = 0 - 2 = -2

Z2 - C2 = 0 - 3 = -3 

Z3 - C3 = 0 - 0 =  0

Z4 - C4 = 0 - 0 =  0

Z5 - C5 = 0 - 0 =  0

Başlangıç tablosunun düzenlenmesinden sonra Zj - Cj satırının gözden geçirilmeli, tüm Zj - Cj ³ 0 ise (problem en büyükleme amaçlı olduğundan), tablodaki çözümün en iyi olduğu kararlaştırılmalıdır. Tablo 4.2’den görüldüğü gibi, Z1 - C1, Z2 - C2  negatif olduğundan, başlangıçtaki temel uygun çözüm en iyi değildir. Temele giren değişken ölçütüne göre enb(,) = Z2 - C2 olduğundan, anahtar sütun x2 değişken sütunudur. x2 yeni çözüm tablosunda temel değişken olarak karşımıza çıkacaktır.

Anahtar satırı belirlemek için çözüm vektörü sütun elemanlarını bire bir olmak koşuluyla anahtar sütun elemanlarına bölelim. Bölme işlemi ile bulunan değerler, başlangıç tablosunun hemen sağında oran başlığı altında gösterilmiştir. En küçük oran x3’e ait olduğundan, x3’ün temelden ayrılması gerektiğine karar verilir. Buna göre, yeni simpleks tablosundaki temel değişkenler sırasıyla x2 (x3’ün yerine), x4 ve x5 olacaktır.

x3 değişken satırı anahtar satır, x2 değişken sütunu anahtar sütun olduğuna göre anahtar sayı 4 olur([^4]).

Anahtar sayının belirlenmesinden sonra anahtar satır elemanları anahtar sayıya bölünmeli ve anahtar satırın yeni elemanları hesaplanmalıdır. Bu işlemler aşağıda topluca verilmiştir.

Anahtar satırın eski elemanları,

olduğuna göre anahtar satırın yeni elemanları,

veya gerekli aritmetik işlemlerin yapılmasıyla aşağıdaki gibi olur.

Bu değerlerin yeni çözüm tablosuna yerleştirilmesinden sonra tablonun diğer elemanları hesaplanabilir.

x4 değişken satırından başlayarak diğer satır elemanlarını hesaplayalım. x4 değişken satırının eski elemanları aşağıda gösterildiği gibidir. 

Bu satırla anahtar sütunun kesiştiği yerdeki sayı 1 ve anahtar satırın yeni elemanları,

olduğuna göre, x4 değişken satırının yeni elemanları, 

`      `[3            1         0         1         0        30]

(-1)

`      `[3/2         0     -1/4        1         0         25]

olarak hesaplanır.

Aynı yaklaşımla x5 değişken satırının yeni elemanlarının, 

|`      `[1|`   `1|`   `0|`   `0|`   `1|`       `40]|
| - | :-: | :-: | :-: | :-: | - |
|(-1)[3/2|`   `1|`   `1/4|`   `0|`   `0|`         `5]|
`      `[-1/2            0          -1/4             0              1              35]

olarak hesaplanacakları bellidir. 

Zj satır elemanları aşağıdaki gibi hesaplanmıştır. 

Z1 = 3(3/2) + 0(3/2)   + 0(-1/2) = 9/2

Z2 = 3(1)    + 0(0)      + 0(0)      =  3

Z3 = 3(1/4) + 0(-1/4)  + 0(-1/4) = 3/4

Z4 = 3(0)    + 0(1)      + 0(0)      =  0 

Z5 = 3(0)    + 0(0)      + 0(1)      =  0

Z6 = 3(5)    + 0(25)    + 0(35)    = 15

Zj - Cj satır elemanları Zj değerlerinden ilgili Cj değerlerinin çıkartılmasıyla,

Z1 - C1 = (9/2) - 2  = 5/2

Z2 - C2 = 3       - 3  =  0

Z3 - C3 = (3/4) - 0  = 3/4

Z4 - C4 = 0       - 0  =  0

Z5 - C5 = 0       - 0  =  0

olarak hesaplanmıştır.

Elde edilen bu değerlerin simpleks çözüm tablosuna yerleştirilmesiyle birinci simpleks çözüm tablosu aşağıdaki gibi düzenlenir.

***Tablo 4.3***

***Simpleks Birinci (En İyi) Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|3    x2|` `3/2|1|` `1/4|0|0|5|
|0    x4|` `3/2|0|-1/4|1|0|25|
|0    x5|-1/2|0|-1/4|0|1|35|
|Zj|` `9/2|3|` `3/4|0|0|15|
|Zj - Cj|` `5/2|0|` `3/4|0|0|-|
Tablo 4.3’den görüldüğü gibi tüm Zj - Cj ³ 0 olduğundan, yürürlükteki çözüm en iyidir. Temelde bulunmayan değişkenlerin amaç fonksiyonuna katkıları negatif olduğundan, temelde gerçekleştirilecek bir değişiklik Z’nin azalmasına yol açacaktır. Bu durumda Z = 15, amaç  fonksiyonu  için  bulunabilecek en  büyük değerdir. Bu  çözümde x1 = 0, x2 = 5, x3 = 0, x4 = 25, x5 = 35’dir. Bu durumda, işletme B’den 5 birim üretirken A’dan hiç üretmeyecek, böylece en yüksek kârı 15 TL olacaktır.

Aylak değişkenlerin en iyi çözümdeki değerleri x3 = 0, x4 = 25, x5 = 35’dir.

Bilindiği gibi, eşitsizliklerin sağ tarafları kullanılabilir kaynak miktarlarını gösterirken, sol tarafları kullanılan kaynak miktarlarını göstermektedir. Bu durumda, bu ikisi arasındaki fark kullanılmayan kaynak miktarına karşılık gelir.

Buna göre, bakırın tamamının kullanıldığı anlaşılır. Nitekim, x1 ve x2’nin en iyi çözümdeki değerleri bakır kısıtına yerleştirildiğinde 6x1 + 4x2 = 6(0) + 4(5) = 20 olarak elde edilecektir.

Öte yandan, alüminyum ve çinkonun tamamının kullanılmasının gerekmediği, üretim işleminin 25 ton alüminyum ve 35 ton çinkonun kullanılmasına gerek kalmadan tamamlandığı görülebilir. Aylak değişkenlerin Zj - Cj değerleri incelendiğinde, 1 ton bakırın kullanımından vazgeçilmesi durumunda kârdaki azalmanın (Z3 - C3)  3/4 TL, 1 ton alüminyum  ve 1 ton çinkonun kullanımlarından vazgeçilmesi durumunda kârdaki azalmaların sırasıyla, Z4 - C4 = 0 ve Z5 - C5 = 0 olacağı görülebilir. 

Amaç fonksiyonunun Zenb ve tüm kısıtlayıcıların (£) biçiminde formüllendiği doğrusal programlama problemlerinin simpleks yöntemle çözülmesine son bir örnek olmak üzere aşağıdaki problemi ele alalım.

***Örnek 4.3***: Aşağıdaki doğrusal programlama problemini simpleks yöntemle çözünüz. 

Zenb = 10x1 + 22x2 + 18x3

`            `x1 + 4x2 + 3x3 £   24

`          `2x1 + 2x2 + 4x3 £   46

`          `3x1 + 5x2 + 6x3 £   60

`          `4x1 + 8x2 + 3x3 £ 120

`                     `x1, x2, x3 ³ 0

***Çözüm 4.3***: Problemin standart biçimi aşağıda gösterilmiştir.

Zenb = 10x1 + 22x2 + 18x3 + 0x4 + 0x5 + 0x6 + 0x7

`              `x1 + 4x2 + 3x3 +  x4  + 0x5 + 0x6 + 0x7 =  24

`            `2x1 + 2x2 + 4x3 + 0x4  +  x5 + 0x6 + 0x7 =  46

`            `3x1 + 5x2 + 6x3 + 0x4  + 0x5 +  x6 + 0x7 =  60

`            `4x1 + 8x2 + 3x3 + 0x4  + 0x5 + 0x6 +  x7 = 120

`                                         `x1, x2, x3, x4, x5, x6, x7 ³ 0

Problemin simpleks başlangıç çözüm tablosu şöyledir.

`		                 `***Tablo 4.4*** 

`		`***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|x7|ÇV|`  `Oran|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0    x4|` `1|` `**4**|` `3|1|0|0|0|24|`  `24/4 = 6 |
|0    x5|` `2|` `2|` `4|0|1|0|0|46|`  `46/2 = 23|
|0    x6|` `3|` `5|` `6|0|0|1|0|60|`  `60/5 = 12|
|0    x7|` `4|` `8|` `3|0|0|0|1|120|120/8 = 15|
|Zj|` `0|` `0|` `0|0|0|0|0|0||
|Zj - Cj|-10|-22|-18|0|0|0|0|-||

Tablo 4.4’den görüldüğü gibi tüm Zj - Cj ³ 0 olmadığından başlangıçtaki temel uygun çözüm en iyi değildir.

Enb () = 22 olduğundan x2’nin bulunduğu sütun anahtar sütundur. Anahtar satırı belirlemek için çözüm vektörü elemanlarını anahtar sütunun karşılıklı elemanlarına oranlayarak en küçük oranı bulalım. Başlangıç çözüm tablosunun sağ tarafında gösterilen oranlar incelendiğinde, en küçük oranın 6 olduğu ve x4’ün bulunduğu satır için hesaplandığı görülebilir. Buna göre, anahtar satır x4 değişken satırı, anahtar sayı 4 olacaktır. Anahtar sayının belirlenmesinden sonra anahtar satır elemanlarının anahtar sayıya bölünmesi ve anahtar satırın yeni elemanlarının hesaplanması gerekir. Bu işlem aşağıda gösterilmiştir. 

Anahtar satır:    

|[1|4|3|1|0|0|0|24]|
| :- | :- | :- | :- | :- | :- | :- | :- |
olduğuna göre, anahtar satırın yeni elemanları,

|[1/4|4/4|3/4|1/4|0/4|0/4|0/4|24/4]|
| :- | :- | :- | :- | :- | :- | :- | :- |
veya gerekli aritmetik işlemlerin yapılmasıyla aşağıdaki gibi bulunur.

|[1/4|1|3/4|1/4|0|0|0|6]|
| :- | :- | :- | :- | :- | :- | :- | :- |
Bu değerlerin yeni çözüm tablosuna yerleştirilmesinden sonra bu tablonun diğer elemanları hesaplanabilir.

x5 değişken satırından başlayarak diğer satır elemanlarını hesaplayalım. Söz konusu değerler aşağıdaki gibi bulunur.

x5 değişken satırının yeni elemanlarının hesaplanması:

|`      `[2|2|`  `4|`  `0|1|0|0|46]|
| :- | :- | :- | :- | :- | :- | :- | :- |
|(-2)[1/4|1|3/4|` `1/4|0|0|0|`  `6]|
`      `[3/2      0        5/2     -1/2     1      0       0      34]

x6 değişken satırının yeni elemanlarının hesaplanması:

|`      `[3|5|`  `6|`  `0|0|1|0|60]|
| :- | :- | :- | :- | :- | :- | :- | :- |
|(-5)[1/4|1|3/4|1/4|0|0|0|`  `6]|
`      `[7/4       0      9/4      -5/4     0      1       0       30 ]

x7 değişken satırının yeni elemanlarının hesaplanması:

|`      `[4|8|`  `3|`  `0|0|0|1|120]|
| :- | :- | :- | :- | :- | :- | :- | :- |
|(-8)[1/4|1|3/4|1/4|0|0|0|`    `6]|
`      `[2         0       -3        -2        0       0      1       72 ]

Zj değerleri, 

Z1 = 22(1/4) + 0(3/2)  + 0(7/4)   + 0(2)    = 11/2 

Z2 = 22(1)    + 0(0)     + 0(0)      + 0(0)    =   22

Z3 = 22(3/4) + 0(5/2)  + 0(9/4)   + 0(-3)  = 33/2

Z4 = 22(1/4) + 0(-1/2) + 0(-5/4) + 0(-2)  = 11/2

Z5 = 22(0)    + 0(1)     + 0(0)      + 0(0)   =    0 

Z6 = 22(0)    + 0(0)     + 0(1)      + 0(0)   =    0 

Z7 = 22(0)    + 0(0)     + 0(0)      + 0(1)   =    0

Z8 = 22(6)    + 0(34)   + 0(30)    + 0(72) =  132

olarak hesaplanmışlardır.

Zj - Cj değerlerinin hesaplanmasıyla ilgili tüm işlemler aşağıda topluca gösterilmiştir. 

Z1 - C1 = 11/2 - 10 = -9/2

Z2 - C2 = 22    - 22 =    0

Z3 - C3 = 33/2 - 18 = -3/2

Z4 - C4 = 11/2 -  0 = 11/2

Z5 - C5 = Z6 - C6 = Z7 - C7 = 0  -  0 =   0                       

Zj ve Zj – Cj için hesaplanan yeni değerlerle oluşturulan simpleks çözüm tablosu aşağıda gösterilmiştir.

`                                           `***Tablo 4.5***

`                       `***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|x7|ÇV|`    `Oran |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :- |
|22   x2|1/4|1|3/4|1/4|0|0|0|6|`  `6/(1/4) = 24.00|
|`  `0    x5|3/2|0|5/2|-1/2|1|0|0|34|34/(3/2) = 22.33|
|` `0    x6|**7/4**|0|9/4|-5/4|0|1|0|30|30/(7/4) = 17.11 |
|` `0    x7|2|0|-3|-2|0|0|1|72||
|Zj|11/2|22|33/2|11/2|0|0|0|132||
|Zj - Cj|-9/2|0|-3/2|11/2|0|0|0|-|-|

Z1 - C1 = -9/2, Z3 - C3 = -3/2 < 0 olduğundan çözüm en iyi değildir. Birinci tablonun hazırlanmasında yapılan işlemlerin tekrarlanması ve yeni bir tablonun hazırlanması gerekmektedir. 9/2 > 3/2 olduğundan x1 temele alınarak, en küçük oranlı x6 temel olmayan değişken konumuna getirilir. Anahtar sütun x1 değişken sütunu, anahtar satır x6 değişken satırı olduğundan anahtar sayı 7/4 olur. Anahtar işlemlerin uygulanmasıyla oluşturulan yeni çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.6***

***Simpleks İkinci (En iyi) Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|x7|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|22    x2|0|1|3/7|3/7|0|-1/7|0|12/7|
|`  `0    x5|0|0|4/7|4/7|1|-6/7|0|58/7|
|10    x1|1|0|9/7|-5/7|0|4/7|0|120/7|
|`  `0    x7|0|0|-39/7|-4/7|0|-8/7|1|264/7|
|Zj|10|22|156/7|16/7|0|18/7|0|1464/7|
|Zj - Cj|0|0|30/7|16/7|0|18/7|0|-|
Tablodan görüldüğü gibi tüm Zj - Cj ³ 0 olduğundan, tablodaki temel uygun çözüm en iyidir. En iyi olduğu belirlenen bu çözümde; x1 = 120/7,  x2 = 12/7,  x3 =  0, x4 = 0, x5 = 58/7,  x6 = 0 ve x7 = 264/7’dir. Birinci tekrarda 132 olarak hesaplanan Z değeri, bu tekrarda 1464/7 (= 209.42) olarak hesaplanmış olup 209.42, Z için bulunabilecek en büyük değerdir.  

Buraya kadar, simpleks yöntemin tüm kısıtlayıcı fonksiyonları (£) biçiminde olan en büyükleme problemlerine uygulanışı üzerinde durduk. Kısıtlayıcı fonksiyonların (³) veya (=) biçiminde olması durumunda simpleks yöntem nasıl uygulanacaktır?

Tüm kısıtlayıcıların (³) işaretli olduğunu ve problemin aşağıdaki gibi modellendiğini düşünelim.

Zenb = C1x1 + C2x2 + ... + Cnxn

`          `a11x1 + a12x2  +  ...  + a1nxn ³ b1

`          `a21x1 + a22x2  +  … + a2nxn ³ b2

`              `.         .           ...         .         .              

`          `am1x1 + am2x2 +  ...  + amnxn ³ bm

`                     `x1 ³ 0, x2 ³ 0, ..., xn ³ 0

Bilindiği gibi (³) biçimindeki bir fonksiyon sol tarafından negatif olmayan bir artık değişken çıkartılmasıyla eşitlik biçimine dönüştürülür. Artık değişkenlerin modele sokulmasıyla kısıtlayıcı fonksiyonlar aşağıdaki gibi olur.

a11x1 + a12x2  + 	...   + a1nxn -    xn+1 + 0xn+2 +  ... + 0xn+m = b1

a21x1 + a22x2  + 	...   + a2nxn + 0xn+1 -    xn+2 +  ... + 0xn+m = b2

`   `.          .	...   	.           .          .        ...         .  	.

am1x1 + am2x2 + 	...   + amnxn + 0xn+1 + 0xn+2 + ...  -  xn+m   = bm

Artık değişkenler negatif olmadığından, bu modelin negatif olmama koşulu,  

x1, x2, ..., xn, xn+1, xn+2, ..., xn+m ³ 0

olarak düzenlenir.

Standart biçimin kısıtlayıcı fonksiyonları matrislerle şöyle gösterilir.          

Kısıtlayıcı fonksiyonların değişken katsayılarından oluşan m x (n + m) matrisin son m sütununun negatif birim matris oluşturduğu kolayca görülebilir. Böylece eşitlik sisteminin x1 =  x2 = ...= xn = 0 uç noktasındaki başlangıç temel çözümü, xn+1 = -b1, xn+2 = -b2, …, xn+m = -bm olarak belirlenir. Negatif olmayan artık değişkenler için negatif değerler bulunması, bu temel çözümün uygun olmadığına işaret eder. Bu nedenle, negatif olmama koşulunu gerçekleyen diğer bir başlangıç çözümünün araştırılması zorunludur. Başlangıç çözümünü araştırmanın yolu, önceden olduğu gibi katsayılar matrisi yanında bir birim matris oluşturmaktır. Birim matris oluşturmak için artık değişkenlerle eşitlik biçimine dönüştürülen kısıtlayıcı fonksiyonlara negatif olmayan birer *yapay değişken* eklenir. Yapay değişkenlerin hiçbir fiziki yorumu yoktur, bunlar yalnızca bir başlangıç uygun çözüme ulaşmak amacıyla, (³) işaretli kısıtlayıcılara eklenen değişkenlerdir. Bu değişkenler Ai (i = 1, 2, ..., m)  ile gösterildiğinde,  kısıtlayıcılar aşağıdaki gibi elde edilir ([^5]).

a11x1 + a12x2  + 	...   + a1nxn -  xn+1 + A1                                            = b1

a21x1 + a22x2  + 	...   + a2nxn                   -  xn+2 + A2                                 = b2

`    `.          .           ...         .           .          .          .    …       .          .          

am1x1 + am2x2 +   ...   + amnxn         .       .        .       .    …    - xn+m + Am = bm

Tüm değişkenler negatif olmadığından, negatif olmama koşulu şöyle olur.

x1, x2, ..., xn, xn+1, xn+2, ..., xn+m, A1, A2, ..., Am ³ 0

Yapay değişkenlerin eklenmesiyle kısıtlayıcı fonksiyonlara ilişkin katsayılar matrisi şöyle gösterilir.  

Kısıtlayıcı fonksiyon katsayılarından oluşan matrisin son m sütununun bir birim matris oluşturduğu görülebilir.

x1 = 0, x2 = 0, ..., xn = 0, xn+1 = 0, xn+2 = 0, ..., xn+m = 0 

olduğunda, söz konusu kısıtlayıcılar aşağıdaki başlangıç temel çözümü verir.

A1 = b1, A2 = b2, …, Am = bm  

Bilindiği gibi aylak ve artık değişkenlerin amaç fonksiyonundaki katsayıları sıfırdır. Yapay değişkenler için durum farklıdır. Yukarıda belirtildiği gibi, ilk temel uygun çözümün bulunmasına yardımcı olmalarına karşın hiçbir fiziki ve ekonomik anlamı olmayan bu yapay değişkenlerin en iyi çözüme girmeleri engellenmelidir. Bunu sağlamak için yapay değişkenlerin amaç fonksiyonundaki katsayılarının çok büyük olduğu düşünülür.

Büyük değerli katsayılar genellikle M ile gösterildiğinden, uygulanacak simpleks yöntemi *büyük M* *yöntemi* olarak adlandırılır. Bu yönteme *Charnes’in M yöntemi* de denilmektedir. Büyük M yöntemi, yalnızca en büyükleme problemlerine değil en küçükleme problemlerine de uygulanır. En büyükleme problemlerinde M mutlak değerce çok büyük bir negatif sayı olarak alınır. Böylece, temelde pozitif değerli bir yapay değişken kaldığında, amaç fonksiyonu değerinin arttırılması mümkün olmaz. Bu yolla yapay değişkenlerin çözüme girmeleri engellenir. Problem en küçükleme problemi olduğunda, yapay değişkenlerin amaç fonksiyonundaki katsayıları çok büyük pozitif sayılar olarak alınır. Böylece, en büyükleme durumunda olduğu gibi yapay değişkenlerin en iyi çözümün temeline girmeleri engellenir([^6]).

Kısıtlayıcı fonksiyonlarının tümü (³) işaretli olan bir doğrusal programlama probleminin büyük M yöntemiyle çözümü aşağıdaki örnek problemde açıklanmıştır. 

***Örnek 4.4***: Aşağıdaki doğrusal programlama problemini simpleks yöntemle çözünüz.

Zenb = -2x1 - 3x2 - x3

`             `x1 + 4x2 + 2x3 ³ 8

`           `3x1 + 2x2 +   x3 ³ 6

`                     `x1, x2, x3 ³ 0

***Çözüm 4.4***: Simpleks yöntemle çözüm yapabilmek için önce eşitsizlikleri eşitlik biçiminde yazalım. Her bir kısıtlayıcı fonksiyona birer yapay değişken eklenir, aynı kısıtlayıcılardan birer artık değişken çıkartılırsa örnek problemin modeli simpleks yöntem için uygun biçime dönüştürülmüş olur([^7]).

Zenb = -2x1 - 3x2 - x3 + 0x4 + 0x5 - MA1 - MA2  

`              `x1 + 4x2 + 2x3 - x4 + A1         = 8

`            `3x1 + 2x2 +   x3 - x5         + A2 = 6

`                       `x1, x2, x3, x4, x5, A1, A2 ³ 0 

Standart biçimdeki bilgilerin kullanılmasıyla oluşturulan tablo aşağıda gösterilmiştir.

`		   	           `***Tablo 4.7***

`           	                `***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|Oran|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :- |
|` `-M   A1|1|**4**|2|-1|` `0|1|0|8|8/4 = 2 |
|-M   A2|3|2|1|` `0|-1|0|1|6|6/2 = 3|
|Zj|-4M|-6M|-3M|M|M|M|M|-14M||
|Zj - Cj|-4M+2|-6M+3|-3M+1|M|M|0|0|-||
Bu kez başlangıç tablosundaki Zj değerlerinin, önceki iki örnek problemin başlangıç tablolarındaki Zj değerlerinden farklı olarak sıfır olmadığına dikkat edilmelidir. Bunun nedeni başlangıçtaki temel değişkenlerinin amaç fonksiyonu katsayılarının sıfırdan farklı olmasıdır. Buna göre Zj değerleri aşağıdaki gibi hesaplanır. 

Z1 = (-M)(1)  + (-M)(3)  =   -4M

Z2 = (-M)(4)  + (-M)(2)  =   -6M  

Z3 = (-M)(2)  + (-M)(1)  =   -3M

Z4 = (-M)(-1) + (-M)(0)  =      M

Z5 = (-M)(0)  + (-M)(-1) =      M

Z6 = (-M)(1)  + (-M)(0)  =     -M

Z7 = (-M)(0)  + (-M)(1)  =     -M

Z8 = (-M)(8)  + (-M)(6)  = -14M

Zj değerlerinden o sütunlarla ilgili değişkenlerin amaç fonksiyonundaki katsayılarının çıkartılmasıyla,  

Z1 - C1 = (-4M) - (-2)   = -4M + 2

Z2 - C2 = (-6M) - (-3)   = -6M + 3

Z3 - C3 = (-3M) - (-1)   = -3M + 1 

Z4 - C4 =      M  -  (0)   =    M 

Z5 - C5 =      M  -  (0)   =    M

Z6 - C6 =   (-M) - (-M) = 0

Z7 - C7 =   (-M) - (-M) = 0

olarak hesaplanmıştır. 

Yukarıdaki işlemlerin tamamlanıp başlangıç tablosunun düzenlenmesinden sonra, çözümden çıkacak ve çözüme girecek değişkenler belirlenir.

M çok büyük bir sayı olarak  tanımlandığından, Zj - Cj  satırındaki   mutlak  değerce en büyük negatif sayı (-6M+3)’dür. O halde, x2 değişken sütunu anahtar sütun olacak, yani x2 bir sonraki tabloda temel değişken olarak işlem görecektir.

Çözümden  çıkacak değişken, önceden olduğu gibi, oranların hesaplanmasıyla belirlenir. Başlangıç tablosunun sağ tarafındaki oranlar incelendiğinde, en küçük olanın A1 değişken satırı için hesaplandığı görülebilir. O halde, A1 çözümden çıkacak yerine x2 girecektir.

Anahtar sayının 4 olduğunun belirlenmesinden sonra gerçekleştirilen anahtar işlemlerle yeni çözüm tablosu aşağıdaki gibi olur.

Tablo 4.8’den görüldüğü gibi, Tablo 4.7’deki başlangıç çözümünde (-14M)’e eşit olan Z değeri bu çözümde (-2M-6)’ya yükselmiştir. Birinci çözümün verildiği Tablo 4.8’in son satırı incelendiğinde, bu değerin daha da artacağı görülebilir. Zira, en iyi çözüme ulaşılıp ulaşılmadığının araştırılmasında kullanılan son satırda hala negatif değerler vardır.

***Tablo 4.8***

***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|-3      x2|1/4|` `1|` `1/2|-1/4|` `0|` `1/4|0|2|
|-M    A2|**5/2**|` `0|` `0|` `1/2|-1|-1/2|1|2|
|Zj||-3|-3/2||M||-M|-2M-6|
|Zj - Cj||` `0|-1/2||M||0|-|
Mutlak değerce en büyük negatif değer [(5 - 10M)/4] olduğundan, x1 ikinci simpleks tabloda temel değişken olarak işlem görecektir. Oranlar birinci satır için 8, ikinci satır için (4/5) olarak hesaplandığından, A2 temeli terkeden değişken olur. Anahtar sayının (5/2) olduğunun belirlenmesinden sonra simpleks yöntemin standart işlemleriyle yeni çözüm tablosu aşağıdaki gibi olur.
##### ***Tablo 4.9***
##### ***Simpleks İkinci Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|-3    x2|`  `0|`  `1|` `**1/2**|-3/10|1/10|` `3/10|-1/10|9/5|
|-2    x1|`  `1|`  `0|` `0|` `1/5|-2/5|-1/5|2/5|4/5|
|Zj|-2|-3|-3/2|1/2|` `1/2|-1/2|-1/2|-7|
|Zj - Cj|` `0|` `0|-1/2|` `1/2|` `1/2|||-|

Z3 - C3 < 0 olduğundan, tablodaki çözüm en iyi değildir. x3 temele alınarak en  küçük oranlı x2 temelden çıkartılır. Anahtar sayının 1/2 olduğunun belirlenmesinden sonra standart işlemler uygulanır. Elementer satır işlemlerinin gerçekleştirilmesiyle ulaşılan yeni çözüm tablosu aşağıda verilmiştir.
##### ***Tablo 4.10***
***Simpleks Üçüncü (En iyi) Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|` `-1     x3|0|2|1|-3/5|1/5|3/5|-1/5|18/5|
|` `-2      x1|1|0|0|1/5|-2/5|-1/5|2/5|4/5|
|Zj|-2|-2|-1|1/5|3/5|-1/5|-3/5|-26/5|
|Zj - Cj|0|1|0|1/5|3/5|||-|
Tablo 4.10’daki temel uygun çözümde tüm Zj - Cj ³ 0 olduğundan çözüm en iyidir. Bu çözümde, x1 = 4/5, x2 = 0, x3 = 18/5, x4 = 0, x5 = 0,  A1 = 0, A2 = 0 olarak belirlenmiştir. Amaç fonksiyonunun en büyük değeri Zenb = -26/5’dir. 

Buraya kadar kısıtlayıcı fonksiyonlarının tamamı ya (£) veya (³) işaretli olan problemler üzerinde durulmuştur. Oysa kısıtlayıcı fonksiyonlardan bir ya da bir kaçı veya hepsi (=) biçiminde olabilir. Kısıtlayıcılar (=) biçiminde olduğundan, aylak değişken eklenmesi gerekmeyecek dolayısıyla, modelin dönüştürülmüş biçimi aynı kalacaktır. Kısıtlayıcılar aylak değişkene sahip olmadığı için de başlangıç temel uygun çözüme ulaşılamayacaktır. Bu sorunu ortadan kaldırmak, yani birim matris oluşturmak amacıyla eşitlik biçimindeki kısıtlayıcı fonksiyonların sol taraflarına (+1) katsayılı yapay değişkenler eklenir. Yapay değişkenlerin amaç fonksiyonundaki katsayıları önceden açıklandığı gibi, en büyükleme problemlerinde çok büyük bir negatif sayı (-M), en küçükleme problemlerinde çok büyük bir pozitif sayıdır (M). Bu yolla, yapay değişkenlerin en iyi çözümün temeline girmeleri engellenmiş olur. 

İleride açıklanacağı gibi, en iyi çözümde yapay değişkenin bulunması durumunda çözüm uygun değildir veya kısıtlayıcı fonksiyonlar çelişiktir denir.

***Örnek 4.5***: Aşağıdaki doğrusal programlama problemini simpleks yöntemle çözünüz.

Zenb = 21x1 + x2 + x3

`             `2x1 +   x2 + 4x3 = 20

`               `x1 + 3x2 + 4x3 = 30

`                        `x1, x2, x3 ³ 0

***Çözüm 4.5***: Kısıtlayıcılar eşitlik biçiminde olduğundan, her birine (+1) katsayılı yapay değişken eklenmesi gerekir. Bu yolla elde edilen model aşağıda gösterilmiştir.

Zenb = 21x1 + x2 + x3 - MA1 - MA2

`            `2x1 +   x2 + 4x3 + A1         = 20

`              `x1 + 3x2 + 4x3         + A2 = 30

`                           `x1, x2, x3, A1, A2 ³ 0

Simpleks yöntemle çözüm yapabilmek için başlangıç tablosunu düzenleyelim. Bu amaçla düzenlenen simpleks başlangıç çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.11***

***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|-M   A1|` `2|1|**4**|` `1|` `0|20|
|-M   A2|` `1|3|4|` `0|` `1|30|
|Zj|-3M|-4M|-8M|-M|-M|-50M|
|Zj - Cj|-3M-21|-4M-1|-8M-1|` `0|` `0|-|
Başlangıç tablosundaki Zj ve Zj - Cj değerleri aşağıdaki gibi bulunur.

Z1 = (-M)(2)   + (-M)(1)   =   -3M,    Z1 - C1 = -3M - 21

Z2 = (-M)(1)   + (-M)(3)   =   -4M,    Z2 - C2 = -4M - 1

Z3 = (-M)(4)   + (-M)(4)   =   -8M,    Z3 - C3 = -8M - 1

Z4 = (-M)(1)   + (-M)(0)   =     -M,    Z4 - C4 =   -M - (-M) = 0

Z5 = (-M)(0)   + (-M)(1)   =     -M,    Z5 - C5 =   -M - (-M) = 0

Z6 = (-M)(20) + (-M)(30) = -50M

Z1 - C1,  Z2 - C2, Z3 - C3 < 0 olduğundan, başlangıçtaki temel uygun çözüm en iyi değildir. M çok  büyük  bir  sayı  olarak  tanımlandığından, mutlak değerce en büyük negatif Zj - Cj = Z3 - C3 =  (-8M-1)’dir. Bu durumda x3’ün bulunduğu sütun anahtar sütundur. En küçük değerli oran A1’e ait olduğundan A1’in temeli terketmesi kararlaştırılır. Anahtar sayının 4 olduğunun belirlenmesinden sonra elementer işlemlerle elde edilen bigilerle oluşturulan yeni çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.12***

***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x3|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1     x3|1/2|1/4|1|1/4|0|5|
|-M    A2|-1|**2**|0|-1|1|10|
|Zj|||1||-M|-10M+5|
|Zj - Cj|||0||0|-|
Z2 - C2 < 0 olduğundan Tablo 4.12’deki çözüm en iyi değildir ve x2’nin temele alınması gerekir. Oranlar incelendiğinde, çözümü terkedecek değişkenin A2 olduğu görülür. Anahtar sayı 2’dir. Simpleks yöntemin standart işlemlerinin uygulanmasıyla bulunan değerlerle oluşturulan yeni çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.13***

***Simpleks İkinci Çözüm Tablosu***

|TDV|x1|x2|x3|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1    x3|` `**5/8**|0|1|3/8|-1/8|15/4|
|1    x2|-1/2|1|0|-1/2|` `1/2|5|
|Zj|1/8|1|1|-1/8|3/8|35/4|
|Zj - Cj|-167/8|0|0|||-|
Z1 - C1 < 0 olduğundan en iyi çözüme henüz ulaşılamamıştır. x1 değişken sütununun anahtar sütun, x3 değişken satırının anahtar satır, anahtar sayının 5/8 olduğunun belirlenmesinden sonra belirlenen üçüncü çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.14***

***Simpleks Üçüncü (En İyi) Çözüm Tablosu***

|TDV|x1|x2|x3|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|21   x1|1|0|8/5|` `3/5|-1/5|6|
|1    x2|0|1|4/5|-1/5|`  `2/5|8|
|Zj|21|1|172/5|62/5|-19/5|134|
|Zj - Cj|0|0|167/2|||-|
Son satırın tüm elemanları ³ 0 olduğundan, en iyi çözüm elde edilmiştir. Bu en iyi çözümde, x1 = 6, x2 = 8, x3 = x4 = x5 = 0 ve Zenb = 134’dür. 

Şimdiye kadar simpleks yöntemi kısıtlayıcı fonksiyonları (³), (£) veya (=) biçiminde olan en büyükleme problemlerine uyguladık ve açıkladık. Oysa yöntem sadece en büyükleme problemlerine değil, en küçükleme problemlerine de uygulanır.

Problem en küçükleme türünde olduğunda simpleks yöntem nasıl uygulanacaktır? 4.2. kesimde açıklandığı gibi, herhangi bir en büyükleme problemi en küçükleme problemine veya en küçükleme problemi en büyükleme problemine dönüştürülebilir. Bu dönüştürme sonucunda orijinalinde en küçükleme amaçlı olan doğrusal programlama problemi, en büyükleme problemlerinin çözümünde kullanılan ardışık işlemlerle çözülebilir.

En küçükleme problemleri en iyilemenin anlamını değiştirmeksizin de çözülebilir. Simpleks yöntemin en küçükleme problemlerine uygulanışı ile en büyükleme problemlerine uygulanışı arasında çok büyük fark olduğu söylenemez. Aralarındaki en önemli fark anahtar sütunun seçiminde kullanılan ölçüttür. En küçükleme  problemlerinde,  en büyükleme problemlerdekinin tersine en büyük  pozitif  Zj - Cj’ye sahip değişken temele girer. Problemin niteliği gereği bütün Zj - Cj değerleri £ 0 olduğunda en iyi çözüme ulaşılmış olur.

En küçükleme probleminin simpleks yöntem ile çözümü Örnek 4.6 üzerinde açıklanacaktır.

***Örnek 4.6***: Aşağıdaki doğrusal programlama problemini simpleks yöntemle çözünüz.

Zenk = 3x1 + 2x2 + x3

`           `2x1 + 3x2 + x3 ³ 21

`              `x1 +  x2 + x3 ³ 12

`                    `x1, x2, x3 ³ 0

***Çözüm 4.6***: Önceden olduğu gibi öncelikle problemin standart biçimde yazılması gerekmektedir. Yukarıda yapılan açıklamalar doğrultusunda eklenen ve çıkartılan değişkenlerle problemin standart biçimi aşağıdaki gibi elde edilir. 

Zenk = 3x1 + 2x2 + x3 + 0x4 + 0x5 + MA1 + MA2

`           `2x1 + 3x2 + x3 - x4 + A1         = 21

`             `x1 +   x2 + x3 - x5         + A2 = 12

`                    `x1, x2, x3, x4, x5, A1, A2 ³ 0

Problemin standart biçimindeki bilgilerin kullanılmasıyla düzenlenen başlangıç çözüm tablosu aşağıda gösterilmiştir. 

***Tablo 4.15***

***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|M    A1|2|**3**|1|-1|` `0|1|0|21|
|M    A2|1|1|1|` `0|-1|0|1|12|
|Zj|3M|4M|2M|-M|-M|M|M|33M|
|Zj - Cj|3M-3|4M-2|2M-1|-M|-M|0|0|-|
Tablo 4.15’in son satırından görüldüğü gibi Z1 - C1, Z2 - C2, Z3 - C3 > 0 olduğundan, en küçükleme amaçlı problem için belirlenen başlangıç temel uygun çözüm en iyi değildir. Enb(3M-3, 4M-2, 2M-1) = 4M-2 olduğundan, x2 temele alınır. En küçük oran (7) A1 değişken satırı için hesaplandığından, A1’in bir sonraki tabloda temelde bulunmaması kararlaştırılır.

Anahtar sayının 3 olduğunun belirlenmesinden sonra öncekinden daha gelişmiş çözümü içeren Tablo 4.16’yı oluşturacak değerler hesaplanır. Yeni değerlerle oluşturulan birinci çözüm tablosu aşağıda gösterilmiştir. 

***Tablo 4.16***

***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|2     x2|2/3|1|1/3|-1/3|` `0|` `1/3|0|7|
|M   A2|1/3|0|**2/3**|1/3|-1|-1/3|1|5|
|Zj||2|||-M||M|5M+14|
|Zj - Cj||0|||-M||0|-|
Birinci çözümün yer aldığı Tablodan görüldüğü gibi Z1 - C1, Z3 - C3, Z4 - C4 > 0’dır. O halde, en iyi çözüme henüz ulaşılamamıştır ve çözüm daha geliştirilebilir. En büyük pozitif Zj - Cj, x3’e ait olduğundan, x3 bir sonraki çözümün temelinde bulunacaktır.

Anahtar satırın A2 değişken satırı, anahtar sayının (2/3) olduğunun belirlenmesinden sonra gerekli işlemlerin tamamlanmasıyla düzenlenen tablo aşağıda gösterilmiştir. 

***Tablo 4.17***

***Simpleks İkinci (En İyi) Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|2     x2|1/2|1|0|-1/2|1/2|1/2|-1/2|9/2|
|1     x3|1/2|0|1|` `1/2|-3/2|-1/2|` `3/2|15/2|
|Zj|3/2|2|1|-1/2|-1/2|` `1/2|` `1/2|33/2|
|Zj - Cj|-3/2|0|0|-1/2|-1/2|||-|
Tüm  Zj - Cj £ 0 olduğundan, en iyi çözüme ulaşılmış ve x1 = 0, x2 =  9/2, x3 = 15/2, x4 = 0, x5 = 0, A1 = 0, A2 = 0 ve Zenk = 33/2 olarak belirlenmiştir. 
## ***4.4  SİMPLEKS  YÖNTEM UYGULAMASINDA***
## `      `***KARŞILAŞILAN ÖZEL DURUMLAR***
`	`Grafikle çözümde olduğu gibi, simpleks yöntemin uygulanması sırasında da ele alınan problemin niteliğine göre bazı özel durumlar ve bunlarla ilgili sorunlar ortaya çıkabilir. Bu kesimde, ortaya çıkabilecek önemli sorunlar, bunların simpleks çözüme ne şekilde yansıdıkları ve nasıl giderildikleri konuları üzerinde durulacaktır.
### ***4.4.1 Temele Girecek Değişken Katsayılarının Eşit Olması***
`	`Bilindiği gibi, doğrusal programlama problemlerinde amaç fonksiyonunun değeri temel olmayan değişkenlerden birinin temele alınmasıyla geliştirilmektedir. En büyükleme problemlerinde Z’nin değerini en hızlı biçimde büyütebilmek için mutlak değerce en büyük negatif Zj - Cj’ye sahip değişken temele alınır. En küçükleme problemlerinde ise temele girecek değişken (Zj - Cj)’nin en büyük pozitif değerine sahiptir.

Bazı  durumlarda iki  ya da daha  fazla sayıdaki değişken aynı en büyük (veya en küçük) Zj - Cj’ye sahip olabilir. Bu durum hangi değişkenin temele alınması gerektiği konusunda kararsızlığa yol açar. Bu gibi durumlarda kararsızlık yaratan değişkenlerden rasgele seçilen herhangi biri temele alınabilir. Ancak, bu yöntem en iyi çözüme ulaşmayı uzatabileceğinden fazla tatminkar değildir. En iyi çözüme ulaşmada daha az tekrarı garanti etmemekle birlikte, en küçük sayının bulunduğu sütun değişkeninin temele alınması önerilebilir. Böyle bir durumda kullanılabilecek diğer bir yaklaşım ise, çözüm vektörünün elemanlarının anahtar sütun olmaya aday sütunların elemanlarına bölünmesiyle elde edilen oranlar arasından en küçük pozitif değerin bulunduğu sütunun anahtar sütun olarak seçilmesidir. Aynı en küçük pozitif değerli oranların birden fazla olması da özel bir durumdur. Bu konu izleyen kesimde ayrıntılı bir biçimde açıklanacaktır.

Anahtar sütun seçiminde kararsızlığın yaşandığı bir örnek aşağıda verilmiştir.

***Örnek 4.7***: Aşağıdaki doğrusal programlama problemini simpleks yöntemle çözünüz. 

Zenb = 8x1 + 8x2 + 6x3

`          `2x1 + 3x2 + 4x3 £ 12

`            `x1 + 2x2 +   x3 £   4

`          `3x1 + 5x2          £ 10

`                     `x1, x2, x3 ³ 0

***Çözüm 4.7***: Problemin standart biçimi aşağıda verilmiştir. 

Zenb = 8x1 + 8x2 + 6x3 + 0x4 + 0x5 + 0x6

`          `2x1 + 3x2 + 4x3 + x4               = 12

`            `x1 + 2x2 +   x3        + x5        =   4

`          `3x1 + 5x2                         + x6 = 10

`                           `x1, x2, x3, x4, x5, x6 ³ 0

Standart biçimden hareketle düzenlenen başlangıç çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.18***

***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0    x4|2|3|4|1|0|0|12|
|0    x5|1|2|1|0|1|0|4|
|0    x6|**3**|5|0|0|0|1|10|
|Zj|0|0|0|0|0|0|0|
|Zj - Cj|-8|-8|-6|0|0|0|-|
Tablo 4.18’den görüldüğü gibi tüm Zj - Cj £ olduğundan, tablodaki çözüm en iyi değildir. Aynı en büyük negatif değerli birden fazla Zj - Cj (Z1 – C1 ve Z2 – C2) olduğundan anahtar sütun seçiminde kararsızlığa düşülmüştür. Bu sorunu ortadan kaldırmak için en küçük sayının bulunduğu sütunu belirleyelim([^8]).

Her iki sütunun elemanlarının en küçüğü olan 1, x1 değişken sütununda bulunduğundan, x1’in temele alınması uygun olur.

En küçük oran x6 değişkeni için hesaplandığından, anahtar satır x6 değişken satırıdır. Bu durumda anahtar sayı 3 olur. Simpleks yöntemin standart işlemleriyle oluşturulan yeni çözüm tablosu aşağıda verilmiştir. 

***Tablo 4.19***

***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x4|0|-1/3|4|1|0|-2/3|16/3|
|0     x5|0|1/3|**1**|0|1|-1/3|2/3|
|8     x1|1|5/3|0|0|0|1/3|10/3|
|Zj|8|40/3|0|0|0|8/3|80/3|
|Zj - Cj|0|16/3|-6|0|0|8/3|-|
Tablo 4.19’dan görüldüğü gibi Z3 - C3 < 0 olduğundan, tablodaki çözüm en iyi değildir. Daha gelişmiş bir çözüm için x3 temele alınmalıdır. En küçük oran x5’e ait olduğundan x5 temelden çıkartılır. Buna göre anahtar sayı 1 olur. Simpleks yöntemin standart işlemleriyle yeni çözüm tablosu aşağıdaki gibi olur.  

***Tablo 4.20***
##### ***Simpleks İkinci (En İyi) Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x4|0|-5/3|0|1|-4|` `2/3|8/3|
|6     x3|0|` `1/3|1|0|1|-1/3|2/3|
|8     x1|1|` `5/3|0|0|0|` `1/3|10/3|
|Zj|8|46/3|6|0|6|` `2/3|92/3|
|Zj - Cj|0|22/3|0|0|6|` `2/3|-|
Görüldüğü gibi ikinci denemede elde edilen Zj - Cj satır elemanlarının hepsi ³ 0 olduğundan, en iyi çözüme ulaşılmıştır. Bu en iyi çözümde x1 = 10/3, x2 = 0, x3 = 2/3, x4 = 8/3, x5 = 0, x6 = 0, Zenb = 92/3’dür.
### `	`***4.4.2 Bozulma Durumu***
`	`Doğrusal programlama problemlerinin çözümünde karşılaşılan diğer bir sorun da bozulma (dejenarasyon) durumudur. Bozulma durumu anahtar satır seçiminde kendisini gösterir. Anahtar satırın belirlenmesi amacıyla hesaplanan oranlar arasında aynı en küçük değere sahip olanların sayısı birden fazla ise bozulma var demektir. Bozulma durumuna başlangıç çözümünde veya ara çözümlerden herhangi birinde rastlanabilir. Bozulmanın giderilebilmesi için çeşitli yöntemlere başvurulabilir. Eşit orana sahip değişkenlerden rasgele seçilen bir tanesi temelden çıkartılarak işlemler sürdürülebilir. Ancak böyle bir yaklaşım, birtakım karışıklıklara neden olabilir. Rasgele seçim sonucunda tekrar tekrar aynı çözüm tablosunu veren bir kısır döngüye girilmesi kaçınılmaz olabilir. Seçimin uygun olması durumunda bozulma hızlı bir şekilde giderilebilecektir. Anahtar satır seçiminde kullanılan diğer bir yaklaşım ise yaygın bir kullanım alanı bulmuş olan *Charnes’in karıştırma yöntemidir*. Yöntem aşağıdaki işlemlerin sırasıyla izlenmesiyle uygulanır. 

1. Bozulmanın ortaya çıktığı tabloda anahtar satır olmaya aday satırların başlangıçtaki temel değişkenlerin bulunduğu yerdeki matrisin([^9]) ilk sütununa rastlayan elemanları, bire bir olmak koşuluyla anahtar sütun elemanlarına bölünür.
1. Birinci adımda hesaplanan oranlardan en küçük değerlisinin bulunduğu satır anahtar satır olarak seçilir. 

İlk bölme işleminde bulunan en küçük oranların değerleri birbirlerine eşit olursa tekrar birinci adıma geçilir. Aynı işlemler yukarıda sözü edilen matrisin ikinci sütununa uygulanır. Eşitlik yine bozulmazsa, aynı işlemler eşit olmayan iki orana rastlanıncaya kadar sürdürülür. Bu matrisin sütunlarıyla ilgili işlemler tamamlandığı halde eşitlik bozulmamışsa, işlemler gövdeyi oluşturan matrisin birinci sütunundan başlamak üzere uygulanır. 

Bu durumu aşağıdaki problem üzerinde inceleyelim.

***Örnek 4.8***: Aşağıdaki doğrusal programlama problemini simpleks yöntemle çözünüz.

Zenb = 8x1 + 6x2 + 5x3

`          `3x1 + 4x2 + 5x3 £ 12

`          `2x1           + 5x3 £  8

`            `x1 + 4x2 + 2x3 £  4

`                     `x1, x2, x3 ³ 0

***Çözüm 4.8***: Problemin standart biçimi aşağıda gösterilmiştir.

Zenb = 8x1 + 6x2 + 5x3 + 0x4 + 0x5 + 0x6

`          `3x1 + 4x2 + 5x3 + x4              	= 12

`          `2x1          + 5x3        + x5         	=  8

`            `x1 + 4x2 + 2x3               + x6 	=  4

`                           `x1, x2, x3, x4, x5, x6 	³  0

Problem için hazırlanan simpleks başlangıç çözüm tablosu aşağıda gösterilmiştir. 

`                                                  `***Tablo 4.21***

`                            `***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|Oran|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :- |
|0     x4|`  `3|` `4|`  `5|1|0|0|16/3|12/3 = 4|
|0     x5|`  `2|` `0|`  `5|0|1|0|` `2/3|`  `8/2 = 4|
|0     x6|`  `1|` `4|`  `2|0|0|1|10/3|`  `4/1 = 4|
|Zj|`  `0|` `0|`  `0|0|0|0|80/3||
|Zj - Cj|-8|-6|-5|0|0|0|-||
Başlangıç temel uygun çözümün bulunduğu Tablo 4.21’den görüldüğü gibi çözüm en iyi değildir ve enb= Z1 - C1 = 8 olduğundan x1 temele alınmalıdır. Temelden çıkacak değişkenin belirlenmesi amacıyla hesaplanan oranlar tablonun sağ tarafında oranlar başlığı altında gösterilmiştir. Anahtar satır seçiminde kullanılacak olan bu oranlar incelendiğinde (bkz. Tablo 4.21) üçünün birden en küçük değerde olduğu görülecektir. Sonuç olarak, anahtar satırın seçiminde bir kararsızlık söz konusudur. Bu kararsızlıktan kurtulmak için Charnes’in yöntemini kullanalım. Önce, eşit oranlı satırlardaki her bir elemanı bulunduğu satırın anahtar sütun üzerindeki sayısına bölelim. Bu uygulamayla elde edilen oranlar aşağıda gösterilmiştir.

|TDV|x1|x2|x3|x4|x5|x6|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|x4|3/3|4/3|5/3|1/3|0/3|0/3|
|x5|2/2|0/2|5/2|0/2|1/2|0/2|
|x6|1/1|4/1|2/1|0/1|0/1|1/1|

İlk önce birim matristen başlayarak eşit olmayan oranlara rastlayıncaya  kadar oranları karşılaştıralım. Görüldüğü gibi, birim matrisin her sütununda en küçük değerli oran olan sıfıra her seferinde iki satırda rastlanmaktadır. O halde, gövdeye geçmek gerekmektedir. Gövdeye geçildiğinde x2’ye ait sütunda üç farklı oran olduğu görülür. Bu oranlar arasından en küçük değerli olan x5 değişken satırı için hesaplandığından anahtar satır x5 değişken satırıdır.

Anahtar sütun ve satırın belirlenmesi ve bilinen işlemlerin tekrarlanmasıyla aşağıdaki tabloya ulaşılır. 

***Tablo 4.22***

***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x4|0|` `4|-5/2|1|-3/2|0|0|
|8     x1|1|` `0|`  `5/2|0|1/2|0|4|
|0     x6|0|` `**4**|-1/2|0|-1/2|1|0|
|Zj|8|` `0|` `20|0|` `4|0|32|
|Zj - Cj|0|-6|` `15|0|` `0|0|-|
Tablo 4.22’den görüldüğü gibi bir önceki adımda sorun yaratan değişkenlerden x4 ve x6’nın temel çözümdeki değerleri sıfırdır. x4 ve x6 temel değişkenlerinin pozitif olması beklenen çözüm değerlerinin sıfır olarak elde edilmesinin nedeni bu değişkenler arasında bağ olmasıdır. Z2 - C2 = 6 < 0 olduğundan çözüm en iyi değildir. x2 temele alınmalıdır.

x2 değişken sütununun anahtar sütun olarak seçilmesi sonucunda anahtar satır olmaya  aday  iki satır bulunduğu görülür. Anahtar satır olmaya aday iki satırdan hangisinin anahtar satır olmaya uygun olduğunu Charnes’in yaklaşımıyla belirleyelim.

Yukarıda açıklandığı gibi hesaplanan oranlar, x6 değişken satırının anahtar satır olarak seçilmesinin uygun olduğunu göstermiştir. Bu durumda anahtar sayı 4 olacaktır.

Bu belirlemelerin ardından simpleks yöntemin klasik anahtar işlemleriyle elde edilen yeni çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.23***
##### ***Simpleks İkinci (En iyi) Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x4|0|0|-2|1|-1|-1|0|
|8     x1|1|0|`  `5/2|0|`  `1/2|0|4|
|6     x2|0|1|-1/8|0|-1/8|1/4|0|
|Zj|8|6|` `77/4|0|13/4|3/2|32|
|Zj - Cj|0|0|` `57/4|0|13/4|3/2|-|
Tablo 4.23’ün tüm Zj - Cj değerleri ³ 0 olduğundan en iyi çözüme ulaşılmıştır. En iyi olan bu çözüm incelendiğinde yine iki değişkenin (x4 ve x2) temelde bulunmalarına rağmen çözüm değerlerinin sıfır olduğu görülebilir. Burada olduğu gibi, temel değişkenlerden bir ya da birkaçının en iyi çözüm değerinin sıfır olduğu bu tür temel uygun çözümlere *bozuk en iyi çözüm* denir. 
### ***4.4.3 Sınırsız Çözüm*** 
` 	`Simpleks yöntemle çözüm yaparken gerçekleşmesi muhtemel bir özel durum da sınırsız çözüm durumudur. Sınırsız çözüm, uygun çözüm bölgesinin belli bir sınırının olmaması durumunda ortaya çıkar ve amaç fonksiyonunun her tekrarda gittikçe artan değerler alması durumunu gösterir. Böyle bir durumda, çözüme girecek değişkenin değeri, buna bağlı olarak amaç fonksiyonunun değeri sınırsız artar ve bir türlü en iyi olan çözüme ulaşılamaz.

Bazı durumlarda uygun çözüm bölgesinin belli bir sınırı olmasa da en iyi çözüme ulaşılabilir. Bu, *sınırsız çözüm bölgesi*-*sınırlı en iyi çözümü* ifade eder. Herhangi bir doğrusal programlama probleminin sınırsız çözüme sahip olup olmadığı anahtar sütun elemanlarının incelenmesiyle anlaşılır. Problemin türü ne olursa olsun, çözümün herhangi bir aşamasında anahtar sütun olarak belirlenen sütunun tüm elemanları negatif değerli olursa çözüm sınırsızdır. Aşağıda sınırsız çözüm durumunu yansıtan bir örnek problem verilmiştir.

***Örnek 4.9***: Aşağıdaki doğrusal programlama problemini simpleks yöntemle çözünüz.

Zenb = 2x1 + 5x2 + 9x3   

`            `x1 +   x2 + 4x3 ³ 12

`            `x1 +   x2 +   x3 ³   4

`                     `x1, x2, x3 ³  0

***Çözüm 4.9***: Problemin standart biçimi aşağıda verilmiştir.

Zenb = 2x1 + 5x2 + 9x3 + 0x4 + 0x5 - MA1 - MA2

`            `x1 +  x2 + 4x3 - x4        + A1         = 12

`            `x1 +  x2 +   x3        - x5         + A2  =  4

`                            `x1, x2, x3, x4, x5, A1, A2 ³ 0

Simpleks yöntemle çözüm için hazırlanan başlangıç tablosu aşağıda gösterilmiştir.

***Tablo 4.24***

***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|-M     A1|` `1|1|**4**|-1|` `0|` `1|1|12|
|-M     A2|` `1|1|1|` `0|-1|` `0|0|4|
|Zj|-2M|-2M|-5M|M|M|-M|-M|-16M|
|Zj - Cj|-2M-2|-2M-5|-5M-9|M|M|` `0|0|-|
M çok büyük bir   sayı  olarak  tanımlandığından, Zj - Cj satırında mutlak değerce en büyük negatif sayı (-5M-9)’dur. O halde, x3 çözüme giren değişken olacaktır. Oranlar hesaplandığında çözümü terkedecek değişkenin A1 olduğu görülür. Anahtar sayı 4’dür. Yeni çözüm tablosu aşağıda verilmiştir.

***Tablo 4.25***
##### ***Simpleks Birinci Çözüm Tablosu*** 

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|9     x3|1/4|1/4|1|-1/4|` `0|1/4|` `0|3|
|-M   A2|3/4|**3/4**|0|1/4|-1|-1/4|` `1|1|
|Zj|||9||M||-M|27-M|
|Zj - Cj|||0||M||0|-|
Tablo 4.25’den görüldüğü gibi Z1 - C1, Z2 - C2, Z4 - C4 < 0 olduğundan, çözüm en iyi değildir. Ayrıca, enb(,,) =  = [(-3M-11)/4] olduğundan x2 değişken sütunu anahtar sütundur.  Oranlar, x3 değişken satırı için 12, A2 değişken satırı için (4/3) olarak hesaplandığından, A2 değişken satırı anahtar satırdır. Anahtar sayı (3/4) dür. Simpleks yöntemin standart işlemlerinin uygulanmasıyla elde edilen yeni çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.26***

***Simpleks İkinci Çözüm Tablosu***

|` `TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|9     x3|0|0|1|-1/3|` `**1/3**|` `1/3|-1/3|8/3|
|5     x2|1|1|0|` `1/3|-4/3|-1/3|` `4/3|4/3|
|Zj|5|5|9|-4/3|-11/3|` `4/3|11/3|92/3|
|Zj - Cj|3|0|0|-4/3|-11/3|||-|
Z4 - C4 = -4/3, Z5 - C5 = -11/3 < 0 olduğundan çözüm en iyi değildir. Tablodan görüldüğü gibi, x5 çözüme girecek x3 temelden çıkacaktır. Bilinen işlemlerden sonra elde edilen üçüncü çözüm tablosu aşağıda gösterilmiştir.

***Tablo 4.27***

***Simpleks Üçüncü Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|A1|A2|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x5|0|0|3|-1|1|1|-1|8/3|
|5     x2|1|1|4|-1|0|1|0|12|
|Zj|5|5|20|-5|0|5|0|60|
|Zj - Cj|3|0|11|-5|0|M+5|M|-|
Z4 - C4 = -5 < 0 olduğundan, kural gereği bu sayıyla ilgili değişkenin, yani x4’ün temele girmek üzere seçilmesi gerekir. Ancak bu durumda bütün satırlar için negatif değerli oranlar hesaplanacağından anahtar satır seçilemez. Bu durum, temel çözüm için öngörülen x4 değişkeninin büyümesi yoluyla eldeki temel değişkenlerden hiçbirinin daha da küçülemeyeceği ve dolayısıyla sıfır olamayacakları anlamına gelmektedir. Bu da çözümün bir sınırının olmadığını, amaç fonksiyonu değerininin sınırsız artabileceği sonucunu vermektedir. 
### ***4.4.4 Alternatif En iyi Çözümler***
`	`Bazı doğrusal programlama problemlerinde, amaç fonksiyonu en iyi değerine birden fazla uç noktasında ulaşabilir. Bu durumda amaç fonksiyonunun en iyi değeri her uç noktası için aynıdır. Farklı olan yalnızca temel değişkenler ve onların çözüm değerleridir.

Herhangi bir doğrusal programlama problemini çözerken en iyi çözümün birden fazla olduğunu söyleyebilmek için en iyi çözümün elde edildiği çözüm tablosunda temel olmayan herhangi bir değişkene ait Zj - Cj değeri sıfır olmalıdır. Özetle, en iyi çözümün temelinde bulunmayan herhangi bir değişkenin Zj - Cj = 0 ise yürürlükteki en iyi çözüm tek değildir. Bu durumda, alternatif çözümü elde etmek üzere söz konusu değişken temele alınır. Yeni en iyi çözüm bulunduğunda işlemler tamamlanmış olur.

Bu özel durumun ortaya çıktığı bir örnek problem aşağıda verilmiştir.

***Örnek 4.10***: Aşağıdaki problemi simpleks yöntemle çözerek problemin en iyi çözümünü bulunuz. 

Zenb = 2x1 + 4x2 + 6x3   

`          `4x1 + 8x2 + 12x3 £ 36

`            `x1 +   x2 +   3x3 £ 12

`          `2x1 + 2x2 +     x3 £ 20

`                       `x1, x2, x3 ³ 0

***Çözüm 4.10***: Aylak değişkenlerin modele sokulmasıyla elde edilen standart biçim aşağıda gösterilmiştir.

Zenb = 2x1 + 4x2 + 6x3 + 0x4 + 0x5 + 0x6

`          `4x1 + 8x2 + 12x3  + x4               = 36

`            `x1 +   x2 +    3x3        + x5        = 12

`          `2x1 + 2x2 +      x3               + x6 = 20

`                              `x1, x2, x3, x4, x5, x6 ³ 0

Buna göre başlangıç çözüm tablosu aşağıdaki gibi olur.

***Tablo 4.28***

***Simpleks Başlangıç Çözüm Tablosu*** 

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x4|` `4|` `8|` `**12**|1|0|0|36|
|0     x5|` `1|` `1|` `3|0|1|0|12|
|0     x6|` `2|` `2|` `1|0|0|1|20|
|Zj|0|0|0|0|0|0|0|
|Zj - Cj|-2|-4|-6|0|0|0|-|
Tüm Zj - Cj ³  0 olmadığından başlangıç temel uygun çözüm en iyi değildir.  > ,  olduğundan, x3 temele alınıp x4 temelden çıkartılarak anahtar işlemler uygulandığında yeni çözüm Tablo 4.29’da gösterildiği gibi elde edilir.
##### ***Tablo 4.29***
***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|6     x3|**1/3**|2/3|1|` `1/12|0|0|3|
|0     x5|0|-1|0|-1/4|1|0|3|
|0     x6|5/3|4/3|0|-1/12|0|1|17|
|Zj|2|4|6|` `1/2|0|0|18|
|Zj - Cj|0|0|0|` `1/2|0|0|-|
Tüm Zj - Cj ³ 0 olduğundan, tablodaki çözüm en iyidir. Bu  en  iyi çözümde x1 = 0,  x2 = 0, x3 = 3, x4 = 0, x5 = 3, x6 = 17, Zenb = 18’dir.  x1, x2, x4 temel olmayan değişkenler olmakla birlikte  Z1 - C1 = 0  ve Z2 - C2 = 0 olması alternatif en iyi çözümün göstergesidir. Yukarıdaki açıklamalar x1 ve x2’nin temele gireceğine işaret etmektedir. O halde, ilk olarak x1’i temele alalım. x1 değişken sütunu anahtar sütun olarak belirlendiğinden, anahtar satır x3 değişken satırı, anahtar sayı da (1/3) olur. Yeni çözüm tablosu aşağıdaki gibi elde edilmiştir. 

***Tablo 4.30***

***Simpleks İkinci En İyi Çözüm Tablosu***

|TDV|x1|x2|x3|x4|x5|x6|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|2      x1|1|` `2|3|` `1/4|0|0|9|
|0      x5|0|-1|0|-1/4|1|0|3|
|0      x6|0|-2|-5|-1/2|0|1|2|
|Zj|2|` `4|` `6|1/2|0|0|18|
|Zj - Cj|0|` `0|` `0|` `1/2|0|0|-|
Tüm Zj - Cj ³ 0 olduğundan tablodaki çözüm en iyidir. Bu  en  iyi çözümde: x1 =  9, x2 = 0, x3 = 0, x4 = 0, x5 = 3, x6 = 2, Zenb = 18’dir. Görüldüğü gibi, amaç fonksiyonunun en iyi değeri olan 18’e farklı bir temel değişkenler kümesiyle yeniden ulaşılmıştır. Ayrıca, tablodan görüldüğu gibi temel olmayan x2 değişkenine ait Z2 - C2’nin sıfıra eşit olması problemin üçüncü bir en iyi çözümünün daha bulunduğuna işaret etmektedir. x2’nin temele alınması, x1’in temelden çıkarılmasıyla belirlenen alternatif çözüm şöyledir: x1 = 0, x2 = 9/2, x3 = x4 = 0, x5 = 15/2, x6 = 112, Zenb = 18
### ***4.4.5 Uygun Olmayan Çözüm*** 
`	`Doğrusal programlama problemlerinin çözümünde karşılaşılan diğer bir sorun da uygun bir çözümün bulunamamasıdır. Bu sorun, kısıtlayıcıları aynı anda sağlayan ortak bir noktanın bulunmaması sonucu ortaya çıkar. Nedeni de eşitsizliklerin tutarsız olmasıdır. Böyle bir durumda problem modelinin gözden geçirilmesi ve gerekli düzenlemelerin yapılması uygun olur.

***Örnek 4.11***: Aşağıdaki problemi simpleks yöntemle çözünüz.

Zenk = 2x1 + 2x2

`           `-x1 +   x2 £ 4

`            `x1 + 2x2 ³ 5

`          `3x1 + 4x2 £ 6

`                 `x1, x2 ³ 0

***Çözüm 4.11***: Uygun değişkenlerin eklenip çıkartılmasıyla belirlenen standart biçim aşağıda verildiği gibidir. 

Zenk = 2x1 + 2x2 + 0x3 + 0x4 + 0x5 + MA1

`           `-x1 +  x2  + x3                        = 4

`            `x1 + 2x2         - x4        + A1  = 5

`          `3x1 + 4x2                + x5         = 6

`                               `x1, x2, x3, x4, A1 ³ 0

Standart biçimdeki bilgilerle düzenlenen simpleks başlangıç çözüm tablosu şöyledir.

***Tablo 4.31***

***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|x2|x4|x3|x5|A1|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x3|-1|1|` `0|1|0|0|4|
|M    A1|` `1|2|-1|0|0|1|5|
|0     x5|` `3|**4**|` `0|0|1|0|6|
|Zj|M|2M|-M|0|0|M|5M|
|Zj - Cj|M-2|2M-2|-M|0|0|0|-|
Z2 - C2 = 2M-2 > Z1 - C1 = M-2 olduğundan x2 temele alınıp, en küçük orana (3/2) sahip x5 temelden çıkartılarak simpleks yöntemin klasik işlemleri uygulandığında yeni çözüm tablosu aşağıdaki gibi elde edilmiş olur.
##### ***Tablo 4.32***
***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|x2|x4|x3|x5|A1|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|0     x3|-7/4|0|` `0|1|-1/4|0|5/2|
|M    A1|-1/2|0|-1|0|-1/2|1|2|
|2     x2|3/4|1|` `0|0|` `1/4|0|3/2|
|Zj||2|-M|0||M|2M+3|
|Zj - Cj||0|-M|0||0|-|
Tüm Zj - Cj £ 0 olduğundan, en iyi olma koşulu sağlanmış ve çözüm x1 = 0, x2 = 3/2, x3 = 5/2, x4 = 0, x5 = 0, A1 = 2, Zenb = 2M+3 olarak belirlenmiştir. Ancak simpleks yöntemde mutlaka sıfır düzeyinde bulunması gereken yapay değişken A1 = 2 olduğundan çözüm uygun değildir. 
### ` `***4.4.6 Sınırlandırılmamış Değişkenlerle Çözüm*** 
`             `Bilindiği gibi doğrusal programlamanın simpleks algoritması ile çözümünde temeli terkedecek değişkenin belirlenmesinde oranlar incelenmekte ve yalnızca pozitif oranlar dikkate alınmaktadır. Bu yolla çözümün uygun olması, yani tüm değişkenlerin negatif olmayan değerler alması sağlanmaktadır. Bazı değişkenlerin işaretleri üzerine herhangi bir sınırlama getirilmemesi durumunda oran testi uygulanamayacağından, simpleks yöntem uygulaması şansı ortadan kalkar. Bu durumda yapılacak tek şey, problemin simpleks yöntemle çözümüne imkan verecek değişiklikleri gerçekleştirmektir.  

İşaretçe sınırlandırılmamış değişkenlerin bulunduğu bir doğrusal programlama probleminin simpleks yöntemle çözülebilmesi için önce problemin klasik doğrusal programlamaya  dönüştürülmesi, yani negatif olmama koşulunun oluşturulması gerekir. Bu amaçla işaretçe sınırlandırılmamış her bir xi değişkeni için iki yeni değişken tanımlanır. Yeni değişkenler  ve  olsun. xi = - olarak tanımlanır ve amaç fonksiyonu ile kısıtlayıcı fonksiyonlardaki tüm xi ler (-) ile değiştirilir. Modelin negatif olmama koşulunda ise ³ 0, ³ 0 düzeltmesi yapılır. Böylece işaretçe sınırlandırılmamış her bir değişken negatif olmayan iki değişkenin farkı olarak açıklanmış ve orijinal problem klasik doğrusal programlama problemine dönüştürülmüş, böylece simpleks yöntem uygulanmasına olanak sağlanmış olur.İleride görüleceği gibi herhangi bir temel uygun çözümde  ve  değişkenlerinin her ikisi birden sıfırdan büyük olamaz. Bu herhangi bir temel uygun çözümde işaretçe sınırlandırılmamış her bir xi’nin aşağıda açıklanan üç durumdan birine düşeceği  anlamına gelmektedir. 

**Durum 1**: > 0 ve  = 0.

Bu durum temel uygun çözümde işareti sınırlandırılmamış xi’nin > 0 olacağına işaret eder. Bu durumda xi = -  = olur. Buradan xi = elde edilir. Örneğin, eğer temel uygun çözümde = 3 ise  = 3,  = 0 olur. 

**Durum 2**: = 0 ve > 0.

Bu durum temel uygun çözümde xi < 0 olması demektir. xi = -  olduğundan,  xi = - elde edilir. Örneğin, eğer temel uygun çözümde = 3 ise tanım gereği -  = 0 - 3 = -3 dolayısıyla xi = -3 elde edilir.  

**Durum 3**: = 0 ve  = 0.

Bu durumda xi = -  = 0 - 0 = 0 elde edilir.

Açıklamaların ortaya koyduğu gibi aynı simpleks tabloda  ve ’den en fazla bir tanesi temelde bulunabilir.  Bunun nedeni şu şekilde açıklanabilir. ’nin temelde bulunduğunu düşünelim. Bu durumda  sütununun sadece ’nin bulunduğu satırında 1 diğer satırlarında 0 bulunacaktır.  sütun değerleri  sütun değerlerinin ters işaretlisine eşit olduğundan,  sütun elemanlarından sadece bir tanesi -1’e diğerleri sıfıra eşit olacaktır. Bu durumda  temelde bulunamaz. Aynı gerekçeden dolayı  ve  aynı anda temelde bulunamazlar. Bu herhangi bir simpleks tabloda ,  veya her ikisinin birden sıfıra eşit olması demektir. Sınırlandırılmamış değişken içeren bir problemin simpleks yöntemle çözümü aşağıdaki örnek problem üzerinde açıklanacaktır.  

***Örnek 4.12***: Aşağıdaki problemi simpleks yöntemle çözünüz.

Zenb = 2x1 + x2 

`           `3x1 + x2 £  6 

`             `x1 + x2  £ 4

`                     `x1 > 0, x2 işareti sınırlandırılmamış

***Çözüm 4.12***: Simpleks yöntem için önce işareti sınırlandırılmamış x2 değişkeni yerine, x2 = - yazalım. Bu durumda yukarıda verilen doğrusal programlama problemi aşağıdaki gibi olur.

Zenb = 2x1 + (-) 

`           `3x1 + (-) £  6

`             `x1 + (-) £ 4

`                   `x1, , ³ 0 

Artık çözülecek problem, içeriğinde x2 yerine (-)’yi bulunduran problemdir. Problemin simpleks yöntemin gerektirdiği forma dönüştürülmesinin ardından uygulamaya geçilebilir.

Düzenlenmiş problemin simpleks yöntemin gerektirdiği standart formu ve çözüm tabloları aşağıda arka arkaya verilmiştir.

Zenb = 2x1 + (-) 

`           `3x1 + (-) + x 3 = 6

`             `x1 + (-) + x4  = 4

`                `x1, ,, x3, x4 ³ 0 

***Tablo 4.33***

***Simpleks Başlangıç Çözüm Tablosu***

|TDV|x1|||x3|x4|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|x3|**3**|1|2|-1|0|6|
|x4|1|1|1|0|-1|4|
|Zj|0|0|0|0|0|0|
|Zj - Cj|-2|-1|1|0|0|-|
##### ***Tablo 4.34***
***Simpleks Birinci Çözüm Tablosu***

|TDV|x1|||x3|x4|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|x3|**3**|1|-1|1|0|6|
|x4|1|1|-1|0|1|4|
|Zj|0|0|0|0|0|0|
|Zj - Cj|-2|-1|1|0|0|-|
***Tablo 4.35***

***Simpleks İkinci Çözüm Tablosu***

|TDV|x1|||x3|x4|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|x1|1|1/3|-1/3|1/3|0|2|
|x4|0|2/3|-2/3|-1/3|1|2|
|Zj|2|2/3|-2/3|2/3|0|4|
|Zj - Cj|0|-1/3|1/3|2/3|0|-|
##### ***Tablo 4.36***
##### ***Simpleks Üçüncü (En iyi) Çözüm Tablosu***

|TDV|x1|||x3|x4|ÇV|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|x1|1|0|0|1/2|-1/2|1|
||0|1|-1|-1/2|3/2|3|
|Zj|2|1|-1|1/2|1/2|5|
|Zj - Cj|0|0|0|1/2|1/2|-|
Tablo 4.36’daki temel uygun çözümde tüm Zj - Cj ³ 0 olduğundan çözüm en iyidir. Bu çözümde, x1 = 1, = 3,  = 0, x3 = 0, x4 = 0 olarak belirlenmiştir. Amaç fonksiyonunun en büyük değeri Zenb = 5’dir. x2 = -  olduğu göz önünde bulundurulduğunda x2 = 3 olarak belirlenir. Diğer taraftan en iyi çözümün temelde bulunmayan değişkenlerinden ’ye ait Zj – Cj değerinin sıfıra eşit olduğu, dolayısıyla bir alternatif çözüm bulunduğu görülebilir.



## ***	



##
##
## ***PROBLEMLER***

***1***.  Aşağıdaki  doğrusal programlama  problemlerini simpleks yöntemle çözünüz.

***a**.* Zenb = 16x1 + 32x2 	***b**.* Zenk = 2x1 + 3x2 + 2x3 + x4

`              `2x1  + 3x2 £ 18              		              3x1 - 3x2 + 4x3 + 2x4 £   2   

`	   `x1 + 3x2 £ 9            		                x1 +  x2 +   x3 + 3x4 £   5     

`	 `3x1 + 8x2 £ 40 			              2x1 +  x2 + 3x3 + 3x4 £ 25                    	        x1, x2 ³ 0			                            x1, x2, x3, x4 ³ 0

***c**.* Zenb = 7x1 + 8x2 + 8x3       	 ***d**.* Zenb = 3x1 + 4x2 + 6x3      

`	`2x1 + 3x2 +   x3 £ 18            	              2x1 + 2x2 + 3x3 £ 12 

`	`4x1 + 6x2           £ 32            	                x1 + 2x2 + 3x3 £   9   

`	`3x1 + 8x2 + 4x3  £ 40            	              3x1 + 6x2 + 9x3 £ 27

`	            `x1, x2, x3 ³ 0                  	                         x1, x2, x3 ³ 0

***e**.* Zenb = 17x1 + 22x2 + 19x3    	  ***f**.* Zenk = 15x1 + 13x2 

`	  `2x1 + 4x2          £ 10            	                         3x1 + 4x2 ³ 12 

`	    `x1 +   x2 +   x3 ³ 16            	              4x1 + 8x2 ³ 20

`	  `2x1 + 3x2 + 4x3 = 18             	                x1 +   x2  = 4

`	             `x1, x2, x3 ³ 0                  	                     x1, x2 ³ 0

***g**.* Zenk = 2x1 + x2 - 2x3 - 3x4    	 ***h**.* Zenb = 20x1 + 30x2 + 10x3

`	  `x1 - x2 + 3x3 + 4x4 = 4		                         2x1 + 4x2 + 6x3 £ 10

`	`2x1 + x2 +  x3 +   x4 = 5		                           x1 + 3x2 + 5x3 £ 15

`               `x1 + x2 +  x3           = 6                                          2x1 + 3x2 + 4x3 = 18

`	           `x1, x2, x3, x4 ³ 0		                                   x1, x2, x3, ³ 0

***2***.  Aşağıdaki  doğrusal  programlama  problemlerini  simpleks yöntemle çözünüz.

***a**.* Zenb = 16x1 + 32x2 	***b**.* Zenk = x1 + 3x2 + 2x3 + x4

`              `2x1  + 3x2 £ 18              		                    3x1 - 3x2 + 4x3  £   2   

`	   `x1 + 3x2 £ 9            		                      x1 +  x2 +   x3  £   5     

`	 `3x1 + 8x2 £ 40 			                    2x1 +  x2 + 3x3  £ 25                    	        x1, x2 sınırlandırılmamış                                 x1, x2, x3 sınırlandırılmamış 

[^1]: Eşitsizliğin sağ tarafı kullanılabilir, sol tarafı kullanılan kaynak miktarını gösterdiğinden, bu ikisi arasındaki farka eşit olan aylak değişken, kullanılmayan kaynak miktarını gösterir. Kullanılmayan kaynağın amaç fonksiyonuna, yani kâra katkısının sıfır olması doğaldır. 
[^2]: Bölen olarak yalnızca pozitif katsayıların dikkate alınmasının nedeni açıktır. Sıfır, amaç fonksiyonunun değerinde bir değişiklik yaratmamakta, negatif sayılar ise uygun olmayan, yani negatif olmama koşulunu sağlamayan bir çözüme yol açmaktadır.
[^3]: Bu kural, hem en büyükleme hem de en küçükleme problemleri için geçerlidir.
[^4]: Anahtar sayılar koyu renk basılarak diğerlerinden ayırdedilmesi sağlanmıştır.
[^5]: Bu kez kısıtlayıcı fonksiyonlarda sıfır katsayısına sahip değişkenlerin gösterilmediğine dikkat edilmelidir. Bundan sonra da bu yol izlenecek, sıfır katsayılı değişkenler kısıtlayıcılarda gösterilmeyecektir.
[^6]: M yerine büyük sayıların kullanıldığı kaynaklara rastlanabilir.  
[^7]: M yerine sabit bir sayı kullanılmak istenseydi, karar değişkenlerinin amaç fonksiyonundaki katsayılardan daha büyük bir sayının alınması yeterli olurdu. Örneğimizde, x1, x2 ve x3 değişkenlerinin katsayıları sırasıyla (-2), (-3) ve (-1) olduğundan, M = 50 veya M = 100 almak yeterlidir. 
[^8]: Diğer yaklaşım, anahtar  satır  seçiminde zorluk çıkaracağından tercih edilmemiştir.
[^9]: Bu matrisin başlangıç tablosunda bir birim matris olduğu unutulmamalıdır.