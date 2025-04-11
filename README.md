# cifar10-transfer-learning
Bu proje, CIFAR-10 veri seti üzerinde transfer öğrenme yöntemlerini kullanarak görüntü sınıflandırma yapmayı amaçlamaktadır. Farklı derin öğrenme modelleri (VGG16, InceptionV3, ResNet50, MobileNetV2, DenseNet121) ile eğitim yapılmış ve her modelin performansı karışıklık matrisleri ile değerlendirilmiştir.

__________________________________________________________________________________________________________________________________________________________________________________________________________________

## Kullanılan Kütüphaneler

- `tensorflow`: Derin öğrenme modellerini oluşturmak için.
- `matplotlib`: Verilerin görselleştirilmesi için.
- `scikit-learn`: Makine öğrenmesi ve değerlendirme metrikleri için.

## Veri Seti

CIFAR-10, 10 farklı sınıftan oluşan 60,000 32x32 renkli görüntü içerir. Bu proje, görüntüleri 75x75 boyutuna yeniden boyutlandırarak kullanılmaktadır.

### Sınıflar

- **0:** Uçak
- **1:** Otomobil
- **2:** Kuş
- **3:** Kedi
- **4:** Kaplan
- **5:** Sırtlan
- **6:** At
- **7:** Balık
- **8:** Yılan
- **9:** İnsan

## Adımlar

1. **Veri Yükleme**
   - CIFAR-10 veri seti TensorFlow kullanılarak indirilir.

2. **Veri Ön İşleme**
   - Veriler [0, 1] aralığına ölçeklendirilir.
   - Sınıf etiketleri one-hot encode edilir.
   - Veri artırma teknikleri uygulanır.

3. **Modellerin Tanımlanması**
   - VGG16, InceptionV3, ResNet50, MobileNetV2 ve DenseNet121 gibi önceden eğitilmiş modeller kullanılır.

4. **Model Eğitimi**
   - Modeller, eğitim verisi üzerinde eğitilir. Eğitim süresi olarak 2 epoch kullanılmıştır.

5. **Tahmin Yapma**
   - Test verisi üzerinde tahminler yapılır ve sonuçlar değerlendirilir.

6. **Karışıklık Matrisi**
   - Gerçek etiketler ile tahmin edilen etiketler arasındaki ilişkiyi göstermek için karışıklık matrisleri oluşturulur ve görselleştirilir.

## Nasıl Kullanılır?

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install tensorflow matplotlib scikit-learn
