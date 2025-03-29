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

### 3. Cross-Chain Bridge (`Brewery-Backend/`)

A Go-based service that enables cross-chain functionality:
- Syncs loan orders between chains
- Relays funding information
- Manages message passing between main and remote chains

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+)
- [Go](https://golang.org/) (v1.18+)
- [Foundry](https://book.getfoundry.sh/getting-started/installation.html)
- [Metamask](https://metamask.io/) or another Web3 wallet

### Installation

#### Clone the Repository

```bash
git clone https://github.com/your-username/Brewery-Lend.git
cd Brewery-Lend
```

#### Smart Contracts Setup

```bash
cd Brewery-Contracts
forge install
forge build
```

#### Frontend Setup

```bash
cd brewery-frontend
npm install
npm run dev
```

#### Bridge Setup

```bash
cd Brewery-Backend/hackathon-example
# Configure your bridge settings in config/config.json
go build
./hackathon-example
```

## 🔄 How It Works

### For Borrowers

1. Connect your wallet to the platform
2. Select an NFT from your wallet to use as collateral
3. Specify loan terms (amount, interest rate, duration)
4. Create the loan order and approve the NFT transfer
5. Receive USDC once a lender funds your loan
6. Repay the loan (principal + interest) before the deadline to reclaim your NFT

### For Lenders

1. Browse available loan orders
2. Review NFT collateral and loan terms
3. Fund a loan by providing the requested USDC amount
4. Earn interest when the borrower repays
5. Receive the NFT collateral if the borrower defaults

### Cross-Chain Flow

1. Borrower creates a loan on the main chain
2. The bridge relays the order to the remote chain
3. Lender on the remote chain funds the loan
4. The bridge notifies the main chain about the funding
5. Loan is processed on the main chain

## 🛠️ Technical Details

### Smart Contract Architecture

The protocol is built around a main contract and secure escrow system. All NFTs are held in escrow contracts during active loans, ensuring security for both borrowers and lenders.

### Security Measures

- Secure escrow for NFT collateral
- Rigorous testing with Foundry
- Clear ownership and transfer mechanisms
- Properly scoped approvals

### Cross-Chain Communication

The bridge uses a secure relay mechanism to pass messages between chains, enabling truly cross-chain functionality without sacrificing security.

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Contact

For questions or support, please open an issue in this repository.

---

Built with ❤️ by the Brewery Lend Team
