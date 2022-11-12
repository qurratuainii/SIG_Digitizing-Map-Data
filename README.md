# SIG_Digitizing-Map-Data

*Tutorial Digitizing Map Data

1. Download file BX24_GeoTifv1-02-clip.tif terlebih dahulu. 

2. Pada QGIS, kita memuat file gambar. Klik Layer lalu klik Add Layer dan klik Add Raster Layer (*Gambar 1*)

3. Dalam Data Source Manager pilih Raster. Di bawah sumber klik pada ... dan cari BX24_GeoTifv1-02.tif yang diunduh dan klik Open. Kemudian klik Add diikuti close jendela tersebut (*Gambar 2*)

4. Ini merupakan file raster yang besar, dan kita mungkin memperhatikan bahwa saat kita memperbesar atau menggeser peta, peta memerlukan sedikit waktu untuk merender gambar. QGIS menawarkan solusi sederhana untuk membuat raster memuat lebih cepat dengan menggunakan Piramida Gambar. QGIS membuat petak pra-render pada resolusi yang berbeda. Ini membuat navigasi peta cepat dan responsif. Klik kanan layer BX24_GeoTifv1-02 dan pilih Properties (*Gambar 3*)

5. Pada jendela Layer Properties, pilih tab Pyramids. Pilih semua resolusi yang ditawarkan di panel Resolutions. Biarkan opsi lain ke default dan klik Build pyramids (*Gambar 4*)

6. Setelah proses selesai, kotak dailog akan menampilkan piramida tanpa tanda silang. Ini menendakan pembangunan Piramida Gambar sudah selesai. Klik OK (*Gambar 5*)

7. Sebelum kita mulai, kita perlu mengatur Opsi Digitalisasi default. Klik Settings lalu pilih Options... (*Gambar 6*)

8. Pilih tab Digitizing pada options dialog. Aktifkan gertakan secara default di bawah bagian Snapping. Dalam mode jepret default pilih Vertex. Ini akan memungkinkan kita untuk snap ke vertex terdekat. Kita juga lebih memilih untuk mengatur toleransi gertakan default dan radius Pencarian untuk suntingan titik dalam pixel daripada unit peta. Ini akan memastikan jarak gertakan tetap konstan terlepas dari tingkat zoom. Tergantung pada resolusi layar komputer kita, kita dapat memilih nilai yang sesuai. Klik OK (*Gambar 7*)

9. Sekarang kita siap untuk memulai digitalisasi. Pertama kita akan membuat layer jalan dan mendigitalkan jalan di sekitar area taman. Klik Layer lalu Create Layer lalu New GeoPackage Layer... ikon dari Panel. GeoPackage adalah format data terbuka, non-proprietary, platform-independen, dan berbasis standar untuk sistem informasi geografis yang diimplementasikan sebagai wadah database SQLite. ini membuatnya lebih mudah untuk memindahkannya daripada sekumpulan shapefile. Dalam tutorial ini, kita membuat beebrapa lapisan poligon dan lapisan garis sehingga GeoPackage akan lebih cocok. Kita selalu dapat memuat GeoPackage dan mengekspor layer sebagai shapefile atau format lain yang kita inginkan (*Gambar 8*)

10. Pada New GeoPackage Layer, klik tombol ... dan simpan database GeoPackage baru bernama digitizing.gpkg. Pilih nama Tabel sebagai Roads dan pilih LineString sebagai tipe Geometri. Peta topografi dasar adalah EPSG:2193-NZGD 2000 CRS (*Gambar 9*)

11. Saat membuat lapisan QGIS, kita harus memutuskan atribut masing-masing fitur. Karena ini adalah lapisan jalan, kita juga akan memiliki dua atribut utama - Nama dan Kelas. Di bidang baru masukkan nama dari jenis data Teks, dengan 50 sebagai Panjang maksimum dan klik Add to fields List. Sekarang buat kelas atribut baru dari tipe data Teks, dengan 50 sebagai panjang maksimum. Klik OK (*Gambar 10*)

12. Setelah Layer Roads dimuat, klik tombol Toggle Editing untuk menempatkan layer dalam mode pengeditan (*Gambar 11*)

13. Klik tombol Add Line Feature. Klik pada kanvas peta untuk menambahkan simpul baru. Tambahkan simpul baru bersama dengan fitur jalan. Setelah kita mendigitalkan ruas jalan, klik kanan untuk mengakhiri fitur (*Gambar 12*)

14. Setelah kita mengklik kanan untuk mengakhiri fitur, kita akan mendapatkan dialog pop-up yang disebut Jalan - Atribut Fitur. Di sini kita dapat memasukkan atribut dari fitur yang baru dibuat. Lewati memasukkan nilai apa pun untuk fid karena ini adalah id berurutan yang akan dibuat secara otomatis. Masukkan nama jalan seperti yang tertera di peta topo. Secara opsional, tetapkan juga nilai kelas Jalan, klik OK (*Gambar 13*)

15. Gaya default dari layer garis baru adalah garis tipis. Mari kita ubah untuk lebih melihat fitur digital di kanvas. Pilih layer Roads dan klik LAyer Styling Panel (*Gambar 14*)

16. Di Panel Penataan Lapisan, cari gaya lapisan jalan yang berbeda. Pilih jalan topo. Klik OK (*Gambar 15*)

17. Sekarang lapisan jalan akan terlihat jelas. jika kita puas dengan hasilnya, klik tombol Save Layer Edits untuk menyimpan perubahan (*Gambar 16*)

18. Sebelum kita mendigitalkan jalan yang tersisa, penting untuk memperbaruui beberapa pengatran snap penting lainnya untuk membuat lapisan bebas kesalahan. Klik kanan pada ruang mana pun di area bilah alat dan aktifkan bilah Snapping toolbar (*Gambar 17*)

19
