 #  ARAŞTIRMALAR

## GITHUB VS GİTFLOW, BITBUCKET

​	Geliştirme ilkelerimizden biri, yaptığımız her şeyin tekrarlanabilir ve incelenebilir olması gerektiğidir.Bunu başarmak için kullandığımız araç Git sürüm kontrol sistemidir . Git tekrarlanabilirlik ve gözden geçirilebilirlik sağlar, ancak yine de kullanıcının iş akışının nasıl göründüğünü belirlemesine izin verir.

### Git Flow: Sürüm Kontrolüne Kapsamlı Bir Yaklaşım

​	Bilinen bir iş akışı yöntemine Vincent Driessen tarafından tarif edildiği gibi Git Flow denir . Git Flow, özellik dalları, sürüm dalları, ana hat veya geliştirme dalları ve düzeltmelerin nasıl ilişkili olduğunu açıklar. Bu yaklaşım, kullanıcılar tarafından kütüphaneler ve masaüstü uygulamaları gibi indirilen paket yazılımlar için çok iyi çalışır

Ancak birçok web sitesi için Git Flow aşırıya kaçmıştır. Bazen, ana hat geliştirme ve serbest bırakma dalları arasında, ayrımı değerli kılmak için yeterince büyük bir fark yoktur. Alternatif olarak, düzeltmeler ve özellik dalları için iş akışınız aynı olabilir.

### GitHub Flow: Basitleştirilmiş Bir Alternatif

​	Git Flow'un doğasında bulunan ek karmaşıklığın aşağıdaki gibi belirli durumlarda gerekli olduğunu bulduk:

* Ayrılmış olarak adlandırılmış veya numaralandırılmış sürümleriniz olduğunda
* Bir sonraki sürüm için özellikleri geliştirmeye ve entegre etmeye devam ederken, bir sürüm adayı üzerinde geliştirmeyi dondurmanız gerektiğinde. Bu, örneğin bir sürüm adayının gözden geçirilmesi, hata düzeltmeleri ile kabul edilmesi veya yayınlanmadan önce onaylanması gerektiğinde olabilir. Geliştirme, bir sonraki sürümde aynı anda devam eder
* Yazılımın birden fazla sürümünün bağımsız olarak desteklenmesi ve bakımının yapılması gerektiğinde

#### Sonuç olarak

GitHub Flow'u birçok projemiz için kullanıyoruz. Git Flow'un neredeyse tüm işlevlerini sağlar, ancak daha az ek yük ile daha uyumlu bir iş akışı için geri ölçeklendirilir.

Daha karmaşık web uygulamalarımızdan bazıları daha karmaşık bir iş akışı gerektirir. Bu projeler için Git Flow'u kullanıyoruz

### GitLab

GitLab, GitHub’ın kullanıcılara sağladığı işlevlerin tamamını sunan bir Git servisidir.Açık kaynak(open source) projelerinizi bu servis üzerinde ücretsiz bir şekilde oluşturabilir ve yönetebilirsiniz. GitLab daha çok firmalarda tercih ediliyor çünkü : Ücretsiz sürümünde kendi sunucularınıza kurarak sadece kurum içi kullanıcıların erişebileceği GitLab servisi hizmeti bulunmaktadır.

### BitBucket

Bitbucket kurulduğunda sadece projelere Mercurial için depolama desteği verdi. Atlassian firmasının satın alınması ile birlikte 3 Ekim 2011 tarihinde Git desteği duyrulmuştur.Mercurial, yazılım geliştiricileri için platformdan bağımsız bir şekilde kullanılan bir sürüm(version) denetim aracıdır. 

- Git veya Mercurial gibi VCS(Version Control System) kullanan projeler için bir web depolama servisidir.

* Hem ticari planlarla hem de ücretsiz hesaplarla kullanılabilmektedir ve ücretsiz hesaplara en fazla beş kullanıyıca kadar limitsiz özel depo (repository) alanı sunmaktadır. Bundan dolayı genelde şirketlerde Bitbucket tercih ediliyor. Takım çalışması için ideal olan bu sistemi denemenizi tavsiye ederim.
* Pyhton dilinin bir framework’u olan olan Django ile yazılmıştır.

