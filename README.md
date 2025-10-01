# Lab-2 | CSS Dasar

Nama : Tiara Hayatul Khoir

Kelas : TI.24.A.5

NIM : 312410474

Mata Kuliah : Pemrograman Web

## Langkah-langkah Praktikum

### 1. Langkah 1 - Membuat Dokumen HTML
Saya membuat file `lab2_css_dasar.html` dengan struktur dasar HTML berisi header, nav, dan div intro.
![Dokumen HTML](https://github.com/tir890/Lab2Web/blob/d954c6c04bf2632ab7ee6dccd82755bea84c56e9/1.png)

### 2. Langkah-2 - Menambahkan CSS Internal
Menambahkan kode `<style>` di dalam `<head>` untuk mengatur body, header, dan h1.
![CSS Internal](https://github.com/tir890/Lab2Web/blob/b81c4862cfed1c2c158dc41bdcd5af174738ef8d/2.png)

### 3. Langkah-3 - Menambahkan Inline CSS
Menambahkan atribut `style` langsung pada elemen `<p>`, sehingga teks berubah warna dan posisinya rata tengah.
![Inline CSS](https://github.com/tir890/Lab2Web/blob/b81c4862cfed1c2c158dc41bdcd5af174738ef8d/3.png)

### 4. Langkah 4 - Membuat CSS Eskternal 
Membuat file `style_eksternal.css` dan menghubungkannya ke `lab2_css_eksternal.html` menggunakan tag `<link>`.
![CSS Eksternal](https://github.com/tir890/Lab2Web/blob/b81c4862cfed1c2c158dc41bdcd5af174738ef8d/4.png)

### 5. Langkah-5 - Menambahkan CSS Selector
Menambahkan ID Selector dan Class Selector pada file eksternal CSS. ID untuk styling khusus satu elemen, sedangkan class bisa dipakai ulang di beberapa elemen.
![CSS Selector](https://github.com/tir890/Lab2Web/blob/b81c4862cfed1c2c158dc41bdcd5af174738ef8d/5.png) 

## Pertanyaan dan Tugas

### 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS  dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
- Contoh eksperimen: ubah warna background, font-size, atau padding.
```css
p {
    font-size: 18px;
    color: darkblue;
    background-color: lightyellow;
    padding: 10px;
}
```
- Kesimpulan: dengan mengubah nilai properti, tampilan elemen bisa langsung berubah tanpa harus mengubah struktur HTML.

### 2. Apa perbedaan pendeklarasian CSS elemen `h1 {...}` dengan #intro `h1 {...}`? berikan  penjelasannya!
Jawaban:
- `h1 { ... }` → berlaku untuk semua elemen `<h1>` di halaman.
- `#intro h1 { ... }` → hanya berlaku untuk `<h1>` yang ada di dalam elemen dengan id="intro".
- Jadi `#intro h1` lebih spesifik daripada `h1`.

### 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada  elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan  penjelasan dan contohnya!
Jawaban:
Urutannya: Inline CSS > Internal CSS > Eksternal CSS (karena inline punya prioritas tertinggi). Contohnya,
```css
<p style="color: red;">Teks ini merah karena inline override internal & eksternal</p>
```

### 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut  terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?  Berikan penjelasan dan contohnya! `( <p id="paragraf-1" class="text-paragraf"> )` 
ID selector (`#id`) punya prioritas lebih tinggi daripada class (`.class`). Contohnya,
```html
<p id="paragraf-1" class="text-paragraf">Contoh teks</p>
```

```css
#paragraf-1 { color: red; }
.text-paragraf { color: blue; }
```

Hasilnya: teks jadi merah (karena ID lebih kuat dari class).
