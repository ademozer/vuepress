# ES6 - EcmaScript 6

Ecmascript 6 yani javascript 2016 

[ES6][es6] da yeni gelen özellikler. 

- Constants (Sabitler)
	```
	    const PI=3.14;
	```
- Block Scoped Variables (Blok Kapsamlı Değişkenler)
	```
		let a=1;
		{
			let b=2;
			console.log(b);
			console.log(a);
		}
		console.log(a);
		console.log(b); // hata verir. (ReferenceError: b is not defined)
	```
- Arrow Functions ( Ok Fonksiyonları)
	```
		let cift = [0,2,4,6,8];
		let tek = cift.map(sayi => sayi + 1);
		console.log(tek); // ekrana [1,3,5,7,9] yazar.

		let dortluk = [];
		cift.map(sayi => {           // map yerine forEach de kullanılabilir. cift.forEach(sayi ...)
		    if(sayi % 4 === 0) {
               dortluk.push(sayi);
		    }
		});
		console.log(dortluk); // ekrana [0, 4, 8] yazar.
	```
- Default Parameter Values (Varsayılan Parametre Değerleri)
	```
	   function f(x, y=10) {
          return x + y;
	   }
	   console.log(f(5)); // ekrana 15 yazar.
	 ```
- Rest Parameters (Kalan Parametreler)
	```
	   function f(x,y, ...diger) {
          return x + y + diger.length;
	   }	
	   console.log(f(1,1,3,"ali",4,8)); // ekrana 6 yazar. 
	```
- Spread Operator (Yayılma Operatörü)
	```
		let params = [3,"ali", 4,8];
		console.log(...params); // ekrana 3 ali 4 8 yazar.

		let isim = "adem";
		let harfler = [...isim]; 
		console.log(harfler); // ekrana [ 'a', 'd', 'e', 'm' ] yazar.
	```
- String Interpolation (String Enterpolasyonu)
	```
		var customer = {name : "Adem"};
		var message = `merhaba ${customer.name}`;
		console.log(message); // merhaba Adem 

	```
- Enhanced Object Properties (Genişletilmiş Nesne Özellikleri)
	```
       var x=0, y=0;
       obj = {x, y} // es5 karşılığı obj = { x : x,  y : y }

       obj = {
       		member1(x, y) {  // es5 karşılığı member1 : function(x,y) { ... şeklindedir.                    
       	    },
       	    member2(a,b) {
       	    } 
       }  
	```
- Modules (Modüller)
	```
		//lib\math.js
		export sum(x,y) => { return x + y};
		export const PI = 3.14;

		//module_example.js
		import {sum, PI} from 'lib/math';

		console.log("2Pi=" + sum(PI,PI)); // 2PI = 6.28

	```
- OOP (Object Oriented Programming - Nesneye yönelik Programlama) Özellikleri
	- Class Definition (Sınıf Tanımlama)
		```
		   class Sekil {
              constructor(name) {
                 this.name = name;
              }
              info(){
                  let message = `Bu şeklin adı ${this.name} dir.`;
                  console.log(message);
              }
		   }
		   var ucgen = new Sekil("Üçgen");
		   ucgen.info(); // Bu şeklin adı üçgendir. 
		```
	- Inheritance (Miras Alma)
		```
           class Ucgen extends Sekil {
              constructor(name, taban, yukseklik) {
                  super(name); 
                  this.taban = taban;
                  this.yukseklik = yukseklik;
              }
              info() {
                 let alan = this.taban * this.yukseklik / 2;
                 let message = `${this.name} üçgeninin alanı ${alan} metrekaredir`; 
                 console.log(message);   
              }
           }
           var ucgen = new Ucgen("Benim Üçgenim", 10, 5);
		   ucgen.info(); //Benim Üçgenim üçgeninin alanı 25 metrekaredir
		```
[es6]: http://es6-features.org