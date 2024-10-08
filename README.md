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
````

# DERS 3 UNİON TYPES,LİTERAL TYPES VE ARRAY

### UNİON TYPES

#### union types bir veya olayıdır.

#### union types kullanmak için veya( | ) karakterini kullanmalısınız.

#### union types ile bir değişkene birden fazla tipte veri eklenmesine izin veririz.

#### örnek:

```typescript
// bu değişkene hem number hem de string veri tipini verebiliriz.
let age: number | string = 21;
```

#### örnek2:

```typescript
// bu değişkene hem number hem string hem de boolean tipte veri atanabilir.
let age: number | string | boolean = true;
```

### LİTERAL TYPES

#### literal types ile de bir değişkene tip değil direkt veri belirleyebiliriz.

#### örnek:

```typescript
// artık bu değişkene pending,approved,rejected dışında bir veri setlenemez.
let statusResult: `pending` | `approved` | `rejected`;
```

#### yani literal type ile değer zorunluluğu ekleyebiliriz.

### ARRAY

#### typescriptte bir değişkene array tipini verebilirsiniz.

#### TS de bu yöntem ile arrayler oluşturulur.

#### önemli olan nokta arrayin içine gelecek olan verilerin tiplerini belirlemek gerekir.

#### eğer tip belirlemeden array belirlerseniz hata alacaksınız.

#### typescriptte array tanımlaması

```typescript
// names değişkenine tip olarak array verdik.
// arrayimizin içine gelecek olan veriler de string tipinde olmalıdır.
// string veri dışında bir veri arraye setlenirse hata alırsınız.
let names: string[] = ["kubilay", "tansel", "şeyma"];
```

#### değişkene array tip tanımlamasının farklı bir yolu da vardır.

#### örnek:

```typescript
// değişkene array tipi tanımlamak için farklı bir yol
let names: Array<number> = [1, 2, 3];
```

#### isterseniz union types kullanarak arraye birden fazla tip ataması yapabiliriz.

#### örnek:

```typescript
// arraye hem string hem de number setleyebiliriz.
let mixedArray: (number | string)[] = [2, 3, 4, "kubilay"];
```
