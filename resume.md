# Mohamed Abbas Ali

I build engineering and manufacturing software, and the teams that ship it.

Chennai, India · [abbazs@gmail.com](mailto:abbazs@gmail.com)

Since 1999 I've worked where engineering meets code. At QuEST Global I built design-automation systems for turbomachinery OEMs, chiefly General Electric and Hitachi, and went on to run those programs. At Caresoft, as General Manager of Operations, my teams' tools saved over 20,000 hours a year, and my simulation work earned a Ford Manufacturing Leadership Award.

At Cadonix I was founding engineer and Head of Engineering of smartBuild, a manufacturing execution system I took from an empty repository to seven production services, more than 70 releases and a team of eight. I still write the code, and I build AI into how my teams work. At Onward Technologies I now design AI platforms that speed up engineering R&D services.

## Experience

### Onward Technologies
*Aug 2026 – now, Chennai · Joined as Solution Architect*

I shape and prove concepts for platforms that use AI to speed up engineering R&D services, taking each idea from a problem statement to a working proof of concept.

- Built a proof of concept that automatically validates Certificates of Analysis and Certificates of Conformance (CoA/CoC). It gathers certificates however they arrive, as PDFs, images or emails, extracts their contents, and verifies each value against the systems of record: ERP, PLM, engineering drawings and more. This replaces manual cross-checking.

### Cadonix
*Apr 2022 – Jul 2026, Chennai · Head of Engineering*

Founding engineer of smartBuild, a manufacturing execution system for industrial formboard assembly and production tracking. I built it from an empty repository in 2023 to seven cloud-deployed services in production, and owned the backend, database, cloud infrastructure, DevOps, security, observability and AI features. I led 8+ engineers across backend, frontend and QA automation.

- **Architecture.** 17-repository Python/TypeScript platform: FastAPI and EdgeDB backend with domain-driven design, Celery workers, an MQTT station-control service, a centralized log service, a Nuxt 3 frontend and an Nginx router.
- **Security.** Led the platform-wide move of 15+ domains to EdgeDB global customer isolation, removing a whole class of IDOR vulnerabilities. Designed JWT multi-session auth with JTI revocation, forced re-authentication on permission escalation, HSTS, and WAF rate limiting.
- **Cloud infrastructure.** Sole owner of all AWS infrastructure in Pulumi (EC2, least-privilege IAM, S3, ALB, NLB, WAF, RDS, ElastiCache) across development, staging and production. Built a local environment of 7 Docker containers that mirrors production with no mocked infrastructure.
- **Delivery.** Shipped 70+ semantic-versioned releases through feature → dev → staging → production promotion. Wrote the CI/CD pipeline for every service and a Python CLI that runs git workflows, service lifecycle, releases and database operations across all 17 repositories.
- **AI in the product and the process.** Built SSE streaming endpoints for LLM-driven build-sequence analysis using Valkey pub/sub, with prompt history, scope enforcement and token-cost tracking. Built an AI merge-request review agent with multi-turn investigation and multi-model fallback, wired into the release CLI.
- **Factory floor.** Led the real-time MQTT station-control service that talks to manufacturing hardware. Designed a separate JWT security domain for station viewports and fixed WebSocket reconnect-pairing incidents.
- **Observability.** Replaced per-service queue logging with a centralized log service that has HTTP ingestion, structured routing and Slack/email alerting. Kept an incident log and alert playbooks.

**Delivery rate, commits per month.** Same team size throughout. AI-assisted engineering became part of our workflow in mid-2025.

| 2023 (May–Dec) | 2024 | 2025 | 2026 (Jan–Apr) |
|---:|---:|---:|---:|
| ~56 | ~34 | ~388 | ~650 |

Before smartBuild:

- IoT wiring-harness testing: ESP32 devices on the production line report to the server over an MQTT broker, with live production metrics.
- Planned the migration of a Lua, MySQL and JavaScript wiring-harness monolith to microservices.

### Caresoft Global
*Sep 2014 – Mar 2022, Pollachi and Chennai · General Manager, Operations (2022) · Deputy General Manager, Operations (2017) · Senior Manager (2014)*

I ran the operation that automated the hardest parts of automotive benchmarking, from data acquisition through data cleaning to migrating data between versions. The tools my teams built saved more than 20,000 hours a year.

