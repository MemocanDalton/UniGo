# Mühendislik Kanıtları

## Mimari Genel Bakış
Uygulama `UniGo Mvp.html` içinde HTML/CSS/JavaScript yapısıyla çalışır ve arka uç için Supabase Auth, REST API (`unigo_listings`, `unigo_profiles`, `unigo_reviews`, `unigo_reports`), RPC (`unigo_view`, `unigo_ask`) ve Storage (`ilan-foto`) uçlarını kullanır.

## Öne Çıkan Teknik Kararlar
- **Oturum Yönetimi:** Süresi yaklaşan veya 401 dönen isteklerde yenileme akışı (`refreshSession`) ve oturum sonlandırma kontrolü eklendi.

- **Görsel Optimizasyonu:** Yüklenen görseller `kucult` fonksiyonu ile en fazla 900px ölçeklenip JPEG olarak sıkıştırılır, ardından `uploadPhotos` ile yüklenir.

- **Eşleşme Önerisi:** İlan yayınlandığında zıt türdeki (`Satılık` / `Aranıyor`) benzer ilanlarla kök bazlı eşleşme kontrolü (`eslesen`) yapılır.
