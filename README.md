Lab3Web - Praktikum 3: CSS Dasar

Repositori ini memuat hasil pengerjaan Praktikum 3: CSS Dasar untuk mata kuliah Pemrograman Web. Praktikum ini bertujuan untuk memahami konsep dasar CSS, aturan penulisan (Internal, Inline, dan Eksternal), serta penggunaan CSS Selector (ID dan Class).

Data Mahasiswa

Nama : Satrio Erlangga

NIM : 312510006

Kelas : I253C

Program Studi : Teknik Informatika

Instansi : Universitas Pelita Bangsa

Langkah-Langkah Praktikum dan Hasil Tampilan Web

1. Membuat Dokumen HTML

Pembuatan struktur dasar dokumen HTML sebelum diberikan gaya atau format CSS apapun.

Salinan Kode (lab2_css_dasar.html):

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>
    <header>
        <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>
    
    <nav>
        <a href="lab2_css_dasar.html">CSS Dasar</a>
        <a href="lab2_css_eksternal.html">CSS Eksternal</a>
        <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>

    <div id="intro">
        <h1>Hello World</h1>
        <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah
        <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama
        yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal
        tag-tag dasar HTML dan CSS.</p>
        
        <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
    </div>
</body>
</html>


Hasil Tampilan Web Browser:
<img width="602" height="159" alt="Cuplikan layar 2026-10-11 074335" src="https://github.com/user-attachments/assets/b890eda4-4910-4ed1-b7b0-61ee4fd31da7" />


2. Mendeklarasikan CSS Internal

Menambahkan aturan CSS secara internal menggunakan tag <style> pada bagian <head> untuk mengatur jenis font (font-family), border, dan pewarnaan elemen heading.

Salinan Kode Tambahan pada <head>:

<style>
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
        padding: 20px 10px;
    }
    h1 i {
        color: #6d6a6b;
    }
</style>


Hasil Tampilan Web Browser:
<img width="670" height="170" alt="Cuplikan layar 2026-10-11 074808" src="https://github.com/user-attachments/assets/0011aa34-99f7-4476-8a0d-57ee0cd30e3a" />


3. Menambahkan Inline CSS

Menyisipkan atribut style secara langsung di dalam tag paragraf <p> untuk mengubah teks menjadi rata tengah dan mengubah warnanya.

Salinan Kode Perubahan pada tag <p>:

<p style="text-align: center; color: #ccd8e4;">
    Kami sedang belajar HTML dan CSS dasar, pada mata kuliah
    <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama
    yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal
    tag-tag dasar HTML dan CSS.
</p>


Hasil Tampilan Web Browser:
<img width="828" height="171" alt="Cuplikan layar 2026-10-11 074848" src="https://github.com/user-attachments/assets/738e7e54-8434-4870-bb42-ee6522b423bd" />


4. Membuat CSS Eksternal

Memisahkan kode CSS ke dalam file baru bernama style_eksternal.css khusus untuk mengatur tampilan navigasi, dan memanggil file tersebut ke dalam dokumen HTML menggunakan tag <link>.

Salinan Kode (style_eksternal.css):

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


Salinan Pemanggilan CSS di <head> (lab2_css_dasar.html):

<!-- menyisipkan css eksternal -->
<link rel="stylesheet" href="style_eksternal.css" type="text/css">


Hasil Tampilan Web Browser:
<img width="957" height="116" alt="Cuplikan layar 2026-10-11 075032" src="https://github.com/user-attachments/assets/fa05550c-a8ff-4e56-b6aa-fbac9a9b6020" />


5. Menambahkan CSS Selector

Menerapkan ID Selector (#intro) untuk mendesain kontainer utama dan Class Selector (.button, .btn-primary) untuk membuat tata letak tombol pada file CSS eksternal.

Salinan Kode Tambahan (style_eksternal.css):

/* ID Selector */
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}
#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}

/* Class Selector */
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}
.btn-primary {
    background: #E42A42;
}


Hasil Tampilan Web Browser:
<img width="959" height="152" alt="Cuplikan layar 2026-10-11 075239" src="https://github.com/user-attachments/assets/016702ef-e6eb-4d3c-8f98-c1d559f9dd61" />


