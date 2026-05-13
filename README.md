# VERI-MADENCILIGI-DERSI-DONEM-ODEVI-
VERİ MADENCİLİĞİ DERSİ DÖNEM ÖDEVİ Konu: Telco Müşteri Kaybı (Churn) Analizi ve Tahminleme Araç: Orange Data Mining Tool
# VER-MADENC-L-DERS-D-NEM-DEV-
VERİ MADENCİLİĞİ DERSİ DÖNEM ÖDEVİ Konu: Telco Müşteri Kaybı (Churn) Analizi ve Tahminleme Araç: Orange Data Mining Tool
Telco Müşteri Kaybı (Churn) Analizi ve Tahminleme
Bu proje, veri madenciliği tekniklerini kullanarak telekomünikasyon sektöründeki müşteri terk (churn) oranlarını analiz 
etmek ve tahmin modelleri geliştirmek amacıyla hazırlanmıştır. Analiz süreci için Orange Data Mining aracı kullanılmıştır.

🛠 Kullanılan Araçlar ve Veri Seti
Araç: Orange Data Mining Tool

Veri Seti: Telco Customer Churn Dataset

Yöntem: Veri Ön İşleme (Preprocessing), Keşifçi Veri Analizi (EDA) ve Sınıflandırma Modelleri.

📊 KISIM 1: Veriyi Tanıma ve Hazırlama (Preprocessing & EDA)
1. Veri Denetimi ve Temizlik
Veri setindeki TotalCharges sütununun başlangıçta metin (text) olarak algılandığı tespit edilmiştir. Bunun sebebi, eksik verilerin " " (boşluk) veya ? şeklinde girilmiş olmasıdır.

Çözüm: Edit Domain widget'ı ile sütun tipi Numeric olarak zorlanmış, boş kalan alanlar Impute widget'ı kullanılarak ortalama (mean) değerler ile doldurulmuştur.

Sütun Seçimi: Tahminleme için istatistiksel bir anlam ifade etmeyen customerID sütunu devre dışı bırakılmıştır.

2. Görsel Analiz (EDA)
Sözleşme Tipi (Contract) Etkisi: Analiz sonuçlarına göre en riskli grup Aylık (Month-to-month) sözleşme yapan müşterilerdir. İki yıllık sözleşme yapanlarda kayıp oranı %2.83'e kadar düşmektedir.

Fatura ve Sadakat İlişkisi (Scatter Plot): En yüksek riskli bölgenin, şirketteki süresi kısa (tenure < 20 ay) ve aylık ödemesi yüksek (MonthlyCharges > 70) olan müşteriler olduğu gözlemlenmiştir.

🤖 KISIM 2: Tahminleme ve Model Değerlendirme
1. Modelleme Süreci
Veri seti %80 Eğitim ve %20 Test olarak ayrılmıştır. Aşağıdaki üç farklı algoritma eğitilmiştir:

Lojistik Regresyon (Logistic Regression)

Karar Ağacı (Decision Tree)

Rastgele Orman (Random Forest)


3. Karar Ağacı Analizi ve Risk Profili
Modelin "aşırı öğrenmesini" (overfitting) engellemek için ağaç derinliği 3 ile sınırlandırılmıştır (Pruning).

Şirket İçin En Riskli Müşteri Profili:

Sözleşme: Aylık (Month-to-month)

İnternet: Fiber Optik

Kıdem (Tenure): 15 ay ve altı

Bu gruptaki müşterilerin terk etme olasılığı %69 olarak saptanmıştır.


📁 Proje İçeriği
telco_churn_analysis.ows: Orange Workflow proje dosyası.

screenshots/: Analiz sırasında alınan grafik ve workflow ekran görüntüleri.

🚀 Nasıl Çalıştırılır?
Bilgisayarınıza Orange Data Mining indirin ve kurun.

Repo içerisindeki .ows dosyasını Orange ile açın.

Veri seti yolunu kendi bilgisayarınıza göre güncelleyerek akışı çalıştırın.


Hazırlayanlar
Zeliha Reis - 446754
Ceyda Gedikli- 446748
