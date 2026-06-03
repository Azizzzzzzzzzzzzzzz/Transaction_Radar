# TransactionRadar 🚀

Advanced Bitcoin blockchain explorer and intelligence platform with real-time transaction tracking, mempool monitoring, and whale alerts.

## 🎯 Features

### Core Features
- **Real-time Mempool Monitoring** - Track unconfirmed transactions as they enter the network
- **Transaction Details** - Complete breakdown of inputs, outputs, fees, and confirmations
- **Address Analytics** - Full transaction history and balance tracking for Bitcoin addresses
- **Block Explorer** - View confirmed blocks with detailed statistics
- **Whale Alerts** - Detect and monitor large Bitcoin movements
- **Address Classification** - Identify exchanges, mining pools, and other entities

### Intelligence Features
- **Radar Score** (0-100) - Risk assessment and activity scoring
- **Entity Clustering** - Group related addresses together
- **Fee Estimation** - Real-time network fee recommendations
- **Network Statistics** - Hash rate, difficulty, and transaction stats
- **Price Data** - Live BTC pricing in USD, EUR, GBP

## 🛠️ Tech Stack

### Frontend
- **Next.js 15** - React framework with App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first styling
- **Zustand** - Lightweight state management
- **Framer Motion** - Smooth animations
- **Lucide React** - Beautiful icons

### Backend
- **Next.js API Routes** - Serverless API layer
- **Axios** - HTTP client for API calls

### APIs
- **Mempool.space API** - Bitcoin blockchain data
- **CoinGecko API** - Price data
- **Blockchain.com API** - Fallback data source

## 📋 Project Structure

```
transaction-radar/
├── app/
│   ├── components/           # Reusable React components
│   │   ├── Navbar.tsx       # Navigation bar
│   │   ├── Footer.tsx       # Footer component
│   │   ├── SearchBar.tsx    # Search functionality
│   │   ├── StatCard.tsx     # Statistics cards
│   │   ├── TransactionCard.tsx
│   │   ├── AddressInfo.tsx
│   │   └── ui/              # UI components
│   │
│   ├── lib/                  # Utility functions
│   │   ├── utils.ts         # Helper functions
│   │   └── api.ts           # API integration
│   │
│   ├── store/               # Zustand stores
│   │   ├── searchStore.ts
│   │   └── networkStore.ts
│   │
│   ├── types/               # TypeScript types
│   │   └── index.ts
│   │
│   ├── (pages)
│   │   ├── page.tsx         # Home page
│   │   ├── tx/[id]/page.tsx # Transaction details
│   │   ├── address/[address]/page.tsx
│   │   ├── block/[id]/page.tsx
│   │   ├── mempool/page.tsx
│   │   ├── blocks/page.tsx
│   │   ├── top-transactions/page.tsx
│   │   ├── trending/page.tsx
│   │   └── about/page.tsx
│   │
│   ├── layout.tsx           # Root layout
│   ├── page.tsx             # Home page
│   ├── providers.tsx        # App providers
│   └── globals.css          # Global styles
│
├── public/                  # Static assets
├── package.json
├── tsconfig.json
├── tailwind.config.ts
├── postcss.config.js
└── next.config.js
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

Open [http://localhost:3000](http://localhost:3000) to view the app.

## 📱 Pages

### Home (`/`)
Hero section with search bar and live network statistics

### Transaction Details (`/tx/[txid]`)
Complete transaction information including:
- Input/output breakdown
- Fee rate and transaction size
- Confirmation status
- Raw transaction data

### Address (`/address/[address]`)
Address analytics with:
- Total received/sent
- Balance calculation
- Transaction history
- UTXO data
- Mempool activity

### Mempool (`/mempool`)
Real-time unconfirmed transactions with:
- Pending tx count
- Mempool size
- Fee distribution
- Recent transactions list

### Blocks (`/blocks`)
Latest confirmed blocks with:
- Block height
- Transaction count
- Block size
- Difficulty

### Top Transactions (`/top-transactions`)
Largest transactions by value with ranking

### About (`/about`)
Information about the platform, technology stack, and contact

## 🎨 Design System

### Colors
- **Bitcoin Orange**: `#ffa500`
- **Success Green**: `#22c55e`
- **Danger Red**: `#ef4444`
- **Dark Background**: `#0f172a`
- **Card Background**: `#1e293b`

### Components
- **radar-card**: Main card container
- **radar-input**: Form input
- **stat-card**: Statistics display
- **glass-effect**: Glassmorphism effect

## 🔄 Real-time Features

### WebSocket Support
- Mempool block updates
- Transaction broadcasts
- Network status changes

### Auto-refresh
- Network stats: 30 seconds
- Mempool data: 10 seconds
- Price updates: 60 seconds

## 📊 Supported Address Types

- **P2PKH** - Pay to Public Key Hash (1...)
- **P2SH** - Pay to Script Hash (3...)
- **P2WPKH** - Pay to Witness Public Key Hash (bc1q...)
- **P2WSH** - Pay to Witness Script Hash (bc1q...)
- **P2TR** - Pay to Taproot (bc1p...)

## 🔐 Security Features

- No private keys handled
- HTTPS enforced in production
- CSP headers configured
- Input validation on all forms
- XSS protection

## 📈 Performance Optimizations

- Image optimization
- Code splitting
- Tree shaking
- Minification
- Responsive images
- Lazy loading

## 🚧 Future Features

- [ ] Advanced charting and analytics
- [ ] Price alerts and notifications
- [ ] User authentication
- [ ] Watchlists and favorites
- [ ] Transaction broadcasting
- [ ] Advanced filtering
- [ ] Export data (CSV, JSON)
- [ ] API with authentication
- [ ] Mobile app
- [ ] Dark/Light theme toggle

## 📚 API Documentation

### Transaction Endpoints
- `GET /api/tx/[txid]` - Get transaction details
- `GET /api/tx/[txid]/outspends` - Get UTXO spending info
- `GET /api/tx/[txid]/merkleproof` - Get merkle proof

### Address Endpoints
- `GET /api/address/[address]` - Get address info
- `GET /api/address/[address]/txs` - Get transactions
- `GET /api/address/[address]/utxo` - Get UTXOs

### Block Endpoints
- `GET /api/block/[hash]` - Get block info
- `GET /api/block/[hash]/txs` - Get block transactions
- `GET /api/blocks/[height]` - Get block by height

### Network Endpoints
- `GET /api/network/stats` - Network statistics
- `GET /api/price` - Bitcoin price data
- `GET /api/mempool/stats` - Mempool statistics

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- Mempool.space for blockchain data
- CoinGecko for price data
- Vercel for hosting
- The Bitcoin community

## 📞 Support

For support, email hello@transactionradar.com or open an issue on GitHub.

## 🌐 Links

- Website: https://transactionradar.com
- GitHub: https://github.com/transactionradar
- Twitter: https://twitter.com/transactionradar
- Email: hello@transactionradar.com

---

Built with ❤️ for the Bitcoin community
