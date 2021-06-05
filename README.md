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

Imperative dillerde sadece sonucu değil, sonuca ulaşmak için neler yapılacağı da anlatılıyor. C - C++ arasındaki en önemli fark bu. C++ brden fazla paradigmaya destek veren bir programlama dili.
Fakat declarative diller sonuç odaklıdır(Ne istediğimizi söylüyoruz)

Assembly dili, makine dilinin komutlara dönüştürüldüğü bir hali gibi düşünebiliriz.
Teknik tanıma göre C düşük seviyeli bir dil değil. Düşük seviye derken kastedilen aslında assembly ve aşağısı. Bu yüzden C'ye düşük seviyeli diyemeyiz. C yüksek seviyeli bir dil fakat daha alt kesiminde. Makinaya yeterince yakın, insana da uzak değil.

1. Kuşak diller -> Makina diller
2. Kuşak diller -> Assembly diller

Benim söylediğim 1 kod 1'e dönüşüyorsa makina dili, 1 dediğimde 2-3'e dönüşüyorsa assembly dili, Daha fazla dönüşüyorsa yüksek seviyeli diller diyebiliriz.
C, sistem programlama alanının ana dilidir, Mikroişlemci programlama dilidir.

C mülkiyet dili değil!
---
Sahibi yok. C derleyicisi yazmak için kimseden izin almak zorunda değilsiniz. Para ödemek zorunda değilsiniz.
Örnek, java ve C# mülkiyeti var. Python'ın yok.

Genaral Purpose!
---
Genel amaçlı
Donanımın doğrudan kontrol edildiği uygulamalar (Sistem programlama)
C'nin dolaylı olarak kullanıldığı diller -> MATLAB ortamında yazılan kod C koduna dönüştürülüyor.

Static tür ve Dimanik Tür
---
Static tür kavramına sahip dillerde çevirici program koda bakarak verinin ne olduğunu anlıyor. (Çeviri sürecinde program biliyor)
Dinamik tür kavramında verinin ne olduğu programın çalışma zamanında belli oluyor. (Çevirici koda bakara verinin ne olduğunu bilmiyor)

Static tür kavramına sahip dilelrin avantajı, kodlama hatalarının daha erken süreçte bulunabilmesidir.

x = 12;
x = 21.84;
x = "ali"

-> Eğer böyle ise bu dinamik tür kavramına sahip bir dildir.
C, sadece static tür kavrmaını destekelrken, c++, C#, java gibi diller dinamik tür kavramını da bellir bir ölçüde destekliyorlar. (Esas olan static tür fakat dinamik türe yönelik araçlar var)

C'de 
x=10;
x=15;
diyebiliriz. Bu onu dinamik yapmaz mı?(X'i float tanımlarsak)
-> X'i float tanımlamak demek zaten onun static tür kavramına sahip bir veri olduğunu gösteriyor zaten.

C, Yapay Bir Dil! (Artificial)
---
İnsanın konuştuğu dile benzerlik sağlamak yerine, uzaklaşmış ve tamamen uydurma kurallar ile bir anlatım benimsenmiştir.
Java, c# gibi diller programcının verimli olması açısından geliştirilmiştir, fakat c ve c++ dilelrinde odak noktası programın verimli olmasıdır. (İşlemcinin verimli kullanılması, yapılacak iş daha az işlem ile yapılsın.)

C'den sonra geliştirilen programlama dillerinin çok önemli bir kısmı C'nin sentaksından, genel yapısından, ifade gücünün yüksekliğinden faydalanmıştır.

Taşınabilir bir dil!
---
Java her yerde çalışıyor demek diin portable olduğunu göstermez. Bu taşınabilirlik kaynak kodu kapsamıyor.

3.. Kuşak diller
---
3. kuşak diller 3 tane dilden türetilmişler.
    Fortran, Cobol, Algol.
    
Günümüzdeki dillerin soy ağacı buraya gidiyor.
 
Fortran -> 1954 yılında geliştirilmiş bir dil.
Formula + translation = Fortran

C'nin doğum tarihi -> 1970





































