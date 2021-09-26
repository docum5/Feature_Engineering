# Feature_Engineering

## Handling categories

***1. Nominal***

- One Hot Encoding : variables with many categories
  Dalam beberapa kasus, beberapa variabel kategori memiliki unique value yang sangat banyak
  sehingga jika kita langsung mengaplikasikan dummy variable kita akan berujung kepada dataframe 
  yang memiliki banyak sekali variabel baru. 
  Berikut langkah yang dapat dilakukan:
  1. Cek berapa unique values per variabel
  2. Find top x most frequent categories for that variable
  3. Jadi kita hanya mempertimbangkan 10 kategori itu aja yang lainnya dianggap 0 

- Count / Frequency Encoding : apabila dalam suatu variabel ada banyak unique valuesnya 
  Mengubah kategorikal variabel(nominal) menjadi angka, yang mana angka tersebut merupakan 
  frekuensi kemunculan data tersebut. 
  contoh : Amerika muncul 20 kali --> Amerika diinisialkan menjadi 20
           Indonesia muncul 34 kali --> Indonesia diinisialkan menjadi 34
           Jepang muncul 44 kali --> Jepang diinisialkan menjadi 44 

- pd.get_dummies = One hot encoding biasa. 

***2. Ordinal***

- Gunakan dictionary untuk menetukan urutan 
  contoh : SMA = 1 , kuliah = 2 , dkk

- Count / Frequency Encoding : Sama seperti nominal, tapi dibuat dalam bentu dictionary

- Ganti dengan nilai meannya. Group by berdasarkan target values
