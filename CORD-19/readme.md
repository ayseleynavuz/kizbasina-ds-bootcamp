# 📚 CORD-19 Veri Seti Üzerine Metin Madenciliği ve Sınıflandırma Çalışması

# dataset url : https://www.kaggle.com/datasets/allen-institute-for-ai/CORD-19-research-challenge/data?select=metadata.csv

## 🎯 Amaç
Bu çalışma, COVID-19 hakkındaki bilimsel yayınlardan oluşan CORD-19 veri seti üzerinde metin madenciliği ve basit makine öğrenmesi teknikleri kullanılarak bilgi çıkarmayı ve sınıflandırma yapmayı amaçlamaktadır. Hedef, bilimsel makalelerin özetlerinden yola çıkarak, bu makalelerin aşı ("vaccine") konusuyla ilgili olup olmadığını otomatik olarak belirlemektir.

## 🛠️ Uygulanan Adımlar

1. **Veri Yükleme ve Temizleme**  
   `metadata.csv` dosyası içinden boş alanlar temizlenerek başlık ve özet verisi elde edildi.

2. **Keşifsel Veri Analizi**  
   - Yayın yıllarına göre aşıyla ilgili makaleler analiz edildi.  
   - WordCloud görselleştirmesi ile sık geçen kelimeler belirlendi.

3. **Etiketleme (Labeling)**  
   - Makale özetlerinde "vaccine" kelimesi geçiyorsa `1`, geçmiyorsa `0` etiketi verildi.

4. **TF-IDF ile Vektörleştirme**  
   - Metinler sayısal değerlere dönüştürüldü.

5. **Model Eğitimi**  
   - Lojistik regresyon modeli ile "vaccine ile ilgili mi?" sorusunu cevaplayan bir sınıflandırıcı oluşturuldu.

6. **Model Değerlendirme ve Tahmin**  
   - Model başarı oranı ölçüldü.  
   - Yeni metinlerin sınıflandırması test edildi.

## 📌 Sonuç
Bu proje ile COVID-19 literatüründeki makaleler hızlı şekilde analiz edilip, belirli konulara (örneğin aşı) odaklı sınıflandırmalar yapılabilir hale getirilmiştir. Bu, sağlık araştırmacılarının bilgiye daha hızlı ulaşmasına katkı sağlayabilir.

