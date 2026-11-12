# Awesome-Role-Based-Access-Control-Entitlements

# Awesome Role-Based Access Control & Entitlements

> A curated list of top Role-Based Access Control (RBAC) and Entitlement Management platforms — both SaaS/Hosted commercial solutions and open-source alternatives for managing user roles, fine-grained permissions, and access entitlements at scale.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Okta](#okta)
  - [Microsoft Entra ID](#microsoft-entra-id)
  - [Ping Identity](#ping-identity)
  - [CyberArk Identity](#cyberark-identity)
  - [SailPoint](#sailpoint)
  - [OneLogin](#onelogin)
  - [Auth0](#auth0)
- [Open-Source Software](#-open-source-software)
  - [Apache Syncope](#apache-syncope)
  - [Evolveum midPoint](#evolveum-midpoint)
  - [OpenAM](#openam)
  - [OpenRBAC](#openrbac)
  - [Keycloak](#keycloak)
  - [Casbin](#casbin)
  - [OpenFGA](#openfga)
  - [SpiceDB](#spicedb)
  - [Ory Keto](#ory-keto)
  - [Cerbos](#cerbos)
  - [Paralus](#paralus)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted RBAC and Entitlement Management platforms. These are not open-source but are included as reference points for feature comparison.

### Okta
**Type:** Enterprise IAM with standard and custom admin roles  
Okta provides standard admin roles (Super Admin, Org Admin, App Admin, Group Admin, Read-Only Admin) with predefined permissions, plus custom roles that bundle granular permissions. Role assignments can be scoped to specific resources for least-privilege access.

### Microsoft Entra ID
**Type:** Identity platform with built-in and custom roles  
Entra ID provides built-in roles (Global Admin, User Admin, App Admin) and custom roles assignable at Tenant, Administrative Unit, or specific resource scope. PIM enables just-in-time role activation with approval workflows and audit trails.

### Ping Identity
**Type:** Enterprise identity with hierarchical admin roles  
PingOne provides built-in admin roles with defined role-assignment hierarchies (e.g., Environment Admin can assign all roles except Organization Admin). Custom roles can be created with granular permission identifiers, with automatic, group-based, or user-based assignments.

### CyberArk Identity
**Type:** Identity administration with role-based rights  
CyberArk Identity uses roles as the unit of access control, assigning application access, administrative rights, and policies to roles rather than individual users. Roles can bundle both app access and administrative privileges.

### SailPoint
**Type:** Enterprise identity governance and administration (IGA)  
SailPoint provides identity governance, access certifications, role management, and policy enforcement across enterprise applications, ensuring entitlements are granted, reviewed, and revoked according to policy.

### OneLogin
**Type:** IAM with app-centric roles and attribute mapping  
OneLogin roles are collections of apps; assigning a user to a role grants access to all apps in that role. Mappings can automatically assign users to roles based on directory attributes (e.g., Department = HR).

### Auth0
**Type:** Developer IAM with dashboard roles  
Auth0 provides dashboard roles including Admin (full read/write), Editor roles for specific resources (Connections, Organizations, Specific Apps, Users), and Viewer roles for read-only access, enabling least-privilege dashboard access.

---

## 🟩 Open-Source Software

Self-hosted, community-driven RBAC and Entitlement Management tools. The open-source ecosystem spans **full IGA platforms with role/entitlement management**, **authorization engines for fine-grained decisions**, and **Kubernetes-native access control**.

### Apache Syncope
**Stack:** Java | **License:** Apache-2.0  
Apache Syncope is an open-source Identity and Access Management (IAM) and Identity Governance Administration (IGA) platform designed to manage digital identities, user provisioning, authentication, authorization, and access control across enterprise environments [citation:2]. Key features include **user, group, role, and entitlement management**, automated user provisioning/deprovisioning workflows, RBAC and delegated administration, support for LDAP, Active Directory, databases, and external systems, REST APIs, SAML 2.0/OIDC/SCIM standards support, and audit logging with compliance reporting [citation:2]. The platform also includes **approval and request management** with configurable approval workflows and workflow event notification [citation:13]. Deploys via Docker containers with a web-based administrative console [citation:2].  
**Best for:** Organizations wanting a comprehensive open-source IGA platform with native role/entitlement management, approval workflows, and broad connector support under Apache-2.0 licensing.

### Evolveum midPoint
**Stack:** Java | **License:** Open Source (subscription model)  
Evolveum midPoint is a comprehensive open-source Identity Governance and Administration (IGA) platform used by organizations worldwide for identity provisioning, governance, compliance, and access management . Its most important features include **identity governance, security auditing and reporting, organizational structure management, credential management, request approval, and entitlement management** . Additional capabilities include advanced RBAC with temporal constraints, identity synchronization (liveSync, reconciliation, discovery, import), password policies, ConnId connectors, provisioning consistency and error handling, and high availability support . It also handles identity lifecycle management, governance, and analytics, automatically creating, assigning, enabling, and disabling accounts while managing the assignment of roles and entitlements to employees, partners, agents, contractors, customers, and students [citation:9].  
**Best for:** Organizations needing enterprise-grade open-source IGA with deep governance, role/entitlement lifecycle management, and approval workflows, accepting the operational overhead of a Java-based platform.

### OpenAM
**Stack:** Java | **License:** Open Source (per GitHub)  
OpenAM is an open access management solution that includes Authentication, SSO, Authorization, Federation, **Entitlements**, and Web Services Security [citation:1]. It supports Cross Domain Single Sign On (CDSSO), SAML 2.0, OAuth 2.0, and OpenID Connect, integrating with legacy, custom, and cloud applications without modification [citation:1]. Access policies can be role-based, authentication level-based, or attribute-based, with scripting for flexible access policy logic [citation:1].  
**Best for:** Organizations wanting a proven open-source access management platform with native entitlements and policy-based authorization, particularly for legacy/cloud integration scenarios.

### OpenRBAC
**Stack:** Spring Boot / Java | **License:** Open Source (per GitHub)  
OpenRBAC is a high-performance RBAC engine designed for modern microservices and multi-tenant applications, going beyond simple RBAC with hierarchical groups and inheritance [citation:5]. Key features include **multi-tenancy via realms**, **hierarchical groups with recursive membership inheritance**, granular RBAC with four-level permission inheritance (Direct, Role, Group, Group-Role), temporary access with expiry dates, and a unified "effective" view that solves the N+1 problem by fetching all effective security contexts in a single query [citation:5]. Includes an Angular admin UI and Keycloak synchronization [citation:5]. **Note:** Audit logging, ABAC support, and client SDKs are planned but not yet available [citation:5].  
**Best for:** Java/Spring Boot teams wanting a purpose-built, high-performance RBAC engine with hierarchical groups and multi-tenancy, accepting that some enterprise features are still on the roadmap.

### Keycloak
**Stack:** Java | **License:** Apache-2.0  
Keycloak is the most widely deployed open-source IAM platform, providing realm-level roles, client roles, composite roles, and group-based role mapping. Fine-grained authorization services allow defining resources, scopes, and policies (role, user, client, time, aggregate) for complex access decisions. Admin console access is controlled via admin roles.  
**Best for:** Organizations wanting a proven IAM foundation with rich role modeling and policy-based authorization, accepting that multi-admin approval for role changes must be implemented separately.

### Casbin
**Stack:** Multi-language (Go, Java, Node, Python, PHP, .NET, Rust) | **License:** Apache-2.0  
Apache Casbin (Incubating) is the "quiet giant" of authorization libraries, with 20,334 GitHub stars and implementations across major languages [citation:10]. It supports ACL, RBAC, ABAC, and RESTful access control models, with models and policies defined in configuration files for flexible role inheritance and custom access logic. **Trade-off:** It is a library, not a platform—you embed it in your application and build admin UI, approval, and audit on top. No network hop and no vendor, but no control plane and no answer for "which objects can this user see" [citation:10].  
**Best for:** Developers wanting a flexible, embeddable authorization engine with model-driven RBAC/ABAC policies, particularly for monoliths needing real ABAC without a separate service.

### OpenFGA
**Stack:** Go | **License:** Apache-2.0  
OpenFGA is a high-performance, flexible authorization/permission engine built for developers and inspired by Google Zanzibar [citation:6]. It entered CNCF Incubating maturity in October 2025 and provides a JSON-based model definition with rich SDKs across Node, Go, Python, Java, .NET, and Ruby [citation:4][citation:10]. The modeling language reads close to English, and `ListObjects` is first-class for answering "which objects can this user see" [citation:10]. **Trade-off:** Operational overhead includes a stateful service plus a sync path that writes a tuple whenever your app creates a shareable resource [citation:10].  
**Best for:** Organizations wanting a CNCF-backed, Zanzibar-style relationship-based authorization system with strong SDK support and clear governance.

### SpiceDB
**Stack:** Go | **License:** Apache-2.0  
SpiceDB is the most established Zanzibar-inspired authorization database, designed for scalably storing and querying fine-grained authorization data [citation:6][citation:8]. Its key differentiator is **consistency control**—explicit consistency levels including a ZedToken requiring a read as fresh as your last write, addressing the cache staleness problem in permission revocation [citation:10]. Performance is p99 < 10ms Check on a single node, scaling horizontally to hundreds of thousands of Check/sec [citation:4]. Pricing includes open source free, AuthZed Cloud advertised as "deploy a permissions system for $2/hr" with $700 in starter credits, and self-hosted enterprise licensed per region and vCPU [citation:10].  
**Best for:** Organizations needing the highest scale and explicit consistency controls for fine-grained authorization, accepting the heaviest operational commitment among Zanzibar implementations.

### Ory Keto
**Stack:** Go | **License:** Apache-2.0  
Ory Keto is an open-source authorization server implementing Google Zanzibar-style relationship-based access control (ReBAC) [citation:4]. It answers "can subject X do action Y on object Z" using relationship tuples, supporting fine-grained permissions that can model RBAC, ABAC, and hierarchical access. Part of the broader Ory stack (Kratos, Hydra).  
**Best for:** Teams already running the Ory stack wanting integrated relationship-based authorization, accepting a partial Zanzibar model compared to SpiceDB.

### Cerbos
**Stack:** Go | **License:** Apache-2.0  
Cerbos is a **policy-driven** authorization solution (not relationship-driven), positioned as a stateless Policy Decision Point (PDP) that stores no permissions [citation:4]. Policies are authored in YAML, and context (subject, resource, environment) is provided by the caller on every request. The open-source PDP is free forever; Cerbos Hub adds a control plane with a Proof of Concept tier at $0/mo up to 100 monthly active principals and Development from $25/mo [citation:10]. **Conditional logic is where this shape wins**, but listing objects is the weak spot, requiring the query-planner API to produce a database filter [citation:10].  
**Best for:** Teams wanting conditional, context-aware authorization policies without moving permission data out of their primary store, particularly where listing is not a primary requirement.

### Paralus
**Stack:** Go | **License:** Apache-2.0 (CNCF Sandbox)  
Paralus is a free, open-source tool that enables controlled, audited access to Kubernetes infrastructure for users, user groups, and services, shipping as a GUI, API, and CLI [citation:12]. It integrates with pre-existing RBAC configuration and SSO providers (OIDC), providing just-in-time service account creation, fine-grained credential management, **dynamic and immediate changing/revoking of permissions**, and real-time audit logs [citation:12]. Custom roles, users, and groups can be created, with access controlled via pre-configured roles across clusters, namespaces, and projects [citation:12].  
**Best for:** Kubernetes teams wanting fine-grained, audited access control with dynamic permission revocation and SSO integration, accepting a Kubernetes-specific scope.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Role/Entitlement Mgmt | Approval Workflow | Authorization Model | Self-Hosted | Best For |
|----------|---------|-------|----------------------|-------------------|---------------------|-------------|----------|
| **Okta** | Proprietary | Cloud | ✅ Standard + custom | (Via workflows) | RBAC | ❌ | Enterprise IAM + scoped roles |
| **Entra ID** | Proprietary | Cloud | ✅ Built-in + custom | ✅ PIM | RBAC | ❌ | Microsoft ecosystem |
| **Apache Syncope** | Apache-2.0 | Java | ✅ Role + entitlement | ✅ Request/approval | RBAC | ✅ | Full IGA + approval workflows |
| **midPoint** | Open Source | Java | ✅ Role + entitlement | ✅ Request approval | RBAC + temporal | ✅ | Enterprise IGA governance |
| **OpenAM** | Open Source | Java | ✅ Entitlements | (Check) | RBAC/ABAC/script | ✅ | Access management + entitlements |
| **OpenRBAC** | Open Source | Spring Boot | ✅ Hierarchical groups | (Planned) | RBAC | ✅ | High-performance RBAC engine |
| **Keycloak** | Apache-2.0 | Java | ✅ Realm/client/composite | ❌ | RBAC + policy | ✅ | Proven IAM foundation |
| **Casbin** | Apache-2.0 | Multi-language | (Library) | ❌ | ACL/RBAC/ABAC | ✅ (Embed) | Embeddable authz |
| **OpenFGA** | Apache-2.0 | Go | (Relationship tuples) | ❌ | ReBAC (Zanzibar) | ✅ | CNCF relationship authz |
| **SpiceDB** | Apache-2.0 | Go | (Relationship tuples) | ❌ | ReBAC (Zanzibar) | ✅ | Highest scale + consistency |
| **Cerbos** | Apache-2.0 | Go | (Policy YAML) | ❌ | ABAC + RBAC | ✅ | Conditional policy decisions |
| **Paralus** | Apache-2.0 | Go | ✅ Custom roles | ❌ (Dynamic revoke) | RBAC (K8s) | ✅ | Kubernetes access control |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source RBAC or Entitlement Management tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem **splits sharply** between **full IGA platforms with native role/entitlement management and approval workflows** (Apache Syncope, Evolveum midPoint) and **authorization engines** (Keycloak, Casbin, OpenFGA, SpiceDB, Ory Keto, Cerbos) that answer "can X do Y on Z" but do **not** include entitlement lifecycle management or multi-admin approval. **Apache Syncope** and **midPoint** are the only open-source projects found with built-in request/approval workflows alongside role and entitlement management [citation:2]. For pure authorization decisions at scale, **OpenFGA** (CNCF-backed) and **SpiceDB** (highest consistency control) are the leading Zanzibar-inspired options [citation:10].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
