# Multisignature-wallet
This is a smart contract written in the Solidity programming language for a MultiSig wallet. MultiSig, short for multi-signature, is a type of digital wallet that requires multiple signatures or approvals from a group of owners before any transaction can be executed.

The contract includes the following:

- `address[] public owners`: an array to store the addresses of the owners of the wallet
- `uint public numConfirmationsRequired`: the minimum number of approvals required for a transaction to be executed
- `struct Transaction`: a struct to store information about a transaction, including the receiver's address and the amount to be transferred
- `mapping(uint=>mapping(address=>bool)) isConfirmed`: a mapping to keep track of which owners have confirmed a particular transaction
- `Transaction[] public transactions`: an array to store all the pending transactions
- `event TransactionSubmitted`: an event emitted when a new transaction is submitted
- `event TransactionConfirmed`: an event emitted when an owner confirms a transaction
- `event TransactionExecuted`: an event emitted when a transaction is successfully executed
- `constructor`: a constructor function to initialize the owners and the required number of confirmations
- `submitTransaction`: a function to submit a new transaction to the contract
- `confirmTransaction`: a function to confirm a transaction by an owner
- `executeTransaction`: a function to execute a confirmed transaction
- `isTransactionConfirmed`: an internal function to check if a transaction has been confirmed by the required number of owners.

The contract also includes some require statements to check for valid inputs and prevent errors or malicious behavior. The SPDX-License-Identifier is also included to specify the license under which the contract is released.
