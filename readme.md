# 🏮 Pasar Malam Tycoon

[![Live Demo](https://img.shields.io/badge/demo-online-brightgreen.svg)](https://pasar-malam-tycoon.netlify.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Built With](https://img.shields.io/badge/Frontend-HTML%2FJS%2FTailwind-blue.svg)](https://pasar-malam-tycoon.netlify.app/)

**Pasar Malam Tycoon** is an interactive, browser-based business management simulation game inspired by the vibrant culture of Southeast Asian night markets (*pasar malam*). 

Step into the shoes of a local food vendor, starting with a humble single stall selling classic treats like *Apam Balik*. Manage inventory, adjust pricing based on weather and foot traffic forecasts, navigate customer demand, minimize food waste, and reinvest your hard-earned profits to expand into a booming two-lot night market enterprise!

---

## 🎮 Play Now

Play the game directly in your web browser:  
👉 **[https://pasar-malam-tycoon.netlify.app/](https://pasar-malam-tycoon.netlify.app/)**

---

## ✨ Features

- **Realistic Night Market Simulation:** Watch customer traffic flow past your stall in real time as weather and price sensitivity dictate buying decisions.
- **Inventory & Pricing Strategy:** Balance supply and demand. Buying too much stock risks unsold food decay, while setting prices too high turns customers away.
- **Dynamic Weather & Traffic Events:** Rain, high humidity, festivals, or quiet weekday evenings directly influence customer volume and dish preferences.
- **Stall Upgrades & Menu Expansion:** Start with basic items like *Apam Balik*, then expand your menu to include high-margin favorites (*Ramly Burgers*, *Air Balang*, *Ayam Gunting*, *Satay*, and *Laksa*).
- **Financial Ledger & Analytics:** Review daily summaries showing gross revenue, inventory expenses, waste penalties, overhead costs, and net profit margins.
- **Automated Saving:** Your progress and night market tier are saved automatically in your browser's local storage.

---

## 🕹️ How to Play

1. **Check the Daily Forecast:** Inspect the evening's weather forecast (Clear, Cloudy, Rainy) and expected foot traffic level (Low, Moderate, High).
2. **Stock & Price Setup:**
   - Purchase ingredients for the night based on predicted demand.
   - Set your unit selling price for each menu item.
3. **Run the Night:** Start the night market simulation and observe live customer orders and sales velocity.
4. **End-of-Day Ledger:** Review your daily financial report to identify profit margins and inventory waste.
5. **Expand Your Empire:** Use your profits to unlock new menu items, upgrade cooking equipment, hire helpers, or expand to a 2-lot stall!

---

## 📊 Economic & Demand Mechanics

Customer purchasing behavior is governed by price elasticity of demand, weather multipliers, and stall reputation.

### Daily Net Profit Equation
The daily profit $\Pi$ for a night is calculated as:

$$\Pi = \sum_{i=1}^{n} (Q_{\text{sold}, i} \times P_i) - \sum_{i=1}^{n} (Q_{\text{bought}, i} \times C_i) - O$$

Where:
- $Q_{\text{sold}, i}$: Quantity of item $i$ sold during the night ($Q_{\text{sold}, i} \le Q_{\text{bought}, i}$)
- $P_i$: Retail price set for item $i$
- $Q_{\text{bought}, i}$: Stock quantity purchased at the start of the day
- $C_i$: Unit cost of inventory for item $i$
- $O$: Fixed daily stall rent and overhead costs

### Demand Factor
The effective customer demand $D_i$ for item $i$ follows:

$$D_i = T \times W \times \left( \frac{P_{\text{market}, i}}{P_i} \right)^{\epsilon}$$

Where:
- $T$: Base foot traffic parameter
- $W$: Weather multiplier (e.g., rainy weather reduces cold beverage demand but boosts warm soup demand)
- $P_{\text{market}, i}$: Average baseline market price for item $i$
- $\epsilon$: Price elasticity exponent ($\epsilon > 1$)

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (ES6+) / React, Tailwind CSS
- **State Management & Persistence:** Browser `localStorage`
- **Deployment:** Netlify Continuous Deployment

---

## 💻 Local Development Setup

To run Pasar Malam Tycoon locally on your machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/pasar-malam-tycoon.git
   cd pasar-malam-tycoon
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the local development server:**
   ```bash
   npm run dev
   ```

4. **Build for production:**
   ```bash
   npm run build
   ```

---

## 🤝 Contributing

Contributions, feature suggestions, and pull requests are welcome!  
If you find a bug or have a feature idea (such as new food items or weather events), feel free to open an issue or submit a PR.

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
