# YBS301 Veri Madenciliği – Çalışma Soruları

Oct 22, 2026 · @I am kahraman,

## Bu set nasıl kullanılır?

Bu set, 1. ve 2. hafta çalışma notları ile NumPy, pandas ve Matplotlib defterlerine dayanan 245 soru içerir. Her konu dört soru tipine ayrılmıştır: çoktan seçmeli, boşluk doldurma, doğru/yanlış ve kısa cevap/hesaplama. Kodlama bölümlerinde ayrıca "kod çıktısını tahmin et" soruları vardır.

| Bölüm | Çoktan seçmeli | Boşluk doldurma | Doğru/Yanlış | Kısa cevap / Kod | Toplam |
| --- | --- | --- | --- | --- | --- |
| Hafta 1 – Temel Kavramlar | 20 | 15 | 10 | 8 | 53 |
| Hafta 2 – Verinin Hazırlanması | 20 | 14 | 10 | 8 | 52 |
| NumPy | 16 | 12 | 8 | 12 | 48 |
| pandas | 16 | 12 | 8 | 10 | 46 |
| Matplotlib | 16 | 12 | 8 | 10 | 46 |
| **Toplam** | **88** | **65** | **44** | **48** | **245** |

Öneri: Soruları önce cevap anahtarına bakmadan çözün, sonra en sondaki **Cevap Anahtarı** bölümüyle kontrol edin. Kod sorularını Jupyter'da çalıştırarak da doğrulayabilirsiniz. Soru numaraları her alt başlıkta yeniden 1'den başlar; cevap anahtarında bölüm ve soru tipiyle eşleştirilmiştir.

## Hafta 1 – Temel Kavramlar

### A. Çoktan seçmeli

1. "Algoritma" kelimesi aşağıdakilerden hangisinin adından gelir?
   - A) Al-Biruni
   - B) Harezmi (Al-Khwarizmi)
   - C) İbn-i Sina
   - D) Russell Ackoff
   - E) Frank Rosenblatt
2. Aşağıdakilerden hangisi **algoritmik olmayan** bir problemdir?
   - A) Bir sayı listesini küçükten büyüğe sıralamak
   - B) İki şehir arasındaki en kısa yolu bulmak
   - C) Bir kredinin aylık taksitini hesaplamak
   - D) Bir fotoğraftaki kişinin yüzünü tanımak
   - E) Bir listedeki en büyük sayıyı bulmak
3. Yapay nöronun ilk modeli olan perseptron kim tarafından, hangi yıl geliştirilmiştir?
   - A) Minsky ve Papert, 1969
   - B) Han ve Kamber, 1991
   - C) Frank Rosenblatt, 1957
   - D) R. Ackoff, 1989
   - E) Abraham Wald, 1943
4. "Veritabanlarında Bilgi Keşfi" (KDD) terimi ilk kez hangi yıl düzenlenen çalışma toplantısında ortaya atılmıştır?
   - A) 1969
   - B) 1980
   - C) 1989
   - D) 1992
   - E) 2000
5. DIKW piramidinde "Nasıl? Neden?" sorularını cevaplayan, neden-sonuç ilişkisinin kurulduğu katman hangisidir?
   - A) Veri
   - B) Enformasyon
   - C) Bilgi
   - D) Bilgelik
   - E) Üst veri
6. Abraham Wald örneğinde "deliklerin kanat ve gövdede yoğunlaştığını, motor ve kokpitte neredeyse hiç olmadığını gösteren harita" DIKW'nin hangi katmanına karşılık gelir?
   - A) Veri
   - B) Enformasyon
   - C) Bilgi
   - D) Bilgelik
   - E) Hiçbiri
7. Veri ambarının tek bir bölüme veya konuya yönelik alt kümesine ne ad verilir?
   - A) Üst veri (metadata)
   - B) OLAP küpü
   - C) İşlemsel veritabanı
   - D) Veri deposu (data mart)
   - E) Dış veri kaynağı
8. Kablo üreten bir işletme "Ağustos'ta İç Anadolu'da ne kadar sattık; geçen ayla ve geçen yılın Ağustos'uyla karşılaştırması nedir?" sorusunu yanıtlamak istiyor. En uygun araç hangisidir?
   - A) Basit SQL sorgusu
   - B) OLAP
   - C) Veri madenciliği
   - D) Kelime işlemci
   - E) Örüntü tanıma
9. KDD sürecinin en çok zaman alan aşaması hangisidir?
   - A) Amacın tanımlanması
   - B) Veriler üzerinde ön işlemler
   - C) Modelin kurulması ve değerlendirilmesi
   - D) Modelin kullanılması ve yorumlanması
   - E) Modelin izlenmesi
10. Veri madenciliğinin kendisi, KDD'nin beş aşamasından hangisine karşılık gelir?
    - A) Amacın tanımlanması
    - B) Veriler üzerinde ön işlemler
    - C) Modelin kullanılması ve yorumlanması
    - D) Modelin izlenmesi
    - E) Modelin kurulması ve değerlendirilmesi
11. Aşağıdakilerden hangisi **tanımlayıcı (descriptive)** bir modeldir?
    - A) Regresyon
    - B) Sınıflandırma
    - C) Zaman serisi analizi
    - D) Birliktelik kuralları
    - E) Karar ağaçları
12. Genetik algoritmalar için aşağıdakilerden hangisi doğrudur?
    - A) Denetimsiz bir kümeleme yöntemidir.
    - B) Doğrudan bir veri madenciliği modeli değil, bir eniyileme yöntemidir.
    - C) Yalnızca zaman serisi verisinde kullanılır.
    - D) Biyolojik sinir sistemini taklit eder.
    - E) Pazar sepeti analizinin diğer adıdır.
13. "Çekiç alan müşteri ilk üç ayda %15 olasılıkla çivi de alır" bulgusu hangi model türüyle elde edilir?
    - A) Kümeleme
    - B) Özetleme
    - C) Sıra örüntü analizi
    - D) Regresyon
    - E) Bayes sınıflandırması
14. Karmaşık ve doğrusal olmayan ilişkileri modelleyebilen ama **yorumlanması zor** olan algoritma hangisidir?
    - A) Karar ağaçları
    - B) Yapay sinir ağları
    - C) k-en yakın komşu
    - D) Bayes sınıflandırması
    - E) Doğrusal regresyon
15. Aşağıdakilerden hangisi geleneksel istatistiğin değil, **veri madenciliğinin** özelliğidir?
    - A) Bir hipotez kurarak başlar.
    - B) Eşitlikleri analist kendisi geliştirir.
    - C) Çoğunlukla sayısal veriyle çalışır.
    - D) Sonuçları görece kolay yorumlanır.
    - E) Sayısal veriye ek olarak metin ve ses verisiyle de çalışır.
16. "Önce ateş edip sonra hedefi kurşunların etrafına çizmek" şeklinde özetlenen yanılgı hangisidir?
    - A) Cımbızlama
    - B) Simpson paradoksu
    - C) Teksas keskin nişancısı
    - D) Kumarbaz safsatası
    - E) Ekolojik safsata
17. Alt gruplarda görülen bir eğilimin, gruplar birleştirildiğinde tersine dönmesine ne ad verilir?
    - A) Simpson paradoksu
    - B) Ortalamaya dönüş
    - C) Sahte hassasiyet
    - D) Hayatta kalma yanılgısı
    - E) Post hoc ergo propter hoc
18. Datasaurus (ve Anscombe dörtlüsü) örneğinin verdiği temel ders nedir?
    - A) Korelasyon katsayısı her zaman güvenilirdir.
    - B) Farklı şekilli veri setleri aynı özet istatistiklere sahip olabilir; veriyi mutlaka görselleştirmek gerekir.
    - C) Ortalama yerine her zaman medyan kullanılmalıdır.
    - D) Büyük veri setlerinde görselleştirme gereksizdir.
    - E) Standart sapma yalnızca normal dağılımda hesaplanır.
19. Kira verisi örneğinde Alanönü mahallesindeki iki çalışanın kira ortalaması eksik değeri doldurmak için kullanılırsa doldurulan değer kaç olur?
    - A) 850
    - B) 865
    - C) 901
    - D) 950
    - E) 1250
20. k-en yakın komşu algoritmasında k değeri **çok küçük** seçilirse ne olur?
    - A) Birbirine benzemeyen noktalar aynı sınıfa toplanır.
    - B) Algoritma etiket bilgisine ihtiyaç duymaz.
    - C) Aslında aynı sınıftan olan noktalar farklı sınıflara düşebilir; gürültüye duyarlılık artar.
    - D) Öklid uzaklığı hesaplanamaz.
    - E) Model tanımlayıcı hale gelir.

### B. Boşluk doldurma

