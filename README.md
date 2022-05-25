# BLOCKCHAINCODE
CODE
pragma solidity >0.8.0;
 
 
amithab.sol 

contract amithab {

    mapping(address => uint256) public balanceOf;   // balances, indexed by addresses
    
    function deposit(uint amount) public {    
        balanceOf[msg.sender] += amount;     // adjust the account's balance
    }
       

}
 
 
 abhishek.sol
    
 import "./amithab.sol";
    contract abhishek is amithab {

        function withdraw(uint amount) public {        
        require(amount <= balanceOf[msg.sender]);
        balanceOf[msg.sender] -= amount;
    }
    }
   
   
   
