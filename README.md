# AygazGoruntuIsleme

# Hayvan Sınıflandırma İçin CNN Modeli

## Proje Özeti

Bu projenin amacı, Konvolüsiyonel Sinir Ağlarının (CNN) temelini anlamak ve hayvan resimlerini sınıflandırmak için bir model oluşturmaktır. Proje, bir CNN modeli eğitme, çeşitli koşullarda test etme ve performansını analiz etmeyi kapsamaktadır. Ayrıca, görüntü manipülasyonu ve renk sabitleme gibi teknikler de uygulanmaktadır.

## Veri Seti

Bu projede kullanılan veri seti, "Animals with Attributes 2" adlı veri setidir. Veri setine Kaggle üzerinden erişebilirsiniz. 50 sınıfın bulunduğu `JPEGImages` klasöründen 10 sınıfa ait görsellerin bulunduğu klasörler belirlenir ve yalnızca seçilen sınıflara ait görüntülerin bulunduğu klasörler başka klasöre kopyalanır. Ayrıca her sınıf için yalnızca ilk 650 görüntü saklanır, bu sayede veri setinin boyutu dengelenmiş olur. Model, aşağıdaki on hayvan sınıfını sınıflandıracak şekilde tasarlanmıştır:

- Collie
- Dolphin
- Elephant
- Fox
- Moose
- Rabbit
- Sheep
- Squirrel
- Giant Panda
- Polar Bear

## Gerekli Kütüphaneler

Bu projede aşağıdaki kütüphaneler kullanılmaktadır:

- **os**: Dosya ve dizin işlemleri yapmanızı sağlar. Örneğin, dosya yolu birleştirme ve dizin listeleme.
- **shutil**: Dosya ve dizinleri kopyalamak, taşımak ve silmek için kullanılır.
- **cv2 (OpenCV)**: Görüntü işleme için kullanılır, resimleri okuma, boyutlandırma, kenar tespiti gibi işlemler yapar.
- **numpy (np)**: Matematiksel işlemler ve büyük veri setleriyle çalışmak için kullanılan bir kütüphanedir.
- **sklearn.model_selection.train_test_split**: Veriyi eğitim ve test setlerine ayırmak için kullanılır.
- **tensorflow.keras.models.Sequential**: Katmanları sırasıyla ekleyerek derin öğrenme modeli oluşturmanıza olanak tanır.
- **tensorflow.keras.layers.Conv2D**: Görüntülerdeki özellikleri öğrenmek için konvolüsyonel katman ekler.
- **tensorflow.keras.layers.MaxPooling2D**: Görüntülerin boyutlarını küçültür ve önemli özelliklerin korunmasını sağlar.
- **tensorflow.keras.layers.Flatten**: Çok boyutlu veriyi tek boyutlu hale getirir.
- **tensorflow.keras.layers.Dense**: Tam bağlantılı katman ekler ve modelin karar verme kısmını oluşturur.
- **tensorflow.keras.layers.Dropout**: Aşırı uyumu (overfitting) engellemek için bazı nöronları rastgele sıfırlar.
- **tensorflow.keras.layers.Input**: Modelin giriş boyutunu tanımlar.
- **tensorflow.keras.preprocessing.image.ImageDataGenerator**: Veri artırma (augmentation) işlemleri yaparak eğitim verisini çeşitlendirir.
- **tensorflow.keras.optimizers.Adam**: Eğitim sırasında modelin parametrelerini optimize etmek için kullanılan bir algoritmadır.
- **sklearn.metrics.classification_report**: Modelin performansını doğruluk, precision, recall gibi metriklerle özetler.
- **sklearn.metrics.confusion_matrix**: Modelin doğru ve yanlış sınıflandırmalarını görselleştiren bir matris oluşturur.
- **seaborn (sns)**: İstatistiksel veriyi görselleştirmek için kullanılan bir grafik kütüphanesidir.
- **matplotlib.pyplot (plt)**: Grafikler ve çizimler oluşturmak için kullanılan bir kütüphanedir.
- **sklearn.preprocessing.OneHotEncoder**: Kategorik verileri sayısal verilere dönüştürür, her sınıf için ikili vektörler oluşturur.

## Kurulum ve Çalıştırma

1. Gerekli kütüphaneleri yükleyin:

```bash
pip install opencv-python numpy tensorflow scikit-learn matplotlib seaborn
