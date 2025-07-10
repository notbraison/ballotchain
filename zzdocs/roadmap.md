# 🗺️ BallotChain – Developer Roadmap (WCHL 2025)

A 3-week builder’s plan to launch a fully on-chain, anonymous voting dApp on the Internet Computer Protocol (ICP), powered by zero-knowledge proofs and Internet Identity.

---

## 📆 Timeline: July 1–25, 2025

---

## ✅ Week 1: MVP Foundations (July 1–7)

### 🎯 Objectives

- Set up dev environment and scaffolding
- Implement Internet Identity login
- Create canister logic for single-vote submission
- Build initial React UI for vote interaction

### 🔧 Tasks

#### Project Setup

- [ ] Install `dfx`, `node`, `npm`, `circom`, `snarkjs`
- [ ] Scaffold project:
  - `/frontend` – React + Tailwind
  - `/backend` – Motoko (or Rust) canister
  - `/zk` – Circom ZK circuits

#### Frontend (React + TypeScript)

- [ ] Set up Vite or Next.js with Tailwind CSS
- [ ] Implement Internet Identity login with `@dfinity/auth-client`
- [ ] Build a minimal vote form and display area

#### Backend (Motoko Canister)

- [ ] Write canister to:
  - Store election metadata
  - Accept votes
  - Track voted identities (hashed II anchors)
  - Count and return results

#### GitHub Repo

- [ ] Initialize `dfx.json`
- [ ] Push first commit
- [ ] Link repo to DoraHacks profile

---

## ✅ Week 2: ZK Integration (July 8–14)

### 🎯 Objectives

- Build and test zero-knowledge proof for voter eligibility
- Connect Circom proofs to frontend and backend
- Prevent double voting through Merkle membership proofs

### 🔐 Tasks

#### Circom Circuit (`/zk`)

- [ ] Define Merkle inclusion proof circuit
- [ ] Compile circuit and generate proving/verifying keys
- [ ] Test with `snarkjs` CLI locally

#### Frontend ZK Integration

- [ ] Create proof generator (Node/WASM version)
- [ ] Generate proof using identity hash and Merkle path
- [ ] Submit vote with ZK proof payload

#### Backend ZK Verification

- [ ] Add ZK verifier (Groth16 verifier)
- [ ] Verify proof inside the canister before storing vote
- [ ] Reject invalid or duplicate votes

#### Testing

- [ ] Use `dfx start` to simulate:
  - Login → proof gen → submit vote → tally → view results

---

## ✅ Week 3: DAO Election Engine & Mainnet Launch (July 15–21)

### 🎯 Objectives

- Enable admins to host elections
- Generate and manage Merkle roots per election
- Deploy system to ICP Mainnet

### 🗳️ DAO Voting Module

- [ ] Admin: create election (name, options, eligible voters)
- [ ] Upload voter list → generate Merkle tree → store root
- [ ] Assign election timeline and status

### 🔁 Backend Enhancements

- [ ] Support multiple elections
- [ ] Tally votes per election
- [ ] Prevent re-voting across elections

### 🌐 Deployment

- [ ] `dfx deploy --network ic` for mainnet
- [ ] Update frontend with deployed canister ID
- [ ] Test full flow with real Internet Identity login

---

## ✅ Finalization & Submission (July 22–25)

### 🎯 Objectives

- Finalize documentation and demo
- Submit working mainnet app with code and proof
- Record and edit demo video

### 📦 Project Wrap-up

- [ ] `README.md`: setup instructions, architecture, team
- [ ] Push final commits
- [ ] Write `info.md` and `roadmap.md`
- [ ] Link demo video and screenshots

### 🎥 Demo Video (5–10 mins)

- [ ] Show full voting flow
- [ ] Explain zk circuit, identity use, and smart contract logic

### 📝 Optional Pitch Deck

- [ ] Problem
- [ ] Solution (BallotChain)
- [ ] Technical architecture
- [ ] Roadmap / next steps

### 🚀 Submission

- [ ] Submit via DoraHacks
- [ ] Share project in Discord community
- [ ] Prepare for national round eligibility (top 50%)

---

## 📚 Resources

- [ICP Developer Docs](https://internetcomputer.org/docs/current/developer-docs/)
- [Circom](https://docs.circom.io/)
- [SnarkJS](https://github.com/iden3/snarkjs)
- [DFINITY Examples](https://github.com/dfinity/examples)
- [Internet Identity](https://identity.ic0.app/)
