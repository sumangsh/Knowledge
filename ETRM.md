# 1. ETRM (Energy Trading and Risk Management)

**ETRM** stands for **Energy Trading and Risk Management.**
It is software used by companies that trade energy products such as:
- Crude oil
- Natural gas
- Electricity
- LNG
- Power derivatives
- Renewable energy certificates

## What ETRM systems do

An ETRM platform typically manages the full lifecycle of an energy trade:

1. **Trade Capture –** recording deals made by traders
2. **Position Management –** tracking exposure in the market
3. **Risk Management –** calculating market risk (VaR, P&L)
4. **Scheduling & Logistics –** pipeline flows, power delivery schedules
5. **Settlement & Invoicing –** financial settlement with counterparties
6. **Regulatory Reporting**


In **ETRM (Energy Trading and Risk Management)** systems, traders use different **deal types** depending on how they want to buy, sell, hedge, or structure energy contracts.

Below are the **main deal types used by energy traders.**

## 1. Physical Deals
These involve **actual delivery of energy commodities.**

**Example**
* Buying **crude oil** from a supplier and delivering it to a refinery.
* Selling **electricity** to a utility.

### __Characteristics__
* Delivery location
* Delivery period
* Volume
* Transport logistics
  
### **Typical commodities**
* Oil
* Gas
* Power
* LNG

## 2. Financial Deals (Derivatives)

These deals **do not involve physical delivery**. They are mainly used for **hedging price risk or speculation.**

### __Examples__
* Futures
* Options
* Swaps

Example:
A trader locks the future price of natural gas using a **swap contract.**

## 3. Fixed Price Deals
The price is **fixed at the time of the trade.**

### Example
Buy 10,000 barrels of crude oil at **$75 per barrel** for next month delivery.
### Used for
- Price certainty
- Budget planning
  
## 4. Floating Price Deals
Price is **linked to a market index** and changes with market conditions.

### Example
Price = **Brent index + $2 premium**

