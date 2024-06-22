#ETH_Project-ETH PROOF: Begginer EVM course

Introducing a fundamental Solidity smart contract with all the required functionality, such as token minting and burning, that simulates a token.


##Description

This program represents a contract written in the Solidity programming language, which is used to generate smart contracts on the Ethereum network. One program contains all of the material presented in the ETH Beginner Course under Solidity. A mapping from addresses to balances, a mint function that needs two inputs (an address and a value), and a burn function are a few examples of this. Public variables that store information about your coin are another.



##Getting Started and Code

You can use Remix, an online Solidity IDE, to run this application. Start using the Remix website by going to https://remix.ethereum.org/.

On the Remix website, click the "+" sign in the left sidebar to begin a new file. Save the file with the extension.sol, for instance, ETH!_Project.sol. After copying the code, paste it into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity >=0.6.12 <0.9.0;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here
    string public name = "TokenName";
    string public symbol = "TKN";
    uint256 public totalSupply = 0;
    
    // mapping variable here
    mapping(address=> uint) public balance;
    // mint function
    function mint(address _account, uint256 _value) public {
        totalSupply += _value;
        balance[_account]+= _value;
    }
    // burn function
    function burn(address _account, uint256 _value) public {
        if(balance[_account]>= _value){
            totalSupply -= _value;
            balance[_account] -= _value;
        }
    }
}
```
##Overview

The goal of this project is to give users a practical understanding of many of the subjects taught in the ETH_Beginner Course on Solidity. This software provides real-world examples and implementations to enhance learning and demonstrate how crucial Solidity concepts function.


