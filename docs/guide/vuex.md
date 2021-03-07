# Vuex Notları

## Vuex Nedir?

[Vuex][vuex], [Flux][flux], [Redux][redux] ve [Elm mimarisi][elm]nden esinlenenen, vue için uyarlanmış bir state yönetim kütüphanesidir.


## Vuex Ne Zaman Kullanılmalı?

Küçük uygulamalar için gerek yok. Orta ve büyük ölçekli SPA uygulamalarında kullanılmalıdır.

Redux yazarı *Dan Abramov* der ki:

>  Flux kütüphaneleri gözlük gibidir. onlara ne zaman ihtiyacınız olacağını bilirsiniz.

## Vuex Yapısı
Vuexin store yapısı 4 ana bileşenden oluşur.
![Vuex][vuex_png]
- **state**      : nesneleri tutar 
- **getters**    : nesnelere komponentlerden erişim sağlar
- **mutations**  : state de tutulan nesneleri değiştirmeyi sağlar.
- **actions**    : mutations daki metodları çağırır. komponentlerden çağrılabilir. 

Vuex, ayrıca bu bileşenlere view komponentlerinden erişim için 3 tane map bileşeni sağlar.
- **mapState**   : state e erişmeyi sağlar.
- **mapGetters** : getters a erişmeyi sağlar.
- **mapActions** : actionsa erişmeyi sağlar.

## mapGetters

[mapGetters nasıl kullanılır.][mapGetters] 

```
import {mapGetters} from 'vuex';


	computed() {
		...mapGetters(["customerList"])
    }
```
Bu kod aşağıdaki ile aynı işi yapar. 

```
    computed() {
	   customerList : {
	   	  return $store.getters.customerList;
	   }
	}
```

Buradaki üç nokta (...) bir ES6 sözdizimi olup [spread (yayılma)][spread] operatörüdür.

[vuex]: https://vuex.vuejs.org/
[vuex_png]: https://vuex.vuejs.org/vuex.png
[mapGetters]: https://tenmilesquare.com/understanding-mapgetters-in-vuex/
[flux]: https://facebook.github.io/flux/docs/overview/
[redux]: https://redux.js.org/
[elm]: https://guide.elm-lang.org/architecture/
[spread]: https://tenmilesquare.com/5-uses-for-the-spread-operator/