# 🧠 BSC Flashloan Bot

A flashloan implementation for Binance Smart Chain (BSC). This repo simulates and deploys a contract that performs token swaps using flashloans.

---

## 📦 Clone the Repository

```bash
git clone https://github.com/salin1771/bsc_flashloan.git
cd bsc_flashloan
⚙️ Prerequisites
Ensure the following are installed globally on your machine:

Node.js

yarn

ts-node

🛠️ Step 1: Environment Configuration
Create an .env file in the root directory:

bash
Copy
Edit
touch .env
Add the following content:

env
Copy
Edit
MAINNET_PROVIDER_URL=https://bsc-dataseed.binance.org
TESTNET_PROVIDER_URL=https://data-seed-prebsc-1-s1.binance.org:8545
PRIVATE_KEY=YOUR_PRIVATE_KEY_HERE_STARTING_WITH_0x
⚠️ Warning: Never commit your .env file or share your private key publicly.

📦 Step 2: Install Dependencies
Install exact packages defined in the repo:

bash
Copy
Edit
yarn install --frozen-lockfile
Then compile the project:

bash
Copy
Edit
npx hardhat compile
🧪 Step 3: Run Tests
Execute the test suite:

bash
Copy
Edit
npx hardhat test
✅ You should see successful swaps with green checkmarks.

🚀 Step 4: Deploy Contracts
✅ Deploy Flashloan Contract to Mainnet
⚠️ Warning: This will consume real BNB gas. Be cautious.

bash
Copy
Edit
npx hardhat run scripts/deployFlash.ts --network mainnet
🔁 Deploy Simulation Contract
This contract simulates usage and logs gas costs:

bash
Copy
Edit
npx hardhat run scripts/deploySim.ts --network mainnet
📘 Notes
Always test on testnet before deploying to mainnet.

Use a secure wallet and consider hardware wallets for private key management.

This repo is meant for educational and research purposes. Use responsibly.



Let me know if you want me to add **shields (badges)**, a **license section**, or **GIF examples** of test output or deployment results.
