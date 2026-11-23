# Test Senaryoları

| ID | Senaryo Adı | Ön Koşul | Adımlar | Beklenen Sonuç |
|---|---|---|---|---|
| TC-01 | `.edu.tr` Validasyonu | Kayıt/Giriş modalı açık | `.edu.tr` olmayan adres girilip gönderilir | Uyarı mesajı gösterilir, kayıt engellenir |

| TC-02 | İlan Oluşturma | Doğrulanmış kullanıcı giriş yapmış | Tür, kategori, başlık, fiyat ve iletişim girilip yayınlanır | İlan listeye eklenir ve kalıcı olarak kaydedilir |

| TC-03 | Filtreleme ve Sıralama | Vitrinde ilanlar mevcut | Kategori, etiket veya sıralama seçilir | Liste seçilen kritere göre güncellenir |

| TC-04 | İlan Detay ve Soru-Cevap | İlan kartına tıklanır | Detay modalı açılır ve soru gönderilir | Soru ilana eklenir ve listede görünür |

| TC-05 | Favori ve Durum Yönetimi | Kullanıcı giriş yapmış | İlan favoriye alınır; kendi ilanında durum değiştirilir | Favori ve durum bilgisi güncellenir |

| TC-06 | Şikayet ve Değerlendirme | İlan detay modalı açık | Puan/yorum veya şikayet formu doldurulup gönderilir | Kayıt işlemi tamamlanır ve geri bildirim verilir |
