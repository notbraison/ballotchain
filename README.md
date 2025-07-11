# 🗳️ BallotChain – Identityless Voting System

A decentralized, privacy-first voting platform on the Internet Computer (ICP).

---

## 📌 Project Summary

BallotChain enables DAOs and online communities to host **anonymous but verifiable elections**. Built fully on-chain using Motoko, Circom, and Internet Identity (II), it ensures:

* ✅ **One vote per person** (verified with Internet Identity)
* ✅ **Anonymity** (via zk-SNARK proofs and Merkle tree commitments)
* ✅ **On-chain auditability** (hosted on ICP with no off-chain servers)

---

## 🚀 Quick Start

### Prerequisites

* Node.js + npm
* DFINITY SDK (`dfx`)
* Circom + SnarkJS

### Setup

```bash
# Clone repo
$ git clone https://github.com/YOUR_USERNAME/ballotchain.git
$ cd ballotchain

# Start local replica and deploy backend
$ dfx start --background
$ dfx deploy

# Launch frontend
$ cd frontend
$ npm install
$ npm run dev
```

Visit `http://localhost:3000` and log in using [Internet Identity](https://identity.ic0.app/).

---

## 🧩 Project Structure

```
ballotchain/
├── frontend/         # React + Tailwind frontend
├── backend/          # Motoko canister smart contract
├── zk/               # Circom circuits + ZK tooling
├── dfx.json          # ICP project config
└── README.md
```

---

## 🔧 Key Features

* **zkVote Module:** Zero-knowledge proof of eligibility using Poseidon + Circom
* **Internet Identity Integration:** One anonymous vote per verified user
* **Fully On-Chain:** All logic and data stored in ICP canisters
* **DAO Voting Engine:** Admins can create and publish secure elections

---

## 📬 Submission Checklist (WCHL 2025)

* [x] Mainnet deployment + working canister ID
* [x] GitHub repo with `dfx.json` and circuits
* [x] Demo video and screenshots
* [x] README, info.md, roadmap.md

---

## 📄 License

MIT – open source and free to build on.

---

For questions, ideas, or contributions, reach out via Discord or GitHub Issues!
