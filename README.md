<!-- Banner -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:001F3F,100:004080&height=220&section=header&text=Impulsive%20Candles%20Indicator&fontColor=ffffff&fontSize=45&desc=Pine%20Script%20v6%20—%20ATR×,%20Volume,%20and%20Body%20Filters%20for%20Momentum%20Detection&descAlignY=65" alt="banner"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1500&color=93C5FD&center=true&vCenter=true&width=700&lines=Detect+Market+Impulse+Moments+Without+Order+Flow;Spot+Liquidity+Imbalances+Visually;Automate+Your+Bias+Building+Process" alt="typing animation"/>
</p>

---

## 🧩 Overview

The **Impulsive Candles Indicator** is a *TradingView Pine Script v6* tool designed to automatically highlight impulsive price moves — moments of strong participation and directional intent — without requiring traders to read order flow or footprint charts.  

It acts as a **visual proxy for order flow imbalance**, combining **volatility (ATR)**, **volume strength**, and **candle body dominance** to detect when the market transitions from passive to aggressive trading behavior.  

This makes it particularly useful for:
- Discretionary traders who **don’t use DOM or footprint charts**  
- Scalpers looking to **spot aggressive buyers/sellers** early  
- Algorithmic traders who need **quantifiable triggers** for impulsive activity  

---

## ⚙️ How It Works

The indicator filters candles based on a 3-part condition:
1. **ATR Range Filter** → The bar’s total range must exceed a multiple of its average true range (`range ≥ ATR × multiplier`).
2. **Volume Confirmation** → Volume must be significantly higher than the recent moving average of volume (`volume ≥ volMA × multiplier`).
3. **Body Structure** → The candle’s body must represent a minimum percentage of the total range, filtering out wicks and noise.

If all conditions are satisfied:
- The candle is colored **teal** (bullish impulse) or **fuchsia** (bearish impulse).  
- **Midline** and **target zones** (BS/SS + TP) are automatically drawn using body size.  
- **Labels** help identify where a continuation or reaction might occur.

---

## 📊 Why It Helps Traders

In fast markets, **not everyone uses footprint or delta-based tools** — but impulsive movement *always* leaves a footprint on price, range, and volume.  
This script visually encapsulates that data, allowing traders to:
- Detect **localized liquidity imbalances**  
- Anticipate **stop runs or structural shifts**  
- Align entries with **market-generated momentum**  
- Use impulse candles as **anchor points for setups**  

It bridges the gap between **price action** and **order flow**, providing a “lite” version of order flow context *right on the chart.*

---

## 🖼️ Visual Example

<p align="center">
  <img src="./docs/assets/example_chart_1.png" width="80%" alt="Example chart showcasing impulsive candles">
</p>

> The teal and fuchsia candles indicate impulsive moves. Horizontal levels mark the midline and target zones derived from body size.

---

## 🧠 Key Features

| Feature | Description |
|----------|-------------|
| 🔹 **Multi-condition filter** | Combines ATR expansion, volume surge, and body ratio. |
| 🔹 **Automatic level plotting** | Draws midline and take-profit levels based on candle size. |
| 🔹 **Color-coded impulses** | Bullish = teal / Bearish = fuchsia. |
| 🔹 **Customizable parameters** | Fully adjustable ATR, volume, and range multipliers. |
| 🔹 **Alert-ready** | Emits alerts when new impulsive bars are detected. |

---

## ⚙️ Inputs

| Parameter | Description |
|------------|-------------|
| `ATR length` | Period for calculating volatility baseline. |
| `Range ≥ ATR ×` | Defines how much larger a bar’s range must be relative to average. |
| `Volume MA length` | Period for volume smoothing. |
| `Volume ≥ VolMA ×` | Multiplier threshold for volume spikes. |
| `Min body %` | Minimum percentage of range occupied by candle body. |
| `Tick width` | Controls midline/label spacing across bars. |

---

## 🚀 Installation

1. Open **TradingView** → **Pine Editor** tab.  
2. Copy the contents of `indicators/impulsive_candles_v1.pine`.  
3. Paste into a new script and click **Add to chart**.  
4. Adjust settings in the input panel as desired.

---

## 🧩 License
This project is released under the **MIT License**.  
You are free to modify and distribute it with attribution.

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:004080,100:001F3F&height=120&section=footer" />
</p>
