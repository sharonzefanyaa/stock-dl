# stock-dl

Dataset ini berisi harga harian historis untuk beberapa saham sektor teknologi. Data historis diambil dari Yahoo finance melalui paket python yfinance dan berisi harga hingga tanggal 01 April 2020. 

**Struktur Data:**
1. Date - menunjukkan tanggal perdagangan
2. Open - harga pembukaan
3. High - harga maksimum selama sehari
4. Low - harga minimum selama sehari
5. Close - harga penutupan disesuaikan untuk pemecahan
6. Adj Close - harga penutupan disesuaikan yang telah disesuaikan untuk dividen dan pemecahan.
7. Volume - jumlah saham yang berpindah tangan selama sehari

Selain itu, setiap nama file adalah simbol ticker yang sesuai, sebagai berikut:
AMZN Amazon.com, Inc
CSCO Cisco Systems, Inc.

**Soal:**
1. Konsep sains data sebagai bidang studi sendiri diajukan oleh William S. Cleveland. Dia memperluas ilmu statistik ke area teknis, yang akan merubah bidang ini secara signifikan. Dia diminta untuk membuat sebuah aplikasi yang membantu perusahaan untuk memprediksi harga saham. Dalam dataset yang disediakan terdapat informasi penting mengenai keterangan setiap kolomnya. Yang akan digunakan kolom Date dan Close saja. Buatlah arsitektur Long Short Term Memory (LSTM). Berikut adalah ketentuan yang perlu diperhatikan dalam pembuatan arsitektur LSTM.

a. Lakukan eksplorasi data terlebih dahulu untuk memahami permasalahan yang dihadapi terlebih dahulu. Dataset yang diberikan adalah data time series, lakukan praproses data untuk menyelesaikan problem dari data tersebut. Pisahkan data time series tersebut menjadi dua bagian input dan output dengan window size = 5 [dari hari senin s.d jumat] dan horizon = 1 [hari senin saja]. Selanjutnya pisahkan dataset menjadi train, test dan validation set dengan ketentuan (80 train, 10 val, 10 test)
b. Buatlah arsitektur baseline dengan LSTM (units=50) dan layer akhir berupa node Perceptron dengan units=1. Activation function untuk LSTM menggunakan ReLU
c. Setelah mengetahui hasil dari nomor (1c), modifikasi arsitektur pada nomor 1c untuk mendapatkan unjuk kerja yang optimal (kalian dapat menambahkan atau mengurangi arsitektur tersebut, atau mengganti hyperparameter, atau menggunakan tuning pada hyperparameter). Jelaskan alasan kalian untuk menggunakan pendekatan yang kalian pilih.
d. Lakukan evaluasi unjuk kerja kedua arsitektur di atas pada test set dengan mencari nilai RMSE, MAE dan MAPE. Dan berikan penjelasan mengenai hasilnya dengan rinci.


2. DJ Patil dikenal sebagai data scientist yang pertama kali. Tugasnya adalah menganalisis maha data untuk diubah menjadi informasi yang bermanfaat dan membuat program serta algoritma untuk membantu perusahaan beroperasi dengan optimal. Ia ingin memperbaiki model prediksi harga saham dengan menggunakan algoritma Transformers. Anda diminta untuk membantu DJ Patil dalam melakukan perbaikan ini.

a. Lakukan praproses data dengan memisahkan data time series tersebut menjadi dua bagian input dan output dengan window size = 5 [dari hari senin s.d jumat] dan horizon = 5 [dari hari senin s.d jumat]. Kemudian pisahkan dataset menjadi 80% training set, 10% validation set dan 10% test set.
b. Buatlah arsitektur baseline sesuai dengan gambar arsitektur Transformer for Stocks berikut ini: (Catatan: bagian FEED FORWARD menggunakan satu layer Conv1D saja dengan Activation function menggunakan ReLU dan bagian node Perceptron pada output disesuaikan dengan horizon datanya)
c. Modifikasi arsitektur Transformer for Stocks di atas agar mendapatkan hasil klasifikasi yang optimal. Kalian dapat menambahkan atau mengurangi arsitektur tersebut dan melakukan mengubah arsitektur pada nomor 2c dengan menggunakan dropout, batch normalization dan lain-lainnya. Dan selanjutnya lakukan proses tuning hyperparameter agar unjuk kerjanya meningkat. Berikan alasan mengapa modifikasi arsitektur dan metode tuning hyperparameter kalian lebih baik.
d. Evaluasi performa dari arsitektur nomor 2d secara rinci dan jelaskan hasil yang kalian dapatkan. Gunakan testing set yang diberikan untuk memprediksi nilai ground truth dengan predicted result.