## Eksperimen dan Jawaban Pertanyaan dan Tugas Modul
Halaman eksperimen.html dirancang secara khusus untuk membuktikan dan mendemonstrasikan secara visual jawaban atas pertanyaan dan tugas pada halaman 8 modul praktikum.

Screenshot Hasil Halaman Eksperimen & Pembuktian Soal:
<img width="524" height="437" alt="Cuplikan layar 2026-10-11 080544" src="https://github.com/user-attachments/assets/14901c80-d4e9-46dd-b5f0-35d75b5aff25" />


1. Eksperimen Properti CSS (Berdasarkan CSS Cheat Sheet)
Telah dilakukan eksperimen dengan memodifikasi beberapa properti dan nilai pada kode CSS yang ada di file style_eksternal.css. Penambahan properti yang dilakukan meliputi line-height, letter-spacing, border-radius, dan efek box-shadow.

Kode Awal: #intro { background: #418fb1; border: 1px solid #099249; min-height: 100px; padding: 10px; }

Kode Modifikasi: #intro { background-color: #2c3e50; border: 2px dashed #e74c3c; min-height: 150px; padding: 20px; border-radius: 12px; box-shadow: 4px 4px 10px rgba(0,0,0,0.5); }

Hasil: Elemen kotak berubah tampilan menjadi lebih modern dengan sudut yang melengkung/tumpul (efek radius), garis tepi putus-putus berwarna merah, serta penambahan efek bayangan 3D di belakang kotak (Hasil visual eksperimen ini dilampirkan pada halaman Eksperimen & Tugas Praktikum 3).

2. Perbedaan Selektor h1 {...} dengan #intro h1 {...}

h1 {...} (Element Selector): Deklarasi ini bersifat umum/global. Aturan gaya (style) CSS yang ditulis pada blok ini akan diterapkan secara otomatis pada seluruh tag judul <h1> yang ada di dalam keseluruhan dokumen HTML tanpa memedulikan letaknya.

#intro h1 {...} (Descendant Selector): Deklarasi ini bersifat spesifik. Aturan CSS ini hanya akan memengaruhi dan diterapkan khusus pada tag <h1> yang letaknya berada di dalam/terbungkus oleh elemen ber-ID "intro" (id="intro"). Tag <h1> yang posisinya berada di luar elemen ID tersebut tidak akan berubah.

3. Prioritas Tampilan: CSS Internal, Eksternal, dan Inline
Apabila sebuah elemen HTML yang sama diberikan aturan desain melalui CSS Internal, CSS Eksternal, dan Inline CSS secara bersamaan, maka deklarasi yang akan menang dan ditampilkan pada browser adalah Inline CSS.

Penjelasan: CSS memiliki sistem hierarki spesifisitas (Cascading) yang menilai seberapa dekat sebuah kode desain dengan tag HTML-nya. Inline CSS ditulis langsung menempel di dalam tag HTML sebagai atribut (contoh: <p style="...">), sehingga ia memiliki bobot prioritas tertinggi yang akan secara otomatis menimpa (override) aturan yang berasal dari Internal CSS (tag <style>) maupun Eksternal CSS (file .css).

Contoh Kasus: Di CSS Eksternal dan Internal paragraf diatur berwarna merah. Namun di dokumen HTML ditulis <p style="color: blue;">. Maka saat dijalankan, paragraf tersebut akan berwarna biru.

4. Prioritas Selektor: ID dan Class pada Elemen HTML yang Sama
Apabila sebuah elemen HTML memiliki atribut ID dan Class sekaligus (contoh: <p id="paragraf-1" class="text-paragraf">), dan keduanya memiliki aturan deklarasi CSS yang berbeda, maka deklarasi yang akan ditampilkan pada browser adalah milik ID Selector.

Penjelasan: Dalam perhitungan bobot spesifisitas CSS (Specificity), ID Selector memiliki poin yang jauh lebih tinggi dan lebih kuat dibandingkan Class Selector. Sebuah elemen HTML hanya diizinkan memiliki satu ID yang unik, sehingga aturan ID lebih diutamakan oleh browser dibandingkan Class yang dapat digunakan berulang kali.

Contoh Kasus: Di CSS terdapat deklarasi .text-paragraf { color: green; } dan #paragraf-1 { color: red; }. Ketika elemen tersebut dirender, maka teks akan berwarna merah karena warna merah merupakan instruksi dari ID yang mengalahkan instruksi warna hijau dari Class.
