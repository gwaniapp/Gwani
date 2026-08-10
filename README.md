# Gwani Wallet

Gwani Wallet is a non-custodial Stellar wallet MVP focused on providing a simple interface for managing Stellar Testnet accounts, viewing balances, signing transactions, and verifying on-chain activity.

## Project Status

🚧 **Development / Stellar Testnet MVP**

This repository contains the implementation developed as part of a 30-day engineering milestone focused on building core non-custodial wallet functionality on Stellar Testnet.

## Objective

The objective of Gwani Wallet is to provide a simple wallet experience that allows users to:

- Create or import a Stellar wallet
- Manage their Stellar account locally
- View their account address
- View XLM and supported asset balances
- Construct and sign Stellar transactions
- Submit transactions to Stellar Testnet
- View transaction history
- Verify transactions through Stellar's public network data

Gwani Wallet does not use a backend service to custody or manage users' private keys.

## Core Features

### 1. Wallet Creation

Users can create a new Stellar wallet and generate a corresponding Stellar account keypair.

### 2. Wallet Import

Users can restore an existing wallet using the supported wallet recovery mechanism.

### 3. Local Key Management

Private wallet credentials are handled locally by the application and are not intended to be stored on a centralized backend.

### 4. Stellar Testnet Integration

The application connects to Stellar Testnet for development and testing.

### 5. Account Balance

Users can view:

- Stellar account address
- XLM balance
- Supported Stellar asset balances

### 6. Transaction Signing

Transactions are constructed and signed through the wallet before being submitted to Stellar Testnet.

### 7. XLM Transfers

Users can initiate Testnet XLM transfers to another Stellar account.

### 8. Transaction History

The wallet displays recent account activity and transaction details.

### 9. Transaction Verification

Completed transactions include a transaction hash that can be independently verified using a Stellar Testnet explorer.

## Technology Stack

- TypeScript / JavaScript
- Stellar Wallet SDK
- Stellar SDK
- React / frontend framework
- Stellar Testnet
- GitHub

> Update this section if the actual implementation uses a different framework or language.

## Stellar Integration

Gwani Wallet is built using Stellar's wallet-development tooling and Testnet environment.

The implementation follows the general Stellar wallet architecture for:

1. Wallet initialization
2. Stellar account management
3. Transaction construction
4. Transaction signing
5. Transaction submission
6. Account and transaction data retrieval

Official Stellar documentation:

https://developers.stellar.org/docs/build/apps/wallet

## Network

### Stellar Testnet

Gwani Wallet currently operates against **Stellar Testnet** for development and testing.

Testnet is used because it provides a stable environment that mirrors important Mainnet functionality without involving real funds.

**Important:** Testnet data and accounts may be reset by Stellar, so Testnet accounts and transaction history should not be treated as permanent production data.

## Project Architecture

```text
Gwani Wallet
│
├── Wallet Core
│   ├── Wallet Creation
│   ├── Wallet Import
│   └── Local Key Management
│
├── Stellar Integration
│   ├── Account Service
│   ├── Balance Service
│   ├── Transaction Builder
│   ├── Transaction Signer
│   └── Transaction Submission
│
├── User Interface
│   ├── Wallet Dashboard
│   ├── Send
│   ├── Assets
│   └── Transaction History
│
└── Testing
    ├── Wallet Tests
    ├── Transaction Tests
    └── Testnet Integration Tests
