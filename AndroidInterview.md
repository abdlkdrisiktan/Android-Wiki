# Android Interview Questions

### Android Rotation Life cycle
![](/images/rotate.png)

### Android Components
Android bileşenleri şunlardır ; Activities, Services, Broadcast Receivers, Content Provider
- Activities
  - Android uygulamasının kullanıcı arayüzüyle ilgili bileşenidir. Bir uygulama tek bir aktivite içerebileceği gibi birden fazla aktivite de içerebilir. Her aktivite Activity sınıfından türetilir. Android’in yeni sürümlerinde AppCompatActivity sınıfından türetilmektedir ve bu sınıf da Activity sınıfından türetilmiştir.
- Services
  - Uygulamaların arka planda yapması gereken işlemleri yaparlar. Örneğin Apple Music uygulamasıyla bir müzik çalmaya başlayıp Whatsapp’ta arkadaşlarınızla konuşmaya devam ederken müzik çalma işini servisler halleder. Service sınıfından türetilirler.
- Broadcast Receivers
  - Sistemden ya da diğer uygulamalardan gelen mesajlara yanıt verirler. Örneğin SMS geldiğinde ya da bir indirme işlemi tamamlandığında uygulamamız bu sayede haberdar olacaktır. Eğer bankacılık uygulamaları kullanıyorsanız SMS ile gelen şifreleri bu yolla uygulamamızda otomatik olarak kullanabileceğimizi anlayabilirsiniz. BroadcastReceiver sınıfından türetilirler.
- Content Providers
  - İçerik sağlayıcılar uygulamalar arası veri iletimi için kullanılır. Whatsapp uygulaması kişi listesine içerik sağlayıcılar aracılığıyla erişiyor. ContentProvider sınıfından türetilirler.
- Fragments
  - Fragmanlar aktiviteleri modüler kullanabilmeye yardımcı olan bileşenlerdir. Alt-aktivite gibi de düşünülebilir. Her fragman kendine ait bir yaşam döngüsüne sahiptir. Aktivite kendi yaşam döngüsünde çalışırken fragman eklenebilir ve çıkarılabilir. Tek bir fragman birden çok aktivitede kullanılabilir.
- Views
  - Ekrandaki kullanıcı etkileşimiyle ilgili bütün araçlar bu bileşenler grubuna girer. Butonlar, listeler gibi.
- Intents
  - Bileşenler arası iletişimi Intents sağlar. Bir aktiviteden başka bir aktiviteye geçişe belirtebilirsiniz. Yeni bir aktivite başlatma niyetinizi bu bileşenlerle gerçekleştirirsiniz. Intent sınıfından türetilirler.
- Resources
  - Yerelleştirilecek kelimeler, resimler gibi şeyler bu grupta bulunur.
- Manifest
  - Konfigürasyon dosyası diyebiliriz. Örneğin uygulamanız internet bağlantısı istediğinde bu dosyada izin isteği bulunması gerekir.Uygulamanın kuralları ve hangi izinlere ihtiyaç duyduğu yazar yani uygulamaya girmeden hangi servislerin kullandığını ve uygulama içerisinde hangi izinlerin olacağı veya servislerin belirtildiği yerdir.


### Design Patterns in Android
bu kısmı hazırlamayı unutma
Üç parçadan oluşmaktadır paternler;
- Creational Design Patterns
### Services Overview

### RxJava neden kullanılır ? AsyncTask ile halledilemez mi ? 

### Dagger nedir ? Neden ihtiyaç duyarız ?

### Android X ile ne geldi ?

### Android Jetpack nedir ?

### Android Architecture Components nelerdir ?

### WorkManager nedir ?
