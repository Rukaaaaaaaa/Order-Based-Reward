🪙 Order-Based Reward Distribution DApp

A decentralized Ethereum application that distributes ERC20 token rewards based on user registration order.

Early participants receive bonus rewards, and all reward logic is executed entirely on-chain.

=================================================================

📌 Features

ERC20 token implementation using OpenZeppelin

Order-based reward distribution

Bonus rewards for early participants

One-time registration per wallet address

MetaMask wallet integration

Frontend interaction using ethers.js

=================================================================

📁 Project Structure
OrderReward.sol – Reward distribution smart contract

RewardToken.sol – ERC20 token contract

index.html – Frontend interface

=================================================================

🏗 Smart Contracts
RewardToken.sol

Implements ERC20 standard

Handles token minting

Manages balances securely

OrderReward.sol

Registers users

Tracks registration order

Distributes rewards

Prevents duplicate registration

Reward Logic

First 3 users → 150 tokens (50 base + 100 bonus)

Other users → 50 tokens

Each wallet can register only once

=================================================================

🌐 Frontend

The index.html file:

Connects to MetaMask

Sends registration transactions

Displays token balances

Uses ethers.js (v6) for contract interaction

=================================================================

🚀 Deployment Steps

Deploy RewardToken.sol

Deploy OrderReward.sol with token address

Grant mint permission if required

Update contract address in index.html

Connect MetaMask and test

=================================================================

🛠 Technologies Used

Solidity

OpenZeppelin

Ethereum

MetaMask

ethers.js

HTML / JavaScript

=================================================================

📄 License

MIT License
