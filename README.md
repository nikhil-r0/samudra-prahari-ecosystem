# 🌊 Samudra Prahari: Coastal Intelligence Ecosystem

### **Official Submission for Smart India Hackathon (SIH) 2025**

**Problem Statement ID:** ID25039

**Theme:** Disaster Management | **Category:** Software

**Organization:** INCOIS (Indian National Centre for Ocean Information Services)

**Samudra Prahari** (Guardian of the Ocean) is a resilient, end-to-end platform designed to bridge the information gap during coastal hazards. It transforms everyday citizen smartphones and social media streams into a verified, real-time intelligence grid, ensuring that authorities can act when seconds matter most.

---

## 🚀 The Core Philosophy: "Built for the Real World"

Most disaster reporting systems fail due to two reasons: **Network Collapse** and **Low User Adoption**. Samudra Prahari solves both:

1. **Resilience:** An offline-first mobile app with **P2P BLE Mesh Networking** ensures reports reach authorities even when towers are down.
2. **Engagement:** The **"Coastal Companion"** suite (tide forecasts, tourist guides) ensures the app is a daily utility, keeping the reporter network active 365 days a year.

---

## 📂 Ecosystem Architecture (Submodules)

This repository is a container for the three primary pillars of the project:

### 1. [Mobile Submodule (`/mobile`)](https://github.com/nikhil-r0/samudra-prahari-app)

**The Ground Truth Sensor.**

* **Offline Reporting:** Built with Expo and `expo-bitchat` for Bluetooth mesh communication.
* **Multilingual Support:** Localized interface for diverse coastal communities.
* **User Retention:** Features tide forecasting, beach cleanliness reporting, and reward badges.

### 2. [Scraper Submodule (`/scraper`)](https://github.com/nikhil-r0/samudra-scraper)

**The Digital Pulse.**

* **Social Intelligence:** Python-based scrapers using **Playwright** to monitor X (Twitter) and Instagram.
* **Decoupled Scaling:** Operates independently of the main API to ensure 24/7 monitoring without performance bottlenecks.
* **Auto-Cleaning:** Intelligent pipeline to de-duplicate and verify redundant posts.

### 3. [Web Submodule (`/web`)](https://github.com/nikhil-r0/samudra-web)

**The Command Center.**

* **Geospatial Dashboard:** Next.js & Leaflet-based map view with **PostGIS/PostgreSQL** for real-time report clustering.
* **AI Analysis Core:** Utilizes **IndicBERT** for multilingual NLP and computer vision to verify hazard authenticity.
* **Role-Based Access:** Secure authentication via **Supabase** for different tiers of emergency responders.

---

## 🛠️ Unified Tech Stack

| Component | Technologies |
| --- | --- |
| **Frontend** | React Native (Expo), Next.js, Tailwind CSS |
| **Backend** | Python (FastAPI), Supabase (PostgreSQL/PostGIS) |
| **Automation** | Playwright (X/Instagram Scrapers) |
| **AI/NLP** | IndicBERT, Hugging Face, PyTorch |
| **Communication** | BLE Mesh Networking (Bitchat Protocol) |

---

## 🏁 Getting Started (Global Setup)

Because this repo uses Git Submodules, follow these steps to clone the entire ecosystem:

```bash
# Clone the root repository
git clone https://github.com/nikhil-r0/samudra-prahari-ecosystem.git
cd samudra-prahari-ecosystem

# Initialize and update all submodules
git submodule update --init --recursive

```

Refer to the individual `README.md` files in `/mobile`, `/scraper`, and `/web` for specific installation instructions for each layer.

---

## 🛡️ Key Innovations for SIH 2025

* **Geospatial Intelligence:** Native database support for clustering nearby reports, allowing analysts to distinguish between isolated incidents and large-scale disasters.
* **AI-Powered Verification:** A multi-stage pipeline that assigns "Confidence Scores" to social media posts, filtering out "fake news" or old footage.
* **P2P Mesh Network:** A functional implementation of decentralized communication for zero-connectivity zones.

---
