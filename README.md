# Emirates Airline: Operational & Financial Leakage Audit

## 📌 Project Overview
This project is a strategic Business Intelligence audit designed to simulate enterprise-level data operations for Emirates Airline. Utilizing a synthetic dataset of *100,000+ bookings* built on a relational database architecture, the analysis moves beyond basic descriptive dashboards to focus entirely on leakage tracking: identifying structural revenue losses, yield anomalies, and operational inefficiencies.

---

## 📊 Data Architecture & Modeling
To manage complex relationships efficiently and maintain a single source of truth, the data model utilizes a *Snowflake Schema*:

* *Fact Table:* emirates_bookings_100k (Contains core transactional records: ticket revenue, cabin class indicators, and booking IDs)
* *Dimension Tables:*
  * emirates_flights: Serves as an operational bridge containing route distances (KM), flight numbers, and real-time schedule statuses (Delayed, Cancelled, On-Time).
  * emirates_airports: Lookup table containing hub codes, departure/destination cities, and international regional data.
  * emirates_passengers: Demographic tracking table containing passenger profile distributions.

---

## 💡 Key Business Insights & Analytical Framework

### 1. Financial Revenue Leakage
* *The Problem:* Non-operational or heavily delayed flights tie up capital and lead to customer compensation costs.
* *The Audit Insight:* Built custom calculated fields to track *"Revenue at Risk"* specifically from flight cancellations, isolating millions in potential leakage. This allows executive leadership to see exactly which flight numbers and routes are draining bottom-line margins rather than just tracking overall sales volume.

### 2. Route Yield Optimization ($/KM Flown)
* *The Problem:* Flat pricing logic over long-haul routes can obscure margin deficits if the ticket price does not accurately scale with operational distance.
* *The Audit Insight:* Evaluated the exact pricing yield relative to route distances. The analysis pinpoints outliers and identifies specific long-haul flights running at low margins, allowing for strategic fare adjustments.

### 3. Structural Vulnerability Map
* *The Problem:* Delays at major international hubs trigger domino-effect logistical logjams.
* *The Audit Insight:* Developed an interactive geospatial map tracking delay distributions by country and city hubs. Selecting a high-risk hub dynamically drills down into localized route data, revealing systemic operational bottlenecks.

---

## 🛠️ Tech Stack & Skills Demonstrated
* *BI & Data Visualization:* Tableau Desktop (Snowflake modeling, multi-layered data joins, custom KPI metrics).
* *Data Modeling:* Advanced relational schema design, filter context control, and performance optimization for 100k+ rows.
* *Business Acumen:* Translating operational aviation metrics into financial impact analytics (Revenue Leakage, Yield Mapping).
