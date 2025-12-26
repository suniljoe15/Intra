# NSE Intraday Stock Analyzer

Personal stock analysis tool for NSE intraday trading with Zerodha Kite Connect integration.

## Features
- Live NSE stock data via Zerodha Kite API
- Buy/Sell signals based on RSI and momentum
- Stop loss and target price suggestions
- Customizable filters
- Mobile responsive design
- Auto-refresh every 2 minutes

## Setup Instructions

### 1. Get Zerodha Kite Connect API Access
1. Go to [Kite Connect](https://kite.trade/)
2. Sign up and create an app
3. Get your API Key and API Secret
4. Generate access token using the authentication flow

### 2. Backend Proxy Setup (Required for Live Data)
Due to CORS restrictions, you need a backend proxy to call Kite API.

**Option A: Using Vercel Serverless Function**

Create `api/kite-proxy.js`:
```javascript
export default async function handler(req, res) {
  const { method } = req;
  const { apiKey, accessToken, instruments } = req.body;

  if (method !== 'POST') {
    return res.status(405).json({ error: 'Method not allowed' });
  }

  try {
    const response = await fetch(
      `https://api.kite.trade/quote?${new URLSearchParams({i: instruments.join(',')})}`,
      {
        headers: {
          'X-Kite-Version': '3',
          'Authorization': `token ${apiKey}:${accessToken}`
        }
      }
    );

    const data = await response.json();
    res.status(200).json(data);
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
}
```

**Option B: Simple Node.js Backend**

Create `server.js`:
```javascript
const express = require('express');
const cors = require('cors');
const fetch = require('node-fetch');

const app = express();
app.use(cors());
app.use(express.json());

app.post('/api/quote', async (req, res) => {
  const { apiKey, accessToken, instruments } = req.body;
  
  try {
    const response = await fetch(
      `https://api.kite.trade/quote?${new URLSearchParams({i: instruments.join(',')})}`,
      {
        headers: {
          'X-Kite-Version': '3',
          'Authorization': `token ${apiKey}:${accessToken}`
        }
      }
    );
    
    const data = await response.json();
    res.json(data);
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});

app.listen(3000, () => console.log('Proxy running on port 3000'));
```

### 3. Deploy to GitHub Pages

1. Create a new repository on GitHub
2. Upload `index.html` and `README.md`
3. Go to Settings > Pages
4. Select "Deploy from a branch"
5. Choose "main" branch and root folder
6. Save

Your site will be live at: `https://yourusername.github.io/repo-name/`

## Usage

### Demo Mode
- Works out of the box with mock data
- Perfect for testing the interface

### Live Mode
1. Click "Config" button
2. Enter your Kite API Key and Access Token
3. Click "Save & Connect"
4. Data will refresh every 2 minutes

## Trading Signals

- **BUY**: RSI < 30 (oversold) or strong upward momentum
- **SELL**: RSI > 70 (overbought) or strong downward momentum
- **Stop Loss**: 3% for buys, 3% for sells
- **Target**: 5% profit target

## Disclaimer
This tool is for educational purposes only. Not financial advice. Always conduct your own research and consult with a financial advisor before making trading decisions.

## License
MIT License - Personal Use Only
```

**File 3: `.gitignore`**
```
node_modules/
.env
*.log
.DS_Store
