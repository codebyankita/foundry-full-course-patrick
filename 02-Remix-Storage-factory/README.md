# Fund Me Smart Contract - Cyfrin Foundry Blockchain Developer Course

*[⭐️ Cyfrin Updraft | Remix Storage Factory](https://updraft.cyfrin.io/courses/solidity/storage-factory/factory-introduction)*

*[🎥  (3:29:58) | Lesson 3 | Remix Storage Factory](https://www.youtube.com/watch?v=umepbfKp5rI&t=12598s)*

## Getting Started

1. Go to [Remix](https://remix.ethereum.org/)
2. Paste the code from `SimpleStorage.sol`, `StorageFactory.sol`, and `AddFiveStorage.sol` into a new file in Remix
3. Hit `Compile`
4. Hit `Deploy` for whatever contract you want.

## Resources talked about in the Video:
1. Bits and Bytes Video link by Linus Tech tips: https://www.youtube.com/watch?v=Dnd28lQHquU 

## Introduction

This repository contains the **Fund Me** smart contract project, part of the **Cyfrin Foundry Blockchain Developer Course** offered by [Cyfrin Updraft](https://www.cyfrin.io/). The project demonstrates how to build a crowdfunding smart contract using **Solidity**, integrated with **Chainlink Price Feeds** to handle real-world price data. The contract allows users to fund the contract in ETH, with a minimum funding requirement in USD, and includes functionality for the owner to withdraw funds.

This repo supports deployment on both **Ethereum Sepolia** and **ZKsync Sepolia** testnets, with detailed instructions for using **Remix** to compile and deploy the contract.

> **⚠️ Warning**: The code in this repository is for **educational purposes only** and has not been audited. Do not use in production without proper security audits.

---

## Course Context

This project is part of the **Solidity 101 Section 3: Remix Fund Me** from the Cyfrin Updraft course. For more details, visit:
- [⭐️ Cyfrin Updraft | Remix Fund Me](https://updraft.cyfrin.io/courses/solidity/fund-me/fund-me-intro)
- [🎥 YouTube | Fund Me Tutorial](https://www.youtube.com/watch?v=umepbfKp5rI&t=7842s) (part of Lesson 2)

---

## Getting Started

### Prerequisites

To deploy and interact with the **Fund Me** contract, you’ll need:
- **Remix**: Online IDE for Solidity development ([Remix](https://remix.ethereum.org/)).
- **MetaMask**: Browser extension for interacting with Ethereum and ZKsync testnets.
- **Testnet ETH and LINK**:
  - **Sepolia ETH**: Obtain from faucets like [Sepolia Faucet](https://sepolia-faucet.pk910.de/) or [Google Cloud Sepolia Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia).
  - **ZKsync Sepolia ETH**: Bridge ETH from Sepolia using [ZKsync Bridge](https://portal.zksync.io/bridge/).
  - **LINK Tokens**: Obtain from [Chainlink Sepolia Faucet](https://faucets.chain.link/sepolia).
- **Node.js** and **npm**: Optional, for local development or front-end integration.
- **Git**: For cloning this repository.

### Recommended Tools
- **Chainlink Price Feeds**: Use addresses from [Chainlink Price Feed Addresses](https://docs.chain.link/data-feeds/price-feeds/addresses?page=1&testnetPage=1).
- **Chainlist**: Configure testnet networks ([Chainlist](https://chainlist.org/)).
- **AI Tools**: Use [Claude](https://claude.ai), [ChatGPT](https://chatgpt.com), or [Phind](https://phind.com) for debugging assistance.

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Access Contract Files**:
   - For Ethereum Sepolia: Use `FundMe.sol` and `PriceConverter.sol`.
   - For ZKsync Sepolia: Use `FundMezkSync.sol`.

---

## Deploying on Ethereum Sepolia

### Steps
1. **Open Remix**:
   - Navigate to [Remix](https://remix.ethereum.org/).
2. **Create Contract Files**:
   - Create a new file named `FundMe.sol` and paste the code from `FundMe.sol`.
   - Create a new file named `PriceConverter.sol` and paste the code from `PriceConverter.sol`.
3. **Import Chainlink Interface**:
   - The `FundMe.sol` contract imports the `AggregatorV3Interface` from Chainlink:
     ```solidity
     import { AggregatorV3Interface } from "@chainlink/contracts/src/v0.8/shared/interfaces/AggregatorV3Interface.sol";
     ```
   - You can view the interface on GitHub: [AggregatorV3Interface.sol](https://github.com/smartcontractkit/chainlink/blob/develop/contracts/src/v0.8/shared/interfaces/AggregatorV3Interface.sol).
4. **Configure Price Feed**:
   - Use the appropriate Chainlink Price Feed address for Sepolia (e.g., ETH/USD). Find addresses at [Chainlink Price Feed Addresses](https://docs.chain.link/data-feeds/price-feeds/addresses?page=1&testnetPage=1).
   - For a sample contract to test price feeds, visit [Chainlink Data Feeds Getting Started](https://docs.chain.link/data-feeds/getting-started).
5. **Compile the Contract**:
   - Go to the **Solidity Compiler** tab in Remix.
   - Select Solidity version `0.8.x` (as specified in the contract).
   - Click **Compile FundMe.sol**.
6. **Deploy the Contract**:
   - Go to the **Deploy & Run Transactions** tab.
   - Select **Injected Provider - MetaMask** as the environment.
   - Connect your MetaMask wallet, ensuring it’s set to **Sepolia**.
   - Enter the Chainlink Price Feed address in the constructor field.
   - Click **Deploy**.
7. **Interact with the Contract**:
   - After deployment, the contract appears in the **Deployed Contracts** section.
   - **Blue buttons** (e.g., `getMinimumUSD`) allow reading data without transactions.
   - **Orange buttons** (e.g., `fund`) trigger transactions, requiring MetaMask confirmation and Sepolia ETH.
8. **Verify Deployment**:
   - Check the transaction on Sepolia Etherscan, e.g., [this transaction](https://sepolia.etherscan.io/tx/0x196ff92ff0974a2d9479fe13d7b782d5f0098b24e167cf91b872c7a76f3aea19).

> **Note**: Ensure you have sufficient Sepolia ETH. If faucets require 0.001 ETH on Ethereum Mainnet, try alternatives like [Sepolia Faucet](https://sepolia-faucet.pk910.de/) or wait 10–20 minutes before retrying.

---

## Deploying on ZKsync Sepolia

### Steps
1. **Open Remix**:
   - Navigate to [Remix](https://remix.ethereum.org/).
2. **Install ZKsync Plugin**:
   - Go to the **Plugin Manager** (plug icon on the left sidebar).
   - Search for **ZKsync** and activate the plugin.
3. **Create Contract File**:
   - Create a folder named `contracts` in the Remix file explorer.
   - Inside `contracts`, create a new file named `FundMezkSync.sol` and paste the code from `FundMezkSync.sol`.
4. **Configure Price Feed**:
   - Ensure the contract uses a ZKsync-compatible Chainlink Price Feed address. Refer to [Chainlink Price Feed Addresses](https://docs.chain.link/data-feeds/price-feeds/addresses?page=1&testnetPage=1).
5. **Compile the Contract**:
   - Go to the **Solidity Compiler** tab, ensuring the ZKsync plugin is active.
   - Select Solidity version `0.8.24` (recommended for ZKsync).
   - Click **Compile FundMezkSync.sol**.
6. **Deploy the Contract**:
   - Go to the **Deploy & Run Transactions** tab.
   - Select **ZKsync** as the environment.
   - Connect your MetaMask wallet, ensuring it’s set to **ZKsync Sepolia**.
   - Enter the Chainlink Price Feed address in the constructor field.
   - Click **Deploy**.
7. **Interact with the Contract**:
   - After deployment, use the **blue buttons** for read-only functions and **orange buttons** for write functions, confirming transactions via MetaMask.
8. **Verify Deployment**:
   - Check the deployed contract on ZKsync Sepolia Explorer, e.g., [this contract](https://sepolia.explorer.zksync.io/address/0x17aeA8944A32FFEc1Ce197cD7023aB555623b1b6).
   - View bridging transactions, e.g., [this transaction](https://portal.zksync.io/transaction/0x32b685e3f8b3aaf334fd0fa9e1d54b7f0e2bb2781b875b91a0d7ceb1a510dd7c?network=sepolia).
9. **Bridging to ZKsync**:
   - Obtain ZKsync Sepolia ETH by bridging ETH from Ethereum Sepolia using [ZKsync Bridge](https://portal.zksync.io/bridge/).
   - Steps:
     1. Buy ETH on an exchange (e.g., Coinbase, Kraken).
     2. Send ETH to your MetaMask wallet.
     3. Use the ZKsync Bridge to transfer ETH to ZKsync Sepolia.

> **⚠️ Note**: Use a **burner wallet** with minimal funds for ZKsync interactions to avoid risks, as the contract is not audited.

---

## Troubleshooting

### Faucet Issues
If faucets like [Chainlink Faucet](https://faucets.chain.link/sepolia) require 0.001 ETH on Ethereum Mainnet:
- Try alternative faucets:
  - [Sepolia Faucet](https://sepolia-faucet.pk910.de/)
  - [Google Cloud Sepolia Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)
- Wait 10–20 minutes and retry the Chainlink Faucet.
- Ensure your wallet has LINK tokens for contracts requiring Chainlink services.

### Compilation Errors in Remix
- For ZKsync, ensure the contract is placed in a `contracts` folder.
- Verify the Solidity version matches the contract’s pragma (e.g., `0.8.24`).
- Check that the ZKsync plugin is active.

---

## Course Resources

- **Website**: [Cyfrin Updraft](https://www.cyfrin.io/) – 50+ hours of smart contract courses.
- **YouTube**: [Fund Me Tutorial](https://www.youtube.com/watch?v=umepbfKp5rI&t=7842s).
- **Twitter**: Follow for updates ([@Cyfrin](https://twitter.com/cyfrin)).
- **Discord**: Join 3000+ developers ([Cyfrin Discord](https://discord.gg/cyfrin)).
- **Codehawks**: Auditing competitions ([Codehawks](https://codehawks.com)).
- **GitHub Discussions**: Ask questions ([Discussions](https://github.com/your-username/your-repo-name/discussions)).
- **Ethereum Stack Exchange**: Technical Q&A ([Stack Exchange](https://ethereum.stackexchange.com/)).
- **Chainlink Docs**: [Deploy Your First Contract](https://docs.chain.link/docs/deploy-your-first-contract/).

---

## Best Practices

1. **Verify Price Feed Addresses**: Always use Chainlink’s official addresses from [Chainlink Price Feed Addresses](https://docs.chain.link/data-feeds/price-feeds/addresses?page=1&testnetPage=1).
2. **Secure Your Wallet**: Use a burner wallet for ZKsync and never expose private keys.
3. **Test Read Functions First**: Use blue buttons to verify contract state before triggering transactions.
4. **Engage with the Community**: Ask questions in GitHub Discussions or Cyfrin Discord.
5. **Use AI Tools**: Leverage Claude or ChatGPT for debugging and understanding code.

---

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

---

## Disclosures

The course instructor, Patrick Collins, is co-founder of:
- **Alpha Chain**: Blockchain infrastructure company.
- **Cyfrin**: Smart contract security and auditing service.
- **Chain Accel**: Advisor to Peeranha.

These affiliations may influence tool recommendations, but alternatives are provided.

---

## License

This repository is licensed under the [GPLv3 License](LICENSE).

---

## Acknowledgments

- **Cyfrin Updraft**: For the comprehensive course.
- **Patrick Collins**: For guiding Web3 developers.
- **Chainlink**: For price feeds and documentation.
- **ZKsync**: For Layer 2 scalability.

### Support the Creator
If you found this project helpful, consider:
- **Donation**: `cyfrin1.eth` (`0x3846c3A30E62075Fa916216b35EF04B8F53931f6`)
- **Follow**:
  - [Twitter](https://twitter.com/PatrickAlphaC)
  - [YouTube](https://www.youtube.com/channel/UCn-3f8tw_E1jZvhuHatROwA)
  - [LinkedIn](https://www.linkedin.com/in/patrickalphac/)
  - [Medium](https://medium.com/@patrick.collins_58673/)

Happy coding, and welcome to Web3! 🚀

(back to top) ⬆️
