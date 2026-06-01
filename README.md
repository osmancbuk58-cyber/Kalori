# Kalori · Cep

Pediatrik günlük kalori ve makro besin ihtiyacı hesaplayıcı. Tek HTML dosyası, vanilla JS, offline çalışır. PWA olarak telefon ana ekranına eklenebilir.

## Kapsam

**Yenidoğan dahil değil** — sadece infant, çocuk ve adolesan için.

## Bölümler

### 1. Bazal Kalori (3 yöntem yan yana)
- **Holliday-Segar**: 100/50/20 kuralı (≤10 kg → 100 kcal/kg, 11-20 kg → 1000 + 50/kg, >20 kg → 1500 + 20/kg)
- **Yaşa göre tablo**: Cinsiyete göre, 2-18 yaş (Hacettepe defteri kaynağı)
- **Schofield BMR (1985)**: Bazal metabolik hız, kilo bazlı sadeleştirilmiş formül

### 2. Düzeltilmiş Kalori
BMR × Aktivite × Stres faktörü
- **Aktivite**: yatağa bağlı (1.2) / hafif (1.3) / normal (1.5) / yüksek (1.7)
- **Stres**: yok (1.0) / hafif (1.2) / orta (1.4) / ağır (1.7)

### 3. Yakalama Büyümesi (Catch-up)
İdeal kilo girilince:
- Mevcut/ideal oran ve malnütrisyon derecesi (Waterlow)
- Catch-up kcal/kg ve toplam kalori
- Formül: (RDA × ideal kilo) / mevcut kilo

### 4. Makro Besin Dağılımı
Düzeltilmiş kaloriden hesaplanan:
- **Protein** (yaşa göre g/kg/gün, WHO/IOM)
- **Yağ** (yaşa göre % toplam kalori)
- **Karbonhidrat** (kalan)

## Klinik notlar

- Schofield BMR yatan/hasta için, aktivite ve stres faktörü ile çarpılarak kullanılır
- Sepsis %30-50 artış, ağır yanık %50-100, ARDS/multipl travma %50-80
- Protein ihtiyacı stres altında artar: hafif hastalık 1.5-2 g/kg, YBÜ/sepsis 2-3, yanık 3+ g/kg
- Catch-up hesabı: refeeding sendromu riski — yavaş başla, P/K/Mg/tiamin takip
- 2 yaş altı için yaşa göre tablo yok, Holliday-Segar kullan

## Tasarım

- Tek HTML dosyası, build sistemi yok
- Vanilla JS (framework yok)
- Koyu mod, accent yeşil tema (Antropometri-Cep ile uyumlu)
- JetBrains Mono + IBM Plex Sans
- Mobile-first, PWA destekli

## Dosyalar

- `index.html` — uygulamanın tamamı
- `manifest.json` — PWA manifest
- `README.md` — bu dosya

## Deploy

GitHub web arayüzü → New repo (public) → uploading existing file → 3 dosyayı sürükle bırak → Commit → Settings → Pages → main / root → Save.

1-2 dakika sonra `https://<kullanici>.github.io/kalori-cep/` aktif.

## Sorumluluk reddi

Bu araç bir klinik karar destek aracıdır. Tüm sayısal çıktılar pediatri hekimi tarafından klinik bağlamla değerlendirilmelidir.

---

**Kalori · Cep · v0.1 · Pediatri**
