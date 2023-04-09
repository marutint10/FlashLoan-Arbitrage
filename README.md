# FlashLoan Arbitrage

This smart contract performs a flashloan arbitrage between Aave's USDC and DAI. It performs the following operations:

Deposit 1,000,000,000 USDC to a DEX contract (dexContractAddress) using the depositUSDC() function.
Buy DAI from the DEX contract using the buyDAI() function.
Deposit the DAI bought in the previous step to the DEX contract using the depositDAI() function.
Sell the deposited DAI for USDC using the sellDAI() function.
The smart contract repays the flashloan and keeps the profit if the arbitrage opportunity is profitable.

### Prerequisites

1. Hardhat
2. Aave Protocol V3
3. OpenZeppelin

### Deployement

1. Clone this repository:

```bash
git clone https://github.com/marutint10/FlashLoan-Arbitrage
```

2. Install the Repo:

```bash
npm install
```

3. Compile the contract

```bash
npx hardhat compile
```

4. deploy the contract:

```bash
npx hardhat run scripts/deployDex.js --network <netowrk-name>
```

- change the address of dexContractAddress

```bash
npx hardhat run scripts/deployFlashLoanArbitrage.js --network <netowrk-name>
```

### Usages

The smart contract can be used to perform a flashloan arbitrage between Aave's USDC and DAI.

1. Call the requestFlashLoan(address \_token, uint256 \_amount) function, where \_token is the token to be flashloaned and \_amount is the amount to be flashloaned.
2. Wait for the executeOperation() function to execute the arbitrage operation.
3. The smart contract will repay the flashloan and keep the profit if the arbitrage opportunity is profitable.

### License

This project is licensed under the MIT License. See the LICENSE file for more information.
