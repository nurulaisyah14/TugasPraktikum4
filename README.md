# Tugas Praktikum { Pertemuan ke 11 } <img src=https://logos-download.com/wp-content/uploads/2016/05/MySQL_logo_logotype.png width="130px" >


|**Nama**|**NIM**|**Kelas**|**Matkul**|
|----|---|-----|------|
|Nurul Aisyah|312310476|TI.23.A.5|Basis Data|

# Soal Latihan Praktikum ( Pegawai )

![alt text](Screenshot/TugasPraktikumP.png)

**Perintah SQL :**

```
CREATE TABLE pegawai (
    idpegawai VARCHAR(5) PRIMARY KEY,
    nama_depan VARCHAR(10) NOT NULL,
    nama_belakang VARCHAR(15) NOT NULL,
    email VARCHAR(25) UNIQUE KEY,
    telepon VARCHAR(15),
    tgl_kontrak DATA,
    id_job VARCHAR(5),
    gaji INT,
    tunjangan INT
    );

INSERT INTO pegawai VALUES
    ('E001', 'Ferry', 'Gustiawan', 'ferry@yahoo.com', '07117059004', '2005-09-01', 'L0001', 2000000, 500000),
	('E002', 'Aris', 'Ganiardi', 'aris@yahoo.com', '081312345678', '2006-09-01', 'L0002', 2000000, 200000),
	('E003', 'Faiz', 'Ahnad', 'faiz@gmail.com', '081367384322', '2006-10-01', 'L0003', 1500000, NULL),
	('E004', 'Emna', 'Bunton', 'emna@gmail.com', '081363484342', '2006-10-01', 'L0004', 1500000, 9),
	('E005', 'Mike', 'Scoff', 'mike@plasa.com', '08163454555', '2007-09-01', 'L0005', 1250000, 9),
	('E006', 'Lincoln', 'Burrows', 'linc@yahoo.com', '08527388432', '2008-09-01', 'L0006', 1750000, NULL);
```

***Output :***

![alt text]![Screenshot 2024-05-20 134009](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/5447855e-fa88-40db-98cd-4d3c34efd56e)


## Tugas Praktikum

**1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000 !**

```
SELECT*FROM pegawai WHERE gaji NOT IN (2000000, 1250000);
```

***Output :***

![Screenshot 2024-05-20 134110](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/00604c68-cdf5-4b67-9254-7457879b8b9a)


**2. Tampilkan pegawai yang tunjangannya NULL!**

```
SELECT*FROM pegawai WHERE tunjangan IS NULL;
```

***Output :***

![Screenshot 2024-05-20 134155](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/9e6b6df7-d5fe-4fee-af98-deffd3bda3e5)


**3. Tampilkan pegawai yang tunjangannya tidak NULL!**

```
SELECT*FROM pegawai WHERE tunjangan IS NOT NULL;
```

***Output :***

![Screenshot 2024-05-20 134331](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/62eb668a-e4d0-4fe6-a209-f0a3f00b8470)



**4. Tampilkan/hitung jumlah baris/record tabel pegawai!**

```
SELECT COUNT(*) AS jmlh_pegawai FROM pegawai;
```

***Output :***

![Screenshot 2024-05-20 134417](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/0d6d38be-022b-41f1-b5ed-c5ff012858be)


**5. Tampilkan/hitung jumlah total gaji di tabel pegawai!**

```
SELECT SUM(gaji) AS ttl_gaji FROM pegawai;
```

***Output :***

![Screenshot 2024-05-20 134453](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/724e2bfd-307e-4df4-a34a-7ad181f2a2a1)


**6. Tampilkan/hitung rata-rata gaji pegawai!**

```
SELECT AVG(gaji) AS mean_gaji FROM pegawai;
```

***Output :***

![Screenshot 2024-05-20 134536](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/d917e8b6-ff90-4608-a119-70d99e986863)


**7. Tampilkan gaji terkecil!**

```
SELECT MIN(gaji) AS terkecil FROM pegawai;
```

***Output :***

![Screenshot 2024-05-20 134607](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/dcd5d587-8245-4d31-b27e-2672bd3506bf)


**8. Tampilkan gaji terbesar!**

```
SELECT MAX(gaji) AS terbesar FROM pegawai;
```

***Output :***