### Github vs BitBucket

- Fiyatlandırma : Bitbucket Github’a oranla daha ucuzdur. Bitbucket ücretlendirme konusunda GitHub’ın önündedir. 5 kullanıcıya(user) kadar, sınırsız private repository(özel depo) vermektedir. Ülkemizde fiyatlandırma göz önüne alınarak genelde şirketlerde Bitbucket tercih edilmektedir
- Kullanıcı Sayıları : Kullanıcı tercihi açık ara Github öndedir. Tahmini 3 milyondan daha fazla kullanıcıya sahip olan Github’ı, 1 milyonu aşkın kullanıcısı olan Bitbucket takip etmektedir
- Desteklenen Versiyon Kontrol Sistemi(VCS): 
- Bitbucket ise hem Git’i hem de Mercurial’i desteklemektedir.
- Github sadece Git’i desteklemektedir.
- Doğrulama (Authentication): Bitbucket hesabınız olmadan da diğer platformlara ait hesaplarınızla giriş yapabilirsiniz. Github üyeliğiniz varsa ise o hesap ile de Bitbucket’a giriş yapabilirsiniz. GitHub ise Bitbucket’ın aksine bu yöntemi kullanılmamayı tercih ediyor.

#### Sonuc

* Projelerinizin daha fazla bir kitleye ulaşmak istiyorsanız ve open source projeleri katkı sağlamak istiyorsanız Github kullanmalısınız.
* Benim projelerim bana özeldir ve kimseyle paylaşmak istemem, Mercurial kullanmak istiyorum ve hesabıma istediğim platformdan giriş yapmak istiyorum diyorsanız Bitbucket kullanmalısınız.

### Merge pull request

Pull request, projenizde birlikte çalıştığınız kişileri bir branch’de yaptığınız değişikliği ana repository’e ittiğinize dair bilgilendirdiğiniz anlamına gelmekte. Pull request olarak göndermek demek; ben projede değişiklikleri yaptım, sen de bu bu değişiklikleri onayla ve projene merge et, ben de katkı sağlamış olayım demek.

###### Create a merge commit

Hedef branch'de ve kaynak branch'de birbirinden bağımsız değişikliklerin yapılması durumunda "merge commit" adı verilen en son commit ile gerçekleşen değişiklikleri birleştiren otomatik bir commit adımı ekledikten sonra merge işlemini gerçekleştirir.

###### Squash and merge

Git squash komutu aslında farklı bir rebase kullanımı olarak değerlendirmek daha doğru olacaktır. Geçmişte atılan commit’leri yeniden düzenlemek, isimlendirmek veya birleştirmek için kullanıyoruz. merge son işlemde ekstra commit ekler.

###### Rebase and merge altında ne fark var

Merge komutu ile A dalındaki değişiklikler B dalı ile birleştirildiğinde B dalının commit tarihçesinde merge işleminden kaynaklanan ve merge commit adı verilen otomatik oluşturulmuş bir commit yer alır. Bu commit A ve B dallarının tarihçelerini birbiri ile ilişkilendirir. Rebase komutu kullandığımızda ise ile A dalındaki her bir commit B dalına sanki commit işlemi B dalında yapılmış gibi yeniden yazılır. Bu sayede B dalının commit tarihçesi sanki tüm değişiklikler bu dalda olmuş gibi düz ve kesintisiz görünür.Yani son işlemde ekstra commit eklenmez.
Rebase komutu yerel ve kısa süreliğine (örneğin bir hata giderme veya deneysel bir çalışma için oluşturulan) geçerli dallar için kullanılmalı.



## ASP.NET BoilerPlate

