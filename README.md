# MyToken Smart Contract

This repository contains a Solidity smart contract for the creation and management of a custom ERC20 token called MyToken (MCT). The contract provides functionalities for token minting, burning, and transferring, along with ownership management.

## Contract Details

### Overview

MyToken is an ERC20 token that extends the functionality of OpenZeppelin's `ERC20` and `Ownable` contracts. It allows for the creation of a custom token with the ability to mint new tokens, burn existing tokens, and transfer tokens between addresses.

### Features

1. **Token Minting:** Only the contract owner can mint new tokens. Minting is performed using the `mintTokens` function, allowing the owner to increase the token supply.
   
2. **Token Burning:** Token holders can burn their own tokens using the `burnTokens` function, which reduces the total supply of tokens. This operation is irreversible.
   
3. **Token Transferring:** Token holders can transfer tokens to other addresses using the `transferTokens` function, which utilizes the standard ERC20 `transfer` function internally.

### Events

The contract emits three events to track important token-related activities:

- `TokensMinted`: Emits when new tokens are minted.
- `TokensBurnt`: Emits when tokens are burned.
- `TokensTransferred`: Emits when tokens are transferred between addresses.

### Contract Initialization

The contract is initialized with the name "MyToken" and the symbol "MCT" during deployment. The initial owner of the contract is specified through the constructor.

## Getting Started

To use this contract, you can deploy it on a compatible Ethereum Virtual Machine (EVM) such as Ethereum mainnet, testnets like Ropsten, Rinkeby, or locally on a development environment like Ganache.

Ensure that you have the necessary dependencies installed, including Solidity compiler version ^0.8.18 and OpenZeppelin contracts.

### Deployment

Deploy the contract to your chosen EVM network using tools like Remix, Truffle, or Hardhat.

### Interacting with the Contract

After deployment, interact with the contract using Ethereum wallets or through other smart contracts. Here are some sample interactions:

- Mint new tokens: Call the `mintTokens` function with the recipient address and the amount of tokens to mint.
- Burn tokens: Call the `burnTokens` function with the amount of tokens to burn.
- Transfer tokens: Use the `transferTokens` function to transfer tokens from one address to another.

## Security Considerations

- Ensure that only authorized entities have access to functions like minting and burning tokens.
- Review and test the contract thoroughly before deployment to prevent potential vulnerabilities.

## License

This project is licensed under the terms of the MIT license. See the `LICENSE` file for more details.

