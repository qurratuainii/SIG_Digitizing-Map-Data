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

19. Sekarang Enable Snapping (Magnet Icon) akan muncul di panel. Klik untuk mengaktifkannya dan pilih All Layers dan pilih Open Snapping Options... (*Gambar 18*)

20. Dalam dialog Snapping options, klik Snapping on Intersection, yang memungkinkan kita untuk menjepret perpotongan layer latar belakang (*Gambar 19*)

21. Sekarang kita dapat mengklik tombol Add Feature dan mendigitalkan jalan lain di sekitar taman. Pastikan untuk mengklik Save Edits setelah menambahkan fitur baru untuk menyimpan pekerjaan kita. Alat yang berguna untuk membantu kita mendigitalkan adalah Vertex Tool. Klik tombol Vertex Tool dan pilih Vertex Tool (Current Layer) (*Gambar 20*)

22. Setelah alat simpul diaktifkan, klik fitur apa pun untuk menampilkan simpul. Klik pada simpul mana pun untuk memilihnya. Verteks akan mengubah warna setelah dipilih. Sekarang kita dapat mengklik dan menyeret mouse kita untuk memindahkan simpul. Ini berguna saat kita ingin melakukan penyesuaian setelah fitur dibuat. Kita juga dapat menghapus simpul yang dipilih dengan mengklik tombol Hapus (*Gambar 21*)

23. Setelah kita selesai mendigitalkan semua jalan, klik tombol Toogle Editing. Klik Save (*Gambar 22*)

24. Sekarang kita akan membuat layer lain untuk mendigitalkan taman sebagai poligon. Klik Layer lalu Create Layer lalu New GeoPackage Layer... ikon dari Panel. Dalam dialog New GeoPackage Layer, klik tombol ... dan pilih database GeoPackage bernama digitizing.gpkg. Beri nama layer baru sebagai atribut yang disebut Taman. Pilih MultiPolygon sebagai Tipe. Peta topografi dasar adalah EPSG:2193 - NZGD 2000 CRS. Klik Oke. Di Bidang Baru Masukkan Nama, dan jenisnya sebagai data Teks, dengan 50 sebagai panjang maksimum dan klik :gulilabel:` Tambahkan ke daftar bidang.`. Klik OK (*Gambar 23*)

25. Dialog pop-up akan muncul. Pilih tombol Add New Layer (*Gambar 24*)

26. Sekarang pilih layer Parks lalu klik road Toogle Editing dan klik tombol Add feature dan klik pada kanvas peta untuk menambahkan simpul poligon. Digitalkan poligon yang mewakili taman. Pastikan menjepret simpul jalan sehingga tidak ada celah antara poligon taman dan garis jalan. KLik kanan untuk menyelesaikan poligon (*Gambar 25*)

27. Masukkan nama taman di jendela pop-up Taman-Atribut Fitur (*Gambar 26*)

28. Sekarang digitalkan bagian atas taman. Masukkan nama taman dan simpan perubahannya (*Gambar 27*)

29. Selanjutnya, sebelum mendigitalkan poligon dalam, mari atur pengaturan yang dapat memudahkan pekerjaan. Lapisan Multi-Polygon menawarkan pengaturan berguna lainnya yang disebut Avoid intersections of new polygons. Pilih Enable Snapping, klik untuk mengaktifkannya, klik All Layers dan pilih Advanced Configuration (*Gambar 28*)

30. Klik tombol Avoid Overlap on Active layers di bilah snapping toolbar (*Gambar 29*)

31. Selanjutnya di edit konfigurasi lanjut, pilih Unit sebagai pixel (*Gambar 30*)

32. Centang kotak di Avoid Overlap Column di baris untuk layer taman (*Gambar 31*)

33. Klik Add Feature untuk menambahkan poligon. Dengan Avoid Overlap kita akan dapat dengan cepat mendigitalkan poligon baru tanpa khawatir akan menjepret secara tepat ke poligon tetangga (*Gambar 32*)

34. Klik kanan untuk menyelesaikan poligon dan masukkan atributnya. Ajaibnya poliggon baru menyusut dan tersentak tepat ke batas poligon tetangga. Ini sangat berguna saat mendigitalkan batas kompleks di mana kita tidak perlu presisi dan masih memiliki poligon yang benar secara topologi. Klik Toggle Editing untuk menyelesaikan pengeditan layer Parks (*Gambar 33*)

35. Selanjutnya untuk mendigitalkan layer bangunan. Buat layer poligon baru bernama Buildings dengan mengkklik ikon Layer Create Layer New GeoPackage Layer ... dari Panels. Atur bangunan dan MultiPolygon. pilih CRS sebagai EPSG:2193 - NZGD 2000. Klik OK (*Gambar 34*)

36. Setelah lapisan bangunan ditambahkan, matikan lapisan Taman dan Jalan untuk membuat peta topo dasar terlihat. Pilih layer Buildings dan klik Toggle Editing (*Gambar 35*)

37. Mendigitalkan bangunan bisa menjadi tugas yang rumit, dan juga menantang untuk menambahkan simpul secara manual sehingga ujung-ujungnya egak lurus dan membentuk persegi panjang. Kita akan menggunakan toolbar QGIS yang disebut Shape Digitizing untuk membantu tugas ini. Klik kanan pada ruang kosong mana pun di area toolbar dan aktifkan Shape Digitalizing Toolbar (*Gambar 36*)

38. Aktifkan pengeditan dengan menekan ikon pensil Toggle Editing (*Gambar 37*)

39. Sekarang klik Add Recatangle dropdown pilih Add rectangle from Extent tombol (*Gambar 38*)

40. Zoom ke area dengan bangunan. Klik dan seret mouse untuk menggambar persegi panjang yang sempurna. Demikian pula, tambahkan bangunan yang tersisa (*Gambar 39*)

41. Kita akan melihat bahwa beberapa bangunan tidak vertikal, dan kita perlu menggambar persegi panjang pada sudut yang sesuai dengan tapak bangunan. Di bawah Add Rectangle dropdown pilih Add Rectangle from center dan tombol point (*Gambar 40*)

42. Zoom ke area bangunan berbentuk berlian. Klik di tengah untuk menjatuhkan titik dan seret mouse untuk menggambar persegi panjang

43. Kita perlu memutas persegi panjang ini agar sesuai dengan gambar pada peta topo. alat putar tersedia di toolbar Advanced Digitizing. Klik kanan pada area kosong pada bagian toolbar dan aktifkan toolbar Advanced Digitizing (*Gambar 41*)

44. Klik tombol Rotate Feature (*Gambar 42*)

45. Gunakan alat fitur Select Single untuk memilih poligon yang ingin kita putar. Setelah alat Fitur Putar diaktifkan, kita akan melihat garis bidik di tengah poligon. Klik tepat pada garis bidik itu dan seret mouse sambil menahan tombol klik kiri. Pratinjau fitur yang diputar akan muncul. Lepaskan tombol mouse saat poligon sejajar dengan tapak bangunan (*Gambar 43*)

46. Simpan hasil edit layer dan klik Toggle Editing setelah kita selesai mendigitalkan semua bangunan. Kita dapat menyeret lapisan untuk mengubah urutan tampilannya. Tugas digitalisasi sekarang selesai. Kita dapat bermain dengan opsi gaya dan pelabelan di properti lapisan untuk membuat peta yang terlihat bagus dari data yang kita buat (*Gambar 44*, *Gambar 45*)
