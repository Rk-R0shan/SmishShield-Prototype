# SmishShield — Multilingual Smishing Defense Platform
> **Smart India Hackathon (SIH 2026) Prototype**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-00F0D0?style=for-the-badge&logo=github)](https://rk-r0shan.github.io/SmishShield/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Telecom Standard](https://img.shields.io/badge/Telecom-TRAI%20DLT%202.0-orange?style=for-the-badge)](https://trai.gov.in)

An India-first, privacy-preserving cybersecurity defense engine designed to detect and counter multilingual SMS phishing (smishing), fake TRAI DLT sender headers, malicious APK payloads, and high-pressure financial coercion across Indian telecom networks.

🌐 **Live Web App**: [https://rk-r0shan.github.io/SmishShield/](https://rk-r0shan.github.io/SmishShield/)

---

## 🎯 The Problem

Over 80% of smishing attacks targeting Indian citizens evade conventional English-only SMS filters by:
1. **Using Native & Phonetic Indic Scripts**: Fraudsters craft messages in Hindi, Tamil, Telugu, Bengali, and Hinglish.
2. **Spoofing Telecom Headers**: Scammers bypass TRAI DLT registration rules by sending institutional banking alerts from standard 10-digit mobile SIMs (`+91-98...`) or international VoIP gateways.
3. **Distributing Banking Trojans via Direct APKs**: Evading app stores by sending disguised `.apk` files via shorteners (`bit.ly`, `is.gd`) claiming to be e-Challan or utility apps.

---

## 🛡️ Core Capabilities

### 1. TRAI DLT 2.0 Sender Header Validator
- Validates official alphanumeric commercial headers (`[Circle][Carrier]-[Brand]`, e.g., `AD-HDFCBK`, `VK-SBINB`, `WB-WBSEDCL`).
- Flags 10-digit mobile numbers sending institutional alerts (strict violation of TRAI commercial SMS regulations).
- Identifies suspicious international country-code routes (`+1...`, `+44...`) sending domestic Indian utility notices.

### 2. Multilingual Threat Intent Engine
- Built-in multi-script detection across **Hindi (Devanagari)**, **Tamil**, **Telugu**, **Bengali (বাংলা)**, **Hinglish**, and **English**.
- Real-time intent classification for the top 7 Indian fraud vectors:
  - ⚡ **Electricity Cutoff Threats**: Urgent night disconnection threats citing unpaid bills.
  - 🚗 **e-Challan APK Trojans**: Fake traffic fines distributing malicious `.apk` malware packages.
  - 💼 **Part-Time Telegram Tasks**: "Earn ₹3,000/day liking YouTube videos" task scams.
  - 👮 **Digital Arrest & Police Extortion**: Fake CBI/Customs warrants and parcel seizure threats.
  - 💰 **UPI PIN Cashback Bait**: Social engineering tricking users to enter UPI PINs to "receive" money.
  - 🏦 **Bank KYC Suspension**: Panic-inducing fake account expiry warnings.
  - 🚨 **Urgency Exploitation**: High-pressure deadlines forcing rushed decisions.

### 3. URL & Android APK Forensics
- **Typosquatting Detection**: Computes Levenshtein edit distance against registered Indian financial portals (e.g., `onlinesbi.sbi`, `hdfcbank.com`).
- **Malware Extension Inspector**: Flags direct download payloads (`.apk`, `.dex`, `.zip`).
- **Free Hosting & Shortener Analysis**: Detects abuse of dynamic free hosting (`ngrok-free.app`, `pages.dev`) and URL shorteners.

### 4. Dual Inference Architecture
- **Hybrid Heuristic Pipeline**: Fast, deterministic multi-factor weighted scoring.
- **On-Device MuRIL Neural Intent Classifier**: Simulated edge transformer inference benchmarked for INT8 mobile NPUs without sending SMS content to external cloud servers.

### 5. 1-Click National Incident Escalation
- **National Cybercrime Portal / Helpline 1930**: Auto-formats evidence for reporting financial cyber fraud.
- **DoT Chakshu Facility**: Generates telecom payload for reporting fraudulent sender headers.
- **WhatsApp Citizen Alerts**: Pre-fills clear warning templates for family and community sharing.

---

## 💻 Running Locally

SmishShield is a standalone zero-dependency edge web application.

```bash
# 1. Clone the repository
git clone https://github.com/Rk-R0shan/SmishShield.git

# 2. Open index.html directly in any browser
cd SmishShield
# On Windows:
start index.html
```

Or run via any local development server:
```bash
npx serve .
```

---

## 📁 Repository Structure

```
SmishShield/
├── index.html       # Primary production application entrypoint
├── Sms.html         # Prototype reference file
├── vercel.json      # Vercel deployment routing configuration
└── README.md        # Technical architecture documentation
```

---

## ⚖️ Compliance & Privacy Notice

SmishShield is designed around the **Digital Personal Data Protection (DPDP) Act 2023** principles:
- **On-Device Edge Privacy**: Designed so SMS content never leaves user devices.
- **Simulated Metrics**: The 28ms latency benchmark represents target edge execution modeling quantized INT8 MuRIL / IndicBERT on mobile NPUs.
