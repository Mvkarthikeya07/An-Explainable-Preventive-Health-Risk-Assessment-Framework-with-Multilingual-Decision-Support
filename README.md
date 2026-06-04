<div align="center">

<h1>🩺 Explainable Preventive Health Risk Assessment</h1>
<h3>A Multilingual, Voice-Assisted Decision Support Framework for Low-Resource Environments</h3>

<p>
  <img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Flask-2.3.2-000000?style=for-the-badge&logo=flask&logoColor=white"/>
  <img src="https://img.shields.io/badge/Languages-5%20Indian%20Languages-orange?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Risk%20Engine-Rule--Based%20%7C%20Explainable-blueviolet?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Published-INDJCST%20Vol.5%20Issue%201-red?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge"/>
</p>

<p>
  A <strong>peer-reviewed, hackathon-recognised</strong> preventive health risk stratification system delivering explainable risk assessments, multilingual guidance, and voice-assisted interaction — designed specifically for underserved and linguistically diverse communities across India.
</p>

> ⚠️ **Medical Disclaimer:** This system is intended strictly for **preventive awareness and educational purposes**. It must **not** be used as a substitute for professional medical advice, diagnosis, or clinical treatment.

</div>

---

## 📌 Table of Contents

- [Abstract](#-abstract)
- [Recognition & Publication](#-recognition--publication)
- [Application Screenshots](#-application-screenshots)
- [System Architecture](#-system-architecture)
- [Risk Stratification Engine](#-risk-stratification-engine)
- [Risk Engine vs ML Models — Design Comparison](#-risk-engine-vs-ml-models--design-comparison)
- [Multilingual Chatbot](#-multilingual-chatbot)
- [Supported Languages](#-supported-languages)
- [Project Structure](#-project-structure)
- [Quick Start](#-quick-start)
- [SDG Alignment](#-sdg-alignment)
- [Evaluation & Validation](#-evaluation--validation)
- [Technology Stack](#-technology-stack)
- [Future Enhancements](#-future-enhancements)
- [Author](#-author)

---

## 📄 Abstract

This project presents a **Preventive Health Risk Analysis and Multilingual Decision Support System** aimed at improving early health awareness and preventive decision-making among diverse and underserved populations. The system evaluates individual health risk levels using physiological and lifestyle indicators and provides **explainable, multilingual, and voice-assisted guidance** through an interactive web interface and a deterministic health assistant chatbot.

Designed with a **prevention-first, transparency-oriented philosophy**, the system prioritizes interpretability, accessibility, and safety over opaque black-box intelligence — making it particularly relevant for public health informatics, responsible AI in healthcare, and accessibility-focused medical technologies.

---

## 🏆 Recognition & Publication

### 📰 Peer-Reviewed Research Publication

> **Published in the Indian Journal of Computer Science and Technology (INDJCST)**

| Field | Detail |
|---|---|
| **Paper Title** | An Explainable Deterministic Framework for Preventive Health Risk Stratification with Multilingual Decision Support for Low-Resource Environments |
| **Author** | M. V. Karthikeya |
| **Journal** | Indian Journal of Computer Science and Technology (INDJCST) |
| **Volume / Issue** | Volume 5, Issue 1 (January – April 2026) |
| **DOI** | [10.59256/indjcst.20260501023](https://www.doi.org/10.59256/indjcst.20260501023) |

**Key research contributions documented in the publication:**
- Development of a rule-based preventive health risk stratification engine grounded in clinical thresholds
- Design of an explainable decision-support framework for non-medical users
- Integration of multilingual accessibility for inclusive healthcare awareness across five Indian languages
- Implementation of a deterministic health assistant chatbot for preventive guidance
- Emphasis on transparent and interpretable AI methodologies in resource-constrained healthcare settings

---

### 🥇 Hackathon Recognition — INNOCLASH'26

> **Developed and presented at INNOCLASH'26 — SDG-Aligned 24-Hour International Hybrid Hackathon**

- **Organizer:** Department of Computer Science and Engineering, Rajalakshmi Institute of Technology, Chennai
- **In Association With:** Datamind, UAE
- **Theme:** SDG-aligned problem solving, real-world societal impact, time-constrained engineering
- **LinkedIn Recognition:** [View Post & Certificate](https://www.linkedin.com/posts/m-v-karthikeya-b26a2131b_hackathon-innoclash-sdg-activity-7425411643255439360-ebbp?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFEhlw4BT-6V0rnLIZSzBIoK7YvV2QlbHLc)

---

## 📸 Application Screenshots

### Language Selection Interface

<img width="1366" height="768" alt="Language Selection - CancerScan AI" src="https://github.com/user-attachments/assets/9fd50428-00cc-4439-bca8-3fba38623cb8"/>

> Users first select their preferred language from five options (English, Hindi, Telugu, Tamil, Malayalam). All subsequent screens, guidance, and voice output adapt to the selected language.

---

### Health Assessment Input Form

<img width="1366" height="768" alt="Health Assessment Input Form" src="https://github.com/user-attachments/assets/ccc58e03-78e0-454d-be12-6ef85141f141"/>

> A clean, minimal form collects six physiological and lifestyle indicators. Voice narration guides users through the form — critical for semi-literate and visually impaired users.

---

### Risk Output Screens — Low / Moderate / High

**🟢 Low Risk Result**

<img width="1366" height="768" alt="Low Risk Result" src="https://github.com/user-attachments/assets/44c53a8c-b3e2-40ff-a814-5c21a0727d8d"/>

**🟡 Moderate Risk Result**

<img width="1366" height="768" alt="Moderate Risk Result" src="https://github.com/user-attachments/assets/0d0badc8-1cc7-4d62-ab28-52920436906e"/>

**🔴 High Risk Result**

<img width="1366" height="768" alt="High Risk Result" src="https://github.com/user-attachments/assets/3b2e685d-5806-475c-8e39-88c083909269"/>

> Each risk result is accompanied by a plain-language explanation and specific preventive guidance — voiced aloud in the user's selected language.

---

### Multilingual Chatbot Interface

<img width="1366" height="768" alt="Multilingual Chatbot" src="https://github.com/user-attachments/assets/b63e2d5e-648d-4f3a-975a-a00a2bd8bfaf"/>

> The integrated health assistant provides diet, exercise, and prevention guidance in the user's language. Voice output is available for every response.

---

## 🏗️ System Architecture

```
User
  │
  ▼
Language Selection (index.html)
  │ session["lang"] = {en / hi / te / ta / ml}
  ▼
Health Assessment Form (assessment.html)
  │ Inputs: age, bmi, bp, sugar, smoking, activity
  ▼
risk_engine.assess_risk(data)          ←── Rule-Based Scoring Engine
  │ Returns: (risk_level, advice_text)
  ▼
Result Page (result.html)
  │ Risk: Low / Moderate / High + Guidance
  │ translations[lang] → localized UI text
  │ Web Speech API → voice narration
  ▼
Chatbot (chatbot.html)  ←── Optional follow-up
  │ chatbot_engine.get_bot_response(msg, risk, lang)
  │ Keyword intent matching → 25 unique language-aware responses
  ▼
Voice Output (voice.js + Web Speech API)
```

---

## ⚙️ Risk Stratification Engine

The risk engine (`risk_engine.py`) implements a **weighted cumulative scoring system** grounded in internationally accepted preventive health thresholds.

### Scoring Matrix

| Parameter | Threshold | Risk Score | Clinical Reference |
|---|---|---|---|
| Age | ≥ 45 years | **+2** | WHO preventive screening threshold |
| BMI | ≥ 25 (Overweight) | **+2** | WHO BMI classification |
| Blood Pressure | ≥ 140 mmHg (Systolic) | **+2** | AHA Stage 2 Hypertension |
| Blood Sugar | ≥ 140 mg/dL (Post-prandial) | **+2** | ADA pre-diabetic threshold |
| Smoking | Yes | **+2** | IARC Group 1 carcinogen |
| Physical Activity | Low | **+1** | WHO physical inactivity risk factor |
| **Maximum Score** | | **11 points** | |

### Risk Classification Bands

| Score Range | Classification | Guidance Delivered |
|---|---|---|
| 0 – 3 | 🟢 **Low Risk** | Maintain balanced diet, stay active, continue healthy habits |
| 4 – 7 | 🟡 **Moderate Risk** | Adopt preventive lifestyle changes, monitor health regularly |
| 8 – 11 | 🔴 **High Risk** | Seek preventive medical consultation and lifestyle intervention |

### Boundary Condition Validation

Validated across **324 synthetic user profiles** spanning all parameter combinations (3 age levels × 3 BMI levels × 3 BP levels × 3 sugar levels × 2 smoking × 2 activity):

| Risk Band | Profiles | Distribution |
|---|---|---|
| Low Risk | 20 | 6.2% |
| Moderate Risk | 176 | 54.3% |
| High Risk | 128 | 39.5% |

All 324 profiles produced logically consistent outputs with no classification contradictions at boundary conditions.

---

## 🔬 Risk Engine vs ML Models — Design Comparison

This project deliberately employs a **rule-based deterministic engine** rather than a probabilistic ML classifier. This is a conscious, principled design choice — not a limitation.

| Criterion | Rule-Based Engine (This System) | ML Classifier (e.g., Logistic Regression, Random Forest) |
|---|---|---|
| **Explainability** | ✅ Every decision traceable to a rule | ❌ Black-box or semi-opaque |
| **Predictability** | ✅ Deterministic — same input = same output always | ⚠️ Probabilistic — outputs may shift |
| **Clinical Auditability** | ✅ Clinicians can review and validate each rule | ❌ Hard to audit learned weights |
| **Training Data Required** | ✅ None — grounded in published clinical thresholds | ❌ Requires labeled patient datasets |
| **Hallucination Risk** | ✅ Zero — rule outputs are bounded | ⚠️ Possible extrapolation errors |
| **Privacy** | ✅ No patient data stored or required | ⚠️ Requires data collection and storage |
| **Regulatory Suitability** | ✅ Easier to justify for public health deployment | ❌ Requires extensive clinical validation |
| **Adaptivity** | ❌ Does not learn from new data | ✅ Can improve with more data |
| **Edge Case Handling** | ✅ Explicitly defined boundary rules | ⚠️ May generalize poorly at extremes |
| **Deployment Weight** | ✅ Lightweight, no GPU/model overhead | ⚠️ Requires model artifacts and compute |

### When Rule-Based Design is the Right Choice

In healthcare AI for underserved populations, **explainability and safety outweigh raw accuracy**. A preventive health system serving semi-literate users in rural India must:
- Never produce unexplained or contradictory outputs
- Be auditable by public health officers without data science expertise
- Function on minimal compute with no ongoing data collection
- Align with internationally validated clinical guidelines

This system satisfies all four constraints. A future ML enhancement layer is planned (see [Future Enhancements](#-future-enhancements)) but only as a supplementary, clearly labelled probabilistic component — never as a replacement for the explainable rule core.

---

## 🤖 Multilingual Chatbot

The integrated health assistant (`chatbot_engine.py`) provides deterministic, language-aware responses across five intents.

### Chatbot Architecture

```
User Message (any language input)
        │
        ▼
Keyword Intent Detection
  "hi/hello/hey"        → greet
  "diet/food/eat"       → diet guidance
  "exercise/workout"    → activity guidance
  "health/healthy"      → general health tips
  "risk"                → personalized risk echo
        │
        ▼
Language Router → responses[session_lang][intent]
        │
        ▼
Text Response + Web Speech API Voice Output
```

### Coverage Matrix

| Intent | Keywords Detected | Languages Supported |
|---|---|---|
| Greeting | hi, hello, hey | English, Hindi, Telugu, Tamil, Malayalam |
| Diet Guidance | diet, food, eat | English, Hindi, Telugu, Tamil, Malayalam |
| Exercise Guidance | exercise, workout, fitness | English, Hindi, Telugu, Tamil, Malayalam |
| General Health | health, healthy, improve | English, Hindi, Telugu, Tamil, Malayalam |
| Risk Echo | risk | English, Hindi, Telugu, Tamil, Malayalam |

**Total unique responses:** 25 (5 intents × 5 languages)  
**Hallucination risk:** Zero — all responses are statically mapped, no generative model involved

---

## 🌐 Supported Languages

| Language | Script | Native Greeting |
|---|---|---|
| English | Latin | Hello! 👋 I'm your Health Assistant. |
| Hindi | Devanagari | नमस्ते! 👋 मैं आपका स्वास्थ्य सहायक हूँ। |
| Telugu | Telugu | నమస్కారం! 👋 నేను మీ ఆరోగ్య సహాయకుడిని. |
| Tamil | Tamil | வணக்கம்! 👋 நான் உங்கள் சுகாதார உதவியாளர். |
| Malayalam | Malayalam | നമസ്കാരം! 👋 ഞാൻ നിങ്ങളുടെ ആരോഗ്യ സഹായി ആണ്. |

All UI labels, risk results, chatbot responses, and voice narration fully adapt to the selected language via `translations.py` and `chatbot_engine.py`.

---

## 🗂️ Project Structure

```
preventive-health-risk/
│
├── app.py                  # Flask routes: /, /assessment, /result, /chatbot, /chat
├── risk_engine.py          # Weighted rule-based risk scoring engine
├── chatbot_engine.py       # Keyword-intent NLP + 5-language response mapper
├── translations.py         # Full UI label translations for 5 languages
├── requirements.txt        # Flask 2.3.2, gTTS
│
├── 📁 templates/
│   ├── index.html          # Language selection landing page
│   ├── assessment.html     # 6-parameter health input form
│   ├── result.html         # Risk level + advice display (voice-enabled)
│   └── chatbot.html        # Multilingual chat interface
│
└── 📁 static/
    ├── css/style.css        # Application styling
    └── js/
        ├── main.js          # Core UI interactions
        ├── chatbot.js       # Chat message handling and AJAX
        └── voice.js         # Web Speech API text-to-speech integration
```

---

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Modern browser with Web Speech API support (Chrome recommended)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/preventive-health-risk-assessment.git
cd preventive-health-risk-assessment
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

**Dependencies:**
```
Flask==2.3.2
gTTS
```

### 3. Run the Application

```bash
python app.py
```

Navigate to `http://127.0.0.1:5000` in your browser.

### 4. Usage Flow

1. **Select your language** from the landing page (English / Hindi / Telugu / Tamil / Malayalam)
2. **Enter health parameters:** Age, BMI, Blood Pressure, Blood Sugar, Smoking status, Activity level
3. **Click "Analyze Risk"** — receive your Low / Moderate / High risk classification with voice narration
4. **Open the Chatbot** for follow-up diet, exercise, and preventive health guidance in your language

---

## 🌱 SDG Alignment

| UN SDG | Goal | This System's Contribution |
|---|---|---|
| **SDG 3** | Good Health and Well-Being | Promotes preventive health awareness before clinical intervention is needed |
| **SDG 10** | Reduced Inequalities | Voice output and 5-language support remove literacy and language barriers |
| **SDG 9** | Industry, Innovation, Infrastructure | Lightweight, deployable healthcare technology requiring minimal infrastructure |

By enabling **low-cost, zero-data, accessible preventive healthcare** in five Indian languages with voice assistance, this system directly serves the populations most at risk of undetected chronic disease.

---

## 🧪 Evaluation & Validation

The system was validated using **324 synthetic user profiles** constructed across all parameter combinations (age × BMI × BP × blood sugar × smoking × activity), covering boundary conditions, edge cases, and extreme values.

### Validation Outcomes

| Validation Test | Result |
|---|---|
| Boundary condition consistency (score = 3 vs 4, 7 vs 8) | ✅ All cases classified correctly |
| Maximum risk scenario (all factors present) | ✅ Score = 11 → High Risk |
| Minimum risk scenario (all factors absent) | ✅ Score = 0 → Low Risk |
| Multilingual output parity (same input, 5 languages) | ✅ Identical risk levels, localized text |
| Chatbot intent matching stability | ✅ Deterministic across all 324 profile sessions |
| Voice narration trigger verification | ✅ Fires correctly on result and chatbot pages |

**No probabilistic accuracy metric is claimed** — the system's correctness is defined by logical consistency with its published clinical thresholds, not statistical model performance.

---

## 🛠️ Technology Stack

| Layer | Technology | Purpose |
|---|---|---|
| Backend | Python 3.8+, Flask 2.3.2 | Request routing, session management, inference serving |
| Risk Engine | Pure Python (rule-based) | Weighted clinical threshold scoring |
| Chatbot Engine | Pure Python (keyword NLP) | Intent matching, multilingual response routing |
| Translation Layer | `translations.py` (static dict) | UI label localization across 5 languages |
| Voice Output | Web Speech API (browser-native) | Text-to-speech narration for accessibility |
| Text-to-Speech | gTTS (Google TTS) | Server-side voice generation option |
| Frontend | HTML5, CSS3, JavaScript | Responsive UI, AJAX chat, voice triggers |

---

## 🔮 Future Enhancements

| Enhancement | Description | Impact |
|---|---|---|
| ML Augmentation Layer | Add Random Forest / XGBoost as a supplementary probabilistic risk signal — clearly labeled, not replacing the rule core | Higher sensitivity for atypical profiles |
| LLM Health Assistant | GPT/Gemini integration with medical safety guardrails | Richer conversational depth |
| Neural Text-to-Speech | Replace gTTS with cloud TTS (Google Cloud, Azure) for natural-sounding voice | Better inclusivity for audio-dependent users |
| Mobile Application | Flutter/React Native app for field deployment | Reach rural, smartphone-first users |
| Wearable Integration | Bluetooth BMI scales, BP monitors auto-populating form fields | Reduce manual input errors |
| Expanded Language Support | Bengali, Kannada, Marathi, Odia, Punjabi | Cover 80%+ of India's linguistic diversity |
| Offline Mode | Service Worker + local storage for connectivity-poor areas | Field-deployable without internet |
| Clinician Dashboard | Aggregated anonymised risk reports for public health officers | Population-level preventive insights |

---

## 🎓 Academic & Research Relevance

This project demonstrates competency across:

- **Responsible AI design** — explainability and safety over black-box accuracy
- **Public health informatics** — clinical threshold–grounded preventive risk stratification
- **Multilingual system engineering** — translation layer architecture for five Indian languages
- **Accessibility-oriented UI/UX** — voice-first design for low-literacy users
- **Applied software engineering** — modular Flask architecture with clean separation of concerns

**Suitable for:**
- MS/MTech applications in Computer Science, Data Science, Health Informatics, and AI
- Research-oriented academic evaluations and thesis supplementary work
- LinkedIn and portfolio showcase for healthcare AI and responsible AI roles

---

## 👤 Author

**M. V. Karthikeya**  
Aspiring Machine Learning Engineer · Healthcare AI Researcher · Python Enthusiast · 📍 India

[![Research](https://img.shields.io/badge/Published-INDJCST%202026-red?style=flat-square)](https://www.doi.org/10.59256/indjcst.20260501023)
[![Hackathon](https://img.shields.io/badge/INNOCLASH'26-Participant-gold?style=flat-square)](https://www.linkedin.com/posts/m-v-karthikeya-b26a2131b_hackathon-innoclash-sdg-activity-7425411643255439360-ebbp)
[![Python](https://img.shields.io/badge/Python-Expert-3776AB?style=flat-square&logo=python)](https://github.com/your-username)
[![Flask](https://img.shields.io/badge/Flask-Intermediate-000000?style=flat-square&logo=flask)](https://github.com/your-username)

---

## 📜 License

This project is released under the **MIT License** — free for academic, educational, and research use with attribution.

---

> ⚠️ **Reminder:** All risk assessments produced by this system are for **preventive awareness only** and must **never** be used as a substitute for professional medical advice, diagnosis, or clinical treatment.

---

<div align="center">

⭐ **If this project helped you, consider starring the repository!**

*Published research · Hackathon recognised · Built for 1.4 billion people*

</div>
