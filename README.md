🔢 Ackermann Fonksiyonu ile Öz Yineleme
---

Bu proje, bilgisayar bilimleri ve matematiksel mantık alanında önemli bir yere sahip olan Ackermann Fonksiyonu’nun C# programlama dili kullanılarak özyinelemeli (recursive) şekilde uygulanmasını sunmaktadır. Proje, özyinelemenin çalışma mantığını ve fonksiyonların hesaplama gücünü göstermek amacıyla geliştirilmiştir.

---

🎯 Projenin Amacı
---

Bu çalışmanın temel amacı, Ackermann Fonksiyonu’nun matematiksel tanımını C# dilinde özyinelemeli olarak kodlamak ve çalışma mantığını somut bir örnek üzerinden açıklamaktır. Bu kapsamda:

- Özyinelemeli fonksiyonların mantığı anlaşılır  
- Matematiksel ifadelerin kod karşılığı gösterilir  
- Hesaplama karmaşıklığı ve büyüme davranışı gözlemlenir  

---

📚 Ackermann Fonksiyonu Nedir?
---

Ackermann Fonksiyonu, Wilhelm Ackermann tarafından tanımlanmış, ilkel özyinelemeli olmayan en klasik fonksiyon örneklerinden biridir. İki doğal sayı alır ve yine bir doğal sayı döndürür.

Tanımı:

```
A(m, n) =
  n + 1                     , m = 0
  A(m - 1, 1)               , m > 0 ve n = 0
  A(m - 1, A(m, n - 1))     , m > 0 ve n > 0
```

Bu fonksiyon çok hızlı büyüyen bir yapıya sahiptir ve küçük değerlerde bile büyük sonuçlar üretebilir. Bu özelliği, özyineleme mantığını ve algoritmik maliyeti anlamak için önemli bir örnektir.

---

⚙️ Teknik Detaylar
---

| Özellik | Açıklama |
|----------|----------|
| Dil | C# |
| Platform | .NET Framework |
| Paradigma | Özyinelemeli Programlama |
| IDE | Visual Studio |

---

💻 Implementasyon Detayları
---

Projenin ana mantığı `Program.cs` dosyasında bulunan `Ackermann(int a, int b)` fonksiyonunda yer almaktadır.

C# implementasyonu:

```csharp
static int Ackermann(int a, int b)
{
    if (a == 0)
    {
        return b + 1;
    }
    else if (a > 0 && b == 0)
    {
        return Ackermann(a - 1, 1);
    }
    else
    {
        return Ackermann(a - 1, Ackermann(a, b - 1));
    }
}
```

Main metodu içerisinde örnek olarak `A(2, 4)` hesaplanmış ve sonuç konsola yazdırılmıştır. Daha büyük değerlerde hesaplama süresi ciddi şekilde artabilir ve StackOverflowException hatası oluşabilir.

---

🚀 Kurulum ve Çalıştırma
---

1. Projeyi indirip klasöre çıkarın  
2. `VeriOdev9.sln` dosyasını Visual Studio ile açın  
3. F5 tuşu ile projeyi çalıştırın  
4. Konsol ekranında sonuç görüntülenir  

---

📂 Proje Yapısı
---

```
Ackermann-Fonksiyonu-ile-Ozyineleme-master/
├── App.config
├── Program.cs
├── VeriOdev9.csproj
├── VeriOdev9.sln
├── Properties/
└── LICENSE
```

---

📜 Lisans
---

Bu proje MIT Lisansı ile lisanslanmıştır. Detaylar LICENSE dosyasında yer almaktadır.

---

👩‍💻 Geliştirici
---

Şilan Pehlivan
