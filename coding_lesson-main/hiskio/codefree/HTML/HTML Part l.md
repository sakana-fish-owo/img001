> **構成網頁的3大基本要素之一：HTML**

`HTML就像網頁的身體，JavaScript 是大腦，CSS是衣服。`

**\HTML（HyperText Markup Language 超文本標記語言）**：

它被用來描述**網頁的結構**。作用在於定義網頁內有什麼內容元素。直接關係網頁製作的結構問題，甚至影響搜尋排名。他可以透過不同標籤，定義不同的內容。如< p >就是放文字、< video >就是放影片。

------

> **HTML 語法組成**

除了少數的例子外，HTML 大多都是成對存在的喔！分別 **「開始標記」、「結束標記」外加「內容」**3 個部分所以構成。*結束標記比開始標記多了一槓斜線*

```html
<p>內容</p>
```

-----

> **HTML 巢狀特性（Nested）**

為一層包著另一層的方式存在，具備父層與子層的關係。通常會因應網頁實作的需求，不斷的往下拓展很多子層。層次之間的關係我們可稱為**層次結構**。

```html
<body>  <!--<p> 父層 -->
  <p>我是 Body 標籤的子層</p> <!-- <body> 的子層-->
</body>
```

```html
<body>
  <div>
    <p>我是第三層元素</p>
    <span>我是第三層元素</span>
  </div>
</body>
```

-----

> **網頁基本架構 < html >、< head>、< body>**

一份正常的 HTML 網頁呈現的樣子如下：

```html
<html>
  <head>
<!--基本功能設置區，不會對使用者顯示-->
    <title>我是網頁標題</title>
  </head>
  <body>
<!-- 這裡放給使用者看的網頁內容-->
  </body>
</html>
```

< html > ：

HTML 網頁中一定有一個，也是**唯一一個** < html > 標籤 (tag)，

它是整個網頁最上（外）層的元素，網頁中所有的標籤元素都包含在 < html > 標籤內。

< body > ：

HTML 網頁中一定有一個，也是唯一一個 < body > 標籤 (tag)，用來呈現網頁的主要內容，**使用者將能看到這些資訊。**

< head > ：

HTML 網頁中一定有一個，也是唯一一個 < head >標籤 (tag)（如果超過一組以上，很可能會造成瀏覽器錯亂），< head >主要是放置網頁相關基本設置的地方，*內容 **不會** 顯示在網頁上讓使用者看到。*

例如：網頁的**主標（title）、網頁內容描述（description）**皆是放在 < head > 裡面 。

另外，<head> 是擺在 <html> 下層的第一個標籤，位置不要放錯囉！

-----

註解符號是由 <!--以及 -->所組成， 前後夾住註解內容：

```html
<!-- 註解文字只能在純 HTML 文件內裡看到，不顯示在瀏覽器的畫面上 -->
```

< em >斜體字 

```html
<h3><em>變成斜體字</em></h3>
```

< strong > 粗體字 

```html
<h3><strong>變成粗體字</strong></h3>
```

< mark > 文字突顯：

```html
<h3><mark>變成突顯字</mark></h3>
<mark style="background-color:#9cffd9;">更換顏色</mark>
```

-----

> **HTML 屬性 Attribute**

屬性是由 **「屬性名稱」、「屬性值」**所構成。常用的屬性之一是  **id 與 class**。 我們可以使用 id 或 class 屬性為不同的 html 標籤元素**命名或分類**。

添加 id 屬性將協助我們**識別內容**：

```html
<div id="introA" class="man">
  <h1>自我介紹-人物A</h1>
  <p>大家好，我是王小明，家住在嘉義，喜歡打籃球和講冷笑話。<p>
</div>

<div id="introB" class="man">
  <h1>自我介紹-人物B</h1>
  <p>大家好，我是林大熊，家住在高雄，喜歡打羽球和吃滷肉飯。<p>
</div>
```

```html
<body>
  <div>
    <h2 id="front-end" class="1">前端技術</h2>
    <h2>Vue</h2>
    <h3>React</h3>
    <h3>Angular</h3>
  </div>
  <div>
    <h2 id="bach-end" class="2">後端技術</h2>
    <h3>Laravel</h3>
    <h3>nodeJS</h3>
    <h3>Ruby on rails</h3>
  </div>
</body>
```

