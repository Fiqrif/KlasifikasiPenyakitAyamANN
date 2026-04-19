# Klasifikasi Penyakit Ayam Menggunakan Ekstraksi Fitur (HSV, RGB, GLCM, Entropy) & ANN

Proyek ini bertujuan untuk mengklasifikasikan jenis penyakit pada ayam berdasarkan citra feses (kotoran) menggunakan pendekatan **Computer Vision** tradisional dan **Artificial Neural Network (ANN)**. Berbeda dengan pendekatan CNN yang melakukan ekstraksi fitur secara otomatis, proyek ini melakukan ekstraksi fitur manual untuk mendapatkan karakteristik warna, tekstur, dan kompleksitas citra.

## 📌 Deskripsi Proyek
Model ini dilatih untuk mengenali 4 kategori kondisi ayam:
1.  **Sehat**
2.  **Coccidiosis**
3.  **NCD (Newcastle Disease)**
4.  **Salmonella**

Berdasarkan hasil pengujian, model mencapai tingkat akurasi sebesar **55,3%**. Model menunjukkan performa yang baik dalam mengenali kelas *Sehat* dan *Coccidiosis*, namun masih memiliki tantangan dalam membedakan kelas *NCD* karena kemiripan visual yang tinggi.

## 📊 Ekstraksi Fitur
Data input berupa citra diekstraksi menjadi **12 fitur numerik** utama:
- **Fitur Warna (HSV):** Mean & Standard Deviation dari *Hue* dan *Saturation*.
- **Fitur Warna (RGB):** Rata-rata nilai *Red*, *Green*, dan *Blue*.
- **Fitur Tekstur (GLCM):** *Contrast*, *Homogeneity*, *Energy*, dan *Correlation*.
- **Fitur Kompleksitas:** *Shannon Entropy*.

## 📂 Dataset
Dataset dibagi menjadi dua folder utama: `PenyakitAyam-Train` dan `PenyakitAyam-Test`.

* **Kaggle Dataset:** : https://www.kaggle.com/datasets/allandclive/chicken-disease-1
* **Google Drive:** 
* 1. Data Test : https://drive.google.com/drive/folders/1KAJp2zBhO2TWA66hh_drd9bMfvjUUTKF?usp=sharing
  2. Data Train : https://drive.google.com/drive/folders/16WcaRWzdi4l4wpZh3V6witJopvEHhz71?usp=sharing

## 🛠️ Teknologi yang Digunakan
- **Bahasa:** Python
- **Environment:** Google Colab / Jupyter Notebook
- **Library Utama:**
    - `OpenCV` & `PIL` (Pemrosesan Citra)
    - `Scikit-image` (Ekstraksi GLCM & Entropy)
    - `TensorFlow/Keras` (Membangun Arsitektur ANN)
    - `Pandas` & `NumPy` (Manipulasi Data)
    - `Matplotlib` & `Seaborn` (Visualisasi)

## 🧠 Arsitektur Model
Model menggunakan jaringan saraf tiruan (ANN) dengan struktur:
- **Input Layer:** 12 Neuron.
- **Hidden Layers:** - Dense (64) + BatchNormalization + Dropout (0.3)
    - Dense (32) + BatchNormalization + Dropout (0.2)
    - Dense (16)
- **Output Layer:** Dense (4) dengan fungsi aktivasi *Softmax*.
- **Optimizer:** Adam.

## 🚀 Cara Penggunaan
1. Clone repositori ini.
2. Pastikan dataset sudah tersedia di direktori yang sesuai (atau sesuaikan *path* di dalam notebook).
3. Jalankan file `2318072MuhamadFiqriFUTSKlasifikasiPenyakitAyamMetodeANN.ipynb`.
4. Kode akan melakukan ekstraksi fitur secara otomatis, menyimpannya ke dalam file `.xlsx`, dan melatih model ANN.

## 📈 Hasil Evaluasi
Hasil klasifikasi dievaluasi menggunakan *Confusion Matrix* dan *Classification Report*. Meskipun akurasi berada di angka 55,3%, proyek ini membuktikan bahwa kombinasi fitur warna dan tekstur dapat memberikan dasar klasifikasi penyakit hewan tanpa memerlukan sumber daya komputasi sebesar Deep Learning murni.

---
**Kontak:**
1. **Github :** @Fiqrif(https://github.com/Fiqrif)
2. **LinkedIn :** https://www.linkedin.com/in/muhamad-fiqri-firmansyah-3509612a6/
