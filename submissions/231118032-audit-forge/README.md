# 🏺 Audit Forge: Mini Library

[![Track](https://img.shields.io/badge/Track-A-blue.svg?style=for-the-badge)](https://github.com/nokta-impact/audit-forge)
[![Mobile](https://img.shields.io/badge/Stack-Expo%20|%20TypeScript-purple.svg?style=for-the-badge)](https://expo.dev)

Nokta Audit-Forge Mission için hazırlanan bu proje, kapalı bir **audit/forge** döngüsünü (Screenshot → Audit → Fix → Review) minimalist bir "Mini Library" uygulaması üzerinden gösterir.

---

## 🎥 Demo
> [!TIP]
> **Demo Video (≤60 sn):** [Video linkini buraya koy]

**📦 APK Path:** `submissions/231118032-audit-forge/app-release.apk`

---

## 🚀 Yerel Çalıştırma

```bash
cd submissions/231118032-audit-forge/app
npm install
npx expo start
```

---

## 📋 Proje Özeti
Bu submission, basit bir **Mini Library** uygulaması ile `@xtatistix/mobile-audit` widget’ının birlikte çalışmasını göstermektedir.

**Audit Loop Akışı:**
1. 🪲 Kullanıcı bir problemi fark eder.
2. 📱 **AuditWidget FAB** ile ekranı yakalar ve bölgeyi işaretler.
3. 📝 Markdown formatında audit raporu üretir.
4. 🤖 Rapor coding agent'a (Antigravity/Gemini) girdi olarak verilir.
5. 🛠️ **READ → LOCATE → HYPOTHESIZE → REPAIR → TEST → VERIFY** süreci işletilir.
6. 📦 Küçük bir fix diff'i commitlenir.

---

## 🎯 Track A Gerekçesi
Bu proje **Track A (Sadelik)** prensipleriyle geliştirilmiştir. Temel amaç büyük bir ürün değil, kusursuz bir "drop-in primitive" entegrasyonu göstermektir.

- **Minimal Entegrasyon:** `AuditWidget` yalnızca `App.tsx` kökünde tek noktada mount edilmiştir.
- **Sıfır Sızıntı:** Widget kaldırıldığında host uygulama hiçbir değişiklik yapmaya gerek kalmadan çalışmaya devam eder.
- **Native Boundary:** Tüm native bağımlılıklar (ViewShot, FileSystem vb.) host uygulama tarafından `deps` üzerinden enjekte edilir.

---

## 📂 Audit Raporları
`audit-reports/` klasöründe yer alan raporlar:

| Rapor | Açıklama | Sonuç |
| :--- | :--- | :---: |
| `01-home-summary-card-contrast.md` | Dashboard kart kontrast problemi | ✅ Fixed |
| `02-books-status-badge-readability.md` | Kitap durum rozeti okunabilirliği | ✅ Fixed |
| `03-requests-bottom-spacing.md` | Alt menü çakışma problemi | ✅ Fixed |
| `04-search-feature-rollback.md` | Başarısız feature denemesi | ⏪ Rollback |

---

## 🛠️ Forge Cycle Özeti
Detaylı süreçler için [FORGE.md](./FORGE.md) dosyasını inceleyebilirsiniz.

| Cycle | Ekran | Konu | Durum |
| :--- | :--- | :--- | :---: |
| 1 | Home | Kart Kontrastı | ✅ Success |
| 2 | Books | Badge Readability | ✅ Success |
| 3 | Requests | Bottom Spacing | ✅ Success |
| 4 | Global | Search Feature | ⏪ Rollback |

---

## 📝 Decision Log
| Tarih | Karar | Gerekçe |
| :--- | :--- | :--- |
| 2026-05-20 | Mini Library Teması | Gerçek state içeren sade bir demo için. |
| 2026-05-20 | Track A Seçimi | Drop-in primitive disiplinine odaklanmak için. |
| 2026-05-20 | Memory Storage | Audit notlarını session bazlı tutmak için hızlı çözüm. |
| 2026-05-20 | Search Rollback | Minimalist UI felsefesini korumak için. |

---

## 👥 Human Touch Points (HTP)
Toplam müdahale sayısı: **4**
- **Cycle 1:** Kart renklerinin HEX kodları manuel optimize edildi.
- **Cycle 2:** Rozet yazı kalınlığı manuel denendi.
- **Cycle 3:** Tab bar yüksekliğine göre padding değeri elle set edildi.
- **Cycle 4:** Rollback kararı manuel stratejik değerlendirme ile verildi.

---

## 🤖 AI Tool Log
| Aşama | Tool | Açıklama |
| :--- | :--- | :--- |
| App Foundation | Antigravity | Expo base ve UI mockup. |
| Widget Bridge | Antigravity | Native deps (FileSystem/Sharing) entegrasyonu. |
| Forge Loops | Gemini | Raporların analizi ve onarım diff üretimi. |
| Documentation | ChatGPT | README ve FORGE yapısı. |

---

## 🛠️ Teknolojiler
- **Runtime:** React Native / Expo SDK 52+
- **Logic:** TypeScript
- **Styling:** Vanilla StyleSheet
- **Audit Tool:** `@xtatistix/mobile-audit`
- **Native Bridges:** `react-native-view-shot`, `expo-file-system`, `expo-sharing`

---

> [!IMPORTANT]
> **Self-Check:**
> - [x] README ilk satırında Track bilgisi var.
> - [x] `AuditWidget` tek noktada mount edildi.
> - [x] 3+ Audit raporu ve `FORGE.md` tam.
> - [x] Root dizine/submission dışına dokunulmadı.