1. Veri madenciliği, KDD sürecinin tamamı değil, yalnızca bir \_\_\_\_\_\_\_\_\_\_ dır.
2. DIKW piramidi \_\_\_\_\_\_\_\_\_\_ tarafından 1989'da ortaya konmuştur.
3. Veri ambarındaki veriler hakkındaki tanımlamalara, yani ambarın "veri kataloğu"na \_\_\_\_\_\_\_\_\_\_ denir.
4. Ambardaki veri üzerinde çok boyutlu analiz ve sorgulama yapmayı sağlayan teknolojinin kısaltması \_\_\_\_\_\_\_\_\_\_ dir.
5. 11 Mayıs 1997'de Garry Kasparov'u yenen IBM sistemi \_\_\_\_\_\_\_\_\_\_ dir.
6. 2016'da Lee Sedol'u 4-1 yenen Google sistemi \_\_\_\_\_\_\_\_\_\_ dur.
7. Modelin çıkardığı kuralların yalnızca eğitim verisinde işe yarayıp yeni veride çökmesine \_\_\_\_\_\_\_\_\_\_ denir.
8. Etiket (sınıf) bilgisi olan veriyle öğrenmeye \_\_\_\_\_\_\_\_\_\_ öğrenme, etiket bilgisi olmayana \_\_\_\_\_\_\_\_\_\_ öğrenme denir.
9. Doğum yılının 1974 yerine 1074 olarak girilmesi bir \_\_\_\_\_\_\_\_\_\_ değer örneğidir.
10. Bir sistemde cinsiyetin E/K, diğerinde 0/1 olarak kodlanması veri temizlemede \_\_\_\_\_\_\_\_\_\_ sorunudur.
11. Sürekli maaş değerlerini "düşük / orta / yüksek" kategorilerine çevirmek, yeniden yapılandırmanın \_\_\_\_\_\_\_\_\_\_ başlığına girer.
12. "Beş kez yazı geldi, şimdi tura gelir" diye düşünmek \_\_\_\_\_\_\_\_\_\_ safsatasıdır.
13. John Snow 1854'te kolera vakalarının Broad Street'teki \_\_\_\_\_\_\_\_\_\_ çevresinde yoğunlaştığını harita üzerinde gösterdi.
14. "Bira alanların %80'i cips de alıyor" türünden bulgular \_\_\_\_\_\_\_\_\_\_ kurallarıyla (pazar sepeti analizi) elde edilir.
15. Dondurma satışları ile köpekbalığı saldırılarını birlikte artıran ortak neden (karıştırıcı değişken) \_\_\_\_\_\_\_\_\_\_ dır.

### C. Doğru / Yanlış

1. Veri madenciliği, zaten bilinen bir sonucu doğrulamak için kullanılan bir araçtır.
2. İşlemsel veritabanları veri madenciliğinde doğrudan kullanılmaz; önce hazırlanmaları gerekir.
3. Veri ambarı tüm işletmeyi, veri deposu (data mart) ise tek bir bölümü ilgilendirir.
4. Kümeleme denetimli bir öğrenme yöntemidir.
5. Kayıp değerleri ortalamayla doldururken genel ortalama yerine sınıf ortalaması daha uygundur.
6. 1969'da Minsky ve Papert, perseptronun basit mantıksal işlemlerde yetersiz kaldığını göstermiştir.
7. Veri madenciliği kirli veri üzerinde çalışır ve hatalı kayıtları analiz sırasında filtreler.
8. Zaman serisi analizi denetimsiz bir yöntemdir.
9. DIKW piramidinde bilgelik katmanı geçmişi anlamaya yöneliktir.
10. Hiyerarşik ve ağ veri modelleri ilk veri modelleri olarak 1960'larda ortaya çıkmıştır.

### D. Kısa cevap ve hesaplama

1. `3, 22, 15, 8, 40, 31, 12, 27, 35` verisini sıralayıp üç eşit bölüme ayırın. (a) Ortalama ile, (b) sınır değerleri ile düzeltin.
2. KDD sürecinin beş aşamasını sırasıyla yazın ve hangilerinin veri madenciliğinden önce, hangilerinin sonra geldiğini belirtin.
3. Kümeleme ile sınıflandırma arasındaki farkı bir iş dünyası örneğiyle açıklayın.
4. Kayıp verilerin tümüne aynı sabit değerin (ör. 9) yazılmasının iki riskini yazın.
5. "Çatısında leylek yuvası olan evlerde daha çok çocuk var; demek ki çocukları leylekler getiriyor." Bu çıkarımdaki hatayı adıyla belirtin ve gerçek açıklamayı yazın.
6. Bir ilaç haberinde "yan etki riskini %50 artırıyor" deniyor; risk 10.000'de 2'den 10.000'de 3'e çıkmış. Göreceli ve mutlak risk artışını hesaplayın; haberin neden yanıltıcı olduğunu açıklayın.
7. Bir market zinciri için SQL, OLAP ve veri madenciliğiyle yanıtlanabilecek birer soru yazın.
8. Hayatta kalma yanılgısına iş dünyasından bir örnek verin ve doğru analizin ne olması gerektiğini açıklayın.

## Hafta 2 – Verinin Hazırlanması

### A. Çoktan seçmeli

1. Temizleme, birleştirme, indirgeme ve dönüştürme işlemleri analistin zamanının yaklaşık ne kadarını alır?
   - A) %20
   - B) %40
   - C) %50
   - D) %80
   - E) %95
2. Bir veri tablosundaki **satırlara** verilen ad aşağıdakilerden hangisi değildir?
   - A) Nesne
   - B) Kayıt
   - C) Gözlem
   - D) Örnek (instance)
   - E) Öznitelik (feature)
3. Hava sıcaklığı (°C) hangi değişken tipine örnektir?
   - A) İsimsel
   - B) Sıra gösteren
   - C) Aralıklı
   - D) Oranlı
   - E) İkili
4. Mutlak sıfır noktası bulunan ve **oranlama** yapılabilen tek değişken tipi hangisidir?
   - A) Oranlı
   - B) Aralıklı
   - C) Sıra gösteren
   - D) İsimsel
   - E) İkili
5. Çalışanların unvanı (memur, şef, müdür) hangi değişken tipindedir?
   - A) İsimsel
   - B) Sıra gösteren
   - C) Tamsayılı
   - D) Aralıklı
   - E) Oranlı
6. Posta kodlarının ortalamasını almak neden anlamsızdır?
   - A) Posta kodları oranlı bir değişkendir.
   - B) Posta kodları isimsel bir değişkendir; sayılar yalnızca etikettir.
   - C) Posta kodlarında eksik veri çoktur.
   - D) Posta kodları negatif olabilir.
   - E) Posta kodları aralıklı bir değişkendir.
7. "Günlük satılan ekmek sayısı" hangi değişken tipindedir?
   - A) Tamsayılı
   - B) İkili
   - C) Sıra gösteren
   - D) İsimsel
   - E) Aralıklı
8. Ölçek hiyerarşisinin doğru gösterimi hangisidir?
   - A) Oranlı ⊂ Aralıklı ⊂ Sıra gösteren ⊂ İsimsel
   - B) İsimsel ⊂ Aralıklı ⊂ Sıra gösteren ⊂ Oranlı
   - C) İsimsel ⊂ Sıra gösteren ⊂ Aralıklı ⊂ Oranlı
   - D) Sıra gösteren ⊂ İsimsel ⊂ Oranlı ⊂ Aralıklı
   - E) Aralıklı ⊂ Oranlı ⊂ İsimsel ⊂ Sıra gösteren
9. Kimlik tablosunda kadınlara ait kayıtlarda "askerlik durumu" alanının boş olması nasıl değerlendirilmelidir?
   - A) Eksik veridir; mod ile doldurulmalıdır.
   - B) Gürültüdür; bölmeleme ile düzeltilmelidir.
   - C) Uygulanamaz bir özelliktir; doldurulmamalıdır.
   - D) Tutarsız veridir; kayıt silinmelidir.
   - E) Aykırı değerdir; kümeleme ile bulunmalıdır.
10. Eksik veri için mevcut enformasyondan **en çok yararlanan** ve en sık kullanılan yöntem hangisidir?
    - A) Nesneyi silmek
    - B) Sabit bir değer yazmak
    - C) Genel ortalama ile doldurmak
    - D) Regresyon veya karar ağacıyla en olası değeri tahmin etmek
    - E) Elle tek tek doldurmak
11. Kümelemede iki nesne arasındaki benzerliğin yalnızca ikisinde de dolu olan özelliklerle hesaplanması hangi eksik veri stratejisidir?
    - A) Elemek
    - B) Göz ardı etmek
    - C) Tahmin ederek doldurmak
    - D) Sabit değer atamak
    - E) Sınıf ortalaması kullanmak
12. Bir kaynakta `musteri_id`, diğerinde `cust_no` olarak adlandırılmış aynı alan hangi birleştirme sorunudur ve çözümü nedir?
    - A) Veri fazlalığı – korelasyon analizi
    - B) Veri değer karmaşası – birim dönüşümü
    - C) Şema uyuşmazlığı – meta veri ve veri sözlükleri
    - D) Gürültü – bölmeleme
    - E) Tutarsızlık – işlevsel bağımlılık
13. Bir veri setinde hem "yıllık gelir" hem de "aylık gelir × 12" sütunu bulunması hangi sorundur?
    - A) Şema uyuşmazlığı
    - B) Veri fazlalığı (redundancy)
    - C) Veri değer karmaşası
    - D) Eksik veri
    - E) Aykırı değer
14. Kaynak A'da ağırlığın kilogram, kaynak B'de libre cinsinden tutulması hangi sorundur?
    - A) Veri fazlalığı
    - B) Şema uyuşmazlığı
    - C) Uygulanamaz özellik
    - D) Veri değer karmaşası
    - E) Kayıplı sıkıştırma
