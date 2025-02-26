
# MedCare

## Overview
MedCare is a healthcare application designed to streamline emergency care by securely storing users' medical histories and utilizing AI to analyze symptoms. It provides hospital recommendations based on available facilities and can send SOS alerts with medical data for critical situations.

## Features
- **Secure Medical History Storage:** Users can input and update their medical history securely.
- **AI-Based Symptom Analysis:** Predicts possible medical conditions using AI models.
- **Hospital Finder:** Uses Google Maps API to locate nearby hospitals with required facilities.
- **Emergency SOS Alerts:** Sends urgent alerts to hospitals with patient details for ambulance dispatch.
- **User Authentication:** Secure login and data encryption for privacy compliance.

## Tech Stack
- **Backend:** Django (Python), Flask for API
- **Frontend:** React Native (for mobile application)
- **Database:** PostgreSQL (for structured data), Firebase (for real-time data)
- **AI/ML:** Infermedica API, Ada Health API
- **Maps & Location:** Google Maps API
- **Messaging & Alerts:** Twilio API (for SMS alerts)
- **Cloud Hosting:** AWS (for secure and scalable hosting)

## Prerequisites
Ensure you have the following installed before setting up the project:
- Python (>=3.8)
- Node.js (>=16.x)
- PostgreSQL (or Firebase setup)
- Virtual environment (venv) or Conda
- Google Cloud API Key (for Maps)
- Twilio API credentials (for SOS alerts)

## Installation & Setup
### 1. Clone the Repository
```bash
git clone https://github.com/samriddhi34/MedCare.git
cd MedCare
```

### 2. Backend Setup
#### Create a virtual environment and activate it:
```bash
python -m venv venv
source venv/bin/activate   # On Windows, use: venv\Scripts\activate
```

#### Install dependencies:
```bash
pip install -r requirements.txt
```

#### Set up environment variables:
Create a `.env` file in the root directory and add:
```ini
SECRET_KEY=<your-secret-key>
DATABASE_URL=<your-database-url>
GOOGLE_MAPS_API_KEY=<your-google-maps-key>
TWILIO_ACCOUNT_SID=<your-twilio-sid>
TWILIO_AUTH_TOKEN=<your-twilio-auth-token>
```

#### Run database migrations:
```bash
python manage.py migrate
```

#### Start the backend server:
```bash
python manage.py runserver
```

### 3. Frontend Setup
#### Navigate to frontend folder:
```bash
cd frontend
```

#### Install dependencies:
```bash
npm install
```

#### Start the React Native app:
```bash
npm start
```

## Running the Application
- **Web Interface:** Open `http://127.0.0.1:8000/` for the backend.
- **Mobile Application:** Use an emulator or a physical device with Expo.

## API Endpoints
### User Authentication
- `POST /api/register/` - Register a new user
- `POST /api/login/` - Login and retrieve auth token

### Medical History
- `GET /api/medical-history/` - Retrieve medical history
- `POST /api/medical-history/` - Add or update medical history

### Symptom Analysis & AI Prediction
- `POST /api/analyze-symptoms/` - Predict potential conditions

### Hospital Finder
- `GET /api/hospitals/?location=<lat,long>&specialty=<type>` - Fetch nearby hospitals with required facility

### Emergency Alerts
- `POST /api/send-sos/` - Trigger an SOS alert with patient details

## Deployment
- Backend will be deployed on **AWS EC2** or **Heroku**
- Frontend will be deployed using **Firebase** or **Expo EAS**

## Security & Compliance
- End-to-end encryption (AES-256) for sensitive data.
- OAuth 2.0 for authentication.
- HIPAA/GDPR compliance for secure patient data handling.

## Contributors
**Samriddhi Sinha**

