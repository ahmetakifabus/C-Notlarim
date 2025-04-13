# C-Notlarim

Ders 1 (5.06.2021)
---
C nasıl bir dil?
---
Imperative -> Buyurgan 
 
Procedural -> Prosedüral 

Non-Proprietary -> Mülkiyeti yok 

Middle level -> Orta Seviyeli 

Static Typing -> Statik tür kavramı 

General Purpose -> Genel Amaçlı 

Efficient -> Verimli 

Artificial -> Yapay 

Standard - Standart 

Portable -> Taşınabilir 

Expressive -> İfade gücü yüksek 

Programlama dilleri 2 tür olabiliyor;
1) Declarative (Bildirimsel)
2) Imperative 

Imperative dillerde sadece sonucu değil, sonuca ulaşmak için neler yapılacağı da anlatılıyor. C - C++ arasındaki en önemli fark bu. C++ birden fazla paradigmaya destek veren bir programlama dili.
Fakat declarative diller sonuç odaklıdır. (Ne istenildiği söyleniyor)

Assembly dili, makine dilinin komutlara dönüştürüldüğü bir hali gibi düşünülebilir.
Teknik tanıma göre C düşük seviyeli bir dil değil. Düşük seviye derken kastedilen aslında assembly ve altındaki diller. Bu yüzden C'ye düşük seviyeli diyemeyiz. C yüksek seviyeli bir dil fakat daha alt kesiminde. Makinaya yeterince yakın, insana da uzak değil.

- Kuşak diller -> Makina diller
- Kuşak diller -> Assembly diller

Ben 1 dediğimde 1'e dönüşüyorsa makina dili, 2-3'e dönüşüyorsa assembly dili, daha fazla dönüşüyorsa yüksek seviyeli diller diyebiliriz.
C, sistem programlama alanının ana dilidir, mikroişlemci programlama dilidir.

C mülkiyet dili değil!
---
Sahibi yok. C derleyicisi yazmak için kimseden izin almak zorunda değilsiniz. Para ödemek zorunda değilsiniz.
Örnek, java ve C# mülkiyeti var. Python'ın yok.

Genaral Purpose!
---
Genel amaçlı 

Donanımın doğrudan kontrol edildiği uygulamalar (Sistem programlama) 

C'nin dolaylı olarak kullanıldığı diller -> MATLAB ortamında yazılan kod C koduna dönüştürülüyor.

Static tür ve Dinamik Tür
---
Static tür kavramına sahip dillerde çevirici program koda bakarak verinin ne olduğunu anlıyor. (Çeviri sürecinde program biliyor)
Dinamik tür kavramında verinin ne olduğu programın çalışma zamanında belli oluyor. (Çevirici koda bakarak verinin ne olduğunu bilmiyor)

Static tür kavramına sahip dillerin avantajı, kodlama hatalarının daha erken süreçte bulunabilmesidir.

x = 12;
x = 21.84;
x = "ali"

-> Eğer böyle ise bu dinamik tür kavramına sahip bir dildir.
C, sadece static tür kavrmaını destekelrken, c++, C#, java gibi diller dinamik tür kavramını da bellir bir ölçüde destekliyorlar. (Esas olan static tür fakat dinamik türe yönelik araçlar var)

C'de 
x=10;
x=15;
diyebiliriz. Bu onu dinamik yapmaz mı?(X'i float tanımlarsak)
-> X'i float tanımlamak demek zaten onun static tür kavramına sahip bir veri olduğunu gösteriyor.

C, Yapay Bir Dil! (Artificial)
---
İnsanın konuştuğu dile benzerlik sağlamak yerine, uzaklaşmış ve tamamen uydurma kurallar ile bir anlatım benimsenmiştir.
Java, c# gibi diller programcının verimli olması açısından geliştirilmiştir, fakat c ve c++ dillerinin odak noktası programın verimli olmasıdır. (İşlemcinin verimli kullanılması, yapılacak iş daha az işlem ile yapılsın.)

C'den sonra geliştirilen programlama dillerinin çok önemli bir kısmı C'nin sentaksından, genel yapısından, ifade gücünün yüksekliğinden faydalanmıştır.

3.. Kuşak diller
---
3. kuşak diller 3 tane dilden türetilmişler.

- Fortran
- Cobol
- Algol.
    
Günümüzdeki dillerin soy ağacı buraya gidiyor.
 
Fortran -> 1954 yılında geliştirilmiş bir dil.
Formula + translation = Fortran

C'nin doğum tarihi -> 1970

Ders 2 (5.06.2021)
---
C kaynak dosyaları ASCII text file denilen bir formatta. Kaynak dosyadaki her bir karakter 1 byte ile ifade ediliyor.

Uzantısı .h olan dosyalara header file deniyor. (Başlık dosyası)

Bizim kaynak dosyadan C'nin sentaksına uygun olarak oluşturduğumuz metni makina kodlarına dönüştürecek programlara ihtiyacımız var.

Bir dili başka bir dile çeviren -> Translator 

Eğer kaynak dil daha yüksek seviyeli ise -> Compiler(Derleyici)

İlerleyen konularda biz derleyici programın bu işi nasıl yaptığını öğreneceğiz.
Derleyicinin çalıştırıldığı ve bizim kaynak dosyamızı makina kodlarına dönüştürdüğü sürece compile time deniliyor. 
Makina kodu üretildi, işimiz bitti diyemeyiz. Bundan sonra bir program daha kullanmak durumundayız. Bu programa linker deniliyor.(Bağlayıcı)

Neden böyle bir programa ihtiyaç var? (Linker)
---
Derleyici dosyanın girdisi kaynak dosya. (Projemizde birden fazla kaynak dosya olacak)
Bu kaynak dosyalar bizim projemizin birer parçası, fakat derleyici bu kaynak dosyalar arasındaki ilişkiden haberdar değil.

Kaç tane kaynak dosyamız varsa derleyicimizi o kadar çalıştırıyoruz.

Derleyici kendisinden sonra gelen bir bağlayıcı program olduğunun farkında olduğu için bir kaynak dosyadaki bir kod bir başka dosyadaki kodu kullandığında, derleyici üretmek durumunda olduğu kodları üretiyor fakat başka kaynak dosyadaki kodun kullanıldığını anlatmak için bağlayıcı programa bunları birleştirme için referans isimler yazıyor.



Neden 1 kaynak dosya değil de birden fazla kaynak dosya var?
---
-> Kodun mantıksal açıdan diğer işlemelerden izole edilmesini daha kolay test edilmesini, farklı kişi ve şirketler tarafından oluşturulabilmesini, tekrar kullanılabilirliğini sağlıyor.

C'yi kim kodlamış?
---
C bir tanımdan ibaret. C'nin tanımı demek, C dilinin standartları demek. C programlama dilinin kodu yok, dili betimleyen metinler var. bunlara C standartları deniyor.

Kaynak kod -> Makina kodu
---
Her kaynak kodun assembly veya makina kodu karşılığı yoktur. Biz kaynak kodda yapılacak işi betimliyoruz. Bu yapılacak işin kod karşılığında yüzlerce kombinasyon olabilir. Derleyicinin kalitesi burada belli oluyor. Ne kadar az kod ile üretebiliyor ise o kadar kaliteli diyebiliriz.

C/C++ Derleyicileri
---
Bu derleyicilere optimizing compiler deniliyor. Derleyicinin kalitesini etkileyen en etkili faktör code optimization. 

Ders 3 (16.06.2021)
---
İşaretli ikili sayı sisteminde en sondaki bit işaret biti oluyor. 
-> İşaret biti 0 ise sayı pozitif
-> İşaret biti " ise sayı negatif

Bir C derleyicisi ilk olarak ne yapıyor?
---
Derleyici translation unit ile karşılaştığında ilk olarak kaynak kodu token denilen birimlere ayırıyor. Bu işleme tokenizing deniliyor.
Token=Atom
Kaynak kodun derleyici tarafından anlamlı en küçük birimi.
Her şey kaynak kodu tokenlara ayırmak ile başlıyor.
Bu tokenlar belirli kategorilere ayrılıyor.

Tokenlar
---
- Keywords   -> Anahtar sözcükler
- Identifier -> İsimler
- Sabitler   -> Constants
- Operators  -> Operatörler
- String Literals  -> String sabitleri
- Delimeter  -> Ayıraçlar

Anahtar sözcükler 
---
Dil tarafından özel anlam yüklenmiş, özel görevler verilmiş, başka amaçlar ile kullanımı yasaklanmış rezerve edilmiş sözcükler.

İsimler
---
Varlıklara verilen adlar. İsim ve değişken aynı şey değil. Değişkenler sadece ismi olan varlıklardan birisi.

Başka hangi varlıkların isimleri var?
-Fonksiyonlar
-Diziler
..
Sadece değişken ile ilişkilendirilen bir kavram değil. Fonksiyonalrın sabitlerin etiketlerin türlerin isimleri olabiliyor.

Compiler extension (Derleyici eklentisi)
---
Derleyiciler, standart C'nin özellikleri dışında programcının işini kolaylaştırmak için standart olmayan bazı araçlar veriyorlar.

-> GCC derleyicisi 100 den fazla eklentiye sahip.

String Literals
---
Çift tırnak içerisinde yazılanlar.

x = y + 5;

6 tane token var.

"x = y + 5;"

1 tane token var.

Printf -> Identifier (Anahtar sözcük değil)
İsmin standart kütüphaneye ait olması onun bir isim olduğu gerçeğini değşitirmiyor.

biz x = 12; yazdığımızda bir bellek alanına yazma amacıyla erişiliyor ve oraya tam sayı değeri ikilik sayı sisteminde yazılıyor.

Expression (İfade)
---
Sabitlerin, isimlerin yada sabitlerin, isimlerin, operatörlerin bir araya gelerek oluşturduğu birim.

1) ifadenin türü
2) Değer kategorisi (Value category)

-> R Value (Nesne gösteren ifadeler)
-> L Value (Bellekte belirgin bir yere ilişkin olmayan ifadeler)
Bir ifadenin değer kategorisi ikisinden biri olmak zorunda.

Aritmetik ifadelerle oluşturulanlar R value expression.
Değişken isimlerinin oluşturduğu ifadeler L value expression.

- x L value
- x+5 R Value
- 12  R Value

Başına & eklersen hata vermezse L value expression verirse R valu expression.

Constant Expression (Sabit İfadesi)
---
10 * 5 + 20 -> Derleyici derleme zamanında bu ifayenin değerini anlıyor, Hesaplamak için bir zamana ihtiyaç yok.
=70 yazmak ile arasında bir fark yok

x=5 -> ifade
x=5; -> İfade deyimi (Expression statement)


C'nin cümleleri 2 kategoriye ayrılıyor;
---
Declaration (Bildirim) : İsimlerin ne olduğunu anlatır.
Statement   (Deyim) : 

y = x + 5;   ->  x ve y atomlarının birer identifier olduğunu derleme sürecinin ilk aşamasında (tokenizing) anlıyor.
Fakat İfade içindeki isimlerin hangi varlıklar ile ilişkin olduğunun anlaşılması işlemi gerekiyor. Bir ismin neyin ismi olduğunun derleyici tarafından anlaşılması. (Name Lookup)

Biz bir ismi kullanabilmek için o ismi bildirmek zorundayız. Çünkü bir ismi kullandığımız zaman o ismin bildirimi aranacak ve görmediği zaman sentaks hatası verilecek.

Statement ( Deyim)
---
Derleyicinin doğrudan makina koduna dönüştürdüğü C cümleleri.
x = y + 10;
Bu işlemin yapılabilmesi için makina kodlarının yürütülmesi gerekiyor o zaman bu bir deyim.(İsim tanıtılmıyor, doğrudan iş yapırılıyor.)


Ders 4 (23.06.2021)
---

"#" ile başlayan komutlar derleyici programa değil, önişlemciye gönderilen komutlar. (Derleyiciden önce çalışan program, preprocessing)

Bir ismi kullandığınız zaman o ismin derleyici tarafından aranması, bulunması gerekiyor.
"#include <stdio.h>" 
Önişlemci programı bu komutu yürüttüğünde (printf ismini kullandıysak) oraya printf isminin ne olduğunu anlatan kodlar yapıştırılıyor.  Yani derleyici namelookup yapıyor.

Sentaks: Dilin kuralları bütünü

Data Types
---
1) Basic Types
2) User - Defined Types (C'nin bazı araçlarını kullanark kendi değişkenimizi oluşturma)

Basic Types
---
Sizin bir bildirim yapmanıza gerek yok. Bunlar dil tarafından hazır sunulan değişken türleri.

1) integer types
2) floating types



- _Bool  1 byte

- char 1 byte
- signed char 1 byte 
- unsigned char 1 byte

- signed short int 2 byte
- unsignedshort int 2 byte

- signed long int 4-8 byte
- unsigned long int 4-8 byte

- signed long long int 8 byte

- unsigned long long int 8 byte

- signed int 2-4-8 byte
- unsigned int 2-4-8 byte

Soru
---
C'de neden geleneksel olarak 1 byte lık char tüeü yerine 4 byte lık int türü kullanılıyor?
>> İşlemciniz 32 bitlik bir işlemciyse belleğe 4 byte'ın katları şeklinde erişir. 1 Byte ın kullanılması bir avantaj sağlamıyor. 

Soru 
---
Değişken boyutlarının derleyiciler için farklı olması farklı ortamlarda compile edilecek kodlar için sorun oluşturmaz mı?
>> int_32_t >> Taşınabilirlik konusunda destek sağlayan araçlardan biri. ;Bu kodu nerde derlersn derle 32 bitlik işaretli bir değişken. Taşınabilirlik problemi olur ama dikkat edersek olmaz.

Tam sayı türlerinin öz evaladı -> int
Gerçek sayıların efendisi -> double

Bildirim ve Tanımlama (Declaration and Definition)
--- 
Bildirim: Bir ismin derleyiciye tanıtımı
Kod içinde bir ismi kullanabilmemiz için derleyicinin compile time'da bu ismin neyin ismi olduğunu anlaması gerekiyor.

1) İsim arama belirli bir sırayla yapılır (Curly Bracked, Name lookup)
2) İsim arama aranan ismin bulunmasıyla biter ve bir daha başlamaz.

Bir bildirimde ilk olarak yazılan değişkenin türünü anlatan sözcük.

Initialization is not assignment! 
---
İlk değer verme atama değildir.
int y = 5; // ilk değer verme
y = 34; //assign - Atama (Bildirim yok, bu bir ifade)

Değişken ömrü
---
Statik ömürlü değişkenler ilk değer verilmeden tanımlandıklarında 0 ile başlarlar.

		1) Global değişkenler
		2) Statik anahtar sözcüğüyle tanımlanmış yerel değişkenler

		Otomatik ömürlüye değer vermezsen tanımsız davranış olur.

		Defined behaviour->Tanımlanmış davranış->cevap belliyse
		
		Undefined behaviour->Tanımsız davranış >> 
			
			C standartları yazılan bi kodun çalışması durumunda ne olacağı durumuna behaviour terimi ile yaklaşıyor.
			Yazdığın kodun çevrilmiş halinin runtime'da çalışması durumunda ne olacağının garantisi yok.
			Undefined behaviour kesinlikle olmaması gerek.

		Neden c, c++ 'ta böyle bir şey var?

		1) c, c++ derleyicileri optimizing compiler olmaları.

		Doğru çalışsa bile bir sonrakinde çalışma ihtimali yok.
  Standartlar hangi kodların undefined behaviour olduğunu belirtiyor.
		Otomatik ömürlüler ilk değer verilmezse garbage value ile başlarlar.
		Garbage value olması tanımsız davranış değil ama garbage value'yu kullanmak tanımsız davranıştır.

		- Otomatik ömür-- > Akış koda geldiğinde nesne hayata geliyor ve çıkınca çıkıyor.
		- Statik ömür-- > Programın başından sonuna kadar nesne hayatta
		- Dinamik ömür-- > Ne zaman istersek başlatıp bitirebiliyoruz

		Otomatik-- > Yerel değişkenler  
		Statik-- > Static ile tanımlanan yerel değişkenler ve Global değişkenler

		Garbage Value-- > İndetermined Value 
			Garbage value kullanmak undefined behaviour


örnek
---

![image](https://user-images.githubusercontent.com/75746171/140424229-410ec758-9cb9-45c4-8581-6d4d40443689.png)

Açıklama
---
X otomatik ömürlü olduğu için program derleyip çalıştırıldığında x değeri hep 10 olarak yazdırılacak.

x tanımlarken başına "static" anahtar sözcüğünü kullanırsam yerel değilken olacak fakat ömrü static ömür olacak ve her yazdırıldığında değeri 10 artacak.

int x;
x=10;

Eğer bir atama olursa fonksiyıon her çağırıldığında bu kod yürütülecekti.

Ama bur bir bildirim -> 
static int x=10;
X'in static ömürlü bir değişken olduğunu ve hayata geldiğinde 10 değeriyle gelmesi gerektiğini anlatıyor.
Static ömürlü olduğu için hayata 1 kez gelecek.

Ders 5 (24.06.2021)
---

Defined behaviour -> Kodun nasıl çalışacağı dilin kurallarına göre bellidir. (Olması geren durum)

Tanımsız davranış kullanırsak derleyiciye vermiş olduğumuz sözü çiğniyoruz.


Örnek
---
a= f1() + f2();
Hangi fonksiyon daha önce çağırılacak? -> Unspecified behaviour.
Bir derleyicide f1 önce diğerinde f2 önce olabilir.

Derleyiciye güvenerek yazılmamalıdır, taşıyıcılık açısından sorun çıkarabiliyor.

Garbage value Tam anlamı
---
X değişkeni tanımlandığında bellekte rastgele bir alan ayrılıyor. Fakat sen ilk değer atamazsan bu bellekte ayrılan yerdeki daha önceki bilgiler bizim tarafımızdan yazılmış gibi kabul edilecek. Fakat bu bilgiler biz yazmadık. Bu bir tanımsız davranıştır.

Eğer static olarak tanımlarsak bellekteki ayırdığı yere 0 yazmışız gibi kabul ediyor bu yüzden undefined behaviour olmuyor.

---
Static ömürlü değişkenelere ilk değer veren ifaderler sabit ifadesi olmak zorunda. Bu otomatik ömürlüler için şart değildir. Şart değildir fakat tanımsız davranıştır çünkü çöp değeri direkt kullanıyoruz.
int y=x;
Bu hatalıdır. Sabit ifadesi değildir. Syntax hatası.

örnekler
---
signed double x; -> Geçersiz (Gerçek sayı türleri için işaret anahtar sözcükleri kullanılmaz doğuştan işaretli olur)

signed x; -> Geçerli (signed int x olur)

int long unsigned x = 4; -> geçerli


---
Bildirim: İsmin ne olduğunu anlatan cümle.

Eğer bir bildirim sonucunda derleyici bir yer ayırıyorsa o aynı zamanda bir tanımlamadır. Her bildirim bir tanımlama olmak orunda değil ama her tanımlama bir bildirim.


İsimlerin Kapsamı
---
name lookup -> Derleyici compile time'da ismin neyin ismi olduğunu anlama süreci. İsim arama.

Scope
---
Kaynak kodda bildirilen her isim Şu kapsam kategorilerindenbirine ait olmak zorunda.

1) file scope (Dosya Kapsamı)
2) Block scope (Blok kapsamı)
3) Function prototype scope (Fonksiyon prototip kapsamı)
4) Function Scope (Fonksiyon kapsamı)

Örnek
---
int x;

void func(void)
{
Static int y;
}

İkisi de static ömürlü fakat aralarındaki fark birisi dosya kapsamındadır diğeri blok kapsamındadır.

