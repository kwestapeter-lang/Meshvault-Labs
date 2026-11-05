# Sub Rosa — Web Applications, Packages, and Off-Chain Services

This directory contains the TypeScript / JavaScript applications, client libraries, and backend services.

## Structure

### `apps/`
- **`web/`**: Interactive web dashboard and demo application for visualizing round lifecycles, bidder activity, and settlement outcomes.

### `packages/`
- **`sdk/` (`@sub-rosa/sdk`)**: TypeScript client SDK for interacting with Sub Rosa contracts, managing rounds, and sealing/submitting bids.
- **`round-bindings/` (`@sub-rosa/round-bindings`)**: TypeScript bindings generated from Soroban contract specs.
- **`tlock/` (`@sub-rosa/tlock`)**: Timelock encryption primitives and commitment hashing utilities.
- **`time/` (`@sub-rosa/time`)**: Deterministic time abstractions, schedulers, and clock utilities.
- **`types/` (`@sub-rosa/types`)**: Common TypeScript types and interfaces.
- **`logging/` (`@sub-rosa/logging`)**: Structured, redaction-safe logging system.

### `services/`
- **`keeper/` (`@sub-rosa/keeper`)**: Autonomous keeper daemon that monitors rounds, opens reveal upon Drand beacon publication, clears, and settles rounds.
- **`agent/` (`@sub-rosa/agent`)**: Automated bidding agent service.
- **`appraisal-api/` (`@sub-rosa/appraisal-api`)**: Valuation and appraisal quote API.
- **`drand-tools/` (`@sub-rosa/drand-tools`)**: Drand beacon fetcher and quicknet verification tools.
- **`receipt-cli/` (`@sub-rosa/receipt-cli`)**: Deterministic round receipt generation and verification CLI.
- **`auction-template/` (`@sub-rosa/auction-template`)**: Reference implementation and testnet scripts.

## Running Tests

From the repository root (or within this workspace):
```bash
# Run all workspace tests
pnpm test

# Run typechecking across all workspaces
pnpm typecheck
```
