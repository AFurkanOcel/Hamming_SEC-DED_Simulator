# Hamming SEC-DED Kodlama ve Hata Düzeltme Simülatörü

Bu proje, **Hamming SEC-DED (Single Error Correction - Double Error Detection)** algoritmasını kullanarak ikili (binary) verilerin hem kodlanmasını hem de hata tespiti ve düzeltmesini gerçekleştiren bir Python Tkinter arayüz uygulamasıdır.

## 🔧 Özellikler

- Kullanıcıdan 4, 8, 16, 32 veya 64 bit uzunluğunda ikili veri girişi alınır.
- Hamming kodu (eşlik bitleriyle) oluşturulur.
- İstenilen bir bit konumunda hata simülasyonu yapılabilir (bit flip).
- Hata varsa tespit edilir, hatalı bit pozisyonu (sendrom) belirlenir ve düzeltilmiş veri gösterilir.
- Tüm işlemler kullanıcı dostu bir grafik arayüz (GUI) üzerinden yapılır.
- Tkinter kullanılarak geliştirilmiştir.

## 🖼️ Arayüzden Görüntüler

Ekran görüntüleri ve demolar buraya eklenebilir.

## 📁 Dosya Yapısı

- `hamming_sec_ded.py` — Uygulamanın ana Python dosyası (GUI ve mantık).
- `settings.ico` — Uygulama simgesi.

## 📦 Gereksinimler

- Python 3.x
- Tkinter (Python ile birlikte gelir)

## ▶️ Uygulama Nasıl Çalıştırılır?

1. Bu depoyu klonlayın:
    ```bash
    git clone https://github.com/kullaniciadi/hamming-sec-ded-simulator.git
    cd hamming-sec-ded-simulator
    ```

2. Uygulamayı başlatın:
    ```bash
    python main.py
    ```

## 📌 Notlar

- Şu anki sürümde veriler yalnızca **RAM** üzerinde tutulur. İstenirse kalıcı dosya kaydı (loglama, CSV’ye veri yazımı vs.) kolayca entegre edilebilir.
- Uygulama, eğitim amaçlı veya hata düzeltme algoritmalarını görselleştirmek isteyen öğrenciler için uygundur.

## 📜 Lisans

Bu proje MIT lisansı ile lisanslanmıştır. Ayrıntılar için `LICENSE` dosyasına bakabilirsiniz.

