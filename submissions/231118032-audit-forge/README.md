Track: A

# Audit Forge Submission

Öğrenci No: 231118032  
Slug: audit-forge

## Proje Özeti

Bu proje, Nokta Audit Forge ödevi kapsamında hazırlanmış minimal bir Expo + TypeScript mobil uygulamasıdır. Uygulamada üç temel ekran bulunmaktadır: başlangıç ekranı, fikir kartları listesi ve fikir detay ekranı.

Audit widget uygulamaya drop-in olarak eklenecek şekilde tasarlanmıştır. Kullanıcı, uygulama ekranında gördüğü hataları veya geliştirme noktalarını işaretleyerek Markdown formatında audit raporu oluşturur. Daha sonra bu raporlar coding agent tarafından okunur ve forge döngüsü ile düzeltmeler yapılır.

## Ekranlar

- Onboarding Screen
- Idea List Screen
- Idea Detail Screen

## Audit Reports

Audit raporları `audit-reports/` klasörü altında tutulmuştur.

## Forge Süreci

Forge süreci `FORGE.md` dosyasında READ → LOCATE → HYPOTHESIZE → REPAIR → TEST → VERIFY → COMMIT/ROLLBACK adımlarıyla kayıt altına alınmıştır.

## Demo Video

Demo video linki: Eklenecek

## Expo QR / Link

Expo linki: Eklenecek

## Decision Log

- Minimal Expo + TypeScript uygulaması oluşturuldu.
- Üç ekranlı sade bir uygulama yapısı kuruldu.
- Audit raporları için ayrı `audit-reports/` klasörü oluşturuldu.
- Forge döngülerini takip etmek için `FORGE.md` dosyası hazırlandı.
- Track A seçilerek sadelik ve drop-in disiplinine odaklanıldı.

## AI Tool Log

- ChatGPT: Proje yapısı, README, FORGE ve audit raporu şablonları için kullanıldı.
- Coding Agent: Audit raporlarına göre düzeltme döngülerinde kullanılacaktır.

## Audit Widget Integration Note

AuditWidget, host uygulama kök bileşeninde tek noktadan mount edilmiştir. Widget entegrasyonu `App.tsx` içinde yalnızca `<AuditWidget deps={deps} />` satırıyla yapılmıştır. Paket sürümünde `currentScreen` prop’u TypeScript tarafından desteklenmediği için aktif ekran bilgisi uygulama state’i üzerinden yönetilmiş, widget host uygulamaya yayılmadan izole tutulmuştur.

Widget kaldırıldığında uygulama ekranları ve navigasyon çalışmaya devam eder.
