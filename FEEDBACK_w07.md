# FEEDBACK_w07 — UniGo Engineering Recovery & MVP Verification Plan

**Ders:** Yazılım Geliştirme Süreçleri  
**Proje:** UniGo — Campus Student Application  
**Hafta:** 07  
**Konu:** Engineering Documentation, MVP Verification, Testing & Traceability

## 1. Genel Değerlendirme

Sevgili UniGo Ekibi,

GitHub üzerinden paylaştığınız UniGo projesi incelenmiştir.

Öncelikle kampüs yaşamını kolaylaştırmayı amaçlayan, ders programı ve öğrenci pazar yeri işlevlerini içeren bir MVP prototipi hazırlamış olmanız olumlu bir başlangıçtır.

Bununla birlikte, Yazılım Geliştirme Süreçleri dersinde değerlendirdiğimiz temel unsur yalnızca çalışan bir uygulama değildir. Uygulamanın hangi problemi çözmek üzere geliştirildiği, hangi gereksinimlere dayandığı, geliştirme sürecinde hangi kararların alındığı ve yazılımın nasıl doğrulandığı da gösterilmelidir.

**Working Prototype ≠ Verified Software Product**

Mevcut repository'de bu mühendislik süreçlerinin önemli bir bölümünü henüz göremiyoruz.

Amacımız projenizi yeniden başlatmak değil; yaptığınız çalışmayı disiplinli, test edilebilir ve izlenebilir bir yazılım geliştirme sürecine dönüştürmenizi sağlamaktır.

## 2. Öncelikli Eksiklikler

İncelenen repository'de şu alanların tamamlanması gerekiyor:

1. Problem Statement ve problem kapsamı.
2. Paydaşlar ve kullanıcı ihtiyaçları.
3. Geliştirme süreci seçimi ve gerekçesi.
4. User Stories ve ölçülebilir Acceptance Criteria.
5. MVP kapsamı ve kapsam dışı özellikler.
6. GitHub Issues ve görev takibi.
7. Test senaryoları ve gerçek test sonuçları.
8. Bug Tracking ve Regression Testing.
9. AI Usage, Human Oversight ve Engineering Evidence.
10. Pull Request, Code Review ve gereksinim izlenebilirliği.

Bu eksikler mevcut çalışmalarınızı geçersiz kılmaz; ancak mühendislik yeterliliğinizi kanıtlamanızı sınırlar.

## 3. PHASE 1 — Problem Definition & Scope

`docs/problem-statement-v1.md` dosyasını oluşturun.

Şu soruları yanıtlayın:

- UniGo tam olarak hangi kampüs problemini çözmektedir?
- Hedef kullanıcılar kimlerdir?
- Ders programı ve pazar yeri işlevleri hangi ihtiyaçlara karşılık gelmektedir?
- Problemin gerçek olduğuna ilişkin hangi gözlem veya kullanıcı geri bildirimi bulunmaktadır?
- Hangi varsayımlar henüz doğrulanmamıştır?

Gerçek saha görüşmesi yapılmadıysa yapılmış gibi belgelemeyin.

**MVP Scope:** İlk aşamada mevcut ders programı ve öğrenci pazar yeri işlevlerine odaklanın.

OBS entegrasyonu, AGNO hesaplama, gerçek kullanıcı kimlik doğrulaması ve merkezi pazar yeri veritabanını gelecek sürüm kapsamına alın.

## 4. PHASE 2 — Development Process

`docs/software-development-process.md` hazırlayın.

Waterfall, Scrum, Kanban ve Iterative Development alternatiflerini karşılaştırın.

Küçük öğrenci takımı ve mevcut MVP koşullarına uygun yaklaşımı gerekçesiyle seçin.

GitHub üzerinde şu iş akışını uygulayın:

Backlog → To Do → In Progress → Review → Done

Görevleri GitHub Issues üzerinden takip edin. Her Issue için sorumlu, açıklama, kabul kriteri ve durum belirtin.

## 5. PHASE 3 — Requirements Engineering

`docs/mvp-requirements.md` dosyasını oluşturun.

En az aşağıdaki gereksinimleri değerlendirin:

- REQ-01: Kullanıcı ders programına yeni ders ekleyebilir.
- REQ-02: Kullanıcı kayıtlı derslerini günlere göre görüntüleyebilir ve silebilir.
- REQ-03: Sistem sıradaki dersi doğru belirler.
- REQ-04: Kullanıcı pazar yeri ilanı oluşturabilir.
- REQ-05: Kullanıcı ilanları arayabilir ve kategoriye göre filtreleyebilir.
- REQ-06: Kullanıcı kendi oluşturduğu ilanı silebilir.
- REQ-07: Kullanıcı profil bilgilerini kaydedebilir.
- REQ-08: Veriler tarayıcı yenilendiğinde korunur.
- REQ-09: Kullanıcı verilerini kontrollü biçimde sıfırlayabilir.
- REQ-10: Uygulama simülasyon ve yerel veri sınırlamalarını açıkça belirtir.

Her gereksinim için:

- Requirement ID
- User Story
- Acceptance Criteria
- Priority
- Implementation Status

alanlarını hazırlayın.

