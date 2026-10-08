# 🩸 Blood Response System

An emergency blood donation coordination platform designed to help blood seekers connect with potential donors faster. Developed as part of the Alkhidmat Foundation Pakistan — Summer Social Internship Program (SSIP) 2026.

## 🎯 Project Overview

Finding available blood donors during an emergency can be difficult and time-consuming. The Blood Response System aims to simplify donor discovery and emergency blood requests through a mobile-first application.

## ✨ Key Features

* 🩸 Donor and requester registration
* 🚨 Emergency blood request interface
* 📍 Nearby donor discovery and location-based matching
* 🏥 Hospital/request verification workflow
* ⏱️ Donor cooldown tracking
* 🌐 Urdu and English language support with RTL layout
* 🔐 JWT-based authentication
* 👤 Donor profiles and availability
* 📱 Mobile-first interface built with Expo

*Note: Feature availability and backend integration may vary in this prototype. See Known Limitations below.*

## 🛠️ Tech Stack

| Component         | Technology                                              |
| ----------------- | ------------------------------------------------------- |
| Mobile frontend   | React Native, Expo                                      |
| Language          | TypeScript                                              |
| Navigation        | Expo Router                                             |
| Backend API       | Python, FastAPI                                         |
| Database          | MongoDB and SQLAlchemy-backed local database components |
| Authentication    | JWT                                                     |
| API communication | Axios                                                   |
| State management  | Zustand                                                 |

## 📁 Project Structure

```text
blood-response-system/
├── blood-response-frontend/
│   ├── app/
│   ├── components/
│   ├── constants/
│   ├── services/
│   └── store/
├── blood-response-backend/
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Prerequisites

* Python 3.11 or another version supported by the backend dependencies
* Node.js 18+
* npm
* Expo Go for mobile testing

### 1. Clone the repository

```bash
git clone https://github.com/Ashvin-lohana/blood-response-system.git
cd blood-response-system
```

### 2. Start the backend

```powershell
cd blood-response-backend
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

Configure the backend environment variables using the provided `.env.example` as a template. Never put real passwords, API keys, or database credentials in GitHub.

Start the API:

```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Open the interactive API documentation at:

`http://localhost:8000/docs`

### 3. Start the mobile frontend

Open a second terminal from the repository root:

```bash
cd blood-response-frontend
npm install
```

Configure the frontend `.env` file using `.env.example`.

Set the API URL according to your environment:

* Web or iOS simulator: `http://localhost:8000/api/v1`
* Android emulator: `http://10.0.2.2:8000/api/v1`
* Physical phone: use your computer's local IP address and ensure both devices are on the same Wi-Fi network.

Start Expo:

```bash
npx expo start
```

Scan the QR code using Expo Go.

## 🔐 Security and Privacy

* Keep `.env` files and credentials out of version control.
* Use environment variables for secrets.
* Do not publish real patient information or sensitive donor data.
* Use dummy data when demonstrating the prototype.

## ⚠️ Known Limitations

* Some backend flows use different database components and require further integration testing.
* External notification integrations, such as WhatsApp, SMS, and push notifications, require implementation and verification before being presented as operational.
* Hospital and donor verification workflows require real-world validation before production use.

## 🔮 Future Improvements

* Unify database architecture.
* Improve donor matching and availability updates.
* Integrate reliable notification services.
* Add automated backend and frontend tests.
* Deploy the backend and prepare a shareable Android demo build.
* Strengthen authentication, privacy, and production monitoring.

## 🤝 Acknowledgements

Developed as a team project during the Alkhidmat Foundation Pakistan — Summer Social Internship Program (SSIP) 2026.

## ⚖️ Disclaimer

This project is an educational prototype intended to explore emergency blood donor coordination. It is not a substitute for hospital services, medical advice, or professionally verified blood donation procedures.