Common indexes:
- [Brent Crude Oil Benchmark](#brent-crude-oil-benchmark)
- [Henry Hub Natural Gas](#henry-hub-natural-gas)

## 5. Swap Deals
A __swap__ exchanges one price type for another.

### Example
- Fixed price vs floating price

Trader may pay fixed price and receive floating price.
Used for:
- Hedging market price fluctuations.

## 6. Option Deals
Options give the **right but not obligation** to buy or sell.

### Types
- Call option (right to buy)
- Put option (right to sell)

Example:
A trader buys a **call option** to purchase crude oil at $80 if the market price increases.

## 7. Spread Deals
Spread trading means **trading the price difference between two markets or products.**

### Example
- Brent vs WTI crude price spread.

Example benchmark:
- [West Texas Intermediate](#west-texas-intermediate)

## 8. Storage Deals
Used when traders **store energy** commodities and sell later.

### Example:
- Buy gas in summer
- Store in storage facility
- Sell in winter when price rises
  

## 9. Transportation Deals
Deals related to **moving energy commodities.**

Examples:
- Pipeline capacity contracts
- Shipping agreements
- Power transmission contracts

## 10. Structured Deals
Complex deals combining **multiple financial instruments.**

Example:
- Swap + option combination
- Multi-leg trades
- Portfolio hedging

These are common in large energy trading firms.

## Simple trader workflow in ETRM

1. Trader executes a deal
2. Deal is captured in the ETRM system
3. Risk team calculates exposure
4. Scheduling team manages delivery
5. Finance performs settlement


# 🔁 Full ETRM Trade Lifecycle (Front → Mid → Back Office)

Think of it as a pipeline:
👉 **Trade Execution → Risk Control → Settlement & Accounting**

## 🟢 1. Front Office (FO) – Traders & Deal Capture

This is where **money-making decisions happen.**

### Who works here
- Traders
- Trading assistants
- Structurers

### What happens

1. **Market Analysis**
   - Prices (oil, gas, power)
   - Supply/demand
   - News & geopolitical events

2. **Trade Execution**
    - Trader agrees on a deal with a counterparty
3. **Trade Capture in ETRM**
    - Deal entered into system (e.g., Endur)
    - Includes:
        - Counterparty
        - Volume
        - Price (fixed/floating)
        - Delivery dates
        - Location

### Example
- Buy LNG at floating price (Brent + premium)
- Sell power forward for next quarter

### Key Output
👉 **A validated trade record in the system**

## 🟡 2. Mid Office (MO) – Risk & Control
This is the **control center** that ensures traders don’t take excessive risk.

### Who works here
- Risk analysts
- Market risk managers
- Credit risk teams

### What happens
1. **Market Risk Management**
- Calculate:
    - P&L (Profit & Loss)
    - VaR (Value at Risk)
- Monitor exposure to price changes

2. **Credit Risk**
- Check counterparty creditworthiness
- Set trading limits

3. Trade Validation
- Ensure trade entered correctly
- Confirm with counterparty

4. **Hedging Decisions**
- Reduce risk using:
    - Swaps
    - Options
    - Futures

### Example
- If gas price risk is high → hedge using swap

### Key Output
👉 **Risk reports + validated & controlled trades**

## 🔵 3. Back Office (BO) – Operations & Settlement
This is where **actual money and physical delivery happen.**
### Who works here
- Operations team
- Settlement analysts
- Accountants

### What happens
1. **Scheduling (Physical Trades)**
    - Plan delivery:
    - Pipelines (gas)
    - Ships (oil/LNG)
    - Power grids
2. **Confirmations**
    - Send official contract confirmation to counterparty
3. **Settlement & Invoicing**
    - Calculate payable/receivable amounts
    - Generate invoices
4. **Accounting**
    - Post entries to finance systems
    - Track revenue, costs, P&L
### Example
- Deliver 1 million MMBtu gas → invoice buyer

### Key Output
👉 **Cash flow + completed delivery**

## 🔄 End-to-End Example

#### Step 1 (Front Office)
- Trader buys crude oil at $75/barrel

#### Step 2 (Mid Office)
- Risk team checks exposure
- Hedges using a swap

#### Step 3 (Back Office)
- Oil is shipped
- Invoice is generated
- Payment is received


# 🔮 1. How Traders Calculate / Estimate Future Prices
There’s no single formula—pricing depends on the market—but most methods are based on **market curves + financial theory.**

## 🧮 A. Futures Pricing (Cost-of-Carry Model)
For commodities like oil or gas, a common model is:
    **Futures Price = Spot Price + Carry Costs**

Carry costs include:
- Storage cost
- Financing (interest rate)
- Insurance
- Minus any income (like convenience yield)

### Simplified formula
$$
F=S \times e^{(r+ \text{storage}− \text{yield}) \times t}
$$

Where:
- F = Futures price
- S = Spot price
- r = interest rate
- t = time

👉 This is based on the Cost of Carry Model





<br/>
<br/>
<br/>

## Brent Crude Oil Benchmark
The **Brent Crude Oil Benchmark** is one of the world’s primary pricing standards for crude oil, representing a blend of oils from fields in the North Sea. It serves as a global reference for pricing two-thirds of internationally traded crude, influencing contracts, futures, and energy economics worldwide.

### Key Facts
- **Type:** Crude oil pricing benchmark
- **Region:** North Sea (UK sector)
- **Administered by:** Intercontinental Exchange
- **Introduced:** Early 1980s
- **Blend composition:** Brent, Forties, Oseberg, Ekofisk, and Troll fields

### Origins and Composition
The Brent benchmark originated from the Brent oil field discovered by Shell plc and ExxonMobil in the UK North Sea during the 1970s. Over time, as production from the original field declined, the benchmark evolved into the Brent Blend, now including multiple North Sea grades—Brent, Forties, Oseberg, Ekofisk, and Troll (collectively known as BFOET). This diversification maintains volume and reliability for pricing.

### Role in Global Oil Markets
Brent serves as a reference price for most crude oils produced outside North America. It underpins contracts for physical oil cargoes, financial derivatives, and over-the-counter swaps. The benchmark’s importance stems from its transparency, liquidity, and use in Organization of the Petroleum Exporting Countries pricing models, as well as its influence on global fuel costs.

### Pricing Mechanism
Pricing is determined through physical trading in the North Sea and financial instruments traded on the Intercontinental Exchange. The price reflects market supply-demand dynamics, geopolitical risks, and global economic trends. Futures contracts on ICE Brent Crude enable producers, refiners, and investors to hedge against volatility.

### Comparison and Influence
Brent is often compared with West Texas Intermediate (WTI) and Dubai Crude Benchmark. While WTI reflects U.S. inland pricing, Brent’s seaborne status makes it more representative of international trade flows, cementing its role as the primary global oil benchmark.


## Henry Hub Natural Gas
Henry Hub Natural Gas is the primary pricing benchmark for natural gas in the United States. Located in Erath, Louisiana, the hub is the official delivery point for New York Mercantile Exchange (NYMEX) natural gas futures contracts. Its prices influence wholesale natural gas markets across North America and serve as a global reference point for LNG trade.

### Key Facts
- **Location:** Erath, Louisiana
- **Operated by:** Sabine Pipe Line Co.
- **Benchmark use:** Reference for NYMEX Natural Gas Futures
- **Pipeline connections:** 16 major interstate and intrastate systems
- **Currency of trade:** U.S. dollars per million British thermal units (MMBtu)

### Infrastructure and Location
Henry Hub is a physical interconnection of multiple pipeline systems, making it a key junction in the U.S. natural gas network. The site links production from the Gulf Coast to regional and national markets, enabling efficient gas flow and providing the physical foundation for price discovery.

### Market Role
The hub’s spot and futures prices form the basis for natural gas contracts in the U.S. and beyond. CME Group lists standardized Henry Hub futures, enabling producers, utilities, and financial institutions to hedge price risk. These contracts are settled in physical delivery at the hub or financially, depending on participants’ needs.

### Global Influence
Henry Hub pricing underpins numerous liquefied natural gas (LNG) export contracts, especially from U.S. terminals. As LNG exports expand, the benchmark increasingly affects international gas markets, competing with indices like Title Transfer Facility (TTF) in Europe and Japan-Korea Marker (JKM) in Asia.

### Price Volatility and Drivers
Henry Hub prices fluctuate with factors such as weather-driven demand, storage levels, production trends, and pipeline capacity. The benchmark thus provides real-time insight into North American supply–demand balance and energy market dynamics.


## West Texas Intermediate
West Texas Intermediate (WTI) is a benchmark grade of crude oil and a key financial index for pricing U.S. and global petroleum. Quoted in U.S. dollars per barrel, it reflects market expectations for supply, demand, and economic activity. Traders, refiners, and policymakers track WTI closely as a barometer of energy and inflation trends.

### Key facts
- **Type:** Light, sweet crude (≈40° API, low sulfur)
- **Benchmark hub:** Cushing, Oklahoma
- **Trading venue:** New York Mercantile Exchange (CME Group))
- **Typical 2026 spot range:** About $60–65 USD per barrel
- **Historical low/high:** –$36.98 (2020) / $145.31 (2008)

### Characteristics and benchmark role
WTI’s “light” and “sweet” properties make it inexpensive to refine into gasoline, diesel, and jet fuel. It serves as the principal price benchmark for North American crude, complementing Brent Crude in Europe and Dubai Crude in Asia. Physical settlement occurs at Cushing, Oklahoma, a critical storage and pipeline nexus connecting U.S. fields to refineries.

### Market function and trading
WTI is primarily traded through futures contracts on the NYMEX Light Sweet Crude Oil Futures. These contracts underpin spot and forward prices used in global energy commerce. The benchmark also anchors derivative products such as exchange-traded funds and contracts-for-difference, allowing investors to hedge or speculate on oil price movements without handling physical barrels.

### Economic significance
As a financial index, WTI mirrors both domestic production dynamics—particularly U.S. shale output—and international events such as supply disruptions or policy shifts by OPEC. Because energy costs feed into transportation and manufacturing, WTI fluctuations influence inflation, corporate earnings, and central-bank outlooks worldwide. Its liquidity and transparency make it one of the most watched commodity indicators across financial markets.