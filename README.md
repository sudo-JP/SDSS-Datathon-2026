# SDSS Datathon 2026 — Airfare Markets Under Pressure

Website: https://kienngyen.github.io/SDSS-Datathon-2026/

## Prerequisites

- Python 3.12+
- Node.js 20+

## Setup & Run

### 1. Install Python dependencies (for notebooks/analysis)

```bash
pip install -r requirements.txt
```

### 2. Install frontend dependencies

```bash
cd frontend
npm install --legacy-peer-deps
```

### 3. Start the dev server

```bash
npm run dev
```

Open `http://localhost:5173` in your browser.

### 4. Build for deployment (GitHub Pages)

```bash
npm run build
```

Static files will be in the `frontend/dist/` folder.

## Project Structure

```
├── models.ipynb                    # Main model notebook (ExtraTrees, XGBoost, walk-forward CV)
├── context.txt                     # Case problem statement
├── Airline Tickets Case.pdf        # Original competition brief
├── requirements.txt
│
├── data/                           # All raw & processed data
│   ├── airline_ticket_dataset.csv  # Primary dataset used by models.ipynb
│   ├── airline_ticket_dataset.xlsx # Excel version of the primary dataset
│   ├── airline_ticket_data.csv     # Alternate raw data used by EDA (dang)
│   ├── carriers.csv
│   ├── flight_route.csv
│   └── database/
│       └── create_airline_ticket_table.sql
│
├── eda/                            # Exploratory data analysis notebooks
│   ├── airline_eda_dang.ipynb
│   ├── airline_eda_jason.ipynb
│   └── airline_eda_kien.ipynb
│
├── images/                         # Auto-generated charts from models.ipynb
│   ├── feature_importance_comparison.png
│   └── route_pricing_analysis.png
│
└── frontend/                       # React + Vite interactive map
    ├── src/
    │   ├── components/             # USMap, MapContainer, RouteStats, TimeFilter
    │   ├── data/                   # Static JSON (airport coords, TopoJSON, routes)
    │   ├── App.tsx
    │   └── main.tsx
    ├── package.json
    └── vite.config.ts
```
