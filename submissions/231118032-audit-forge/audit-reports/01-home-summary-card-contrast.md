# Audit Report — Home Summary Card Contrast

## Screen

HomeScreen

## Severity

Low

## Problem

Dashboard üzerindeki özet kartlarının (Toplam Kitap, Ödünçte vb.) arka plan ve metin kontrastı bazı ışık koşullarında okunabilirliği düşürüyor. Kenarlıklar yeterince belirgin değil.

## Expected Behavior

Kartların arka planı ve yazı renkleri arasındaki kontrast oranı artırılmalı, kenarlıklar daha belirgin hale getirilmelidir.

## Suggested Fix

- `summaryCard` arka plan rengini `#fffaf1` olarak güncelle.
- `borderColor` değerini `#e6d6bf` yaparak derinlik kat.
- Değer metni (`summaryValue`) için `#2f241d` gibi koyu bir ton kullan.

## User Note

Summary kartları biraz soluk görünüyor, daha premium bir hava katılabilir.

## Agent Input

READ → LOCATE → HYPOTHESIZE → REPAIR → TEST → VERIFY  
Fix only the summary card contrast issue.  
Do not change the grid layout.

## Burn-in Screenshot

![Home](./screenshots/home_summary.png)
