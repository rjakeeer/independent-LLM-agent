# 🛡️ Independent LLM Security Agent (`independent-LLM-agent`)

![License: MIT](https://shields.io)
![Protocol: MCP](https://shields.io)
![Python: 3.11+](https://shields.io)
![Docker: Sandbox](https://shields.io)
![Status: Phase 1 - Local](https://shields.io)

---

### 🌐 Overview / Описание / Beschreibung

* **EN:** An independent, privacy-first AI security agent powered by uncensored open-weight LLMs. Designed to run in isolated environments via encrypted tunnels, utilizing the Model Context Protocol (MCP) for automated vulnerability analysis, PoC verification, and secure code patching.
* **RU:** Независимый ИИ-агент для кибербезопасности с приоритетом на приватность, работающий на базе открытых языковых моделей без цензуры. Разработан для запуска в изолированных средах через зашифрованные туннели с использованием протокола MCP для автоматического анализа уязвимостей, проверки PoC и генерации безопасных патчей.
* **DE:** Ein unabhängiger, datenschutzorientierter KI-Sicherheitsagent auf Basis unzensierter Open-Weight-LLMs. Entwickelt für den Betrieb in isolierten Umgebungen über verschlüsselte Tunnel unter Verwendung des Model Context Protocols (MCP) zur automatisierten Schwachstellenanalyse, PoC-Verifizierung und Erstellung sicherer Code-Patches.

---

### ⚠️ Legal Disclaimer / Отказ от ответственности

> **ENGLISH:** This project is developed strictly for educational purposes, security research, and authorized penetration testing (AppSec/DevSecOps). The author does not condone or support any illegal activities. You may only use this tool against systems, networks, and applications that you own or have explicit written permission to test. The author assumes no liability and is not responsible for any misuse or damage caused by this software.
>
> **РУССКИЙ:** Данный проект создан исключительно в образовательных целях, для исследований в области информационной безопасности и авторизованного тестирования на проникновение (AppSec/DevSecOps). Автор не поощряет и не поддерживает любую незаконную деятельность. Вы можете использовать данный инструмент только в отношении систем, сетей и приложений, которыми владеете лично или на тестирование которых имеете явное письменное разрешение. Автор не несет никакой ответственности за неправомерное использование или любой ущерб, причиненный данным ПО.

---

### 🗺️ Project Roadmap

#### Phase 1: Local Sandbox & Lightweight Agent (Current Stage)
The primary goal of the first stage is to build and validate the entire autonomous agent pipeline **100% locally** on a standard workstation using a compact uncensored model before scaling to remote GPU infrastructure.

* **Core Stack & Tools:**
  * **Inference Engine:** Ollama (local API endpoint)
  * **LLM:** Lightweight uncensored / abliterated model (`Bonsai-2 Uncensored 9B` or `Qwen-Coder-7B-abliterated`)
  * **Agent Framework:** Cline / Roo Code (VS Code)
  * **Custom MCP Servers (Python / `FastMCP`):**
    * `recon_server.py` — automated port scanning (`nmap`) and HTTP header inspection.
    * `filesystem / git_server` — autonomous file creation and repository reporting.
  * **Target Environment:** Isolated vulnerable web application running locally in Docker (e.g., DVWA / custom vulnerable Flask app).

* **Phase 1 Milestones & Deliverables:**
  * [ ] Deploy the lightweight uncensored LLM locally and verify zero censorship refusals on security research queries.
  * [ ] Connect custom Python MCP tools to the agent and spin up the local Docker target sandbox.
  * [ ] Execute an automated penetration test against the local testbed and generate a working PoC exploit.
  * [ ] **Autonomous Reporting:** Have the agent automatically generate a structured Markdown vulnerability report (including the PoC and remediation patch) and commit/save the file directly into this repository.

---

*(Phase 2: Migration to an isolated GPU VPS over an encrypted WireGuard/Tailscale tunnel with a full-scale 27B–32B model — coming soon).*
