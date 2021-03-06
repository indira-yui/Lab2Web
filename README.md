# Lab2Web

| INDIRA ALINE    |   312010042   |
|-----------------|---------------|
|   TI. 20 A. 1   |PEMROGRAMAN WEB|
|     HTML        |    CSS        |

### Pertemuan 3
Untuk mata kuliah kali ini membahas tentang membuat website dengan HTML dan CSS Dasar seperti CSS ***inline***, ***internal***,dan juga ***eksternal*** serta selector **ID** dan juga **Class**

## 1). Membuat Dokumen Dasar HTML
### Output 
![menambahkan_dokumen_dasar_html](img/dokumen_html.png)
Disini terdapat sebuah dokumen dasar HTML namun belum beserta CSS atau hanya masih file HTML dasarnya saja, belum diberi CSS ***inline*** **internal** ataupun **eksternal**

### Contoh coding
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>
    <header>
        <h1>CSS internal dan <i>inline CSS</i></h1>
    </header>
    <nav>
        <a href="lab2_css_dasar.html">CSS Dasar</a>
        <a href="lab2_css_eksternal.html">CSS Eksternal</a>
        <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>
    <!-- CSS ID Selector -->
    <div id="main">
        <h1>Hello World</h1>
        <p>Kami sedang belajar HTML dan CSS Dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p>
    </div>
</body>
</html>
```

## 2). Mendeklarasikan CSS Internal
### Output
![menambahkan_CSS_Internal](img/css_internal.png)
CSS Internal adalah CSS yang filenya terdapat didalam HTML dengan deklarasi **style**, gambar diatas adalah hanya CSS Internal saja belum terdapat inline dan eksternal.

### Contoh coding
```css
<!-- Mendeklarasikan CSS Internal -->
    <style>
        body{
            font-family: 'Times New Roman', Times, serif;
        }
        header{
            min-height: 90px;
            border-bottom: 1px solid black;
        }
        h1{
            font-size: 25px;
            color: blue;
            text-align: center;
            padding: 20px 10px;
        }
        h1 i{
            color: aqua;
        }
    </style>
```

## 3). Menambahkan Inline
### Output
![menambahkan_Inline_CSS](img/css_inline.png)
 CSS ***Inline*** adalah CSS yang pendeklarasiannya ada pada tag HTML nya sendiri dengan menggunakan **style** seperti contoh di atas, saya melakukan mendeklarasikan CSS ***Inline*** pasar pada tag (p) dengan properti (text-align) dan juga (color) CSS ***Inline*** sendiri sangat spesifik dan hanya merubah pada tag yang hanya diberi **style** CC ***Internal*** sangat kuat, maksudnya yaitu jika kita melakukan code yang sama dengan deklarasi yang berbeda yang terpanggil hanya ***Inline*** karena ***Inline*** memiliki prioritas tinggi dibanding **internal** dan **eksternal**.

 ### Contoh coding
 ```html
 <!-- Tag (p) menggunakan CSS Inline -->
        <p style="text-align: center; color: royalblue;">Kami sedang belajar HTML dan CSS Dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p>
 ```

 ## 4). Membuat CSS Eksternal
 ### Output
 ![menambahkan_CSS_Eksternal](img/eksternal_css.png)
 CSS **Eksternal** adalah CSS yang  file terpisah dengan HTML melalui link penempatannya, CSS **Eksternal** sangat direkomendasikan oleh para programmer website developer dalam membuat gaya pada CSS, karena 1 file CSS **Eksternal** bisa untuk banyak file HTML, karena itu direkomendasikan banyak programmer kelebihan dari CSS **Eksternal** di (a:hover) saya sedikit menambahkan (border-radius: 4px;) agar terlihat menarik.

 ### Contoh coding
 ```css
 nav{
    background: gray;
    color: azure;
    padding: 15px;
}
nav a{
    color: azure;
    text-decoration: none;
    padding: 15px 20px;
}
nav .active,
nav a:hover{
    background: black;
    border-radius: 4px;
}
 ```

 ## 5). Menambahkan CSS Selector
### Output
![menambahkan_CSS_Selector](img/css_selector.png)
CSS Selector adalah sebuah pendeklarasian untuk menambahkan gaya pada elemen HTML seperti selector **(p)** **(h1)** dll. Ada juga selector ID yang pendeklarasiannya dalam file CSS yaitu **(#)** kemudian definisikan properti CSS dalam kurung seperti contoh **#nav** itu adalah contoh pendeklarasiannya yang artinya **nav** akan diberi tampilan CSS.
Selain itu ada juga selector **class** sama seperti **ID** **Class** juga dapat sebagai mana yang akan diberi gaya pada CSS namun yang membedakannya yaitu pendeklarasiannya jika **ID** itu **(#)** maka **class** **(.)** atau titik seperti contoh di file CSSnya **.main** yang diberi class akan di ubah.

### Contoh coding
```css
/* ID Selector */
#main{
    background: azure;
    border: 1px solid black;
    min-height: 100px;
    padding: 10px;
}
#main h1{
    text-align: left;
    border: 0px;
    color: azure;
}
/* Class Selector */
.button{
    padding: 15px 20px;
    background: gray;
    color: azure;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
    border-radius: 4px;
}
.btn-primary{
    background: gray;
}
```

## Pertanyaan dan Jawaban
### 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
**Jawaban**
![jawaban_no.1](img/jawaban1.png)

----------------------------------------------------------------------------------------------------------

### 2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
**Jawaban**
Jadi jika hanya mendeklarasikan elemen **{h1}** saja brarti semua elemen **{h1}** akan berubah oleh CSS, sedangkan mendeklarasikan **(#intro h1)** hanya elemen h1 dengan deklarasi **(#intro h1)** saja yang berubah karena **ID** itu unik.

-----------------------------------------------------------------------------------------------------------------

### 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
**Jawaban**
![jawaban_no3](img/no3.png)
Jika di deklarasikan secara bersama,antara **INTERNAL** **INLINE** dan **EKSTERNAL** yang terpanggil di browser adalah CSS **INLINE** karena **INLINE** memiliki prioritas terkuat dibanding CSS **INTERNAL** dan **EKSTERNAL** foto di atas adalah contoh pendeklarasian secara bersama antara **INTERNAL** **INLINE** dan **EKSTERNAL** untuk css **INLINE** memiliki property {color:rgb}  dan juga property {text-align;center} sedangkan CSS **INTERNAL** memiliki property {color: chocolate} dan {text-align:left} dan **EKSTERNAL** adalah {color:tomato} dan {text-align:justify} namun yang terpanggil adalah css **INLINE** dengan Property {color:rgb} dan {text-align:center}.
![jawaban_no3](img/jawaban3.png)
Contoh di atas adalah file css **EKSTERNAL** nya!

### 4). Pada sebuah elemen HTML terdapat **ID** dan **CLASS** , apabila masing-masing selector tersebut terdapat deklarasi CSS , maka deklarasi manakah yang ditampilkan pada browser? berikan penjelasan dan contoh nya!
**JAWABAN**
![jawaban_no4](img/jawaban4.png)
 antara **ID** dan **CLASS** yang terpanggil dibrowser adalah **ID** yang memiliki property {color:chocolate) dan {text-align:left} karena **ID** itu unik dibanding **CLASS** yang banyak dapat digunakan sedangkan **ID** hanya tertentu dan bersifat unik.
