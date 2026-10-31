# 🦈 Wireshark SOC & Packet Analysis Labs

### **Analyzing network protocols, investigating security incidents, and tracking down cyber threats**

Wireshark Packet Analysis Cybersecurity SOC Traffic Analysis HTTP TCP PCAP VoIP NetworkWalks

---

## 🔗 📌 Project Overview
This repository contains the documentation, specific display filters, and investigative findings from completing the **NetworkWalks Wireshark SOC Lab Series** (8 live labs) along with the **Advanced Level Traffic Analysis Quiz**. 

The focus of this project was to transition from basic network capture mechanics to active security threat-hunting—using packet analysis to expose unencrypted logins, detect automated brute-force attacks, identify adversary infrastructure, and extract data from live communication streams.

---

## 🏆 Verified Achievements (100% Score)

Below are the verified milestones achieved during the investigation phases:

### 🧠 Wireshark Quiz (Advanced Level)
* **Score:** 10/10 Correct (100%) - Outstanding

<img width="1366" height="724" alt="quiz2" src="https://github.com/user-attachments/assets/9dad29a0-5757-4ba2-8931-b1db494c0fd8" />


## 🎯 Objectives
The main objectives of this project were to:
* Capture live local Wi-Fi data flows and map transport-layer handshake parameters.
* Parse pre-captured traffic artifacts (`.pcap`) offline to trace remote asset footprints.
* Reconstruct multi-packet conversations using **TCP Stream Following** tools.
* Analyze protocol vulnerabilities to extract plain-text sensitive credentials.
* Identify malicious behaviors including high-frequency brute-force patterns.
* Utilize VoIP analysis features to trace fraudulent communication activity.

---

## 📐 Completed Labs & Forensic Focus Areas

### 📞 Lab 8: Catch the Call Scammer (100/100 Marks)
* **Core Focus Area:** Analyzed VoIP infrastructure, SIP call setup sequences, and RTP media payloads. Dissected caller extensions, specific codec formats, and extracted credit card strings directly from replayed voice streams.

<img width="1080" height="1700" alt="Lab 8 Result - Ackim Kafula" src="https://github.com/user-attachments/assets/5762d787-4358-465e-87af-6108504f75e5" />


### 🦹‍♂️ Lab 7: Catch the Brute Force Attacker (100/100 Marks)
* **Core Focus Area:** Monitored high-volume authentication failures, pinpointed automated target profiles, extracted credential patterns, and identified the precise success status response code that confirmed a compromised system.

<img width="1080" height="1700" alt="Lab 7 Result - Ackim Kafula" src="https://github.com/user-attachments/assets/b07ebf00-26da-4705-97fc-45abcae7a5e0" />


### 🔑 Lab 6: HTTP Plain Text Credentials (100/100 Marks)
* **Core Focus Area:** Audited insecure web form interfaces handling client requests. Tracked specific browser source footprints, quantified login attempts, and retrieved unencrypted passwords directly from the packet details line.

<img width="1080" height="1700" alt="Lab 6 Result - Ackim Kafula(1)" src="https://github.com/user-attachments/assets/be541828-cf2c-4d52-be1e-fdc55ec28c39" />


### 🕵️‍♂️ Lab 5: Follow TCP Stream, Part 2 (100/100 Marks)
* **Core Focus Area:** Practiced advanced session reassembly logic across multiple traffic flows. Located obfuscated system keywords, detected backup server connections, analyzed directional stream responses, and tracked down exfiltrated file assets.

<img width="1080" height="1700" alt="Lab 5 Result - Ackim Kafula" src="https://github.com/user-attachments/assets/4c4f0741-b7c9-4b97-9c91-99232d6731df" />


### 💬 Lab 4: Follow TCP Stream 1 (100/100 Marks)
* **Core Focus Area:** Identified non-standard active network chat application ports, reassembled specific custom communication streams, extracted temporary administrative infrastructure passwords, and recovered internal guest Wi-Fi keys.

<img width="1080" height="1700" alt="Lab 4 Result - Ackim Kafula" src="https://github.com/user-attachments/assets/e16f50b8-9a22-469d-8567-b81585a01e5b" />


### 🖥️ Baseline Capture Labs
* **Lab 1: Packet Capture** – Capturing live local Wi-Fi traffic while interacting with web services to locate local parameters, active DNS servers, and negotiation TLS profiles.
* **Lab 2: PCAP Analysis** – Investigating offline saved capture datasets to query core networking definitions without active transmission footprint traces.
* **Lab 3: Identify the Attacker's IP** – Analyzing sandboxed interactive traffic flows to accurately isolate structural infrastructure attack hosts.

---

## ⚙️ Essential Display Filters Mastered

| Operational Goal / Security Use Case | Wireshark Display Filter Syntax |
| :--- | :--- |
| **Isolate Custom Non-Web Chat Ports** | `tcp and not tcp.port == 80 and not tcp.port == 443` |
| **Track a Specific Network Host** | `ip.addr == 192.168.1.20` |
| **Filter Source Traffic to Web Interfaces** | `ip.src == 10.0.0.15 and tcp.dstport == 80` |
| **Isolate Web Login Submissions** | `http.request.method == "POST"` |
| **Isolate Targeted TCP Streams** | `tcp.stream eq 5` |

---

## 🧠 Key Takeaways & SOC Skills Learned

### 1. Reconstructing plain-text streams
* **SOC Application:** Right-clicking packets and selecting `Follow -> TCP Stream` breaks down traffic visually. Client-to-server data appears in **Red**, and Server-to-client responses appear in **Blue**. This technique allows an analyst to bypass reading raw hex bytes and read exactly what an attacker or system transmitted.

### 2. Spotting Insecure Infrastructures
* **SOC Application:** Exposing how legacy plain HTTP transfers private user credentials in standard visible text blocks. This highlights why enforcing robust configurations like **HTTPS** and TLS wrapping is crucial for preventing data interception.

### 3. Traffic Baseline Analysis
* **SOC Application:** Using the `Statistics -> Conversations` window allows an analyst to quickly map out communication pairs. Sorting by **Bytes** or packet volume immediately unmasks anomalies like high-volume data exfiltration or automated brute-force scripts targeting internal endpoints.

---

## 🛡️ Security & Ethical Use Disclaimer
All packet captures analyzed throughout these labs were conducted inside controlled virtual network sandboxes or using provided training PCAP capture sets. Network monitoring tools must only be used on infrastructures you own or have explicit authorization to audit.

---

## 🧑‍💻 Author
* **Ackim Kafula**
* **Program Name:** Cybersecurity at NetworkWalks
* **Connect with me:** [My LinkedIn Profile: [(https://www.linkedin.com/in/ackim-kafula-5647542ab/)](https://www.linkedin.com/in/ackim-kafula-5647542ab/)
