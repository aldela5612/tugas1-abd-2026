# Data Tugas 1

## Dataset yang Dipilih

Dataset yang digunakan dalam Tugas 1 adalah **TMDB Movies Dataset 2023 – 930K Movies** yang diperoleh dari Kaggle. Dataset ini berisi data film dari The Movie Database (TMDB) dengan berbagai informasi seperti judul film, tanggal rilis, rating, jumlah vote, pendapatan, durasi, bahasa, genre, perusahaan produksi, negara produksi, deskripsi film, dan informasi lainnya. Struktur dataset yang tersedia memiliki 24 kolom.

| Item                    | Isi                                                                                         |
| ----------------------- | ------------------------------------------------------------------------------------------- |
| Nama dataset            | TMDB Movies Dataset 2023 – 930K Movies                                                      |
| Sumber                  | Kaggle                                                                                      |
| URL Sumber              | https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies/versions/458 |
| Lisensi/ketentuan pakai | ODC Attribution License (ODC-By), sesuai informasi lisensi pada halaman dataset Kaggle      |
| Ukuran                  | 1.164.598 baris dan 24 kolom berdasarkan file dataset yang digunakan                        |
| Periode data            | Tahun/tanggal rilis film bervariasi sesuai data yang tersedia pada TMDB                     |
| Unit analisis           | Film/movie                                                                                  |

## Deskripsi Dataset

TMDB Movies Dataset merupakan dataset yang berisi informasi mengenai film yang bersumber dari The Movie Database (TMDB).

Dataset memiliki berbagai atribut yang menggambarkan karakteristik suatu film, antara lain:

* ID film
* Judul film
* Rating rata-rata
* Jumlah vote
* Status film
* Tanggal rilis
* Pendapatan
* Durasi film
* Kategori adult
* Backdrop
* Anggaran produksi
* Homepage
* IMDb ID
* Bahasa asli
* Judul asli
* Ringkasan/overview film
* Popularity
* Poster
* Tagline
* Genre
* Perusahaan produksi
* Negara produksi
* Bahasa yang digunakan
* Keywords

Contoh struktur kolom dataset menunjukkan bahwa setiap baris merepresentasikan satu film dan kolom-kolom tersebut berisi atribut yang berkaitan dengan film tersebut.

## Sumber Dataset

Dataset diperoleh dari platform Kaggle melalui halaman:

https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies/versions/458

Dataset tersebut dipublikasikan oleh pengguna Kaggle `asaniczka` dan berisi data film dari TMDB. Halaman dataset mencantumkan bahwa dataset diperbarui secara berkala/daily.

## Lisensi dan Ketentuan Penggunaan

Berdasarkan informasi yang tercantum pada halaman Kaggle, dataset menggunakan:

**ODC Attribution License (ODC-By).**

Penggunaan dataset dalam tugas ini dilakukan untuk keperluan akademik dan mengikuti ketentuan lisensi serta ketentuan penggunaan yang berlaku pada sumber dataset.

Sumber dataset tetap dicantumkan dalam dokumentasi proyek sebagai bentuk atribusi.

## Periode Data

Dataset memiliki tanggal atau tahun rilis film yang beragam. Periode data mengikuti informasi film yang tersedia pada sumber TMDB dan versi dataset yang digunakan.

Karena dataset dapat diperbarui oleh pemilik dataset, periode dan jumlah data dapat berbeda antara satu versi dataset dengan versi lainnya.

Oleh karena itu, jumlah data yang digunakan dalam Tugas 1 mengacu pada file dataset yang telah diunduh dan digunakan secara lokal dalam project ini.

## Unit Analisis

Unit analisis dataset adalah **film/movie**.

Setiap baris merepresentasikan satu data film, sedangkan setiap kolom merepresentasikan atribut atau karakteristik yang berkaitan dengan film tersebut.

Dengan demikian:

* **Unit analisis:** film/movie
* **Observasi:** 1.164.598 film/baris
* **Variabel/atribut:** 24 kolom

## Ukuran Dataset

Berdasarkan pemeriksaan terhadap file dataset yang digunakan pada project ini, diperoleh:

```text
Jumlah baris  : 1.164.598
Jumlah kolom  : 24
```

Dataset tersebut memenuhi ketentuan ukuran dataset pada Tugas 1 karena jumlah barisnya **lebih dari 1.000.000 baris**.

Pemeriksaan dilakukan menggunakan Python dan Pandas pada notebook `01_data_profiling.ipynb`.

## File Dataset

Dataset mentah disimpan pada folder:

```text
data/raw/
```

Nama file:

```text
TMDB_movie_dataset_v11.csv
```

Sehingga lokasi file dataset adalah:

```text
data/raw/TMDB_movie_dataset_v11.csv
```

File tersebut merupakan data mentah yang diperoleh dari dataset Kaggle dan digunakan sebagai input utama dalam proses data profiling.

## Struktur Folder

Struktur folder data pada project adalah:

```text
data/
├── README.md
├── raw/
│   └── TMDB_movie_dataset_v11.csv
└── processed/
```

Keterangan:

### `data/README.md`

Berisi dokumentasi mengenai dataset yang digunakan, sumber dataset, periode data, unit analisis, ukuran dataset, serta aturan penyimpanan data.

### `data/raw/`

Digunakan untuk menyimpan dataset mentah yang diperoleh dari sumber eksternal.

Dataset pada folder ini tidak boleh diubah secara langsung.

### `data/processed/`

Digunakan untuk menyimpan hasil transformasi, pembersihan, atau preprocessing dataset apabila diperlukan.

## Cara Memperoleh Data

Dataset diperoleh dengan langkah-langkah berikut:

1. Membuka halaman dataset TMDB Movies Dataset pada Kaggle.
2. Mengunduh dataset dari halaman Kaggle.
3. Menempatkan file dataset pada folder `data/raw/`.
4. Memastikan file dataset dapat dibaca menggunakan Python dan Pandas.
5. Memeriksa jumlah baris dan kolom dataset.
6. Menggunakan dataset sebagai input pada notebook `01_data_profiling.ipynb`.

URL sumber dataset:

https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies/versions/458

## DATA_PATH

Dataset dibaca melalui variabel `DATA_PATH` pada notebook:

```text
notebooks/01_data_profiling.ipynb
```

Konfigurasi yang digunakan:

```python
DATA_PATH = "data/raw/TMDB_movie_dataset_v11.csv"
```

Path tersebut digunakan untuk mengarahkan proses pembacaan data ke file dataset yang berada di folder `data/raw/`.

## Pemeriksaan Awal Dataset

Sebelum melakukan proses data profiling secara keseluruhan, dilakukan pemeriksaan awal dengan membaca sebagian data.

Kode yang digunakan:

```python
import pandas as pd

df = pd.read_csv(DATA_PATH, nrows=10000)

print(df.head())
print(df.shape)
```

Hasil pemeriksaan awal:

```text
(10000, 24)
```

Hasil tersebut menunjukkan bahwa dataset berhasil dibaca dan memiliki 24 kolom.

Selanjutnya dilakukan pembacaan keseluruhan dataset untuk mengetahui jumlah observasi:

```python
import pandas as pd

df_full = pd.read_csv(DATA_PATH)

print("Jumlah baris :", df_full.shape[0])
print("Jumlah kolom :", df_full.shape[1])
```

Hasil:

```text
Jumlah baris : 1164598
Jumlah kolom : 24
```

## Tujuan Penggunaan Dataset

Dataset digunakan sebagai dataset utama dalam Tugas 1 untuk melakukan **data profiling** dan analisis karakteristik data berukuran besar.

Data profiling dilakukan untuk memperoleh gambaran mengenai:

