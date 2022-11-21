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
Memanggil fungsi setState() akan memberi tanda kepada framework bahwa state internal di dalam objek ini telah berubah yang mungkin akan mempengaruhi user interface sehingga menyebabkan framework untuk menjadwalkan sebuah build untuk state object ini. Apabila fungsi ini tidak dipanggil maka framewrok bisa saja tidak menjadwalkan build ini dan user interface tidak akan berubah. <br>
Pada tugas yang saya kerjakan, variabel yang terdampak dari fungsi setState() ini adalah variabel counter dan juga textInfo dimana, perlu build ulang tiap kali dilakukan increment atau decrement counter sehingga menampilkan tampilan yang diinginkan. <br>

(4) Jelaskan perbedaan antara const dengan final. <br>
Walaupun kedua variabel const dan final memiliki kesamaan yaitu tidak dapat diubah setelah inisialisasi, perbedaan keduanya antara lain: <br>
**const**: digunakan untuk menginisialisasi variabel yang diketahui nilai awalnya <br>
**final**: digunakan untuk menginisialisasi variabel yang tidak diketahui nilai awalnya <br>

(5) Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas. <br>
Pertama - tama saya menambahkan fungsi baru yang berkebalikan dengan fungsi incrementCounter, yaitu decrementCounter yang di dalamnya memiliki conditions ketika counter bernilai 0, maka tidak akan melakukan decrement kepada variabel counter. Selain itu saya juga menambahkan dua buah fungsi yang selalu dipanggil pada fungsi increment/decrement sebuah counter, yaitu setTextInfo dan setVisibility yang akan merubah variabel visibility dan textInfo yang bergantung pada variabel counter. Setelah semua fungsi berhasil dibuat, maka meletakkan FloatingActionButton baru dengan Icon remove dengan menyesuakannya sesuai yang diminta oleh soal. <br>

