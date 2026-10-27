# UrbanIQ — AI Urban Resource Optimization Dashboard

**UrbanIQ** is a high-fidelity, production-quality, responsive single-page web dashboard for monitoring and optimizing municipal resource distribution: **Waste Fleet Route Optimization**, **Predictive Water Grid Leak Detection**, and **Smart Energy Load Balancing**.

Inspired by modern SaaS analytics platforms and smart-city operations control rooms, UrbanIQ is built entirely in a self-contained root-level `index.html` with zero build steps, zero local dependencies, and zero API keys—ready for instant static hosting on **GitHub Pages** or direct browser viewing.

---

## 🚀 Live Demo & Key Features

### 1. Global Command Center (Overview)
- **Citywide Optimization Score Meter:** Live multi-sector efficiency index (94.8% Nominal).
- **Cross-Sector KPI Scorecards:** Real-time metrics for fleet route efficiency, water integrity, electrical demand buffer, and monthly economic/carbon savings.
- **Multi-Sector Urban Flux Radar Chart:** Compares waste efficiency, water integrity, power stability, carbon offset, and dispatch velocity across 5 municipal districts.
- **AI UrbanIQ Recommendation Engine:** Interactive prescriptive decision cards allowing operators to test actions (e.g. pressure stepdown, battery dispatch, fleet rerouting).
- **Unified Cross-Sector Incident Feed:** Real-time event log with severity filtering (Critical, Warning, Info) and instant "Acknowledge" capability.
- **Neural Telemetry Terminal:** Live operations stream of simulated neural optimization routines.

### 2. Module 01: AI Waste Route Optimization
- **Fleet Metrics:** 28 active collection vehicles, 18 in collection, 10 completed routes, 18.4% fuel savings (~412 L/day).
- **Vector Schematic City Route Map:**
  - Self-contained SVG blueprint displaying urban road hierarchy, waterways, and 4 district zones.
  - Central Municipal Processing & Sorting Depot with animated radar sweep.
  - 8 interactive truck markers (T-101 to T-108) with coordinates, animated pulsing glow, and status tooltips.
  - Completed paths (solid teal) vs active legs (animated dashed cyan) vs AI-optimized bypass paths (neon purple).
  - Map controls: Toggle Traffic Congestion layer, Reset Viewport.
- **Selected Vehicle HUD Panel:** Real-time telematics showing driver, sector, stops remaining, route progress bar, ETA, speed, and fuel efficiency.
- **Interactive Route Optimization:** Click **"Optimize Routes"** to trigger simulated genetic TSP solving, updating routes, recalculating fuel savings (+5.2%), and animating new route trajectories.
- **Fleet Status Table:** Filterable by zone, operational status (Collecting, En Route, Active, Idle), and live search query.

### 3. Module 02: Predictive Water Grid & Leak Forecasting
- **Hydraulic Telemetry:** Monitored pipelines (1,420 km / 480 nodes), 5 active leak alerts, 3 critical risk segments, and 14,250 L/hr estimated water loss prevented.
- **Visualizations:**
  - **Leak Probability Spectrum:** Bar chart highlighting critical segments (SEG-402, SEG-118, SEG-809) with color thresholds (Critical ≥80%, High 60-79%, Moderate 30-59%, Low <30%).
  - **Dual-Axis Hydraulic Telemetry Chart:** 24-hour synchronized Pressure (PSI) vs Flow Rate (L/s) revealing anomalous transient pressure drop at 03:00.
  - **Risk Distribution Doughnut:** Breakdown of all 480 monitored nodes.
- **Priority Mitigation Panel:** Actionable cards with recommended engineering interventions.
- **Pipeline Diagnostic Modal:** Detailed acoustic spectrogram (0-500 Hz), ground moisture readings, and interactive **Simulated Emergency Valve Isolation** control.
- **Interactive Prediction Engine:** Click **"Run Prediction"** to simulate real-time acoustic analysis and update risk metrics.

### 4. Module 03: Metropolitan Energy Load Balancing
- **Power Telemetry:** Current demand (842 MW), peak forecast (965 MW), renewable generation mix (46.8%), and peak shaved (74 MW / $18,400 daily savings).
- **Visualizations:**
  - **Power Demand Over Time:** Responsive area/line chart with baseline forecast, AI-controlled demand curve, and grid safe capacity ceiling (1,050 MW).
  - **Generation Mix Breakdown:** Doughnut chart showing Solar (235 MW), Wind (158 MW), Hydro (68 MW), Battery Storage (35 MW), and Conventional Gas (346 MW).
  - **District Electricity Consumption:** Bar chart comparing 6 municipal zones.
