# Laporan Proyek Machine Learning - Henry Dwi Prana Sitepu

## Kesehatan
Diabetes adalah penyakit kronis serius yang memengaruhi jutaan orang di seluruh dunia. Penyakit ini terjadi ketika tubuh tidak dapat memproduksi insulin yang cukup, atau tidak dapat secara efektif menggunakan insulin yang dihasilkannya, yang menyebabkan peningkatan kadar glukosa dalam darah (gula darah) [1]. Komplikasi jangka panjang dari diabetes dapat sangat merusak dan mencakup penyakit jantung, stroke, gagal ginjal, kebutaan, dan amputasi [2]. Deteksi dini dan diagnosis yang tepat waktu sangat penting untuk manajemen penyakit yang efektif dan pencegahan komplikasi parah. Namun, diagnosis diabetes seringkali membutuhkan serangkaian tes laboratorium yang bisa memakan waktu dan biaya, terutama di daerah dengan akses terbatas ke fasilitas medis.

Proyek ini bertujuan untuk mengatasi tantangan diagnosis dini diabetes dengan mengembangkan model klasifikasi berbasis machine learning. Kami akan menggunakan Pima Indians Diabetes Database, sebuah dataset yang dikumpulkan oleh National Institute of Diabetes and Digestive and Kidney Diseases [3]. Dataset ini berfokus pada data medis pasien wanita keturunan Indian Pima, yang memiliki prevalensi diabetes tipe 2 yang tinggi. Dengan memanfaatkan data ini, kita dapat membangun sistem prediktif yang berpotensi membantu tenaga medis dalam mengidentifikasi individu berisiko tinggi lebih awal, sehingga intervensi dapat dilakukan sebelum komplikasi berkembang.

**Mengapa Masalah Klasifikasi Diabetes pada Pima Indians Dataset Perlu Diselesaikan?**

Penyelesaian masalah klasifikasi diabetes menggunakan Pima Indians Dataset memiliki relevansi dan urgensi yang signifikan:

  1) Pentingnya Diagnosis Dini: Diabetes yang tidak terdiagnosis dan tidak diobati dapat menyebabkan konsekuensi kesehatan yang parah.
     Model prediksi dapat menjadi alat screening awal yang non-invasif, membantu mengidentifikasi individu yang perlu menjalani tes lebih lanjut.
     Hal ini dapat meningkatkan efisiensi sistem kesehatan dan hasil pasien, terutama di populasi yang rentan [4].
     
  2) Ketersediaan Data dan Kompleksitas yang Sesuai: Pima Indians Dataset menyediakan data riil yang representatif untuk masalah diagnosis diabetes. 
     Meskipun memiliki beberapa fitur numerik, dataset ini relatif kecil (768 sampel) dan tidak memerlukan preprocessing yang sangat kompleks. 
     Ini menjadikannya ideal untuk demonstrasi dan pembelajaran algoritma klasifikasi dasar tanpa terjebak dalam kompleksitas data yang berlebihan. 
     Penelitian sebelumnya telah menunjukkan bahwa algoritma machine learning sederhana seperti Regresi Logistik dan Support Vector Machine dapat mencapai akurasi yang baik pada dataset ini [5], [6].
  
  3) Pengembangan Alat Prediktif Medis: Proyek ini berkontribusi pada upaya yang lebih luas dalam penerapan kecerdasan buatan di bidang kedokteran.
     Dengan membangun model yang dapat memprediksi risiko diabetes, kita dapat mengeksplorasi potensi machine learning sebagai alat bantu keputusan klinis yang mendukung dokter dalam diagnosis dan perencanaan perawatan [4].
     
**Bagaimana Masalah Klasifikasi Diabetes Diselesaikan?**

Untuk menyelesaikan masalah klasifikasi diabetes menggunakan Pima Indians Dataset, kami akan mengikuti alur kerja machine learning standar yang terbukti efektif:

  1) Pengumpulan dan Pemahaman Data: Data akan diperoleh dari Pima Indians Diabetes Database. Tahap ini melibatkan eksplorasi data awal (EDA) untuk memahami distribusi setiap fitur
     (misalnya, glukosa, tekanan darah, BMI), mengidentifikasi potensi anomali atau nilai hilang, dan melihat bagaimana fitur-fitur ini berkorelasi dengan status diabetes [5].
     
  2) Pra-pemrosesan Data: Meskipun dataset ini relatif bersih, beberapa fitur mungkin memiliki nilai nol yang secara medis tidak masuk akal (misalnya, tekanan darah nol). 
     Tahap ini akan melibatkan penanganan nilai-nilai tersebut, seperti imputasi dengan nilai rata-rata atau median, atau penghapusan jika dianggap tidak valid. 
     Normalisasi atau standardisasi fitur juga mungkin diperlukan untuk mengoptimalkan kinerja beberapa algoritma [5].
     
  3) Pemisahan Data Latih dan Uji: Dataset akan dibagi menjadi training set dan testing set (misalnya, 70:30 atau 80:20). Training set digunakan untuk melatih model, 
     sementara testing set digunakan untuk mengevaluasi kinerja model pada data yang belum pernah dilihat, memastikan kemampuan generalisasi model.

  4) Pemilihan dan Pelatihan Model Klasifikasi: Beberapa algoritma klasifikasi dasar yang cocok untuk masalah ini akan dipilih. 
     Contohnya meliputi Regresi Logistik (model linier yang memprediksi probabilitas biner), K-Nearest Neighbors (KNN) (algoritma berbasis instansi), dan/atau Support Vector Machine (SVM). Model akan dilatih menggunakan training set.

  5) Evaluasi Model: Kinerja model akan dievaluasi secara komprehensif menggunakan metrik yang relevan untuk masalah klasifikasi biner, seperti Akurasi, Precision, Recall, F1-Score, dan Confusion Matrix.
     Karena masalah kesehatan, recall (kemampuan model untuk menemukan semua kasus positif) mungkin menjadi metrik yang sangat penting untuk meminimalkan false negatives (kasus diabetes yang tidak terdeteksi) [6].

  6) Interpretasi dan Validasi: Hasil evaluasi akan diinterpretasikan untuk memahami seberapa baik model dapat memprediksi status diabetes. Jika diperlukan, proses ini mungkin melibatkan penyetelan hyperparameter atau pemilihan model yang berbeda untuk mengoptimalkan kinerja.
     Melalui langkah-langkah ini, kami berupaya membangun model klasifikasi yang efektif dan dapat diandalkan untuk mendeteksi diabetes, yang berpotensi menjadi alat bantu yang berharga dalam upaya deteksi dini penyakit ini.

