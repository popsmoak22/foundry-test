# Counter Contract – Foundry Demo

This is a simple smart contract project that demonstrates how to build, test, and deploy a basic `Counter` using [Foundry](https://book.getfoundry.sh/).

## Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation) installed
- [Git](https://git-scm.com/)
- [MetaMask](https://metamask.io/) with testnet (e.g. Sepolia) setup
- Sepolia ETH (via [faucet](https://sepoliafaucet.com/))

---

## 🛠️ Project Setup

### 1. Initialize Foundry project

```bash
forge init foundry-test
```

# 2. Move into the project folder

```bash
cd counter-foundry
```

# 3. Install forge-std for scripting and testing

```bash
forge install foundry-rs/forge-std
```

# 4. Auto-generate remappings

````bash
forge remappings > remappings.txt
````
