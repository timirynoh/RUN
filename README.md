# Naya

A responsive fintech frontend prototype for African international students and diaspora members in KKTC.

## Run

Node.js 22+ is recommended.

```sh
npm ci --cache /tmp/naya-npm
npm run dev -- --port 3000
```

Build with `npm run build`, then serve the production build with `npm run preview`. Use the existing checkout; no additional worktree is needed.

## Included

Dark/light themes, multi-currency wallet views, simulated transfers and conversions with fees, bill and local airtime payment forms, transaction history, spending visualizations, subscription pause controls, virtual card freeze controls, CSV export and browser print-to-PDF. Demo account activity and preferences persist in local storage. A service worker caches previously loaded pages and assets for offline balances and history. Payments are blocked offline. Browser notifications require permission and a supported secure browser context.

## Integration boundaries

This is a demo, not a banking system. No real funds, account numbers, payment cards or identity documents should be entered. Balances are client-side demo data and must never be trusted by a production backend. Spending charts use illustrative values. Exchange rates are indicative, not live.

Real banking, KYC/AML, cross-border settlement, telecom top-ups, push delivery, fraud monitoring and human support require licensed providers and backend services. Support chat is a local demo assistant. Biometrics only checks platform authenticator availability; secure passkey enrollment and verification require a server. The language preference offers English, Turkish and French, but full interface translations remain to be implemented.

For offline validation, load a production build while online, allow service worker activation, then reload without a network connection. Cached data is device-local and not a live balance.

## Campus interface

The home screen uses rounded cards, colorful quick actions, campus guides and a floating five-tab navigation. Wallet, Exchange, Chats and More have dedicated screens. Home actions can be personalized; preferences and the welcome checklist persist on-device. Exchange quotes show the rate, fee and total debit before confirmation. Peer-to-peer trading and community messaging are explicitly marked as future features; no actual offers, escrow or verified users are presented.

## Cloudflare Pages

Connect this repository, choose `main`, use `npm run build` as the build command and `dist` as the output directory. Leave the root directory blank. No environment variables are required for the frontend demo. Cloudflare Pages can deploy updates automatically after pushes to `main`.