Örnek
---

![image](https://user-images.githubusercontent.com/75746171/140424477-fdfa55b6-81fb-44fe-a029-8eb0319c572c.png)


x'in değeri hep 10, y nin değeri sürekli artıyor. Çünkü x her fonksiyon çağırıldığında 10 değerini alıyor. Ama y hayata 10 değeri ile geldi ve derğini değiştirdiğimizde hala hayatta.

Ayrıca y ismi main fonk. içinde kullanılamaz. Bunun ömür ile değil kapsam ile alakası var.

Ders 6 (12.08.2021) 10.00 
---

int printf = 0;

printf("tahsin onur");

printf bir isim, derleyici bu ismi arayacak ve name lookup bitecek, sentaks hatasının nedeni int türden bir değişkenin isminin bir fonksiyon çağrı operatörünün operantı olması.

Önişlemci programı, include komutunun bulunduğu yere başlık dosyasının içindeki bildirimleri yapıştırıyor.

Printf -> Bu ismi standart kütüphanenin kullanması bunun bir isim olduğu gerçeğini değiştirmiyor.


Fonksiyonlar
---
C'deki temel yapıtaşı. Bir işi yapan kod.

1. Fonksiyonu tanımlamak (İşi yapmasını sağlayan c kodunu yazmak)
2. Fonksiyonu çağırmalk (Bu noktada bu fonksiyon çalışsın)
3. Fonksiyonu bildirmek (Fonksiyon hakkında deleyiciye bilgi vermek, ne olduğunu açıklamak)




Çağrılan fonksiyonun çağıran fonksiyona değer iletmesinin C'de 3 tane yöntemi var.

1. Geri dönüş değeri (Return value)
2. Call by reference (Nesnenin adresini gönderiyor, geri dönüş değeri adrese yazılıyor)
3. Global değişkene değer yazıp okumak

Variyadik fonk. -> Değişken sayıda parametreye sahip fonksiyonlar. (Scanf)

Fonksiyona geri dönüş değeri yazmazsan int yazfdın kabul eder hata vermez ama uyarı verir.

Statement (Deyim)
---
- Expression Statement (İfade Deyimi)
- Compound Statement (Bileşik Deyim)
- Null Statement (Boş Deytim)
- Control Statement (Kontrol Deyimi)


- z = 10; Expression Statement
- ++a; Expression Statement

Comtrol Statement (Küme Parantezi içine alınmış)

Null Statement -> Noktalı virgülün öncesinde ifade olmadan kullanılması

Copntrol Statement
---
En az bir anahtar sözcük içerir, Programın akışını kontrol eden deyimler.


Return Deyimi
---
Geri dönüş değeri olmayanlar için ifadesiz return deyimi - return;

Ders 7 (13.08.2021) 08.00
---

C'de bazı fonksiyonların geri dönüş değeri başarı bilgisidir. Aslında bazı fonksiyonlar bir işi yapmak için vardır. 

Bazılarının geri dönüş değeri int ve başarı bilgisi, 
0 -> başarı bilgisi
non-zero -> başarısızlık bilgisi

C99 standartlarına göre main fonksiyonunda return deyimi koymazsan return 0 yazmış kabul ediliyor.


Fonksiyonun void olması geri dönüş değeri olmadığı anlamına geliyor fakat değer iletmediği anlamına gelmiyor. Adrese yazma yolu ile iletiyor olabilir.

() -> Fonksiyon çağrı operatörü, function call operator

Bir fonksiyon çağrı ifadesi ile neler yapılabilir?
---

max2(x,y) 	-> İfade
max2(x,y);	-> Deyim (İfade Deyimi)

Call by Value - Call by Reference
---

func(x);
Eğer bu fonksiyon çağrısı karşılığı değişkenin değerini fonksiyonun parametre değişkenine kopyalıyorsa (Fonksiyonun parametre değişkeni, fonksiyon çağırıldığında x'in kendisi değil) 
Nesnenin kendisini göndermiyor, kopyasını gönderip üzeirnde çalışıyor.

Call by reference ise nesnenin direkt kendisini kllanıyor.

C'de tüm fonksiyon çağrıları call by value dur.

![image](https://user-images.githubusercontent.com/75746171/140425440-5ce21e78-90a4-4b9e-a180-d3e16c0a219b.png)

Burada x değeri ekrana 10 olarak yazdırılır çünkü fonksiyon çağrıları call by value olduğu için x değerini değiştiremez.

Bir fonksiyon başka vbir fonksiyonun değişkjenine ancak adresi yolu ile erişebilir. Pointer denilen şeyin amacı da budur.

Ders 8 (13.08.2021) 09.35
---
Standart C kütüphanesi nedir?
---
Dil tarafından derleyicilerin size sunulması garantşisi verilen hazırr bazı kodlar.

Başlık dosylarında standart C fonksiyonlarının bildirimleri var, kodları değil (stdio.h)

Bildirim -> bir ismin  ne anlama geldiğini anlatan C cümleleri.

Standartlar printf fonksiyonunun kodunu değil bildirimini (ne olduğunu) verir. Kodunu insanlar yazar.

Ders 9 (13.08.2021) 14.33
---
Karakter Sabitleri
---
C'de karakter sabitlerinin türü int türüdür.
ASCII karakter kodlamasında büyük ve küçük harfler arasındaki fark 32 sayı bunun sebebi yazmayı kolaylaştırmak, büyük yerine küçük yazılması için 5. biti değiştirmek yeterli oluyor.

Karakter sabiti ve string sabiti farklı, string sabiti "" içnde yazılan yazılar.

"adasd" 	String literal
'aasd'  	Character constant

Formatlama
---
Giriş ve çıkış yapılacak verinin insanın anlayacağı forma sokulması.

printf, scanf, - Formattan geliyor.

Output width -  
Fill character - sağa veya sola dayalı.

Fonksiyonda son parametre ... ise variadic function, çağıran tarafın dilediği kadar argnam gönderebilmesini sağlar.

"%"  -  printf için bir alt dil oluşturulnuş. Karakterin formatlama bilgisini gönderiyor. 




Diziler söz konusu olduğunda dizilerin fonksiyonlara call by reference olarak gtirilebilir. Yani fonksiyona yazıyı göndermenin yolu, yazıyı tutan dizinin adresini göndermek.
Yani printf fonksiyonunun parametresinin pointer olmasının sebebi bir yazının adresini istemesidir. Başındaki const anahtar sözcüğü de adresteki nesneyi salt okuma amaçlı erişeceğini göstermesidir. 

%d int türden değerleri 10'luk sayı sisteminde 
%x int-unsigned türden değerkeri 16'lık sistemde
%ld long türden değerleri 10'luk sistemde


Örnek
---
int main()
{
	int = 987123;
	
	printf(%d, printf( %d, printf("%d , x")));
}

printf geri dönüş değeri ekrana yazdırdığı kadarkter sayısı olduğu için ekrana yazılan değer 98712361 olur.

scanf (const char *p, ...)
---

Call by reference olmak zorunda, hangi değişkeni set etmek istiyorsan o değişkenin adresine gönderiliyor. 

Variyadik olma sebebi birden fazla değişkeni tek çağrı ile set edebilmek.

scanf başarı garantisi olan bir fonksiyon değil, değişkeni set etmemiş olacak, çöp değeri ile kullanacak. Bu da bir tanımsız davranış. scanf geri dönüş değeri başarılı olup olmadığını anlatıyor. 

Ders 10 (16.09.2021) 09.15
---

int scanf(const char* p, ...);

1. parametreye gönedrdiğimiz yazı scanf fonksiyonu tarafından parse edilecek (ayrıştırılacak), oradaki formatlama dönüştürücülerinin ne olduğuna bağlı olarak gönderdiğimiz adreslerdeki değişkenler set edilecek. 

Değişkenleri set eden fonksiyon olduğu içiçn call by reference biçiminde çağırılmalı. (Her zaman adres gönderiyoruz.)

scanf geri dönüş değeri başarı ile set ettiği değişken sayısıdır.

scanf("%d%d%d" , &x, &y, &z);

Geri dönüş değeri kaç tane değer set ettiğidir.

Operatörler
---

Her operatörün ürettii bir değer var. Operatörün ürettiği değer yapılan işlemin sonucu.
Atama operatörün ile ürettiği bir değer var. 

Birden fazla operatör olduğunda hangi operatörün ürettiği değer hangi operatörün operandı olacak? (Operatör önceliği)

Bir ifadenin alt ifadelerinin hangisinin daha önce daçıklanacağı unspecified behaviour.


int x = f1() + f2() * 5;

Hangi fonksiyon daha önce çağırılacak?
Operatör önceliği bir işlemin fiziksel olarak daha önce yapıldğı anlamına gelmiyor. 
Operatör önceliği neyi belirliyor?
Birden fazla operatör olduğunda hangi operatörün ürettiği değer hangi operatörün operandı olcağını belirliyor. (Çarpma operatörünün ürettiği değer toplama operatörünün sağ operandı olacak.)

Hangisinin daha önce çağırılacağı unspecified behaviour. 

Standartlar programlama dilini öğrenmek isteyenler için oluşturulan bir döküman değil. Dilin kurallarını anlatan belge. Derleyici yazanların uynması gereken kuralları anlatıyor.

Operatör Tablosu
---
1. ()  []  .  ->
2. +  -  !  sizeof  (type)  & * ++ --
3. *  /  %
4. +  -
5. >>  <<
6. >  >=  <  <=
7. ==  !=
8. &
9. ^
10. |
11. &&
12. ||
13. ?  
14. =  +=  -=  *=  /=  %=  ^=  |=  >>=  <<=
15. ,


+x ve x yazmak arasında değer oarak bir farklılık yok, o zman neden +x yazılır?

x ifadesinin değer kategorisi L value expression ama +x ifadesinin değer kategorisi R value expression.

Yani ifadenin değerini değiştirmeden değer kategorisini değiştirmek istersen +x yap.

Binler  x / 1000;
Yuzler  x % 1000 / 100;
Yuzler  x / 100 % 10;
Onlar   x % 100 / 10;
Birler  x % 10;

++ operatörlerin operandları L value expression olmak zorunda. ++5 ifadesi sentaks hatası. Çünkü L value expression olmak zorunda. 

Ön ek vay son ek kullanımındadki fark oepratörün ürettiği değerde.

Atama operatörünün ürettiği değer nesneye atanan değerdir.


Örnek:
---
int x, y, z, t;

printf("4 sayi giriniz: ");
scanf("%d%d%d%d", &x, &y, &z, &t);

int pos_count = (x > 0) + (y > 0) + (z > 0) + (t > 0);

printf("%d tanesi 0'dan büyük\n", pos_count);

Karşılaştırma operatörlerinin ürettiği değer 1 veya 0 olduğu için bu örnekte yazdırılan sonuç pozitif sayı sayısı olur. 

Ders 12 (17.09.2021) 13.56
---

min += sec / 60;
sec %= 60;
hour += min / 60;
min %= %60;
day += hour / 24;
hour %= 24;

Virgül operatörü
---
Sequence point (Yan etki noktası)

++x; 
X'in değeri ne zaman değişecek. Bu kodsal noktalara sequence point deniliyor. 

Bir yan etki noktasından önce yan etkiy emaruz kalmış nesneyi tekrar kullanırsak tanımsız davranış oluşur. 

yani: 
y = x++ + x; Undefined behaviour

yada :

int x = 10;
int y = (x = 7) + x;

Yan etkiye maruz kalmış (x = 7) ama aynı ifade içinde sequence point geçmeden bu değer kullanılmış. Undefined behaviour.

Diğer dillerde tanımsız davranıl yok fakat neden C'de var? Diğer dillerde bu kadar kod optimizasyonu olmadığı için. Derleyici diyor ki, ben kodu öyle bir şekilde derleyecem ki verimli çalışacak, fakat tanımsız davranış olmama koşulunu istiyor. Çünkü optimizasyon yaparken tanmımksız davarnış olmadığına güvenerek yağpıyor. 


Virgül operatörünün sol oeprandından sonra bir yan etki noktası olması özelliği ne anlama geliyor?

++a;
++b;
++c;

++a, ++b, ++c;

Yazmak arasında hiçbir farkl yok. Yani ifade deyimleri virgül operatörü ile birleştirilebilir.

Her operatör bir değer üretir, virgül operatörü de bir değer üretir. Virgül operatörünün ürettiği değer sağ operandın değeridir.

Örnek:
---
int a, b = 10, c = 20;
a = (b , c);

Parantez içi ifadenin değeri 20. Yani a'ya atanan değer 20.

return ++g , x;
Önce g değeri arttırılacak sonra x değeri geridönüş değeri olacak.

5.6 ifadesinin değeri 5.6
5,6 ifadesinin değeri 6

int a[10] = {(0,1,2,3,4,5,6,7,8,9)}

a dizisi = (0,0,0,0,0,0,0,0,0,9)

int x = 1'000'000;
int y = 1'000'000;
double dval = 3.5;

printf("%f\n", x * y * dval);
// burada (x*y) çarpma operatörünün sol operandı olacak ve işlem int türünden gerçekleşecek

printf("%f\n", dval * x * y); 
// Fakat burada işlem double türünden gerçekleşecek. Doğru değer budur.

Bu iki işlemin sonucu aynı değil.

Örnek
---
![image](https://user-images.githubusercontent.com/75746171/140427339-b90744c6-646b-4155-8855-a6151daddec0.png)

Not:
---

![image](https://user-images.githubusercontent.com/75746171/140427368-419117d5-d62c-4ca5-a90c-eaec48aa0972.png)

Burada if içine girecek çünkü fonksiyon isimleri fonksiyonun adresine dönüştürülüyor ve bu adresler lojik doğru olarak yorumlanıyor. (Always true)

Ders 13 (17.09.2021) 16.58
---
int x = 5;

if (x=3);
	printf("dogru\n");
	
if sonundaki noktalı virgül aslında if'in doğru kısmını oluşturuyor. Bu yüzden printf çalışır.

Boş deyim yazılabilen her yere boş blok ta yazılabilir {}

Örnek
---
Noktalı virgül kullanmadan merhaba dunya yaz.

if (printf("merhaba dunya\n"))
  {}

while (!printf("merhaba dunya\n"))

getchar, putchar
---
printf ve scanf formatlı giriş çıkış fonksiyonları. Formatsız olan karakter bazında giriş çıkış yapan fonksiyonlar var.

int getchar(void);  Standart inputun bufferındaki tam sayı değerini okuyor.

int putchar(int);


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/140427884-52d03bba-007b-41a4-82b4-6b945f567190.png)

abc345 yazdığında 97 98 99 yazacak. (harflerin karşılığı) Ve 345 standart input buffer'ında durmaya devam edecek.

Çağırılan getchar fonksiyonları acb'yi standart inputun buffer'ından çıkartacak ve sıra scanf e geldiğinde standart inputun bufferında abc olmadığı için 345 alacak.

Yani scanf ve getchar aynı buffer ı kullanıyor.

while ((c = getchar() != '\n')

=>> standart inputun bufferından new line gelene kadar tüm karakterleri alır.

Standart inputun bufferındaki karakterleri tek tek almak istediğiniz yer yerde kullanabilirsiniz.

int _getch(void); // line buffered değil echo vermiyor.
int _getche(void); // line buffered değil echo veriyor.

getchar std newline istiyor echo veriyor
getch   std değil newline istemiyor echo vermiyor
getche  std değil newline istemiyor echo veriyor.

int putchar(int);
Standart outputa hangi karakter basılmışsa aynı değeri gönderiyor. Hata olması durumunda -1 değeri gönderiyor. Sadece karakter görüntüsü yazıyor.

Bazı fonksiyonlar - ctype
---

int isupper(int c;)
Büyük harf karakteri mi?
Büyük harf ise nonzero, değilse 0.

int islower(int c;)
Küçük harf mi?

int isalpha(int c;)
Harf karakteri mi?

int isdigit(int c;)
Rakam karakte mi?

int isalnum(int c;)
Alpha numeric karakter mi?

int isxdigit(int c;)
Hexadecimalde basamak gösteren karakter mi?


int isspace(int c;)
Whitespace karakter mi?
'\n' ' '  '\t'  '\V' '\f' '\r'


int ispunct(int c;)
Görüntüsü var ama harf ya da rakam değil.

int isprint(int c;)
Görüntüsü olan karakter. ' ' Boşluk karakteri dahil

int isgraph(int c;) 
' ' Boşluk dahil değil

int isblank(int c;)
Boşluk veya tab karakteri mi?


int iscntrl(int c;)
Görüntüsü olmayan karakterler

Ders 14 (18.09.2021) 15.00
---

int toupper(int);
Büyül harfe dönüşü yapan fonksiyon
Küçük harf karakteri olmayan bir sayıyı gönderirsem aynı sayıyı geri döndürüyor.

int tolower(int)
Küçük harften büyük harfe dönüşüm yapan fonksiyon.

Ternary operatörü (Koşul)
---
op1 ? op2 : op3

m = a > b ? a : b * 5;

a, b'den büyükse m'ni değeri a, büyük değilse m'nin değeri b * 5 ifadesi.

isleap(y) ? 29 : 28;

y artık yıl ise değeri 29 aksi halde 28.


Örnek:
---
int x;
int a;

printf("Bir tam sayi girin: ");
scanf("%d", &a);

if (a == 5)
	x = 7;
else if (a == 9)
	x = 27;
else if (a == 27)
	x = 19;
else
	x = -1;
	
printf ("x = %d\n" , x);

Bunu yazmak yarine şunu da yazabiliriz:

x = a == 5 ? 7 :
a == 9 ? 13 :
a == 27 ? 19 : -1

printf ("x = %d\n" , x);

şöyle de yazılabilir:

x = a == 5 ? 7 : (a == 9 ? 13 : (a == 27 ? 19 : -1));



![image](https://user-images.githubusercontent.com/75746171/140499614-e5b84156-2645-474e-8fb3-b5f915b807e6.png)



Loop Statements (Döngü Deyimleri)
---
Bir kod parçasının bir koşula bağlı olarak yinelenmesinmi sağlayan kontrol deyimleri.

while 
do while
for

Yardımcı deyimler: break, continue

Ders 15 (18.09.2021) 21.35
---
Maximum munch kuralı: En uzun atom
- Tokenizing ile ilgili bir kural.
- Tokenizing yaparken en uzun atomu alıyor.

int x = 5;
int y = 9;
int z = x+++y;

printf("x = %d\n", x);
printf("y = %d\n", y);
printf("z = %d\n", z);

6,9,14 çıktı.

ctrl L -> satırı sil
ctrl D -> Satırı kopyala yapıştır aşağıya
shift + alt -> dikey seç

for statement
---
for(;;)

- İlk aralıkta herhangi bir ifade olmak zorunda değil. Föngü öncesine yazılabilir.
- 3. ifadeyi silersem döngü sonuna yazarsam herhangi bir anlam farklılığı olmayacak.
- 2. ifadeyi yazmazsan oraya lojik doğru ifadesi yazmış olursun.

Ders 16 (19.09.2021) 08.53
---
- Tekrar edin
- Kodları yeniden yaszın
- Ödev sorularını yapmaya çalışın
- Programlamaya ilişkin klasik kaynakları okumaya başlayın
- stackoverflow sitesinde C ile ilgili soruları cevapları okuyun
- quoura'da C ile ilgili yazan yazıları takip edin
- hackerrank sitesine gir

int factorial(int n)
{
	return n < 2 ? 1 : n * factorial(n - 1);
}


Ders 17 (19.09.2021) 10.42
---

Fonksiyon bildirimleri
---

void func(int x);

Program akışının runtime da bu fonksiyonun koduna gitmesi için gerekli kodları derleyici üretiyor. Fonksiyona giriş kodları.
Ve çıkış kodlarını da üretiyor. 
Araya da referans bir isim yazıyor (external reference)

Derleyici hiçbir şey atamıyor, derleyici sadece makina kodu üretiyor. Yani fonksiyonun geri dönüş değerinin bir adrese yazılacağını biliyor ve oraya yazacak şekilde bir kod üretiyor.

int func(int x, int y);
int foo(int x);
double f(void);

int main()
{
int x = func(10,20);
int y = foo(x);
double d = f();
}


Linker bu fonksiyonların derlenmiş halini arayacak ve bulamayınca hata verecek yani hatayı linlker veriyor.

Bağlayıcı programın kaynak kod ile bir ilgisi yok, derlenmiş kod ile çalışıyor. Linker çalıştırılacak kodları birleştiriyor. Derleyici fonksiyonun geri dönüş değerinin nereye yazılacağını belirliyor ve kodu ona göre üretiyor. 


Önişlemci komutlarının yazılması programı yavaşlatmaz çünkü içinde sadece bildirimler var.

Derleyicide stdio.h 'da bildirilen fonksiyonların tanımları değil onların derlenmiş halleri var bunlara obje dosyalar deniliyor.

Ders 18 (19.09.2021) 14.31
---

Önişlemci komutları
---
- Derleyicidn önce çalışan ayrı bir program.
- Girdisi kaynak dosya çıktısı derleyicinin girdisi. (Translation unit)

#include
#define
#undef
#if
#else
#elif
#endif
#ifdef
#ifndef
#line
#error
#pragma


Koşullu derleme bloğu

#ifndef 
-
-
#endif

#define önişlemci komutu
---
- Bir isim önişlemci programa tanıtılması.
- Buna macro denir.
- #define	MAX 	100
- Max gördüğün her yerde 100 yazıyor.

Macro kullanma amacaı
---
Macro yerine neden bir değişken  tanımlamıyoruz?
- Bunlar farklı araçlar. Değişkenler bellekte bir yer kaplayacak fakat macroda makina kodunun bir parçası haline geliyor. 

Ders 19 (19.09.2021) 15.54
---
Fonksiyonel makrolar
---
#define sum_square(a,b)		((a) * (a) + (b) * (b))

int main()
{
int x, y;
printf("iki tam sayi girin");
scanf("%d%d", &x, &y);

z = sum_square(x,y);
}


Fonksiyonel makrolar ve foksiyonların karşılaştırılamsı
---
- Makrolar kaynak kodu büyütme eğiliminde
- Programın hızlı çalışmasıyla derlenmiş kodun büyüklüğü arasında doğrudan bir ilişki yok. Daha hızlı çalışan bir kod olabilir fakat makina kodu daha fazla yer kaplıyor olabilir.
- Makronun hızlandırma nedeni fonksşyona girii ve çıkış kodları olmuyor.
- Makrolar türden bağımsız.
- Makro kullanımı durumunda debugger desteği daha az olablir.
- Makrolarda kodlama hatası rüski daha yüksek.
- Fonksiyonlar türe bağlı
- Fonksiyıon adresi kullanılan temalarda makrolar kullanılamaz (Callback function)

Preprocessor Operators
---
#operatörü		String yapma operatörü (Stringification)
##operatörü		Atom yapıştırma operatörü (Token pasting)	
defined operatörü

#x = "x"

Örnek:
---

#define 	iprint(x)	printf("%d\n", x)

int main()
{
int a = 10;
int b = 7;
int c = 21;

iprint(a);
iprint(a + b);
iprint(a * a +  b * b + c * c);

}

## operatörü

(a##b) = ab

Örnek:
---

define uni(a,b)		a##b

int main()
{
int counter = 0;
uni(co, unter) = 20;
//counter = 20;
}


Conditional Compiling
---
Koşullu derleme

undef
if
else
elif
endif
ifdef
ifndef



#if NEC > 1000

#endif


Ders 20 (20.09.2021) 06.45
---

ifdef : if defined
---
Makro define edildiyse önişlemci ifdef içine girecek.

ifndef: if not defined
---
Önişlemcinin kod bloğuna girmesi için makronun tanımlanmamış olması gerekiyor.

if defined EMRAH !defined FURKAN
	int a[1200];
endif

Multiple Inclusion Guard
---
![image](https://user-images.githubusercontent.com/75746171/140502940-b5aa5586-835f-4e0f-8a2f-4b1f086fd9b9.png)



Değişken isimleri programın çalışma zamanında bellekte yer kaplamaz. Varlıklara verilen isimler bizimle derleyici arasında bir iletişim yolu. Ürettiği kod olarak bakarsak bu nesneler aslında bellekteki bloklar. Derleyici kod üretirken adresleri kullanıyor. Yani değişken isimleri programın çalışma zamanında bellekte bir yer kaplamıyor.



Stdio include edince program yavaşlamıyor mu?
---
Hayır çünkü başlık dosyaları içinde tanımlamalar yok bildirimler var. Derleyici bunları sadece derleme zamanında kullanıyor.


#undef NEC 
- nec makrosu tanımlanmamış kabul edilecek (Daha önce tanımlanmış olsa bile)


Örnek:
---
#define		SIZE	100

#define 	SIZE	500

//tanımsız davranış
Bir makronun farklı iki şekilde define edilmesi.
- Var olmayan bir makroyu undef etmek tanımsız bir davranış değil. Önlem almak için yapılabilir.
- Önişlemci için scope kavramı yok, bu kavram derleyici ile ilgili.

Dil tarafından tanımlanmış makrolar (Define edilmese bile)
---
- __LINE__ Satır numarası ile yer değiştirecek.
- __FILE__ Hangi kaynak dosya içerisinde kullanılmışsa o kaynak dosyanın ismi olan string ile yer değiştiriyor.
- __DATE__ Derleme yapılan tarih ile yer değiştirecek
- __TIME__ Saat ile değiştirecek.
- __STDC__ Bir yer değiştirme makrosu değil. C derleyicisi ise iş yapılması için kullanılıyor.
- __func__ fonksiyonun ismi ile yer değiştiriyor.


Ders 21 (20.09.2021) 
---
'A' C'de karakter sabitlerinin türü int

swith(integer expr){
case 1:
	statement1;
case 2:
	statement 2:
}

Ders 22 (20.09.2021) 15.01
---
Derleyicilerin "kodların bağlanması için" linker programınba hitaben obje kod içine (özel bir notasyonla) yazdığı isimlere "external reference" denir.

Kaynak kodu olmayan bir fonksiyonu çağırdığınız zaman sentaks hatası almazsınız, ama link aşamasında hata alırsınız.

Tür dönüşümleri
---

![image](https://user-images.githubusercontent.com/75746171/142155963-1439ec82-7ff4-4f33-be00-1c00a0b445ba.png)


![image](https://user-images.githubusercontent.com/75746171/142155994-eeb7460f-8e81-44a4-8b2f-82c10f9ce3aa.png)


![image](https://user-images.githubusercontent.com/75746171/142156022-2c6a85c6-fe15-480e-8723-4077dcf6be25.png)


![image](https://user-images.githubusercontent.com/75746171/142156043-c03c77fd-66fb-4a8b-b77c-924f2a4cfa4f.png)


Atama Tür Dönüşümleri
---

int x;
x= expr;

expr hangi türden olursa olsun tür dönüşümü kendisine atama yapılan nesnenin int türüne yapılacak.

type cast operator (Tür değiştirme peratörü)
---
Bir ifadenin kendi türünden değil başka türdenmiş gibi işleme sokulmasını talep ediyoruz.

- (int)dval
- double dval = (double)x / y;

Tür dönüştürme operatörü kalıcı değil.

Ders 23 (20.09.2021) 17.35
---

Rastgele sayı üretimi
---
![image](https://user-images.githubusercontent.com/75746171/142156815-2d810df6-44ed-4d96-952f-8c915745db08.png)


Program baştan başladığında zarlar hep aynı gelecek. 

Farklı bir zincir oluşturmak için:
Gerçek rastgele sayı üreticisi kullan. get_true_random_number(void);

![image](https://user-images.githubusercontent.com/75746171/142156882-0da0ae6d-b694-43b2-adcc-d7ec1f2a21a9.png)

Ders 24 (21.09.2021) 11.02
---
![image](https://user-images.githubusercontent.com/75746171/142156975-871c568f-4f63-4b91-b3ff-fcb4d50c3eae.png)

Veri yapıları (Data Structure)
---
Birçok problemde bizim verilerimiz var. Bu verrileri işleme sokabilmek için bellekte tutmalıyız. Bunların bellekte nasıl tutulduğu bilgisine veri yapısı deniliyor.

- Arrays
- Heap
- Hash Table
- Graphs
- Heap
- Trees
- Linked Lists
- Deque

Diziler 
---
C'de dizilerde ekleme silme işlemi yok.

[] index operatörü. Operatör öncelik tablosunda 1. sırada.


int a[100];
int x,y,z,t;

Aralarındaki fark derleyici dizi için tek bir bellek bloğu ayırıyor. diğerinde ise ardışık olmak zorunda değil, derleyiciye bağlı.

- [] operatörü ile oluşturulan ifadeler her zaman L value expression.
- Dizi isimleri hiçbir zaman atama operatörnün sol tarafında olamaz.

- Bir dizi ismi bir ifade içide kullanıldığında (Bir iki istisna haricinde) her zaman dizinin ilk elemanının adresine dönüştürülür.

Yani:

int a[10];

a yazmak ile &a[0] yazmak arasında bir fark yok.

Ders 25 (21.09.2021) 14.10
---

![image](https://user-images.githubusercontent.com/75746171/142157187-c2c7374d-9564-4e96-9d46-3bda08dd33ba.png)


Dizilere ilk değer verilmesi
---
- Dizi boyutunu yazmak zorunda değilim.

int a[20] = { [5] = 67, [3] = 45, [1] = 11 };

- Burada değer verilmeyen elemanlar 0 değeri ile başlıyor.
- a'nın içi boş ise dizinin boyutu da 6 olur.

 a[i] = i[a] (Pointerlar ile ilgili bir kural)
 
 Sizeof OPeratörü
 ---
 - C'de anahtar sözcük ile ifade edilen tek operatör.
 - Bir sabit ifadesi oluşturuyor.
 - Bir türün storage ihtiyacının kaç byte olduğunu hesaplıyor
 - Elde edilen değer bir tam sayı değeri ve bu değer bir türün bellekte kaç byte yere ihtiyacı olduğu değere eşit.
 - Ürettiği değer işaretsiz bir tam sayı türü. (Derleyiciye göre değişir.)
 
- sizeof (int), Bunun değer sistemdeki int türü için gerekli olan storage ihtiyacı
- int a[sizeof(double)] = { 0 }; // Hata değil çünkü ifade bir sabit ifadesi.

![image](https://user-images.githubusercontent.com/75746171/142157377-4f29d25d-c7da-4c88-ace2-c6e22b15a010.png)

- Bazı durumlarda bir ifadedeki işlemler için derleyici işlem kodu üretmiyor.
- Yani sizeof(++x). sizeof oepratörünün operandı olan bir ifade için derleyici işlem kodu üretmiyor. Sadece tür bilgisi olarak bakıyor.
- sizeof içine bir fonksiyon yazdığın zaman da fonksiyon çağrılmayacak.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/142157485-1a38a945-322e-48ce-babc-c39b32ba88c2.png)

Örnek
---
![image](https://user-images.githubusercontent.com/75746171/142157650-bf19ab08-8fd3-4bb5-b785-4192548e19c9.png)

 Örnek:
 ---
![image](https://user-images.githubusercontent.com/75746171/142157688-7f27a890-7564-44aa-8cac-c4ef172b3c2d.png)


Ders 26 (23.09.2021) 14.22
---
![image](https://user-images.githubusercontent.com/75746171/134501785-d080463b-818d-40f3-8392-78d7f50377ad.png)

Koşul operatörünün 2. ve 3. operandları arasında da tür dönüşşümü söz konusu yani içerdeki ifade double türünden, çıktı olarak 8 alırız.

![image](https://user-images.githubusercontent.com/75746171/134502026-5988a770-52c1-4e45-9a1d-e30669853732.png)

C ifadesinin türü char fakat +c ifadesi ile int dönüşümü oluyor. Çıktı olarak 4 alrıız.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/134502795-4351cf59-3668-4a24-84c5-49faef0cd81b.png)

Bir rastgele dizideki unique elemanları yazdıran kod.

Subsequence
---
Bir dizinin içinde ardışık n tane elemanın oluşturduğu dizi.

Örnek
---

![image](https://user-images.githubusercontent.com/75746171/134504065-8bf4ca57-1a41-4c5e-8cfb-875de787c4e4.png)

Çıktısı:

![image](https://user-images.githubusercontent.com/75746171/134504134-4f1889c3-92ce-4a83-8639-048b71926dc1.png)

Farklı bir yazılış biçimi:

![image](https://user-images.githubusercontent.com/75746171/134504250-10de6e7e-2a19-43b6-a498-c9b283f78e4d.png)

Örnek:
---
Küçükten büyüğe sıralama yap

![image](https://user-images.githubusercontent.com/75746171/134508490-5803ab6a-db40-4004-b8c4-4fb374a6ab1b.png)

Örnek:
Tekler başta ve kendi içinde sıralı
Çiftler başta ve kendi içinde sıralı

![image](https://user-images.githubusercontent.com/75746171/134509248-14cdf1e4-46e2-452f-8795-3c565b890a2d.png)

Ekran çıktısı: 
![image](https://user-images.githubusercontent.com/75746171/134509365-114818eb-a11c-4d9d-ab20-81a35cd80761.png)


Örnek:
---

2 diziyi birleştirme sıralı şekilde

![image](https://user-images.githubusercontent.com/75746171/134511229-aa59d925-bd43-45ad-b740-86957d17b234.png)

2 dizinin elamanlarını karşılaştırıp küçük olanı al ve indeksini 1 arttır.

Binary search algoritması
---

Sıralı bir veri yapısında bir değer aramaya yönelik. Aradığım değerden büyük mü küçük mü? Buna dayanarak eleme yapıyor.

Ders 27 (29.09.2021) 17.50
---

Partitition point
---
Koşulu sağlamayan ilk terimin konumu. Tekelr başta çiftler sonda olacak ise bunu bozan ilk terim.

- Dizide BABA yazısını tutmak demek dizideki her bir elemanında BABA yazısı karakterlerinin kodlarını tutmak demek.

Null turnated byte stream (NTBS)
---

Yazının son karakterinden sonra başka karakter olmadığını belirtmek için dizinin o elemanına özel bir değer atanıyor. Bu değer null charavter. Değeri 0 olan tam sayıdır aslında. '\0' olarak yazılır.

![image](https://user-images.githubusercontent.com/75746171/135308108-5e6719b9-b7df-4bb5-82d7-05936d54cb8c.png)

Doğru şekilde can yazısını tutuyor diyemeyiz. 3 indexli eleman çöp değerdedir.

![image](https://user-images.githubusercontent.com/75746171/135308580-0c813f4e-2542-4dc4-9261-59d24c3441e5.png)

Tanımsız davranış yok. Dizinin tüm elemanları zaten 0'dı. İlk 3 karakteri değiştirdik.

![image](https://user-images.githubusercontent.com/75746171/135309197-ab147dea-0f8f-4e36-8e2e-3f2189e98c15.png)

Sentaks hatası, dizinin ismi hiçbir zaman atama operatörünün sol operandı olamaz.

Bu ikisini karıştırma
---
- '0' sıfır karakterinin kodu ASCII 48
- '\0' null karakterinin ASCII kodu 0

![image](https://user-images.githubusercontent.com/75746171/135310243-88972908-f115-495d-8467-01e47a80e40a.png)

Dizinin boyutu belirtilmedi. Yani dizinin son karakteri null karakter değil. Tanımsız davranış.

![image](https://user-images.githubusercontent.com/75746171/135310390-f6326fd1-1086-4c4e-af6c-830625604a25.png)

Bu şekilde tanımsız davranış ortadan kalkar.

![image](https://user-images.githubusercontent.com/75746171/135312587-fa861a1b-2eaf-4ed7-93e1-01cd3e27d1c8.png)

Bu durumda ise dizinin elemanlarına sırasıyla yazının karakterleri ile ilk değer verilmiş oluyor.

![image](https://user-images.githubusercontent.com/75746171/135313209-a0b69c92-2f8e-44e3-8e99-ff7b6e30bdff.png)

C++ 'ta sentaks hatası. C'de geçerli fakat sonunda null karakter yok.

![image](https://user-images.githubusercontent.com/75746171/135313507-6d8a8bfd-8600-484d-8680-f05ef086bbb4.png)

Dizinin ismi aslında dizinin adresine dönüştürülüyor, scanf'e adres gönderiyor. Dizinin ilk elemanının adresi. Yani &str[0]

 Puts
 ---
 Sadece yazıyı yazdırıyor, standart inputa new line veriyor.
 
![image](https://user-images.githubusercontent.com/75746171/135318886-d2d33788-f19f-43aa-916f-8442f44d7e51.png)

çıktısı: 

![image](https://user-images.githubusercontent.com/75746171/135318983-f06959c7-8d3b-4a6d-9024-5ff887e1e0b8.png)

Örnek
---

![image](https://user-images.githubusercontent.com/75746171/135319696-cec1a85c-05b7-432c-890c-38b8aef9861f.png)

Yazılan yazının uzunluğunu verecek.


![image](https://user-images.githubusercontent.com/75746171/135323733-00a0ed89-f67b-491e-9447-bc8facfe30d2.png)

Karakterden kaç adet olduğunu veriyor.

Örnek Mülakat:
---

Yazıdaki tüm karaakterlerden kaç tane olduğunu yazdıracak.

![image](https://user-images.githubusercontent.com/75746171/135324483-8cffe88d-c115-47a2-adac-2d1f71ad731e.png)

Örnek : Bir karakteri silen kod
---

![image](https://user-images.githubusercontent.com/75746171/135325324-bf5bf4b0-6554-43e0-9efc-fe6462311e17.png)

Örnek : Dizinin elemanlarını takas ettiren kod
---

![image](https://user-images.githubusercontent.com/75746171/135326512-bc9fdc92-dc26-4e83-b90d-8b827ca2ca14.png)


![image](https://user-images.githubusercontent.com/75746171/135326592-81efa050-8f0b-46fb-8ab6-a616d584fe08.png)

Örnek : Yazıyı tesr çevir
---

![image](https://user-images.githubusercontent.com/75746171/135327179-0ff72741-2cf0-4937-8886-1afdc5411ee6.png)

![image](https://user-images.githubusercontent.com/75746171/135327233-0d1c8b7d-2701-4f01-afe1-40fa92362806.png)

Örnek: Yazının palindrom olduğunu anla
---
![image](https://user-images.githubusercontent.com/75746171/135328037-dd330927-f204-471f-ad36-930889f242e2.png)
![image](https://user-images.githubusercontent.com/75746171/135328085-9455ca9f-b954-49f2-9c2b-7968de403b94.png)

![image](https://user-images.githubusercontent.com/75746171/135328149-fc0d50a3-968d-48cb-8a0c-60307d995fa0.png)

Örnek: Kelime sayan kod
---

![image](https://user-images.githubusercontent.com/75746171/135328757-9ec4339f-facd-43b5-9fdb-0d6f68556b5c.png)
![image](https://user-images.githubusercontent.com/75746171/135328930-2b1c20c0-119a-4610-8959-0055ccbb039b.png)

Ders 28 (29.09.2021) 22.31
---

Örnek: İki yazının eşitliğini sınamak
---

![image](https://user-images.githubusercontent.com/75746171/135337052-5aff6cbe-8694-456b-8d6d-0bf945eafe99.png)

![image](https://user-images.githubusercontent.com/75746171/135337086-e47f108f-f05f-4089-ba4e-01cd24c861cc.png)

Örnek: Yazının tersini kopyalamak
---

![image](https://user-images.githubusercontent.com/75746171/135338580-ceff9afd-a657-4dce-978f-5c3150d0147e.png)

![image](https://user-images.githubusercontent.com/75746171/135338637-38ff8146-e7d1-4787-a13f-1c0ba800ba7c.png)

Örnek: Sayının tersi
---

![image](https://user-images.githubusercontent.com/75746171/135340701-88824f0f-9244-4ff9-aead-a4c10c01b6f3.png)

![image](https://user-images.githubusercontent.com/75746171/135340747-d1e9c198-535a-4b91-ae23-48c9e17c3113.png)


inline -> Fonksiyonun çağırıldığı yerde kodu yerleştir demektir.


Pointers
---

T x;

- Eğer bir ifade T türünden bir nesnenin adresi anlamına geliyorsa o ifadenin türü T * kabul ediliyor.
- int türden nesne adresi anlamına gelen ifadenin türü int *
- int türünden bir nesnenin adresi olan ifadenin türü farklı bir tür, double türünden bir nesnenin adresi olan ifadenin türü farklı bir tür. 
- Yani farklı türden nesnelerin adresleri farklı türdür.

int* ptr;
- // ptr, int türden bir nesnenin adresini (değer olarak) tutacak bir nesne.


Ders 29 (30.09.2021) 01.26
---

int* ptr; 	// ptr is a pointer to int

... türünden bir değişkenin adresini tutacak bir değişken!

- Global değişkenler ya da static yerel değişkenler ilk değer vermezsek özel bir adres sabiti ile hayata başlıyorlar. Bu adres sabitine null pointer deniliyor.

Pointerlar 2 ayrı kategoriye ayrılıyor.
---
- Object pointers (Nesne adresleri)
- Function pointers


- Nesne adresleri hangi türden olursa olsun aynı miktarda yer kaplıyor. (4 byte, visual stdio)


int* p1, p2;
- Burada p1 int* türünden fakat p2 int türünden tanımlanmış oluyor.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/135358403-a853b1b9-8219-4851-9892-fa004f970c44.png)

Yapılmaması gerek bir hata, fakat sentaks hatası değil.

Pointer Operators
---

![image](https://user-images.githubusercontent.com/75746171/135358753-e754072a-1047-429c-b312-366bbed7c40f.png)

Adress of operators
---

- Sağdan sola öncelik yönüne sahip. 
- Adres operatörünün operandı sol taraf değeri olmak zorunda.
- Adres operatörü ile oluşturulan ifadeler sol taraf değeridir.

&x = x'in adres değeri.

Örnek:
---
int* ptr = &x; //ptr değişkenine x nesnesinin adresi değeri verildi. Bu ilk değer verme olayıdır.

ptr = &y; //Bu ise atama olayıdır.

Burada ptr'nin değeri x isimli değişkenin adresi ise bunun anlamı "ptr x'i gösteriyor" demektir. (ptr points to x)

![image](https://user-images.githubusercontent.com/75746171/135359890-2fc32044-800b-4860-a825-869052d280cc.png)


![image](https://user-images.githubusercontent.com/75746171/135360793-7b09079b-9ade-451a-bfe2-7a6310c3089d.png)

Array decay, pointer'a dizi atamıyor. Dizinin ilk elemanının adresine dönüşen değeri atıyor.

Soru:
---
Array decay olmayan durumlar?

- sizeof operatörü
- 

![image](https://user-images.githubusercontent.com/75746171/135361137-0ffc23f4-c66a-400c-a688-21c49cc7c81e.png)

- Printf işlevi ile bir adresi formatlı olara std. çıkış akımına yazdırabiliriz.
- Burada kullanılan conversion specifier %p


![image](https://user-images.githubusercontent.com/75746171/135361377-74e3845a-f661-4845-90d9-babe5750736a.png)

Bir dizinin adresi = Bir dizinin ilk elemanının adresi

(*) Operatörü
---
Operandı adres olmak zorunda.

![image](https://user-images.githubusercontent.com/75746171/135458589-07e92bdb-677d-46f6-bd05-bc7a3dbede48.png)

*x	hata
&*x	hata değil
*ptr	hata değil
*a	hata değil

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/135459912-43558f9a-68fb-4375-9e6d-bf499e32493f.png)

![image](https://user-images.githubusercontent.com/75746171/135459947-9257bf6f-39c1-4305-8777-558973d2190b.png)

![image](https://user-images.githubusercontent.com/75746171/135460180-9579e86a-9ec9-4372-b889-e0e168927dce.png)

![image](https://user-images.githubusercontent.com/75746171/135460214-c8e916ce-b4cf-4de5-8266-38a5eccb43b0.png)

- C'de tüm fonksiyon çağrıları call by value dur.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/135478264-0c7575b0-2745-43dd-bb17-4b0176ac14c3.png)

![image](https://user-images.githubusercontent.com/75746171/135478567-b880cbe4-8672-44cb-a647-c5228c205c65.png)

- Burada a'nın kendisini değil, a'nın değerini fonksiyona gönderiyor. Yani a değişmiyor.
- Nesnenin değerini değil de kendisini göndermek istiyorsak (Call by reference) pointer kullanacağız.

Örnek 2:
---
![image](https://user-images.githubusercontent.com/75746171/135479016-ab792359-cfb5-4a6f-976a-c9e5f8b7e49f.png)


![image](https://user-images.githubusercontent.com/75746171/135479043-1de27336-b2ad-4524-8015-b5924f0b3266.png)


Örnek: Gerçek bir swap fonksiyonu
---
![image](https://user-images.githubusercontent.com/75746171/135479913-799da61d-f732-4a43-aec1-1aa14a2cce2c.png)

![image](https://user-images.githubusercontent.com/75746171/135479960-262a4a27-9edc-42a1-90b1-de262b3c861e.png)

Örnek: scanf fonksiyonu yazma
---

![image](https://user-images.githubusercontent.com/75746171/135522713-44092878-7d00-4123-a338-3daf92680635.png)

Ders 30 (30.09.2021) 23.06
---

- Pointerların en çok kullanıldığı yerler call by reference fıonksiyon çağrıları. (Bir fonksiyon başka bir fonksiyonun yerel değişkenine erişmek isterse)


Neden bir fonksiyonun parametre değişkeni pointer olur?
- Fonksiyon diyor ki sen bana bir nesnenin adresini gönder ben de değeri o adresteki nesneye yazayım. (Alternatif return)

Yanlış swap fonksiyonu
---
![image](https://user-images.githubusercontent.com/75746171/136140325-146f399b-b485-4462-9e10-72932f412f9d.png)

Değerler değişmeyecek.

Örnek: Daire alanını hesapla, Call by reference
---
![image](https://user-images.githubusercontent.com/75746171/136140857-d22e3ba9-1673-42fe-8c5d-72d715260c0d.png)

Fonksiyonun geri dönüş değeri kaldırıldı, işlemler pointerlar ile yapılıyor.


- Return deyimi ile geri dönüş değeri ürtetiliyorsa geri dönüş değeri için bir belek ayırılıyor. İfadenin değeri kopyalanıyor. yüksek değerlerde kopyalamanın maliyeti fazla olur.
- Hesaplanacak değerin sizeof değeri düşük ise return ile geri dönüş almak uygun olabilir. Fakat büyük boyutlarda adres ile atama yapılması gerekir.
- Birden fazla değer döndürmek için pointer kullanılablir. Diğer türlü fonksiyoınun geri dönüş değeri var ise sadece 1 değer döndürebilir.
- C dilinde bir fonksiyon bir başka fonksiyona bir dizi gönderecek ise call by reference zorunlu.
- Diziler fonksiyonlar arasında adres yolu ile geçilir.


Const Anahtar sözcüğü ve sematiği (Değişmez değişken)
---

- Const
- colatile
- restrict


- Bir değişkeni const ile tanımladığımızda; (Dizi de olabilir)

const int x = 45;

- Hayata bu değer ile başlayacak ve bir daha hiç değişmeyecek.

Pointer değişkenler ile const
---

int	*	ptr	=	&x;

- Burada const anahtar sözcüğü asteriksten önce veya sonra kullanılması tamamen farklı anlamlara geliyor.


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/136145160-6acc6159-a932-4936-abf4-1f8511167824.png)

- ptr nin değeri hiç değişmeyecek (Hayatı boyunca hep x'i gösterecek.)

![image](https://user-images.githubusercontent.com/75746171/136145507-bb794e96-d2e6-4920-a8cc-9709d2b3cd43.png)



![image](https://user-images.githubusercontent.com/75746171/136146432-3a6294c6-abdf-4a12-8386-ae8ee822ee2e.png)

- Adresini aldığı nesneyi değiştirecek.


![image](https://user-images.githubusercontent.com/75746171/136146593-e885139e-4520-4432-887f-bcce5462b1bd.png)

- Salt okuma amaçlı erişecek.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/136147566-d57b4c28-831a-4200-a79b-63d1654d5567.png)

- Dizinin elemanları değişmeyecek. Const yaptık. Ama fonksiyonun parametresi const int* değil. Lojik bir hata var.

Pointer aritmetiği
---

![image](https://user-images.githubusercontent.com/75746171/136154090-f7bcfb6c-c084-43a5-b0f9-add0b6b86370.png)

- Bir adres ile 1 toplandığında bir sonraki (aynı türden) nesnenin adresi elde edilir.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/136154852-351e3998-ffbd-4728-9b26-5028e9debd72.png)

![image](https://user-images.githubusercontent.com/75746171/136154897-aaa98a51-1fbf-41c7-aa88-a55153365224.png)


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/136155142-7cd13ee0-4be0-42e8-a64e-e61107b86c40.png)

- ++ptr demek ptr'yi 1 arttırmak demek. Yani ptr dizinin ilk elemanını değil 2. elamanını gösteriyor.
- Pointer değişkeninin 1 arttırılması dizinin 1 sonraki elamanını gösteriyor anlamına gelir.
- Yani a + 1 demek dizinin 1 indisli elemanının adresi demek. &a[0] + 1 = &a[1] , a[5] = *a(a+5)
Burada içerik operatörünün operandı bir adres olduğundan o adresteki nesneye eriimini sağlıyor.

- Yani a[i] demek *(a+i) ifadeleri aynı anlama gelir.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/136155759-47f567e0-53cf-4cc1-bc12-88fdfff55bf9.png)

![image](https://user-images.githubusercontent.com/75746171/136155795-34cdcac2-964b-411b-95fd-f8d994c13d3e.png)


- a[i] ile i[a] aynı anlama geliyor. Bunu sebebi ifadenin şuna dönüşmesi:
- *(a+i) *(i+a)

Ders 31 (06.10.2021) 10.30
---

- Pointerın arttırılması dizinin elemanlarını gösteren pointerlar için anlamlı, bundan bir fayda sağlamak içi.n kullanılıyor.

Index operatörü []
---
Bir operandı adres bir oerandı tam sayı olması gerekiyor.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/136343355-b424bf51-fbfd-4535-bf48-f1ba8c9a2dd9.png)

x = 23

![image](https://user-images.githubusercontent.com/75746171/136343557-ac464ce2-d498-4ae3-9d9e-89d5fdb64d79.png)

Aynı anlama geliyor.

Soru:
---
![image](https://user-images.githubusercontent.com/75746171/136343919-a8f1665c-81bd-4dde-be8b-065bc3bc09ea.png)

Çıktı:

![image](https://user-images.githubusercontent.com/75746171/136343981-ab6a99d4-99fa-44f1-b116-1d002d16b979.png)

Özet:

![image](https://user-images.githubusercontent.com/75746171/136344244-f114b25a-9de9-413a-a0f2-7994cb4f37a4.png)


- C ve C++ dillerinde iki adresin toplanması geçersizdir. (Sentaks hatası)


Adreslerin çıkartılması
---

![image](https://user-images.githubusercontent.com/75746171/136363620-1e773eed-0872-44c2-ab77-73bc7f65a459.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/136363747-065a59db-0823-4305-b30c-f3c552e8899b.png)

![image](https://user-images.githubusercontent.com/75746171/136363776-51db2019-f839-49f0-a37a-3118eabaeddf.png)


Soru:
---
ptr, a isimli bir dizinin bir elemanını göstermektedir. ptr'nin gösterdiği dizi elemanının indisi nedir?

ptr - a


Özet
---
- Adres ve tam sayı toplanabilir.
- Adresten tam sayı çıkartılabilir.
- Tam sayıdan adres çıkartılamaz.
- 2 adres toplanamaz.
- 2 adres çıkartılabilir.  Sonucun ne olduğu tamamen derleyiciye bağlı ve elde edilebilecek hiçbir şey yok.

Örnek: Dizinin tüm elemanlarını yazdır.
---

![image](https://user-images.githubusercontent.com/75746171/136643260-17a7f7a4-8e08-43a5-a155-e9e8e400bf18.png)

Size kez döner. Pointer 1 artar her seferinde gösterilen adres değişecek.

Örnek: Dizinin en büyük elemanını hesaplayan program
---

![image](https://user-images.githubusercontent.com/75746171/136643570-83bca93c-0535-48c4-b1a5-e2a68fa5b3a0.png)

Örnek: Dizinin hem en büyük hem en küçük değerini hesapla
---

![image](https://user-images.githubusercontent.com/75746171/136643665-885f37af-cb6d-48f5-b317-a69ba703f54e.png)

Örnek: Bir diziden bir diziye n tane öge kopyala
---
![image](https://user-images.githubusercontent.com/75746171/136643968-c90adbd1-8db9-4af7-ad21-04ba8712199e.png)

Başka bir yazma şekli:

![image](https://user-images.githubusercontent.com/75746171/136643984-14f5aa9f-078b-4bdd-8299-98040f39fa12.png)


A'nın .. indisli elemanında b'nin .. indisli elemanına
---

![image](https://user-images.githubusercontent.com/75746171/136644086-a5736f6e-31af-430d-a11d-5f13be35a1a9.png)

Örnek: Bir tam sayı dizisini ters çevireecek reverse array fonksiyonu
---

![image](https://user-images.githubusercontent.com/75746171/136644147-8a102bf1-962a-485c-94dc-cca7addb603b.png)

![image](https://user-images.githubusercontent.com/75746171/136644152-c7423480-b24c-4e3d-aea4-a74c88336b56.png)


Örnek : Bir dizinin standart sapması
---
![image](https://user-images.githubusercontent.com/75746171/137942965-0b5ac1a7-f52d-4306-b8b1-124b0c51befc.png)

Ders 32 (19.10.2021)
---

![image](https://user-images.githubusercontent.com/75746171/137944102-5bf6dfb1-8778-43df-abe4-888f7995689b.png)


![image](https://user-images.githubusercontent.com/75746171/137944890-9125dd52-27a1-455c-8e27-12eaeb762204.png)

Hepsi sentaks hatası

Örnek
---

![image](https://user-images.githubusercontent.com/75746171/137945310-ff306afa-9506-46ed-852b-7f6e3ecf1259.png)

![image](https://user-images.githubusercontent.com/75746171/137945364-c99b8ba1-2be1-43aa-adc3-1e0c642573aa.png)

Not:
---
![image](https://user-images.githubusercontent.com/75746171/137946816-9928194e-fa59-4588-8c36-0dc2cfdbdf26.png)

Tür Eş isim bildirimleri 1
---

![image](https://user-images.githubusercontent.com/75746171/137948502-0b3d378a-669c-4582-868e-381c4633d330.png)


Word demek int demek.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/137948941-ddd3f54f-c235-43c0-ab42-71ff878e7dc0.png)

Burada p1 pointer fakat p2 değil. Mülakatlarda soruluyor.

- typedef yapsaydın ikisi de pointe olacaktı.

Örnek
---
![image](https://user-images.githubusercontent.com/75746171/137951067-574961d6-4b48-4c61-ad88-ebabc943b037.png)

size_t türü nerelerde kullanılıyor?
---

- Bazı fonksiyonmlar size of değeri istiyorsa size_t türündendir
- Dizi boyutu istiyorsa size_t'dir
- Yazı uzunluğu istiyor ise
- Tane - adet türü olarak kullanılıyor.

Ders 33 (19.10.2021)
---

Adres döndüren fonksiyonlar
---

Örnek

![image](https://user-images.githubusercontent.com/75746171/137958044-231c1584-3cd1-473b-a363-79420b926b1c.png)

![image](https://user-images.githubusercontent.com/75746171/137958077-dd4aec17-d1c5-430f-8e84-4654613d2414.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/137958376-1453981d-b975-45fe-bccf-cda75e77d4a2.png)


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/137958852-e897826c-d55f-4976-be71-eb2bf6770d9c.png)

- Otomatik ömürlü, hayat bitmiş bir değişkenin değeri döndürülüyor. UB.

![image](https://user-images.githubusercontent.com/75746171/137966059-fef1a59a-a364-4b92-b23c-f7ae2af40661.png)

Örnek: Dizinin max elemanının adresini döndüren fonk.
---
![image](https://user-images.githubusercontent.com/75746171/137969093-d02007a8-2acf-488d-9744-839c541c34f2.png)

Örnek: Dizinin max elemanından sonuna kadarki elamanları yazdır
---
![image](https://user-images.githubusercontent.com/75746171/137970241-4fbc8623-d81c-4328-b0a0-89f66d34972e.png)

![image](https://user-images.githubusercontent.com/75746171/137970291-fefaef71-bf2e-49a3-93d9-ca50f955ab16.png)

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/137972108-fc14bb2c-c1c2-41e9-a66e-11529c937411.png)

Dizinin en büyük ve en küçüğünü yer değiştir sonra sağda kalan dizideki en büyük ve küçüğü yer değiştir.


Null Pointer
---

- Null bir makrodur. (Önişlemci programı ilgilendiren bir isim, bir sembolik sabittir)
- Bir keyword değil, identifier değil.
- stdio.h , string.h, stdlib.h başlık dosyalarında tanımlanmıştır.
- Null bir adres sabitidir. (Null pointer diye okuyunuz.)
- Null pointer, Null character
- Pointer değişkkenlere ilk değer olarak verilebilir.
- Null pointer herhangi bir türden bir pointer değişkene atanabilir.


Null pointer ile yapılabilecek işlemler
--

![image](https://user-images.githubusercontent.com/75746171/137978380-286b313a-12f6-4403-b073-c153189b6fce.png)

![image](https://user-images.githubusercontent.com/75746171/137978449-c14a43a5-bc43-4bb3-9b44-be4b5496f13e.png)


- İlk değer verilmemiş global pointer değişkenler ve statik yerel değişkenler hayata bull pointer değeri ile başlarlar.

![image](https://user-images.githubusercontent.com/75746171/137978758-5ea7a0fd-fbcb-4854-89cc-cfed0aee151d.png)
 
 Bu ikisi aynı anlama geliyor.

![image](https://user-images.githubusercontent.com/75746171/137978835-ca70eeb5-d525-4ce0-b48a-3f3f5d187fe0.png)

![image](https://user-images.githubusercontent.com/75746171/137979002-6de951f9-063f-43b8-8521-d0f14138cc8f.png)


Ders 33 (19.10.2021) 
---

Null pointer nerelerde kullanılır?
---

- Adres döndüren bir fonksiyonun başarısızlık bilgisini iletmesi. Adres döndüren bir işlev başarısızlık durujmunda null pointer döndürüyor.
- Arama fonkksiyonları adres döndürüyorlar (Çoğunlukla). Değer bulunutrsa bulduğu karakterin adresini gönderiyor bulamazsa null pointer döndürüyor.
- Bir fonksiyonun parametresinin pointer olması durumunda bu fonksiyona bir nesne adresi göndermemiz gereliyor. Null pointer gönderilirse tanımsız davranış olur. (Bazı fonksiyonlar null pointergöndermeyi seçenek olarak verebiliyor.)


Örnek:
---
Bir tam sayı dizisinde bir değeri arayan search adlı fonksiyonu tanımlayınız

![image](https://user-images.githubusercontent.com/75746171/137989984-2c539e07-8fa7-4276-a7ec-0baf5b0d17aa.png)


Not:
---
Pointer değişkeninin değeri ya bir nesnenin adresidir ya da null pointer olması özelliği bazı durumlarda pointer değişkenlerini bayrak değişkeni olarak kullanabilmemii sağlıyor.

![image](https://user-images.githubusercontent.com/75746171/137991126-0ba31d83-2bea-4a7c-b111-b006eaaa0640.png)

Burada if içine girip girmediğini pointerin bull olup olmadığına bakarak anlaşılabilir.

Diğer kullanım alanı: Dinamik bellek yönetimi
---

ptr = nesne adresi

- Pointer değişkenimizin hayatı devam ederken onun göstermekte olduğu nesnenin hayatı sona eriyor.

Null pointer			Null character
---
Null				'\0'
Adres sabiti			Tam sayı sabiti
Pointer değişkene atanır	Bir char dizisinin elemanına atanıyor(int değişkene)

Örnek (Puts işlevi)
---

![image](https://user-images.githubusercontent.com/75746171/137996935-1e1faa92-2e10-443f-8b63-049826cd6604.png)

![image](https://user-images.githubusercontent.com/75746171/137996968-b6667b5d-dd55-494b-973e-59aefeab1a0c.png)


Örnek: Tanımsız davranış
---
![image](https://user-images.githubusercontent.com/75746171/138084862-fa83dd0d-b2e0-4241-9c4c-a932acb70aa2.png)

Otomatik ömürlü dizinin adresi ile dönüş ypıldı.


![image](https://user-images.githubusercontent.com/75746171/138085192-0aa0ce25-dfff-4f3c-b456-3850b511402a.png)

Burada static ömürlü nesnenin adresi ile dönüyorsa bu şekilde kullanılamaz. Her seferinden eski değer gidip yeni değer geliyor. Çağırılma şekli yanlış:

![image](https://user-images.githubusercontent.com/75746171/138085381-347dea09-1617-44a4-8ead-ecb70dcaa99a.png)


<string.h>
---
- Yazılar ile ilgili işlem yapıyorlar

- strlen
- strchr
- strtok
- strrchr
- strstr
- -----

Örnek: Tersten yazdır
---
![image](https://user-images.githubusercontent.com/75746171/138087537-4ca6f418-133e-4afb-bc12-db1c88db5667.png)

![image](https://user-images.githubusercontent.com/75746171/138087571-c9b7d283-1239-44d2-a31f-0caefd4ee04f.png)

Bu da fonksiyon ile yazdırma:

![image](https://user-images.githubusercontent.com/75746171/138087688-8eda90d4-a39e-4d25-9590-a20abb2beb25.png)

![image](https://user-images.githubusercontent.com/75746171/138087713-f2441768-641f-46e9-9d35-a96015bbe724.png)


char *strchr(const char *p, int c);
Bir karakteri arıyor, Bulujduğpu yerin adresinin döndürüyor bulamazsa null pointer döndürüyor.

Ders 35 (20.10.2021)
---

Önek: Bir yazının adresini tutan pointeri yazının sonundaki null karakteri gösterecek hale getir.
---
![image](https://user-images.githubusercontent.com/75746171/138096738-3702e758-55a3-4b3e-951c-95a5651ace8f.png)



![image](https://user-images.githubusercontent.com/75746171/138096858-c090e5bd-e6c4-42b0-8475-062548c0515d.png)

Fakat bu dpoğru olmaz. Yazının boş olması durumunda ilk karakter null karakterdir ve onu atlar.

![image](https://user-images.githubusercontent.com/75746171/138097009-47235265-5b7d-4495-ab20-da61c815923f.png)

Burada ise yazının başlangıç adresine yazının uzunluğu ekleniyor, geçerlidir.

Örnek: kopyala
---

![image](https://user-images.githubusercontent.com/75746171/138097717-010c1e95-80f7-4bc6-abab-397ef8bfd372.png)

Örnek: Bir kopyalama fonksiyonu yaz
---

![image](https://user-images.githubusercontent.com/75746171/138097904-91feffe5-6aee-48d7-a574-0c2bd628f17e.png)


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138098122-d19648f4-d7f2-46f3-8b69-64ecf0cb3a24.png)

Bu bir tanımsız davranış

Sebep:

Kesişen bloklar.

Okuma yazma işlemi kesişen bloklar üstünde yapılıyor (str+2 ve str)

Buradaki restrict anahtar sözcüğü ile kesişim kümesi olmadığını gösteriliyor.


Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138099643-a6577d74-e5aa-4eb1-baac-d18de2234054.png)

![image](https://user-images.githubusercontent.com/75746171/138099713-28a51506-e034-4925-bb3b-5a724ab7c770.png)

Ders 36 (20.10.2021)
---

Konular:

![image](https://user-images.githubusercontent.com/75746171/138099938-31d6df66-5922-48ce-8ef8-1f35db565492.png)

Not: 
![image](https://user-images.githubusercontent.com/75746171/138101235-cc852b2c-d66e-47b7-8b4e-2bdd0e560568.png)

Bu bir dizinin ilk elemanını yazdırır yani n.

![image](https://user-images.githubusercontent.com/75746171/138101799-9975218a-06c7-40ff-9279-e3efa842f26e.png)

Bu bir tanımsız davranış çümkü string literali sadece okuma amaçlı erişilebilir.

- Burada bir fonksiyona string literali gönderilecekse türü const char* olmalıdır.


Not:
---
- String literalleri static ömürlü dizilerdir.
- Programınb başından sonuna kadar hayatta kalırlar
- Yazı adresi döndüren bir fonksiyonun bir string literali adresi döndürmesi ub değildir.


![image](https://user-images.githubusercontent.com/75746171/138103708-6cdfa0d8-f9ad-48b3-a010-f501df0e875b.png)

- printf'in ilk parametresi const char*
- Burada biz argüman olarak merhaba arkadaşlar yazısı olan dizinin adresini gönderiyoruz.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138104580-921e2323-3b49-4a81-a509-c12a0e4ddf1d.png)

İkisi de aynı anlama geliyor.


![image](https://user-images.githubusercontent.com/75746171/138107177-8d1ee033-e119-4e1a-a667-b1b2455276d4.png)


Burada aslında bir dizi tanımlanıyor.

Mülakat sorları:
---

![image](https://user-images.githubusercontent.com/75746171/138108428-ec65a04b-5381-43dd-bc77-6105721d858c.png)

----

![image](https://user-images.githubusercontent.com/75746171/138108729-0c9c4a3e-9732-404f-a019-2d2a9fb8b128.png)

P nin değeri sizeof yüzünden değişmior o yüzden p değeri 6 yazar.

Pointer Arrays
---

Örnek:
![image](https://user-images.githubusercontent.com/75746171/138276637-a5814a77-f1fb-4168-9101-2a0b6d700dfd.png)

Ekrana 10 yazar.

Örnek: Pointerin gösterdiği nesnelere erişecek
---
![image](https://user-images.githubusercontent.com/75746171/138276771-fd1402b4-c44c-472d-adaa-9691855987e6.png)

![image](https://user-images.githubusercontent.com/75746171/138276792-2e0543ac-0099-4b08-9ef6-e66f1d3df279.png)

Başka bir örnekte :

![image](https://user-images.githubusercontent.com/75746171/138276949-fe0dda48-80b8-443d-85f5-b3353cc39895.png)

a'nın değerini 77 yapıyor.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138277326-9ac3c5ae-1a34-4e64-836b-f8acb4bcd5dd.png)

p[1], dizinin 1 indisli elemanı. Onun değeri ise b dizisinin adresi. [2] 'nin sol operandı b dizisi oluyor. b dizisinin 2 indisli elamanını değiştiriyor.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138278035-7d6d4079-df1e-445b-8b88-d3c5e1b99f95.png)

![image](https://user-images.githubusercontent.com/75746171/138278071-97f5404d-0c98-4c39-ad25-4e01a1a865d6.png)

p[2], dizinin 2 indisli elemanı

---


![image](https://user-images.githubusercontent.com/75746171/138278629-8bdc6227-b82b-49e6-b7a6-b10d8799f97b.png)

Bu dizinin elemanları const demek.

![image](https://user-images.githubusercontent.com/75746171/138278909-9d805a0b-9fab-4559-8a8b-f80a40bfae3d.png)

Burada ise dizinin elemanları const int* demek.

![image](https://user-images.githubusercontent.com/75746171/138279919-a8169b9e-2655-41d3-85b9-76abc003fc1f.png)

Bu ifade dizinin boyutu demek ile aynı anlama geliyor.


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138289186-32358f90-1073-4288-acea-cff7b6195d98.png)

- Burada pointer dizilerini oluşturmaktaki asıl amaç lookup table yapmak.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138289506-359ce969-df62-452a-a7ca-9b82ad8f82c1.png)

Her tuşa basıldığında rastgele bir ay elde ediyor.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138289821-4f4fc38f-5abc-4607-bfa9-11ae3d412455.png)

![image](https://user-images.githubusercontent.com/75746171/138289859-3a325922-4fed-4a9a-aceb-3e3c4e1fa095.png)

Ders 37 (21.10.2021)
---
Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138366912-09360c30-269b-4b17-9bf8-3e295ef22c94.png)

Bu dizinin elemamnlarının ilk harflerini yazdır.

![image](https://user-images.githubusercontent.com/75746171/138366981-18381ae1-417d-4031-84cc-2e7be2d267f3.png)

![image](https://user-images.githubusercontent.com/75746171/138367022-7ccf71a8-f5cc-4a1f-81ad-d444849c7450.png)

Son elemanlarını yazdır.

![image](https://user-images.githubusercontent.com/75746171/138367133-388d7f91-0568-4293-8915-3851784b4e10.png)

İçinde c karakterierl olanları yazdır.

![image](https://user-images.githubusercontent.com/75746171/138367209-469e5507-5cb5-491d-8f33-1b32609b6e6e.png)

Belli karakterleri içerenleri yazdır.

![image](https://user-images.githubusercontent.com/75746171/138367307-5193f3d5-dedc-4897-aa4f-41e47a65f365.png)

Küçükten büyüğe sırala.

![image](https://user-images.githubusercontent.com/75746171/138367872-ec8b3227-bdcd-4357-8217-ea0ba14d9f5b.png)

Kısa olanlar başta ve kendi içinde sıralı.


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138448963-7fde196f-4f61-4fbe-b23a-14676b830319.png)

Dizinin sonuna null poniter ekleyerek sonunu belirledik. Diziyi yazdırdırk.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138449200-5bcb69a4-a96b-4e42-a933-90665518a192.png)

- Dizide 2 string literali arasında virgül yok. Buınlar birleşecek ve tek string literali olarak tanımlanacak. Dizinin 20 elemanı olması gerekşiyordu 19 tane oldu. Son elemana null pointer oldu. Döngünün sonunda null pointer dereference edilmiş olacak.

Pointer to Pointer (Gösterici gösteren gösterici)
---


ptr değişkeninin adresini bir pointer değişkende tutmak istersem : 

![image](https://user-images.githubusercontent.com/75746171/138450566-346f1480-9885-4c51-a6a6-5aba8c5f64a5.png)


Not:
---
![image](https://user-images.githubusercontent.com/75746171/138450925-513c9a7f-1122-49d5-8e9e-32d4fc9bc8fa.png)

- Burada p değişkeni içerik operatörünün operandı yapılırsa ptr'ye erişilecek.
- ptr değişkeni içerik opratörünün operandı yapılırsa x'e erişilecek.


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138482711-5247201c-b9e6-46e6-a190-2f46a536a891.png)

- ptr, x'e diyor ki,  sen benim gösterdiğim nesnesin.
- p'de ptr'ye diyor ki, sen benim gösterdiğim nesnsin.
- Ve p, x'e diyor ki, sen benim gösterdiğim nesnenin gösterdiği nesnesin.

Not: Pointerların en çok kullanıldğı yerler, call by reference fonksiyon çağrıları.


Örnek: Değişkenlerin değerlerini takas et
---
![image](https://user-images.githubusercontent.com/75746171/138484487-553fb756-2f62-4e4c-9bfc-2083899be2cc.png)


![image](https://user-images.githubusercontent.com/75746171/138484460-39cd25d5-8b32-488e-9293-745e2be4f2a2.png)


- Bu işlem sık yapılıyorsa bunu fonksiyona yaptıralım. Ama bu fonksiyon değişkenleri adresleri ile çağırmalı,

![image](https://user-images.githubusercontent.com/75746171/138484751-98c25a40-8ade-4fe1-a4ba-bd93517c5041.png)

Not:
---
Bu ikisini karıştırma

![image](https://user-images.githubusercontent.com/75746171/138485027-a69da6f9-e5d2-497a-997d-ec744319fa36.png)

- Birincide ptr'nin değeri olan adresi gönderiyorum
- ikinicide ptr'nin kendi adresini gönderiyorum.


Örnek:
---
Öyle bir fonks,yon tanımlayınız ki bir taö sayı dizisinin hem en küçük hem de en büyük elemanlarının adreslerini, çağıran koda iletsin.

![image](https://user-images.githubusercontent.com/75746171/138486944-3eceb871-69b7-4078-9146-badb9776ff94.png)



Fonksiyonda,
- 1. parametre dizinin adresi
- 2. parametre dizinin boyutu
- 3. parametre int* türden bir nesnenin adresini ver ben min elamanın adresini yazıcam
- 4. parametre int* türden bir nesnenin adresini ver ben max elamanın adresini yazıcam


Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138487349-37e78ef3-60e5-44d0-bede-33e168e99cb4.png)

Bu kod dizinin elemanlarını yazdırıyor.
Eğer ben bu işlemi sık sık yapacaksam bunu bir fonksiyonda yapmalıyım. Fonksiyon char* türden bir adres aldığı için parametresi char** olmalıdır.

Kitap:
Understanding and usin c pointers

Ders 38 (22.10.2021)
---

Void Pointers
---

![image](https://user-images.githubusercontent.com/75746171/138493746-639487f5-1ad6-4480-bd68-0f398d38ef46.png)

- void pointeri dereference edip o nesneye erişip kullanmak sentaks hatası.

![image](https://user-images.githubusercontent.com/75746171/138494172-1e0234aa-87cd-4b6d-9a10-b4f3c7cd98c7.png)

Void pointer ne işe yara?
---

Generic programming: türden bağımsız programlama

Generic functions: Bellirli bir türe hizmet vermiyor, her türe hizmet veriyorum. Türü ne olursa olsun.


Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138495639-dfe37684-7f5b-44f0-8f06-d33d751903b2.png)

![image](https://user-images.githubusercontent.com/75746171/138495662-1a2b7efb-1f12-48e0-bbd8-965e9cdd18f6.png)

Burada nesneler byte byte takas edildi.

Bazı fonksiyonlar
---
Hemen her uygulamada kullanılan fonksiyonlar.

Memset
---
![image](https://user-images.githubusercontent.com/75746171/138501115-9c906eb3-3601-42f0-90ee-7afda530c368.png)

- Bir bellek bloğunun bütün bytelarını bir tam sayı değeri ile doldurur.

![image](https://user-images.githubusercontent.com/75746171/138501415-c6309adf-9abc-446f-a0ea-f8073f5e6895.png)

Bir dizi var ve tüm elemanlarını sıfırlamak istiyoruz.

- memset ile dizinin bütün bytelarına sıfır yazarsam dizinin elemanları sıfır oldu.

![image](https://user-images.githubusercontent.com/75746171/138501538-93c4a9cb-be0e-4f2b-9875-8fa1466e7da2.png)

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138501722-8fe3d40e-c5b1-4e7e-bc34-45f02ff1af29.png)

![image](https://user-images.githubusercontent.com/75746171/138501741-910b348c-9c57-4039-b013-52f1f5132c8a.png)

Memset'in kodu
---
![image](https://user-images.githubusercontent.com/75746171/138502002-67388dbf-d04b-4313-9c65-c86848f2ec5e.png)

Memcpy
---
- Bir bellek bloğunu bir yeren bir yere kopyalıyor.

![image](https://user-images.githubusercontent.com/75746171/138503974-54f6fdc0-cbdf-463e-b7c6-96327884aed2.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138502504-b6465eb7-d571-40cc-8952-2b7e9efc388b.png)

![image](https://user-images.githubusercontent.com/75746171/138502528-e1b5a2d9-2666-4a64-a4b9-19be449872dc.png)

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138502765-df6e24e2-44d0-4494-9754-b1d03312d838.png)

![image](https://user-images.githubusercontent.com/75746171/138502801-72d9ac1c-4a6d-4292-8814-9bc8a09fdfc6.png)

memcpy'nin kodu
---
![image](https://user-images.githubusercontent.com/75746171/138502907-3bb8e9d6-f62f-4a4b-9699-3c77ab27b758.png)

memmove
---
![image](https://user-images.githubusercontent.com/75746171/138504057-16dd14d8-de66-4c32-8ab8-c9a8f4b3e119.png)

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138504237-df41aaeb-bed6-478a-ba6e-f8807591ce5b.png)

![image](https://user-images.githubusercontent.com/75746171/138504266-80a530c3-739c-4846-be46-68aa76d1c706.png)


Memchr fonksiyınu
---
Bellek bloğunda bir byte arıyor.

![image](https://user-images.githubusercontent.com/75746171/138504523-ccc88e8f-332e-4807-99f1-f57da8f31dd8.png)

- Eğer vp adresinden başlayan bellek bloğuda (boyutu n olan) val varsa adresini döndürecek yoksa null pointer döndürecek.

Örnek
---

![image](https://user-images.githubusercontent.com/75746171/138505342-deca2ef9-4705-4db0-a016-9f8608b20fb1.png)

- memchr char* dönüştürüldü çünkü void*

![image](https://user-images.githubusercontent.com/75746171/138505452-d3b3e946-8aba-4a9d-b090-4feaf73fa74b.png)

memcmp fonksiyonu
---
strcmp iki yazıyı karşılaştırıyor, memcmp 2 bellek bloğunu karşılaştıroyor.

![image](https://user-images.githubusercontent.com/75746171/138505612-486034a6-d3a7-41e9-98a3-a5d8cafffd67.png)

Birinci blok büyük ise pozitif, ikinci büyük ise negatif, eşit ise 0 değeri döndürüyor.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138505947-b2d055aa-2736-4142-befc-c54c2cbc71cf.png)

![image](https://user-images.githubusercontent.com/75746171/138505976-b4f9e13d-f6f3-461f-b3ba-8b163ceb0068.png)


Fonksiyonun kodu
---

![image](https://user-images.githubusercontent.com/75746171/138506161-c9c8a42d-3b14-4dd0-b1bf-c36d4aa5ee59.png)


Örnek:
---
Türden  bağımsız olarak diziyi reverse et (büyüklüğünün yarısı kadar olan döngüde elemanlarını takas et)

![image](https://user-images.githubusercontent.com/75746171/138506944-edccbd4e-f9c0-4ef3-96e9-e8c3129b6284.png)


Örnek: Bir dizide arama yapan fonksiyınu generic olarak oluştur.
---

![image](https://user-images.githubusercontent.com/75746171/138528596-2acca282-b3c9-418c-9bf2-0ca6c0edd748.png)

1- dizinin adresi
2- Dizinin boyutu
3- Dizinin elamanının sizeof değeri
4- Aranacak değeri tutan nesnenin adresi


![image](https://user-images.githubusercontent.com/75746171/138531042-451a0cac-b3f5-4018-8142-c01e8fccba47.png)

![image](https://user-images.githubusercontent.com/75746171/138531054-07ffe13e-d5eb-4d85-a993-af93bc1f8596.png)

Ders 39 (23.10.2021)
---

Fill işlemi
---
- Veri yapısının elemanlarını belli bir değerle set etme.

int türüne bağlımlı olan fill fonksiyonu:

![image](https://user-images.githubusercontent.com/75746171/138551735-8d1b9d7e-c08b-4b49-a2e3-95a693fbaa3f.png)

Türden bağımsız hali:

![image](https://user-images.githubusercontent.com/75746171/138551938-49dc1b58-1ddb-48ab-b2db-b801010f63fd.png)

![image](https://user-images.githubusercontent.com/75746171/138551942-7824faa9-9105-4d2f-931c-2ed26a024017.png)

![image](https://user-images.githubusercontent.com/75746171/138551951-9806861b-1ee9-40b0-8aba-5b146d3d8b00.png)


3.. parametre, bir elama nınnın sizeof değeri
4.. parametre set edilecek olan değere sahip nesneye ait olan adresi
Diziyi fonk içinde char* çeviriyor. ve onu da char* olan başka bir diziye atıyor.

Not:
---
void** türü void* türden bir nesnenin adresi olan tür. Bir generic tür değil.

![image](https://user-images.githubusercontent.com/75746171/138552184-7596f5c7-d5f7-4627-b2be-a3156902025f.png)

Bu adresin türü void** 'dır.
Yani void* türü gösterecek bir değişkene ihtiyaç varsa void** türü kullanılır.

Function Pointers (Fonksiyon Göstericileri)
---

Nesne adresi: Programın çalışma zamanında o nesne bellekte nerede?
Fonksiyon adresi: Fonksiyon kodununb çalıpması için makina koduna ihtiyaç var. Bu makina komutlarının belleğe yüklenmesi gerekiyor. Yüklenen bu adres fonksiyonun adresi.

Fonksiyonun adresi nasıl elde edilir?
---
Fonksiyonun ismini ades operatörünün operandı yap.
&func ifadesi func işlevinin adresi anlamına geliyor.

Nasıl bir dizinin ismi bir ifade içinde kullanıldığında dizinin ilk elemanının adresine dönüştürülüyor ise (erray decay) bir fonksiyon ismi de ifade içinde kullanıldığında o fonksiyonun adresine dönüştürülür.

yani func = &func

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138552597-02244b20-04a4-4558-b28d-aa657d064fbd.png)

Not
---

Nasıl nesnelerin adreslerini tutan değişkenler oluşturabiliyorsak, fonksiyonalrın adreslerini tutan değişkenler de oluşturabiliyoruz.

![image](https://user-images.githubusercontent.com/75746171/138552864-9d07655f-4c5a-43ff-a0d7-99cc8cb86663.png)

Örnek:
---

İsmi fp olan bir değişkene strcmp nin adresi ile ilk değer verelim.

![image](https://user-images.githubusercontent.com/75746171/138552919-69b3bb82-64e6-4873-a989-b76019cf683b.png)

Ne işe yarar?
---

![image](https://user-images.githubusercontent.com/75746171/138552962-ba02bb24-546d-4816-a10f-526590d82ece.png)

Func fonksiyonu çağırıldı. Peki nasıl çağırılıyor? Burada bir operatör kullanılıyor. Operatör öncelik tablosunun en yüksek seviyesinde. Function call operatör. ()

- () operatörünün operandı aslında fonksiyonun adresi. O adresteki fonskiyınun adresini çağırıyor.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138553066-e499d1fb-fde7-4211-be30-8a2c8fe4cde4.png)

![image](https://user-images.githubusercontent.com/75746171/138553075-cdb4cc4d-278f-4af8-bfd4-227c3639dfd1.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138553151-d83c79af-9b67-40c9-9e3f-39098e486925.png)

![image](https://user-images.githubusercontent.com/75746171/138553155-c43b9bba-9857-4c3f-bbb2-37c64a66e6cf.png)

Bir fonksiyıonu ismi ile çağırmakla, fonksiyon pointerı ile çağırmak farklı çünkü fonksiyon ismi ile çğırırsam o fonksiyon çağrılacak fakat fonk. pointer ile çağırırsam çağrı yapıldığı noktada fp'nin değeri hangi fonk adresi ise o fonk çağrılacak.

Not: Fonk pointer türü ile ona atadığımız adres aynı türden olmak zorunda.

![image](https://user-images.githubusercontent.com/75746171/138553296-e2b5ea20-a64e-4dac-9689-af0caf3fc632.png)

Aralarında bi fark yok.

Not:
---
- Tüm object pointers sizeof değeri aynıdır.
- tüm function pointers sizeof değeri aynıdır.
- Object pointer sizeof depğeri ile func pointer size of değeri aynı olmak zorunda değil.

Bir fonksiyonun parametre değişkeninin function parametre olması, sık karşılaşılan bir drum.

![image](https://user-images.githubusercontent.com/75746171/138554585-b908bf77-e4d6-435b-bdf7-0ddc42b10176.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138554639-360969eb-4d15-44fe-bd88-4b50b9a389c4.png)

![image](https://user-images.githubusercontent.com/75746171/138554649-d057d699-e861-4073-9734-ecbd4e969590.png)

Fonksiyon çağırttık...

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138554903-1c149da9-a156-491f-8d63-ac9a86796e87.png)

![image](https://user-images.githubusercontent.com/75746171/138554907-b7f35c75-0710-477d-8e52-4f6f9f51a751.png)

Soru
---
a fonksiyonunun içinde b isimli başka bir fonksiyon çağrılıyor. Ben a'yı başka bir sefer çağırdığımda bu sefer a'nın içinde b yerine c fonksiyonu çağırmak istiyotrum. Bu iş için function pointer kullanılabilir mi?

![image](https://user-images.githubusercontent.com/75746171/138555047-1524c0d6-8f1e-4dc3-be68-02170cb4c414.png)

- globalde bir fptr tanımlanır ve main içinde o değişken b yapılır.


- func'ın başka bir fonksiyonu çağırmasını istersen setfunc yap ve ona başka fonksiyonun adresini ver.

![image](https://user-images.githubusercontent.com/75746171/138559312-94237822-b7fb-4f07-8df8-2b539a20b317.png)

qsort fonksiyonu
---

![image](https://user-images.githubusercontent.com/75746171/138559378-a6173238-95bb-4705-a266-79f8fb6db092.png)

- Generic bir fonksiyon. Bir sıralama ilişkisi ile bir diziyi sıralıyor.

1- parametre sıralanacak dizinin adresi
2- parametre sıralanacak dizinin boyutu
3- parametre sıralanavak dizinin bir ögesinin sizeof değeri
4- parametre sıralanacak dizinin 2 elemanını karşılaştırma amaçlı kuıllanılacak olan fonksiyonun adresini isteyen function poniter

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138559772-ed694231-bc0a-4529-ae42-9faf12a91da8.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138597589-fcee5ef1-2fb7-4120-8ca2-70cd892b3d7f.png)

![image](https://user-images.githubusercontent.com/75746171/138597605-e144094c-e8d7-461e-9f84-3c652d918274.png)

Örnek: 
---
Bubble sort algoritması ile sıralama yapan qsort benzeri parametrik yapıya sahip bir fonksiyon tanımlayınız.

![image](https://user-images.githubusercontent.com/75746171/138600365-9fabe837-3fa5-4b27-b2d4-29e8edb67907.png)

Not: O zman her fonksiyonu generic olarak yazabilrim. (call back kullanılarak)

- Dizinin elemanlarını yazdıran generic bir fonksiyon yazabiriliz. 


Örnek:
---
- Son parametresi dizinin bir elemanının adreisni alacak ve değerini yazdıracak fonklsiyon.

Döngünün her turunda fprint fonksiyonuna p'yi argüman olarak gönderdim.

![image](https://user-images.githubusercontent.com/75746171/138600694-55f81bcd-5748-4ff6-a934-8d6736e7474d.png)

![image](https://user-images.githubusercontent.com/75746171/138600705-3565d4d2-1756-47b7-af8d-9aebf5851662.png)

Foınksiyon Göstericileri ve typedef bildirimleri
---

![image](https://user-images.githubusercontent.com/75746171/138600917-59b5c756-7f3d-450b-a99e-c444e0f05b24.png)

Böyle yazmayacağız.
- Function pointer türleri hemen her zaman kütüphaneler tarafından typedef bildirimerli yapılıyor. ve okuma yazma kolaylığı sağlanıyor.

Örnek:

![image](https://user-images.githubusercontent.com/75746171/138600995-085243ca-9234-47c8-acd1-b3a960d399ff.png)

![image](https://user-images.githubusercontent.com/75746171/138601010-423c3f85-bb39-4cf0-b21b-4a21d6bf7c75.png)

fptr türünden fp tanımlandı.

![image](https://user-images.githubusercontent.com/75746171/138601034-36e3a7b5-1340-4c41-985a-ff5aa8eb5d99.png)

fptr türünden bir nesnenin adresini isteyen pointer

![image](https://user-images.githubusercontent.com/75746171/138601068-30b74cea-9984-4d83-a226-f754f10fa0be.png)

elemanları fptr türünden 10 elemanlı fa dizisi.

![image](https://user-images.githubusercontent.com/75746171/138601145-852dd2e9-ddfb-4256-ad3d-a7695e782765.png)


2 paramöetresi olan ve ikisi de fptr türünden olan bir fonksiyon.

![image](https://user-images.githubusercontent.com/75746171/138601159-cc2ce756-dc01-4dc4-895c-a5ee88a97776.png)

geri dönüş değeri fptr olan 2 parametresi fptr türünden olan fonksiyon.

Ders 40 (24.10.2021)
---

- Fonksiyon göstericileri kullanan bildirimler karmaşık oldığu için fonksiyon göstericisi türleri ytpedef bildirimine tabi tutuluyor.
- 
![image](htt ps://user-images.githubusercontent.com/75746171/138602145-f615692e-3499-4bd8-957a-57d383f3e7a0.png)

Böyle tanımlamak yedrine;

![image](https://user-images.githubusercontent.com/75746171/138602160-8c76d9a3-1676-41c3-8741-fd574de5491d.png)

Aynı anlama gelir.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138602246-e74b6a25-2243-4540-ba47-3fc71565ecaf.png)

![image](https://user-images.githubusercontent.com/75746171/138602256-05f084c1-3aff-4027-8b56-27b850f591ea.png)


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138602564-20b37369-d006-454a-aaa7-ceea77f9b3f6.png)

![image](https://user-images.githubusercontent.com/75746171/138602579-50364317-d340-496c-9279-72723711e47e.png)

Örnek: pointer to function pointer
---
![image](https://user-images.githubusercontent.com/75746171/138602711-a5214792-8642-45da-be85-9e36039f650f.png)

--------------------

![image](https://user-images.githubusercontent.com/75746171/138602840-8c2b4f9b-7c3f-49f4-ae89-05ae6719541e.png)

Geri dönüş değeri olmayan parametresi olmayan bir fonksiyon adresi türünü fptr ile isimlendirdi.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138617108-a40576d6-ae32-49f6-be3c-7837f8d61036.png)

Parametresi bir fonksiyon göstericisi.

![image](https://user-images.githubusercontent.com/75746171/138617185-a2bccc26-057c-4349-bc19-f46b3d1dbc87.png)

![image](https://user-images.githubusercontent.com/75746171/138617193-4e160e5a-6afb-4d84-8dca-b8abf0973855.png)

- func çağırıldığında fregister ile kayıt edilen fonksiyonları (kayıt edildikleri sıra ile ya da son olanı önce ) çağıracak. Peki bu nasıl oluyor?
- Çünkü aslında fregister bunları elemanları function pointer olan array'de tutacak.


![image](https://user-images.githubusercontent.com/75746171/138617351-26fac048-9f37-47eb-a8ec-b23ce7c6b89d.png)

Özet:
---
- String literalleri
- Pointer dizileri
- Ponter to pointer
- Void pointer
- Function pointers

konuları bitti.

- Sodility ili (akıllı kontratlar, blockchain) bak

Çok Boyulu Diziler
---
Multi dimensional arrays

- C'de çok boyutlu diziler yoktur.
- C'de aslında çok boyutlu diziler, elemanları dizi olan dizilerdir.
- 

![image](https://user-images.githubusercontent.com/75746171/138617671-51b6e18c-cf76-4f14-b55d-3b4105b32984.png)

- Burada 10 a dizisinin boyutu. a, elemanları 20 elemanlı int dizi olan bir dizi.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138617752-60a395cf-b65c-4556-97e9-5b68d6fd0082.png)

![image](https://user-images.githubusercontent.com/75746171/138617808-638ebb5d-0a78-4ec0-a3a7-07630e09012d.png)


- a[0], a'nın elemanlarından biri. Bu elemanlar 20 elemanlı int diziler. Yani sizeof a[0] 80 olur.
-  Yani a[10][20] demek 20 elemanlı 10 diziden oluşan bir diziir. a boyutu 10 olan bir dizi. Ama a'nın elemanları boyutu 20 olan int diziler.

Not: a'yı 200 elemanlı bir int dizi olarak kullanabilir miyim?
Evet. Bir int pointer dizinin ilk elemanının son elemanınıgösteriyorsa bunu 1 arttırdığıızda bu pointer dizinin 20 elemanlı 2. elemanını gösterir.

a[10][4] a'nın elemanlarının adresleri arasındaki fark 16 olacak.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138645370-cd751559-bfe1-4c64-a7cd-59e16e25c101.png)


![image](https://user-images.githubusercontent.com/75746171/138645336-ac78dade-6aaf-4e55-9a81-0b11fd1e95a8.png)

Örnek:
---
Elemanları 10 elemanlı double dizi olan boyutu 5 olan a dizisini tanımlayınız.

double a[5][10];

- Elemanları 10 elemanlı const char* olan 5 elemanlı

const char* a[5][10];

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138646006-1d032e81-5e55-497e-a05c-97ba12565eb5.png)

![image](https://user-images.githubusercontent.com/75746171/138646024-68fccfc6-5aea-4ff6-831a-97d304d8740b.png)


Not:
---

![image](https://user-images.githubusercontent.com/75746171/138646865-12e2c389-b8d2-48ad-9c82-7d58dd1c78bf.png)


a[5] ile *(a+5) aynı anlamda..

Çok boyutlu dizilere ilk değer verilmesi
---

Örnek: Diziyi yazdır.
---

![image](https://user-images.githubusercontent.com/75746171/138647906-3d319526-9979-4ebc-b031-12372af4342c.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138649892-079b1488-56ea-4d9b-99f0-f4874a07f95a.png)


Not:

int a[5][4];
Bu dizinin elemanlarının türü int değil. int[4], yani 4 elemanlı int diziler.


![image](https://user-images.githubusercontent.com/75746171/138650814-3f1bb110-0cec-492d-b5a5-c4a91862acf4.png)

typedef yaptık bu ikisi aynı oldu.

Ders 41 (25.10.2021)
---
![image](https://user-images.githubusercontent.com/75746171/138652770-b78987f6-bdc4-43a8-969b-d6c120966df2.png)

- Bu diziler türleri farklı olan diziler.
- a, elemanları 20 elemanlı dizi olan bir dizi
- b, elemanları 8 elemanlı dizi olan bir dizi
- c, elemanları 4 elemanlı dizi olan bir dizi.

Bu dizilerin türleri tamamen farklı. Dolayısıylar bunların adreslerini isteyen fonksiyonlar farklı parametrik yapıdadır.


Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138664512-a70e04ea-7861-4ed4-992c-c838d2a438f0.png)

![image](https://user-images.githubusercontent.com/75746171/138664561-2bf88bf2-5e63-4eba-bce8-8b26f1d12860.png)

Örnek: Diziyi yazır
---
![image](https://user-images.githubusercontent.com/75746171/138665577-f61e903a-27ae-4121-96cf-a7702a631526.png)


Not: Dikkat!
---

![image](https://user-images.githubusercontent.com/75746171/138666280-40c8547d-3901-46ba-8250-1ee2347e89c0.png)

- erdinc proramın sonuna kadar bellekte kala nbir string literali, static ömürlü bir dizi.
- Bu şekidle bir tanımlama yaptığımızda aslında 2 ayrı işlem yapılıyor birisi pointer değişken diğeri de char dizi.

- mustafa ise programın sonunak kdar bellekte kalan bir char dizi değil. 


Not:
---

![image](https://user-images.githubusercontent.com/75746171/138667485-d2238e4f-9e73-4c8e-8953-374aa94aaaba.png)


- Pointerları fonksiyonun parammetre değişkenleri olmaları urumunda farklı tanımlanabilir.
- Bu bir dizi değil. Fonlsiyonların parametre değişkenleri dizi olamaz.

 ![image](https://user-images.githubusercontent.com/75746171/138667691-4f3075a8-a9b0-4328-9e8f-1140cc0587c2.png)

Bunların arasından da bir fark yok.

Bazı önemli standart c fonksiyonları
---

![image](https://user-images.githubusercontent.com/75746171/138668323-74567224-779f-4025-9f1b-4aecd53bc722.png)

Böyle yazdığımızda 3452 tam sayısını tutmuyor. Bu dizide tutulanlar 3 4 5 2 sayılarının ascii kodları ve sonda da null karakter var.


atoi : Alphasbetic to integer
---
![image](https://user-images.githubusercontent.com/75746171/138668997-69e8ce65-d5b5-4674-a157-f1c7b8c1c41e.png)


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138672106-95a2aec4-d23e-432d-9a4c-cb5984026f72.png)

![image](https://user-images.githubusercontent.com/75746171/138672157-b7fbd1bd-8a70-40a8-a78b-ee37f732d4be.png)

atol: Yazıdan long değer çekiyor
atof: Yazıdan float değer çekiyor.

cppreference.com sitesinden bakabilirsin.

Yazılan tüm fonksiyonlar:

![image](https://user-images.githubusercontent.com/75746171/138673574-852695b0-f5b4-46f8-a2dc-4bc5fe0e5682.png)


strtok fonksiyonu: string tokenize
---
Yazının içinden bir kurala uyan yazıları elde etmeye (tokenlarına ayırmaya) çalışıyor.

Ör: bir yazıdan kelimeler, bir yazıdan telefon numarası

![image](https://user-images.githubusercontent.com/75746171/138673877-0963a2c0-6fac-4635-ad33-8c2bb5950b8e.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138674308-a43c2840-2d07-441a-8147-db6ee0ba833c.png)

![image](https://user-images.githubusercontent.com/75746171/138674355-24ffb785-76fd-45fd-b641-eddcceb47117.png)

- Null adresi geçmemizin nedeni fonksiyonun ikinci çağrı mı ilk çağrımı olduğnu ayır edilmesini sağlamak. Fonksiyona gelen değişken null poniter ise ilk çağrı olmaıdğını anlıyor.

![image](https://user-images.githubusercontent.com/75746171/138674955-b77de05b-5b08-443d-aff6-7d7bdba2ed4f.png)

Bu şekilde tokenin sonuna null karakter koyuyor. Aslında null pointer döndürdüğünde static bir değişkende null pointerin adresini tutuyor ve aramaya kaldığı yerden devam ediyor.

Bellek üstünde formatlı okuma yazma işlemleri
---

Formatlı giriş çıkış işlemleri 3 farklı biçimde yapılıyor.

Formatlı çıkışi işlemleri:
- Fkrmatlanmış veriyi standart outputa yazıyoruz. (Konsol ekrana bağlıysa yazı ekranda çıkıyor.
- formatlı yazı char dizide oluşturuşuyor. (Ekranda değil char dizide tutuluyor) (Bellek üstünde yazma işlemi)
- Dosyaya yazılıor

Formatlı çıkış işlemleri yapan fonmksşiyonların hepsi aynı (printf). Parametrik yapıları ve isimleri farklı.

printf - Çıktısını standart outputa veriyor
sprintf - Çıktısını belleğe veriyor
fprintf - Çıktısını dosyaya veriyor.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138676347-ec06d9aa-f5d5-48f0-8d2f-a9f4576e56c0.png)

sprintf çıktısını bu diziye yazacak.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138676866-f253cb2a-f1fa-4f93-830b-e7c3505316d2.png)

Program çalıştığında ekrana bu yazıyı yazacak fakat ben ekranda görmek istemiyorum dosya isminde görmek sitiyorum.

![image](https://user-images.githubusercontent.com/75746171/138677153-1bac01aa-1c78-4a8f-92ab-f7641b355291.png)

Dosyayı oluşturduve içine yazıyı yazdı.


sscanf fonksiyonu farklı olarak karakterleri standart inputtan almıyor, bizim verdiğimiz adresteki diziden alıyor. 

fscanf fonksiyonu ise dosyadan eçkiyor.

Programı sonlandıran standart c fonksiyonları
---

- exit
- atexit
- abort


Ders 42 (25.10.2021)
---

2 tür program sonu var.

- Normal termination (exit)
- Abnormal termination (abort) 

Programlar main'de sonlanmak zorunda değil.
Farklı bir fonksiyonda da bitebilir.

atexit:
---

![image](https://user-images.githubusercontent.com/75746171/138684123-e138a352-9324-4962-afc7-9db46638adb7.png)

- Adresini aldığı fonksiyonu kaydediyor. 
- Yani adreslerini elemanları function pointer olan bir diziye yazıyor. Exit çağırıldığında programı sonlandırmadan önce atexit in yazdığı fonksiyon pointer dizisine erişiyor ve orada adresleri yazan fonksiyonu çağırıyor. (Sondan başa doğru)

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/138684726-5e22bdd1-6390-4338-aefe-1b58d4b28a17.png)

![image](https://user-images.githubusercontent.com/75746171/138684752-e129919b-d9e3-467a-8bba-c7cf20093a23.png)


Not:
---
return 0; --- exit(0) 'a dönüştürülüyor.
return 1; --- exit(1) 'a dönüştürülüyor.

- Eskiden main fonksiyonunun içinde return statement olmaması onun çöp değer döndürmesi anlamına geliyordu fakat c99 standartları ile eğer return koymazsan yazmış kabul ediliyor.

Abort fonksiyonu
---

Paramatresi de yok geri dönüş değeri de yok. Direkt programı sonlandırıyor.


Dinamik Bellek Yönetimi
---
Dymacmic memory management

Storage Durations
- automatic
- static
- dynamic

Dinamik ömür: Programın çalışma zamanında istediğim herhangi bir anda neyneyi hayata getircem ve istediğim zaman çıkarıcam.

Örnek:
---

func fonksiyonu olsa ve kendisini çağıran koda kendisinin oluşturduğu bir nesneyi iletmek istese, bunu diğer ömür kategorileri ile yapamayız. Otomatik ömürlü nesnenin adresi döndürülemez. Static ömürlü olsa hep aynı nesnenin adresini döndürürüz. Dinamik ömürlüde her seferinden farklı nesne gönderrebiliriz.

Dinamik ömürlü nesne ile dinamik bellek yönetimi bağlantısı:

Dinamik ömürlü nesnelerin bir yere sahip olması gerekiyor. Bu bellek alanının programın çalışma zamanında elde edilmesi süreci dinamik bellek yönetimi oluyor.

Not: Sanal bellek nedir?
---
İşletim sistemi bellekte yeterli alan olmadığında iskteki alanları sanki bellekmiş gibi kullanılmasını sağlıyor.


Özet:
- Dinamik bellek yönetimi, programın çalışması sırasında bir bellek alanının elde edilmesine ve kullanımı sona erdiğinde sisteme geri verilmesi ile ilgili faaliyetlerdir.

- Dinamik bellek yönetimi c ve c++ programlama dillerinde en fazla kodlama hatası yapılan bölüm.
- Maliyeti arttırır. Hata yapma riskini arttırır. Kod okunmasını zorlaştırır.

Dinamik ömürlü nesneler (programın çalışma zamanında bellekte yeri ayrılan nesneler) kllandığı bellek alanına heap bellek alanında tutuluyor.

Bellek alanını alıp işi bittiğinde geri vermeme olayı memory leak problemini oluşturuyor. (Bellek sızıntısı)

Dinamik bellek yönetimi fonksiyonları
---
malloc : Memory allocation

- Program çalışma zamanında bellek alanına ihtiyaç oldjğunca çağırılır. Temiz bellek verir.

callog : 

- malloc ile aynı fakat elde edilen bellek bloğunu garbage value ile bize veriyor.

realloc: 

- Daha önce elde edilen bellek bloğunu büyütmek istediğimiz zaman çağrılır.

free :

- Bellek bloğunu geri vermek için çağrılır.

malloc fonksiyonu
---
![image](https://user-images.githubusercontent.com/75746171/138689986-f047f49b-99df-4a83-86b9-2d7044e72a3b.png)

kaç byte lık blok istediğini söyle ve elde etmeye çalışayım. Elde edebilirsem elde ettiğim bloğun adresini döndüreyim. Edemezsen null pointer döndüreyim.

Önemli
--
- Asla dinamik bellek işlevleriyle elde edilmemiş bellek bloklarını free etme girişiminde bulunma. Undefined behaviour
- Free işlevi ile dinamik bellek boyutunu küçültemezsiniz.
- Free çağrısından sonra bellek bloğunun adresini tutmakta olan pointer geçersiz (invalid) pointer olur.
- Free edilmiş bir bellek bloğunun tekrar free edilmesi işlemi tanımsız davranış.

free(pd) yaptığımızda pd'nin değeri nul pointer mıdır?
- Hayır. pd'nin değerini değiştirecek fonksiyonun çağrısı ancak o değişkenin adresi ile yapılablir.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/138694018-e518f39b-8498-4425-9a9d-8aa9cb98d0b8.png)

![image](https://user-images.githubusercontent.com/75746171/138694056-ec5e8e60-8ed3-4c3c-9efb-aff083904c18.png)


Soru
---
Dinamik bellek kullanılacak
20 tane 1000 byte lık blok
1000 tane 20 byte lık blok
arasında bir fark var mıdır?

- Evet. Her malloc çağrısı veri yapısına giriş yapmak demek.
- Yani her tahsisat için 16 bytelık bellek bloğunu kullandık. 
- 20 x 16 = 320 byte
- 1000 x 16 = 16000 byte

Yine bellek bloğu ihtiyacının 16 byte olduğunu düşünelim.
40 byte istersek 40 byte ayırtmıyor. 40+16 byte ayırıyor. 16 byte ını kendi kullandığı veri yapısına giriş için kullanıyor.


Ders 43 (31.10.2021)
---

![image](https://user-images.githubusercontent.com/75746171/139580779-8442a73f-26fa-4832-8d67-2e428a9d14f3.png)

Verdiğimiz adresteki yazının bir kopyasını çıakrtıyor ve adresini döndürüyor. Ancak kopyasını dinamik bellek bloğunda oluturuyor. Yani işimiz bittiğnide free etmemiz gerekiyor.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/139580873-ffba8567-957c-432f-ae74-14811e40b6b3.png)

En sonda free yapmazsak bellek sızıntısı oluyor. 

![image](https://user-images.githubusercontent.com/75746171/139580893-855c0e29-2ffc-4414-baea-7269e6174c34.png)

Bellek sızıntısı:
---
Dinamik bellek yönetimi fonksiyonları ile elde ettiğimiz belle blokları heap denilen bellek havuzundan veriliyor. Bu alan sonsuz değil. malloc ile bu alandan bir yer almıl oluyoruz. Bu alanı geri verene kadar başka bir amaçla kullanılamıyor. 

- Bu alanlar geri verilmezse başka bir kodun dinamik bellek bloğu ihtiyacı olduğu durumda yer kalmadığı için bu ihtiyaç karşılanamayacak.

- Birçok dilde garbage collector denilen bir sistem var. C'de bu sistem yok. Bi dillerde dinamik belle kyönetimi kolay. Bellek bloğu alınıyor fakat geri vermek zorunluluk değil. Bu alanın kullanımı sona erince sistem tarafından geri veriliyor.

strdup fonksiyon kodu.
---

Yazının uzunluğu + 1 kadar alını ayırmam gerek. (Null karakter)

![image](https://user-images.githubusercontent.com/75746171/139581532-41273d00-9310-4f92-a751-fa477d76c1c1.png)

Not:
---

Sınıftaki öğrecilerin notlarını tutmakl için bir diziye ihtiyaç var. 

![image](https://user-images.githubusercontent.com/75746171/139581839-33f4a078-e1f2-45d2-b98a-af81ff386e4e.png)

Bir bellek bloğu elde edip onun adresinin bir poniterda tutabiliriz. pd int türden n elemanlı bir dizinin başlangıç adresi olarak kullanılabilir.

Dinamik bir matris oluşturmak.
---
Matrisin satır ve sutunsayısı programın çalışma zamanında blli oluyorsa dinamik bellek yönetimii le oluşturulabilir.

row 5
col 20

5 tane 20 elemanlı diziye ihtiyaç var.

Ben 20 elemanlı dizileri dinamik bellek yönetimi ile elde edebilirim.

Adresler ile bunlara erişebilirm. Bu adresleri tutan dinamik 5 elemanlı bir poniter dizisi oluşturmam gerekiyor.

Ve dinamik pointer dizisinin de adresini tutan bir pointera ihtiyaç olacak. Bu da int** olacak.

![image](https://user-images.githubusercontent.com/75746171/139582146-fc3868a9-0dd1-4070-a980-5ce253c8afdd.png)



![image](https://user-images.githubusercontent.com/75746171/139582204-c6c7fc82-540a-4f6d-8523-2ad904e56742.png)

- row adet pointerın sığabileceği bir pointer dizisi için yer ayırmış oldum. 


Memory fragmentation
---
Parçalara ayırma.

![image](https://user-images.githubusercontent.com/75746171/139583222-eeb10fe5-c248-4f5b-9999-8c98f9f51a89.png)

Böyle bir durumda yüksek bir belleke ihtiyaç oldu ve ardışık olarak yok. 

--------

Not:
Malloc fonksiyonuna 0 ile çağrı yapıldığında 

![image](https://user-images.githubusercontent.com/75746171/139583455-9bfe9fe8-14ac-47d5-bad4-5aa796d224c7.png)

![image](https://user-images.githubusercontent.com/75746171/139583461-0f161437-d465-41d4-8714-af0afac9a353.png)

Callog
---
![image](https://user-images.githubusercontent.com/75746171/139583491-2a89ffd7-ae16-4215-8686-497d87b0244a.png)

malloc'un tel parametresi var. 100 elemanlı int dizi için yer ayırdığımda 100xsizeofint. 
callog ise ilk parametresi kaç tane nesne için yer ayırdığım, 2. parametresi her bir nesnenin sizeof değeri.

reallog fonksiyonu
---
re ön eki tekrar anlamında. Daha önce elde edilmiş bellek bloğunu büyütme için, yada küç.ültmek için.

Birinci parameteresi bellek bloğnun adresi, ikincisi bellek bloğunun yeni boyutu.

- Başarısız olursa null poniter, başarılı olursa elde edilenbellek bloğınun adresini döndğrür.

![image](https://user-images.githubusercontent.com/75746171/139583971-4b939dcb-2006-4c05-97f8-9bdc6cbb7c76.png)

Not:
---

büyük boyutlu alanımız var. realloc çağırıldığı zaman çok az bir alan arttırsa bile çok büyük bellek bloğu başka bir alana kopyalanıyor. Bunun cidi bir maliyeti var. Reallocation take time! Büyük ihtimalle eski bellek bloğunun yeni bellek bloğuna kopyalanması ile gerçekleşecek.

reallocation invalidates pointers!
Yani: Malloc ile elde etitin bellek bloğnu realloc ile büyüttüğün zaman eski bellek bloğu geri verilmiş olabilir. Sen eski bellek bloğundaki pointerları dereference edersen tanıksız davarnış.

Not:
---
realloc çağrıalrında 1. parametreye bull pointer geçilirse realloc malloc gibi davranır.

realloc(pd, n) = malloc(n)

Ders 44 (31.03.2021)
---

Veri yapısı: Mantıksal ilişki içindeki verileri erişilebilir şeklide bir arada tutan düzenekler.

Default kullanılan veri yapısı dinamik dizi. İhtiyaç olduğunda diğerşerini kullanıl-yırouz.

Storage class specifiers (Yer belirleyicileri)
---
C'nin bazı anahtar sözcüklerine verilen özel isimler.

- auto
- register
- extern
- static

type qualifiers (tür niteleyicileri)
---

- const
- volatile
- restrict

linkage (bağlantı) kavramı ile tanışacağız.

- auto artık kullanılmıyor.
- register da aynı şekilde kullanımı azalıyor.

auto
---
Değişkenlerin bildiriminde kullanılan bşir anahtar sözcük.
![image](https://user-images.githubusercontent.com/75746171/139587310-6d245e55-ea17-4ef5-89a6-77ae12d53d53.png)

- Değişkenin otomatik ömürlü olduğunu anlatıyor.

register
---
Derleyiciye bu değişkenin register'da tutulması ricasını iletiyoruz.

32 bit işlemci dediğimizde 32 bit registerın büyüklüğü. Değişkene işlem yapılması için register a çekiliyor.

Neden gereksiz hale geldi?
Çünklü artık modern derleyiciler bu optimizasyonu çpok iyi yapıyor. Derleyiciye registerda tut dememize gerek yok.

static
---
Blok içinde ve globalde kullanımındaki anlamı farklı.


Neden static yerel değişkenleri kullanıyoruz?

- Global değişkenleri ömrü ile static yerel değişkenlerin ömrü aynı sadece scope farklı.

- Çağrılan fonksiyonun kendisini çağıran fonksiyona değer iletmesi gerekiyor. Bunun yolalrından biri static bir yerel değiŞkende bu değeri tutmak ve bunun adresini iletmek.

Static yerel değiğşkenin adresini döndüren programlar.

İsimlerin bağlantı (Linkage) kavramı
---

farklı kaynak dosydaki isimlerin aynı varlığa ait olması, external linkage (dış bağlantılı). 

- external linkage
- internal linkage
- no linkage


![image](https://user-images.githubusercontent.com/75746171/139589086-1556a133-03a8-4de2-b03a-fd30704c22a5.png)

- Tanımlanan global değişkenin ismiyle diğer kaynak dosyalrda kullanılabilsin istiyoruz. Dış bağlantıya ait bir isim yapmak zorundayız. External

- Kullanıldığında başka bir varlığa ait olsun diyorsan internal.

- Normal tanımlanan gloabal değişkenleri external linkage
- Fonksiyonlarda da aynısı geçerli.


nutility (başlık dosyası) içinde extern olarak tanımladıktan sonra main içinde bu değişkeni kullanabiliriz. (Önişlemci include komutu ile birliklte)

![image](https://user-images.githubusercontent.com/75746171/139589274-52370455-1e72-465b-872d-917feb3d7efb.png)

- Extern sadece bir bildirim. Derleyici bunun için yer ayırmıyor.

- Global düzeyde static anahtar sözcüğünü kullandığımız zaman bu isim iç bağlantıya ait demektir. Bu değişkeni diğer kaynak dosyalardan ismi ile kullanılmasını isytemiyoruz.

- Aynı şekilde fonskiyonlarda sadece bu kaynak dosyada çağırılmasını istiyorsam static kullancam.

![image](https://user-images.githubusercontent.com/75746171/139589628-424861a6-13bb-4acc-b03d-6335b04d4e17.png)

![image](https://user-images.githubusercontent.com/75746171/139589645-12d3ea01-7e5c-4794-a9c6-d796595f5897.png)


Ders 45 (01.11.2021)
---

Bir global değişken ya da bir fonksiyon söz konusu olduğunda 2 seçeneğimiz var:

1. Global değişken ya da fonksiyonu diğer moddüllerden ismi kullanılır kılmak (external linkage)
2. Global değiğşken ya da fonksiyonu sadece bu kaynak dosya kullanabilsin. (internal linkage)

No linkage isimler : Parametre değişkenleri ve yerel değişkenlerin isimleri.

- Header file'da extern bildirimi ile tanımlanan x dxdeğişkenini, başlık dosyasını include ettiğimde ve x ismini kullandığımda derleyici x ismini arayacak ve extern bildirimi ile karşılacşacak ve bunun için ayrıca yer ayırmayacak.
- Değişkenlerde extern zorunlu fakat fonksiyonlarda default olarak extern yazıyor ayrıca belirtmeye gerek yok.

- Global değişkeni ya da fonksiyonu diğer modüllere kapatmak istiyorsak static anahtar sözcüğü ile tanımlayacaz. (Yerel düzeyde kullanılan static anahtar sözcüğü ile karıştırma)
- Ve böyle bir değişkeni başka modüller de tanımlayabilir, fakat bunlar ayrı ayrı değişkenlşer.


- Nesne yönelimli programlama ile benzerlik oluşturmak amaçlı Makro ile private ve public sözcükleri tanımlanabilir.

#define		private		static

- makroda ismi yazıp karşılığını yazmazsam derleyici bunu görmüyor ve siliyordu. Burdan hareketle;


 ![image](https://user-images.githubusercontent.com/75746171/139657686-b21cc75f-0fc3-430d-be95-697f3110dc63.png)

![image](https://user-images.githubusercontent.com/75746171/139657701-31e46588-cc10-4518-bf52-10fe5d59595b.png)

- Fonksiyonlar için böyle bir ipucu verilebilir.


Namespace
---
C++ dilinde global isim alanı namespace delinen varlıklar içeriyo.r. Namespace elr isimleri birbirinden ayırmak gizlemek çakışmayı önlemek için kullanılanvarlıklar. İstediğimiz kadar oluşturabiliriz. Ayın isimde farklı namespacelerde tanımlanabilşir. C'de namespace yok. 

type qualifiers
---
- Const
- volatile
- restrict  (C++'da yok)

Volatile Anahtar Sözcüğü
---

Bir değişkene bir sabit atadğımızda onu kendi kodumuz değiştirmediği sürece değişmemsi lazım. Fakat öyle senaryolar var ki Bizim kodumuz bir değişkenin değerini değiştirmese de program dışı kaynaklar x değişkeninin değerini değiştirebiliyor.

Örneğin bir başka işlemci kendi reigsterını değiştiriyor fakat bu bizim kullandığımız bir bellek alanı ve bir adres vasıtası ile ona erişiyoruz. 

Ya da kesmeler ile olabilir. Kesme bir fonksiyonu çağırıyor ve o sziin değişkeninizi değiştiriyor. Fakat bu bizim progrmaımız dışında oluşturulmuş ayrı bir program.

Derleyici bizim değişkenimizin program dışı kaynakalr tarafından değiştirilebileceğinibilmezse bir takım optimizasyonlar yapıyor ve o bellekteki nsneye erişmek yerine onun daha önce registerda tutulan değerini kullanabiliyor. Böylece programımızın lojik yapğısoından bir farklılık oluyor.

![image](https://user-images.githubusercontent.com/75746171/139666736-22bcfe62-afbb-4617-a36b-f08418f2b5ec.png)

Örneğin burada bu döngüden çıkması için bir kesmenin x'i değiştirmesi gerekiyor ancak derleyici bunu bilemez, derleyici kaynak koda bakıyor. X'i değiştirecek bir kod olmadığı için x'in registerdaki değerini kullanıyor. X'in değeri program dışı kaynaklar tarafından değiğştirildiği için derleyicinin yaptığı optimizasyon, kodumuzun lojik yapısını değiştiriyor. 

Kesme geldi ve x'i değiştirdi fakat derleyici bunu farkında olmadığı için x'in eski değerini kullandı.

Bu gibi durumlarda biz değişkeni volatile anahtar sözcüğü ile tanımlıyoruz. Ve derleyiciye şunu söylüyoruz:

- x değişkeninin değeri sen görmesen de program dışı kaynaklar tarafından değiştirilebilr, ben kaynak kodda x'i kullandığpım her yerde hiçbir optimizasyon yapmayacaksın. x'in bellek alanına erişip oradaki değeiri alacaksın. 
- Eğer bunu yapmazssak x'in değer değişikliğini derleyicinin ürettiği kod yapkalayamayacak.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/139667558-ea4b15d6-5d0c-4a80-9bd6-37eb88f573a4.png)

biz yıldız p'yi kullandığımız zaman derleyici o adresteki nesnenin değerini elde etmek zorunda değil. Çünkü O değeri en son bir bellek alanında ya da register da tutuyor olabilir. Yani biz kullandıığımız zaman nasıl olsa değer değişmedi diyerek en son sakladığı değperi kullanıyor olabilir. Bu bir optimizasyon tekniği.

Biz volatile kullanırsak derleyicinin optimizasyon yapmasını engelleriz ve doğrudan bu adresteki nesnenin değerini get etmek zorunda bırakırız.

Örneğin interrupt yazdığınız fonksiyondaki flag'ler volatile olmak zorunda. Eğer yapmazsak flag değeri değişmesine rağmen bu değer değişikliği runtime'da yakalanamaz.

restrict  Ders 45 sonu.
---
C99 standartları ile dile eklenen bir anahtar sözcük. 
C++ dilinde yoktur.

Bir pointerın gösterdiği nesneyi gösteren tek pointer olduğu, onun gösterdiğin nesneyi gösteren başka bir pointer olmadığını anlatıyor.

![image](https://user-images.githubusercontent.com/75746171/139668800-7db110c1-f570-4d68-84bb-91d42e1d8440.png)

Bu fonksiyonun kodu çalışırken dest in gösterdiği nesne ile src nin gsöterdiği nesne farklı nesneler.
Bu pointerların aynı nesneyi gösterme ihtimali yok.

Ders 46 (01.11.2021)
---

User defined types
---
Programcı tarafından oluşturulan türler

Dilin bazı araçlarını kullanarak kendi türümüzü oluşturabiliyotuz. Bunun için bildirim yapmamız gerekiyor.

User defined types: Hazır olarak gelmeyen ama bir bildirimi le kullanılabilir hale getirdiğimiz türler.


User defined types oluşturmak için 3 araç var.

1. Structers (Yapılar)
2. Union (Birlikler)
3. Enumarations (Numaralandırmalar)


![image](https://user-images.githubusercontent.com/75746171/139710798-8d72442f-7091-4210-b62e-cf6fd474da37.png)

Yapı ve yapının elemanları. Bu bellekte bir yer kaplamıyor bu sadece bir bildirim.


![image](https://user-images.githubusercontent.com/75746171/139710856-e7785fde-ea18-413c-890b-bc8982febd2f.png)

Burada mydata bir nesne, bellekte bir yer kaplıyor.

- Bir yapı türünün sizeof değeri (storage ihtiyacı) elemanlarının sizeof değerlerinin toplamı kadardır. 

Memory selection operators
---
Yapının elemanlarına erişim için kullanılıyor.

Not:
---
![image](https://user-images.githubusercontent.com/75746171/139713767-f5a591ec-fc3c-4661-ba57-348f39b36e8c.png)

- Derleyici x değişkeni için ayrı bir yer ayırıyor ama mydata.a için ayırmıyor, struct data türünden mydata nesnesi için yer ayırıyor.
- Yani a, mydata nesnesinin içnde yer alan int türden bir değişken.


![image](https://user-images.githubusercontent.com/75746171/139714151-5d3b55c4-56c9-4287-b7a9-02f10b385fe7.png)

 
![image](https://user-images.githubusercontent.com/75746171/139715716-65266780-9e01-4cc4-888c-6393461135ab.png)

mydata nesnesinin x'ine erişmiş olduk.

![image](https://user-images.githubusercontent.com/75746171/139715797-fd0ee5f5-b862-47ed-95e4-7fc2efd50cf1.png)

Bu ikisi de aynı anlamda.

![image](https://user-images.githubusercontent.com/75746171/139721902-148080e5-272f-40df-ad26-cd808b4cb857.png)

Yapı nesnesine bir yapı nesnesi atandığında derleyici karşılıklı elemanalrı birbirine kopyalıyor

![image](https://user-images.githubusercontent.com/75746171/139722009-482d3b5c-00c6-46ef-95d4-4d25378be0a2.png)

Yapı nesnelerine ilk değer verme
---
![image](https://user-images.githubusercontent.com/75746171/139722572-84a5191a-077d-4ead-ac60-9185940569b3.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/139722950-d0441680-c949-4e9b-adc9-a6e35ca8bbea.png)

![image](https://user-images.githubusercontent.com/75746171/139722971-a4ec3811-2301-40ce-b2ad-4e0bd454bf05.png)


![image](https://user-images.githubusercontent.com/75746171/139723273-f6f3a71f-07ad-4efd-a156-ee587437be5a.png)

![image](https://user-images.githubusercontent.com/75746171/139723303-0dffee46-153a-4cbd-b7a4-3fedff790dde.png)

Not:
---
![image](https://user-images.githubusercontent.com/75746171/139723971-fda15e1b-405a-4b4e-bcde-92bbc91789ac.png)


Burada hem struct data türünü bildiriyorum hem de struct data türüden bir global değişken tanımlamış oluyorum. 

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/139724939-304a20eb-1476-4524-91cb-b15f92ea2c16.png)

![image](https://user-images.githubusercontent.com/75746171/139724981-f6d5a47c-f6c8-4cab-ac7b-3dde1432338c.png)

Not:
---

![image](https://user-images.githubusercontent.com/75746171/139725367-657b300d-94d1-4210-bba7-48cd890a2741.png)

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/139725581-66473d1a-206c-4bab-b868-252ee72bf2a4.png)

![image](https://user-images.githubusercontent.com/75746171/139725606-82c81d9a-4148-4a6e-bc08-15d00a9f2e42.png)

Not:
--
![image](https://user-images.githubusercontent.com/75746171/139725934-a8f06240-31d4-49a0-b942-ee822fb8e926.png)

Aynı anlamdalar.

![image](https://user-images.githubusercontent.com/75746171/139726021-ed1c8237-6f0d-4967-ae2b-8e532f49dac1.png)

Burada ise bir sentaks hatası yok.

![image](https://user-images.githubusercontent.com/75746171/139726136-80495d39-eb43-43ab-988f-7e35d505907b.png)

Dizinin 2 indisli elemanının id isimli elemanını 1 arttırdı.

Ders 47 (01.11.2021)
---

2 operatör öğrendik.

- Dot operator
- ->(ok) operator

![image](https://user-images.githubusercontent.com/75746171/139728541-7fa30d1f-85d2-4265-8513-96b8b269596f.png)

Aynı anlamda.

Yapılar ve typedef bildirimleri
---

En sık kullanılan yer yapı türlerine eş isimler vermek.

- Struct anahtar sözcüğünden kurtulmanın yolu typedef bildirimleri.

1. Hangi türe eş isim vereceksen o türden bir değişken tanımla.
2. Başına typedef getir.
3. Değişken ismini değiştir ve bu türe vermek istediğin isim yap.

![image](https://user-images.githubusercontent.com/75746171/139729503-fb5c4aec-fe23-4fcd-93a8-f07ce19fd51e.png)


10 Elemanlı int dizi türüne typedef ismi verebiliriz.

![image](https://user-images.githubusercontent.com/75746171/139729604-1e051e47-f43d-49dd-b525-f53fbbb4b826.png)

![image](https://user-images.githubusercontent.com/75746171/139729701-a0445347-b7fa-4328-a24e-48533b70e811.png)


Yapılarda typedef
---
![image](https://user-images.githubusercontent.com/75746171/139729812-5adebf63-dda3-4e6b-a634-51ed05393c12.png)

Önce bu türden bir değişken tanımladık.

![image](https://user-images.githubusercontent.com/75746171/139729859-9f941acb-143b-4993-b021-5044776ebfae.png)

Sonra başına tyedef koyduk ve değişken ismini tür eş ismi olarak değiştirdik.

![image](https://user-images.githubusercontent.com/75746171/139729971-29c287b7-5591-41d9-9908-d0be5bb59169.png)

- Artık bu ikisini de kullanabilirim.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/139730255-8ef6ed92-d952-4da8-807b-b02950bd4502.png)

- Burada bir yapı türü oluşturdum bu türün ismi hem struct data ve aynı zamanda bir typedef ismi var ve o da data.

![image](https://user-images.githubusercontent.com/75746171/139730380-6c78bb30-fa91-475e-beff-d5a6cd05da71.png)

Hem yapı tanımlıyoruz hem isim bildirimi yapıyoruz.

Not :
---
En sık kullanılan typedef bildirimlerinden biri.


![image](https://user-images.githubusercontent.com/75746171/139730804-09259af8-d9d3-4ce9-a5e0-1b94f3a9b23a.png)

- Ve böyle tanımlarsak sentaks hatası.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/139730925-ccc06418-b70b-4024-b49d-b6e778bae13d.png)

- Burada aynı şekilde başında typedef olduğu için DataPtr, struct Data* türünün eş ismi.

Artık böyle yazabilirim:

![image](https://user-images.githubusercontent.com/75746171/139731089-a341a3dd-756a-40e7-a0d4-9dcd5fb3dc9a.png)


Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/139731252-4b2b25e8-c4d9-45db-8a62-4aac727abed7.png)

g, global bir değişken. ptr global bir pointer ve bu türün bir ismi yok.

![image](https://user-images.githubusercontent.com/75746171/139731449-1cd6ac81-a416-43cc-9d9e-b67450224396.png)

- İster etiket ismi olsun ister olmasın, g struct data türünden bir global değişkenin ismi, ptr ise struct data türünden bir pointer değişkenin ismi.
- Şimdi başına typedef anahtar sözcüğünü getirirsek, 

![image](https://user-images.githubusercontent.com/75746171/139731534-771859ab-e204-46cf-a0aa-5b7a5c4eb6e8.png)

- g, struct Data türünün eş ismi, ptr ise struct Data* türünün eş ismi.
![image](https://user-images.githubusercontent.com/75746171/139731938-00246bca-5a96-41bf-b4bc-e4b73622df55.png)

- Burada ise DataPtr pointer türünün eş ismi fakat bu türün bir ismi yok.

Bu ne işe yarayabilir?
- Böyle bir typedef bildirimi bu türden sadece dinamik ömürlü bir nesne oluşturma olanağı veriyor.

Açıklama:

![image](https://user-images.githubusercontent.com/75746171/139732124-2ac6944e-7805-49a7-b925-7aedcca9462c.png)

- Sizeof operatörünün operandı bir ifade olduğunda derleyici o ifadenin türüne bakıyor ve sizeof değerini elde ediyor. Burada bu tür herhangi bir şekilde isimlendirilmemiş ama derleyici bu ifadenin türünün yukardaki yapı türü olduğunu gördüğü için sizeof değerinin 16 olduğunu biliyor. ve malloc ile nesnenin ihtiyaç duyduğu bellek alanı ayrılmış oluyor.

Diğer önemli nokta ise:
- pd bureada çöp değerde, aslında çöp değerde olan pd'yi dereference ettiğim için tanımsız davranış olması gerekir fakat değil. Çünkü derleyici sizeof operatörünün operandı olan ifade için derleyici kod üretmiyor.

Örnek:
---

![image](https://user-images.githubusercontent.com/75746171/139732875-9c70bb53-7361-4855-8419-71b127afd686.png)

- Böyle bir typedef bildiriminde bir yapının bildirimi yapılmış oluyor. Fakat u yapı türüne bir isim verilmiyor. Fakat bildirilen yapı türünden nesnelerin adresi olan türe DataPtr ismi veriliyor.
- Bunun yapılma amacı bu türden oluşturulacak nesnelerin salt dinamik ömürlü olmasını sağlamak. 

Yapılar ve Fonksiyonlar
---

Bazı c kütüphanelerinde fonksiyonların parametrik yuapısı şu biçimde:

![image](https://user-images.githubusercontent.com/75746171/139742616-a53d8f0f-95ac-4000-8666-d7c407006f39.png)

T bir yapı türü. T türünden bir nesne oluşturacaksınız. onun elemanlarından bazılarını set edeceksiniz. O nesnenin adresini böyle bir fonksiyona göndereceksiniz. Fonksiyon sizin set ettiğiniz elemanların değerlerini input olarak kullanacak. Ama kendisi de iletmek istediği delğerlere adresini aldığı yapı nesnesinin bazı elemanlarını yazacak. Yani hem adresini verdiğiniz nesneyi input olarak hem de kendi ürettiği derğerleri iletmek için kullanacak. Böyle parametrelere in-out parametre deniliyor.



Şimdi fonksiyonun parametresine değil de geri dönüş değerine bakalım.

Bir fonksiyonun geri dönüş değeri
a) bir yapı türü olabilir
b) bir yapı türünden adres olabilir ve bir yapı türünden const nesne adresi olabilir.

En çok karşımıza çıkacak fonksiyon yapısı geri dönüş değeri bir yapı türünden adres olan fonksiyonlar.

API: Uygulama programcıları için oluşturulan arayüz. Application programmer's interface. Bize işimizi görecek bazı fonksiyonları sağlayan kütüphaneler.

----------------

Kullanacağımız kütüphaneler yapıları kullanarak parametreleri yapı türünden olan fonksiyonlar veriyorlar. 

- C tarzı kütüphaneler
- OOP (object orianted programming) tarzı kütüphaneler

C Tarzı kütüphaneler: Bu tür kütüphanelerde yapıların elemanlarını kullanarak işinizi görüyorsunuz.

Tüm elemanları bilmemiz gerekiyor ve sorumluyuz. Bu büyük bir yük.

OOP tarzı kütüphaneler: Yapının elemanlarını bilmemiz gerekmiyor. Çünkü kullanmayacağız. Yapmamız gereken kütüphanenin bize verdiği fonksiyonları çağırmak.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/139745465-2a452170-25b5-4c3a-a7c9-7333404f3fb2.png)

Bu fonksiyıonu çağırıyoruz ve bize date nesnesi adresi veriyor. Ama bu fonksyondan aldığımız adresteki nesneyi elemanlarına erişerek kullanmak yerine fonksiyonlara gönderiyoruz.Yani hrer şey fonksiyonlar yolu ile yapılıyor. Yapı nesnesinin değer değiştirmesi, değer elde edilmesi. 

Bu yaklaşım daha sağlam çünkü, hata riski az. Çağrılan fonksiynolar ona erişecek ama biz erişmeyeceğiz. 

<time.h>
---
struct tm yapısı

![image](https://user-images.githubusercontent.com/75746171/139746578-3ddf6417-5bb0-4840-a50c-a5fcf5d66419.png)

9 Elemanı var.
Her eleman tarih zaman bilgisinin bir bileşenini tutuyor.

tm_year;  Yıl değeri tutuyor. 1985 değil 1900 tutacak. O yüzden 1900 ekle.

tm_mon;  index 0 dan başlıyor. 0=ocak 1=şubat
tm_mday;  Ayın günü. 
tm_wday;  haftanın günü. 0 Değeri pazar.
tm_yday;  yılın kaçıncı günü olkduğuun tutuyor
tm_hour;  0-23 aralığında. 
tm_min; dakika
tm_sec; saniye
tm_isdst; is daylight saving time. Gün ışığı tasarruf modu. -1 ise bu bilgi tutulmuyor. 0 ise tasarruf modunda değiliz. nonzero değer ise tasarruf modundayız.

Standart time fonksiyonu
---

![image](https://user-images.githubusercontent.com/75746171/139747414-6f8b5050-3da4-4a01-9dbf-84b34a10e832.png)

time_t türünden nesnenin adresini alıyor ve bu adresteki nesneyi epoktan geçen saniye sayısı ile set ediyor.

Örnek:
---
![image](https://user-images.githubusercontent.com/75746171/139747713-33520cfc-6f98-4ca9-9d2f-1d58e0009089.png)


![image](https://user-images.githubusercontent.com/75746171/139747730-6b0c3b54-25d6-4b4d-9517-72e47e14d93d.png)

Saniyeleri sayarken görüyoruz.

Ders 48 (02.11.2021)
---

Gecikme sağlayacak bir fonksiyon:

![image](https://user-images.githubusercontent.com/75746171/139799127-30515c57-9aa4-40b5-aa7b-3c2673d2866f.png)

Ders 49 (02.11.2021)
---

Complete type, incomplete type
---
![image](https://user-images.githubusercontent.com/75746171/139802632-81127a88-6eb4-48c0-a76f-539a5d49f547.png)

Hata mesajı: Incomplete type is not allowed

![image](https://user-images.githubusercontent.com/75746171/139802830-dec6e1ca-71e4-42cc-b45a-f1981ed329a4.png)

- Bir yapı türünü belirli bağlamlarda "incomplete type" olarak kullanabiliriz.

struct Data;

Sadece böyle bir bildirimle yazabileceğimiz bazı kodlar var.

![image](https://user-images.githubusercontent.com/75746171/139803251-53d0d87a-b690-486f-af02-1407e85566e7.png)

Yani bir fonksiyonun bildiriminde fonksiyonun parametre türleri ya da geri dönüş değeri türü incomplete type olabilir.

![image](https://user-images.githubusercontent.com/75746171/139803407-e650af61-42a6-44dc-90c9-b994b45ffb6a.png)

- Yani bir yapı türüne eş isim vermek için o yapının complete type olması gerekmiyor.

![image](https://user-images.githubusercontent.com/75746171/139803546-47231551-59f8-4196-9878-5b58be35d827.png)

- Global değişkenlerin extern bildirimlerini yapabiliriz.  Burada extern tanımlama değil, derleyici bunun için yer ayırmıyor.

![image](https://user-images.githubusercontent.com/75746171/139804878-78be4e71-ea1e-41b7-8b94-5e07a054f592.png)

Not:
---
Eğer bir yapı türünü başlık dosyasında salt incomplete type olarak kllanmılıyorsa o zaman onun başşlık dosyasını include etmemize gerek yok.

Ders 50 (02.11.2021)
---
Composition
---
Bir yapının elemanlarının başka bir türden olması

- Bir yapını elemanı kendi türünden olamaz.

Fakat kendi türünden bir pointer olabilir.

![image](https://user-images.githubusercontent.com/75746171/139819736-d5c5f983-9c43-4e8d-ad9b-6394fcda520b.png)

- Çünkü bir pointerın sizeof değeri sistemde belli. Derleyici bu bildirimden stuctdata türünün sizeof değerini çıkarabiliyor.
- 










































































