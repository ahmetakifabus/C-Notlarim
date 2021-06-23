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

1.55
 

 







































































 


































