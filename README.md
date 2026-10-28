# Praktik Pengolahan Citra Digital: Pseudocolor

## Identitas Mahasiswa
- **Nama:** Said Hibban
- **NIM:** 24260016
- **Mata Kuliah:** Pengolahan Citra Digital

## 1. Deskripsi
Program ini dibuat menggunakan Python di Google Colab untuk mengubah gambar hitam putih menjadi gambar berwarna menggunakan metode **Pseudocolor**. Proses ini dilakukan dengan memberikan warna berbeda pada tingkat intensitas piksel gambar.

## 2. Tujuan
- Memahami bahwa gambar digital tersusun dari nilai-nilai piksel.
- Mengetahui cara membaca dan menampilkan gambar menggunakan Python.
- Mempraktikkan metode pseudocolor untuk memberikan warna pada gambar grayscale.

## 3. Tools dan Library
- **Google Colab:** Tempat menjalankan kode Python.
- **OpenCV:** Mengolah gambar dan menerapkan peta warna.
- **Matplotlib:** Menampilkan gambar dan hasil pengolahan.
- **Google Colab Files:** Mengunggah gambar dari komputer.

## 4. Langkah-Langkah Program

1. **Mengunggah gambar**  
   Gambar hitam putih dipilih dari komputer menggunakan fitur `files.upload()`.

2. **Membaca gambar**  
   Gambar dibaca dalam format grayscale, sehingga setiap piksel memiliki nilai intensitas dari 0 sampai 255. Nilai 0 menunjukkan hitam, sedangkan nilai 255 menunjukkan putih.

3. **Menampilkan gambar asli**  
   Gambar ditampilkan menggunakan Matplotlib untuk melihat kondisi sebelum diproses.

4. **Menerapkan metode pseudocolor**  
   Fungsi `cv2.applyColorMap()` digunakan dengan peta warna `COLORMAP_JET` untuk mengubah nilai intensitas grayscale menjadi warna.

5. **Menampilkan hasil**  
   Hasil pengolahan ditampilkan untuk membandingkan gambar asli dengan gambar yang sudah diberi warna.

## 5. Penjelasan Kode Utama

```python
img = cv2.imread(nama_file, cv2.IMREAD_GRAYSCALE)
```

Kode ini membaca gambar yang diunggah dan mengubahnya menjadi grayscale.

```python
hasil = cv2.applyColorMap(img, cv2.COLORMAP_JET)
```

Kode ini menerapkan peta warna JET pada gambar grayscale. Intensitas piksel dipetakan menjadi warna tertentu.

```python
hasil = cv2.cvtColor(hasil, cv2.COLOR_BGR2RGB)
```

Kode ini mengubah urutan kanal warna dari BGR menjadi RGB agar warna ditampilkan dengan benar oleh Matplotlib.

## 6. Hasil
Gambar yang awalnya hitam putih akan ditampilkan dalam warna berdasarkan nilai intensitas pikselnya. Perubahan warna ini membantu memperlihatkan perbedaan tingkat intensitas pada gambar.

## 7. Kesimpulan
Berdasarkan praktik ini, gambar grayscale dapat diberi warna menggunakan metode pseudocolor dengan bantuan Python dan OpenCV. Metode ini mengubah representasi intensitas piksel menjadi warna tertentu, tetapi **tidak mengembalikan warna asli objek**. Warna yang dihasilkan merupakan warna buatan berdasarkan peta warna yang digunakan.
