# STXWillChain- Automated Will Execution

## Overview
This smart contract automates the execution of a will using blockchain technology, incorporating features such as:
- **Time-locked distributions** to ensure assets are claimed only after a set period.
- **Multi-oracle verification** for confirming the owner's passing.
- **NFT inheritance** to distribute digital assets securely.
- **Dispute resolution** with voting mechanisms.
- **Phased inheritance releases** for controlled asset distribution.

## Features
### 1. Oracle-Based Death Confirmation
- Requires multiple oracle confirmations before executing the will.
- Uses a **multi-signature** approach for verification.

### 2. Beneficiary & Asset Management
- Adds beneficiaries with a **percentage share of assets**.
- Supports **NFT allocation** for digital asset inheritance.
- Implements **time-locked asset claims** for delayed distribution.

### 3. Secure Fund Transfer
- Ensures **inheritance tax deduction** (default 2%).
- Transfers STX tokens and NFTs securely.

### 4. Dispute Resolution Mechanism
- Allows raising disputes with **evidence submission**.
- Uses **on-chain voting** to resolve disputes fairly.
- Implements an **automatic resolution** mechanism after voting.

### 5. Emergency & Administrative Functions
- Enables **contract deactivation** for emergency cases.
- Allows **updating required oracle confirmations**.
- Provides **read-only queries** for contract status and beneficiary info.

## Functions
### Public Functions
1. **initialize-contract (oracle-list)** - Registers multiple oracles.
2. **add-beneficiary (beneficiary, share, lock-period, nft-list)** - Assigns shares and NFTs.
3. **confirm-death ()** - Oracle confirms owner's passing.
4. **update-will-hash (new-hash)** - Updates the hash of the last will.
5. **claim-inheritance ()** - Allows beneficiaries to claim assets.
6. **raise-dispute (evidence-hash)** - Submits a dispute.
7. **deactivate-contract ()** - Deactivates the contract.
8. **update-required-confirmations (new-count)** - Adjusts the number of confirmations needed.

### Read-Only Functions
1. **get-beneficiary-info (beneficiary)** - Fetches a beneficiary's details.
2. **get-contract-status ()** - Returns contract status details.
3. **get-nft-owner (token-id)** - Checks NFT ownership.

## Security Measures
- **Role-based access control**: Only the contract owner can manage beneficiaries and will updates.
- **Multi-oracle validation**: Prevents fraudulent death confirmations.
- **Time-locked distribution**: Ensures planned asset transfers.
- **Dispute resolution process**: Prevents wrongful inheritance claims.

## Deployment & Usage
1. Deploy the contract and set the **contract owner**.
2. Register trusted oracles for death confirmation.
3. Add beneficiaries, specifying share amounts and NFT allocations.
4. Once oracles confirm the owner's passing, beneficiaries can claim their inheritance.
5. If any disputes arise, the dispute resolution process will be activated.

## Potential Enhancements
- Integrating decentralized identity (DID) verification for oracles.
- Allowing customizable tax rates per beneficiary.
- Enhancing dispute resolution with AI-driven arbitration.

## License
This contract is open-source and distributed under the MIT License.

