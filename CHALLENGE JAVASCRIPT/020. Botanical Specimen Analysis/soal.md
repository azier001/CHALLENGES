# 🌿 Dokumentasi Fungsi Analisis Spesimen Botani

## 📌 Deskripsi Tantangan

**Tingkat Kesulitan:** Mudah

Buatlah fungsi bernama `analyzePlantSpecimen` yang menganalisis spesimen tanaman dan mengembalikan string terformat yang berisi berbagai informasi tentang tanaman tersebut.

---

## 🔧 Deklarasi Fungsi

```javascript
function analyzePlantSpecimen(plantName, numberOfLeaves, plantHeight)
```

---

## 🧾 Parameter

| Parameter      | Tipe   | Deskripsi                        |
| -------------- | ------ | -------------------------------- |
| plantName      | String | Nama dari spesimen tanaman.      |
| numberOfLeaves | Number | Jumlah daun pada tanaman.        |
| plantHeight    | Number | Tinggi tanaman dalam sentimeter. |

---

## 🔬 Aturan Analisis

1. **Luas Daun (cm²):**

   * Setiap daun berbentuk persegi panjang dengan lebar `1.5 cm`.
   * Rumus: `luasSatuDaun = tinggiTanaman * 1.5`
   * Total luas daun: `totalLuasDaun = luasSatuDaun * jumlahDaun`

2. **Konversi Tinggi:**

   * Konversi tinggi tanaman dari cm ke inci: `tinggiInci = tinggiTanaman / 2.54`
   * Dibulatkan ke satu angka di belakang koma.

3. **Klasifikasi Tinggi Tanaman:**

   * "pendek" jika `< 30 cm`
   * "sedang" jika `30–100 cm`
   * "tinggi" jika `> 100 cm`

4. **Kode Warna:**

   * Gunakan huruf pertama dari `plantName`, diulang 3 kali.
   * Contoh: `"Fern"` → `"FFF"`

---



## 💡 Contoh Penggunaan

```javascript
console.log(analyzePlantSpecimen("Fern", 10, 45));
```

### ✅ Output

```
Tanaman: Fern
Jumlah Daun: 10
Tinggi: 45 cm (17.7 in)
Kategori: sedang
Total Luas Daun: 675.00 cm²
Kode Warna: FFF
```

---

## 🧪 Contoh Tambahan

```javascript
console.log(analyzePlantSpecimen("Bamboo", 20, 150));
```

```
Tanaman: Bamboo
Jumlah Daun: 20
Tinggi: 150 cm (59.1 in)
Kategori: tinggi
Total Luas Daun: 4500.00 cm²
Kode Warna: BBB
```

```javascript
console.log(analyzePlantSpecimen("Moss", 5, 12));
```

```
Tanaman: Moss
Jumlah Daun: 5
Tinggi: 12 cm (4.7 in)
Kategori: pendek
Total Luas Daun: 90.00 cm²
Kode Warna: MMM
```

---

## 📎 Catatan

* Fungsi ini sangat cocok untuk melatih operasi matematika dasar, format string, dan logika kondisi di JavaScript.
* Menampilkan hasil dengan struktur yang rapi dan mudah dibaca.

---

Selamat menganalisis spesimen botani! 🌱