![Screenshot 2024-05-20 134633](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/caa4347c-c5ee-40d4-be42-3826c25fc840)


# Soal Latihan Praktikum ( Hewan )

![alt text](Screenshot/TugasPraktikumH.png)

**Perintah SQL :**

```
CREATE TABLE hewan (
    id VARCHAR (5) PRIMARY KEY,
    name VARCHAR (10) NOT NULL,
    owner VARCHAR (10),
    species VARCHAR (10),
    sex enum('M', 'F')
    );

INSERT INTO hewan VALUES
    ('p1', 'Puffball', 'Diane', 'Hamster', 'F'),
    ('p2', 'Claws', 'Gwen', 'Cat', 'M'),
    ('p3', 'Fluffy', 'Haro 1d', 'Cat', 'F'),
    ('p4', 'Buffy', 'Haro 1d', 'Dog', 'F'),
    ('p5', 'Fang', 'Benny', 'Dog', 'M'),
    ('p6', 'Bowser', 'Diane', 'Dog', 'M'),
    ('p7', 'Chirpy', 'Gwen', 'Bird', 'F'),
    ('p8', 'Whistler', 'Gwen', 'Bird', NULL),
    ('p9', 'Slim', 'Benny', 'Snake', 'M');
```

***Output :***

![Screenshot 2024-05-20 134743](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/825338e7-435f-4fa0-9835-4fe967ac9d47)


## Tugas Praktikum

**1. Tampilkan jumlah hewan yang dimiliki setiap owner.**

```
SELECT owner, COUNT(*) AS jmlh_hewan FROM hewan GROUP BY owner;
```

***Output :***

![Screenshot 2024-05-20 134811](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/c81a905f-9ffd-4e5c-a637-1b6dbfbf73c7)


**2. Tampilkan jumlah hewan berdasarkan spesies**

```
SELECT species, COUNT(*) AS jmlh_hewan FROM hewan GROUP BY species;
```

***Output :***

![Screenshot 2024-05-20 134835](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/e977aa33-b052-4d32-b893-088b562e1171)


**3. Tampilkan jumlah hewan berdasarkan jenis kelamin**

```
SELECT sex, COUNT(*) AS jmlh_hewan FROM hewan GROUP BY sex;
```

***Output :***

![Screenshot 2024-05-20 134900](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/190eeb6e-6bc0-4a21-a247-968ea89f6b12)


**4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin**

```
SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species, sex;
```

***Output :***

![Screenshot 2024-05-20 135017](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/e8a4917a-5364-482a-9e86-8a49a5380cb1)


**5. Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin**

```
SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE
species IN ('Cat', 'Dog')
GROUP BY species, sex;
```

***Output :***

![Screenshot 2024-05-20 135226](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/2293b1af-5f17-48d8-8fb2-3827fc53fc5e)


**6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja**

```
SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE sex IS NOT NULL GROUP BY sex;
```

***Output :***

