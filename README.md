# MG3012 Assignment 2: MessageBoard dApp

| | |
|---|---|
| **Student** | Muhammad Bin Barkaat |
| **Course** | MG3012 Blockchain Technology for Business (BSFT, Fall 2026) |
| **Instructor** | Dr. Usama Arshad |
| **Network** | Ethereum Sepolia testnet |

## Contract Address

`0x69fC3e706E0eA176EF3dB681DC56eF6d02aEB9E1`

Deployment transaction: https://sepolia.etherscan.io/tx/0x88681522ed7a28898ed529ecd89c901b7e03a1224bfdd971b36d3a5e45599646

## What It Does

`MessageBoard` stores a public message on chain. Anyone can update it. Only the owner can reset it.

| Function | Type | Description |
|---|---|---|
| `setMessage(string)` | Write | Updates the message (1 to 140 characters) and emits `MessageUpdated` |
| `resetMessage()` | Write | Owner only reset |
| `getMessage()` | Read | Returns the current message |
| `getLastUpdater()` | Read | Returns the address of the last updater |
| `getUpdateCount()` | Read | Returns the number of updates so far |

## Files

| File | Description |
|---|---|
| `SmartContract.sol` | Solidity contract |
| `index.html` | Frontend using HTML and JavaScript with ethers.js v6 |
| `style.css` | Styling |
| `Screenshots/` | Connection and transaction screenshots |

## Setup

1. Open [Remix IDE](https://remix.ethereum.org), create `SmartContract.sol` and paste the code.
2. Compile with Solidity 0.8.20 or later in the Solidity Compiler tab.
3. In **Deploy & Run**, choose **Injected Provider - MetaMask** and make sure MetaMask is on **Sepolia**. Fund it from a Sepolia faucet.
4. Enter an initial message such as `Hello Sepolia` next to **Deploy** and confirm in MetaMask.
5. Copy the deployed contract address and paste it into `CONTRACT_ADDRESS` in `index.html`.
6. Open `index.html` using VS Code Live Server, or run `python -m http.server` and visit `http://localhost:8000`.
7. Click **Connect MetaMask**, then **Read Contract Data**, then **Update Message**.

## Screenshots

| File | Shows |
|---|---|
| `Screenshots/Connection.png` | Frontend connected to MetaMask |
| `Screenshots/Transaction1.png` | First successful write transaction |
| `Screenshots/Transaction2.png` | Second successful write transaction |
