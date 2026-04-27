# 🎲 RandomWinner Game

A simple Solidity lottery game powered by secure on-chain randomness using Chainlink VRF.

##  Overview

This project implements a decentralized lottery where players can join a game by paying an entry fee. Once the maximum number of players is reached, a random winner is selected using Chainlink VRF.

##  How It Works

- The contract owner starts a game by setting:
  - Maximum number of players
  - Entry fee (in ETH)
- Players join the game by paying the exact entry fee
- When the game is full, a random winner is selected
- The winner receives the total pool:
  
  
## 🔐 Randomness

Winner selection is powered by Chainlink VRF, ensuring:
- Fairness
- Verifiability
- Tamper-proof randomness

##  Deployment

- **Network:** Sepolia Testnet  
- **Contract Address:** ` 0x389aCc76bDdeE7Af4cD05b4586E84C51DAe8dc10 `

##  Key Features

- Fully on-chain lottery system  
- Secure randomness via Chainlink VRF  
- Automatic payout to winner  
- Simple and transparent game logic  

##  Tech Stack

- Solidity (0.8.24)
- Chainlink VRF v2.5
- Ethereum (Sepolia)

##  License

MIT

##  Author
- shola Emmanuel


sholaemmanuel.dev