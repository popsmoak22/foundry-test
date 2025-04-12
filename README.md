# 🧮 Counter Contract – Foundry Demo

This is a simple smart contract project that demonstrates how to build, test, and deploy a basic `Counter` using [Foundry](https://book.getfoundry.sh/).

## 📦 Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation) installed
- [Git](https://git-scm.com/)
- [MetaMask](https://metamask.io/) with testnet (e.g. Sepolia) setup
- Sepolia ETH (via [faucet](https://sepoliafaucet.com/))

---

## 🛠️ Project Setup

```bash
# 1. Initialize Foundry project
forge init counter-foundry

# 2. Move into the project folder
cd counter-foundry

# 3. Install forge-std for scripting and testing
forge install foundry-rs/forge-std

# 4. Auto-generate remappings
forge remappings > remappings.txt
