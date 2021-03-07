# Vue Kullanımı


## Vue Örnekleri

- [Vue Vuex Jwt][vue-jwt]
- [Vue Material Design Dashboard][vue-mdd]

<https://www.telerik.com/blogs/how-to-emit-data-in-vue-beyond-the-vuejs-documentation>

<https://johnpapa.net/vue-typescript/>

emit : yaymak. 

bir alt bileşenden üst bileşene bir olayın (event) aktarılması işlemidir.

alt bileşende 

```
   <v-btn @click="$emit("saveCustomer", customer)" />
```

şeklinde çağrılır. 

bu bileşeni kullanan ana bileşende ise kullanım aşağıdaki gibidir. 

```
   <customer @saveCustomer="saveCustomer($event)">
   ...
   methods : {
   	   saveCustomer(value) {
   	   	    this.customer = value;
   	   }
   }
 ```

 ## Slot Kavramı
 
 <https://vuejs.org/v2/guide/components-slots.html#Slot-Content>
 <https://github.com/WICG/webcomponents/blob/gh-pages/proposals/Slots-Proposal.md>

 **slot** lügatte *yuva* anlamına gelir.
 Vue terminolojisinde ise, *bir gölge ağacında tanımlanmış konum* anlamına gelir. 

 örneğin bir BaseLayout.vue şablonu aşağıdaki gibi olabilir. 


```
 <div class="container">
   <header> 
     <slot name="header"></slot>
   </header>
   <main> 
     <slot></slot>
   </main>
   <footer> 
     <slot name="footer"> </slot> 
   </footer>
 </div>
 ```

 bu şablonu kullanan bir kod aşağıdaki gibi olabilir.

 ```
 <base-layout>
    <template v-slot:header>
    	Başlık
   </template>
   <template v-slot:default>
       İçerik
   </template>
   <template #footer>
   	   alt kısım
   </template>
</base-layout>
```

bir başka örnek. 


```
   SubmitButton.vue

   <button type="submit">
      <slot>Submit</slot>
   </button>
   ...

   <submit-button /> 
   <submit-button> Kaydet </submit-button>
   <submit-button> 
      <template #default>
         <v-icon>mdi-save</v-icon>
      </template>
   </submit-button>
```


- Nasıl ki v-on: yerine @, v-bind: yerine : kısa gösterimlerini kullanabiliyorsak v-slot: yerine de # kısa gösterimini kullanabiliriz. #footer ile  v-slot:footer aynı anlamdadır. 
- *slot-scope* sözdizimi 2.6 versiyonu ile birlikte (@deprecated) olarak işaretlenmiş olup 3 versiyonu ile birlikte tamammen kullanımdan kaldırılmıştır. 
- *slot* attribute 2.6 versiyonu ile birlikte (@deprecated) olarak işaretlenmiş olup 3 versiyonu ile tamamen kaldırılacaktır. 
bunun yerine *v-slot* ya da kısa gösterim ile *#* kullanılacaktır. 

![scoped-slots](https://v3.vuejs.org/images/scoped-slot.png)

## JSON Excel

<https://libraries.io/npm/vue-json-excel>

## Vue 3 te ne yeni

<https://www.smashingmagazine.com/2020/11/new-vue3-update/>

[vue-jwt]: https://jasonwatmore.com/post/2018/07/06/vue-vuex-jwt-authentication-tutorial-example
[vue-mdd]: https://vuejsexamples.net/vue-js-material-design-dashboard/