# Data Transjakarta #

Dataset ini berisi data Transjakarta di bulan **April 2023**. Setelah melihat dan memahami informasi dari dataset ini, saya menemukan informasi apa saja yang saya miliki yang dilihat dari kolom yang ada, dataset ini memiliki 22 kolom yang berisikan informasi, antara lain:

| Kolom             | Deskripsi                                      |
|-------------------|------------------------------------------------|
| `transID`           | Unik ID transaksi setiap transaksi             |
| `payCardID`         | ID kartu yang digunakan pengguna sebagai alat bayar |
| `payCardBank`       | Jenis kartu yang digunakan pengguna Transjakarta |
| `payCardName`       | Nama pengguna yang tertanam dalam kartu       |
| `payCardSex`        | Jenis kelamin pengguna yang tertanam dalam kartu |
| `payCardBirthDate`  | Tahun lahir pengguna kartu                     |
| `corridorID`        | Kode jenis rute                                |
| `corridorName`      | Nama rute beserta start dan finish-nya         |
| `direction`         | Terdapat 0 dan 1 dimana 0 adalah arah pergi dan 1 arah balik rute |
| `tapInStops`        | ID halte pengguna tap masuk (Entrance)         |
| `tapInStopsName`    | Nama halte pengguna tap masuk                   |
| `tapInStopsLat`     | Koordinat latitude halte pengguna tap masuk    |
| `tapInStopsLon`     | Koordinat longitude halte pengguna tap masuk   |
| `stopStartSeq`      | Menunjukkan pemberhentian keberapa berdasarkan direction |
| `tapInTime`         | Waktu pengguna tap masuk berupa tanggal dan jam |
| `tapOutStops`       | ID halte pengguna tap keluar (Exit)            |
| `tapOutStopsName`   | Nama halte pengguna tap keluar                  |
| `tapOutStopsLat`    | Koordinat latitude halte pengguna tap keluar   |
| `tapOutStopsLon`    | Koordinat longitude halte pengguna tap keluar  |
| `stopEndSeq`        | Menunjukkan pemberhentian keberapa berdasarkan direction |
| `tapOutTime`        | Waktu pengguna tap keluar berupa tanggal dan jam |
| `payAmount`         | Harga yang dibayar oleh pengguna               |


## Latar Belakang ##

Transjakarta adalah sistem transportasi yang berbasis Bus Rapid Transit (BRT) dan non-BRT yang telah beroperasi pada tahun 2004 untuk menjawab tantangan kemacetan di ibu kota Indonesia.

