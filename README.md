# OSI Hospitality — Financial Analysis Dashboard

A premium, interactive, single-page financial analysis dashboard and data consolidation system built for **OSI Hospitality Private Limited** (FY 2026-27). This system processes Trial Balance documents, consolidates weekly Airbnb sales data, computes corporate income tax (adjusted for IT depreciation), tracks property-level performance, and synchronizes state with a Supabase database.

---

## 🚀 Quick Start

Get the local development server up and running in less than 5 minutes:

### 1. Prerequisites
Ensure you have [Node.js](https://nodejs.org/) installed (v18+ recommended).

### 2. Install Dependencies
Clone the repository, navigate into the directory, and install the package requirements:
```bash
npm install
```

### 3. Run Development Server
Start the local Vite development server:
```bash
npm run dev
```
Open your browser and navigate to the address shown in the terminal (usually `http://localhost:5173`).

### 4. Build for Production
To build the static assets optimized for production:
```bash
npm run build
```
Preview the production build locally:
```bash
npm run preview
```

---

## ✨ Features & Dashboard Tabs
The dashboard is structured into 11 specialized views accessible via the top navigation bar:

| Tab | Purpose & Features |
|---|---|
| **Overview** | Executive KPI summary (Revenue, Net Profit, EBITDA, margins) + Chart.js trend charts + Health Indicators (Quick/Current ratio, Debt to Equity). |
| **Sales** | Revenue mix breakdown, monthly sales trends, and sales channel summary table. |
| **P&L** | Auto-generated Profit & Loss statement categorized by Direct/Indirect Expenses, Finance Costs, and Depreciation. |
| **Balance Sheet** | Dynamic Assets, Liabilities & Equity composition with interactive charts and a capital structures bridge. |
| **Top Cost** | Cost ledger rank/concentration and a Month-on-Month (MoM) matrix table of all operating expenditures. |
| **Tax** | Real-time Corporate Income Tax computation at 25.168% of Taxable Profit, with XLSX upload support for *Depreciation as per Income Tax Act*. |
| **Ratios** | Profitability (Gross, Net, Operating Margins) and Liquidity/Leverage ratios calculated on the fly. |
| **Trends** | High-level comparison charts mapping monthly and quarterly operational indicators. |
| **YTD vs LY** | Year-to-Date vs Last Year comparative metrics with visual indicators (▲/▼) mapping growth performance. |
| **Properties** | Listing-specific performance breakdown mapping individual hospitality units and their rental yields. |
| **Sales Register & Data** | Consolidates weekly Excel logs (Airbnb sales, MMT, Direct Sales) into a unified ledger with direct database synchronization. |

---

## 🛠️ Tech Stack & Libraries

To ensure fast load times and maximum control over logic and aesthetics, the project utilizes a lightweight yet robust front-end stack:

*   **Core Architecture**: HTML5 + Vanilla JavaScript + custom Vanilla CSS.
*   **Module Bundler**: [Vite](https://vitejs.dev/) (v5.4.0) for instant hot-module reloading and optimized static asset compilation.
*   **Data Visualization**: [Chart.js](https://www.chartjs.org/) (v4.4.1) for premium animated charts (doughnuts, bars, line graphs).
*   **Excel Parsing Engine**: [SheetJS / XLSX](https://sheetjs.com/) (v0.18.5) for client-side extraction of Trial Balances and sales logs directly from `.xlsx`/`.xls` uploads.
*   **Backend Sync**: [Supabase JS SDK](https://supabase.com/) (v2) for database persistence, version control of trial balances, and consolidated sales registries.

---

## 📂 Supported Data Sources & Excel Layouts

The application ingests and parses specific financial sheets. Sample worksheets are present in the workspace:

1.  **Trial Balances** (`TB_April 2026.xls`, `April 2026_TB.xls`): Contain ledger records mapping codes, account heads, debit/credit balances to compile the P&L and Balance Sheet.
2.  **Airbnb Weekly Sales** (`Airbnb_Sale data 1 Apr to 7 Apr.xlsx` etc.): Raw weekly sales logs parsed by the Sales Register engine to calculate occupancy, gross revenue, hosting fees, and channel payout.
3.  **Income Tax Depreciation** (`Depreciation as per Income Tax Act.xlsx`): Specific depreciation schedules uploaded in the **Tax** tab to recalculate taxable PBT and compute net deferred tax assets/liabilities.

---

## 🔒 Security & Password Protection

To secure confidential financial metrics:
*   The application starts with a full-screen **Password Protection Screen**.
*   Requires a valid username and password pair before mounting the dashboard wrap and executing Supabase API queries.

---

## 📄 License

Private/Proprietary. All rights reserved by **OSI Hospitality Private Limited**.
