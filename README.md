# 🎬 Film Gişe Geliri Tahmini

Makine öğrenmesi modelleri kullanılarak filmlerin dünya çapındaki gişe gelirlerinin tahmin edildiği ve farklı regresyon modellerinin karşılaştırıldığı bir projedir

## Kullanılan Modeller

- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- Decision Tree
- Random Forest
- Extra Trees
- AdaBoost
- Gradient Boosting
- HistGradientBoosting

- ## Veri Seti

Bu projede Kaggle üzerindeki **TMDB Box Office Prediction** veri seti kullanılmıştır.

Veri setinde filmlere ait bütçe, süre, tür, orijinal dil, vizyon tarihi, yapım şirketleri, yapım ülkeleri, oyuncu kadrosu, ekip bilgileri ve dünya çapındaki gişe geliri gibi özellikler bulunmaktadır.

`train.csv` dosyası repository içerisine eklenmemiştir. Notebook’u çalıştırmak için veri setinin Kaggle’dan indirilerek notebook ile aynı klasöre yerleştirilmesi gerekmektedir.

- ## Proje Aşamaları

- Veri setinin incelenmesi
- Eksik ve hatalı değerlerin temizlenmesi
- Tarih bilgilerinden yeni özellikler çıkarılması
- Metin biçimindeki liste sütunlarının ayrıştırılması
- Nadir kategori değerlerinin `Other` altında birleştirilmesi
- Sayısal ve kategorik verilerin ön işlenmesi
- Zaman bazlı eğitim-test ayrımı
- Regresyon modellerinin karşılaştırılması
- Overfitting analizi
- Hiperparametre denemeleri
- Özellik önemi analizi
- Veri seti dışındaki Barbie filmi için gişe tahmini

- ## Değerlendirme Ölçütleri

Modeller aşağıdaki ölçütlere göre karşılaştırılmıştır:

- Train R²
- Test R²
- Train-Test R² farkı
- Log MAE
- Log RMSE
- Gerçek dolar cinsinden MAE
- Gerçek dolar cinsinden RMSE
- Eğitim süresi
- Tahmin süresi

- ## Proje Sonucu

Model karşılaştırmaları sonucunda Extra Trees modeli yüksek test başarısı göstermiştir. Decision Tree modeli sınırlandırılmadığında eğitim verisine aşırı uyum sağlamış, ağaç derinliği sınırlandırıldığında ise overfitting azalmıştır.

Random Forest, Extra Trees ve Gradient Boosting modellerinde yapılan hiperparametre denemeleri sonucunda daha dengeli sonuçlar elde edilmiştir. Özellik önemi analizinde bütçe, bütçe bilgisinin eksikliği, ana tür, koleksiyona ait olma durumu, ekip büyüklüğü ve vizyon dönemi öne çıkan değişkenler olmuştur.

Ayrıca veri setinde bulunmayan Barbie (2023) filmi için farklı modellerle gişe tahmini yapılmış ve tahminler filmin gerçek dünya çapındaki gişe geliriyle karşılaştırılmıştır.

## Kullanılan Teknolojiler

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
