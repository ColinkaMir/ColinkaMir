# Prooflines · ColinkaMir

Independent validator operator and open source builder. I run node infrastructure
(Lido SimpleDVT lanes on Ethereum: SSV and Obol; Monad testnet operations since April 2026)
and build public, off-node observability tools for the networks I operate on.

The theme across everything: **operators should be able to see the network without
trusting anyone's node, including mine.**

## Live tools

| Tool | What it does |
|---|---|
| [monad-sonar](https://github.com/ColinkaMir/monad-sonar) | Reads Monad's live peer and validator set without running a node, speaking the discovery protocol directly. Self-host CLI plus [hosted public feeds](https://prooflines.org/monad/sonar/) for testnet and mainnet, refreshed every 30 minutes |
| [Geo-Latency Map](https://prooflines.org/monad/geo-latency/) | Stake-weighted validator geography and ICMP latency for both Monad networks ([pipeline source](https://github.com/ColinkaMir/monad-stake-geography)) |
| [VDP Tracker](https://prooflines.org/monad/vdp-tracker/) | On-chain scanner, API and dashboard for Monad's Validator Delegation Program ([source](https://github.com/ColinkaMir/monad-vdp-tracker)) |
| [Observed Infra Feed](https://prooflines.org/monad/observed/) | Declared-versus-observed cross-check of validator metadata, the consumer side of MRC-13 |
| [MOST Leaderboard](https://prooflines.org/monad/most/) | Live standings of the Monad Open Source Track pilot, recomputed every 5 minutes |
| [x402 Gate](https://github.com/ColinkaMir/monad-x402-gate) | Pay-per-call network data over HTTP 402: dual-rail on Monad mainnet (native MON self-verified, plus the official USDC scheme via facilitator), [live endpoint](https://prooflines.org/monad/x402-on-monad/) with real on-chain revenue |
| [monad-x402-map](https://github.com/ColinkaMir/monad-x402-map) | Verified map of the Monad x402 niche: every entry probed, checked on-chain, or actually paid, with the tx hashes to prove it |
| [most-pool-watch](https://github.com/ColinkaMir/most-pool-watch) | Telegram watcher for the MOST pool: loud alerts for your events, claim registry, conflict watch, contribution-days leaderboard |
| [MonadBeaconBot](https://github.com/ColinkaMir/monad-node-bot) | Multi-user Telegram bot: node and RPC health, validator liveness, VDP alerts |

## Merged ecosystem work

- **ObservedSource** layer merged into the MRC-13 (Validator Metadata Registry) reference implementation
- **Agent-wallet confirm flow** in [nad-agent](https://github.com/portdeveloper/nad-agent) (MOST pool): mainnet guardrails, reliable non-TTY confirmations, resolved send previews; the declarative spend-policy proposal accepted by the maintainer
- **Co-authored** the [read conventions for attestation registries](https://github.com/ShadowOfTime1/monad-attestation-read-conventions) note (MRC-13/MRC-14 consumer side), operational half from the live observed feed
- Independently identified the `debug_checkpoint` keystore-password leak in Monad's canonical diagnostic tooling (publicly credited as a second finder)

## Currently

- **MOST pilot member** (Monad Open Source Track), contributing across the pool repos
- Operating the hosted feeds and dashboards at [prooflines.org/monad](https://prooflines.org/monad/), agent-readable via [llms.txt](https://prooflines.org/llms.txt) and [/.well-known/x402](https://prooflines.org/.well-known/x402)
- Writing up the agentic-payments practice: [permission models](https://prooflines.org/monad/agent-permissions/) and [x402 without a facilitator](https://prooflines.org/monad/x402-on-monad/)
- Watching the Monad VDP relaunch with a mainnet validator bid in preparation

Contact: [prooflines.org](https://prooflines.org)
