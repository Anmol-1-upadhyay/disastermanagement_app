# SOS-Application
An emergency Application for Android users.

# Emergency Assistance App

## Overview
The Emergency Assistance App is designed to facilitate quick and efficient communication between individuals in distress (**Requesters**) and available **Responders** during emergencies. The system consists of three primary components:
- **Requester** (User in distress)
- **Central Processing Unit (CPU)**
- **Responder** (Volunteer or agency providing assistance)

## Features

### Requester
- **User-Friendly Interface:** Designed for ease of use, especially in distress situations.
- **SOS Button:** Sends the requester's location (via GPS) to the Central Processing Unit.
- **Responder Details:** Once the CPU identifies the nearest responder using a shortest path algorithm, it sends back:
  - **ETA (Estimated Time of Arrival)**
  - **Distance to the requester**
  - **Responder Status (Active/Inactive)**
- **Periodic Updates:** Requester’s screen refreshes every 30 seconds with updated responder information to optimize battery usage.
- **Cancellation Mechanism:** Users must draw a line connecting three dots on the screen to prevent accidental cancellation of SOS requests.
- **Accessibility:** Support for vernacular languages and accessibility features for diverse user backgrounds.

### Central Processing Unit (CPU)
- **Request Processing:** Receives the requester's GPS coordinates and determines the nearest responder.
- **Efficient Routing:** Implements algorithms such as **Dijkstra's Algorithm** or **A* (A-star)** for optimal pathfinding.
- **Request Allocation:** Sends emergency requests to the identified responder(s). If a responder accepts, the CPU updates the requester with necessary details.
- **Real-Time Updates:** Refreshes requester and responder data every 30 seconds.

### Responder
- **Registration:** Volunteers or agencies can register, defining their service areas and operational limits (if any).
- **Request Handling:** Receives emergency requests from the CPU and accepts or declines based on availability.
- **Live Status Updates:** The CPU continuously monitors and updates responder status (Active/Inactive) during the operation.

## Technical Implementations
- **Frontend:** Developed using **Kotlin** in **Android Studio**.
- **GPS Functionality:** Utilizes **Android's LocationManager**.
- **Communication:** Uses **SMS APIs** for notifications between Requesters and Responders.
- **Maps & Routing:** Integrates **Google Maps API** or **OpenStreetMap** for location tracking and navigation.
- **Backend:** Manages user data and registrations using **Firebase** or a custom backend.

## Algorithmic Implementations
- **Dijkstra’s Algorithm:** Determines the shortest path from the requester’s location to the nearest responder.
- **A* Algorithm:** Alternative to Dijkstra’s, optimized for real-time pathfinding using heuristics.

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/username/EmergencyApp.git
   ```
2. Open the project in **Android Studio**.
3. Configure **Firebase** and **Google Maps API** keys.
4. Build and run the app on an Android device.

## Usage
- Open the app and register as a **Requester** or **Responder**.
- Requesters can press the **SOS button** to send an emergency request.
- The system will assign the nearest responder and display real-time updates.
- Responders can accept requests and navigate to the requester.

## Contributing
1. Fork the repository.
2. Create a new branch:
   ```sh
   git checkout -b feature-branch
   ```
3. Make your changes and commit:
   ```sh
   git commit -m "Added new feature"
   ```
4. Push to your branch:
   ```sh
   git push origin feature-branch
   ```
5. Open a **Pull Request**.

## License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

