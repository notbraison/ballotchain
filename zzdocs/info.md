# 🗳️ Identityless Voting System – WCHL 2025

## 🚀 Project Summary

A fully on-chain decentralized voting system built on the Internet Computer Protocol (ICP), designed to ensure anonymous yet secure participation using **zero-knowledge proofs (ZKPs)**, **Merkle tree commitments**, and **Internet Identity (II)** authentication.

This system allows individuals and DAOs to host elections where votes are:
- **Anonymous:** Voter identities are never revealed.
- **Verifiable:** All votes are publicly auditable.
- **Immutable:** Data is stored permanently and securely on ICP canisters.

---

## 🎯 Tracks Considered

- ✅ **Primary Track:** Fully On-Chain – Pure Decentralization

Rationale: The voting system is fully decentralized with on-chain data and logic. If the ZK components evolve into reusable infrastructure, the Open Track may be more appropriate.

---

## 🧩 Key Features

### ✅ 1. zkVote Module
- **Poseidon Hash:** Efficient cryptographic hash for zero-knowledge compatibility.
- **Merkle Commitments:** Voter eligibility is encoded as a Merkle tree.
- **ZK Proofs:** Users generate zk-SNARKs to prove they are in the Merkle tree **without revealing their identity**.
- **Ballot Submission:** Ballots are accepted only if the proof is valid and have not been submitted before.

### ✅ 2. Internet Identity Integration
- **One Vote per Principal:** Each Internet Identity anchor maps to a Merkle tree leaf.
- **Privacy:** The Internet Identity anchor is hashed before inclusion, maintaining anonymity.
- **No KYC Required:** Privacy-preserving and verifiable using only cryptographic methods.

### ✅ 3. Mainnet DAO Election Engine
- Any verified user can:
  - **Create an election** with voter list and options.
  - **Deploy a Merkle root** of eligible voters.
  - **Define a voting window** and ballot options.
- Voters use the frontend to:
  - **Log in via Internet Identity**
  - **Generate a ZK proof** of eligibility
  - **Submit an encrypted or private vote**

---

## 🛠️ proposed Tech Stack

| Component         | Tool / Language                  | Purpose                                                           |
|------------------|----------------------------------|-------------------------------------------------------------------|
| Smart Contracts   | Motoko or Rust on ICP            | Voting logic, proof validation, tallying, storage                 |
| Identity          | Internet Identity (ICP native)   | Authenticate users securely without revealing identity            |
| Frontend          | React + TypeScript               | User interaction, proof generation, II login                      |
| SDKs              | Dfinity SDK (`dfx`)              | Canister management and deployment                                |
| ZK Proofs         | Circom + SnarkJS                 | Define ZK circuits and generate/verify SNARKs                     |
| Hashing           | Poseidon hash in Circom          | Efficient for Merkle tree commitments and ZK compatibility        |
| Deployment        | ICP Mainnet                      | Host the app with canister IDs on the decentralized web           |
| UI Styling        | Tailwind CSS                     | Fast, modern styling for forms, buttons, and layouts              |

---

## 🧭 Development Roadmap

### 🔹 Phase 1: MVP (July 1–July 10)
- [ ] React frontend with Internet Identity login
- [ ] Motoko/Rust canister for:
  - Accepting one vote per identity
  - Basic on-chain ballot storage
- [ ] Simple Merkle tree voter list (JS)

### 🔹 Phase 2: ZK Integration (July 11–July 18)
- [ ] Design Circom circuit:
  - Proves membership in Merkle tree
- [ ] Use SnarkJS to generate and verify ZK proofs
- [ ] Validate proof before accepting vote

### 🔹 Phase 3: DAO Voting Toolkit (July 19–July 25)
- [ ] Election creation tool
- [ ] Public results dashboard
- [ ] Generalization for any DAO to reuse

---

## ✅ Submission Checklist

- [ ] 📦 Public GitHub repo with dfx.json
- [ ] 📝 README with setup, project description, proof explanation
- [ ] 🖼️ Screenshots of UI, proof generation, vote tally
- [ ] 🎥 5–10 min demo video with:
  - UI walk-through
  - Proof generation
  - Canister logic demo
- [ ] 💻 Live mainnet deployment with working canister ID
- [ ] 🧾 Optional: Pitch deck with team, problem, solution, roadmap

---

## 🏆 Strategic Advantages

- 🎯 Focused use case: Anonymous voting is a real-world need.
- 🔒 Privacy-first: Combines Internet Identity with ZK proofs.
- 🌐 Fully decentralized: All logic lives on-chain.
- 🔄 Reusable: Could become a general-purpose ZK election SDK.
- 🧠 Ambitious but scoped: Ideal for WCHL's 3-week build cycle.

---

## 🧠 Inspiration / Prior Art

- Semaphore by PSE (Ethereum ecosystem)
- Tornado Cash anonymity set design
- ZK-rollup voting experiments
- Gitcoin's ZK identity proof-of-humanity

---

## 🔗 Resources

- https://internetcomputer.org/docs/current/developer-docs/backend/canister-dev
- https://github.com/iden3/circom
- https://github.com/dfinity/examples
- https://github.com/privacy-scaling-explorations/semaphore
