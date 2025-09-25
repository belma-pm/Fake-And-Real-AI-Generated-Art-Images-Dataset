# 🎨 CNN ile Yapay Zeka (AI) Sanat Eseri Tespiti (Global AI Hub Bootcamp Projesi)

Bu repo, Global AI Hub bootcamplerinde template olarak kullanılan formatta hazırlanmıştır ve projemin tüm kaynaklarını içermektedir. Proje, Gerçek sanat eserleri ile Yapay Zeka (AI) tarafından üretilen eserleri Konvolüsyonel Sinir Ağları (CNN) kullanarak ayırt etmeyi amaçlamaktadır.

---

## Giriş

Bu projede, derin öğrenme alanında görüntü sınıflandırması, model geliştirme, hiperparametre optimizasyonu ve **Açıklanabilir Yapay Zeka (XAI)** konularında pratik deneyim kazanılmıştır.

**Seçilen Veri Seti:** Real and Fake AI Generated Art Images Dataset.

**Kullanılan Algoritma:** Yüksek performanslı bir CNN (Convolutional Neural Network) mimarisi.

Projenin tüm teknik detayları, kodları ve analizleri, **adım adım açıklamalı Markdown hücreleri** ile zenginleştirilmiş `supervised.ipynb` dosyamızda mevcuttur. Sadece kod çıktılarına değil, metodoloji ve yorumlamaya da geniş yer verilmiştir.

---

## Metrikler ve Model Yorumu

Projemiz, uygulanan **Hiperparametre Optimizasyonu** sayesinde başlangıçtaki aşırı öğrenme (overfitting) sorununu tamamen çözerek {93\%} doğruluk oranına ulaşmıştır.

### Elde Edilen Nihai Sonuçlar

| Metrik | Sonuç | Yorum |

| **Doğruluk (Accuracy)** | {93\%} | Proje hedefini aşan, çok güçlü bir sonuçtur. |
| **FAKE Recall** | $\mathbf{94\%}$ | Modelin, AI tarafından üretilen sahte eserleri tespit etmedeki başarısı. (En kritik metrik) |

### Confusion Matrix ve Yorumlama

| Gerçek Sınıf \ Tahmin | FAKE (0) | REAL (1) |

| **FAKE (0)** | $\mathbf{2026}$ (Doğru) | $138$ (Hata) |
| **REAL (1)** | $154$ (Hata) | $\mathbf{2010}$ (Doğru) |

* **Yorum:** Model, toplam $\mathbf{4328}$ doğrulama örneğinden sadece $\mathbf{292}$ tanesinde hata yapmıştır. $\mathbf{94\%}$ FAKE Recall değeri, modelin **sahte sanat eserlerini çok güvenilir bir şekilde** ayırt ettiğini kanıtlar.

### Grad-CAM Analizi (Açıklanabilirlik)

Modelin karar verme süreci, **Grad-CAM (Gradient-weighted Class Activation Mapping)** ile şeffaflaştırılmıştır.

* **FAKE Görseller:** Model, AI tarafından üretilen görsellerde genellikle **tutarsız dokusal desenlere ve keskin olmayan kenar geçişlerine** odaklanmıştır.
* **REAL Görseller:** Model, gerçek resimlerdeki **organik fırça darbelerine ve ince sanatsal detaylara** odaklanarak karar vermiştir.

Bu analiz, modelin tahminlerini "anladığını" ve sadece rastgele desenlere güvenmediğini göstermektedir.

---

## Sonuç ve Gelecek Çalışmalar

Yaptığımız bu çalışma ile, hızlı gelişen yapay zeka sanat dünyasında güçlü bir temel oluşturulmuştur.

**Gelecek Çalışmalar ve İyileştirmeler:**

1.  **Arayüz (UI) Geliştirme:** Projeyi Streamlit veya Flask kullanarak basit bir web arayüzüne taşımak (Örnek UI klasörünü kullanarak). Kullanıcının yüklediği görselin anında REAL/FAKE tespiti yapılabilmelidir.
2.  **Transfer Learning:** Model başarısını daha da artırmak için VGG16 veya ResNet gibi önceden eğitilmiş mimarilerle (Transfer Learning) denemeler yapmak.
3.  **Dinamik Veri Toplama:** Yeni çıkan AI modellerinin (DALL-E 3, Midjourney v7) çıktılarını düzenli olarak toplayıp modeli dinamik olarak güncellemek.

Bu proje, kariyer yolumda Derin Öğrenme ve Yapay Zeka alanlarına odaklanma isteğimi pekiştirmiştir.

---

## Linkler

Çalışmama ait tüm Kaggle linkleri aşağıdadır:

https://www.kaggle.com/code/belmatas/fake-and-real-ai-generated-art-images-dataset/edit

