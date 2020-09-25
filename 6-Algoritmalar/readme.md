# Algoritmalar
## Bir Not
Eğer bir int listenin sorted olup olmadığı kontrol etmek istiyorsak ilk olarak listeyi orderby ile sıralayıp temp bir liste tanımlıyoruz. Sonra iki listeyi `SequenceEqual` methodu ile karşılaştırıyoruz eğer true dönerse listemiz sıralıdır. 
 ```csharp
    var arr= new List<int>(){1,2,3,4};
    var ordering= arr.OrderBy(m=>m);
    if(ordering.SequenceEqual(arr))
    {
        Console.WriteLine("Ordered");
    }
    else{
        Console.WriteLine("Not Ordered");
    }
```
