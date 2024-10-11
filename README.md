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

# -DERS 4 İNTERFACE VE TYPE -

#### bizler base tipleri görmüştük.

#### bunlar string,number,boolean vs.

#### interface ve type işlemi bizlere kendi tiplerimizi oluşturmamızı sağlar.

#### peki nasıl kullanılır.

### type :

#### type keywordü ile kendimize özel bir tip tanımlaması yapabiliriz.

#### örnek:

```typescript
// artık user adına bir tipimiz mevcut
// bizler bir değişkende user tipini kullanırsak artık o değişkene user tipinin şartları dışında bir ver setlenemez.
type User = {
  name: string;
  age: number;
};
// user veri tipini vermediğimiz bir objede age kısmına string,bool,number tipi setlediğimizde bir hata almayız.
// hatta biz bu objede age number keylerini kullanmayabilir
// ya da department adında yeni bir key kullanabiliriz.
const object1 = {
  name: "kubilay",
  age: "23",
};
// fakat bizler user tipini verdiğimiz bir objede age keyine number tipi veriden başka bir tipte veri setleyemeyiz.
// hatta User tipinde belirlediğimiz name ve age keyi zorunlu kullanımdadır. Bu keylerden başka bir key kullanamayız.
const object2: User = {
  name: "kubilay",
  age: "2", // tip uyuşmuyor!!!

// User tipini eğer bir arrayde kullanırsak kesinlikle şartları sağlamak gerekir
type User={
    name:string,
    age:number,
}

let arry:User[];

// burada arraye veri setlerken User tipini kullandığımız için user tipindeki şartları sağlamadık ve hata aldık
arry=["kubilay"] //!!! veri tipi uyuşmuyor

// artık arry değişkeninin kullanımı aşağıdaki gibidir.
// arry değişkenine setlenecek her değer aşağıdaki gibi User tipinin dengi  olmalıdır.
arry=[{name:"kubilay",age:22}]

};
```

### interface

#### interface de kendi tiplerimizi oluşturmamızı sağlar.

#### arasındaki tek fark type da eşittir (=) kullanıyoruz,interface de eşittir (=) kullanmaya gerek yoktur.

#### örnek:

```typescript
//  interface ile tip tanımladık
interface User {
  name: string;
  age: number;
}
// tipimizi obj1 sabitinde kullandık
const obj1: User = {
  name: "kubilay",
  age: 22,
};
```

#### !! ayrıca interface'ler birbirlerinden miras alabilir. önümüzdeki derslerde bu konuya bakacağız.

# -DERS 5 OPTİONAL TYPES-

#### bizler kendi tipimizi oluşturup bir değişkende kullandığımız zaman o dğeişkendeki veri oluşturduğumuzun tipin dengi olmak zorundaydı

#### örneğin aşağıdaki kodda oluşturduğumuz User veri tipimizde name ve age değerleri vardı ve bizler bir objede User tipi kullanırsak o değerleri zorunlu setlemek durumundaydık .

#### örnek:

```typescript
interface User {
  name: string;
  age: number;
}

const obj1: User = {
  name: "kubilay",
  age: 22,
};
```

#### bazı durumlarda tipimizin içindeki değerleri bazen setlemetyi zorunlu kılmayız. işte bu durumlarda OPTİONAL TYPES kullanabiliriz.

#### OPTİONAL TYPES kullanmak için sadece tipimizdeki keylerin sonuna soru işareti (?) eklememiz yeterlidir.

#### örnek:

```typescript
// User adında bir tip belirledik ve içerisinde name ve age keylerini kullanarak bu değerleri zorunlu kılmıştık.
// fakat age keyinde optional types kullandık bu yüzden bu tipi kullandığımız bir değişkende age keyini kullanmak zorunlu değildir.
interface User {
  name: string;
  age?: number;
}
// user tipi kullandığımız bir objede opsiyonel olarak age keyini kullanmadık ve hata almadık.
const obj1: User = {
  name: "kubilay",
};
```

# -DERS 6 FUNCTİONS(FONKSİYONLAR) !ÖNEMLİ-

#### bizler js de bir fonksiyon oluştururduk ve bu fonksiyona parametreler geçebilirdik.

#### örnek olarak bir toplama fonksiyonu yazıp 2 tane parametre alırız ve bu parametreleri toplayıp konsola yazdırabiliriz.

#### örnek:

```javascript
const topla(a+b){
    console.log(a+b)
}
// fakat js de tip belirlemediğimiz için bu fonksiyona istediğimiz tipte parametre geçebiliriz. ve bu bizlere projemizde hata döndürebilir.
// aşağıda bir string bir de number değer setledik ve bu fonk bize kullanılabilecek bir değer döndürmez
topla(5,"x")
```

