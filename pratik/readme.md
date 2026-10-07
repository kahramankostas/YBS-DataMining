# 🐍 Python, NumPy ve Pandas Uygulamalı Pratik Alanı

**YBS 301 - Veri Madenciliği Dersi Pratik ve Alıştırma Rehberi**

Bu klasör, Veri Madenciliği dersinde öğrenilen teorik bilgileri (EDA, veri temizleme, ön işleme, veri dönüştürme vb.) Python ekosisteminin temel analitik kütüphaneleriyle uygulamaya geçirebilmeniz için hazırlanmıştır.

---

## 📌 Pratik Materyalleri ve Eğitim İçerikleri

### 📺 1. Python Temelleri (Video Eğitimi)

Python programlama diline yeni başlayanlar veya temel konuları (değişkenler, döngüler, fonksiyonlar, veri yapıları) tekrar etmek isteyen öğrenciler için önerilen video eğitimi:

**🎬 Python Sıfırdan Öğrenme Ders Videosu**

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/_wZUNiGtkcw"
    title="Python Sıfırdan Öğrenme Ders Videosu"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen>
  </iframe>
</div>
---

### 🔢 2. NumPy ile Sayısal Hesaplama
* 📓 **Notebook Dosyası:** [`01_numpy.ipynb`](01_numpy.ipynb)
* 🎯 **Öğrenme Hedefleri:**
  1. NumPy dizisi (`ndarray`) oluşturma, veri tipleri ve boyut inceleme.
  2. İndeksleme, dilimleme (*slicing*) ve **boolean maskeleme** ile koşullu veri seçimi.
  3. **Vektörel işlemler** ve *broadcasting* kullanarak döngüsüz yüksek hızlı hesaplamalar.
  4. Eksen (*axis*) mantığı ile toplu istatistiksel hesaplamalar (ortalama, medyan, standart sapma).
  5. Rastgele sayı üretimi, yeniden şekillendirme (*reshape*) ve veriyi 0–1 arasına ölçekleme (Min-Max normalizasyonu).

---

### 🐼 3. Pandas ile Veri Analizi ve Veri Ön İşleme
* 📓 **Notebook Dosyası:** [`02_pandas.ipynb`](02_pandas.ipynb)
* 🎯 **Öğrenme Hedefleri:**
  1. `Series` ve `DataFrame` veri yapılarını tanıma.
  2. Veri seti yükleme ve ilk keşifsel veri analizi komutları (`head()`, `info()`, `describe()`).
  3. `loc` / `iloc` ve mantıksal filtreler ile esnek veri seçimi.
  4. **Eksik veri doldurma/silme**, mükerrer kayıt (*duplicate*) tespiti ve hatalı veri tiplerini düzeltme.
  5. Yeni özellik türetme (*Feature Engineering*) ve tarih/zaman işlemleri.
  6. `groupby`, `pivot_table` ve `merge` ile veri gruplama, özetleme ve çoklu veri setlerini birleştirme.

---

## 💡 Nasıl Çalışılır ve Uygulama Yapılır?

1. **Google Colab ile Tarayıcıda Çalıştırma:**
   * Notebook dosyalarını (`.ipynb`) bilgisayarınıza indirip [Google Colab](https://colab.research.google.com/) üzerine yükleyerek herhangi bir kurulum yapmadan doğrudan tarayıcınızda çalıştırabilirsiniz.
2. **VS Code veya Jupyter Lab ile Yerel Kurulum:**
   * Bilgisayarınızda Python ve VS Code / Jupyter Lab kurulu ise ilgili `.ipynb` dosyasını açıp Python çekirdeğini (kernel) seçerek çalıştırabilirsiniz.
3. **Kullanım Kılavuzu:**
   * Hücreleri sırayla çalıştırmak için **`Shift + Enter`** kısayolunu kullanın.
   * Notebook'lar içerisinde yer alan **`✍️ Alıştırma`** bölümlerindeki soruları önce kendiniz çözmeye çalışın.
   * Kontrol etmek istediğinizde çözümler defterlerin en alt kısmında yer almaktadır.

---

## 🔗 Hızlı Bağlantılar

* 🏠 [Ana Depo Sayfası (README.md)](../readme.md)
* 📂 [1. Hafta: Keşifsel Veri Analizi (EDA)](../hafta1/README.md)
* 📂 [2. Hafta: Veri Hazırlama & Ön İşleme (Pestil-Köme)](../hafta2/README.md)