Referensi

[1] World Health Organization, "Diabetes," WHO, 2024. [Online]. Available: https://www.who.int/news-room/fact-sheets/detail/diabetes.

[2] Centers for Disease Control and Prevention, "Type 2 Diabetes," CDC, 2024. [Online]. Available: https://www.cdc.gov/diabetes/basics/type2.html.

[3] V. Harrison, "Pima Indians Diabetes Database," UCI Machine Learning Repository, D. Dua and C. Graff, Eds., Irvine, CA: University of California, School of Information and Computer Science, 1990. [Online]. Available: https://archive.ics.uci.edu/dataset/45/pima+indians+diabetes.

[4] L. K. H. Lau, C. K. K. Lee, and A. C. T. Li, "Machine learning in diabetes management: A review," Journal of Diabetes Science and Technology, vol. 15, no. 1, pp. 200-210, Jan. 2021.

[5] K. Polat and S. Güneş, "Detection of diabetes disease using least square support vector machine and fuzzy logic," Expert Systems with Applications, vol. 36, no. 2, pp. 1007-1011, Mar. 2009.

[6] B. P. Singh, R. Singh, and S. Singh, "Comparative analysis of machine learning algorithms for diabetes prediction," in Proc. Int. Conf. on Advances in Computing and Communications (ICACC), Kochi, India, 2013, pp. 138-141

## Business Understanding

Klarifikasi Masalah

Bagian ini menguraikan secara spesifik permasalahan yang ingin diselesaikan dalam proyek ini, tujuan yang ingin dicapai, serta pendekatan solusi yang akan diterapkan.

## Problem Statements
Berdasarkan latar belakang mengenai prevalensi diabetes dan kebutuhan akan deteksi dini, serta karakteristik Pima Indians Diabetes Database, beberapa pernyataan masalah kunci dapat dirumuskan:

  1) Bagaimana cara membangun model klasifikasi machine learning yang efektif untuk memprediksi apakah seorang wanita keturunan Indian Pima berisiko terkena diabetes,
     berdasarkan data diagnostik yang tersedia?
     
  2) Algoritma klasifikasi dasar mana yang paling optimal dalam memprediksi diabetes pada dataset ini,
     dan bagaimana kita dapat mengidentifikasi algoritma yang memberikan keseimbangan terbaik antara kinerja (akurasi, presisi, recall) dan interpretasi? 
     
  3) Bagaimana performa model yang dibangun dapat dievaluasi secara komprehensif,
     khususnya dalam konteks medis di mana false negatives (kasus diabetes yang tidak terdeteksi) memiliki konsekuensi yang serius? 

## Goals

Tujuan dari proyek ini dirumuskan untuk secara langsung menjawab pernyataan masalah di atas:

  1) Membangun model klasifikasi machine learning yang mampu memprediksi diabetes dengan akurasi yang tinggi (target ≥70%) pada Pima Indians Diabetes Database. 
     Target akurasi ini ditetapkan dengan mempertimbangkan kompleksitas data medis dan tantangan diagnostik.
     
  2) Mengidentifikasi dan mengimplementasikan setidaknya dua algoritma klasifikasi dasar (misalnya, Regresi Logistik dan Support Vector Machine) pada Pima Indians Diabetes       Database, serta membandingkan kinerja masing-masing algoritma. 
     Perbandingan ini akan memberikan wawasan mengenai kekuatan dan kelemahan relatif setiap metode untuk masalah ini.

  3) Mengevaluasi kinerja model menggunakan metrik yang relevan seperti Akurasi, Precision, Recall, F1-Score, dan Confusion Matrix pada testing set.
     Penekanan khusus akan diberikan pada metrik recall untuk meminimalkan false negatives, yang sangat penting dalam aplikasi diagnostik medis.
     
## Solution Statements

