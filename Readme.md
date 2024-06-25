# Smart contract to create your own ERC20 token

Creating a Smart Contract (ERC20 token)on Remix with '.sol' extension. And is made with the help 
of OpenZeppelin


## Description

This smart contract is designed to illustrate various essential features of token, including:

1. Mint tokens.
2. Burn tokens.
3. Transfer tokens.


## Getting Started

### Installing

This program runs on EVM along with ".sol" as extension. We can either run it on websites like Remix.

### Executing program

We need a solidity compatible virtual machine in order to run this program.
Create a new file with ".sol" extension
```
// SPDX-License-Identifier: MIT
// Compatible with OpenZeppelin Contracts ^5.0.0
pragma solidity ^0.8.20;

import "@openzeppelin/contracts@5.0.2/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts@5.0.2/token/ERC20/extensions/ERC20Burnable.sol";
import "@openzeppelin/contracts@5.0.2/access/Ownable.sol";

contract Sparsh is ERC20, ERC20Burnable, Ownable {
    constructor(address initialOwner)
        ERC20("Sparsh", "SAM")
        Ownable(initialOwner)
    {
        _mint(msg.sender, 1000 * 10 ** decimals());
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }
}

```


## Help

Common Issues:
User must have knowledge about OpenZeppelin and how to manipulate 'wizard' in order to create the 
ERC20 token.


## Authors


Contributors names and contact info


ex. Sparsh Shandil 
ex. [@Allegiantshark](https://linktr.ee/allegiantshark)


## License

This project is licensed under the Sparsh Shandil License - see the LICENSE.md file for details
