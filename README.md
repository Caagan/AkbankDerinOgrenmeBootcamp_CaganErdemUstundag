# AkbankDerinOgrenmeBootcamp_CaganErdemUstundag
Akbank Derin Öğrenme Bootcamp Projesidir. Çağan Erdem Üstündağ tarafından yapılmıştır. Veri seti olarak Kaggle üzerinden "Dogs vs. Cats" seti seçilmiştir.

# Dogs vs Cats Classification Project

## Giriş
Bu proje, **Akbank Derin Öğrenme Bootcamp: Yeni Nesil Proje Kampı** kapsamında geliştirilmiştir. Amaç, **CNN (Convolutional Neural Network)** mimarisi kullanarak köpek ve kedi resimlerini sınıflandıracak bir derin öğrenme modeli geliştirmektir.  

Proje Kaggle üzerinde geliştirilmiş ve test edilmiştir. Tüm teknik anlatımlar notebook hücrelerinde Markdown formatında verilmiştir.

**Veri Seti:**  
- [Dogs vs Cats](https://www.kaggle.com/c/dogs-vs-cats)  
- Tür: Binary Classification (2 sınıf)  
- Eğitim: ~25.000 görsel  
- Test: ~12.500 görsel  

---

## Veri Önişleme
- Görseller **rescale** edilmiştir (0-1 aralığı).  
- Veri çoğaltma (Data Augmentation) teknikleri uygulanmıştır:  
  - Rotation, Horizontal Flip, Zoom, Brightness Adjustment  
- Train-validation-test setlerine ayrım yapılmıştır (80%-20%).  
- Veri görselleştirmeleri ile sınıfların dağılımı analiz edilmiştir.  

---

## Model Geliştirme
- **CNN Mimarisi:**  
  - Convolutional Layers  
  - Max Pooling Layers  
  - Dropout ile regularization  
  - Dense Layers  
  - ReLU ve Sigmoid aktivasyon fonksiyonları  

- **Hiperparametre Optimizasyonu:**  
  - `RandomSearch` kullanılarak filtre sayısı ve learning rate optimizasyonu  
  - Epoch sayısı kısa tutulmuş, hızlı denemeler gerçekleştirilmiştir  

- **Model İzleme:**  
  - TensorBoard ile eğitim süreci izlenmiştir  

---

## Model Değerlendirme
- **Accuracy ve Loss Grafikleri:** Epoch bazında çizilmiş, overfitting kontrol edilmiştir  
- **Confusion Matrix & Classification Report:**  
  - Model her iki sınıfta da başarılı tahminler yapmıştır  
- **Grad-CAM Görselleştirme:**  
  - Modelin hangi bölgelerden etkilendiği görselleştirilmiştir  
  - Sınıflandırmada modelin odaklandığı alanlar analiz edilmiştir  

---

## Elde Edilen Sonuçlar
- **Validation Accuracy:** ~0.90  
- **Test Accuracy:** ~0.88  
- Model hem köpek hem kedi sınıflarında yüksek başarı göstermektedir  
- Overfitting gözlemlenmemiştir, dropout ve augmentation etkili olmuştur  

---

## Gelecek Çalışmalar
- Transfer Learning ile daha derin ve başarılı bir model oluşturulabilir  
- Streamlit veya Flask ile gerçek zamanlı sınıflandırma deployment yapılabilir  
- Daha fazla augmentasyon ve optimizasyon teknikleri denenebilir  
- Model interpretability artırılabilir (Grad-CAM daha detaylı uygulanabilir)  

---

## Kaggle Notebook Linki
-[https://www.kaggle.com/code/aanstnda/akbankderin-renmebootcamp-dogsvscats-a-anerdem](https://www.kaggle.com/code/aanstnda/notebookf0febd2ee0)

## Kaggle Veri Seti Linki
https://www.kaggle.com/c/dogs-vs-cats 
---

**Not:** Tüm teknik açıklamalar ve kodlar notebook hücrelerinde mevcuttur. Bu README, projenin özetini ve sonuçlarını paylaşmak amacıyla hazırlanmıştır.  

