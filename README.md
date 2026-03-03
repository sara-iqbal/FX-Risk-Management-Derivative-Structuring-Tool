

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

---

### **Final Instructions for GitHub:**

1. **Name the file:** `README.md`.
2. **The Image:** Save your graph from Colab as `chart.png`, upload it to your GitHub repo, and replace `your_image_link_here` with the filename `chart.png`.
3. **Add your Code:** Upload your `.ipynb` file to the same folder.

**Would you like me to draft a high-impact LinkedIn post for you to share this project with your network and Freddie?**