Untuk mencapai tujuan yang telah ditetapkan, proyek ini akan mengimplementasikan pendekatan berbasis machine learning dengan menguji dan membandingkan dua algoritma klasifikasi yang berbeda. 
Setiap solusi akan diukur menggunakan metrik evaluasi yang jelas dan relevan dengan konteks medis.

  1) Pembangunan Model Klasifikasi Diabetes dengan Algoritma Regresi Logistik :

      - Deskripsi Solusi:  melatih model Regresi Logistik pada training set Pima Indians Diabetes Database. Sebelum pelatihan, fitur-fitur numerik akan menjalani                    preprocessing seperti penanganan nilai nol yang tidak valid (misalnya, mengganti nilai nol pada fitur seperti glukosa, tekanan darah, 
        dan BMI dengan median atau rata-rata) dan penskalaan (misalnya, Standard Scaler) untuk memastikan semua fitur memiliki skala yang seragam. Penyesuaian                       hyperparameter dasar akan dilakukan jika diperlukan.
    
      - Metrik Evaluasi: Akurasi, Precision, Recall, F1-score, dan Confusion Matrix pada testing set. Target recall untuk kelas positif (diabetes) adalah ≥60%, di samping           akurasi keseluruhan ≥70%.
    
      - Justifikasi: Regresi Logistik adalah model linear yang kuat, mudah diinterpretasikan, dan seringkali menjadi baseline yang baik untuk masalah klasifikasi biner, 
        terutama dalam aplikasi medis di mana interpretasi model penting.
    
  2) Pembangunan Model Klasifikasi Diabetes dengan Algoritma Support Vector Machine (SVM):

      - Deskripsi Solusi: Model Support Vector Machine (SVM) akan dilatih pada training set Pima Indians Diabetes Database. Seperti Regresi Logistik, data akan melalui              tahapan preprocessing yang sama (penanganan nilai nol dan penskalaan fitur). Eksplorasi hyperparameter seperti jenis kernel (misalnya, linear atau RBF) dan                  parameter regularisasi C akan dilakukan untuk mengoptimalkan batas keputusan SVM.
        
      - Metrik Evaluasi: Akurasi, Precision, Recall, F1-score, dan Confusion Matrix pada testing set.  target recall untuk kelas positif (diabetes) adalah ≥60%, di samping           akurasi keseluruhan ≥70%.

      - Justifikasi: SVM dikenal sangat efektif untuk masalah klasifikasi, bahkan ketika data tidak dapat dipisahkan secara linear. 
        Kemampuannya untuk menangani ruang fitur berdimensi tinggi (walaupun Pima Indians berdimensi rendah) dan menemukan hyperplane optimal menjadikannya pilihan yang             baik untuk dibandingkan dengan Regresi Logistik.

Dengan mengimplementasikan dan membandingkan kedua solusi ini, proyek ini diharapkan dapat mengidentifikasi algoritma yang paling efektif untuk diagnosis dini diabetes pada Pima Indians Diabetes Database, sekaligus memberikan analisis komprehensif tentang performa model yang diukur dengan metrik yang relevan secara klinis.

## Data Understanding

Bagian ini menyajikan detail mengenai data yang digunakan dalam proyek klasifikasi ini, yaitu Pima Indians Diabetes Database. 
Dataset ini merupakan salah satu dataset klasik yang banyak digunakan dalam penelitian machine learning untuk masalah klasifikasi biner, khususnya di bidang kesehatan. 
Fokusnya adalah pada diagnosis diabetes pada populasi wanita keturunan Indian Pima

Dataset ini dapat diakses dan diunduh dari Kaggle, sebuah platform populer untuk data science dan machine learning, melalui tautan berikut:
  - Sumber Dataset : https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database
 

### Variabel-variabel pada pima indians diabetes dataset adalah sebagai berikut:
- Pregnancies: Jumlah kehamilan yang dialami oleh pasien
- Glucose: Konsentrasi glukosa plasma (gula darah) 2 jam setelah tes toleransi glukosa oral. Ini adalah indikator utama kadar gula darah.
- BloodPressure: Tekanan darah diastolik (mm Hg).
- SkinThickness: Ketebalan lipatan kulit trisep (mm). Fitur ini seringkali dikaitkan dengan jumlah lemak tubuh.
- Insulin: Kadar insulin serum 2 jam (mu U/ml).
- BMI (Body Mass Index): Indeks Massa Tubuh(berat_badan(kg)/tinggi badan(m)) pangkat 2
- DiabetesPedigreeFunction: Fungsi silsilah diabetes. Ini menghitung kemungkinan seseorang mengembangkan diabetes berdasarkan riwayat keluarga.
- Age: Usia pasien (tahun).
- Outcome: Variabel target, menunjukkan apakah pasien menderita diabetes. Ini adalah variabel biner:
    - 0 (merepresentasikan tidak menderita diabetes)
    - 1 (merepresentasikan menderita diabetes)

