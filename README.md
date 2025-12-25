# Nightfall Legacy (Built for Base)

Nightfall Legacy is a lightweight, read-only toolkit designed for inspecting onchain data on Base Mainnet and Base Sepolia. It offers an easy way to validate network identity, retrieve balances, explore blocks, and interact with contracts through read-only queries, using Coinbase Wallet SDK and Base RPC endpoints.

## Repository Structure

- app/nightfall-legacy.ts  
  The core script that connects to Coinbase Wallet and interacts with the Base RPC, performing read-only operations.

- config/base.networks.json  
  Static configuration containing the RPC URLs, explorers, and chainIds for Base Mainnet and Base Sepolia.

- docs/architecture.md  
  Describes the architecture of the project, including design choices and how it aligns with Base's network and security principles.

- docs/testnet-validation.md  
  Contains validation notes recorded during the testing phase on Base Sepolia, detailing each verification step and outcomes.

- scripts/sample-addresses.json  
  A file containing sample addresses to be used for repeatable tests and validations.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - minltoken.sol — minimal contract for validating deployment and verification  
  - inheritance.sol — stateful contract for testing interactions  

- package.json  
  Dependency configuration that references the necessary SDKs and libraries from Base and Coinbase.

- README.md  
  Main documentation file with instructions on how to use the repository and run the code.

---

## Key Features

- **Coinbase Wallet SDK integration** for seamless wallet connection using EIP-1193  
- **Validation of Base chainIds** (8453 for Mainnet and 84532 for Sepolia)  
- **Network snapshot capabilities**, including the latest block details, timestamp, gas usage, and gas price  
- **Address inspection**: Check balance, transaction count, and bytecode presence  
- **ERC-20 token inspection**: Get metadata, total supply, and holder balance  
- **Cross-checking with Basescan**: All queries are linked to the relevant Basescan explorer for independent verification  

---

## Supported Networks

- **Base Sepolia**  
  chainId (decimal): 84532  
  Explorer: [sepolia.basescan.org](https://sepolia.basescan.org)  

- **Base Mainnet**  
  chainId (decimal): 8453  
  Explorer: [basescan.org](https://basescan.org)  

---

## Tooling & Dependencies

This repository leverages official tools from the Base and Coinbase ecosystems:
- **Coinbase Wallet SDK** for seamless wallet interaction  
- **OnchainKit** for Base-compatible primitives  
- **viem** for efficient and typed RPC communication with Base networks  
- **Other Base and Coinbase GitHub repositories** integrated as direct dependencies  

---

## License

MIT License

Copyright (c) 2025 YOUR_NAME

---

## Author Information

GitHub: [https://github.com/plainer-metes](https://github.com/plainer-metes)  

Email: plainer.metes-0b@icloud.com

Public contact: [https://x.com/puzzzzzzaw6776](https://x.com/puzzzzzzaw6776)  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

**Network**: Base Sepolia  
**chainId (decimal)**: 84532  
**Explorer**: [sepolia.basescan.org](https://sepolia.basescan.org)

**Contract minltoken.sol address**:  
0xbeF82294C310f3072c301e74ee9aA58B2D293738

**Deployment and verification**:
- [Deployment link](https://sepolia.basescan.org/address/0xbeF82294C310f3072c301e74ee9aA58B2D293738)
- [Code verification](https://sepolia.basescan.org/0xbeF82294C310f3072c301e74ee9aA58B2D293738/0#code)

**Contract inheritance.sol address**:  
 0x9d2A101A8746E9B3466075C8cBAc736BeCbCA278

**Deployment and verification**:
- [Deployment link](https://sepolia.basescan.org/address/0x9d2A101A8746E9B3466075C8cBAc736BeCbCA278)
- [Code verification](https://sepolia.basescan.org/0x9d2A101A8746E9B3466075C8cBAc736BeCbCA278/0#code)

These deployments on Base Sepolia serve to validate the functionality and compatibility of tooling with Base Mainnet before production deployment.
