### Nifi Kurulum

Nifi kurmadan önce sisteminizde Java kurulu olması gerek. 
Bu anlatım da aşağıdaki gibi bir sistem üstüne kurulum yapılacak. 
- Ubuntu 20.04.2 LTS
- Openjdk 11.0.11

Apache Nifi 1.16.0 sürümünü [şu adresten](https://dlcdn.apache.org/nifi/1.16.0/nifi-1.16.0-bin.tar.gz) indiriyoruz. 

`wget (https://dlcdn.apache.org/nifi/1.16.0/nifi-1.16.0-bin.tar.gz -O nifi.tar.gz --show-progress`

İndirdikten sonra dosyaları çıkartıyoruz. 

`tar zxvf nifi.tar.gz`

Dosyaları çıkarttığınız dizine `nifi.1.16.0` adonda bir dizin oluşacak. Dizinin içine girerek nifi'yi çalıştırıyoruz.

`./nifi-1.16.0/bin/nifi.sh start`

Nifi'yi çalıştırdığınızda `logs` dizini oluşacak bu dizin ve altında `app, bootstrap, user, request` loglarının tutulacağı dosyalar oluşacak. Bunlardan `nifi-app.log` içinde kullanıcı adı ve parola bilgisi bulunacak bu bilgiler şuna benzer

>Generated Username [f9dd819c-8404-4499-a666-68808611a454]
Generated Password [wl8r5SFbfHAzW2WU5A2tvKYCZj+vHg4K]

Bu bilgileri kullanarak [https://localhost:8443/nifi](https://localhost:8443/nifi) adresinde oturum açabilirsiniz.

Bu kurulum nifinin en basit kurulumudur. Oturum açma yöntemi `single-user-provider` diye geçer. Bunun dışında nifi de başka oturum açma yöntemleri de vardır bunlar
- OpenLDAP
- Sertifika ile
- OpenID
- Keycloak
- Kerberos
- SAML
- Apache Knox
- JSON Web Tokens

Buradaki yöntemlerin bir çoğunun kurulumunun anlatımını ileriki zamanlarda yapacağım.