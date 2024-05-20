# Tugas Praktikum { Pertemuan ke 11 } <img src=https://qph.fs.quoracdn.net/main-qimg-648763cc041459725b62108f4fdf5b91 width="110px" >


|**Nama**|**NIM**|**Kelas**|**Matkul**|
|----|---|-----|------|
|Nurul Aisyah|312310476|TI.23.A5|Basis Data|# Tugas Praktikum 4 Basis Data

## Buat Table pegawai dan isi datanya seperti berikut:
![Screenshot 2024-05-20 130022](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/fd805927-4eec-4a30-a20b-c4ccdf4a2ca8)

### Tugas Praktikum
1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000 !
2. Tampilkan pegawai yang tunjangannya NULL!
3. Tampilkan pegawai yang tunjangannya tidak NULL!
4. Tampilkan/hitung jumlah baris/record tabel pegawai!
5. Tampilkan/hitung jumlah total gaji di tabel pegawai!
6. Tampilkan/hitung rata-rata gaji pegawai!
7. Tampilkan gaji terkecil!
8. Tampilkan gaji terbesar!

#### 1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000 !

![image](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/fcc417bf-89dc-42f2-a9c7-427475034d10)
Penjelasan: Pernyataan ini menampilkan semua kolom dari tabel pegawai untuk pegawai yang gajinya tidak sama dengan 2.000.000 dan 1.250.000. Kondisi NOT IN (2000000, 1250000) memastikan bahwa hanya pegawai dengan gaji selain kedua nilai tersebut yang ditampilkan.

#### 2. Tampilkan pegawai yang tunjangannya NULL!

![image](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/c73a1f97-55f4-41a2-8979-42d1f1977c79)
Penjelasan: Pernyataan ini menampilkan semua kolom dari tabel pegawai untuk pegawai yang tidak memiliki tunjangan. Kondisi tunjangan IS NULL digunakan untuk memeriksa nilai NULL dalam kolom tunjangan.

#### 3. Tampilkan pegawai yang tunjangannya tidak NULL!

![image](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/1ed82217-89b6-493d-bce7-d718fc9e59f7)
Penjelasan: Pernyataan ini menampilkan semua kolom dari tabel pegawai untuk pegawai yang memiliki tunjangan. Kondisi tunjangan IS NOT NULL digunakan untuk memeriksa nilai yang bukan NULL dalam kolom tunjangan.

#### 4. Tampilkan/hitung jumlah baris/record tabel pegawai!

![gambar 4 praktikum ok](https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/7232b419-97e6-4ef3-bed9-8528897e0bae)
Penjelasan: Pernyataan ini menghitung jumlah total baris atau record dalam tabel pegawai. Fungsi COUNT(*) mengembalikan jumlah total baris yang ada, dan hasilnya diberi alias jumlah_pegawai.

#### 5. Tampilkan/hitung jumlah total gaji di tabel pegawai!

![Screenshot 2024-05-20 130456](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/c8542a73-a8f0-49d7-9b8c-465a9dac7954)
Penjelasan: Pernyataan ini menghitung jumlah total gaji dari semua pegawai dalam tabel pegawai. Fungsi SUM(gaji) menjumlahkan nilai dalam kolom gaji untuk setiap baris, dan hasilnya diberi alias total_gaji.

#### 6. Tampilkan/hitung rata-rata gaji pegawai!

![Screenshot 2024-05-20 130532](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/68b60eee-9ade-4eef-b17f-975d9bafd00f)
Penjelasan: Pernyataan ini menghitung rata-rata gaji dari semua pegawai dalam tabel pegawai. Fungsi AVG(gaji) mengembalikan nilai rata-rata dari kolom gaji, dan hasilnya diberi alias rata_rata_gaji.

#### 7. Tampilkan gaji terkecil!

![Screenshot 2024-05-20 130601](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/4db3c21b-aed2-424c-96e0-17ce0eb8f084)
Penjelasan: Pernyataan ini menampilkan gaji terkecil di antara semua pegawai dalam tabel pegawai. Fungsi MIN(gaji) mengembalikan nilai terkecil dari kolom gaji, dan hasilnya diberi alias gaji_terkecil.

#### 8. Tampilkan gaji terbesar!

![Screenshot 2024-05-20 130627](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/5e81eea3-2295-4f3d-b0d5-c8c3dec36c4b)
Penjelasan: Pernyataan ini menampilkan gaji terbesar di antara semua pegawai dalam tabel pegawai. Fungsi MAX(gaji) mengembalikan nilai terbesar dari kolom gaji, dan hasilnya diberi alias gaji_terbesar.


### Kesimpulan
Dalam MySQL, kita dapat menggunakan query untuk menampilkan jumlah hewan berdasarkan kriteria tertentu. Kesimpulannya adalah:

