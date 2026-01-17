# AKQ Poker Optimization – Game Theory Analysis

## Overview
This project analyzes **AKQ Poker**, a simplified two-player sequential poker game, using **game theory, expected value (EV) calculations, and mixed strategies**.  
The objective is to derive **optimal, unexploitable strategies** and verify them using **Python simulations**.

This project was completed as part of a **Game Theory coursework/project** at IIT Guwahati.

---

## Game Description
- Two-player sequential game: **Player 1 (P1)** and **Player 2 (P2)**
- Deck consists of **three cards**: Ace (A), King (K), Queen (Q)
- Card ranking: **A > K > Q**
- Both players post an ante of $1
- Players can **bet, check, call, raise, or fold**
- Higher-ranked card wins the pot at showdown

---

## Strategic Analysis

### Key Observations
- **Queen (Q)** should never call a bet as it always loses at showdown
- **Ace (A)** should always extract maximum value
- **King (K)** faces strategic trade-offs between calling and folding
- Bluffing with weak hands is **mathematically necessary** to avoid exploitation

---

## Expected Value (EV) Analysis
- EVs were computed assuming rational play under uncertainty
- When outcomes are deterministic, probabilities are adjusted accordingly
- Individual actions (bet, check, call, fold) were analyzed for each card

---

## Nash Equilibrium & Mixed Strategies
- No **pure-strategy Nash equilibrium** exists for AKQ Poker
- Players must adopt **mixed strategies** to remain unexploitable
- Probabilities are assigned to actions to equalize opponent EVs
- This results in **Game Theory Optimal (GTO)** behavior

---

## Python Simulation & Verification
To validate the theoretical strategies:
- Multiple strategies for Player 1 were tested
- A best-response strategy for Player 2 was implemented
- Simulations were run under stochastic conditions

### Tested Strategies
**Player 1 Strategy 1**
- A always bets
- K always checks
- Q bluffs with probability 1/3
- K calls with probability 2/3 against a bet

**Player 1 Strategy 2**
- All cards check initially
- K calls with probability 1/3 against a bet

### Results
- Strategy 1 significantly outperformed Strategy 2
- Strategy 1 achieved closer-to-equilibrium behavior
- Simulations confirmed theoretical EV calculations

Kaggle notebooks:
- https://www.kaggle.com/code/niceofyou06/akq-poker
- https://www.kaggle.com/code/vedjani/akq-poker

---

## Key Learnings
- Importance of **bluffing** to prevent predictability
- Decision-making based on **expected value**, not outcomes
- Understanding **ranges instead of single hands**
- Practical illustration of **Game Theory Optimal (GTO)** play
- Applications beyond poker: auctions, sports strategy, military planning

---

