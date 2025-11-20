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

## How we want the Meter feature to work

SunChain Smart Hub Meter – Technical & Functional Specification

Project: SunChain – Decentralized Solar Energy Network
Objective: Develop a smart hub meter capable of managing multiple users in a community microgrid with AI integration, pay-as-you-go energy distribution, and blockchain-enabled transparency.


1. Core Objectives

The meter must:

- Track energy usage for multiple users (100–1000 users per hub).

- Allow users to connect instantly without owning individual inverters, batteries, or panels.

- Provide operators full control over electricity distribution.

- Optimize battery lifespan and efficiency through intelligent management.

- Support offline and online operations for rural areas with intermittent internet.


2. User Management & Tracking

Unique user IDs assigned upon joining (1, 2, 3…).

Track active users, newly joined users, and total energy usage per user.

AI Agent to calculate individual usage and billing, even with a single hub meter.

Real-time dashboard or local screen to display:

- Total users connected

- New users joined

- Energy consumption per user

- Notifications or alerts (overload, battery low)


3. Energy & Load Management

Smart hub meter must handle aggregate load from all connected users.

Peak load management: prevent overload and manage distribution efficiently.

- Battery management:

- Avoid deep discharge

- Optimize charging cycles

- Predictive load control to maximize battery lifespan


4. AI Integration

AI Agent embedded or connected to meter to:

Collect, process, and store energy data offline if no internet

Perform anomaly detection, predictive maintenance, and billing calculations

Decide when to supply or pause electricity based on usage and battery status

Generate summary proofs for blockchain upload


AI Agent must sync with blockchain automatically when connectivity is available.


5. Connectivity & Data Handling

Support internet connectivity options: Wi-Fi, NB-IoT, 4G/5G, or LoRa.

Store raw readings locally until AI Agent uploads aggregated summaries to blockchain.

Minimize bandwidth usage: only summary/proof sent on-chain.

Must support offline operation: users still receive electricity while data is buffered.


6. Billing & Blockchain Compatibility

Integrate with SunChain smart contracts for automated billing.

AI Agent calculates per-user usage → generates proof → uploads to blockchain.

Supports payments via SunChain token or stablecoin.

Revenue automatically split among:

Hub operator

Maintenance team

Investors


7. Display / Dashboard

Local screen or web dashboard shows:

Active users

Newly joined users

Energy usage per user / hub

Battery status and alerts

Billing summary


Optional: allow remote monitoring for operators.


8. Hardware Requirements

Voltage & load capacity: must handle aggregate peak load from all users.

High storage capacity for buffering 24-hour readings of hundreds of users.

Processing capability for AI calculations locally (edge device or embedded).

Power backup: maintain data logging during mains outages.

Robust IoT module for connectivity.

Physical durability: heat, dust, and environmental protection for outdoor hubs.


9. Scalability

Single hub meter can manage hundreds to thousands of users.

For very large deployments, hubs can be split into sub-hubs, each with a meter + AI Agent.

Must support inter-hub communication and synchronization if needed.


10. Key Features Summary

Features    -    	Description

Multi-user tracking - Track 100–1000 users per hub with unique IDs

Pay-as-you-go -	Integration with token/stablecoin payments

AI-assisted management - Load balancing, anomaly detection, predictive maintenance

Battery protection -	Deep discharge prevention, charging cycle optimization

Offline operation -	AI Agent collects and buffers data without internet

Blockchain integration -	Daily summary/proof uploads for transparency & revenue split

Display/dashboard -	Real-time user count, energy usage, billing, battery status

Peak load management -	Prevent overload & distribute electricity efficiently

Scalability -	Supports additional hubs or sub-hubs as users grow

Connectivity - Wi-Fi, LoRa, NB-IoT, 4G/5G


11. Notes for Manufacturers

Design firmware to communicate seamlessly with AI Agent.

Ensure secure, reliable, and accurate measurements.

Ensure robust power electronics for hub-level energy aggregation.

Allow for future upgrades: more users, sensors, or blockchain features.

- Conclusion

The SunChain Smart Hub Meter will be a centralized hub with decentralized control, powered by AI for intelligent energy management, and fully integrated with blockchain for transparency, pay-as-you-go billing, and investor trust.


## Technical Stack

Blockchain: Solana

Smart Contracts: Rust (Anchor Framework)

Frontend: React / Next.js

IoT Data: On-chain data + IPFS storage

Token: SunToken (SCN) – SPL token on Solana


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

## Quarter, Milestone, Goal

Q4 2025	IoT-enabled Pilot	3 communities live
Q1 2026	Expand to 5 new communities,	500 active users
Q2 2026	Launch SunChain Africa Platform, Mainnet-ready deployment

## Vision

To make clean energy as open and borderless as the internet itself, powered by Solana.

## Contact:
Email: ishaqisah013@gmail.com
Twitter: @Sirisarck
Website: https://github.com/SirIsarck/sirisarck.github.io



