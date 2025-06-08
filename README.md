# 🤟 IsaretDiliAlgilama

Bu proje, MFÖ'nün **"Ele Güne Karşı"** şarkı sözlerinin işaret dili ve ağız hareketleri ile görselleştirilmesini amaçlayan bir **makine görmesi** çalışmasıdır. Geliştirilen sistem, işaret dilini nesne tanıma yoluyla algılar ve kelime bazlı tahminlerde bulunur.

---

## 🎯 Proje Amacı

Amaç, işaret dili hareketlerini içeren bir görsel veri seti oluşturmak ve bu veriyi kullanarak nesne tespiti yoluyla işaret dilinin bilgisayar tarafından anlaşılmasını sağlamaktır.

---

## 🧠 Kullanılan Teknolojiler

- 📦 **TensorFlow 2** – Model eğitimi ve tahmin için
- 🎯 **TensorFlow Object Detection API** – Nesne tanıma mimarisi
- 🗂️ **TFRecord** – Veri seti formatı
- 🧰 **Roboflow** – Görüntü etiketleme ve veri seti yönetimi
- 🖼️ **1292 görsel** – 93 farklı kelimeye ait işaret ve ağız hareketleri

---

## 🧪 Yöntemler

1. **Veri Seti Oluşturma:**
   - MFÖ'nün "Ele Güne Karşı" şarkı sözlerindeki kelimeler için 1292 adet görsel çekildi.
   - 93 farklı işaret dili ve ağız hareketi sınıfı belirlendi.
   - Roboflow üzerinden tüm görseller manuel olarak etiketlendi.

2. **Model Eğitimi:**
   - NickNochnack'ın [Real-Time Object Detection](https://github.com/nicknochnack/RealTimeObjectDetection) reposu temel alındı.
   - Model pipeline'ı özelleştirildi (batch size, öğrenme oranı vb.)
   - Eğitim: %70 eğitim, %20 doğrulama, %10 test oranıyla bölündü.

3. **Model Testi:**
   - Örnek çıktı: “sormak” kelimesi %76 doğrulukla tahmin edildi.
   - Model temel düzeyde başarılı sonuçlar verdi.

---

## 🖥️ Kullanım

1. TensorFlow ve Object Detection API kurulumu yapılır.
2. Roboflow’dan veri indirilerek `TFRecord` formatında yerleştirilir.
3. `pipeline.config` dosyası veri yollarına göre özelleştirilir.
4. Model eğitilir ve sonuçlar analiz edilir.

---