#### js de fonksiyonlarda tip belirlememek bizler için handikap bir durum olabilir.

#### typescriptte fonksiyon parametrelerimize tip şartı koyabiliriz.

#### bu sayede o fonksiyona parametre olarak sadece setlenen tipin dengi olan tipteki veriler girilebilir.

#### örnek:

```javascript
// burada topla fonk una 2 tane parametre gelecek(a,b)
// bu parametrelerin tipi number olmak zorundadır.
const topla = (a: number, b: number) => {
  console.log(a + b);
};
// b parametresine atanan değer b parametre tipini dengi olmadığı için hata alacağız.
topla(5, "3"); // !! tip uyuşmazlığı
topla(5, 3); // doğru kullanım.
```

#### bizler typescript ile fonk içerisinden return ettiğimiz değerin tipini de belirtebiliriz.

#### bu sayede fonk dan return edilen değer o tipte değilse hata alırız ve projemiz patlamaz.

#### fonksiyonda return edeceğimiz verinin tipini belirtmek için fonksiyon parantezinin () sonuna iki nokta (:) koyarız. ve daha sonra belirteceğimiz tipi yazarız.

#### örnek:

```typescript
// topla fonksiyonundan return edeceğimiz veri için  tip belirlemesi yaptık
const topla = (a: number, b: number): number => {
  return a + b;
};

const toplam = topla(5, 3);

console.log(toplam);
```

#### istersek return tipine birden fazla tip de verebiliriz.

#### örnek:

```typescript
// topla fonksiyonundan return edeceğimiz veri için  birden fazla tip belirlemesi yaptık.
const topla = (a: number, b: number): number | string => {
  return a + b;
};

const toplam = topla(5, 3);

console.log(toplam);
```

#### örnek uygulama: fonksiyonda string tipinde bir array alıp arrayin içinde map ile dönüp ekrana yazdıracağız.

#### uygulama:

```typescript
// fonksiyon parametresine string bir array Alıyor.
const write = (Arry: string[]) => {
  // aldığı array içerisindeki her bir veri üzerinde dönüyor ve dönerken o verileri ar ismi ile tanımlıyor.
  // ar verileri string olmak zorundadır.
  Arry.map((ar: string) => {
    // döndüğü her veriyi tek tek ar ismi ile konsola yazdırıyor.
    console.log(ar);
  });
};

// names adında string tipinde bir array tanımladık
const names: string[] = ["kubi", "typescript", "öğretiyor."];

// fonksiyonu çağırdık ve parametresine names değişkenini atadık
write(names);
```

#### yukarıdaki uygulamalarda fonksiyonlar hiçbir şey döndürmüyor.

#### bizler return kullanmadığımız fonksiyonlarda return tipi olarak void verebiliriz.

### Void: geriye bir şey döndürmeyen methot.

#### örnek :

```typescript
// burada fonk bir şey return etmediği için return parametresine void verdik.
const write = (Arry: string[]): void => {
  Arry.map((ar: string) => {
    console.log(ar);
  });
};

const names: string[] = ["kubi", "typescript", "öğretiyor."];

write(names);
```

#### örnek uygulama: kendimize ait bir tip oluşturup o tipte 2 tane objeyi bir arrayde tanımlayıp arrayi fonksiyona parametre geçelim. daha sonra fonksiyonda array üzerinde gezip konsola yazdıralım.

### uygulama :

```typescript
// tipimizi tanımlayalım
interface User {
  name: string;
  age: number;
}

// fonksiyonumuzu oluşturalım
// fonksiyondaki parametreye gelen array USer tipinde olduğu için
// parametredeki arrayin tipi User olmalıdır.
const writeConsole = (Arry: User[]): void => {
  // ar verileri user tipinde olduğu için
  // ar tipi user olmalıdır.
  Arry.map((ar: User) => {
    console.log(ar);
  });
};
// 1. objemiz.
const obj1: User = {
  name: "kubilay",
  age: 22,
};
// 2. objemiz.
const obj2: User = {
  name: "ŞEYMA",
  age: 21,
};
// arrayimizi oluşturduk burada arrayimiz User tipinde olduğu için
// sadece user tipindeki veriler setlenebilir.
let ourArray: User[] = [obj1, obj2];
writeConsole(ourArray);
```

#### burada sadece objedeki name veya age i yazdırmak istersek:

#### ar.age veya ar.name dememiz yeterlidir.
