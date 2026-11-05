# Squeek Match 🐹

A memory matching game dealt **live from the blockchain**. Every card is a real
**Squeek NFT**, loaded straight from the Squeekchain contract on Sepolia at the
moment you start a game — no two games use the same deck.

**Play it:** open `index.html` (or the GitHub Pages URL of this repo) in any browser.

## How it uses Squeekchain

- Reads `totalSupply()` and `tokenURI(id)` directly from the Squeeks ERC-721
  contract on Ethereum Sepolia — the chain Squeekchain's public testnet runs on:
  `0xc4c7982657f00509548f3a3a41db7fa439a6856b`
- Card art and traits come from each NFT's fully on-chain metadata
  (base64-encoded SVG + trait list), rendered in the browser.
- "Play with my Squeeks" mode: enter any wallet address (read-only — nothing is
  ever signed or sent) and the game builds a deck from the Squeeks that wallet
  actually holds, topping up with random ones if needed.
- Random-deck mode draws fresh token ids on every game, with automatic failover
  across public Sepolia RPC endpoints.

No wallet connection, no signatures, no transactions — the game is purely
read-only against public contracts, so it is safe for anyone to play.

## Run / deploy

It is a single static file: `index.html`. Host it anywhere static:

- **GitHub Pages:** push this repo, then Settings → Pages → deploy from the
  `main` branch root.
- Or open the file locally / drop it on any static host.

## About

Squeek Match is an independent mini-game built on public Squeekchain (Sepolia)
contracts, created for the Squeekchain Genesis builder program.

squeekchain-project: 95e1b81e-6adf-4713-a8c0-ab28a7de1c45
