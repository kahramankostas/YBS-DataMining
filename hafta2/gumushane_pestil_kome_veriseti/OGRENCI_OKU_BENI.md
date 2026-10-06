# Gümüşhane Pestil & Köme Satış Verisi — Veri Hazırlama Uygulaması

## Senaryo

Gümüşhane çarşısında faaliyet gösteren kurgusal bir aile işletmesi, pestil, köme, dut pekmezi, kuşburnu marmelatı gibi yöresel ürünleri iki kanaldan satıyor: çarşıdaki dükkan ve bir e-ticaret pazaryeri. Ürünleri ilin altı ilçesindeki (Merkez, Torul, Kürtün, Kelkit, Köse, Şiran) üreticilerden ve kooperatiflerden alıyor. Müşterilerin önemli bir kısmı İstanbul, Ankara, Kocaeli, Bursa ve Almanya'da yaşayan Gümüşhaneliler.

İşletme sahibi şu soruların cevabını istiyor: "Hangi ilçeden, hangi üründen, hangi ayda ne kadar satıyoruz? Gurbetçi müşterilerimiz yerel müşterilerden farklı mı davranıyor? Kargo mesafesi memnuniyeti etkiliyor mu?" Ancak veriler üç ayrı sistemden geliyor ve hiçbiri temiz değil. Sizin göreviniz, bu soruları cevaplayabilecek **tek, temiz, analize hazır bir veri seti** üretmek.

Dönem: Ocak 2024 – Eylül 2025. Kişi ve işletme adları kurgusaldır. Mesafe ve rakım değerleri yaklaşık, ders amaçlıdır.

## Dosyalar

| Dosya | Kaynak | Not |
|---|---|---|
| `A_dukkan_kasa_satislari.csv` | Dükkanın kasa yazılımı | Ayırıcı `;`, ondalık `,` — Türkçe Excel çıktısı |
| `B_eticaret_siparisleri.xlsx` | Pazaryeri dışa aktarımı | İngilizce sütunlar; `metadata` sayfasını mutlaka okuyun |
| `C_uretici_kayitlari.csv` | Üretici/kooperatif kayıt defteri | Ayırıcı `;` |
| `D_ilce_referans_tablosu.csv` | Dış kaynak (referans) | Temiz kabul edilir; düzeltmelerde kullanın |

## Görevler

Her adımda **ne yaptığınızı, neden yaptığınızı ve kaç satırın etkilendiğini** raporlayın. "Sildim" demek yetmez; neyi, kaç tane, hangi kurala göre sildiğinizi yazın.

**1. Değişken tipleri.** Üç dosyadaki her sütunu şu sınıflardan birine atayın: isimsel, ikili, sıra gösteren, tamsayılı, aralıklı ölçekli, oranlı ölçekli. Aralıklı ve oranlı ölçek ayrımını veri setinden en az iki örnekle gerekçelendirin (ipucu: sıcaklık, rakım ve tarih ile ağırlık, tutar ve mesafeyi karşılaştırın). Analize katkısı olmayan sütunları da belirleyin.

**2. Veri temizleme.**
- Gürültülü veri: Fiziksel veya mantıksal olarak imkansız değerleri bulun. Her aykırı değer hata değildir; gerçek ama sıra dışı kayıtları hatalardan ayırt edin ve bu ayrımı nasıl yaptığınızı açıklayın.
- Eksik veri: Eksikliğin veri setinde kaç farklı biçimde kodlandığını bulun (boş hücre tek biçim değildir). Her sütun için "gözardı et" ya da "tahmin et (ortalama/medyan/mod/regresyon)" kararını gerekçesiyle verin.
- Tutarsız veri: Aynı anlamdaki farklı yazımları tek biçime indirin. Birbiriyle çelişen alanları bulun ve D referans tablosu ile alan kısıtları (ör. yaş aralığı, tutar = adet × birim fiyat) yardımıyla düzeltin.

**3. Veri birleştirme.**
- Şema birleştirme: A ve B'deki sütunları eşleştirin. B'nin `metadata` sayfası bu iş için var. B'deki üretici kodlarını C ile eşleştirin.
- Varlık eşleştirme: Aynı müşteri her iki kanalda da alışveriş yapmış olabilir, ancak müşteri numaraları farklı sistemlerden gelir. Ortak müşterileri hangi alanlarla eşleştirdiğinizi ve kaç tane bulduğunuzu raporlayın. Aynı ad-soyada sahip farklı kişilere dikkat edin.
- Veri fazlalığı: Birbirinden türetilebilen sütunları korelasyon analizi ile gösterin ve hangisini tuttuğunuzu açıklayın. Tekrarlanan satırları bulun.
- Değer karmaşıklığı: Para birimi, ağırlık birimi, puan ölçeği, sıcaklık birimi, cinsiyet ve üyelik kodlaması farklılıklarını giderin.

**4. Veri indirgeme.**
- Veri küpü: İlçe × ürün × ay boyutlarında satış tutarı küpü oluşturun; yıl/çeyrek düzeyine toplulaştırın (roll-up).
- Boyut indirgeme: Gereksiz özellikleri gerekçesiyle çıkarın.
- Veri sıkıştırma: Birleşik veri setinizin boyutunu CSV, sıkıştırılmış CSV (gzip) ve Parquet olarak karşılaştırın; hangisinin kayıpsız, hangisinin kayıplı olduğunu tartışın.
- Büyük sayıların indirgenmesi: Sipariş tutarı için histogram (eşit genişlik ve eşit frekans) oluşturun; %10'luk basit rastgele örnek ile ilçeye göre tabakalı örnek alın ve ortalama tutarları karşılaştırın.

**5. Veri dönüştürme.**
- Normalleştirme: Sipariş tutarı, mesafe ve rakım için en küçük-en büyük, z-skor ve ondalık ölçekleme uygulayın. Aykırı değerleri temizlemeden önce ve sonra min-maks sonucunun nasıl değiştiğini gösterin.
- Genelleme: İlçe → bölge (D tablosu), yaş → yaş grubu, tarih → ay / çeyrek / mevsim.
- Özellik oluşturma: En az dört yeni özellik türetin. Öneriler: gurbetçi müşteri (ikili), kg başına fiyat, bayram öncesi sipariş (ikili), enflasyondan arındırılmış tutar.

## Teslim

Temizleme kodu (Python), son temiz veri seti ve her adımdaki karar ve sayıları içeren kısa bir rapor hazırla.
