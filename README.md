# KaamWali.AI  
### Empowering Domestic Workers through Technology  

---

## Overview  
KaamWali.AI is a full-stack platform built to support domestic workers by enabling digital onboarding, worker discovery, identity verification, feedback tracking, hiring workflows, and safety monitoring.

The system focuses on inclusivity by supporting multilingual interfaces and voice-based interactions, making it accessible for low-literacy users.

---

## Problem Statement  

Domestic workers face several challenges in accessing fair opportunities:

- Lack of digital presence and visibility  
- Dependence on middlemen  
- No structured trust or feedback system  
- Safety concerns in informal job environments  

---

## Current Features 

### Authentication
- Login/signup for workers and employers  
- Role-based access  
- Mock OTP-based authentication  

### Multilingual Support
- Supports multiple Indian languages  
- Dynamic translations via backend API  

### Voice-Based Onboarding
- Speech-to-text using Web Speech API  
- Structured profile generation via backend  

### Worker Profiles
- Detailed worker profiles with:
  - Skills, experience, availability  
  - Trust score and verification status  
- Resume PDF generation using Puppeteer  

### Employer Search & Matching
- Filter workers by:
  - Location  
  - Skills  
  - Experience  
  - Salary  
- Worker cards with detailed insights  

### Feedback & Trust System
- Feedback collection from employers  
- Sentiment-based scoring  
- Dynamic trust score updates  

### Identity Verification
- Document upload system  
- OCR-based detection (Google Vision / Tesseract when configured)  

### Hiring System
- Hire / release workers  
- Track hiring status and history  
- Hire request workflow  

### Safety Features
- Panic alert system  
- Incident reporting  
- Admin safety monitoring dashboard  
- Optional SMS alerts (Twilio)  

---

## Tech Stack  

- **Frontend:** React 18, Vite, Tailwind CSS  
- **Backend:** Node.js, Express.js  
- **Database:** MongoDB  
- **Authentication:** Mock OTP + bcrypt  
- **Speech Recognition:** Web Speech API  
- **PDF Generation:** Puppeteer  
- **OCR:** Google Vision API / Tesseract  
- **File Uploads:** Multer  

---

## Architecture Workflow  

1. User signs up (Worker / Employer)  
2. Worker completes onboarding (voice/text)  
3. Profile stored in database  
4. Employers browse and filter workers  
5. Hiring requests are created  
6. Feedback updates trust score  
7. Safety incidents are tracked  

---

## Project Structure  
```text
kaamwali-ai/
│
├── backend/
│   ├── index.js              # Main server entry point
│   ├── db.js                 # MongoDB connection
│   ├── profileParser.js      # Voice/profile parsing logic
│   ├── generateWorkerPDF.js  # Resume PDF generation
│   ├── VerifydocRoute.js     # Document verification routes
│   │
│   ├── models/
│   │   └── Worker.js
│   │
│   ├── routes/
│   │   ├── feedback.js
│   │   └── i18n.js
│   │
│   ├── templates/
│   │   └── workerResumeTemplate.js
│   │
│   └── uploads/
│
├── frontend/
│   ├── index.html
│   ├── vite.config.js
│   │
│   └── src/
│       ├── App.jsx
│       ├── api.js
│       ├── firebase.js
│       ├── firebaseAuth.js
│       ├── translations.js
│       │
│       ├── components/
│       ├── contexts/
│       ├── hooks/
│       ├── styles/
│       └── assets/
│           └── images/
│
├── .gitignore
├── package-lock.json
└── README.md
```
---

## Current Limitations  

- OTP system is mock (not real SMS-based)  
- Some frontend routes are not fully connected  
- Safety routes mismatch in some areas  
- API calls partially hardcoded in frontend  

---

## Future Scope  

- Real OTP authentication (Firebase)  
- AI-based profile generation  
- Smart matching algorithm  
- Improved UI/UX  
- Full deployment pipeline  

---

## Impact  

- Provides digital identity to domestic workers  
- Enables fair job discovery  
- Builds a trust-based hiring ecosystem  
- Introduces safety tracking in informal work  

---