15. 25 özellikli bir veri setinde kaç olası özellik alt kümesi vardır?
    - A) 625
    - B) 50
    - C) 1.048.576
    - D) 16.777.216
    - E) 33.554.432
16. Sarmalama (wrapper) yaklaşımı için hangisi doğrudur?
    - A) Algoritmadan bağımsız ölçütler kullanır.
    - B) Hesaplama maliyeti çok düşüktür.
    - C) Özellik seçerken madencilik algoritmasının kendisini kullanır; maliyeti yüksektir.
    - D) Yalnızca kayıpsız sıkıştırmada kullanılır.
    - E) Sonuç geçerliliği süzmeden daha düşüktür.
17. JPEG ve MP3 hangi indirgeme türüne örnektir?
    - A) Kayıplı sıkıştırma
    - B) Kayıpsız sıkıştırma
    - C) Boyut indirgeme
    - D) Veri küpü birleştirme
    - E) Parametrik büyük sayıların indirgenmesi
18. Yaş değerlerini "genç / orta yaşlı / yaşlı" kavramlarına taşımak hangi dönüştürme işlemidir?
    - A) Düzeltme (smoothing)
    - B) Bir araya getirme (aggregation)
    - C) Genelleme (generalization)
    - D) Normalleştirme
    - E) Özellik oluşturma
19. En büyük mutlak değeri 8.450 olan bir veri ondalık ölçekleme ile normalleştirilecektir. j kaç olmalıdır?
    - A) 2
    - B) 3
    - C) 4
    - D) 5
    - E) 8
20. Aşağıdaki normalleştirme yöntemlerinden hangisi aykırı değerlere **en duyarlı** olanıdır?
    - A) Z-skor
    - B) Min-maks
    - C) Ondalık ölçekleme
    - D) Medyan ile doldurma
    - E) Histogram

### B. Boşluk doldurma

1. Veri rafineri hattının dört istasyonu sırasıyla \_\_\_\_\_\_\_\_\_\_, \_\_\_\_\_\_\_\_\_\_, \_\_\_\_\_\_\_\_\_\_ ve \_\_\_\_\_\_\_\_\_\_ dır.
2. Komşu değerlere bakılarak yerel düzleştirme sağlayan gürültü giderme yöntemi \_\_\_\_\_\_\_\_\_\_ dır.
3. Orijinal verinin sıkıştırılmış hâlinden birebir geri elde edilebildiği sıkıştırmaya \_\_\_\_\_\_\_\_\_\_ sıkıştırma denir; ZIP buna örnektir.
4. Doğrusal regresyonda verinin yerine yalnızca a ve b katsayılarının saklanması \_\_\_\_\_\_\_\_\_\_ büyük sayıların indirgenmesidir.
5. Boş kümeyle başlayıp her adımda en iyi özelliği ekleyen sezgisel yöntem \_\_\_\_\_\_\_\_\_\_ dır.
6. Tüm özelliklerle başlayıp her adımda en kötüsünü çıkaran sezgisel yöntem \_\_\_\_\_\_\_\_\_\_ dır.
7. "Posta kodu → şehir" gibi özellikler arası kurallara \_\_\_\_\_\_\_\_\_\_ bağımlılık denir ve tutarsız kayıtları bulmakta kullanılır.
8. Günlük satış verisini aylık toplama çevirmek \_\_\_\_\_\_\_\_\_\_ işlemidir.
9. Min-maks normalleştirmenin çıktı aralığı \_\_\_\_\_\_\_\_\_\_ dır.
10. Ondalık ölçeklemede j, max|X\*| < 1 olmasını sağlayan en \_\_\_\_\_\_\_\_\_\_ tam sayıdır.
11. scikit-learn'deki `StandardScaler` standart sapmayı \_\_\_\_\_\_\_\_\_\_ ile, ders kitabı ise \_\_\_\_\_\_\_\_\_\_ ile hesaplar.
12. R'daki `clusterSim` paketinde `n1` \_\_\_\_\_\_\_\_\_\_, `n4` ise \_\_\_\_\_\_\_\_\_\_ normalleştirmesidir.
13. Kategorik bir sütundaki eksik değerleri `SimpleImputer` ile doldururken `strategy="__________"` kullanılır.
14. İkili (binary) değişken, \_\_\_\_\_\_\_\_\_\_ değişkenin yalnızca iki sonucu olan özel hâlidir.

### C. Doğru / Yanlış

1. Bir tablodaki her boş hücre eksik veridir.
2. Bugün 20 °C, dün 10 °C ise bugün dünden iki kat daha sıcaktır.
3. Sıra gösteren değişkende kademeler arası mesafeler eşittir.
4. Sarmalama (wrapper) yaklaşımının hesaplama maliyeti süzme (filter) yaklaşımından düşüktür.
5. Veri madenciliğindeki normalleştirme, bir değişkeni normal dağılıma dönüştürmek demektir.
6. Min-maks, z-skor ve ondalık ölçekleme değerlerin sıralamasını korur.
7. İndirgenmiş veriyle elde edilen sonuç, verinin tamamıyla elde edilecek sonuçtan çok farklı olmamalıdır.
8. Eksik değerlerin hepsine "Bilinmiyor" veya 0 yazmak tercih edilen bir yöntemdir.
9. Normalleştirme, k-NN ve kümeleme gibi mesafe tabanlı algoritmalarda zorunluya yakındır.
10. Z-skor normalleştirmesinin sonuçları her zaman 0 ile 1 arasındadır.

### D. Kısa cevap ve hesaplama

1. `X = 20, 35, 50, 65, 80` verisini (a) min-maks, (b) z-skor (örneklem std, n − 1), (c) ondalık ölçekleme ile normalleştirin.
2. `X = 12, 48, 30, 6, 54` verisinde 30 değerinin min-maks normalleştirilmiş karşılığı nedir? Hesabı gösterin.
3. `X = −1250, 340, 875, −60` verisini ondalık ölçekleme ile normalleştirin.
4. Aşağıdakilerin değişken tipini belirleyin: (a) Araç plakasındaki il kodu (06, 34, 61) (b) Müşteri memnuniyeti (çok memnun … hiç memnun değil) (c) Kelvin cinsinden sıcaklık (d) Bir hanedeki çocuk sayısı (e) "Kredi onaylandı mı?" (f) Takvim yılı (g) Boy (cm)
5. 15 özellikli bir veri setinde kaç özellik alt kümesi vardır? Bu durum neden sezgisel yöntemleri gerekli kılar?
6. "Eksik veri" ile "uygulanamaz" alan arasındaki farkı, askerlik örneği dışında yeni bir örnekle açıklayın.
7. k-NN'de yaş (20–65) ve maaş (15.000–80.000) normalleştirilmeden kullanılırsa ne olur? Neden?
8. Veri birleştirmenin üç temel sorununu ve her birinin çözümünü yazın.

## NumPy

Bu bölümdeki kod sorularında aşağıdaki diziler (defterdeki ile aynı) kullanılmıştır:

```python
import numpy as np
notlar = np.array([45, 78, 92, 33, 67, 88, 51, 29, 95, 60])
siparisler = np.array([150, 620, 340, 89, 1250, 470, 300, 199, 760, 55, 410, 980])
gunler = np.array(["Pzt", "Sal", "Çar", "Per", "Cum", "Cmt", "Paz"])
ciro = np.array([[2.1, 2.5, 3.0, 3.8],   # Gümüşhane
                 [4.2, 4.0, 4.9, 5.5],   # Trabzon
                 [1.5, 1.7, 1.6, 2.2]])  # Bayburt
```

### A. Çoktan seçmeli

1. `print([1, 2, 3] * 2)` komutunun çıktısı nedir?
   - A) `[2, 4, 6]`
   - B) `[1, 2, 3, 1, 2, 3]`
   - C) `12`
   - D) Hata verir
   - E) `[[1, 2, 3], [1, 2, 3]]`
2. `np.array([1, "iki", 3])` dizisinin veri tipi için hangisi doğrudur?
   - A) `int64` olur; "iki" yok sayılır.
   - B) `float64` olur.
   - C) Hata verir.
   - D) Tüm elemanlar metne (Unicode string) dönüşür.
   - E) Her eleman kendi tipini korur.
3. `np.array([1.9, 2.7]).astype(int)` sonucu nedir?
   - A) `[1 2]`
   - B) `[2 3]`
   - C) `[1.9 2.7]`
   - D) `[2 2]`
   - E) Hata verir
4. `np.arange(0, 20, 5)` hangi diziyi üretir?
   - A) `[0 5 10 15 20]`
   - B) `[5 10 15 20]`
   - C) `[0 5 10 15]`
   - D) 0 ile 20 arasında eşit aralıklı 5 sayı
   - E) `[0 4 8 12 16]`
5. `np.linspace(0, 1, 5)` hangi diziyi üretir?
   - A) `[0. 0.2 0.4 0.6 0.8]`
   - B) `[0. 0.25 0.5 0.75 1.]`
   - C) `[0 1 2 3 4]`
   - D) `[0.2 0.4 0.6 0.8 1.]`
   - E) 5 adet rastgele sayı
