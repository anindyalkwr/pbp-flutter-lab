# (README) Tugas 7: Elemen Dasar Flutter

Pemrograman Berbasis Platform (CSGE602022) - diselenggarakan oleh Fakultas Ilmu Komputer Universitas Indonesia, Semester Ganjil 2022/2023

## Penjelasan dan demonstrasi program
(1) Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget dan jelaskan perbedaan dari keduanya. <br>
**_Stateless_ _widget_**: _stateless_ widget_ adalah _widget_ yang penampilan dan propertinya tidak berubah atau dalam kata lain _immutable_ selama jalannya sebuah aplikasi. <br>
**Stateful _widget_**: _stateful_ _widget_ adalah _widget_ yang dapat merubah propertinya saat dijalankan dalam suatu aplikasi dan bersifat dinamis. _Widget_ ini _mutable_ dan dapat diubah berkali - kali mengembalikan respon dari _events_ _action_ yang dilakukan oleh pengguna atau ketika menerima data. <br>

|  _Stateless_  |   _Stateful_  |
| ------------- | ------------- |
| Statis  | Dinamis  |
| Tidak berubah selama berjalannya sebuah aplikasi  | Dapat berubah sewaktu-waktu apabila ketika menerima data atau berinteraksi dengan pengguna  | 
<br>
 
(2) Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya. <br>
AppBar: Sebuah desain material _app bar_ yang berisikan _toolbar_ dan beberapa widget lainnya seperti _TabBar_ atau _FlexibleSpaceBar_ <br>
Center: Widget yang men-_centerkan_ elemen child widget di dalamnya <br>
Column: Tata letak sebuah list dari _child widgets_ secara vertikal <br>
Container: Widget yang mengkombinasikan penggambaran, peletakkan, dan penyesuaian ukuran umum untuk widgets <br>
FloatingActionButton: Tombol bulat yang _hover_ di atas konten untuk mempromosikan _primary action_ dalam sebuah aplikasi <br>
Icon: Berisikan material kumpulan desain _icon_ <br>
MaterialApp: Widget yang membungkus w lain untuk keperluan aplikasi Material Design <br>
Row: Tata letak sebuah list dari _child widgets_ secara horizontal <br>
Scaffold: Implementasi struktur tata letak material desain visual dasar dan menyediakan API's untuk menampilkan _drawers, snack bars_, dan _bottom sheets_ <br>
Text: Menampilkan pesan beserta gayanya <br>

(3) Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut. <br>

(4) Jelaskan perbedaan antara const dengan final. <br>

(5) Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas. <br>
Pertama - tama saya menambahkan fungsi baru yang berkebalikan dengan fungsi incrementCounter, yaitu decrementCounter yang di dalamnya memiliki conditions ketika counter bernilai 0, maka tidak akan melakukan decrement kepada variabel counter. Selain itu saya juga menambahkan dua buah fungsi yang selalu dipanggil pada fungsi increment/decrement sebuah counter, yaitu setTextInfo dan setVisibility yang akan merubah variabel visibility dan textInfo yang bergantung pada variabel counter. Setelah semua fungsi berhasil dibuat, maka meletakkan FloatingActionButton baru dengan Icon remove dengan menyesuakannya sesuai yang diminta oleh soal. <br>

#### Referensi: <br>
1. [Welcome to the Flutter API reference documentation!](https://api.flutter.dev/index.html)
