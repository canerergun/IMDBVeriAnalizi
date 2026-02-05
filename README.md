# 🎬 IMDb Veri Analizi Projesi (Büyük Veri İşleme)

Bu proje, IMDb'nin milyonlarca satırlık devasa veri setlerini kullanarak film ve dizi dünyasına dair derinlemesine bir analiz sunar. Yaklaşık **12.2 milyon satırlık** bir veri seti üzerinde temizleme, filtreleme ve görselleştirme teknikleri uygulanmıştır.

## 📌 Projenin Amacı
Büyük çaplı bir veri setini (GB boyutunda) yerel bir makinede verimli bir şekilde işleyerek; içerik türleri, yıllara göre üretim trendleri ve popüler tür kombinasyonları gibi sektörsel trendleri ortaya çıkarmak.

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler
Proje, Python veri bilimi ekosisteminin en güçlü araçları kullanılarak geliştirilmiştir:
- **Pandas:** GB boyutundaki `.tsv.gz` dosyalarının okunması ve manipülasyonu.
- **NumPy:** Sayısal veri işleme ve eksik değer yönetimi.
- **Matplotlib & Seaborn:** Veri setinin hikayeleştirilmesi ve görselleştirilmesi.
- **Datetime:** Zaman tabanlı trend analizleri.

## 📂 Veri Seti Hakkında
Analizlerde IMDb'nin resmi `title.basics.tsv.gz` veri seti kullanılmıştır.
- **Veri Boyutu:** Yaklaşık 12,265,715 satır.
- **Sütunlar:** `tconst`, `titleType`, `primaryTitle`, `isAdult`, `startYear`, `runtimeMinutes`, `genres` vb.

## 🚀 Yapılan Analiz ve İşlemler
1. **Veri Temizleme:** IMDb'ye özgü `\N` ifadeleri temizlenmiş, hatalı yıl ve süre verileri mantıksal filtrelere tabi tutulmuştur.
2. **İçerik Dağılımı:** Toplam içeriğin %75.9'unun "TV Episode" olduğu ve dizi sektörünün büyüklüğü tespit edilmiştir.
3. **Zaman Analizi:** 1900'den günümüze içerik üretim hızı incelenmiş, 2021 yılının veri setindeki en üretken yıl olduğu saptanmıştır.
4. **Süre Analizi:** İçeriklerin ortalama süresi (45.2 dk) ve sürelere göre kategorizasyon yapılmıştır.
5. **Tür (Genre) Analizi:** En çok üretilen türlerin başında Drama, Belgesel ve Komedi'nin geldiği görülmüştür.

## 📊 Öne Çıkan Bulgular
- **Üretim Patlaması:** Özellikle 2010 sonrası içerik üretiminde eksponansiyel bir artış gözlemlenmiştir.
- **Eksik Veri Analizi:** Veri setindeki içeriklerin yaklaşık %64'ünde süre bilgisinin eksik olduğu görülmüş, analizler mevcut veriler üzerinden normalize edilmiştir.
- **Tür Dağılımı:** Tek başına türlerin yanı sıra karmaşık tür yapılarının dağılımı listelenmiştir.

## 🎯 Gelecek Çalışmalar İçin Öneriler
- [ ] `title.ratings.tsv` dosyası ile birleştirilerek başarı (puan) analizi yapılması.
- [ ] Türler arası korelasyonun (Hangi türler genelde beraber bulunur?) incelenmesi.
- [ ] NLP (Doğal Dil İşleme) teknikleri ile popüler film isimlerindeki anahtar kelime analizi.

## ⚙️ Kurulum
Bu projeyi yerelinizde çalıştırmak için:
1. Depoyu klonlayın: `git clone https://github.com/canerergun/IMDBVeriAnalizi.git`
2. Gerekli kütüphaneleri yükleyin: `pip install pandas numpy matplotlib seaborn`
3. Jupyter Notebook'u açın ve `IMDBVeriAnalizi.ipynb` dosyasını çalıştırın.

---
⭐ **Not:** Bu proje, büyük veri setleri ile Python üzerinde veri temizleme ve görselleştirme yetkinliklerini pekiştirmek amacıyla geliştirilmiştir.
