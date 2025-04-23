
# Vault Pool: Uniswap Integration

Welcome to the **Vault Pool** project, an implementation using Uniswap V3 for creating and managing liquidity pools on Ethereum. This repository contains code for building a vault pool, deploying smart contracts, and testing with Foundry. Below is the comprehensive guide for setting up, testing, and troubleshooting your development environment.

---

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation Guide](#installation-guide)
- [Set up](#set-up)
- [Local Development with Anvil](#local-development-anvil)
- [How to Run Scripts](#how-to-run-scripts)
- [Troubleshooting](#troubleshooting)
- [Learn More](#learn-more)
- [Contributing](#contributing)
- [Security Reports](#security-reports)

---

## Prerequisites

Before you begin, ensure you have the following tools installed on your machine:

- **[Foundry](https://book.getfoundry.sh)**: A fast, portable, and modular toolkit for Ethereum development.
- **[Anvil](https://book.getfoundry.sh/anvil/)**: A local Ethereum chain emulator that allows you to deploy and test smart contracts locally before moving to a real network.

---

## Installation Guide

1. **Install Foundry (Forge)**

   Foundry is the framework you will use for testing and deploying smart contracts.

   Install Foundry using the following command:

   ```bash
   foundryup
   ```

    To check if Foundry is correctly installed, run:

    ```bash
    forge --version
    ````

    If Foundry is not installed, follow [the installation guide](https://book.getfoundry.sh/) for detailed steps.

## Set up

Now that Foundry is set up, let's proceed with installing the dependencies and running tests:

1- Install dependencies:

Run this command to install required dependencies:

```bash

forge install
````

2- Run the tests:

Test the smart contracts and make sure everything is functioning as expected.

```bash
forge test
```

This will run the unit tests and verify if the Vault Pool contract is functioning properly.


## Local Development with Anvil
For local testing, you can deploy contracts and test them on Anvil, a local Ethereum chain emulator provided by Foundry. Anvil is perfect for testing without needing a live Ethereum network.

### Steps to start Anvil:

1- Start Anvil, a local Ethereum node:

In the terminal, run:
````
anvil
````

This starts a local instance of Anvil, which mimics the behavior of a real Ethereum network.

2- Deploy and interact with smart contracts:
In a new terminal window, you can deploy scripts, create pools, add liquidity, and swap tokens using Foundry's script feature. Run the following command to deploy the contracts and interact with them:

````bash
forge script script/Anvil.s.sol 
    --rpc-url http://localhost:8545 
    --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80 --broadcast
````

## How to Run Scripts
We have several pre-configured scripts for deploying hooks, creating pools, adding liquidity, and performing swaps. You can find these scripts in the script/ directory. Here's a breakdown of some common commands:

+ Deploy Contracts: To deploy the Vault Pool contract and its associated contracts, use the Anvil.s.sol script.

+ Add Liquidity: The script also contains functionality for adding liquidity to pools once deployed. This ensures that liquidity is available for swaps.

+ Perform Swaps: We have a method to perform swaps between tokens in the deployed pool. Make sure to configure the correct parameters when running the script.

## Learn More

To dive deeper into Solidity, Uniswap V3, and smart contract security, check out the following resources:

+ [Updraft by Cyfrin](https://updraft.cyfrin.io/)- A platform dedicated to Solidity and smart contract security.

+ [Solodit](https://solodit.cyfrin.io/) - Security Reports - Get security audits and reports for your projects.

+ [Beginner Friendly Audit Competitions](https://codehawks.cyfrin.io/first-flights) - Participate in competitions to learn and improve your skills.

+ [Cyfrin Certifications](https://updraft.cyfrin.io/certifications) - Get certified and gain recognition for your blockchain development skills.


### Contributing
We welcome contributions to improve this project! If you have suggestions, bug reports, or enhancements, feel free to submit a pull request or open an issue.

+ Fork this repository.

+ Clone your forked repository:

````
git clone https://github.com/your-username/VaultPool.git
````

+ Make your changes, and run tests to ensure everything works.

+ Submit a pull request with a detailed description of the changes you’ve made.

## Report an Issue or Suggest an Improvement: 
We prioritize the security of our code. If you encounter any potential security vulnerabilities and an issue, please reach out to us through the following link:

[Submit an Issues](https://github.com/SashaFlores/VaultPool/issues) 

[Want to discuss something or suggest an improvement](https://github.com/SashaFlores/VaultPool/discussions)

Stay safe and secure while building on blockchain!






