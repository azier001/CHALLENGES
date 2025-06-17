
# 🌼 Fleeceflower Pattern Generator

Fungsi `createFleeceflowerPattern(size)` menghasilkan **pola simetris berbentuk wajik** (mirip bunga fleece) dalam bentuk string, menggunakan karakter `'1'` dan `'0'` yang disusun secara bergantian. Cocok digunakan untuk latihan logika dan manipulasi string di JavaScript.

---

## 🧠 Penjelasan Umum

### 🔢 Validasi Ukuran

Fungsi hanya menerima:
- Bilangan **ganjil**
- Minimal **3**

Jika tidak sesuai, maka akan menghasilkan error:

```javascript
throw new Error("Size must be an odd integer of at least 3");
```

---

## ⚙️ Parameter

| Parameter | Tipe     | Deskripsi                                                   |
|-----------|----------|-------------------------------------------------------------|
| `size`    | `number` | Ukuran tinggi dan lebar pola (harus ganjil, minimal 3)       |

---

## 🧩 Struktur Logika

1. **Tentukan titik tengah** dari pola (baris ke berapa adalah pusat):
   ```javascript
   const center = Math.floor(size / 2);
   ```

2. **Looping setiap baris (`i`)** sebanyak `size` kali:
   - Hitung jarak dari baris ke pusat:
     ```javascript
     const distanceFromCenter = Math.abs(i - center);
     ```
   - Tentukan jumlah karakter `'1'` dan `'0'`:
     ```javascript
     const elementsInRow = size - 2 * distanceFromCenter;
     ```
   - Tambahkan spasi di kiri:
     ```javascript
     row += " ".repeat(leadingSpaces);
     ```

3. **Tambahkan pola biner bergantian** ke setiap baris:
   ```javascript
   for (let j = 0; j < elementsInRow; j++) {
       row += (j % 2 === 0) ? "1" : "0";
   }
   ```

4. **Tambahkan baris ke dalam `pattern` dan akhiri dengan newline (kecuali baris terakhir)**.

---

## ✅ Contoh Output

```javascript
console.log(createFleeceflowerPattern(5));
```

### Output:
```
  1  
 101 
10101
 101 
  1  
```

---

## 📌 Catatan Tambahan

- Pola selalu **simetris secara vertikal dan horizontal**.
- Dapat dimodifikasi untuk karakter lain seperti `*` dan `-`.

---
