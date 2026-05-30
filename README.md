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
* **United States, United Kingdom, Australia, & New Zealand:** Calculates interest using standard monthly/daily compounding regimes.

### 🚀 Amortization Compression & Acceleration
* **Advanced Frequencies:** Models Standard Monthly, Semi-Monthly (24/yr), Bi-Weekly (26/yr), and Accelerated Bi-Weekly structures.
* **Capital Surplus Injections:** Models regular, discretionary extra payment cycles applied directly toward principal reduction, completely bypassing interest-charging mechanisms.

### 📈 Modern Wealth Optimizations
* **Opportunity Cost Simulator:** A sophisticated net-worth modeling engine that compares the financial return of aggressive debt payoff against allocating the same surplus cash flow to passive index fund investments (e.g., compounding S&P 500 average yields).
* **Rate Shock Resilience Test:** Allows homeowners to stress-test their active mortgage term against impending rate hikes at renewal, predicting exact payment shocks and budget variances.

### 🎨 Visual & Analytical Dashboard
* **Dynamic Bento Grid:** A responsive, gorgeous dashboard utilizing modular glassmorphism, dynamic shadow profiles, and fluid transition states.
* **Visual Blueprint Stack:** Rendered concentric circles and interactive breakdown stacks displaying real-time comparisons of baseline vs. compressed amortization.
* **Advanced Charting (Plotly.js):** Fluid, interactive linear and bar charts plotting outstanding principal, cumulative interest, and net worth comparisons over time.
* **High-Fidelity Amortization Table:** Interactive schedules outlining breakdown changes per period.
* **One-Click PDF Reports (html2pdf.js):** Generate clean, professional financial planning brochures directly in the browser.

### 🔒 Private Session Persistence
* **Automatic LocalStorage Cache:** Safely caches your exact calculation parameters, active modes, themes, complexity levels, and custom rate shock inputs on your local browser. Calculations resume instantly upon revisiting the page without sending any private financial data to a web server. Includes a dedicated "Reset" feature to purge the browser cache instantly.

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

