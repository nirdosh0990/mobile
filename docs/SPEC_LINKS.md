# Specification Links

This document maps features in this repository to their source specifications in the [specs repository](https://github.com/localstore-platform/specs).

**Spec Version:** [v1.1-specs](https://github.com/localstore-platform/specs/tree/v1.1-specs)

**Last Updated:** 2025-12-06

---

## How to Use This Document

1. When implementing a feature, find it in the table below
2. Click the spec link to view the authoritative specification
3. Use line number references to load only relevant sections
4. Follow the spec exactly for API contracts, schemas, and behaviors

---

## Core Specifications

### Architecture

- [Flutter Mobile App Spec](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/flutter-mobile-app-spec.md)
  - Complete app architecture (entire file - ~2500 lines)
  - Project structure (lines 100-300)
  - Feature specifications (lines 300-1800)
  - UI/UX guidelines (lines 1800-2200)
  - Performance optimization (lines 2200-2400)

- [API Specification](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/api-specification.md)
  - REST endpoints for mobile (lines 80-1200)
  - Authentication (lines 120-280)
  - Dashboard metrics (lines 500-750)

- [GraphQL Schema](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/graphql-schema.md)
  - Queries for dashboard (lines 400-600)
  - Real-time subscriptions (lines 800-900)

### Design

- [Wireframes & UX Flow](https://github.com/localstore-platform/specs/blob/v1.1-specs/design/wireframes-ux-flow.md)
  - Mobile owner dashboard (lines 400-800)
  - Onboarding flow (lines 50-150)

### Implementation

- [Sprint 1 Plan](https://github.com/localstore-platform/specs/blob/v1.1-specs/planning/sprint-1-implementation.md)
  - Mobile app tasks (Week 4-6)

---

## Cross-Cutting Concerns

### Localization

- [Communication Language Guidelines](https://github.com/localstore-platform/specs/blob/v1.1-specs/knowledge-base/communication-language-guidelines.md)
- [Glossary](https://github.com/localstore-platform/specs/blob/v1.1-specs/knowledge-base/glossary.md)
  - Vietnamese/English term translations
  - Standard terminology

### Market Context

- [Vietnam Market Strategy](https://github.com/localstore-platform/specs/blob/v1.1-specs/research/vietnam-market-strategy.md)
  - Mobile-first requirements
  - Payment integrations (MoMo, ZaloPay, VNPay)
  - Social platform integrations (Zalo, Facebook)

### Monitoring & Operations

- [Monitoring Runbook](https://github.com/localstore-platform/specs/blob/v1.1-specs/documentation/monitoring-runbook.md)
- [Launch Readiness Checklist](https://github.com/localstore-platform/specs/blob/v1.1-specs/documentation/LAUNCH-READINESS.md)

---

## Spec Update Protocol

When the specs repository releases a new version:

1. Review [SPEC_CHANGELOG.md](https://github.com/localstore-platform/specs/blob/master/SPEC_CHANGELOG.md)
2. Identify breaking changes affecting this repository
3. Update this file to reference new spec version
4. Implement required changes
5. Update repository version and tag release

---

## AI Context Loading

AI assistants should:

- Load specs **on-demand** using the links above
- Use line number ranges to minimize context
- Reference this spec version consistently
- Follow [AI Context Guide](https://github.com/localstore-platform/specs/blob/v1.1-specs/.github/AI_CONTEXT_GUIDE.md)

**Example:**

```text
semantic_search(
  repo: "https://github.com/localstore-platform/specs",
  query: "OTP authentication endpoint"
)
```

Then read specific sections:

```text
read_file(
  "architecture/api-specification.md",
  lines: 150-280
)
```
