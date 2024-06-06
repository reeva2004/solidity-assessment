## Create a Token

The solidity program "create a token" will demonstrate the basic of the topics like Data-Types, Mapping, Function Demonstration and conditional statement.

## Description

The Solidity code defines a smart contract named MyToken which implements a basic token system with minting and burning functionalities. The contract has three public variables: tokenName storing the name of the token "Exothm", tokenAbb storing the token's abbreviation "Ext", and totalSupply representing the total number of tokens in circulation, initially set to 0. It uses a mapping bal to associate each address with its token balance. The mint function allows new tokens to be created by increasing the totalSupply and the balance of the specified address. Conversely, the burn function destroys tokens by reducing both the totalSupply and the balance of the specified address, provided the address has enough tokens to burn. This ensures that tokens cannot be burned beyond the available balance.

## Getting Started

### Installing

To download the code, you can visit the following file path:-https://github.com/reeva2004/solidity-assessment/blob/main/assessment.sol

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:
contract MyToken {

    // public variables here
    string public tokenName = "Exothm";
    string public tokenAbb = "Ext";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address=>uint) public bal;

    // mint function
    function mint(address _address, uint _value) public{
        totalSupply += _value;
        bal[_address] += _value;

    }
    // burn function
    function burn(address _address, uint _value) public{
        if(bal[_address]>= _value){
            totalSupply -= _value;
            bal[_address] -= _value;
        } 

    } }


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you will set the value and address in right side under the MyToken contract. After initializing the value use the function mint and burn to check the working of code.


## Authors


Metacrafter Chris
@metacraftersio


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
