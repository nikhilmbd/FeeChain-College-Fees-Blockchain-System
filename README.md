# College Finance Blockchain System

A secure college finance management system that uses blockchain-based NFT receipts
to provide transparent, tamper-proof fee payment records for students and administrators.

## Problem Statement
Traditional college fee systems lack transparency, verifiable proof of payment,
and centralized dashboards for students and administrators.

## Planned Tech Stack
- Frontend: Next.js, React
- Backend: Next.js API routes
- Blockchain: Smart contracts, NFT receipts
- Cloud: Firebase, Google Cloud
- 
## NFT Receipt (Future Design)
- studentId
- feeId
- paymentId
- txHash
- tokenId
- timestamp

## Purpose:
- Acts as immutable proof of payment
- Minted only after off-chain payment success

## Payment Flow

- Off-chain payment records
- Firestore-based payment status
- Blockchain used only for proof

## 🧾 NFT-Based Fee Receipt System (Blockchain Integration)

### 🔍 Why NFT Receipts?

Traditional college fee receipts are stored in centralized databases, which can be altered, deleted, or lost.
To improve transparency and trust, this project uses **NFT-based receipts** as immutable proof of fee payment.

Each NFT represents a **single confirmed fee payment** and acts as a permanent digital receipt that can be independently verified on the blockchain.

---

### ⛓️ What Is Stored On-Chain?

The blockchain is used **only for proof**, not for payment processing.

When a fee payment is successfully completed:
- An **ERC-721 NFT receipt** is minted on the **Ethereum Sepolia testnet**
- The smart contract emits an on-chain event containing:
  - `studentId` (reference only)
  - `feeId` (reference only)
  - `paymentId` (reference only)
  - `tokenId` (NFT receipt ID)
  - `timestamp`

⚠️ No money, personal data, or sensitive information is stored on the blockchain.

---

### 🔥 What Stays in Firebase (Off-Chain)?

Firebase is used for all operational and real-time data, including:
- Student profiles
- Fee details
- Payment records
- Payment status (`initiated`, `success`, `failed`)
- Role-based access control (Student / Admin)

Firebase handles efficiency and scalability, while blockchain provides immutable verification.

---

### 🔐 How Blockchain Improves Trust

Blockchain ensures that once a fee receipt NFT is minted:
- It **cannot be modified or deleted**
- The transaction is **publicly verifiable**
- Anyone can verify the receipt using:
  - Contract address
  - Transaction hash
  - Event logs on the blockchain explorer

This increases transparency and trust between students, institutions, and auditors.

---

### 🧠 Design Principle (Key Idea)

> **Payment logic stays off-chain for efficiency, while proof of payment goes on-chain for immutability.**

This hybrid approach avoids unnecessary blockchain costs while still leveraging its strongest feature — trust without intermediaries.
