<div align="center">

# ECOVERA
### Endüstri 5.0 Tabanlı Sürdürülebilir Akıllı Üretim Karar Destek Sistemi

**Üretim verisinden performans takibine, senaryo karşılaştırmasından iyileştirme önceliklerine.**

Rana Beyza Culus · Endüstri Mühendisliği Bitirme Projesi

`Python` · `FastAPI` · `React` · `TypeScript` · `SQLite` · `Windows`

</div>

![ECOVERA genel bakış ekranı](assets/genel-bakis.png)

## Proje hakkında

ECOVERA, enerji tüketimi, emisyon, maliyet ve operasyonel göstergeleri birlikte değerlendirerek üretimde iyileştirme önceliklerinin belirlenmesine destek olmak için geliştirdiğim uygulamadır. Çevresel, ekonomik ve operasyonel performansı SSI görünümünde birleştirir; kritik riskleri ayrıca izler ve alternatif senaryoların sonuçlarını karşılaştırır.

Endüstri mühendisliği bitirme projem kapsamında geliştirilen sistem, anonimleştirilmiş beyaz eşya yan sanayi verisiyle vaka çalışması olarak değerlendirildi ve Windows üzerinde çift tıklamayla açılabilen bir uygulama olarak paketlendi.

## Projedeki sorumluluklarım

- Enerji, emisyon, maliyet ve operasyonel performans göstergelerini karar destek modelinde yapılandırdım.
- Gösterge değerlendirmesi, SSI, kritik risk kontrolleri ve senaryo kurgularını tez çalışmasıyla ilişkilendirdim.
- Veri yükleme, hesaplama, görselleştirme ve raporlamayı tek uygulama akışında birleştirdim.
- Vaka verisiyle baz durumu ve alternatif iyileştirme senaryolarını analiz ettim.
- Çalışmayı tez dokümantasyonu, yazılım testleri ve Windows dağıtım paketiyle tamamladım.

## Uygulama akışı

CSV/Excel ile veri yüklemeden başlayan süreç; gösterge analizi, performans sınıflandırması, kritik risk kontrolü, aksiyon önerileri ve senaryo karşılaştırmasıyla ilerler. Sonuçlar dönemsel raporlarda izlenebilir.

### 1 · Göstergeler: performansın kaynağını inceleme

Gösterge analizi, çevresel, ekonomik ve operasyonel performansı oluşturan bileşenleri görünür kılar. Fayda ve maliyet yönleri farklı göstergeler ortak değerlendirme ölçeğinde izlenebilir. Böylece toplam puanın arkasındaki güçlü ve zayıf alanlar incelenir.

![Gösterge analizi — hassas değerler ve formül alanları bulanıklaştırılmıştır](assets/gosterge-analizi.png)

### 2 · SSI ve performans sınıflandırması: ortak değerlendirme

SSI ekranı; çevresel, ekonomik ve operasyonel boyut skorlarını, bileşik skoru ve ağırlık dağılımını birlikte sunar. Altın, Gümüş ve Bronz kademeleri model içindeki performans sınıflarıdır. Sosyal göstergeler ayrı bir izleme alanında sunulur.

![SSI, boyut skorları ve proje içi sınıflandırma](assets/ssi-siniflandirma.png)

### 3 · Veto ve kritik risk: toplam skordan ayrı kontrol

İyi bir toplam skorun kritik bir riski örtmesini önlemek amacıyla karbon yoğunluğu ve iş sağlığı/güvenliği koşulları ayrıca değerlendirilir. Veto durumu, eşik karşılaştırmaları ve dönemsel geçmiş aynı ekranda izlenir. Modelde veto etkinleştiğinde performans kademesi verilmez; SSI tanısal olarak gösterilmeye devam eder.

![Veto ve kritik risk izleme — sayısal değerler bulanıklaştırılmıştır](assets/veto-kritik-risk.png)

### 4 · Aksiyon reçetesi: bulgudan iyileştirme gündemine

Aksiyon reçetesi, değerlendirmede zayıf kalan alanları öncelik ve boyut etiketleriyle önerilere dönüştürür. Enerji kullanımı, maliyet bileşenleri, karbon yoğunluğu, ekipman etkinliği ve fire gibi konular için incelenebilecek iyileştirme alanlarını listeler.

Mühendis görünümünde her öneri, ilgili gösterge ve normalize skorla birlikte sunulur; böylece önceliğin gerekçesi incelenebilir.

![Mühendis görünümü: gerekçeli ve önceliklendirilmiş aksiyon önerileri — ham değerler bulanıklaştırılmıştır](assets/aksiyon-recetesi.png)

### 5 · Senaryo analizi: değişiklikleri uygulamadan önce karşılaştırma

Üretim, enerji, emisyon, maliyet ve operasyonel girdiler için varsayımsal değerler tanımlanır. Sistem baz durumu ve senaryoyu birlikte gösterir; skor değişimini, en çok iyileşen göstergeyi ve en fazla etkilenen boyutu raporlar.

![Senaryo girişleri ve sonuç karşılaştırması — ham sayısal girdiler bulanıklaştırılmıştır](assets/senaryo-sonuclari.png)

### 6 · Raporlama: dönemsel değişimi izleme

SSI ve boyut skorlarının zaman içindeki değişimi aynı raporlama ekranında izlenebilir. Grafikler, tek bir dönem sonucunun ötesinde performans eğilimini inceleme olanağı sunar. CSV dışa aktarımı ve yazdırma/PDF görünümü değerlendirmelerin paylaşılmasını destekler.

![SSI ve boyut skorlarının dönemsel eğilimleri](assets/raporlama.png)

## Teknik yapı ve doğrulama

| Katman | Teknolojiler / yaklaşım |
|---|---|
| Hesaplama ve servis | Python, FastAPI, modüler hesaplama motoru |
| Veri saklama | SQLite, SQLAlchemy |
| Arayüz | React, TypeScript, Vite |
| Test | Pytest ile motor ve API testleri |
| Masaüstü dağıtımı | PyInstaller tabanlı Windows uygulama paketi |

17 Ekim 2026 tarihli kaynak incelemesinde **201 Python testi geçti** ve arayüzün üretim derlemesi tamamlandı. Tezdeki temel baz durum ve senaryo sonuçları yeniden hesaplanarak karşılaştırıldı.

## Mevcut durum ve sonraki aşama

Mevcut sürüm, bitirme projesi kapsamında geliştirilen **çalışan Windows prototipidir**. Sonraki aşamada erişim kontrollerinin tamamlanması, dağıtım doğrulaması ve pilot kullanım değerlendirmesiyle ürünleştirmeye ilerlenmesi hedeflenmektedir.

## Paylaşım ve değerlendirme notları

- Bu depo proje tanıtımı içindir. Kaynak kod, gerçek veri seti, tez ve çalıştırılabilir paket paylaşılmaz; geliştirme kaynakları için açık kaynak lisansı verilmez.
- Görsellerde hassas ham değerler bulanıklaştırılmıştır. Normalize sonuçlar korunmuştur; dönem etiketleri farklı gösterim oturumlarına aittir.
- Senaryo sonuçları model çıktılarıdır; gerçekleşmiş tasarruf veya performans artışı iddiası değildir. Altın/Gümüş/Bronz kademeleri proje içi sınıflardır, resmi veya akredite sertifika değildir.
- Sistem karar desteği sağlar; uygulama kararı kullanıcıya aittir. Test sonuçları tüm kullanım koşullarının doğrulandığı veya ticari kullanıma hazır olunduğu anlamına gelmez.

---

**Rana Beyza Culus** · [GitHub profili](https://github.com/Beyzarana7)