**Pemahaman Data (Exploratory Data Analysis - EDA)**

  1) Pemuatan Data dan Inspeksi Awal
       - df.head(): Menampilkan beberapa baris pertama dari dataset. Ini memberikan gambaran cepat tentang bagaimana data terstruktur, nama-nama kolom, dan jenis nilai yang terkandung di dalamnya.
         
     
         ![head](https://github.com/user-attachments/assets/d9daa626-ed1c-43bc-904a-d176be953a25)

         
       - df.info(): Menyediakan ringkasan singkat tentang DataFrame, termasuk jumlah entri, jumlah kolom, tipe data masing-masing kolom (misalnya, int64, float64), dan keberadaan nilai non-null. Ini membantu dalam mengidentifikasi apakah ada kolom dengan nilai yang hilang secara eksplisit (NaN) pada tahap awal

        ![info](https://github.com/user-attachments/assets/3fa5df32-a77e-4505-ad86-fc958d3a0ba5)


  2) Statistik Deskriptif dan Identifikasi Nilai Tidak Masuk Akal
       - df.describe(): Menghasilkan statistik deskriptif untuk setiap kolom numerik, seperti hitungan (count), rata-rata (mean), standar deviasi (std), nilai minimum       
         (min), nilai maksimum (max), serta kuartil (25%, 50% / median, 75%).

         Seperti yang telah dibahas sebelumnya, observasi penting dari df.describe() adalah adanya nilai 0 pada kolom Glucose, BloodPressure, SkinThickness, Insulin, dan             BMI. Nilai nol untuk fitur-fitur ini secara medis tidak masuk akal (misalnya, tekanan darah nol atau BMI nol pada individu hidup). Ini mengindikasikan bahwa 0               sebenarnya mewakili nilai yang hilang (missing values), bukan pengukuran yang valid.

      
          ![describe](https://github.com/user-attachments/assets/14afcc96-01c3-4afa-889d-bb9aa0cf8c37)


         
  3) Persebaran Data (Boxplot)
     Menggunakan library seaborn yaitu boxplot() untuk melihat persebaran data dan untuk melihat outlier dari setiap fitur, berikut beberapa visualisasi yang dibuat:

       - Glucose
         
          ![glucose_boxplot](https://github.com/user-attachments/assets/9cf3bfdd-492e-481d-b87e-cf605614d703)


       - BMI
         
        ![bmi_boxplot](https://github.com/user-attachments/assets/9c9c93be-0494-4c69-860f-b942fa4ba7bc)

         
       - Insulin
         
         ![insulin_boxplot](https://github.com/user-attachments/assets/f0f02880-fc45-47dc-94ca-c26237fd258f)

  3) Visualisasi Distribusi Fitur
     Visualisasi ini memungkinkan kita melihat bentuk distribusi masing-masing fitur (misalnya, apakah terdistribusi normal, skewed, atau multimodal). Ini juga membantu          mengidentifikasi outlier atau anomali yang mungkin belum terdeteksi. Setelah imputasi, histogram juga menunjukkan bagaimana distribusi berubah setelah nilai nol diisi.
     
     ![histogram_features](https://github.com/user-attachments/assets/0986bf91-540d-43c2-8017-55fc31568578)


  4) Visualisasi Hubungan Fitur dengan Target (Box Plots)
     Box plot sangat efektif untuk membandingkan distribusi suatu fitur antara dua kelompok (diabetes vs. non-diabetes). Kita dapat melihat apakah ada perbedaan median,          rentang interkuartil, dan keberadaan outlier yang berbeda antara kedua kelas. Ini membantu mengidentifikasi fitur mana yang paling diskriminatif atau memiliki kekuatan      prediktif tinggi terhadap diabetes. Misalnya, Glucose dan BMI kemungkinan besar akan menunjukkan perbedaan distribusi yang signifikan antara kelompok sehat dan              diabetes.

     ![pair_plot](https://github.com/user-attachments/assets/d50d60be-80e5-4090-8304-65f891d7ce68)


  5) Analisis Korelasi
     Matriks korelasi menunjukkan kekuatan dan arah hubungan linear antara setiap pasangan fitur.

      ![corr_matrix](https://github.com/user-attachments/assets/2722d1a4-7619-49e1-8204-89544f732037)


## Data Preparation

  Tahap Data Preparation adalah fase krusial dalam siklus hidup proyek machine learning yang bertujuan untuk mengubah data mentah menjadi format yang bersih, relevan, dan sesuai untuk proses pemodelan. Kualitas data yang masuk ke dalam model secara langsung memengaruhi kinerja dan keandalan model yang dihasilkan. Pada proyek ini, proses persiapan data difokuskan pada penanganan nilai-nilai yang tidak valid, penanganan outlier, pembagian dataset, penanganan ketidakseimbangan kelas (dengan SMOTE), dan penskalaan fitur, memastikan data siap untuk algoritma klasifikasi.

  1) Penanganan Nilai tidak masuk akal atau tidak valid
      Setelah inspeksi awal pada tahap Data Understanding (terutama melalui df.describe()), ditemukan bahwa beberapa kolom fitur (Glucose, BloodPressure, SkinThickness,Insulin, BMI) memiliki nilai minimum 0. Nilai 0 pada fitur-fitur ini secara medis tidak mungkin terjadi pada individu hidup dan oleh karena itu dianggap sebagai representasi dari nilai yang hilang (missing values) atau data yang tidak valid.

      Untuk mengatasi hal ini, pendekatan yang diambil adalah menghapus seluruh baris (sampel) dari dataset di mana salah satu atau lebih dari fitur-fitur ini memiliki nilai 0.

     **Tujuan :**  
        - Akurasi Data: Nilai 0 yang implausible akan mendistorsi statistik deskriptif dan analisis, serta menyesatkan model. Dengan menghapus baris yang mengandung nilai-            nilai ini, kita memastikan bahwa model dilatih hanya pada data yang secara medis valid.
    
        - Performa Model: Banyak algoritma machine learning sensitif terhadap nilai yang tidak valid atau outlier. Menghapus baris yang bermasalah dapat mencegah model mempelajari pola yang salah dan meningkatkan robustness serta akurasi prediksi.

  2) Penanganan Outlier (Penghapusan Berbasis IQR)
     Setelah menangani nilai-nilai yang tidak masuk akal, langkah selanjutnya adalah mengidentifikasi dan menangani outlier (nilai ekstrem) yang mungkin masih ada dalam fitur-fitur numerik. Outlier dapat sangat memengaruhi kinerja model, terutama algoritma yang sensitif terhadap distribusi data seperti Regresi Logistik dan SVM.

      **Tujuan:**
         - Meningkatkan Akurasi Model: Outlier dapat mendistorsi parameter model selama pelatihan, menyebabkan model berkinerja buruk pada data normal. Menghapus outlier membantu model belajar pola yang lebih representatif dari mayoritas data.
         - Normalisasi/Standardisasi yang Lebih Baik: Seperti yang disebutkan sebelumnya, outlier dapat mendistorsi rata-rata dan standar deviasi, membuat penskalaan fitur menjadi kurang efektif. Menangani outlier terlebih dahulu menghasilkan penskalaan yang lebih akurat.

  3) Pembagian Dataset (Splitting Data)
     Setelah tahap penanganan nilai yang tidak masuk akal dan penghapusan outlier, dataset yang telah dibersihkan dibagi menjadi dua bagian utama: data latih (training set) dan data uji (testing set). Pembagian ini dilakukan menggunakan fungsi train_test_split dari library sklearn.model_selection.

     Kemudian, pembagian data dilakukan dengan proporsi 70% untuk training set dan 30% untuk testing set. Parameter random_state=42 diatur untuk memastikan hasil pembagian yang konsisten dan reproducible. Penting juga untuk menggunakan stratify=y guna memastikan bahwa proporsi kelas (Outcome) dalam training set dan testing set tetap sama dengan proporsi kelas dalam dataset asli yang telah dibersihkan, sehingga representasi kelas terjaga dengan baik.

     **Tujuan :**
       - Evaluasi Objektif: Tujuan utama pembagian data adalah untuk mengevaluasi kinerja model pada data yang belum pernah dilihat selama proses pelatihan. Ini memberikan indikasi yang lebih realistis tentang bagaimana model akan berkinerja di lingkungan produksi.
       - Mencegah Overfitting: Dengan melatih model hanya pada training set dan mengevaluasinya pada testing set terpisah, kita dapat mendeteksi apakah model terlalu spesifik (hafalan) terhadap data pelatihan (overfitting) dan gagal melakukan generalisasi dengan baik pada data baru.

  4) SMOTE
       Pada dataset prediksi diabetes, seringkali ditemukan adanya ketidakseimbangan kelas (class imbalance), di mana jumlah sampel dari kelas minoritas (misalnya, pasien diabetes) jauh lebih sedikit dibandingkan kelas mayoritas (non-diabetes). Jika tidak ditangani, model cenderung bias terhadap kelas mayoritas dan kurang baik dalam memprediksi kelas minoritas.

