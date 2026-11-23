# Aplikasi Prediksi Harga Mobil

Aplikasi Streamlit untuk memperkirakan harga mobil dari spesifikasi yang dimasukkan pengguna.

## Menjalankan di komputer

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploy ke Streamlit Community Cloud

1. Buat repository GitHub baru.
2. Unggah `app.py`, `requirements.txt`, dan `Automobile_Price_Clean.csv` ke root repository.
3. Buka https://share.streamlit.io/ dan login menggunakan GitHub.
4. Pilih **Create app**, pilih repository, branch `main`, dan file utama `app.py`.
5. Klik **Deploy**. Setelah proses selesai, salin URL aplikasi yang diberikan.

## Catatan model

Aplikasi melatih Random Forest Regressor 100 pohon saat pertama kali dijalankan menggunakan 201 baris dataset bersih. Preprocessing menggunakan imputasi rata-rata untuk fitur numerik dan kategori paling sering untuk fitur kategorikal, lalu One-Hot Encoding. Ini mereplikasi pendekatan dan jenis algoritma workflow Orange, tetapi merupakan pipeline scikit-learn yang dilatih ulang dari dataset, bukan ekspor file model internal Orange.
