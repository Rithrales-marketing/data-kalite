# Ağrı Merkezi — Haftalık MR İsteme Raporu (veri)

Bu klasör, ağrı merkezi CRM "Aylık Kaynak Raporu" haftalık dışa aktarımlarından üretilen veriyi ve Meta reklam harcamalarını içerir.

## Kapsam
- Yalnızca Murat, Aycan, Cevdet ve Hasan Hoca kaynakları. Medisera, Referans ve diğer hocalar hariç.
- Haftalar Pazar–Cumartesi. CRM filtresi: Arama Yapılacak Tarih, İşlem Aşaması ≠ Yeni Kayıt, Asistan ≠ CRM Admin.

## Tanımlar
- `mr_istenen` = MR Bekleniyor ve sonraki aşamalar (MR Değerlendirildi, 2. ve 3. görüşme, randevu verildi/iptal, işlem, muayene).
- `mr_isteme_orani` = mr_istenen / toplam kayıt. MR Yok paydada kalır.

## Dosyalar
- `data/weeks/week_YYYY-MM-DD.json` — haftanın kaynak × işlem aşaması ham sayıları.
- `data/spend/YYYY-MM-DD.json` — haftanın Meta harcaması (TL, KDV hariç), hoca ve kanal kırılımında.
- `data/haftalik_kaynak_ozet.csv` — tüm haftaların kaynak bazlı özeti.

## Harcama eşleştirme kuralları
Kampanya adına göre: `F` + hoca → o hocanın Meta Form kaynağı, `WP` + hoca → WhatsApp kaynağı, `S` ile başlayan → Murat Hoca Organik Web. Ek kurallar: `CU_WP_*` → Cevdet WhatsApp, `asd` → Murat WhatsApp, `murat_hoca_fatma_coban_*` → Murat Meta Form, `MH_*` → Murat (Form/WP).