6. `ciro[:, 3]` ifadesi ne getirir?
   - A) Trabzon şubesinin tüm yılı
   - B) Tüm şubelerin 3. çeyreği
   - C) Tüm şubelerin 4. çeyreği: `[3.8 5.5 2.2]`
   - D) İlk üç satır
   - E) Hata verir; dizi 3 satırlıdır
7. `ciro.sum(axis=0)` sonucunun şekli (shape) nedir?
   - A) `(3,)`
   - B) `(4,)`
   - C) `(3, 4)`
   - D) `(1,)`
   - E) `(12,)`
8. Aşağıdaki kodun son satırı ne yazdırır?

   ```python
   a = np.array([10, 20, 30, 40, 50])
   parca = a[1:3]
   parca[0] = 999
   print(a)
   ```
   - A) `[10 20 30 40 50]`
   - B) `[999 20 30 40 50]`
   - C) `[10 999 30 40 50]`
   - D) `[10 20 999 40 50]`
   - E) Hata verir
9. 60 ile 90 arasındaki (ikisi dahil) notları seçen **doğru** yazım hangisidir?
   - A) `notlar[notlar >= 60 and notlar <= 90]`
   - B) `notlar[notlar >= 60 & notlar <= 90]`
   - C) `notlar[(notlar >= 60) and (notlar <= 90)]`
   - D) `notlar[(notlar >= 60) & (notlar <= 90)]`
   - E) `notlar[60 <= notlar <= 90]`
10. `argmax()` fonksiyonu neyi döndürür?
    - A) En büyük değerin kendisini
    - B) En büyük değerin konumunu (indeksini)
    - C) Tüm değerlerin toplamını
    - D) Dizinin sıralanmış hâlini
    - E) En büyük değerin kaç kez tekrarlandığını
11. `ciro` dizisinin şekli (3, 4)'tür. Aşağıdaki işlemlerden hangisi broadcasting kuralına göre **hata verir**?
    - A) `ciro + np.array([1, 2, 3, 4])`
    - B) `ciro + np.array([[1], [2], [3]])`
    - C) `ciro + np.array([1, 2, 3])`
    - D) `ciro + 10`
    - E) `ciro + np.ones((1, 4))`
12. 12 elemanlı bir dizi için `dizi.reshape(-1, 6)` sonucunun şekli nedir?
    - A) `(6, 2)`
    - B) `(2, 6)`
    - C) `(12, 6)`
    - D) `(-1, 6)`
    - E) Hata verir
13. `np.array([12.5, np.nan, 11.2]).mean()` sonucu nedir?
    - A) `11.85`
    - B) `7.9`
    - C) `nan`
    - D) `0`
    - E) Hata verir
14. NumPy'da tekrarlanabilir rastgele sayı üretmek için önerilen modern yöntem hangisidir?
    - A) `np.random.default_rng(seed=42)`
    - B) `random.random()`
    - C) `np.random.seed()` parametresiz
    - D) `np.rand(42)`
    - E) `np.arange(42)`
15. scikit-learn modeline tek bir özellik (`yas`, şekli `(4,)`) verirken yapılması gereken dönüşüm hangisidir?
    - A) `yas.ravel()`
    - B) `yas.T`
    - C) `yas.reshape(-1, 1)`
    - D) `yas.reshape(1)`
    - E) `yas.flatten()`
16. NumPy dizilerinin Python listelerinden çok daha hızlı olmasının temel nedeni nedir?
    - A) Daha az bellek kullanan metin tipinde saklanmaları
    - B) Tek tip veri tutmaları ve işlemleri C dilinde toplu (vektörel) yapmaları
    - C) Otomatik olarak GPU kullanmaları
    - D) Elemanları sıralı tutmaları
    - E) Eksik değer içerememeleri

### B. Boşluk doldurma (kod çıktısını tahmin et)

1. `(notlar >= 50).sum()` → \_\_\_\_\_\_\_\_\_\_
2. `(notlar >= 50).mean() * 100` → % \_\_\_\_\_\_\_\_\_\_
3. `notlar[(notlar < 35) | (notlar > 90)]` → \_\_\_\_\_\_\_\_\_\_
4. `notlar.mean()` → \_\_\_\_\_\_\_\_\_\_ ve `np.median(notlar)` → \_\_\_\_\_\_\_\_\_\_
5. `siparisler[siparisler > 500]` → \_\_\_\_\_\_\_\_\_\_
6. `((siparisler >= 200) & (siparisler <= 500)).sum()` → \_\_\_\_\_\_\_\_\_\_
7. `gunler[::2]` → \_\_\_\_\_\_\_\_\_\_
8. `gunler[-2]` → \_\_\_\_\_\_\_\_\_\_
9. `ciro.sum(axis=1)` → \_\_\_\_\_\_\_\_\_\_
10. `ciro[1, 2]` → \_\_\_\_\_\_\_\_\_\_
11. `np.arange(1, 13).reshape(4, 3).T.shape` → \_\_\_\_\_\_\_\_\_\_
12. `np.nanmean(np.array([12.5, 14.0, np.nan, 11.2, np.nan, 15.8]))` → \_\_\_\_\_\_\_\_\_\_

### C. Doğru / Yanlış

1. NumPy dizileri farklı tipteki elemanları olduğu gibi, dönüştürmeden tutar.
2. NumPy dilimlemesinde `başlangıç:bitiş` ifadesindeki bitiş indeksi sonuca dahildir.
3. `axis=0` parametresi her sütun için bir sonuç üretir.
4. `astype(int)` ondalıklı sayıları en yakın tam sayıya yuvarlar.
5. Rastgele sayı üretecinin tohumu (seed) sabitlenirse kod her çalıştırıldığında aynı sonuçlar elde edilir.
6. Boolean maskeleri birleştirmek için Python'un `and` ve `or` anahtar kelimeleri kullanılır.
7. Bir dilim üzerinde yapılan değişikliğin orijinal diziyi etkilememesi için `.copy()` kullanılır.
8. `np.where(kosul, a, b)` ifadesi Excel'deki EĞER fonksiyonuna benzer şekilde çalışır.

### D. Kısa cevap ve kod yazma

1. "Dilim bir kopya değil, görünümdür (view)" ifadesini bir kod örneğiyle açıklayın.
2. Broadcasting kuralını kendi cümlelerinizle yazın. (3, 4) ve (3, 1) şekilli iki dizi toplanırsa sonucun şekli ne olur?
3. `axis=0` ile `axis=1` arasındaki farkı `ciro` dizisi üzerinden açıklayın. "Verilen eksen yok olur" kuralını kullanın.
4. `ciro` dizisinde yıllık cirosu en yüksek şubenin adını yazdıran kodu yazın (`subeler = np.array(["Gümüşhane", "Trabzon", "Bayburt"])`). Sonuç ne olur?
5. Aşağıdaki not matrisinde her **sınavın** sınıf ortalamasını hesaplayan kodu yazın ve sonucu bulun.

   ```python
   sinavlar = np.array([[70, 85, 90], [55, 60, 48], [92, 88, 95], [65, 72, 80]])
   ```
6. Aynı matriste ortalaması en yüksek öğrenci hangisidir? (`ogrenciler = ["Ayşe", "Mehmet", "Zeynep", "Emre"]`) Ortalamasını da yazın.
7. `notlar` dizisinde 50'nin altındaki notlara 10 puan ekleyen (100'ü geçmeyecek şekilde) kodu `np.where` ile yazın. 45, 33 ve 29 notları neye dönüşür?
8. `siparisler` dizisinde 300 TL ve üzeri siparişler için "Ücretsiz Kargo", diğerleri için "Kargo Ücretli" yazan bir dizi üreten kodu yazın. Kaç sipariş ücretsiz kargo alır?
9. Bir `X` matrisinin her sütununu min-maks yöntemiyle normalleştiren tek satırlık kodu broadcasting kullanarak yazın.
10. Aynı matrisi z-skor ile standartlaştıran kodu yazın. Sonucun doğru olduğunu nasıl kontrol edersiniz?
11. `müşteriler` matrisinin yaş sütunu `[25, 42, 35, 58, 30]` ise 42 yaşın min-maks değeri kaçtır? (3 ondalık)
12. Bir dizideki `np.nan` değerlerini dizinin ortalamasıyla dolduran kodu yazın. Neden `mean()` yerine `np.nanmean()` kullanılmalıdır?

## pandas

Kod sorularında defterdeki `nufus` serisi ve `ogrenciler` tablosu kullanılmıştır; `df` ise defterdeki e-ticaret sipariş veri setidir.

```python
import pandas as pd
nufus = pd.Series({"İstanbul": 15.7, "Ankara": 5.8, "İzmir": 4.5,
                   "Trabzon": 0.82, "Gümüşhane": 0.14}, name="Nüfus (milyon)")
ogrenciler = pd.DataFrame({
    "ad":    ["Ayşe", "Mehmet", "Zeynep", "Emre", "Elif"],
    "bolum": ["YBS", "İşletme", "YBS", "İktisat", "YBS"],
    "vize":  [70, 55, 92, 65, 80],
    "final": [85, 48, 95, 72, 60],
})
```

### A. Çoktan seçmeli

