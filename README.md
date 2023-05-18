# Default Dataset Klien Kartu Kredit


### Inspirasi:
Pada akhir kasus ini, akan dapat menjawab pertanyaan-pertanyaan di bawah ini.

- Preprocessing Data; persiapan data; dan visualisasi data
- Fitur Teknik dan fitur pilihan
- Pengembangan Model
- Evaluasi Model
- Variabel mana yang merupakan prediktor terkuat dari pembayaran gagal bayar?

### Variables:
Deskripsi variabel dalam himpunan data:

- D: ID of each client
- LIMIT_BAL: Amount of given credit in NT dollars (includes individual and family/supplementary credit
- SEX: Gender (1=male, 2=female)
- EDUCATION: (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown)
- MARRIAGE: Marital status (1=married, 2=single, 3=others)
- AGE: Age in years
- PAY_0: Repayment status in September, 2005 (-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, ... 8=payment delay for eight months, 9=payment delay for nine months and above)
- PAY_2: Repayment status in August, 2005 (scale same as above)
- PAY_3: Repayment status in July, 2005 (scale same as above)
- PAY_4: Repayment status in June, 2005 (scale same as above)
- PAY_5: Repayment status in May, 2005 (scale same as above)
- PAY_6: Repayment status in April, 2005 (scale same as above)
- BILL_AMT1: Amount of bill statement in September, 2005 (NT dollar)
- BILL_AMT2: Amount of bill statement in August, 2005 (NT dollar)
- BILL_AMT3: Amount of bill statement in July, 2005 (NT dollar)
- BILL_AMT4: Amount of bill statement in June, 2005 (NT dollar)
- BILL_AMT5: Amount of bill statement in May, 2005 (NT dollar)
- BILL_AMT6: Amount of bill statement in April, 2005 (NT dollar)
- PAY_AMT1: Amount of previous payment in September, 2005 (NT dollar)
- PAY_AMT2: Amount of previous payment in August, 2005 (NT dollar)
- PAY_AMT3: Amount of previous payment in July, 2005 (NT dollar)
- PAY_AMT4: Amount of previous payment in June, 2005 (NT dollar)
- PAY_AMT5: Amount of previous payment in May, 2005 (NT dollar)
- PAY_AMT6: Amount of previous payment in April, 2005 (NT dollar)
- default.payment.next.month: Default payment (1=yes, 0=no)


##### Variabel Target:

Kami akan memvisualisasikan kolom target "default" untuk mengetahui seberapa implance (keseimbangan) data
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/24969671-b117-4d92-a033-c4e7bc09d983)
Data tersebut cukup tidak seimbang dimana sekitar 22% klien akan gagal bayar bulan depan.

##### Variabel SEX:
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/fc30c9da-2731-4348-b8a0-d1efee0675ff)
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/dfdcfeb4-fa7a-40be-92df-e69a25c2e0ca)

- Lebih banyak klien wanita memiliki kartu kredit daripada klien pria.
- 24% klien pria melakukan penipuan kartu kredit sedangkan rasio untuk wanita sekitar 20%

##### VARIABEL PENDIDIKAN:
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/8def1da7-73d7-40d8-a518-b98781719d31)
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/e82fc39a-be16-44ae-9166-a866ce67adb3)

- Mahasiswa merupakan kelompok dengan jumlah nasabah terbanyak yang menggunakan kartu kredit (47%)
- Siswa SMA adalah kelompok yang memiliki kasus penipuan tertinggi (25%), diikuti oleh mahasiswa (23%)

##### VARIABEL STATUS PERNIKAHAN:
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/e834ab62-9fea-4ffe-96ff-899002db9abd)
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/9b60b488-09df-4cc1-8ba5-e1bd33e10d22)

- Single adalah kelompok dengan jumlah nasabah terbanyak yang menggunakan kartu kredit (53%)
- Orang yang sudah menikah adalah kelompok yang memiliki kasus penipuan tertinggi (30%)

##### VARIABEL USIA:
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/5bf87b78-51c1-4956-aa6c-958e3864b91c)
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/4dcefa22-8112-4584-a811-e7c0f1cce77f)
- Histogram condong ke kanan yang berarti pelanggan yang lebih tua cenderung tidak menggunakan kartu kredit
- Klien utama berusia 30-an
- Pelanggan berusia 30-an juga paling rentan terhadap penipuan kredit

##### LIMIT_BAL VARIABEL:
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/89d5f4f4-3bac-43a9-988c-0dec25b6a4c3)

##### Jumlah tagihan dan Jumlah pembayaran sebelumnya
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/3d78cc9e-45f5-414a-973f-7d8bf9903a6c)

##### Analisis Korelasi:
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/7451d943-3ef2-4a05-956d-c3fa437a3f33)

Korelasinya tinggi antara PAY_0,2,3,4,5,6 dan BILL_AMT1,2,3,4,5,6.

#### Compare Performance Models:

![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/fda630d0-8e44-469f-b356-61348bde3595)

![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/e3459f81-7d1a-4428-8f96-3df7a5479cd7)

# Kesimpulan:

- Dalam proyek ini, pertama-tama kami memeriksa ketidakseimbangan data, memvisualisasikan feaure dan menyelidiki hubungan antara fitur yang berbeda untuk menemukan prediktor terkuat dari pembayaran default

- Kami kemudian menjalankan model 5 ML yang berbeda untuk menemukan model terbaik untuk mendeteksi default kredit:
- Model logistik dengan akurasi 68,08%,

- Decision_tree model dengan akurasi 72,83%,
- Randome_forest model dengan akurasi 79,35%,
- Model XGboost dengan akurasi 81,35%,
- Model hyperparameter XGboost dengan akurasi 80,58%

Di antara semua model ML yang kami gunakan untuk memprediksi kartu kredit default, XGboost adalah model terbaik dengan skor akurasi tertinggi dan Variabel yang merupakan prediktor terkuat dari pembayaran gagal bayar adalah default.payment.next.month 

