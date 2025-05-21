# SmartCarDiag (الفاحص الذكي للسيارات)

<div align="center">
  <img src="docs/images/logo.png" alt="SmartCarDiag Logo" width="200" />
  <p><strong>OBD-II Diagnostic System with AI-Enhanced Analysis</strong></p>
  <p>
    <a href="#features">Features</a> •
    <a href="#architecture">Architecture</a> •
    <a href="#technologies">Technologies</a> •
    <a href="#getting-started">Getting Started</a> •
    <a href="#usage">Usage</a> •
    <a href="#documentation">Documentation</a> •
    <a href="#roadmap">Roadmap</a> •
    <a href="#contributing">Contributing</a> •
    <a href="#license">License</a>
  </p>
  <p>
    <img src="https://img.shields.io/badge/Rust-1.70%2B-orange" alt="Rust Version" />
    <img src="https://img.shields.io/badge/Django-4.2%2B-green" alt="Django Version" />
    <img src="https://img.shields.io/badge/Next.js-14.0%2B-black" alt="Next.js Version" />
    <img src="https://img.shields.io/badge/PostgreSQL-14%2B-blue" alt="PostgreSQL Version" />
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT" />
  </p>
</div>

## Overview

SmartCarDiag is a comprehensive vehicle diagnostic system that connects to your car's OBD-II port to provide real-time diagnostics, troubleshooting, and AI-powered analysis. It's designed to help vehicle owners, mechanics, and automotive enthusiasts understand car problems in plain language and make informed decisions about repairs.

Available in English (🇬🇧), Arabic (🇸🇦), and Swedish (🇸🇪).

<div align="center">
  <img src="docs/images/dashboard-screenshot.png" alt="SmartCarDiag Dashboard" width="800" />
</div>

## Features

### 🔍 Advanced Diagnostics
- Real-time Diagnostic Trouble Code (DTC) scanning and interpretation
- Live vehicle data monitoring (RPM, speed, temperature, etc.)
- Comprehensive database of 10,000+ error codes
- Multi-vehicle profile management

### 🤖 AI-Powered Analysis
- Plain language explanations of technical issues
- AI-generated repair recommendations and cost estimates
- Severity assessment of detected problems
- Identification of related issues and root causes

### 📊 Detailed Reporting
- Generate PDF diagnostic reports
- Share results via QR codes, email, or WhatsApp
- Historical data tracking and trend analysis
- Before/after comparisons for repairs

### 🔌 Connectivity
- Support for Bluetooth, WiFi, and USB OBD-II adapters
- Cloud sync for accessing diagnostics across devices
- Offline capability for field diagnostics
- Secure data storage and privacy controls

## Architecture

SmartCarDiag uses a three-tier architecture:

1. **Rust Core**: High-performance system core that communicates with OBD-II devices, processes diagnostic data, and maintains the DTC database.

2. **Django Backend**: Provides RESTful API services, handles user authentication, manages the database, and integrates with AI services.

3. **Next.js Frontend**: Responsive user interface with multi-language support, real-time data visualization, and intuitive diagnostic workflows.

<div align="center">
  <img src="docs/images/architecture-diagram.png" alt="SmartCarDiag Architecture" width="650" />
</div>

## Technologies

### Core System (Rust)
- Rust 1.70+
- OBD-II communication libraries
- JSON processing
- Multithreaded data handling

### Backend (Django)
- Django 4.2+ with Django REST Framework
- PostgreSQL 14+
- Celery for asynchronous tasks
- OpenAI/HuggingFace for AI integration

### Frontend (Next.js)
- Next.js 14+
- TypeScript
- Tailwind CSS
- React-Query for data fetching
- Chart.js for data visualization

### DevOps
- Docker and Docker Compose
- GitHub Actions for CI/CD
- Nginx for production deployment

## Getting Started

### Prerequisites

- Docker and Docker Compose
- OBD-II adapter (ELM327 compatible - Bluetooth, WiFi, or USB)
- A vehicle with OBD-II support (generally all cars made after 1996)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/smartcardiag.git
   cd smartcardiag

Create environment variables file:
bashcp .env.example .env
# Edit .env with your configuration

Build and start the containers:
bashdocker-compose up -d

Access the application:
Frontend: http://localhost:3000
API: http://localhost:8000/api


Development Setup
For developers who want to contribute or modify the system:

Set up Rust development environment:
bashcd rust_core
cargo build

Set up Django development environment:
bashcd django_backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

Set up Next.js development environment:
bashcd nextjs_frontend
npm install
npm run dev


Usage
Connecting to Your Vehicle

Plug your OBD-II adapter into your vehicle's OBD port (usually under the dashboard)
Turn on your vehicle's ignition
In the SmartCarDiag app, go to "Settings" > "Connection"
Select your connection method (Bluetooth, WiFi, or USB)
Follow the on-screen instructions to complete the connection

Running a Diagnostic Scan

From the dashboard, select "Diagnostic Scan"
Choose the vehicle you want to scan
Click "Start Scan" and wait for the process to complete
Review the identified issues, complete with AI analysis and recommendations

Monitoring Live Data

Navigate to "Live Data" in the main menu
Select which parameters you want to monitor
Start recording to track data over time
Export data as CSV or generate graphs for analysis

Documentation
Full documentation is available in the /docs directory:

User Guide
API Documentation
Developer Guide
Troubleshooting

Roadmap
Q2 2025

Voice command integration
Mobile app release (iOS and Android)
Advanced vehicle performance analysis

Q3 2025

Mechanic marketplace integration
Predictive failure analysis
Enhanced diagnostic accuracy

Q4 2025

Integration with vehicle service records
VIN-based vehicle history reporting
Community diagnostics database

Contributing
We welcome contributions from the community! Please see our Contributing Guidelines for more details on how to get involved.
License
This project is licensed under the MIT License - see the LICENSE file for details.
Acknowledgements

ELM327 Documentation
OBD-II PIDs Reference
OpenAI for AI models
All open-source libraries and tools used in this project


<div align="center">
  <p>Made with ❤️ by <a href="https://github.com/yourusername">Abdulwahed Mansour</a></p>
  <p>Support: <a href="mailto:abdulwahed.sweden@gmail.com">abdulwahed.sweden@gmail.com</a></p>
</div>
```
