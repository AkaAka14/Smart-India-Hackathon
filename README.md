 # 🚌 ScheduLine – Smart Bus Assignment System (Smart India Hackathon Project)

Welcome to **ScheduLine**, a smart crew scheduling solution developed for the **Smart India Hackathon (SIH)**. This system revolutionizes public transportation logistics by automating the assignment of **buses, drivers, and conductors** based on real-world constraints like distance, preferences, and shift timings.

<p align="center">
  <img src="https://img.shields.io/badge/Smart%20India%20Hackathon-2024-blueviolet?style=flat-square" />
  <img src="https://img.shields.io/badge/Focus-Automated%20Scheduling-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Tech-DSA%20%7C%20ML%20%7C%20Maps%20API-green?style=flat-square" />
</p>

---

## 🚀 Problem Statement

Public transportation systems often face scheduling chaos due to last-minute staff assignments and inefficient route allocation. Our solution tackles this by:

- **Optimizing crew allocation**
- **Incorporating driver preferences**
- **Reducing commute distance to starting point**
- **Allowing rest intervals between routes**

---

## 🧠 Solution Overview

ScheduLine is a web-based platform that:

- Takes in **routes, timings, and staff profiles**
- Assigns drivers and conductors to buses in a way that minimizes logistical inefficiencies
- Uses **distance calculation via Google Maps API** and **driver time preferences** for optimal assignment
- Enables **multi-route assignment** with intelligent rest period planning

---

## 🔧 Tech Stack

| Layer       | Tech Used |
|------------|-----------|
| **Frontend** | HTML · CSS · JavaScript · React|
| **Backend/Logic** | Python · Custom Matching Algorithms |
| **APIs**    | Google Maps API |
| **Database** | MONGOdb |

-

## Features

- **AI-Driven Scheduling:** Assigns buses and crew using ML models and optimization logic.
- **Real-Time Monitoring:** Visualizes bus routes and crew assignments on interactive maps.
- **Crew & Leave Management:** Allows crew to request leave and managers to approve/reject.
- **Bus & Route Management:** Add, edit, and view buses and routes with detailed info.
- **Automated Data Processing:** Scripts for generating, assigning, and updating bus/crew data.
- **Modern UI:** Built with React, Tailwind CSS, and Vite for a responsive experience.
- **RESTful API:** Node.js/Express backend with MongoDB for persistent storage.

---

## Repository Structure

```
Backend/    # Node.js/Express backend, MongoDB models, controllers, routes, AI integration
Frontend/   # React frontend, Tailwind CSS, Vite, all UI components
Extraset/   # Data generation scripts, assignment logic (Python/JS), mock/test data
output.csv  # Example output data
```

---

## Key Modules

### Backend ([Backend/](Backend/))
- **API Endpoints:** User auth, dashboard data, bus/crew CRUD, leave management ([routes/authRoutes.js](Backend/routes/authRoutes.js), [routes/leaveRoutes.js](Backend/routes/leaveRoutes.js))
- **Models:** User, BusRoute, AssignedDB ([models/](Backend/models/))
- **Controllers:** Business logic for authentication, assignment, leave, etc. ([controllers/authController.js](Backend/controllers/authController.js))
- **AI Integration:** Python scripts for ML-based assignment ([Extraset/db.js/AI_model/sihmodel1.py](Extraset/db.js/AI_model/sihmodel1.py))

### Frontend ([Frontend/](Frontend/))
- **Dashboards:** Manager and Crew dashboards ([src/components/DashboardManager.jsx](Frontend/src/components/DashboardManager.jsx), [src/components/DashboardCrew.jsx](Frontend/src/components/DashboardCrew.jsx))
- **Bus & Route Info:** Add/view buses, visualize routes ([src/components/AddBus/AddBus.jsx](Frontend/src/components/AddBus/AddBus.jsx), [src/components/Bus Info/BusInfo.jsx](Frontend/src/components/Bus Info/BusInfo.jsx), [src/components/Route Map/RouteMap.jsx](Frontend/src/components/Route Map/RouteMap.jsx))
- **Authentication:** Login/Register ([src/App.jsx](Frontend/src/App.jsx))
- **About/Contact:** Project info ([src/components/About/about.jsx](Frontend/src/components/About/about.jsx))

### Data & Scripts ([Extraset/](Extraset/))
- **Data Generation:** Generate mock bus/crew data ([busdata/sample.py](Extraset/busdata/sample.py))
- **Assignment Logic:** Assign buses to crew using Python/JS ([utils/assignlogic.py](Extraset/utils/assignlogic.py), [utils/algoUpdatelogic.js](Extraset/utils/algoUpdatelogic.js))
- **Conversion Scripts:** CSV/JSON conversion ([utils/assignedBuses.js](Extraset/utils/assignedBuses.js))

---

## Getting Started

### Prerequisites
- Node.js, npm
- Python 3.x (for AI/data scripts)
- MongoDB (local or Atlas)

### Backend Setup
```sh
cd Backend
npm install
cp .env.sample .env   # Set your MongoDB URI and secrets
npm start
```

### Frontend Setup
```sh
cd Frontend
npm install
npm run dev
```

### Data & AI Scripts
- Run Python scripts in [Extraset/db.js/AI_model/](Extraset/db.js/AI_model/) for ML-based assignments.
- Use [Extraset/utils/](Extraset/utils/) scripts for data processing and assignment.

---

## API Endpoints

- **Auth:** `/api/auth/register`, `/api/auth/login`
- **Dashboard:** `/api/auth/dashboard-manager`, `/api/auth/dashboard-crew/:id`
- **Bus Data:** `/api/auth/bus-data/`, `/api/auth/add-bus`
- **Leave:** `/api/leave/leave-request`, `/api/leave/leave-requests`, `/api/leave/leave-status/:id`

---

## Technologies Used

- **Frontend:** React, Tailwind CSS, Vite, Axios, Leaflet.js
- **Backend:** Node.js, Express, MongoDB, Mongoose, JWT
- **AI/Data:** Python (pandas, scikit-learn, geopy, faker), JavaScript (Node scripts)

---

## Contributors

- [Akansha](https://github.com/AkaAka14)
- [Ayush Singhal](https://github.com/ayush-3107)
- [Tanisha](https://github.com/Tanisha020)
- [Malavika Gupta](https://github.com/Malavika-Gupta)
- [Mohak Mittal](https://github.com/Mohak1809)
- [Vansh Agrawal](https://github.com/Agrawal-Vansh)

---

