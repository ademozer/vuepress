# OOP : Object Oriented Programming (Nesneye yönelik programlama)

<https://howtodoinjava.com/java/oops/object-oriented-programming/>

## Nesneye yönelik programlamanın 4 temel yapı taşı vardır.
![OOP Pillars](https://howtodoinjava.com/wp-content/uploads/2016/04/oop.png)

- Soyutlama (Abstraction)       : Varlığın temel özelliklerini ortaya çıkarma sürecidir.
- Kapsülleme (Encapsulation)    : Veri üzerindeki özellik ve işlemleri bir varlıkta paketleme sürecidir.
- Kalıtım (Inheritance)         : Mevcut bir türden yeni tür üretmek için kullanılır.    
- Çok Biçimlilik (Polymorphism) : Bir varlığın farklı bağlamlarda farklı davranışlar sergileyebilmesidir.

## NYP de bilinmesi gereken diğer Kavramlar

- Kuplaj     : (Coupling)           : İyi bir yazılım düşük kuplaja (low coupling) sahip olmalıdır. 
- Uyum       : (Cohesion)           : İyi bir yazılım yüksek uyuma (high cohesion) sahip olmalıdır.
- İş birliği : (Association)        : İki nesne arasında sahiplik olmayan bir ilişkiyi gösterir.
- Toplama    : (Aggregation)        : İki nesne arasında sahiplik olan bir ilişkiyi gösterir.
- Birleşim   : (Composition)        : İki nesne arasında bütün parça ilişkisini gösterir.   

## GRASP : General Responsibility Assignment Software Patterns (Genel Sorumluluk Atama Yazılım Desenleri)
9 tnedir

- 1. Information Expert : (Bilgi Uzmanı) 
	Sorumluluğun yerine getirebilecek ilgili sınıfa atanması<br> 
	Bu desen düşük eşleşim ve yüksek uyum desenleri ile de ilişkilidir.<br> 
	Bu desen aynı zamanda bilgi gizleme(information hiding) ve kapsülleme (encapsulation) ile de ilgilidir.

- 2. Creator : (Oluşturucu)
	Nesnenin oluşturulması ile ilgili desendir.
	Örnek olarak Fabrika Deseni (Factory Pattern) verilebilir. 
	Bu desende düşük eşleşim(low coupling) ile de ilişkilidir.

- 3. Controller : (Kontrolcü)
	Olayları işlemek ile ilgili desendir. 
	Command, Facade, Layers, Pure Fabrication desenleri ile ilişkilidir. 

- 4. Indirection : (Yönlendirme)
	MVC deseni örnek olarak verilebilir. 
	bu desende Controller View ile Model arasında bir köprü gibidir. View Modele Controller vasıtası ile dolaylı yoldan ulaşır. 
	Yine bu desen de düşük eşleşimi(low coupling) destekler.

- 5. Low Coupling : (Düşük Eşleşim) <https://www.sourcecodeexamples.net/2018/06/low-coupling-grasp-pattern.html>

- 6. Hihh Cohesion : (Yüksek Uyum)

- 7. Polymorphism : (Çok Biçimlilik)

- 8. Protected Variations : (Korumalı varyasyonlar)
	OCP Prensibi ile ilişkilidir.

- 9. Pure Fabrication : (Saf Üretim)
    

## SOLİD Prensipleri

- SRP : Single Responsibility (Tek Sorumluluk) 
- OCP : Open Closed (Gelişime Açık Değişime Kapalı)
- LSP : Liskov's Substutution (Alt sınıf üst sınıfın yerine kullanılabilmeli)
- ISP : Interface Segregation (Arayüz ayrıştırma)
- DIP : Dependency Inversion (Bağımlılığın ters çevrilmesi) 

## Tasarım Desenleri

- Strategy : bir strateji bir birinin yerine kullanılabilir bir dizi algoritmayı tanımlar. 
    <http://best-practice-software-engineering.ifs.tuwien.ac.at/patterns/strategy.html>
	örnek senaryo: 
		Hava Limanına Ulaşım.
			Seçenekler
			  Taxi
			  Özel Araç
			  Servis
			  Metro
- Command
- Proxy



## Mikroservis Tasarım Desenleri
<https://medium.com/better-programming/modern-day-architecture-design-patterns-for-software-professionals-9056ee1ed977>
- CB : Circuit Breaker (Devre Kesici)
	Bazı servislerde hata alınması durumunda kullanıcıya anlamlı bir mesaj vermek için kullanılabilir. 
	Netflix in geliştirmiş olduğu Hystrix uygulaması bu pattern kullanılarak geliştirilmiştir.
	<https://github.com/Netflix/Hystrix/wiki/How-it-Works>
- CQRS : Command and Query Responsibility Segragation (Komut ve Sorgu Sorumluluk Ayrımı)
	Read,Select -> Query  : Veri sorgulama işlemeleri ayrı bir db den yapılır. bu db belli aralıklarla orjinal db den güncellenir. 
	Create,Update,Write,Delete -> Command : Veri güncelleme işlemi orjinal db ye yapılır. 
	Bu pattern veriye erişimin çok olduğu durumlarda kullanılabilir. 
	Az kişinin kullanıdığı küçük ölçekli uygulamalarda tavsiye edilmez.

- MVC  : Model View Controller (Model Görünüm Kontrolcü)    
	Çok kullanılan bir patterndir. 
	DB ile ilgili nesneler Model olarak ifade edilir.
	UI ile ilgili nesneler View olarak ifade edilir.
	Her türlü fonksiyon, prosedür çağrımları Controller olarak ifade edilir.

- ES : Event Sourcing (Olay Kayıt)
	Özellikle microservice mimarisinde kullanılan bir patterndir.  

- Sidecar (Sepet)
- BFF : Backend for Frontend (Önuç için arkauç)
- Strangler (Boğucu)
	Uygulama modernizasyonuna gidilen durumlarda kullanılır. hem eski sistem hem de yeni sistemi Façade (Cephe) olarak birlikte kullanma imkanı verir. Göç(migration) sürecinin ilk evresinde kodların çoğu eski sistemdedir. orta evre de kodların yarısı eski sistemde yarısı yeni sistemdedir. son evrede ise kodların tamamı yeni sistemdedir. artık eski sistem kodları uygulamadan tamamen kaldırılabilir. 

## API Gateway && Service Mesh

<https://medium.com/better-programming/the-roles-of-service-mesh-and-api-gateways-in-microservice-architecture-f6e7dfd61043>