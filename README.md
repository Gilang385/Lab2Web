# Lab 2 Web: Praktikum Dasar CSS
Repositori ini berisi latihan dan tugas yang telah diselesaikan sebagai bagian dari Lab 2: CSS Dasar untuk mata kuliah Pemrograman Web di Universitas Pelita Bangsa. Praktikum ini mencakup dasar-dasar penggunaan CSS, seperti penerapan CSS internal, eksternal, dan inline, serta penggunaan selector, properti, dan nilai CSS.
## Tujuan
Tujuan dari praktikum ini adalah untuk memperkenalkan dasar-dasar CSS kepada mahasiswa. Dengan latihan ini, mahasiswa akan mempelajari cara menggunakan CSS secara internal, eksternal, dan inline, serta bagaimana memilih elemen HTML yang akan diubah tampilannya menggunakan berbagai jenis selector CSS.

## Langkah-langkah
## Langkah 1: Membuat Dokumen HTML
Langkah pertama adalah membuat struktur dasar HTML seperti berikut:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS DASAR</title>
    <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
<body>
    <header>
        <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>
    <nav>
        <a href="labs2_css_dasar.html">CSS Dasar</a>
        <a href="labs2_css_eksternal.html">CSS Eksternal</a>
        <a href="labs1_tag_dasar.html">HTML Dasar</a>
    </nav>
    <!-- CSS ID Selector -->
     <div id="intro">
        <h1>Hello World</h1>
        <p> Kami sedang belajar HTML dan CSS dasar, pada matakuliah <b>pemrograman web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p>
        <a class="button btn-primary" href="#intro">Informasi selengkapnya</a>
     </div>
</body>
    
</body>
</html>
```
## Langkah 2: Menambahkan CSS Internal
Selanjutnya, tambahkan CSSS internal di dalam tag `<head>`:

```css
    body {
        font-family: 'Open Sans', sans-serif;
    }
    header {
        min-height: 80px;
        border-bottom: 1px solid #77CCEF;
    }
    h1 {
        font-size: 24px;
        color: #0F189F;
        text-align: center;
    }
    h1 i {
        color: #6d6a6b;
    }
```

## Langkah 3: Menambahkan CSS Inline
CSS inline diterapkan langsung di elemen `<p>` :

```html
<p style="text-align: center; color: #ccd8e4;"
```

## Langkah 4: Menambahkan CSS Eksternal
Buat file eksternal `(assets/css/style.css)` dan hubungkan ke dokumen HTML:

```html
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
```
Isi dari `assets/css/style.css`:

```css
nav {
    background: #20A759;
    color: #fff;
    padding: 10px;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}
nav .active,
nav a:hover {
    background: #0B6B3A;
}

```

## Langkah 5: Menggunakan Selector CSS
Gunakan selector CSS seperti ID dan class:

```css

#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}
#intro h1{
    text-align: left;
    border: 0;
    color: #fff;
}
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display:inline-block
    margin 10px;
    text-decoration: nonne;
}

.btn-primary {
    background: #E42A42;

}
```

# TAMPILAN WEBNYA
## 1. Tampilan Sebelum CSS Diterapkan:

- Tangkapan layar ini menunjukkan tampilan dasar halaman HTML sebelum ada gaya CSS yang diterapkan.

![Gambar WhatsApp 2024-10-07 pukul 14 59 54_0adb96b7](https://github.com/user-attachments/assets/5184cc60-26b3-4751-8324-725ae1227d86)

##   2. Tampilan Setelah CSS Diterapkan:
- Tangkapan layar ini menunjukkan perubahan tampilan setelah CSS internal dan inline diterapkan, seperti perubahan warna teks dan tata letak.
![Gambar WhatsApp 2024-10-07 pukul 15 06 15_3986d7c8](https://github.com/user-attachments/assets/bcd6932d-d989-4412-9e71-635f3aeef525)

##    3. Tampilan Setelah CSS Eksternal Diterapkan:
- Di tangkapan layar ini, file CSS eksternal telah diterapkan, sehingga gaya pada navigasi dan elemen lainnya menjadi lebih terstruktur.
![Gambar WhatsApp 2024-10-07 pukul 15 16 49_463e7ae0](https://github.com/user-attachments/assets/938be3d8-3734-4ae9-bea1-436b26bc736c)

## 4. Tampilan Final Setelah Semua CSS Diterapkan:

- Ini adalah hasil akhir setelah semua jenis CSS (internal, inline, dan eksternal) diterapkan, termasuk penggunaan selector ID, class, dan elemen.
![Gambar WhatsApp 2024-10-07 pukul 15 34 59_fb05fdcb](https://github.com/user-attachments/assets/8465d091-fde8-4058-a2b7-6e3b25d006ce)

![Gambar WhatsApp 2024-10-07 pukul 15 40 40_98cbc099](https://github.com/user-attachments/assets/de0aa89e-69f4-44ba-b998-17ab863c9465)

## Hasil Eksperimen
## 1. Perbedaan Selector Elemen (`h1 {...}`) vs. Selector ID (`#intro h1 {...}`):

- Selector elemen menerapkan gaya ke semua elemen `<h1>`, sedangkan selector ID hanya akan mempengaruhi elemen `<h1>` di dalam elemen dengan ID `#intro`.
## 2. Urutan Prioritas CSS Internal, Eksternal, dan Inline:

- Jika ketiga jenis CSS ini diterapkan pada elemen yang sama, inline CSS memiliki prioritas tertinggi, diikuti CSS eksternal, dan terakhir CSS internal. Misalnya:
```html
<h1 style="color: red;">Judul ini akan berwarna merah karena CSS inline.</h1>
```
## 3. Prioritas Selector ID dan Class:
- Selector ID memiliki prioritas lebih tinggi dibandingkan selector class, karena ID lebih spesifik.
```html
<p id="paragraf-1" class="text-paragraf">Gaya teks akan mengikuti selector ID.</p>
```

## Kesimpulan
Praktikum ini memberikan pengalaman dalam menggunakan berbagai metode deklarasi CSS dan menunjukkan bagaimana aturan CSS diterapkan dengan berbagai selector dan urutan prioritasnya.


