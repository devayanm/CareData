# 🩺 CareData: Decentralized Healthcare, Simplified

**CareData** revolutionizes digital health management by combining blockchain security, modern patient-centered design, and truly interactive telehealth. Our mission: ***Empower every patient to take full ownership of their medical data, appointments, and wellness—in a single platform, from anywhere.***

---

## 🔗 Table of Contents

- [🌟 Overview](#-overview)
- [🚀 Features & Highlights](#-features--highlights)
- [🛠️ Tech Architecture](#️-tech-architecture)
- [👩‍⚕️ Full User Experience](#-full-user-experience)
- [⚡ Interactive Setup Guide](#-interactive-setup-guide)
- [🔐 Configuring Security (.env)](#-configuring-security-env)
- [📂 Folder Blueprint](#-folder-blueprint)
- [💡 Pro Tips & FAQ](#-pro-tips--faq)
- [🔮 Future Vision](#-future-vision)
- [🙌 Credits](#-credits)

---

## 🌟 Overview

> **CareData** is a powerful, privacy-first web3 platform letting patients:
> - **Securely store and share medical records** using Ethereum smart contracts.
> - **Book appointments and consult instantly** via video chat with real doctors.
> - **Order lab tests, track analytics**, and receive results—all online.
> - **Learn about health, prevention, and new technologies** through our dynamic blog and wellness hub.

With a seamless, interactive UI and automated workflows, CareData elevates patient empowerment while keeping your privacy and security at the core.

---

## 🚀 Features & Highlights

### 💾 Decentralized Medical Records
- **Blockchain Recording & Verification:** No data silos, no risk of tampering—your health records are *truly yours*.
- **Multi-file, fast document uploads** with secure storage via Cloudinary.

### 👩‍⚕️ Full Telemedicine Suite
- **Video Consultations:** Integrated, one-click video sessions.
- **Appointment Dashboard:** Effortless scheduling, rescheduling, or cancellation with real-time doctor availability.

### 🧪 Smart Lab Integration
- **Lab Test Booking:** Browse labs, book directly, and receive digital test results.
- **Auto-notifications** to keep you up-to-date on your sample’s journey.

### 📰 Interactive Medical Blog
- **Dynamic articles feed:** Health tips, research updates, and patient stories.
- **Like/Comment:** Coming soon—make the community more connected!

### 🛡️ Built for Privacy & Security
- End-to-end **encryption and blockchain signatures** for sensitive actions.
- Modern session management, cloud security best practices, and clear user consent throughout.

### 🖥️ Modern, Responsive UI
- **Mobile-first Bootstrap styling**
- **Accessible forms** and dark-mode-ready layouts
- Intuitive navigation inspired by the best of healthcare and tech startups

---

## 🛠️ Tech Architecture

| Layer        | Technology                                          |
|--------------|----------------------------------------------------|
| Frontend     | EJS templating, Bootstrap 5, Vanilla JS            |
| Blockchain   | Ethereum Sepolia Testnet, Solidity Smart Contracts  |
| Web3 Bridge  | EtherJS (v5.x) for seamless connections            |
| Backend      | Node.js, Express.js                                |
| Database     | MongoDB (with Compass support for visualization)   |
| File Storage | Cloudinary (unsigned uploads)                      |
| Other        | Real-time notifications, Email (Nodemailer-ready)  |



---

## 👩‍⚕️ Full User Experience

1. **Onboarding & Registration**
   - Quick registration/login with robust session storage.
   - Walkthrough guides new users through connecting MetaMask and setting basic profile info.

2. **MetaMask & Blockchain Sync**
   - CareData detects your MetaMask status.
   - Guides you to switch to Sepolia Testnet, get test Ether, and connect accounts—*with step-by-step UI popups*.

3. **Health Records Portal**
   - Intuitive upload with drag-and-drop or click-to-select.
   - Real-time signature prompts and blockchain confirmations in the UI (“Sign this record…”).

4. **Seeking Care**
   - Browse doctors by specialty, see real-time slots, and instantly schedule.
   - Secure, encrypted video consults and chat (built in).

5. **Lab Services**
   - Choose from partner labs, select packages, and book with a click.
   - All test results available digitally, and downloadable anytime.

6. **Medical News & Community**
   - Health blog with search, filters, and trending topics.
   - Plan: Discussions, sharing of articles, bookmarking for later.

---

## ⚡ Interactive Setup Guide

### 1️⃣ Prerequisites

- **Node.js v14+**: [Download here](https://nodejs.org/)
- **MongoDB** (or MongoDB Atlas—for cloud setup)
- **Metamask Browser Extension**: [Get it here](https://metamask.io/)
- **Cloudinary Account** for fast file/image uploads

### 2️⃣ Quickstart Installation

```
git clone https://github.com/yourusername/caredata.git
cd caredata
npm install
```

### 3️⃣ Copy and Edit `.env` (Security config)

```
PORT=3000
SESSION_SECRET=your-super-secret
CLOUD_NAME=your-cloudinary-cloud-name
API_KEY=your-cloudinary-api-key
API_SECRET=your-cloudinary-api-secret
MONGO_URI=mongodb+srv://user:pass@cluster.mongodb.net/dbname
```

### 4️⃣ Set Up Cloudinary Unsigned Upload
- Enable [unsigned uploading](https://medium.com/@aalam-info-solutions-llp/how-to-upload-images-to-cloudinary-with-react-js-ad402f775818).
- In `/public`, create `cloudinaryCredentials.js`:

```
export const cloudinary_url = 'https://api.cloudinary.com/v1_1//upload';
export const cloudinary_upload_preset = '';
```

### 5️⃣ Add EtherJS Library
- Download from [Ethers v5.1 ESM CDN](https://cdn.ethers.io/lib/ethers-5.1.esm.min.js) and place as `/public/ethers-5.6.esm.min.js`

### 6️⃣ Launch Application

```
node index.js
```
Open [http://localhost:3000/caredata](http://localhost:3000/caredata) to begin!

---

## 👩‍💻 Usage Guide

- Attach your MetaMask wallet (prompted on login, clear indicators when not connected)
- Switch to Sepolia Testnet (UI will guide you if you’re on the wrong network)
- To get free Sepolia ETH:  
  1. [Sign up at Alchemy](https://www.alchemy.com/)  
  2. [Request ETH from Sepolia Faucet](https://sepoliafaucet.com/)

*All blockchain/transaction prompts are interactive—just follow the pop-ups and wallet screens.*

---

## 🔐 Configuring Security (.env)

**Sample:**

```
PORT=3000
SESSION_SECRET=keep-me-secret
CLOUD_NAME=mycloud
API_KEY=myapikey
API_SECRET=myapisecret
MONGO_URI=mongodb+srv://user:pass@cluster.mongodb.net/mydb
```

*Always keep this file private!*

---

## 📂 Folder Blueprint

```
caredata/
├── public/
│   ├── ethers-5.6.esm.min.js
│   ├── cloudinaryCredentials.js
├── views/               # All EJS templates/UI pages
├── routes/              # Express routes
├── models/              # Mongoose schemas
├── controllers/         
├── .env
├── index.js
└── README.md
```

---

## 💡 Pro Tips & FAQ

- 🟢 **MetaMask not detected?** Make sure your extension is enabled and reload.
- 🟢 **Cloudinary/Upload failed?** Double-check unsigned preset and API keys.
- 🟢 **Video call issue?** Test camera/mic permissions and browser compatibility.
- 🚫 **Never commit `.env` or secret files.**
- 💡 **Want dark mode or accessibility support?** The UI is built for easy theming—just tweak Bootstrap or add CSS!

---

## 🔮 Future Vision

- AI-driven, privacy-preserving analytics and personalized health reminders
- P2P patient-doctor messaging and file sharing
- Multi-language support (internationalization)
- Modular mobile app (React Native) with push notifications
- Advanced admin dashboard with smart analytics, fraud monitoring, and patient feedback
- Community forum and real-time chat

---

## 🙌 Credits

- [Ashesh Mandal](https://github.com/asheshmandal2003)
- [Devayan Mandal](https://github.com/devayanm)
  
---

> *CareData brings the safest, smartest, most patient-friendly digital health experience—powered by the blockchain. Take charge of your care today!*

---
