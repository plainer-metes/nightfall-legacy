# Nightfall Legacy — Testnet Validation Notes

This document contains validation notes recorded during the testing phase on **Base Sepolia**.

---

## 2025-12-24 — Initial Testnet Validation on Base Sepolia

**Network:** Base Sepolia  
**Chain ID:** 84532  
**RPC Endpoint:** https://sepolia.base.org  
**Explorer:** https://sepolia.basescan.org

### Step 1 — Configuration Verification
- [ ] Verify `chainId` is correctly set to `84532` for Base Sepolia.
- [ ] Confirm network config is loaded from `config/base.networks.json`.
- [ ] Ensure `rpcTimeoutMs` is set to `10000` for responsive queries.

### Step 2 — RPC Connectivity Test
- [ ] Fetch latest block number: Should return a non-zero value.
- [ ] Re-fetch after a delay: Ensure block number increments and stays in sync.
- [ ] Test fallback RPC: Use fallback URL and ensure successful connection.

### Step 3 — Read-only Probes (Sample Data)
Using addresses from `scripts/sample-addresses.json`:
- [ ] Read ETH balance for `exampleEOA` — Should return a valid value (non-negative).
- [ ] Contract presence check for `exampleContract` — Should return a valid bytecode or `0x`.
- [ ] Ensure no errors for `zero` and `burn` addresses.

### Step 4 — Explorer Verification
- [ ] Open `exampleEOA` address on BaseScan Sepolia.
- [ ] Check the transaction hash for a recent block and verify it opens on the correct explorer.
- [ ] Ensure no links point to the wrong network (e.g., Mainnet).

### Conclusion:
- [ ] All validation steps passed successfully on Base Sepolia.
- [ ] Ready for integration with Base Mainnet once final checks are done.

_Last updated: initial scaffold_
