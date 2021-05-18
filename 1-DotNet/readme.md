# .Net Framework Notları
## .Net'de Derleme İşlemi
.Net Framework'de kod iki kez derlenir. İlk derlemede kaynak kodu Language Compiler (C# için C Sharp Compiler-CSC) ile derlenir. Çıkan sonuç ise Microsoft Intermediate Language(MSIL), Intermediate Language Code (IL) ya da Managed Code olarak adlandırılır. Bu çıkan sonuç derlenmiş kod olsada ara bir katman olduğundan işletim sistemi tarafından çalıştırılamaz.

Buradan sonuçla derlenmiş bu kodun işletim sisteminde çalıştırılabilmesi için gerek duyduğu yapı CLR'dır. İkinci derlemede ise CLR kullanılanarak MSIL native code'a çevrilir. Yani MSIL/IL/Managed Code' un çalıştırılımasından sorumludur. CLR kodu alır ve JIT'e gönderir. **JIT Compiler** CLR'in parçası olup MSIL -> Native Code çevriminden sorumludur. Tüm satırları okuyup derleyerek işletim sisteminin çalıştırabileceği Native Code'a çevirir.

### Neden İki Aşamalı Bir Derlemeye İhtiyaç Duyuldu?
Bunun nedeni tek bir derleme ile yapılmış olduğunu varsaysak yazdığımız programın hangi ortamda(Windows 7-8-10-Server vs) çalışacağını bilmiyoruz. Ayrıca yine çalışacak ortamdaki konfigurasyonları, güvenlik ayarlarını vs. bilmiyoruz. Bunun için ara bir derleme yolu seçilmiştir. CLR'da bu IL kodunu gerekli konfigurasyon,ayarlar vs. e göre son derleme işlemini yapıyor. CLR in bu aşamada sorumlu olduğu bir çok nokta vardır. Bunlar: 
- Security Manager
- JIT Compiler
- Garbage Collector
- Exception Manager
- Common Language Specification(CLS)
- Common Type System (CTS)
### Security Manager
Burada iki komponent, Code Access Security(CAS) ve Code Verification(CV), mevcut user'ın Assembly'e erişimi olup olmadığını kontrol eder. Ayrıca CLR Security Manager işleminde kodun sahip olduğu haklar ve otoritelere bakar, kodun işletim sistemi için güvenli olduğunu kontrol eder.
# C# Exception

Programlar çalışırken bazı hatalar ile karşılaşılabilir. Böyle durumlarda programı çalıştırdığımızda program bu hata hakkında bilgi veren `exception` lar verir.
.Net'de iki tür exception vardır:
- Program çalıştırken üretilen exceptionlar.
- CLR(Common Language Runtime) tarafında üretilen exceptionlar. 

