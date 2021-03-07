# Vuetify nedir? 

[Vuetify][vuetify] [VueJs][vue] ile [Material CSS][material] frameworküne uygun önyüz geliştirmeyi sağlayan bir plugindir. 
[John Leider][john] tarafından geliştirilmektedir.

## Veutify kurulumu 

```
    vue add vuetify
```
## Vuetify UI Komponentleri

- [v-alert][v-alert]     : Uyarı
- [v-app][v-app]         : Yerleşim Düzeni(Layout) Tasarımı
    - v-main
- [v-responsive][v-resp] : En Boy Oranları (Aspect Ratio)
- [v-avatar][v-avatar]   : Genellikle kullanıcı profil resmini göstermek İçin kullanılır.
- [v-badge][v-badge]     : Avatar benzeri içeriğin üzerindeki simge veya yazı
- [v-banner][v-banner]   : Banner
- Bar Komponentleri
    - [v-app-bar][v-app-bar]
        - v-app-bar-nav-icon
    - [v-toolbar][v-toolbar]
        - v-toolbar-title
        - v-toolbar-items
    - [v-system-bar][v-system-bar]
- [v-bottom-navigation][v-bottom-navigation]
- [v-bottom-sheet][v-bottom-sheet] : Altta bir diyalog açar. v-dialog komponentinden türemiştir. 
- [v-breadcrumbs][v-breadcrumbs] : Sayfalar için gezinme yardımcısı
    - v-breadcrumbs-item
- [v-btn][v-btn] : HTML deki `<button>` tagine karşılık gelir.
    - v-btn-toggle
- [v-speed-dial][v-speed-dial] : Kayan Eylem Butonları(Floating Action Buttons)
- [v-calendar][v-calendar] : Takvim Komponentleri (Calendars)
    - v-calendar-daily
    - v-calendar-monthly
    - v-calendar-weekly
- [v-card][v-card] : Panelden statik görüntüye kadar her şey için kullanılabilen çok yönlü bir komponent
    - v-card-actions
    - v-card-subtitle
    - v-card-text
    - v-card-title
- [v-carousel][v-carousel] : Slayt benzeri çoklu görüntüleri yöneten bir komponent. bu komponenti muhtemelen kullanmayacağız.
    - v-carousel-item
- [v-chip][v-chip] : Küçük bilgi parçalarını göstermek için kullanılır.
- [v-dialog][v-dialog] : Dialogs
- [v-divider][v-divider] : İki komponentin arasını ayırır. HTML deki `<hr>` tagine benzer.
- [v-expansion-panels][v-expansion-panel] : Genişleme Panelleri
    - v-expansion-panel
    - v-expansion-panel-header
    - v-expansion-panel-content
- [v-footer][v-footer] : Sayfanın en altında genel bilgileri göstermek için kullanılır.
- Grid Sistemi Komponentleri
    - [v-container][v-container] : İçeriği ortalar. *v-row* komponentini sarmalar.
        - v-row : *v-col* komponentini sarmalar. eski *v-layout* yerine kullanılır. 
            - v-col : içerik buraya konulur. eski *v-flex* yerine kullanılır.
        - v-spacer
