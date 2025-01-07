# Mining Data with Morlet Wavelets - Historical Crypto Cycle Analysis


# Crypto ETF Formulation

![alt text](image.png)

	Annualized Return	Volatility	Sharpe Ratio	Sortino Ratio	Max Drawdown	Alpha	Beta
Crypto ETF	0.916497	0.652803	1.373304	1.896141	-0.800194	0.647176	1.608164

This document provides the key formulas used for calculating an index out of assets.

---

## 1. Initial Shares Calculation
The number of initial shares to hold for each asset is calculated as:
```math
\text{Initial Shares (per asset)} = \frac{\text{Initial Investment} \times \text{Weight (per asset)}}{\text{Asset Price at Initial Time}}
```

---

## 2. Index Level Calculation
The index level at any time \( t \) is calculated as:
```math
\text{Index Price} = \left( \frac{\text{Total Value of Investments at Time } t}{\text{Initial Total Value}} \right) \times \text{Base Value}
```
Where:
- **Total Value** is the sum of the current value of each asset's investment.
- **Base Value** sets the initial index value (e.g., 100).

---

## 3. Rebalancing Logic
During rebalancing, the following formulas are used:

### Target Investment (per asset):
```math
\text{Target Investment (per asset)} = \text{Total Investment} \times \text{Weight (per asset)}
```

### Transaction Fees:
```math
\text{Transaction Fees} = \text{Delta Shares} \times \text{Price (per share)} \times \text{Transaction Fee Rate}
```

### Delta Shares:
```math
\text{Delta Shares} = \left| \frac{\text{Target Investment (per asset)}}{\text{Current Price (per share)}} - \text{Initial Shares (per asset)} \right|
```

---

## 4. Adjusting Shares After Rebalancing
After rebalancing, the new shares for each asset are calculated as:
```math
\text{New Shares (per asset)} = \frac{\text{Adjusted Target Investment (per asset)}}{\text{Price (per share)}}
```

---

These formulas form the foundation for calculating and managing an index based on multiple assets.

