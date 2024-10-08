
# MyToken

This is a simple ERC20-like token contract named **MyToken** (symbol: MTA) that allows minting and burning of tokens. Users can increase or decrease their token balances, and the total supply adjusts accordingly.

## Description

The `MyToken` contract is a basic implementation of a token system with two primary functions:
- **Minting Tokens**: Increases the total supply and assigns the minted tokens to a specified address.
- **Burning Tokens**: Reduces the total supply and deducts tokens from a specified address, as long as the balance is sufficient.

## Features:
1. Public variables to store the token's name (`tokenName`), abbreviation (`tokenAbbrv`), and the total supply (`totalSupply`).
2. A mapping (`balances`) that associates an address with its token balance.
3. A **mint function** to increase the total supply and the balance of an address.
4. A **burn function** to decrease the total supply and the balance of an address, ensuring that the sender has enough tokens to burn.

## Getting Started

### Installing

To use this contract in your local environment, follow these steps:

1. Clone the repository from GitHub.
   ```bash
   git clone https://github.com/your-repo/your-project.git
   cd your-project
   ```

2. Install Solidity compiler if you don't have it already. You can use tools like **Remix**, **Hardhat**, or **Truffle** to compile and deploy the contract.

### Executing program

To deploy the contract, follow these steps:

1. Compile and deploy the `MyToken` contract using **Remix**, **Hardhat**, or **Truffle**. For **Remix**:
   1. Open the `MyToken.sol` file in Remix.
   2. Compile the contract.
   3. Deploy it to a local Ethereum network or testnet.

2. After deploying, you can interact with the contract through the following functions:
   
   - **Mint Tokens**: Mint new tokens to a specific address.
     ```solidity
     myToken.mint("0xAddress", 1000)
     ```
     This increases the total supply by 1000 and adds 1000 tokens to `0xAddress`.

   - **Burn Tokens**: Burn tokens from a specific address.
     ```solidity
     myToken.burn("0xAddress", 500)
     ```
     This reduces the total supply by 500 and removes 500 tokens from `0xAddress`, provided it has enough balance.

3. Example commands to deploy and interact using Hardhat:
   ```bash
   npx hardhat compile
   npx hardhat run scripts/deploy.js --network localhost
   ```

## Help

Common issues you might run into:
- **Insufficient Balance**: If an address doesn’t have enough tokens to burn, the transaction will fail.
- **Deployment Issues**: Ensure you're connected to the right network, and the Solidity version (`pragma solidity ^0.8.18`) is supported by your environment.

```bash
npx hardhat --help
```

## Authors

Yessine Maalej  
[@YessineMaalej](https://twitter.com/yessinemaalej)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

