# 🌤️ Weather App
**PM Accelerator - Tech Assessment**

Welcome to the central repository for the **Weather & Forecast Explorer** application. 

This project was developed as a modern, decoupled fullstack application, splitting the concerns between a responsive Frontend and a robust Backend API. 

## 🔗 Project Repositories

Please navigate to the individual repositories below to view the source code, detailed documentation, and setup instructions for each component:

* **[🖥️ Frontend Repository](https://github.com/DanielLS2000/Weather-App-Frontend)**: Built with Next.js and Material-UI.
* **[⚙️ Backend Repository](https://github.com/MedCaju/MedCaju-Backend)**: Built with Python, FastAPI, and SQLite.

---

## 🌐 Live Demo & Architecture Context

**Live Application:** [https://weather-app-frontend-tau-two.vercel.app/](https://weather-app-frontend-tau-two.vercel.app/)

**Important Note on Rate Limiting:**
The application utilizes the free tier of the Open-Meteo API. Because the live backend is hosted on a shared free server (Render.com), it shares its IP address with thousands of other applications. You might occasionally encounter a `429 Too Many Requests` error if the shared IP hits the daily API limit.

**To evaluate the system without shared-IP restrictions, please clone and run the repositories locally following the instructions inside each repository.**

---

## 🏗️ High-Level Architecture

* **Frontend:** A Next.js client that handles UI state, geographic input capture, and renders dynamic charts and interactive Google Maps embeds.
* **Backend:** A FastAPI RESTful service that acts as a proxy and orchestrator. It handles forward/reverse geocoding via Nominatim, fetches weather data from Open-Meteo, calculates averages, and stores search histories.
* **Database:** SQLite with SQLAlchemy ORM, handling full CRUD operations and dynamically recalculating weather data on record updates.
* **Export Engine:** Native backend endpoints capable of exporting historical data in JSON, CSV, XML, PDF, and Markdown.

---
*Developed by Daniel Lima.*
