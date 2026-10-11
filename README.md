# Lab3Web - Praktikum 3: CSS Dasar

<div align="center">
  <p>Repositori ini memuat hasil pengerjaan <b>Praktikum 3: CSS Dasar</b> untuk mata kuliah Pemrograman Web.</p>
  <p>Fokus utama praktikum ini adalah memahami konsep Cascading Style Sheets (CSS), aturan penulisan (Internal, Inline, dan Eksternal), serta hierarki spesifisitas penggunaan CSS Selector (ID dan Class).</p>
</div>

<hr>

##  Data Mahasiswa

> **Nama** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Satrio Erlangga  
> **NIM** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: 312510006  
> **Kelas** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: I253C  
> **Program Studi**: Teknik Informatika  
> **Instansi** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Universitas Pelita Bangsa  
> **Mata Kuliah** &nbsp;&nbsp;: Pemrograman Web  
> **Dosen** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Agung Nugroho, S.Kom., M.Kom.

<hr>

##  Langkah-Langkah Praktikum

### 1. Membuat Dokumen HTML Dasar
Pembuatan struktur dasar HTML (*file* `lab2_css_dasar.html`) tanpa menggunakan format CSS apa pun.

**Salinan Kode (`lab2_css_dasar.html`):**
```html
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
```
Screenshot hasil langkah 1:
<img width="959" height="152" alt="Cuplikan layar 2026-10-11 075239" src="https://github.com/user-attachments/assets/70b57ee3-88cc-4f40-ba66-471beb57bba4" />

2. Mendeklarasikan CSS Internal
Menambahkan tag <style> pada bagian <head> untuk mengatur jenis font dasar, garis batas (border), dan warna teks judul.

Tambahan Kode pada <head>:
```<style>
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
```
Screenshot hasil langkah 2:
<img width="959" height="152" alt="Cuplikan layar 2026-10-11 075239" src="https://github.com/user-attachments/assets/81ef6aea-7bb5-4e60-a1b7-d767bf3aa11a" />

3. Menambahkan Inline CSS
Menyisipkan atribut style langsung pada tag paragraf <p> untuk memodifikasi warna dan perataan teks (rata tengah).

Modifikasi Tag <p>:
```
<p style="text-align: center; color: #ccd8e4;">
    Kami sedang belajar HTML dan CSS dasar...
</p>
```
Screenshot hasil langkah 3:
<img width="959" height="152" alt="Cuplikan layar 2026-10-11 075239" src="https://github.com/user-attachments/assets/02cdd890-59d1-4457-988c-8ce99eb8e843" />

4. Membuat CSS Eksternal
Memisahkan kode CSS ke dalam file baru (style_eksternal.css) dan menghubungkannya dengan dokumen HTML menggunakan tag <link> untuk mendesain bagian menu navigasi.

Salinan Kode (style_eksternal.css - Bagian Navigasi):
```
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
Screenshot hasil langkah 4:
<img width="959" height="152" alt="Cuplikan layar 2026-10-11 075239" src="https://github.com/user-attachments/assets/88ee44ca-ea14-4fc7-be67-2e036046edda" />

5. Menambahkan CSS Selector (ID & Class)
Menerapkan ID Selector (#intro) dan Class Selector (.button, .btn-primary) pada file CSS eksternal yang sama untuk menata letak kotak utama dan gaya tombol interaktif.

Salinan Kode Tambahan (style_eksternal.css - Bagian Selector):
```
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
```
Screenshot hasil langkah 5:
<img width="959" height="152" alt="Cuplikan layar 2026-10-11 075239" src="https://github.com/user-attachments/assets/1580e9f2-5ee0-42f3-8ad7-d524514bc8d7" />

Eksperimen & Pembahasan Jawaban Soal Modul
Halaman eksperimen.html dirancang secara khusus untuk membuktikan dan mendemonstrasikan secara visual jawaban atas pertanyaan dan tugas pada halaman 8 modul praktikum.

Screenshot Hasil Halaman Eksperimen & Pembuktian Soal:
<img width="524" height="437" alt="Cuplikan layar 2026-10-11 080544" src="https://github.com/user-attachments/assets/501135b7-a572-4eef-8582-c4db387360b0" />

1. Eksperimen Properti CSS (Berdasarkan CSS Cheat Sheet)
Telah dilakukan eksperimen dengan memodifikasi beberapa properti dan nilai pada kode CSS yang ada di file style_eksternal.css. Penambahan properti yang dilakukan meliputi line-height, letter-spacing, border-radius, dan efek box-shadow.

Kode Awal: #intro { background: #418fb1; border: 1px solid #099249; min-height: 100px; padding: 10px; }

Kode Modifikasi: #intro { background-color: #2c3e50; border: 2px dashed #e74c3c; min-height: 150px; padding: 20px; border-radius: 12px; box-shadow: 4px 4px 10px rgba(0,0,0,0.5); }

Hasil: Elemen kotak berubah tampilan menjadi lebih modern dengan sudut yang melengkung/tumpul (efek radius), garis tepi putus-putus berwarna merah, serta penambahan efek bayangan 3D di belakang kotak (Hasil visual eksperimen ini telah dilampirkan pada file laporan praktikum).

2. Perbedaan Selektor h1 {...} dengan #intro h1 {...}
h1 {...} (Element Selector): Deklarasi ini bersifat umum/global. Aturan gaya (style) CSS yang ditulis pada blok ini akan diterapkan secara otomatis pada seluruh tag judul <h1> yang ada di dalam keseluruhan dokumen HTML tanpa memedulikan letaknya.

#intro h1 {...} (Descendant Selector): Deklarasi ini bersifat spesifik. Aturan CSS ini hanya akan memengaruhi dan diterapkan khusus pada tag <h1> yang letaknya berada di dalam atau terbungkus oleh elemen HTML ber-ID "intro" (id="intro"). Tag <h1> yang posisinya berada di luar elemen tersebut tidak akan berubah.

3. Prioritas Tampilan: CSS Internal, Eksternal, dan Inline
Apabila sebuah elemen HTML yang sama diberikan aturan desain melalui CSS Internal, CSS Eksternal, dan Inline CSS secara bersamaan, maka deklarasi yang akan menang dan ditampilkan pada browser adalah Inline CSS.

Penjelasan: CSS memiliki sistem hierarki spesifisitas (Cascading) yang menilai kedekatan kode desain dengan tag HTML-nya. Inline CSS ditulis langsung menempel di dalam tag HTML sebagai atribut (contoh: <p style="...">), sehingga ia memiliki bobot prioritas tertinggi yang akan secara otomatis menimpa (override) aturan yang berasal dari Internal CSS (<style>) maupun Eksternal CSS (file .css).

4. Prioritas Selektor: ID vs Class pada Elemen HTML yang Sama
Apabila sebuah elemen HTML memiliki atribut ID dan Class sekaligus (contoh: <p id="paragraf-1" class="text-paragraf">), dan keduanya memiliki aturan deklarasi CSS yang berbeda, maka deklarasi yang akan ditampilkan pada browser adalah milik ID Selector.

Penjelasan: Dalam perhitungan bobot spesifisitas CSS (Specificity), ID Selector memiliki poin/bobot (nilai 100) yang jauh lebih tinggi dan lebih kuat dibandingkan Class Selector (nilai 10). Sebuah elemen HTML hanya diizinkan memiliki satu ID yang unik, sehingga instruksi dari ID akan selalu diutamakan oleh browser.


