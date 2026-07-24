# PyTorch ile Hisse Senedi Fiyatı Tahmini 📈

Bu proje, 1 aylık Makine Öğrenimi öğrenme kampının bir parçası olarak geliştirilmiştir. Projenin amacı, geçmiş hisse senedi verilerini kullanarak gelecekteki fiyatları tahmin eden Derin Öğrenme (Deep Learning) tabanlı zaman serisi modelleri oluşturmaktır.

## Kullanılan Teknolojiler
*   **Python:** Veri analizi ve modelleme.
*   **PyTorch:** LSTM ve GRU sinir ağlarının inşası ve eğitimi.
*   **Pandas & Scikit-Learn:** Veri ön işleme, MinMaxScaler ile ölçeklendirme ve train/test ayrımı.
*   **Matplotlib:** Sonuçların ve zaman serisinin görselleştirilmesi.
*   **yfinance:** Borsa verilerinin (Amazon - AMZN) canlı olarak çekilmesi.

## Modeller ve Karşılaştırma
Projede geçmiş 20 günlük fiyat hareketlerine bakarak ertesi günü tahmin eden iki farklı model eğitilmiştir:

1.  **LSTM (Long Short-Term Memory):** Eğitim süresi ~76 saniye.
2.  **GRU (Gated Recurrent Unit):** Eğitim süresi ~45 saniye.

### Test Sonuçları (RMSE)
*   LSTM Hata Payı: **$4.23**
*   GRU Hata Payı: **$3.79**

**Sonuç:** GRU modeli daha basit mimarisi sayesinde hem daha hızlı eğitilmiş hem de test verisi üzerinde biraz daha isabetli (düşük hata payı) tahminler üretmiştir.
