# 🏥 ZeynPharmacy - Backend & Web UI Platform

![.NET](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-B92259?style=for-the-badge&logo=entityframework&logoColor=white)

> **⚠️ Important Note:** Due to security and privacy policies, the source code of this repository is kept closed (Closed-Source). This document is detailed to introduce the project's technical capabilities and architectural design.

## 📱 ZeynPharmacy Mobile App
This repository contains the Backend API and Web UI. The mobile application, built for multi-QR scanning and document decoding, is maintained in a separate repository.
👉 **[Click here to view the ZeynPharmacy Mobile Repository](#)** 

---

## 🚀 About the Project
ZeynPharmacy goes beyond traditional pharmacy management software by offering an innovative platform centered around an **inter-pharmacy swap system**. Developed with modern web technologies, the application incorporates industry best practices at every stage, from strict security authorization layers to database performance optimizations.

## 🏗️ Architecture & Folder Structure

The project is strictly decoupled into modular layers, fully compliant with **Clean Architecture** principles:

```text
📂 Zeyn.Solution
 ┣ 📂 Zeyn.Api             # RESTful API Endpoints / Presentation Layer
 ┣ 📂 Zeyn.Application     # Business Logic, Services & Use Cases
 ┣ 📂 Zeyn.Domain          # Core Entities, Enums & Framework-Independent Rules
 ┣ 📂 Zeyn.Infrastructure  # Data Access (EF Core), Fluent API & External Integrations
 ┗ 📂 Zeyn.Web             # ASP.NET Core MVC / Blazor UI Components
```


## 🛠️ Technologies & Architectural Patterns
- **Backend:** .NET (C#), ASP.NET Core Web API
- **Frontend / UI:** ASP.NET Core MVC, Blazor (Component-based UI), Modern Design with Tailwind CSS
- **Database & ORM:** MySQL, Entity Framework Core (Code-First)
- **Architectural Disciplines:** Clean Architecture, SOLID, Dependency Injection, Request-Response Pattern
- **Productivity Tools:** AutoMapper (DTO modeling), FluentValidation (Input validation rules)
- **Security Layer:** Customized Role & Permission Management System

## ✨ Core Modules & Features
1. **Pharmacy Swap Module (`Zeyn.Pharmacy.Swap`):** A specific business module enabling pharmacies to exchange medications, medical products, and other inventory among themselves.
2. **Comprehensive Identity Management (`Zeyn.Auth` & `Zeyn.Permission`):** Role and detailed permission authorization. The system equips users with micro-permissions based on modules and actions.
3. **Centralized Exception & Log Management:** An isolated structure that evaluates exceptions at a single point, delivering controlled and secure information to the client.
4. **High-Performance Data Transfer:** All processes are executed with a DTO architecture in the database, preventing the N+1 query problem and unnecessary memory allocations. Only essential data is consumed for optimal performance in read scenarios.

## 🛡️ Security & Infrastructure Standards
System security is maintained at the highest level. Entities or Database objects are never exposed directly to the outside world. Requests and Responses are transported via isolated DTOs. User session and token validation mechanisms play a proactive role across all endpoints and web components to prevent unauthorized access.