Untuk mengatasi hal ini, teknik Synthetic Minority Over-sampling Technique (SMOTE) diterapkan pada data latih (X_train, y_train) setelah pembagian data. SMOTE bekerja dengan menghasilkan sampel sintetis baru untuk kelas minoritas berdasarkan tetangga terdekat dari sampel minoritas yang ada
    **Tujuan :**
      - Meningkatkan Kemampuan Prediksi Kelas Minoritas: Dengan menyeimbangkan distribusi kelas pada data latih, SMOTE membantu model belajar pola dari kelas minoritas secara lebih efektif, yang krusial untuk meningkatkan Recall (kemampuan mendeteksi semua kasus positif diabetes) dan F1-Score model.
      - Mencegah Bias Model: Mengurangi bias model terhadap kelas mayoritas, sehingga model dapat menggeneralisasi lebih baik pada kedua kelas.
      - Memastikan Data Uji Tetap Murni: Penting untuk dicatat bahwa SMOTE hanya diterapkan pada data latih. Data uji dibiarkan dalam distribusi aslinya untuk memberikan evaluasi kinerja model yang tidak bias dan realistis terhadap data dunia nyata.
      
  5) Standardisasi
      Setelah pembagian data, penskalaan fitur dilakukan secara terpisah pada training set dan transformasi yang sama diterapkan pada testing set. Teknik penskalaan yang digunakan adalah Standardisasi, melalui StandardScaler dari sklearn.preprocessing.

     **Tujuan :**
       - Sensitivitas Algoritma: Banyak algoritma machine learning, terutama yang berbasis jarak (seperti K-Nearest Neighbors dan Support Vector Machine) atau yang menggunakan optimasi berbasis gradient descent (seperti Regresi Logistik), sangat sensitif terhadap skala fitur. Jika fitur memiliki rentang nilai yang sangat berbeda, fitur dengan rentang nilai yang lebih besar dapat mendominasi perhitungan jarak atau pembaruan bobot, sehingga fitur dengan rentang nilai kecil menjadi kurang signifikan.
    
       - Kinerja Model yang Konsisten: Penskalaan memastikan bahwa setiap fitur memiliki "bobot" yang setara dalam perhitungan model, mencegah fitur dominan yang tidak relevan secara inheren. Ini seringkali menghasilkan model yang lebih stabil dan akurat.
    
## Modeling
Tujuan utama dari proyek ini adalah untuk membangun model klasifikasi machine learning yang dapat memprediksi apakah seorang wanita keturunan Indian Pima berisiko terkena diabetes menggunakan data diagnostik yang tersedia. Untuk mencapai tujuan ini, dua algoritma klasifikasi yang berbeda, yaitu Regresi Logistik dan Support Vector Machine (SVM), diimplementasikan dan dibandingkan untuk mengidentifikasi model yang paling optimal.

### Logistik Regresi

**Cara Kerja Algoritma:**

