# ZeynEczane (ZeynPharmacy) - Eczane Yönetim ve Takas Sistemi

Bu proje, eczaneler arası ürün takasını, stok yönetimini ve genel eczane operasyonlarını kolaylaştırmak amacıyla geliştirilmiş kapsamlı bir otomasyon sistemidir. Yüksek ölçeklenebilirlik, esneklik ve sürdürülebilirlik ilkeleri (Clean Architecture & SOLID) göz önünde bulundurularak tasarlanmıştır.

*Not: Güvenlik ve gizlilik politikaları gereği, bu deponun (repository) kaynak kodları kapalı tutulmaktadır. Bu sayfa, projenin teknik yeteneklerini ve mimari yapısını tanıtmak amacıyla detaylandırılmıştır.*

## 🚀 Proje Hakkında 

ZeynEczane, geleneksel eczane yönetim yazılımlarının ötesine geçerek, **eczaneler arası takas sistemini** merkeze alan yenilikçi bir platform sunar. Modern web teknolojileriyle geliştirilen uygulama, sıkı güvenlik yetkilendirme katmanlarından veritabanı performans optimizasyonlarına kadar her aşamada sektörel standartları (Best Practices) barındırmaktadır.

## 🏛️ Mimari Yapı (Clean Architecture)

Proje, **Clean Architecture (Temiz Mimari)** prensiplerine tam uyumlu bir şekilde modüler katmanlara ayrılmıştır:

- **Core / Domain:** Projenin kalbidir. Veritabanı ve framework bağımsız iş kuralları, Entity'ler ve Enum'lar bu modülde soyutlanmıştır.
- **Infrastructure:** Veritabanı erişimi (Entity Framework Core), Fluent API veri modelleme ve dış entegrasyon bağımlılıkları burada yönetilir.
- **Application / Service:** İş mantığının (Business Logic) bulunduğu, Domain ile Presentation katmanları arasında köprü görevi gören asıl servis katmanıdır.
- **Presentation:** RESTful API servisleri (`Zeyn.Api`) ve son kullanıcı arayüzü (`Zeyn.Web` - ASP.NET Core MVC / Blazor) bileşenlerini barındırır.

## 🛠️ Kullanılan Teknolojiler ve Mimari Desenler

- **Backend:** .NET (C#), ASP.NET Core Web API
- **Frontend / UI:** ASP.NET Core MVC, Blazor (Component bazlı UI), Tailwind CSS ile Modern Tasarım
- **Veritabanı ve ORM:** MySQL, Entity Framework Core (Code-First)
- **Mimari Disiplinler:** Clean Architecture, SOLID, Dependency Injection, Request-Response Pattern
- **Verimlilik Araçları:** AutoMapper (DTO modellemeleri), FluentValidation (Girdi doğrulama ve validasyon kuralları)
- **Güvenlik Katmanı:** Özelleştirilmiş Yetki/İzin Sistemi (Role & Permission Management)

## ✨ Öne Çıkan Ana Modüller

1. **Eczane Takas Modülü (`Zeyn.Pharmacy.Swap`):** Eczanelerin kendi aralarında ilaç, medikal ürün ve diğer envanter takasını yapabilmesine imkan sağlayan spesifik iş modülü.
2. **Kapsamlı Kimlik Yönetimi (`Zeyn.Auth` & `Zeyn.Permission`):** Rol ve detaylı izin yetkilendirmesi. Sistem, kullanıcıları modüller ve aksiyonlar bazında mikro yetkilerle donatır.
3. **Merkezi Hata ve Log Yönetimi:** İstisnaları tek bir noktada değerlendirerek istemciye kontrollü ve güvenli bilgi aktaran izole yapı.
4. **Yüksek Performanslı Veri Taşıma:** Tüm süreç veri tabanında DTO mimarisi eşliğinde koşturularak N+1 sorgu problemi ve gereksiz memory allocation'ların önüne geçilmiştir; okuma senaryolarında izo-performans için sadece gerekli veriler tüketilir.

## 🛡️ Güvenlik ve Altyapı Standartları

Sistem güvenliği üst seviyede tutulmuştur. Dış dünyaya asla doğrudan Entity veya Database objesi çıkarılmaz. İstekler (Request) ve Cevaplar (Response) izole DTO'lar ile taşınır. Kullanıcı session ve token doğrulama mekanizmaları tüm end-point ve web bileşenlerinde proaktif rol oynayarak yetkisiz erişimi engeller.
