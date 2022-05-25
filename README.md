# BLOCKCHAINCODE
CODE
pragma solidity >0.8.0;

contract Bank {

    mapping(address => uint256) public balanceOf;   // balances, indexed by addresses
    
    function deposit(uint amount) public {    
        balanceOf[msg.sender] += amount;     // adjust the account's balance
    }
         
    
    function withdraw(uint amount) public {        
        require(amount <= balanceOf[msg.sender]);
        balanceOf[msg.sender] -= amount;
        
    }
}
