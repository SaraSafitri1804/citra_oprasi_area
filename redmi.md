# Operasi Area: Filter Konvolusi pada Foto

## Deskripsi Proyek

Proyek ini merupakan implementasi operasi area dalam pengolahan citra digital menggunakan metode konvolusi spasial 2D. Program dibuat menggunakan Python untuk mengolah citra grayscale dengan beberapa jenis kernel filter dan membandingkan hasilnya melalui visualisasi.

Filter yang digunakan meliputi Mean, Gaussian, Sharpening, Sobel, dan Laplacian.

## Tujuan

1. Memahami konsep operasi area dan konvolusi spasial 2D.
2. Mengimplementasikan konvolusi secara manual menggunakan Python.
3. Mempelajari pengaruh berbagai kernel terhadap citra digital.
4. Membandingkan hasil penghalusan, penajaman, dan deteksi tepi.
5. Mengamati pengaruh filter terhadap citra yang diberi noise.

## Tools dan Library

- Python
- Visual Studio Code
- Jupyter Notebook
- NumPy
- Pillow (PIL)
- Matplotlib

## Metode yang Digunakan

### 1. Konversi Grayscale

Foto RGB diubah menjadi citra grayscale dengan rentang intensitas 0–255. Ukuran foto dibatasi hingga lebar maksimum 480 piksel agar proses konvolusi lebih efisien.

### 2. Konvolusi 2D

Konvolusi dilakukan dengan padding refleksi, membalik kernel, mengalikan nilai kernel dengan area citra, lalu menjumlahkan hasilnya untuk memperoleh nilai piksel baru.

### 3. Jenis Filter

- **Mean Filter:** Menghaluskan citra dengan menghitung rata-rata nilai piksel di sekitar piksel pusat.
- **Gaussian Filter:** Menghaluskan citra menggunakan bobot Gaussian yang lebih besar di bagian tengah kernel.
- **Sharpening Filter:** Mempertegas detail dan meningkatkan ketajaman citra.
- **Sobel Filter:** Mendeteksi tepi berdasarkan perubahan intensitas pada arah horizontal dan vertikal.
- **Laplacian Filter:** Mendeteksi tepi berdasarkan perubahan intensitas tingkat kedua.

### 4. Analisis Hasil

Hasil setiap filter divisualisasikan dan dibandingkan. Program juga menguji pengaruh ukuran kernel dan nilai sigma Gaussian serta membandingkan filter pada citra yang ditambahkan noise Gaussian.

## Struktur Proyek

```text
filter-konvolusi/
├── filter_konvolusi.ipynb
├── foto_uji.jpg
├── perbandingan_konvolusi.png
└── README.md
```

**Catatan:** `foto_uji.jpg` merupakan nama file yang ditetapkan pada notebook. Pastikan foto yang digunakan memiliki nama dan lokasi yang sesuai. File hasil visualisasi akan dibuat setelah sel terkait berhasil dijalankan.

## Instalasi

Pastikan Python sudah terpasang, kemudian instal library yang diperlukan melalui terminal:

```bash
pip install numpy pillow matplotlib
```

## Cara Menjalankan

1. Buka folder proyek di Visual Studio Code.
2. Buka file `filter_konvolusi.ipynb`.
3. Pastikan library sudah terpasang dan kernel Python tersedia.
4. Letakkan foto pada folder yang sesuai atau sesuaikan nilai `PATH_FOTO` di notebook.
5. Jalankan setiap sel secara berurutan.
6. Amati visualisasi hasil filter dan keluaran pengujian noise.

## Hasil yang Diharapkan

Program menghasilkan perbandingan citra asli dan grayscale, hasil Mean dan Gaussian, citra hasil sharpening, deteksi tepi Sobel dan Laplacian, serta pengujian pengaruh ukuran kernel dan noise.

## Kesimpulan

Konvolusi merupakan operasi area yang menghasilkan nilai piksel baru berdasarkan nilai piksel di sekitarnya. Filter Mean dan Gaussian digunakan untuk menghaluskan citra, Sharpening untuk mempertegas detail, sedangkan Sobel dan Laplacian untuk mendeteksi tepi. Pemilihan filter memengaruhi detail, ketajaman, dan noise pada hasil citra.
