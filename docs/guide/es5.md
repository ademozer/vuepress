# Javascript (ES5) Kavramlar

## Hoisting

çoğu dilde bir değişken ya da fonksiyon çağrılmadan önde mutlaka tanımlanmalıdır.

*javascript*te ise kullanıldıktan sonra da tanımlanabilir.

örnek:

```
   "use strict";
   x = 10;
   console.log("x=" + x);
   var x;
```

konu ile ilgili daha detaylı bilgi için <https://www.tutorialsteacher.com/javascript/javascript-hoisting>

## Array Methods

- concat()
- every()
- filter()
- forEach()
- indexOf()
- join()
- lastIndexOf()
- map()
- pop()
- push()
- reduce()
- reduceRight()
- reverse()
- shift()
- slice()
- some()
- sort()
- splice()
- unshift()
- toString()

## Data Types (Veri Tipleri)

- Primitive (İlkel)
	- String
	- Number
	- Boolean
	- Null
	- Undefined
- Non Primitive (İlkel Olmayan)
	- Object
	- Array
	- Date

# Fetch API kullanımı

<https://dmitripavlutin.com/javascript-fetch-async-await/>
<https://dmitripavlutin.com/compare-javascript-strings/>

# Debounce ve Throttle 

<https://css-tricks.com/debouncing-throttling-explained-examples/>
<https://blog.bitsrc.io/understanding-throttling-and-debouncing-973131c1ba07>
<https://lodash.com/docs/4.17.15#throttle>

- **debounce (hata bildirme)** : birden fazla ardışık aramayı tek seferde yapmayı sağlar.  pencereyi yeniden boyutlandırmada kullanılabilir. (window.onResize)
- **throttle (kısma)**         : bir fonksiyonun belli bir süre de 1 kere çalışması anlamına gelir. pencereyi kaydırmada kullanılabilir. (window.onScroll)

Vue *debounce* ve *throttle* için dahili bir özellik sunmaz. **lodash** kullanılmasını tavsiye eder. 

örnek kullanım aşağıdaki gibidir. 

```
	import _ from 'lodash'
	...
	export default {
		name : "MyComponent",
		data : () => ({

		}),
		methods : {
			doSomeThing() {
				console.log("something")
			}
		},
		created () {
			_.debounce(doSomeThing, 100);
		}
	}
```


