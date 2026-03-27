# 🏥 ZeynPharmacy - Pharmacy Management & Swap System

![.NET](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-B92259?style=for-the-badge&logo=entityframework&logoColor=white)

This project is a comprehensive automation system developed to facilitate inter-pharmacy product swapping, inventory management, and general pharmacy operations. It is designed with high scalability, flexibility, and sustainability principles (**Clean Architecture & SOLID**) at its core.

> **⚠️ Important Note:** Due to strict security and privacy policies, the source code of this repository is kept closed (Closed-Source). This repository serves as a portfolio piece to demonstrate the project's technical capabilities and architectural approach.

---

## 🚀 About the Project

ZeynPharmacy goes beyond traditional pharmacy management software by offering an innovative platform centered around an **inter-pharmacy swap system**. Developed with modern web and mobile technologies, the application incorporates industry best practices at every stage, from strict security authorization layers to advanced database performance optimizations.

---

## 🏗️ Architecture & Folder Structure

The project is strictly decoupled into modular layers, fully compliant with **Clean Architecture** principles:

```text
📂 Zeyn Solution
 ┣ 📂 Zeyn.Api             # RESTful API Endpoints / Presentation Layer
 ┣ 📂 Zeyn.Application     # Business Logic, Services & Use Cases
 ┣ 📂 Zeyn.Domain          # Core Entities, Enums & Framework-Independent Business Rules
 ┣ 📂 Zeyn.Infrastructure  # Data Access (EF Core), Fluent API & External Integrations
 ┣ 📂 Zeyn.Mobile          # Flutter Mobile App Integration (QR & Scanner)
 ┗ 📂 Zeyn.Web             # ASP.NET Core MVC / Blazor UI Components
```

---

## ✨ Core Modules & Features

1. **Integrated Mobile Application (QR & Document Scanner):** A fully synchronized mobile app featuring multi-QR code scanning for rapid inventory counting, consolidating multiple QR codes into a single code, document scanning, and real-time QR decoding services.
2. **Pharmacy Swap Module (`Zeyn.Pharmacy.Swap`):** A highly specific business module that enables pharmacies to exchange medications, medical products, and other inventory among themselves seamlessly.
3. **Comprehensive Identity Management (`Zeyn.Auth` & `Zeyn.Permission`):** Advanced role and detailed permission authorization. The system equips users with micro-permissions based on specific modules and actions.
4. **Centralized Exception & Log Management:** An isolated structure that evaluates exceptions at a single point, delivering controlled and secure information to the client.
5. **High-Performance Data Transfer:** All processes are executed alongside a DTO architecture in the database layer, eliminating the N+1 query problem and unnecessary memory allocations. Only essential data is consumed for optimal performance in read scenarios.

---

## 🛠️ Technologies & Architectural Patterns

- **Backend:** .NET (C#), ASP.NET Core Web API
- **Mobile Development:** Flutter, Dart (For QR & Scanner modules)
- **Frontend / UI:** ASP.NET Core MVC, Blazor (Component-based UI), Modern Design with Tailwind CSS
- **Database & ORM:** MySQL, Entity Framework Core (Code-First)
- **Architectural Disciplines:** Clean Architecture, SOLID, Dependency Injection, Request-Response Pattern
- **Productivity Tools:** AutoMapper (DTO modeling), FluentValidation (Input validation rules)
- **Security Layer:** Customized Role & Permission Management System

---

## 🛡️ Security & Infrastructure Standards

System security is maintained at the highest level. Database entities or internal objects are never exposed directly to the outside world. Requests and Responses are transported via strictly isolated DTOs. Proactive user session and token validation mechanisms (JWT) are integrated across all endpoints and web components to prevent unauthorized access.

---


<p align="center">
  <b>ZeynPharmacy</b> • 2026
</p>
