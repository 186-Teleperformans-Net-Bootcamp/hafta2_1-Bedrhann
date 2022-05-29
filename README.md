**Extension**
Ödevimizde Extension geliştirmemiz bunu datetime türüne uygulamamız isteniyordu;
Uygulayacağım Extension'ı  programımda Extensions klasörü altında tanımladım ve bir "datetime" nesnesi almasını sağladım ve bu nesne ile gelen tarihi, "now" hazır metodu ile o anın tarihini oluşturduğum nesnem ile aralındaki farkı aldım ve bu farkı "span"  ile toplam saniye türünü dönüştürdüm.Ve gerekli kontroller ile bu saniyenin kaç yıl kaç ay gibi parametreleri içerdiğini hesaplayıp sonra istenin string şeklinde geri dönüşünü sağladım ve controller'da gerekli endpointin içinde "query"den extensiona gönderilecek nesneyi alıp extensiona aktaran ve geri dönen string değerini string olarak response ile geri dönen bir ödev yapmış oldum.


**Attribute**

Bizden istenen veritabanı tablomu oluştacak class'ımı Model klasörü altında tanımladım ve class'ımın üzerinde tanımladığım attribute ile oluşacak tablonun adını alıyorum ve property'lerin üzerinde tanımlanan attribute ile de o verinin ismini,türünü,zorunluluğunu aldum ve bunları string ile attribute'a gönderdim.Validation klasörüm aldında tanımladığım validation class'ına gerekli Customer nesnesini gönderip içeride tablo adının ingilizce karakter olma kontrolünü sağlayıp gerekli string çıktıyı vermesini sağladım.
Controller'da CreateTable metodu ile queryden id'sini aldığım nesnenin yine aynı metod içinde örnek bir nesnesini yarattım ve gerekli çıktıyı string olarak geri döndürdüm.

**SOLİD**
Interface klasörü altında tanımladığım interface'leri WorkAnimal altında tanımladığım Cat ve Parrot nesnelerime aktardım.Farklı özellikleri farklı interface'ler ile alarak Interface Segration özelliğini kullandım ve program içinde bu class'lara bağımlılığı kaldırmak için startup.cs içinde services olarak en üst arayüzle kullanmak istediğim nesneyi oluşturdum ve başka bir nesne gerektiğinde sadece startuptaki yaratılan nesneyi değiştirmem gerekli olucak ve bu şekilde de dependency injection'u kullanmış oldum.

# 2. Hafta Ödev 1

> Extension Geliştirin

- Datetime tipine bir extension geliştirin.
- Verilen Datetime ın o anki tarihe ne kadar yakın olduğunu text olarak dönsün.
- Örn: 
 `var date = Datetime.Now();
  Console.Writeline(date.Ago());
  --- 2 gün 3 saat 4 dakika önce
 `
 
> Attribute ve Reflection Kullanımı

- Amaç veritabanı tablosu olacak şekilde bir mapping işlemi yapılacak. Db tablosuna karşılık bir class gelecek ve oluşturulan bu class dan attributeler yardımı ile veritabanı tablosunu oluşturucak script çıkarılacaktır. Burada sql verinin doğruluğu önemli değildir.`tablo adı:Öğrenci --- kolonları id tipi int zorunlu` gibi bir çıktı yeterli olacaktır.
- iki tane attribute geliştirin. Biri Table diğeri Column
- Table, class üzerine tanımlanabilsin ve parametre olarak ad (string değer) alabilsin. Türkçe, özel karakterler içermesin
- Column, property ler üzerine tanımlansın, parametre olarak ad, tip ve zorunluluk değeri alsın.
- Oluşturulan class dan scripti çıkarak kodu yazın

> SOLID kavramı

- Dependency inversion prensibini, interface segregation ile birlikte kullanın ve .net in kendi dependency injection frameworkü ile basit bir örnek yapın.
- Kodun çalışabilirliği değil daha çok kullanımı, tasarımı önemlidir.

 
 
 
