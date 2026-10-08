# Supply Chain Visibility System with Optimization Analytics

> Infosys Virtual Internship | Microsoft Power BI | AIS Data Complete Weather

An end-to-end supply-chain analytics project developed during the Infosys Virtual Internship. The project transforms vessel movement and weather data into interactive Power BI dashboards for transportation visibility, cargo-flow analysis, delivery performance, supplier and transportation analytics, warehouse efficiency, and executive reporting.

## Project at a Glance

| Item | Details |
|---|---|
| Internship | Infosys Virtual Internship |
| Project | Supply Chain Visibility System with Optimization Analytics |
| BI Tool | Microsoft Power BI |
| Dataset | AIS Data Complete Weather |
| AIS observations | ~1.1 million |
| Unique vessels | ~13,000 |
| Core tools | Power BI, Power Query, DAX |
| Milestones | 1–4 |

## Objectives

- Build a structured analytical data model.
- Transform and prepare AIS data using Power Query.
- Develop DAX-based KPIs and operational measures.
- Analyze cargo flow and delivery performance.
- Analyze supplier and transportation activity using documented proxies.
- Evaluate warehouse and destination-level operational performance.
- Build an executive-level Power BI reporting layer.

## Data & Modelling

The dataset contains vessel identification, location, speed, destination, ETA, cargo, and weather information. Important fields include MMSI, VesselName, BaseDateTime, LAT, LON, SOG_kmh, VesselType, ETA_hours, dest_cluster, and weather fields.

Data was prepared in Power Query. Derived fields include:

- Operational_Status — Moving / Stopped
- Speed_Category — Stopped / Slow / Moderate / Fast

The Power BI model follows a star-schema-style structure:

```text
dim_Vessel  ──────>  Fact_Vessel  <──────  dim_Destination
```

## Project Milestones

### Milestone 1 — Data Modelling & KPI Foundation

Created the core Power BI model and Supply Chain Visibility dashboard.

Key measures include:

- Total AIS Records
- Unique Vessels
- Average Speed
- Total Distance
- Average ETA
- Stopped Records
- Stopped %

The dashboard covers vessel activity, operational status, speed categories, destination activity, ETA analysis, weather context, and interactive slicers.

### Milestone 2 — Inventory & Delivery Analytics

Added cargo-flow, inventory-turnover-proxy, and delivery-performance analysis.

Because the AIS dataset does not contain conventional inventory fields such as inventory quantity, COGS, or average inventory value, an **Inventory Turnover Proxy** was developed from moving AIS records and active moving vessels.

The milestone also covers delivery trends, delayed deliveries, regional performance, and vessel-type analysis.

### Milestone 3 — Supplier & Transportation Analytics

Added supplier and transportation analysis using clearly documented operational proxies:

| Business Concept | Proxy Used |
|---|---|
| Supplier | Vessel Name |
| Carrier | Vessel Type |
| Route | Destination Cluster |
| Transportation Cost | Distance-based proxy |
| Supplier Quality | ETA-performance-based proxy |

The dashboard analyzes supplier activity, transportation distribution, carrier/vessel-type activity, route distribution, and operational quality.

### Milestone 4 — Warehouse Analytics & Final Dashboard

Added:

- Warehouse & Operational Efficiency reporting
- Executive Overview
- Destination-wise Operational KPI Summary
- Dashboard performance optimization
- Final testing, documentation, and deployment

## Key Results

| KPI | Result |
|---|---:|
| AIS observations | ~1.1M |
| Unique vessels | ~13K |
| Average vessel speed | 4.36 km/h |
| Total transportation distance | 277.88M km |
| Average ETA | 59.89 hours |
| Stopped observations | 79.64% |
| Moving observations | 20.36% |
| Cargo movement records | ~224K |
| Inventory Turnover Proxy | 66.04 |
| On-Time Rate | 25.56% |
| Operational Utilization Proxy | 20.36% |

### Destination-level findings

The final Operational KPI Summary reports:

- **Destination 5:** 85.99% on-time rate
- **Destination 4:** 15.26% on-time rate
- **Destination 6:** 32.10% operational utilization
- **Destination 1:** 15.71% operational utilization
- **Destination 6:** 8.40 km/h average vessel speed
- **Destination 5:** 27.84 hours average ETA

These figures demonstrate substantial variation in operational and delivery performance between destination clusters.

## Important Assumptions

Several measures in the project are **operational proxies**, not conventional accounting/business measures.

For example, the documentation explicitly defines Vessel Name as a supplier proxy, Vessel Type as a carrier proxy, and an ETA-based measure as a supplier-quality proxy. The Inventory Turnover Proxy is also not a conventional accounting inventory-turnover ratio.

These assumptions should be considered when interpreting dashboard results.

## Technology Stack

- **Microsoft Power BI** — modelling, dashboards and visualization
- **Power Query** — data preparation and transformation
- **DAX** — calculated measures and KPIs
- **Git & GitHub** — version control
- **Git LFS** — large Power BI PBIX storage

## Repository Structure

```text
Supply-Chain-Visibility-and-Optimization-Analytics/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── dashboards/
│   ├── README.md
│   ├── DASHBOARD-ASSETS.md
│   └── Supply-Chain-Visibility-Optimization-Analytics.pbix
│
├── data/
│   └── README.md
│
├── docs/
│   ├── README.md
│   ├── project-documentation.md
│   └── Supply-Chain-Visibility-Optimization-Analytics-Documentation.docx
│
├── notebooks/
│   └── README.md
│
└── src/
    └── README.md
```

## Documentation

The repository contains the complete internship documentation and a project documentation summary covering the data model, DAX measures, dashboards, KPIs, visualizations, business insights, assumptions, performance optimization, testing, and deployment.

## Portfolio & Data Disclaimer

This repository is intended for educational and portfolio documentation. Internship datasets, screenshots, reports, and other materials should only be published when their public distribution is permitted.

Do not commit confidential information, credentials, personal data, or restricted internship material.

## License

Released under the **MIT License** for original repository material that the author has the right to license. Third-party or restricted internship materials remain subject to their respective terms.

## Author

**Faaiz Hamid**

GitHub: [@faaizhamid07](https://github.com/faaizhamid07)
