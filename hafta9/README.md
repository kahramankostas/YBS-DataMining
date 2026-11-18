# 3. Hafta: Veri Hazırlama ve Ön İşleme Laboratuvar Uygulaması

Bu klasör, **YBS 301 Veri Madenciliği** dersinin 3. haftasına ait ders sunumunu, **Gümüşhane Pestil & Köme Veri Seti** üzerinde adım adım gerçekleştirilen uçtan uca uygulamalı Jupyter Notebook'unu, vaka senaryosu kılavuzunu ve tüm materyalleri barındıran sıkıştırılmış arşiv dosyasını (`hafta3.zip`) içermektedir.

---

## 📌 Hafta İçeriği & Materyaller

* 📑 **Ders Sunumu:** [2.pptx](2.pptx) *(Geçen hafta hatırlatması ve uygulama başlangıç rehberi)*
* 📓 **Uygulamalı Jupyter Notebook:** [gumushane_veri_hazirlama_uygulamasi.ipynb](gumushane_pestil_kome_veriseti/gumushane_veri_hazirlama_uygulamasi.ipynb)
* 📁 **Uygulama Veri Seti Dizini:** [gumushane_pestil_kome_veriseti/](gumushane_pestil_kome_veriseti/)
* 📄 **Vaka Senaryosu ve Görev Kılavuzu:** [gumushane_pestil_kome_veriseti/readme.md](gumushane_pestil_kome_veriseti/readme.md)
* 📦 **Tüm Materyaller Tek Paket (ZIP):** [hafta3.zip](hafta3.zip)
* 🐍 **Python, NumPy ve Pandas Pratik Alanı:** [Pratik Rehberi](pratik/readme.md)

---

## 🏬 Uygulama Senaryosu ve Çözülecek İş Problemleri

Gümüşhane çarşısında faaliyet gösteren yöresel bir işletmenin üç farklı sistemden (Dükkan Kasa Satışları, E-Ticaret Pazaryeri, Üretici Kayıtları ve İlçe Referans Tablosu) toplanmış dağınık ve kirli verileri temizlenip birleştirilmektedir.

Uygulama kapsamında işletme sahibinin şu 3 kritik sorusuna analitik yanıtlar aranmaktadır:
1. **İlçelere, ürünlere ve aylara göre satış tutarları nasıl değişmektedir?**
2. **Gurbetçi müşteriler ile yerel müşterilerin satın alma alışkanlıkları farklı mıdır?**
3. **Kargo mesafesi ve teslimat süresi müşteri memnuniyetini (rating) nasıl etkilemektedir?**

---

## 🗺️ Notebook Yol Haritası ve Laboratuvar Adımları

[`gumushane_veri_hazirlama_uygulamasi.ipynb`](gumushane_pestil_kome_veriseti/gumushane_veri_hazirlama_uygulamasi.ipynb) notebook'u içerisinde şu aşamalar adım adım uygulanmaktadır:

| Adım | İşlem Başlığı | Kapsam ve Yapılanlar |
| :---: | :--- | :--- |
| **0** | **Hazırlık & Okuma** | Ham dosyaların karakter kodlaması (UTF-8-SIG), ayırıcılar (`;`, `,`) ve tip korunumu (`dtype=str`) ile okunması. |
| **1** | **Değişken Tipleri** | İsimsel, ikili, sıra, tamsayı, aralıklı ve oranlı ölçek analizi. |
| **2** | **Veri Temizleme** | Gürültülü, tutarsız ve eksik (boş hücre, `?`, `-`, `bilinmiyor`, `1900-01-01`) değerlerin tespiti ve stratejik giderilmesi. |
| **3** | **Veri Birleştirme** | Şema eşleme, varlık çözümleme (entity resolution), birim dönüşümleri (kuruş → TL, gram → kg) ve çoklu kaynak entegrasyonu. |
| **4** | **Veri İndirgeme** | İlçe × Ürün × Ay veri küpü (*roll-up*), boyut indirgeme, dosya formatları karşılaştırması (CSV vs. gzip vs. Parquet) ve tabakalı örnekleme. |
| **5** | **Veri Dönüştürme** | Min-Max ve Z-Score normalizasyonu, kategorik genelleme (ilçe → bölge), yeni öznitelik türetme (*feature engineering*). |
| **6** | **İş Sorularını Cevaplama** | Pivot tablolar, gruplamalar ve istatistiksel karşılaştırmalarla işletme sorularının yanıtlanması. |
| **7** | **Rapor ve Özet** | Her aşamada etkilenen satır sayısını gösteren süreç özet raporunun üretilmesi. |

---

## 💻 Çalışma Yöntemleri

### 1. Google Colab Üzerinde Çalışma
1. `hafta3.zip` arşivini bilgisayarınıza indirin.
2. [Google Colab](https://colab.research.google.com/)'ı açın ve sol menüdeki 📁 simgesinden `hafta3.zip` dosyasını çalışma alanına yükleyin.
3. `gumushane_veri_hazirlama_uygulamasi.ipynb` defterini açarak `Shift + Enter` ile hücreleri sırayla çalıştırın (Zip otomatik açılacaktır).

### 2. Yerel Ortamda (VS Code / Jupyter Lab) Çalışma
1. Klasör içerisindeki `gumushane_veri_hazirlama_uygulamasi.ipynb` dosyasını Jupyter Lab veya VS Code ile açın.
2. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas numpy matplotlib openpyxl pyarrow
   ```
3. Hücreleri sırayla çalıştırarak ✍️ "Sıra Sende" bölümlerini tamamlayın.

---

## 🔗 İlgili Bağlantılar

* 🏠 [Ana Depo Sayfası (README.md)](../readme.md)
* 📂 [2. Hafta: Veri Hazırlama ve Ön İşleme Notları](../hafta2/README.md)
* 🐍 [Python & Pandas Pratik Alanı](../pratik/readme.md)
