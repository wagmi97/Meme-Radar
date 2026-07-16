# The Meme Radar 📡  (Pons CA: 0xc31a440316a29f8cee06adeaa30299f0ea8741b3)
 
**Track meme stock trends from Reddit, X, and TikTok in real-time.**

A financial intelligence app that monitors r/wallstreetbets, r/stocks, r/investing, X, and TikTok to identify which stocks/memes are gaining or losing attention, with sentiment analysis powered by authentic trading community terminology.

---

## 🎯 What It Does

- **Scans Sites** every 5 minutes for stock and meme mentions
- **Analyzes sentiment** using wallstreetbets lingo (diamond hands 💎🙌, tendies 🍗, to the moon 🚀)
- **Tracks top 10 trending stocks/memes** (rising in mentions)
- **Identifies fading stocks/memes** (losing interest)
- **Shows evidence** - actual posts/comments that influenced sentiment decisions
- **Visualizes trends** with charts and graphs
- **Mobile-friendly** modern UI

---

## 💰 Cost

**$0/month** - Runs entirely on free tiers:
- Vercel (hosting)
- DynamoDB Free Tier (database)
- Reddit API (free OAuth access)

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ (LTS)
- Docker (for DynamoDB Local)
- Reddit account (to create OAuth app)
- AWS CLI (for DynamoDB)

### Setup

1. **Clone the repository**
   ```bash
   cd /Users/markbnet/Documents/thememeradar.com
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create Reddit OAuth App**
   - Go to https://www.reddit.com/prefs/apps
   - Click "Create App"
   - Choose "script" type
   - Set redirect URI to `http://localhost:3000`
   - Note your Client ID and Client Secret

4. **Set up environment variables**
   ```bash
   cp .env.local.example .env.local
   # Edit .env.local with your Reddit credentials
   ```

5. **Generate JWT secret**
   ```bash
   openssl rand -base64 32
   # Copy output to JWT_SECRET in .env.local
   ```

6. **Start DynamoDB Local**
   ```bash
   docker run -d -p 8000:8000 --name dynamodb-local amazon/dynamodb-local
   ```

7. **Initialize database tables**
   ```bash
   npm run db:init
   ```

8. **Start development server**
   ```bash
   npm run dev
   ```

9. **Visit http://localhost:3000**

---

## 📚 Documentation

- **[CLAUDE.md](./CLAUDE.md)** - Comprehensive development guide, architecture, and standards
- **[TODO.md](./TODO.md)** - Project roadmap and task tracking

---

## 🧪 Testing

```bash
# Run all tests
npm test

# Run E2E tests
npm run test:e2e

# Run tests in watch mode
npm run test:watch
```

**Test-Driven Development (TDD)** is required for all features.

---

## 📊 Project Status

**Current Phase:** Phase 1 - MVP Development

See [TODO.md](./TODO.md) for detailed task list.

---

## 🛠️ Tech Stack

- **Frontend:** Next.js 14, React, TypeScript, Tailwind CSS
- **Backend:** Next.js API Routes, DynamoDB
- **APIs:** Reddit OAuth 2.0
- **Testing:** Jest, Playwright
- **Deployment:** Vercel, GitHub Actions CI/CD

---

## 🤝 Contributing

This is currently a personal project. Contributions may be accepted in the future.

---

## 📄 License

TBD

---

## 🔗 Links

- **Production:** TBD (not deployed yet)
- **GitHub:** TBD
- **Documentation:** [CLAUDE.md](./CLAUDE.md)

---

**Built with 🚀 by humans + Claude Code**
