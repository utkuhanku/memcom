# ⬡ MemCom — Your Tokens, Your Feed

**The on-chain replacement for X Communities, built for Solana meme culture.**

MemCom is a token-gated community platform where your wallet is your identity and your holdings are your feed. Connect your Solana wallet — only see content for the tokens you actually hold. No one else sees what you see.

> Built for the [Bags Hackathon](https://bags.fm/hackathon) · Category: Social Finance + Fee Sharing

## 🔗 Live

- **Landing:** [memcom.xyz](https://memcom.xyz)
- **App:** [app.memcom.xyz](https://app.memcom.xyz)

## The Problem

X (Twitter) shut down Communities. Telegram groups are unverified chaos. Discord servers have no on-chain identity. There's no place where **verified token holders** can find each other and share context — gated by real holdings, not usernames.

## The Solution

MemCom reads your wallet, identifies every SPL token you hold, pulls real-time market data, and builds a personalized feed — only for your tokens. If you don't hold it, you don't see it.

### How It Works

1. **Connect Wallet** — Phantom, Solflare, or Backpack
2. **Holdings Verified** — All SPL tokens read via Helius DAS API
3. **Feed Generated** — Real-time price data from DexScreener, contextual posts for each token
4. **Token-Gated** — Your holdings = your communities. Period.

## Features

- **Wallet-native identity** — No email, no password. Your public key is your profile.
- **Dynamic token detection** — No hardcoded token list. Any SPL token in your wallet is recognized.
- **Real-time prices** — DexScreener API integration, auto-refreshing every 30 seconds.
- **Contract address widgets** — Copy CA, link to chart, all inline.
- **X/Twitter integration** — Posts sourced from X with distinct "via 𝕏" styling.
- **Token-specific tabs** — Filter feed by individual token.
- **Send Love tip box** — SOL tips directly on-chain to support builders.
- **Independent sidebar scroll** — Wallet info, holdings, live prices always accessible.

## Bags Integration

MemCom is built on top of the Bags ecosystem:

- **Bags API** for token metadata and launch data
- **Fee Sharing** model — trading fees shared with community participants
- **Bags Token** — MemCom has its own Bags token for community governance

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Chain | Solana Mainnet |
| RPC | Helius DAS API |
| Prices | DexScreener API |
| Token Data | Bags API + Helius getAssetBatch |
| Wallet | Phantom / Solflare / Backpack |
| Hosting | GitHub Pages |
| Domain | GoDaddy + Cloudflare DNS |
| Frontend | Vanilla HTML/CSS/JS (zero dependencies) |

## Setup (for developers)

```bash
# Clone the repos
git clone https://github.com/utkuhanku/memcom        # Landing page
git clone https://github.com/utkuhanku/memcom-app     # App

# Get your own API keys
# 1. Helius: https://helius.dev (free tier)
# 2. Bags: https://dev.bags.fm

# In memcom-app/index.html, replace:
# YOUR_HELIUS_API_KEY → your Helius key
# YOUR_BAGS_API_KEY → your Bags key

# Deploy to GitHub Pages or any static host
```

## Architecture

```
User connects wallet
        ↓
Solana RPC (Helius) → Read all SPL token accounts
        ↓
Helius DAS API → getAssetBatch (name, symbol, image)
        ↓
DexScreener API → Real-time price, volume, mcap
        ↓
Dynamic feed built from held tokens only
        ↓
Token-gated: no holding = no access
```

## Roadmap

- [x] Wallet connection + on-chain verification
- [x] Dynamic token detection (any SPL token)
- [x] Real-time DexScreener prices
- [x] Token-gated feed
- [x] X/Twitter post integration
- [x] Send Love tip box
- [ ] Community posts (Supabase backend)
- [ ] Bags token launch + fee sharing
- [ ] DAO governance voting
- [ ] Mobile PWA
- [ ] X API direct integration

## Hackathon

This project is submitted to the **Bags Hackathon Q1 2026** under the **Social Finance** and **Fee Sharing** categories.

MemCom fills the gap left by X Communities — providing verified, on-chain, token-gated social spaces for the Solana meme ecosystem. Built as an open-source public good.

## License

MIT

## Links

- [memcom.xyz](https://memcom.xyz)
- [app.memcom.xyz](https://app.memcom.xyz)
- [Bags Hackathon](https://bags.fm/hackathon)
- [GitHub](https://github.com/utkuhanku/memcom)

---

*Built with vibes by [@utkuhanku](https://x.com/utkuhanku) · Ecosystem public good for Solana meme culture*
