# Sub Rosa — Smart Contracts (Rust / Soroban)

This directory contains the Rust smart contracts for the Sub Rosa protocol.

## Structure

- **`round/` (`sub-rosa-round`)**:
  Confidential commit-reveal coordination round implemented as a Soroban smart contract primitive.
  - `src/lib.rs`: Contract entrypoints (`create_round`, `commit`, `open_reveal`, `reveal`, `clear`, `settle`, `void`, pagination views).
  - `src/types.rs`: Data types, round status, configuration, and authoritative `enum Error` codes.
  - `src/storage.rs`: Persistent, temporary, and instance storage helpers with TTL management.
  - `src/drand.rs`: Quicknet Drand BLS verification and timing.
  - `src/test.rs`: Comprehensive contract test suite (93 unit tests).
  - `src/error_paths.rs`: Integration tests for every defined contract error code.
  - `ERRORS.md`: Authoritative contract error code documentation kept in lock-step with `enum Error`.

## Building and Testing

From the repository root:
```bash
# Build the contract
cargo build -p sub-rosa-round

# Run all contract unit and integration tests
cargo test -p sub-rosa-round
```

Or from within `contracts/round`:
```bash
cargo check
cargo test
```
