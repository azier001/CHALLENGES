
# 🌸 Dokumentasi Fungsi `createFleeceflowerPattern(size)`

Fungsi `createFleeceflowerPattern` digunakan untuk membuat pola berbentuk bunga fleeceflower dengan karakter `1` dan `0` secara simetris. Cocok digunakan untuk latihan logika, manipulasi string, atau tampilan pola pada console.

---

## 🧠 Deskripsi Fungsi

Fungsi ini menghasilkan pola berbentuk berlian simetris yang terdiri dari angka `1` dan `0` secara bergantian. Pola akan selalu simetris horizontal dan vertikal jika input berupa bilangan ganjil ≥ 3.

---

## 📥 Parameter

| Nama Parameter | Tipe    | Deskripsi                                          |
|----------------|---------|----------------------------------------------------|
| `size`         | Integer | Ukuran tinggi dan lebar pola (harus ganjil ≥ 3)   |

---

## ⚠️ Validasi

Jika `size < 3` atau merupakan bilangan genap, maka fungsi akan mengembalikan:

```text
"Invalid input"
```

---

## 📐 Karakter Pola

| Karakter | Arti                                |
|----------|--------------------------------------|
| `1`      | Posisi genap (mulai dari 0) dalam pola |
| `0`      | Posisi ganjil dalam pola             |
| ` ` (spasi) | Padding untuk membuat simetri         |

---

## 💡 Contoh Penggunaan

```javascript
console.log(createFleeceflowerPattern(5));
```

### 💬 Output

```
  101  
 10101 
1010101
 10101 
  101  
```

---

## 🧮 Penjelasan Logika

- Pola berbentuk simetris berdasarkan nilai tengah `mid = Math.floor(size / 2)`
- Setiap baris dihitung dari jarak ke tengah (`Math.abs(mid - i)`)
- Setiap baris diisi dengan angka `1` dan `0` bergantian, dimulai dari `1`
- Spasi ditambahkan di kiri dan kanan agar pola tetap simetris

---

## 🧪 Contoh Lain

```javascript
createFleeceflowerPattern(7)
```

**Output:**
```
   101   
  10101  
 1010101 
101010101
 1010101 
  10101  
   101   
```

---

## 📝 Catatan

- Fungsi ini hanya valid untuk bilangan ganjil ≥ 3
- Cocok digunakan untuk latihan nested loop dan manipulasi string