* struktur dataset;
* jumlah baris dan kolom;
* tipe data;
* nilai yang hilang atau missing values;
* data duplikat;
* jumlah nilai unik;
* statistik deskriptif;
* distribusi data;
* karakteristik setiap variabel;
* serta kualitas data secara umum.

Hasil profiling akan digunakan untuk memahami kondisi dataset sebelum dilakukan proses analisis atau pengolahan data lebih lanjut.

## Aturan Penyimpanan Data

Data mentah disimpan pada:

```text
data/raw/
```

Data mentah tidak boleh diubah secara langsung.

Apabila diperlukan proses:

* cleaning;
* transformation;
* preprocessing;
* filtering;
* atau perubahan struktur data,

maka hasilnya disimpan pada:

```text
data/processed/
```

Proses transformasi harus dapat direproduksi sehingga proses pengolahan data dapat ditelusuri kembali.

## Aturan Git dan GitHub

Dataset mentah berukuran besar tidak diunggah ke repository GitHub.

Folder dataset mentah dan hasil data processing dimasukkan ke dalam `.gitignore`:

```text
data/raw/
data/processed/
```

Dengan konfigurasi tersebut, file CSV dataset tidak ikut di-commit ke repository GitHub.

Dokumentasi dataset tetap disimpan melalui:

```text
data/README.md
```

Dengan demikian, repository tetap memiliki dokumentasi mengenai sumber dan cara memperoleh dataset tanpa menyimpan file dataset berukuran besar secara langsung.

## Reproduksibilitas

Untuk menjalankan kembali proses data profiling, pengguna perlu:

1. Mengunduh dataset dari sumber Kaggle.
2. Menempatkan file `TMDB_movie_dataset_v11.csv` pada folder `data/raw/`.
3. Membuka notebook `notebooks/01_data_profiling.ipynb`.
4. Memastikan nilai `DATA_PATH` sesuai dengan lokasi file dataset.
5. Menjalankan cell pada notebook secara berurutan.

Konfigurasi path:

```python
DATA_PATH = "data/raw/TMDB_movie_dataset_v11.csv"
```

## Ringkasan Dataset

Ringkasan dataset yang digunakan dalam Tugas 1:

| Informasi          | Nilai                                  |
| ------------------ | -------------------------------------- |
| Dataset            | TMDB Movies Dataset 2023 – 930K Movies |
| Sumber             | Kaggle                                 |
| Sumber data        | The Movie Database (TMDB)              |
| File               | `TMDB_movie_dataset_v11.csv`           |
| Jumlah baris       | 1.164.598                              |
| Jumlah kolom       | 24                                     |
| Unit analisis      | Film/movie                             |
| Format             | CSV                                    |
| Folder data mentah | `data/raw/`                            |
| Notebook profiling | `notebooks/01_data_profiling.ipynb`    |
| DATA_PATH          | `data/raw/TMDB_movie_dataset_v11.csv`  |
| Lisensi            | ODC Attribution License (ODC-By)       |

## Referensi Sumber Data

**Kaggle – TMDB Movies Dataset 2023 – 930K Movies**

https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies/versions/458

**The Movie Database (TMDB)**

https://www.themoviedb.org/

## Catatan

Jumlah baris yang dicantumkan pada dokumentasi ini merupakan jumlah baris dari file dataset yang digunakan dalam project ini, yaitu **1.164.598 baris**.

Dataset Kaggle dapat mengalami pembaruan sehingga jumlah data pada versi yang berbeda dapat berubah. Oleh karena itu, dokumentasi ini mengacu pada file dataset yang digunakan secara aktual dalam project.

Dataset mentah tidak dimodifikasi dan disimpan pada folder `data/raw/`. Setiap hasil pengolahan atau transformasi data harus disimpan secara terpisah pada folder `data/processed/`.

---

**Dataset Tugas 1:** TMDB Movies Dataset
**Sumber:** Kaggle
**Jumlah data yang digunakan:** 1.164.598 baris × 24 kolom
