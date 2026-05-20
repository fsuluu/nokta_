# Audit Report — Search Feature Experiment (Rollback)

## Screen

BooksScreen / RequestsScreen

## Severity

Low (Feature Request)

## Problem

Kullanıcılar kitaplar arasında arama yapabilmek için üst kısma bir arama çubuğu eklenmesini istiyor.

## Expected Behavior

Ekranın üst kısmına bir `TextInput` alanı eklenerek liste filtrelenebilir olmalı.

## Suggested Fix

- `BooksScreen` içine arama state'i ve filtreleme mantığı ekle.
- UI'a bir search icon ve input field yerleştir.

## User Note

Kitap sayısı arttığında aradığımı bulmak zorlaşıyor.

## Agent Input

READ → LOCATE → HYPOTHESIZE → REPAIR → TEST → VERIFY  
Try adding search field. Rollback if it breaks clean UI philosophy (Track A).

## Burn-in Screenshot

![Search](./screenshots/search_failed.png)
