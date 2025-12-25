# Nightfall Legacy — Architecture Overview

This document describes the architecture of the **Nightfall Legacy** project, including design choices and how it aligns with Base's network and security principles.

---

## Design Choices

The project is designed with a **read-only first** approach, which:
- Focuses on querying the blockchain state (balances, metadata, block info).
- Avoids direct transaction management or any on-chain changes, ensuring that interactions are lightweight and low-risk.

### Base Network Alignment

Nightfall Legacy is built to be **Base-first**, integrating tightly with Base Mainnet and Sepolia testnet:
- **Base Mainnet**: Production environment, used for live blockchain interactions.
- **Base Sepolia**: Testnet, used for testing before moving to Mainnet.

All network-specific configurations (RPC, explorers, chainIds) are stored in a centralized `config/base.networks.json` file, ensuring:
- No hardcoding of network values across the project.
- Easy adaptability for future Base network integrations.

### Security Principles

Security is a top priority for this project:
- **Decentralization**: Using Base ensures full compatibility with Ethereum and decentralized ledger security.
- **Read-Only**: By restricting functionality to read-only operations, the attack surface is minimized.

The project's architecture enables efficient querying of Base while minimizing exposure to risks, ensuring its resilience and stability.

---

## Future Considerations

1. **Support for additional Base networks**:  
   As Base grows, we aim to add support for new testnets and mainnets while keeping network configuration simple and dynamic.

2. **Transaction simulation**:  
   While the current scope is focused on read-only operations, we may explore transaction simulation in the future for further testing of smart contracts.

_Last updated: initial scaffold_
