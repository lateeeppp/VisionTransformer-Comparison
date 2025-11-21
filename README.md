# Vision Transformer Comparison

Cara Menjalankan Kode
Repository ini berisi satu notebook utama (**122140137_Ikhsannudin Lathief_VisionTransformer.ipynb**) yang melakukan seluruh proses:
- Load dataset
- Preprocessing & augmentasi
- Training 3 model (ViT-B16, DeiT-Small, Swin-Tiny)
- Evaluasi performa
- Visualisasi (learning curve, confusion matrix)
- Pengukuran waktu inferensi
- Penyimpanan hasil prediksi (jawaban_[nama_model].csv)
- Penyimpanan model weights

Notebook ini bersifat **end-to-end**, sehingga tidak membutuhkan file Python tambahan.

---

## 1. Persiapan Lingkungan

Install dependency:

```bash
pip install -r requirements.txt
```

## 2. Struktur Dataset

```javascript
IF25-4041-dataset/
    train/
        <semua gambar .jpg>
    train.csv
```

## 3. Cara Menjalankan Notebook

1. Buka di Google Colab
```bash
122140137_Ikhsannudin Lathief_VisionTransformer.ipynb
```
2. Jalankan seluruh cell
3. Notebook akan:
  - Mempersiapkan dataset
  - Melatih ViT, DeiT, dan Swin
  - Mengevaluasi performa semua model
  - Menghasilkan visualisasi kurva dan confusion matrix
  - Mengukur waktu inferensi
  - Menyimpan file hasil prediksi jawaban_<model>.csv
  - Menyimpan model terbaik di folder weights/ (untuk weights terlalu besar sehingga tidak bisa diupload ke Github)

## 4. Lokasi Output

Setelah menjalankan notebook, output akan muncul di:
```php-template
results/<model_name>/
    metrics_<model>.csv
    history_<model>.csv
    learning_curve_<model>.png
    confusion_matrix_<model>.png
    jawaban_<model>.csv
```

Waktu inferensi berisi file:
```
inference_test_summary.csv
```
Model weights disimpan di:
```php-template
weights/<nama_model>_best.pth
```
