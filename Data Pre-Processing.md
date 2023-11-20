Sebagai system yang dapat belajar dari data. ML tidak dapat secara langsung digunakan begitu saja pada semua data, namun sebuah data harus melalui serangkaian proses terlebih dahulu agar dapat diterima dengan baik oleh model. Beberapa proses yang umum digunakan sebelum masuk kedalam pemodelan machine learning anatara lain yaitu,

# 1.	Exploratory Data Analysis
- Pada kasus nyata, jarang sekali ada data yang sudah bersih sejak awal. Mayoritas data yang ditemui mengandung noise seperti outlier, missing value dll. Untuk mengetahui data tersebut terdapat noise atau tidak maka dicari menggunakan EDA. 
- EDA atau analisis eksplorasi data merupakan serangkaian teknik dan metode yang digunakan untuk menggali dan memahami karakteristik utama dari dataset sebelum menjalankan analisis lebih lanjut atau membangun model. 
- Tujuan EDA adalah untuk mengidentifikasi pola, anomali, dan hubungan dalam data secara deskriptif.

Berikut ini adalah tahapan EDA yang umum digunakan,

**1. Pahami tujuan analisis data**
- Tentukan tujuan analisis data yang diinginkan
- Buatlah pertanyaan-pertanyaan yang ingin dijawab

**2. Sumber Data**
- Pastikan sumber data yang digunakan adalah data public atau data privat yang telah diberi izin
- Setelah data diperoleh lakukan import data ke Bahasa pemrograman seperti Python dan R menggunakan library yang compatible.

**3. Tipe Data** 
- Tipe data menjadi hal yang sangat penting pada masing-masing kolom/fitur dalam data, hal tersebut dikarenakan tipe data akan menentukan cara pengolahan pada masing-masing kolom
- Tipe data umumnya terdiri dari 2 jenis yaitu kuantitatif/numerik dan kualitatif/kategorik.
  - Numerik, umumnya adalah data yang terdiri dari angka yang biasa didapat dari pengukuran dimana numerik terbagi menjadi dua yaitu diskrit dan kontinu. 
      1.	Data diskrit adalah data numerik dalam bentuk bilangan bulat dan tidak dapat dibagi ke dalam unit yang lebih kecil. Data ini umumnya merupakan data hasil perhitungan. 
      2.	Data kontinu adalah data numerik dalam bentuk bilangan decimal dan diperoleh dari hasil pengukuran.
  - Kategorik, data yang dapat dikelompokkan dan terbagi berdasarkan karakteristik atau ciri khasnya masing-masing. Terbagi menjadi dua yaitu data nominal dan data ordinal. 
      1.	Data nominal, adalah data jenis pengelompokan data yang tidak memiliki keterkaitan dengan data lainnya dan tidak memiliki arti khusus. Jadi, data ini dapat dibedakan tanpa harus mengurutkan atau dibandingkan dengan data lainnya.
      2.	Data ordinal, Berlawanan dari kata nominal, data ordinal adalah jenis pengelompokan data yang memiliki urutan atau harus disusun secara berurutan dengan mekanisme peringkat.

**4. Seleksi Fitur Manual**
- Seleksi fitur manual atau memilih kolom secara manual dan menghapus kolom yang tidak digunakan 
- Tahapan ini dilakukan karena dalam data seringkali tidak semua data digunakan hanya data tertentu saja yang umum digunakan. 
- Pemilihan fitur secara manual sering kali melibatkan domain bisnis yang ada.
- Selain dengan cara manual terdapat juga metode-metode khusus pemilihan feature 

**5.	Mengubah Nama kolom** 
- Nama kolom pada data yang pertama kali diperoleh seringkali tidak representative, sehingga harus diubah

**6.	Menghapus baris duplikat** 
-	Baris yang mengalami duplikasi perlu dihapus karena dapat memperburuk kualitas data. Hal tersebut disebabkan oleh duplikasi data akan mengurangi keragaman data yang menjadikan suatu data tidak representative. 
-	Dupplikasi data juga akan menjadikan model tidak belajar dengan baik karena selalu diberi contoh yang sama.

