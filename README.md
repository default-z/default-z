### Mohamed Abdelmoniem
**.NET Full-Stack Developer**

I build production web applications with ASP.NET Core, Entity Framework Core and SQL Server — from the domain model through the API/MVC layer to CI/CD deployment.

---

#### What I build

- Server-rendered and API-driven ASP.NET Core applications (Web API + MVC/Razor)
- Systems structured around **Clean Architecture** (Domain / Application / Infrastructure / Presentation as separate projects), with dedicated architecture-conformance tests to keep layering honest
- Authentication & authorization: JWT bearer auth, ASP.NET Core Identity, and custom role/action-based access control
- Real-time features with SignalR, background job processing with Hangfire, structured logging with Serilog
- Automated test suites — unit, integration (against a real SQL Server instance, not just in-memory), and architecture tests
- CI/CD pipelines in GitHub Actions that build, test and deploy to Windows/IIS hosting

#### Selected projects

Full source for both is private (production/business systems) — each repo below is an engineering case study: architecture, business rules, testing strategy and engineering decisions, without the implementation code.

| Project | What it is | Highlights |
|---|---|---|
| [**Zawed — Showcase**](https://github.com/default-z/Zawed-Showcase) | Livestock auction & marketplace platform | Clean Architecture across 5+ projects · real-time bidding via SignalR · OTP + KYC + step-up auth · background auction-sweep jobs · 2,000+ automated tests |
| [**Khedma — Showcase**](https://github.com/default-z/Khedma-Showcase) | Bilingual CMS-driven business platform | Dashboard and public site share one database (no drift by design) · version-counter cache invalidation · permission-based RBAC · privacy-first analytics |

#### Tech stack

**Backend**
C# · .NET 10 · ASP.NET Core (Web API & MVC) · Entity Framework Core · LINQ · ASP.NET Core Identity · JWT

**Architecture & engineering**
Clean Architecture · Dependency Injection · FluentValidation · SignalR · Hangfire · xUnit · FluentAssertions · NSubstitute · NetArchTest (architecture tests) · Git & GitHub Actions

**Databases**
SQL Server · EF Core Migrations · Central Package Management

**Tools**
Serilog · Swagger / OpenAPI (Swashbuckle) · MailKit · HtmlSanitizer

#### Currently

Building production ASP.NET Core systems professionally. More public showcases go up as current work reaches a stage I can document without exposing the underlying business.

#### Contact

- Email: mohamedabdelmoniem.2003.1@gmail.com
- LinkedIn: [mohamed-abdelmoniem](https://www.linkedin.com/in/mohamed-abdelmoniem-068845295/)