ASP.NET Boilerplate, “her şirket tek tek uğraşmasın, tüm .NET developer’lar için ortak bir framework geliştirelim” hedefiyle ortaya çıkmış açık kaynak kodlu, iyi dokümante edilmiş bir projedir. Sadece framework değil, modern uygulamalar için DDD(Domain Driven Design) tekniklerini baz alan sağlam bir mimari ve model sunar.
ASP.NET Boilerplate’in (ABP) sağladıklarına bakalım :

- Dependency Injection: Bu (base class’dan dolayı) bir application service olduğu için Transient olarak Dependency Injection sistemine otomatik olarak kaydedilmiştir. Kendisi için gereken tüm servisleri (bu örnekte sadece bir Repository) direkt olarak inject edebilir (constructor ya da property injection yapılabilir). ABP conventional, kolay kullanımlı ve hazır bir DI altyapısı sağlar.
* Repository: Her Entity için otomatik olarak bir repository oluşturulur. IRepository<Task> şeklinde Task repository’sini kullanıyoruz burada. IRepository’nin birçok hazır metodu var. FirstOrDefault bunlardan birisi.
* Authorization: Eğer bu servisi çağıran kullanıcının “task güncelleme” yetkisi yoksa daha metod çağrısı başlamadan uygun bir authorization exception fırlatır. Attribute kullanarak authorization kontrolünü basitleştirmiş oluyoruz.
* Validation: UpdateTaskInput DTO’su (Data Transfer Object) içerisinde Task Entity’siyle isim ve tip olarak birebir eşleşen property’ler var. Normalde ilk iş bunların validate edilmesi gerekiyor. ABP data annotation’lar ve custom validation teknikleri kullanarak gelen input’un property’lerini otomatik olarak validate eder, eğer valid değilse client’ın anlayacağı formatta bir Exception fırlatır (AJAX çağrısı için uygun bir JSON döner örneğin). Ayrıca nesnenin kendisinin null olmasına da izin vermez, böylece input == null mı kontrolüne gerek kalmaz.
* Audit Logging: Eğer audit logging açıksa bu metod çağrısını yapan kullanıcı, çağrının yapıldığı zaman, IP… gibi bilgilerle beraber çağrılan metod ve parametrelerini kaydeder. Ayrıca süre ölçümü de yapar, böylece yavaş metodlarımızı tespit edip kontrol edebiliriz.
* Unit Of Work: Her application service metodu bir unit of work kabul edilir. ABP, metoda girerken veritabanı bağlantısını otomatik olarak açıp bir transaction başlatır. Eğer metod hiçbir Exception fırlatmadan başarıyla tamamlandıysa transaction otomatik olarak commit edilerek bağlantı kapatılır. Böylece metod içerisinde farklı repository’leri dahi kullansak tüm işlemler atomic olmuş olur. Ayrıca Entity’lerde yapılan tüm değişiklikler eğer hata olmazsa metod bitiminde otomatik olarak kaydedilir. Bu nedenle repository.Update(task) gibi bir kod çağrısına dahi gerek kalmamış oluyor.Burada birçok ayrıntı ve konfigurasyon var ancak varsayılan davranış bu şekildedir.
* Exception Handling: Bir web uygulamasında, bu metod bir Exception fırlatırsa bu Exception otomatik olarak handle edilir, client’ın request türüne göre (AJAX ya da normal request) uygun bir dönüş değeri gönderilir client’a. Client tarafında da bu otomatik olarak handle edilerek kullanıcıya uygun hata mesajı gösterilir. UserFriendlyException özel bir exception türü olup direkt olarak mesaj kullanıcıya gösterilir. Diğer Exception’lar sadece loglanır ve kullanıcıya genel bir hata mesajı gösterilir.
* Logging: UpdateTask metodunun ilk satırında direkt olarak hazır Logger nesnesini kullanarak log yazabiliyoruz. Varsayılan loglama kütüphanesi olarak Log4Net kullanılır.
* Localization: Dikkat edilirse Exception fırlatılırken L adın bir metod kullanıldı. Bu da base class’dan gelen bir metod olup verilen key’e ve o anki kullanıcının diline göre ilgili lokalizasyon metnini verir.
* Auto Mapping: Son satırda ABP’nin MapTo extension metodunu görüyoruz. ABP, Automapper kullanarak bir nesneyi diğerine map edebilir. Böylece gelen input’daki (daha önce validate edilmiş) verilerle Entity’deki property’leri güvenle ezebiliyoruz.
* Dynamic Web API Layer: Bu application service aslında basit bir sınıftır. Browser’dan AJAX’la bunu çağırabilmek için genellikle wrapper şeklinde bir Web API Controller geliştirilir. ABP bu controller’ı runtime’da otomatik yaratır, böylece client’dan doğrudan application service’ler kullanılabilir olur.
* Javascript AJAX Proxy: Dinamik oluşturulan Web API’yi çağırmak için de ABP tarafından yine dinamik olarak bir javascript proxy’si oluşturulur. Böylece javascript’den metod çağırır gibi application service’leri kullanabiliriz.
Görüldüğü gibi çok basit gözüken bu işlem için dahi bütün bunları manuel yapmaya kalsak oldukça zamanımızı alacakken ABP framework tüm bunları otomatik yaparak bizi benzer ve rutin işlemleri tekrar tekrar yapma zahmetinden kurtarır.

