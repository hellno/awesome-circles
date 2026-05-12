# Awesome Circles [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources for the [Circles](https://aboutcircles.com) ecosystem - a decentralized, trust-based currency on [Gnosis Chain](https://www.gnosis.io) where every human mints 1 CRC per hour.

Circles is a personal-money protocol: every account issues its own currency, balances decay 7% per year (demurrage), and value flows along trust edges. Group currencies wrap personal CRC into fungible community money, and a network-wide pathfinder turns transitive trust into seamless payments.

This list points to the apps people use, the docs builders read, the protocol they build on, and the communities they ship with.

## Contents

- [Start Here](#start-here)
- [Wallets & Apps](#wallets--apps)
- [Mini Apps](#mini-apps)
  - [Consumer Mini Apps](#consumer-mini-apps)
  - [Group & Admin Tools](#group--admin-tools)
  - [Developer Demos](#developer-demos)
- [Protocol & Architecture](#protocol--architecture)
- [Developer Tools](#developer-tools)
- [Explorers & Indexers](#explorers--indexers)
- [Pathfinders](#pathfinders)
- [SDKs & Libraries](#sdks--libraries)
- [APIs & Infrastructure](#apis--infrastructure)
- [Starter Kits & Tutorials](#starter-kits--tutorials)
- [Build a Mini App](#build-a-mini-app)
- [Research, Simulation & Reputation](#research-simulation--reputation)
- [Hackathon Projects](#hackathon-projects)
- [Background Reading](#background-reading)
- [Community](#community)
- [Contribute](#contribute)

## Start Here

The front door to Circles for new users.

- [Circles World](https://world.gnosis.io) - Top-of-funnel landing page. Earn CRC by inviting friends, create a group, build an app, or host an event.
- [Circles World - Mini Apps](https://circles.gnosis.io) - Browse the live mini-app gallery from any Gnosis App wallet.
- [About Circles homepage](https://aboutcircles.com/manifesto) - Manifesto, whitepaper, FAQ, and ecosystem overview.
- [How Circles Works](https://docs.aboutcircles.com/overview/how-it-works) - Personal currencies, group currencies, trust, and demurrage in one page.
- [Introducing Circles v2](https://www.gnosis.io/blog/introducing-circles-v2-money-for-a-multipolar-world) - The v2 launch announcement on the Gnosis blog explaining design rationale.

## Wallets & Apps

User-facing surfaces for holding, sending, and spending CRC.

- [Metri](https://app.metri.xyz) - The official Circles v2 wallet. Passkey login, Safe smart account, fiat on/off-ramps via CoW Swap, and real-world spending via Gnosis Pay.
- [Gnosis App](https://app.gnosis.io) - Gnosis super-app that hosts Circles accounts, invite links, and the Mini App store.
- [Gnosis Pay](https://gnosispay.com) - Visa-compatible card that lets you spend CRC and other Gnosis Chain assets at any merchant.

## Mini Apps

Mini Apps are small, single-purpose web apps that load inside the Gnosis / Circles host and use a postMessage protocol for wallet signing. They come in two flavors: **embedded** (shipped from the official registry, native UX) and **standalone** (run anywhere, sign via QR or deep link).

### Consumer Mini Apps

- [Coinflip Game](https://coinflip-miniapp-omega.vercel.app/game) - Bet 1 CRC on heads or tails. The canonical "hello world" of embedded mini apps.
- [XMTP Demo](https://zengzengzenghuy.github.io/xmtp-circles-miniapp/) - End-to-end encrypted DMs and group chat between Circles accounts via XMTP.
- [Merch Shop](https://github.com/aboutcircles/merch-shop-miniapp) - Reference checkout flow for selling merch in CRC.

### Group & Admin Tools

- [Invitations Manager](https://aboutcircles.github.io/circles-invitation-links-manager/) - Mint, share, and track Circles invite links from one dashboard.
- [Circles Groups](https://circles-groups-miniapp.vercel.app/) - Create and manage group currencies and their member trust sets.
- [Group Liquidity Bootstrapper](https://group-liquidity-bootstrapper.vercel.app/) - Spin up an LBP to seed liquidity for a group currency on Gnosis Chain.
- [MiniApps Builders Org Manager](https://circles-org-miniapp.vercel.app/) - Manage builder-org accounts that ship mini apps.
- [Test Account Flag](https://test-account-flag.vercel.app) - Mark an avatar as a test account so it doesn't pollute ecosystem analytics.

### Developer Demos

- [Sign Message Demo](https://aboutcircles.github.io/miniappDemo/demo-sign/) - Minimal example of requesting a signature via the Mini App postMessage protocol.
- [ERC20 Transfer Demo](https://aboutcircles.github.io/miniappDemo/demo-tx/) - Minimal example of requesting a wallet transaction.

> Built a mini app? Submit it via the *Contribute* section below. Strong submissions can also enter the Mini Apps Launchpad bounty (linked under *Build a Mini App*).

## Protocol & Architecture

The on-chain layer that everything else builds on. Deployed on [Gnosis Chain](https://www.gnosis.io/gnosis-chain).

- [Circles Architecture Overview](https://docs.aboutcircles.com/overview/circles-architecture) - Hub V2, vaults, treasury, mint policies, and name registry on one diagram.
- [circles-contracts-v2](https://github.com/aboutcircles/circles-contracts-v2) - Solidity source for the Hub V2 (ERC-1155), Migration contract, Name Registry, Standard Treasury, Vaults, and Base Mint Policy.
- [circles-groups](https://github.com/aboutcircles/circles-groups) - Reference group-template contracts (membership conditions, custom mint policies).
- [Personal Currencies](https://docs.aboutcircles.com/overview/how-it-works/personal-currency) - Per-avatar minting, demurrage math, and the rule of trust.
- [Group Currencies](https://docs.aboutcircles.com/overview/how-it-works/group-currencies) - How communities pool personal CRC into a fungible group token.

## Developer Tools

- [CirclesTools](https://aboutcircles.github.io/CirclesTools/) - Hub of browser utilities: Profile Checker, Group Checker / Creator / Manager, Trust Graph & Trust Path Visualizers, Personal CRC Replenisher, Circles Backing dApp, LBP Starter, Token Distribution Checker, Safe State & Tx Hash Checker, Equilibrium Analysis, Onboarding Helper, and Legacy Safe Creator.
- [Pathfinder App](https://pathfinder.app.aboutcircles.com/flow-visualization/) - Compute and visualize optimal transfer routes through the trust network.
- [CirclesTools source](https://github.com/aboutcircles/CirclesTools) - Repository for the tools hub.
- [flow-visualization](https://github.com/aboutcircles/flow-visualization) - Source for the pathfinder flow visualizer.
- [group-tms](https://github.com/aboutcircles/group-tms) - Trust-Management Service: keeps a group's trust set in sync with declarative conditions.
- [Developer Tools docs](https://docs.aboutcircles.com/developer-support/circles-tools) - Annotated index of every tool in the hub.

## Explorers & Indexers

- [circles-explorer](https://github.com/aboutcircles/circles-explorer) - Block-explorer-style UI for Circles transactions, events, humans, groups, and orgs.
- [circles-envio-indexer](https://github.com/aboutcircles/circles-envio-indexer) - Envio-based indexer for Circles v2 events.
- [profile-service](https://github.com/aboutcircles/profile-service) - Stores and retrieves avatar profile metadata via IPFS.
- [circles-data-app](https://github.com/aboutcircles/circles-data-app) - Python data app for working with on-chain Circles data.

## Pathfinders

Routing engines that turn the trust graph into transfer paths.

- [pathfinder](https://github.com/aboutcircles/pathfinder) - Original Circles pathfinder.
- [pathfinder2](https://github.com/aboutcircles/pathfinder2) - Rewrite in Rust, used by the production pathfinder service.
- [pyfinder](https://github.com/aboutcircles/pyfinder) - Python pathfinder implementation.
- [pathfinder-proxy](https://github.com/aboutcircles/pathfinder-proxy) - Proxy layer in front of the pathfinder RPC.

## SDKs & Libraries

- [@aboutcircles/sdk](https://github.com/aboutcircles/sdk) - Current TypeScript SDK. Simplified surface over avatars, trust, pathfinding, profiles, and Safe execution. Published as `@aboutcircles/sdk` on npm.
- [circles-sdk (legacy)](https://github.com/aboutcircles/circles-sdk) - Earlier full-surface TypeScript SDK. Still referenced by many existing tutorials.
- [@aboutcircles/sdk-core](https://www.npmjs.com/package/@aboutcircles/sdk-core) - Low-level contract bindings for Hub V2.
- [@aboutcircles/sdk-rpc](https://www.npmjs.com/package/@aboutcircles/sdk-rpc) - Typed client for the Circles JSON-RPC methods.
- [@aboutcircles/sdk-pathfinder](https://www.npmjs.com/package/@aboutcircles/sdk-pathfinder) - Pathfinder client used by the SDK.
- [@aboutcircles/sdk-profiles](https://www.npmjs.com/package/@aboutcircles/sdk-profiles) - Read and write avatar profile metadata.
- [@aboutcircles/sdk-runner](https://www.npmjs.com/package/@aboutcircles/sdk-runner) - Execute operations through a Safe smart account.
- [@aboutcircles/sdk-transfers](https://www.npmjs.com/package/@aboutcircles/sdk-transfers) - Build transfer payloads from pathfinder output.
- [@aboutcircles/sdk-types](https://www.npmjs.com/package/@aboutcircles/sdk-types) - Shared TypeScript types.
- [@aboutcircles/sdk-utils](https://www.npmjs.com/package/@aboutcircles/sdk-utils) - Demurrage math and helpers.
- [circles-core](https://github.com/aboutcircles/circles-core) - Common methods for interacting with Circles, used across older clients.
- [SDK Reference](https://docs.aboutcircles.com/circles-sdk-reference/circles-sdk-interface) - Full method and event surface for the current SDK.

## APIs & Infrastructure

- [Circles JSON-RPC](https://docs.aboutcircles.com/api-reference/circles-api) - `https://rpc.aboutcircles.com/`. Public RPC: `circles_query`, `circlesV2_findPath`, `circlesV2_getTotalBalance`, `circles_events`, and more.
- [Pathfinder Service](https://docs.aboutcircles.com/circles-sdk/pathfinder) - Optimal routing through the trust graph, available via SDK or raw RPC.
- [Circles Indexer / Query](https://docs.aboutcircles.com/querying-circles-profiles-and-data/query-data) - SQL-style queries over indexed avatars, trust edges, balances, and transfers.
- [circles-nethermind-plugin](https://github.com/aboutcircles/circles-nethermind-plugin) - Nethermind execution-client plugin that exposes the Circles RPC namespace from a self-hosted node.
- [circles-spaceneth](https://github.com/aboutcircles/circles-spaceneth) - Standalone Nethermind node bundled with indexer and contracts for local testing.
- [crc-faucet](https://github.com/aboutcircles/crc-faucet) - CRC faucet for testnets / demos.
- [circles-migration-tool](https://github.com/aboutcircles/circles-migration-tool) - Tooling for migrating accounts and balances from v1 to v2.
- [marketplace-api](https://github.com/aboutcircles/marketplace-api) - Product-catalog aggregator and order API for the Circles Marketplace.
- [Avatar event subscriptions](https://docs.aboutcircles.com/querying-circles-profiles-and-data/subscribing-to-avatar-events) - Stream balance, trust, and group events in real time.

## Starter Kits & Tutorials

- [circles-gnosisApp-starter-kit](https://github.com/aboutcircles/circles-gnosisApp-starter-kit) - Official TypeScript starter for Gnosis × Circles apps.
- [circles-dev-kit](https://github.com/aboutcircles/circles-dev-kit) - Guided, hands-on tour of the Circles SDK.
- [Circles-starter-kit](https://github.com/aboutcircles/Circles-starter-kit) - Hacker guide for developers to learn Circles and build projects.
- [circles-sdk-svelte-examples](https://github.com/aboutcircles/circles-sdk-svelte-examples) - Worked Svelte examples for common SDK calls.
- [circles-vite-app](https://github.com/aboutcircles/circles-vite-app) - Vite playground for both Circles v1 and v2.
- [SDK Quickstart](https://docs.aboutcircles.com/circles-sdk/getting-started-with-the-sdk) - Install, connect a wallet, and mint your first CRC.
- [Setting up the SDK with React + JavaScript](https://docs.aboutcircles.com/tutorials-and-examples/setting-up-circles-sdk-with-react-and-javascript) - End-to-end React integration.
- [Gnosis App Starter Kit Tutorial](https://docs.aboutcircles.com/tutorials-and-examples/circles-x-gnosis-app-starter-kit) - Walkthrough of the official starter.
- [Vibecoding a Standalone Mini App](https://docs.aboutcircles.com/miniapps/standalone-mini-apps/simple-vibecoding-tutorial) - Ship a standalone mini app with no protocol expertise.
- [Agentic Setup for Circles](https://docs.aboutcircles.com/miniapps/agentic-setup-for-circles) - Wire Circles into an AI-coding-agent workflow.

## Build a Mini App

- [What are Circles Mini Apps](https://docs.aboutcircles.com/miniapps/what-are-circles-mini-apps) - Embedded vs. standalone, when to pick which.
- [Embedded Mini App guide](https://docs.aboutcircles.com/miniapps/embedded-mini-apps) - Build a mini app that ships inside the official store.
- [Intermediate Embedded guide](https://docs.aboutcircles.com/miniapps/embedded-mini-apps/intermediate-embedded-mini-app-guide) - Advanced patterns for embedded apps.
- [Standalone Mini App guide](https://docs.aboutcircles.com/miniapps/standalone-mini-apps) - Run anywhere, sign via QR or deep link.
- [Contribute a Mini App](https://docs.aboutcircles.com/miniapps/contribute-mini-apps) - Slug, code at `src/routes/apps/<slug>/`, logo, `miniapps.json` entry, PR.
- [Mini Apps Launchpad](https://docs.aboutcircles.com/miniapps/circles-mini-apps-launchpad) - Rolling bounties: $500 App of the Week, $1,000 Winner of the Month.
- [CirclesMiniapps repo](https://github.com/aboutcircles/CirclesMiniapps) - The host SvelteKit app and the registry. Submit PRs here.

## Research, Simulation & Reputation

- [PyCircleSim](https://github.com/aboutcircles/PyCircleSim) - Agent-based simulator for Circles network dynamics in Python.
- [pyfinder-dgen](https://github.com/aboutcircles/pyfinder-dgen) - Synthetic Circles data generator for pathfinder benchmarking.
- [circles_arbbots](https://github.com/aboutcircles/circles_arbbots) - Arbitrage bots that help equilibrate prices across CRC tokens.
- [circles-reputation-metrics](https://github.com/aboutcircles/circles-reputation-metrics) - Building blocks for a Circles reputation/recommendation system.
- [Universal basic income on blockchain: the case of Circles UBI](https://www.frontiersin.org/journals/blockchain/articles/10.3389/fbloc.2024.1362939/full) - Peer-reviewed analysis of Circles as a UBI mechanism (Frontiers in Blockchain).

## Hackathon Projects

Prior winners - useful as design inspiration.

- [BraceBuddy](https://ethglobal.com/showcase/bracebuddy-ph10y) - NFC bracelet onboarding for Circles (ETHGlobal Brussels 2024, 1st prize).
- [Woleth](https://ethglobal.com/showcase/woleth-eth-3ukpz) - Telegram-embedded EVM wallet using Circles invite mechanics (ETHGlobal Brussels 2024, runner-up).
- [Famjam](https://ethglobal.com/showcase/famjam-99inm) - Family currency that rewards kids for good behavior (ETHGlobal Brussels 2024, runner-up).
- [Voting with UBI](https://ethglobal.com/showcase/voting-with-ubi-k56uu) - DAO voting weighted by Circles group tokens (ETHGlobal Singapore 2024).
- [Circles Subscriptz](https://ethglobal.com/showcase/circles-subscriptz-tgfhj) - Trustless recurring payments in CRC (ETHGlobal Prague 2025).
- [Past Hackathon Projects index](https://docs.aboutcircles.com/developer-support/past-hackathon-projects-on-circles) - Maintained list with descriptions.

## Background Reading

- [Circles v2 Whitepaper](https://github.com/aboutcircles/whitepaper-public) - Canonical protocol whitepaper (PDF in repo).
- [Glossary](https://docs.aboutcircles.com/developer-support/glossary) - Avatars, demurrage, hubs, mint policies, vaults, and more.
- [Trust Score](https://docs.aboutcircles.com/user-guides/circles-features/trust-score) - How trust reputation is computed.
- [Daily Burn / Demurrage](https://docs.aboutcircles.com/user-guides/circles-features/daily-burn-demurrage) - Why your balance shrinks 7%/year.
- [Rule of Trust](https://docs.aboutcircles.com/user-guides/circles-features/circles-transfer-and-rule-of-trust) - How transitive trust enables strangers to pay each other.

## Community

- [Telegram - About Circles](https://t.me/about_circles) - Main builders + users chat.
- [@aboutcircles on X](https://x.com/aboutcircles) - Announcements and ecosystem updates.
- [GitHub - aboutcircles](https://github.com/aboutcircles) - All official repositories.
- Discord, Forum, and Farcaster: linked from the About Circles homepage (see top of this page).
- Email: `hello@aboutcircles.com`

## Contribute

Contributions welcome - see [contributing.md](contributing.md) for the format and review criteria. Open a PR if your project, tool, or guide belongs on this list.
