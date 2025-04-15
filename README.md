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

It will automatically install the latest version of the precompiled binaries: [`forge`](#forge) and [`anvil`](#anvil)

```
foundryup
```

**Done!**

## File Loactions
- **src**: This folder contains the main contract code
- **test**: contains the test code for your contract
- **script**: contains the code to deploy your contract on a testnet or local node

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

```bash
$ forge build
```

````console
[⠒] Compiling...
No files changed, compilation skipped
````

### 6. Test

```bash
$ forge test
```

````console
[⠊] Compiling...
No files changed, compilation skipped

Ran 2 tests for test/Counter.t.sol:CounterTest
[PASS] testFuzz_SetNumber(uint256) (runs: 256, μ: 32120, ~: 32354)
[PASS] test_Increment() (gas: 31851)
Suite result: ok. 2 passed; 0 failed; 0 skipped; finished in 27.08ms (19.18ms CPU time)

Ran 1 test suite in 344.97ms (27.08ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
````

## Anvil

You need to start an RPC-compatible node like Anvil or hardhat e.t.c. before deploying to a node
```bash
$ anvil
```


### 7. Finally, let's run our deployment script:

```sh
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>forge script script/Counter.s.sol
```

### (Optional) Use a Public RPC Instead (e.g., mainnet/testnet)

If you’re not trying to test against a local node but against a real network, you can use a public fork like:

````sh
--fork-url https://eth-mainnet.g.alchemy.com/v2/YOUR_KEY
````
or for a testnet:

````sh
--fork-url https://sepolia.infura.io/v3/YOUR_KEY
````
> [!IMPORTANT]  
> Just make sure your private key has ETH on that chain (or use one of the private keys in your local Anvil chain)