**7.	Menghapus Missing or Null Values**
-	Data yang hilang atau kosong akan merusak dan mengganggu pemodelan data. 
- Untuk mengatasinya dapat dilakukan dengan beberapa cara yaitu 
  a.  Penghapusan data, Teknik ini merupakan Teknik yang paling mudah digunakan namun data missing values dapat dihapus jika totalnya hanya < 5 % dari jumlah data 
  b.	Imputasi, dilakukan jika jumlah missing lebih dari 5 %. Imputasi adalah Teknik mengisi data. Nantinya data yang missing dapat diisi dengan,
    1.	Jika data numerik, dapat diisi median atau mean 
    2.	Jika data kategorik, dapat diisi dengan nilai kategori ‘lainnya’ atau memberikan nilai maksimum


**8.	Deteksi Outliers**
- Outliers atau nilai yang tidak wajar dapat merusak model karena nilai tersebut merupakan nilai yang sangat jarang muncul. 

**9. Univariate Analysis** 
- Univariate analysis adalah Teknik analisis dan eksplorasi pada satu kolom data.
- Analisis yang dilakukan umumnya terdiri dari,
  a.	Menghitung statistika deskriptif
  b.	Melihat nilai outlier 
  c.	Melihat Distribbusi datanya
  d.	Mengetahui frekuensi kemunculan data 

**10.	Bivariate Analysis**
- Bivariate analysis adalah Teknik analysis dan eksplorasi pada dua kolom dalam dataset.
- Umumnya menggunakan 1 kolom predictor dan 1 kolom target.  
- Analisis yang dilakukan umumnya menggunakan matriks korelasi dan scatter plot. 
  a. Matriks korelasi untuk melihat hubungan antar fitur 
  b.	Scatter plot digunakan untuk melihat sebaran data dan gambaran pola keseluruhan dari dua kolom

**11.	Multivariate Analysis**
- Multivariate analysis adalah Teknik analysis dan eksplorasi pada lebih dari dua kolom dalam dataset
- Analisis ini digunakanuntuk mengtahui seberapa pengaruh antar fitur dalam data.
- Umumnya menggunakan heat maps 

# 2.	Data Normalization
- Normalisasi data adalah Teknik untuk membuat data menjadi normal. Maksud normal disini adalah data memiliki nilai yang seragam dengan rentang yang sama. 
- Suatu data tidak normal karena pada masing-masing kolom pada dataset memiliki satuan yang berbeda. 
- Ada beberapa cara dalam normalisasi data yaitu,
  a. Simple Features Scalling, merupakan scalling yang dilakukan dengan cara nilai fitur lama dibagi dengan nilai maksimal pada fitur. Pembagian tersebut akan menghasilkan range 0 – 1. 
  b. Min-Max Normalization, serupa dengan simple features scalling dengan memberikan nilai pengurangan fitur minimal. 
  c. Mean Normalization, Teknik ini mengandalkan nilai mean suatu fitur kemduian dihitung dengan nilai maksimal dan minimal dari fitur tersebut. 
  d. Z-Score Normalization, normalisasi data yang digunakan untuk mengubah setiap nilai dalam suatu distribusi menjadi nilai yang memiliki mean (rerata) nol dan deviasi standar satu. Ini membuat distribusi data menjadi distribusi normal standar atau disebut juga distribusi Z.
  e. Z-score normalization cocok digunakan ketika data memiliki distribusi yang mendekati distribusi normal dan normalisasi ini tidak cocok jika data memiliki distribusi yang signifikan dan tidak simetris atau jika kita ingin mempertahankan interpretasi nilai asli dari data.

# 3.	Data Discretization/Binnning/Kategorisasi Data
- Data discretization adalah proses mengubah data numerik menjadi kategorik 
- Kenapa perlu melakukan data discretization?
    a. Data numerik seringkali terdapat nilai outlier sehingga memnyulitkan perhitungan
    b. Mempersulit kerja algortima tertentu
- Beberapa Teknik yang digunakan untuk discretization data,
    a. Teknik manual, Teknik ini akan mengelompokan data sesuai kenginan pemilik data
    b. Teknik linspace, Teknik ini akan mengelompokan data dengan jarak yang sama. 
    c. Teknik Quantile, Teknik ini mengelompokan data berdasarkan persentile. 
    d. Teknik Clustering, Teknik ini mengelompokan data berdasarkan kemiripan antar fiturnya. 

