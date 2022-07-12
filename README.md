# Hotel-Booking-Demand-EDA
Hotel booking demand in Europe Explanatory Data Analysis with Data Visualization

Created as a team project with [Ano](https://github.com/delabrilliano) and [Erike](https://github.com/Nasyahh)

![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20180615.jpg)
## Introduction

Exploratory Data Analysis adalah sebuah proses menganalisis suatu data untuk menemukan suatu informasi atau insight yang kemudian dari insight tersebut dapat dirumuskan suatu rekomendasi untuk pengambil keputusan (stakeholder). Rekomendasi yang diberikan bersifat actionable dan memiliki impact kedalam bisnis. Disini kita akan melakukan EDA untuk data [Hotel Bookings](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand) . 

Tentang data "Hotel Booking Demand"
Industri pariwisata merupakan salah satu industri yang paling terdampak oleh pandemi covid-19, khususnya industri perhotelan. Dengan adanya pembatasan berpergian, menurut riset yang dilakukan Mckinsey pada tahun 2020, tingkat pemesanan hotel berkurang sangat jauh sampai-sampai membuat para investor di industri tersebut sangat pesimis.

Untuk menghadapi hal tersebut, Hotel perlu mengefisienkan operasionalnya untuk meningkatkan revenue agar bisa 'Survive' dari pandemi ini. Maka dari itu, Kami akan melakukan Exploratory Data Analysis dengan database 'Hotel Booking Demand' untuk mencari apa yang bisa ditingkatkan dan diperbaiki dari sebuah operasional hotel.

**Maka, Business Problem yang akan kita bahas adalah**
1. Menaikkan Revenue
2. Menurunkan cancellation rate
3. Meningkatkan occupancy rate

**Dari ketiga business problem diatas, dapat kita turunkan menjadi business question sebagai acuan kita dalam menganalisis data "Hotel Booking Demand".**
1. Bagaimana durasi menginap di city hotel dan resort hotel?
2. Dari 2015-2017 bagaimana tren jumlah pengunjung yang menginap di City Hotel dan Resort Hotel?
3. Dari 2015-2017 bagaimana tren pengunjung yang menginap per bulannya di masing-masing hotel?
4. Apa Tipe deposit yang memiliki tingkat pembatalan paling tinggi?
5. Tipe hotel mana kah yang memiliki tingkat pembatalan pesanan tertinggi?
6. Market Segment mana yang memiliki tingkat pembatalan tertinggi?
7. Apakah variabel tipe deposit dan pembatalan saling berhubungan?
8. Bagaimana hubungan perbedaan reserved room dan assigned room terhadap cancellation??
9. Bagaimana perbandingan pemesanan sebagai tamu baru dan pemesanan sebagai tamu berulang ?
10. Bagaimana perbandingan jumlah pengunjung dewasa, anak-anak, dan bayi untuk city hotel dan resort hotel? 

## Exploratory Data Analysis

**Tahapan yang dilakukan dalam EDA ini adalah sebagai berikut:**
1. Data Wrangling - Data Preparation
2. Data Analysis
3. Kesimpulan & Rekomendasi - Saran

### 1. Data Wrangling
- Pengecekan tipe data dilakukan dengan syntax `df.dtypes`
- Pengecekan statistik deskriptif menggunakan `df.describe()`
- Pengecekan missing values pada data dilakukan dengan syntax `df.isnull().sum()`

### 2. Data Analysis

#### BQ1 - Bagaimana durasi menginap di city hotel dan resort hotel?
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20180838.jpg)

Insight :
- 47% pelanggan menginap di City Hotel dengan durasi lebih sedikit dari rata-rata durasi menginap, hanya 1-3 hari
- Hanya 19% pelanggan di City Hotel dengan durasi lama/long stay
- Pelanggan yang menginap di Resort Hotel memiliki kecenderungan yang sama antara yang menginap dalam 1-3 hari dan lebih dari 4 hari/long stay

#### BQ2 - Dari 2015-2017 bagaimana tren jumlah pengunjung yang menginap di City Hotel dan Resort Hotel?
City Hotel
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20180928.jpg)

Resort Hotel
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20180938.jpg)

