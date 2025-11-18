## SunChain

Decentralized Solar Energy Network on Solana

## Problem Statement

Millions of Africans lack reliable electricity.
Grid power is inconsistent, expensive, and centralized.
Rural communities depend on fuel generators that harm the environment.

## Our Solution — SunChain

A Decentralized Physical Infrastructure Network (DePIN) connecting community solar hubs using Solana.

Each hub records energy data on-chain for transparency and trust.
Users pay via Solana smart contracts using stablecoins.

## Why Solana

Ultra-fast and low-cost micro energy payments

Real-time IoT data tracking via on-chain oracles

Scalable for millions of microgrid users


## How It Works

1. Communities install solar panels and IoT-enabled smart meters.


2. Energy data is transmitted to Solana and stored on-chain.


3. Users buy tokens or pay directly for electricity.


4. Revenue is distributed transparently among operators and investors.

## Impact

Provides clean and affordable power access

Creates new economic opportunities for rural tech operators

Demonstrates how blockchain can support real-world infrastructure

## Deployment & Usage

This section outlines how to set up and interact with the SunChain prototype using the Solana and Anchor frameworks.  
*(Note: The following commands use placeholder examples. They can be replaced with actual paths and program IDs once the smart contracts are ready.)*

## 1. Prerequisites
Before deployment, ensure you have the following installed:
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli) (v1.18 or higher)
- [Anchor Framework](https://book.anchor-lang.com/chapter_2/installation.html)
- Node.js and Yarn (for frontend interaction)
- Rust (for compiling smart contracts)
- Git (for repository management)

Verify installation:
```bash
solana --version
anchor --version
rustc --version
```

## 2. Clone the Repository
```bash
git clone https://github.com/SirIsarck/SunChainSOL1.git
cd SunChainSOL1
```

## 3. Configure Solana Cluster
Choose your preferred Solana environment:
```bash
solana config set --url https://api.devnet.solana.com
solana config get
```

Generate a new keypair if needed:
```bash
solana-keygen new --outfile ~/.config/solana/id.json
```

## 4. Build the Smart Contract (Program)
```bash
anchor build
```
This command compiles the placeholder SunChain program into a deployable `.so` binary under the `target/deploy/` directory.

## 5. Deploy to Devnet
```bash
anchor deploy
```
After deployment, youâ€™ll receive a `Program ID`.  
Copy and update it in `Anchor.toml` and the frontend configuration file.

Example placeholder:
```toml
[programs.devnet]
sunchain = "So1na1111111111111111111111111111111111111111"
```

## 6. Interacting with the Program
Once deployed, you can interact with the program using the Anchor CLI or Solana client SDKs.

Example placeholder command:
```bash
anchor test
```

Or manually invoke a transaction:
```bash
solana program invoke   --program-id <PROGRAM_ID>   --keypair ~/.config/solana/id.json
```

## 7. Frontend Integration (Optional)
If you plan to connect a web dashboard for IoT and on-chain data visualization:

Install dependencies:
```bash
yarn install
```

Start the local server:
```bash
yarn dev
```

## Usage

Connect a Solana wallet (Phantom or Solflare)

Register a community solar hub

Monitor real-time energy data

Execute payments and revenue sharing through the smart contract

## Technical Stack

Blockchain: Solana

Smart Contracts: Rust (Anchor Framework)

Frontend: React / Next.js

IoT Data: On-chain data + IPFS storage

Token: SPL token (SunToken)


## ## Reward Mechanism

SunChain introduces a simulated on-chain reward model for DePIN energy nodes.  
Each node earns SCH (SunChain Tokens) based on:
- Node Uptime: Continuous operation time.
- Data Accuracy: Correct and verified energy readings.
- Energy Contribution: Amount of simulated energy reported to the Solana network.

Rewards are calculated and distributed through a smart-contract logic that can be adapted to Solana Mainnet in future versions.

** This demo illustrates how decentralized energy nodes can earn tokenized incentives for powering real-world infrastructure in the DePIN economy.


## Security

On-chain verification of energy data

Escrow-based smart contracts for payment management

External smart contract audit planned before mainnet launch

## Team

- Isarck Eser (@SirIsarck001) – Founder, DePIN Innovator
- Kabir Muhammad (@Ishaqkdw) – CFO, Web3 Community Builder
- Zaharaddeen Isah (@Zaharaddeenisah) – Mentor, Renewable Energy & Blockchain Researcher
Collaborators: IoT Engineer, Smart Contract Developer, Community Operations Lead

## Roadmap

## Quarter Milestone	Goal

Q4 2025	IoT-enabled Pilot	3 communities live
Q1 2026	Expand to 5 new communities	500 active users
Q2 2026	Launch SunChain Africa Platform	Mainnet-ready deployment

## Vision

To make clean energy as open and borderless as the internet itself, powered by Solana.

## Contact:
Email: ishaqisah013@gmail.com
Twitter: @Sirisarck
Website: https://github.com/SirIsarck/sirisarck.github.io



