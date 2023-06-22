## MyToken

This Solidity smart contract demonstrates minting of our own token of whatever name we want and burn it as well.

## Description

This program is a smart contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a mainly Two function that are "Mint" and "Burn" function, which is used to mint and burn the values. There are public variables like string, uint, etc, and even has the mapping of addressses to balances.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName="CAT";
    string public tokenAbbrv="MEOW";
    uint public totalSupply=0;
    // mapping variable here
    mapping(address=>uint) public balances;
    // mint function
    function mint(address _address,uint _value) public {
        totalSupply+=_value;
        balances[_address]+=_value;
    }
    // burn function
    function burn(address _address,uint _value) public {
        if(balances[_address]>=_value){
            totalSupply-=_value;
            balances[_address]-=_value;
        }
    }

}



To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it. After, that to check whether the contract is running successfully we can check by performing the minting and the burning function. We can check the TotalCount, TotalAbrrevation, Balance, too. After, the Deployment of Contract copy the initial address above and then paste down to the left-most side where u can see the TotalCount, TotalAbbrv, Balances, Mint, Burn, etc and then You can perform the basic task that the contract has. So, atlast we can see all the things are performed well and as said.

## Authors

Metacrafter Krtik
[@metacraftersio](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License.
