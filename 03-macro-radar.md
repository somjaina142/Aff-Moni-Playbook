# Macro Radar

**Priority: 9/10 (HIGH VALUE)**  
**Build Phase: 1**

---

## Purpose

"Outside-in" intelligence hub. Shows what's happening in the world that could impact the portfolio. Converts global chaos into actionable signals.

**User Goal:** Know within 10 seconds if the macro environment is safe, cautious, or dangerous.

---

## Core Features

### 1. Market Health Ticker

**What it shows:**
```
┌─────────────────────────────────────────────────────────────────┐
│  🌍 GLOBAL MARKET STATUS                                        │
│                                                                 │
│  ┌────────────────────────────────────────────────────────────┐│
│  │  🔴 CAUTIOUS                                               ││
│  │  2 risk signals active                                     ││
│  │  [VIEW DETAILS]                                            ││
│  └────────────────────────────────────────────────────────────┘│
│                                                                 │
│  S&P 500    4,520  ▼ -1.2%    │    Gold      $1,950  ▲ +0.8%  │
│  SET Index  1,450  ▼ -0.5%    │    Oil       $78.50  ▲ +2.1%  │
│  BTC        $42K   ▲ +1.5%    │    USD/THB   35.2   ▲ +0.3%  │
│                                                                 │
│  Last update: 3 min ago                                        │
└─────────────────────────────────────────────────────────────────┘
```

**User interaction:**
- Status indicator (Safe 🟢 / Cautious 🟡 / Danger 🔴) always visible
- Click any asset → mini chart (7-day trend)
- Click status banner → detailed breakdown of active signals

**Design requirements:**
- Color-coded status: green/yellow/red background gradient
- Auto-refresh every 5 minutes (configurable)
- Show sparkline (7-day mini chart) on hover for each asset

---

### 2. Macroeconomic Indicators Panel

**What it shows:**
```
┌─────────────────────────────────────────────────────────────────┐
│  MACRO INDICATORS                                               │
├─────────────────────────────────────────────────────────────────┤
│  Fed Funds Rate     5.25%    │    US Inflation (CPI)    3.2%    │
│  BoT Policy Rate    2.50%    │    TH Inflation          1.1%   │
│  US 10Y Yield       4.35%    │    US GDP Growth         2.1%   │
│                                                                 │
│  🇺🇸 US Recession Probability: 35%                              │
│  🇹🇭 Thailand Economic Outlook: STABLE                          │
└─────────────────────────────────────────────────────────────────┘
```

**User interaction:**
- Hover over any indicator → tooltip explains what it means
- Click "Explain" → Educational snippet (what is Fed Funds Rate, why it matters)
- Toggle: "Compare to Last Month / Last Year"

**Design requirements:**
- Trend arrows (▲ rising / ▼ falling / ─ stable)
- Color code: good = green, warning = yellow, danger = red (context-dependent)
- Thai indicators highlighted (localized relevance)

---

### 3. Geopolitical & News Feed

**What it shows:**
```
┌─────────────────────────────────────────────────────────────────┐
│  GEOPOLITICAL SIGNALS                          Last 24h         │
├─────────────────────────────────────────────────────────────────┤
│  🔴 HIGH     Russia-Ukraine escalation reported                 │
│              Impact: Energy prices likely to rise               │
│              Suggested action: Review energy exposure            │
│                                                                 │
│  🟡 MEDIUM   Fed meeting minutes suggest rate hold               │
│              Impact: USD strength, emerging market pressure      │
│              Suggested action: Monitor THB exposure              │
│                                                                 │
│  🟢 LOW      Thailand Q1 GDP beats expectations                 │
│              Impact: Positive for SET, THB                      │
│              Suggested action: None required                     │
└─────────────────────────────────────────────────────────────────┘
```

**User interaction:**
- Filter by impact level (Critical / High / Medium / Low)
- Click signal → full analysis and suggested portfolio adjustment
- "Mark as read" to dismiss (stored in user preference)

**Design requirements:**
- Sort by impact (Critical first)
- Auto-expire signals older than 7 days (configurable)
- Each signal must have: Event, Impact assessment, Suggested action

---

### 4. Country-Specific Intelligence

