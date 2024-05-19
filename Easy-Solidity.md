# Welcome to the first section to the RareSkills interview questions.

# Easy Solidity Interview Questions

### 1. What is the difference between private, internal, public, and external functions?
=>  Private: can only be called by functions in the same contract.

=>  Internal: can only be called by functions in the same contract or in contracts that inherit from that contract.

=>  Public: can be called by anyone.

=>  External: can only be called by functions outside the contract

### 2. Approximately, how large can a smart contract be?
=>  A smart contract can be as large as 24,576 bytes or 24K bytes

### 3. What is the difference between create and create2?
=> The main difference lies in how calculate predict the address of a smart contract.

CREATE allows the user to calculate or derive a contract address by the sender's address and a nonce, But it becomes less predictable when the nonce changes between the address calculation and contract creation as nounces are non-reuseable and must follow a sequential order.

new_address = hash(sender, nonce)

while...

CREATE2 determines the address by an arbitrary salt value and the init_code. It ensures that the address is not affected by future events and it's independent.

new_address = hash(0xFF, sender, salt, bytecode)

The computation of the new address is determined by the following factors which are : 

0xFF :  serving as a constant to avert collisions with CREATE.

sender: The sender’s address

salt:  A salt (32 bytes), an arbitrary value supplied by the sender

bytecode : The bytecode of the contract slated for deployment.

The CREATE2 opcode generates a smart contract with address determined by the combination of salt value and contract creation code.

### 4. What major change with arithmetic happened with Solidity 0.8.0?
=> It reverts with underflow/ overflow

### 5. What special CALL is required for proxies to work?
=> The special call required for proxies to work is delegatecall().

### 6. Prior to EIP-1559, how do you calculate the dollar cost of an Ethereum transaction?
=> Prior to the EIP-1559, the cost of dollar transactin was calculated as: 

          ==> ((GAS USED * GAS PRICE / 10^-9) * CURRENT ETHER PRICE.
          
    During the period when EIP-1559 was used, the miner gets 100% gas cost.

### 7. What are the challenges of creating a random number on the blockchain?

### 8. What is the difference between a Dutch Auction and an English Auction?

### 9. What is the difference between transfer and transferFrom in ERC20?

### 10. Which is better to use for an address allowlist: a mapping or an array? Why?

### 11. Why shouldn’t tx.origin be used for authentication?

### 12. What hash function does Ethereum primarily use?

### 13. How much is 1 gwei of Ether?
    
### 15. How much is 1 wei of Ether?

### 16. What is the difference between assert and require?

### 17. What is a flash loan?

### 18. What is the check-effects pattern?

### 19. What is the minimum amount of Ether required to run a solo staking node?

### 20. What is the difference between fallback and receive?

### 21. What is reentrancy?

### 22. As of the Shanghai upgrade, what is the gas limit per block?

### 23. What prevents infinite loops from running forever?

### 24. What is the difference between tx.origin and msg.sender?

### 25. How do you send Ether to a contract that does not have payable functions, or a receive or fallback?

### 26. What is the difference between view and pure?

### 27. What is the difference between transferFrom and safeTransferFrom in ERC721?

### 28. How can an ERC1155 token be made into a non-fungible token?

### 29. What is access control and why is it important?

### 30. What does a modifier do?

### 31. What is the largest value a uint256 can store?

### 32. What is variable and fixed interest rate?
