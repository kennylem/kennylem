<p align="center">
  <img src="assets/banner.svg" alt="Leme, systems physician in training. I read systems the way a doctor reads a patient: symptoms, evidence, diagnosis, cure, prevention." width="100%">
</p>

<p align="center">
  <a href="https://YOUR-PORTFOLIO-URL"><img src="assets/btn-portfolio.svg" alt="Interactive portfolio" height="48"></a>
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN"><img src="assets/btn-linkedin.svg" alt="LinkedIn" height="48"></a>
  <a href="mailto:cklementinewa@gmail.com"><img src="assets/btn-email.svg" alt="Email" height="48"></a>
</p>

<p align="center">
  <img src="assets/about.svg" alt="Case file: Leme, incident diagnosis and reliability, mechanical engineering and numerical modeling, fintech and trading systems" width="100%">
</p>

## 🩺 How I think about incidents

I treat every incident like a clinical case. I don't just want to fix the symptom: I want to understand the system well enough to find the **root cause**, and make sure it doesn't happen again.

<p align="center">
  <img src="assets/method.svg" alt="Symptoms, Investigation, Diagnosis, Treatment, Prevention" width="100%">
</p>

### 🗂️ Pick a case file *(click to open)*

<sub>Illustrative cases showing how I reason. My real write-ups live in the lab below.</sub>

<details>
<summary><b>Case 01 · The app got slow after a deploy</b></summary>

<br>

- **Symptoms:** p99 latency doubled since the release; users report timeouts.
- **Investigation:** compare metrics before and after the deploy, read the logs of slow requests, check CPU, database and network.
- **Diagnosis:** one new query scans a whole table; `EXPLAIN` confirms a missing index.
- **Treatment:** add the index (or roll back), watch latency recover, tell the team.
- **Prevention:** latency SLO alert, query review in the release checklist, a short runbook.

</details>

<details>
<summary><b>Case 02 · Random 503 errors</b></summary>

<br>

- **Symptoms:** a healthy service throws 503s in short bursts.
- **Investigation:** line up the bursts with connection metrics, restarts and upstream logs.
- **Diagnosis:** the connection pool is exhausted whenever a batch job runs.
- **Treatment:** cap the job's concurrency, raise the pool size, confirm the bursts stop.
- **Prevention:** pool-saturation dashboard and alert; batch schedule documented.

</details>

<details>
<summary><b>Case 03 · Disk full at 3 a.m.</b></summary>

<br>

- **Symptoms:** writes fail, the pager goes off at night.
- **Investigation:** find which directories grew; check log rotation and recent changes.
- **Diagnosis:** debug logging left on, rotation never configured.
- **Treatment:** free space safely, enable rotation, restore the service.
- **Prevention:** disk alert at 80%, rotation in the base config, a post-incident note.

</details>

## 🧪 The lab

**[incident-diagnostics-lab](https://github.com/kennylem/incident-diagnostics-lab)**: I deliberately create production-like incidents and diagnose them from **logs, metrics, and system behavior**.

<p align="center">
  <img src="assets/pulse.svg" alt="" width="100%">
</p>

## 🧰 The toolbox

<p align="center">
  <img src="assets/toolbox.svg" alt="Toolbox: Python, SQL, Bash, MATLAB; Logs, Grafana, Splunk; Linux, networking, REST APIs, Git; RAG, LangChain, LangGraph, Ollama; data analysis, CFD, numerical modeling" width="100%">
</p>

## 🌱 Currently learning

**Google SRE fundamentals** (SLIs, SLOs, error budgets, incident management), alongside Linux, networking, Python and SQL.

## 💬 Let's talk about

Incident diagnosis · Root cause analysis · Debugging · Logs · System reliability
