# 🔍 Windows USB Forensic Investigation

This project is a complete digital forensics investigation focusing on **USB device activity on a Windows system**.  
It demonstrates practical DFIR (Digital Forensics & Incident Response) skills using industry tools such as **Autopsy** and **Chainsaw**.

The goal of this project was to:
- Analyse Windows event logs  
- Identify USB-related service activity  
- Recover email and browser artifacts  
- Detect suspicious items  
- Produce a structured forensic report  

This repository serves as a portfolio project showcasing practical investigation, analysis, and documentation skills.

---

## 📁 Project Structure

Windows-USB-Forensic-Investigation/
│
├── report/
│ └── USB_Forensic_Investigation_Report.docx # Final forensic report
│
├── screenshots/
│ ├── (Autopsy screenshots showing keyword hits, suspicious items, etc.)
│
└── evidence/
├── service_installation.csv # Chainsaw detection output
└── (Additional logs or extracted artifacts)

yaml
Copy code

---

## 🧰 Tools Used

### 🔹 Autopsy 4.22.1  
Used for:
- Keyword searches  
- Browser history review  
- Email artifact extraction  
- Event log parsing  
- Identifying suspicious files  

### 🔹 Chainsaw  
Used for:
- High-speed event log hunting  
- Identifying Event ID 7045 service installations  
- Highlighting USB driver loads  
- Detecting suspicious system activity  

### 🔹 Windows Event Logs  
Analysed:
- `Security.evtx`  
- `System.evtx`  
- `Setup.evtx`  
- `Application.evtx`

---

## 🔎 Key Findings

### ✔ USB Service Installations  
Chainsaw detected **multiple Event ID 7045** entries showing:
- USB driver installations  
- Kernel-mode services  
- Possible device enumeration events  

This confirms a USB device was inserted and initialized on the system.

---

### ✔ Browser & Email Artifacts  
Autopsy recovered **12 email addresses**, including:

- i560@gmail.com  
- temiilori560@gmail.com  
- temiisocool@outlook.ie  
- temilori67@gmail.com  

These were found in:
- Browser history  
- Extracted HTML logs  
- Security.evtx text blocks  

---

### ✔ Suspicious Items  
Autopsy flagged 4 items for review, including:
- HTML logs containing email metadata  
- CSV log data  
- Sections of `Security.evtx` referencing account changes  

---

## 📄 Final Report

The complete investigation is documented in:

📄 **report/USB_Forensic_Investigation_Report.docx**

This report includes:
- Methodology  
- Tools  
- Evidence  
- Timeline  
- Screenshots  
- Conclusions  
- Recommendations  

---

## 🧠 Skills Demonstrated

This project demonstrates the following DFIR skills:

- Windows artifact analysis  
- Log triage and correlation  
- Chain-of-evidence handling  
- Keyword & regex searching  
- Autopsy workflow & reporting  
- Chainsaw event log analysis  
- Professional forensic documentation  
- Repository structuring for portfolio projects  

---

## 🚀 How to Reproduce the Analysis

1. Import Windows `.evtx` logs into Autopsy  
2. Run ingest modules (keyword search, recent activity, etc.)  
3. Review:
   - Keyword hits  
   - Browser activity  
   - Suspicious items  
4. Run Chainsaw against the event logs:
chainsaw hunt .\EventLogs\ --rules .\rules\

yaml
Copy code
5. Correlate Autopsy and Chainsaw findings  
6. Document conclusions in a forensic report  

---

## 👤 Author  
**Temii Ilori**  
Digital Forensics & Cybersecurity Student  
