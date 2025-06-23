
# Blockchain Developer, Smart Contract, & Solidity Career Path - Powered By AI - Beginner to Expert Course | Foundry Edition 2024

## Welcome to the Course Repository

This repository contains all the code, resources, and projects for the **Blockchain Developer, Smart Contract, & Solidity Career Path - Powered By AI - Beginner to Expert Course | Foundry Edition 2024** offered by [Cyfrin Updraft](https://www.cyfrin.io/). The course takes you from beginner to expert in smart contract development using **Solidity**, **Foundry**, and other cutting-edge tools, with a focus on hands-on projects and real-world blockchain applications.

[Cyfrin Updraft](https://github.com/Cyfrin/foundry-full-course-cu)
This repo includes projects for each section of the course, covering everything from basic Solidity programming to advanced topics like DeFi, NFTs, cross-chain applications, and smart contract security.

---

## Course Overview

The **Cyfrin Updraft** course is designed to teach you how to build, test, and deploy smart contracts using Solidity and Foundry. The course is divided into multiple sections, each focusing on a specific aspect of blockchain development. Below is the structure of the repository, with each folder corresponding to a section of the course.

### Repository Structure

| Folder Name                        | Description                                                                 |
|------------------------------------|-----------------------------------------------------------------------------|
| `01-Simple-storage`                | Basic Solidity contract for storing and retrieving data using Remix.         |
| `02-Remix-Storage-factory`         | Factory pattern for deploying contracts using Remix.                        |
| `03-remix-fund-me`                 | Crowdfunding smart contract with Chainlink price feeds using Remix.         |
| `04-foundry-simple-storage`        | Simple storage contract implemented using Foundry.                         |
| `05-foundry-fund-me`               | Crowdfunding contract with advanced testing and deployment using Foundry.   |
| `06-html-foundry-fund-me`          | Full-stack DApp with HTML/JavaScript frontend for the Fund Me contract.     |
| `07-foundry-smart-contract`        | Smart contract lottery using Chainlink VRF and Automation.                 |
| `08-foundry-erc20`                 | Custom ERC20 token implementation with Foundry.                            |
| `09-foundry-nft`                   | NFT contract with on-chain SVG and IPFS integration.                       |
| `10-foundry-defi-stablecoin`       | Decentralized stablecoin project with collateral and liquidation mechanics. |
| `11-foundry-crosschain-rebase`     | Cross-chain rebase token with Chainlink CCIP integration.                  |
| `12-foundry-merkle-airdrop-signature` | Merkle tree-based airdrop with signature verification.                    |
| `13-foundry-upgrade`               | Upgradable smart contracts using proxy patterns (UUPS).                    |
| `14-foundry-account-abstraction`    | Account abstraction implementation for Ethereum and ZKsync.                |
| `15-foundry-dao`                   | Decentralized Autonomous Organization (DAO) with governance mechanisms.    |
| `16-smartcontract-security-auditing` | Security best practices and auditing techniques for smart contracts.      |

---

## Getting Started

### Prerequisites

To follow along with the projects in this repository, you’ll need the following tools:

- **Node.js** and **npm**: For JavaScript-based frontends and dependency management.
- **Foundry**: Install Foundry for smart contract development and testing (`curl -L https://foundry.paradigm.xyz | bash`).
- **MetaMask**: For interacting with testnets like Sepolia and ZKsync.
- **VSCode**: Recommended IDE with extensions like Hardhat Solidity and Prettier.
- **Git**: For version control and cloning this repository.
- **Testnet ETH and LINK**: Use faucets for Sepolia or ZKsync to fund your wallet.

### Recommended Tools

- **Testnet**: Sepolia (preferred for this course).
- **DevOps Tools**: [foundry-devops](https://github.com/Cyfrin/foundry-devops) for deployment scripts.
- **Faucets**:
  - [Sepolia GCP Faucet](https://sepoliafaucet.com/)
  - [Alchemy Sepolia Faucet](https://sepoliafaucet.com/)
  - [Infura Sepolia Faucet](https://docs.metamask.io/developer-tools/faucet)
  - [Chainlink Sepolia Faucet](https://faucets.chain.link/sepolia)
  - [ZKsync Sepolia Faucet](https://docs.zksync.io/zksync-era/ecosystem/network-faucets)
- **Tenderly**: For virtual testnet simulations ([Sign up](https://tenderly.co/?mtm_campaign=partner&mtm_kwd=cyfrin)).
- **Chainlist**: For network configurations ([Chainlist](https://chainlist.org/)).
- **AI Tools**: Use [Claude](https://claude.ai), [ChatGPT](https://chatgpt.com), [Phind](https://phind.com), or [Gemini](https://gemini.google.com) for code assistance.

> **⚠️ Warning**: All code in this repository is for **demo purposes only** and has not been audited. Do not use in production without proper security audits.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/codebyankita/foundry-full-course-patrick.git
   ```

2. Install Foundry (if not already installed):
   ```bash
   curl -L https://foundry.paradigm.xyz | bash
   foundryup
   ```

3. Install dependencies for each project (where applicable):
   ```bash
   forge install
   ```

4. Set up environment variables:
   Create a `.env` file in the project root and add your private key, RPC URLs, and API keys (e.g., Etherscan, Alchemy). Example:
   ```bash
   PRIVATE_KEY=your_private_key
   SEPOLIA_RPC_URL=your_sepolia_rpc_url
   ETHERSCAN_API_KEY=your_etherscan_api_key
   ```

   > **Note**: Never commit your `.env` file or private keys to GitHub. Add `.env` to your `.gitignore`.

5. Compile and test a project:
   ```bash
   cd 04-foundry-simple-storage
   forge compile
   forge test
   ```

---

## Course Resources

Join the Cyfrin Updraft community and access additional resources:

- **Website**: [Cyfrin Updraft](https://www.cyfrin.io/) – 50+ hours of smart contract development courses.
- **Twitter**: Stay updated with course releases ([@Cyfrin](https://twitter.com/cyfrin)).
- **LinkedIn**: [Add Updraft to your learning experiences](https://www.linkedin.com/company/cyfrin).
- **Discord**: Join 3000+ developers and auditors ([Cyfrin Discord](https://discord.gg/cyfrin)).
- **Newsletter**: Weekly security research tips and resources.
- **Codehawks**: Participate in smart contract auditing competitions ([Codehawks](https://codehawks.com)).
- **YouTube**: Watch course videos and tutorials ([Cyfrin YouTube](https://www.youtube.com/c/Cyfrin)).

### Bonus NFTs

Complete challenges in each section to mint NFTs on **Sepolia** or **ZKsync**. Links to contracts and instructions are available in each project folder.

> **⚠️ ZKsync NFT Safety**: Use a burner wallet for minting NFTs on ZKsync to avoid risks, as these contracts are not audited. Follow [this Tweet thread](https://twitter.com/PatrickAlphaC/status/example) for wallet safety tips.

---

## Best Practices

1. **Follow the Repository**: Check the `chronological-updates` branch for updates and fixes.
2. **Engage with the Community**: Ask questions in the [GitHub Discussions](https://github.com/your-username/your-repo-name/discussions) or [Ethereum Stack Exchange](https://ethereum.stackexchange.com/).
3. **Learn at Your Own Pace**: Take breaks and refer to documentation frequently.
4. **Use AI Tools**: Leverage AI assistants like ChatGPT or Claude for debugging and learning.
5. **Secure Your Private Keys**: Never store private keys in plain text. Use encrypted keystores or tools like [Thirdweb Deploy](https://thirdweb.com).

---

## Contributing

Contributions are welcome! If you find bugs, have suggestions, or want to add improvements, please:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

---

## Disclosures

Transparency is key! The course instructor, Patrick Collins, is co-founder of:
- **Alpha Chain**: A blockchain infrastructure company working with Chainlink, Ethereum, and others.
- **Cyfrin**: A smart contract security and auditing service.
- **Chain Accel**: An advisor to the Peeranha project.

These affiliations may influence tool recommendations, but alternatives are provided for each section.

---

## License

This repository is licensed under the [GPLv3 License](LICENSE).

---

## Acknowledgments

- **Cyfrin Updraft**: For creating this comprehensive course.
- **Patrick Collins**: For guiding thousands of developers into Web3.
- **Chainlink**: For providing price feeds, VRF, and CCIP functionality.
- **ZKsync**: For Layer 2 scalability solutions.
- **Community**: For active participation and support in the blockchain space.

Happy coding, and welcome to the world of Web3 development! 🚀

(back to top) ⬆️
