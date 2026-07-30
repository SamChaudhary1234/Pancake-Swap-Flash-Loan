# 🧠 BSC Flashloan Bot

This is my flashloan implementation for Binance Smart Chain (BSC). The project allows me to simulate and deploy smart contracts that perform token swaps using flashloans.

> **Disclaimer:** This project is intended for educational and research purposes only. Flashloans and smart contract deployments involve significant financial and technical risks. Use this project responsibly.

---

## ✅ Prerequisites

Before running the project, make sure the following tools are installed on your machine:

* Node.js
* Yarn
* TypeScript Node (`ts-node`)

You can verify the installations using:

```bash
node --version
yarn --version
ts-node --version
```

---

## 🔐 Step 1: Environment Configuration

Create a `.env` file in the root directory:

```bash
touch .env
```

Add the following configuration:

```env
MAINNET_PROVIDER_URL=https://bsc-dataseed.binance.org
TESTNET_PROVIDER_URL=https://data-seed-prebsc-1-s1.binance.org:8545
PRIVATE_KEY=YOUR_PRIVATE_KEY_HERE_STARTING_WITH_0x
```

### ⚠️ Security Warning

Never commit the `.env` file or expose your private key publicly.

Make sure `.env` is included in the `.gitignore` file:

```gitignore
.env
```

For production deployments, I recommend using a dedicated wallet with limited funds or a hardware wallet for improved security.

---

## 📥 Step 2: Install Dependencies

Install the exact dependency versions defined in the repository:

```bash
yarn install --frozen-lockfile
```

Compile the smart contracts:

```bash
npx hardhat compile
```

---

## 🧪 Step 3: Run Tests

Run the complete test suite:

```bash
npx hardhat test
```

After the tests complete successfully, the terminal should display successful token swaps with green checkmarks.

I always recommend testing the complete flashloan and swap flow locally or on the BSC testnet before attempting a mainnet deployment.

---

## 🚀 Step 4: Deploy the Contracts

### Deploy the Flashloan Contract to BSC Mainnet

> ⚠️ **Warning:** Deploying to the mainnet consumes real BNB for gas fees. Verify the wallet, contract configuration and network settings before executing this command.

```bash
npx hardhat run scripts/deployFlash.ts --network mainnet
```

### Deploy the Simulation Contract

The simulation contract helps test the flashloan flow and records the estimated gas costs:

```bash
npx hardhat run scripts/deploySim.ts --network mainnet
```

---

## 🛡️ Important Notes

* I test all contract changes on the BSC testnet before deploying them to the mainnet.
* I never use a wallet containing significant funds for development or testing.
* Flashloan transactions can fail because of slippage, insufficient liquidity, gas costs or changes in token prices.
* A successful simulation does not guarantee that a mainnet transaction will be profitable.
* The smart contracts should be independently reviewed and audited before being used with real funds.

---

## 📚 Purpose

I created this repository to explore and understand:

* Flashloan execution on Binance Smart Chain
* Smart contract deployment using Hardhat
* Token swaps and liquidity pools
* Gas-cost simulation
* Automated testing of Solidity contracts
* DeFi transaction workflows

---

## 👨‍💻 Author

**Sam Chaudhary**

This repository is built for learning, experimentation and research related to flashloans and decentralized finance.