Cara kerja Regresi Logistik adalah sebagai berikut:

  1) "Pemberian Skor" Awal: Model pertama-tama akan memberikan "skor" pada setiap orang berdasarkan kombinasi faktor-faktor kesehatan mereka. Skor ini dihitung dengan cara sederhana: setiap faktor dikalikan dengan "bobot" tertentu (yang dipelajari model), lalu hasilnya dijumlahkan. Bobot ini menentukan seberapa penting setiap faktor.
     
  2) Mengubah Skor Menjadi Probabilitas (Dengan Fungsi Sigmoid): Skor yang dihasilkan tadi bisa berupa angka berapa pun (negatif, nol, atau positif). Nah, agar bisa menjadi probabilitas (yang nilainya harus antara 0% sampai 100%), model menggunakan sebuah "rumus ajaib" yang disebut Fungsi Sigmoid.
     
      - Fungsi Sigmoid ini seperti sebuah konverter: ia mengambil skor mentah dan mengubahnya menjadi angka antara 0 dan 1. Angka 0 berarti probabilitas sangat rendah (0%), dan angka 1 berarti probabilitas sangat tinggi (100%). Bentuk kurvanya seperti huruf "S" landai, memastikan hasilnya selalu berada dalam rentang probabilitas yang valid.
        
  3) Pengambilan Keputusan (Ambang Batas): Setelah mendapatkan probabilitas (misalnya, 0.75 atau 75% kemungkinan diabetes), model kemudian membandingkannya dengan sebuah ambang batas (biasanya 0.5 atau 50%).
     - Jika probabilitas di atas 0.5, maka model memprediksi orang tersebut cenderung diabetes.
     - Jika probabilitas di bawah 0.5, maka model memprediksi orang tersebut cenderung tidak diabetes.
  4) "Belajar dari Kesalahan" (Fungsi Kerugian): Bagaimana model bisa menemukan bobot yang tepat untuk setiap faktor? Ini dilakukan melalui proses "belajar".
     - Model akan membuat prediksi awal, lalu melihat seberapa jauh prediksi probabilitasnya dari kenyataan (apakah orang itu benar-benar diabetes atau tidak). Perbedaan ini diukur menggunakan Fungsi Kerugian (Loss Function), yang sering disebut log-loss.
     - Log-loss ini memberi tahu model seberapa "buruk" prediksinya. Semakin besar nilai log-loss, semakin jauh prediksi model dari kebenaran.
     - Model kemudian secara berulang-ulang menyesuaikan bobotnya sedikit demi sedikit, mencoba mengurangi nilai log-loss ini sampai seminimal mungkin. Proses ini seperti belajar dari kesalahan untuk menjadi lebih akurat.  
  1) Proses Pemodelan :
     - Inisialisasi Model: Model LogisticRegression diinisialisasi dari sklearn.linear_model.
     - Pelatihan Model: Model dilatih menggunakan data latih yang telah distandardisasi (X_train_scaled, y_train_smote) dengan memanggil metode fit().
     - Prediksi: Setelah dilatih, model digunakan untuk membuat prediksi pada data uji (X_test_scaled) dengan memanggil metode predict().

  2) Parameter
      - Model dasar LogisticRegression diinisialisasi dengan random_state=42.
      - Pencarian Hyperparameter: GridSearchCV digunakan untuk mencari parameter terbaik dari grid berikut:
        
          - C: [0.001, 0.01, 0.1, 1, 10, 100] (Parameter regularisasi terbalik; nilai yang lebih kecil berarti regularisasi yang lebih kuat).
          - solver: ['liblinear', 'lbfgs'] (Algoritma yang digunakan untuk optimasi).
    
      - Proses GridSearchCV menggunakan estimator=log_reg_model, param_grid=param_grid_lr, cv=5 (5-fold cross-validation), scoring='recall' (metrik yang diutamakan untuk            pemilihan model terbaik), n_jobs=-1 (menggunakan semua core CPU), dan verbose=1.
      - Hasil terbaik dari tuning ini adalah best_lr_params, dan model terbaiknya adalah best_lr_model.
      - Nilai Parameter Terbaik Regresi Logistik:
          - c = 0.1
          - solver = 'lbfgs'

  3) Kelebihan
     - Sederhana dan Mudah Diinterpretasikan: Karena merupakan model linear, bobot yang dipelajari untuk setiap fitur dapat diinterpretasikan sebagai indikator pentingnya          fitur tersebut terhadap outcome.
     - Cepat untuk Dilatih dan Efisien: Cocok untuk dataset berukuran sedang dan komputasi yang relatif ringan.

  4) Kekurangan
     - Sensitif terhadap Outlier: Meskipun data telah ditangani outlier, model ini masih bisa terpengaruh oleh outlier ekstrem jika tidak ditangani dengan baik.
     - Tidak Baik untuk Masalah Kompleks: Kinerjanya bisa buruk pada masalah dengan hubungan fitur yang sangat kompleks atau non-linear.

  ### Support Vector Machine

  Support Vector Machine (SVM) adalah algoritma klasifikasi yang kuat yang bekerja dengan menemukan hyperplane (batas keputusan) terbaik yang secara optimal memisahkan kelas-kelas dalam ruang fitur. Untuk data yang tidak dapat dipisahkan secara linear, SVM menggunakan teknik kernel trick untuk memetakan data ke ruang berdimensi lebih tinggi di mana pemisahan linear mungkin dilakukan.

  1) Proses Pemodelan :
      - Inisialisasi Model: Model SVC (Support Vector Classifier) diinisialisasi dari sklearn.svm
      - Pelatihan Model: Model dilatih menggunakan data latih yang telah distandardisasi (X_train_scaled, y_train_smote) dengan memanggil metode fit()
      - Prediksi: Setelah dilatih, model digunakan untuk membuat prediksi pada data uji (X_test_scaled) dengan memanggil metode predict().
      - Prediksi: Setelah dilatih, model terbaik digunakan untuk membuat prediksi pada data uji (X_test_scaled).

  2) Parameter
     - Model dasar SVC diinisialisasi dengan random_state=42.
     - Pencarian Hyperparameter: GridSearchCV digunakan untuk mencari parameter terbaik dari grid berikut:
           - C: [0.1, 1, 10, 100] (Parameter regularisasi).
           - kernel: ['linear', 'rbf'] (Jenis kernel yang digunakan, menentukan bentuk batas keputusan).
           - gamma: ['scale', 'auto'] (Koefisien kernel untuk 'rbf', 'poly' dan 'sigmoid'. scale menggunakan 1 / (n_features * X.var()) dan auto menggunakan 1 / n_features).
     - Proses GridSearchCV menggunakan estimator=svm_model, param_grid=param_grid_svm, cv=5 (5-fold cross-validation), scoring='recall' (metrik yang diutamakan untuk               pemilihan model terbaik), n_jobs=-1 (menggunakan semua core CPU), dan verbose=1.
     - Hasil terbaik dari tuning ini adalah best_svm_params, dan model terbaiknya adalah best_svm_model.
     - Nilai parameter terbaik SVM :
         - c = 10
         - gamma = 'scale'
         - kernel = 'rbf'

  3) Kelebihan
     - Efektif di Ruang Berdimensi Tinggi: Bekerja dengan baik bahkan ketika jumlah fitur lebih besar dari jumlah sampel.
     - Tidak Rentan Terhadap Overfitting: SVM fokus pada pencarian hyperplane terbaik dengan margin maksimal, yang secara inheren membantu mengurangi overfitting.

  4) Kekurangan
     - Sensitif terhadap Pemilihan Kernel dan Parameter: Kinerja sangat bergantung pada pemilihan kernel dan hyperparameter seperti C dan gamma (untuk kernel RBF).
     - Membutuhkan Normalisasi/Standardisasi: Sangat sensitif terhadap penskalaan fitur, membuat preprocessing seperti standardisasi menjadi krusial.

  **Model Terbaik**
   Regresi Logistik menunjukkan kinerja yang lebih baik dibandingkan Support Vector Machine (SVM) pada dataset ini,setelah kedua model menjalani proses hyperparameter          tuning.

  1) Alasan
     - Akurasi Keseluruhan (Accuracy): Regresi Logistik mencapai akurasi 0.76, yang lebih tinggi dibandingkan SVM yang hanya 0.73. Ini menunjukkan kemampuan prediksi yang          lebih baik secara keseluruhan.
     - Recall untuk Kelas Positif (Diabetes - Kelas 1): Dalam konteks diagnosis diabetes, recall sangat penting untuk meminimalkan false negatives. Regresi Logistik                memiliki recall 0.64 untuk kelas 1, yang lebih tinggi dibandingkan SVM yang hanya 0.61. Ini berarti Regresi Logistik lebih baik dalam mengidentifikasi kasus                 diabetes yang sebenarnya, mengurangi risiko terlewatnya diagnosis.
     - F1-Score untuk Kelas Positif: Regresi Logistik memiliki F1-score 0.60 untuk kelas 1, sedangkan SVM memiliki 0.56. Skor F1 yang lebih tinggi untuk Regresi Logistik           menunjukkan keseimbangan yang lebih baik antara precision dan recall dalam mengidentifikasi kasus diabetes.



