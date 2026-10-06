# 2. Hafta: Veri Hazırlama ve Ön İşleme Uygulaması

Bu klasör, **YBS 301 Veri Madenciliği** dersinin 2. haftasına ait ders sunumunu ve uygulamalı laboratuvar çalışmasını (**Gümüşhane Pestil & Köme Veri Seti**) barındırmaktadır.

---

## 📌 Hafta İçeriği & Materyaller

* 📑 **Ders Sunumu:** [2.pptx](2.pptx)
* 📁 **Uygulama Veri Seti Dizin:** [gumushane_pestil_kome_veriseti/](gumushane_pestil_kome_veriseti/)
* 📄 **Detaylı Öğrenci Rehberi:** [OGRENCI_OKU_BENI.md](gumushane_pestil_kome_veriseti/OGRENCI_OKU_BENI.md)

---

## 🏬 Vaka Senaryosu: Gümüşhane Pestil & Köme İşletmesi

Gümüşhane çarşısında faaliyet gösteren kurgusal bir aile işletmesi, pestil, köme, dut pekmezi ve kuşburnu marmelatı gibi yöresel ürünleri iki farklı kanaldan satmaktadır:
1. **Çarşı Dükkanı (Fiziki Kasa)**
2. **E-Ticaret Pazaryeri (Online)**

Veriler 3 farklı sistemden gelmekte olup gürültülü, eksik ve tutarsız kayıtlar içermektedir. Bu haftaki uygulamamızın amacı, bu ham verileri temizleyip birleştirerek analize hazır **tek ve temiz bir veri seti** haline getirmektir.

---

## 📁 Veri Seti Dosyaları

| Dosya | Kaynak | Açıklama & Format Özellikleri |
| :--- | :--- | :--- |
| `A_dukkan_kasa_satislari.csv` | Dükkan Kasa Yazılımı | Ayırıcı `;`, ondalık `,` (Türkçe Excel çıktısı) |
| `B_eticaret_siparisleri.xlsx` | Pazaryeri Dışa Aktarımı | İngilizce sütunlar; `metadata` sayfasını mutlaka okuyunuz |
| `C_uretici_kayitlari.csv` | Üretici Registrasyon Defteri | Ayırıcı `;` |
| `D_ilce_referans_tablosu.csv` | Dış Kaynak Referans Tablosu | Temiz kabul edilen referans tablosu (mesafe, rakım vb.) |

---

## 🎯 Laboratuvar Görev Başlıkları

1. **Değişken Tipleri:** Sütunların ölçek türlerine (İsimsel, İkili, Sıra, Tamsayı, Aralıklı, Oranlı) atanması ve analize katkısının değerlendirilmesi.
2. **Veri Temizleme:** Gürültülü, eksik (imputation) ve tutarsız kayıtların tespiti ve kurallara göre temizlenmesi.
3. **Veri Birleştirme:** Şema eşleştirme (schema matching), varlık eşleştirme (entity resolution) ve çelişen değerlerin giderilmesi.
4. **Veri İndirgeme:** Veri küpü (roll-up), boyut indirgeme, veri sıkıştırma (CSV, gzip, Parquet karşılaştırması) ve tabakalı örnekleme.
5. **Veri Dönüştürme:** Min-Max ve Z-Score normalizasyonu, kategorik genelleştirme ve yeni özellik (feature engineering) türetme.

> [!TIP]
> Görevlerin detaylı açıklamaları, soru yönlendirmeleri ve teslim kriterleri için [`gumushane_pestil_kome_veriseti/OGRENCI_OKU_BENI.md`](gumushane_pestil_kome_veriseti/OGRENCI_OKU_BENI.md) dosyasını inceleyiniz.