1. pandas'taki `Series` yapısı için en doğru tanım hangisidir?
   - A) İki boyutlu bir tablo
   - B) NumPy dizisine indeks (etiket) eklenmiş tek boyutlu yapı
   - C) Python sözlüğünün başka bir adı
   - D) Yalnızca metin tutan bir liste
   - E) Bir grafik nesnesi
2. Sütun tiplerini, eksik olmayan değer sayılarını ve bellek kullanımını gösteren komut hangisidir?
   - A) `df.head()`
   - B) `df.describe()`
   - C) `df.info()`
   - D) `df.shape`
   - E) `df.sample()`
3. `ogrenciler.loc[1:3]` ve `ogrenciler.iloc[1:3]` sırasıyla kaç satır döndürür?
   - A) 3 ve 3
   - B) 2 ve 2
   - C) 3 ve 2
   - D) 2 ve 3
   - E) 4 ve 3
4. Bir kategorik sütundaki değerlerin **oranlarını** veren komut hangisidir?
   - A) `df["odeme"].value_counts(normalize=True)`
   - B) `df["odeme"].nunique()`
   - C) `df["odeme"].unique()`
   - D) `df["odeme"].describe()`
   - E) `df["odeme"].count()`
5. `il` sütunu "Trabzon" veya "Gümüşhane" olan satırları seçmek için en uygun yöntem hangisidir?
   - A) `df[df["il"] == ["Trabzon", "Gümüşhane"]]`
   - B) `df[df["il"].isin(["Trabzon", "Gümüşhane"])]`
   - C) `df[df["il"].contains("Trabzon", "Gümüşhane")]`
   - D) `df.loc["Trabzon":"Gümüşhane"]`
   - E) `df.groupby(["Trabzon", "Gümüşhane"])`
6. Tekrar eden satırları silen komut hangisidir?
   - A) `df.dropna()`
   - B) `df.duplicated()`
   - C) `df.drop_duplicates()`
   - D) `df.unique()`
   - E) `df.reset_index()`
7. Defterde `"  ankara "` ve `"İSTANBUL"` gibi tutarsız yazımları düzeltmek için hangi zincir kullanılmıştır?
   - A) `.str.strip().str.title()`
   - B) `.fillna().dropna()`
   - C) `.astype(int)`
   - D) `.str.contains()`
   - E) `.map(len)`
8. Defterde eksik `puan` değerleri nasıl doldurulmuştur?
   - A) Tüm sütunun ortalamasıyla
   - B) 0 ile
   - C) Ürünün kendi medyan puanıyla (`groupby("urun")["puan"].transform("median")`)
   - D) Satırlar silinerek
   - E) "Bilinmiyor" yazılarak
9. `pd.cut` fonksiyonunun görevi nedir?
   - A) Tabloyu ikiye bölmek
   - B) Sayısal bir değişkeni belirlenen aralıklara bölmek (ayrıklaştırma)
   - C) Metinleri kesmek
   - D) Eksik değerleri silmek
   - E) İki tabloyu birleştirmek
10. `groupby` işleminin arkasındaki mantık nasıl ifade edilir?
    - A) Oku → Yaz → Kaydet
    - B) Böl → Uygula → Birleştir
    - C) Temizle → Birleştir → İndirge
    - D) Sırala → Filtrele → Sil
    - E) Seç → Kopyala → Yapıştır
11. Sipariş tablosu, bazı müşterilerin bulunmadığı müşteri tablosuyla `how="left"` kullanılarak birleştirilirse ne olur?
    - A) Eşleşmeyen siparişler atılır.
    - B) Tüm siparişler korunur; eşleşmeyenlerin müşteri bilgileri NaN olur.
    - C) Yalnızca müşteri tablosundaki satırlar kalır.
    - D) Hata verir.
    - E) Tablolar alt alta eklenir.
12. Aynı yapıdaki iki tabloyu (ör. Ocak ve Şubat siparişleri) alt alta eklemek için hangi fonksiyon kullanılır?
    - A) `merge`
    - B) `pivot_table`
    - C) `concat`
    - D) `crosstab`
    - E) `resample`
13. `df.set_index("tarih").resample("ME")["tutar"].sum()` ne hesaplar?
    - A) Haftalık toplam tutar
    - B) Aylık toplam tutar
    - C) Yıllık ortalama tutar
    - D) Günlük en büyük tutar
    - E) Müşteri başına tutar
14. `to_csv(..., encoding="utf-8-sig")` seçeneğinin amacı nedir?
    - A) Dosyayı şifrelemek
    - B) Dosyayı sıkıştırmak
    - C) Excel'de Türkçe karakterlerin düzgün görünmesini sağlamak
    - D) Tarih sütunlarını korumak
    - E) İndeksi silmek
15. `df["tarih"].dt.dayofweek >= 5` koşulu hangi günleri seçer?
    - A) Pazartesi ve Salı
    - B) Cuma ve Cumartesi
    - C) Cumartesi ve Pazar
    - D) Yalnızca Pazar
    - E) Hafta içi günleri
16. `pd.crosstab(df["kategori"], df["memnuniyet"], normalize="index")` hangi tabloyu üretir?
    - A) Her kategorinin içinde memnuniyet düzeylerinin oranları (satır toplamları 1)
    - B) Kategori başına toplam ciro
    - C) Memnuniyet düzeyine göre ortalama fiyat
    - D) Korelasyon matrisi
    - E) Eksik değer sayıları

### B. Boşluk doldurma (kod çıktısını tahmin et)

1. `nufus[nufus > 1]` kaç il döndürür? → \_\_\_\_\_\_\_\_\_\_
2. `nufus.mean().round(2)` → \_\_\_\_\_\_\_\_\_\_
3. `nufus.idxmax()` → \_\_\_\_\_\_\_\_\_\_
4. `ogrenciler.shape` → \_\_\_\_\_\_\_\_\_\_
5. `ogrenciler["vize"].mean()` → \_\_\_\_\_\_\_\_\_\_
6. `(ogrenciler["bolum"] == "YBS").sum()` → \_\_\_\_\_\_\_\_\_\_
7. `ogrenciler[ogrenciler["final"] > 70]["ad"].tolist()` → \_\_\_\_\_\_\_\_\_\_
8. `ogrenciler.groupby("bolum")["vize"].mean()` sonucunda YBS'nin değeri (2 ondalık) → \_\_\_\_\_\_\_\_\_\_
9. `ogrenciler.loc[1, "ad"]` → \_\_\_\_\_\_\_\_\_\_
10. `ogrenciler.iloc[2, 2]` → \_\_\_\_\_\_\_\_\_\_
11. `ogrenciler.loc[(ogrenciler["bolum"] == "YBS") & (ogrenciler["vize"] >= 75), "ad"].tolist()` → \_\_\_\_\_\_\_\_\_\_
12. `bins=[0, 500, 5000, 50000, np.inf]` ve etiketler `["Düşük", "Orta", "Yüksek", "Çok Yüksek"]` ile `pd.cut` uygulandığında 500 TL'lik bir tutar \_\_\_\_\_\_\_\_\_\_, 4.800 TL'lik bir tutar \_\_\_\_\_\_\_\_\_\_ grubuna düşer.

### C. Doğru / Yanlış

1. `loc` ile yapılan dilimlemede bitiş etiketi sonuca dahildir.
2. `iloc` satırları etiketlerine (isimlerine) göre seçer.
3. `dropna()` ile eksik satırları silmek en kolay yoldur ama veri kaybına yol açar.
4. Kategorik bir değişkendeki (ör. `il`) eksik değerler sütunun ortalamasıyla doldurulur.
5. pandas'ta koşulları birleştirirken `&` yerine `and` kullanılabilir.
6. `how="inner"` ile yapılan `merge`, sonuçtaki satır sayısını azaltabilir.
7. `"İSTANBUL".lower()` işlemi Türkçede her zaman beklenen `"istanbul"` sonucunu verir.
8. `df.describe(exclude="number")` sayısal olmayan sütunların özetini verir.

### D. Kısa cevap ve kod yazma

1. Defterdeki kirli veri setinde bilerek oluşturulan dört veri kalitesi sorununu ve her birinin pandas'taki çözümünü yazın.
2. Yeni bir veri setiyle karşılaştığınızda çalıştırdığınız ilk beş komutu ve her birinin ne gösterdiğini yazın.
3. Ankara'dan kredi kartıyla verilmiş siparişleri seçen kodu yazın.
4. `ogrenciler` tablosuna, vizenin %40'ı ve finalin %60'ından oluşan `ortalama` sütununu ekleyen kodu yazın. Zeynep'in ortalaması kaç olur?
5. `df` için kategori bazında sipariş sayısı, toplam ciro ve ortalama puanı tek tabloda veren `groupby` + `agg` kodunu yazın.
6. `inner` ve `left` join arasındaki farkı defterdeki müşteri tablosu örneğiyle (76–80 numaralı müşteriler yok) açıklayın.
7. Eksik puanları genel ortalama yerine ürün bazında medyanla doldurmanın neden daha akıllıca olduğunu, 2. haftadaki "sınıf ortalaması" kavramıyla ilişkilendirerek açıklayın.
8. Satırlarda `kategori`, sütunlarda `mevsim`, hücrelerde toplam `tutar` olan ve toplam satır/sütunu içeren pivot tablo kodunu yazın.
9. RFM analizinde R, F ve M'nin neyi ölçtüğünü yazın. Bir müşterinin R değerinin düşük olması iyi mi kötü mü?
10. `pd.cut` ile `pd.qcut` arasındaki fark nedir? RFM çözümünde M değerini "Bronz / Gümüş / Altın" olarak gruplamak için neden `qcut` kullanılmıştır?

