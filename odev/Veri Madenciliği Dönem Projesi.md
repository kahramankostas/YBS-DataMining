# Veri Madenciliği Dönem Projesi

Nov 4, 2026 · @I am kahraman,

## Genel bakış

Bu dönemin projesinde 4–5 kişilik ekipler, gerçek bir veri setiyle bir iş sorusunu baştan sona çözecek. Projeler **20 Aralık 2026, saat 23.59 (TSİ)**’ye kadar teslim edilecek ve **23 Aralık 2026** tarihindeki dersimizde sunulacak. Proje, dönem boyunca gördüğümüz veri madenciliği sürecinin tamamını kapsar: verinin yapısını ve türlerini anlamak, **NumPy** ve **pandas** ile veriyi okumak, temizlemek ve dönüştürmek, görselleştirmeyle keşfetmek, model kurmak ve sonucu doğru ölçmek. Bu süreçte derste kullandığımız araçlardan (NumPy, pandas, matplotlib, scikit-learn vb.) yararlanacaksınız.

Projenin sonunda bir yöneticiye şu soruların cevabını verebilmelisiniz:

- Hangi iş sorusunu çözüyorsunuz ve bu cevap kimin, hangi kararına yarıyor?
- Veride ne gördünüz? (grafiklerle)
- Hangi modeli neden seçtiniz ve ne kadar güvenilir?
- Sonuçlara göre şirket yarın sabah ne yapmalı?

Kod yazmak önemli, ama asıl puan **doğru soruyu sormaya, doğru metriği seçmeye ve sonucu iş diliyle anlatmaya** gidiyor.

## Gruplar: 4 veya 5 kişi

Her grup 4 veya 5 kişiden oluşur; tek başına veya 4 kişiden az bir ekiple çalışılamaz. Kapsam kişi sayısıyla büyür, böylece herkes adil bir yükle değerlendirilir. Tüm grupların sunum süresi aynıdır: 5 dakika sunum + 5 dakika soru-cevap.

| Ekip | Zorunlu kapsam |
| --- | --- |
| 4 kişi | Bir problem türü, baseline + en az 3 model, 5 katlı çapraz doğrulama, `GridSearchCV` ile hiperparametre arama + bir ek modül: K-Means ile segmentasyon **veya** aynı veride ikinci bir problem (ör. sınıflandırma + regresyon) |
| 5 kişi | 4 kişilik kapsam + en az 4 model + **her iki** ek modül (K-Means ile segmentasyon **ve** aynı veride ikinci bir problem) |

- Gruplar, konu bildirimiyle birlikte kesinleşir. Sonradan grup değişikliği yalnızca hoca onayıyla yapılır.
- Gruptan ayrılan öğrenci, hoca onayıyla başka bir gruba katılır; o güne kadarki ortak işi yeni grubuna taşıyamaz.
- Kümeleme ağırlıklı bir konu seçen ekipler de en az bir denetimli model kurar (ör. bulunan segmenti tahmin etmek veya veri setindeki bir hedef).

## Konu ve veri seti

