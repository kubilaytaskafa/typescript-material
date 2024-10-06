### bu eğitim materyali sadece gerektiği kadar typescript öğretir bilginize.

# DERS 1 TYPESCRİPT NEDİR?-

#### typescript javascriptin takım elbise giymiş halidir.

#### typescript ile tip yönetimi sağlayabilirsiniz.

#### typescript bir dil değildir. bir syntax yapısıdır.

#### typescript denemeleri yapmak için:https://www.typescriptlang.org/play/?#code/MYewdgzgLgBAKiADgGwIYF4AUqBcYCuAtgEYCmATgDTF5FnkCUtJF6AfAN4CwAUAPR8YQmMQCW5GBAA-5KTFGB9QGSlCMAJ6pEgRkBkAEy0xevcqSj5yYGKgDUxXgF8jPBClSYAjACZKn9wyA

#### peki typescript ne yapar?

#### typescript bizlere veri tipleri belirtmemizi sağlar. peki bu nedir?

#### örneğin javascriptte bir yaş değişkeni ataması yapalım

````javascript
//bu kısımda yaş değişkenine atanan değer stringtir.
let age="21"```
````

````javascript
// bu kısımda yaş değişkenine atanan değer numberdır
let yas=21 ```
````

#### yukarıda gördüğünüz üzere javascriptte yaş değişkenini 2 tipte de verebiliriz.

#### fakat bu yöntem sakıncalıdır. çünkü bu değişkeni kullanarak sayısal bir işlem yaparsak (dogum tarihi vs.) string ifade olan değer bize hata döndürür.

## işte tam burada typescript bize yardımcı olur.

#### typescript sayesinde bizler değişkene bir tip ataması yaparız.bu sayede o değere yalnızca atanan tipte değerler setlenebilir.

#### örnek:

```typescript
// bu atamada typescript bizlere hata mesajı verir.
let age: number = "21";
// hata mesajı= Type 'string' is not assignable to type 'number'. yani string tipi bu değişkene setlenemez.
```

#### typescript doğru kullanım örneği:

````typescript
// doğru kullanım budur.
let age:number=21 ```
````

## Peki typescript React ta nasıl kullanılır.

#### Reactta eğer vite ile proje oluşturuyorsanız zaten proje oluşumunda size hangi yazım stili ile yazmak istediğinizi sorar.hep javascript seçiyorduk fakat artık typescriptte seçebiliriz.

#### dosya uzantılarımız artık jsx değil tsx dir.

# DERS 2 TEMEL TİPLER VE ANY TİPİ-

#### bizlerin temel tipleri:

- string =yazı
- number =sayı
- boolean =boolean
- undefined = tanımlanmamış
- null =boş
- object =obje

#### string temel tipi kullanımı:

```typescript
// burada name değişkeni sadece string tipte değer alır.
let name: string = "kubilay";
// bu değişkeni string tipte değer harici bir değer ile değiştiremezsiniz.
name = 24;
```

#### number temel tipi kullanımı:

````typescript
// artık age değeri sadece number tipinde değer alacaktır.

let age:number=21;```
````

#### boolean veri tipi kullanımı:

```typescript
// result değişkeni sadece true veya false değeri alır.
let result: boolean = true;
```

### ANY VERİ TİPİ

#### any veri tipi bazı durumlarda hayat kurtarır.

#### örneğin bir veri çekme işlemi yaptık ve apiye gittik. apiden bize bir kullanıcı verisi döndü bizler bu kullanıcının yaşını almak istiyoruz fakat backend yazan developer yaş verisini string veya number olarak verebilir.

#### işte servisten gelen değerin tipinin bilinmediği durumlarda bu veriyi atayacağımız değişkenin tipini any vererek kendi hayatımızı kurtarmış oluruz.

#### örnek kullanım :

```typescript
// burada data.age temsilidir takılma :)
// age gelen veri ne tipte olursa olsun setlenebilir.
let age: any = data.age;
```

#### !!!! any tipini kullanırken dikkat etmeniz gerekir.