- [v-hover][v-hover] : Üzerine gelme işlemi
- [v-icon][v-icon] : İkonlar
    - [mdi-](https://materialdesignicons.com/) : Material Design İcons 
    - [material icons](https://material.io/resources/icons/?style=baseline) 
    - [fa-](https://fontawesome.com/icons?from=io) : Font Awesome 
    <br><https://vuetifyjs.com/en/customization/icons/#install-material-icons>
    <br><https://vuetifyjs.com/en/customization/icons/#install-font-awesome-5-icons> 
    ```
    <v-icon>mdi-home</v-icon>
    <v-btn icon="mdi-home" />
    ```
- [v-img][v-img]: HTML deki `<img>` tagine karşılık gelir.
- [v-lazy][v-lazy] : Yavaş yükleme (Lazy Loading) 
- [v-list][v-list] : Listeler. HTML deki `<ul>` ve `<ol>` taglerine karşılık gelir.
    - v-list-item : HTML deki `<li>` tagine karşılık gelir. 
    - v-list-group
    - v-list-item-action
    - v-list-item-avatar
    - v-list-item-content
- [v-menu][v-menu] : Menüler
- [v-navigation-drawer][v-navigation-drawer] : Gezinme Çekmeceleri ( Navigation Dravers). 
    ```
    <template>
    <v-main> 
        <v-navigation-drawer
            v-model="drawer"
            :clipped = "$vuetify.breakpoint.lgAndUp"
            app
             >  
        </v-navigation-drawer>
        <v-app-bar>
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        </v-app-bar>
    </v-main>
    </template>
    <script>
    export default {
        name : "Test",
        data: () => ({
            drawer: null
        }),
        mounted() {
            console.log("Test Bağlandı");
        }
    }
    </script>
    ```
- [v-overlay] : Overlays
- [v-pagination][v-pagination] : Sayfalama (Pagination) 
- [v-parallax][v-parallax] : bir resme 3d efekti vermek için kullanılır.  
- Picker Komponentleri
    - [v-color-picker][v-color-picker] : Renk Seçici (Color Picker) 
    - [v-date-picker][v-date-picker] : Tarih (Yıl/Ay/Gün) Seçici (Date Picker)
    - [v-time-picker][v-time-picker] : Saat Seçici (Time Picker)
- Progress
    - [v-progress-circular][v-progress-circular] : Dairesel(Circular)
    - [v-progress-linear][v-progress-linear] : Doğrusal (Linear)
- [v-rating][v-rating] : Oranlar (Ratings)
- [v-sheet][v-sheet] : HTML deki `<span>` tagine benzer. Düşük seviyeli(low level) bir komponenttir.
- [v-skeleton-loader][v-skeleton-loader] : bir şeyin yüklenmekte olduğunu belirtir.
- [v-snackbar][v-snackbar] : kullanıcıya bir mesaj göstermek için kullanılır. *v-dialog* a benzer. 
- [v-sparkline][v-sparkline] : Mini Grafik (Sparkline) 
- [v-stepper][v-stepper] : Adım Adım İlerleme (Stepper)
    - v-stepper-step
    - v-stepper-content
    - v-stepper-header
    - v-stepper-items
- [v-subheader][v-subheader] :HTML deki  `<span>` benzeri bir komponent daha. listelerdeki bölümleri ayırmak için kullanılır.
- Tables (Tablolar)
    - [v-data-iterator][v-data-iterator] : Veri görüntülemek için kullanılır.<br>
        v-data-table ın aksine verileri istenildiği gibi gösterebilir.  
        v-data-table ise verileri alt alta listeler.
        - v-data-footer

    - [v-simple-table][v-simple-table] : HTML deki `<table>` tagine karşılık gelir.
    - [v-data-table][v-data-table] : Tablo şeklindeki verileri görüntülemek için kullanılır.
        - v-data-table-header
        - v-edit-dialog
        - v-simple-checkbox<br>
        Rows Per Page ifadesini değiştirmek için footer-props özelliği kullanılır.
        ```
            <v-data-table 
                  :headers = "headers" 
                  :items = "items"  
                  class = "elevation-2"
                  :footer-props = "{'items-per-page-text':'Sayfada görüntülenecek kayıt sayısı'}"> 
            </v-data-table>
        ```
- [v-tabs][v-tabs] : İçeriği seçilebilir bir öğenin arkasına gizlemek için kullanılır.
    - v-tab
    - v-tabs-items
    - v-tab-item
    - v-tabs-slider
- [v-timeline][v-timeline] : Kronolojik bir bilgiyi göstermek için kullanılır.
    - v-timeline-item
- [v-tooltip][v-tooltip] : Kullanıcı bir öğenin üzerine geldiğinde bilgi aktarmak için kullanılır. *v-hover* a benzer.
- [v-treeview][v-treeview] : Çok miktarda iç içe veriyi ağaç yapısında görüntülemek için kullanılır.
- [v-virtual-scroll][v-virtual-scroll] : Sanal Kaydıraç (Virtual Scroller)


## Grup Komponentleri
- [v-btn-toggle][v-btn-toggle] : *v-btn* ile çalışmak için oluşturulmuş olup *v-item-groups* için bir sarmalayıcıdır.
    - v-btn
- [v-chip-group][v-chip-group] : *v-chip* için bir sarmalayıcıdır.
    - v-chip
- [v-item-group][v-item-group] : herhangi bir bileşenden seçilebilir öğe oluşturmak için kullanılır.
    - v-item
- [v-list-item-group][v-list-item-group] : *v-list-item* öğelerinden seçilebilir bir grup oluşturur.
    - v-list-item
    - v-list-item-action
    - v-list-item-avatar
    - v-list-item-content
    - v-list-item-title
    - v-list-item-subtitle
    - v-list-item-action-text
- [v-slide-group][v-slide-group] : sayfalandırılmış bilgileri görüntülemek için kulllanılır.
    - v-slide-item
- [v-window][v-window]: bir sayfadan diğerine geçmek için temel bir işlevsellik sağlar. *v-tabs*, *v-carousel*, *v-stepper* gibi.
    - v-window-item

## Vuetify Form Komponentleri

Form tasarlamak için aşağıdaki komponentler kullanılır. 
- [v-input][v-input] : özel inputlar oluşturmak için bir temel bir komponenttir.
- [v-text-field][v-text-field] : kullanıcı tarafından sağlanan bilgileri toplamak için kullanılır.
- [v-autocomplete][v-autocomplete] : basit ve esnek önceden yazma özelliği sağlar.
- [v-combobox][v-combobox] : `v-autocomplete` den türemiştir. kullanıcı listede olmayan veri girebilir.
- [v-file-input][v-file-input] : dosya seçme imkanı sağlar.  
- [v-form][v-form]: Validasyon özellikleri sağlar. Validasyon için alternatif olarak [vee-validate](https://github.com/logaretm/vee-validate)  ya da [vuelidate](https://github.com/vuelidate/vuelidate) de kullanılabilir.
- [v-overflow-btn][v-overflow-btn] : Listeden öğe seçme özelliği sağlar. *v-combobox* gibi. 
- [v-select][v-select]: HTML deki `<select>` tagine karşılık gelir. *v-combobox* ve *v-owerflow-btn* gibi listeden seçme özelliği sağlar.
- [Seçim Kontrolleri (Selection Controls)](https://vuetifyjs.com/en/components/selection-controls/)
    - v-checkbox : HTML deki `<input type="checkbox">` tagine karşılık gelir.
    - v-radio    : HTML deki `<input type="radio">` tagine karşılık gelir. *v-radio-group* ile birlikte kullanılır.
    - v-radio-group : *v-radio* öğesini sarmalar. *v-model* property ile kullanılmalıdır.
    - v-switch   : true ya da false değerini alabilen verileri göstermek için kullanılır.
    - v-simple-checkbox
- [v-slider][v-slider] : Sayısal verileri görselleştirmek için kullanılır.
    - v-range-slider
- [v-textarea][v-textarea] : HTML deki `<textarea>` taginin işlevselliğini sağlar.


## v-input 
bu komponentin genişletilmiş halini kullanmanız tavsiye edilir. fakat bu hali ile de kullanılabilir.  
bu tag ile birlikte kullanılan 4 adet slot vardır. 
- append
- prepend
- messages
- default

örnek kullanım: 
```
<v-input :messages="['Messages']" 
         append-icon="mdi-close" 
         prepend-icon="mdi-phone"> 
    Default Slot 
</v-input>
```
diğer kullanım örnekleri:  
<https://github.com/vuetifyjs/vuetify/blob/master/packages/docs/src/examples/inputs/playground.vue>

## v-text-field 
    
kullanım tüleri aşağıdaki gibidir.
        
- Düz (Reqular) : Bir Çizgi üzerinde giriş yapılır. 
```        
<v-text-field label="Label" placeholder="Place Holder"/>
```                   
- Boş (Solo) : Bir kutu içerisinde giriş yapılır.
```        
<v-text-field label="Label" placeholder="Place Holder" solo | filled | outlined/>
```                
- Dolu (Filled) : içi dolu bir kutu 
- Dışı çizgili (Outlined) : dışı çerçeveli bir kutu 
- shaped : filled, outlined, solo ile birlikte kullanıldığında üst köşeleri yuvarlar. 
- clearable : en sağa bir X ikonu ekler. bu ikona tıklandığında input temizlenir. 
- persistent-hint : hintin sürekli görünmesini sağlar. 

diğer kullanım örnekleri:
<https://github.com/vuetifyjs/vuetify/blob/master/packages/docs/src/examples/text-fields/playground.vue>
## Direktifler
- **Click Outside** 
<br>*v-click-outside* direktifi hedef elementin dışına tıklanınca çağrılır.
<https://vuetifyjs.com/en/directives/click-outside/>
```
  <template>
    <v-card 
        v-click-outside="onClickOutside"
        :color="active ? 'primary' : undefined"
        :dark="active"
        class="mx-auto"
        height="256"
        rounded="xl"
        width="256"
        @click="active = true">
            {{ active ? 'Etrafımı Tıkla' : 'Beni Tıkla' }}
    </v-card>
  </template>
  <script>
     export default {
        data: () => ({
            active: false,
        }),

        methods: {
        onClickOutside () {
            this.active = false
        },
        },
    }
  </script>  
```
- **Intersection Observer**
<br> *v-intersect* direktifi [Intersection Observer (Kesişim Gözlemci) API][ioa] yi kullanır. 
<https://vuetifyjs.com/en/directives/intersect/>

- **Mutuation Observer**
<br> *v-mutate* direktifi [Mutuation Observer (Değişim Gözlemci)  API][moa] yi kullanır. 
<https://vuetifyjs.com/en/directives/mutate/>

- **Resize Directive**
<br> *v-resize* direktifi windowun boyutlarıdaki değişimi algılar.
<https://vuetifyjs.com/en/directives/resizing/>

- **Ripple Directive**
<br> *v-ripple* direktifi kullanıcının yaptığı eylemi(action) göstermek için kullanılır.
<br> Blok seviyesindeki bileşenlere uygulanabilir. (Not: *Ripple* Hafifçe Dalgalanma demektir.)
<br> v-btn, v-tabs-item gibi bir çok bileşen v-ripple direktifi uygulanmış şekilde gelir. 
<https://vuetifyjs.com/en/directives/ripples/>

- **Scrolling Directive**
<br> *v-scroll* direktifi hedef bileşen kaydırıldığında bir *callback* metodu çağırmanızı sağlar.
<https://vuetifyjs.com/en/directives/scrolling/>

- **Touch Support**
<br> *v-touch* direktifi kaydırma hareketlerini yakalamaya ve iki yönlü *callback* çağırmaya imkan sağlar.
<https://vuetifyjs.com/en/directives/touch-support/>

## Style Animasyonları
- Css Reset & Border Radius
<br><https://vuetifyjs.com/en/styles/css-reset/>
<br><https://vuetifyjs.com/en/styles/border-radius/>

- Colors
<br><https://vuetifyjs.com/en/styles/colors/>

- Content & Display
<br><https://vuetifyjs.com/en/styles/content/>
<br><https://vuetifyjs.com/en/styles/display/>

- Elevation
<br>Yükseklik
<br><https://vuetifyjs.com/en/styles/elevation/>

- Flex - Float
<br><https://vuetifyjs.com/en/styles/flex/>
<br><https://vuetifyjs.com/en/styles/float/>

- Spacing (Margin, Padding)
<br><https://vuetifyjs.com/en/styles/spacing/>

- Text And Typography
<br><https://vuetifyjs.com/en/styles/text-and-typography/>

- Transitions
<br><https://vuetifyjs.com/en/styles/transitions/>

- Programatic Scrolling
<br><https://vuetifyjs.com/en/styles/scroll/>

##

[vuetify]: https://vuetifyjs.com/en/ 
[material1]: https://materializecss.com/
[material]: https://material.io/components
[vue]: http://vuejs.org
[john]: https://github.com/johnleider
[ioa]: https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API
[moa]: https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver
[v-alert]: https://vuetifyjs.com/en/components/alerts/
[v-app]: https://vuetifyjs.com/en/components/application/
[v-resp]: https://vuetifyjs.com/en/components/aspect-ratios/
[v-avatar]: https://vuetifyjs.com/en/components/avatars/
[v-badge]: https://vuetifyjs.com/en/components/badges/
[v-banner]: https://vuetifyjs.com/en/components/banners/
[v-app-bar]: https://vuetifyjs.com/en/components/app-bars/
[v-toolbar]: https://vuetifyjs.com/en/components/toolbars/
[v-system-bar]: https://vuetifyjs.com/en/components/system-bars/
[v-bottom-navigation]: https://vuetifyjs.com/en/components/bottom-navigation/
[v-bottom-sheet]: https://vuetifyjs.com/en/components/bottom-sheets/
[v-breadcrumbs]: https://vuetifyjs.com/en/components/breadcrumbs/
[v-btn]: https://vuetifyjs.com/en/components/buttons/
[v-speed-dial]: https://vuetifyjs.com/en/components/floating-action-buttons/#buttons-floating-action-button
[v-calendar]: https://vuetifyjs.com/en/components/calendars/
[v-card]: https://vuetifyjs.com/en/components/cards/
[v-carousel]: https://vuetifyjs.com/en/components/carousels/
[v-chip]: https://vuetifyjs.com/en/components/chips/
[v-dialog]: https://vuetifyjs.com/en/components/dialogs/
[v-divider]: https://vuetifyjs.com/en/components/dividers/
[v-expansion-panel]: https://vuetifyjs.com/en/components/expansion-panels/
[v-footer]: https://vuetifyjs.com/en/components/footer/
[v-container]: https://vuetifyjs.com/en/components/grids/
[v-btn-toggle]: https://vuetifyjs.com/en/components/button-groups/
[v-chip-group]: https://vuetifyjs.com/en/components/chip-groups/
[v-item-group]: https://vuetifyjs.com/en/components/item-groups/
[v-list-item-group]: https://vuetifyjs.com/en/components/list-item-groups/
[v-slide-group]: https://vuetifyjs.com/en/components/slide-groups/
[v-window]: https://vuetifyjs.com/en/components/windows/
[v-hover]: https://vuetifyjs.com/en/components/hover/
[v-icon]: https://vuetifyjs.com/en/components/icons/
[v-img]: https://vuetifyjs.com/en/components/images/
[v-lazy]: https://vuetifyjs.com/en/components/lazy/
[v-list]: https://vuetifyjs.com/en/components/lists/
[v-menu]: https://vuetifyjs.com/en/components/menus/
[v-navigation-drawer]: https://vuetifyjs.com/en/components/navigation-drawers/
[v-overlay]: https://vuetifyjs.com/en/components/overlays/
[v-pagination]: https://vuetifyjs.com/en/components/paginations/
[v-parallax]: https://vuetifyjs.com/en/components/parallax/
[v-color-picker]: https://vuetifyjs.com/en/components/color-pickers/
[v-date-picker]: https://vuetifyjs.com/en/components/date-pickers/
[v-time-picker]: https://vuetifyjs.com/en/components/time-pickers/
[v-progress-circular]: https://vuetifyjs.com/en/components/progress-circular/
[v-progress-linear]: https://vuetifyjs.com/en/components/progress-linear/
[v-rating]: https://vuetifyjs.com/en/components/ratings/
[v-sheet]: https://vuetifyjs.com/en/components/sheets/
[v-skeleton-loader]: https://vuetifyjs.com/en/components/skeleton-loaders/
[v-snackbar]: https://vuetifyjs.com/en/components/snackbars/
[v-sparkline]: https://vuetifyjs.com/en/components/sparklines/
[v-stepper]: https://vuetifyjs.com/en/components/steppers/
[v-subheader]: https://vuetifyjs.com/en/components/subheaders/
[v-data-iterator]: https://vuetifyjs.com/en/components/data-iterators/
[v-simple-table]: https://vuetifyjs.com/en/components/simple-tables/
[v-data-table]: https://vuetifyjs.com/en/components/data-tables/
[v-tabs]: https://vuetifyjs.com/en/components/tabs/
[v-timeline]: https://vuetifyjs.com/en/components/timelines/
[v-tooltip]: https://vuetifyjs.com/en/components/tooltips/
[v-treeview]: https://vuetifyjs.com/en/components/treeview/
[v-virtual-scroll]: https://vuetifyjs.com/en/components/virtual-scrollers/
[v-input]: https://vuetifyjs.com/en/components/inputs/
[v-text-field]: https://vuetifyjs.com/en/components/text-fields/
[v-autocomplete]: https://vuetifyjs.com/en/components/autocompletes/
[v-combobox]: https://vuetifyjs.com/en/components/combobox/
[v-file-input]: https://vuetifyjs.com/en/components/file-inputs/
[v-form]: https://vuetifyjs.com/en/components/forms/
[v-overflow-btn]: https://vuetifyjs.com/en/components/overflow-btns/
[v-select]: https://vuetifyjs.com/en/components/selects/
[v-slider]: https://vuetifyjs.com/en/components/sliders/
[v-textarea]: https://vuetifyjs.com/en/components/textarea/