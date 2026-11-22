# BEARPROOF Agent Arena: verified skill for Agent ID holders

An entry for the Agent ID Hackathon (Agent Application Innovation Award). The plan: on BSC mainnet,
only an address that holds an Agent ID can commit a verified BEARPROOF run; the leaderboard is keyed
by Agent ID, so one person is one competitor; and verified achievements mint free, non-transferable
badges. Contracts are verified on BscScan with every owner power documented. Playing stays free.

## Status

22 Nov 2026: scaffold only. Nothing is deployed, no contract address exists yet, and no number on
this page is a result. This section is updated as each part ships.

## Pre-existing work and what is new

- Pre-existing (not part of this submission): the BEARPROOF game, its deterministic simulation and
  replay verifier, built 23 Sep – 31 Oct 2026 in
  [github.com/0smanturgut/bearproof](https://github.com/0smanturgut/bearproof) (MIT; a fork of
  [ricardo-foundry/canvas-vampire-survivors](https://github.com/ricardo-foundry/canvas-vampire-survivors),
  credited). Pinned as a dependency at tag
  [`v1.0-final`](https://github.com/0smanturgut/bearproof/tree/v1.0-final) (`48f8560`).
- Built during the Agent ID Hackathon (BNB Chain, 18 Nov – 9 Dec 2026), Innovation Award, from 22 Nov 2026: everything in this repository. First commit: 22 Nov 2026
  (`git log --reverse`).
  Game-side changes made for this event live in the game repository after the tag
  [`agentid-start`](https://github.com/0smanturgut/bearproof/tree/agentid-start).
- Related submissions: the same game is also entered at Concordium Trusted Agents (Encode Club); CoinMarketCap API Hackathon Round 2 (DoraHacks); Celo "Agents Open for Business" (Loops House); Reactive Omni Buildathon (DoraHacks); X Layer TapeOut Accelerate. Each entry has its own repository,
  integration and contracts. Shared code lives in
  [proofkit](https://github.com/0smanturgut/proofkit), written from 22 Nov 2026.
- AI use: see [AI_USAGE.md](AI_USAGE.md).
- Test traffic: transactions from wallets the team controls are listed in [CLAIMS.md](CLAIMS.md)
  and are not counted as users.

## Planned layout

- `contracts/`: the arena ledger, the prize vault and the badges
- `skill/`: instructions an Agent ID holder's own agent follows to commit a run
- `docs/owner-powers.md`: every privileged function and who holds it

## Run the checks

```bash
npm test
node scripts/secret-scan.mjs
```

A [CrowLab](https://crowlab.ai) project. MIT licensed.
