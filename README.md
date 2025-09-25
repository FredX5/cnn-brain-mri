#  Brain MRI - Tumor Detection with CNN

## Veri Seti
Bu projede, Kaggle üzerinde bulunan **Brain MRI Images for Brain Tumor Detection** veri seti kullanılmıştır. Veri setinde:
- `yes/` klasöründe tümörlü beyin MR görüntüleri
- `no/` klasöründe tümörsüz beyin MR görüntüleri
yer almaktadır.

## Kullanılan Yöntem
- Görüntüler `ImageDataGenerator` ile normalize edilip train/validation/test olarak ayrıldı.
- Basit bir **Convolutional Neural Network (CNN)** modeli tasarlandı:
  - 3 adet Conv2D + MaxPooling2D katmanı
  - Flatten + Dense katmanları
  - Çıkış katmanında `sigmoid` aktivasyonu (binary classification için)

## Metrikler
Model, 10 epoch boyunca eğitildi.  
- Eğitim doğruluğu: %XX  
- Doğrulama doğruluğu: %YY  
- Test seti doğruluğu: %ZZ  

Sonuçlar, CNN mimarisinin bu veri setinde beyin tümörlerini ayırt etmede oldukça etkili olduğunu göstermektedir.

## Ekler
- Proje içerisinde ayrıca örnek görselleştirmeler bulunmaktadır (tahmin edilen etiketler vs.).
- Gelecekte bu proje, **Streamlit** kullanılarak web arayüzü üzerinden kullanıcıların MRI yükleyip anında tahmin alabilecekleri şekilde deploy edilebilir.

## Sonuç ve Gelecek Çalışmalar
Bu çalışma, temel bir CNN modeliyle beyin tümörü tespiti yapılabileceğini göstermiştir.  
Gelecekte yapılabilecekler:
- Daha derin modeller (ResNet, EfficientNet gibi) denenebilir.
- Veri arttırma (data augmentation) yöntemleriyle performans artırılabilir.
- Model, gerçek zamanlı klinik uygulamalar için optimize edilebilir.
- Gelecek Vizyonu

Projemi, kullanıcıların kendi MR görüntülerini yükleyip modelin tahminini görebileceği bir arayüz ile geliştirmek istiyorum. Gelecekte veri toplama sürecini gerçek zamanlı hâle getirip, modeli farklı MR türleri ve nadir tümörleri tanıyacak şekilde iyileştirmeyi planlıyorum. Bu proje bootcamp sonrası da benimle kalacak ve yeni teknolojiler öğrenerek sürekli geliştirebileceğim bir temel olacak.
##Link-Kaggle
https://www.kaggle.com/code/faridjamalov/https-www-kaggle-com-code-faridjamalov-cnn-br 