## Matplotlib

### A. Çoktan seçmeli

1. Birden fazla grafik ve ince ayar gerektiğinde önerilen çizim arayüzü hangisidir?
   - A) `plt.plot(...)` ile durum tabanlı arayüz
   - B) `fig, ax = plt.subplots()` ile nesne yönelimli arayüz
   - C) Excel grafikleri
   - D) `print()` ile metin çıktısı
   - E) `np.plot(...)`
2. Matplotlib'de **Figure** ve **Axes** arasındaki ilişki için hangisi doğrudur?
   - A) Axes tüm tuvaldir; Figure tek bir grafik alanıdır.
   - B) Figure tüm tuvaldir; bir veya daha fazla Axes (tek grafik alanı) içerir.
   - C) İkisi aynı şeyin farklı adlarıdır.
   - D) Axes yalnızca eksen etiketlerini ifade eder.
   - E) Figure yalnızca kaydedilen dosyadır.
3. Bir mağaranın 12 aylık ziyaretçi sayısındaki eğilimi göstermek için en uygun grafik hangisidir?
   - A) Pasta
   - B) Histogram
   - C) Çizgi
   - D) Kutu
   - E) Isı haritası
4. Sayısal bir değişkenin simetrik mi, çarpık mı, kaç tepeli mi olduğunu görmek için hangi grafik kullanılır?
   - A) Histogram
   - B) Pasta
   - C) Sütun
   - D) Çizgi
   - E) Saçılım
5. Üç bölümün not dağılımlarını karşılaştırıp aykırı değerleri görmek için en uygun grafik hangisidir?
   - A) Pasta
   - B) Çizgi
   - C) Yığılmış sütun
   - D) Kutu grafiği (boxplot)
   - E) Histogram
6. Haftalık çalışma süresi ile sınav notu arasındaki ilişkiyi incelemek için hangi grafik kullanılır?
   - A) Pasta
   - B) Saçılım (scatter)
   - C) Histogram
   - D) Yatay sütun
   - E) Kutu
7. Pasta grafiği hangi durumda uygun **değildir**?
   - A) 4 ödeme yönteminin toplamdaki payını gösterirken
   - B) 12 kategorinin birbirine yakın değerlerini karşılaştırırken
   - C) Az sayıda parçanın bütüne oranını gösterirken
   - D) 3 segmentin pazar payını gösterirken
   - E) Yüzdelikleri `autopct` ile yazarken
8. Sağa çarpık bir dağılımda (ör. aylık gelir) ortalama ile medyan arasındaki ilişki nasıldır?
   - A) Ortalama < medyan
   - B) Ortalama = medyan
   - C) Ortalama > medyan
   - D) İkisi arasında ilişki yoktur
   - E) Medyan hesaplanamaz
9. Kutu grafiğinde bıyıkların uzandığı sınır neye göre belirlenir?
   - A) Ortalamanın 2 standart sapma ötesi
   - B) 1,5 × IQR
   - C) Minimum ve maksimum değer, her zaman
   - D) Medyanın iki katı
   - E) 3 × IQR
10. `linestyle="--"` parametresi çizgiyi nasıl çizer?
    - A) Düz
    - B) Noktalı
    - C) Kesikli
    - D) Nokta-çizgi
    - E) Görünmez
11. `savefig` ile ilgili doğru kullanım hangisidir?
    - A) `plt.show()`'dan sonra çağrılmalıdır.
    - B) `plt.show()`'dan önce çağrılmalıdır; aksi hâlde boş resim kaydedilebilir.
    - C) Yalnızca `.jpg` formatında kayıt yapar.
    - D) `dpi` parametresi almaz.
    - E) Yalnızca pyplot arayüzüyle çalışır.
12. `fig, axes = plt.subplots(2, 2)` ile oluşturulan panelde **sol alttaki** grafiğe nasıl erişilir?
    - A) `axes[0, 0]`
    - B) `axes[0, 1]`
    - C) `axes[1, 0]`
    - D) `axes[1, 1]`
    - E) `axes[2]`
13. Kategori sayısı fazla veya kategori isimleri uzunsa hangi grafik tercih edilmelidir?
    - A) Yatay sütun grafiği (`barh`)
    - B) Pasta grafiği
    - C) Çizgi grafiği
    - D) Histogram
    - E) Saçılım grafiği
14. `ax.bar_label(cubuklar, fmt="%d bin ₺")` komutu ne yapar?
    - A) Eksen başlığını yazar.
    - B) Değerleri çubukların üstüne yazar.
    - C) Açıklama (legend) ekler.
    - D) Çubukları sıralar.
    - E) Grafiği kaydeder.
15. Korelasyon ısı haritasında çok yüksek korelasyonlu değişkenler modelde hangi soruna yol açabilir?
    - A) Eksik veri
    - B) Çoklu doğrusal bağlantı
    - C) Kayıplı sıkıştırma
    - D) Şema uyuşmazlığı
    - E) Hayatta kalma yanılgısı
16. pandas'ta `satis_df.plot(...)` komutu ne döndürür?
    - A) Bir NumPy dizisi
    - B) Bir `Axes` nesnesi; matplotlib ile özelleştirmeye devam edilebilir
    - C) Bir CSV dosyası
    - D) Hiçbir şey
    - E) Yeni bir DataFrame

### B. Boşluk doldurma

1. Y eksenini 0–4 aralığına sabitlemek için `ax.__________(0, 4)` kullanılır.
2. 2,00 seviyesine yatay bir çizgi eklemek için `ax.__________(2.00, color="red", linestyle="--")` kullanılır.
3. Grafiğe ok işaretli bir not (ör. "Zirve: 2300") eklemek için `ax.__________` kullanılır.
4. Çoklu grafik paneline genel bir başlık eklemek için `fig.__________` kullanılır.
5. Paneldeki grafiklerin başlık ve etiketlerinin üst üste binmesini önlemek için `plt.__________()` çağrılır.
6. Üçgen işaretçi kullanmak için `marker="__________"` yazılır.
7. Saydamlığı 0–1 arasında ayarlayan parametre \_\_\_\_\_\_\_\_\_\_ dir.
8. Saçılım grafiğinde noktaları bir değişkene göre renklendirmek için `c=` ve `cmap=` kullanılır; renk skalasını göstermek için `fig.__________` eklenir.
9. `np.polyfit(x, y, deg=1)` iki değer döndürür: eğim ve \_\_\_\_\_\_\_\_\_\_.
10. Bir stili yalnızca belirli bir blok içinde geçerli kılmak için `with plt.style.__________("ggplot"):` kullanılır.
11. pandas ile yığılmış sütun grafiği çizmek için `df.plot(kind="bar", __________=True)` yazılır.
12. Baskı kalitesinde kayıt için `.pdf` veya `.svg` formatı, sunum/rapor için `dpi=__________` aralığı önerilir.

### C. Doğru / Yanlış

1. Pasta grafiği, 12 ayın satışlarını karşılaştırmak için en iyi seçimdir.
2. Histogram, kategorik değişkenlerin değerlerini karşılaştırmak için kullanılır.
3. Sağa çarpık dağılımlarda medyan, ortalamadan daha güvenilir bir merkez ölçüsüdür.
4. Her grafiğin bir başlığı, eksen etiketleri ve birden fazla seri varsa açıklaması (legend) olmalıdır.
5. `bins` sayısını değiştirmek histogramın görünümünü etkilemez.
6. Yatay sütun grafiğinde çubukları sıralamak okunabilirliği artırır.
7. `plt.subplots(1, 3)` ile oluşturulan `axes` bir NumPy dizisidir.
8. Görselleştirme yalnızca veri madenciliğinin sonunda, sonuçları raporlamak için kullanılır.

### D. Kısa cevap ve kod yazma

1. Aşağıdaki her senaryo için uygun grafik türünü yazın: (a) 2024 ve 2025 aylık ziyaretçi karşılaştırması (b) Beş kategorinin yıllık cirosu (c) 400 öğrencinin not dağılımı (d) Reklam harcaması ile satış ilişkisi (e) 4 ödeme yönteminin payı (f) Beş değişken arasındaki korelasyonlar.
2. `pyplot` (durum tabanlı) arayüz ile nesne yönelimli arayüzün farkını birer kod satırıyla gösterin.
3. 8 dönemlik GNO değerleri için üçgen işaretçili, y ekseni 0–4 aralığında, 2,00'de kırmızı kesikli çizgisi olan ve tüm etiketleri yazılmış bir çizgi grafiğinin kodunu yazın.
4. Aşağıdaki kodda kaydedilen resim boş çıkıyor. Hata nedir, nasıl düzeltilir?

   ```python
   fig, ax = plt.subplots()
   ax.plot(aylar, ziyaretci)
   plt.show()
   fig.savefig("ziyaretci.png")
   ```
