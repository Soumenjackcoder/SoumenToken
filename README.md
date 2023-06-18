# Project's Title

SoumenToken(Based on solidity smart contract)

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has some functions where you can mine and burn this token. if you want to write your own token then you can use these functionalities.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., SoumenToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.4;

contract MyToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MAT";
    uint public toyalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balance;

    // mint function
    function mint(address _address, uint _value) public {
       toyalSupply += _value;
       balance[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
       if(balance[_address] >= _value) {
          toyalSupply -= _value;
          balance[_address] -= _value;
       }
    }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile SoumenToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "SoumenToken" contract from the dropdown menu, and then click on the "Deploy" button.
Once the contract is deployed, you can interact with it by calling these functions.

## Authors
Soumen Mandal 
[https://soumendev.com/]

