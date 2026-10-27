# Prooflines · ColinkaMir

Independent validator operator and open source builder. I run node infrastructure on Ethereum
(Lido SimpleDVT lanes: SSV and Obol). On Monad I work off-node: [monad-sonar](https://github.com/ColinkaMir/monad-sonar)
speaks the discovery protocol directly, so the whole validator and peer set can be read from an
ordinary server; the geo-latency map and network dashboards run on its feeds. Everything else
reads the chain directly.

The theme across everything: **operators should be able to see the network without
trusting anyone's node, including mine.**

Everything below is live at [prooflines.org/monad](https://prooflines.org/monad/) and open source.

## Monad: network observability

| Tool | What it does |
|---|---|
| [monad-sonar](https://github.com/ColinkaMir/monad-sonar) | Reads Monad's live peer and validator set without running a node, speaking the discovery protocol directly. Self-host CLI plus [hosted public feeds](https://prooflines.org/monad/sonar/) for testnet and mainnet, refreshed every 30 minutes |
| [Geo-Latency Map](https://prooflines.org/monad/geo-latency/) | Stake-weighted validator geography and ICMP latency for both Monad networks ([pipeline source](https://github.com/ColinkaMir/monad-stake-geography)) |
| [VDP Tracker](https://prooflines.org/monad/vdp-tracker/) | On-chain scanner, API and dashboard for Monad's Validator Delegation Program ([source](https://github.com/ColinkaMir/monad-vdp-tracker)) |
| [Observed Infra Feed](https://prooflines.org/monad/observed/) | Declared-versus-observed cross-check of validator metadata, the consumer side of MRC-13 |

## Monad: for node operators

| Tool | What it does |
|---|---|
| [MonadBeaconBot](https://t.me/MonadBeaconBot) | Multi-user Telegram bot: node and RPC health, block stalls, lag behind the network, validator liveness, VDP alerts ([source](https://github.com/ColinkaMir/monad-node-bot)) |
| [MOST Leaderboard](https://prooflines.org/monad/most/) | Live standings of the Monad Open Source Track pilot, recomputed every 5 minutes |
| [most-pool-watch](https://github.com/ColinkaMir/most-pool-watch) | Telegram watcher for the MOST pool: loud alerts for your events, claim registry, conflict watch, contribution-days leaderboard |

## Monad: agents and payments

| Tool | What it does |
|---|---|
| [Receipts](https://prooflines.org/monad/agent-trust/) | Provenance for ERC-8004 reputation: which ratings on an agent are backed by independent payers and which were produced by its own owner. HTTP API and MCP server, already called by another team's app ([source](https://github.com/ColinkaMir/monad-agent-trust)) |
| [monad-mcp](https://github.com/ColinkaMir/monad-mcp) | Monad network intelligence as MCP tools at `https://prooflines.org/mcp`: network snapshot, validator set, geo concentration, VDP status, one paid report |
| [x402 Gate](https://github.com/ColinkaMir/monad-x402-gate) | Pay-per-call network data over HTTP 402: dual-rail on Monad mainnet (native MON self-verified, plus the official USDC scheme via facilitator), [live endpoint](https://prooflines.org/monad/x402-on-monad/) with real on-chain revenue |
| [monad-x402-index](https://github.com/ColinkaMir/monad-x402-index) | The [discovery index](https://prooflines.org/monad/x402-discovery/resources) for x402 on Monad, in the CDP bazaar shape, rebuilt hourly |
| [monad-x402-map](https://github.com/ColinkaMir/monad-x402-map) | Verified map of the Monad x402 niche: every entry probed, checked on-chain, or actually paid, with the tx hashes to prove it |

## Merged ecosystem work

**25 merged pull requests across 7 Monad ecosystem repositories since June 2026**, most of them
through the MOST pool:

- **nad-agent** (13): mainnet guardrails, reliable non-TTY input, resolved send previews, the
  declarative spend policy, argument and token-id validation, a `doctor` seed and RPC probe
- **monad-monitor** (4): alert confirmation that resets on unknown readings, the no-block clock,
  honest exit codes for JSON watch output
- **puddleswap** (3), **mipland**, **knot**: decoded revert reasons, known-unit pool analytics,
  chain-id check before publishing MIP-8 results, an Aave v3 repay action
- **sentinel** (2): ERC-8004 reputation provenance from Receipts shown before an agent is registered
- **MRC-13** (Validator Metadata Registry): the ObservedSource layer in the reference implementation
- **Co-authored** the [read conventions for attestation registries](https://github.com/ShadowOfTime1/monad-attestation-read-conventions) note (MRC-13/MRC-14 consumer side), operational half from the live observed feed
- Independently identified the `debug_checkpoint` keystore-password leak in Monad's canonical diagnostic tooling (publicly credited as a second finder)

## Currently

- **MOST pilot member** (Monad Open Source Track), proposing and fixing defects across the pool repos
- **Receipts** submitted to the Monad Metropolis hackathon
- Operating the hosted feeds and dashboards at [prooflines.org/monad](https://prooflines.org/monad/), agent-readable via [llms.txt](https://prooflines.org/llms.txt) and [/.well-known/x402](https://prooflines.org/.well-known/x402)
- Writing up the agentic-payments practice: [permission models](https://prooflines.org/monad/agent-permissions/) and [x402 without a facilitator](https://prooflines.org/monad/x402-on-monad/)
- Watching the Monad VDP relaunch with a mainnet validator bid in preparation

Contact: [prooflines.org](https://prooflines.org)