5. Bir kutu grafiğinde kutu, kutunun içindeki çizgi, bıyıklar ve tek tek noktalar neyi gösterir?
6. İki şubenin dört çeyreklik cirosunu yan yana (gruplandırılmış) sütunlarla göstermek için x konumlarını neden `x - genislik/2` ve `x + genislik/2` olarak kaydırırız?
7. 1×2'lik bir panelin solunda metrekare–fiyat saçılımı (oda sayısına göre renkli, renk çubuklu), sağında fiyat histogramı olacak kodu yazın.
8. Saçılım grafiğinde çalışma saati ile not arasında r = 0,85 bulunmuştur. Bu sonucu yorumlayın ve 1. haftadaki "korelasyon nedensellik değildir" ilkesiyle ilişkilendirin.
9. Müşteri segmentlerini (Ekonomik, Standart, Premium) yaş–gelir saçılımında farklı renklerle göstermek neden sınıflandırma/kümeleme sonuçlarını sunmanın temel yoludur?
10. Görselleştirme veri madenciliğinin hangi iki aşamasında kullanılır? Her biri için bir örnek verin ve Datasaurus örneğiyle bağlantı kurun.

## Cevap Anahtarı

### Hafta 1 – Temel Kavramlar

**A. Çoktan seçmeli:** 1-B · 2-D · 3-C · 4-C · 5-C · 6-B · 7-D · 8-B · 9-B · 10-E · 11-D · 12-B · 13-C · 14-B · 15-E · 16-C · 17-A · 18-B · 19-B · 20-C

**B. Boşluk doldurma:** 1) adımı · 2) R. Ackoff · 3) üst veri (metadata) · 4) OLAP · 5) Deep Blue · 6) AlphaGo · 7) aşırı öğrenme (overfitting) · 8) denetimli; denetimsiz · 9) aykırı · 10) uyumsuzluk · 11) veri dönüştürme (kesikleştirme) · 12) kumarbaz · 13) su pompası · 14) birliktelik · 15) yaz / sıcak hava

**C. Doğru / Yanlış:** 1-Y · 2-D · 3-D · 4-Y (denetimsizdir) · 5-D · 6-D · 7-Y (bu geleneksel istatistiğin özelliğidir; VM temizlenmiş veriyle çalışır) · 8-Y (denetimlidir) · 9-Y (geleceğe yöneliktir) · 10-D

**D. Kısa cevap ve hesaplama:**

1. Sıralı: 3, 8, 12 | 15, 22, 27 | 31, 35, 40. (a) Ortalama: 7,67 × 3 | 21,33 × 3 | 35,33 × 3. (b) Sınır değerleri: 3, 12, 12 | 15, 27, 27 | 31, 31, 40 (8 → 12'ye 4, 3'e 5 uzaklıkta; 22 → 27'ye yakın; 35 → 31'e yakın).
2. Amacın tanımlanması → Ön işlemler (ikisi de VM öncesi) → Modelin kurulması ve değerlendirilmesi (VM'nin kendisi) → Modelin kullanılması ve yorumlanması → Modelin izlenmesi (ikisi de VM sonrası).
3. Sınıflandırmada sınıflar önceden bellidir (denetimli): geçmiş "ödedi / ödemedi" etiketli kredi verisiyle yeni başvuruyu sınıflandırmak. Kümelemede etiket yoktur (denetimsiz): müşterileri alışveriş davranışına göre benzer segmentlere ayırmak.
4. Algoritma sabit değeri gerçek bir değer sanarak yanılabilir; seçilen kod başka anlamlı bir değerle çakışabilir ve dağılımı bozar.
5. Korelasyon nedensellik sanılmıştır (cum hoc ergo propter hoc). Karıştırıcı değişken ev büyüklüğüdür: büyük evlerde hem daha çok çocuk hem daha çok yuva yeri vardır.
6. Göreceli artış: (3 − 2) / 2 = %50. Mutlak artış: 10.000'de 1 = %0,01. Haber, çok küçük bir mutlak artışı büyük göreceli yüzdeyle sunduğu için yanıltıcıdır.
7. Örnek: SQL → "Geçen ay toplam kaç litre süt sattık?"; OLAP → "Ekim'de Ankara şubelerinde kategori bazında satış geçen yıla göre nasıl?"; VM → "Hangi ürünler birlikte alınıyor?" veya "Hangi müşteriler bizi bırakmak üzere?"
8. Örnek: Yalnızca başarılı girişimleri inceleyip "okulu bırakmak başarı getirir" sonucuna varmak. Doğru analiz, batan girişimleri de örnekleme katmaktır. (Benzer şekilde, yalnızca kalan müşterilere memnuniyet anketi yapmak da yanıltır.)

### Hafta 2 – Verinin Hazırlanması

**A. Çoktan seçmeli:** 1-D · 2-E · 3-C · 4-A · 5-B · 6-B · 7-A · 8-C · 9-C · 10-D · 11-B · 12-C · 13-B · 14-D · 15-E (2²⁵) · 16-C · 17-A · 18-C · 19-C (8.450 / 10⁴ = 0,845) · 20-B

**B. Boşluk doldurma:** 1) temizleme, birleştirme, indirgeme, dönüştürme · 2) bölmeleme (binning) · 3) kayıpsız (lossless) · 4) parametrik · 5) ileriye doğru seçme · 6) geriye doğru eleme · 7) işlevsel · 8) bir araya getirme (aggregation) · 9) \[0, 1\] · 10) küçük · 11) n (popülasyon); n − 1 (örneklem) · 12) z-skor; min-maks · 13) most\_frequent · 14) isimsel

**C. Doğru / Yanlış:** 1-Y (uygulanamaz alanlar olabilir) · 2-Y (aralıklı ölçekte oran hesaplanamaz) · 3-Y · 4-Y (çok daha yüksektir) · 5-Y (amaç yalnızca ölçeklemedir) · 6-D · 7-D · 8-Y · 9-D · 10-Y (ortalama 0, std 1; değerler negatif veya 1'den büyük olabilir)

**D. Kısa cevap ve hesaplama:**

1. (a) Min-maks (payda 60): 0 · 0,25 · 0,50 · 0,75 · 1. (b) Z-skor: X̄ = 50; Σ(X − X̄)² = 900 + 225 + 0 + 225 + 900 = 2.250; s = √(2.250 / 4) = √562,5 ≈ 23,717 → −1,265 · −0,632 · 0 · 0,632 · 1,265. (c) Ondalık: max = 80 → j = 2 → 0,20 · 0,35 · 0,50 · 0,65 · 0,80.
2. (30 − 6) / (54 − 6) = 24 / 48 = **0,5**.
3. max|X| = 1.250 → j = 4 → −0,125 · 0,034 · 0,0875 · −0,006.
4. (a) İsimsel (b) Sıra gösteren (c) Oranlı (0 K gerçek yokluktur) (d) Tamsayılı (e) İkili (f) Aralıklı (g) Oranlı.
5. 2¹⁵ = 32.768 alt küme. Alt küme sayısı özellik sayısıyla üstel büyüdüğü için hepsini denemek pratik değildir; ileriye doğru seçme, geriye doğru eleme gibi sezgisel yöntemler kullanılır.
6. Örnek: "Eşinin adı" alanı bekâr kişilerde boşsa uygulanamazdır; evli bir kişide boşsa eksik veridir. Uygulanamaz alan doldurulursa hatalı bilgi üretilir.
7. Öklid mesafesi neredeyse tamamen maaş farkına göre belirlenir, yaşın etkisi kaybolur. Normalleştirme iki özelliğin mesafeye eşit ağırlıkla katkı yapmasını sağlar.
8. Şema uyuşmazlığı → meta veri ve veri sözlükleri; veri fazlalığı → korelasyon analizi; veri değer karmaşası → birim dönüşümü ve standartlaştırma.

### NumPy

**A. Çoktan seçmeli:** 1-B · 2-D · 3-A · 4-C · 5-B · 6-C · 7-B · 8-C · 9-D · 10-B · 11-C · 12-B · 13-C · 14-A · 15-C · 16-B

**B. Kod çıktısı:** 1) 7 · 2) 70.0 · 3) `[92 33 29 95]` · 4) 63.8 ve 63.5 · 5) `[620 1250 760 980]` · 6) 4 · 7) `['Pzt' 'Çar' 'Cum' 'Paz']` · 8) `'Cmt'` · 9) `[11.4 18.6 7.]` · 10) 4.9 · 11) `(3, 4)` · 12) 13.375

**C. Doğru / Yanlış:** 1-Y (ortak tipe dönüştürür) · 2-Y · 3-D · 4-Y (keser) · 5-D · 6-Y (`&`, `|`, `~` kullanılır) · 7-D · 8-D

**D. Kısa cevap ve kod yazma:**

