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


Namespace
---
Global namespace -> Fonksiyonun dışı genel kod yeri 
Local namespace  -> Fonksiyon birimlerinin içindeki alan 

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
void func()
{
int x=10;
printf(x);
x+=10;
}

int main
{
func();
func();
func();
}

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

Unspecified Behaviour
---
Hata değildir. Kodu başka şekilde üretilebilir.

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

void func(void)
{
int x=10;
static int y = 10;
printf(x,y);
x++;
y++;
}

int main()
{
func();
func();
func();
}


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
Expression Statement (İfade Deyimi)
Compound Statement (Bileşik Deyim)
Null Statement (Boş Deytim)
Control Statement (Kontrol Deyimi)

z = 10; Expression Statement
++a; Expression Statement

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

int main()
{
	int x= 10;
	printf("x = %d\n", x);
	foo(x);
	printf("x = %d\n",x);
}

Burada x değeri ekrana 10 olarak yazdırılır çünkü fonksiyon çağrıları call by value olduğu için x değerini değiştiremez.

Bir fonksiyon başka vbir fonksiyonun değişkjenine ancak adresi yolu ile erişebilir. Pointer denilen şeyin amacı da budur.

Ders 8 (13.08.2021) 09.35
---
Standart C kütüphanesi nedir?
---
Dil tarafından derleyicilerin size sunulması garantşisi verilen hazırr bazı kodlar.

Başlık dosylarında standart C fonksiyonlarının bildirimleri var, kodları değil (stdio.h)

Bildirim -> bir ismin  ne anlama geldiğini anlatan C cğmleleri.

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
Armstrong sayıları


for (int i = 100, i < 1000; ++i)
{
int d1 = i / 100;
int d2 = i / 10 % 10;
int d3 = i % 10;
	if(i == d1 * d1 * d1 + d2 * d2 * d2 +  d3 * d3 * d3)
	{
	printf("%d\n" , i);
	}
}

Not:
---

int func(void)
{
printf("func cagildi\n");
return 0;
}

int main()
{
if(func)
	{
	printf("evet dogru\n");
	}
}

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
int c1, c2, c3;
int x;
printf("bir giris yapin");

c1 = getchar();
c2 = getchar();
c3 = getchar();

printf("%d %d %d\n", c1, c2, c3);
scanf("x = %d\n", &x);

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



Expression	c	c++
---
++x		R	L
--x		R	L
x,y		R	L
a > 10 ? x : y	R	L
x++		R	R
x--		R	R



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
#ifndef NUTILITY_H  // #pragma once (standart değill)
#define NUTILITY_H

struct Data {
	int a,b,c;
};
#endif



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

int main()
{
int x = -1;
unsigned int y = 1;

if(x > y)
	printf("dogru"\n);
else 
	printf("yanlis\n");
}

çıktısı: dogru


Operandlardan biri:

unsigned short
signed short
unsigned char
signed char
char
_Bool

Bu türlerden biriyse (int altı türler) doğrudan int türüne yükseltiliyor.

- Büyüklük sıralaması:
unsigned long long
signed long long
unsigned long
signed long
unsigned int
signed int


long double > double > float > long long > long > int

a + b

operandların ranklari farklı ise işlem daha yüksek rank ile yapıalcak.

aynı türün rank aynı türleri farklı ise (unsigned ve signed) tür dönüşümü işaretsiz yöne yapılacak

ival + uval işlemi unsigned türde yapılacak.


unsigned int x;  //4 byte
signed long y;	 //4 byte

x + y; 
Burada eğer işaretsiz türün tutabileceği tüm değerler işaretli türde tutulabiliyorsa işlem işaretli türde yapılacak.


char c1 = 10;
char c2 = 20;

c1 + c2 
cevap int türünden yazılır.


- Rankler aynı işaretler de aynı ise işlem yüksek rank'te yapılıyor.
- Rankler farklı büyük rank işaretsiz ise işlem yüksek rank'te yapılıyor.
- Rankler farklı büyük rank işaretli ise işlem ya yüksek rank'te ya da yüksek rankın işaretsiz olanında yapılıyor.

