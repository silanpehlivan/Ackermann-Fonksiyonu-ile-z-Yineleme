<div align="center">

# Ackermann Fonksiyonu

### Küçük bir fonksiyon, hızla büyüyen bir hesap.

![C#](https://img.shields.io/badge/C%23-2563eb?style=for-the-badge)
![.NET Framework](https://img.shields.io/badge/.NET%20Framework-0891b2?style=for-the-badge)
[![MIT](https://img.shields.io/badge/MIT-16a34a?style=for-the-badge)](LICENSE)

Ackermann fonksiyonunu özyinelemeli olarak uygulayan ve hızlı büyüme davranışını örnekleyen konsol projesi.

**Özyineleme ve hesaplama maliyeti**

[Projeyi keşfet](https://github.com/silanpehlivan/Ackermann-Fonksiyonu-ile-z-Yineleme/tree/master) · [Kurulum ve ayrıntılar](#projeyi-çalıştırmak-ve-incelemek)

</div>

---

## İçeride neler var?

- **01** · İç içe özyinelemeli fonksiyon çağrıları
- **02** · A(2, 4) için örnek hesaplama
- **03** · Özyineleme ve hesaplama maliyetinin incelenmesi

## Projeyi çalıştırmak ve incelemek

<details>
<summary><strong>Kurulum, kod yapısı ve teknik notları aç</strong></summary>

## Öne Çıkanlar

- İç içe özyinelemeli fonksiyon çağrıları
- A(2, 4) için örnek hesaplama
- Özyineleme ve hesaplama maliyetinin incelenmesi

## Teknolojiler

C# · .NET Framework

### Teknik yaklaşım

Ackermann fonksiyonunun taban koşulları ve iç içe rekürsif çağrıları doğrudan uygulanır. A(2, 4) örneği çağrı yapısını incelemek için başlangıç noktasıdır.

### Kodu incelemeye başlayın

- [Program.cs](Program.cs)

### Kapsam ve sınırlar

Girdi büyüdükçe çağrı sayısı hızla artar; büyük değerlerde çalışma süresi ve stack taşması sınırları dikkate alınmalıdır.



Bu proje, bilgisayar bilimleri ve matematiksel mantık alanında önemli bir yere sahip olan Ackermann Fonksiyonu’nun C# programlama dili kullanılarak özyinelemeli (recursive) şekilde uygulanmasını sunmaktadır. Proje, özyinelemenin çalışma mantığını ve fonksiyonların hesaplama gücünü göstermek amacıyla geliştirilmiştir.

---

 Projenin Amacı
---

Bu çalışmanın temel amacı, Ackermann Fonksiyonu’nun matematiksel tanımını C# dilinde özyinelemeli olarak kodlamak ve çalışma mantığını somut bir örnek üzerinden açıklamaktır. Bu kapsamda:

- Özyinelemeli fonksiyonların mantığı anlaşılır  
- Matematiksel ifadelerin kod karşılığı gösterilir  
- Hesaplama karmaşıklığı ve büyüme davranışı gözlemlenir  

---

 Ackermann Fonksiyonu Nedir?
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

 Teknik Detaylar
---

| Özellik | Açıklama |
|----------|----------|
| Dil | C# |
| Platform | .NET Framework |
| Paradigma | Özyinelemeli Programlama |
| IDE | Visual Studio |

---

 Implementasyon Detayları
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

 Kurulum ve Çalıştırma
---

1. Projeyi indirip klasöre çıkarın  
2. `VeriOdev9.sln` dosyasını Visual Studio ile açın  
3. F5 tuşu ile projeyi çalıştırın  
4. Konsol ekranında sonuç görüntülenir  

---

 Proje Yapısı
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




</details>

---

<div align="center">

**© 2023 Şilan PEHLİVAN**

Bu proje MIT lisansı kapsamında sunulmaktadır. Kullanım ve dağıtım koşulları: [LICENSE](LICENSE).

</div>
