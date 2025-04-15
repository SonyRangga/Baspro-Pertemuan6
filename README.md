# 📘 Perkalian Matriks 5x5 di Python

Program ini melakukan **perkalian dua matriks 5x5** dengan cara manual menggunakan Bahasa Pemrograman Python , tanpa menggunakan library eksternal `Numpy`

---

## 1. Pendefinisian Matriks A & B

```
A = [
    [1, 2, 3, 4, 5],
    [6, 7, 8, 9, 10],
    [11, 12, 13, 14, 15],
    [16, 17, 18, 19, 20],
    [21, 22, 23, 24, 25]
]

B = [
    [1, 0, 1, 0, 1],
    [0, 1, 0, 1, 0],
    [0, 0, 1, 0, 0],
    [0, 1, 0, 1, 0],
    [1, 0, 1, 0, 1]
]

```
- `A` adalah matriks 5x5 yang berisi angka dari 1 hingga 25
- `B` adalah matriks 5x5 yang isinya pola 1 dan 0


---

## 2. Menyiapkan Matriks Hasil

```python
hasil = []
```
- `hasil` akan menampung hasil dari perkalian matriks `A` dan `B`.

---

## 3. Perhitungan Kali Dalam Matriks

```python
for i in range(5):
    baris = []
    for j in range(5):
        total = 0
        for k in range(5):
            total += A[i][k] * B[k][j]
        baris.append(total)
    hasil.append(baris)
```

### Penjelasan:
- Perulangan `i` dan `j` menelusuri setiap posisi baris dan kolom pada matriks hasil
- Perulangan `k` menjumlahkan hasil kalo antara elemen baris ke-i dari A dan kolom ke-j dari B
- Nilai total dimasukan ke baris hasil, lalu disimpan ke dalam matriks `hasil`

---

## 4. Menampilkan Hasil

```python
print("Hasil perkalian matriks A x B:")
for row in hasil:
    print(row)
```

### Penjelasan:

- Menampilkan hasil akhir dari perkalian matriks `A x B` dalam bentuk matriks 2D

---

## ✅ Contoh Perhitungan (Posisi `[0][0]`):

```
A[0] = [1, 2, 3, 4, 5]
B kolom 0 = [1, 0, 0, 0, 1] -> ambil dari B[0][0], B[1][0], ..., B[4][0]

total = (1×1) + (2×0) + (3×0) + (4×0) + (5×1)
      = 1 + 0 + 0 + 0 + 5 = 6
```

---

## 📊 Matriks Hasil

Hasil dari `A x B` adalah:

```
[6,  6,  9,  6,  6]
[16, 16, 24, 16, 16]
[26, 26, 39, 26, 26]
[36, 36, 54, 36, 36]
[46, 46, 69, 46, 46]
```

---

## 🔍 Ringkasan

- Tidak menggunakan library eksternal seperti `numpy`.
- Melakukan perkalian `matriks A x B` dengan algoritma manual (3 kali nested loop)..
- Cocok untuk pembelajaran dasar matriks dan algoritma perkalian manual.
- Menyimpan hasil ke dalam matriks baru dan mencetak hasilnya ke layar.