Tam sayi türlerinde taşma tanımsız davranıştır.

- İşaretsiz türlerde taşma yoktur. Tüm işlemler modüler aritmetiğe göre yapılır.


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
int rand(void); 
0 - RAND_MAX arası rastgele sayı

void srand();

Zar örnek
---
for(;;){
printf("%d%d\n", rand() % 6 + 1, rand() % 6 + 1);
_getch();
}


Program baştan başladığında zarlar hep aynı gelecek. 

Farklı bir zincir oluşturmak için:
Gerçek rastgele sayı üreticisi kullan. get_true_random_number(void);

Böyle bir fonksiyon yoksa:

Calender time:
<time.h> başlık dosyasındaki 
time_t time(time_t *ptr); fonksiyonu

Null pointer ile çağırırsan dönüş değeri epoktan(01.01.1970 00:00) (unix işletim sisteminin doğum tarihi )geçen saniye sayısını döndürecek.

for(;;){
printf("%ld\r", time(NULL));


int main()
{
srand((unsigned)time(NULL));
for (int i = 0; i < 10; ++i){
	printf("%d", rand());
}
}
Her seferinde farklı değer verecek çünkü doğum yerleri farklı.

Ders 24 (21.09.2021) 11.02
---
Dizinin max elemanını bul..

int a[SIZE];

int max = a[0];

for (int i = 1; i < SIZE; ++i){
	if (a[i] > max)
		max = a[i];
}

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

#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>


int random_char(void)
{
	int c;

	while (!isalnum(c = rand() % 128))
		;
	return c;
}

void print_random_password(void)
{
	int len = rand() % 5 + 6;
	for (int i = 0; i < len; ++i)
		putchar(random_char());
}

int main()
{
	randomize();
	print_random_password();
}

- Kod bu haldeyken hep aynı rastgele parolayı üretiyor.
- 


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

 char c = 1;
 
 sizeof c ==== 1
 sizeof +c === 4 (integer'a yükseltiliyor)
 
 int main()
{
	int x = 10;
	printf("%zu\n", sizeof(++x));
	printf("%d\n", x);
}
// Çıktılar 4 ve 10

- Bazı durumlarda bir ifadedeki işlemler için derleyici işlem kodu üretmiyor.
- Yani sizeof(++x). sizeof oepratörünün operandı olan bir ifade için derleyici işlem kodu üretmiyor. Sadece tür bilgisi olarak bakıyor.
- sizeof içine bir fonksiyon yazdığın zaman da fonksiyon çağrılmayacak.

Örnek:
---
#include <stdio.h>

int main()
{
	char buf[200];
	int a[50];
	double da[20];

	printf("sizeof(buf)= %zu\n", sizeof(buf));	//200
	printf("sizeof(a)= %zu\n", sizeof(a));		//200
	printf("sizeof(da)= %zu\n", sizeof(da));	//160
	
	sizeof(a) / sizeof(a[0]); // Dizide kaç eleman olduğunu hesaplar.
	//Dizinin toplam kaç byte yer kapladığını buldu ve dizinin 1 elamanının sizeof
	//unu buldu ve böldü
}

Örnek
---
#include <stdio.h>

int main()
{
	int a[] = { 2, 5, 7,1,34,6,9,44,678,123,45 };

	for (int i = 0; i < sizeof(a) / sizeof(a[0]); ++i)
		printf("%d", a[i]);
}	// derleyici compile time da 11 değerini elde edecek.
	// dizi değişse bile döngü sayısı aynı

 Örnek:
 ---
 #include <stdio.h>

int main()
{
	int a[5] = { 0, 1,2,3,4 };

	for (int i = -2; i < (sizeof(a) / sizeof(a[0])); ++i)
		printf("%d", a[i + 2]);
	
}
//	sizeof(a) unsigned int değer
//	< operandının sol operandı işaretli int sağ tarafı işaretsiz int
//	-2 işaretsiz int türüne dönüştürüldüğünde int değerinde en byükten 
//	bir küçük sayıya dönüşüyor ve koşul yanlış oluyor döngüden çıkıyor.


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




















































