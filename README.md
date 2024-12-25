# Enerji Tüketimi Takip ve Optimizasyon Sistemi

Bu proje, enerji tüketimini gerçek zamanlı olarak izlemek, analiz etmek ve optimize etmek için geliştirilmiş bir web tabanlı uygulamadır. Flask web framework'ü kullanılarak oluşturulan uygulama, enerji verilerini toplar, kullanıcıya çeşitli analizler sunar ve enerji tasarrufu için önerilerde bulunur.

---

## Özellikler

### 1. Gerçek Zamanlı Veri Toplama
- Enerji tüketim verileri 10 saniyelik aralıklarla rastgele simüle edilerek toplanır.
- Toplanan veriler bir CSV dosyasına kaydedilir.

### 2. Veri Görselleştirme
- Enerji tüketimi, zaman serisi grafikleri kullanılarak görselleştirilir.
- Kullanıcı, tüketim trendlerini kolayca analiz edebilir.

### 3. Enerji Tasarrufu Önerileri
- Yüksek enerji tüketimi tespit edildiğinde, kullanıcıya enerji tasarrufu önerileri sunulur.

### 4. Enerji Tüketimi Tahmini
- Gelecekteki enerji tüketimi, geçmiş verilere dayalı olarak lineer regresyon modeli kullanılarak tahmin edilir.

### 5. E-posta Bildirimleri
- Enerji tüketimi kullanıcı tarafından belirlenen hedefin üzerine çıktığında, e-posta bildirimi gönderilir.

### 6. Veri Filtreleme ve Karşılaştırma
- Kullanıcı, belirli bir zaman aralığında veya belirli bir enerji eşiği üzerindeki verileri filtreleyebilir.

### 7. Verilerin Dışa Aktarılması ve İçe Aktarılması
- Enerji verileri CSV formatında dışa aktarılabilir ve yeniden içe aktarılabilir.

### 8. Kullanıcı Girişi
- Oturum yönetimi desteği ile kullanıcı giriş ve çıkış işlemleri gerçekleştirilir.

---

## Kurulum

### Gerekli Bağımlılıklar
Projeyi çalıştırmak için aşağıdaki Python kütüphanelerini kurmanız gerekmektedir:

```bash
pip install flask matplotlib pandas flask-mail flask-login scikit-learn
```

### Çalıştırma
1. Uygulamayı çalıştırmadan önce Flask-Mail ayarlarını (`MAIL_USERNAME` ve `MAIL_PASSWORD`) güncelleyin.
2. Uygulamayı aşağıdaki komutla başlatın:

```bash
python app.py
```

3. Tarayıcınızda `http://127.0.0.1:5000` adresine giderek uygulamayı kullanmaya başlayabilirsiniz.

---

## Kullanım

### Ana Sayfa (Dashboard)
- Enerji tüketim verileri ve öneriler görüntülenir.
- Enerji hedefi belirlenebilir.

### Grafik Görüntüleme
- Enerji tüketimi trendleri bir grafik üzerinde görselleştirilir.

### Tasarruf İpuçları
- Yüksek tüketim noktaları için öneriler sunulur.

### Verileri Karşılaştırma
- Belirli bir zaman aralığındaki veriler karşılaştırılabilir.

### Verileri Dışa Aktar ve İçe Aktar
- Toplanan enerji verilerini CSV formatında dışa aktarabilir veya mevcut bir CSV dosyasından veri yükleyebilirsiniz.

### Enerji Tüketimi Tahmini
- Gelecekteki enerji tüketim tahminlerini görüntüleyebilirsiniz.

### E-posta Bildirimleri
- Enerji hedefi aşıldığında e-posta bildirimi alınır.

---

## Teknik Detaylar

### Enerji Tüketim Simülatörü
- Enerji tüketim verileri rastgele değerler (0.5 - 5.0 kWh) arasında simüle edilir.

### Lineer Regresyon Modeli
- Geçmiş verilere dayalı enerji tahmini yapmak için `scikit-learn` kütüphanesi kullanılır.

### Flask-Mail Entegrasyonu
- E-posta bildirimleri Gmail SMTP sunucusu kullanılarak gönderilir.

---

## Geliştirme ve Katkı
Bu projeye katkıda bulunmak isterseniz, yeni özellikler eklemek veya hataları düzeltmek için bir "pull request" gönderebilirsiniz. Her türlü geri bildirim ve öneri memnuniyetle karşılanır.

