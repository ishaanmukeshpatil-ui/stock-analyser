# Indian Stock Analyzer (ISA)

A pitch-black themed Indian stock market analyzer with neon charts, featuring AI-powered analysis and comprehensive market insights.

## Features

### Page 1: Current Situation
- **Resizable Candlestick Chart** with TradingView Lightweight Charts
- **Timeframe Selection**: 1D, 5D, 1M, 3M, 6M, 1Y, 5Y, MAX
- **Functional Search Bar** with stock suggestions
- **Editable Watchlist** - add/remove stocks, localStorage persistence
- **Data Window** showing OHLC, Change, Volume, Technical Indicators (RSI, MACD)
- **Stock Context** - selected stock carries over to other pages

### Page 2: History & Analysis
- **Section I**: Previous Data & Quarterly Findings with interactive timeline
- **Section II**: Current Status in 3-column layout:
  - **Geopolitics** - Risk indicators (red/orange/green dots)
  - **News Analysis** - Company updates and milestones
  - **Overall** - Financial health, market position, analyst consensus
- **Dropdown Items** - Click to open modal popup with detailed summaries
- **Section III**: Overall Summary with bullish/bearish analysis
- **Quarterly Reports** with year selector (2021-2025)
- **Competitor Analysis** (Jio vs Airtel, Retail vs Amazon, Oil vs IOC)

### Page 3: AI Chatbot
- **Google Gemini Integration** for intelligent responses
- **Context-Aware** - knows which stock you're analyzing
- **Quick Actions** for common queries
- **Source Citations** for all claims

## Theme

- **Pitch Black Background** (#000000)
- **White Thin Borders** (rgba 8% opacity)
- **Neon Colors** for charts and indicators
- **Inter Bold** font for headings
- **No Emojis** - clean minimalist interface

## Tech Stack

- **React 18** + **Vite**
- **Tailwind CSS**
- **TradingView Lightweight Charts**
- **Google Gemini API**
- **IndianAPI** for stock data

## Quick Start (Single File)

Open `test-locally.html` directly in your browser - no installation required!

## Full Setup

### Prerequisites
- Node.js 18+
- npm

### Installation

```bash
cd indian-stock-analyzer
npm install
```

### Environment Setup

Create `.env` file:
```
VITE_INDIAN_API_KEY=your_indianapi_key
VITE_GEMINI_API_KEY=your_gemini_key
```

### Development

```bash
npm run dev
```

Open `http://localhost:3000`

### Build for Production

```bash
npm run build
```

## Deployment

### Netlify (Recommended)
1. Push to GitHub
2. Connect repo to Netlify
3. Auto-deploys on push

See [DEPLOYMENT.md](DEPLOYMENT.md) for details.

## Project Structure

```
indian-stock-analyzer/
├── test-locally.html      # Single-file version (no build needed)
├── src/
│   ├── components/
│   │   ├── Layout.jsx
│   │   ├── Header.jsx
│   │   ├── Sidebar.jsx
│   │   ├── CandlestickChart.jsx
│   │   ├── DataWindow.jsx
│   │   ├── Watchlist.jsx
│   │   └── SourceLink.jsx
│   ├── pages/
│   │   ├── CurrentSituation.jsx
│   │   ├── HistoryAnalysis.jsx
│   │   └── AIChatbot.jsx
│   ├── services/
│   │   ├── apiClient.js
│   │   ├── stockService.js
│   │   └── geminiService.js
│   └── utils/
│       ├── formatters.js
│       └── constants.js
├── package.json
├── vite.config.js
├── tailwind.config.js
├── netlify.toml
└── README.md
```

## API Integration

| Feature | Primary | Fallback |
|---------|---------|----------|
| Stock Data | IndianAPI.in | GitHub Free API |
| Historical | IndianAPI.in | Mock Data |
| News | IndianAPI.in | Mock Data |
| AI Analysis | Google Gemini | Mock Responses |

## API Endpoints Used

- `GET /stock?name=X` - Stock details
- `GET /historical_data?stock_name=X&period=1m` - Historical data
- `GET /trending` - Trending stocks
- `GET /news` - Market news
- `GET /statement?stock_name=X&stats=quarterly` - Quarterly results

## Source Citations

All analysis includes clickable source links to:
- BSE India - Company filings
- Economic Times - News
- Livemint - Market updates
- Reuters - Global news
- RBI - Macroeconomic data
- Bloomberg - Financial data

## Watermark

The application includes a subtle watermark "made by ishaan;>" in the bottom-right corner.

## Disclaimer

This application provides analysis based on publicly available data. It should not be considered as financial advice. Past performance does not guarantee future results. Always consult a qualified financial advisor before making investment decisions.

## License

MIT License

## Author

Made by Ishaan
