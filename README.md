# Chicago Food Inspections 

A full-stack application for viewing, searching, and analyzing Chicago Department of Public Health (CDPH) food inspection data. Built with React + TypeScript frontend and Node.js + Express backend.

---

## 🔍 Project Overview

The Chicago Food Inspections platform transforms raw government inspection data into a
structured, searchable, and interactive system that allows users to explore food safety
records across the city.

Key capabilities include:
- Inspection history lookup by facility
- Risk-level analysis
- Interactive charts and maps
- CRUD-based data management for inspection records

The system improves public transparency, supports data-driven decision-making, and
makes complex inspection data accessible to both citizens and officials.

---

## 🏗️ Architecture

```
├── food-inspections-api/        # Backend API (Node.js + Express)
│   ├── config/                  # Database configuration
│   ├── routes/                  # API endpoints
│   │   ├── facilities.js        # Facility CRUD & search
│   │   ├── inspections.js       # Inspection data
│   │   ├── analytics.js         # Dashboard & visualization data
│   │   └── violations.js        # Violation records
│   ├── server.js                # Express server
│   └── package.json
│
└── frontend/                    # Frontend Application (React + TypeScript)
    ├── src/
    │   ├── api/                 # API client & endpoints
    │   ├── components/          # Reusable React components
    │   ├── features/            # Feature pages
    │   │   ├── dashboard/       # Analytics dashboard
    │   │   ├── facilities/      # Facility management
    │   │   ├── inspections/     # Inspection viewer
    │   │   ├── search/          # Facility search
    │   │   ├── violations/      # Violation history
    │   │   └── visualizations/  # Data visualizations
    │   ├── charts/              # Chart components
    │   ├── theme/               # Material-UI theming
    │   └── main.tsx             # Entry point
    ├── package.json
    └── vite.config.ts
```
---

## 👩‍💻 My Role & Contributions (Primary Focus)

**Role:** Application & Interface Development (Frontend + Integration)

I was responsible for building the **user-facing application layer** and connecting
frontend features to backend APIs and the database.

### Core Contributions
- Designed and implemented the **React-based frontend** using Material UI
- Built responsive dashboards displaying:
  - Total facilities and inspections
  - Risk-level distribution
  - Recent inspection activity
- Developed **interactive data visualizations** using Chart.js
- Implemented **advanced search functionality** with real-time filtering
- Built editable data grids enabling CRUD operations on facilities
- Integrated geographic mapping features with:
  - Risk-based color coding
  - Marker clustering for performance
  - Click-to-view facility details
- Improved performance for large datasets through:
  - Lazy loading
  - Zoom-based filtering
  - Clustered map rendering
- Collaborated closely with backend and database layers to ensure consistent data models


## 🧱 System Architecture (High Level)

- **Frontend:** React 18, Material UI, Chart.js, Leaflet
- **Backend:** Express.js, SQLAlchemy, Pydantic
- **Database:** PostgreSQL 16 with PostGIS
- **Architecture Pattern:** Bronze–Silver–Gold Medallion ETL design

### Data Pipeline
- **Bronze Layer:** Raw CSV ingestion from Chicago Open Data
- **Silver Layer:** Data cleaning, validation, and standardization
- **Gold Layer:** Analytics-ready, normalized schema with spatial indexing

---

## 📊 Key Features Implemented

### Dashboard
- Overview statistics (facilities, inspections, risk distribution)
- Recent inspections table
- Visual summaries for quick insights

### Facilities Management
- Paginated facility listing
- Inline editing and deletion
- Real-time updates across the application

### Advanced Search
- Partial and exact matching
- License number and facility name support
- Integrated CRUD actions

### Visual Analytics
- Risk distribution charts
- Inspection result breakdowns
- Top violations analysis
- Temporal inspection trends

### Geographic Mapping
- City-wide facility map
- Risk-based color-coded markers
- Marker clustering for scalability
- Interactive facility detail views

---

## 🚀 Quick Start

### Prerequisites
- **Node.js** 18+ (LTS)
- **npm** or **yarn**
- **PostgreSQL** 16+ (with food inspections data loaded)

### Environment Setup

1. **Backend Setup** (`food-inspections-api/.env`)
```bash
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
DB_NAME=food_inspections
PORT=3000
NODE_ENV=development
```

2. **Frontend Setup** (uses localhost:3000 by default)

### Installation & Running

**Backend:**
```bash
cd food-inspections-api
npm install
npm run dev
# Server starts at http://localhost:3000
```

**Frontend:**
```bash
cd frontend
npm install
npm run dev
# Application starts at http://localhost:5173
```
---

## 🚧 Deployment Status

The application currently runs in **local development mode only**.

Public deployment was blocked due to:
- PostGIS hosting limitations on free tiers
- Large dataset size (250,000+ records, ~2GB)
- CORS and cross-domain configuration challenges
- Cost constraints for production-grade infrastructure

---

## 🧠 Key Learnings

- Large-scale data cleaning often consumes **50%+ of project effort**
- Performance optimization is critical for geographic visualizations
- Deployment introduces real-world constraints absent in local development
- Maintaining type consistency across backend and frontend is non-trivial
- End-to-end ownership builds deeper system understanding

---

## 🤝 Original Team Project

This work is based on a collaborative academic project developed by a team of three.

🔗 Original Repository:  
https://github.com/adithhari/CDPH-foodinspections
