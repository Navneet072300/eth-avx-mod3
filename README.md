# ETH-AVAX-MOD3
The program provided is an example of a smart contract written in Solidity.This program is an create and mint token program in which the contract owner will only able to mint tokens to a provided address. Any user can able to burn and transfer tokens.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain and Hardhat network is used like ERC20 and openzeppelin. The contract has a several function like onlyowner that only the owner can mint the token, mint to add some token, burn to withdraw som tokens and transfer to transfer from one address to another.

## Getting Started

### Executing program

To run this program, we have used Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., token.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Burnable.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyToken is ERC20, ERC20Burnable, Ownable {
    constructor() ERC20("META", "MTA") {}

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }
}





```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile token.sol" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "token" contract from the dropdown menu, and then click on the "Deploy" button.
Once the contract is deployed, mint some amount of token, check the balance using getBalance, name of contract from name and symbol from symbol. You can transfer token from one address to another using trnsfer and burn by using burn function.
## Authors

Navneet Shahi 



## License

This project is licensed under the MIT License. You are free to modify and distribute the code for personal and educational purposes.