> **容器 < div > - 常用的容器標籤**

很常使用到的標籤元素，他可以**作為將網頁分成不同區塊(block)的「容器」**。

將某些特定的標籤元素們做**分組**時很有幫助。

可透過移動< div >，就能將**該區塊內的元素一併移動**。可以對< div >元素進行**整體性樣式設定**。

< div >內可以**包含任何文字或其他HTML標籤元素**，例如連結，圖像或影音。

```html
<!--將以下同樣類別的物品用div做區隔  -->
<body>
  <div class="h2">
    <h2>蘋果</h2>
    <h2>香蕉</h2>
    <h2>梨子</h2>
  </div>
  <div class="h3">
    <h3>機車</h3>
    <h3>汽車</h3>
    <h3>火車</h3>
    <h3>飛機</h3>
  </div>
</body>
```

> **< span > 行內容器**

span 主要是用作行內 (inline) 容器，如果是要包裹一個區塊 (block) 的情況，則是使用 div。

```html
<p>My mother has <span class="highlight">blue</span> eyes.</p>
```

只要在css裡設定hightlight是藍色就可以單字換色了。

-----

> **標題（Headings)** 

通常來說 < h1 > 在一個頁面只會出現一次，用於表示頁面的主標（例如新聞標題），其他標題則從 < h2 > 開始。

> 跟markdown很像

```html
<h1>最重要標題，通常一個頁面一個</h1>
<h2>標題二</h2>
<h3>標題三</h3>
<h4>標題四</h4>
<h5>標題五</h5>
<h6>最不重要的標題</h6>
```

> **有序列表、無序列表**

\無序列表< ul > 和 < li >

< ul > 標籤本身不具有任何效果，需要搭配 < li >才能將列表完整呈現， 兩者必須同時存在，列表才能在畫面上正常顯示。

```html
<ul>
  <li>電腦</li>
  <li>滑鼠</li>
  <li>鍵盤</li>
</ul>
```

\有序列表（ordered Lists）

將 < ul > 換成 < ol >。

```html
<ol>
  <li>電腦</li>
  <li>滑鼠</li>
  <li>鍵盤</li>
</ol>
```

> **插入圖片< img >**

**圖片< img >只有單一標籤**，且標籤內帶有兩個重要常用的預設屬性 **src 與 alt** ，他們分別決定了圖片連結位址與 圖片說明。

```html
<img src="圖片連結" alt="圖片說明" />
```

alt用以

\1.將鼠標懸停在該這張圖片上，閱讀 alt 設定好的圖片說明。

\2.軟體可以向視障用戶大聲讀取圖像內的描述。

\3.具有描述性意義的 alt 屬性可以提高網站在搜尋引擎系統裡的網站排名。

如果該圖片不具備任何資訊傳達用途（例如：只是拿來當背景用），留空反而好！

> **插入影片< video >**

**有前後**。用法與 <img> 類似，具備 src 屬性。透過 **width 和 height屬性設定瀏覽器中顯示的影音的面積**，而 **controls 屬性**將告訴瀏覽器顯示的介面等控制選項。

```html
<video src="影片位址(url)" width="320" height="240" controls>
  Video not supported(說明欄可空白)
</video>
```

> **插入外嵌網頁< iframe >**

用來在**一個 HTML 網頁裡面嵌入另外一個 HTML 網頁**，常見的用法為 iframe 語法嵌入 Facebook 的粉絲專頁或按讚分享按鈕 & youtube 影片。其實還有很多的屬性可以用，有興趣了解更多的可以上 [w3school](https://www.w3schools.com/tags/tag_iframe.asp) 

＊有些網頁會在系統設定不允許被嵌入

```html
<iframe src="網址"  width="頁面寬度"   height="頁面高度" >
</iframe>
```

```html
<iframe width="500" height="300" src="https://www.youtube.com/embed/sezDCcAu10E" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```html
<iframe src="https://www.facebook.com/plugins/like.php?href=https%3A%2F%2Fwww.facebook.com%2Fsakanafishowo&width=320&layout=standard&action=like&size=large&share=false&height=35&appId" width="320" height="35" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
```

[「讚」按鈕 - 社交外掛程式 (facebook.com)](https://developers.facebook.com/docs/plugins/like-button?locale=zh_TW#)