# 4.	Encoding 
- Encoding adalah transformasi dari data kategorik ke data numerik. 
- Tahapan ini sering digunakan karena banyak algoritma machine learning menggunakan data numerik 
- Ada beberapa tahapan encoding yang umum digunakan,
  a. Label Encoding, Teknik encoding yang mengubah setiap kategori menjadi numerik Tunggal
  b. One-Hot Encoding, mengubah setiap kategori menjadi vektor biner dengan panjang sesuai dengan jumlah kategori

# 5.	Feature Engineering 
- Feature engineering adalah  proses menciptakan, mengubah, atau memilih fitur (variabel) dalam suatu dataset dengan tujuan meningkatkan kinerja model atau mempermudah pemahaman data.  
- Secara gambaran besar, berbagai tahapan yang dilakukan sebelumnnya merupakan gambaran besar yang termasuk kedalam Feature Engineering. 
- Karena tujuannya meningkatkan kinerja model, sering sekali Feature Engineering dilakukan setelah pemodelan dilakukan. Ada beberapa hal yang umum dilakukan dalam Feture engineering.
  a.	Membuat kolom baru
  b.	Transformasi variable
  c.	Encoding variable
  d.	Scalling dan normalisasi
  e.	Handling missing values
  f.	Binning
  g.	Reduksi dimensi
  h.	Handling outlier

# 6.	Feature Selection
- Seleksi fitur yaitu memilih kolom yang akan digunakan dalam data disebabkan hal tertentu yaitu,
  a. Untuk melihat seberapa pengaruh fitur terhadap target
  b. Tidak semua fitur digunakan untuk analisis.
  c. Semakin banyak fitur akan semakin kompleks
  d. Semakin banyak fitur maka komputasi semakin berat
  e.	Menghilangkan informasi yang tidak penting
  f. Mengurangi overfitting data 

-	Beberapa Teknik seleksi fitur yang umum digunakan adalah 
  a. Metode filter, metode ini menggunakan analisis hasil statistika berdasarkan skor suatu fitur dan hubungannya dengan variable target. Beberapa Teknik metode filter ini yaitu
    - Chi-square, Mengukur independensi antara variabel kategorikal. Chi-squared test dapat digunakan untuk menilai apakah ada hubungan signifikan antara variabel kategorikal dan variabel target.
    - Korelasi koefisien, Mengukur derajat hubungan linier antara dua variabel. Filter selection dapat menggunakan koefisien korelasi untuk menilai relevansi antara setiap fitur dan variabel target. Menggunakan heatmap 
    - ANOVA, Digunakan untuk menilai perbedaan mean antara dua atau lebih kelompok. ANOVA dapat digunakan untuk memilih fitur-fitur yang memiliki perbedaan rata-rata yang signifikan antara kelas-kelas dalam variabel target.
  b. Metode Wrapped, yaitu membungkus tiap fitur yang ada lalu diproses oleh algoritme tertentu dan menghasilkan akurasi. Fitur dengan akurasi terbaik yang akan dipilih. Salah satu tekniknya adalah forward dan backward selection. 
  c. Embedded Method, yaitu menerapkan seleksi fitur saat dataset dimodelkan sehingga ketika pemodelan selesai maka Teknik ini juga selesai. Ada beberapa Teknik yang digunakan yaitu
    - Lasso
    - Ridge regression
    - Elastic nets 
    - Feature importance, Teknik ini bekerja pada algoritma tree based models. 
    - Gini indeks 

# 7.	Feature Extraction 
- Jika seleksi fitur memilih fitur terbaik dari banyaknya fitur yang tersedia. Namun ketika kita memilih fitur terbaik apakah yang tidak baik harus dihapus ? untuk menghindari penghapusan fitur karena berpotensi membuang informasi yang bermanfaat maka dapat dilakukan dengan feature extraction
- Feature extraction adalah mereduksi feature (bukan dihapus) lalu menghasilkan fitur baru untuk meminimalisir hilangnya informasi dari keseluruhan feature. 
- Selain mengurangi potensi hilangnya informasi, Feature extraction memungkinkan untuk mengubah data yang dimensi tinggi (fitur nya banyak) menjadi data yang berdimensi rendah (fiturnya sedikit). 
- Salah satu Teknik feature extraction adalah PCA 