Insight : 
- Dalam data City Hotel pengunjung yang menginap hingga Check-Out pada tahun 2015 sebanyak 7624, tahun 2016 sebanyak 22553, tahun 2017 sebanyak 15743. Terdapat kenaikan di 2015-2016 sebanyak 14929 pengunjung atau sebanyak 195% tetapi mengalami penurunan di tahun 2017 yaitu sebanyak 7080 pengunjung atau 31% dari tahun sebelumnya.
- Dalam data Resort Hotel pengunjung yang menginap hingga Check-Out pada tahun 2015 sebanyak 6077, tahun 2016 sebanyak 13423, dan tahun 2017 sebanyak 9066. Terdapat kenaikan di 2015-2016 sebanyak 7346 pengunjung atau sebanyak 120% tetapi mengalami penurunan di tahun 2017 yaitu sebanyak 4357 pengunjung atau 32% dari tahun sebelumnya.

#### BQ3 - Dari 2015-2017 bagaimana tren pengunjung yang menginap per bulannya di masing-masing hotel?
Insight :
- Tahun 2015 terdapat peningkatan pengunjung City Hotel antara bulan Juli-September dan mengalami penurunan di bulan November, sedangkan pengunjung Resort Hotel selama Juli-Desember tidak banyak mengalami fluktuasi
- Tahun 2016 terdapat peningkatan pengunjung City Hotel secara bertahap dari bulan Januari hingga Juni, walaupun terdapat penurunan di bulan Juli namun mengalami bounce back di bulan Agustus dan mencapai puncaknya di bulan Oktober, lalu mengalami penurunan sampai akhir tahun. Resort Hotel juga mengalami tren kenaikan dan penurunan yang tidak banyak selisihnya tiap bulan, mengalami puncak di bulan Oktober, namun nilainya hanya setengah dari City Hotel
- Tahun 2017 terdapat peningkatan pengunjung City Hotel antara bulan Januari-Mei dan mengalami penurunan Juni-Agustus, sedangkan Resort Hotel di saat yang sama mendapatkan pengunjung yang tidak banyak berubah jumlahnya tiap bulan

#### BQ 4 - Apakah Tipe deposit yang memiliki tingkat pembatalan paling tinggi?
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20181044.jpg)
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/1.png)

Insight :
- Pemesanan dengan tipe deposit 'No Deposit' adalah tipe deposit yang paling banyak dengan presentase sebesar 87.65% dari total jumlah pesanan. 
- Berdasarkan analisis bivariate diatas, dari total seluruh pesanan di hotel tersebut, pesanan yang tidak memberikan deposit, memiliki tingkat pembatalan tertinggi, sebesar 24.87%.

#### BQ 5 - Tipe hotel mana kah yang memiliki tingkat pembatalan pesanan tertinggi?
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20181118.jpg)
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/2.png)

Insight :
- Tipe hotel yang paling banyak dipesan adalah city hotel dengan presentase 66.45% dari seluruh pemesanan.
- Dari hasil analisis bivariate diatas, dapat terlihat bahwa tingkat pembatalan di city hotel hampir 3x lipat dibanding Resort Hotel.
- Dari analisis multivariate diatas, dapat terlihat bahwa tingkat pembatalan tertinggi berasal dari Hotel yang bertipe City Hotel dengan tanpa deposit.

#### BQ 6 - Market Segment mana yang memiliki tingkat pembatalan tertinggi?
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20181146.jpg)

Insight :
- Pemesanan hotel terbanyak melalui Online Travel Agent sebesar 47.3% dari total seluruh pemesanan
- Dari hasil analisis bivariate diatas, dapat terlihat bahwa tingkat pembatalan tertinggi berasal dari Online TA sebesar 17.37%.
- Dari hasil analisis multivariate diatas, dapat terlihat bahwa tingkat pembatalan tertinggi berasal dari Online TA dengan tipe deposit 'No Deposit'.

#### BQ 7 - Apakah variabel tipe deposit dan pembatalan saling berhubungan?
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/Screenshot%202022-06-19%20181241.jpg)

Insight :
- Dari hasil uji Chi-Square Test, didapatkan bahwa nilai p < 0.05 yang berarti variabel tipe deposit dan pembatalan merupakan variabel yang dependen satu sama lain.

#### BQ 8 - Bagaimana hubungan perbedaan reserved room dan assigned room terhadap cancellation?
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/4.png)

Insight:
- 94.62% tamu yang kamarnya mengalami perubahan dari yang dipesan tidak membatalkan pesanannya. 
- Sedangkan hanya 5.38% tamu yang kamarnya mengalami perubahan dari yang dipesan membatalkan pesanannya

#### BQ 9 - Bagaimana perbandingan pemesanan sebagai tamu baru dan pemesanan sebagai tamu berulang ?
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/5.png)

