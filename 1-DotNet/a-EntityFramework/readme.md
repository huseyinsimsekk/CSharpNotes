# Entity Framework
- Sorgu çalıştırılınca otomatik transaction kontrolü yapılır. Ayrıca transaction yönetimi için özelleştirme yapma imkanı sunar.
- Caching imkanı sağlar. Sık kullanılan sorgular cache'den dönebiliriz. Sürekli db ye gitme maaliyetini azaltır.
- Değişiklik olan entity veya bir property'nin izlenmesi sağlar. 
- Data annotation'lar ile konfigüre edebiliriz.
- Linq sorguları kullanma imkanı verir. Entity'de linq sorguları yazıldıktan sonra bu sorguları sql sorgularına çevirip çalıştırılmasını sağlar. Aynı zaman yine direkt olarak sql sorguları yazmamıza da imkan verir.

## Entity Framework WorkFlow

- İlk olarak domain classlar yani entity(model)'ler tanımlanır. Bunları set edeceğimiz bir DbContext'ten türemiş bir `Context` classı oluşturulur. Bazı konfigürasyonlar yapılır. ConnectionString'in belirtilmesi veya schema'nın kontrol edilmesi gibi.
- Bir entity class'ının örneği alınıp data doldurulur. Bu datayı db'ye eklemek istediğimizde Add methodu ile ekleyip SaveChanges methodu ile commitleriz. Bu methodlar EF API tarafından karşılanıp sql sorgusuna çevrilip db'de çalışır.
- `Okuma` linq sorguları ile istek göndeririz. Bu sorgu EF API tarafından karşılanıp sql sorgusuna çevrilip çalıştırılır. Dönen sonuç tekrardan EF API tarafından modele dönüştürülür. Diğer sorgularda bu yapıda çalışır.