**What it shows:**
```
┌─────────────────────────────────────────────────────────────────┐
│  🇹🇭 THAILAND FOCUS                                             │
├─────────────────────────────────────────────────────────────────┤
│  SET Index P/E Ratio: 14.2x (below 10-year avg of 15.8x)        │
│  THB Strength: Weakening against USD (▼ -3.2% YTD)              │
│  Tourism: +18% YoY arrivals                                     │
│  Government: PM focused on digital wallet scheme                │
│                                                                 │
│  📊 THAI MARKET SENTIMENT: NEUTRAL                              │
│  Suggested THB equity exposure: 15-20% of portfolio             │
└─────────────────────────────────────────────────────────────────┘
```

**User interaction:**
- Dedicated Thailand section (user's home market)
- Toggle: Switch focus to other countries (US, China, etc.)
- "Deep Dive" button → comprehensive country analysis

**Design requirements:**
- Must include: Stock market valuation, Currency strength, Economic growth, Political stability
- Auto-generate suggested exposure percentage based on current conditions

---

### 5. Asset Class Correlation Heatmap

**What it shows:**
```
┌─────────────────────────────────────────────────────────────────┐
│  CORRELATION MATRIX (Last 90 days)                              │
│                                                                 │
│           Stocks  Bonds   Gold   Oil    Crypto   Cash          │
│  Stocks    [GG]   [YR]   [YY]   [YG]    [YG]    [RR]          │
│  Bonds     [YR]   [GG]   [GY]   [YY]    [YY]    [GY]          │
│  Gold      [YY]   [GY]   [GG]   [YY]    [YY]    [YG]          │
│  Oil       [YG]   [YY]   [YY]   [GG]    [YG]    [RR]          │
│  Crypto    [YG]   [YY]   [YY]   [YG]    [GG]    [RR]          │
│  Cash      [RR]   [GY]   [YG]   [RR]    [RR]    [GG]          │
│                                                                 │
│  Legend: GG=Strong Positive  YR=Moderate Negative  RR=Negative │
└─────────────────────────────────────────────────────────────────┘
```

**User interaction:**
- Hover over cell → exact correlation coefficient
- Toggle timeframe (30/90/180 days)

**Design requirements:**
- Color gradient: Green (positive correlation) → Yellow (neutral) → Red (negative)
- This feature helps user understand diversification effectiveness

---

### 6. Thailand Sector Opportunity Radar

**Priority: 8/10 (HIGH VALUE) | Category: Decision-Support | Frequency: Weekly**

**What it shows:**
```
┌─────────────────────────────────────────────────────────────────┐
│  🇹🇭 THAILAND SECTOR OPPORTUNITIES              Updated: 2h ago  │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  🎯 HIGH-OPPORTUNITY SECTORS (2026):                            │
│  ─────────────────────────────────                              │
│                                                                 │
│  📊 HEALTHCARE & WELLNESS          OPPORTUNITY: HIGH            │
│  ──────────────────────────          ───────────────            │
│  Thailand → Super-aged society by 2030 (25% 60+)              │
│  Health economy: USD 40.5B (2023), +28.4% YoY                   │
│  Growth drivers: Medical tourism, wellness, preventive health  │
│                                                                 │
│  🏥 Your Exposure: BDMS (THB 500k) - ON TREND ✅               │
│  📈 Related stocks: BDMS, BH, BCH, CHG                         │
│  💡 Action: Hold or add on healthcare dips                     │
│  [VIEW HEALTHCARE STOCKS]                                       │
│                                                                 │
│  ─────────────────────────────────────────────────────────────  │
│                                                                 │
│  💻 DIGITAL INFRASTRUCTURE        OPPORTUNITY: HIGH            │
│  ──────────────────────────        ───────────────              │
│  Digital investment growing 10-12% annually                    │
│  Thailand → Top 10 data center destination globally            │
│  AI, cloud, big data adoption accelerating                     │
│                                                                 │
│  🏥 Your Exposure: THB 0 - UNDERWEIGHT ⚠️                       │
│  📈 Related stocks: GUNKUL, BCPG (renewable + data), TRUE      │
│  💡 Action: Consider adding digital infrastructure exposure    │
│  [VIEW TECH STOCKS]                                             │
│                                                                 │
│  ─────────────────────────────────────────────────────────────  │
│                                                                 │
│  🏭 EEC MANUFACTURING              OPPORTUNITY: MODERATE        │
│  ──────────────────────────        ─────────────────            │
│  BOI applications +67.5% YoY in EEC                            │
│  Industrial land sales growing 3-4% annually                   │
│  Geopolitical-driven investment relocation                     │
│                                                                 │
│  🏥 Your Exposure: THB 0 - OPPORTUNITY TO EXPLORE              │
│  📈 Related stocks: AMATA, WHA, ROJNA                          │
│  💡 Action: Research for long-term position                    │
│  [VIEW INDUSTRIAL STOCKS]                                       │
│                                                                 │
│  ─────────────────────────────────────────────────────────────  │
│  SET 2026 INDEX TARGET: 1,510 points  Current: 1,450 (+4.1%)  │
│  Key drivers: De-dollarization flows, accommodative rates      │
└─────────────────────────────────────────────────────────────────┘
```

**User Journey:**
```
1. User opens Macro Radar → Scrolls to "Thailand Sector Opportunities"
2. Sees high-opportunity sectors ranked by macro trend alignment
3. Each sector shows:
   - WHY it's an opportunity (macro drivers)
   - USER'S current exposure (matched to portfolio)
   - Related SET stocks to research
   - Suggested action
4. Click "View Stocks" → Filtered list of sector tickers
5. One-click "Add to watchlist" for further research
```

**Wireframe - Sector Stock List:**
```
┌─────────────────────────────────────────────────────────────────┐
│  🏥 HEALTHCARE SECTOR STOCKS                    SET-listed       │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  TICKER   NAME                     DIV      P/E    ALIGNED?    │
│  ──────   ─────────────────────    ─────    ────   ──────────   │
│  BDMS     Bangkok Dusit Medical   3.5%     16.2   ✅ Aging pop │
│  BH       Bangkok Hospital        2.8%     18.1   ✅ Medical tourism│
│  BCH      Bangkok Chain Hospital  3.1%     17.5   ✅ Expansion  │
│  CHG      Chain Holding           2.4%     22.0   ⚠️ Pricey    │
│                                                                 │
│  💡 YOUR PORTFOLIO:                                              │
│  BDMS - THB 500,000 (✅ Already invested)                       │
│                                                                 │
│  [ADD BH TO WATCHLIST] [ADD BCH TO WATCHLIST] [CLOSE]          │
└─────────────────────────────────────────────────────────────────┘
```

**Interaction States:**

| State | Display |
|-------|---------|
| **Loading** | "Analyzing Thailand sector trends..." |
| **Empty** | "No high-opportunity sectors identified currently" |
| **Error** | "Unable to fetch sector data. [Retry]" |
| **Success** | Ranked sectors with exposure analysis |

**Design Requirements:**
- Update weekly with latest macro research
- Cross-reference with user's portfolio holdings
- Show "Your Exposure" for each sector
- Color code: GREEN = already invested, YELLOW = underweight, RED = not invested but opportunity

**Data Sources:**
- Krungsri Research industry reports
- SET sector classifications
- BOI investment data
- User portfolio data (cross-reference)

---

## Signal Prioritization Logic

The system should auto-prioritize signals based on:

1. **Portfolio Impact Weight** — How much does this affect user's specific holdings?
2. **Signal Confidence** — How certain is the signal? (News speculation vs. hard data)
3. **Time Sensitivity** — Does this require immediate action or just monitoring?

**User sees:**
- Critical signals first
- Unread signals highlighted
- Dismissed signals stored in history (retrievable)

---

## Data Requirements

| Data Point | Source | Refresh |
|------------|--------|---------|
| Global stock indices | Yahoo Finance | 5 min |
| Commodity prices | Investing.com API | 15 min |
| FX rates | Open Exchange Rates | Hourly |
| Macro indicators | FRED / Trading Economics | Daily |
| Geopolitical news | Reuters / Bloomberg RSS | Real-time |
| Thailand specific | Bank of Thailand / SET | Daily |

---

## Success Metrics

- User understands global market status within 10 seconds ✅
- User sees active risk signals at glance ✅
- User can identify Thailand-specific economic conditions ✅
- Actionable signals surface automatically ✅

---

_Requirement specification by Hooko | Priority: 9/10_