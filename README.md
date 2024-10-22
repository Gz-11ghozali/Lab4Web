# Lab4Web
### Penjelasan Langkah-Langkah Praktikum:

#### 1. **Membuat Dokumen HTML Dasar:**
   - **Langkah pertama** adalah membuat file HTML bernama `lab4_box.html`. File ini merupakan struktur HTML dasar untuk menampung elemen-elemen kotak (box) yang akan kita buat. Struktur ini dimulai dengan tag `<!DOCTYPE html>`, dan kemudian di dalamnya terdapat elemen-elemen HTML seperti `<html>`, `<head>`, dan `<body>`.
   - Di dalam tag `<head>`, Anda mendefinisikan meta tag untuk karakter encoding (UTF-8) dan tag judul (`<title>`) dengan judul "Box Element".
   
   **Contoh Kode:**
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

#### 2. **Membuat Box Element dengan Tag `<div>`:**
   - **Langkah kedua** adalah menambahkan elemen-elemen kotak menggunakan tag `<div>` di dalam tag `<section>`. Setiap div memiliki class tersendiri (`div1`, `div2`, `div3`), yang nantinya akan diatur menggunakan CSS.

   **Contoh Kode:**
   ```html
   <section>
     <div class="div1">Div 1</div>
     <div class="div2">Div 2</div>
     <div class="div3">Div 3</div>
   </section>
   ```

#### 3. **Menambahkan Properti CSS Float:**
   - **Langkah ketiga**, tambahkan kode CSS untuk membuat setiap elemen `div` mengapung (float) ke kiri. Ini membuat elemen-elemen kotak tersebut berada dalam satu baris secara horizontal. Selain itu, padding (jarak di dalam elemen) ditambahkan untuk membuat konten terlihat lebih baik.
   - Background untuk masing-masing div juga diberi warna berbeda (merah, kuning, hijau).

   **Contoh Kode CSS:**
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

#### 4. **Mengatur Clearfix Element:**
   - **Langkah keempat**, tambahkan elemen `div` keempat (`div4`) dan tambahkan properti `clear` pada CSS untuk mengatur tampilan setelah elemen `float`. Dengan `clear: left`, div keempat akan dipaksa berada di bawah elemen-elemen sebelumnya, tidak berada dalam baris yang sama.
   
   **Contoh Kode:**
   ```html
   <div class="div4">Div 4</div>
   ```

   **CSS untuk div4:**
   ```css
   .div4 {
     background-color: blue;
     clear: left;
     float: none;
   }
   ```

#### 5. **Eksperimen Clear:**
   - **Eksperimen** dilakukan dengan mengubah nilai properti `clear` menjadi `left`, `right`, atau `both`, untuk melihat perubahan posisi elemen setelah elemen-elemen float.

#### 6. **Membuat Layout Sederhana:**
   - **Langkah keenam**, buat folder baru bernama `lab4_layout` dan file HTML bernama `home.html` dengan kerangka layout yang lebih kompleks. Kerangka layout terdiri dari elemen-elemen HTML seperti header, navigasi, section, aside (sidebar), dan footer.
   
   **Contoh Struktur Layout:**
   ```html
   <header>
     <h1>Layout Sederhana</h1>
   </header>
   <nav>
     <a href="home.html" class="active">Home</a>
     <a href="artikel.html">Artikel</a>
     <a href="about.html">About</a>
     <a href="kontak.html">Kontak</a>
   </nav>
   <section id="hero"></section>
   <section id="wrapper">
     <section id="main"></section>
     <aside id="sidebar"></aside>
   </section>
   <footer>
     <p>&copy; 2021 - Universitas Pelita Bangsa</p>
   </footer>
   ```

#### 7. **Menambahkan CSS untuk Layout:**
   - Setelah menyiapkan struktur layout, tambahkan CSS untuk styling, seperti pengaturan font, margin, padding, lebar container, tampilan navigasi, panel hero, serta main content dan sidebar.
   
   **Contoh CSS Navigasi:**
   ```css
   nav {
     background-color: #1f5faa;
   }
   nav a {
     padding: 15px 30px;
     color: #ffffff;
     text-decoration: none;
   }
   nav a.active,
   nav a:hover {
     background-color: #2b83ea;
   }
   ```

#### 8. **Mengatur Hero Panel:**
   - **Langkah berikutnya** adalah menambahkan panel hero yang mencakup teks dan tombol "Learn more" dengan styling yang rapi. Elemen ini dibuat menggunakan section dengan ID `hero` yang diatur padding dan margin-nya.

   **CSS Hero Panel:**
   ```css
   #hero {
     background-color: #e4e4e5;
     padding: 50px 20px;
   }
   ```

#### 9. **Mengatur Main Content dan Sidebar:**
   - Menggunakan float CSS untuk membuat main content dan sidebar berada berdampingan. Main content memiliki lebar lebih besar dibanding sidebar.

   **Contoh CSS Main dan Sidebar:**
   ```css
   #main {
     float: left;
     width: 640px;
   }
   #sidebar {
     float: left;
     width: 260px;
   }
   ```

#### 10. **Menambahkan Sidebar Widget:**
   - Tambahkan elemen widget di sidebar dengan list item dan teks pendukung. Setiap widget diatur dengan border dan padding yang memberikan batas visual yang jelas.

#### 11. **Menambahkan Footer:**
   - Footer ditambahkan dengan properti `clear: both` untuk memastikan tampil di bawah semua elemen lain yang mengapung.

#### 12. **Menambahkan Konten Artikel:**
   - Di dalam main content, tambahkan artikel dengan gambar dan teks. Gambar diatur menggunakan float untuk ditempatkan di kiri atau kanan teks.

   **Contoh CSS Artikel:**
   ```css
   .entry img {
     float: left;
     margin-right: 15px;
   }
   .entry .right-img {
     float: right;
   }
   ```
