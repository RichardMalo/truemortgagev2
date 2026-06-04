# 📊 Debt Strategy Engine — True Mortgage v2

An elite, high-fidelity client-side financial forecasting dashboard engineered to model complex debt amortization, property holding costs, and accelerated payoff strategies. From standard home purchase scenarios to complex revolving credit card debt, this application delivers institutional-grade calculations wrapped in a premium, highly responsive user interface.

### 🔗 Try the Live Application
To explore the live interactive application, **[click here to view the live dashboard](https://richardmalo.github.io/truemortgagev2/)**.

---

## ✨ Features Breakdown

### 🎯 Dual Calculation Engines
* **Mortgage & Property Engine:** Models property acquisitions, cash down payments, contract terms, compounding configurations, and mortgage insurance.
* **Credit Card & Revolving Debt Engine:** Simulates repayment timelines for revolving credit balances under regional minimum payment laws (such as Ontario's standard 3% rule vs. Quebec's legal 5% floor).

### ⚙️ Multi-Region Jurisdictional Logic
The engine dynamically adapts to regional banking regulations using an intuitive custom flag selector:
* **Canada:** Computes fixed mortgages using semi-annual compounding as mandated by Canadian banking law (mitigating effective annual interest yields).
* **USA, UK, AU, & NZ:** Calculates interest using standard monthly/daily compounding regimes.

### 🚀 Amortization Compression & Acceleration
* **Advanced Frequencies:** Models Standard Monthly, Semi-Monthly (24/yr), Bi-Weekly (26/yr), and Accelerated Bi-Weekly structures.
* **Capital Surplus Injections:** Models regular, discretionary extra payment cycles applied directly toward principal reduction, completely bypassing interest-charging mechanisms.

### 📈 Modern Wealth Optimizations
* **Opportunity Cost Simulator:** A sophisticated net-worth modeling engine that compares the financial return of aggressive debt payoff against allocating the same surplus cash flow to passive index fund investments (e.g., compounding S&P 500 average yields).
* **Rate Shock Resilience Test:** Allows homeowners to stress-test their active mortgage term against impending rate hikes at renewal, predicting exact payment shocks and budget variances.

### 🎨 Visual & Analytical Dashboard
* **Dynamic Bento Grid:** A responsive, gorgeous dashboard utilizing modular glassmorphism, dynamic shadow profiles, and fluid transition states. Bento cards can be grabbed, dragged, and swapped across grid slots to fully customize your analytical workspace.
* **Visual Blueprint Stack:** Rendered concentric circles and interactive breakdown stacks displaying real-time comparisons of baseline vs. compressed amortization.
* **Advanced Charting (Plotly.js):** Fluid, interactive linear and bar charts plotting outstanding principal, cumulative interest, and net worth comparisons over time.
* **High-Fidelity Amortization Table:** Interactive schedule mapping principal reduction, absolute interest decay curves, and extra payment efficiency metrics across every active cycle step.
* **Table Label Selector (DATE vs PERIOD):** A segmented pill control allowing users to toggle table row headers between chronological calendar dates (e.g., `Jun 1, 2026`) and numerical cycle periods (e.g., `P1`, `P2`, `P3...`), fully supported in both Simple and Advanced Modes.
* **Annual Bank Wages (Descending Circle Chart):** A wrapping, horizontal sequence of visual circles of descending sizes representing interest payments grouped by calendar year. It features area-based (square-root) scaling, custom glassmorphic styling, responsive wrapping, and a run-rate back-fill algorithm for mortgages starting mid-year (extrapolating the first year's annual run-rate). It includes a premium segmented switch toggle allowing users to instantly transition the chart between Annual Bank Wages and Monthly Rent Equivalent interest values.
* **Snapped PC & Mobile Responsive Layouts:** Optimized for all screen sizes, including a custom snapped desktop breakpoint (769px to 1150px) where selectors, region dropdowns, and tools automatically scale down to fit side-by-side on a single row without wrapping.
* **One-Click PDF Reports (html2pdf.js):** Generate clean, professional financial planning brochures directly in the browser.

### 📂 Multi-Scenario Sandbox (Profile Manager)
* **Named Financial Blueprints:** Save, clone, rename, and delete multiple distinct financial profiles (e.g., "30-Year Baseline", "Aggressive 15-Year Payoff", "Refinance at 4.5%").
* **Side-by-Side Compare Mode:** Compute parallel amortization schedules in the background, rendering solid active lines alongside dashed purple comparative traces on Plotly charts simultaneously.
* **Row-by-Row Delta Badges:** Displays floating, sub-pixel savings indicators (e.g., `-$35,200` in green if ahead, or `+$12,400` in red if trailing) directly underneath amortization ledger outstanding balance columns.
* **Glassmorphic Sliding Panel:** Features a premium right-sliding management sheet triggered by a folder icon `📂` next to the country selector in the main header, complete with responsive mobile full-bleed designs and spring GSAP transitions.
* **Session Persistence & Backwards Compatibility:** Automatically preserves the entire profile registry inside `localStorage` across page loads and blueprint syncs, including a legacy data-migration pipeline for returning users.

### 🔒 Private Session Persistence & Operations
* **Automatic LocalStorage Cache:** Safely caches your exact calculation parameters, active modes, themes, complexity levels, customized drag-and-drop card layouts, and custom rate shock inputs on your local browser. Calculations resume instantly upon revisiting the page without sending any private financial data to a web server.
* **Unified Deep Cleanse Reset:** Prompts confirmation and executes a thorough cleanse across both the sidebar Reset button and settings menu. Wipes localStorage caches, restores bento draggable visual blocks to their default sequence, resets all inputs to mortgage baselines, and visually synchronizes all button selectors (tabs) back to Simple and Mortgage mode configurations instantly.

### 🔑 Secure Sync & Portability (JSON Backups)
* **JSON Strategy Blueprints:** Export and import your customized debt strategies as standard JSON files to back up your custom scenarios. All data remains 100% private in local storage.
* **PBKDF2 & AES-GCM 256-bit Encryption:** Protect sensitive financial details by choosing to encrypt files with a custom passcode before downloading. Key derivation (SHA-256, 100,000 iterations) and symmetric encryption are executed fully client-side using browser-native Web Crypto APIs.
* **Premium Drag-and-Drop Dropzone:** Styled with interactive hover and drag transitions, making importing backups extremely intuitive and visual.

### ⚙️ System Settings Dropdown & Modals
* **Centrally Centered Settings Gear:** Integrates a smooth, rotating settings gear dropdown `⚙️` next to the main title. This groups sync portability, constraints, and system resets under a single elegant control.
* **Sleek Overlay Modals:** Consolidates advanced operational explanation guides (Engine Constraints & Limits) and sync dropzones into gorgeous overlay modals utilizing elastic GSAP opening animations.

---

## 🛠️ Technology Stack

This application is built as a self-contained, zero-dependency, ultra-fast client-side dashboard maximizing modern browser capabilities:

* **Markup & Structure:** Semantic HTML5
* **Design System & Styling:** Vanilla CSS3 using custom properties (Variables), standard flex/grid layouts, custom keyframes, and light/dark theme tokens.
* **Core Logic Engine:** ES6+ JavaScript
* **Motion & Micro-animations:** **GSAP** (GreenSock Animation Platform) for high-performance entry animations and spring curves.
* **Data Visualization:** **Plotly.js** for custom responsive charting.
* **Document Engine:** **html2pdf.js** for high-fidelity client-side PDF generation.

---

## 💻 Local Development & Deployment

Since the engine is fully client-side and serverless, it has no complex build steps or external package dependencies.

### Running Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/RichardMalo/truemortgagev2.git
   ```
2. Open the directory:
   ```bash
   cd truemortgagev2
   ```
3. Open `index.html` directly in your favorite web browser, or serve it using a lightweight local development server (e.g., Live Server in VS Code, or python's http module):
   ```bash
   # Python 3
   python -m http.server 8000
   ```
   Then navigate to `http://localhost:8000`.

### Deploying to GitHub Pages
To publish changes to GitHub Pages under the provided URL:
1. Make sure GitHub Pages is enabled in your repository settings:
   * Go to **Settings** -> **Pages** on your GitHub repository.
   * Under **Build and deployment**, set the source to **Deploy from a branch**.
   * Select the `main` branch and the `/ (root)` folder, then click **Save**.
2. Any subsequent commits pushed to the `main` branch will automatically build and update the live dashboard!

