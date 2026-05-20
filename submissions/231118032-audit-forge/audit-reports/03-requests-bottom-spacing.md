# Audit Report — Requests Bottom Spacing

## Screen

RequestsScreen

## Severity

Medium

## Problem

İstekler listesinde en alttaki kartlar, yüzen (floating) tab bar'ın arkasında kalıyor. Listeyi sona kadar kaydırsak bile son eleman tam görünmüyor.

## Expected Behavior

Sayfanın alt kısmında tab bar yüksekliği kadar boşluk (safe area / padding) bırakılmalıdır.

## Suggested Fix

- `page` stilindeki `paddingBottom` değerini `110` olarak güncelle.
- Listenin tab bar üzerine çıkmadığından emin ol.

## User Note

En alttaki istekleri okuyamıyorum, parmağımla yukarı çeksem bile tab bar kapatıyor.

## Agent Input

READ → LOCATE → HYPOTHESIZE → REPAIR → TEST → VERIFY  
Increase bottom padding for scroll content.

## Burn-in Screenshot

![Requests](./screenshots/requests_list.png)
