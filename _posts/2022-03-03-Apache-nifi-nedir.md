---
layout: default
title:  "Apache NiFi Nedir?"
date:   2022-03-03 12:50:34 +0100
categories: Apache NiFi
---
{% seo %}
## Apache NiFi Nedir?

Apache NiFi, uçtan uca veri taşımak ve veriyi taşıma esnasında değiştirmek için kullanabileceğiniz bir Data Pipeline aracıdır. 
Apache NiFi adı, NSA (National Security Agency) de kullanılan Niagara Files programından geliyor. 2014 yılında Apache Software Foundation'a geçti.

Java tabanlı bir uygulamadır. Arka tarafında Spring Boot Framework çalışır. UI kısmında flow (akış diyagramı) tasarımı yaparsınız.
Yaptığınız akışı çalıştırır ve bir noktadan bir noktaya datanızın geçtiğini de izleyebilirsiniz. Akış sırasında bir sorun olduğun da hangi sırada sorun yaşadğınızı görebilir ve neden sorun yaşandığınızı hemen görebilirsiniz. Soruna ulaşmak oldukta kolay olup hızlıca aksiyon alabilirsiniz.

## Terminoloji 

**Processors** : Nifi de akış diyagramınızı oluşturmanız için kullanacak olduğunuz component. Veriyi bir yerden çekmenize, değiştirmenize, filtrelemenize, kayıt etmenize veya bir yere göndermenizi sağlarlar.  

**Flow File** : İşlembiler arasında datalarınız bir dosyaya yazılır bu dosyalara nifi'de flow file diyoruz.

**Processors Group** : İşlemcileri grupladığımız ayrı bir işlemci aslında kendisi

**Controller Service** : Herhangi bir servis ile konuşmak için kullanabileceğiniz servisler, veritabanı ile bağlantı yapmak ya da AWS S3 Giriş bilgilerini tutan bir servis

**Variables** : Birden fazla yerde aynı ifade kullanılacağı zaman variable eklemek işleri kolaylaştırır.

**Attributes** : Flowfile bir dosya olduğunu zaten söylemiştik. Bu flowfile'ları ayrıca attribute denilen tanımlayıcı ifadeler kullanılabilir.

**Connection** : İki işlemci ya da işlemci grubu arasındaki bağlantılara denir. Ayrıca iki işlemci arasında işlenmeyi bekleyen flowfile'ları görmemizi de sağlar.

 