# 📊 Data Preprocessing - Online Retail Dataset

## 📌 Deskripsi
Proyek ini bertujuan untuk melakukan **data preprocessing** pada dataset *Online Retail*. Dataset ini berisi data transaksi penjualan dari sebuah perusahaan ritel online.

---

## 📁 Dataset
Dataset yang digunakan:
- Online Retail Dataset

Berisi informasi seperti:
- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

---

## ⚙️ Tahapan Preprocessing

### 1. Data Understanding
- Menampilkan data awal menggunakan `head()` dan `tail()`
- Melihat struktur data dengan `info()`
- Mengecek missing value dengan `isnull()`

---

### 2. Handling Missing Value
Ditemukan:
- 1454 missing pada **Description**
- 135080 missing pada **CustomerID**

Penanganan:
- Description → diisi dengan modus
- CustomerID → diisi dengan "Unknown"

---

### 3. Data Cleaning
Dilakukan filtering:
- Menghapus nilai negatif pada Quantity
- Menghapus nilai negatif pada UnitPrice

```python
df = df[(df['Quantity'] > 0) & (df['UnitPrice'] > 0)]
