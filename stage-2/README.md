## Stage 2 - Data Preprocessing
* Data duplikasi sebanyak 125 rows di-drop dari seluruh dataset.
* Outliers pada feature numerik tidak dihapus tetapi jumlahnya dikurangi dengan feature transformation. Feature transformation yang tepat digunakan yaitu
log-transformation menggunakan np.log1p dan power-transformation menggunakan yeo-johnson transformer.
* Agar feature numerik memiliki range yang sama atau memiliki mean dan standar deviasi yang hampir sama, maka beberapa feature scaling yang tepat digunakan yaitu:
MinMaxScaler, StandardScaler, atay RobustScaler.
* Untuk feature kategorikal, perlu feature encoding agar tipe string dapat diubah menjadi tipe int atau float. Berikut ini strategi feature enconding:
  * Sin-cos transformation atau Quarter binning untuk kolom month.
  * One-hot encoding untuk visitor_type dan weekend.
  * Untuk operating_systems, browser, region, dan traffic_type bisa menggunakan count encoder, frequency encoder target encoder, rare-label encoding + one-hot enconding.
* Karena kolom target memiliki class imbalance dengan ratio 85:15 maka berikut cara yang tepat untuk menanganinya melakukan resampling (oversampling, undersampling, or over-undersampling) agar distribusi target menjadi 50:50. Selain itu, memberi class weight lebih besar pada minority class dari kolom target dan menggunakan metrik evaluasi model yang tepat seperti ROC-AUC atau f1-score.
* Data-preprocessing untuk model linear dan tree-based dibuat terpisah karena feature numerik tidak perlu ditransform atau discaling apabila menggunakan tree-based model.