Seiring dengan berjalannya waktu, Transjakarta telah mengalami perkembangan yang signifikan. Awalnya hanya beroperasi di wilayah Jakarta, kini cakupannya telah meluas hingga ke wilayah Bodetabek (Bogor, Depok, Tangerang, dan Bekasi) [source : Peta Integrasi TJ](https://transjakarta.co.id/peta-rute/). Ini memungkinkan masyarakat tidak hanya bergerak di dalam kota Jakarta, tetapi juga antar-kota dengan lebih mudah.

Dengan menyediakan moda transportasi yang terpadu dan terbebas dari kemacetan, Transjakarta tidak hanya menjadi solusi untuk masalah transportasi, tetapi juga merupakan pilihan utama bagi warga Jakarta dalam melakukan perjalanan sehari-hari. Kemudahan akses, kecepatan, dan kenyamanan yang ditawarkan Transjakarta membuatnya menjadi alternatif yang menarik dibandingkan dengan kendaraan pribadi atau moda transportasi lainnya.

Namun, seperti halnya sistem transportasi publik lainnya, Transjakarta juga menghadapi sejumlah tantangan. Dalam rangka terus meningkatkan kualitas layanan dan efisiensi operasional, PT. Transjakarta secara berkala melakukan evaluasi bulanan. Evaluasi ini menjadi instrumen penting untuk memantau kinerja armada, operasi rute, dan fasilitas halte. Dengan memahami kebutuhan dan pola penggunaan masyarakat, Transjakarta dapat melakukan penyesuaian yang tepat guna memastikan layanannya tetap relevan dan efektif.

Ada beberapa isu yang masih dihadapi oleh Transjakarta antara lain:
1. **Meningkatkan fasilitas & aksesibilitas**:  Mengenai fasilitas untuk penunjang lansia dan banyaknya kasus pelecehan seksual terhadap penumpang perempuan. Kejadian seperti ini menyoroti kebutuhan mendesak untuk meningkatkan keamanan penumpang.[Berita TJ Inklusif](https://www.kompas.id/baca/metro/2023/03/15/penumpang-idamkan-jpo-halte-transjakarta-yang-inklusif) <br>
[Berita cegah pelecehan seksual](https://www.antaranews.com/berita/3410523/transjakarta-diminta-tingkatkan-pengawasan-cegah-pelecehan-seksual)

1. **Mengoptimasi kinerja armada** : Distribusi transjakarta saat hari-hari besar mengelamai beberapa perubahan jumlah penumpang. Apakah perubahan yang terjadi cukup signifikan terhadap distribusi rataan harian tiap waktu kerja.

1. **Memahami *flow* penggunaan Transjakarta**: Rute yang mengalami kemacetan yang akan membantu adanya penyesuaian jadwal dan alokasi sumber daya. Dikarenakan kepadatan penumpang pada jam tertentu menjadi kendala utama, menciptakan antrean panjang dan waktu tunggu yang meningkat. 
Sumber: *https://megapolitan.kompas.com/read/2023/01/17/12114871/menengok-sibuknya-penumpang-bus-transjakarta-di-halte-harmoni-berlari?page=all.*

1. **Pemantauan dan Evaluasi Berkelanjutan**: Transjakarta, sebagai salah satu alternatif utama transportasi di Jakarta, tetap berperan penting dalam memenuhi kebutuhan penumpang akan pengalaman bertransportasi yang nyaman, cepat, dan handal. 

Dengan mengatasi permasalahan yang dihadapi, Transjakarta dapat terus berkontribusi secara signifikan terhadap mobilitas perkotaan dan kesejahteraan penduduk Jakarta.

**stakeholders** terkait yaitu **Divisi Operasional dan Pelayanan & Bisnis Transjakarta**


## Tujuan bisnis ##

1. Menganalisa data *flow* penggunaan Transjakarta di halte yang ramai agar mendapatkan insight mengenai *peak hour* dan rekomendasi yang tepat untuk kelompok lansia dan penggunna wanita.

1. Melihat tren kepadatan harian customer Transjakarta sepanjang April 2023, serta membandingkan rataan harian tingkat kepadatan di tanggal merah dan hari kerja saat weekdays.

1. Merekomendasikan perbaikan fasilitas yang dapat mengatasi tantangan aksesibilitas dan meningkatkan kualitas layanan secara keseluruhan seperti fasilitas untuk lansia dan armada khusus perempuan.

## Data Info ##

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 36474 entries, 0 to 36473
Data columns (total 33 columns):
 #   Column            Non-Null Count  Dtype         
---  ------            --------------  -----         
 0   index             36474 non-null  int64         
 1   transID           36474 non-null  object        
 2   payCardID         36474 non-null  int64         
 3   payCardBank       36474 non-null  object        
 4   payCardName       36474 non-null  object        
 5   payCardSex        36474 non-null  object        
 6   payCardBirthDate  36474 non-null  int64         
 7   corridorID        36474 non-null  object        
 8   corridorName      36474 non-null  object        
 9   direction         36474 non-null  float64       
 10  tapInStops        36474 non-null  object        
 11  tapInStopsName    36474 non-null  object        
 12  tapInStopsLat     36474 non-null  float64       
 13  tapInStopsLon     36474 non-null  float64       
 14  stopStartSeq      36474 non-null  int64         
 15  tapInTime         36474 non-null  datetime64[ns]
 16  tapOutStops       36474 non-null  object        
 17  tapOutStopsName   36474 non-null  object        
 18  tapOutStopsLat    36474 non-null  float64       
 19  tapOutStopsLon    36474 non-null  float64       
...
 31  day_group         36474 non-null  object        
 32  rush_hour         36474 non-null  object        
dtypes: datetime64[ns](2), float64(7), int32(3), int64(5), object(16)
memory usage: 8.8+ MB
