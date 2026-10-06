# YBS 301 – Veri Madenciliği
## Çalışma Notları · 2. Hafta: Verinin Hazırlanması

> **"Çöp girerse, çöp çıkar" (Garbage in, garbage out)**
> Veri hazırlığı sıkıcı bir angarya değil; veri madenciliği çıktısının kalitesini ve güvenilirliğini belirleyen en kritik mühendislik sürecidir.

Bu notlar, ders kitabının 3. ünitesi (Verinin Hazırlanması) ile ders sunumundaki şemalar birleştirilerek hazırlanmıştır.

---

## İçindekiler

0. [Geçen Haftanın Özeti (b12 Testi)](#0-geçen-haftanın-özeti-b12-testi)
1. [Veri Hazırlama Nedir, Neden Bu Kadar Vakit Alır?](#1-veri-hazırlama-nedir-neden-bu-kadar-vakit-alır)
2. [Temel Kavramlar: Nesne, Özellik, Ölçme, Ölçek](#2-temel-kavramlar-nesne-özellik-ölçme-ölçek)
3. [Temel Değişken Tipleri](#3-temel-değişken-tipleri)
4. [4 Aşamalı Veri Rafineri Hattı](#4-4-aşamalı-veri-rafineri-hattı)
5. [İstasyon 1: Veri Temizleme](#5-istasyon-1-veri-temizleme)
6. [İstasyon 2: Veri Birleştirme](#6-istasyon-2-veri-birleştirme)
7. [İstasyon 3: Veri İndirgeme](#7-istasyon-3-veri-indirgeme)
8. [İstasyon 4: Veri Dönüştürme ve Normalleştirme](#8-istasyon-4-veri-dönüştürme-ve-normalleştirme)
9. [Uygulama: Python ve R ile Normalleştirme](#9-uygulama-python-ve-r-ile-normalleştirme)
10. [Kendini Sına](#10-kendini-sına)

---

## 0. Geçen Haftanın Özeti (b12 Testi)

Derse başlarken geçen haftayı hatırlayalım. Önceki haftanın veri setlerine (Iris, Wine, Breast Cancer, California Housing, Titanic, MNIST, 20 Newsgroups) göz atma fırsatınız oldu mu?

### Karşılaştırmalı analiz matrisi

| | Geleneksel İstatistik | Veri Madenciliği |
|---|---|---|
| **Yaklaşım** | Önceden kurulan bir **hipotez** ile başlar | Hipotez olmadan **otomatik keşif** yapar |
| **Veri tipi** | Çoğunlukla sayısal (nümerik) veri | Metin, ses, görsel gibi çok boyutlu veri |
| **Bilgi derinliği** | Sığ bilgi (özet ve tanımlayıcı sonuçlar) | Derin ve gizli bilgi (önceden tahmin edilemeyen örüntüler) |

### KDD süreci

```
1. Amacın Tanımlanması → 2. Ön İşlemler → 3. Modelin Kurulması → 4. Kullanım ve Yorumlama → 5. İzleme
                           ▲ Sürecin en uzun ve kritik aşaması (bu haftanın konusu!)
```

### Model motorları

| | Tahmin Edici (Predictive) | Tanımlayıcı (Descriptive) |
|---|---|---|
| Öğrenme tipi | **Denetimli**: hedef değişken ve sınıflar (ör. Kadın/Erkek) bellidir | **Denetimsiz**: önceden belirlenmiş etiket yoktur |
| Amaç | Geçmişten öğrenip geleceği tahmin etmek | Verideki doğal benzerlikleri ve gizli örüntüleri tanımlamak |
| Kategoriler | Regresyon, sınıflandırma | Kümeleme, birliktelik kuralları, sıra örüntüleri, özetleme |
| Algoritmalar / risk | Karar ağaçları, YSA, k-NN, genetik algoritmalar, zaman serisi · Risk: **aşırı öğrenme** | Pazar sepeti, ameliyat → enfeksiyon gibi zaman aralıklı ilişkiler |

### Sektörel uygulamalar

**Pazarlama:** satın alma örüntüleri, hedef odaklı kampanyalar · **Finans:** kredi kartı dolandırıcılığı, risk yönetimi, hisse tahmini · **Sağlık:** ilaç etkileri, erken teşhis · **Endüstri:** kalite kontrol, makine performansını düşüren gizli faktörler · **Eğitim:** öğrenci başarı/başarısızlık nedenleri

---

## 1. Veri Hazırlama Nedir, Neden Bu Kadar Vakit Alır?

**Veri hazırlama:** Toplanan ham (işlenmemiş) verinin veri madenciliğinde analize hazır duruma getirilmesi için yapılan işlemlerin bütünü.

- **Amaç:** Ham verinin yapısındaki, onu değersizleştiren hataları ve sorunları ortadan kaldırmak.
- Literatürde aşamaların adı ve sayısı yazara göre değişir, ama amaç hep aynıdır.
- Temizleme, birleştirme, indirgeme, dönüştürme ve anlama işlemleri **analistin zamanının yaklaşık %80'ini** alır.

### Buzdağı benzetmesi

| Görünen kısım (su üstü) | Görünmeyen kısım (su altı) |
|---|---|
| Veri madenciliği ve keşif: değerli taşların madenden çıkarılması | Veri hazırlama: temizleme, birleştirme, indirgeme, dönüştürme (%80) |

### Neden bu kadar vakit alır?

- Gerçek dünya verisi **kusurludur**.
- İnsan hataları, teknolojik kısıtlar ve sistem arızaları veriyi **gürültülü (noisy)**, **eksik (missing)** ve **tutarsız (inconsistent)** hâle getirir.

### Veri nereden gelir?

İnsanın oluşturduğu bilgisayar dosyaları, işletme veritabanı yönetim sistemleri, standart veritabanları, otomatik kayıt araçları (RFID, barkod, karekod), uydular… Farklı kaynaklar, farklı yapı ve tiplerde veri demektir.

> 💡 **Hatırlatma:** "Önceden bilinmeyen" bilgi, sonucun **tahmin edilemediği** anlamına gelir. Sonucu zaten tahmin edilebilen bir soru için veri madenciliğinin maliyetine katlanmak mantıklı değildir.

---

## 2. Temel Kavramlar: Nesne, Özellik, Ölçme, Ölçek

Bir veri seti tablo olarak gösterilir:

```
               ÖZELLİKLER (sütunlar)
              A      B      C      D      E
NESNELER  K1  ·      ·      ·      ·      ·
(satırlar)K2  ·      ·      ·      ·      ·
          K3  ·      ·   [değer]   ·      ·   ← verilen nesne için özelliğin aldığı değer
          K4  ·      ·      ·      ·      ·
```

| Kavram | Tanım | Eş anlamlıları |
|---|---|---|
| **Nesne** | Tablodaki satırlar; gözlemler | kayıt, gözlem, örnek (instance) |
| **Özellik** | Tablodaki sütunlar; varlıkları birbirinden ayırt eden değişkenler | değişken, nitelik, öznitelik (feature) |
| **Ölçme** | Birimlerin sahip olduğu özelliklerin derecesini belirleyip sayısal olarak ifade etmek | |
| **Ölçek** | Sınıflama, sıralama, derecelendirme veya miktar belirleme için uyulması gereken kuralları ve kısıtları belirleyen ölçme aracı | |

**Market örneği** — hepsi ölçmedir ama ölçekleri farklıdır:
- Ürünleri türlerine göre sınıflamak → isimsel
- Çalışanları yönetim katından en alt kademeye sıralamak → sıra gösteren
- Bir ürünün ağırlığını ölçmek → oranlı
- Çalışanların aylık performansını puanlamak → sayısal ölçek

> ⚠️ Değişken tipleri arasındaki farkı bilmemek analizde ciddi hatalara yol açar (ör. posta kodlarının ortalamasını almak).

---

## 3. Temel Değişken Tipleri

### Değişken tipleri matrisi

| Grup | Değişken Tipi | Temel İşlevi | İzin Verilen İşlemler | Mutlak Sıfır? | Örnekler |
|---|---|---|---|---|---|
| **Kategorik** | **İsimsel (Nominal)** | Sınıflandırma, etiketleme | Yalnızca eşitlik (=, ≠), sayma | Yok | Cinsiyet, ürün türü, hastalık türü |
| | **İkili (Binary)** | İki olasılıklı durum | Sayma | Yok | Doğru/Yanlış, Pozitif/Negatif, 0/1 |
| | **Sıra Gösteren (Ordinal)** | Derecelendirme, sıralama | =, ≠, <, > | Yok | Kıdem, unvan, mezuniyet derecesi |
| **Sürekli (sayısal)** | **Tamsayılı (Integer)** | Kesir alamayan sayılabilir değerler | +, −, × | Var | Satılan ekmek sayısı, koli adedi, çocuk sayısı |
| | **Aralıklı (Interval-scaled)** | Eşit aralıklı nicel ölçüm | +, − | **Yok** (göreli sıfır) | Hava sıcaklığı (°C) |
| | **Oranlı (Ratio-scaled)** | En üst düzey nicel ölçüm | Tüm işlemler, **oranlama** | **Var** (mutlak yokluk) | Ağırlık, boy, gelir |

### Her tip için kritik noktalar

**İsimsel:** Sayı ile kodlanabilir (5 kişi → 1, 2, 3, 4, 5) ama bu sayılar yalnızca **etikettir**; aritmetik işlem anlamsızdır.

**İkili:** İsimsel değişkenin özel hâlidir; yalnızca iki sonuç vardır.

**Sıra gösteren:** Hem eşitlik hem sıralama içerir, yani isimsel değişkeni **kapsar**. Ama kademeler arası mesafeler eşit değildir: "müdür" ile "şef" arasındaki fark, "şef" ile "memur" arasındaki farkla aynı değildir.

**Aralıklı:** Sıra gösterenin tüm özelliklerine ek olarak farklar matematiksel olarak anlamlıdır. Sıfır noktası **keyfidir**: 0 °C "sıcaklık yok" demek değildir.
→ Bu yüzden **oran hesaplanamaz**: 20 °C, 10 °C'nin "iki katı sıcak" değildir.

**Oranlı:** Sıfır her ölçüm biriminde aynı anlama gelir: 0 kg = 0 g = ağırlık yok. Bu yüzden **oranlama yapılabilir**: 10 kg, 5 kg'ın iki katıdır. Diğer tüm tiplerin özelliklerini içerir.

### Ölçek hiyerarşisi

```
İsimsel  ⊂  Sıra Gösteren  ⊂  Aralıklı  ⊂  Oranlı
  (=)        (=, <, >)       (+, −)       (×, ÷, oran)
```

Her üst düzey, alttakilerin tüm özelliklerini taşır.

> 🧠 **Hızlı test:** "Sıfır, yokluk anlamına geliyor mu?" → Evet: oranlı · Hayır: aralıklı.
> "Sıralama anlamlı mı?" → Evet: sıra gösteren · Hayır: isimsel.

---

## 4. 4 Aşamalı Veri Rafineri Hattı

```
Gürültülü     ┌────────────┐   ┌──────────────┐   ┌─────────────┐   ┌───────────────┐    Analize Hazır
Ham Veri  ──► │ 1. TEMİZLE │──►│ 2. BİRLEŞTİR │──►│ 3. İNDİRGE  │──►│ 4. DÖNÜŞTÜR   │──► Kaliteli Veri
              └────────────┘   └──────────────┘   └─────────────┘   └───────────────┘
              Tutarsızlığı     Farklı kaynakları  Hacmi ve boyutu   Algoritmanın
              düzelt, eksiği   eşleştir; şema ve  daralt, maliyeti  anlayacağı forma
              tamamla, gürül-  birim uyumsuzluk-  düşür             getir (ör. 0–1
              tüyü filtrele    larını çöz                           aralığı)
```

| İstasyon | Amaç | Sloganı |
|---|---|---|
| 1. Temizleme | Eksik veri, gürültü, tutarsızlık | Eksikliği gider, aykırı değeri tıraşla |
| 2. Birleştirme | Çoklu kaynağı tek veri ambarında toplamak | Şemaları düğümle, tekrarları sil |
| 3. İndirgeme | Daha küçük ama aynı sonucu veren veri | Boyutu daralt, hacmi sıkıştır |
| 4. Dönüştürme | Algoritmaya uygun form | Z-skor/min-maks ile matematiksel kalıba sok |

> 📝 **Veri kalitesi** şu sorunların varlığıyla ölçülür: gürültü ve aykırı değerler, eksik, tutarsız ve tekrarlı veriler.
> Çoğu uygulamada bu süreçlerden **birden fazlası** birlikte uygulanır; sıra veri yapısına göre değişebilir.

---

## 5. İstasyon 1: Veri Temizleme

**Tanım:** Veri kalitesi problemlerinin fark edilmesi ve doğrulanması. Üç ana başlık: **eksik veri, gürültülü veri, tutarsız veri.**

### 5.1 Eksik veri

**Nedenleri:** Ankette bilgi vermek istememe, yanlış anlama, veri giriş hatası, tutarsız olduğu için silinme.

> ⚠️ **Her boş değer eksik veri değildir!** Kimlik tablosunda kadınlara ait kayıtlarda askerlik bilgisinin boş olması, o özelliğin o nesne için **uygulanamaz** olmasından kaynaklanır. Bunu "eksik" sayıp doldurmak hataya yol açar.

#### Eksik veri stratejisi karar ağacı

```
                    Veri setinde eksik (NULL) değerler var
                                   │
       ┌───────────────────────────┼─────────────────────────────┐
       ▼                           ▼                             ▼
 Veri seti büyük ve          Algoritma eksik veriyi       Eksik değerin tahmin
 eksik oranı çok mu          kendi tolere edebiliyor mu?  edilmesi mi gerekiyor?
 düşük?                            │ Evet                        │ Evet
       │ Evet                      ▼                             ▼
       ▼                     GÖZ ARDI ET                  TAHMİN EDEREK DOLDUR
 NESNEYİ/ÖZELLİĞİ ELE        (ör. kümelemede yalnızca     (Imputation)
 En basit yol; ama           dolu özelliklerle            ├─ Elle doldurma
 enformasyon kaybı riski     benzerlik hesabı)            ├─ Sabit değer (riskli)
                                                          ├─ Ortalama/medyan/mod
                                                          ├─ Sınıf ortalaması
                                                          └─ Regresyon / karar ağacı
                                                             (en güvenilir)
```

#### Stratejilerin ayrıntısı

**A) Elemek**
- **Nesneyi (satırı) silmek:** Basit ve etkili. Ama o satırın diğer özelliklerindeki enformasyon da kaybolur. Yalnızca birkaç eksik satır varsa uygundur.
- **Özelliği (sütunu) silmek:** O özellik analiz için önemli olabilir; dikkatli olunmalı.

**B) Tahmin ederek doldurmak**

| Yöntem | Açıklama | Değerlendirme |
|---|---|---|
| Elle doldurma | Eksik değeri tek tek bulup girmek | Eksik çok, veri büyükse uygulanamaz |
| Sabit değer | Tüm boşluklara "Bilinmiyor" veya 0 gibi bir değer | Basit ama algoritmayı yanıltır, **tercih edilmez** |
| Merkezi eğilim ölçüsü | Aynı özelliğin ortalaması, medyanı veya modu | Hızlı; varyansı düşürür |
| Sınıf ortalaması | Önce eksik verinin ait olduğu sınıf belirlenir, o sınıfın ortalaması kullanılır | Genel ortalamadan daha isabetli |
| **En olası değer** | Regresyon, sonuç çıkarmaya dayalı araçlar veya karar ağaçlarıyla tahmin | Mevcut enformasyondan **en çok yararlanan** ve **en sık kullanılan** yöntem |

**C) Göz ardı etmek**
Birçok algoritma eksik veriyi atlayacak şekilde ayarlanabilir. Örneğin kümelemede iki nesne arasındaki benzerlik, yalnızca ikisinde de dolu olan özelliklerle hesaplanır. Özellik sayısı az veya eksik sayısı çok değilse sonuç hemen hemen doğrudur.

### 5.2 Gürültülü veri ve aykırı değerler

**Gürültü:** Analiz edilecek veride beklenen değerlerden sapan aykırı değerler veya hatalar.
**Nedenleri:** Hatalı veri toplama gereçleri, veri girişi ve iletimi problemleri, teknolojik kısıtlar, özellik isimlerindeki tutarsızlık.

#### Müdahale yöntemleri

| # | Yöntem | Nasıl çalışır? |
|---|---|---|
| 1 | **Bölmeleme (Binning)** | Verileri sırala → eşit bölmelere ayır → her bölmeyi bölme ortalaması (veya medyan/sınır değerleri) ile düzleştir. Komşu değerlere bakıldığı için **yerel düzleştirme** sağlar. |
| 2 | **Kümeleme (Clustering)** | Benzer verileri kümelere topla; **hiçbir kümeye girmeyen** noktalar aykırı değerdir. |
| 3 | **İnsan–bilgisayar denetimi** | Bilgisayar şüpheli örüntüleri işaretler, insan karar verir. Örnek: El yazısı tanımada aykırı bir örüntünün faydalı mı çöp mü olduğunu insan daha kolay ayırt eder. |
| 4 | **Regresyon** | Veriyi bir fonksiyona (doğruya) uydurarak pürüzleri giderir. |

**Bölmeleme hatırlatması (1. haftadan):**
Veri `4, 8, 15, 21, 21, 24, 25, 28, 34` → 3 bölme
- Bölme 1: 4, 8, 15 → ortalama **9** → 9, 9, 9
- Bölme 2: 21, 21, 24 → ortalama **22** → 22, 22, 22
- Bölme 3: 25, 28, 34 → ortalama **29** → 29, 29, 29

### 5.3 Tutarsız veri

- Bazı tutarsızlıklar **kaynak belgelere** bakılarak elle düzeltilebilir.
- Bilgi mühendisliği araçları, bilinen veri kısıtlarını ihlal eden kayıtları bulur. Örneğin özellikler arası **işlevsel bağımlılıklar** ("posta kodu → şehir") hataları ortaya çıkarabilir.
- Örnek: Doğum tarihi 2010, yaş 45 → tutarsız kayıt.

---

## 6. İstasyon 2: Veri Birleştirme

**Tanım:** Çoklu kaynaklardan (veritabanları, veri küpleri, dış dosyalar) gelen verinin uygun bir **veri ambarında** birleştirilmesi.

### Çözüm matrisi

| Problem | Açıklama | Çözüm |
|---|---|---|
| **Şema uyuşmazlığı** | Aynı varlık farklı kaynaklarda farklı isimlendirilmiş (`musteri_id` ↔ `cust_no`) | **Meta veri** (veri hakkında veri) ve veri sözlükleriyle eşleştirme |
| **Veri fazlalığı (Redundancy)** | Aynı özellik birden fazla kaynaktan gelip tekrarlanmış (ör. hem "yıllık gelir" hem "aylık gelir × 12") | **Korelasyon analizi**: iki değişken arasındaki ilişkinin yönü, büyüklüğü ve önemi ölçülerek tekrarlar bulunur |
| **Veri değer karmaşası** | Ölçek, birim veya gösterim farkları (Kaynak A kilogram, Kaynak B libre; bir sistemde cinsiyet E/K, diğerinde 0/1) | **Birim dönüşümü ve heterojenlik düzeltmesi**: tek bir standarda indirgeme |

---

## 7. İstasyon 3: Veri İndirgeme

**Amaç:** Çok büyük ve karmaşık veriyi olduğu gibi analiz etmek pratik değildir. Daha küçük hacimde bir veri kümesi oluşturulur.

> 🔑 **Altın kural:** İndirgenmiş veriyle elde edilen sonuç, verinin tamamıyla elde edilecek sonuçtan **çok farklı olmamalıdır**.

### Boyut ve hacim daraltma hunisi

| Yöntem | Ne yapar? | Örnek / Teknik |
|---|---|---|
| **Veri küpü birleştirme (OLAP)** | Ayrıntılı veriyi daha üst düzeyde özetleyerek ön hesaplama yapar | Günlük/aylık satışları yıllık toplama çevirmek |
| **Boyut indirgeme** | Gereksiz veya ilgisiz **özellikleri (sütunları)** çıkarır | İleriye doğru seçme, geriye doğru eleme, ikisinin birleşimi; sarmalama (wrapper) veya süzme (filter) |
| **Veri sıkıştırma** | Kodlama veya dönüşümle verinin sıkıştırılmış gösterimini elde eder | Kayıpsız (lossless) / kayıplı (lossy) |
| **Büyük sayıların indirgenmesi** | Veriyi daha küçük gösterimlerle temsil eder | Parametrik: regresyon, log-doğrusal model · Parametrik olmayan: histogram, kümeleme, örnekleme |

### 7.1 Boyut indirgeme ayrıntıları

**Faydaları:** Algoritmalar daha verimli çalışır, model daha anlaşılır olur, görselleştirme kolaylaşır, işlemci süresi ve bellek ihtiyacı azalır.

**Sorun:** `d` özellik varsa olası alt küme sayısı **2ᵈ**'dir.
Örnek: 30 özellik → 2³⁰ ≈ 1 milyardan fazla alt küme! Hepsini denemek imkânsızdır, bu yüzden **sezgisel (heuristic) yöntemler** kullanılır:

| Sezgisel yöntem | Mantık |
|---|---|
| **İleriye doğru seçme** | Boş kümeyle başla, her adımda en iyi özelliği ekle |
| **Geriye doğru eleme** | Tüm özelliklerle başla, her adımda en kötüsünü çıkar |
| **Birleşik** | Her adımda en iyiyi ekle, en kötüyü çıkar |

En iyi/en kötü özellikler istatistiksel anlamlılık testleri (özelliklerin bağımsız olduğu varsayımıyla) veya karar ağaçlarındaki **enformasyon kazancı (information gain)** gibi ölçütlerle belirlenir.

**Sarmalama (Wrapper) vs. Süzme (Filter):**

| | Sarmalama (Wrapper) | Süzme (Filter) |
|---|---|---|
| Özellik seçerken | Madencilik algoritmasının **kendisini** kullanır | Algoritmadan **bağımsız** ölçütler kullanır |
| Sonuç geçerliliği | Daha yüksek (algoritmanın başarı ölçüsünü en iyiler) | Daha düşük |
| Hesaplama maliyeti | **Çok yüksek** | Düşük |

### 7.2 Veri sıkıştırma

- **Kayıpsız (lossless):** Orijinal veri sıkıştırılmış veriden **birebir** geri elde edilebilir (ör. ZIP).
- **Kayıplı (lossy):** Orijinalin yalnızca **yaklaşık** hâli elde edilebilir (ör. JPEG, MP3).

### 7.3 Büyük sayıların indirgenmesi (numerosity reduction)

- **Parametrik:** Verinin kendisi yerine yalnızca **modelin parametreleri** saklanır.
  - Doğrusal regresyon: veriyi bir doğruya uydurur (y = a + bx → yalnızca a ve b saklanır).
  - Çoklu regresyon: birden fazla özellikle modeller.
  - Log-doğrusal model: kesikli çok boyutlu olasılık dağılımlarını yaklaşık olarak modeller.
- **Parametrik olmayan:**
  - **Histogram** (en yaygını): Veriyi aralıklara bölüp dağılımı elde eder.
  - **Kümeleme:** Veriyi kümelerle ve küme temsilcileriyle ifade eder.
  - **Örnekleme:** Büyük veri kümesini çok daha küçük bir alt kümeyle temsil eder.

---

## 8. İstasyon 4: Veri Dönüştürme ve Normalleştirme

**Neden?** Orijinal özellikler gerekli enformasyonu içerse de algoritmalar için uygun formda olmayabilir. Orijinallerden türetilen yeni özellikler daha faydalı olabilir.

### Beş dönüştürme işlemi

| İşlem | Açıklama | Örnek |
|---|---|---|
| **Düzeltme (Smoothing)** | Verideki gürültüyü temizlemek | Bölmeleme, regresyon, kümeleme |
| **Bir araya getirme (Aggregation)** | Özetleme | Günlük veriyi aylığa çevirmek |
| **Genelleme (Generalization)** | Düşük düzey veriyi daha üst kavramlara taşımak | Yaş → genç/orta yaşlı/yaşlı · Cadde → şehir → ülke |
| **Normalleştirme (Normalization)** | Sayısal değerleri küçük bir aralığa ölçeklemek | Min-maks, z-skor, ondalık ölçekleme |
| **Özellik oluşturma (Feature construction)** | Mevcut özelliklerden yeni özellik türetmek | Yükseklik × genişlik → **alan** |

> ⚠️ **Karıştırmayın:** Veri madenciliğindeki "normalleştirme", istatistikteki bir değişkeni **normal dağılıma** dönüştürme işlemi değildir. Burada amaç yalnızca **ölçeklemektir**.

**Normalleştirme neden gerekli?**
- **Yapay sinir ağlarında** öğrenme aşamasını hızlandırır.
- **Mesafeye dayalı** algoritmalarda (kümeleme, k-NN) zorunluya yakındır. Aksi hâlde değer aralığı büyük olan özellik (ör. maaş: 15.000–80.000) küçük olanı (ör. yaş: 20–65) ezer.

### Normalleştirme tanı matrisi

| Yöntem | Formül | Çıktı Aralığı | Kullanım Mantığı |
|---|---|---|---|
| **Min-Maks (Enk-Enb)** | X* = (X − X_enk) / (X_enb − X_enk) | **[0, 1]** | Doğrusal dönüşüm; veriyi alt ve üst sınırları arasında dar bir alana hapseder |
| **Z-Skor** | X* = (X − X̄) / s | Çoğunlukla **−3 ile +3** (ortalama = 0, std = 1) | Uygulamada **en çok kullanılan**; her değerin ortalamadan kaç standart sapma uzakta olduğunu ölçer |
| **Ondalık Ölçekleme** | X* = X / 10ʲ | **(−1, +1)** | Virgülü, en büyük mutlak değerin basamak sayısı kadar sola kaydırır |

---

### Çalışılmış örnek veri

Üç yöntemde de aynı veriyi kullanacağız:

`X = 251, 148, 166, 244, 472, 356, 379`

### 8.1 Min-Maks (Enk-Enb) Normalleştirme

X_enk = 148, X_enb = 472 → payda = 472 − 148 = **324**

| X | Hesap | X* |
|---|---|---|
| 251 | (251 − 148) / 324 = 103 / 324 | **0,318** |
| 148 | (148 − 148) / 324 = 0 / 324 | **0** |
| 166 | (166 − 148) / 324 = 18 / 324 | **0,056** |
| 244 | (244 − 148) / 324 = 96 / 324 | **0,296** |
| 472 | (472 − 148) / 324 = 324 / 324 | **1** |
| 356 | (356 − 148) / 324 = 208 / 324 | **0,642** |
| 379 | (379 − 148) / 324 = 231 / 324 | **0,713** |

> ✅ En küçük değer her zaman 0, en büyük değer her zaman 1 olur.
> ⚠️ **Zayıf yönü:** Aykırı değerlere çok duyarlıdır. 472 yerine hatalı bir 4720 olsaydı diğer tüm değerler 0'a yığılırdı. Ayrıca yeni gelen bir veri eski aralığın dışındaysa sonuç [0, 1] dışına taşar.

### 8.2 Z-Skor Normalleştirme

**Adım 1 – Ortalama:**
X̄ = (251 + 148 + 166 + 244 + 472 + 356 + 379) / 7 = 2016 / 7 = **288**

**Adım 2 – Standart sapma (örneklem, n − 1):**

| X | X − X̄ | (X − X̄)² |
|---|---|---|
| 251 | −37 | 1.369 |
| 148 | −140 | 19.600 |
| 166 | −122 | 14.884 |
| 244 | −44 | 1.936 |
| 472 | 184 | 33.856 |
| 356 | 68 | 4.624 |
| 379 | 91 | 8.281 |
| **Toplam** | **0** | **84.550** |

s = √(84.550 / 6) = √14.091,67 ≈ **118,71**

**Adım 3 – Dönüştürme:**

| X | Hesap | X* |
|---|---|---|
| 251 | −37 / 118,71 | **−0,312** |
| 148 | −140 / 118,71 | **−1,179** |
| 166 | −122 / 118,71 | **−1,028** |
| 244 | −44 / 118,71 | **−0,371** |
| 472 | 184 / 118,71 | **1,550** |
| 356 | 68 / 118,71 | **0,573** |
| 379 | 91 / 118,71 | **0,767** |

> 📌 **Yorum:** 148 değeri ortalamanın yaklaşık 1,18 standart sapma **altında**, 472 değeri ise 1,55 standart sapma **üstündedir**.
> ✅ Kontrol: Dönüştürülmüş değerlerin ortalaması 0, standart sapması 1'dir.

> ⚠️ **Dikkat 1:** Ders kitabında z-skor sonucunun "sıfır ile bir arasında" olduğu yazmaktadır; bu doğru değildir. Örnekte de görüldüğü gibi negatif değerler ve 1'den büyük değerler çıkar. Doğrusu: Ortalama 0, standart sapma 1 olur; değerlerin çoğu −3 ile +3 arasına düşer.
> ⚠️ **Dikkat 2:** Kitaptaki tabloda 379 için 0,770 yazmaktadır; doğru değer **0,767**'dir (R çıktısı da 0,7666 verir).

### 8.3 Ondalık Ölçekleme

X* = X / 10ʲ, burada **j**, max|X*| < 1 olmasını sağlayan **en küçük tam sayıdır**.

En büyük mutlak değer 472 → 3 basamaklı → **j = 3** → tüm değerler 1.000'e bölünür.

| X | 251 | 148 | 166 | 244 | 472 | 356 | 379 |
|---|---|---|---|---|---|---|---|
| X* | 0,251 | 0,148 | 0,166 | 0,244 | 0,472 | 0,356 | 0,379 |

> 💡 Negatif değerlerde de çalışır: −986 ile 917 arasındaki bir veride max|X| = 986 → j = 3 → −0,986 ile 0,917 arası.

### Üç yöntemin karşılaştırması

| X | Min-Maks | Z-Skor | Ondalık |
|---|---|---|---|
| 148 | 0 | −1,179 | 0,148 |
| 166 | 0,056 | −1,028 | 0,166 |
| 244 | 0,296 | −0,371 | 0,244 |
| 251 | 0,318 | −0,312 | 0,251 |
| 356 | 0,642 | 0,573 | 0,356 |
| 379 | 0,713 | 0,767 | 0,379 |
| 472 | 1 | 1,550 | 0,472 |

> 🔑 Üç yöntem de **sıralamayı ve göreli mesafeleri korur** (doğrusal dönüşümlerdir); yalnızca ölçek değişir.

### Hangisini ne zaman seçmeli?

| Durum | Öneri |
|---|---|
| Kesin sınırlı bir aralık gerekiyorsa (ör. YSA girdisi, görüntü pikselleri) | Min-Maks |
| Veride aykırı değer var veya min-maks bilinmiyorsa | Z-Skor |
| Hızlı, basit ve yorumlanabilir bir ölçek isteniyorsa | Ondalık ölçekleme |

---

## 9. Uygulama: Python ve R ile Normalleştirme

<details>
<summary>🐍 Python (pandas + scikit-learn)</summary>

```python
import numpy as np
import pandas as pd
from sklearn.preprocessing import MinMaxScaler, StandardScaler

df = pd.DataFrame({"X": [251, 148, 166, 244, 472, 356, 379]})

# 1) Min-Maks
df["minmax"] = MinMaxScaler().fit_transform(df[["X"]])

# 2) Z-Skor (kitaptaki gibi örneklem std, n-1)
df["zskor_kitap"] = (df["X"] - df["X"].mean()) / df["X"].std(ddof=1)

# 2b) scikit-learn StandardScaler (popülasyon std, n)
df["zskor_sklearn"] = StandardScaler().fit_transform(df[["X"]])

# 3) Ondalık ölçekleme
j = int(np.ceil(np.log10(df["X"].abs().max() + 1)))
df["ondalik"] = df["X"] / 10**j

print(df.round(3))
```

> ⚠️ `StandardScaler`, standart sapmayı **n** ile hesaplar (popülasyon), kitap ise **n − 1** ile (örneklem). Bu yüzden sonuçlar küçük farklılık gösterir (ör. 472 için 1,550 yerine 1,674). İkisi de doğrudur; hangi formülün kullanıldığına dikkat edin.

**Eksik veri doldurma örneği:**

```python
from sklearn.impute import SimpleImputer

veri = pd.DataFrame({"yas": [25, np.nan, 40, 35, np.nan],
                     "sehir": ["Ankara", "İzmir", np.nan, "Ankara", "Ankara"]})

veri["yas"] = SimpleImputer(strategy="median").fit_transform(veri[["yas"]]).ravel()
veri["sehir"] = SimpleImputer(strategy="most_frequent").fit_transform(veri[["sehir"]]).ravel()
print(veri)
```

Kategorik özellikte ortalama alınamayacağı için **mod (en sık değer)** kullanıldığına dikkat edin.

</details>

<details>
<summary>📊 R (clusterSim paketi – ders kitabındaki gibi)</summary>

```r
# install.packages("clusterSim")
library(clusterSim)

x <- c(251, 148, 166, 244, 472, 356, 379)

data.Normalization(x, type = "n4")  # Min-Maks
# [1] 0.3179 0.0000 0.0556 0.2963 1.0000 0.6420 0.7130

data.Normalization(x, type = "n1")  # Z-Skor
# [1] -0.3117 -1.1794 -1.0277 -0.3707 1.5500 0.5728 0.7666
```

`clusterSim` paketinde 16 farklı normalleştirme yöntemi vardır. `n1` = z-skor, `n4` = min-maks.

</details>

---

## 10. Kendini Sına

<details>
<summary><b>1. İsimsel ve sıra gösteren değişken arasındaki fark nedir?</b></summary>

İkisi de kategoriktir. İsimsel değişkende yalnızca eşitlik/farklılık anlamlıdır (cinsiyet, ürün türü). Sıra gösteren değişkende ise kategoriler arasında **anlamlı bir sıralama** vardır (kıdem, mezuniyet derecesi), ama kademeler arası mesafeler eşit değildir.
</details>

<details>
<summary><b>2. Aşağıdakilerin değişken tipini belirleyin: (a) Kan grubu (b) Sınav notu harfi (AA, BA, BB…) (c) Doğum yılı (d) Aylık gelir (e) Sigara içiyor mu? (f) Bir sınıftaki öğrenci sayısı</b></summary>

(a) İsimsel · (b) Sıra gösteren · (c) Aralıklı (0 yılı "zamanın yokluğu" değildir) · (d) Oranlı · (e) İkili · (f) Tamsayılı
</details>

<details>
<summary><b>3. "Bugün 20 °C, dün 10 °C idi; bugün iki kat daha sıcak." Bu ifade neden yanlıştır?</b></summary>

Celsius **aralıklı** bir ölçektir; 0 °C sıcaklığın yokluğu değil, keyfi bir referans noktasıdır. Mutlak sıfır olmadığı için oran hesaplanamaz. (Kelvin cinsinden: 293 K / 283 K ≈ 1,035; yani yalnızca yaklaşık %3,5 fark vardır.)
</details>

<details>
<summary><b>4. Veri hazırlamanın dört temel süreci nelerdir?</b></summary>

Veri temizleme, veri birleştirme, veri indirgeme, veri dönüştürme.
</details>

<details>
<summary><b>5. Eksik veri için en sık kullanılan ve en güvenilir strateji hangisidir? Neden?</b></summary>

Regresyon veya karar ağaçlarıyla **en olası değerin tahmin edilmesi**. Çünkü diğer özelliklerdeki enformasyondan en fazla yararlanan yöntemdir.
</details>

<details>
<summary><b>6. Bir personel tablosunda kadın çalışanların "askerlik durumu" alanı boştur. Bu alanı ortalama/mod ile doldurmak doğru mudur?</b></summary>

Hayır. Bu bir eksik veri değil, o nesne için **uygulanamaz** bir özelliktir. Doldurmak hatalı bilgi üretir. Bunun yerine "uygulanamaz" gibi ayrı bir kategori kullanılabilir.
</details>

<details>
<summary><b>7. Veri birleştirmede karşılaşılan üç temel sorun ve çözümleri nelerdir?</b></summary>

Şema uyuşmazlığı → meta veri; veri fazlalığı → korelasyon analizi; veri değer karmaşası → birim dönüşümü/standartlaştırma.
</details>

<details>
<summary><b>8. Veri indirgeme yöntemlerini sayınız.</b></summary>

Veri küpü birleştirme, boyut indirgeme, veri sıkıştırma, büyük sayıların indirgenmesi.
</details>

<details>
<summary><b>9. 20 özellikli bir veri setinde kaç olası özellik alt kümesi vardır? Bu neden sorundur?</b></summary>

2²⁰ = 1.048.576 alt küme. Hepsini denemek hesaplama açısından çok maliyetlidir; bu yüzden ileriye doğru seçme / geriye doğru eleme gibi sezgisel yöntemler kullanılır.
</details>

<details>
<summary><b>10. Sarmalama (wrapper) ve süzme (filter) yaklaşımlarının farkı nedir?</b></summary>

Sarmalama, özellik seçerken madencilik algoritmasının kendisini kullanır: daha geçerli sonuç verir ama çok daha fazla hesaplama gerektirir. Süzme, algoritmadan bağımsız ölçütlerle seçim yapar: hızlıdır ama daha az isabetlidir.
</details>

<details>
<summary><b>11. (Sıra Sizde) X = 10, 21, 14, 29, 37, 45 değerlerini z-skor ile normalleştirin.</b></summary>

**Ortalama:** (10 + 21 + 14 + 29 + 37 + 45) / 6 = 156 / 6 = **26**

| X | X − X̄ | (X − X̄)² |
|---|---|---|
| 10 | −16 | 256 |
| 21 | −5 | 25 |
| 14 | −12 | 144 |
| 29 | 3 | 9 |
| 37 | 11 | 121 |
| 45 | 19 | 361 |
| | **Toplam** | **916** |

**Standart sapma:** s = √(916 / 5) = √183,2 ≈ **13,535**

| X | 10 | 21 | 14 | 29 | 37 | 45 |
|---|---|---|---|---|---|---|
| X* | −1,182 | −0,369 | −0,887 | 0,222 | 0,813 | 1,404 |
</details>

<details>
<summary><b>12. Aynı veriyi (10, 21, 14, 29, 37, 45) min-maks ve ondalık ölçekleme ile normalleştirin.</b></summary>

**Min-Maks:** X_enk = 10, X_enb = 45, payda = 35

| X | 10 | 21 | 14 | 29 | 37 | 45 |
|---|---|---|---|---|---|---|
| X* | 0 | 0,314 | 0,114 | 0,543 | 0,771 | 1 |

**Ondalık ölçekleme:** max = 45 → j = 2

| X | 10 | 21 | 14 | 29 | 37 | 45 |
|---|---|---|---|---|---|---|
| X* | 0,10 | 0,21 | 0,14 | 0,29 | 0,37 | 0,45 |
</details>

<details>
<summary><b>13. k-NN algoritmasında "yaş" (20–65) ve "maaş" (15.000–80.000) özellikleri normalleştirilmeden kullanılırsa ne olur?</b></summary>

Öklid mesafesi neredeyse tamamen maaş farkına göre belirlenir; yaş özelliğinin etkisi kaybolur. Normalleştirme, iki özelliğin mesafeye eşit ağırlıkla katkı yapmasını sağlar.
</details>

<details>
<summary><b>14. Min-maks normalleştirmenin en önemli zayıflığı nedir?</b></summary>

Aykırı değerlere çok duyarlıdır. Tek bir uç değer, diğer tüm değerleri dar bir aralığa sıkıştırır. Ayrıca yeni gelen veriler eski min-maks aralığının dışındaysa sonuç [0, 1] dışına taşar.
</details>

---

### 📌 Akılda Kalsın

- Veri hazırlama, analistin zamanının **~%80'ini** alır: **çöp girerse, çöp çıkar.**
- Değişken tipleri: **Kategorik** (isimsel, ikili, sıra gösteren) ↔ **Sürekli** (tamsayılı, aralıklı, oranlı).
- **Aralıklı ≠ oranlı:** Fark, sıfırın "yokluk" anlamına gelip gelmemesidir.
- 4 istasyon: **Temizle → Birleştir → İndirge → Dönüştür.**
- Her boş hücre eksik veri değildir: **uygulanamaz** alanlara dikkat!
- İndirgenmiş veri, tam veriyle **aynı sonuca** yakın sonuç vermelidir.
- **Min-maks** → [0, 1] · **Z-skor** → ortalama 0, std 1 · **Ondalık** → (−1, 1)
- Mesafe tabanlı algoritmalarda (kümeleme, k-NN) ve YSA'da **normalleştirme şarttır**.
