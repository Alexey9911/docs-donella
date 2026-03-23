# Bookie Documentation Project

## About this project

- This is the official documentation for Bookie, an AI-powered autonomous agent for executing DeFi operations on Solana
- Documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Terminology

- Use "Bookie" not "the agent" or "the bot"
- Use "wallet" not "account" when referring to Solana wallets
- Use "swap" not "trade" or "exchange" for token exchanges
- Use "transaction" not "tx" in user-facing content
- Use "natural language" not "NLP" or "AI commands" in user docs

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Connect Wallet**
- Code formatting for addresses, commands, and code references
- No emojis in documentation
- Direct, technical tone without marketing fluff
- Focus on facts and functionality over hype

## Content boundaries

- Document user-facing features only (no internal architecture details)
- Focus on security best practices prominently
- Always emphasize non-custodial nature and manual approval requirements
- Don't document unreleased features
- Don't make performance claims without data to back them up
- Avoid speculative content about future integrations

## Design system

- Default theme: Light mode (white background)
- Primary color: Orange (#f97316)
- Accent color: Yellow-orange (#facc15)
- Hover color: Dark orange (#ea580c)
- Clean, minimalist aesthetic
- Orange accents for CTAs and important elements
