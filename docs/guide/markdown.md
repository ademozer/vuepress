# Mark Down Nedir?

Mark Down bir işaretleme dili (**markup language**) olup html ye dönüştürülebilir. 
[CommonMark][commonmark]

kare(#) başlık anlamına gelir. bir tane olursa h1 tagine karşılık gelir.

tek yıldız (*) html deki **em** ya da **i** tagine karşılık gelir. içindeki metni *italik* yapar.

```
*italik*
```

çift yıldız(asterix)  ya da çift underscore (_) html deki **b** ya da **strong** tagine karşılık gelir. içindeki metni **bold** yani __kalın__ yapar.  bazı markdown editörleri underscore u desteklemez. 
bu nedenle asterix kullanacağız.

```
**bold**
```

üç yıldız html deki ***stong em*** taglerine karşılık gelir. içindeki metni ***bold ve italik*** yapar.

```
***bold + italik***
```

> blockquote yani alıntı için paragrafın başına büyük(>) işareti konulur. 
> alıntı birden fazla paragraf ise her paragrafın başına bu işaret konulur. 
> iç içe alıntı için çift büyük (>>) işareti konulur.

#### Listeler ####

##### sırasız liste (unordered list) =>  ul li #####

```
- elma
- armut
- ayva
```

- elma
- armut
- ayva

(-)  yerine (*,+) da kullanılabilir.

##### sıralı liste (ordered list) => ol li #####
```
1. elma
1. armut
2. ayva
```
1. elma
2. armut 
3. ayva

##### tanım listesi (definition lists) => dl dt dd #####

```
İlk madde
: deneme1
: deneme2

İkinci madde
: deneme2
: deneme4
```

**Not:** Bunu bazı markdown yorumlayıcıları desteklemeyebilir. 

#### Resimler (images) ####

! + [] + () ile dahil edilir.<br> 
[] içerisine resmin ismi yazılır.<br> 
() içerisine de url aresi yazılır. bu html deki **img** tagine karşılık gelir.<br>

```
![Tux](https://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg)
``` 
![Tux](https://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg)

#### Code ####

backticks (Alt+96)  **code** tagine karşılık gelir. bunu iki defa kullanırsanız  birisi escape karekteri olur. 
``` Markdown dosyasında  `code` kullanabilirsiniz. ``` 

ters backticks(Alt+0180) <br>
kod blokları için space ya da tab karakterleri kullanılır.
```
    <html>
        <head>
            <title> deneme </title>
        </head>
    </html>
```
#### Tablo ####
```
    |Syntax     |Açıklama  |
    | :---:     | :---     |
    |Header     | Title    |
    |Pargraph   | Text     |
```
|Syntax     |Açıklama  |
|  :---:    | :---     |
|Header     | Title    |
|Pargraph   | Text     |


#### Yatay Çizgi (Horizontal Rule) ####

 için 3*,3- ya da 3_ kullanılır. (sonuncusu tercihimizdir. 3 tane underscore)

 ```
    ***
    ---
    ___
```
___

#### Link ####

Link için [] + () yapısı kullanılır. 

 ```
    Benim favori aram motorum [Duck Duck Go](http://duckduckgo.com "kendisi en iyi arama motorudur bence") dur.
 ```

Benim favori aram motorum [Duck Duck Go](http://duckduckgo.com "kendisi en iyi arama motorudur bence") dur. 

##### Diğer Bir Link Yöntemi ##### 
```
    [Dillinger Online Markdown Editörü][dillinger]
    ... 
    [dillinger] : http://dillinger.io
```
 [Dillinger Online Markdown Editörü][dillinger] <br>
 [Markdown Söz Dizimi][markdown]

##### Url ve Email #####

 ```
    <http://www.magdeburger.com.tr>
    <adem.ozer@magdeburger.com.tr>
 ```

<http://www.magdeburger.com.tr> <br>
<adem.ozer@magdeburger.com.tr>



[dillinger]: http://dillinger.io
[markdown]: https://www.markdownguide.org/basic-syntax
[commonmark]: https://commonmark.org/help/

