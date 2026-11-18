# introduction-Machine-Learning-Supervised-Learning

# Pengantar Machine Learning dengan Scikit-Learn
 
Kumpulan contoh kode Python untuk memahami konsep dasar Machine Learning: supervised learning (regresi & klasifikasi), underfitting/overfitting, dan unsupervised learning (clustering).
 
## Isi
 
| No | Topik | Algoritma | Dataset |
|----|-------|-----------|---------|
| 1 | Regresi Linear | `LinearRegression` | Data dummy (`y = 4 + 3x + noise`) |
| 2 | Underfitting vs Good Fit vs Overfitting | `PolynomialFeatures` + `LinearRegression` (degree 1, 2, 30) | Data dummy |
| 3 | Klasifikasi & Evaluasi | `KNeighborsClassifier` (k=5) + Confusion Matrix | `load_breast_cancer` |
| 4 | Clustering | `KMeans` (4 cluster) | `make_blobs` |
 
## Penjelasan Singkat
 
### 1. Linear Regression
Membuat 100 data dummy dengan hubungan linear dan noise, melatih model, lalu memvisualisasikan garis prediksi terhadap data latih.
 
### 2. Underfitting vs Overfitting
Membandingkan tiga model polinomial pada data yang sama:
- **Degree 1**: underfitting (high bias), model terlalu sederhana.
- **Degree 2**: good fit, model optimal.
- **Degree 30**: overfitting (high variance), model menangkap noise.
### 3. Klasifikasi KNN + Confusion Matrix
- Data dibagi 80% training dan 20% testing (`random_state=42`).
- Model KNN dengan `n_neighbors=5`.
- Evaluasi memakai confusion matrix dan metrik:
| Metrik | Rumus |
|--------|-------|
| Accuracy | (TP + TN) / (TP + TN + FP + FN) |
| Precision | TP / (TP + FP) |
| Recall (Sensitivity) | TP / (TP + FN) |
| Specificity | TN / (TN + FP) |
 
### 4. K-Means Clustering
Menghasilkan 300 titik tanpa label di 4 pusat, mengelompokkannya dengan K-Means, lalu menampilkan hasil cluster beserta centroid.
 
## Kebutuhan
 
- Python 3.8+
- numpy
- matplotlib
- scikit-learn
- seaborn
## Instalasi
 
```bash
pip install numpy matplotlib scikit-learn seaborn
```
 
## Cara Menjalankan
 
1. Simpan kode ke file, misalnya `ml_basics.py` (atau jalankan per bagian di Jupyter Notebook / Google Colab).
2. Jalankan:
```bash
python ml_basics.py
```
 
Setiap bagian akan menampilkan grafik; tutup jendela plot untuk lanjut ke bagian berikutnya. Metrik evaluasi KNN dicetak di terminal.
 
## Catatan
 
- Variabel `X` dan `y` ditimpa pada setiap bagian, jadi jalankan secara berurutan atau pisahkan per bagian.
- `KMeans` tanpa `random_state` dapat menghasilkan label cluster berbeda di setiap eksekusi.
- Pada `KMeans`, `n_init` dapat diatur eksplisit (mis. `n_init=10`) untuk menghindari warning di versi scikit-learn tertentu.
## Konsep yang Dipelajari
 
- Supervised vs Unsupervised Learning
- Bias-Variance Tradeoff
- Train/Test Split
- Confusion Matrix, Accuracy, Precision, Recall, Specificity
 