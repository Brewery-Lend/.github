# Brewery Lend

![image](https://github.com/user-attachments/assets/4f1d3542-5069-4f2d-8048-6d389b9bb03c)

## 🍺 Overview

Brewery Lend is a decentralized finance (DeFi) platform that enables NFT owners to access liquidity without selling their digital assets. By using NFTs as collateral, users can borrow cryptocurrency while retaining ownership rights upon loan repayment. The platform also provides opportunities for lenders to earn interest by funding these loans.

### Key Features

- **NFT-Backed Loans**: Use any ERC-721 NFT as collateral to borrow USDC
- **Cross-Chain Functionality**: Operate across multiple blockchains through our bridge solution
- **Flexible Terms**: Customizable loan amounts, interest rates, and durations
- **Transparent Marketplace**: Clear visibility of all available loan opportunities
- **Secure Escrow**: NFT collateral held in secure smart contracts during loan periods

## 📚 Project Structure

The project consists of three main components:

### 1. Smart Contracts (`Brewery-Contracts/`)

The core protocol implemented as Solidity smart contracts:

- **BrewLend.sol**: Main contract managing the lending process, orders, funds, and repayments
- **CollateralEscrow.sol**: Secure storage for NFT collateral during loan periods
- **Interfaces.sol**: Shared interfaces and data structures

### 2. Frontend (`brewery-frontend/`)

A modern web application built with:
- Next.js
- React
- TypeScript
- TailwindCSS
- ethers.js/wagmi/RainbowKit for Web3 integration

