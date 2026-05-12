# ThreatPad 🛡️

> A desktop SOC incident notes tool built for analysts, by an analyst.

ThreatPad is a Python/tkinter application designed to reduce workflow friction during security incident investigations. It keeps your notes, IOC handling, and investigation checklists in one place — with zero cloud dependency and no telemetry.

---

## Features

### 📝 Multi-Tab Note Editor
- Open multiple incident notes simultaneously in separate tabs
- Tab colour coding for quick visual triage
- Session restore on relaunch
- Find and replace, line numbers, and syntax highlighting
- Performance-optimised for large documents (debounced highlighting, 100KB guard)

### 🔍 IOC Handling
- **Defang / Refang** — Safely neutralise or restore IPs, URLs, domains, and email addresses
- **Extract IOCs** — Pull indicators out of raw text in one click
- **Hashing & Encoding** — MD5, SHA1, SHA256, Base64 encode/decode built in

### 🚨 Client Contamination Detection
- Assign a client to each investigation tab
- Automatic cross-contamination detection prevents data from one client appearing in another's notes
- Safe Copy blocks clipboard output if contamination is detected, with a clear warning

### ✅ Training Wheels Mode
- Guided SOC checklists for 15+ incident types (phishing, malware, ransomware, account compromise, and more)
- Microsoft Sentinel and Defender alert checklists built in
- Step-by-step prompts to ensure nothing gets missed

### ⚡ Productivity Tools
- **Copy Pasta** — Reusable snippet library for common analyst responses and templates
- **Templates** — Pre-built note structures for standard incident types
- **Incident Timers** — Track time spent per investigation
- **Action Log** — Automatic log of analyst actions taken during a session

### 🆘 Oh Sh*t Mode (Break Glass)
- Emergency review panel for rapid situational awareness
- Surfaces all open tab content and key context in one view

### 🎨 Customisation
- Dark mode
- Font and theme customisation
- Adjustable layout preferences

---

## Tech Stack

| Component | Detail |
|-----------|--------|
| Language | Python 3 |
| GUI | tkinter |
| Storage | Local only — no cloud, no telemetry |
| Platform | Windows (primary) |

---

## Getting Started

1. Clone or download the repository
2. Ensure Python 3 is installed
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run ThreatPad:
   ```bash
   python threatpad.py
   ```

---

## Usage Notes

- **Client selector** — Always set the correct client before writing notes to enable contamination protection
- **Safe Copy** — Use Safe Copy (not Ctrl+C) when copying IOC data to ensure defanging is applied and contamination is checked
- **Training Wheels** — Enable via the View menu; select an incident type to load the relevant checklist
- **Tabs** — Right-click a tab for colour coding options

---

## Roadmap

- [ ] IOC enrichment integrations (VirusTotal, AbuseIPDB)
- [ ] Export to PDF / DOCX
- [ ] Configurable checklist editor
- [ ] Keyboard shortcut reference panel

---

## About

ThreatPad was built to solve real-world friction in L1/L2 SOC work — note-taking scattered across tools, IOC defanging done manually, and the constant risk of mixing client data in a multi-tenant environment. It's a personal tool built for practical use, not a product.

---

*Built with Python. Runs locally. No nonsense.*
