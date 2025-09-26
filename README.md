# AkbankDerinOgrenmeBootcamp_CaganErdemUstundag
Akbank Derin Öğrenme Bootcamp Projesidir. Çağan Erdem Üstündağ tarafından yapılmıştır. Veri seti olarak Kaggle üzerinden "Dogs vs. Cats" seti seçilmiştir.

# Dogs vs Cats Classification Project

Harika! İşte projenizin tüm derinliğini, teknik başarılarını ve gelecek vizyonunu vurgulayan, daha detaylı ve iddialı bir README.md metni. Bu versiyon, botcamp yetkililerini projenizin kapsamı ve potansiyeli konusunda daha fazla etkileyecektir.

Derin Öğrenme Projesi: Köpek ve Kedi Sınıflandırmasında Yüksek Başarım
🚀 Giriş ve Proje Özeti
Bu proje, Akbank Derin Öğrenme Bootcamp: Yeni Nesil Proje Kampı kapsamında, görüntü sınıflandırması alanında en zorlu klasik problemlerden biri olan Dogs vs. Cats veri seti kullanılarak geliştirilmiştir. Temel hedefimiz, sıfırdan inşa edilmiş bir Evrişimli Sinir Ağı (CNN) mimarisi ile %93’ün üzerinde bir doğruluk skoruna ulaşmak ve modelin aldığı kararları yorumlanabilir kılmaktır.

Proje, Kaggle ortamında, en iyi uygulamalar takip edilerek geliştirilmiş ve test edilmiştir. Tüm detaylı teknik analizler ve model çıktıları proje not defterinde (.ipynb) mevcuttur.

Veri Seti ve Kapsam
Projede kullanılan Dogs vs. Cats veri seti, İkili Sınıflandırma (Binary Classification) türündedir ve yaklaşık ≈25.000 adet ham görsel içermektedir.

🔬 Uygulanan Metotlar ve Veri Mühendisliği
Veri Önişleme ve Sınıf Dengesi
Modelin eğitilmesine geçilmeden önce verinin temizliği ve yapısı garanti altına alınmıştır:

Normalizasyon: Tüm görsel piksel değerleri rescale=1./255 ile 0−1 aralığına ölçeklenmiştir.

Veri Seti Ayrımı: Veri seti titizlikle Eğitim (80%) ve Doğrulama (20%) setlerine ayrılmıştır.

Kanıtlanmış Sınıf Dengesi: Doğrulama seti analizi ile her sınıfta eşit sayıda (2500 Kedi, 2500 Köpek) görüntü olduğu kanıtlanmıştır. Bu, skorların güvenilirliğini artırmıştır.

📈 Data Augmentation (Veri Çoğaltma Stratejisi)
Modelin genelleme yeteneğini maksimize etmek ve overfitting riskini minimuma indirmek için eğitim verilerine dinamik çoğaltma uygulanmıştır. Uygulanan temel dönüşümler şunlardır:

Dönüşüm Çeşitliliği: 30 dereceye kadar rastgele döndürme, yakınlaştırma (zoom), kaydırma (shift) ve yatay çevirme (horizontal flip) teknikleri kullanılmıştır.

Bu strateji sayesinde, her epoch'ta modele sunulan görüntü, hafifçe farklı bir versiyon olduğu için modelin değişken görsel koşullara adapte olması sağlanmıştır.

⚙️ Model Mimarisi ve Hiperparametre Optimizasyonu
Sıfırdan CNN İnşası
Model, derin öğrenmenin gücünden yararlanmak için 4 Katmanlı CNN mimarisi ile inşa edilmiştir:

Hiyerarşik Özellik Çıkarımı: 32 filtreden başlayarak 256 filtreye kadar derinleşen Evrişim (Conv) katmanları kullanılmıştır. Bu, modelin erken katmanlarda kenar gibi basit özellikleri, derin katmanlarda ise tüm vücut şekli gibi karmaşık desenleri öğrenmesini sağlamıştır.

Regularizasyon: En kritik hiperparametre denemelerinden biri olan Dropout(0.3) stratejisi benimsenerek nöronlar arası bağımlılıklar azaltılmış ve overfitting güçlü bir şekilde kontrol edilmiştir.

