# FluxToken
This MyToken program in Solidity exemplifies the fundamental syntax and features of the Solidity programming language. This program's goal is to provide as a jumping-off point for individuals who are unfamiliar with Solidity and wish to acquire a sense of how it operates.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.

## Getting Started

### Executing program

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
      string public name = "VERMILLION";
      string public abbrv = "VRMLN";
      uint public supply = 0;
      
    // mapping variable here
      mapping(address => uint) public blnc;

    // mint function
      function mint(address add, uint val) public{
         supply += val;
         blnc[add] += val;
      }

    // burn function
      function burn(address add, uint val) public{
         if(blnc[add] >= val){
            supply -= val;
            blnc[add] -= val;
         }
      }
}

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile damski.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "damski.sol" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function. Click on the "damski" contract in the left-hand sidebar, and then click on the "mint" function, click on the "add" button but copy first the address of the account and paste it back on the add function. Finally, click the "val" and enter the amount and "transact" to execute the function and retrieve the token.
