# Lab3Web - Praktikum 3: CSS Dasar

Repositori ini memuat hasil pengerjaan Praktikum 3: CSS Dasar untuk mata kuliah Pemrograman Web. Praktikum ini bertujuan untuk memahami konsep dasar CSS, aturan penulisan (Internal, Inline, dan Eksternal), serta penggunaan CSS Selector (ID dan Class).

---

## Data Mahasiswa
- **Nama** : Satrio Erlangga
- **NIM** : 312510006
- **Kelas** : I253C
- **Program Studi** : Teknik Informatika
- **Instansi** : Universitas Pelita Bangsa

---

## Langkah-Langkah Praktikum dan Hasil Screenshot

### 1. Membuat Dokumen HTML
Pembuatan struktur dasar HTML tanpa menggunakan CSS.
<img width="602" height="159" alt="Cuplikan layar 2026-10-11 074335" src="https://github.com/user-attachments/assets/0d946bcf-398e-469e-94b3-fcbf0af5c6e3" />


### 2. Mendeklarasikan CSS Internal
Menambahkan tag `<style>` pada bagian `<head>` untuk mengatur font, border, dan warna teks.
<img width="670" height="170" alt="Cuplikan layar 2026-10-11 074808" src="https://github.com/user-attachments/assets/9de92907-e4b0-4292-ae5c-7beddc4eaf81" />


### 3. Menambahkan Inline CSS
Menyisipkan atribut `style` langsung pada tag `<p>` untuk mengubah warna dan perataan teks.
<img width="828" height="171" alt="Cuplikan layar 2026-10-11 074848" src="https://github.com/user-attachments/assets/aba58446-26b5-4e6a-80d7-2bb5b82627b9" />


### 4. Membuat CSS Eksternal
Memisahkan kode CSS ke dalam file `style_eksternal.css` dan memanggilnya menggunakan tag `<link>` untuk mendesain bagian navigasi.
<img width="957" height="116" alt="Cuplikan layar 2026-10-11 075032" src="https://github.com/user-attachments/assets/8e9e5b2e-9161-4cbe-8ce8-8332239882e0" />


### 5. Menambahkan CSS Selector (ID & Class)
Menerapkan ID Selector (`#intro`) dan Class Selector (`.button`, `.btn-primary`) pada file CSS eksternal.
<img width="959" height="152" alt="Cuplikan layar 2026-10-11 075239" src="https://github.com/user-attachments/assets/5b924b79-8bed-42f5-974f-1f876a3d5db2" />


---
Eksperimen & Pembahasan Jawaban Soal Modul
Halaman eksperimen.html dirancang secara khusus untuk membuktikan dan mendemonstrasikan secara visual jawaban atas pertanyaan dan tugas pada halaman 8 modul praktikum.

Screenshot Hasil Halaman Eksperimen & Pembuktian Soal:
<img width="524" height="437" alt="Cuplikan layar 2026-10-11 080544" src="https://github.com/user-attachments/assets/df60f1de-0a0e-4385-aa15-a91f8d82fe7a" />

### Jawaban Pertanyaan dan Tugas Modul

**1. Eksperimen Properti CSS (Berdasarkan CSS Cheat Sheet)**
Telah dilakukan eksperimen dengan memodifikasi beberapa properti dan nilai pada kode CSS yang ada di file `style_eksternal.css`. Penambahan properti yang dilakukan meliputi `line-height`, `letter-spacing`, `border-radius`, dan efek `box-shadow`.
*   *Kode Awal:* `#intro { background: #418fb1; border: 1px solid #099249; min-height: 100px; padding: 10px; }`
*   *Kode Modifikasi:* `#intro { background-color: #2c3e50; border: 2px dashed #e74c3c; min-height: 150px; padding: 20px; border-radius: 12px; box-shadow: 4px 4px 10px rgba(0,0,0,0.5); }`
*   *Hasil:* Elemen kotak berubah tampilan menjadi lebih modern dengan sudut yang melengkung/tumpul (efek radius), garis tepi putus-putus berwarna merah, serta penambahan efek bayangan 3D di belakang kotak (Hasil visual eksperimen ini telah dilampirkan pada screenshot *Eksperimen & Tugas Praktikum 3*).

**2. Perbedaan Selektor `h1 {...}` dengan `#intro h1 {...}`**
*   **`h1 {...}` (Element Selector):** Deklarasi ini bersifat umum/global. Aturan gaya (style) CSS yang ditulis pada blok ini akan diterapkan secara otomatis pada seluruh tag judul `<h1>` yang ada di dalam keseluruhan dokumen HTML tanpa memedulikan letaknya[cite: 11].
*   **`#intro h1 {...}` (Descendant Selector):** Deklarasi ini bersifat spesifik. Aturan CSS ini hanya akan memengaruhi dan diterapkan khusus pada tag `<h1>` yang letaknya berada di dalam/terbungkus oleh elemen ber-ID "intro" (`id="intro"`)[cite: 12]. Tag `<h1>` yang posisinya berada di luar elemen ID tersebut tidak akan berubah.

**3. Prioritas Tampilan: CSS Internal, Eksternal, dan Inline**
Apabila sebuah elemen HTML yang sama diberikan aturan desain melalui CSS Internal, CSS Eksternal, dan Inline CSS secara bersamaan, maka deklarasi yang akan menang dan ditampilkan pada browser adalah Inline CSS[cite: 11].
*   *Penjelasan:* CSS memiliki sistem hierarki spesifisitas (Cascading) yang menilai seberapa dekat sebuah kode desain dengan tag HTML-nya. Inline CSS ditulis langsung menempel di dalam tag HTML sebagai atribut (contoh: `<p style="...">`), sehingga ia memiliki bobot prioritas tertinggi yang akan secara otomatis menimpa (override) aturan yang berasal dari Internal CSS (tag `<style>`) maupun Eksternal CSS (file `.css`)[cite: 10, 11].
*   *Contoh Kasus:* Di CSS Eksternal dan Internal paragraf diatur berwarna merah. Namun di dokumen HTML ditulis `<p style="color: blue;">`. Maka saat dijalankan, paragraf tersebut akan berwarna biru.

**4. Prioritas Selektor: ID dan Class pada Elemen HTML yang Sama**
Apabila sebuah elemen HTML memiliki atribut ID dan Class sekaligus (contoh: `<p id="paragraf-1" class="text-paragraf">`), dan keduanya memiliki aturan deklarasi CSS yang berbeda, maka deklarasi yang akan ditampilkan pada browser adalah milik ID Selector[cite: 12].
*   *Penjelasan:* Dalam perhitungan bobot spesifisitas CSS (Specificity), ID Selector memiliki poin yang jauh lebih tinggi dan lebih kuat dibandingkan Class Selector. Sebuah elemen HTML hanya diizinkan memiliki satu ID yang unik, sehingga aturan ID lebih diutamakan oleh browser dibandingkan Class yang dapat digunakan berulang kali[cite: 11, 12].
*   *Contoh Kasus:* Di CSS terdapat deklarasi `.text-paragraf { color: green; }` dan `#paragraf-1 { color: red; }`. Ketika elemen tersebut dirender, maka teks akan berwarna merah karena warna merah merupakan instruksi dari ID yang mengalahkan instruksi warna hijau dari Class[cite: 11, 12].