Bütün bunların dışında aşağıdaki konularda da bize yardımcı olur:

* Modularity: ABP, modüler uygulama geliştirmek için bize güçlü bir altyapı sunar. Kendi paketleri de modül olarak geliştirilmiştir.
* Multi-Tenancy: ABP multi-tenancy destekler. Tek bir veritabanında aynı uygulamayı her müşteri kendi perspektifinden kullanır, birbirinin datasını görmez, kendi rol, kullanıcı ve yetkileri olur.
* Data Filters: Soft-delete gibi pattern’leri kolaylaştırmak için otomatik data filtreleme kullanır. En basit haliyle, eğer gerekiyorsa, Where şartına IsDeleted=False ifadesini otomatik ekler.
* Setting Management: Her uygulamada bazı ayarların kaydedilmesi ve okunması gerekir.
* Domain Events & EventBus: Global domain event’lar tanımlamak, tetiklemek ve yakalamak için altyapı sağlar.
* Unit & Integration Tests: ABP içinde unit ve integration test’leri kolaylaştırmak için gereken temel sınıflar mevcuttur.

## Razor Page

ASP.NET Core 2.0 ile beraber hayatımıza giren Razor Pages, ASP.NET Core MVC alt yapısında, sayfa bazlı web uygulamaları geliştirebileceğimiz bir programlama modeli. Tamamen MVC alt yapısı üzerine geliştirilmiş bir kabuk olarak düşünebilirsiniz. MVC template’lerindeki klasör sayısını azaltmak, sayfa bazlı uygulamaları daha kolay geliştirmek için tasarlanmış yeni bir model. Altını çizerek belirtmek isterim ki, MVC’ye alternatif ya da onun yerini alacak bir model değil.

PHP ya da eski ASP ile tecrübesi olanların ya da scripting dilleri ile uygulama geliştirenlerin daha çok hoşuna gideceğini düşünüyorum. Büyük bir ihtimal, web uygulaması geliştirmeyi daha basite indirgemek ve script tabanlı dilleri tercih edenleri de mutlu etmek için böyle bir modele yönelmiş olabilir Microsoft. Ama asıl önemlisi web uygulaması yapmayı yeni öğrenmek isteyen kişileri çekmek sanırım Razor Pages’ın en büyük amacı. Çünkü gerçekten kolay.

MVC alt yapısını kullanarak yapıldığı için uzun zamandır MVC modeli ile geliştirme yapanlar için çok fazla bir şey ifade etmeyecektir. Hatta bir çok MVC tercih eden kişi, ne gerek vardı falan da diyor. Kendilerince haklılar. Burda tekrar belirtmek isterim ki, Razor Pages, MVC’nin bazı özelliklerini daha basit ve kolay hale getiriyor. Uzaya roket gönderebileceğiniz bir teknoloji değil.