İki yolunuz var: aşağıdaki havuzdan bir konu seçmek ya da kendi konunuzu önermek. Veri setlerini adıyla [Kaggle](https://www.kaggle.com/datasets) veya [UCI Machine Learning Repository](https://archive.ics.uci.edu) üzerinde aratarak bulabilirsiniz.

### Önerilen konu havuzu

| # | İş sorusu | Veri seti (aranacak ad) | Problem türü | Zorluk |
| --- | --- | --- | --- | --- |
| 1 | Hangi çalışan işten ayrılacak? | IBM HR Analytics Employee Attrition (Kaggle) | Sınıflandırma | Kolay |
| 2 | Hangi yolcu memnun değil, neden? | Airline Passenger Satisfaction (Kaggle) | Sınıflandırma | Kolay |
| 3 | Sigorta maliyetini ne belirliyor? | Medical Cost Personal Datasets (Kaggle) | Regresyon | Kolay |
| 4 | Öğrencinin final notu tahmin edilebilir mi? | Student Performance (UCI) | Regresyon / sınıflandırma | Kolay |
| 5 | Kaliforniya’da konut fiyatını ne belirliyor? | California Housing Prices (Kaggle) | Regresyon | Kolay |
| 6 | Telefonla aranan müşteri mevduat açar mı? | Bank Marketing (UCI) | Sınıflandırma | Orta |
| 7 | Hangi otel rezervasyonu iptal edilecek? | Hotel Booking Demand (Kaggle) | Sınıflandırma | Orta |
| 8 | Kredi başvurusu riskli mi? | Statlog (German Credit Data) (UCI) | Sınıflandırma | Orta |
| 9 | Web sitesi ziyaretçisi alışveriş yapacak mı? | Online Shoppers Purchasing Intention (UCI) | Sınıflandırma | Orta |
| 10 | Günlük bisiklet kiralama talebi ne olacak? | Bike Sharing (UCI) | Regresyon | Orta |
| 11 | Kredi kartı müşterileri hangi segmentlere ayrılıyor? | Credit Card Dataset for Clustering (Kaggle) | Kümeleme + denetimli | Orta |
| 12 | Online mağazanın müşterileri RFM’e göre nasıl gruplanıyor? | Online Retail (UCI) | Kümeleme + denetimli | Zor |

### Kendi konunuzu önerirseniz

Serbest konu teşvik edilir; özellikle Türkiye’den veya kendi çevrenizden veri kullanan ekipler bonus alabilir (bkz. Puanlama). Önerilen veri seti şu şartları sağlamalı:

- En az **500 satır** ve en az **5 özellik**; denetimli problemlerde en az 1 kategorik özellik.
- Açık lisanslı veya izinli, kaynağı belirtilebilen gerçek veri. Kişisel veri içeriyorsa anonim olmalı.
- Net bir hedef değişken ve bu hedefin iş anlamı.
- Hoca onayı (proje önerisi aşamasında).

Türkiye’den veri için başlangıç noktaları: [TÜİK veri portalı](https://data.tuik.gov.tr), [İBB Açık Veri Portalı](https://data.ibb.gov.tr). Bu kaynaklardaki veriler çoğu zaman birleştirme ve temizlik ister; ekstra emek puanlamada dikkate alınır.

### Kullanılamayacak veri setleri

- Derste kullanılanlar: churn, konut, mağaza ve kredi temerrüt verileri.
- Çözümü internette çok yaygın olanlar: Iris, Titanic, Boston Housing, MNIST.
- Sentetik olarak üretilmiş veri (sizin ya da bir yapay zekâ aracının ürettiği).

## Projede olması gerekenler

Aşağıdaki liste, puanlamanın kontrol listesidir. Teslimden önce her maddeyi işaretleyin; eksik madde doğrudan puan kaybıdır.

### 1. İş sorusu

- [ ] Problem 1–2 cümleyle tanımlandı: kim, hangi kararı, bu modelle nasıl verecek?
- [ ] Hedef değişken ve problem türü (sınıflandırma / regresyon / kümeleme) yazıldı.

### 2. Veriyi tanıma ve temizleme

- [ ] Veri setinin kaynağı, satır ve sütun sayısı, değişkenlerin anlamı verildi.
- [ ] Veri yapısı incelendi: değişken türleri (sayısal, kategorik, sıralı, tarih) belirlendi, hatalı veri tipleri düzeltildi.
- [ ] Eksik değerler ve aykırı değerler kontrol edildi; ne yapıldığı gerekçesiyle yazıldı.
- [ ] Veri temizleme ve dönüşüm pandas/NumPy ile yapıldı (ör. tekrar eden kayıtlar, yeni özellik türetme, gruplama ve özet tablolar, gerekirse veri birleştirme).
- [ ] Temel tanımlayıcı istatistikler ve değişkenler arası ilişkiler (ör. korelasyon) incelendi.
- [ ] Hedef değişkenin dağılımı gösterildi (sınıflandırmada sınıf dengesi).
- [ ] En az **5 grafik**, en az **4 farklı türde**; tür, soruya uygun seçildi.
- [ ] Her grafikte başlık, eksen etiketleri ve gerekiyorsa açıklama (legend) var.
- [ ] Her grafiğin altında 1–2 cümlelik yorum var: “Bu grafikte ne görüyoruz?”

### 3. Modele hazırlık

- [ ] `train_test_split` ile ayırım yapıldı; sınıflandırmada `stratify` kullanıldı.
- [ ] Ölçekleme ve kategorik kodlama `ColumnTransformer` + `Pipeline` ile yapıldı.
- [ ] Veri sızıntısı yok: hiçbir dönüştürücü test verisiyle fit edilmedi.

### 4. Modelleme

- [ ] Bir referans model kuruldu (`DummyClassifier` veya `DummyRegressor`).
- [ ] Ekip büyüklüğüne göre yeterli sayıda model karşılaştırıldı (bkz. Gruplar).
- [ ] 5 katlı çapraz doğrulama sonuçları ortalama ± standart sapma olarak verildi.
- [ ] `GridSearchCV` ile en az bir modelin hiperparametreleri arandı.

### 5. Değerlendirme

- [ ] Sınıflandırma: karışıklık matrisi, `classification_report`, ROC-AUC.
- [ ] Regresyon: MAE, RMSE, R² ve gerçek–tahmin grafiği.
- [ ] Kümeleme: dirsek ve silhouette ile küme sayısı seçimi, küme profil tablosu.
- [ ] Ana metriğin neden seçildiği iş diliyle açıklandı (sınıflandırmada FP mi, FN mi pahalı?).
- [ ] Eğitim ve test skorları karşılaştırılarak aşırı öğrenme kontrol edildi.

### 6. Ek modül

- [ ] 4 kişilik ekipler: bir ek modül (K-Means segmentasyonu veya ikinci problem) tamamlandı.
- [ ] 5 kişilik ekipler: her iki ek modül tamamlandı.

### 7. Yorum ve öneriler

- [ ] Katsayılar veya özellik önemleri yorumlandı: hangi değişken sonucu nasıl etkiliyor?
- [ ] Somut en az **3 iş önerisi** yazıldı.
- [ ] Çalışmanın sınırlılıkları ve bir sonraki adım belirtildi.

### 8. Tekrarlanabilirlik

- [ ] Tüm rastgele işlemlerde `random_state` sabit.
- [ ] Defter, **Restart & Run All** ile baştan sona hatasız çalışıyor.

## Teslimler ve takvim

Tüm dosyalar en geç Dec 20, 2026 saat **23.59 (TSİ)**’ye kadar yüklenmelidir. Sunumlar Dec 23, 2026 tarihindeki dersimizde yapılacaktır.

### Teslim edilecekler

1. **Jupyter defteri** (`.ipynb`): Tüm analiz, kod ve markdown yorumlar. Dosya adı: `GrupNo_Soyad1_Soyad2_Soyad3_Soyad4(_Soyad5).ipynb`.
2. **Sunum dosyası** (PDF veya PPTX): En fazla 6 slayt. Sunum dosyası da defterle birlikte 20 Aralık’ta teslim edilir.
3. **Veri seti**: Dosyanın kendisi (50 MB’a kadar) veya indirme bağlantısı.
4. **Beyanlar**: Defterin son hücresinde katkı tablosu ve yapay zekâ kullanım beyanı (bkz. ilgili bölümler).


## Sunum

Sunumlar 23 Aralık 2026 tarihindeki dersimizde yapılır. Her grubun toplam **10 dakikası** vardır: **5 dakika sunum + 5 dakika soru-cevap**. Süre aşımında sunum durdurulur.

Sunumu bir şirket yönetim toplantısında yapıyormuş gibi hazırlayın: dinleyici kodu değil, bulguyu ve öneriyi merak ediyor.

### Önerilen akış (~ 6 slayt)

1. **Problem ve veri**: İş sorusu, neden önemli olduğu; kaynak, büyüklük, hedef değişken.
2. **Veriden bulgular**: En anlatıcı 2–3 grafik.
3. **Modeller**: Baseline dahil karşılaştırma tablosu, seçilen model ve gerekçesi.
4. **Değerlendirme**: Ana metrik, karışıklık matrisi veya gerçek–tahmin grafiği, iş yorumu.
5. **Ek modül**: Segmentasyon ve/veya ikinci problemin özeti.
6. **Öneriler ve sınırlılıklar**: Şirket ne yapmalı? En az 3 somut aksiyon ve bir sonraki adım.

### Hazırlık tavsiyeleri

5 dakika çok kısa bir süre; iyi hazırlanmış bir ekip bu sürede çok şey anlatır, hazırlıksız bir ekip ise ilk slaytta kalır. Bu yüzden:

- **Slaytları özenle hazırlayın.** Slayt başına tek bir mesaj, az metin, büyük ve okunur grafikler kullanın. Kod ekran görüntüsü koymayın.
- **En az iki kez süre tutarak prova yapın.** Sunumun 5 dakikayı geçmediğinden emin olun; kimin hangi slaytı anlatacağını ve geçişleri önceden belirleyin.
- **Soru-cevaba hazırlanın.** Ekip olarak birbirinize defterden sorular sorun; herkes her bölümü açıklayabilmeli.
- **Teknik aksaklığa karşı önlem alın.** Sunumun PDF kopyasını USB bellekte ve bulutta hazır bulundurun; ders başlamadan dosyanın açıldığını kontrol edin.

### Kurallar

- Ekipteki herkes sunumda söz alır.
- Soru-cevapta hoca, ekipten **rastgele bir üyeye** defterdeki herhangi bir hücreyi sorabilir. Herkes projenin tamamına hâkim olmalıdır.
- Canlı kod çalıştırmak zorunlu değildir; sonuçlar slaytlarda olmalıdır.

## Puanlama

Her öğrencinin notu iki parçadan oluşur: **%70 proje puanı** (ekip ortak) + **%30 bireysel puan**. Proje, ekip büyüklüğüne göre beklenen kapsama göre değerlendirilir.

### Proje puanı (100)

| Kriter | Puan | Tam puan için |
| --- | --- | --- |
| İş sorusu | 10 | Net, ölçülebilir soru; modelin hangi kararı desteklediği belli |
| Keşifsel analiz ve görselleştirme | 20 | Soruya uygun grafik türleri, eksiksiz etiketler, her grafiğin yorumu |
| Veri hazırlama | 15 | Veri yapısının doğru anlaşılması, temizlik ve dönüşümler, eksik/aykırı değer kararları gerekçeli, doğru bölme, Pipeline, sızıntı yok |
| Modelleme ve model seçimi | 20 | Baseline, kapsamda istenen model sayısı, çapraz doğrulama, GridSearchCV, ek modül(ler) |
| Değerlendirme ve iş yorumu | 20 | Doğru metrik ve gerekçesi, aşırı öğrenme kontrolü, somut iş önerileri |
| Sunum | 10 | 5 dakikaya uyum, net anlatım, iyi hazırlanmış slaytlar ve görseller |
| Kod kalitesi | 5 | Restart & Run All ile hatasız, okunur kod, açıklayıcı markdown |

**Bonus (en fazla +5, toplam 100’ü geçemez):** Türkiye’den veya kendi bulduğunuz özgün bir veri seti; FP/FN maliyetine göre eşik değeri seçimi; veri setlerini birleştirme gibi ek emek.

### Bireysel puan (100)

Bireysel puanın tamamı **soru-cevap performansından** gelir. Hoca, her üyenin projeye hâkimiyetini soru-cevapta ölçer; katkı tablosu da bu değerlendirmede dikkate alınır.

## Yapay zekâ ve akademik dürüstlük

Yapay zekâ araçları (ChatGPT, Claude, Copilot vb.) **yardımcı olarak** kullanılabilir; ama projenin her satırını anlatabilmek sizin sorumluluğunuzdadır.

- **Serbest**: Hata ayıklama, bir fonksiyonun ne yaptığını sorma, kavram açıklatma, metin düzeltme.
- **Yasak**: Projenin tamamını veya analiz ve yorum bölümlerini bir araca yazdırıp olduğu gibi teslim etmek.
- **Beyan zorunlu**: Defterin son hücresinde hangi aracı, hangi iş için kullandığınızı 2–3 cümleyle yazın. Beyan etmek puan kaybettirmez; beyan etmemek kaybettirir.
- **Kural**: Soru-cevapta açıklayamadığınız bir bölüm, sizin yazmadığınız kabul edilir ve o bölümden puan alınmaz.

Ekipler arasında kod veya metin kopyası tespit edilirse ilgili tüm ekiplerin proje puanı sıfırlanır. Veri setinin ve yararlandığınız kaynakların bağlantısını mutlaka verin.

### Katkı tablosu (defterin son hücresi)

| Üye | Yaptığı işler |
| --- | --- |
| Ad Soyad | ör. veri temizleme, 3 grafik ve yorumları, sunumun 2. bölümü |
| Ad Soyad |  |
| Ad Soyad |  |
| Ad Soyad |  |
| Ad Soyad (5 kişilik ekipler) |  |

## Defter şablonu ve SSS

Defterinizi aşağıdaki başlıklarla kurun; puanlayan kişi aradığını aynı yerde bulsun.

```markdown
# Proje Başlığı
Ekip no · Üyeler · Veri seti ve kaynağı

## 1. İş Sorusu
## 2. Veriyi Tanıma ve Temizleme
### 2.1 Veri yapısı, değişken türleri, eksik ve aykırı değerler
### 2.2 Veri temizleme ve dönüşüm (pandas, NumPy)
### 2.3 Görselleştirme ve bulgular
## 3. Veri Hazırlama (bölme, ColumnTransformer, Pipeline)
## 4. Modelleme
### 4.1 Baseline
### 4.2 Model karşılaştırması ve çapraz doğrulama
### 4.3 Hiperparametre arama (GridSearchCV)
## 5. Değerlendirme (seçilen model, test sonuçları, aşırı öğrenme kontrolü)
## 6. Ek Modül(ler) (4 kişi: bir modül · 5 kişi: iki modül)
## 7. Yorum ve İş Önerileri
## 8. Sınırlılıklar ve Sonraki Adım
## 9. Katkı Tablosu ve Yapay Zekâ Beyanı
```

### Sık sorulan sorular

**Derste görmediğimiz bir model kullanabilir miyiz?** Evet (ör. gradient boosting). Ama karşılaştırılan modellerden en az ikisi derste gördüklerimizden olmalı ve kullandığınız her modeli anlatabilmelisiniz.

**Google Colab kullanabilir miyiz?** Evet. Teslimde `.ipynb` dosyasını indirip yükleyin.

**Veri setimiz çok büyük, ne yapalım?** Gerekçesini yazarak rastgele örneklem alabilirsiniz (ör. 20.000 satır).

**Modelimizin skoru düşük çıktı, puan kaybeder miyiz?** Hayır. Düşük skoru dürüstçe raporlayıp nedenini tartışmak, şişirilmiş bir sonuçtan daha değerlidir. Test skoru şüpheli derecede yüksekse (ör. 1,00) veri sızıntısı olup olmadığını kontrol edin.

**5 dakikada tüm projeyi nasıl anlatacağız?** Anlatamazsınız, anlatmanız da beklenmiyor. En önemli bulguya ve önerilere odaklanın; ayrıntılar defterde ve soru-cevapta.

**Ekip arkadaşım çalışmıyor, ne yapalım?** Ara kontrol haftasına kadar hocaya bildirin; hoca ekiple görüşür. Katkı tablosu ve soru-cevap performansı bireysel puana yansır.


