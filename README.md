# Mohamed Abdelmoniem

**.NET Software Engineer — Backend & Full-Stack Development**

![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET%2010-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-5C2D91?style=flat-square&logo=dotnet&logoColor=white)
![EF Core](https://img.shields.io/badge/EF%20Core-512BD4?style=flat-square&logo=nuget&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![xUnit](https://img.shields.io/badge/xUnit-25A162?style=flat-square&logo=dotnet&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

I build business systems and APIs with ASP.NET Core, Entity Framework Core and SQL Server — from the domain model and its business rules through the API/MVC layer, the test suite, and CI/CD into production.

---

## What I build

- Server-rendered and API-driven ASP.NET Core applications (Web API + MVC/Razor), consumed by web and mobile clients
- Systems structured around **Clean Architecture** — Domain, Application, Infrastructure and Presentation as separate projects, with dedicated architecture-conformance tests so the layering is enforced by the build, not just convention
- Domain models built around explicit **state machines** for the business processes they represent (listing lifecycles, order pipelines, auction phases) rather than ad-hoc status flags
- Authentication & authorization: JWT bearer auth for API clients, cookie auth for staff/back-office, OTP-based passwordless flows, and permission-based (not role-name-based) access control
- Real-time features with SignalR, background job processing (self-perpetuating scheduled jobs, not just cron scripts), structured logging with Serilog
- Automated test suites — unit, integration (against real SQL Server, not in-memory fakes), and architecture-conformance tests
- CI/CD pipelines in GitHub Actions that build, run the full test suite, and only deploy on a green build

## Featured engineering projects

Both source repositories are private (production/business systems). Each showcase below is a full engineering case study — architecture, domain model, business rules, security decisions, and testing strategy — without the implementation code.

<table>
<tr>
<td width="50%" valign="top">

### [Zawed →](https://github.com/default-z/Zawed-Showcase)
**Livestock Auction & Marketplace Platform**

A multi-app ASP.NET Core system (WebApi + AdminMvc + background job host) covering the full lifecycle of an online livestock sale: listing moderation, timed auctions with real-time bidding, OTP + KYC-gated accounts, an escrow-style payment/settlement flow, delivery handover, and staff operations — backed by 2,000+ automated tests across unit, integration and architecture-conformance suites.

`Clean Architecture` `SignalR` `Background Jobs` `OTP/KYC` `State Machines`

</td>
<td width="50%" valign="top">

### [Khedma →](https://github.com/default-z/Khedma-Showcase)
**CMS-Driven Business Platform**

A bilingual (Arabic/English) content platform where the public site and the admin dashboard are the *same application*, reading and writing the same database rows — eliminating the drift that splits a panel and its site out of sync. Cache invalidation via a single version counter, permission-based RBAC, and privacy-first first-party analytics with no IP storage.

`Clean Architecture` `Shared-State Design` `RBAC` `Bilingual/RTL`

</td>
</tr>
</table>

## Engineering capabilities

<table>
<tr>
<td width="33%" valign="top">

**Backend engineering**

- C# · ASP.NET Core (Web API & MVC)
- Entity Framework Core · LINQ
- SQL Server · migrations
- JWT · cookie auth · OTP flows
- SignalR
- REST API design
- Swagger / OpenAPI

</td>
<td width="33%" valign="top">

**Software engineering**

- Clean Architecture
- Domain modeling & state machines
- Business-rule enforcement at the domain layer
- Repository/service patterns
- Dependency Injection
- Git & GitHub Actions CI/CD

</td>
<td width="33%" valign="top">

**Testing & quality**

- Unit testing (xUnit, NSubstitute)
- Integration testing against real SQL Server
- Architecture-conformance testing (NetArchTest)
- FluentValidation
- Structured logging (Serilog)

</td>
</tr>
</table>

## Architecture & system design

Both featured projects are built around an explicit domain model rather than a CRUD-with-status-flags approach — auction lots, listings, and orders each have their own state machine with rules enforced in the domain layer, not left to the UI to get right. Layering is checked automatically: a dedicated architecture-test project fails the build if a layer boundary is crossed (e.g. Domain depending on Infrastructure). The Zawed showcase documents this in the most depth, including Mermaid diagrams of the listing, auction, and order state machines and the end-to-end seller-to-settlement flow.

## Testing & engineering quality

Both platforms are tested, not just claimed to be:

| | Test files | Test cases | What's covered |
|---|---|---|---|
| **Zawed** | 227 | 2,000+ | Unit, integration (real SQL Server), and architecture-conformance |
| **Khedma** | 15 | 106 | Unit and integration (real SQL Server, per-test databases) |

Integration suites run against a real SQL Server instance in both projects — specifically because the behavior under test (filtered unique indexes, cascade rules, atomic counter updates) doesn't exist in an in-memory fake. Every push runs the full suite in CI before anything can deploy.

## Currently

Building production ASP.NET Core systems professionally. More public showcases go up as current work reaches a stage I can document without exposing the underlying business.

## Contact

[![Email](https://img.shields.io/badge/Email-mohamedabdelmoniem.2003.1%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:mohamedabdelmoniem.2003.1@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-mohamed--abdelmoniem-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohamed-abdelmoniem-068845295/)