## Evaluation

**Metrik Evaluasi yang Digunakan**
Dalam masalah klasifikasi biner seperti deteksi diabetes, metrik evaluasi yang komprehensif diperlukan untuk memahami kinerja model dari berbagai aspek. Metrik yang digunakan dalam proyek ini adalah:
1) Akurasi (Accuracy)
2) Presisi (Precision)
3) Recall (Sensitivitas)
4) F1-Score
5) Confusion Matrix

**Penjelasan Metrik dan Cara Kerjanya**
  Untuk memahami metrik-metrik ini, mari kita definisikan istilah dasar dari Confusion Matrix:
    - True Positive (TP): Jumlah kasus positif yang diprediksi dengan benar oleh model (misalnya, pasien didiagnosis diabetes dan memang menderita diabetes).
    - True Negative (TN): Jumlah kasus negatif yang diprediksi dengan benar oleh model (misalnya, pasien didiagnosis tidak diabetes dan memang tidak menderita diabetes).
    - False Positive (FP): Jumlah kasus negatif yang diprediksi sebagai positif (misalnya, pasien didiagnosis diabetes, tetapi sebenarnya tidak menderita diabetes). Juga          dikenal sebagai Type I error
    - False Negative (FN): Jumlah kasus positif yang diprediksi sebagai negatif (misalnya, pasien didiagnosis tidak diabetes, tetapi sebenarnya menderita diabetes). Juga          dikenal sebagai Type II error.

  1) Accuracy
     Akurasi mengukur proporsi total prediksi yang benar (baik positif maupun negatif) dari seluruh prediksi. Ini adalah metrik paling sederhana dan memberikan gambaran          umum tentang seberapa baik model bekerja.

     Formula:

     ![accuracy_formula](https://github.com/user-attachments/assets/47ace958-556a-4fc1-b729-e6320526c35a)

     
     Cara kerja : Akurasi bekerja dengan menghitung rasio jumlah prediksi yang tepat (TP + TN) terhadap total jumlah semua sampel (TP + TN + FP + FN). Ini ideal ketika           dataset memiliki distribusi kelas yang seimbang. Namun, jika ada ketidakseimbangan kelas (misalnya, jauh lebih banyak pasien non-diabetes daripada diabetes), akurasi        tinggi bisa menyesatkan karena model mungkin hanya pandai memprediksi kelas mayoritas.

  3) Precision
     Presisi mengukur proporsi prediksi positif yang benar dari semua kasus yang diprediksi sebagai positif. Ini menjawab pertanyaan: "Dari semua yang diprediksi sebagai         diabetes, berapa banyak yang benar-benar diabetes?"

     Formula:

      ![Precision_formula](https://github.com/user-attachments/assets/933959c4-136f-453b-96ba-7579ad47bdee)


     Cara Kerja:  Presisi fokus pada kualitas prediksi positif. Sebuah model dengan precision tinggi memiliki sedikit false positives. Dalam konteks medis, precision             tinggi berarti model jarang salah mendiagnosis seseorang yang sehat sebagai diabetes.

  5) Recall
     Recall mengukur proporsi kasus positif yang benar yang berhasil diidentifikasi oleh model dari semua kasus positif yang sebenarnya ada. Ini menjawab pertanyaan: "Dari       semua kasus diabetes yang sebenarnya, berapa banyak yang berhasil ditemukan oleh model?"

     Formula:

      ![recall_formula](https://github.com/user-attachments/assets/39d42cd0-d4ce-444d-ad01-2ebac341347d)

     Cara Kerja: Recall fokus pada menemukan semua kasus positif. Sebuah model dengan recall tinggi memiliki sedikit false negatives. Dalam konteks diagnosis diabetes,           recall sangat penting karena false negatives (pasien diabetes yang tidak terdeteksi) dapat menyebabkan komplikasi kesehatan yang parah.

  7) F1 - Score
     F1-Score adalah harmonic mean dari precision dan recall. Ini adalah metrik yang lebih seimbang daripada akurasi, terutama untuk dataset dengan kelas yang tidak              seimbang, karena ia mempertimbangkan false positives dan false negatives. Skor F1 mencapai nilai terbaiknya pada 1 dan nilai terburuk pada 0.

     Formula:

     ![f1score_formula](https://github.com/user-attachments/assets/e3c3aa15-6203-4dd6-a8e6-e0bb2d2f4c5e)

     Cara Kerja : F1-Score memberikan skor tunggal yang menyeimbangkan precision dan recall. Ini sangat berguna ketika kita membutuhkan keseimbangan yang baik antara             menghindari false positives dan false negatives.

  9) Confusion Matrix
     Confusion Matrix adalah tabel yang menunjukkan kinerja model klasifikasi pada testing set di mana nilai true dari sampel diketahui. Ini menyajikan visualisasi yang          jelas tentang berapa banyak prediksi yang benar dan salah untuk setiap kelas.

     Formula:

     ![confusion_formula](https://github.com/user-attachments/assets/850338c5-1648-41c1-b8bf-b2137896935c)


     Cara Kerja: Dengan melihat Confusion Matrix, kita dapat dengan cepat mengidentifikasi jenis kesalahan yang paling sering dilakukan model (misalnya, apakah model             cenderung menghasilkan lebih banyak false positives atau false negatives). Ini adalah dasar perhitungan untuk precision, recall, dan F1-score.

**Hasil Proyek Berdasarkan Metrik Evaluasi**

Berdasarkan analisis Classification Report dan Confusion Matrix dari kedua model pada testing set (dengan 71 kasus non-diabetes (kelas 0) dan 28 kasus diabetes (kelas 1)):

### Regresi Logistik

 ![hasil_lr](https://github.com/user-attachments/assets/91e911a7-204e-45f9-b830-fcc6eb5c6c7a)

  1) Confusion Matrix
     - TP: 18 (pasien diabetes diprediksi diabetes)
     - TN: 57 (pasien non-diabetes diprediksi non-diabetes)
     - FP: 14 (pasien non-diabetes diprediksi diabetes - Type I error)
     - FN: 10 (pasien diabetes diprediksi non-diabetes - Type II error)

  2) Interpretasi Hasil:
     - Akurasi (0.76): Model secara keseluruhan memprediksi dengan benar 76% dari waktu.
     - Presisi Kelas 0 (Non-diabetes) (0.85): Ketika model memprediksi seseorang tidak menderita diabetes, 85% di antaranya benar.
     - Recall Kelas 0 (Non-diabetes) (0.80): Model berhasil mengidentifikasi 80% dari semua kasus non-diabetes yang sebenarnya.
     - Presisi Kelas 1 (Diabetes) (0.56): Dari semua pasien yang diprediksi menderita diabetes, 56% yang benar-benar menderita diabetes. Ini menunjukkan peningkatan yang           baik dibandingkan hasil sebelumnya.
     - Recall Kelas 1 (Diabetes) (0.64): Model berhasil mengidentifikasi 64% dari semua pasien diabetes yang sebenarnya. Ini adalah peningkatan signifikan dan memenuhi             target recall ≥60% yang ditetapkan. Ini berarti model ini lebih baik dalam menemukan kasus diabetes yang sebenarnya.
     - F1-Score Kelas 1 (Diabetes) (0.60): Skor F1 yang lebih tinggi ini mengindikasikan bahwa model memiliki kinerja yang lebih seimbang dalam mengidentifikasi kelas              diabetes dibandingkan sebelumnya, karena recall dan precision yang lebih baik.