- **Peak Shaving Comparison Widget:** Side-by-side metric comparison of peak demand, peaker plant runtime, grid strain, and capacity cost avoidance.
- **Substation Capacity Meters:** Live horizontal loading progress bars with warning states for industrial, commercial, and residential substations.
- **Interactive Grid Balancing:** Click **"Balance Grid (Peak Shave)"** to dispatch battery reserves, lower the peak demand curve, and reduce substation strain.

### 5. Module 04: Incident Lifecycle & Alarm Center
- Full municipal incident registry with severity counters (Critical, Warning, Info, Resolved).
- Sector filtering across Water, Energy, and Waste.
- Operator actions: **Acknowledge**, **Resolve**, and view event timestamps.

### 6. Module 05: Reports & Compliance Audit Ledger
- Executive compliance scorecard (EPA Clean Water Act, Municipal Decarbonization, NERC Grid Reliability).
- **Downloadable Real CSV File:** Click **"Export CSV"** to generate and download `UrbanIQ_Resource_Audit_Report.csv` directly from client-side state.
- **Print / PDF View:** Dedicated `@media print` stylesheet optimizing the report for clean municipal printing and PDF creation.

### 7. Global Utility Features
- **Live Dynamic Clock:** Real-time clock updating every second.
- **Time-Range Selector:** Working `[24H]`, `[7D]`, and `[30D]` selector that smoothly adjusts all charts and labels.
- **Telemetry Refresh:** Spun sync control introducing realistic micro-variations across telemetry nodes.
- **Notification Center:** Bell icon with unread badge count, dropdown alert list, and "Mark all read" action.
- **Spotlight Search Palette:** Keyboard accessible via `Ctrl + K` or `/` to instantly search and navigate across trucks, pipelines, and alerts.
- **Floating Toast Notification System:** Non-intrusive feedback stack for all simulated actions.
- **Responsive Mobile Drawer:** Fully responsive layout tested across desktop, laptop, tablet, and mobile screens.

---

## 🛠️ Technical Architecture

- **Single Root File:** `index.html` contains all markup, styling, and JavaScript logic.
- **CSS Framework:** [Tailwind CSS](https://tailwindcss.com/) via official browser CDN build with custom theme extensions.
- **Charts & Data Viz:** [Chart.js 4.4](https://www.chartjs.org/) via CDN.
- **Typography:** Google Fonts (*Plus Jakarta Sans* & *JetBrains Mono*).
- **Icons & Graphics:** 100% inline SVG vectors (zero external image requests).
- **JavaScript:** Pure Vanilla ES6+ (no Node.js runtime, build step, bundler, or server dependencies).
- **Hosting Compatibility:** Fully compatible with GitHub Pages, including repository subpaths (`https://<username>.github.io/<repo>/`).

---

## 📦 Deployment Instructions (GitHub Pages)

### Option A: Deploy via GitHub Web Interface
1. Create a new public repository on GitHub (e.g., `urbaniq-dashboard`).
2. Upload `index.html` and `README.md` to the **root** of the repository.
3. In your GitHub repository, navigate to **Settings** → **Pages** (under "Code and automation").
4. Under **Build and deployment**:
   - **Source**: Select `Deploy from a branch`.
   - **Branch**: Select `main` (or `master`) and folder `/(root)`.
   - Click **Save**.
5. Wait 1-2 minutes. Your dashboard will be live at:
   ```
   https://<your-username>.github.io/urbaniq-dashboard/
   ```

### Option B: Deploy via Git CLI
```bash
# 1. Initialize git repository
git init
git add index.html README.md
git commit -m "Initial commit: UrbanIQ Resource Optimization Dashboard"

# 2. Add remote repository and push
git branch -M main
git remote add origin https://github.com/<your-username>/urbaniq-dashboard.git
git push -u origin main
```
Then enable GitHub Pages under **Repository Settings** → **Pages** → **Deploy from branch: main / (root)**.

---

## ⚠️ Disclaimer
All metrics, leak probabilities, route optimizations, and grid balancing actions shown in this application are **simulated demo data** generated locally within the browser. UrbanIQ is an educational and enterprise demonstration platform and does not interface with live physical municipal infrastructure.
