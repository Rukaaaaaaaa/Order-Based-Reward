📘 Order-Based Reward Distribution DApp

A decentralized application (DApp) built on Ethereum that distributes ERC20 token rewards based on user registration order.

Early participants receive bonus rewards, and all reward logic is enforced on-chain using smart contracts.

🚀 Overview

This project demonstrates:

ERC20 token creation using OpenZeppelin

Smart contract-based reward distribution

Order-based bonus mechanism

MetaMask wallet integration

Frontend interaction using ethers.js

The system ensures:

✅ Transparent reward allocation

✅ On-chain enforcement of rules

✅ One-time registration per address

✅ Bonus rewards for early participants

📂 Project Structure

├── contracts
│   ├── OrderReward.sol
│   └── RewardToken.sol
└── frontend
    └── index.html

🏗 Smart Contracts
1️⃣ RewardToken.sol

Implements ERC20 token standard using OpenZeppelin

Handles token minting

Restricts minting access to the reward contract

Key Features:

ERC20 compliant

Secure mint function

Used as reward currency

2️⃣ OrderReward.sol

Core logic contract that:

Allows users to register once

Tracks registration order

Distributes rewards based on order

Calls RewardToken contract to mint tokens

Reward Logic:
| Registration Order | Reward                           |
| ------------------ | -------------------------------- |
| First 3 users      | 150 tokens (50 base + 100 bonus) |
| Others             | 50 tokens                        |

Security Features:

Prevents duplicate registration

Enforces order-based bonus logic

Fully on-chain verification

🌐 Frontend (index.html)

The frontend:

Connects to MetaMask

Calls smart contract functions

Displays token balance

Sends registration transactions

Built using:

HTML

JavaScript

ethers.js (v6)

⚙️ How to Deploy
Step 1: Deploy RewardToken

Deploy RewardToken.sol using:

Remix IDE
or

Hardhat

Save the deployed contract address.

Step 2: Deploy OrderReward

Deploy OrderReward.sol, passing:

RewardToken contract address

Step 3: Set Mint Permission

If required, transfer ownership or grant minting role to the OrderReward contract.

Step 4: Update Frontend

Inside index.html, update:

Contract address

ABI

Network configuration

🧪 Testing

Test with multiple MetaMask accounts:

Connect wallet

Register

Confirm transaction

Check token balance

Repeat with different accounts

Expected result:

First 3 accounts receive 150 tokens

Later accounts receive 50 tokens

Duplicate registration fails

🔒 Security Considerations

Uses OpenZeppelin ERC20 standard

One-time registration mapping

On-chain validation

No centralized reward control

🛠 Technologies Used

Solidity

OpenZeppelin Contracts

Ethereum

MetaMask

ethers.js

HTML / JavaScript

📌 Future Improvements

Add event logging for better UI feedback

Deploy to testnet (Sepolia / Goerli)

Add admin dashboard

Improve UI design

Add automated tests using Hardhat

📄 License

MIT License