- Jumlah hewan berdasarkan pemilik (owner): Dengan menggunakan klausa group by antara kolom "owners" dan "id", serta fungsi COUNT, kita dapat menghitung jumlah hewan yang dimiliki oleh setiap pemilik.

- Jumlah hewan berdasarkan spesies: Dengan menggunakan klausa GROUP BY pada kolom "species" dan fungsi COUNT, kita dapat menghitung jumlah hewan untuk setiap spesies.

- Jumlah hewan berdasarkan jenis kelamin: Dengan menggunakan klausa GROUP BY pada kolom "sex" dan fungsi COUNT, kita dapat menghitung jumlah hewan untuk setiap jenis kelamin.

- Jumlah hewan berdasarkan spesies dan jenis kelamin (khusus cat dan dog): Dengan menggunakan klausa WHERE untuk memfilter spesies yang diinginkan dan klausa GROUP BY pada kolom "species" dan "sex" serta fungsi COUNT, kita dapat menghitung jumlah hewan untuk kombinasi spesies dan jenis kelamin tertentu.

- Jumlah hewan berdasarkan jenis kelamin yang diketahui: Dengan menggunakan klausa WHERE untuk memfilter jenis kelamin yang tidak NULL (diketahui) dan klausa GROUP BY pada kolom "sex" serta fungsi COUNT, kita dapat menghitung jumlah hewan untuk jenis kelamin yang diketahui.

Dengan menggunakan query-query ini, kita dapat memperoleh informasi statistik tentang jumlah hewan berdasarkan kriteria yang relevan dalam basis data MySQL.

## Buat table hewan dan isi datanya seperti berikut:
<img width="371" alt="gambar table hewan" src="https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/1aed8694-0460-4c82-83f8-09e7d3e9c2a8">

### Tugas Praktikum
1. Tampilkan jumlah hewan yang dimiliki setiap owner.
2. Tampilkan jumlah hewan berdasarkan spesies
3. Tampilkan jumlah hewan berdasarkan jenis kelamin
4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin
5. Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin
6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja

#### 1. Tampilkan jumlah hewan yang dimiliki setiap owner.

<img width="391" alt="gambar 1 hewan" src="https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/b127c79e-90d7-4851-856a-986e6b0f23ca">

#### 2. Tampilkan jumlah hewan berdasarkan spesies

<img width="364" alt="gambar 2 hewan" src="https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/2caa3c99-d2bb-49e5-8151-eea41518f3c5">

#### 3. Tampilkan jumlah hewan berdasarkan jenis kelamin

<img width="357" alt="gambar 3 hewan" src="https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/01d05899-5d4c-4e03-9f2d-141b30105097">

#### 4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin

<img width="448" alt="gambar 4 hewan" src="https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/ff18abed-5d71-4073-854e-86f7383026ff">

#### 5. Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin

![gambar 5 hewan](https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/a757d651-4a26-4354-b066-d1783e3455ef)

#### 6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja

![gambar 6 hewan](https://github.com/Akramfarrasanto/Praktikum-4-Basis-Data/assets/115552876/2b1c31c7-e922-4da6-abcd-90a29c98c3be)

### Kesimpulan
#### Dalam MySQL, kita dapat menggunakan query untuk menampilkan jumlah hewan berdasarkan kriteria tertentu. Kesimpulannya adalah:
#### - Jumlah hewan berdasarkan pemilik (owner): Dengan menggunakan klausa group by antara kolom "owners" dan "id", serta fungsi COUNT, kita dapat menghitung jumlah hewan yang dimiliki oleh setiap pemilik.
#### - Jumlah hewan berdasarkan spesies: Dengan menggunakan klausa GROUP BY pada kolom "species" dan fungsi COUNT, kita dapat menghitung jumlah hewan untuk setiap spesies.
#### - Jumlah hewan berdasarkan jenis kelamin: Dengan menggunakan klausa GROUP BY pada kolom "sex" dan fungsi COUNT, kita dapat menghitung jumlah hewan untuk setiap jenis kelamin.
#### - Jumlah hewan berdasarkan spesies dan jenis kelamin (khusus cat dan dog): Dengan menggunakan klausa WHERE untuk memfilter spesies yang diinginkan dan klausa GROUP BY pada kolom "species" dan "sex" serta fungsi COUNT, kita dapat menghitung jumlah hewan untuk kombinasi spesies dan jenis kelamin tertentu.
#### - Jumlah hewan berdasarkan jenis kelamin yang diketahui: Dengan menggunakan klausa WHERE untuk memfilter jenis kelamin yang tidak NULL (diketahui) dan klausa GROUP BY pada kolom "sex" serta fungsi COUNT, kita dapat menghitung jumlah hewan untuk jenis kelamin yang diketahui.
#### Dengan menggunakan query-query ini, kita dapat memperoleh informasi statistik tentang jumlah hewan berdasarkan kriteria yang relevan dalam basis data MySQL.