1. `a = np.array([10, 20, 30]); p = a[0:2]; p[0] = 99` sonrasında `a` da `[99 20 30]` olur, çünkü dilim aynı belleği gösterir. Bağımsız kopya için `a[0:2].copy()` kullanılır.
2. Şekiller sağdan karşılaştırılır; her boyut ya eşit ya da biri 1 olmalıdır. 1 olan boyut diğerine uyacak şekilde genişletilir. (3, 4) + (3, 1) → (3, 4).
3. `axis=0` satır eksenini yok eder, her sütun (çeyrek) için bir sonuç verir: `[7.8 8.2 9.5 11.5]`. `axis=1` sütun eksenini yok eder, her satır (şube) için bir sonuç verir: `[11.4 18.6 7.]`.
4. `print(subeler[ciro.sum(axis=1).argmax()])` → **Trabzon** (18,6 milyon TL).
5. `sinavlar.mean(axis=0)` → `[70.5 76.25 78.25]`.
6. `ogrenciler[sinavlar.mean(axis=1).argmax()]` → **Zeynep**, ortalama 91,67.
7. `yeni = np.where(notlar < 50, np.minimum(notlar + 10, 100), notlar)` → 45 → 55, 33 → 43, 29 → 39.
8. `np.where(siparisler >= 300, "Ücretsiz Kargo", "Kargo Ücretli")` → 8 sipariş ücretsiz kargo alır.
9. `(X - X.min(axis=0)) / (X.max(axis=0) - X.min(axis=0))`
10. `z = (X - X.mean(axis=0)) / X.std(axis=0)`. Kontrol: `z.mean(axis=0)` ≈ 0 ve `z.std(axis=0)` ≈ 1 olmalıdır.
11. (42 − 25) / (58 − 25) = 17 / 33 ≈ **0,515**.
12. `dolu = np.where(np.isnan(d), np.nanmean(d), d)`. `mean()` dizide tek bir `nan` olsa bile `nan` döndürür; `nanmean()` eksikleri yok sayarak hesaplar.

### pandas

**A. Çoktan seçmeli:** 1-B · 2-C · 3-C · 4-A · 5-B · 6-C · 7-A · 8-C · 9-B · 10-B · 11-B · 12-C · 13-B · 14-C · 15-C · 16-A

**B. Kod çıktısı:** 1) 3 (İstanbul, Ankara, İzmir) · 2) 5.39 · 3) `'İstanbul'` · 4) `(5, 4)` · 5) 72.4 · 6) 3 · 7) `['Ayşe', 'Zeynep', 'Emre']` · 8) 80.67 · 9) `'Mehmet'` · 10) 92 · 11) `['Zeynep', 'Elif']` · 12) Düşük (aralıklar sağdan kapalıdır: (0, 500\]); Orta

**C. Doğru / Yanlış:** 1-D · 2-Y (konuma göre seçer) · 3-D · 4-Y (mod veya "Bilinmiyor" kullanılır) · 5-Y · 6-D · 7-Y (noktalı i + birleşik nokta çıkar) · 8-D

**D. Kısa cevap ve kod yazma:**

1. Tekrar eden satırlar → `duplicated()` / `drop_duplicates()`; tutarsız il yazımı → `.str.strip().str.title()` + `replace`; hatalı adet (−1) → `df[df["adet"] > 0]`; eksik il ve puan → `fillna("Bilinmiyor")` ve ürün bazında medyan.
2. `head()` (ilk satırlar), `info()` (tipler, eksikler), `describe()` (özet istatistik), `value_counts()` (kategori dağılımı), `shape` / `nunique()` (boyut, benzersiz değer sayısı).
3. `df[(df["il"] == "Ankara") & (df["odeme"] == "Kredi Kartı")]`
4. `ogrenciler["ortalama"] = ogrenciler["vize"] * 0.4 + ogrenciler["final"] * 0.6` → Zeynep: 92 × 0,4 + 95 × 0,6 = 36,8 + 57 = **93,8**.
5. `df.groupby("kategori").agg(siparis_sayisi=("siparis_id", "count"), toplam_ciro=("tutar", "sum"), ortalama_puan=("puan", "mean"))`
6. `inner` join'de 76–80 numaralı müşterilerin siparişleri tablodan atılır. `left` join'de tüm siparişler korunur; bu siparişlerin cinsiyet, yaş ve üyelik bilgileri NaN olur.
7. Ürünlerin puan düzeyleri birbirinden farklıdır. Eksik değeri kendi grubunun (ürünün) değeriyle doldurmak, 2. haftadaki sınıf ortalaması mantığıyla aynıdır ve genel ortalamadan daha isabetlidir. Medyan ayrıca aykırı değerlerden etkilenmez.
8. `pd.pivot_table(df, values="tutar", index="kategori", columns="mevsim", aggfunc="sum", fill_value=0, margins=True, margins_name="Toplam")`
9. R: son alışverişten bu yana geçen gün; F: toplam sipariş sayısı; M: toplam harcama. Düşük R iyidir, müşteri yakın zamanda alışveriş yapmıştır.
10. `pd.cut` verilen sınır değerlerine göre böler; gruplardaki eleman sayıları farklı olabilir. `pd.qcut` yüzdeliklere göre böler, her grupta yaklaşık eşit sayıda gözlem olur. RFM'de müşterileri eşit büyüklükte üç segmente ayırmak istendiği için `qcut` kullanılmıştır.

### Matplotlib

**A. Çoktan seçmeli:** 1-B · 2-B · 3-C · 4-A · 5-D · 6-B · 7-B · 8-C · 9-B · 10-C · 11-B · 12-C · 13-A · 14-B · 15-B · 16-B

**B. Boşluk doldurma:** 1) `set_ylim` · 2) `axhline` · 3) `annotate` · 4) `suptitle` · 5) `tight_layout` · 6) `^` · 7) `alpha` · 8) `colorbar` · 9) kesişim (sabit terim) · 10) `context` · 11) `stacked` · 12) 150–300

**C. Doğru / Yanlış:** 1-Y (zaman için çizgi, karşılaştırma için sütun) · 2-Y (sayısal dağılım içindir) · 3-D · 4-D · 5-Y · 6-D · 7-D · 8-Y (başında da kullanılır)

**D. Kısa cevap ve kod yazma:**

1. (a) Çizgi (iki seri + legend) (b) Sütun (c) Histogram (d) Saçılım (e) Pasta veya sütun (f) Isı haritası (`imshow` + `corr()`).
2. Durum tabanlı: `plt.plot(x, y); plt.title("...")`. Nesne yönelimli: `fig, ax = plt.subplots(); ax.plot(x, y); ax.set_title("...")`.
3. Aşağıdaki "D3 çözümü" koduna bakın.
4. `savefig`, `plt.show()`'dan sonra çağrıldığı için figür temizlenmiş olabilir. Çözüm: `fig.savefig("ziyaretci.png", dpi=150, bbox_inches="tight")` satırını `plt.show()`'dan önceye alın.
5. Kutu: Q1–Q3 aralığı (IQR); içindeki çizgi: medyan; bıyıklar: 1,5 × IQR sınırına kadar olan değerler; tek tek noktalar: aykırı değerler.
6. Aynı x konumuna çizilen iki çubuk üst üste biner. Yarım genişlik sola ve sağa kaydırmak çubukları yan yana koyar; etiket ise `ax.set_xticks(x, ceyrekler)` ile ortaya yazılır.
7. Aşağıdaki "D7 çözümü" koduna bakın.
8. Güçlü pozitif doğrusal ilişki vardır: çalışma süresi arttıkça not artma eğilimindedir. Ancak bu, çalışmanın notu artırdığını tek başına kanıtlamaz; motivasyon veya derse devam gibi karıştırıcı değişkenler olabilir.
9. Her grup ayrı renkle çizilince grupların birbirinden ayrışıp ayrışmadığı, sınırları ve örtüşen bölgeler tek bakışta görülür; bu, bir modelin ürettiği sınıfları veya kümeleri değerlendirmenin en hızlı yoludur.
10. Başta: veriyi tanımak, aykırı değerleri ve ilişkileri görmek (ör. histogram, kutu grafiği). Sonda: model sonuçlarını raporlamak (ör. segment saçılımı, gösterge paneli). Datasaurus, aynı özet istatistiğe sahip verilerin çok farklı görünebileceğini gösterir; bu yüzden analize başlamadan önce görselleştirmek şarttır.

**D3 çözümü:**

```python
fig, ax = plt.subplots(figsize=(9, 4))
ax.plot(donemler, gno, marker="^", linewidth=2, label="GNO")
ax.axhline(2.00, color="red", linestyle="--", label="Başarı sınırı (2.00)")
ax.set_ylim(0, 4)
ax.set_title("Dönemlere Göre Genel Not Ortalaması")
ax.set_xlabel("Dönem")
ax.set_ylabel("GNO")
ax.legend()
plt.show()
```

**D7 çözümü:**

```python
fig, axes = plt.subplots(1, 2, figsize=(12, 4))
sc = axes[0].scatter(metrekare, fiyat, c=oda, cmap="plasma", s=50)
fig.colorbar(sc, ax=axes[0], label="Oda sayısı")
axes[0].set_title("Metrekare ve Fiyat")
axes[0].set_xlabel("Metrekare")
axes[0].set_ylabel("Fiyat (milyon TL)")
axes[1].hist(fiyat, bins=12, edgecolor="white")
axes[1].set_title("Fiyat Dağılımı")
axes[1].set_xlabel("Fiyat (milyon TL)")
axes[1].set_ylabel("Daire sayısı")
plt.tight_layout()
plt.show()
```
