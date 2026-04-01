# Bookie Documentation

Official documentation for [Bookie](https://bookie.app) - an AI-powered autonomous agent for executing DeFi operations on Solana using natural language.

## About Bookie

Bookie converts natural language commands into Solana transactions, enabling users to swap tokens, send funds, and track portfolios without complex interfaces. Built with Jupiter V6 integration for optimal liquidity routing and sub-second execution speeds.

## Documentation Structure

- **Getting Started** - Quickstart guide and architecture overview
- **Core Features** - Natural language execution, Jupiter integration, portfolio tracking, transaction speed
- **Security** - Solana integration, wallet security, transaction simulation
- **API Reference** - REST API endpoints for developers

## Local Development

Install Mintlify CLI:

```bash
npm install -g mint
```

Preview documentation locally:

```bash
mint dev
```

Check for broken links:

```bash
mint broken-links
```

View your local preview at `http://localhost:3000`.

## Project Structure

```
.
├── docs.json              # Mintlify configuration
├── index.mdx              # Homepage
├── introduction/          # Getting started guides
├── core-features/         # Feature documentation
├── integrations/          # Security and Solana integration
└── api-reference/         # API documentation
```

## Design System

- **Default Theme:** Light mode (white background)
- **Primary Color:** Orange (#f97316)
- **Accent Color:** Yellow-orange (#facc15)
- **Hover Color:** Dark orange (#ea580c)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on contributing to the documentation.

## Links

- [Bookie App](https://bookiebot.dev)
- [GitHub](https://github.com/Bookiepmndrs/bookie-repo)
- [Twitter](https://x.com/BookieWeb3)
- [Telegram](https://t.me/bookiedfi_bot)

## License

MIT License - see [LICENSE](LICENSE) for details.