Insight :
- Pemesanan yang dilakukan oleh tamu baru jauh lebih banyak yaitu sebanyak 115.580 dibandingkan pemesanan oleh tamu berulang yaitu sebanyak 3.810.
- Pemesanan yang dilakukan oleh tamu baru pada City Hotel memiliki jumlah jauh lebih banyak yaitu sebesar 77.298 dibandingkan resort hotel sebanyak 38.282
- Jumlah pemesanan yang dilakukan oleh tamu berulang pada City Hotel tidak berbeda jauh dari Resort Hotel, dengan city hotel sebanyak 2.032 tamu berulang dan resort hotel sebanyak 1.778 tamu berulang
- Secara total pesanan jumlah tambu baru memiliki persentase jauh lebih besar yaitu 96.81% dibandingkan tamu berulang sebesar 3.19%

#### BQ 10 - Bagaimana perbandingan jumlah pengunjung dewasa, anak-anak, dan bayi untuk city hotel dan resort hotel? 
![](https://github.com/reyhanalif/Hotel-Booking-Demand-EDA/blob/main/DataViz/6.png)

Insight : 
- Jumlah tamu dewasa pada city hotel adalah sebanyak 146.838, lebih banyak hampir dua kali lipat dari resort hotel yang memiliki jumlah sebanyak 74.798
- Jumlah tamu anak-anak pada city hotel adalah sebanyak 7.248, lebih banyak dari resort hotel yang memiliki jumlah sebanyak 5.155
- Jumlah tamu bayi pada city hotel adalah sebanyak 392, lebih sedikit dari resort hotel yang memiliki jumlah sebanyak 557

## Results
**- Business Question 1:**
    - City Hotel yang bertempat di kota Lisbon, Portugal memiliki banyak potensi wisata sejarah dan budaya sehingga City Hotel memiliki banyak peminat ditambah dengan mudahnya wisatawan asing datang melalui bandara internasional
    - Resort Hotel berlokasi di Algarve daerah selatan negara Portugal yang memiliki pemandangan pantai dan suasana desa pesisir yang sepi serta kota pelabuhan yang memiliki nilai sejarah yang panjang.

**- Business Question 2-5:**
    - Dari beberapa hasil analisis bivariate-multivariate yang telah dilakukan, pemesanan dengan 'No Deposit' selalu memiliki tingkat pembatalan paling tinggi. Terutama 'No Deposit' pada pemesanan City Hotel, dan 'No Deposit' pada pemesanan melalui Online Travel Agent.
    - Dengan analisa Chi-Squared, ditemukan bahwa variabel tipe deposit dan variabel pembatalan, adalah variabel yang saling berhubungan.

**- Business Question 6-8:**
    - Pembatalan pesanan saat terjadi perubahan jenis kamar akibat kamar yang dipesan tidak tersedia memiliki jumlah yang relatif lebih sedikit dibandingkan tamu yang tidak membatalkan pesanannya, yaitu sebesar 5.38%. Ini berarti sebagian besar tamu walaupun mendapat perubahan kamar dari yang telah dipesan, mereka tetap tidak membatalkan pesanannya.  
    - Dari perbandingan jumlah pemesanan tamu baru dan pemesanan tamu berulang, didapat bahwa jumlah pemesanan tamu baru persentasenya jauh lebih besar dibandingkan tamu berulang yang hanya sebesar 3.19%. Berdasarkan jurnal berjudul "Why Customers Don’t Revisit in Tourism and Hospitality Industry?" oleh Jing-Rong Chang, alasan tamu tidak melakukan pemesanan kembali dapat disebabkan karena aksesabilitas lokasi hotel yang kurang strategis, harga yang tidak sesuai dengan fasilitas, kebersihan hotel, dan review negatif di internet.
    - Data jumlah tamu hotel berdasarkan kategori usia menunjukkan bahwa tamu dewasa pada City Hotel memiliki jumlah hampir 2x lipat dari Resort Hotel. Meskipun jumlah tamu dewasa kedua hotel memiliki selisih yang signifikan, data jumlah tamu dengan kategori Anak-Anak dan Bayi memiliki selisih yang tidak jauh berbeda. City Hotel memiliki jumlah tamu dengan kategori usia Anak-Anak lebih banyak daripada Resort Hotel, namun Resort Hotel memiliki jumlah lebih banyak pada kategori usia bayi dibandingkan City Hotel. Ini artinya proporsi jumlah tamu yang membawa anak dan bayi di Resort Hotel lebih besar daripada City Hotel.

## Business Recommendations:
**- Business Question 1:**
    - City Hotel dapat menawarkan kemudahan dan promosi untuk penginapan yang lama/long stay serta menambahkan pilihan paket wisata sehingga wisatawan tertarik datang dan menginap lebih lama.

**- Business Question 2-5:**
    - Berdasarkan studi yang dilakukan pada tahun 2019 oleh Fernández, Vall-Llosera, dan Moya yang berjudul "ANALYSIS OF OTA IMPACT ON HOTEL RESERVATIONS", ditemukan bahwa pemesanan hotel melalui Online Travel Agents (OTA) mencakup hingga 93,2% dari total pemesanan hotel. Hal ini selaras dengan data set yang kami gunakan, dimana pemesanan hotel paling besar berasal dari OTA (47%). Berdasarkan hal tersebut, `Divisi Marketing` dari hotel ini bisa memfokuskan promosi dan marketing melalui channel OTA agar dapat menjangkau pasar yang paling luas. Ditambah lagi, berdasarkan data dari PhocusWright (Perusahaan riset yang berfokus ke Travel industry) 60% dari traveler, akan mengunjungi OTA ketika melakukan riset untuk opsi ketika nanti berpergian. Dengan melakukan marketing melalui OTA, sebuah hotel akan bisa menjadi 'stand-out' ketika ditemukan oleh calon pengunjungnya di OTA. 
    - Tipe deposit 'No Deposit' selalu memiliki tingkat pembatalan pesanan paling tinggi. Sebaliknya, tipe deposit 'refundable' dan 'non-refundable' selalu memiliki tingkat pembatalan lebih rendah. Ditambah juga, setelah dilakukan chi-squared test antara variabel deposit types dan pembatalan pesanan, ditemukan bahwa kedua variabel tersebut saling berhubungan. Hal ini selaras dengan studi yang dilakukan oleh Chayanon Tongmungkorn (2021) dimana beliau menemukan bahwa tipe deposit merupakan salah satu variabel yang paling berpengaruh terhadap keputusan pelanggan untuk melakukan pembatalan pesanan. Berdasarkan studi dari Chen, Schwartz, dan Vargas (2011) Hotel bisa mengoptimisasi sistem revenue nya dengan memvariasikan kebijakan pembatalan pemesanan seperti penggunaan deposit, deadline pembatalan, dan pemberian penawaran yang menarik. Berdasarkan hal tersebut divisi `executive office` yang bertugas untuk mengatur segala operasional hotel, bisa mengimplementasikan pemberian discount jika seorang pelanggan melakukan pemesanan dengan tipe deposit 'refundable' dan memberi diskon + penawaran lain untuk pelanggan yang memilih tipe deposit 'non-refundable'. Selain itu, Hotel juga bisa memberikan deadline pembatalan yang ketat untuk pemesanan yang bertipe 'no deposit'.

**- Business Question 6-7:**
    - Untuk menarik tamu lama datang kembali, kebersihan hotel harus selalu diperhatikan, `Departemen Houeskeeper` dapat membuat jadwal pembersihan yang ketat dan laporan terkontrol untuk memastikan kebersihan hotel terjaga. Kemudian `Departemen Sales & Marketing` yang bertanggung jawab mengelola situs hotel harus dapat mengidentifikasi komentar negatif pelanggan di internet serta menanggapinya dengan cepat dan hati-hati. Lokasi yang kurang strategis juga dapat diantisipasi dengan menyediakan shuttle bus yang terkoneksi ke tempat wisata atau transportasi publik, hal ini dapat disiapkan oleh `Departemen Front Office`
    - Resort Hotel banyak dipilih oleh tamu yang memiliki anak-anak dan bayi. Menurut **Mags Huggins** yang telah bekerja di industri turisme lebih dari 20 tahun, hotel perlu menemukan cara untuk membedakan diri mereka sendiri untuk menarik tamu. Banyak hotel telah sukses melakukan pemasaran diri mereka sendiri dengan salah satu segmen yang tumbuh paling cepat adalah keluarga. Untuk menarik jumlah tamu yang datang, `Departemen House Keeper` sebagai pengelola public area hotel berkoordinasi dengan `Departemen Financial` dapat menambah fasilitas untuk tempat bermain anak-anak dan `Departemen Sales & Marketing` yang mengurus relasi publik dapat membuat acara eventual seperti cooking class untuk anak-anak dan magic show. Kemudian `Departemen Food & Beverage` yang mengelola hidangan hotel dapat membuat pilihan menu makan pagi yang menarik untuk anak-anak. `Departemen Sales & Marketing` yang bertanggung jawab mengelola situs hotel juga dapat menampilkan banyak gambar anak-anak bersenang-senang serta ulasan dari orang tua yang membawa anak-anak pada laman situs hotel. 
