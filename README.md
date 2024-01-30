# Mülakat Soruları

Merhabalar, kendime mülakat sırasında sorulacak sorulara ön hazırlık olması ve bilinmesi gerektiğini düşündüğüm şeyler için özet niteliğinde bir doküman hazırlamak istedim. Benim gibi yeni mezun seviyesindeki arkadaşlar için teorik ve yer yer uygulamalı gösterim şeklinde bir içerik hedefliyorum. Yanlış veya eksik şeyler yer alabilir. Detaylı bilgiler için harici linkler ekleyebilirim.

## SORULAR

[.NET nedir?](https://learn.microsoft.com/tr-tr/dotnet/core/introduction)

- .NET yazılım geliştirme için kullanılan bir platformdur. Microsoft tarafından geliştirilmiştir.

Framework nedir?

- Bir sistemin, kavramın veya metnin altında yatan temel yapı olarak tanımlanıyor. Bilgisayar kavramı olarak da yazılım geliştirme için destek veren bir iskelet olarak düşünebiliriz. İçerisinde belirli görevler için araçlar ve kütüphaneler sağlayan yapılardır.
- [2023 itibarıyla dünya çapındaki geliştiriciler arasında en çok kullanılan frameworkler](https://www.statista.com/statistics/1124699/worldwide-developer-survey-most-used-frameworks-web/)
- ![image](https://github.com/fatihaltinci/mulakat-sorulari/assets/105079427/8cdeb563-f1d4-408d-84bf-d49111f1a102)

.NET Framework ve .NET Core arasındaki fark nedir?

- .NET Core'a geçişle birlikte açık kaynaklı ve Windows dışında da çalışabilme (crossplatform) yapıya sahip olmuştur.

ORM nedir?

- ORM (Object Relational Mapping) nesneleri veritabanıyla ilişkilendirmedir. Bu ilişkilendirmeyi yapan farklı dillerde farklı ORM'ler vardır. ORM ile SQL bağlantıları, komutları, parametrelerini kullanmazsınız. ORM bunu sizin için yapar ve veritabanını OOP olarak haritalandırmanıza olanak tanır: C#'ta nesneleri kullanarak veritabanınıza kayıt ekleyebilir, okuyabilir, güncelleyebilir ve silebilirsiniz. Yalnızca DB ile doğru şekilde eşlemeniz gerekir. Entity Framework ADO.NET üzerine kuruludur ve içinde ADO.NET'i kullanır. SQL ifadeleri ORM tarafından oluşturulur. Veritabanı bağımlılığı yoktur.
- C#: Entity Framework,  Dapper -> @ecanyuksel [Entity Framework vs Dapper: Hangisi Daha İyi?](https://medium.com/@ecanyuksel/entity-framework-vs-dapper-hangisi-daha-i̇yi-81cfbe5c2313)
- Java: Hibernate
- Python: Django gibi.
- ![image](https://media.licdn.com/dms/image/D5612AQGZjJpjEP1iEA/article-cover_image-shrink_720_1280/0/1686716645931?e=1712188800&v=beta&t=4gtLY5nidqn8xkUKhbjbm6dDaq891OIdIf86g8FX4-M)

- Normal SQL Sorgusu vs ORM
- ![image](https://github.com/fatihaltinci/mulakat-sorulari/assets/105079427/656ff602-dc74-40e0-90b2-be70a63a5061)
- ![image](https://github.com/fatihaltinci/mulakat-sorulari/assets/105079427/46520c1e-284e-42b7-a2f0-3eb0f3df3316)
- ORM kullanmanın performansa etkisi gibi olumsuz durumları da vardır.
  
[ADO.NET nedir?](https://learn.microsoft.com/tr-tr/dotnet/framework/data/adonet/)

- Microsoft’un veriye erişme teknolojisinin adıdır. ADO.NET (ActiveX Data Objects), DB'ye bağlanmanıza ve SQL bağlantılarını, komutlarını, parametrelerini kullanarak değiştirmenize olanak tanıyan bir katmandır. 
- ![image](https://learn.microsoft.com/tr-tr/visualstudio/data-tools/media/raddata-ado-net-architecture-diagram.png?view=vs-2022)
- ADO.NET için veritabanına 2 bağlantı türü vardır: Connected, Disconnected.
- Connected: Uygulamamız, database ile sürekli bağlantılı haldedir ve db'de anlık işlemlerimiz yapılmaktadır.
- Disconnected: Uygulamamız, veri tabanının kopyasını RAM'e alır ve bundan sonraki tüm işlemlerini RAM'deki veride yapar.
- Bu bağlantılar için yazılmış detaylı ve güzel bir Medium yazısı var şurda: @cemtuganli [ADO.NET Architecture: CONNECTED VS DISCONNECTED](https://medium.com/@cemtuganli/ado-net-architecture-connected-vs-disconnected-791f17279fc5)

EF için ORM Modelleme yaklaşımları nelerdir?

- Database First, Code First, Model First şeklinde 3 yaklaşım var.
- [DB First](https://learn.microsoft.com/tr-tr/ef/ef6/modeling/designer/workflows/database-first): Bu yaklaşım mevcut bir veritabanı üzerinden çalışma yapılması mantığına göre işler.
- [Model First](https://learn.microsoft.com/tr-tr/ef/ef6/modeling/designer/workflows/model-first): Bu yaklaşım yeni bir model oluşturmanıza ve ardından modelden bir veritabanı şeması oluşturmanıza olanak tanır.
- [Code First](https://learn.microsoft.com/tr-tr/ef/ef6/modeling/code-first/workflows/new-database): Bu yaklaşım veritabanı işlemlerinizi Visual Studio tarafında kod yazarak gerçekleştirmenizi sağlayan bir yaklaşımdır. Tam hakimiyet istenilen durumda bu yaklaşım tercih edilmelidir.
- ![image](https://github.com/fatihaltinci/mulakat-sorulari/assets/105079427/4e5aa78b-0f90-47f8-947e-1907465a138e)

[LINQ nedir?](https://learn.microsoft.com/tr-tr/dotnet/csharp/linq/)

- LINQ (Language Integreated Query), sorgu özelliklerini doğrudan C# diliyle tümleştirmeye dayalı bir dizi teknolojinin adıdır. LINQ, veri kaynaklarından veri sorgulamayı kolaylaştırmak için kullanılır.

[SOLID Prensipleri nedir?](http://cagataykiziltan.net/solid-prensipleri/) -> Burda güzel örnekler ile ifade edilmiş. @cagataykiziltan

- Solid Yazılım Prensipleri, yazılım geliştirme sürecinde kullanılması önerilen temel prensiplerdir ve yazılımın kalitesini ve bakımını kolaylaştırmak için tasarlanmıştır. Böylelikle yazılım modülleri ve sınıflar daha anlaşılır, test edilebilir, değiştirilebilir ve bakımı kolay hale gelir.
- (S)ingle Responsibility Principle (SRP: Tek Sorumluluk Prensibi): Bu prensipte savunulan görüş her sınıfın tek bir sorumluluğu taşımaları gerektiğidir.
- (O)pen/Closed Principle (OCP: Açık Kapalı Prensibi): Bu prensipte savunulan sınıflarımızın geliştirmelere açık ancak değişikliklere kapalı olmasıdır.
- (L)iskov ‘s Substitution Principle (LSP: Liskov’un Yerine Geçme Prensibi): Bu prensip kalıtım mantığının doğru bir şekilde anlaşılması ve kullanılması konusunda bizi yönlendirmek için vardır. Kalıtım alınan sınıfın içerisindeki özellikler kendisinden kalıtılan sınıfta da doğru ve eksiksiz bir şekilde kullanılmalıdır.
- (I)nterface Segregation Principle (ISP: Arayüz Ayrıştırma Prensibi): Bu prensip interfacelerin düzgün kullanımını ele alır. Eğer bir interface oluşturulduysa belirli bir amacı olmalı ve o amacı yerine getirebilmelidir. Single Responsibility ilkesinin interfaceler için düzenlenmiş tipidir diyebiliriz.
- (D)ependency Inversion Principle (DIP: Bağımlılık Ters Çevirme Prensibi): Üst seviye (High-Level) sınıflar alt seviye (Low-Level) sınıflara bağlı olmamalıdır, ilişki abstraction veya interface kullanarak sağlanmalıdır. Abstraction detaylara bağlı olmamalıdır. Tam tersi detaylar soyutlamaya bağlı olmalıdır.

Yazılım mimarisi nedir?

- Bir yazılım yapılması için gerekli olan tüm adımları, organizasyonu, iskeleti olarak düşünebiliriz.

Mimari modeller nedir?

- Mimari modeller denenmiş ve test edilmiş iyi tasarım deneyimlerinin kalıplarıdır. Yazılım mimarisi bir sistemi oluşturan parçaların bir bütün halde nasıl tasarlandığını ve aralarındaki etkileşimin nasıl olduğunu açıklar.

[Yaygın mimari modeller nelerdir?](https://www.arakatman.com/yazilim-mimarisi-ve-mimari-modeller/) -> Burda modelleri güzel bir şekilde açıklamış. 

- Model-View-Controller Yazılım Mimarisi (MVC Architecture)
- Katmanlı Yazılım Mimarisi (Layered Architecture)
- İstemci-Sunucu Yazılım Mimarisi (Client-Server Architecture)
- Boru & Filtre Yazılım Mimarisi (Pipe & Filter Architecture)
- Depo Yazılım Mimarisi (Repository Architecture)
- Servis Odaklı Mimari (Service Oriented Architecture)
- Mikroservis Mimarisi (Microservice Architecture)

[MVC Nedir?](https://learn.microsoft.com/tr-tr/aspnet/core/mvc/overview?view=aspnetcore-8.0)

- ![image](https://github.com/fatihaltinci/mulakat-sorulari/assets/105079427/34b35daa-3318-4fa3-a146-c715776df55a)
- Buradaki grafik üstünde akışı anlatacak olursam: Son kullanıcı bir browser arayıcılığıyla etkileşime geçerek bir istekte bulunur ve bu Controller tarafına gider. Controller burda adından da anlaşılacağı gibi kontrolcü görevdedir ve bu isteğe uygun veriyi Model'den talep eder ve veriyi alır. Değişiklikleri yaptıktan sonra (uygun metot çağrıldıktan sonra) bu veriyi View'a gönderir ve gerekli response kullanıcıya View tarafında iletilir.
- Yaşam döngüsü şu şekildedir:
- ![image](https://github.com/fatihaltinci/mulakat-sorulari/assets/105079427/1c598373-6f18-4f18-8da4-f13b86699de5)
- ASP.NET Core MVC için bütün istek işlem şeması şu şekilde:
- ![image](https://github.com/fatihaltinci/mulakat-sorulari/assets/105079427/5c8087f2-17e5-40e9-84ae-e20dae322225)
- MVC'nin gelen istekleri karşılarken uyguladığı farklı yaklaşımlar var. Page Controller ve Front Controller. Bu yaklaşımları anlatan güzel bir yazı var: [MVC, MVP ve MVVM Patternleri](https://denizirgin.com/mvc-mvp-ve-mvvm-patternleri-aa7d1011daff). -> @denizirgin_3389 | Özetle:
- Model: Veritabanıyla bağlantı yapılan yerdir. İsteğe göre gerekli veri işlemleri burda olur.
- View: Kullanıcının isteğine cevap verilen arayüzdür. 
- Controller: İsteğin ilk geldiği ve isteğe uygun işlemleri yapan yani uygun metodu çağırarak işlemleri yapan yer burasıdır.

HTTP Nedir?

HTTP (Hyper Text Transfer Protokol), protokolü ağ üzerinden web sayfalarının görüntülenmesini sağlayan TCP/IP tabanlı bir iletişim protokolüdür. Bağlantı noktası olarak TCP 80 portu kullanılır.



