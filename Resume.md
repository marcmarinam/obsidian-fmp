# Marc Marina Miravitlles

**Software Engineer** — Backend-leaning full-stack

Barcelona, Spain (Remote) · marc.marina.miravitlles@gmail.com · +34 648 439 648

---

## Summary

Backend-leaning full-stack engineer with ~5 years building and operating production Node.js/TypeScript services. I work end-to-end across GraphQL APIs, Kubernetes, and Prometheus/Grafana observability, and recently led the multi-brand rebuild of my team's platform. I do my best work on ambiguous, cross-team problems that need making reliable.

---

## Experience

### Software Engineer — Findmypast

_2021 – Present · Remote (Spain) from 2023; previously London, UK_

Joined as a Junior Engineer and grew into a mid-level engineer, owning platform-level work — first on E-Commerce, then on the Customer Engagement Platform (CEP).

- **Architected multi-brand support**, replacing brand-specific services with shared infrastructure and business logic — including migrating legacy account data with zero loss by temporarily extending the schema rather than dropping unmapped fields.
- **Led the rewrite of CEP into a Turborepo monorepo** — mobbed with the team to establish the pattern, then reviewed migrations for consistency across 10+ workspaces; used Knip for dead-code detection to keep the result lean.
- **Established production observability** — custom Prometheus histogram metrics, Grafana dashboards, and SLO tracking via histogram bucket ratios on Kubernetes, where no SLOs existed before.
- **Own the CRM and messaging integration (Iterable)**, driving user engagement through in-app messaging and email campaigns; added Zod-based schema validation to guard against Iterable's permissive JSON payloads. My main focus for the last two years.
- **Run a Snowplow Signals pipeline** (an early pilot deployment) building per-user behaviour profiles from site activity — driving targeted in-app and email nudges based on what each user actually engages with.
- **Operate services on Kubernetes** — found and fixed a deployment misconfiguration letting unhealthy releases register as "ready"; also HPA tuning, graceful shutdown, and Helm charts.
- **Build AI prototypes in the Innovation Guild** _(ongoing, periodic)_ — an AI summary generator over newspaper search results with OCR-linked source text, and a similar summarizer for scanned historical transcripts.
- _(Earlier tenure)_ Launched a subscriptions/micropayments platform and led the legacy migration (Kafka, Redis, external payment provider); later built an internal A/B testing framework adopted company-wide, using it to turn a hardcoded 14-day free trial into a dynamic, journey-based length — boosting conversion ~40% and hitting an all-time monthly record for trial starts.

_Stack: TypeScript, Node.js, GraphQL/Apollo, Kubernetes, Prometheus, Grafana, Kafka, Redis, Turborepo_

### Earlier experience

Full-stack web development at **GJQ Holdings** (Laravel, MySQL, Git; 2018–2019) and a cross-platform productivity app built on **Node/Express + MongoDB** with an Android client (2020).

---

## Skills

**Languages:** TypeScript, JavaScript, SQL **Backend & APIs:** Node.js, GraphQL (Apollo), REST, Kafka, Redis, PostgreSQL, MongoDB **Infrastructure & Observability:** Kubernetes, Docker, Helm, Prometheus, Grafana **Tooling:** Turborepo, Yarn, Knip, Git, CI/CD

---

## Self-Directed / Homelab

Run a Proxmox VE cluster hosting K3s with Prometheus/Grafana monitoring, Harbor, Tailscale, and Caddy — mirroring the production stack I work with professionally.

---

## Education

**BSc Software Engineering** (final year top-up) — London Metropolitan University (2019–2020) · First-Class **Multiplatform App Development** — Centre d'Estudis Politècnics, Barcelona (2017–2019)