# C# Veri Yapıları
### C# Collection
Collection'lar datayı yönetmek, depolamak, maniple edebilmek için tasarlanmıştır. Dataya ekleme, silme, arama, sıralama gibi işlemler yapmamıza imkan sağlayan yapılardır.   

> ### Generic ve Non-Generic Collection Farkı
> En genel fark Generic tipler `strongly typed` yani barındırdığı veri tipleri aynı olmalıdır. Non-Generic tiplerde ise veri tiplerini aynı olma zorunluluğu yoktur. Yani bir string eleman ekleyebilir bir başka ekleyeceğimiz eleman integer olabilir. 

## 1- Queue (Kuyruk)

First In First Out `FIFO` mantığıyla çalışın bir veri yapısıdır. Queue bir *Collection* sınıfıdır. Bu nedenle **dinamik** bir yapıdır. Eleman eklenip-çıkartıldıkça boyutu değişir.

#### Tanımlama
```csharp
Queue<string> queue = new Queue<string>(); // Collection'da tutmak istediğimiz tipi verebiliriz.
```

#### Önemli Metodlar

- `Enqueu()` Kuyruğun sonuna bir eleman ekler.
- `Dequeue()` Kuyruğun başındaki elemanı kuyruktan çıkarır.
- `Peek()` Kuyruğun başındaki elemanı döner. `Dequeu()` metodundan farkı elemanı kuyruktan çıkarmaz.
- `Contains(T)` Kuyrukta belirli bir elemanı arar. `True` veya `False`döner.
- `Clear()` Kuyruğu temizler.
- `Count()`Kuyruktaki eleman sayısını verir.

## 2- ArrayList
`Non-Generic` bir collection tipidir. Array'e benzer ancak bir size belirlememize gerek yoktur. 
#### Tanımlama
```csharp
ArrayList arrayList = new ArrayList();
```
#### Önemli Metodlar
> ### Not : Diğer Collectionlar ile benzer metodlar tekrardan yazılmamıştır.

- `InsertRange()` ArrayList'e belirli bir indisten başlayarak bir collection ekler. İlk parametre `integer` index başlangıcı, ikinci parametre eklenecek collectiondır.
- `AddRange()` Bir collection'ı ArrayList'e eklemek için kullanılır.
- `RemoveRange()` Belirli bir indisten başlayarak belirtilen sayıda elemanı collectiondan siler. İlk parametre index başlangıcı, ikici parametre kaç tane eleman silineceğidir.

## 3- SortedList
Küçükten büyüğe doğru artan `key` değer ile `key-value` çiftleri barındıran bir collectiondır. Key değeri `null` **olamaz**.
#### Tanımlama
```csharp
SortedList<int, string> keyValuePairs = new SortedList<int, string>();
```
