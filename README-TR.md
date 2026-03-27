# 🏥 ZeynPharmacy - Backend ve Web Arayüzü Platformu

![.NET](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-B92259?style=for-the-badge&logo=entityframework&logoColor=white)

> **⚠️ Önemli Not:** Güvenlik ve gizlilik politikaları gereği, bu deponun (repository) kaynak kodları kapalı tutulmaktadır (Closed-Source). Bu doküman, projenin teknik yeteneklerini ve mimari tasarımını tanıtmak amacıyla detaylandırılmıştır.

## 📱 Zeyn Eczane Mobil Uygulaması
Bu depo Backend API ve Web arayüzünü içermektedir. Çoklu QR tarama ve belge çözümleme işlemleri için geliştirilen mobil uygulama ayrı bir depoda tutulmaktadır.
👉 **[Zeyn Eczane Mobil Deposunu incelemek için buraya tıklayın](#)**

## 🚀 Proje Hakkında
ZeynPharmacy, geleneksel eczane yönetim yazılımlarının ötesine geçerek, **eczaneler arası takas sistemini** merkeze alan yenilikçi bir platform sunar. Modern web teknolojileriyle geliştirilen uygulama, sıkı güvenlik yetkilendirme katmanlarından veritabanı performans optimizasyonlarına kadar her aşamada sektörel standartları (Best Practices) barındırmaktadır.

## 🏗️ Mimari ve Klasör Yapısı

Proje, **Clean Architecture (Temiz Mimari)** prensiplerine tam uyumlu bir şekilde, birbirinden bağımsız modüler katmanlara ayrılmıştır:

```text
📂 Zeyn.Solution
 ┣ 📂 Zeyn.Api             # RESTful API Uç Noktaları / Sunum Katmanı
 ┣ 📂 Zeyn.Application     # İş Mantığı, Servisler ve Kullanım Senaryoları
 ┣ 📂 Zeyn.Domain          # Temel Varlıklar (Entities), Enumlar ve Çerçeveden Bağımsız Kurallar
 ┣ 📂 Zeyn.Infrastructure  # Veri Erişimi (EF Core), Fluent API ve Dış Entegrasyonlar
 ┗ 📂 Zeyn.Web             # ASP.NET Core MVC / Blazor Kullanıcı Arayüzü Bileşenleri
```

## 🛠️ Teknolojiler ve Mimari Desenler
- **Backend:** .NET (C#), ASP.NET Core Web API
- **Frontend / Arayüz:** ASP.NET Core MVC, Blazor (Bileşen tabanlı UI), Tailwind CSS ile Modern Tasarım
- **Veritabanı ve ORM:** MySQL, Entity Framework Core (Code-First)
- **Mimari Disiplinler:** Clean Architecture, SOLID, Dependency Injection, Request-Response Pattern
- **Verimlilik Araçları:** AutoMapper (DTO modellemeleri), FluentValidation (Girdi doğrulama ve kuralları)
- **Güvenlik Katmanı:** Özelleştirilmiş Rol ve İzin Yönetimi Sistemi

## ✨ Öne Çıkan Modüller ve Özellikler
1. **Eczane Takas Modülü (`Zeyn.Pharmacy.Swap`):** Eczanelerin kendi aralarında ilaç, medikal ürün ve diğer envanterleri sorunsuz bir şekilde takas etmelerini sağlayan spesifik iş modülü.
2. **Kapsamlı Kimlik Yönetimi (`Zeyn.Auth` & `Zeyn.Permission`):** Rol ve detaylı izin yetkilendirmesi. Sistem, kullanıcıları modüller ve aksiyonlar bazında mikro yetkilerle donatır.
3. **Merkezi Hata ve Log Yönetimi:** İstisnaları tek bir noktada değerlendirerek istemciye kontrollü ve güvenli bilgi aktaran izole yapı.
4. **Yüksek Performanslı Veri Taşıma:** Tüm süreç veritabanında DTO mimarisi eşliğinde koşturularak N+1 sorgu problemi ve gereksiz bellek (memory) tahsislerinin önüne geçilmiştir. Okuma senaryolarında optimum performans için sadece gerekli veriler tüketilir.

## 🛡️ Güvenlik ve Altyapı Standartları
Sistem güvenliği en üst seviyede tutulmuştur. Entity veya veritabanı nesneleri asla doğrudan dış dünyaya açılmaz. İstekler (Request) ve Yanıtlar (Response) izole edilmiş DTO'lar aracılığıyla taşınır. Yetkisiz erişimi engellemek için kullanıcı oturum (session) ve token doğrulama mekanizmaları tüm uç noktalarda ve web bileşenlerinde proaktif bir rol oynar.

---

<p align="center">
  <b>ZeynPharmacy</b> • 2026
</p>