#### Referensi: <br>
1. [Welcome to the Flutter API reference documentation!](https://api.flutter.dev/index.html)

# (README) Tugas 8: Flutter Form

Pemrograman Berbasis Platform (CSGE602022) - diselenggarakan oleh Fakultas Ilmu Komputer Universitas Indonesia, Semester Ganjil 2022/2023

## Penjelasan dan demonstrasi program
(1) Jelaskan perbedaan Navigator.push dan Navigator.pushReplacement. <br>
Navigator.push: Routing akan di push ke dalam stack tanpa menghapus routing sebelumnya <br>
Navigator.pushReplacement: Routing akan di push ke dalam stack dengan menggantikan routing sebelumnya (dihapus setelah routing baru selesai di load) <br>

(2) Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya. <br>
Pada proyek kali ini, saya menambahkan beberapa widget baru antara lain: <br>
ListTile: Digunakan untuk menampilkan pilihan pada drawer <br>
ListView: Digunakan untuk menampilkan data yang telah diinput oleh pengguna <br>
TextFormField: Digunakan untuk menerima input dari pengguna <br>
DropdownButton: Digunakan untuk menerima input dari pilihan dropdown pengguna <br>
TextButton: Digunakan sebagai ActionListener untuk menjalankan (menyimpan data) <br>

(3) Sebutkan jenis-jenis event yang ada pada Flutter (contoh: onPressed). <br>
onPressed: Event akan dieksekusi setelah menerima input berupa tekan (biasanya pada button) <br>
onHover: Event akan dieksekusi setelah menerima input selama pointer mouse berada di widget <br>
onFocusChange: Event akan dieksekusi setelah menerima input selama pengguna sedang berinteraksi pada widget <br>
onChanged: Event akan dieksekusi setelah menerima input selama pengguna sednag melakukan perubahan terhadap value yang dimiliki oleh widget <br>
onSaved: Event akan dieksekusi ketika nilai dari form disimpan melalui FormState.save <br>

(4) Jelaskan bagaimana cara kerja Navigator dalam "mengganti" halaman dari aplikasi Flutter. <br>
Navigator mengganti halaman dari aplikasi Flutter dengan memanfaatkan konsep Stack, yang dimana flutter biasanya akan melakukan push untuk menuju halaman yang ingin dijalankan diatas stack dan dapat memanfaatkan pop untuk kembali ke halaman yang sebelumnya diakses atau dengan push kembali halaman tersebut. Flutter memanfaatkan MaterialPageRoute dalam menjalankan proses perpindahan halaman. <br>

(5) Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas. <br>
Pertama, saya menambahkan file baru ```form.dart``` dan ```data.dart``` dan mengimplementasikan appbar sederhana di tiap file tersebut. Setelah itu saya menambahkan masing - masing drawer sebagai navigator untuk berpindah halaman dengan memanfaatkan widget ListTile. Selanjutnya saya menambahkan berbagai macam widget input pada ```form.dart``` yang disesuaikan dengan kebutuhan Tugas 8. Kemudian saya membuat class baru bernama Data yang memiliki attribut judul, nominal, dan juga jenis yang akan disimpan nantinya pada list di file form.dart menggunakan widget TextButton. Terakhir, dengan melakukan import saya bisa mengakses list di file form.dart untuk digunakan pada file data.dart yang kemudian ditampilkan menggunakan widget ListView. Terakhir saya menyesuaikan tampilan yang telah saya buat dengan mengikuti ketentuan dari Tugas 8 ini. <br>

# (README) Tugas 9: Integrasi Web Service pada Flutter

Pemrograman Berbasis Platform (CSGE602022) - diselenggarakan oleh Fakultas Ilmu Komputer Universitas Indonesia, Semester Ganjil 2022/2023

## Penjelasan dan demonstrasi program
(1) Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON? <br>
Seharusnya bisa, yaitu dengan mengkonversikan data json langsung setelah di decode dari url. Dari literatur yang saya lakukan, sedikit bahkan jarang ada yang menggunakan cara tersebut bahkan dari dokumentasi flutter pun membuat folder model terlebih dahulu. Sehingga menurut saya hal tersebut tidaklah lebih baik dibandingkan membuat model terlebih dahulu karena lebih sulit di baca dan tidak efisien. <br>

(2) Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya. <br>
```FutureBuilder```: Memudahkan mengelola asynchronous data sources <br>
```ListTile```: Untuk menampilkan data dalam alignment dan position yang diinginkan, serta menjalankan perintah onTap() <br>
```ListView```: Untuk menampilkan data dalam alignment dan position yang diinginkan <br>

(3) Jelaskan mekanisme pengambilan data dari json hingga dapat ditampilkan pada Flutter. <br> 
a. Menambahkan http package dengan command ```flutter pub add http``` dan memberikan akses internet ke dalam proyek yang sedang dibuat dengan menambahkan beberapa line kode pada file ```android/app/src/main/AndroidManifest.xml``` <br>
b. Buat folder ```model``` dan buat dart file untuk model dari data json yang ingin diambil dan ditampilkan. Saya memanfaatkan website quicktype dalam menulis kode model MyWatchlist yang menyesuaikan dengan kode json yang diberikan <br>
c. Pada folder ```page```, tambahkan halaman yang akan menampilkan data json dan buatlah fungsi Future yang akan mengambil data dari url HTTP yang diberikan dengan decode url menjadi bentuk json dan dikonversikan ke dalam object WatchList. <br>
d. Tampilkan data dengan widget yang diinginkan, saya sendiri memanfaatkan ```ListView``` dan ```ListTile``` untuk menampilkan data <br>

(4) Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas. <br>
a. Menambahkan ListTile baru yang navigate ke halaman mywatchlist pada drawer. <br>
b. Menambahkan folder ```model```, dan file ```mywatchlist.dart``` yang berisikan kode yang disalin dari website Quicktype berdasarkan data json yang diberikan. <br>
c. Menambahkan file ```mywatchlist_page.dart``` di folder dart yang mengambil dan menampilkan data json menggunakan fungsi Future berdasarkan url Tugas Django sebelumnya. <br>
d. Menampilkan data json dalam ListTile sehingga dapat menambahkan fungsi ```onTap()``` yang akan menavigasi setiap judul watch list ke halaman detail ketika ada request tap dengan membawa detail data tiap watchList <br>
e. Menambahkan file ```watchlistitem.dart``` yang akan menampilkan detail data berdasarkan judul yang ditap. <br>
f. Menambahkan tombol back yang akan navigate.pop (kembali ke halaman sebelumnya) yang ditempelkan pada bottom navigation bar agar positionnya fixed. <br>