Razor Pages, adından da anlaşılacağı üzere “Razor” ve “Sayfa” konsepti üzerine geliştirilmiş bir model. MVC’deki View kavramı, biraz daha geleneksel tabirle “sayfa” olarak karşımıza çıkıyor. Ama tabii ki Layouts, TagHelpers gibi yaklaşımlar Razor Pages’de de var.

Razor Pages’de sayfalar birer PageModel ile tanımlanıyor. PageModel’leri MVC’deki Controller ve Model olarak düşünebilirsiniz. Web sayfanıza gelen talepler(request), Controller’daki gibi PageModel tarafından karşılanıyor. Controller’a ek olarak View tarafına taşınan model de bu PageModel üzerinde olabilmektedir.

## JSON Serialize / Deserialize

Serialization: Bir nesnenin saklanacak / transfer edilecek forma dönüştürülme işlemidir. Serileşmenin tersi olarak Deserialization ifadesi kullanılır ve bu da Stream'in (Akış) nesne modeline dönüştürülme işlemidir.

 .Net Framework içerisinde bulunan System.Runtime.Serialization namespace'i bu işlemler için kullanılmaktadır. İçerisinde bulunan sınıflar ve araçlar sayesinde, kendi nesnelerimizi istenilen/ihtiyaç duyulan formatta saklama imkanı sunar.

Serialization bize iki temel metot sunar. 

- XML "eXtensiple Markup Language" ve SOAP "Simple Object Access Protokol" Serileştirme işlemleri : Tür esnekliği ile ön plana çıkan bu yapı, çok sık tercih edilmektedir. XML Serileştirme işleminde sadece ortak tipler ve metotlar serileştirilebilir. Bu yapıda verilerimnizi kullanacak olan uygulamayı kısıtlamadan saklayabiliriz. XML ve SOAP açık bir standart yapı olduğundan, aynı zaman da her türlü uygulama ile rahatlıkla okunabildiğinden veri paylaşımı oldukça hızlıdır.
- Binary (ikili) Serialization : Tür bağımlılığı açısından önemlidir. İkili serileştirme işlemi, daha çok bir birinden bağımsız iki uygulama arasında, nesne modellerini taşımak için kullanılır. İkili serileştirme işlemi; bir nesnenin durumunun saklama ortamına uygun hale getirilip yazılması süreci olarak tanımlanabilir. İşlem süresince, nesnenin “public” ve “private” öğeleri, sınıfın adı, sınıfı barındıran Assembly’ nin adı saklama ortamına yazılmak üzere “byte” lar akışına çevirilir.
  Nesne, Deserialize edildiğinde ise nesnenin tam bir kopyası oluşturulur ve kullanıma sunulur. Binary serialization ile .Net Remoting kullanarak farklı domain içinde bulunan bir bilgisayardaki uygulamalara bile taşınabilir. Bazen Binary Serialization ile bir nesneyi serialize etmek, sürücüde gereğinden çok fazla yer işgal etmeye neden olabilir, çünkü nesnemiz kendi ve içinde bulunan her yapı ve nesne için sürücüde binary header ile fazladan yer işgal eder. Hatta eğer nesnelerden oluşmuş bir array veya collection(IList, ObservableCollection vb…) varsa bunun içinde bulunan her nesne içinde (foreach) bir binary header (o class’ın yapısı) dosyamıza eklenerek dosyanın boyutunu şişirebilir.

## MVC vs MVVM Vs MVU

#### MVC (Model-View-Controller)

ASP.NET MVC, MVC pattern’ini ASP.NET’e eklemek için Microsoft’un geliştirdiği framework’tür.

Model : Kullanıcaya göstermek ve manipule etmesini sağlamak istediğimiz verileri içereren nesneler.

