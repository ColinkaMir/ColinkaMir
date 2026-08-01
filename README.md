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
| [MonadBeaconBot](https://github.com/ColinkaMir/monad-node-bot) | Multi-user Telegram bot: node and RPC health, validator liveness, VDP alerts |

## Merged ecosystem work

- **ObservedSource** layer merged into the MRC-13 (Validator Metadata Registry) reference implementation
- **Mainnet guardrails** in [nad-agent](https://github.com/portdeveloper/nad-agent), Monad's local AI agent wallet (MOST pool)
- Independently identified the `debug_checkpoint` keystore-password leak in Monad's canonical diagnostic tooling (publicly credited as a second finder)

## Currently

- **MOST pilot member** (Monad Open Source Track), contributing across the pool repos
- Operating the hosted feeds and dashboards at [prooflines.org/monad](https://prooflines.org/monad/)
- Watching the Monad VDP relaunch with a mainnet validator bid in preparation

Contact: [prooflines.org](https://prooflines.org)
