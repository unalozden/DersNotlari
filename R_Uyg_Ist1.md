**R’de Paket Yükleme-Paket Çağırma-Excel Dosyasını İçe Aktarma-Tanımsal Değerlerini Hesaplama-Parametrik ve Non-Parametrik Testler- Korelasyon Analizi-Basit Doğrusal Regresyon**

\> **install.packages("readxl")** 	# readxl  paketinin yüklenmesi


\> **library("readxl")**		# readxl  paketinin çağrılması


\>**r\_data<- read\_excel("d:\\rdata.xlsx")**		# rdata adlı excel dosyanın r\_data adıyla R’ye aktarılması


\>**View(r\_data)**		# r\_data adlı dosyanın görüntülenmesi.


\>**r\_data**		# r\_data adlı dosyanın görüntülenmesi.


\>**summary(r\_data)** 	# r\_data veri dosyası içindeki tüm değişkenlerin tanımsal istatistik değerleri.


\>**summary(r\_data$vize)** 	# r\_data veri dosyası içindeki vize değişkeninin tanımsal istatistik değerleri.


\>**mean(r\_data$final)** 	# r\_data veri dosyası içindeki final değişkeninin aritmetik ortalaması.


\>**install.packages(“psych”)**		# psych paketinin yüklenmesi


\>**library(psych)**		# psych paketinin çağrılması


\>**describe(r\_data)** 	# r\_data veri dosyası içindeki tüm değişkenlerin tanımsal istatistik değerleri


\>**shapiro.test(r\_data$vize)**	#r-data veri seti içindeki “vize” değişkeninin normallik testi / Ho: Vize notları normal dağılmaktadır.


\>**var.test**(**r\_data$vize~r\_data$cinsiyet**) #Grup varyanslarının eşitliğini test etmek için / Ho: Grup (Kadın/Erkek) varyansları eşittir.


\>**t.test(r\_data$vize~r\_data$cinsiyet)** 	# bağımsız iki örneklem t-testi / Ho: Kadınların vize not ortalaması = Erkeklerin vize not ortalaması.


\>**t.test(r\_data$vize~r\_data$cinsiyet, var.equal=T)** 	#Grup varyanslarının eşit ise (ya da eşit olduğu düşünülüyorsa) İki bağımsız örneklem t testi / Ho: Ho: Kadınların vize not ortalaması = Erkeklerin vize not ortalaması.


\>**t.test(r\_data$vize,r\_data$final, paired=TRUE)** # Eşlenik örneklem t-testi / Ho: Vize not ortalaması = Vize not ortalaması.


\>**t.test(r\_data$vize, mu=80)** # Tek örneklem  t-testi / Ho: Vize not ortalaması = 80.


**oneway.test(r\_data$vize~r\_data$bolum)** # Tek yönlü varyans analizi / Ho: Bölümlerin  vize not ortalamaları eşittir.


\>**wilcox.test(r\_data$vize, r\_data$final)** #Wilcoxon işaret testi / Ho: Vize Ortalaması = Final Ortalaması.


\>**wilcox.test**(**r\_data$final~r\_data$cinsiyet**) #Mann Whitney U / Ho: Cinsiyete göre final notu ortalamaları arasında fark yoktur.


\>**kruskal.test(r\_data$final~r\_data$bolum)**	#Kruskal Wallis testi / Ho: Bölümlerin  final not ortalamaları eşittir.


\>**chisq.test(r\_data$cinsiyet, r\_data$bolum)** #Ki-kare testi bağımsızlık testi /Ho: bölümler ile cinsiyet arasında ilişki yoktur.


\>**corr.test(r\_data$vize,r\_data$final)**  #Pearson korelasyon katsayısı /Ho: Vize notları ile Final notları arasında doğrusal korelasyon yoktur.


\>**corr.test(r\_data$vize,r\_data$final,** **method="spearman")** #Spearman sıra korelasyon katsayısı /Ho: Vize notları sıralaması ile Final notları sıralaması arasında korelasyon yoktur.


\>**lm(r\_data$vize~r\_data$final)** 	#Vize notlarının, final notları ile açılandığı basit doğrusal regresyon.


\>**model<- lm(r\_data$vize~r\_data$final)**	#Vize notlarının, final notları ile açılandığı basit doğrusal regresyonun model nesnesine atanması.


\>**summary(model)**	#Model (regresyon modeli) hakkında özet bilgiler.