View : Kullanıcıya Model’i gösterdiğimiz ve Model üzerinde çeşitli manipulasyonlara izin verdiğimiz yer, Web olsun, windows olsun fark etmez, amaç kullanıcıya birşeyler göstermek ve inputlar almak.

Controller: Kullanıcıların View üzerinden gerçekleştirdiği işlemlerle alınan veriyi Model’e taşır, Model’den aldığı veriyi View üzerinden kullanıcıya gösterir.

#### MVVM (Model-View-View Model)

MVVM bir projenin “sorumlulukların ayrıştırılması” esasına göre geliştirilmesi temeline dayanan bir tasarım kalıbı sunmaktadır. MVVM bir yazılımı Model, View ve ViewModel adında üç farklı yapıda geliştirmemizi tavsiye etmektedir.Model tarafında bir değişiklik yapılmak istendiğinde UI tarafında hiçbir değişiklik yapılmasına gerek kalmadan geliştirmeler rahatlıkla yapılabilir

Model: Veritabanından, web servislerinden ya da herhangi bir veri kaynağından gelen verilerimizi temsil etmek için kullanılan entity sınıflarından oluşmaktadır. Ayrıca veri tutarlığını ve doğruluğunu kontrol eden iş kuralları da burada yer almaktadır.

View: Bu kısım verilerimizi son kullanıcılara aktardığımız görsel arayüzdür. Son kullanıcı ile uygulama arasında bir köprü görevi görür.

ViewModel: ViewModel ise görsel arayüz ile model arasında köprü görevi görmektedir, yani Model’i View’a bağlayan yapıdır.

#### MVP (Model View Presenter)

Model: Presenter’ın ihtiyaç duyduğu bilgileri sağlar. İş mantığı bu kısımda ele alınır. 

View: Verilerin görüntülendiği ve işlem yapmak için kullanıcı ile etkileşime geçilen kısımdır.

Presenter: Model ile View arasındaki bağlantıyı sağlayan kısımdır. Verileri modelden alır ve UI mantığını uygular. 

#### MVW(Model-View-Whatever)

Burada W(Whatever) her hangi bir şey(C-Controller, VM-ViewModel ya da P-Presenter) olabilir.

#### Model-View-Update (MVU) nedir?

Son olarak, modeldeki tüm değişiklikler , View tarafından gönderilen mesajları alan ve değişiklikleri buna göre uygulayan saf bir Update işlevi tarafından uygulanır.
###### Farklılıkları:
MVP (Model, View, Presenter)’nin en büyük farklı controller’ı parçalıyor olması. Böylece view/activity doğal bağına devam ederken activity, controller sorumluluklarından arınmış olur. Model MVC’yle aynı. View’de fark olarak bu sefer Activity ve fragment de view’dedir. Ancak herhangi bir logic implement edilmez. Burada hem view hem de presenter birer interface’i implement ediyor. Activity hem view’i hem de presenter’ı create eder. Presenter kullanıcıdan gelen inputu view’i aracılığıyla alır. Presenter, MVC’deki controller’dır ancak bu sefer view’e bir bağımlılığı yoktur. Avantajı MVC’de view’e bağımlılığından dolayı Controller’a unit test yazamıyorduk. Burada View mock’lanarak yazılabilir. MVP küçük projelerde avantajlı olmakla beraber büyük projelerde çok fazla class olmasına sebep olabilir, zamanla presenter classlar şişebilir. MVVM(Model, View, View-Model), View’in değişikliklere yanıt verebileceği event-based bir mimari kurmak istersek de karşımıza MVVM çıkacak. Model, MVC’yle aynı. View, viewmodelden sağlanan observable variable’ları bağlar. ViewModel, Model’i wrapleyip View tarafından ihtiyaç duyulan observable datanın sağlanmasından sorumlu. Yani aslında yine business logic’den model sorumlu. Data değiştiğinde ViewModel bundan haberdar oldu ve View’e haber verdi. View’de UI’ı update etti diyebiliriz basitçe.