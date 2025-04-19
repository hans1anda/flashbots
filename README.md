# Flashbots Transaction Bundle Sender (Goerli Testnet)

This project is a simple Node.js script that sends private transactions using **Flashbots** on the Ethereum Goerli testnet. The goal is to execute transactions in a secure and front-running-free environment, leveraging MEV (Maximal Extractable Value) infrastructure.

## 🔍 About the Project

This script performs the following steps:

1. Connects to the Goerli testnet using Alchemy.
2. Creates a Flashbots Bundle Provider.
3. Prepares a transaction bundle (with both legacy and EIP-1559 types).
4. Simulates the bundle to ensure it will not fail.
5. Sends the bundle to Flashbots for inclusion in the next 10 blocks.

This approach ensures a high probability that your transaction will be included, even if a Flashbots relay is not immediately selected as the block proposer.

## 🚀 Getting Started

### Prerequisites

- Node.js
- NPM

### Installation

```bash
npm install ethers @flashbots/ethers-provider-bundle
