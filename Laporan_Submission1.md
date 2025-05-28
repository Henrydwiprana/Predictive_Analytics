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

  1) Membangun model klasifikasi machine learning yang mampu memprediksi diabetes dengan akurasi yang tinggi (target ≥75%) pada Pima Indians Diabetes Database. 
     Target akurasi ini ditetapkan dengan mempertimbangkan kompleksitas data medis dan tantangan diagnostik.
     
  2) Mengidentifikasi dan mengimplementasikan setidaknya dua algoritma klasifikasi dasar (misalnya, Regresi Logistik dan Support Vector Machine) pada Pima Indians Diabetes Database, serta membandingkan kinerja masing-masing algoritma. 
     Perbandingan ini akan memberikan wawasan mengenai kekuatan dan kelemahan relatif setiap metode untuk masalah ini.

  3) Mengevaluasi kinerja model menggunakan metrik yang relevan seperti Akurasi, Precision, Recall, F1-Score, dan Confusion Matrix pada testing set.
     Penekanan khusus akan diberikan pada metrik recall untuk meminimalkan false negatives, yang sangat penting dalam aplikasi diagnostik medis.
     
## Solution Statements

Untuk mencapai tujuan yang telah ditetapkan, proyek ini akan mengimplementasikan pendekatan berbasis machine learning dengan menguji dan membandingkan dua algoritma klasifikasi yang berbeda. 
Setiap solusi akan diukur menggunakan metrik evaluasi yang jelas dan relevan dengan konteks medis.

  1) Pembangunan Model Klasifikasi Diabetes dengan Algoritma Regresi Logistik :

      - Deskripsi Solusi: Kami akan melatih model Regresi Logistik pada training set Pima Indians Diabetes Database. Sebelum pelatihan, fitur-fitur numerik akan menjalani preprocessing seperti penanganan nilai nol yang tidak valid (misalnya, mengganti nilai nol pada fitur seperti glukosa, tekanan darah, 
        dan BMI dengan median atau rata-rata) dan penskalaan (misalnya, Standard Scaler) untuk memastikan semua fitur memiliki skala yang seragam. Penyesuaian hyperparameter dasar akan dilakukan jika diperlukan.
    
      - Metrik Evaluasi: Akurasi, Precision, Recall, F1-score, dan Confusion Matrix pada testing set. Target recall untuk kelas positif (diabetes) adalah ≥70%, di samping akurasi keseluruhan ≥75%.
    
      - Justifikasi: Regresi Logistik adalah model linear yang kuat, mudah diinterpretasikan, dan seringkali menjadi baseline yang baik untuk masalah klasifikasi biner, 
        terutama dalam aplikasi medis di mana interpretasi model penting.
    
  2) Pembangunan Model Klasifikasi Diabetes dengan Algoritma Support Vector Machine (SVM):

      - Deskripsi Solusi: Model Support Vector Machine (SVM) akan dilatih pada training set Pima Indians Diabetes Database. Seperti Regresi Logistik, data akan melalui tahapan preprocessing yang sama (penanganan nilai nol dan penskalaan fitur). 
        Eksplorasi hyperparameter seperti jenis kernel (misalnya, linear atau RBF) dan parameter regularisasi C akan dilakukan untuk mengoptimalkan batas keputusan SVM.
        
      - Metrik Evaluasi: Akurasi, Precision, Recall, F1-score, dan Confusion Matrix pada testing set. Sama seperti solusi KNN, target recall untuk kelas positif (diabetes) adalah ≥70%, di samping akurasi keseluruhan ≥75%.

      - Justifikasi: SVM dikenal sangat efektif untuk masalah klasifikasi, bahkan ketika data tidak dapat dipisahkan secara linear. 
        Kemampuannya untuk menangani ruang fitur berdimensi tinggi (walaupun Pima Indians berdimensi rendah) dan menemukan hyperplane optimal menjadikannya pilihan yang baik untuk dibandingkan dengan Regresi Logistik.

Dengan mengimplementasikan dan membandingkan kedua solusi ini, proyek ini diharapkan dapat mengidentifikasi algoritma yang paling efektif untuk diagnosis dini diabetes pada Pima Indians Diabetes Database, 
sekaligus memberikan analisis komprehensif tentang performa model yang diukur dengan metrik yang relevan secara klinis.

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

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Pemahaman Data (Exploratory Data Analysis - EDA)**

  1) Pemuatan Data dan Inspeksi Awal
       - df.head(): Menampilkan beberapa baris pertama dari dataset. Ini memberikan gambaran cepat tentang bagaimana data terstruktur, nama-nama kolom, dan jenis nilai yang terkandung di dalamnya.
         
         ![head](https://github.com/Henrydwiprana/Predictive_Analytics/blob/main/head.png)
         
       - df.info(): Menyediakan ringkasan singkat tentang DataFrame, termasuk jumlah entri, jumlah kolom, tipe data masing-masing kolom (misalnya, int64, float64), dan keberadaan nilai non-null. Ini membantu dalam mengidentifikasi apakah ada kolom dengan nilai yang hilang secara eksplisit (NaN) pada tahap awal

         ![info](https://github.com/Henrydwiprana/Predictive_Analytics/blob/main/info.png)

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
