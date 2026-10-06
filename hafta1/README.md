# 1. Hafta: Veri Setlerini Tanıma ve Keşifsel Veri Analizi (EDA)

Bu klasör, **YBS 301 Veri Madenciliği** dersinin 1. haftasına ait teorik ders materyallerini ve laboratuvar çalışma notlarını içermektedir.

---

## 📌 Hafta İçeriği & Materyaller

* 📑 **Ders Sunumu:** [ders1.pptx](ders1.pptx)


---

## 💡 Veriyi Anlamak, Çözümün Yarısıdır

Veri madenciliği sürecine başlarken ilk aşama, üzerinde çalışılan veriyi her yönüyle tanımak, boyutlarını, tiplerini, eksikliklerini ve dağılımını kavramaktır. Bu rehberde temel benchmark veri setlerinin yükleniş kodlarını ve inceleme kontrol adımlarını bulabilirsiniz.

---

## 📊 İncelenecek 7 Temel Veri Seti

Veri madenciliği uygulamalarında ve literatürde sıklıkla kullanılan 7 temel veri seti:

| Veri Seti | Veri Tipi / Kategorisi | Satır & Sütun | Açıklama |
| :--- | :--- | :--- | :--- |
| 🌸 **Iris** | Klasik Tablo / Sınıflandırma | 150 örnek, 4 nitelik | Çiçek türlerini (3 sınıf) sınıflandırmak için en bilinen başlangıç seti. |
| 🍷 **Wine** | Klasik Tablo / Sınıflandırma | 178 örnek, 13 nitelik | Kimyasal analiz özellikleri ile 3 farklı şarap üreticisini tahmin eder. |
| 🎗️ **Breast Cancer** | İkili Sınıflandırma | 569 örnek, 30 nitelik | Tümörün iyi (benign) ya da kötü (malignant) huylu oluşunun tespiti. |
| 🏡 **California Housing** | Regresyon | 20.640 blok grubu | Medyan konut fiyat tahmini için sürekli hedef değişkenli veri seti. |
| 🚢 **Titanic** | Karmaşık & Eksik Veri | Yolcu profilleri | Yaş/kabin eksik değerleri, kategorik ve sayısal karışık nitelikler. |
| 🔢 **MNIST 784** | Görüntü İşleme | 70.000 örnek (28x28 piksel) | El yazısı rakam matrisi (784 piksel özelliği). |
| 📰 **20 Newsgroups** | Metin / NLP | Binlerce haber iletisi | Ham metinlerin vektörleştirilmesi ve konu modelleme çalışmaları. |

---

## 💻 Python ile Veri Setlerini Yükleme Kodları

Aşağıdaki Python kod bloğu ile `scikit-learn` ve `OpenML` kütüphaneleri üzerinden veri setlerini doğrudan kodunuza aktarabilirsiniz:

```python
from sklearn.datasets import (
    load_iris,
    load_wine,
    load_breast_cancer,
    fetch_california_housing,
    fetch_openml,
    fetch_20newsgroups
)

# 1. Klasik Tablo (Paketle birlikte hazır gelir, internet gerekmez)
iris = load_iris(as_frame=True)
X_iris, y_iris = iris.data, iris.target

wine = load_wine(as_frame=True)
cancer = load_breast_cancer(as_frame=True)

# 2. Regresyon: California Housing (İlk çağrıda arka planda indirir ve önbelleğe alır)
housing = fetch_california_housing(as_frame=True)
X_house, y_house = housing.data, housing.target

# 3. Titanic (OpenML üzerinden tek satırda çekilir)
titanic = fetch_openml('titanic', version=1, as_frame=True)
X_titanic, y_titanic = titanic.data, titanic.target

# 4. Görüntü: MNIST 784 (OpenML üzerinden çekilir, ~70.000 satır 28x28 piksel)
mnist = fetch_openml('mnist_784', version=1, as_frame=False)
X_mnist, y_mnist = mnist.data, mnist.target

# 5. Metin / NLP: 20 Newsgroups (Sadece belirli kategorileri çekmek için)
categories = ['alt.atheism', 'soc.religion.christian', 'comp.graphics', 'sci.med']
newsgroups = fetch_20newsgroups(subset='train', categories=categories, shuffle=True, random_state=42)
text_data, text_labels = newsgroups.data, newsgroups.target
```

---

## 📋 Veri Setini Tanı: Keşif Kontrol Listesi (EDA Checklist)

Her bir veri seti üzerinde çalışırken aşağıdaki 12 temel sorunun yanıtını belirleyin:

| # | Kontrol Sorusu | Python (Pandas) Karşılığı | Açıklama / İpucu |
| :-: | :--- | :--- | :--- |
| **01** | Veri setinde kaç gözlem var? | `df.shape[0]` veya `len(df)` | Toplam satır sayısı |
| **02** | Kaç özellik (sütun) var? | `df.shape[1]` veya `len(df.columns)` | Nitelik sayısı |
| **03** | Özelliklerin isimleri neler? | `list(df.columns)` | Kolon başlıkları |
| **04** | Hangi özellikler sayısal? | `df.select_dtypes(include='number')` | `int64`, `float64` veriler |
| **05** | Kategorik özellik var mı? | `df.select_dtypes(include=['object', 'category'])` | Metinsel / sınıfsal veriler |
| **06** | Eksik veri var mı? | `df.isnull().sum()` | Sütun bazlı eksik (NaN) sayıları |
| **07** | Hedef değişken nedir? | `y` (bağımlı değişken) | Tahmin edilmek istenen sütun |
| **08** | Hedef değişken kaç farklı değer alıyor? | `y.nunique()` / `y.unique()` | Sınıf / değer çeşitliliği |
| **09** | Sınıflar dengeli mi? | `y.value_counts(normalize=True)` | Sınıf dağılım oranları (%) |
| **10** | Özelliklerin değer aralıkları benzer mi? | `df.describe().T[['min', 'max']]` | Ölçekleme (scaling) ihtiyacı |
| **11** | En yüksek korelasyona sahip iki özellik hangileri? | `df.corr().abs()` | Bağımsız değişkenler arası ilişki |
| **12** | Dikkatinizi çeken bir anormallik var mı? | EDA gözlemi | Aykırı değerler, sıfır yoğunluğu vb. |

> [!IMPORTANT]
> **Ve son olarak kendinize sorun:**  
> *“Bu veri setinden hangi sorulara cevap vermeye çalışabiliriz?”*  
> Model kurmadan önce iş problemini ve hedefini formüle edin (sınıflandırma, regresyon, kümeleme veya anomali tespiti).
