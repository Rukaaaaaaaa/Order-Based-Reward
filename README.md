# 🪙 Order-Based Reward Distribution DApp

A decentralized reward distribution application built on **Ethereum**, where users receive **ERC20 token rewards based on their registration order**.

All reward logic is executed fully **on-chain** using Solidity smart contracts, ensuring transparency, immutability, and eliminating centralized manipulation.

---

# 📌 Overview

This DApp rewards early participants with bonus tokens:

- **First 3 users** → `150 tokens` (50 base + 100 bonus)
- **All subsequent users** → `50 tokens`
- Each wallet can **register only once**

The entire reward mechanism is handled directly by smart contracts deployed on Ethereum.

---

# 🛠 Requirements

Before running the project, make sure you have:

- Node.js (if using Hardhat)
- Remix IDE (alternative deployment method)
- MetaMask browser extension
- A test network (e.g., Sepolia)

---

# 📁 Project Structure
.
├── OrderReward.sol
├── RewardToken.sol
└── index.html


- `RewardToken.sol` – ERC20 token contract  
- `OrderReward.sol` – Registration and reward distribution logic  
- `index.html` – Frontend interface for interacting with the contracts  

---

# 🏗 Smart Contract Logic

## 🎯 Reward Rules

| Registration Order | Reward |
|-------------------|--------|
| 1st user          | 150 tokens |
| 2nd user          | 150 tokens |
| 3rd user          | 150 tokens |
| 4th+ users        | 50 tokens  |

## 🔐 Security Design

- Prevents duplicate registrations
- On-chain reward calculation
- Uses OpenZeppelin ERC20 standard implementation
- No centralized reward control
- Transparent and verifiable logic

---

# 🚀 Deployment Steps

## 1️⃣ Deploy RewardToken

Deploy `RewardToken.sol` using:
Remix IDE
or
Hardhat

Save the deployed contract address.

---

## 2️⃣ Deploy OrderReward

Deploy `OrderReward.sol` and pass the `RewardToken` contract address into the constructor.

---

## 3️⃣ Grant Mint Permission

Ensure the `OrderReward` contract has permission to mint tokens.

Depending on your implementation, you may need to:
Transfer ownership
or
Grant MINTER_ROLE

---

## 4️⃣ Update Frontend

Inside `index.html`, update:
Token contract address
OrderReward contract address
Network configuration


---

# ▶️ Running the Frontend

1. Open `index.html` in your browser  
2. Click **Connect MetaMask**  
3. Register your wallet  
4. Check your token balance  

To test reward tiers, switch between multiple MetaMask accounts.

---

# 🧪 Testing Scenario

| Account | Expected Result |
|----------|----------------|
| Account 1 | 150 tokens |
| Account 2 | 150 tokens |
| Account 3 | 150 tokens |
| Account 4 | 50 tokens |
| Duplicate registration | ❌ Transaction fails |

---

# 🧰 Technologies Used
Solidity
OpenZeppelin Contracts
Ethereum
MetaMask
ethers.js (v6)
HTML / JavaScript


---

# 💡 Key Features

- Fully decentralized reward logic  
- Gas-efficient registration system  
- Transparent on-chain verification  
- Fair early-user incentive mechanism  

---

# 👨‍💻 Author

Vu Phung Trung Kien  
Smart Contract Implementation Project  

---

# 📄 License

This project is licensed under the MIT License.
