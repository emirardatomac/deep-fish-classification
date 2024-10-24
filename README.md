# Balık Türleri Sınıflandırma Projesi

Bu proje Akbank Derin Öğrenme Proje Kampı dahilinde, derin öğrenme (Deep Learning) tekniklerini kullanarak farklı balık türlerini görüntüler üzerinden sınıflandırmayı hedeflemektedir. TensorFlow ve Keras kütüphaneleri ile yapay sinir ağı (ANN) modeli oluşturulmuştur.

## İçerik

- [Veri Seti](#veri-seti)
- [Proje Yapısı](#proje-yapısı)
- [Model Mimarisi](#model-mimarisi)
- [Sonuçlar](#sonuçlar)
-[Kaggle Linki](#kaggle-linki)

## Veri Seti

Bu proje, Kaggle üzerinde bulunan **A Large-Scale Fish Dataset** veri setini kullanmaktadır. Veri seti 9 farklı balık türüne ait binlerce görüntüden oluşmaktadır.

- **Veri seti linki**: [Kaggle: Fish Dataset](https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset)

## Proje Yapısı

- **data/**: Balık türü görüntüleri.
- **notebooks/**: Eğitim ve test süreçlerinin yapıldığı Jupyter notebook'ları.
- **models/**: Eğitilmiş model dosyaları.
- **README.md**: Proje ile ilgili genel bilgi ve kullanım yönergeleri.

## Model Mimarisi

Modelimiz aşağıdaki bileşenlerden oluşmaktadır:

- **Giriş Katmanı**: Görüntü boyutu (128x128x3)
- **Ara Katmanlar**:
  - Fully connected katmanlar (512, 256, 128 nöron)
  - Dropout ile overfitting’i önleme
  - Batch normalization
- **Çıkış Katmanı**: Softmax aktivasyonu ile 9 sınıflı tahmin.

## Sonuçlar

Model, test verisi üzerinde %94 doğruluk oranı elde etmiştir. Performansı artırmak için erken durdurma ve öğrenme oranı azaltma teknikleri uygulanmıştır.

## Kaggle Linki

https://www.kaggle.com/code/emirardatomac/akbank-dl-ann-project/notebook
