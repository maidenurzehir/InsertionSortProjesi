# Insertion Sort Projesi (Proje 1)

## 1) Insertion Sort adımları
Başlangıç: **[22, 27, 16, 2, 18, 6]**

- i=1, key=27 → yerinde  
  **[22, 27, 16, 2, 18, 6]**
- i=2, key=16 → 27 ve 22 sağa kayar  
  **[16, 22, 27, 2, 18, 6]**
- i=3, key=2 → 27, 22, 16 sağa kayar  
  **[2, 16, 22, 27, 18, 6]**
- i=4, key=18 → 27 ve 22 sağa kayar  
  **[2, 16, 18, 22, 27, 6]**
- i=5, key=6 → 27, 22, 18, 16 sağa kayar  
  **[2, 6, 16, 18, 22, 27]** ✅

## 2) Big-O
- Ortalama / En kötü: **O(n²)**
- En iyi (dizi zaten sıralı): **O(n)**
- Ek bellek: **O(1)**

## 3) Time Complexity – 18 sayısı hangi case?
Sıralı dizide **[2, 6, 16, 18, 22, 27]** ortalarda → **Average case**.

---

## 4) Selection Sort – ilk 4 adım
Başlangıç: **[7, 3, 5, 8, 2, 9, 4, 15, 6]**

1. min=2 → 0. elemanla yer değiştir  
   **[2, 3, 5, 8, 7, 9, 4, 15, 6]**
2. Kalan kısım min=3 → yerinde  
   **[2, 3, 5, 8, 7, 9, 4, 15, 6]**
3. Kalan kısım min=4 → 2. indeksle değiştir  
   **[2, 3, 4, 8, 7, 9, 5, 15, 6]**
4. Kalan kısım min=5 → 3. indeksle değiştir  
   **[2, 3, 4, 5, 7, 9, 8, 15, 6]**

   # Merge Sort Projesi (Proje 2)

## 1) Merge Sort Aşamaları
Dizi: **[16, 21, 11, 8, 12, 22]**

### Adım 1 – Böl (Divide)
- Sol yarı: [16, 21, 11]
- Sağ yarı: [8, 12, 22]

Sol tarafı böl:
- [16, 21, 11] → [16] ve [21, 11]
- [21, 11] → [21] ve [11]

Sağ tarafı böl:
- [8, 12, 22] → [8] ve [12, 22]
- [12, 22] → [12] ve [22]

---

### Adım 2 – Birleştir (Conquer / Merge)
- [21] + [11] → [11, 21]
- [16] + [11, 21] → [11, 16, 21]
- [12] + [22] → [12, 22]
- [8] + [12, 22] → [8, 12, 22]

---

### Adım 3 – Son Birleştirme
[11, 16, 21] + [8, 12, 22]  
Karşılaştırılarak:
- 8, 11, 12, 16, 21, 22

**Sonuç:** **[8, 11, 12, 16, 21, 22]**

---

## 2) Big-O Gösterimi
- Ortalama durum (Average case): **O(n log n)**
- En kötü durum (Worst case): **O(n log n)**
- En iyi durum (Best case): **O(n log n)**  
  (T(n) = 2T(n/2) + O(n))
- Ek bellek kullanımı: **O(n)**

---

**Özet:** Merge Sort diziyi sürekli ikiye bölerek küçük parçalarda sıralar ve yeniden birleştirir. Bu yüzden işlem sayısı logaritmik çarpanla artar.

# Binary Search Tree Projesi (Proje 3)

Dizi: **[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]**

## BST Ekleme Aşamaları (insert)
1. **root 7’dir.**
2. **5** eklenir → 5 < 7 ⇒ **7’nin solunda 5**.
3. **1** eklenir → 1 < 7 ⇒ sola (5); 1 < 5 ⇒ **5’in solunda 1**.
4. **8** eklenir → 8 > 7 ⇒ **7’nin sağında 8**.
5. **3** eklenir → 3 < 7 ⇒ sola (5); 3 < 5 ⇒ sola (1); 3 > 1 ⇒ **1’in sağında 3**.
6. **6** eklenir → 6 < 7 ⇒ sola (5); 6 > 5 ⇒ **5’in sağında 6**.
7. **0** eklenir → 0 < 7 ⇒ sola (5); 0 < 5 ⇒ sola (1); 0 < 1 ⇒ **1’in solunda 0**.
8. **9** eklenir → 9 > 7 ⇒ sağa (8); 9 > 8 ⇒ **8’in sağında 9**.
9. **4** eklenir → 4 < 7 ⇒ sola (5); 4 < 5 ⇒ sola (1); 4 > 1 ⇒ sağa (3); 4 > 3 ⇒ **3’ün sağında 4**.
10. **2** eklenir → 2 < 7 ⇒ sola (5); 2 < 5 ⇒ sola (1); 2 > 1 ⇒ sağa (3); 2 < 3 ⇒ **3’ün solunda 2**.

## Doğrulama (In-order dolaşım)
Sol-Kök-Sağ: **[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]**  → artan sıralı.

## Big-O (bilgi amaçlı)
- Ortalama/good case arama/ekleme/silme: **O(log n)**
- En kötü (ağaç hatalı dengelenmişse): **O(n)**