### Support Vector Machine

 ![hasil_svm](https://github.com/user-attachments/assets/d9c782ad-76fb-4d65-ae34-5a07751c13f7)

   1) Confnusion Matrix:
      - TP: 17 (pasien diabetes diprediksi diabetes)
        TN: 55 (pasien non-diabetes diprediksi non-diabetes)
        FP: 16 (pasien non-diabetes diprediksi diabetes - Type I error)
        FN: 11 (pasien diabetes diprediksi non-diabetes - Type II error)

   2) Interpretasi Hasil:
      - Akurasi (0.73): Model SVM mencapai akurasi keseluruhan 73%.
      - Presisi Kelas 0 (Non-diabetes) (0.83): Ketika model memprediksi seseorang tidak menderita diabetes, 83% di antaranya benar.
      - Recall Kelas 0 (Non-diabetes) (0.77): Model berhasil mengidentifikasi 77% dari semua kasus non-diabetes yang sebenarnya.
      - Presisi Kelas 1 (Diabetes) (0.52): Dari semua pasien yang diprediksi menderita diabetes, 52% yang benar-benar menderita diabetes.
      - Recall Kelas 1 (Diabetes) (0.61): Model berhasil mengidentifikasi 61% dari semua pasien diabetes yang sebenarnya.
      - F1-Score Kelas 1 (Diabetes) (0.56): F1-score ini menunjukkan keseimbangan antara precision dan recall untuk kelas diabetes.

  Kesimpulan Evaluasi 
    Berdasarkan metrik evaluasi yang terbaru, terutama recall dan F1-score untuk kelas positif (diabetes), serta pengurangan false negatives dan false positives, Regresi        Logistik adalah model terbaik untuk masalah klasifikasi diabetes ini. Kemampuannya untuk mengidentifikasi lebih banyak kasus diabetes yang sebenarnya (dengan recall         0.64) sambil juga meminimalkan false positives (dengan precision 0.56) membuatnya menjadi pilihan yang lebih unggul dibandingkan SVM dalam upaya deteksi dini penyakit       ini.






