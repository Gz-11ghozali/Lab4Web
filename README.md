# Lab4Web
### Langkah-Langkah Praktikum Membuat Layout Sederhana:

#### 1. **Membuat Dokumen HTML**
Buat file HTML bernama `lab4_box.html` dengan kode berikut:
```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>Box Element</title>
</head>
<body>
   <header>
      <h1>Box Element</h1>
   </header>
</body>
</html>
```

#### 2. **Membuat Box Element**
Tambahkan box element di dalam `section` menggunakan tag `<div>`.
```html
<section>
   <div class="div1">Div 1</div>
   <div class="div2">Div 2</div>
   <div class="div3">Div 3</div>
</section>
```

#### 3. **CSS Float Property**
Tambahkan deklarasi CSS di bagian `<head>` untuk membuat float element.
```html
<style>
div {
   float: left;
   padding: 10px;
}
.div1 {
   background: red;
}
.div2 {
   background: yellow;
}
.div3 {
   background: green;
}
</style>
```
![Screenshot 2024-10-21 071438](https://github.com/user-attachments/assets/99fb3fb4-df9b-4391-8689-450a416eb7b6)

#### 4. **Clearfix Element**
Tambahkan elemen div baru dan atur properti `clear`.
```html
<section>
   <div class="div1">Div 1</div>
   <div class="div2">Div 2</div>
   <div class="div3">Div 3</div>
   <div class="div4">Div 4</div>
</section>
```

CSS untuk `div4`:
```css
.div4 {
   background-color: blue;
   clear: left;
   float: none;
}
```
![Screenshot 2024-10-21 072013](https://github.com/user-attachments/assets/4e11b1d8-1c92-4b08-9079-b0394db165fc)

#### 5. **Membuat Layout Sederhana**
Buat folder baru bernama `lab4_layout`, kemudian buat file `home.html` dengan struktur layout sebagai berikut:
```html
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>Layout Sederhana</title>
   <link rel="stylesheet" href="style.css">
</head>
<body>
   <div id="container">
      <header>
         <h1>Layout Sederhana</h1>
      </header>
      <nav>
         <a href="home.html" class="active">Home</a>
         <a href="artikel.html">Artikel</a>
         <a href="about.html">About</a>
         <a href="kontak.html">Kontak</a>
      </nav>
      <section id="hero">
         <h1>Hello World!</h1>
         <p>Lorem ipsum dolor sit amet...</p>
         <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
      </section>
      <section id="wrapper">
         <section id="main">
         </section>
         <aside id="sidebar">
         </aside>
      </section>
      <footer>
         <p>&copy; 2021 - Universitas Pelita Bangsa</p>
      </footer>
   </div>
</body>
</html>
```
![Screenshot 2024-10-21 073745](https://github.com/user-attachments/assets/45ef8a4d-f515-4129-85a7-dce002da0d24)

#### 6. **CSS Layout Sederhana**
Tambahkan file `style.css` dengan kode berikut:

##### a. **Google Fonts & Reset CSS** (Ini setelah langkah 7, sesuai dengan instruksi Anda):
```css
/* import google font */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
   margin: 0;
   padding: 0;
}
```

##### b. **CSS untuk Body dan Container**:
```css
body {
   line-height: 1;
   font-size: 100%;
   font-family: 'Open Sans', sans-serif;
   color: #5a5a5a;
}

#container {
   width: 980px;
   margin: 0 auto;
   box-shadow: 0 0 1em #cccccc;
}
```

##### c. **CSS untuk Header dan Navigasi**:
```css
/* header */
header {
   padding: 20px;
}

header h1 {
   margin: 20px 10px;
   color: #b5b5b5;
}
/* navigasi */
nav {
   display: block;
   background-color: #1f5faa;
}

nav a {
   padding: 15px 30px;
   display: inline-block;
   color: #ffffff;
   font-size: 14px;
   text-decoration: none;
   font-weight: bold;
}

nav a.active,
nav a:hover {
   background-color: #2b83ea;
}
```
![Screenshot 2024-10-21 074344](https://github.com/user-attachments/assets/fd8b303e-5b91-4352-b2d3-5d6fb0244c22)

![Screenshot 2024-10-21 074457](https://github.com/user-attachments/assets/c6b2d599-56b3-452f-8db4-28413cdb72b7)

##### d. **CSS untuk Hero Panel**:
```css
/* Hero Panel */
#hero {
   background-color: #e4e4e5;
   padding: 50px 20px;
   margin-bottom: 20px;
}

#hero h1 {
   margin-bottom: 20px;
   font-size: 35px;
}

#hero p {
   margin-bottom: 20px;
   font-size: 18px;
   line-height: 25px;
}
```
![Screenshot 2024-10-21 074630](https://github.com/user-attachments/assets/488a8dd5-5a6c-44ba-85e7-d715bae34e83)

##### e. **CSS untuk Main Content dan Sidebar**:
```css
/* main content */
#wrapper {
   margin: 0;
}

#main {
   float: left;
   width: 640px;
   padding: 20px;
}

/* sidebar area */
#sidebar {
   float: left;
   width: 260px;
   padding: 20px;
}
```

##### f. **CSS untuk Sidebar Widget**:
```css
/* widget */
.widget-box {
   border: 1px solid #eee;
   margin-bottom: 20px;
}

.widget-box .title {
   padding: 10px 16px;
   background-color: #428bca;
   color: #fff;
}

.widget-box ul {
   list-style-type: none;
}

.widget-box li {
   border-bottom: 1px solid #eee;
}

.widget-box li a {
   padding: 10px 16px;
   color: #333;
   display: block;
   text-decoration: none;
}

.widget-box li:hover a {
   background-color: #eee;
}

.widget-box p {
   padding: 15px;
   line-height: 25px;
}
```
![Screenshot 2024-10-21 075041](https://github.com/user-attachments/assets/314e1b3a-4cff-49a7-8cbe-f3d7a22ca4a1)

##### g. **CSS untuk Footer**:
```css
/* footer */
footer {
   clear: both;
   background-color: #1d1d1d;
   padding: 20px;
   color: #eee;
}
```
![Screenshot 2024-10-21 075148](https://github.com/user-attachments/assets/248d651b-b35a-410b-804a-db5ad0a9e40b)

##### h. **CSS untuk Box Element dalam Main Content**:
```css
/* box */
.box {
   display: block;
   float: left;
   width: 33.333333%;
   padding: 0 10px;
   text-align: center;
}

.box h3 {
   margin: 15px 0;
}

.box p {
   line-height: 20px;
   font-size: 14px;
   margin-bottom: 15px;
}

.image-circle {
   border-radius: 50%;
}
```
#### **Menambahkan Section Main dengan Box dan Artikel**
Berikut adalah tambahan kode HTML yang diminta, di dalam `section id="main"` pada file `home.html`:

```html
<section id="main">
   <div class="row">
      <div class="box">
         <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
         <h3>Heading</h3>
         <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
         <a href="#" class="btn btn-default">View detail</a>
      </div>
      <div class="box">
         <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
         <h3>Heading</h3>
         <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
         <a href="#" class="btn btn-default">View detail</a>
      </div>
      <div class="box">
         <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
         <h3>Heading</h3>
         <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
         <a href="#" class="btn btn-default">View detail</a>
      </div>
   </div>

   <hr class="divider" />

   <article class="entry">
      <h2>First featurette heading.</h2>
      <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
   </article>

   <hr class="divider" />

   <article class="entry">
      <h2>First featurette heading.</h2>
      <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
   </article>
</section>
```

#### **CSS untuk Box dan Artikel**
Berikut adalah kode CSS untuk melengkapi tampilan box dan artikel tersebut:

```css
/* box */
.box {
   display: block;
   float: left;
   width: 33.333333%;
   box-sizing: border-box;
   -moz-box-sizing: border-box;
   -webkit-box-sizing: border-box;
   padding: 0 10px;
   text-align: center;
}

.box h3 {
   margin: 15px 0;
}

.box p {
   line-height: 20px;
   font-size: 14px;
   margin-bottom: 15px;
}

.box img {
   border: 0;
   vertical-align: middle;
}

.image-circle {
   border-radius: 50%;
}

/* row layout */
.row {
   margin: 0 -10px;
   box-sizing: border-box;
   -moz-box-sizing: border-box;
   -webkit-box-sizing: border-box;
}

.row:after, .row:before,
.entry:after, .entry:before {
   content: '';
   display: table;
}

.row:after,
.entry:after {
   clear: both;
}

/* divider */
.divider {
   border: 0;
   border-top: 1px solid #eeeeee;
   margin: 40px 0;
}

/* entry */
.entry {
   margin: 15px 0;
}

.entry h2 {
   margin-bottom: 20px;
}

.entry p {
   line-height: 25px;
}

.entry img {
   float: left;
   border-radius: 5px;
   margin-right: 15px;
}

.entry .right-img {
   float: right;
}
```
![Screenshot 2024-10-21 075950](https://github.com/user-attachments/assets/1f9b1538-a075-4ca8-8a7a-c463083ac3a4)
![Screenshot 2024-10-21 080459](https://github.com/user-attachments/assets/7fbd9ef3-b5b5-4520-8e32-8776b65d02f6)
