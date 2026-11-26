# YBS 301 – Veri Madenciliği
## Çalışma Notları · 1. Hafta: Temel Kavramlar

> *"Hard in training, easy in battle"* – Alexander Suvorov
> *"Bilgisayar bilimi bilgisayarlarla ne kadar ilgiliyse, astronomi de teleskoplarla o kadar ilgilidir."* – Edsger W. Dijkstra

Bu notlar, ders kitabının 1. ünitesi (Temel Kavramlar) ile ders sunumundaki örnekler birleştirilerek hazırlanmıştır.

---

## İçindekiler

1. [Neden Veri Madenciliği?](#1-neden-veri-madenciliği)
2. [Algoritma Kavramı](#2-algoritma-kavramı)
3. [Tarihsel Gelişim](#3-tarihsel-gelişim)
4. [Veri Madenciliğine Etki Eden Disiplinler](#4-veri-madenciliğine-etki-eden-disiplinler)
5. [Veri → Enformasyon → Bilgi → Bilgelik (DIKW)](#5-veri--enformasyon--bilgi--bilgelik-dikw)
6. [Veri Madenciliği Kavramı ve Veri Ambarı](#6-veri-madenciliği-kavramı-ve-veri-ambarı)
7. [Veritabanlarında Bilgi Keşfi (KDD) Süreci](#7-veritabanlarında-bilgi-keşfi-kdd-süreci)
8. [Veri Ön İşleme](#8-veri-ön-işleme)
9. [Veri Madenciliği Modelleri](#9-veri-madenciliği-modelleri)
10. [Diğer Analiz Yaklaşımlarıyla Karşılaştırma](#10-diğer-analiz-yaklaşımlarıyla-karşılaştırma)
11. [Uygulama Alanları](#11-uygulama-alanları)
12. [Veriyle Düşünürken Tuzaklar: Yanlılıklar ve Safsatalar](#12-veriyle-düşünürken-tuzaklar-yanlılıklar-ve-safsatalar)
13. [Uygulama: Veri Setini Tanı](#13-uygulama-veri-setini-tanı)
14. [Kendini Sına](#14-kendini-sına)

---

## 1. Neden Veri Madenciliği?

- İletişim ve bilişim teknolojileri her şeyi hızla değiştiriyor: ekonomik koşullar, müşteri beklentileri, rakip stratejileri…
- Bu değişime ayak uydurmak için yöneticilerin **zamanında elde edilmiş doğru bilgiyle** karar vermesi gerekir.
- Bugün çok büyük miktarda veriyi toplamak ve saklamak kolay; **ama o veriden anlamlı bilgi çıkarmak kolay değil.**
- Geleneksel analiz yöntemleri veri hacmindeki büyük artış karşısında yetersiz kalmıştır → **veri madenciliği bu ihtiyaçtan doğmuştur.**

> 💡 **Kilit fikir:** Veri madenciliği çözümün kendisi değil; doğru kararı vermeye destek olacak bilgiyi ortaya çıkaran bir **araçtır**.

---

## 2. Algoritma Kavramı

- "Algoritma" kelimesi, Harezm bölgesinden matematikçi **Harezmi (Al-Khwarizmi)** adından gelir.
- **Tanım:** Algoritma, belirli bir problemi çözmek veya belirli bir amaca ulaşmak için çözüm yolunun **adım adım** tasarlanmasıdır.
- Problemler ikiye ayrılabilir:
  - **Algoritmik problemler:** Adımları net tanımlanabilen problemler (sıralama, en kısa yol vb.).
  - **Algoritmik olmayan problemler:** Kesin adımlarla tarif edilemeyen problemler (bir yüzü tanımak, bir kediyi "kedi" olarak ayırt etmek, iyi bir hamleyi sezmek vb.). Makine öğrenimi ve veri madenciliği tam da bu alanda devreye girer.

**Oyunlar üzerinden kilometre taşları:**

| Tarih | Olay | Neden önemli? |
|---|---|---|
| 11 Mayıs 1997 | IBM **Deep Blue**, satranç dünya şampiyonu Garry Kasparov'u yendi | Büyük ölçüde kaba kuvvet arama + uzman bilgisi |
| 15 Mart 2016 | Google **AlphaGo**, Lee Sedol'u 4-1 yendi | Go'da olası hamle sayısı çok fazla; sistem veriden öğrenerek oynadı |

---

## 3. Tarihsel Gelişim

| Dönem | Gelişme |
|---|---|
| **1950'ler** | İlk bilgisayarlar: sayım ve karmaşık hesaplamalar. 1957'de Frank Rosenblatt **perseptronu** geliştirdi (yapay nöronun ilk modeli). |
| **1960'lar** | Veri depolama ihtiyacı → **veritabanı** kavramı. Dönem sonunda basit öğrenmeli bilgisayarlar. 1969'da Minsky ve Papert, perseptronun basit mantıksal işlemlerde yetersiz kaldığını gösterdi. İlk veri modelleri: **Hiyerarşik** ve **Ağ** veri modelleri. |
| **1970'ler** | **İlişkisel Veritabanı Yönetim Sistemleri**; kurala dayalı uzman sistemler, basit makine öğrenimi. |
| **1980'ler** | VTYS'ler yaygınlaştı; işletmeler müşteri, rakip ve ürün verilerini düzenli saklamaya başladı. |
| **1989** | **KDD (IJCAI-89) Veritabanlarında Bilgi Keşfi Çalışma Grubu** toplantısı. |
| **1991** | Toplantının sonuç makalesi yayımlandı → temel tanım ve kavramlar ortaya kondu. |
| **1992** | Veri madenciliği için ilk yazılım geliştirildi. |
| **2000'ler** | Hemen hemen tüm alanlara yayıldı; CRM ve ERP sistemleriyle iş dünyasında yaygınlaştı. |

> 📝 İlk zamanlarda bu işe "veri taraması", "veri yakalama" gibi adlar verildi. "Veri madenciliği" adı 1990'larda bilgisayar mühendisleri tarafından kullanılmaya başlandı.

---

## 4. Veri Madenciliğine Etki Eden Disiplinler

Veri madenciliği tek bir alan değil, birçok disiplinin kesişimidir: **İstatistik, Makine Öğrenimi, Veritabanı Sistemleri, Görselleştirme, Örüntü Tanıma** (ve yapay zekâ, nöro-hesaplama gibi diğerleri).

| Disiplin | Kısaca |
|---|---|
| **İstatistik** | Veri analizinin klasik disiplini. Bilgisayar gücüyle birlikte eskiden yapılamayan analizler mümkün hâle geldi. |
| **Makine Öğrenimi** | Bilgisayarların örneklerden çıkarım yaparak öğrenmesi. Yapay zekânın temelidir. |
| **Görselleştirme** | Verinin tablo/grafik gibi görsellerle sunulması. Boyut sayısı arttıkça 2B/3B grafikler yetmedi, yeni araçlar geliştirildi. |
| **Veritabanı Sistemleri** | Veritabanı + VTYS. Veri madenciliğinin "olmazsa olmazı". |
| **Örüntü Tanıma** | Önceden tanımlı bir örüntünün (parmak izi, ses, yüz, el yazısı…) benzerlerini veride arayıp bulma. |

### 🐱 Makine öğrenimini bir çocuk gibi düşünün

İlk kez kedi gören bir çocuğa "bu bir kedi" denir. Başka bir gün farklı renkte, daha küçük bir kedi gördüğünde önceki deneyimi hatırlar ve onu da kedi olarak tanır. Örnek gördükçe "kedi" kavramı netleşir ve çocuk **ortak özelliklere** bakarak sınıflandırma yapmayı öğrenir.

Makine öğrenimi de aynısını yapar: Büyük veri kümelerinden örnekler alır, ortak özellikleri çıkarır ve yeni gelen veriyi sınıflandırır.

### İstatistik mi, makine öğrenimi mi?

Sunumdaki "#10yearchallenge" şakası: 2009'da "İstatistik" diye anılan `y = βX + ε` denklemi, 2019'da "Makine Öğrenimi" diye anılıyor. Mesaj: **Yöntemlerin çoğunun kökü istatistiktir; isim değişse de temel aynıdır.**

---

## 5. Veri → Enformasyon → Bilgi → Bilgelik (DIKW)

R. Ackoff'un (1989) **DIKW piramidi**, ham veriden karara giden yolu dört katmanda gösterir.

| Katman | Cevapladığı soru | Tanım | Süreç |
|---|---|---|---|
| **Veri** | Hiçbir şey | Tek başına anlam taşımayan ham gözlemler, sayılar, semboller | Parçaları toplama |
| **Malumat / Enformasyon** | Ne? | Bağlam içinde ilişkilendirilmiş, düzenlenmiş veri | Parçaları bağlama |
| **Bilgi** | Nasıl? Neden? | Kavrayış sağlayan, neden-sonuç ilişkisi kurulmuş bilgi | Bütünün oluşması |
| **Bilgelik** | Neden yapmalı? En iyisi ne? | Birikmiş bilgiyi doğru karar için kullanmak (geleceğe dönük) | Bütünleri birleştirme |

> Alt üç katman **geçmişi** anlamaya, en üst katman **geleceğe** yönelik karara hizmet eder.

### ✈️ Örnek: Abraham Wald ve bombardıman uçakları (II. Dünya Savaşı)

| Katman | Wald örneğindeki karşılığı |
|---|---|
| **Veri** | Görevden dönen uçaklardaki delik sayıları ve konumları ("kanatta 120, gövdede 95, motorda 3 delik"). |
| **Enformasyon** | Deliklerin kanat ve gövdede yoğunlaştığı, motor ve kokpitte neredeyse hiç olmadığı haritası. |
| **Bilgi** | İsabetler rastgele dağılır. Motor/kokpitten vurulan uçaklar **geri dönemediği** için örneklemde yoktur. Yani boş görünen yerler aslında **ölümcül** noktalardır. |
| **Bilgelik** | Zırh sınırlı (ağırlık uçağı yavaşlatır) → zırhı delik olan yerlere değil, **deliksiz görünen hayati bölgelere** ekle. |

> ⚠️ Bu örnek aynı zamanda **Hayatta Kalma Yanılgısı (Survivorship Bias)**'nın klasik örneğidir: Yalnızca "hayatta kalanlara" bakarak karar vermek bizi yanıltır.

---

## 6. Veri Madenciliği Kavramı ve Veri Ambarı

### Tanımlar (kitaptan özet)

- Büyük veri yığınlarında, geleceği tahmin etmeye yardımcı olacak **anlamlı ve yararlı ilişki ve kuralların** bilgisayar yazılımlarıyla aranmasıdır.
- Veriler arasındaki **örüntü (desen) ve ilişkileri** keşfedip bunları doğru tahminler için kullanan bir **süreçtir**.
- İstatistiksel/matematiksel teknikler ve örüntü tanımayla, veri yığınlarında yeni **korelasyon, örüntü ve eğilimlerin** keşfedilmesidir.

> 🔑 **En önemli vurgu:** Veri madenciliğiyle elde edilen bilgi **daha önce bilinmeyen, tahmin bile edilemeyen** bilgidir. Veri madenciliği, zaten bilinen bir sonucu doğrulamak için kullanılan bir araç değildir.

**Madencilik benzetmesi:** Altın, bor, kömür gibi madenler çıkarılıp işlenmedikçe değer taşımaz. Veritabanlarındaki veri de işlenmeyi bekleyen ham maddedir.

**Diğer adları:** bilgi çıkarımı, enformasyon keşfi, enformasyon hasadı, veri arkeolojisi, veri örüntü işleme.

> ⚠️ **Sık yapılan hata:** Veri madenciliği ≠ Veritabanlarında Bilgi Keşfi (KDD). Veri madenciliği, KDD sürecinin **yalnızca bir adımıdır**.

### Veri Ambarı ve ilgili kavramlar

İşlemsel (günlük kayıtların tutulduğu) veritabanları veri madenciliğinde **doğrudan kullanılmaz**; önce hazırlanmaları gerekir.

```
İç veri kaynakları ─┐
                    ├─► [Çek → Temizle → Dönüştür] ─► VERİ AMBARI ─► [Erişim, Sorgulama, Analiz] ─► OLAP / Veri Madenciliği
Dış veri kaynakları ┘                                     │
                                                          └─► Veri Depoları (Data Mart)
```

| Kavram | Açıklama |
|---|---|
| **İç veri kaynakları** | İşletmenin kendi süreçlerinden gelen veri (üretim, satın alma, pazarlama kayıtları). |
| **Dış veri kaynakları** | Sektör verileri, istatistik kurumu raporları, yasal düzenlemeler, döviz kurları vb. |
| **Veri ambarı (Data Warehouse)** | İç ve dış kaynakların birleştirilip düzenlendiği, konu odaklı, veri madenciliğine hazır geniş veritabanı. **Tüm işletmeyi** ilgilendirir. |
| **Üst veri (Metadata)** | Ambardaki veriler hakkındaki tanımlamalar; ambarın "veri kataloğu". |
| **Veri deposu (Data Mart)** | Veri ambarının alt kümesi; **tek bir bölüm veya konuya** yöneliktir. |
| **OLAP** | Çevrimiçi Analitik İşleme. Ambardaki veri üzerinde **çok boyutlu** analiz ve sorgulama. |

### Sorgulama düzeyleri: SQL → OLAP → Veri Madenciliği

Kablo üreten bir işletme örneği:

| Düzey | Örnek soru | Araç |
|---|---|---|
| 1. Basit sorgu | "Geçen ay toplam ne kadar halojensiz tesisat kablosu sattık?" | İşlemsel veritabanı / SQL |
| 2. Çok boyutlu sorgu | "Ağustos'ta İç Anadolu'da ne kadar sattık? Geçen ayla, geçen yılın Ağustos'uyla ve tahminle karşılaştırması nedir?" | OLAP (veri küpü: ürün × bölge × zaman × satış) |
| 3. Gizli örüntü | Daha önce akla gelmemiş, tahmin edilemeyen ilişkiler | Veri madenciliği |

> İlk iki düzey **bilinen veya tahmin edilebilir** sonuçlar verir; veri madenciliği **bilinmeyeni** arar.

---

## 7. Veritabanlarında Bilgi Keşfi (KDD) Süreci

**KDD:** Veriden faydalı bilginin keşfedilmesi sürecinin **tamamı**. Terim ilk kez 1989'daki çalışma toplantısında ortaya atıldı.

Han ve Kamber'in gösterimi:

```
Veritabanları / Düz dosyalar
   → Veri Temizleme ve Bütünleştirme
   → Veri Seçimi ve Dönüştürme
   → Veri Madenciliği
   → Örüntüler
   → Değerlendirme ve Sunum
   → BİLGİ
```

### Beş aşama

| # | Aşama | Konum | Öz |
|---|---|---|---|
| 1 | **Amacın Tanımlanması** | VM öncesi | Amaç bir probleme odaklı ve açık olmalı. Başarının nasıl ölçüleceği, yanlış tahminin maliyeti ve doğru tahminin kazancı tanımlanmalı. |
| 2 | **Veriler Üzerinde Ön İşlemler** | VM öncesi | Verinin analize hazırlanması. **Sürecin en çok zaman alan aşaması.** |
| 3 | **Modelin Kurulması ve Değerlendirilmesi** | **Veri madenciliğinin kendisi** | Birçok model denenir; en iyiye ulaşana kadar hazırlık ve kurma aşamaları tekrarlanır. Geçerlilik sınanır. |
| 4 | **Modelin Kullanılması ve Yorumlanması** | VM sonrası | Sonuçlar başlangıçtaki amaca ulaştı mı? Ulaşmadıysa süreç yenilenir. |
| 5 | **Modelin İzlenmesi** | VM sonrası | Koşullar zamanla değişir; model sürekli izlenir, gerekirse güncellenir. |

> 💡 "Çöp girer, çöp çıkar": Sonuçların kalitesi verinin kalitesine bağlıdır. Ön işleme özensiz yapılırsa model aşamasından tekrar tekrar geri dönmek gerekir.

---

## 8. Veri Ön İşleme

```
Veri Ön İşleme (Verilerin Hazırlanması)
├── 1. Verilerin Toplanması ve Birleştirilmesi
├── 2. Verilerin Temizlenmesi
│     ├── Kayıp veriler için işlem
│     └── Gürültünün temizlenmesi
└── 3. Verilerin Yeniden Yapılandırılması
      ├── Normalizasyon
      ├── Veri azaltma (indirgeme)
      └── Veri dönüştürme
```

### 8.1 Toplama ve birleştirme

Amaca uygun verinin hangi kaynaklarda olduğu belirlenir; önce iç kaynaklar, sonra kamu veritabanları veya veri satan kuruluşlar gibi dış kaynaklar kullanılır. **Verinin hangi koşullarda ve hangi yöntemle toplandığı önemlidir.**

### 8.2 Temizleme

**Temel kavramlar:**

- **Kayıp veri:** Kayıtlarda eksik olan değerler (doğum tarihi girilmemiş çalışan, gelirini belirtmeyen müşteri).
- **Aykırı değer:** Doğru olamayacak kadar uç değer (doğum yılı 1974 yerine 1074).
- **Gürültülü veri:** Aykırı ya da yanlış girilmiş değerlerin genel adı.
- **Uyumsuzluk:** Farklı kaynaklardan gelen verinin farklı birim, zaman veya kodlamada olması (bir sistemde cinsiyet E/K, diğerinde 0/1).

#### Kayıp verilerle başa çıkma

| Yaklaşım | Ne zaman uygun? | Dikkat |
|---|---|---|
| a. Kaydı silmek | Kayıp veri oranı çok küçükse | Oran yüksekse sonuçları bozar |
| b. Tek tek elle doldurmak | Veri küçük, eksik değere ulaşmak mümkün, zaman var | Aksi hâlde zaman kaybı |
| c. Hepsine aynı sabit değeri yazmak (ör. "Y", "E", 9) | Hızlı çözüm | Algoritmayı yanıltabilir; seçilen kod başka anlamlı bir değerle çakışmamalı. Bazen gizli bir örüntü de ortaya çıkarabilir. |
| d. Ortalama ile doldurmak | Sayısal değişkenlerde | Genel ortalama yerine **sınıf ortalaması** daha uygundur |
| e. Diğer değişkenlerle tahmin etmek | Daha doğru doldurma istenirse | Regresyon, zaman serisi, Bayes, karar ağaçları, beklenti maksimizasyonu |

**Örnek (kira verisi):** 6 numaralı, Alanönü mahallesinde oturan 9 yıllık çalışanın kirası eksik.

- Genel ortalama: (850 + 675 + 780 + 950 + 1250) / 5 = **901**
- Sınıf ortalaması (yalnızca Alanönü'ndeki iki çalışan): **865**
- Hangisinin kullanılacağına karar verici karar verir.

#### Gürültüyü temizleme

Örnek veri: `24, 18, 7, 27, 31, 24, 11, 37, 28`
Sıralı: `7, 11, 18, 24, 24, 27, 28, 31, 37` → üç eşit bölüme ayrılır.

| Bölüm | Orijinal | **Ortalama ile** düzeltme | **Sınır değerleri ile** düzeltme |
|---|---|---|---|
| 1 | 7, 11, 18 | 12, 12, 12 | 7, 7, 18 |
| 2 | 24, 24, 27 | 25, 25, 25 | 24, 24, 27 |
| 3 | 28, 31, 37 | 32, 32, 32 | 28, 28, 37 |

- **Bölümleme (ortalama/medyan):** Her bölümdeki değerler bölüm ortalaması veya medyanıyla değiştirilir.
- **Sınır değerleri:** Her değer, bölümün en küçük veya en büyük değerinden hangisine yakınsa onunla değiştirilir (11, 7'ye 4 uzaklıkta, 18'e 7 uzaklıkta → 7 olur).
- Kitapta ayrıca (maks − min) / eleman sayısı değerinin bölüme atandığı bir varyant da verilmektedir (Bölüm 1: (18−7)/3 = 3,67).
- **Kümeleme:** Veri benzerliğe göre kümelenir; hiçbir kümeye girmeyen noktalar aykırı değerdir ve en yakın kümenin ortalama/sınır değeriyle değiştirilir.
- **Regresyon:** Değişkenler arasındaki ilişki bir fonksiyonla modellenir; bir değişken diğerini tahmin etmekte kullanılır (doğrusal / çoklu doğrusal regresyon).

### 8.3 Yeniden yapılandırma

Bazı algoritmalar yalnızca sayısal, bazıları yalnızca kategorik, bazıları yalnızca 0/1 verilerle çalışır. Bu yüzden veri algoritmaya uygun hâle getirilir.

| İşlem | Açıklama | Yöntemler / Örnek |
|---|---|---|
| **Normalizasyon** | Değerleri 0–1 gibi ortak bir aralığa getirmek | Min-maks, sıfır-ortalama (z-skor), ondalıklı normalizasyon |
| **Veri azaltma** | Temel özellikleri kaybetmeden veri miktarını azaltmak, değişkenleri birleştirmek | Boyut azaltma, veri sıkıştırma, temel bileşenler analizi (PCA), faktör analizi |
| **Veri dönüştürme** | Veriyi algoritmanın kullanabileceği biçime getirmek | Sürekli maaşları (1.500–5.000 TL) "düşük / orta / yüksek" kategorilerine çevirmek (kesikleştirme) |

---

## 9. Veri Madenciliği Modelleri

### Ortak özellik: Öğrenme

1. Yazılım örnek veriyi inceler, kurallar çıkarır → **öğrenme**
2. Kuralları verinin kalan kısmına uygulayıp kendini sınar → **test**
3. Gerekirse kuralları yeniler → **doğrulama**
4. **Aşırı öğrenme (overfitting)** kontrol edilir: Kurallar yalnızca eğitim verisinde işe yarıyor, yeni veride çöküyorsa model ezber yapmıştır.

### Denetimli ve denetimsiz öğrenme

| | Denetimli (Supervised) | Denetimsiz (Unsupervised) |
|---|---|---|
| Etiket / sınıf bilgisi | **Var** (ör. her kaydın yanında "kadın/erkek" yazıyor) | **Yok** |
| Amaç | Yeni gözlemin etiketini tahmin etmek | Benzerliklere göre doğal grupları bulmak |
| Veri kullanımı | Eğitim kümesi + test kümesi | Tüm veri |
| Örnek | Sınıflandırma, regresyon | Kümeleme |

### Model sınıflandırması

```
Veri Madenciliği Modelleri
├── TAHMİN EDİCİ (Predictive)
│   ├── Regresyon
│   ├── Sınıflandırma
│   └── (Zaman serisi analizi)
│       Algoritmalar: Karar ağaçları, Yapay sinir ağları, Genetik algoritmalar,
│       k-en yakın komşu, Bayes sınıflandırması, Destek vektör makineleri,
│       Hatayı geri yayma
└── TANIMLAYICI (Descriptive)
    ├── Kümeleme
    ├── Birliktelik kuralları
    ├── Sıra örüntü analizi
    ├── Özetleme
    └── (İstisna/aykırı değer analizi, tanımlayıcı istatistik)
```

### 9.1 Tahmin edici modeller

**Bilinenden yola çıkıp bilinmeyeni tahmin etmek.** Örnekler: Bankanın, müşterinin geçmiş kredi verisine bakarak yeni krediyi geri ödeyip ödemeyeceğini tahmin etmesi; hastanenin geçmiş vakalardan yeni hastanın teşhisini tahmin etmesi.

- **Regresyon:** Bağımlı ve bağımsız değişkenler arasındaki ilişkiyi en iyi tanımlayan fonksiyonu bulur (sürekli çıktı).
- **Sınıflandırma:** Verileri önceden belirlenmiş sınıflara atar (kategorik çıktı). Denetimli öğrenmedir.

| Algoritma | Ana fikir | Artı / Eksi |
|---|---|---|
| **Karar ağaçları** | Kök düğümden başlayıp her düğümde bir özelliği test ederek dallara ayrılır; yapraklar sınıfları verir | En yaygın; anlaşılması ve kurulması kolay |
| **Yapay sinir ağları** | Biyolojik sinir sistemini taklit eder | Karmaşık, doğrusal olmayan ilişkileri modeller; **yorumlanması zor** |
| **Genetik algoritmalar** | Evrimi taklit eder: nüfus, kromozom, uygunluk fonksiyonu | Doğrudan bir VM modeli değil, **eniyileme** yöntemidir |
| **Zaman serisi analizi** | Zamana bağlı verinin gelecek değerini tahmin eder | En yaygın alan borsa; denetimlidir |
| **k-en yakın komşu (k-NN)** | Yeni noktayı, kendisine en yakın k komşunun sınıfına atar (Öklid uzaklığı) | k çok büyük → farklı noktalar karışır; k çok küçük → benzer noktalar ayrı sınıflara düşer |
| **Bayes sınıflandırması** | Bayes kuralıyla yeni verinin her sınıfa girme olasılığını hesaplar | Olasılık temelli, hızlı |

### 9.2 Tanımlayıcı modeller

**Verideki örüntü ve ilişkileri tanımlar**; kayıtlar arasında bağlantı kurar.

| Model | Ne yapar? | Örnek |
|---|---|---|
| **Kümeleme** | Veriyi benzerliğe göre gruplara ayırır; hedef değişken yoktur (**denetimsiz**). Kümelerin anlamını alan uzmanı yorumlar. | Poliçesini yenilemeyen müşterilerin ortak özelliklerini bulmak |
| **Birliktelik kuralları** | Birlikte görülen öğeleri bulur (pazar sepeti analizi) | "Bira alanların %80'i cips de alıyor" → raf düzeni, çapraz satış |
| **Sıra örüntü analizi** | Birliktelik + **zaman sırası** | "Çekiç alan müşteri ilk üç ayda %15 olasılıkla çivi alır" |
| **Özetleme** | Veriyi alt gruplara yerleştirip ortalama, standart sapma gibi betimleyici göstergeler üretir (karakterizasyon / genelleştirme) | Müşteri segmentlerinin profili |

> 🔑 **Kümeleme vs. Sınıflandırma:** Sınıflar önceden biliniyorsa sınıflandırma (denetimli), bilinmiyorsa kümeleme (denetimsiz).

---

## 10. Diğer Analiz Yaklaşımlarıyla Karşılaştırma

### Geleneksel istatistik vs. veri madenciliği

| Geleneksel İstatistik | Veri Madenciliği |
|---|---|
| Bir **hipotez** kurarak başlar | Hipoteze ihtiyaç duymaz |
| İstatistikçi eşitlikleri **kendisi** geliştirir | Algoritmalar eşitlikleri **otomatik** geliştirir |
| Çoğunlukla **sayısal** veri | Sayısala ek olarak **metin, ses** vb. |
| Kirli veri analiz sırasında bulunup filtrelenir | **Temizlenmiş** veri üzerinde çalışır |
| Sonuçlar görece kolay yorumlanır | Yorumlamak zordur, **uzman** gerekir |

### Kullanım amacına göre

| Araç | Ne zaman? |
|---|---|
| **Veri sorgusu / SQL** | Ne aradığınızı tam biliyorsanız |
| **OLAP** | Çok boyutlu, basit ilişkileri incelemek istiyorsanız |
| **Veri madenciliği** | Açıkça gözlenemeyen örüntü ve ilişkileri keşfetmek istiyorsanız |

### Keşfedilen bilgi tipine göre

| Bilgi tipi | Açıklama | Araç |
|---|---|---|
| **Sığ bilgi** | Veritabanından doğrudan sorgulanabilen bilgi | SQL |
| **Çok boyutlu bilgi** | Veri küpü üzerinden analiz edilebilen bilgi | OLAP |
| **Gizli bilgi** | Kolayca görülemeyen örüntü ve ilişkiler | Veri madenciliği |
| **Derin bilgi** | Bulunması için ipucu gerektiren, en zor erişilen bilgi | Veri madenciliğinin araştırma sınırları |

---

## 11. Uygulama Alanları

Büyük veri üretilen ve karar gereken her alanda kullanılabilir: **pazarlama, finans (bankacılık, sigorta, borsa), perakende, sağlık, telekomünikasyon, endüstri ve mühendislik, eğitim, tıp, biyoloji, genetik, kamu, istihbarat ve güvenlik.**

| Alan | Örnek uygulamalar |
|---|---|
| **Pazarlama** (en yoğun alan) | Müşteri segmentasyonu, pazar sepeti analizi, kampanya hedefleme, müşteri kaybı (churn) tahmini |
| **Finans** | Kredi riski değerlendirme, kredi kartı dolandırıcılığı tespiti, borsa tahmini |
| **Sağlık** | Hastalık teşhisi ve risk tahmini, tedavi etkinliğinin analizi |
| **Endüstri / Mühendislik** | Arıza tahmini, kalite kontrol, üretim süreci optimizasyonu |
| **Eğitim** | Öğrenci başarısını etkileyen faktörler, okulu bırakma riskinin tahmini |

### 🗺️ Tarihî örnek: John Snow ve kolera (Londra, 1854)

Dr. John Snow, kolera ölümlerini Soho haritası üzerinde işaretledi ve vakaların **Broad Street'teki su pompası** çevresinde yoğunlaştığını gördü. Pompanın kolu çıkarıldı, salgın yavaşladı. Bu çalışma, veri görselleştirme ve mekânsal analizin karar almaya dönüşmesinin en bilinen erken örneklerindendir.

---

## 12. Veriyle Düşünürken Tuzaklar: Yanlılıklar ve Safsatalar

> **Korelasyon nedensellik değildir!** İki değişkenin birlikte hareket etmesi, birinin diğerine neden olduğunu göstermez.

### Sunumdaki sahte korelasyon örnekleri

| Örnek | Gerçek açıklama |
|---|---|
| Dondurma satışları ↔ köpekbalığı saldırıları | Ortak neden (karıştırıcı değişken): **yaz / sıcak hava** |
| Organik gıda satışları ↔ otizm teşhisleri (r = 0,997) | İkisi de zamanla artıyor; teşhis kriterleri ve farkındalık değişti. Ortak trend ≠ neden |
| Kişi başı çikolata tüketimi ↔ Nobel ödülü sayısı (r = 0,79) | Ülkenin refah düzeyi, eğitim ve araştırma yatırımı |
| 2016 Brexit "ayrıl" bölgeleri ↔ 1992 deli dana (BSE) bölgeleri | Haritalar benzer görünse de bölgesel benzerlik nedensellik göstermez (ekolojik düzeyde çıkarım tehlikesi) |
| Çatıdaki leylek yuvası ↔ çocuk sayısı | Büyük evlerde hem daha çok çocuk hem daha çok yuva yeri var |

### 🦖 Datasaurus: "Önce görselleştir!"


![](https://damassets.autodesk.net/content/dam/autodesk/research/publications-assets/gifs/same-stats-different-graphs/DinoSequentialSmaller.gif" )

Farklı şekillerdeki (dinozor dahil) veri setleri **aynı ortalama, standart sapma ve korelasyon** değerlerine sahip olabilir. Yalnızca özet istatistiklere bakmak yanıltıcıdır; veriyi mutlaka **grafikle** inceleyin. (Anscombe dörtlüsü de aynı dersi verir.)

### Yanlılık ve safsata listesi

**1. Örneklem ve seçim yanlılıkları**

| Terim | Kısaca |
|---|---|
| **Hayatta kalma yanılgısı** | Yalnızca "başaranlara/hayatta kalanlara" bakmak (Wald'ın uçakları) |
| **Cımbızlama (Cherry Picking)** | İşine gelen verileri seçip diğerlerini yok saymak |
| **Gönüllü katılım yanlılığı** | Ankete yalnızca güçlü fikri olanların katılması; örneklem temsilî olmaz |

**2. İstatistiksel ve metodolojik çarpıtmalar**

| Terim | Kısaca |
|---|---|
| **Teksas keskin nişancısı** | Önce ateş edip sonra hedefi kurşunların etrafına çizmek; rastgele kümelenmeye sonradan anlam yüklemek |
| **Simpson paradoksu** | Alt gruplarda görülen eğilimin, gruplar birleşince tersine dönmesi |
| **Sahte hassasiyet** | Kaba bir tahmini "%37,284" gibi aşırı kesin göstermek |
| **Ortalamanın aldatıcılığı** | Ortalamaya göre plan yapmak; "ortalama kişi" çoğu zaman yoktur |
| **Göreceli vs. mutlak risk** | "Riski %50 artırıyor" (1/10.000'den 1,5/10.000'e) gibi algıyı abartmak |

**3. Mantıksal ve çıkarımsal safsatalar**

| Terim | Kısaca |
|---|---|
| **Cum hoc ergo propter hoc** | Birlikte olduğu için biri diğerinin nedenidir sanmak |
| **Post hoc ergo propter hoc** | Ondan sonra olduğu için onun yüzünden olduğunu sanmak |
| **Ekolojik safsata** | Grup düzeyindeki bulguyu tek tek bireylere genellemek |
| **Kumarbaz safsatası** | "Beş kez yazı geldi, şimdi tura gelir" sanmak; bağımsız olaylar birbirini etkilemez |
| **Ortalamaya dönüşü görmezden gelme** | Aşırı uç bir sonucun ardından gelen "normale dönüşü" bir müdahalenin etkisi sanmak |

---

## 13. Uygulama: Veri Setini Tanı

Derste kullanılacak klasik veri setleri: **Iris, Wine, Breast Cancer, California Housing, Titanic, MNIST, 20 Newsgroups**

Bir veri setiyle karşılaştığınızda şu sorulara cevap verin:

1. Veri setinde kaç gözlem (satır) var?
2. Kaç özellik (sütun) var?
3. Özelliklerin isimleri neler?
4. Hangi özellikler sayısal?
5. Kategorik özellik var mı?
6. Eksik veri var mı?
7. Hedef değişken nedir?
8. Hedef değişken kaç farklı değer alıyor?
9. Sınıflar dengeli mi?
10. Özelliklerin değer aralıkları birbirine benziyor mu? (→ normalizasyon gerekir mi?)
11. En yüksek korelasyona sahip iki özellik hangileri?
12. Veriye baktığınızda dikkatinizi çeken bir şey nedir?

**Son soru:** *"Bu veri setinden hangi sorulara cevap vermeye çalışabiliriz?"*

<details>
<summary>💻 Python ile başlangıç kodu (Iris örneği)</summary>

```python
import pandas as pd
from sklearn.datasets import load_iris

iris = load_iris(as_frame=True)
df = iris.frame

print(df.shape)                    # 1-2: gözlem ve özellik sayısı
print(df.columns.tolist())         # 3: özellik isimleri
print(df.dtypes)                   # 4-5: veri tipleri
print(df.isnull().sum())           # 6: eksik veri
print(df["target"].value_counts()) # 7-9: hedef ve sınıf dengesi
print(df.describe())               # 10: değer aralıkları
print(df.corr())                   # 11: korelasyonlar
```

</details>

---

## 14. Kendini Sına

<details>
<summary><b>1. Veri madenciliği ile KDD aynı şey midir?</b></summary>

Hayır. KDD, veriden bilgi keşfi sürecinin tamamıdır; veri madenciliği bu sürecin "modelin kurulması ve değerlendirilmesi" adımına karşılık gelir.
</details>

<details>
<summary><b>2. Veri madenciliğinde üzerinde analiz yapılan veritabanı nasıl adlandırılır?</b></summary>

**Veri ambarı.** İç ve dış veri kaynaklarının birleştirilip temizlenmesiyle oluşturulan, konu odaklı, veri madenciliğinde doğrudan kullanılabilen geniş veritabanıdır. Alt kümelerine veri deposu (data mart), ambar hakkındaki tanımlamalara üst veri (metadata) denir.
</details>

<details>
<summary><b>3. KDD sürecinin en çok zaman alan aşaması hangisidir? Neden?</b></summary>

Veri ön işleme. Sonuçların kalitesi verinin kalitesine bağlıdır; özensiz hazırlık model aşamasından sürekli geri dönülmesine yol açar.
</details>

<details>
<summary><b>4. 5, 8, 15, 21, 22, 30 verisini iki bölüme ayırıp ortalama ile düzeltin.</b></summary>

Bölüm 1: 5, 8, 15 → ortalama 9,33 → 9,33 / 9,33 / 9,33
Bölüm 2: 21, 22, 30 → ortalama 24,33 → 24,33 / 24,33 / 24,33
</details>

<details>
<summary><b>5. Aynı veriyi sınır değerleriyle düzeltin.</b></summary>

Bölüm 1: 5, 5, 15 (8 → 5'e yakın)
Bölüm 2: 21, 21, 30 (22 → 21'e yakın)
</details>

<details>
<summary><b>6. Ön işlemede yapılan işlemler nelerdir?</b></summary>

Verilerin toplanması ve birleştirilmesi; temizlenmesi (kayıp veriler ve gürültü); yeniden yapılandırılması (normalizasyon, azaltma, dönüştürme).
</details>

<details>
<summary><b>7. Kümeleme ile sınıflandırma arasındaki fark nedir?</b></summary>

Sınıflandırmada sınıflar önceden bellidir (denetimli öğrenme, tahmin edici model). Kümelemede önceden tanımlı sınıf yoktur, gruplar benzerliğe göre oluşur (denetimsiz öğrenme, tanımlayıcı model).
</details>

<details>
<summary><b>8. Aşırı öğrenme (overfitting) nedir?</b></summary>

Modelin çıkardığı kuralların yalnızca eğitim verisinde geçerli olup yeni verilerde başarısız olmasıdır; model genellemek yerine ezberlemiştir.
</details>

<details>
<summary><b>9. Geleneksel istatistik ile veri madenciliği arasındaki temel farklar nelerdir?</b></summary>

Hipotez gerekliliği, eşitliklerin elle ya da otomatik geliştirilmesi, veri türleri (sayısal vs. metin/ses), veri temizliğinin zamanlaması ve sonuçların yorumlanma kolaylığı (bkz. Bölüm 10).
</details>

<details>
<summary><b>10. Wald örneğinde DIKW katmanlarını eşleştirin.</b></summary>

Veri: delik sayıları ve konumları · Enformasyon: deliklerin yoğunlaştığı bölgelerin haritası · Bilgi: boş kalan motor/kokpit bölgelerinin ölümcül olduğunun kavranması · Bilgelik: zırhı deliksiz görünen hayati bölgelere ekleme kararı.
</details>

<details>
<summary><b>11. "Dondurma satışları arttıkça köpekbalığı saldırıları artıyor, öyleyse dondurma satışını yasaklayalım." Bu çıkarımdaki hata nedir?</b></summary>

Korelasyon nedensellik sanılmıştır (cum hoc ergo propter hoc). İki değişkeni de etkileyen karıştırıcı değişken sıcak havadır: yazın hem dondurma tüketimi hem denize girme artar.
</details>

<details>
<summary><b>12. k-NN algoritmasında k değeri çok büyük ya da çok küçük seçilirse ne olur?</b></summary>

Çok büyük k: Birbirine benzemeyen noktalar aynı sınıfa toplanır. Çok küçük k: Aslında aynı sınıftan olan noktalar ayrı sınıflara düşebilir; gürültüye duyarlılık artar.
</details>

---

### 📌 Akılda Kalsın

- Veri madenciliği **önceden bilinmeyeni** keşfeder; bilineni doğrulamaz.
- Veri madenciliği, KDD sürecinin **bir adımıdır**.
- Sürecin en uzun aşaması **ön işlemedir**: çöp girer, çöp çıkar.
- **Tahmin edici** (regresyon, sınıflandırma) ↔ **tanımlayıcı** (kümeleme, birliktelik, sıra örüntü, özetleme).
- **Denetimli** = etiket var; **denetimsiz** = etiket yok.
- **Korelasyon ≠ nedensellik.** Özet istatistiğe güvenmeden önce **görselleştir**.

---

*Ders geri bildirim formunu doldurmayı unutmayın!*
