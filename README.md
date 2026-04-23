# 📊 Müşteri Segmentasyonu ve Tahminleme Projesi

Bu proje, bir e-ticaret veri seti kullanarak müşterileri alışkanlıklarına göre segmente etmeyi ve ardından bu segmentleri yüksek doğrulukla tahmin edebilen bir makine öğrenmesi modeli oluşturmayı amaçlar.

## 🚀 Proje Özeti

Proje iki ana aşamadan oluşmaktadır:
1.  **Unsupervised Learning (Gözetimsiz Öğrenme):** RFM (Recency, Frequency, Monetary) analizi yapıldıktan sonra müşteriler **K-Means** algoritması ile 5 ana gruba ayrılmıştır.
2.  **Supervised Learning (Gözetimli Öğrenme):** Oluşturulan segmentler hedef değişken (label) kabul edilerek **XGBoost** algoritması ile eğitilmiştir. Bu sayede yeni gelen müşterilerin hangi segmente ait olduğu tahmin edilebilir hale getirilmiştir.

## 🛠️ Kullanılan Teknolojiler

* **Veri İşleme:** Pandas, NumPy
* **Görselleştirme:** Matplotlib, Seaborn
* **Makine Öğrenmesi:** Scikit-Learn, XGBoost, K-Means, PCA

## 📈 RFM Analizi ve Segmentler

Müşteriler şu üç kritere göre analiz edilmiştir:
* **Recency (Yenilik):** Müşterinin son alışverişinden bu yana geçen süre.
* **Frequency (Sıklık):** Müşterinin toplam alışveriş sayısı.
* **Monetary (Parasal Değer):** Müşterinin bıraktığı toplam ciro.

Belirlenen Müşteri Profilleri:
* 🏆 **VIP:** En çok harcama yapan ve en sık gelen grup.
* 💛 **Loyal Customer:** Düzenli alışveriş yapan sadık kitle.
* 🌱 **Promising:** Yeni gelmiş ve potansiyeli yüksek olanlar.
* 😴 **Sleeping Customer:** Bir süredir etkileşimi kesmiş grup.
* 💔 **Lost Customer:** Uzun süredir gelmeyen ve kaybedilmiş kitle.

## 🎯 Model Performansı (XGBoost)

Veri seti %80 eğitim ve %20 test olarak bölünmüştür. XGBoost modelinin test seti üzerindeki sonuçları:

* **Doğruluk Oranı (Accuracy):** %99.31
* **Hata Oranı (Error Rate):** %0.69

Modelin neredeyse kusursuz çalışması, K-Means ile yapılan segmentasyonun matematiksel olarak ne kadar tutarlı olduğunu kanıtlamaktadır.

### Hata Matrisi (Confusion Matrix)
Modelin hangi segmentleri karıştırdığını analiz etmek için kullanılan hata matrisi sonucuna göre; model sadece "Promising" ve "Sleeping" segmentleri arasındaki çok ince çizgide minimal hata yapmaktadır.

## 📁 Dosya Yapısı
* `customer-segmentation.ipynb`: Tüm analiz ve modelleme kodlarını içeren ana dosya.
* `online_retail_II.csv`: Kullanılan ham veri seti.
* `images/`: Proje grafiklerinin ve hata matrisinin bulunduğu klasör.

## 👤 İletişim

**SAMET CAN KESKİN**

[LinkedIn](https://www.linkedin.com/in/sametcankeskin0) • [GitHub](https://github.com/smtkskn)
