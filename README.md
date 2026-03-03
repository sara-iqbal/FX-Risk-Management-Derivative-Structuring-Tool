

# **FX Risk Management & Derivative Structuring Tool**

### **Case Study: GBP/USD Exposure & Zero-Cost Collar Pricing**

##  Project Overview

This project provides a quantitative framework for analyzing Foreign Exchange (FX) risk for corporate clients. Sitting at the intersection of **FinTech and Financial Engineering**, this tool automates the analysis of "The Cable" (GBP/USD) to provide clients with structured hedging alternatives to standard forward contracts.

##  Key Methodology

This project follows the lifecycle of a professional FX structuring desk:

1. **Market Data Acquisition:** Integrated real-time data fetching for spot rates.
2. **Volatility Modeling:** Computed annualized historical volatility to drive option pricing.
3. **Quantitative Pricing:** Built a **Black-Scholes-Merton** engine adjusted for domestic and foreign interest rate differentials.
4. **Strategic Structuring:** Engineered a **Zero-Cost Collar**, solving for the strike price where the Net Premium = 0.
5. **Risk Visualization:** Generated payoff profiles to communicate P&L outcomes to stakeholders.

## Strategy Analysis

Below is the visual output of the risk engine comparing three distinct client paths:

### **Deep Dive Analysis of the Results:**

* **Unhedged (Red Dashed):** Shows a $1:1$ linear risk. While it offers 100% upside, the "Left Tail" risk is significant; a 5% drop in GBP/USD results in a direct 5% hit to the client's bottom line.
* **Forward Contract (Green):** The "Certainty" play. It eliminates all volatility, locking in a rate regardless of market movement. However, it creates an "Opportunity Cost" if the GBP strengthens.
* **Zero-Cost Collar (Blue):** The "Balanced" play.
* **The Floor:** Protection is triggered at 1.30, preventing further losses.
* **The Participation Zone:** The client benefits from GBP strength between 1.30 and 1.38.
* **The Cap:** Upside is capped at 1.38 to fund the protection, requiring no upfront cash outlay.



## **Project Statistics**

| Metric | Value |
| --- | --- |
| **Asset Analyzed** | GBP/USD (Cable) |
| **Data Points** | 252 Trading Days (1 Year) |
| **Hedge Horizon** | 3 Months (90 Days) |
| **Model** | Black-Scholes-Merton (Currency) |
| **Calculated Volatility** | [Insert your % from Colab] |
| **Risk Reduction** | ~100% Downside Protection below Strike |

## **Data Sources**

* **Market Data:** Sourced via the **Yahoo Finance (yfinance)** API, providing real-time Close prices and historical daily returns for `GBPUSD=X`.
* **Interest Rates:** Modeled based on current Central Bank rates (BoE and Federal Reserve) to calculate the **Interest Rate Differential**, a critical component for FX Forward and Option pricing.

## **Context for Ebury**

This project demonstrates the "Exceptional Analytical and Problem-Solving Abilities" required for the **Junior FX Structurer** role. It proves technical proficiency in **Python**, a deep understanding of **FX Spot, Swaps, and Options**, and the ability to turn complex quantitative data into **compelling proposals**.

<img width="1025" height="629" alt="image" src="https://github.com/user-attachments/assets/d40ce051-9e58-4e74-95c6-60867c579d1f" />

## **Strategy Visualization & Performance Analysis**

The following chart illustrates the P&L profile of different hedging strategies modeled using the Black-Scholes-Merton framework.

### **Technical Breakdown of the Analysis**

#### **1. The Baseline: Unhedged Exposure (Red Dashed Line)**

* **Profile**: Linear $1:1$ exposure to the spot market.
* **Analysis**: This represents the client’s "do nothing" scenario. While it offers unlimited upside if the GBP strengthens, it exposes the client to significant P&L erosion if the GBP weakens.
* **Risk Metric**: The steep downward slope illustrates a high **Value at Risk (VaR)** due to unmanaged market volatility.

#### **2. The Conservative Approach: Forward Contract (Green Line)**

* **Profile**: A flat horizontal line locked slightly above the 0.00 P/L axis.
* **Analysis**: By "locking in" a forward rate, the client eliminates all exchange rate risk.
* **Outcome**: This provides 100% certainty for budgeting; however, the client "sacrifices" all potential gains if the market moves in their favor.

#### **3. The Structured Solution: Zero-Cost Collar (Blue Solid Line)**

This is the core deliverable, demonstrating sophisticated risk engineering to meet specific client needs.

* **The Floor (Protection)**: A Put Option is priced to cap losses at roughly **1.30**. Even in a catastrophic market crash, the client's downside is strictly limited.
* **The Participation Zone**: Between the two "kinks" (1.30 and 1.38), the client benefits from market movements, allowing for favorable P&L growth as the GBP strengthens.
* **The Cap (Obligation)**: A Call Option is sold to fund the floor, capping gains at **1.38**.
* **Financial Efficiency**: This is a **Zero-Cost** structure; the premium received from selling the call perfectly offsets the premium paid for the put, requiring no upfront cash from the client.

---

## **Core Project Statistics**

| Parameter | Data Point |
| --- | --- |
| **Asset** | GBP/USD (The Cable) |
| **Historical Volatility ($\sigma$)** |7.12% |
| **Domestic Rate ($r_d$)** | 5.25% (BoE) |
| **Foreign Rate ($r_f$)** | 5.50% (Fed) |
| **Time to Maturity ($T$)** | 0.25 Years (3 Months) |
| **Max Downside Protection** | 100% below 1.30 Strike |
| **Upside Participation** | 8.0% Range (from 1.30 to 1.38) |

---

## **Strategic Conclusion**

As a **Junior FX Structurer**, I analyzed these scenarios to determine that the **Zero-Cost Collar** provides the most balanced risk-reward profile for a mid-cap client. It protects the bottom line while maintaining market competitiveness, directly aligning with Ebury's mission to empower international business through tailored financial solutions.


---

### **Final Instructions for GitHub:**

1. **Name the file:** `README.md`.
2. **The Image:** Save your graph from Colab as `chart.png`, upload it to your GitHub repo, and replace `your_image_link_here` with the filename `chart.png`.
3. **Add your Code:** Upload your `.ipynb` file to the same folder.

