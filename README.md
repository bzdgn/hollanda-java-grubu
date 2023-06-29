TOC
---
- [0 Merhaba](#0-merhaba) <br/>
- [1 Grubun Amacı](#1-grubun-amacı) <br/>
- [2 Etkileşime Dair](#2-etkileşime-dair) <br/>
- [3 Proje Linkleri](#3-proje-linkleri)  <br/>
- [4 Tartışma Konuları ve Olası Proje Listesi](#4-tartışma-konuları-ve-olası-proje-listesi) <br/>


 0 Merhaba
----------
```java
System.out.println("Herkese merhaba!");
```

Bildiğiniz üzere Hollanda'da yaşayan Java kullanıcılarının toplandığı bir whatsapp grubu oluşturdum. Aklımda kabaca olana dair birkaç şey söylemek istiyorum. Yazılımcı olarak çoğu zaman çalıştığımız firmanın projelerine gömülüyoruz, ve yoğun çalışma temposu içerisinde, bu projelerin kapsamına dair library ve framework'leri kullanıyoruz. Ve çoğu zaman, kullandığımız framework ve muhteviyatındaki library'lere, zaman kısıtından ötürü yeterli vakit ayıramadan, amaçlanan işi yapacak kadar bilgi topluyoruz. Mesela basit bir web service yazarken, Spring Boot framework'ünü ve arka tarafta restful service açmamızı sağlayan bir library kullanıyoruz. Bu durumda kullandığımız framework ve library'lere dair minimal bir bilgiye sahip olmak, kabaca bir boilerplate kodu yazıp projeye hızlı bir başlangıç sağlamamızı sağlıyor. Fakat kullandığımız library'ye dair detayları, best practice'leri öğrenmek ek bir vakit gerektiriyor.

Bu durumda bir yazılımcı, Spring Boot ve altında kullandığı library için birer kitap alabilir. Kabaca 400 civarında sayfaya sahip olan iki kitabı okumak, meşakattli bir iş. Halbuki hepimiz, benzeri framework ve library'leri kullanırken farklı parçalarına dair bilgi biriktiriyoruz. İşte bu noktada bir grup kurmak, insanların daha verimli bir vakit maliyetiyle bilgi alışverişinde bulunmasını sağlıyor.

Aklımda olan ikinci şey, mimariye dair pratik bilgi paylaşımı. Vakti olan biri mimarilere dair güzel kitaplar okuyabilir, fakat kitaplardaki teorik bilgilerin uygulamaya geçmesi ayrı bir dert. Dil-agnostik bir kitap okuduğumuzda bunu Java'da uygulamak ek bir kurulum maliyeti yaratıyor. Mesela integrasyon testlerine dair bir okuma yaptığımızda, burada kullandığımız framework ve bunu kullandığımız dile dair bir bilgi verilmiyor ve her şey teorik ilerliyorsa, bu durumda teorik bilgiyi pratiğe dökmek için gene internette belirli bir vakit harcamak gerekiyor. Haliyle eğer aynı teknolojileri kullanan insanlar olarak mimarilere dair basit örnekler üretebilirsek, bu bize büyük katkı sağlayacaktır.

Son olarak, çoğumuzun client-developer olarak çalıştığını varsayıyorum. Aslında kabaca yaptığımız mevcut teknolojileri lego parçaları gibi birbirine bağlayıp, onların sağladığı servislerle müşterilere çözüm üretmek. Fakat yazılımdan keyif almamızı sağlayacak bir başka şey ise, sıfırdan bazı şeyleri inşa etmek. Bu bir veritabanı olabilir, basit bir ConnectionManager utility olabilir, bir HttpServlet uygulaması olabilir. Buna açık ve ilgili olan insanlar her zaman benimle iletişime geçebilir. Biliyorum bu, teknolojinin sürekli değiştiği ve yeni framework ve library'leri öğrenmek için koşturduğumuz bir zamanda Don Kişot'luk gibi gelebilir. Fakat öte yandan, benim gibi alaylı biriyseniz, ve kullandığınız framework'leri tune ederken aslında çoğu zaman derin bir bilgi birikimi olmadığı için, kullandığınız teknoloji size kapalı kutuda gizemli bir şeyler yapıyor gibi geliyorsa, ve proje kritik bir noktaya geldiğinde "keşke şu servisin arka tarafta nasıl çalıştığına dair biraz daha detaylı bilgiye sahip olsaydım" gibi bir huzursuzluk çöküyorsa, sıfırda bir şeyleri yazmanın maliyetine rağmen kazandıracağı birikimin değerli olduğu düşüncesine varabilirsiniz. Ben açıkçası, uzun süredir hobi olarak uğraşmak istediğim bir konuda, Java'da veritabanı yazmak için aldığım veritabanı kitabını okurken bu grubu kurmaya karar verdim.


[TOC](#toc)


 1 Grubun Amacı
---------------

Özetlemek gerekirse grubumuz şunları amaçlamaktadır;

- Library ve Framework'lere dair bilgi paylaşımı
- Mimari çözümlere dair örnekler ve bilgi paylaşımı
- Library, framework ve mimarilere dair örnek projeler
- Beraber sıfırdan yazabileceğimiz örnek projeler
- Bilgi eksiği olan grup üyelerine yardım ve bilgi paylaşımı


[TOC](#toc)


 2 Etkileşime Dair
------------------

Bugüne kadar bulunduğum irc kanalları, facebook ve diğer gruplarda gördüğüm, insanların bir grubu canlı ve sağlıklı tutması için emek harcamak gerektiği oldu. Burada önemli olan iki şey var. Bunlardan ilki iletişim mentalitesi ve kullanılan dil, ikincisi grubu aktif tutmak için gereken ortak konular bulabilmek. Her ikisi de birbirini etkiliyor, biraz tavuk/yumurta problemi gibi.

Bence kimse bir şeyi sormaktan çekinmemeli. "Şunu sorarsam senior java'cı bunu soruyor derler" gibi bir kaygı, hepimiz için sakınmamız gereken bir şey olmalı. Mesela ben ya da herhangi bir kullanıcı burada, basit bir `Map` implementasyonunun ya da `Collections`'dan herhangi bir veri yapısının nasıl kullanılabileceğini sorabilirim, bunun yadırganmaması gerektiğine inanıyorum. Çok sevdiğim bir laf var, "bildiğini sandığın şeyi öğrenemezsin". İkincisi eklemek istediğim de, çoğu zaman birinin sorduğu trivial basit bir soru bile bildiğimizi sandığımız şeyi test etmemiz için bir fırsat sunuyor. Eğer hepimiz soru sorarken, bir şeyi ön plana çıkarırken aynı rahatlıkta olursak, birbirimize bu fırsatı sunarsak, eksikliklerimizi de giderebilmemiz ve kendimizi geliştirmemiz kolaylaşır. 

Bu sebeplerle birbirimize karşı olabildiğince açık olursak ve nezakete dikkat edersek, gruptan oldukça verimli bir şekilde faydanalabiliriz. Bu kadar söz fazla bile, herkese merhaba!


[TOC](#toc)


 3 Proje Linkleri
-----------------

Grupta konuşulan her framework, library, mimari ya da konuya dair, eğer varsa boilerplate ya da örnek proje yapmanın, konuları teoriden çıkarıp pratiğe dökmenin öğrenme için faydalı olacağına inanıyorum.

Bu kısmı bu yüzden ekledim. Bir arkadaşımız OpenAPI üzerine soru sorunca, örnek bir proje gerekti. Daha sonraki konuşulan şeyler için de bu kısımdan konulara dair örnek proje linklerini buradan paylaşalım;

| library, framework ya da konu | proje linki |
| ----------------------------- | ----------- |
| OpenAPI Web Service örneği    | https://github.com/bzdgn/open-api-web-service-example/ |


[TOC](#toc)


 4 Tartışma Konuları ve Olası Proje Listesi
-------------------------------------------

Bu kısımda ileride yapılabilecek örnek proje ve tartışma konularını ekliyorum. Bu kısım oldukça genel ve jenerik olmalı;

1. Relational Database implementasyonu (https://link.springer.com/book/10.1007/978-3-030-33836-7)
2. Karmaşık SQL query'ler
3. Database'de Partition, Clustering
4. Retry Logic, HTTP requestlerde hata Exception Handling ve retry mekanizması
5. Advanced Search yani Spring Data ve Filter API
6. Hateoas'a uygun RESTful web service
7. HTTP Mock, SOAP UI, Mock Server ve bu açıdan unit/integration testler


[TOC](#toc)

