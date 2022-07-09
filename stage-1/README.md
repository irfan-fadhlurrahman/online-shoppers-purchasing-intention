## Stage 1 -Exploratory Data Analysis, Insights & Visualization

### Exploratory Data Analysis

* Hampir seluruh kolom memiliki tipe data yang sesuai kecuali `operating_systems`, `browser`, `region`, 
dan `traffic type` yang seharusnya ber tipe string atau object karena keempat kolom tersebut bertipe kategorikal.
* Semua kolom tidak memiliki missing values.
* Semua kolom memiliki nilai summary yang cukup wajar walaupun seluruh variabel numerik memiliki nilai mean yang berbeda jauh dengan median karena metrik pengukuran memungkinkan didominasi nilai 0 apabila tidak ada aktivitas visitor.
* Kolom special_day hanya memiliki 6 unique values dan lebih baik di-treat sebagai tipe kategorikal.
* Kolom `special_day` dan `visitor_type` memiliki salah satu kategori yang terlalu mendominasi di atas 80% sehingga bisa tidak disertakan pada saat modelling.
* Selain itu, class imbalance terdapat di kolom target revenue dengan ratio 85:15. Kolom revenue memiliki hampir 2,000 pengunjung website menghasilkan revenue (15%) sedangkan lebih dari 10,000 pengunjung website tidak (85%).
* Seluruh kolom numerik memiliki distribusi yang right-skewed dan terdapat banyak outliers.
* Berdasarkan analisis korelasi semua kolom numerik dan kategorikal memiliki korelasi ke target kecuali feature `region`.
* Berdasarkan spearman's correlation yang ditunjukkan oleh heatmap, ada korelasi antar feature numerik yang significant di atas 0.8 yaitu kolom jumlah page dan jumlah durasi page memiliki korelasi yang tinggi yaitu 0.88 - 0.95.

### Insight
* Dengan lebih rendah exit_rates dan bounce_rates serta lebih tinggi page_values, maka visitor dengan perilaku seperti itu cenderung melakukan transaksi di e-commerce.