Gereksinimlerin mevcut kodda gerçekten karşılanıp karşılanmadığını inceleyin.

## 6. PHASE 4 — Software Testing

`docs/test-cases.md` ve `docs/test-execution-report-w07.md` dosyalarını oluşturun.

En az 12 test senaryosu hazırlayın:

1. Geçerli ders ekleme.
2. Bitiş saatinin başlangıçtan önce olması.
3. Aynı güne çakışan derslerin girilmesi.
4. Ders silme ve liste güncelleme.
5. Sıradaki ders hesaplaması.
6. Geçerli pazar yeri ilanı oluşturma.
7. Boş veya geçersiz fiyat girişleri.
8. Kategori filtreleme.
9. İlan arama.
10. İlan silme.
11. LocalStorage kalıcılığı.
12. Tüm verileri silme onayı ve sıfırlama.
13. Mobil görünüm ve karanlık mod.
14. Örnek veri yükleme davranışı.
15. Kullanıcı girdilerinin güvenli görüntülenmesi.

Her testte şu alanlar bulunmalıdır:

**Test ID → Requirement ID → Preconditions → Steps → Expected Result → Actual Result → Status → Evidence**

Testleri Positive, Negative ve Boundary Value Analysis ilkelerine göre sınıflandırın.

Uygulamayı gerçekten çalıştırmadan `PASS` yazmayın.

## 7. PHASE 5 — Bug Tracking & Regression Testing

Testlerde doğrulanan hatalar için GitHub Issue açın.

Issue formatı:

- `[BUG] Hata başlığı`
- Related Requirement
- Related Test Case
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity
- Evidence

Hata giderme sürecini şu şekilde belgeleyin:

Reproduce → Diagnose → Fix → Retest → Regression Test

Örneğin ders ekleme mantığında düzeltme yapıldığında ders listeleme, sıradaki ders hesaplaması ve LocalStorage işlevlerini yeniden test edin.

Doğrulanmamış riskleri gerçekleşmiş hata gibi raporlamayın.

## 8. PHASE 6 — GitHub Collaboration

Ekip üyeleri anlamlı görev paylaşımı yapmalıdır.

Her değişiklik için uygun bir Issue ve mümkünse ayrı bir Branch kullanın.

Örnek akış:

Issue → Branch → Commit → Pull Request → Peer Review → Merge

Pull Request açıklamasında ilgili Issue, değişiklik özeti ve gerçek test sonuçları yer alsın.

**Approve ≠ Merge.**

Başka bir ekip üyesinin yaptığı inceleme ve değerlendirme görünür olmalıdır.

Geçmişte yapılmamış incelemeleri geriye dönük yapılmış gibi göstermeyin.

## 9. PHASE 7 — Engineering Evidence & AI Usage

Aşağıdaki belgeleri hazırlayın:

- `docs/engineering-evidence.md`
- `docs/requirements-traceability.md`
- `evidence/ai-human-evidence.md`

Yapay zekâ kullanıldıysa hangi önerilerin alındığını, hangilerinin kabul veya reddedildiğini ve öğrencilerin bu kararları neden verdiğini açıklayın.

AI tarafından hazırlanmış kodun test edildiğini ve insan tarafından incelendiğini varsaymayın; kanıt gösterin.

## 10. PHASE 8 — Code Quality Review

Mevcut `UniGo MVP.html` dosyasını inceleyin.

Özellikle:

- HTML, CSS ve JavaScript ayrıştırılmalı mı?
- Form doğrulamaları yeterli mi?
- Ders saatleri ve çakışmalar doğru ele alınıyor mu?
- İlan fiyatı ve iletişim alanları güvenli mi?
- LocalStorage hata durumları doğru yönetiliyor mu?
- README, gerçek uygulamayla tutarlı mı?

Mevcut tasarımı bozmadan, gerekli değişiklikleri küçük ve test edilebilir adımlarla gerçekleştirin.

## 11. Definition of Done

Bir görev ancak aşağıdaki şartlarda tamamlanmış kabul edilir:

- Gereksinim tanımlanmıştır.
- Kabul kriterleri karşılanmıştır.
- Kod veya belge ilgili Issue ile ilişkilidir.
- Testler gerçekten yürütülmüştür.
- Sonuçlar ve kanıtlar kaydedilmiştir.
- Gerekliyse regresyon testi yapılmıştır.
- Başka bir ekip üyesi tarafından inceleme gerçekleştirilmiştir.
- Değişiklikler GitHub üzerinde izlenebilir durumdadır.

## 12. Beklenen Sonuç

Bu telafi çalışması sonunda UniGo ekibinden yeni ve büyük özellikler değil, **mevcut MVP'nin mühendislik açısından açıklanabilir ve doğrulanabilir hâle getirilmesi** beklenmektedir.

Önceliğiniz daha fazla kod yazmak değil, mevcut kodun neden ve nasıl geliştirildiğini göstermek olmalıdır.

**Engineering Principle:**

Problem → Requirement → Implementation → Test → Evidence → Human Review

**AI can assist development. Engineering accountability remains with the team.**

Başarılar dilerim.

**Dr. Öğr. Üyesi Murat Göksu**
