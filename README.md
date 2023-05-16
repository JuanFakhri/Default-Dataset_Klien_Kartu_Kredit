# Default Dataset Klien Kartu Kredit

### Perkenalan:
Resiko kredit mengacu pada kemungkinan kerugian yang bisa jadi dialami pemberi pinjaman ataupun investor sebab kegagalan peminjam buat membayar kembali pinjaman ataupun penuhi kewajiban keuangan yang lain. Ini merupakan resiko kandas bayar utang yang bisa jadi mencuat dari ketidakmampuan peminjam ataupun keengganan buat membayar kembali duit yang dipinjam.

Resiko kredit jadi atensi utama untuk bank, lembaga keuangan, serta investor yang meminjamkan uang ataupun berinvestasi dalam sekuritas, sebab bisa menimbulkan penyusutan nilai investasi mereka ataupun apalagi kehilangan pokok. Buat mengelola resiko kredit, pemberi pinjaman serta investor kerap memakai model evaluasi kredit, melaksanakan uji tuntas pada peminjam, serta menetapkan batasan kredit serta persyaratan agunan.

Model Machine Learning sudah membantu perusahaan- perusahaan ini untuk meningkatkan akurasi analisis resiko kredit mereka, sediakan tata cara ilmiah buat mengenali calon debitur terlebih dulu.

Dalam proyek ini, saya akan membangun model risiko kredit untuk memprediksi risiko default klien untuk sebuah bank di Taiwan.

### Inspirasi:
Pada akhir kasus ini, akan dapat menjawab pertanyaan-pertanyaan di bawah ini.

1. Preprocessing Data; persiapan data; dan visualisasi data
2. Fitur Teknik dan fitur pilihan
3. Pengembangan Model
4. Evaluasi Model
5. Bagaimana kemungkinan pembayaran gagal bayar bervariasi menurut kategori variabel demografis yang berbeda?
6. Variabel mana yang merupakan prediktor terkuat dari pembayaran gagal bayar?

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

#### 2) Visualisasi Data:

##### Variabel Target:

Kami akan memvisualisasikan kolom target "default" untuk mengetahui seberapa implance (keseimbangan) data
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/24969671-b117-4d92-a033-c4e7bc09d983)
Data tersebut cukup tidak seimbang dimana sekitar 22% klien akan gagal bayar bulan depan.

##### Variabel SEX:
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/fc30c9da-2731-4348-b8a0-d1efee0675ff)
![image](https://github.com/JuanFakhri/Default_Dataset_Klien_Kartu_Kredit/assets/61308533/dfdcfeb4-fa7a-40be-92df-e69a25c2e0ca)

- Lebih banyak klien wanita memiliki kartu kredit daripada klien pria.
- 24% klien pria melakukan penipuan kartu kredit sedangkan rasio untuk wanita sekitar 20%

