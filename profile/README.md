# Forchetto

Multi-tenant restaurant management SaaS for independent restaurants, built by [BocoLabs](https://www.bocolabs.com).

> Source code is private. The architecture is outlined below; code walkthroughs are available on request.

## Architecture
- **Frontend:** Next.js (App Router), TypeScript, Tailwind CSS, shadcn/ui
- **Backend:** AWS serverless (Lambda, Aurora PostgreSQL, Cognito), infrastructure as code with CDK
- **Multi-tenancy:** tenant isolation enforced at the database level with PostgreSQL Row-Level Security
- **Access control:** 5 roles (owner, manager, waiter, cashier, kitchen) with per-route and per-action authorization
- **API layer:** type-safe API client and a BFF with HTTP-only cookies

## Engineering practices
- GitHub Actions CI with branch protection rulesets
- Secret scanning with gitleaks; dependency scanning with OSV-Scanner and Dependabot
- Git hooks, strict TypeScript and ESLint checks

## Status
In active development (backend integration phase).

[bocolabs.com](https://www.bocolabs.com) · [Case study](https://www.bocolabs.com/en/projects/forchetto-restaurant-saas)
