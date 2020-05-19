# C# Veri Yapıları

## 1- Queue 

First In First Out `FIFO` mantığıyla çalışın bir veri yapısıdır. Queue bir *Collection* sınıfıdır. Bu nedenle **dinamik** bir yapıdır. Eleman eklenip-çıkartıldıkça boyutu değişir.

#### Tanımlama
```csharp
Queue<string> queue = new Queue<string>(); // Collection'da tutmak istediğimiz tipi verebiliriz.
```

#### Önemli Metodlar

- `Enqueu()` Kuyruğun sonuna bir eleman ekler.
- `Dequeue()` Kuyruğun başındaki elemanı kuyruktan çıkarır.
- `Peek()` Kuyruğun başındaki elemanı döner. `Dequeu()` metodundan farkı elemanı queue'den çıkarmaz.
- `Contains(T)` Kuyrukta belirli bir elemanı arar. `True` veya `False`döner.
- `Clear()` Kuyruğu temizler.
- `Count()`Kuyruktaki eleman sayısını verir.
