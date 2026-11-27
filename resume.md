# Mohamed Abbas Ali

I write software for engineering and manufacturing, and I lead the teams that build it.

Chennai, India · [abbazs@gmail.com](mailto:abbazs@gmail.com)

I studied mechanical engineering, started as a CAD designer in 1999, and soon moved to writing software for engineers. At QuEST Global I built design-automation software for turbomachinery makers, mostly General Electric and Hitachi, and later ran those programs. At Caresoft I was General Manager of Operations. The tools my teams built there saved more than 20,000 hours a year, and my simulation work won a Ford Manufacturing Leadership Award.

At Cadonix I was the first engineer on smartBuild, a manufacturing execution system. I started it in an empty repository and grew it to seven services in production, more than 70 releases and a team of eight. I was Head of Engineering and I still wrote the code, and AI tools became a normal part of how my team worked. Since August 2026 I've been at Onward Technologies, building proofs of concept that use AI for engineering R&D work.

## Experience

### Onward Technologies
*Aug 2026 – now, Chennai · Joined as Solution Architect*

I look for places where AI can speed up engineering R&D work, then build a working proof of concept to find out whether the idea holds up.

- Built a proof of concept that checks Certificates of Analysis and Certificates of Conformance (CoA/CoC) automatically. Certificates arrive as PDFs, images or emails. It reads them and checks each value against the ERP, the PLM, the engineering drawings and other systems of record. Until now, people did this cross-checking by hand.

### Cadonix
*Apr 2022 – Jul 2026, Chennai · Head of Engineering*

I was the first engineer on smartBuild, a manufacturing execution system for formboard assembly and production tracking. I started it from an empty repository in 2023, and it grew to seven services running in production in the cloud. I was responsible for the backend, database, cloud, deployment, security, monitoring and AI features, and I led a team of 8+ engineers across backend, frontend and QA automation.

- **How it is built.** 17 repositories of Python and TypeScript. A FastAPI backend on EdgeDB, organised by business domain, with Celery workers, an MQTT service that controls the stations, a central log service, a Nuxt 3 frontend and an Nginx router in front.
- **Security.** I moved 15+ domains to EdgeDB's per-customer isolation, so one customer can no longer reach another customer's data by changing an ID in a request (IDOR bugs). I also designed the login system: JWT with multiple sessions and token revocation, a forced re-login when someone gets more permissions, HSTS, and rate limiting at the WAF.
- **Cloud.** I wrote and ran all of the AWS infrastructure myself, in Pulumi: EC2, IAM with minimal permissions, S3, load balancers, WAF, RDS and ElastiCache, for development, staging and production. Developers could run the whole system on their own machine in 7 Docker containers set up like production, with nothing mocked.
- **Releases.** 70+ versioned releases, each moving from feature branch to dev, staging and then production. I wrote the CI/CD pipeline for every service, and a Python command-line tool that handles git, starting and stopping services, releases and database tasks across all 17 repositories.
- **AI features.** An LLM analyses build sequences and streams its answer to the browser over SSE, through Valkey pub/sub, with prompt history, checks that keep questions on topic, and token-cost tracking. I also built an AI agent that reviews merge requests. It can dig through the code over several turns, switches to another model if one fails, and runs from the release tool.
- **Factory floor.** I led the MQTT service that talks to the machines on the shop floor in real time. I gave the station screens their own separate JWT login, and fixed the WebSocket reconnect bugs that broke station pairing.
- **Logs and alerts.** Each service used to log through its own queue. I replaced that with one log service: services send logs to it over HTTP, it sorts them, and alerts go to Slack or email. I kept an incident log and wrote playbooks for the alerts.

**Commits per month.** The team size didn't change. We started using AI coding tools in our daily work in mid-2025.

| 2023 (May–Dec) | 2024 | 2025 | 2026 (Jan–Apr) |
|---:|---:|---:|---:|
| ~56 | ~34 | ~388 | ~650 |

Before smartBuild:

- Wiring-harness testing over IoT: ESP32 devices on the production line send results to the server over MQTT, with live production numbers.
- Planned how to split a wiring-harness system, one large application in Lua, MySQL and JavaScript, into separate services.

### Caresoft Global
*Sep 2014 – Mar 2022, Pollachi and Chennai · General Manager, Operations (2022) · Deputy General Manager, Operations (2017) · Senior Manager (2014)*

