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
Fakat declarative diller sonuç odaklıdır(Ne istediğimizi söylüyoruz)

Assembly dili, makine dilinin komutlara dönüştürüldüğü bir hali gibi düşünebiliriz.
Teknik tanıma göre C düşük seviyeli bir dil değil. Düşük seviye derken kastedilen aslında assembly ve aşağısı. Bu yüzden C'ye düşük seviyeli diyemeyiz. C yüksek seviyeli bir dil fakat daha alt kesiminde. Makinaya yeterince yakın, insana da uzak değil.

1. Kuşak diller -> Makina diller
2. Kuşak diller -> Assembly diller

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

Taşınabilir bir dil!
---
Java her yerde çalışıyor demek dilin portable olduğunu göstermez. Bu taşınabilirlik kaynak kodu kapsamıyor.

3.. Kuşak diller
---
3. kuşak diller 3 tane dilden türetilmişler.
    Fortran, Cobol, Algol.
    
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
Keywords   -> Anahtar sözcükler
Identifier -> İsimler
Sabitler   -> Constants
Operators  -> Operatörler
String Literals  -> String sabitleri
Delimeter  -> Ayıraçlar

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

x L value
x+5 R Value
12  R Value

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



_Bool  1 byte

char 1 byte
signed char 1 byte 
unsigned char 1 byte

signed short int 2 byte
unsignedshort int 2 byte

signed long int 4-8 byte
unsigned long int 4-8 byte

signed long long int 8 byte

unsigned long long int 8 byte

signed int 2-4-8 byte
unsigned int 2-4-8 byte

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

1.53
























































 




























