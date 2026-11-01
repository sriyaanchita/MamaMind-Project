# MamaMind
## AI-Powered Maternal Wellness and Family Support System with Wearable Health Monitoring

**A little reminder, not another task.**

MamaMind is a mobile application designed to support mothers during the postpartum period through personalized self-care, AI-powered assistance, shared parenting responsibilities, baby-care management, and wearable health monitoring.

The project aims to create a supportive digital environment that encourages maternal well-being while involving family members in everyday care.

## 1. Problem Statement

The postpartum period can be physically and emotionally demanding. New mothers often experience challenges related to self-care, medication schedules, baby-care responsibilities, emotional support, and maintaining daily routines.

Many existing applications focus on either maternal health or baby tracking rather than combining maternal wellness, family involvement, and wearable monitoring in one platform.

MamaMind addresses this gap through an integrated mobile application.

## 2. Key Features

### Mother Dashboard
- Personalized wellness dashboard
- Daily self-care activities
- Meditation and relaxation exercises
- Medication reminders
- AI-powered emotional support companion
- Personal journaling and Happy Jar
- Moms Community
- Baby-care shortcuts and activity tracking

### Father / Partner Dashboard
- Shared parenting responsibilities
- Baby-care task coordination
- Father coaching and parenting guidance
- Supportive recommendations for maternal well-being

### Baby Dashboard
- Baby profile management
- Feeding, sleeping, and diaper activity records
- Vaccination reminders
- Baby milestones and care history

### AI-Powered Wellness Assistance
- Conversational wellness companion
- Supportive self-care recommendations
- Voice and text interactions
- Gentle reminders and parenting assistance

The AI companion provides general wellness support and does not replace professional medical advice.

### Wearable Health Monitoring

The proposed wearable system uses an ESP32 microcontroller with sensors for monitoring:

- Heart rate
- Blood oxygen saturation (SpO₂)
- Physical movement

**Designed Data Flow:**

ESP32 + Sensors → Wi-Fi → Firebase Cloud Firestore → MamaMind Mobile Application

The health-monitoring interface has been developed. Hardware-to-Firestore integration and live sensor validation are currently in progress.

## 3. Technology Stack

| Component | Technology |
|---|---|
| Mobile Application | React Native, Expo, TypeScript |
| Navigation | Expo Router |
| Authentication | Firebase Authentication |
| Database | Firebase Cloud Firestore |
| Backend | Node.js, Express.js |
| AI Functionality | AI Backend Integration |
| Hardware | ESP32 |
| Sensors | Heart Rate, SpO₂, MPU6050 |
| Communication | Wi-Fi, HTTPS |
| Development Tools | VS Code, Arduino IDE, Git, GitHub |
| Android Distribution | Expo Application Services (EAS Build) |

## 4. System Architecture


                    MamaMind
                       |
              Firebase Authentication
                       |
              Role-Based Navigation
                       |
          +------------+------------+
          |            |            |
        Mother       Father        Baby
       Dashboard    Dashboard    Dashboard
          |            |            |
          +------------+------------+
                       |
               Cloud Firestore
                       |
             Records and Activity Logs

          ESP32 + Wearable Sensors
                       |
                     Wi-Fi
                       |
              Secure Upload Backend
                       |
                Cloud Firestore
                       |
              Health Monitoring UI

             Mobile App <-> AI Backend

## 5. Application Modules

### Authentication Module
Provides secure user login and role-based navigation for mothers, fathers, and baby-care interfaces.

### Maternal Wellness Module
Includes meditation, medication reminders, daily-care activities, journaling, and personalized wellness suggestions.

### Family Support Module
Allows partners to coordinate shared responsibilities and access parenting guidance.

### Baby-Care Module
Supports baby profiles, daily activity records, vaccination reminders, and milestone tracking.

### AI Companion Module
Provides conversational support, wellness suggestions, and parenting assistance through text and voice interactions.

### Wearable Monitoring Module
Provides a dashboard designed to display heart rate, SpO₂, and movement data received through Firebase Firestore.

## 6. Installation and Setup

### Prerequisites

- Node.js and npm
- Git
- Expo development environment
- Firebase project configuration
- Android device or emulator

### Clone the Repository

```bash
git clone https://github.com/sriyaanchita/MamaMind-Project.git
cd MamaMind-Project/source-code
```

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Configure Firebase and backend environment variables according to the project setup.

Do not commit private API keys, service-account credentials, or `.env` files containing secrets.

### Run the Application

```bash
npx expo start
```

### Build Android APK

```bash
eas build -p android --profile preview
```

The build requires a valid EAS configuration and accessible backend services.

## 7. Testing and Evaluation

The following functional areas can be tested:

- User authentication and role-based navigation
- Medication reminders and daily-care management
- Baby-care record storage and retrieval
- Firebase data synchronization
- AI companion interactions
- Android APK installation
- Wearable sensor upload and data-display verification

Hardware readings require physical sensor testing and successful end-to-end Firestore integration before they can be considered validated.

## 8. Sustainable Development Goals

### SDG 3 – Good Health and Well-Being
Supports maternal wellness, self-care, and health awareness during the postpartum period.

### SDG 5 – Gender Equality
Encourages shared parenting responsibilities and greater family involvement.

### SDG 9 – Industry, Innovation and Infrastructure
Integrates AI, IoT, cloud technologies, and mobile application development.

## 9. Future Scope

- Complete live ESP32-to-Firestore integration
- Improve wearable sensor reliability
- Introduce personalized wellness trend visualization
- Enhance family notifications and synchronization
- Expand AI-powered parenting assistance
- Add multilingual and accessibility features


## 10. Disclaimer

MamaMind is an academic wellness-support project. It is not a medical device and is not intended to diagnose, treat, or prevent medical conditions.

Heart-rate and SpO₂ readings cannot independently determine stress or emotional states.

---

**MamaMind — Supporting Mothers, Connecting Families, Nurturing Well-Being.**
