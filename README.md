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