I ran the operation that automated the hardest parts of automotive benchmarking: collecting the data, cleaning it, and moving it between versions. The tools my teams built saved more than 20,000 hours a year.

- We built manufacturing simulation tools, including one that builds plant simulation models from structured data, so nobody has to build them by hand. My part in a symbiotic-simulation program won a 2020 Manufacturing Leadership Award ([announcement](https://www.at.ford.com/en/homepage/news-and-clipsheet/news/2020/6/leadership-awards.html)).
- I came up with new benchmarking methods, such as rebuilding CAD models of vehicle parts from CT scans. We also automated analysis on full-vehicle CAD data, for example adding up the excess bolt length and weight across a whole truck.
- We built the internal software the business ran on: project-tracking apps and dashboards, a tool for labelling machine-learning training data, and tools that pull structured data out of CAD drawings.

### QuEST Global
*Jun 2001 – Aug 2014, Bangalore · Program Manager (2013) · Project Manager (2008) · Subject Matter Specialist (2006) · Technical Leader (2004) · Project Engineer (2001)*

Thirteen years writing engineering-automation software for turbomachinery and aerospace companies, mostly General Electric and Hitachi. I started by writing the automation myself and ended up leading the teams and programs that delivered it.

- We built knowledge-based engineering systems that produce the 3D models and manufacturing drawings for centrifugal compressors and steam turbines (impellers, casings, diaphragms and forgings) straight from the aerodynamic flow path, the design rules and the machining data. Before that, engineers modelled and drew all of it by hand.
- We automated inspection and analysis work on aircraft engines and power-generation equipment, for example generating eddy-current scan plans for engine rotor discs, and tracing temperature-probe sight lines on gas-turbine blades against FEM results.
- I went on site to work out the scope with customers' engineering teams, split each program so a prototype proved the idea first, and wrote the estimates that won the follow-on programs. The goal was to cut the time from order to delivery.
- We also built smaller tools for engineers, from editing blade geometry to generating maintenance checklists from a component's configuration.

### TCS
*Oct 1999 – Jun 2001, Chennai · CAD Designer*

## Open source

Small tools I wrote for my own work with AI.

- **[xcat](https://github.com/abbazs/xcat)** (Rust). One command that does tree, cat and copy-to-clipboard, so I can paste a whole codebase into an LLM. Prebuilt binaries for Linux, macOS and Windows.
- **[pyxclip](https://github.com/abbazs/pyxclip)** (Rust, PyO3). A Python clipboard library that works on every platform without installing anything else. Copies text, images and file paths.
- **[rich-stepper](https://github.com/abbazs/rich-stepper)** (Python). A step-by-step progress display for the terminal, built on Rich. I use it in the merge-request review agent.

## Tools I work with

- **Languages:** Python, TypeScript, Rust, JavaScript, C#, C, C++, Java
- **Backend:** FastAPI, Pydantic, Celery, Django, Flask
- **Frontend:** Nuxt 3, Vue 3, D3.js, WPF
- **Data:** EdgeDB / Gel, PostgreSQL, MySQL, MSSQL, SQLite, SQLAlchemy, pandas, NumPy
- **Cloud and infrastructure:** AWS (EC2, S3, ALB, NLB, WAF, IAM, RDS, ElastiCache), Pulumi, Docker, Nginx
- **Messaging and real time:** RabbitMQ / Amazon MQ, MQTT, Valkey, SSE, WebSockets, ESP32
- **Delivery and quality:** GitLab CI, GitHub Actions, pytest, pytest-bdd, Playwright
- **AI:** LLM APIs, streaming responses, writing prompts, code-review agents, AI coding tools
- **CAD and simulation:** Siemens NX / Unigraphics (UFUNC, NXOpen, Knowledge Fusion), SolidWorks API, Pro/TOOLKIT, Witness (SIMBA)

## Education

- **BS in Data Science and Applications**, IIT Madras. 2022 – in progress. Diploma in Programming completed.
- **Diploma in Mechanical Engineering**, 1995 – 1998.

## Recognition

- **Manufacturing Leadership Award**, Ford, 2020. For my contribution to the Symbiotic Simulation project.
- **Leadership courses.** Coaching and mentoring, negotiation, and contracting in Transactional Analysis (Navgati); Curriculum for Living (Landmark Education).

## Contact

[abbazs@gmail.com](mailto:abbazs@gmail.com) · [22f2000997@ds.study.iitm.ac.in](mailto:22f2000997@ds.study.iitm.ac.in)

*Updated November 2026.*
