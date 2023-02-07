# C Temelleri

## İçindekiler:

* [Değişkenler - Variables](#değişkenler---variables)

    * [Değişken Sınır Aralıkları](#değişken-sınır-aralıkları)

    * [Değişken Tanımlama](#değişken-tanımlama)

    * [Değişken İsimleri Seçilirken Dikkat Edilmesi Gereken Hususlar](#değişken-i̇simleri-seçilirken-dikkat-edilmesi-gereken-hususlar)

    * [Değişken Niteleyicileri](#değişken-niteleyicileri)

* [Sabitler](#sabitler)
    
    * [#define ile Sabit Tanımlama](#define-ile--sabit-tanımlama)

    * [const ile Sabit Tanımlama](#const-ile-sabit-tanımlama)

* [Operatörler](#operatörler)

    * [Atama Operatörleri](https://github.com/Mona-Roza/Notes/tree/main/embedded_system/c_basicss#atama-operatörleri)

    * [Aritmetik Operatörler](#aritmetik-operatörler)

    * [Karşılaştırma Operatörleri](#karşılaştırma-operatörleri)

    * [Mantıksal Operatörler](#mantıksal-operatörler)

    * [Diğer Operatörler](#diğer-operatörler)

* [printf()'in kullanımı](#printfin-kullanımı)

    * [Format Specifiers](#format-specifiers)

    * [Kaçış Dizileri](#kaçış-dizileri)

* [scanf()'in kullanımı](#scanfin-kullanımı)

* [Diziler-Arrays](#diziler---arrays)

    * [Tek Boyutlu Diziler](#tek-boyutlu-diziler)

    * [Çok Boyutlu Diziler](#çok-boyutlu-diziler)

* [Koşul Deyimleri](#koşul-deyimleri)

    * [If-Else Statement](#if-else-statement)

    * [Switch-Case Statement](#switch-case-statement)

* [Döngü Deyimleri](#döngü-deyimleri)

    * [for](#for)

    * [while](#while)

    * [do…while](#dowhile)

    * [break ve continue Deyimleri](#break-ve-continue-deyimleri)

    * [goto Deyimi ve Etiket](#goto-deyimi-ve-etiket)

* [Fonksiyonlar](#fonksiyonlar)

    * [Fonksiyon Prototipi](#fonksiyon-prototipi)

    * [Fonksiyon Tipleri](#fonksiyon-tipleri)

        * [Değer Döndürmeyen Fonksiyonlar](#değer-döndürmeyen-fonksiyonlar)

        * [Değer Döndüren Fonksiyonlar](#değer-döndüren-fonksiyonlar)
    
    * [Özyineli - Recursive Fonksiyonlar](#özyineli---recursive-fonksiyonlar)

    * [Dizileri Fonksiyon Parametresi Olarak Gönderme](#dizileri-fonksiyon-parametresi-olarak-gönderme)

* [Algoritma Pekiştirme Soruları](#algoritma-pekiştirme-soruları)

    * [Değişken Soruları](#değişken-soruları)

    * [Koşul Deyimleri Soruları](#koşul-deyimleri-soruları)

    * [Döngü Deyimleri Soruları](#döngü-deyimleri-soruları)

## Değişkenler - Variables:
Değişkenler(variables), bellekte bilginin saklandığı gözlere verilen simgesel isimlerdir. Değişkenlerin değeri programın içerisinde değiştirilebilir.
	
* Karakterler (Harfler) -> char (ör: a, b, c, e, f, ...) (1 byte-8 bit) 	

* Sayılar:
    * Tam Sayılar -> int (integer) (ör: 1,2,3,4, -1,-5,-10,...) (4 byte-32 bit)
    
    * Noktalı Sayılar:
        - float (ör: 0.55555) (4 byte- 32 bit)
        - double (ör: 0.55555555) (8 byte- 64 bit)

* Kelimeler (Katarlar) -> string (ör: "mona", "okul", "bilgisayar",....) (4 byte-32 bit)

### Değişken Sınır Aralıkları:

Değişkenler kapladıkları yer dolayısıyla belli bir sınır aralığına sahiptirler. 

<script src="https://gist.github.com/Mona-Roza/fb4c5cbf70632711e3fb522593cc5ff2.js"></script>


| Veri Türü | Bit Genişliği |	Sınır Aralığı |
|---|---|---| 
| char | 8 bit | [-128, 127] |
| int | 32 bit/ 16 bit | [-2 147 483 648, 2.147.483.649] |
| float | 32 bit | [1 17549e-038,  3 40282e+038] | 
| double | 64 bit | [2 22507e-038, 1 79769e+308] |
    
	
### Değişken Tanımlama:

Değişken tanımlanırken öncelikle değişkenin veri türü/tipi belirtilmeli ardından değişkene verilecek simgesel isim belirlenmelidir. Değişkenin değeri tanımlanma sırasında veya programın herhangi bir noktasında verilebilir. Örnek kullanım:

```
    int num;
    num = 5;
```

veya

```
    int num =5;
```

### Değişken İsimleri Seçilirken Dikkat Edilmesi Gereken Hususlar:

i. Değişken isimleri açıklayıcı olmalıdır.

ii. Değişken isimleri dilin anahtar sözcükleri olmamalıdır. (int, char, main, …) 

iii. İlk karakter alt çizgi veya harf olmalıdır. (ör: _degisken1, degisken2, 3uncudegisken -> olamaz)

iv. Boşluk karakteri bulundurmamalıdır.
        
### Değişken Niteleyicileri:
Değişken niteleyicileri temel değişken tip adlarının önüne takı gibi eklenerek yeni veri tipleri oluştururlar. (ör: short int degisken1) 
    
    • short : Değer aralığını kısaltır. Sadece int için kullanılır. Bit genişliğini 16 Bite düşürür.
 
    • long: Değer aralığını arttırır. Sadece int için kullanılır.

    • unsigned: İşaret bitini kaldırıp aralık değeri değişmeden aralığı pozitif kısma taşır. 

    • signed: Her tanımladığımız değişken signed olarak işaretli. 
 
    • volatile: Önüne geldiği değişkenin üzerinde derleyicinin bir optimizasyon yapmasına engel olur.

    • static: Önüne geldiği değişkenin bir kere çalıştırıldıktan sonra program sonuna kadar hafızada depolanıp çağrıldığında aynı konumdan gelebilmesini, böylelikle belleğin tekrar tekrar yorulmamasını sağlar.

## Sabitler:
Sabitler (constants), program boyunca değeri değiştirelemeyen değişkenlerdir. Sabitlerin değerleri tanımlama sırasında verilir ve program boyunca bir daha değiştirilemez.
	
### #define ile  Sabit Tanımlama: 
#define ile tanımlanan sabitler globalde(genel olarak) tanınır. Define bir önişlemci komutu olduğundan derleme anında define ile belirtilen sabit değerler, kod içerisinde yerine yerleştirilir ve bu şekilde derleme yapılır, bellekte yer tutmazlar. Örnek kullanım:

    `#define pi  3.14141592653589793`
    
### const ile Sabit Tanımlama: 
const ile tanımlanan sabitler, değişkenlere benzer olarak tanımlandıkları bölgelere göre tanınırlar ve değişkenler gibi bellekte yer tutarak çalışma zamanında çağırıldıkları anda işleme tabii tutulurlar. Örnek Kullanım:
    
    `const int pi = 3.141592653589793;`

## Operatörler:
Operatörler, aritmetik işlemlerde ve kontrol deyimlerinde kullanılan işlem değeri olan karakterlerdir. 
	
### Atama Operatörleri:

| Operatör | Operatörün Anlamı |
|----|----|
| = |Atama operatörü. (derlemeli dillerde) soldakinin içerisine sağdakini ata. |
| sayi1 += sayi2 | sayi1 = sayi1 + sayi2 | 
| sayi1 -= sayi2 | sayi1 = sayi1 - sayi2 |
| sayi1 /= sayi2 | sayi1 = sayi1 / sayi2 |
| sayi1 *= sayi2 | sayi1 = sayi1 * sayi2 |
| sayi1 |= sayi2 | sayi1 = sayi1 | sayi2 |
| sayi &= sayi2 | sayi1 = sayi1 & sayi2 |
| ^= | XOR Eşittir |

### Aritmetik Operatörler:

| Operatör | Operatörün Anlamı |
|----|----|
| + | Topalama operatörü. Sağındaki ve solundaki iki sayıyı topla. |
| -	| Çıkartma operatörü. Sağındaki sayıyı solundaki sayıdan çıkarır. |
| * | Çarpma operatörü. Sağındaki ve solundaki iki sayıyı çarpar. |
| / | Bölme operatörü. Solundaki sayıyı sağındaki sayıya böler. |
| % (Mod) | Mod Alma işlemi yapar. (Bölümünden kalan) |
| sayi++ | Sayıyı bir arttırır. (sayinın sağında ya da solunda olması okunma sırasına göre işlem önceliğini değiştirir.) |
| sayi-- | Sayıyı bir azaltır. |

### Karşılaştırma Operatörleri:

| Operatör | Operatörün Anlamı |
|----|----|
| < | Küçüktür |
| > | Büyüktür |
| >= |Büyük Eşittir |
| <= | Küçük Eşittir |
| == | Eşit mi? |
| != | Eşit değil mi? |

### Mantıksal Operatörler:

| Operatör | Operatörün Anlamı |
|----|----|
| && | AND |
| &	| Bit düzeyinde AND | 
| || | OR(Alt Gr + <) |
| | | Bit düzeyinde OR |
| ^ | Bit düzeyinde XOR |
| ! | Değil |
| ~ | Sayının (r-1)'e göre mantıksal tersi |

### Diğer Operatörler:

| Operatör | Operatörün Anlamı |
|----|----|
| (Condition):(if it's true)?(if it's false); | Bu operatör ile tek satırlık koşullar yerine getirilir. |

## printf()'in kullanımı: 
Kullanıcıya çıktı vermeye yarar. Örnek kullanım:

`printf("Yazdırılacak metin");`

### Format Specifiers:

| Veri Tipi | Format specifier |
|---|---|
| char | %c|
| int | %d|
| float | %f | 
| double | %f |
| long double | %Lf |
| pointer | %p |
| unsigned int | %u |
| string | %s |

:warning: %f için özellik : %.(noktadan sonraki hanesayısı)f

### Kaçış Dizileri:

| Kaçış Dizgisi | Temsil Edilen İşaret | 
|---|---|
| \a | Uyarıyı (Bip, Zil) temsil ediyor |
| \b | Geri tuşu |
| \e | Kaçış karakteri |
| \f | Form Besleme Sayfa Sonu | 
| \n | Yeni Satır (Satır Besleme) |
| \r | Satır Başı |
| \t | Yatay Sekme |
| \v | Dikey Sekme |
| \\ | Ters Eğik Çizgi |
| \' | Kesme İşareti veya tek tırnak işareti |
| \" | Çift tırnak işareti |
| \? | Soru işareti (trigraphs) |
| \nnn | önlemek için kullanılır Sayısal değeri nnn tarafından verilen bayt sekizlik sayı |
| \xhh… | Sayısal değeri hh tarafından verilen bayt, onaltılık sayı |
| \uhhhh | Unicode kod noktası 10000 onaltılık değerin altında |
| \Uhhhhhhh | Unicode kod noktası, burada h onaltılık bir rakamdır |
	

## scanf()'in kullanımı: 
Kullanıcıdan veri almaya yarar. Örnek kullanım:
```	
int degisken_adi;
scanf("%d", &degisken_adi);
```

## Diziler - Arrays: 
Diziler, aynı veri çeşidinden olan değişkenlerin oluşturduğu bir kümedir. Diziler kullanılarak, aynı isimle birden fazla değişkene erişilebilir ve işlem yapılabilir. 

Diziler tek ya da çok boyutlu olarak tanımlanabilir. 

Diziler belirli bir veri türünden tanımlanabileceğinden dizilerde sadece aynı veri türünden değişken değerleri yer alabilir.

### Tek Boyutlu Diziler:
Programlarda, aynı veri türünden ve farklı isimlere sahip çok fazla sayıda değişken tanımlamak yerine, dizi bildirimi yapmak suretiyle sadece tek isim kullanarak aynı sayıda değişken tanımlamak daha pratik bir sistem ve kolaylık sağlar. Dizi tanımlandığında, dizinin her bir elemanına dizi adı ile birlikte 0'dan başlayarak kullanılan indeks değeri ile erişim sağlanır. Genel  yazım biçimi:

```
veri_tipi dizi_adi[boyut];
dizi_adi[0] = a;
dizi_adiç[1] = b;
...
dizi_adi[boyut-1] = z;
```

veya

`veri_tipi dizi_adi[] = {a, b, ..., z};`

### Çok Boyutlu Diziler:
Çok boyutlu diziler 2 veya daha fazla ekseni olan koordinat düzlemlerine yerleştirilmiş matrisler gibi düşünülebilirler. 2 boyutlu bir dizinin genel yazım biçimi:

```
veri_tipi dizi_adi[x][y];
dizi_adi[0][0] = a;
dizi_adi[0][1] = b;
...
dizi_adi[x-1][y-1] = z;
```

veya

`veri_tipi dizi_adi[][] = {{a, b, ..., z}, {a, b, ...,z}};`

:warning: Bir dizinin adı aynı zamanda dizinin 0. elemanını işaret eden bir işaretçidir. 

## Koşul Deyimleri:
Koşullu ifadeler belirli şartlar durumunda program akışını değiştirecek kod blokları yaratmaya yarar.

### If-Else Statement: 
if-else koşullu işlem yapma deyimidir. İf ve else tek bir karşılaştırma deyimi olup else'nin kullanımı isteğe bağlıdır. Eğer koşul olumlu ise if'den sonraki küme yürütülür ve else'den sonraki küme atlanır; olumsuz ise, if'den sonraki küme atlanır ve eğer varsa else'den sonraki küme yürütülür. Genel yazım biçimi: 

```
if( koşul )
{
    İşlem satıları
    .
    .
    .
}

else if( ikincil_koşul) 
{ 
    İşlem satıları
    .
    .
    .
}

else{ 

    İşlem satıları
    .
    .
    .

}
```

:warning: İki veya daha çok koşul mantıksal operatörler ile birleştirilerek verilebilir.

### Switch-Case Statement: 
Bir değişkenin içeriğine bakarak programın akışını birçok seçenekten birine yönlendiren bir karşılaştırma deyimidir. Genel yazım biçimi:

```
switch(degisken)
{
    case değer1:
        Kod bloğu1;
        .
        .
        .
        break;
        
    case değer2:
        Kod bloğu2;
        .
        .
        .
        break;
        
    .
    .
    .
    
    case değerN:
        Kod bloğuN;
        .
        .
        .
        break;
    
    default:
        Kod bloğu1;
        .
        .
        .
        break;
}
```

:warning: Eğer switch'in koşulu olan değişkenin değeri case ile belirtilen değerlerden hiçbiri değilse default kod bloğu yürütülür. 

## Döngü Deyimleri:
Bu tip deyimler bir kümenin belirli bir koşul altında yinelenmesi için kullanılır. C dilinde while, do…while ve for olmak üzere üç tip döngü deyimi vardır. 

### for: 
Bir küme ya da bir deyim for kullanılarak birçok kez yinelenebilir. Yinelenmesi için koşul sınanması çevrim başında (ya da çevrime girmeden) yapılır. For döngüsünü kullanabilmek için bir döngü sayacına ihtiyacımız vardır. Döngü sayacının başlangıç değeri, durma değeri ve çevrim sonunda sayaca uygulanacak aritmetik işlem for döngüsünün koşul kısmında belirtilmelidir. Genel yazım biçimi:

```
int i;

for(i= başlangıç_değeri; koşul; sayaç işlemi)
{
    Tekrarlanacak kod bloğu;
}
```
:warning: Koşul olumlu olduğu sürece çevrim yinelenir.
    

### while: 
Tekrarlama deyimidir. Bir küme ya da bir deyim while kullanılarak birçok kez yinelenebilir. Yinelenmesi için koşul sınanması çevrim başında yapılır. Genel yazım biçimi:

```
while(koşul)
{
    Tekrarlanacak kod bloğu;
}
```
:warning: Koşul olumlu olduğu sürece çevrim yinelenir.

:warning: While döngüsünü for döngüsünü kullandığımız gibi kullanmak mümkündür. Bunun için yapmamız gerekenleri anlatabilmek için örnek bir kod bloğu inceleyelim.

```
    int i =10;
    
    while(i>0)
    {
        printf("%d", i);
        i--;
    }
```
    
Örnekten de görüleceği gibi, döngü değişkenine bir başlangıç değeri verilir ve döngünün her bir çevrinde bu değer üzerinden değerin koşul şartına uymayana kadar dönmesi sağlanır.

:warning: While döngüsünde en çok dikkat edilmesi gereken nokta koşulda kullanılan değişkene başlangıç değeri atanmasıdır. Herhangi bir değişkene başlangıç değeri verilmediğinde, o değişkenin içeriği rastgele bir değer alır; bu değer koşulu olumsuz kılarsa hiç döngü içine girilmez. Diğer bir nokta ise koşulda kullanılan değişkenin döngü içerisinde değiştirilmesi gerektiğidir. 
		
### do…while: 
Bu deyimin while'dan farkı, koşulun döngü sonunda sınanmasıdır. Yani koşul sınanmadan çevrime girilir ve döngü kümesi en az bir kere yürütülür. Genel yazım biçimi:
	
```
do
{
    Tekrarlanacak küme;
    
}while(koşul);
```

### break ve continue Deyimleri: 
Döngü deyimleri içindekiler yürütülürken, çevrimin, koşuldan bağımsız ivedi olarak sonlanması istendiğinde veya döngünün ivedi olarak bir sonraki çevrime geçmesi istendiğinde break ve continue kullanılır.
	
* break deyimi: Bir döngü içerisinde break deyimi ile karşılaşıldığı zaman, döngü, koşula bakılmaksızın sonlanır ve programın akışı döngüden sonraki ilk deyime yada fonksiyona atlar. Break deyimi, özel bir durum oluştuğunda while, do…while, for ve switch içerisinden çıkmak için kullanılır. 
		
	:warning: İçiçe döngüde kullanıldığı zaman en içtekinde etki eder, üstteki döngü dönmeye devam edecektir. 
			
* continue deyimi: Bir döngü içerisinde continue deyimiyle karşılaşılırsa, ondan sonra gelen deyimler veya fonksiyonlar atlanır ve döngü bir sonraki çevrime girer. Break deyiminin tersi denilebilir. Break döngüyü ivedi olarak sonlandırır, continue bir sonraki çevrime geçirir.
		
### goto Deyimi ve Etiket: 
goto deyimi yardımıyla döngü kurabiliriz. Ancak bu okunmayı zorlaştırdığından programcılar tarafından önerilmemektedir. Yine de bazen kullanılması zorunluluk haline gelebilir. 

:warning: goto deyimi, bir label ile kullanılır. Önce bir label ismi verilir, ardından kod bloğu yazılır ve goto deyimi ardından label ismi ile belirtilen yere geri dönmesi emredilir.Genel yazım biçimi:

```
    int x=1;
    
    etiket1:
        x++;
        if(x<100) 
        {
            goto etiket1;
        }
```

## Fonksiyonlar:
Fonksiyonlar, belirli bir işi yapmak için uygun bir biçimde bir araya getirilmiş kod dizileridir. Bu kod dizileri istenilen yerde çağrılabilir. Böylece tekar eden dizileri yerine fonksiyon çağrılarak aynı kod tekrar tekrar kullanılmış olur. Fonksiyonun genel yapısı:

```
dönüş_veri_tipi/void fonksiyon_adi([varsa]parametreler)
{
    [varsa] yerel tanımlamalar
    ...
    kod bloğu
    ...
    [dönüş_veri_tipi varsa] return değer;
}
```

* dönüş_veri_tipi: Eğer fonksiyon geriye bir değer döndürecek ise fonksiyon imzasında döndürülecek değerin veri tipi belirtilir.

* fonksiyon_adi: Fonksiyonu çağırırken kullanılacak belirleyici isimdir. Değişken adı tanımlarken uyulması gereken kurallar burada da geçerlidir.

* parametreler: Varsa, fonksiyon içinde kullanılması gerekli değerleri ve tiplerini içerir. Her parametre değişken tanımlar gibi tanımlanır. Kullanılan parametre birden fazla ise virgül (,) ile ayrılır. 

:warning: Fonksiyona gönderilen parametre olarak gönderilen değişkenleri değeri fonksiyon içerisinde değiştirilse dahi fonksiyon bittiğinde sahip oldukları ilk değere geri dönerler. Ancak fonksiyona parametre olarak bir değişkenin adresi gönderildiyse ve bu adres üzerinden değişkenin değeri değiştirildiyse bu değişiklik kalıcı olur. 

* yerel tanımlamalar: Fonksiyona özgü değişken ve sabit gibi tanımlamalardır. Bu değişkenler fonksiyon çalıştığı sürece bellekte tutulur, ardından bellekten silinirler.

### Fonksiyon Prototipi:
Tanımlanan bir fonksiyon eğer main fonksiyonundan sonra tanımlandıysa bu fonksiyon için main fonksiyonundan önce bir prototip yazılması gerekir. Ancak main fonksiyonundan önce tanımlanan fonksiyonlar için fonksiyon prototipi yazılmasa da olur. Genel yapısı fonksiyonun imzasından ibarettir:

`dönüş_veri_tipi/void fonksiyon_adi([varsa]parametreler);`

### Fonksiyon Tipleri:
İki tip fonksiyon vardır. Bunlar değer döndüren fonksiyonlar ve değer döndürmeyen fonksiyonlardır.

#### Değer Döndürmeyen Fonksiyonlar:
Değer döndürmeyen fonksiyonlar, alt program gibi kullanılarak main veya diğer fonksiyonlar tarafından çağrıda bulunulur. Fonksiyon içindeki işlemler icra edilir, fakar çağrıda bulunan fonksiyona herhagi bir değer döndürmezler. Genel yapısı:

```
void fonksiyon_adi([varsa] parametreler)
{
    ...
    kod bloğu
    ...
}
```

#### Değer Döndüren Fonksiyonlar:
Değer döndüren fonksiyonlarda, fonksiyon tarafından üretilen değer **return** ifadesi ile çağrıda bulunan fonksiyona döndürülmekte ve bu değer orada kullanılmaktadır. Genel yapısı:

```
dönüs_tipi fonksiyon_adi([varsa] parametreler)
{
    ...
    kod bloğu
    ...
    return dönüş_değeri;
}
```

:warning: **return** ifadesinden sonra yazılan kodlar işleme alınmaz, bu ifade işleme alındığı anda fonksiyon çalışmayı bırakır.

### Özyineli - Recursive Fonksiyonlar:
Doğrudan veya dolaylı olarak kendi kendini çağıran fonksiyonlardır. Bazı uygulamalarda birçok algoritmanın recursive fonksiyonlarla yazılması daha kolay ve sadedir. Döngü deyimleri kullanılarak yazılan uygulamalar da recursive fonksiyonlarla gerçekleştirilebilirler. Genel yapısı:

```
dönüş_tipi fonksiyon_adi([varsa] parametreler)
{
    ...
    kod bloğu
    ...

    if(koşul)
    {
        return fonksiyon_adi([varsa] parametreler);
    }
    else
    {
        return deger;
    }
    
}
```

### Dizileri Fonksiyon Parametresi Olarak Gönderme:
Şu ana kadar gördüğümüz bilgi çerçevesinde, fonksiyonlara gönderilen parametre değerlerinin fonksiyon içerisinde değiştirilmesi mümkün değildir, çünkü fonksiyona değişkenin sadece değeri gönderilir. Fonksiyon içerisindeki işlemlerden gönderilen parametrenin kendisi etkilenmez. Dizilerde durum böyle değildir. Normal kullanımda dizi fonksiyona gönderildiğinde elemanlar değiştirilebilir. Çünkü diziler bölümünde belirttiğimiz gibi dizinin adı aynı zamanda dizinin ilk elemanını gösteren bir işaretçidir. Durum böyle olduğundan, dizi gönderildiğinde, dizi elemanları adresleriyle birlikte gönderilmiş olur ve fonksiyon içerisindeki değişiklerden etkilenirler.Genel yapısı:

```
dönüş_tipi/void fonksiyonadi(veri_tipi parametre_dizi[])
{
    ...
    kod bloğu
    ...
    [varsa] return değer;
}
```
## Algoritma Pekiştirme Soruları:

### Değişken Soruları:

* Bir kenar uzunluğu ve o kenara ait yüksekliği girilen üçgenin alanını hesaplayan programı yazınız.

* Girilen bir fiyatın KDV (%18) eklendikten sonraki KDV’li fiyatını ekrana yazdıran programı yazınız.

* Yarıçapı girilen dairenin çevresini ve alanını hesaplayan programı yazınız. (π = 3.14 ve constant olarak alınız)  

### Koşul Deyimleri Soruları:

* Girilen bir sayının pozitif mi negatif mi olduğunu ekrana yazdıran programı yazınız.

* Girilen iki sayıdan hangisinin daha küçük olduğunu ekrana yazdıran algoritma ve akış şeması

* Bir öğrencinin almış olduğu vize notu ile final notunun ağırlıklı ortalamasını hesaplayan programı yazınız. (Vize notunun %30’unu final notunun %70’ini alarak hesaplama yapınız, geçti mi kaldı mı? Final 60'ın altında olursa kalsın ortalama 50'nin altında olursa kalsın)

* Girilen bir sayının tek mi çift mi olduğunu hesaplayan ve sonucu ekrana yazdıran programı yazınız.

* Girilen bir sayının mutlak değerini hesaplayan ve sonucu ekrana yazdıran programı yazınız.

* Girilen bir x sayısının yine girilen bir y sayısına tam bölünüp bölünmediğini ekrana yazdıran programı yazınız.

## Döngü Deyimleri Soruları:

* 1 ile 1000 arasındaki sayıları ekrana yazdıran programı yazınız.

* 1’den N’e kadar olan tamsayıların toplamını hesaplayan programı yazınız.

* Çarpım tablosunu yazdıran programı yazınız.

* Çarpım tablosunun istenilen kısmını yazdıran programı yazınız. (5 yazınca 5'ler, 10 yazınca 10'lar)

* Kullanıcıdan alınan sayının yine kullanıcıdan alınan üs değeri ile hesaplayan programı yazınız.

* Girilen pozitif bir tamsayının faktöriyelini hesaplayan programı yazınız.

* Girilen sayının asal olup olmadığını hesaplayan programı yazınız.

* 1'den 100 e kadarki asal sayıları hesaplayan programı yazınız.

* Girilen pozitif bir tamsayının tam bölenlerini bulup ekrana yazdıran programı yazınız.

* Girilen sayının asal çarpanlarını hesaplayan programı yazınız.

* 1 den 1000 e kadar olan sayılardan perfect number olanları yazdıran programı yazınız. (ör: 6=1+2+3 tam bölenlerinin toplamı)

* İçi boş kare yazdıran programı yazınız.

* Fibonaci dizisinin ilk 10 elemanını yazdıran programı yazınız.

* Girilen sayının basamaklarını tek tek ayırıp yazdıran programı yazınız.

* Girilen sayının kaç basamaklı olduğunu yazdıran programı yazınız.

* Girilen sayıyı ters çeviren programı yazınız.

* 1 den 1000 e kadarki armstrong sayılarını hesaplayan programı yazınız. (ör: 153 1 in 3. 5 in 3.  3 ün 3. kuvvetlerinin toplamına eşittir denilen sayılardır)

* 1 den 1000 e kadarki palindrom sayıları bulan programı yazınız.(121)

* 1 den 1000e kadar olan sayıların perfect number olanlarını ekrana yazdıran programı yazınız. (basamaklarının faktöriyellerinin toplamı kendisine eşit olan sayılar perfect numberdir.  ör: 145=145 1! + 4! + 5!)
x
