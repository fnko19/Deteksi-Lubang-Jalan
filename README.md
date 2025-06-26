# Deteksi Lubang Jalan menggunakan Metode Canny Edge Detection

Proyek ini melakukan deteksi lubang jalan (*pothole*) secara sederhana pada video menggunakan teknik pengolahan citra klasik: konversi ke grayscale, Gaussian blur, deteksi tepi Canny, morfologi closing, dan penyaringan kontur. Output-nya adalah video baru dengan lubang jalan yang terdeteksi diberi kotak dan label.

## 📁 Struktur File

```
.
├── DetectionPlotholeCanny.ipynb  # Notebook utama deteksi lubang (untuk dijalankan di Google Colab)
├── README.md                # Dokumentasi proyek ini
└── p.mp4                    # Video input (simpan di Google Drive Anda)
```

## 🧰 Kebutuhan
Download sampel video yang digunakan dalam proyek ini disini:
https://drive.google.com/file/d/1rDsXpmt5lZ9AnK6BCgc2hHmdjCgcDPVK/view?usp=sharing

Lalu, jalankan perintah berikut di sel kode Colab untuk menginstal dependensi (jika belum tersedia):

```python
!pip install opencv-python
# Jika terjadi konflik dependensi, gunakan:
# !pip install opencv-python-headless
```

Kemudian *mount* Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Pastikan video Anda disimpan di Google Drive dan path-nya sesuai di script (misalnya: `/content/drive/MyDrive/p.mp4`).

## 🧪 Cara Menjalankan

Buka dan jalankan file notebook [`TB_VISKOM_D121221054.ipynb`](./TB_VISKOM_D121221054.ipynb) di Google Colab.
(untu File satunya yang DetectionPlotholeCanny.ipynb merupakan source program sebelum revisi bersama dosen pada saat presentasi akhir
Tugas Besar Mata Kulia Visi KOmputer)

Pastikan Anda:

1. Menginstal dependensi:
    ```python
    !pip install opencv-python
    ```

2. Mount Google Drive:
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```

3. Ubah `video_path` sesuai lokasi video Anda di Google Drive.

Output video akan disimpan di:  
```
/content/........mp4 #sesuai dengan nama output path yang ada pada code progra
```

## ✅ Hasil

- Hasil berupa video yang diberi anotasi dengan kotak pada area yang diduga sebagai lubang jalan berdasarkan bentuk dan ukuran.
- Ini merupakan pendekatan klasik (tanpa pembelajaran mesin), akurasi tergantung pada kualitas video dan kondisi jalan.

## 📌 Catatan

- Sesuaikan parameter seperti ambang batas Canny atau filter kontur agar performa lebih baik untuk lingkungan yang berbeda.
- Lebih lanjut menambahkan analisis intensitas atau penyaringan temporal untuk hasil yang lebih akurat.