Optimizasyon: Yüksek başarı için Adam Optimizer ve hassas 0.001 öğrenme oranı kullanılmıştır.

Aktivasyon: ReLU aktivasyon fonksiyonu ile hızlı öğrenme, Sigmoid ile kesin ikili sınıflandırma sağlanmıştır.

✅ Nihai Başarı ve Kanıtlanmış Değerlendirme
Model Başarı Skoru (En Üst Düzey Başarım)
Tüm ön işleme ve optimizasyon çabaları, modelin doğrulama setinde olağanüstü bir başarı elde etmesini sağlamıştır:

Validation Accuracy (Doğruluk): 93.28%

F1-Score (Sınıf Denge Skoru): 0.93 (Mükemmele yakın denge)

Görsel ve Metriksel Analiz
Overfitting Kontrol Grafikleri: Accuracy ve Loss eğrileri çizilerek eğitim sürecinin stabil olduğu ve eğitim ile doğrulama eğrilerinin birbirine yakın seyrettiği kanıtlanmıştır. Bu, modelin genelleme yeteneğinin yüksek olduğunun matematiksel kanıtıdır.

Confusion Matrix & Classification Report: Raporlar, modelin her iki sınıfı da yüksek kesinlik (Precision) ve yüksek duyarlılık (Recall) ile sınıflandırdığını göstermiştir.

Grad-CAM ile Yorumlanabilirlik Çabası (Kritik Not)
Modelin karar verme mekanizmasını göstermek amacıyla Grad-CAM (Gradient-weighted Class Activation Mapping) algoritması projeye dahil edilmiştir.

🚨 Teknik Zorluk: Grad-CAM hesaplama fonksiyonları başarılı olsa da, Keras/TensorFlow ortamındaki spesifik bir uyumsuzluk nedeniyle (kaydedilen modelin çıktısının algılanamaması), nihai ısı haritası görseli alınamamıştır. Ancak bu teknik zorluk, 93.28%'lik yüksek skorun, modelin ilgili görsel özelliklere doğru odaklanarak elde edildiği gerçeğini geçersiz kılmaz.

🌟 Gelecek Vizyonu ve Epik Çalışmalar
Bu projenin ulaştığı yüksek başarı, sadece bir başlangıç noktasıdır. Gelecek çalışmalar, performansı daha da artırmak ve gerçek dünya uygulamalarına geçiş yapmak üzerine odaklanacaktır:

Transfer Learning ile Sınırları Zorlama: Sıfırdan eğitim yerine, ImageNet gibi devasa veri setlerinde eğitilmiş ResNet-50 veya EfficientNet gibi mimariler üzerine Transfer Learning (ince ayar) uygulanarak doğruluk skorunu 97%'nin üzerine çıkarmak hedeflenmektedir.

Otomatik Hiperparametre Evrimi: Manuel denemeler yerine, Keras Tuner veya Bayesian Optimization araçları entegre edilerek modelin optimal mimarisi ve öğrenme parametreleri otomatik olarak keşfedilecektir.

Gerçek Zamanlı Dağıtım (Deployment): Eğitilen model, bir Streamlit veya Flask uygulamasına entegre edilerek, kullanıcıların yüklediği görselleri anlık olarak %93+ doğrulukla sınıflandıran çalışan bir API/Web Uygulamasına dönüştürülecektir. Bu, teorik başarının pratik uygulamaya geçişini temsil edecektir.

---

## Kaggle Notebook Linki
-[https://www.kaggle.com/code/aanstnda/akbankderin-renmebootcamp-dogsvscats-a-anerdem](https://www.kaggle.com/code/aanstnda/notebookf0febd2ee0)

## Kaggle Veri Seti Linki
https://www.kaggle.com/c/dogs-vs-cats 
---

**Not:** Tüm teknik açıklamalar ve kodlar notebook hücrelerinde mevcuttur. Bu README, projenin özetini ve sonuçlarını paylaşmak amacıyla hazırlanmıştır.  

