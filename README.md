# Basis-data-praktikum-5

```
Latihan
1 Lakukan join table Mahasiswa dan Dosen
2 Lakukan join tabel Matakuliah dan Dosen
3 Lakukan join table JadwalMengajar, Dosen, dan Matakuluan
4 Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen
```
### Tabel Mahasiswa
![gambar 1 Table](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/b79d1080-bc67-4db6-a84a-6c1480f31482)

### Tabel Dosen
![gambar 2 Table](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/5b181d92-e5d4-4df6-b908-58f9c7ce0e02)

### Tabel KrsMahasiswa
![gambar 3 table](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/bd9b3ade-e271-49cb-8533-552b9a967860)

### Tabel JadwalMengajar
![gambar 4 Table](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/69d3304c-ec46-492c-8bb6-763e7fc69473)

### Tabel Matakuliah
![GAmbar 5 TAble](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/0fcfe233-c8bb-46cf-9206-288e49a93b1a)

# LATIHAN

1 Lakukan join table Mahasiswa dan Dosen
![Latihan 1](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/0de02f81-b16c-41f0-928b-e568bb068484)

2 Lakukan join tabel Matakuliah dan Dosen
![Latihan 2](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/04b0dba6-9da0-42a1-80b6-36d672cd50d5)

```
Pada kode ini hasilnya tabel dosen null karena kedua tabel tidak saling ber relasi
```

3 Lakukan join table JadwalMengajar, Dosen, dan Matakuluan
![Latihan 3](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/362e3845-6509-44bd-9031-b9d1c60463d7)

4 Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen
![Latihan 4](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/bbefbd3e-a1bf-4d22-89fc-4f8efcdc715b)

# LATIHAN

1. JOIN table Mahasiswa dan Dosen
```
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jenis_kelamin, Dosen.nama AS 'Dosen' 
FROM Mahasiswa 
JOIN Dosen ON Dosen.kd_ds=Mahasiswa.kd_ds;
```
![Latihan ke 2 no 1](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/ade3d970-17e1-4ae9-82ba-b867b614de62)

2. LEFT JOIN table Mahasiswa dan Dosen
```
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jenis_kelamin, Dosen.nama AS 'Dosen'
FROM Mahasiswa
LEFT JOIN Dosen ON Dosen.kd_ds=Mahasiswa.kd_ds;
```
![Latihan ke 2 no 2](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/38ce2ded-0505-4924-b8a5-737fcd292ea1)

3. JOIN table JadwalMengajar, Dosen, dan Matakuliah
```
SELECT jadwalMengajar.kd_mk, matakuliah.nama AS 'Mata kuliah', matakuliah.sks, Dosen.nama AS 'Dosen Pengampu'
FROM jadwalMengajar
JOIN Dosen ON jadwalMengajar.kd_ds = Dosen.kd_ds
JOIN matakuliah ON jadwalMengajar.kd_mk = matakuliah.kd_mk;
```
![Latihan ke 2 no 3](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/07e30996-e865-43ec-8f06-299623fb197b)

4. JOIN table JadwalMengajar, Dosen, dan Matakuliah
```
SELECT jadwalMengajar.kd_mk, matakuliah.nama AS 'Mata kuliah', matakuliah.sks, Dosen.nama AS 'Dosen Pengampu', jadwalMengajar.hari, jadwalMengajar.jam, jadwalMengajar.ruang
FROM jadwalMengajar
JOIN Dosen ON jadwalMengajar.kd_ds = Dosen.kd_ds
JOIN matakuliah ON jadwalMengajar.kd_mk = matakuliah.kd_mk;
```
![Latihan ke 2 no 4](https://github.com/Akramfarrasanto/Praktikum-5-Basis-Data/assets/115552876/5796e2dd-b6cb-4dd3-9b74-35c3523ae0d7)
