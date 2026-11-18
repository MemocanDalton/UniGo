# Kampüs 360

Öğrenciler için kampüs uygulaması prototipi (v0.1): ders programı, öğrenci pazar yeri ve günlük özet ekranı.

## Özellikler
- Ders programı: ders ekleme, silme, gün seçme, sıradaki dersi gösterme
- Pazar yeri: ilan verme, silme, arama, kategori filtresi
- Profil: ad ve bölüm, örnek veri yükleme
- Karanlık mod desteği

## Çalıştırma
`index.html` dosyasını tarayıcıda açmanız yeterli. Kurulum gerekmez.

## Notlar
- Bu sürümde veriler yalnızca kullanıcının tarayıcısında (localStorage) saklanır, cihazlar arasında paylaşılmaz.
- Öğrenci ders ve ilan bilgilerini kendisi girer, OBS entegrasyonu yoktur.

## Yol haritası
- Ortak veritabanı (herkes aynı ilanları görsün)
- Okul e-postası ile giriş
- İlan fotoğrafı yükleme