![Screenshot 2024-05-20 135250](https://github.com/nurulaisyah14/TugasPraktikum4/assets/148174512/a151022b-f2f1-4c7f-a43a-9e655c4550a8)



## Tulis semua perintah-perintah SQL percobaan di atas beserta outputnya!

```
CREATE DATABASE praktikum4;
USE praktikum4;
CREATE TABLE pegawai (
    idpegawai VARCHAR (5) PRIMARY KEY,
    nama_depan VARCHAR (10) NOT NULL,
    nama_belakang VARCHAR (15) NOT NULL,
    email VARCHAR (25) UNIQUE KEY,
    telepon VARCHAR (15),
    tgl_kontrak DATE,
    id_job VARCHAR (5),
    gaji INT,
    tunjangan INT
    );

INSERT INTO pegawai VALUES
    ('E001', 'Ferry', 'Gustiawan', 'ferry@yahoo.com', '07117059004', '2005-09-01', 'L0001', 2000000, 500000),
	('E002', 'Aris', 'Ganiardi', 'aris@yahoo.com', '081312345678', '2006-09-01', 'L0002', 2000000, 200000),
	('E003', 'Faiz', 'Ahnad', 'faiz@gmail.com', '081367384322', '2006-10-01', 'L0003', 1500000, NULL),
	('E004', 'Emna', 'Bunton', 'emna@gmail.com', '081363484342', '2006-10-01', 'L0004', 1500000, 9),
	('E005', 'Mike', 'Scoff', 'mike@plasa.com', '08163454555', '2007-09-01', 'L0005', 1250000, 9),
	('E006', 'Lincoln', 'Burrows', 'linc@yahoo.com', '08527388432', '2008-09-01', 'L0006', 1750000, NULL);

SELECT * FROM pegawai;

SELECT * FROM pegawai WHERE gaji NOT IN (2000000, 1250000);

SELECT * FROM pegawai WHERE tunjangan IS NULL;

SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;

SELECT COUNT(*) AS jumlah_pegawai FROM pegawai;

SELECT SUM(gaji) AS total_gaji FROM pegawai;

SELECT AVG(gaji) AS rata_rata_gaji FROM pegawai;

SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;

SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;

CREATE TABLE hewan (
    id VARCHAR (5) PRIMARY KEY,
    name VARCHAR (10) NOT NULL,
    owner VARCHAR (10),
    species VARCHAR (10),
    sex enum('M', 'F')
    );

INSERT INTO hewan (id, name, owner, species, sex)
VALUES ('p1', 'Puffball', 'Diane', 'Hamster', 'F'),
       ('p2', 'Claws', 'Gwen', 'Cat', 'M'),
       ('p3', 'Fluffy', 'Haro 1d', 'Cat', 'F'),
       ('p4', 'Buffy', 'Haro 1d', 'Dog', 'F'),
       ('p5', 'Fang', 'Benny', 'Dog', 'M'),
       ('p6', 'Bowser', 'Diane', 'Dog', 'M'),
       ('p7', 'Chirpy', 'Gwen', 'Bird', 'F'),
       ('p8', 'Whistler', 'Gwen', 'Bird', NULL),
       ('p9', 'Slim', 'Benny', 'Snake', 'M');

SELECT * from hewan;

SELECT owner, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY owner;

SELECT species, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species;

SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY sex;

SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species, sex;

SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE species IN ('Cat', 'Dog') GROUP BY species, sex;

SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE sex IS NOT NULL GROUP BY sex;
```

## Berikan Kesimpulan Anda !

Terdapat beberapa ***Query Filter*** yang ditemukan pada tugas praktikum 4 :

- Operator `IN` digunakan untuk memfilter data yang terdapat pada list IN
- Operator `NOT IN` digunakan untuk memfilter data yang tidak terdapat pada list IN
- Operator `IS NULL` digunakan untuk menampilkan data dengan nilai data NULL
- Operator `IS NOT NULL` digunakan untuk menampilkan data dengan nilai data tidak NULL
- `COUNT` adalah perintah yang digunakan untuk menghitung jumlah baris suatu kolom pada tabel.
- `SUM` adalah perintah yang digunakan untuk menghitung jumlah nilai suatu kolom pada tabel.
- `AVG` adalah perintah yang digunakan untuk menghitung rata-rata dari nilai suatu kolom pada tabel.
- `MIN` adalah perintah yang digunakan untuk menampilkan nilai terkecil dari suatu kolom pada tabel.
- `MAX` adalah perintah yang digunakan untuk menampilkan nilai terbesar dari suatu kolom pada tabel.
- Klausa `GROUP BY` berfungsi untuk mengelompokkan data berdasarkan field tertentu.

## FINISH <img align="center" alt="Ikhsan-Python" height="40" width="45" src="https://em-content.zobj.net/source/microsoft-teams/337/student_1f9d1-200d-1f393.png"> <img align="center" alt="Ikhsan-Python" height="40" width="45" src="https://em-content.zobj.net/thumbs/160/twitter/348/flag-indonesia_1f1ee-1f1e9.png">kombinasi spesies dan jenis kelamin tertentu.
#### - Jumlah hewan berdasarkan jenis kelamin yang diketahui: Dengan menggunakan klausa WHERE untuk memfilter jenis kelamin yang tidak NULL (diketahui) dan klausa GROUP BY pada kolom "sex" serta fungsi COUNT, kita dapat menghitung jumlah hewan untuk jenis kelamin yang diketahui.
#### Dengan menggunakan query-query ini, kita dapat memperoleh informasi statistik tentang jumlah hewan berdasarkan kriteria yang relevan dalam basis data MySQL.
