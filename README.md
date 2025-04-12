# Counter Contract – Foundry Demo

This is a simple smart contract project that demonstrates how to build, test, and deploy a basic `Counter` using [Foundry](https://book.getfoundry.sh/).

Foundry consists of:

-   **Forge**: Think of Forge as the power toolset for Ethereum developers—like Hardhat, Truffle, or DappTools—used for building, testing, and managing smart contracts with speed and precision.
-   **Cast**: * Imagine Cast as the Swiss army knife for Ethereum—it lets you poke, prod, and interact with smart contracts and the blockchain directly from your terminal, whether you're querying data or sending transactions.
-   **Anvil**: Anvil is your personal blockchain sandbox—a blazing-fast local Ethereum node, similar to Ganache or Hardhat Network, perfect for simulating real-world interactions during development and testing.
-   **Chisel**: Chisel is like a Solidity playground in your terminal—a rapid, interactive REPL (Read-Eval-Print Loop) where you can experiment with Solidity snippets and get instant feedback.

## Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation) installed
- [Git](https://git-scm.com/)
- [MetaMask](https://metamask.io/) with testnet (e.g. Sepolia) setup
- Sepolia ETH (via [faucet](https://sepoliafaucet.com/))

---

## 🛠️ Project Setup

### Installation

Getting started is simple and straight-forward:

Install `foundryup`:

```
curl -L https://foundry.paradigm.xyz | bash
```

Next, run `foundryup`.

It will automatically install the latest version of the precompiled binaries: [`forge`](#forge), [`cast`](#cast), [`anvil`](#anvil), and [`chisel`](#chisel).

```
foundryup
```

**Done!**

## Forge

### 1. Initialize Foundry project

```bash
forge init foundry-test
```

### 2. Move into the project folder

```bash
cd foundry-test
```

### 3. Install forge-std for scripting and testing

```bash
forge install foundry-rs/forge-std
```

### 4. Auto-generate remappings

````bash
forge remappings > remappings.txt
````

## Usage

### 5. Build

```shell
$ forge build
```

### 6. Test

```shell
$ forge test
```

### 7. Anvil

```shell
$ anvil
```

### 8. Finally, let's run our deployment script:

```sh
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>forge script script/Counter.s.sol
```







