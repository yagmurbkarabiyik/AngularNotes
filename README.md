# AngularNotes
Gençay Yıldız tarafından Youtube üzerinden yayınlanan A'dan Z'ye Angular 16 Eğitimi derslerinde öğrenmiş olduğum bilgiler ve almış olduğum notlar.
[Kursa buradan ulaşabilirsiniz.](https://www.youtube.com/playlist?list=PLQVXoXFVVtp1DcC4z0euk71_ICphrOEFV)

# Angular Nedir❓
Google tarafından JavaScript temelli geliştirilen, SPA(Single Page Application) oluşturmak için tasarlanmış olan open source web uygulama mimarisidir. 

Single Page Application ➡ Özetle, bir web uygulamasının tüm işlevselliğini tek bir sayfa üzerinde içeren tasarım şeklidir. Sayfa geçişleri esnasında hızlı bir kullanıcı deneyimi eşliğinde yüksek performans sağlar. 

## Angular CLI(Command Line Interface)
Angular CLI sayesinde manuel olarak yapabileceğimiz bazı adımları komut satırı üzerinden de halledebiliyoruz. Angular CLI kullanabilmek için öncellikle "npm install -g @angular/cli" komutunu çalıştırdıktan sonra artık Angular CLI ile projeler geliştirebiliriz. 

## Angular CLI Komutları
  -ng new projeAdı ➡ Sade bir şablonda yeni bir Angular uygulaması oluşturabilirsiniz.
  -ng version ➡  Angular projesinin yüklü olduğu sürümü ve bağımlılıklarını görüntülemek için kullanılır.
  -ng generate ➡ Angular projesinin yapı taşlarının (service, module, class ya da component gibi) üretilmesini sağlayan komuttur. Generate yerine sadece "g" harfini yazmanız da yeterli olacaktır. 
  -ng serve ➡ Angular uygulamamızı canlı olarak görüntüleyebilmemizi sağlar. Yani uygulamamızı ayağa kaldırır. 
  -ng build ➡  Bu komut ile uygulamanızı test aşamasından üretim aşamasına geçirerek, uygulamanızın hızlı ve optimize edilmiş bir şekilde çalışmasını sağlayabilirsiniz.

## Angular Bazı Dosya ve Sayfa Yapılanmaları
  -node_modules ➡ Projede kullanılan paketler bu dizinde bulunur. 
  -src ➡ Uygulamanın en önemli dosyasıdır. Uygulamanın kaynak kodlarını ve projenin geliştirme sürecinde kullanılan dosyaları içeren ana klasördür. Bu klasör, Angular uygulamanızın temelini oluşturur.
  -assets ➡ Uygulamayla ilgili resim, icon, video gibi dosyalar bu klasörde tutulur. 
  -index.html ➡ Temel geliştirme sayfasıdır.
  -main.ts ➡ Uygulama sürecinde hangi module dosyasının ana module olacağı burada belirtilmeli. Uygulamanın başlangıç noktasını belirleyen ve uygulamanın çalıştırılmasını başlatan dosyadır.
  -angular.json ➡ Uygulamayla ilgili script, style, budget gibi temel konfigürasyonlar burada yapılır.
  -package-lock-json ➡ Kullanılan paketlerin sürümleri hakkında bilgi içeren dosyadır.
  -tsconfig-json ➡ TypeScript ile alakalı konfigürasyonlar bu dosyada bulunur.
  -app ➡ Kullanılacak componentleri ve diğer Angular yapı taşlarını barındırır. Uygulamayla ilgili tüm çalışmalar burada yapılır. 
  -app-routing-module.ts ➡ Sayfalar arası route bilgilerini konfigüre edebileceğimiz dosyadır.
  -app.component.html ➡ Bu dosya, kullanıcı arayüzünün nasıl görüntüleneceğini tanımlar. Yani, kullanıcıların tarayıcıda gördüğü sayfanın yapısını ve içeriğini oluşturur.
  -app.module.ts ➡  Uygulamanın genel yapılandırmasını ve tüm modüllerin nasıl bir araya getirileceğini tanımlar.

  ### **☑.ts dosyalarını controller gibi düşünebiliriz.**


  ## Module Nedir❓
 ☑ Uygulama ögelerinin gruplandırılmasını sağlamaktadır. Böylece uygulama daha güzenli bir şekilde inşa edilebilir hale getirilmektedir. Uygulamanın çeşitli parçalarını (componenet, service gibi) bir araya getirererk bir bütün olarak kullanılabilir kılmaktadır. 
 ☑ Module dosyaları birbirini import etmediği takdirde, bir module içerisinde bulunan parça diğer bir module altındaki parçalar tarafından **kullanılamaz.**
 ☑ Module dosyaları Dependency Injection Pattern kullanarak uygulamadaki ögeler arasında bağımlılıkları yönetmekte ve bakım açısından kolaylık sağlamaktadır.
 ☑ Ayrıca, Angular'ın işlemleri optimize etmek için kullandığı 'Lazy Loading' özelliğini de destekleyerek sadece ihtiyaç duyulduğu takdirde yüklenmelerini sağlayabilmektedirler.


 ## Component Nedir❓
 ☑ Uygulamanın görüntüleme katmanını ifade eden ve veri modeliyle etkileşim kurarak kullanıcılara uygulamanın görsel ksmını sunan yapılardır.
 ☑ Yapısal olarak HTML ve TypeScript dosyalarından oluşmaktadırlar.
 ☑ Veri modeliyle etkileşim kurabilmek için Data Binding özelliğini kullanmaktadır.

 ## Data Binding Nedir❓
  ☑ Data Binding özelliği sayesinde veri modeli ile template dosyaları arasında (.ts ve .html dostaları arasında) veri akışı dinamik bir şekilde sağlanabilmektedir.
  ☑ Böylece uygulamadaki verisel değişiklikler otomatik olarak sayfalara yansıtılabilmektedir.
  ☑ Angular'da Data Binding çift yönlü çalışmaktadır. (Two Way Data Binding)

  ## Dependency Injection Nedir❓
  ☑ Uygulamada mevut olan ögeler arasındaki bağımlılıkları yönetebilmek için kullanılanılmaktadır. Yani bir bileşenin veya bir servisin bağımlı olduğu başka bir nesnenin (servis, bileşen, yapılandırma vb.)     dışarıdan enjekte edilmesi işlemidir. Dependency Injection, Angular uygulamalarında bileşenlerin, servislerin ve diğer nesnelerin birbirleriyle iletişim kurmasını, bağımlılıklarını yönetmesini ve daha kolay test edilebilmesini sağlar. Bu tasarım deseni, kodun daha modüler, sürdürülebilir ve test edilebilir olmasına yardımcı olur.

  ## Directive Nedir❓
  ☑ HTML nesnelerinin davranışlarını ve görünümlerini yönetebilmemizi sağlayan özel etiketlerdir.
  ☑ Uygulamanın oldukça dinamik ve etkileşimli olmasını sağlar.

  ## Decorator Nedir❓
   ☑ TypeScript dilinin bir özelliğidir.
   ☑ Bir class ya da class member'ına ekleyebilmekteyiz. Böylece ilgili yapının davranışı hakkında bir ön tanımda bulunmaktayız.
   ☑ Örneğin: @Component, @Injectable gibi @ işareti ile tanımlayabiliriz.

  ## Service Nedir❓ 
   ☑ Dış servislerle (API - EndPoint) iletişim kurmak, karmaşık iş operasyonlarını, business logic'i yürütmek  ya da componentler arasında iletişim sağlamak için kullanılan fiili yapılanmalardır.
   ☑ Operasyonel/fiili/kodlama gerektiren yapılardır.

  ## Template Nedir❓ 
   ☑ Componentlerin HTML kısmıdır. İçerisinde HTML kodları barındırabileceği gibi özel Angular elemanları, directive ya da pipe gibi birçok yapı barındırabilir.

  ## Guards Nedir❓
   ☑ Angular uygulamasıda route erişimlerinin izin kontrolleri Guard yapılanması üzerinden yapılmaktadır.
   ☑ Sayfalar arası geçiş süreçlerinde ilgili kullanıcılarının erişimine izin verilip verilmeyeceğine dair karar veren yapılanmalardır.

  ## Pipes Nedir❓
   ☑ Verilerin görüntülenme süreçlerinde işlenmesine yönelik işlevsellik sağlayan yapılardır.

  # Components
   ☑ Genellikle Angular uygulamasında componentlerin görevi sayfa altyapıları olarak kullanılmalarıdır. Bunun dışında sayfa olarak kullanılan componentlerin alt componentleri olarak da kullanılabilmekte. Böylece partial mantığında sayfaları geliştirmemize imkan verebilmektedir.
   ☑ Componentler birbirinden bağımsızdır. **Birbirleriyle iletişim kurarak büyük ve karmaşık uygulamaları yönetmeyi kolaylaştırır.**

   ### Template ➡ Componentin görsel çalışmalarının yapıldığı parçadır. 
   ☑ Componentin .html dosyasına karşılık gelmektedir ve templateUrl ile ilişkilendirilmektedir.
   ✳ Template işlemlerini fiziksel olarak ayrı bir dosya üzerinden gerçekleştirmek istiyorsanız .ts dosyası içerisinde template field'ına karşılık çalışabilirsiniz.

   ### Style ➡ Componentin css, scss çalışmalarının yapıldığı tasarım parçasıdır.
   ### Component Class ➡ Componentin merkezi olan ve .ts uzantılı olan dosyadır.
   ☑ Tüm JavaScript, TypeScript, JQuery işlemleri bu parça üzerinde gerçekleştirilir. Component içerisinde kullanılacak değişkenlerle birlikte fonksiyonlar bu sınıf üzerine tanımlanır. 
   ☑ Fonksiyonların nasıl işleneceği gibi işlevsellikler bu sınıf tarafından yönetilir. 
   ☑ İş mantığı gereği business logic barındıran servisler bu sınıf üzerinden çağırılır. Aynı şekilde API gibi dış servislere erişim sürecinin başlatılmasından sorumludur.

  ### Selector ➡ İlgili componentin, uygulamanın herhangi bir noktasında nasıl çağırılacağını tanımlayan bir referans özelliğidir. 
  ☑ **Sadece HTML dosyalarında kullanılabilmektedir.**
  ☑ Componentlerin birbirini selector ile referans edebilmeleri için ya aynı module içerisinde olmaları gerekiyor ya da buludukları module'den export edilmeleri gerekir.

   ☑ **Oluşturulan componentin kullanılabilmesi için ana module içerisinde declare edilmesi gerekir.**

  
  
  

