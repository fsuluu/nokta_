# Audit Report — Books Status Badge Readability

## Screen

BooksScreen

## Severity

Low

## Problem

Kitap listesindeki durum rozetlerinin (Rafta, Ödünçte) renkleri yeterince canlı değil ve metinler küçük kalıyor. Durumun hızlıca ayırt edilmesi zor.

## Expected Behavior

Rozetler daha belirgin renklere sahip olmalı ve font ağırlığı artırılarak okunabilirlik iyileştirilmelidir.

## Suggested Fix

- `statusBadge` için `fontWeight: "900"` kullan.
- Arka plan ve metin renklerini (`#dcfce7` / `#166534`) daha kontrastlı seç.
- Padding değerlerini optimize ederek rozet formunu belirginleştir.

## User Note

Kitapların rafta mı ödünçte mi olduğu ilk bakışta pek anlaşılmıyor, daha renkli olabilir.

## Agent Input

READ → LOCATE → HYPOTHESIZE → REPAIR → TEST → VERIFY  
Improve badge readability and status colors.

## Burn-in Screenshot

![Books](./screenshots/books_list.png)
