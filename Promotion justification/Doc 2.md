**1. Technical Leadership** _You can lead confidently in tackling some of the most complex or challenging technical problems faced by your team, from design and planning to implementation._

- CEP Gate rewrite — identified severe maintainability and architectural problems in the existing codebase, wrote the proposal, led the technical design, drove alignment with the team (including convincing a dissenting senior), and led the implementation with a small team
- Consolidation of subservices in CEP Data Processor — proposed and led the merging of multiple independently deployed iterator apps into a unified service, reducing operational complexity and making troubleshooting easier

---

**2. Ownership Promotion** _You actively promote ownership of tools, systems, and processes within your team._

- Improved metrics collection for shared logic across apps, making it easier to observe external request data across the entire system
- Significantly improved monorepo quality by introducing clear boundaries between apps and packages, and adopted Turborepo to make management faster and less error-prone
- Introduced dead code detection tooling (Knip) to surface and reduce tech debt across the codebase
- Owned the deployment process — audited old and new services and configured Kubernetes deployment strategies to enable automatic rollbacks and prevent bad deploys reaching production
- Proposed removing a set of internal packages in favour of leaner, purpose-built tooling during the CEP rewrite

---

**3. Long-term Thinking** _You look beyond short-term deliverables, helping the team manage their long-term responsibilities._

- Shortly after joining the CEP codebase, identified deep-rooted tech debt and architectural problems and proposed the full rewrite rather than accumulating more incremental fixes
- Performed independent refactors to ease the transition to multi-brand support ahead of it becoming urgent
- Had significant input in planning both the CEP rewrite roadmap and the BNA migration plan
- Invested in the team's long-term capability by developing junior engineers to the point of promotion, strengthening the team beyond immediate deliverables

---

**4. Business Alignment** _You work with others to influence and shape planned work and ensure it's aligned with business priorities._

- Led the technical design and implementation of CEP Gate's BNA (British Newspaper Archive) integration — the largest company-wide objective in recent years — while surfacing and managing risks throughout
- Worked proactively with other teams to ensure our systems exposed what they needed to meet their own objectives, gathering requirements and planning the work. Prepared user-profile to enable multi-brand support for other features in the site.

---

**5. Cross-team Collaboration** _You seek out areas of overlap with other projects/teams and work across boundaries to ensure plans are aligned._

- Drove the user profile migration to global member ID — coordinated across teams to add multi-brand user identification (FMP + BNA), represented the team in cross-team discussions, and surfaced and resolved blockers
- Ensured a smooth transition by adding extensive instrumentation during the migration
- Gathered requirements from other teams needing new fields or inputs and planned and delivered the work accordingly

---

**6. Knowledge Sharing** _You help others to deliver more value by sharing your expertise in certain technologies and processes._

- Converted the internal tools repository into a proper monorepo, ran a walkthrough for the team, explained decisions in PR reviews, and remained the go-to person for questions
- Regularly shared knowledge in planning meetings and pairing/mobbing sessions, particularly in areas teammates were less familiar with
- Primary team expert in monorepo tooling (Turborepo/Yarn PnP), Kubernetes deployments, and Prometheus/Grafana observability — knowledge reinforced by running a personal homelab K8s cluster
- Acted as a long-running source of knowledge for less-experienced engineers, sustaining their development over months rather than answering isolated questions

---

**7. Trusted Influence** _You are a trusted influencer within your team and regularly use this position to positively impact the team._

- Regularly sought out by teammates and seniors for opinions on technical decisions, architecture, and tooling
- Successfully challenged a senior's preference for incremental CEP updates, argued for a full rewrite, and brought the whole team around to that position
- Proposed the embedded messages architecture that front-loaded engineering work but eliminated ongoing CRM setup overhead, with full content flexibility and Zod validation to ensure campaigns run as intended
- Championed Turborepo as the monorepo tool — introduced it, demonstrated prior examples, and the team adopted it successfully

---

**8. Growth & Mentorship** _You are supporting the growth and development of your team, and individuals inside or outside your team._

- Mentored more than one junior engineer from the point they joined the company through to their promotion, supporting their growth over an extended period rather than through one-off help
- Helped a mid-level engineer deepen their understanding across a wide range of concepts — showing I can mentor and grow peers at my own level, not only those more junior than me
- Regularly supported peers working in unfamiliar areas through pairing and mobbing sessions, explaining concepts on demand, and unblocking them when stuck

---

**9. Quality Evangelism** _You are an evangelist for consistent high-quality and efficient delivery within your team._

- Pushed for leaner, more focused testing — proposed testing independent layers rather than full stack logic, resulting in faster and easier-to-debug test suites in the new CEP
- Introduced and enforced code quality tooling including linting, strict TypeScript, and Knip for dead code detection
- Conducts thorough code reviews focused on catching bugs, maintaining consistency, and explaining reasoning — without being a blocker
- Configured Kubernetes deployment strategies to protect production and integration environments from bad deploys
- Caught multiple bugs in review, particularly around server setup and route handling

---

**10. Engineering Excellence** _You can independently design and develop clean, durable engineering solutions._

- Designed and built an in-house message dismissal system to replace Iterable's inadequate handling — the solution worked well and was subsequently adopted in additional areas
- Designed the BNA communications preferences backend and frontend — the first multi-brand comms preference implementation, requiring brand-aware option resolution and correct rendering per brand
- Proposed and implemented the embedded messages architecture — more upfront engineering investment, but eliminated ongoing CRM campaign setup and provided full content flexibility with validation

---

**11. Evaluation & Prototyping** _You can confidently evaluate and prototype new approaches, technologies and platforms, promoting strong and informed decision-making._

- Proposed and validated the monorepo approach using Turborepo, drawing on prior experience building monorepos with it both inside and outside the company — demonstrated working examples to build team confidence before committing
- Evaluated and discarded a set of existing internal packages in favour of leaner alternatives during the CEP rewrite, reducing unnecessary dependencies