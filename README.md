# SmishShield 2.0 — Multilingual Smishing Defense Platform
> **Smart India Hackathon (SIH 2026) Prototype**

An India-first, privacy-preserving cybersecurity defense engine designed to detect and counter multilingual SMS phishing (smishing), fake TRAI DLT sender headers, malicious APK payloads, and high-pressure financial coercion across Indian telecom networks.

---

## 🌟 Key Capabilities

1. **TRAI DLT 2.0 Header Validator**:
   - Inspects standard commercial enterprise SMS headers (`[Circle][Carrier]-[Brand]`, e.g., `AD-HDFCBK`, `VK-SBINB`).
   - Flags 10-digit mobile SIM spoofs (`+91-98...`) and international VoIP gateway headers pretending to represent banks or utilities.

2. **Multilingual & Multi-Script Intent Engine**:
   - Full native detection across **Hindi (Devanagari)**, **Tamil**, **Telugu**, **Bengali (বাংলা)**, **Hinglish**, and **English**.
   - Covers 7 critical Indian fraud vectors:
     - ⚡ Electricity Night Cutoff Threats
     - 🚗 Fake e-Challan APK Trojans
     - 💼 Part-Time Telegram Task Scams
     - 👮 Digital Arrest & Police Extortion
     - 💰 UPI PIN Cashback Inversion Bait
     - 🏦 Bank KYC Account Suspension Scams
     - 🚨 Artificial High-Pressure Urgency Tactics

3. **Typosquatting & Malicious Payload Scanner**:
   - Evaluates domain Levenshtein distances against trusted whitelist registries.
   - Detects Android APK direct payloads, abused free hosting subdomains, and suspicious TLDs (`.xyz`, `.top`, `.icu`).

4. **Dual Inference Modes**:
   - **Hybrid Heuristics Pipeline**: Deterministic multi-factor scoring (DLT Header + URL Forensics + Urgency + Credential Bait).
   - **On-Device MuRIL Neural Intent Classifier**: Simulated edge transformer model benchmarked for local INT8 mobile NPUs without cloud server transmission.

5. **1-Click National Incident Escalation**:
   - Packages incident forensic evidence for **National Cyber Crime Helpline 1930** (`cybercrime.gov.in`).
   - Formats payload submissions for **DoT Chakshu / Sanchar Saathi** telecom header reporting.
   - Generates WhatsApp family alert templates and structured FIR forensic text.

---

## 🚀 Deployment

### Option A: Deploy on Vercel
1. Install Vercel CLI or link with GitHub:
   ```bash
   npx vercel
   ```
2. Follow prompts to deploy instantly.

### Option B: Deploy on GitHub Pages
1. Push this repository to GitHub.
2. Go to **Settings** $\rightarrow$ **Pages**.
3. Under **Branch**, select `main` / `root` and click **Save**.
4. Your site will be live at `https://<username>.github.io/<repo-name>/`.

---

## 📁 File Structure
- `index.html` — Main interactive web application
- `Sms.html` — Prototype reference file
- `vercel.json` — Vercel routing configuration
- `README.md` — Technical overview and deployment guide