- We built manufacturing simulation tooling, including a system that generates plant simulation models from structured data instead of building them by hand. My contribution to a symbiotic-simulation program earned a 2020 Manufacturing Leadership Award ([announcement](https://www.at.ford.com/en/homepage/news-and-clipsheet/news/2020/6/leadership-awards.html)).
- I defined new benchmarking processes, such as reconstructing CAD models of vehicle components from CT scans, and we automated analysis on full-vehicle CAD data, such as totalling excess bolt length and weight across a truck assembly.
- We built the internal software the business ran on: project-management applications and dashboards, a labelling tool for machine-learning training data, and extraction of structured data from unstructured CAD drawings.

### QuEST Global
*Jun 2001 – Aug 2014, Bangalore · Program Manager (2013) · Project Manager (2008) · Subject Matter Specialist (2006) · Technical Leader (2004) · Project Engineer (2001)*

Thirteen years building engineering-automation software for turbomachinery and aerospace OEMs, chiefly General Electric and Hitachi. I grew from writing the automation myself to leading the teams and programs that delivered it.

- We built knowledge-based engineering systems that generate production 3D models and manufacturing drawings for centrifugal compressors and steam turbines, covering impellers, casings, diaphragms and forgings, directly from aerodynamic flow paths, design rules and machining data, replacing manual modelling and drafting.
- We automated inspection and analysis work on aerospace and power-generation hardware, such as generating eddy-current scan plans for aircraft-engine rotor discs and tracing temperature-probe sight lines on gas-turbine blades against FEM results.
- I led on-site scoping with customer engineering departments, phased each program to prove a prototype first, and wrote the estimates that won follow-on automation programs aimed at shortening order-to-delivery time.
- We also built supporting tools for engineers, from blade-geometry editing to generating maintenance checklists from component configurations.

### TCS
*Oct 1999 – Jun 2001, Chennai · CAD Designer*

## Open source

Tools I built for my own AI-assisted workflow.

- **[xcat](https://github.com/abbazs/xcat)** (Rust). A tree, cat and clipboard tool in one CLI, for feeding codebases into LLM context windows. Prebuilt binaries for Linux, macOS and Windows.
- **[pyxclip](https://github.com/abbazs/pyxclip)** (Rust, PyO3). Cross-platform Python clipboard library with no system dependencies. Handles text, RGBA images and file paths.
- **[rich-stepper](https://github.com/abbazs/rich-stepper)** (Python). Multi-step terminal progress widget for Rich, used in the AI merge-request review agent.

## Tools I work with

- **Languages:** Python, TypeScript, Rust, JavaScript, C#, C, C++, Java
- **Backend:** FastAPI, Pydantic, Celery, Django, Flask
- **Frontend:** Nuxt 3, Vue 3, D3.js, WPF
- **Data:** EdgeDB / Gel, PostgreSQL, MySQL, MSSQL, SQLite, SQLAlchemy, pandas, NumPy
- **Cloud and infrastructure:** AWS (EC2, S3, ALB, NLB, WAF, IAM, RDS, ElastiCache), Pulumi, Docker, Nginx
- **Messaging and real time:** RabbitMQ / Amazon MQ, MQTT, Valkey, SSE, WebSockets, ESP32
- **Delivery and quality:** GitLab CI, GitHub Actions, pytest, pytest-bdd, Playwright
- **AI engineering:** LLM APIs, streaming, prompt design, AI code-review agents, AI-assisted development
- **CAD and simulation:** Siemens NX / Unigraphics (UFUNC, NXOpen, Knowledge Fusion), SolidWorks API, Pro/TOOLKIT, Witness (SIMBA)

## Education

- **BS in Data Science and Applications**, IIT Madras. 2022 – in progress. Diploma in Programming completed.
- **Diploma in Mechanical Engineering**, 1995 – 1998.

## Recognition

- **Manufacturing Leadership Award**, Ford, 2020. For contribution to the Symbiotic Simulation project.
- **Leadership courses.** Coaching and mentoring, negotiation, and contracting in Transactional Analysis (Navgati); Curriculum for Living (Landmark Education).

## Contact

[abbazs@gmail.com](mailto:abbazs@gmail.com) · [22f2000997@ds.study.iitm.ac.in](mailto:22f2000997@ds.study.iitm.ac.in)

*Updated November 2026.*
