## ETH_Project - ETH PROOF: Begginer EVM course

Introducing a fundamental Solidity smart contract with all the required functionality, such as token minting and burning, that simulates a token.


## Description

This program represents a contract written in the Solidity programming language, which is used to generate smart contracts on the Ethereum network. One program contains all of the material presented in the ETH Beginner Course under Solidity. A mapping from addresses to balances, a mint function that needs two inputs (an address and a value), and a burn function are a few examples of this. Public variables that store information about your coin are another.



## Getting Started and Code

You can use Remix, an online Solidity IDE, to run this application. Start using the Remix website by going to https://remix.ethereum.org/.

On the Remix website, click the "+" sign in the left sidebar to begin a new file. Save the file with the extension.sol, for instance, ETH!_Project.sol. After copying the code, paste it into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity >=0.6.12 <0.9.0;
```
It specifies that the code is written in Solidity and it is compatible with versions from 0.6.12 upto, but not including, 0.9.0.

```javascript
contract MyToken {

    // public variables here
    string public name = "TokenName";
    string public symbol = "TKN";
    uint256 public totalSupply = 0;
```
It creates a new contract named MyToken. 'string public name ="TokenName"' and string public symbol = "TKN"' represent name and symbol of the token respectively. 'uint256 public totalSupply=0' declares a public state variable 'totalSupply' which keeps track of total supply

```javascript
    mapping(address=> uint) public balance;
```
This line declares a public state variable 'balance' which is a mapping from address to integer.

```javascript
    function mint(address _account, uint256 _value) public {
        totalSupply += _value;
        balance[_account]+= _value;
    }
```
It is a public function that allows to increase the supply of tokens.  it increases the 'totalSupply' by '_value' and also increases the balance of '_account' by '_value'

```javascript
    function burn(address _account, uint256 _value) public {
        if(balance[_account]>= _value){
            totalSupply -= _value;
            balance[_account] -= _value;
        }
    }
}
```
It is a public function that allows to decrease the supply of tokens. If '_account' has atleast '_value' tokens, it decrease the 'totalSupply' by '_value' and also decreases the balance of '_account' by '_value'.

## Overview

The goal of this project is to give users a practical understanding of many of the subjects taught in the ETH_Beginner Course on Solidity. This software provides real-world examples and implementations to enhance learning and demonstrate how crucial Solidity concepts function.


