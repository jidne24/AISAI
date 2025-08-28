# AISAI — Automated IP-Secured Attendance Intelligence

[![Project Status](https://img.shields.io/badge/status-proof%20of%20concept-blue)](https://github.com/yourusername/AISAI)
[![Tech: Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)
[![Framework: Flask](https://img.shields.io/badge/Flask-▲-black)](https://flask.palletsprojects.com/)
[![DB: SQLite3](https://img.shields.io/badge/SQLite3-lightgrey)](https://www.sqlite.org/)

---

## Quick demo
![demo](assets/demo.gif)

---

## One-line summary
IP-based attendance verification for controlled Wi-Fi networks — fast, reliable, automated.

---

## Project overview
Automated IP-Secured Attendance Intelligence (AISAI) prevents proxy attendance and removes manual record-keeping overhead by validating one submission per device (IP) inside a controlled Wi-Fi network. Teachers create short, configurable attendance sessions; students submit a registration number from their devices; AISAI validates by IP, aggregates results, computes attendance, and stores semester records securely.

---

## Key goals
- 🔒 Eliminate proxy attendance via IP validation (one submission per device)  
- ⚡ Automated marking and calculations for immediate results  
- 📊 Intuitive dashboards for teachers and students  
- 💾 Secure semester-long storage (SQLite3)  
- 📈 Exportable, accreditation-ready reports

---

## Features
- Teacher admin dashboard: start/stop sessions, session duration control, live monitoring.  
- Student submission UI: fast single-field submission with live status.  
- IP-based validation to avoid duplicate submissions in controlled Wi-Fi.  
- Automated aggregation & grade calculation (triggered post-session).  
- Export CSV / Excel reports and semester archives.

---

## How it works (high level)
1. Teacher starts an attendance session (configurable window, e.g., 15–20 sec).  
2. Students on the same controlled Wi-Fi open the client page and submit their registration number.  
3. Server captures the requester IP and accepts a single valid submission per IP.  
4. Post session, a command/process aggregates results, computes attendance, and appends records to an SQLite database.  
5. Teachers download reports or view analytics on the dashboard.

---

## System architecture
**Modules**
- **Server (Python + Flask):** session control, IP validation, DB ops  
- **Client (Flask templates):** student submission interface  
- **Admin dashboard:** start sessions, monitor, and export

_Add architecture diagram: `assets/arch-diagram.png`_

---

## Tech stack
- Python (Flask)  
- SQLite3  
- socket & threading (for local networking logic)  
- pandas (data processing)  
- Simple templated frontend (HTML/CSS + Flask Jinja)

---

## Security & privacy
- IP-based validation works **only** within a controlled campus Wi-Fi environment.  
- Student identifiers are stored securely in a local SQLite database for the semester.  
- For privacy and startup protection, the source code is **not public** in this repository.  
- **Source code is available on request** under NDA for collaborators or evaluators (see `RELEASES.md`).

---

## What you can view in this repo
- Visual demo (`assets/demo.gif`)  
- Architectural diagrams and screenshots (`assets/`)  
- Slides and project documentation (`SLIDES.md`, `ABOUT.md`)  
- Project goals, design decisions, security model and exportable reports examples

---

## Slide highlights / presentation
See `SLIDES.md` for the full slide deck content. (A PDF copy is available in Releases.)

---

## For recruiters & evaluators
If you'd like to evaluate the codebase, a compiled demo, or collaborate:
- Email: **jidnehuda24@gmail.com**  
- LinkedIn: **https://www.linkedin.com/in/jidne24**  
Source review is available under NDA — please reference "AISAI source access" in your message.

---

## License
This repo contains documentation, diagrams and demo media. The project design is licensed under the MIT License — see `LICENSE` for details.

---

## Credits
Project created by **Gidne Huda** — third year student, passionate about applied networking & educational solutions.
