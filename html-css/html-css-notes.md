#### HTML
```
<html>
    <head>
        <title>Test Page</title>
    </head>
    <body>
        <p>Hao Tan</p>
        <p>tanhao2013@me.com</p>
    </body>
</html>
```

```
    <h1></h1>
    <h2></h2>
    <!-- <br> 用于断句且不产生行间隔 -->
    <h3><br></h3>
    <p><br></p>
```

styles.css

```
p {
	font-family: Georgia, "Times New Roman", Times, serif;
	font-size: 1.2em;
}

h1 {
	font-family: "Trebuchet MS", Helvetica, serif;
	font-size: 2em;
}

.important{
	font-size: 2.5em;
}

.bigger{
	font-size: 3em;
}
```




index.html

```
   <html>
    <head>
        <title>Test Page ex1</title>
        <link rel="stylesheet" type="text/css" href="css/styles.css"></link>
    </head>
    <body>
        <p>Hao Tan</p>
        <h1>tanhao2013@me.com</h1>
        <p class="important">Hao Tan ... </p>
        <h1 class="bigger">tanhao2013@me.com .... </h1>
        <!-- 部分block -->
        <span>af;f;af</span>
    </body>
</html>
```

#### Block vs inline
Blocks: headings, paragraphs, lists, tables, divs.

*    block element不会有其他元素在旁,总是另起一行
*    side-by-side需要特别的样式,如`float`
*    a href不会另起一行
*    img是inline,可以设置为'display: block;'

```
    <img src="images/logo.png" alt="logo" width="50", height="20">
```


#### Links
```
    <!-- 外部网站跳转 -->
    <a href="http://www.stackoverflow.com">Stack Overflow</a>

    <!-- 内部网站跳转 -->
    <a href="catalog/product.html">Our products</a>
    
    <!-- 内部页面跳转 -->
    <div class="content" id="top">
        <a href="#top">Back to the top</a>
    <div>
    
    <a href="home.html#top">Back to the home top</a>
    
    <a href="http://www.stackoverflow.com/python.html#Class">Python class</a>
```

```
a {
	color: #b8860b;
}

a:hover {
	font-weight: bold;
	text-decoration: none;
}

a:active {
	font-size: 1.25em;
}

a:visited {
	color: deeppink;
}
```

#### opening a new window
```
 <p id="openWindow">Read more about this.</p>
 <script>    
     document.getElementById("openWindow").onclick=openWindow;
     function openWindow(){
         var w = window.open("more-info.html","","width=200,height=300,left=300,top=400;");
     }
 </script>
```


#### Lists
```
    <li></li>
    <ul></ul>
    <ol></ol>
```

```
ul {
	margin: 0 1.5em 0 1.5em;
}

ol {
	margin: 0 1.5em 0 1.5em;
}

li {
	margin: .75em;
}
```

#### css selectors

```
    <!-- 元素 -->
    p, div, img 
    <!-- 元素class -->
    p.special, div.important, img.gallery 
    <!-- class -->
    .special, .important, .gallery 
    <!-- 元素id -->
    p#intro, div#sidebar, img#logo
    <!-- id -->
    #intro, #sidebar, #logo  
```

```
/*
  div下important类的所有paragraphs
 */
div.important p {

}

/*
  ul下带pix-list的id的list下img
 */
ul#pix-list li img {

}

/*
  selects the first paragraph following any div
 */
div + p {

}

/*
 selects only the first level of divs within the div that has an id of "main"
 */
div#main > div {

}
```

#### tables

#### Forms

```
 <form action="sendEmail.html" method="post">
     Last Name: 
     <input type="text" name="surname" size="25" maxlength="40">
 </form>
 
 
 <h1>Testing forms</h1>
		<div id="form-1">
			<form action="sendEmail.html" method="post">
     			Last Name:
     			<br>
     			<input type="text" name="surname" size="25" maxlength="40">
     			<br>
     			Sex Choose:
     			<!-- lable 标签能让字段选择时鼠标直接点击字段即可 -->
     			<input type="radio" name="sex" value="Male" checked="checked">Male
     			<label>
					<input type="radio" name="sex" value="Female">Female
				</label>
				<br>
				Your foods:
				<input type="checkbox" name="foods" value="Fish" checked="checked">Fish
				<input type="checkbox" name="foods" value="Rice">Rice
				<br>
				Your country:
				<select name="country" id="country-select">
					<option value="CN">China</option>
					<option value="EN">English</option>
					<option value="FR">France</option>
				</select>
				<br>
     			Infomation:
     			<br>
     			<textarea name="infomation" cols="30" rows="5"></textarea>
     			<br>
     			<input type="submit" value="submit">
 			</form>
		</div>
```

```
px -> 绝对值;不能适应不同屏幕;images, borders, windows, iframes, fixed, absolute, relative positing; 
em -> typography, margins, padding
％ -> divs, tables, iframes, margins, padding
```

*    absolute and fixed position 
*    relative position
*    z-index

```
p.space-out {
    position: relative;
    top: 50px;
}

table#adjusted {
    position: relative;
    bottom: 25%;
    right: 35%;
}


div#additional-box {
    width: 20%;
    max-width:500px;
    min-width: 200px;
    max-height: 600px;
    min-height: 150px;
    overflow: scroll;
    /*
    overflow: hidden; 
     */
}
```