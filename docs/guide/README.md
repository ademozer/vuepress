# VuePresse Giriş

VuePress iki kısımdan meydana gelmiştir : bir vue-powered [tema sistemi](https://v1.vuepress.vuejs.org/theme/) ve [Plugin API](https://v1.vuepress.vuejs.org/plugin/) ile [minimalist statik site oluşturucu](https://github.com/vuejs/vuepress/tree/master/packages/%40vuepress/core) , ve bir de teknik dökümantasyon için iyileştirilmiş [varsayılan tema](https://v1.vuepress.vuejs.org/theme/default-theme-config.html). Vue'nin kendi alt projelerinin dökümantasyonunu sağlamak için geliştirildi. 

VuePress trafından üretilen her sayfa, SEO dostu büyük yükleme performansı sağlayan önceden oluşturulmuş static HTML dir.  
Sayfalar yüklendikten sonra Vue statik içeriği devralır ve Single Page Application (SPA) yapısına dönüştürür. Kullanıcı sitede dolaşırken talep ederse ek sayfaları görebilir.

## Tarayıcı API Erişim Kısıtlamaları (Browser API Access Restrictions)

VuePress uygulamaları, statik yapılar oluştururken Node.js'de sunucu tarafından işlendiğinden [evrensel kod gereksinimleri][ucr]ne uymalıdır. Kısacası **beforeMount** ve **mount** kancaları(hooks) kullanılırken tarayıcının DOM API lerine erişildiğinden emin olunmalıdır. 

SSR dostu olmayan bileşenler (örneğin özel yönergeler içeren) kullanıyorsanız veya bunların tanıtımını yapıyorsanız, bunları yerleşik **`<ClientOnly>`** bileşeninin içine alabilirsiniz:

[ucr]: https://ssr.vuejs.org/en/universal.html