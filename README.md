# Hazırlayan

**Ad Soyad:** Barış Çelikel
**Öğrenci No:** 25360859093
**Ders:** Nesneye Yönelik Programlama (NYP)

# Akıllı Şehir Lojistik ve Dağıtım Simülasyonu

Bu proje, Bursa Teknik Üniversitesi Bilgisayar Mühendisliği Bölümü, Nesneye Yönelik Programlama dersi proje ödevi kapsamında geliştirilmiştir.

Proje, bir şehrin lojistik ağını yöneten ve farklı araçlar kullanarak paket teslimat süreçlerini simüle eden Java tabanlı bir uygulamadır.

# Proje Hakkında

Bu simülasyon, müşterilere ait paketlerin belirlenen iş kurallarına göre uygun araçlarla teslim edilmesini sağlar. Sistem; müşterileri, araçları ve paketleri yöneterek gerçek hayatta karşılaşılabilecek lojistik problemlerini nesne yönelimli programlama prensipleri ile çözer.

Program, teslimat sürecini konsol üzerinden takip etmeye olanak tanır ve araçların kısıtlarına göre uygun kararlar alır.

# Özellikler

**Nesne Yönelimli Tasarım:** Kalıtım, polimorfizm, soyutlama ve kapsülleme prensipleri uygulanmıştır.

**Müşteri Yönetimi:** Müşterilerin kimlik ve konum bilgileri sistem içerisinde tutulur.

**Paket Yönetimi:** Paketlerin ağırlık, içerik ve teslimat durumları takip edilir.

**Araç Simülasyonu:** Kamyon, motosiklet ve drone olmak üzere farklı araç tipleri ile teslimatlar gerçekleştirilir.

**Yakıt Yönetimi:** Araçlar gittikleri mesafe kadar yakıt tüketir ve gerektiğinde yakıt ikmali yapar.

**Kuyruk Sistemi:** Paketler FIFO (First In First Out) mantığıyla sırayla teslim edilir.

**Hata Yönetimi:** Özel durumlar için exception yapıları ve try-catch blokları kullanılmıştır.

# Kullanılan Sınıflar

## Konum

Müşterilerin x ve y koordinat bilgilerini tutar ve iki nokta arasındaki mesafeyi hesaplar.

## Musteri

Müşterinin ad, ID ve konum bilgilerini saklar. Ayrıca müşterinin dar sokakta bulunup bulunmadığı bilgisi tutulur.

## Paket

Teslim edilecek paketlerin ağırlık, içerik ve durum bilgilerini içerir.

## Arac (Abstract)

Tüm araçların ortak özelliklerini barındıran soyut sınıftır.

Özellikleri:

* Plaka
* Kapasite
* Yakıt
* Hız

Soyut Metot:

* teslimatYap()

## Kamyon

Arac sınıfından türetilmiştir. Yüksek taşıma kapasitesine sahiptir.

## Motor

Arac sınıfından türetilmiştir. Hızlı teslimat sağlar ve belirli durumlarda hız düşüşü yaşar.

## Drone

Arac sınıfından türetilmiştir. Hafif paketlerin hızlı teslimatı için kullanılır.

## LojistikSistemi

Müşteri listesini, araç listesini ve paket kuyruğunu yönetir.

# Simülasyon Kuralları

**Kamyon Kısıtı:**
Müşterinin `darSokakMi` özelliği true ise kamyon teslimat gerçekleştiremez ve hata mesajı verir.

**Drone Kısıtı:**
Drone'lar yalnızca 5 kg altındaki paketleri taşıyabilir. Daha ağır paketlerde `AgirPaketException` fırlatılır.

**Motosiklet Kısıtı:**
Paket ağırlığı 10 kg'ın üzerindeyse motosikletin hızı %20 oranında azaltılır.

**Yakıt Yönetimi:**
Araçlar hareket ettikleri mesafe kadar yakıt tüketir. Yakıt yetersiz kaldığında `yakitIkmal()` metodu çağrılır.

**Kuyruk Mantığı:**
Paketler sisteme giriş sırasına göre FIFO mantığında işlenir ve teslim edilir.

# Teknik Detaylar

Proje geliştirilirken aşağıdaki teknik gereksinimlere uyulmuştur:

* Programlama Dili: Java
* Tüm değişken ve metot isimleri Türkçe olarak yazılmıştır.
* Hata yönetimi için try-catch blokları kullanılmıştır.
* Dış kütüphane kullanımından kaçınılmış, Java'nın standart özelliklerinden yararlanılmıştır.
* Kod okunabilirliğini artırmak amacıyla gerekli yorum satırları eklenmiştir.
* Paket kuyruğu yapısı Queue/FIFO mantığına uygun olarak tasarlanmıştır.

# Örnek Senaryo

* Sisteme müşteriler eklenir.
* Kamyon, motor ve drone araçları oluşturulur.
* Paketler kuyruğa alınır.
* Sistem sıradaki paketi uygun araca atar.
* Teslimat kuralları kontrol edilir.
* Teslimat tamamlanır veya gerekli hata mesajları gösterilir.

# Proje Dosya Adı

**NYP_Proje_Baris_Celikel_25360859093**

Bu proje, nesneye yönelik programlama kavramlarını gerçek hayattaki lojistik süreçleri üzerinde uygulamayı amaçlayan eğitim amaçlı bir simülasyon çalışmasıdır.
