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
## İki Boyutlu Array Hakkında Bazı İşlemler
```csharp
  int[,] two = new int[5, 10];
  Console.WriteLine("GETLENGTH: " + two.GetLength(0)); // Writes 5
  Console.WriteLine("GETLENGTH: " + two.GetLength(1)); // Writes 10
  Console.WriteLine("LENGTH: " + two.Length); // Writes 50
  ```
  
