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

## Upcoming Blockchain Integration
- NFT receipts as proof
- Sepolia testnet
- No on-chain money logic
